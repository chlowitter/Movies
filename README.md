1. clone the repsitory
2. run the setup script and add your aws credentials with us-east-1 as the region

'''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''

chmod 700 setupscript

./setupscript

'''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''

3. run these php files to setup the table and and load in the data

'''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''

php MoviesCreateTable.php

php MoviesLoadData.php

''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''

4. These files are examples of how to query the database

''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''

php MoviesQuery01.php 

php MoviesQuery02.php

''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''

5. These files are examples of updating the data

''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''

php MoviesItemOps01.php

php MoviesItemOps02.php

php MoviesItemOps03.php

php MoviesItemOps04.php

php MoviesItemOps05.php

php MoviesItemOps06.php

''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''

6. This files scans the data based on the parameters you set. It is currently set to pull all movies created between 1950 and 1959.

''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''

php MoviesScan.php

''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''





