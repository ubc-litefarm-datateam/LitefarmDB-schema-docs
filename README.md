### **📝 LiteFarmDB Schema Docs**

# LiteFarm Database Schema Documentation  

📌 **Live Documentation:** [LiteFarmDB Schema Docs](https://ubc-litefarm-datateam.github.io/LitefarmDB-schema-docs/)  

## 📖 Overview  
This repository hosts the **LiteFarm database schema documentation**, generated using **SchemaSpy**. The documentation provides an interactive view of the database structure, including **tables, relationships, and constraints**, which is useful for developers and data analysts working on the LiteFarm Dashboard.  

## 🛠 How It Was Generated  

We used **SchemaSpy**, an [open-source database schema visualization tool](https://schemaspy.org/), to generate this documentation.  

### **1️⃣ Install SchemaSpy & Dependencies**  
Before running SchemaSpy, ensure you have:  
- **Java (JDK 11 or later)**
- **PostgreSQL JDBC Driver**  
- **Graphviz** (Required for relationship diagrams)

On macOS, install dependencies using Homebrew:  
```sh
brew install graphviz
```

### **2️⃣ Run SchemaSpy**  
Use the following command to generate the schema documentation:  
```sh
java -jar schemaspy-6.2.4.jar -t pgsql \
-db pg-litefarm \
-host localhost \
-port #### \
-u readonly \
-p '<your_password>' \
-o schema_output \
-dp postgresql-42.7.5.jar
```

- **`-t pgsql`** → Specifies PostgreSQL as the database type  
- **`-db pg-litefarm`** → Database name  
- **`-host localhost`** → Database host  
- **`-port ####`** → PostgreSQL port  
- **`-u readonly`** → Database user  
- **`-p <password>`** → Password (optional, use `-p` without value for prompt)  
- **`-o schema_output`** → Output directory for generated HTML files  
- **`-dp postgresql-42.7.5.jar`** → PostgreSQL JDBC driver  

### **3️⃣ Hosting on GitHub Pages**  
Once the schema documentation was generated, we hosted it on **GitHub Pages**:  
1. Moved the `schema_output/` folder to the repository.  
2. Set up GitHub Pages under **Settings > Pages** and selected the `main` branch.  
3. The documentation is now accessible at:  
   👉 [LiteFarmDB Schema Docs](https://ubc-litefarm-datateam.github.io/LitefarmDB-schema-docs/)  

## 🚀 Future Improvements  
- Automating SchemaSpy updates when the database schema changes.  
- Adding API documentation for database interactions.  
