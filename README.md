# python.Readme.md
# Define a class called Source
class Source:
  # Define a constructor method that takes five parameters: name, major, year, university, and age
  def __init__(self, name, major, year, university, age):
    # Assign the parameters to the instance attributes
    self.name = name
    self.major = major
    self.year = year
    self.university = university
    self.age = age

  # Define a method called write_info that takes one parameter: filename
  def write_info(self, filename):
    # Open the file with the given filename in write mode
    file = open(filename, "w")
    # Write the instance attributes to the file in separate lines
    file.write("Name: " + self.name + "\n")
    file.write("Major: " + self.major + "\n")
    file.write("Year: " + str(self.year) + "\n")
    file.write("University: " + self.university + "\n")
    file.write("Age: " + str(self.age) + "\n")
    # Close the file
    file.close()

# Create an instance of the Source class with your information
source = Source("Buony Lam", "Computer Science", 3, "Jimma University", 27)

# Call the write_info method with the filename "readme.txt"
source.write_info("readme.txt")
