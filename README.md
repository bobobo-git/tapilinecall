# tapilinecall
call via tapi to number

technically it calls tapiRequestMakeCall with parameters

## erläuterungen dazu  

tapiRequestMakeCall ist ein Systemaufruf um mit einem eingetragenen Dialprogramm (*) eine angegebne Rufnummer anzurufen.  

(*) das aufgerufene DialProgramm ist von mir aus nicht so ganz eindeutig zuzuordnen.
in Computer\HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Telephony\HandoffPriorities
in RequestMakeCalls steht mal gerne DIALIT32.EXE oder auch DIALIT32.EXE"DIALER.EXE

Das wird unter Umständen genommen. auf meinem Rechner ist das so.

Auf einer eher jungfräulicehn Installation wuere bei Aufruf von tapilinecall "Rufnummer" nach einer dazu zugehörigen App gefragt.
In dem Fall war es ProCall . und das wird auch dort seitdem als dialer benutzt. obwohl auch dort das dial32 ding in der REgistry steht.

Dieser Eintrag wird mutmasslich weiter unten oder oben im Prozess belegt bzw. überschrieben.


