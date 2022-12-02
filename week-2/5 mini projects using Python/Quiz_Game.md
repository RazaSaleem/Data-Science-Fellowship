# Quiz Game

```python

print("Welcome to my Laptop quiz!")

playing = input("Do you want to play quiz game? ")

if playing.lower() != "yes":
    quit()

print("Okay! Let's play :)")
score = 0

answer = input("What does AI stand for? ")
if answer.lower() == "artificial intelligence":
    print('Correct!')
    score += 1
else:
    print("Incorrect!")

answer = input("What does ROM stand for? ")
if answer.lower() == "read only memory":
    print('Correct!')
    score += 1
else:
    print("Incorrect!")

answer = input("What does API stand for? ")
if answer.lower() == "application program interface":
    print('Correct!')
    score += 1
else:
    print("Incorrect!")

answer = input("What does DBMS stand for? ")
if answer.lower() == "database management system":
    print('Correct!')
    score += 1
else:
    print("Incorrect!")

print("You got " + str(score) + " questions correct!")
print("You got " + str((score / 4) * 100) + "%.")

```
