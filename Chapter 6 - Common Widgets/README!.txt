Provided in the screenshot, you can see the common widgets that I have used,
including a text, input and a button

Here's some example how I created the widgets:


Text :
const Text(
  'Subject Name',
  style: TextStyle(
    fontSize: 16.0,
    fontFamily: "Sniglet",
    color: Color.fromARGB(223, 92, 203, 255),
  ),
),



Input : the customContainer is a reusable widget i can call if want a same design for inputs
customContainer(
  TextFormField(
    controller: subjectController,
    decoration: const InputDecoration(
      border: InputBorder.none,
    ),
    onChanged: (value) {
      // Handle input change
    },
  ),
),



Button : 
ElevatedButton(
  style: ElevatedButton.styleFrom(
    backgroundColor: const Color.fromARGB(224, 124, 214, 255),
    padding: const EdgeInsets.symmetric(horizontal: 14, vertical: 14),
    shape: RoundedRectangleBorder(
      borderRadius: BorderRadius.circular(20),
    ),
  ),
  onPressed: () {
    // Navigate to the next page (Schedule Page 2)
    Navigator.push(
      context,
      MaterialPageRoute(
        builder: (context) => const SchedulePage2(), // No arguments needed
      ),
    );
  },
  child: const Text(
    'View Schedule',
    style: TextStyle(
      fontSize: 16,
      color: Colors.white,
      fontFamily: "Sniglet",
    ),
  ),
),
