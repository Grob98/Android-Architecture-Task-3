# Aufgabe 3 - Lösung

### 3.1
Beantworte die folgenden Fragen:

- Wie viele Fragements werden in diesem Projekt genutzt? Benenne diese.

    1.AddEditTaskFragment
    2.StatisticsFragment
    3.TaskDetailFragment
    4.TasksFragment

- Wie viele Viewmodels werden in diesem Projekt genutzt?

    Es wird für jedes Viewmodel ein Fragment genutzt - 4.

- Welche Daten enthält das Entity von Task?

     String - "title"
     String - "description"
     Boolean - "completed"
     String - "entryid"

</br></br>

### 3.2 
Starte die App im Emulator und erstelle einen beliebigen neuen Task.
Führe folgende Sachen aus:

- Minimiere die App und öffne sie anschließend wieder.
- Beende die App komplett und starte die App anschließend neu.

Was fällt dir in Bezug auf den Lebenszyklus auf?

    Bei Minimieren und wieder Öffnen werden die Tasks durch das Viewmodel beibehalten, aber beim Beenden der App verlieren wir alle Tasks.

    Um dieses Problem zu beheben, müssten wir die Datenbank anpassen, damit die Daten beim Neustart wieder eingelesen werden können.


</br></br>

### 3.3
Zuerst erstelle erneut einen beliebigen neuen Task. 

Wir haben einen Fehler in der App entdeckt. Wenn wir uns in den Task Details befinden und den Task entfernen möchten, dann gelangen wir wieder zurück in die Übersicht, aber der Task wurde nicht gelöscht.

Finde den Fehler und korrigiere ihn. 


Der Fehler ist in der Zeile 68 im TaskDetailViewModel zu finde. Durch das einfügen der Zeile "tasksRepository.deleteTask(it)" können wir das Problem beheben.