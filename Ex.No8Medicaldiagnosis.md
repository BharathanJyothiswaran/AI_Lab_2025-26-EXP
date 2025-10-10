# Ex.No: 8  Logic Programming –  Medical Diagnosis Expert System
### DATE:                                                                            
### REGISTER NUMBER : 
### AIM: 
Write a Prolog program to build a medical Diagnosis Expert System.
###  Algorithm:
1. Start the program.
2. Write the rules for each diseases.
3. If patient have mumps then symptoms are fever and swollen glands.
4. If patient have cough, sneeze and running nose then disease is measles.
5. if patient have symptoms headache ,sneezing ,sore_throat, runny_nose and  chills then disease is common cold.
6. Define rules for all disease.
7. Call the predicates and Collect the symptoms of Patient and give the hypothesis of disease.
        

### Program:

disease(raju, mumps) :-

symptom(raju, fever),

symptom(raju, swollen_glands).

disease(raju, measles) :-

symptom(raju, cough),

symptom(raju, sneeze),

symptom(raju, running_nose).

disease(raju, common_cold) :-

symptom(raju, headache),

symptom(raju, sneezing),

symptom(raju, sore_throat),

symptom(raju, runny_nose),

symptom(raju, chills).

disease(raju, fever) :-

symptom(raju, bodypain),

symptom(raju, cold),

symptom(raju, headache),

symptom(raju, high_temp).

symptom(raju, headache).

symptom(raju, sneezing).

symptom(raju, sore_throat).

symptom(raju, runny_nose).

symptom(raju, chills).

diagnose(Patient) :-

disease(Patient, Disease),

format('~n~w is diagnosed with ~w.~n', [Patient, Disease]), !.

diagnose(Patient) :-

format('~nNo disease could be diagnosed for ~w based on current

symptoms.~n', [Patient]).

% --- Program Entry ---

start :-

writeln('--- Welcome to the Medical Diagnosis Expert System ---'),

diagnose(raju).

### Output:

<img width="726" height="327" alt="image" src="https://github.com/user-attachments/assets/79853071-1fbc-44b0-97d1-248e4c9450bd" />


### Result:
Thus the simple medical diagnosis system was built sucessfully.
