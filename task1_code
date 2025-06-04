#include <bits/stdc++.h>
#include <fstream>

using namespace std;

void writeToFile(const string& filename) {
    ofstream outFile(filename); // Open file in write mode (overwrites existing content)
    if (!outFile) {
        cerr << "Error opening file for writing!" << endl;
        return;
    }
    cout << "Enter text to write to the file (type 'STOP' to finish):" << endl;
    string line;
    while (getline(cin, line)) {
        if (line == "STOP") break;
        outFile << line << endl;
    }
    outFile.close();
    cout << "Data written to the file successfully!" << endl;
}

void readFromFile(const string& filename) {
    ifstream inFile(filename); // Open file in read mode
    if (!inFile) {
        cerr << "Error opening file for reading!" << endl;
        return;
    }
    cout << "Contents of the file:" << endl;
    string line;
    while (getline(inFile, line)) {
        cout << line << endl;
    }
    inFile.close();
}

void appendToFile(const string& filename) {
    ofstream outFile(filename, ios::app); // Open file in append mode
    if (!outFile) {
        cerr << "Error opening file for appending!" << endl;
        return;
    }
    cout << "Enter text to append to the file (type 'STOP' to finish):" << endl;
    string line;
    while (getline(cin, line)) {
        if (line == "STOP") break;
        outFile << line << endl;
    }
    outFile.close();
    cout << "Data appended to the file successfully!" << endl;
}

int main() {
    string filename = "example.txt";
    int choice;

    do {
        cout << "\nFile Handling Menu:\n";
        cout << "1. Write to File\n";
        cout << "2. Read from File\n";
        cout << "3. Append to File\n";
        cout << "4. Exit\n";
        cout << "Enter your choice: ";
        cin >> choice;
        cin.ignore(); // Ignore the newline left in the buffer

        switch (choice) {
            case 1:
                writeToFile(filename);
                break;
            case 2:
                readFromFile(filename);
                break;
            case 3:
                appendToFile(filename);
                break;
            case 4:
                cout << "Exiting program..." << endl;
                break;
            default:
                cout << "Invalid choice! Please try again." << endl;
        }
    } while (choice != 4);

    return 0;
}
