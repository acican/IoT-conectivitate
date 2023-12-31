# IoT-conectivitate
evolutie tehnologie conectivitate

Generalitati 

Asigurarea unei conexiuni internet pentru casa presupune instalarea de carte furnizorul serviciului a unui router ce asigura legatura cu lumea externa. La interior acesta da posibilitatea crearii unei retele LAN proprii la care se pot conecta prin cablu sau fara fir (wifi) dispozitivele predispuse acestei conexiuni. Conform protocolului internet acestea primesc adrese IPv4 in domeniul 192.168.0.X sau 192.168.1.X, unde X are valori intre 0 si 254. Aceste adrese sunt alocate de către router de regula in mod dinamic (de la mic la mare si disponibil) in momentul conectarii dispozitivelor prin fir sau wifi. De la exterior router-ul este vazut cu un IP a carei valoare o genereaza furnizorul conform retelei sale si care se poate schimba in timp, la reconectare de exemplu. 
Aceasta valoare o putem afla usor in momentul in care suntem conectati la internet, folosind serviciile unor site-uri dedicate, ex "my-ip". Datorita faptului ca acest IP nu este fix nu putem sa accesam sigur, de la exterior, o aplicatie sau un dispozitiv din reteaua noastra interna.
Pentru a face acest lucru trebuie fie sa ne asiguram un IP fix, daca furnizorul internet asigura acest serviciu, fie sa folosim serviciile unor site-uri specializate in rezolvarea acestei probleme, ca "no-ip" sau "dynDNS". Vorbind despre casa inteligenta (domotica sau IoT) aceasta este una din problemele cu care ne confruntam daca vrem sa controlam pe calea internetului un dispozitiv propriu sau fara suport tehnic. In mod normal insa aceste dispozitive omologate au tot suportul din partea furnizorului, ca aplicatii (de regula pe telefon) si de conectivitate internet.
Asa cum am vazut in interiorul retelei noastre avem disponiblile conexiuni prin cablu sau wifi. Cele prin cablu sunt de preferat in cauzul PC-urilor fixe sau alte dispozitive pentru care se poate cabla linia cu fir, altfel conexiunea wifi este cea de baza. Este cazul telefoanelor, PC mobile, telecamere, dispozitive pentru TV, etc. Toate acestea sunt dispozitive ce vehiculeaza un flux de date important pe care conexiunea internet wifi o asigura. 
Putem de asemenea sa ne confruntam si cu dispozitive care folosesc si o alta tehnologie de conexiune si anume bluethooth, in special in transfer de flux audio de exemplu la casti, dar si la alt fel de comunicatii. 

Standarde

In lumea dispozitivelor inteligente au intrat multe altele precum becurile, prizele, senzori de diferite tipuri, jaluzele, etc care in general nu au nevoie de transfer mare de date si nici viteza mare de comunicatie. Pentru acestea conexiunea wifi este prea mult. Astfel au aparut tehnologii de comunicatie cu banda si viteza mai mica dar si consum de putere redus, important in cazul dispozitivelor alimentate la baterie. Una dintre acestea este zigbee adoptata de marile companii ca Amazon, Samsung, Ikea. Inca din 2002 acestea au creat Zigbee Alliance in scopul sustinerii acestui standard. Dispozitivele conectate prin aceasta tehnologie sunt vazute ca noduri, ce pot fi configurate in diferite moduri de lucru, terminale, intermediare sau coordonatoare. Se pot crea retele distribuite in care nodurile intermediare pot receptiona si transmite datele de la nodurile inconjuratoare ceea ce face ca reteaua sa functioneze pe arii extinse si sa se rezolve problema obstacolelor in calea undelor radio. Pentru conectarea la reteaua internet wifi au nevoie de un hub dedicat. Prin 2014 apare un alt protocol, thread, care adopta de asemenea idea de retea distribuita bazat insa pe IPv6 (6LoWPAN), ce utilizeaza standardul de comunicatie IEEE 802.15.4 fara fir pe distante scurte. Inteconectarea cu reteaua LAN se face prin intermediul unui router edge. Sunt de asemenea si alte solutii cum ar fi Z-Wave sau bluethooth de consum mic BLE cu functii de identificare si configurare dispozitive.
Pentru controlul acestor dispozitive au aparut aplicatiile specializate, de regula pentru telefon, cunoscute fiind cele ale marilor companii ca Google, Amazon, Philips. Problema care a aparut este ca dispozitive care poate au acelasi protocol de comunicatie sa nu fie recunoscute de la o platforma la alta, daca nu au fost in prealabil preînregistrate. Asta duce in cazul folosirii mai multor unor astfel de dispozitive diverse sa fie nevoie de instalarea mai multor aplicatii, care pot crea confuzie la un moment dat. Asa ca prin 2019 apare idea unui standard comun la nivel de aplicatii numit initial "Connected Home over IP" (CHIP). In 2021 Zigbee Alliance se transforma in Connectivity Standards Alliance, iar proiectul CHIP se redenumeste "matter", urmand sa se concretizeze un satandard de comunicatie care propuna modiicarile de adoptat la difertele straturi ISO ale sistemului de comunicatie (in special nivelul aplicatie si cel de transport). In octombrie 2022 este publicata prima varianta,  "Matter 1.0". Se bazeaza pe IPv6 si pare sa avantajeze protocolul thread. Totusi dispozitivele mai vechi atât zigbee cat si thread pot sa se adapteze la acest standard prin actualizări soft de firmware.
La inceputul anului 2023 sunt anuntate dispozitive si aplicatii care sa cosespunda standardului matter. Probabil ca o sa se continue cu productia de componente specializate in care partea radio raspunde atat protocolului zigbee cat si thread chiar si BLE, asa cum apar in lista de aici, "https://www.everythingrf.com/search/rf-modules/filters?page=1&country=global&stechnology=;Thread;".

Pentru probe sunt interesante ofertele de module de test. De exemplu pentru zigbee am testat modulul Core2530(B), XBee-compatibil:

![Core2530-B_l](https://github.com/acican/IoT-conectivitate/assets/10486613/5e9a4cc2-ae17-403b-83e6-1c4ced260249)

interfata cu controler arduino :

![XBee_OutputSideCircuit-590x415](https://github.com/acican/IoT-conectivitate/assets/10486613/131f5698-ff8a-4fc3-9947-9c42457e73fd)

De interes este si kit-ul de la NORDIC semiconductor, developer board nRF52840 :

![nRF52840-DK-prod page](https://github.com/acican/IoT-conectivitate/assets/10486613/c362d1e5-a45a-4f3c-98d1-fde871bde2f6)

eventual cuplat cu NFR52840-DONGLE :

![2902521-40](https://github.com/acican/IoT-conectivitate/assets/10486613/467c17f8-edd0-42bc-b590-ff767a7b5d1d)

