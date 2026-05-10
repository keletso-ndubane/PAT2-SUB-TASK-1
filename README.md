# PAT2-SUB-TASK-1
Morse code
 
Morse code is a method of communication that uses a series of dots (·) and dashes (–) to represent letters, numbers, and punctuation. It was widely used for long-distance communication before modern digital systems.

Morse code was developed in the early 1830s and 1840s by Samuel Morse and Alfred Vail. It was originally created for use with the telegraph, which allowed messages to be sent over long distances using electrical signals.
The first official Morse code message was sent in 1844, saying:
“What hath God wrought”
Morse code became an important communication tool, especially in:
Maritime communication (ships at sea).
Military operations.
Emergency distress signals (like SOS).

#How Morse Code Works
Morse code represents each character using a unique combination of:
Dots (·) → short signals
Dashes (–) → longer signals

Example:
Letter
Morse Code

A
· –

Timing Rules

A dot = short signal
A dash = 3 times longer than a dot
Space between parts of the same letter = short pause.
Space between letters = medium pause.
Space between words = long pause.

 Examples of Words in Morse Code
 
HELLO → ···· · ·–·· ·–·· –––

CODE → –·–· ––– –·· ·

 Importance of Morse Code
 
Even though it is not commonly used today, Morse code is still important because:

It is simple and reliable
It can be used in emergencies
It requires minimal equipment

Reference

Electronic Concept of Digital Robotics book, google and meta.

 # Morse Code Translator

This C++ program converts English text into Morse code.

#include <iostream>;
using namespace std;
int main() {
    string morse[26] = {
        ".-", "-...", "-.-.", "-..", ".", "..-.", "--.", "....",
        "..", ".---", "-.-", ".-..", "--", "-.", "---", ".--.",
        "--.-", ".-.", "...", "-", "..-", "...-", ".--", "-..-",
        "-.--", "--.."
    };

    string message;
    string fullMessage = "";

    cout << "Enter a message in English (A-Z characters only): ";
    getline(cin, message);

    cout << "\nOutput Morse code:\n";

    for (int i = 0; i < message.length(); i++) {

        char ch = toupper(message[i]);

        
        if (ch == ' ') {
            fullMessage += "   ";
            continue;
        }

        
        if (ch >= 'A' && ch <= 'Z') {

            string code = morse[ch - 'A'];

            cout << ch << ": " << code << endl;

            fullMessage += code + "   ";
        }
    }

    cout << "\nFull Morse Code Message:\n";
    cout << fullMessage << endl;

    return 0;
}
