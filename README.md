# python-project
project for basic python course
Name: Robiul Islam
Batch: Python 08


Summary:
This program offers a basic implementation of a criminal database, allowing for adding, retrieving, and listing criminal records. It demonstrates fundamental programming concepts like classes, methods, conditionals, and user input handling in Python.
Code:
class CriminalDatabase: def 	init	(self):
self.database = {}
def add_criminal(self, id, name, crime, sentence): if id not in self.database:
self.database[id] = { 'name': name, 'crime': crime, 'sentence': sentence
}
print(f"Criminal {name} added successfully.") else:
print("Criminal ID already exists.")

def get_criminal(self, id): criminal = self.database.get(id) if criminal:
print(f"ID: {id}, Name: {criminal['name']}, Crime: {criminal['crime']}, Sentence: {criminal['sentence']}")
else:
print("Criminal not found.")
def list_criminals(self): if not self.database:
print("No criminals in the database.") else:
for id, details in self.database.items():
print(f"ID: {id}, Name: {details['name']}, Crime: {details['crime']},
 
Sentence: {details['sentence']}")
# Example usage
if 		name	== "	main	": db = CriminalDatabase()
while True:
print("\nCriminal Database Menu:") print("1. Add Criminal")
print("2. Get Criminal") print("3. List Criminals") print("4. Exit")
choice = input("Enter your choice: ") if choice == '1':
id = input("Enter Criminal ID: ")
name = input("Enter Criminal Name: ") crime = input("Enter Crime: ") sentence = input("Enter Sentence: ")
db.add_criminal(id, name, crime, sentence)
elif choice == '2':
id = input("Enter Criminal ID to retrieve: ") db.get_criminal(id)
elif choice == '3': db.list_criminals()

elif choice == '4': print("Exiting the program.") break
else:
print("Invalid choice. Please try again.")
 
Enter your choice: 1 Enter Criminal ID: 20 Enter Criminal Name: X Enter Crime: Murder
Enter Sentence: Lifetime imprisonment Criminal X added successfully.

Enter your choice: 3
ID: 20, Name: X, Crime: Murder, Sentence: Lifetime imprisonment


Enter your choice: 2
Enter Criminal ID to retrieve: 25 Criminal not found.
