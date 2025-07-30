#include <iostream>
#include <string>
#include <vector>

// Enum for diabetes levels
enum class DiabetesLevel {
    NOT_DIABETIC,
    PRIMARY_DIABETES,
    SECONDARY_DIABETES,
    INSULIN_DEPENDENT,
    NON_INSULIN_DEPENDENT
};

// Struct to hold patient information
struct PatientInfo {
    std::string name;
    int age;
    int weight;
    double height;
    char sex;
};

// Class for diabetes diagnosis
class DiabetesDiagnosis {
public:
    void runDiagnosis() {
        displayWelcomeScreen();
        PatientInfo patientInfo = getPatientInfo();
        std::vector<std::string> symptoms = getSymptoms();

        DiabetesLevel diagnosis = analyzeSymptoms(symptoms);
        displayDiagnosis(diagnosis);
    }

private:
    void displayWelcomeScreen() {
        std::cout << "********* W E L C O M E *********\n";
        std::cout << " C A M P I O N S C H O O L \n";
        std::cout << " M E D I C A L D I A G N O S I S S O F T W A R E \n";
    }

    PatientInfo getPatientInfo() {
        PatientInfo patientInfo;

        std::cout << "Enter patient's name: ";
        std::getline(std::cin, patientInfo.name);

        std::cout << "Enter patient's age: ";
        std::cin >> patientInfo.age;

        std::cout << "Enter patient's weight (kg): ";
        std::cin >> patientInfo.weight;

        std::cout << "Enter patient's height (m): ";
        std::cin >> patientInfo.height;

        std::cout << "Enter patient's sex (M/F): ";
        std::cin >> patientInfo.sex;

        return patientInfo;
    }

    std::vector<std::string> getSymptoms() {
        std::vector<std::string> symptoms;

        // Get symptoms from user
        // ...

        return symptoms;
    }

    DiabetesLevel analyzeSymptoms(const std::vector<std::string>& symptoms) {
        // Analyze symptoms and return diagnosis
        // ...
        return DiabetesLevel::NOT_DIABETIC; // Example return value
    }

    void displayDiagnosis(DiabetesLevel diagnosis) {
        switch (diagnosis) {
            case DiabetesLevel::NOT_DIABETIC:
                std::cout << "The patient is not diabetic.\n";
                break;
            case DiabetesLevel::PRIMARY_DIABETES:
                std::cout << "The patient has primary diabetes.\n";
                break;
            // ...
            default:
                std::cout << "Unknown diagnosis.\n";
                break;
        }
    }
};

int main() {
    DiabetesDiagnosis diagnosis;
    diagnosis.runDiagnosis();

    return 0;
}



Output:-

![IMG_20250730_165000](https://github.com/user-attachments/assets/ab114929-38d0-42b2-b156-f38b2e5ed07f)

