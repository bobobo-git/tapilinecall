# tapilinecall
call via tapi to number

[tapilinecall exe](tapilinecall.exe)  
[tapilinecall zip](tapilinecall.zip)  



technically it calls tapiRequestMakeCall with parameters



## erläuterungen dazu  

als erstes eine Warnung . Bei Manuipulationen in der WindowsRegistry ist man auf sich alleine gestellt.  
Ich übernehme keinerlei Gewährleistung über Fehler die auftreten wenn nachdem mein Programm eingesetzt wird oder auch nur wenn das hier gelesen wird.  



tapiRequestMakeCall ist ein Systemaufruf um mit einem eingetragenen Dialprogramm (*) eine angegebne Rufnummer anzurufen.  

(*) das aufgerufene DialProgramm ist von mir aus nicht so ganz eindeutig zuzuordnen.
in Computer\HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Telephony\HandoffPriorities
in RequestMakeCalls steht mal gerne DIALIT32.EXE oder auch DIALIT32.EXE"DIALER.EXE

Das wird unter Umständen genommen. auf meinem Rechner ist das so.

Auf einer eher jungfräulicehn Installation wuere bei Aufruf von tapilinecall "Rufnummer" nach einer dazu zugehörigen App gefragt.
In dem Fall war es ProCall . und das wird auch dort seitdem als dialer benutzt. obwohl auch dort das dial32 ding in der Registry steht.

Dieser Eintrag wird mutmasslich weiter unten oder oben im Prozess belegt bzw. überschrieben.

