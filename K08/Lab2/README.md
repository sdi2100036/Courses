# Lab 2 - Modules, Makefile and Unit Testing

Σε αυτό το εργαστήριο θα συζητήσουμε το information hiding και το πως να οργανώσεται τον κώδικά σας σε ενότητες. Θα εξετάσουμε τα Makefile αρχεία
και την έννοια του unit testing μέσω της χρήσης της βιβλιοθήκης acutest.

## 1. Κατεβάστε τον κώδικα του εργαστηρίου

Στο κώδικα του εργαστηρίου θα βρείτε τα παρακάτω αρχεία:

- [x] `Makefile`: ένα αρχείο Makefile για τη μεταγλώττιση του κώδικα
- [x] `non_modular_list.c`: ένα αρχείο που περιέχει την υλοποίηση μιας λίστας και μια main() συνάρτηση
- [x] `test_module.c`: το αρχείο με τα unit tests για την άσκηση του εργαστηρίου

## 2. Οργάνωση του αρχείου `non_modular_list.c`

Καλείστε να δημιουργήσετε ένα module για την λίστα που είναι υλοποίημένη στο αρχέιο `non_modular_list.c`. Θα δημιουργήσετε δύο αρχείο για τη λίστα `list.c` και `list.h`  και τρίτο αρχείο `main.c` για την main() συνάρτηση του αρχείου `non_modular_list.c`.

- [ ] `list.c`: πρέπει να περιέχει οτιδήποτε αφορά την υλοποίηση της λίστας ( struct και συναρτήσεις )
- [ ] `list.h`: δήλωση των στοιχείων που θα βλέπει ο χρήστης για τη δομή ( δήλωση συναρτήσεων και typedefs )
- [ ] `main.c`: η main() συνάρτηση του αρχείου `non_modular_list.c`.

Αφού τελειώσετε, δοκιμάστε τη μεταγλώττιση του κώδικα σας με τη χρήση της εντολής `make`. Για να τρέξετε το πρόγραμμά σας εκτελέστε την εντολή `./main`. Τα αποτελέσματα του αρχείου πρέπει να είναι ίδια με αυτά του `non_modular_list.c`.

## 3. Υλοποίηση συναρτήσεων για τη λίστα

Καλείστε να υλοποίησετε τρεις συναρτήσεις στο αρχείο `list.c` ( μην ξεχάσετε την δήλωσή τους στο .h αρχείο ) :


- [ ] `List *list_prepend(List *l,int data);` : Συνάρτηση που να προσθέτει μια τιμή στην αρχή της λίστας. Η νέα τιμή πρέπει να είναι ο πρώτος κόμβος της λίστας:
- [ ] ```List *list_add_after_first(List *l,int data);``` :  Συνάρτηση που να προσθέτει μια τιμή, μετά τον πρώτο κόμβο της λίστας. Η νέα τιμή θα είναι ο δεύτερος κόμβος
- [ ] ```List *list_merge(List *l1,List *l2);```: Συνάρτηση που να ενώνει δύο λίστες σε μια, την οποία και επιστρέφει


## 4. Unit tests

Αφού υλοποιήσετε τις συναρτήσεις σας, δοκιμάσε να τρέξετε τα unit tests του αρχείου `test_module.c`. Για να κάνετε compile το αρχείο χρησιμοποιήσετε την εντολή 
`make test`. Για να τρέξετε τα test χρησιμοποιήστε την εντολή `./test`. Το πρώτο τεστ είναι υλοποιημένο και πρέπει να επιστρέφει το μύνημα [ OK ]. Καλείστε να υλοποιήσετε τα unit tests
για τις συναρτήσεις που γράψετε στο προηγούμενο ερώτημα. Μπορείτε να βασιστείτε στη συνάρτηση test_list_push(), που ελέγχει την λειτουργικότητα της συνάρτησης stack_push().

- [ ] `void test_list_prepend();`
- [ ] ```void test_list_add_after_first();``` 
- [ ] ```void test_list_merge();```


## 5. Παράδοση

Πρέπει να παραδώσετε το εργαστήριο κάνοντας `commit` και `push` στο remote repository στο github classroom. Πρέπει ο κώδικας σας να περνάει τα unit tests.
