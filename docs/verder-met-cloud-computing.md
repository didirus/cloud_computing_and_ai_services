# Zelf verder met cloud computing

Dit document bevat informatie over:
- [Free Trial / Free Tier](#-free-trial--free-tier)
- [Je eigen project starten](#-je-eigen-project-starten)
- [Data Warehousing — grote datasets analyseren](#-data-warehousing--grote-datasets-analyseren)
- [AI en Machine Learning](#-ai-en-machine-learning)
- [Andere handige cloud services](#-andere-handige-cloud-services)
- [Project-ideeën](#-project-ideeën)

Na deze workshop kun je met je eigen cloud-account verder experimenteren. Alle grote cloud providers (Google Cloud, AWS, Azure) bieden vergelijkbare diensten aan.

### Free Trial / Free Tier
Gratis credits of free tiers voor nieuwe gebruikers:

**Google Cloud Platform:**
- **$300 gratis tegoed** voor 90 dagen
- Ga naar [cloud.google.com/free](https://cloud.google.com/free)
- Maak een account aan met je persoonlijke e-mailadres
- Je hebt toegang tot alle services (met creditcard voor verificatie, maar wordt niet belast)

**AWS (Amazon Web Services):**
- **12 maanden gratis** voor bepaalde services + always-free tier
- Meer info: [aws.amazon.com/free](https://aws.amazon.com/free)

**Microsoft Azure:**
- **$200 gratis tegoed** voor 30 dagen + 12 maanden gratis services
- Meer info: [azure.microsoft.com/free](https://azure.microsoft.com/free)

### Je eigen project starten
Bij alle cloud providers maak je eerst een project/account aan:

**In GCP (zoals in deze workshop):**
1. Ga naar de [Console](https://console.cloud.google.com/)
2. Klik rechtsboven op **Select a Project** → **New Project**
3. Geef je project een naam en klik **Create**
4. Let op je Project ID — die heb je nodig voor API-calls en configuratie

**In AWS:** Maak een AWS account aan, resources worden georganiseerd per *Region* en *Service*
**In Azure:** Maak een Azure account aan, resources worden georganiseerd in *Resource Groups* en *Subscriptions*

### Data Warehousing — grote datasets analyseren
Cloud providers bieden *serverless data warehouses* voor SQL-queries op grote datasets:
- **GCP:** BigQuery
- **AWS:** Athena, Redshift Serverless
- **Azure:** Synapse Analytics, Data Explorer

**Voorbeeld: BigQuery in GCP**

> **Let op:** BigQuery is niet enabled in het workshop-project. Je kunt dit uitproberen met je eigen GCP account (met free trial tegoed). In je eigen project moet je dan de BigQuery API activeren via **APIs & Services** → **Enable APIs and Services** → zoek op "BigQuery API".

**Public datasets vinden en gebruiken:**
1. Ga naar de [GCP Console](https://console.cloud.google.com/) en open **BigQuery** via het menu
2. Klik in de Explorer (linkerzijbalk) op **+ ADD** → **Public datasets**
3. Browse door datasets of zoek bijvoorbeeld op "covid", "wikipedia", "stackoverflow"
4. Klik op een dataset → **View dataset** om deze toe te voegen aan je Explorer
5. Vouw de dataset uit om tabellen te zien → klik op een tabel om het schema te bekijken
6. Klik **Query** om een query te starten

**Voorbeeld query (COVID-19 data):**
```sql
SELECT country_name
FROM `bigquery-public-data.covid19_open_data.covid19_open_data`
TABLESAMPLE SYSTEM (0.1 PERCENT)
WHERE country_name IS NOT NULL
GROUP BY country_name
LIMIT 10;
```

**Tips:**
- Gebruik **Preview** op een tabel om snel data te zien (gratis, geen query)
- Elke query toont hoeveel data wordt verwerkt (eerste 1 TB/maand is gratis)
- Bekijk de **Schema** tab om te zien welke kolommen beschikbaar zijn

**Documentatie:** [cloud.google.com/bigquery/docs](https://cloud.google.com/bigquery/docs)

### AI en Machine Learning
Alle cloud providers bieden uitgebreide AI/ML platforms:
- **GCP:** Vertex AI (zoals Colab Enterprise in deze workshop)
- **AWS:** SageMaker, Bedrock
- **Azure:** Azure Machine Learning, Azure AI Studio

**Voorbeeld: Vertex AI in GCP**

Colab Enterprise is onderdeel van het Vertex AI platform. Binnen Vertex AI kun je ook:

**Generative AI:**
- **Gemini API** — Google's multimodale AI-modellen
- **Model Garden** — toegang tot open-source modellen (Llama, Claude, etc.)
- **Prompt engineering** in de console met verschillende modellen testen

**ML-pipelines bouwen:**
- **AutoML** — train modellen zonder code te schrijven
- **Custom training** — je eigen models trainen op grote datasets
- **Workbench** — Jupyter notebooks met GPU/TPU ondersteuning

**Aan de slag:**
1. Ga naar **Vertex AI** in de console
2. Probeer de **Generative AI Studio** voor no-code experimenten
3. Bekijk de [tutorials](https://cloud.google.com/vertex-ai/docs/tutorials)

### Andere handige cloud services
Veel voorkomende service categorieën en hun equivalenten:

| Service type | GCP | AWS | Azure |
|-------------|-----|-----|-------|
| **Serverless functies** | Cloud Functions | Lambda | Azure Functions |
| **Container hosting** | Cloud Run | App Runner, Fargate | Container Apps |
| **Object storage** | Cloud Storage | S3 | Blob Storage |
| **Virtual machines** | Compute Engine | EC2 | Virtual Machines |
| **Managed databases** | Cloud SQL | RDS | Azure SQL Database |
| **NoSQL databases** | Firestore, Datastore | DynamoDB | Cosmos DB |

### Project-ideeën
Gebruik deze ideeën als startpunt voor je eigen cloud projecten (voorbeelden met GCP services, maar vergelijkbare projecten zijn mogelijk in AWS en Azure):

- **Chatbot:** Bouw een chatbot met de Gemini API en Cloud Functions (AWS: Lambda + Bedrock, Azure: Functions + Azure OpenAI)
- **Data analyse:** Analyseer grote datasets met BigQuery en visualiseer in Looker Studio (AWS: Athena + QuickSight, Azure: Synapse + Power BI)
- **Image classification:** Train een image classification model met Vertex AI AutoML (AWS: SageMaker, Azure: Azure ML)
- **Web app:** Maak een web app en deploy op Cloud Run (AWS: App Runner, Azure: Container Apps)
- **Data pipeline:** Zet een data pipeline op met Cloud Storage, BigQuery en Cloud Functions (AWS: S3 + Athena + Lambda, Azure: Blob Storage + Synapse + Functions)

