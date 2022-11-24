# tapilinecall
call via tapi to number

[tapilinecall exe](tapilinecall.exe)  
[tapilinecall zip](tapilinecall.zip)  

[tapi-wahlhilfe](tapi-wahlhilfe.zip) eine etwas erweiterte Version die das Speichern von Zeitstempeln erlaubt sowie den Anruf der letzen Nummer ohne Angabe der Nummer. 


technically it calls tapiRequestMakeCall with parameters



## erläuterungen dazu  

als erstes eine Warnung . Bei Manipulationen in der WindowsRegistry ist man auf sich alleine gestellt.  
Ich übernehme keinerlei Gewährleistung über Fehler die auftreten wenn mein Programm eingesetzt wird oder auch nur wenn das hier gelesen wird.  


tapiRequestMakeCall ist ein Systemaufruf um mit einem eingetragenen Dialprogramm (*) eine angegebne Rufnummer anzurufen.  Ansich eine Fernsteuerung, aber weas ferngesteuert wird ist nicht immer ganz eindeutig zu sagen.

(*) das aufgerufene DialProgramm ist von mir aus nicht so ganz eindeutig zuzuordnen.
in Computer\HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Telephony\HandoffPriorities
in RequestMakeCalls steht mal gerne DIALIT32.EXE oder auch DIALIT32.EXE"DIALER.EXE

Das wird unter Umständen genommen. auf meinem Rechner ist das so.

Auf einer eher jungfräulicehn Installation wurde bei Aufruf von tapilinecall "Rufnummer" nach einer dazu zugehörigen App gefragt.
In dem Fall war es ProCall . und das wird auch dort seitdem als dialer benutzt. obwohl auch dort das dial32 ding in der Registry steht.
Dieser Eintrag wird mutmasslich weiter unten oder oben im Prozess belegt bzw. überschrieben.

in Windows(10) gibt es die Möglchkeit sich die StandardApps nach Protokoll zuzuweisen. Einmal zugewiesenene kann man hier aber nicht zurücknehmen.

kein Ahnung ob das nun hilft.

Bei mir ging tapilinecall nicht mher, nachdem ich ein wenig hinundhergedreht habe (auch in der Registry) hat es dann wieder funktioniert.

Alles unbefriedigend ...

allerdings wenns geht, geht es (ne Zeitlang)


--------- Kundenrezension -----
Herzlichen Dank!  
Ich habe gestern 12 Plätze so eingerichtet, es lief gut. (*1)  
Am besten war es, immer erst den Dialer direkt aufzurufen und einen Testanruf zu machen > wenn die Leitung so funktionierte, lief es auch über Skriptaufruf einwandfrei.  

(*1)  

Dialer-batch-Datei  
```
@echo off 
set /p Rufnummer="Rufnummer einfuegen per Rechtsklick - Danach Enter"
set Rufnummer=0%Rufnummer%  
echo %Rufnummer%  
tapilinecall.exe %Rufnummer%
set Rufnummer=
```  

ich kann Erfolg vermelden.  
Habe es so zum Laufen gebracht:  

Dialer.exe aus System32 kopiert und umbenannt in Dialit32.exe, abgelegt  

