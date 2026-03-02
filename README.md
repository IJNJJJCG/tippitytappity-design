# tippitytappity-design

tippitytappity is a program to practice typing


## Data model

```mermaid
classDiagram
  Speed <|-- Accuracy
  class Speed{
        - name: string
        - email: string
        - password: string
        + login(user: string, pass: string) boolean
        + get_email() string
  }
  class Accuracy{
        - badges vector~string~
        + add_badge(title: string)
        + get_badges() vector~string~
  }
  class History{

  }
  class Display{

  }
  class Results{

  }
  class NextPhrase{

  }
  class RandomPhraseGenerator{

  }
  class Time{

  }
```
