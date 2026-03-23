**ΠΑΡΑΤΗΡΗΣΕΙΣ**

**1)** Κάτω απο τη γραμμη 43 πρέπει να μπει _$insertrecord->timemodified=...;_ απαιτείται απο την προδιαγραφή του table _mdl\_local\_practice_ ωστε να γίνει ενα εστω στοιχειώδες insert στη βάση στο αρχείο _/db/install.xml_. Για να δουλεψει έστω το submit

**2)** Η γραμμή _redirect(new moodle\_url('/local/practice/lndex.php'));_ είναι λάθος και δεν θα επιστρέψει τη σωστή σελίδα _index.php_ και όχι _lndex.php_

**3)** Εαν δεν υπάρχει κάποιος λόγος ωστε να εισαγουμε χθεσινή ημέρομηνία στο _timecreated_, τότε είναι λάθος το _time()-86400_.

**4)** Εισαγουμε το _firstname_ στο _lastname_ στο _index.php_. 

**5)** Εδω υπάρχει λάθος και στο _main.mustache_ template όπου ενω το column name ειναι Lastname φέρνει το firstname.

**6)** Δεν ερχεται το _timecreated_ στο template, γιατι  δεν όριζεται στο αρχείο _classes/output/main.php_

**7)** Στο _main.mustache_ template το table εχει tag "<HEAD>" αντι "<THEAD>"

**8)** Το πεδίο _email_ δεν ελεγχεται πουθενα. H _class practice\_form_ κανει _extend_ την _abstract class moodleform_ η οποία έχει την μεθοδο _validate_ που μπορουμε να τη χρησιμοποιήσουμε για το _email_.
