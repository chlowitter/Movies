<?php
require 'vendor/autoload.php';
date_default_timezone_set('UTC');
use Aws\DynamoDb\Exception\DynamoDbException;
use Aws\DynamoDb\Marshaler;
$sdk = new Aws\Sdk([
    'endpoint' => 'http://localhost:8000',
    'region'   => 'us-east-1',
    'version'  => 'latest'
]);
$dynamodb = $sdk->createDynamoDb();
$marshaler = new Marshaler();
$tableName = 'Movies';
$title = $_POST['title'];
$year = $_POST['year'];
$json = json_encode([
        'year' => $year,
        'title' => $title
    ]);
    $params = [
        'TableName' => $tableName,
        'Item' => $marshaler->marshalJson($json)
    ];
    try {
        $result = $dynamodb->putItem($params);
    } catch (DynamoDbException $e) {
        echo "Unable to add movie:\n";
        echo $e->getMessage() . "\n";
        break;
    }
?>
