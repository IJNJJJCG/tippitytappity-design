# tippitytappity-design

tippitytappity is a program to practice typing


## Data model

```mermaid
classDiagram
Testing your accuracy and speed
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
  class RandomPhraseGenerator {
        - wordBank: vector~string~
        + getRandomPhrase(length: int) string
        + getNextPhrase() string
  }
```
