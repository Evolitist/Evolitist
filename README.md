```kotlin
fun main() {
  initProfile {
    basicData.apply {
      username = "Evolitist"
      nickname = "evo"
      fullName = "Oleg Lopukhov"
      birthDate = LocalDate(1998, 3, 31)
      occupation = Russia.Novosibirsk
    }

    employment.apply {
      current = EmploymentEntry(
        company = "Improve Group",
        position = "Android developer",
        rank = Ranks.MIDDLE,
      )
      past = mapOf(
        LocalDate(2018, 5, 4).periodUntil(LocalDate(2018, 12, 28)) to EmploymentEntry(
          company = "ATAPY Software",
          position = "Android developer",
          rank = Ranks.UNRANKED,
        ),
        LocalDate(2019, 1, 9).periodUntil(LocalDate(2020, 8, 14)) to EmploymentEntry(
          company = "ABBYY",
          position = "Android developer",
          rank = Ranks.UNRANKED,
        ),
      )
    }

    skills = mapOf(
      "Android" to Level.INTERMEDIATE,
      "Kotlin" to Level.ADVANCED,
      "Flutter" to Level.ADVANCED,
      "Dart" to Level.INTERMEDIATE,
      "Git" to Level.INTERMEDIATE,
      "Linux" to Level.ADVANCED,
      "Java" to Level.INTERMEDIATE,
      "RxJava" to Level.LEARNING,
      "Dagger" to Level.LEARNING,
      "Retrofit" to Level.INTERMEDIATE,
    )
  }
}
```
