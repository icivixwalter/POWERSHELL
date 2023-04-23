GUIDA_POWER_SHELL
			
			

			
	Note
		il tutorial per powershell si trova qui:
				
			1 powershell
			https://marjolein-teepen.com/it/tutorial-powershell-per-principianti-imparare-powershell-scripting/

			2 help  Guida di Windows PowerShell(current)

			https://forsenergy.com/it-it/windowspowershellhelp/html/

			3 guida Microsofr
			https://learn.microsoft.com/it-it/powershell/module/microsoft.powershell.management/get-service?view=powershell-7.3&viewFallbackFrom=powershell-6

			ATTIVA POWERSHELL CON IL DOS
				se sei sul dos PASSA a pawershel con questo comando da terminale

				POWERSHELL
						@terminale@attiva@POWERSHELL
						@come.si.attiva@POWERSHELL
						@attiva@POWERSHELL
						@aprire@terminale@powershell_(apri il terminale con ctr+shif+t)
						@open@terminal@powershell_(apri il terminale con ctr+shif+t)
						@open@shell@dos_(apri il terminale con ctr+shif+t)

	POWER_SHELL_MICROSOFT
		Capitolo 1 - Introduzione a PowerShell
							https://learn.microsoft.com/it-it/powershell/scripting/learn/ps101/01-getting-started?view=powershell-7.3

			Prerequisiti per iniziare a usare Powershell
					Ho notato che, nella maggior parte dei casi, i relatori di meeting e conferenze hanno già PowerShell installato quando avviano presentazioni introduttive. Questo libro inizia rispondendo alle domande che ho sentito chiedere dai partecipanti che non avevano alcuna esperienza con PowerShell.

					In particolare, questo capitolo illustra come trovare e avviare PowerShell e su come risolvere alcune delle difficoltà iniziali che i nuovi utenti riscontrano con PowerShell. Assicurarsi di seguire in modo scrupoloso gli esempi presentati in questo capitolo sul computer Windows 10 dell'ambiente lab.

			Dove è possibile trovare PowerShell?
   GUIDA_WINDOWS_POWERSHELL
   					codice----> @GUIDA@PowerShell_(Guida per PowerShell)
   					@in@lavorazione_(LA GUIDA PER POWER SHELL)
   							https://forsenergy.com/it-it/windowspowershellhelp/html/defed09e-2acd-4042-bd22-ce4bf92c2f24.htm
   	1.Guida introduttiva a Windows PowerShell
   	2.Manuale dell'utente di Windows PowerShell
   					codice----> @Manuale@Utente@PowerShell@Mu_(Manuale utente)
   					codice----> @MuPs_(Manuale per Windows)
   		2.1.Nozioni di base su Windows PowerShell
   		2.2.Informazioni su Windows PowerShell
   		2.3.Concetti fondamentali di Windows PowerShell
         2.4.Utilizzo di Windows PowerShell per l'amministrazione
   					codice----> @UtlWnd_(Utilizzo per Windows)
   					codice----> @Utilizzo.di@Windows@@UtlWnd_(PowerShel per l'amministrazione)
				2.4.1.Gestione dei processi con cmdlet di tipo Process
   					codice----> @Processi@Gestione@UtlWnd_(Gestione processi)
				2.4.2.Gestione dei servizi
   					codice----> @Servizi@Gestione@UtlWnd_(Gestione dei servizi)

					Note
						Sono disponibili otto cmdlet principali di tipo Service, progettati per una vasta gamma di attività di servizio. In questo manuale verrà illustrato solo come visualizzare l'elenco dei servizi e come modificarne lo stato di esecuzione. 
						Per visualizzare un elenco completo dei cmdlet di tipo Service, utilizzare 
								Get-Help *-Service; 
									codice----> @UtlWnd@elenco@servizi_(cmdlet service per elencare i servizi)
						per visualizzare informazioni su ciascun cmdlet di questo tipo, digitare 
								Get-Help <nome-cmdlet>, 
								ad esempio Get-Help New-Service.
													@Get-Help



   	3.Argomenti della Guida "About" di Windows PowerShell
			3.1.PowerShell
					Nota
						Ottiene i processi in esecuzione nel computer locale o in un computer remoto.

					Get-Process
						@Processi@Es.3_(tutti i processi > 20 mega)
									get-process | where-object {$_.WorkingSet -gt 20000000}
						Sintassi
								Get-Process [[-Name] <string[]>] [-ComputerName <string[]>] [-FileVersionInfo] [-Module] [<CommonParameters>]
								
								Get-Process -Id <Int32[]> [-ComputerName <string[]>] [-FileVersionInfo] [-Module] [<CommonParameters>]
								
								Get-Process -InputObject <Process[]> [-ComputerName <string[]>] [-FileVersionInfo] [-Module] [<CommonParameters>]
						Descrizione
							Con il cmdlet Get-Process vengono ottenuti i processi in un computer locale o remoto.

							Senza parametri, Get-Process ottiene tutti i processi nel computer locale. È inoltre possibile specificare un determinato processo per nome o ID processo (PID) oppure passare un oggetto processo attraverso la pipeline a Get-Process.	
											@Get-Process_(restituisce i processi per  nome o per id)

							Per impostazione predefinita, Get-Process restituisce un oggetto processo che presenta informazioni dettagliate sul processo e supporta metodi che consentono l'avvio e l'arresto del processo. È anche possibile utilizzare i parametri di Get-Process per ottenere informazioni sulla versione del file per il programma in esecuzione nel processo e per ottenere i moduli caricati dal processo.

						Parametri **
								..... todo: da finire
										https://forsenergy.com/it-it/windowspowershellhelp/html/27a05dbd-4b69-48a3-8d55-b295f6225f15.htm
						Input e output **

						Note **
						Esempio 1*
						Esempio 2*
						Esempio 3*
						Esempio 4*
						Esempio 5*
						Esempio 6*
						Esempio 7*
						Esempio 8*
						Esempio 9
								Con questi comandi viene illustrato come utilizzare la variabile automatica $pid 
								per identificare il processo che ospita la sessione corrente di Windows PowerShell. 
								
								È possibile utilizzare questo metodo per distinguere il processo host dagli altri processi 
								di PowerShell che può essere opportuno arrestare o chiudere.
								
								Con il primo comando vengono ottenuti tutti i processi PowerShell nella sessione corrente. 
											get-process powershell
												@get-process_(TUTTI I PROCESSI)
								
								Con il secondo comando viene ottenuto il processo PowerShell che ospita la sessione corrente.
								(attenzione il processo viene salvata nella variabile $pid che salva il Pid)
											get-process -id $pid
												@get-process_(individua solo i processo host che ospita gli altri )

				Stop-Process
							@stop@processi_( puoi blocare i processi trovando il pid da studiare *** E FINIRE ***)
							@todo_(DA FINIRE STOP AI PROCESSI TROVANDO IL PID...)
										si trova qui:
											https://forsenergy.com/it-it/windowspowershellhelp/html/

      4.Argomenti della Guida relativi ai provider di Windows PowerShell
      5.Guida di Windows PowerShell Integrated Scripting Environment (ISE)
      6.Guida della console PowerShell.exe

	A
		Apri file
			Con il comando Invocke-item

	G
		Get-Service
			Get-Service
				Ottiene i servizi nel computer.
				comando
				   	[[-Name] <String[]>]
				   	[-DependentServices]
				   	[-RequiredServices]
				   	[-Include <String[]>]
				   	[-Exclude <String[]>]
				   	[<CommonParameters>]
		   	Descrizione
		   		Questo cmdlet è disponibile solo nella piattaforma Windows.
					
					Il Get-Service cmdlet ottiene oggetti che rappresentano i servizi in un computer, inclusi i servizi in esecuzione e arrestati. Per impostazione predefinita, quando Get-Service viene eseguito senza parametri, vengono restituiti tutti i servizi del computer locale.
					
					È possibile indirizzare questo cmdlet per ottenere solo servizi specifici specificando il nome del servizio o il nome visualizzato dei servizi oppure è possibile inviare tramite pipe oggetti servizio a questo cmdlet.

				Note varie
					visualizzi o modifichi i servizi windows
				esempio, per trovare l'elenco dei cmdlet che consentono di visualizzare e modificare i servizi di Windows, digitare:
				 	
				 	get-command *-service

			 	Dopo aver individuato il cmdlet che esegue una determinata attività, è possibile apprendere ulteriori informazioni sul relativo utilizzo mediante il cmdlet Get-Help. Ad esempio, per visualizzare la Guida sul cmdlet Get-Service, digitare:
			 		get-help get-service

		 		Per comprendere appieno l'output del cmdlet, reindirizzarne l'output al cmdlet Get-Member. Ad esempio, con il comando seguente, in cui viene utilizzato il cmdlet Get-Service, è possibile visualizzare informazioni sull'output dei membri dell'oggetto.

					get-service | get-member






				Esempio 1: Ottenere tutti i servizi nel computer

						Questo esempio ottiene tutti i servizi nel computer. Si comporta come se si digitava Get-Service *. La visualizzazione predefinita mostra la stato, il nome servizio e il nome visualizzato di ogni servizio.

							Get-Service


				Esempio 2: Ottenere i servizi che iniziano con una stringa di ricerca
					Questo esempio recupera i servizi con nomi di servizio che iniziano con WMI (Strumentazione gestione Windows).
						Get-Service "wmi*"

				Esempio 3: Visualizzare i servizi che includono una stringa di ricerca
					In questo esempio vengono visualizzati i servizi con un nome visualizzato che include la parola network. La ricerca nel nome visualizzato trova i servizi correlati alla rete anche quando il nome del servizio non include Net, ad esempio xmlprov, il servizio Di provisioning di rete.
						Get-Service -Displayname "*network*"


				Esempio 4: Ottenere i servizi che iniziano con una stringa di ricerca e un'esclusione
					Questo esempio ottiene solo i servizi con nomi di servizio che iniziano con win, ad eccezione del servizio WinRM.
							Get-Service -Name "win*" -Exclude "WinRM"


				Esempio 5: Visualizzare i servizi attualmente attivi
					In questo esempio vengono visualizzati solo i servizi con stato Running.
						Get-Service | Where-Object {$_.Status -eq "Running"}

					Get-Service ottiene tutti i servizi nel computer e invia gli oggetti nella pipeline. Il Where-Object cmdlet seleziona solo i servizi con una proprietà Status uguale a Running.

					Status è solo una proprietà di oggetti servizio. Per visualizzare tutte le proprietà, digitare Get-Service | Get-Member



				Esempio 6: Elencare i servizi nel computer con servizi dipendenti

					Questo esempio ottiene i servizi con servizi dipendenti.

							Get-Service |
							  	Where-Object {$_.DependentServices} |
							    	Format-List -Property Name, 
							    		DependentServices, @{
							      			Label="NoOfDependentServices"; Expression={$_.dependentservices.count}
							    	}
								
					Il Get-Service cmdlet ottiene tutti i servizi nel computer e invia gli oggetti nella pipeline. Il Where-Object cmdlet seleziona i servizi la cui proprietà DependentServices non è null.

					I risultati vengono inviati alla pipeline al Format-List cmdlet . Il parametro Property visualizza il nome del servizio, il nome dei servizi dipendenti e una proprietà calcolata che visualizza il numero di servizi dipendenti per ogni servizio.	

					Esempio 7: Ordinare i servizi in base al valore della proprietà
						TODO: da finire
							https://learn.microsoft.com/it-it/powershell/module/microsoft.powershell.management/get-service?view=powershell-7.3&viewFallbackFrom=powershell-6


	I
		Invoke-Item
					Esegue l'azione predefinita sull'elemento specificato.
							@Invoke_(esegue l'azione, apre il file o lo esegue)
							@powershell@esegui@file_(esegui comando powershell)
							@apri@file@invoke_(powershell esempo pri file)

			Sintassi
				Invoke-Item
			      [-Path] <String[]>
			      [-Filter <String>]
			      [-Include <String[]>]
			      [-Exclude <String[]>]
			      [-Credential <PSCredential>]
			      [-WhatIf]
			      [-Confirm]
			      [<CommonParameters>]
			      		@Invoke@Esempio_(Power shell comando invoke apertura file esempio)
			      		@Invoke@Esempio@Apri_(Con Power shell apro il progetto comandi dos)
								Invoke-Item "C:\CASA\LINGUAGGI\DOS\Progetti_DOS.sublime-project"


		      Invoke-Item
			      -LiteralPath <String[]>
			      [-Filter <String>]
			      [-Include <String[]>]
			      [-Exclude <String[]>]
			      [-Credential <PSCredential>]
			      [-WhatIf]
			      [-Confirm]
			      [<CommonParameters>]
	      Descrizione
	      			@Invoke-Item_(esegue il file )
	      	Il Invoke-Item cmdlet esegue l'azione predefinita nell'elemento specificato. Ad esempio, 
	      			esegue un file eseguibile o 
	      			apre un file di documento nell'applicazione associata al tipo di file di documento. 
   			L'azione predefinita dipende dal TIPO DI ELEMENTO e viene determinato dal provider di PowerShell che fornisce l'accesso ai dati.

	S
		Start-Process
				Esempio di apertura file
						Start-Process -FilePath "C:\Users\NomeUtente\Desktop\file.docx"


TROVARE_TUTTI_I_PROGETTI
      
        //@DOVE@SI@TROVANO.I@PROGETTI   
        //@TUTTI.I.PROGETTI_(tutti i progetti Dos, React, SublimeTex, Java, C++, Powershell ecc.)
        //----------------------------------------------------------------------------------------//
        
            Se vuoi trovare tutti progetti devi aprire la path in cui c'e il riepilo di tutti i progetti
            quali il DOS, PAWERSHELL, REACT ecc..

            Per aprire questa cartella fare riferimento a queste chiavi di ricerca:
        
            Questo è il progetto di TUTTI@PROGETTI 
            TROVA_PROGETTI.MD
            @TUTTI@I@PROGETTI_(questo è il file contiene i riferimenti a tutti progetti)
            
            Apro il progetto con TUTTI i progetti con il DOS
            Invoke-Item "c:\\CASA\\LINGUAGGI\\TROVA_PROGETTI\\TROVA_PROGETTI.sublime-project"
            
            Apro tutti i progetti con powershell
            START "apri il progetto dei comandi di TUTTI@PROGETTI" "c:\\CASA\\LINGUAGGI\\TROVA_PROGETTI\\TROVA_PROGETTI.sublime-project"
            
        //----------------------------------------------------------------------------------------//
