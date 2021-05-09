
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

### Experience

* Development of an application for testing special devices via RS232 bus on Java 
* Development of an application for finding the most popular and rated movies (Java) in the course "Java and Android development" on Udemy. As well as the development of about 10 different applications in this course. 
* Development of a tracking stock prices app (Java), as a test task for admission to the Yandex school.
* Development of an android application for cryptocurrencies (Kotlin) as part of the course "Kotlin" on Udemy.


### Education

* Graduated from Moscow State Technical University named after Bauman
* "Full Android Course" on Udemy.com
* “Complete course  Android + Java from zero” on Udemy.com
* “Java from zero to Junior” on Udemy.com
* “Kotlin – quick start” on Udemy.com

### English

Self-tаught, level B2/Upper-Intermediate

