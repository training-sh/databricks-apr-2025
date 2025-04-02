Not secure access

```
fs.azure.account.key.<STORAGE_ACCOUNT_NAME>.blob.core.windows.net <ACCESS_KEY>
```
```
spark.conf.set("fs.azure.account.key.<STORAGE_ACCOUNT_NAME>.blob.core.windows.net", "<ACCESS_KEY>")
```

```
# how to create schema programatically instead of using inferSchema
from pyspark.sql.types import StructType, LongType, StringType, IntegerType, DoubleType
```
```
# True is nullable, False is non nullable
movieSchema = StructType()\
                .add("movieId", IntegerType(), True)\
                .add("title", StringType(), True)\
                .add("genres", StringType(), True)
```
```
ratingSchema = StructType()\
                .add("userId", IntegerType(), True)\
                .add("movieId", IntegerType(), True)\
                .add("rating", DoubleType(), True)\
                .add("timestamp", LongType(), True)
```
