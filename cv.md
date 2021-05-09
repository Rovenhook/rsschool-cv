
## Maxim Golovanov

*phone, whatsapp:* 
**+7-985-225-38-04**

*email:* **stuchalka8@gmail.com**

*telegram:* **Rovenhook**

### Summary

I like the idea of never ending journey to the world of self-development and having an interesting, flexible job. Programming meets the requirements perfectly. 

### Skills

Java, Kotlin, Android Studio, IntelliJ Idea, SQLite, Git, JSON, AAC (Room, LiveData, LifeCycle), Singleton, Retrofit, GSON, RxJava, MVP, MVVM, Firebase

### Code example


    @Database(entities = [CoinPriceInfo::class], version = 1, exportSchema = false)
    abstract class AppDatabase : RoomDatabase() {
        companion object {

            private var db: AppDatabase? = null
            private const val DB_NAME = "main.db"
            private val LOCK = Any()

            fun getInstance(context: Context): AppDatabase {
                synchronized(LOCK) {
                    db?.let { return it }
                    val instance =
                        Room.databaseBuilder(
                            context,
                            AppDatabase::class.java,
                            DB_NAME
                        ).build()
                    db = instance
                    return instance
                }
            }
        }

        abstract fun coinPriceInfoDao(): CoinPriceInfoDao
        
    }

