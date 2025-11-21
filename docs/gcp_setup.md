
# Maak kennis met de Google Cloud Platform (GCP)

Je bent toegevoegd aan een Google Cloud project waarin je met **Vertex AI Workbench** gaat werken.

## Projectgegevens
- **Projectnaam:** `vertex-ai-tutorial-project`
- **Project-ID:** `crypto-triode-477511-g4`
- **Regio:** `europe-west4 (Netherlands)`


## Stappen met uitleg

### 1. Open het project
> 💡 Een **project** (GCP) of 'account' (AWS) of 'subscription' (Azure) is een soort subdomein binnen de cloud provider waar al je resources bij elkaar staan. Elke resource (zoals een notebook, database of virtuele machine) hoort bij een specifiek project. Dit zorgt voor organisatie, kostencontrole en toegangsbeheer per project.

1. Ga naar: [https://console.cloud.google.com/](https://console.cloud.google.com/)
2. Controleer linksboven of je projectnaam overeenkomt met
   **vertex-ai-tutorial-project**.

---

### 2. Navigeer naar Workbench
> 💡 Cloud providers bieden verschillende services aan (zoals databases, AI-tools, storage). **Workbench** is een managed notebook-service binnen Vertex AI (Google's ML-platform). Je krijgt een JupyterLab-omgeving zonder lokale installatie — alles draait in de cloud.

1. Open via het zijmenu:
   **Vertex AI → Workbench**

Je komt op een pagina met de titel *"Workbench"*.

---

### 3. Open JupyterLab

Alle studenten werken samen in **één gedeelde instance**.

> 💡 Een **instance** is de compute-omgeving waarin je code draait: een virtuele machine met een bepaalde CPU, geheugen en schijfruimte. In cloud computing betaal je alleen voor wat je gebruikt: wanneer de instance draait, worden resources (CPU-tijd, opslag) toegewezen. In deze workshop delen jullie één instance om kosten te besparen, maar ieder maakt zijn eigen notebook aan.

> 💡 **Hoe werkt een notebook in de cloud?** Een notebook draait op de instance (de virtuele machine in de cloud). Notebooks worden opgeslagen op de instance, zodat je vanaf elke locatie kunt inloggen en verder werken.

> ⚠️ **Notebooks zijn alleen voor exploratie:** Gebruik notebooks uitsluitend voor exploratief werk zoals data-analyse, experimenten en prototypes. Na de development-fase verwerk je je bevindingen in een **productie-waardige Python package** met een nette mappenstructuur, modules en functies.

1. Zoek de gedeelde instance in de lijst.
4. Klik op **Open JupyterLab** naast de instance naam.

Je krijgt nu toegang tot een JupyterLab-omgeving in je browser.

---

### 5. Het JupyterLab startscherm

Wanneer je JupyterLab opent, zie je het **Launcher** venster met verschillende opties:

#### Notebook
Hier kun je een nieuwe notebook aanmaken van verschillende *kernels*:
- **Python 3**: Standaard Python 3 notebook — dit gebruik je voor de oefeningen
- **PyTorch 1-13**: Notebook met PyTorch 1.13 voorgeïnstalleerd
- **TensorFlow 2-11**: Notebook met TensorFlow 2.11 voorgeïnstalleerd

#### Console
Start een interactieve Python console (zoals een terminal binnen JupyterLab).

#### Other
Diverse opties:
- **Terminal**: Open een Linux terminal om commando's uit te voeren
- **Text File**: Maak een nieuw tekstbestand aan
- **Markdown File**: Maak een Markdown-bestand aan (voor documentatie)
- **Python File**: Maak een `.py` bestand aan (voor scripts)

#### Google Cloud Resources
Toegang tot Google Cloud services zoals Clusters, Serverless, Notebook Templates en Scheduled Jobs.


---

### 7. Maak je eigen notebook aan

> 💡 **Waarom cloud notebooks?** In de cloud draait je code op krachtige servers van bijvoorbeeld Google, in een datacenter (hier in Nederland, regio europe-west4). Je hoeft geen Python zelf te installeren en veel veelgebruikte packages (zoals pandas, scikit-learn, matplotlib, tensorflow, torch, enz.) zijn al aanwezig. Dit maakt het makkelijk om samen te werken en om zwaardere berekeningen (zoals het inladen of trainen van een model) uit te voeren dan op je eigen laptop mogelijk zou zijn.

In het linker zijpaneel vind je een bestandsbrowser waarmee je door je bestanden kunt navigeren. 

1. Navigeer naar je eigen map onder `./studenten`
1. Klik in het Launcher venster op **Python 3 (ipykernel)** onder de sectie "Notebook".

Een nieuw notebook wordt geopend. Gebruik deze tijdens de les voor je eigen experimenten.

> 💡 Tip: Je kunt meerdere notebooks tegelijk open hebben in aparte tabs.

### 8. Kopieer de oefeningen 

We gaan werken met de oefeningen die in de iPython Notebooks in de root staan. 

1. Kopieer de .ipynb bestanden van de root, door ze te selecteren, rechtermuis-knop te klikken en dan "copy".
1. Navigeer naar je eigen map onder `./studenten`
1. Plak hier de bestanden

### 7. Afronden

Aan het eind van de workshop:
- Sla je werk op (JupyterLab doet dit meestal automatisch).
- De gedeelde instance zal na vandaag stoppen en niet meer beschikbaar zijn, dus download je notebooks voor backup (via JupyterLab: rechtermuisklik op bestand → Download). 

> 💡 **Waarom instance stoppen?** In cloud computing betaal je voor de tijd dat resources actief zijn. Door de instance te stoppen wanneer iedereen klaar is, voorkom je onnodige kosten. Je notebooks blijven bewaard op de schijf, alleen de onderliggende machine wordt uitgeschakeld. Bij een volgende sessie kan de instance weer gestart worden en kun je verder werken waar je was gebleven.


---

### Veel succes!
Als iets niet lukt tijdens de workshop, controleer eerst of je in het juiste project zit (`crypto-triode-477511-g4`) en de juiste regio gebruikt (`europe-west4`).
