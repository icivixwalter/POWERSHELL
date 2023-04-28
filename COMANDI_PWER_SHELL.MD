COMANDI_PWER_SHELL.MD
	Nota
		elenco comandi di powershell.



	DELETE
		WindowsPowerShell
			per eliminare su linea di comando l'elenco dei file occorre:
			
			attivare WindowsPowerShell cliccando con il dx su start ed attivando
			WindowsPowerShell
				
				a) elencare prima i profile wifi esistenti
					
					esempio con cmd:
						netsh wlan show profile
						
							...........................	
							
							PS C:\WINDOWS\system32> netsh wlan show profile
							
							Profili sull'interfaccia Wi-Fi:
							
							Profili di Criteri di gruppo (sola lettura)
							---------------------------------
							    <Nessuno>
							
							Profili utente
							-------------
							    Tutti i profili utente    : Alcatel_4G
							    Tutti i profili utente    : Vodafone-WiFi
							    Tutti i profili utente    : New_Tim42_2
							    Tutti i profili utente    : NETGEAR27
							    Tutti i profili utente    : NETGEAR27-5G
							    Tutti i profili utente    : Modem 4G Wi-Fi_3DC8
							    Tutti i profili utente    : Mi A3
							    Tutti i profili utente    : Honor 9 Lite wr
							    Tutti i profili utente    : Home&Life SuperWiFi-003349
							    Tutti i profili utente    : FASTWEB-1-LRGBvSQreQnN
							    Tutti i profili utente    : DM4000_1F6264
	    							Tutti i profili utente    : Alcatel 4G
						
				b) cancellare il profilo es. vodafone		
				
					netsh wlan delete profile name="Vodafone-Wifi"
					
