# tippitytappity-design

tippitytappity is a program to practice typing


## Data model

```mermaid
classDiagram
Testing your accuracy and speed
Users "1" *-- "*" TestResult : has a history of
TypingSession ..> TestResult : creates a
TypingSession --> RandomPhraseGenerator : uses
  class Users{
        - username: string
        - testHistory: vector~TestResult~
        + getHistory() vector~TestResult~
        + addTestResult(result: TestResult)
  }
  class TestResult{
        - wpm: float
        - accuracy: float
        - timeElapsedSeconds: int
        - dateCompleted: datetime
  }
  class TypingSession{
        - targetPhrase: string
        - userTypedText: string
        - startTime: datetime
        - endTime: datetime
        + start()
        + end()
        + calculateWPM() float
        + calculateAccuracy() float
  }
  class RandomPhraseGenerator{
        - wordBank: vector~string~
        + getRandomPhrase(length: int) string
        + getNextPhrase() string
  }
```
