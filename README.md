# Αναφορά Διορθώσεων & Παρατηρήσεων 

---

### 1.
Κάτω απο τη γραμμη 43 πρέπει να μπει 
$insertrecord->timemodified=...; απαιτείται απο την προδιαγραφή του table mdl_local_practice ωστε να γίνει ενα εστω στοιχειώδες insert στη βάση στο αρχείο /db/install.xml. Για να δουλεψει έστω το submit

### 2.
Η γραμμή redirect(new moodle_url('/local/practice/lndex.php')); είναι λάθος και δεν θα επιστρέψει τη σωστή σελίδα index.php και όχι lndex.php

### 3.
Εαν δεν υπάρχει κάποιος λόγος ωστε να εισαγουμε χθεσινή ημέρομηνία στο timecreated, τότε είναι λάθος το time()-86400.

### 4.
Εισαγουμε το firstname στο lastname στο index.php.


### 5.
Εδω υπάρχει λάθος και στο main.mustache template όπου ενω το column name ειναι Lastname φέρνει το firstname.

### 6.
Δεν ερχεται το timecreated στο template, γιατι  δεν όριζεται στο αρχείο classes/output/main.php

### 7.
Στο main.mustache template το table εχει tag <head> αντι <thead>, όμως ακολουθει με <tbody> και <tfoot>

### 8.
Το πεδίο email δεν ελεγχεται πουθενα. H class practice_form κανει extend την abstract class moodleform η οποία έχει την μεθοδο validate που μπορουμε να τη χρησιμοποιήσουμε για το email.

---