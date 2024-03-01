def word_count(text):
    words = text.split()
    return len(words)

def longest_word(text):
    words = text.split()
    return max(words, key=len)

def count_substring(text, substring):
    return text.count(substring)

def unique_words(text):
    words = text.split()
    return len(set(words))

print("Enter a text:")
text = input()

print("\nOriginal text:")
print(text)

while True:
    print("\nText analysis options:")
    print("1. Word count")
    print("2. Longest word")
    print("3. Count of substring")
    print("4. Unique words")
    print("5. Exit")
    
    option = int(input("\nEnter a number of the analysis option (1-5): "))
    
    if option == 1:
        print("\nWord count:", word_count(text))
    elif option == 2:
        print("\nLongest word:", longest_word(text))
    elif option == 3:
        substring = input("\nEnter the substring to count: ")
        print("Count of substring:", count_substring(text, substring))
    elif option == 4:
        print("\nUnique words:", unique_words(text))
    elif option == 5:
        print("\nThank You for using the Text Processing Program")
        break
    else:
        print("\nInvalid option. Please enter a number between 1 and 5.")
