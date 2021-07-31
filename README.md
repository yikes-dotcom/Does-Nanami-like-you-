# Does-Nanami-like-you-
#Just a fun quiz Ashley and I did for class
print("[Nanami Judgement Program]")
#Written in collaboration with Ashley Molina 
#Refernces made to Jujutsu Kaisen. Directed by Sunghoo Park, Studio MAPPA, Oct 3, 2020 to Mar 27, 2021, accessed on Apr 3,2021"

print("\nFind out how Kento Nanami feels about you with ONE question!")

print()

acceptableSuits = ['Beige', "Scarlet", "Black"]

suitQuestion = input("What color suit do you think fits Nanami? (answer with the color name!)\n(a) Beige\n(b) Scarlet\n(c) Black\n(d) Gojo Satoru\n\nYour answer: ").title()

print()

def judgementQuiz(guess, acceptablecolors):
    numofTries = 0
    gojoCounter = 0
    while numofTries != 3:
        if guess.isalpha():
            if guess in acceptablecolors:
               print("Nanami: Hm,", guess + ".", "I suppose you do have taste...")
               print("\nNarrator: You've impressed him!")
               break
            else:
                print("\nNanami: While", guess, "is an alright color, it isn't my favorite, please try again.")
                guess = input("Narrator: What color do you think the suits Nanami?: ").title()
                numofTries += 1
        else:
            if guess == "Gojo Satoru":
                print("\nNanami: ... Did he put you up to this?")
                guess = input("You may try again... \n\n").title()
                numofTries += 1
                gojoCounter += 1
                if gojoCounter > 1:
                    print("\nNanami: No.")
                    print("\nNarrator: Uh oh! Seems like Nanami has stepped out of the program!")
                    numofTries += 1
                    break
            else:
                print("\nSuit colors don't consist of numbers.")
                guess = input("Try again... ").title()
                numofTries += 1

judgementQuiz(suitQuestion, acceptableSuits)
