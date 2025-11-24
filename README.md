# Fundamental-in-ai-and-ml
THIS PROJECT HELPS YOU TO GUIDE THROUGH THE SYMPTOMS OF COVID AND TELL YOU THE MEASURES OF PRECAUTION
% COVID PREDICTOR
%  ASK USER NAME
amihavingcovid:-
    write('What is your NAME: '), read(INPUT), write('Welcome to COVID DETECTOR'), write(INPUT), write('!'), nl, symptoms_are.
%--------display SYMPTOMS---------
symptoms_are :-
    nl, write('SELECT SYMPTOM :'), nl, write('1. [Fever]'), nl,  write('2. [Dry_cough]'), nl,  write('3. [Shortness_of_breath]'), nl,  write('4. [Fatigue]'), nl,  write('5. [Muscle_aches]'), nl,  write('6. [Headache]'), nl,  write('7. [Sore_throat]'), nl,  write('8. [Runny_nose]'), nl,  write('9. [Loss_or_change_of_taste_or_smell]'), nl,  write('10. [Nausea]'), nl, nl, read(Choice), symptoms(Choice).

%-----SYMPTOM FACTS-----
symptoms(1):- user_have(fever).
symptoms(2):- user_have(dry_cough).
symptoms(3):- user_have(shortness_of_breath).
symptoms(4):- user_have(fatigue).
symptoms(5):- user_have(muscle_aches).
symptoms(6):- user_have(headache).
symptoms(7):- user_have(sore_throat).
symptoms(8):- user_have(runny_nose).
symptoms(9):- user_have(loss_or_change_of_taste_or_smell).
symptoms(10):- user_have(nausea).
symptoms( ):-
    write('invalid choice, try again,'), nl, symptoms_are.
%symptom facts
symptom(fever).
symptom(dry_cough).
symptom(shortness_of_breath).
symptom(fatigue).
symptom(muscle_ache).
symptom(headache).
symptom(sore_throat).
symptom(runny_nose).
symptom(loss_or_change_of_taste_or_smell).
symptom(nausea).
%symptom confirmer
user_have(X):-
    symptom(X), write('##SYMPTOM DETECTED:'), write(X), nl, write('{you might be infected},'), nl, write('{avoid social contacts},'), nl, write('{eat healthy and avoid junk food},'), nl, write('{see a doctor quickly},'), nl, write('!').
