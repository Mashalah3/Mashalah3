# 🚀 Questo progetto è nelle sue prime fasi di sviluppo.
# 📌 Al lavoro su nuove funzionalità e menu principale.
# ⚠️ Eventuali domande o suggerimenti si prega di inviare a: hendriksdevmail@gmail.com
# 🖥 Versione: 1.0.2

dal  webdriver di importazione del selenio  
 avvisi di importazione
 tempo di importazione
importa  casuale
 stringa di importazione
 richieste di importazione
importa  csv
 sistema di importazione
 sistema operativo di importazione
chiaro  =  lambda : os . sistema ( 'chiaro' )
chiaro ()
io  =  0
#Opzioni
#--------------
Opzioni #Emial
#--------------
auto_email  =  "vero"


stampa ( """ \
_____ _ _ _____ _              
|_ _(_) ||_ _| | |             
  | | _| | _| | ___ | | __          
  | | | | |/ / |/ _ \| |//          
  | | | | <| | (_) | <           
  \_/ |_|_|\_\_/\___/|_|\_\                                                                               
  ___ _   
/ _ \ | |  
/ /_\ \ ___ ___ ___ _ _ _ __ | |_
| _ |/ __/ __/ _ \| | | | '_ \| __|
| | | | (_| (_| (_) | |_| | | | | |_
\_| |_/\___\___\___/ \__,_|_| |_|\__|                                                                    
_____ _              
/__\| |             
| / \/_ __ ___ __ _| |_ ___ ___  
| | | '__/ _ \/ _` | __/ _ \| '__|
| \__/\ | | __/ (_| | || (_) | |    
\____/_| \___|\__,_|\__\___/|_|    
                                       
""" )
profilo  =  webdriver . Profilo Firefox ()
profilo . set_preference ( "general.useragent.override" , "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_5) AppleWebKit/537.36 (KHTML) Chrome/83.0.4103.97 Safari/537.36" )
profilo . set_preference ( "media.volume_scale" , "0.0" )
profilo . set_preference ( "dom.webdriver.enabled" , Falso )
profilo . set_preference ( 'useAutomationExtension' , False )
profilo . update_preferences ()
webdriver  =  webdriver . Firefox ( executable_path = "./geckodriver" , firefox_profile = profilo )
driver  =  webdriver
# Cambia percorso in Chrome Driver Path (o sposta ChromeDriver nella cartella del progetto)

url  =  'https://www.tiktok.com/signup/phone-or-email/email'

def  randomStringDigits ( stringLength = 13 ):
    # Genera una stringa casuale di lettere e cifre
    lettereAndDigits  =  stringa . lettere_ascii  +  stringa . cifre
    ritorno  '' . join ( random . choice ( lettersAndDigits ) for  i  in  range ( stringLength ))
rngpassword  =  randomStringDigits ( 15 )
autista . ottenere ( URL )
tempo . dormire ( 5 )
#Cambia lingua
stampa ()
stampa ( "Impostazione della lingua in inglese" )
autista . find_element_by_xpath ( '/html/body/div[1]/div/div[2]/div[2]/div[1]/select' ). fare clic su ()
tempo . dormire ( 1 )
autista . find_element_by_xpath ( '/html/body/div[1]/div/div[2]/div[2]/div[1]/select/option[4]' ) . fare clic su ()
tempo . dormire ( 1 )

#Impostazione della data di nascita
#Setting Mese
stampa ()
stampa ( "Impostazione del mese di compleanno" )
autista . find_element_by_xpath ( '/html/body/div[1]/div/div[1]/form/div[2]/div[1]/div' ) . fare clic su ()
tempo . dormire ( 1 )
autista . find_element_by_xpath ( '/html/body/div[1]/div/div[1]/form/div[2]/div[1]/ul/li[1]' ) . fare clic su ()
tempo . dormire ( 1 )

#Giornata del setting
stampa ()
stampa ( "Impostazione del giorno del compleanno" )
autista . find_element_by_xpath ( '/html/body/div[1]/div/div[1]/form/div[2]/div[2]/div' ) . fare clic su ()
tempo . dormire ( 1 )
autista . find_element_by_xpath ( '/html/body/div[1]/div/div[1]/form/div[2]/div[2]/ul/li[1]' ) . fare clic su ()
tempo . dormire ( 1 )

#Impostazione dell'anno
stampa ()
stampa ( "Impostazione dell'anno di compleanno" )
autista . find_element_by_xpath ( '/html/body/div[1]/div/div[1]/form/div[2]/div[3]/div' ) . fare clic su ()
tempo . dormire ( 1 )
autista . find_element_by_xpath ( '/html/body/div[1]/div/div[1]/form/div[2]/div[3]/ul/li[20]' ) . fare clic su ()
tempo . dormire ( 1 )

#Impostazione dell'indirizzo e-mail
stampa ()
stampa ( 'Impostazione dell'indirizzo e-mail' )
se  auto_email  ==  "vero" :
    get_response  =  richieste . get ( "https://lazy-mail.com/mailbox/create/random" )
    csrf_token  =  get_response . testo . split ( "tipo di input= \" nascosto \" name= \" _token \" valore= \" " )[ 1 ]. split ( " \" " )[ 0 ]
    post_data  = { "_token" : csrf_token }
    post_response  =  richieste . post ( "https://lazy-mail.com/mailbox/create/random" , data = post_data , cookies = get_response . cookies )
    email_generata  =  post_risposta . URL . diviso ( "casella di posta/" )[ 1 ]
    autista . find_element_by_xpath ( "/html/body/div[1]/div/div[1]/form/div[4]/div[2]/div/input" ) . send_keys ( generato_email )
altro :
    e-mail  =  input ( "Inserisci la tua e-mail: " )
    autista . find_element_by_xpath ( "/html/body/div[1]/div/div[1]/form/div[4]/div[2]/div/input" ) . send_chiavi ( email )
tempo . dormire ( 1 )

#Impostazione password
stampa ()
print ( "Impostazione password: {}" . format ( rngpassword ))
autista . find_element_by_xpath ( '/html/body/div[1]/div/div[1]/form/div[4]/div[4]/div[1]/input' ) . send_keys ( rngpassword )
tempo . dormire ( 1 )

#Invio di e-mail
stampa ()
stampa ( "Invio di email" )
autista . find_element_by_xpath ( '/html/body/div[1]/div/div[1]/form/div[4]/div[5]/button' ) . fare clic su ()
tempo . dormire ( 1 )

#In attesa di codice
stampa ()
stampa ( "In attesa di codice" )
se  auto_email  ==  "vero" :
    mentre ( vero ):
        get_email  =  richieste . get ( "https://lazy-mail.com/mail/fetch?new=true" , ​​cookies = post_response . cookies )
        get_email  =  richieste . get ( "https://lazy-mail.com/mail/fetch" , cookies = post_response . cookies )
        se  "Codice di verifica"  non è  in  get_emails . testo :
            tempo . dormire ( 10 )
        altro :
            get_code  =  ottieni_email . testo . split ( "ext \" : \" Per verificare il tuo account, inserisci questo codice in TikTok:<br\/>" )[ 1 ]. diviso ( " \" " )[ 0 ]
            rottura
    autista . find_element_by_xpath ( '/html/body/div[1]/div/div[1]/form/div[4]/div[5]/div/input' ) . invia_chiavi ( get_code )
altro :
    code  =  input ( 'Inserisci codice ricevuto via email: ' )
    autista . find_element_by_xpath ( '/html/body/div[1]/div/div[1]/form/div[4]/div[5]/div/input' ) . send_keys ( codice )
