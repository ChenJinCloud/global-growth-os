# 🛠️ Growth Toolkit - Layer 3: Output

Reusable tools, templates, scripts, and workflows for executing growth strategies.

## 📂 What's Inside

### [excel-templates/](./excel-templates/)
Production-ready Excel/Google Sheets templates:
- **growth-model.xlsx** - Financial modeling for growth planning
- **user-cohort-analysis.xlsx** - Cohort retention and metrics analysis
- **user-acquisition-analysis.xlsx** - CAC and funnel analysis
- And more...

**Audience:** Anyone doing growth analysis, no coding required

### [python-scripts/](./python-scripts/)
Python scripts for data analysis and visualization:

**data-analysis/**
- `cohort_analyzer.py` - Generate cohort analysis from raw data
- `retention_calculator.py` - Calculate retention metrics
- `funnel_analyzer.py` - Analyze conversion funnels

**visualization/**
- `growth_charts.py` - Create growth visualizations
- `cohort_heatmap.py` - Visualize cohort retention patterns

**Setup:** See [python-scripts/README.md](./python-scripts/README.md)

### [sql-templates/](./sql-templates/)
SQL query templates for data warehouses:
- **user-metrics.sql** - Calculate user engagement metrics
- **cohort-analysis.sql** - Cohort-based retention queries
- **funnel-analysis.sql** - Conversion funnel queries

Compatible with: PostgreSQL, MySQL, BigQuery, Snowflake (with minor adaptations)

**Audience:** Data analysts, engineers with SQL knowledge

### [notion-templates/](./notion-templates/)
Notion workspace templates and databases:
- **Growth Operating System** - Master workspace template
- **Growth Experiment Tracker** - Log and track growth experiments
- **Source Library** - Organize and tag growth sources

**See [notion-templates/links.md](./notion-templates/links.md)** for direct Notion links

## 🎯 Quick Start by Role

### Growth Manager / Product Manager
- Start with: [excel-templates/](./excel-templates/)
- Then explore: [SQL templates](./sql-templates/) if you have data access
- Reference: [High-quality sources](../docs/02-methodology/high-quality-sources.md)

### Data Analyst
- Start with: [python-scripts/](./python-scripts/) for analysis workflows
- Reference: [SQL templates](./sql-templates/) for querying data
- Use: Excel templates as output formats

### Engineer / Full-Stack Growth
- Start with: [python-scripts/](./python-scripts/) and [SQL templates](./sql-templates/)
- Build upon: Create dashboards from outputs
- Reference: [Research methodology](../docs/02-methodology/research-methodology.md)

### Operations / Marketing
- Start with: [excel-templates/](./excel-templates/)
- Learn: [Growth fundamentals](../docs/01-foundation/fundamentals.md)
- Reference: [Experiment tracker](./notion-templates/) for operations

## 🔄 Typical Workflow

```
1. Define Growth Question
   ↓
2. Choose Approach (See research-methodology.md)
   ↓
3. Gather Data
   ↓
4. Use Toolkit to Analyze
   - SQL templates to query
   - Python scripts to process
   - Excel for summary analysis
   ↓
5. Create Reports & Visualizations
   ↓
6. Make Data-Driven Decisions
```

## ⚙️ Setup & Dependencies

### For Python Scripts
```bash
cd python-scripts
pip install -r requirements.txt
python cohort_analyzer.py --input data.csv
```

See [python-scripts/README.md](./python-scripts/README.md) for details

### For SQL Templates
1. Connect to your data warehouse
2. Adapt table/column names to your schema
3. Run queries and get results

See [sql-templates/README.md](./sql-templates/README.md) for database-specific notes

### For Excel Templates
1. Download template
2. Import your data
3. Charts and calculations update automatically

## 📚 Examples & Use Cases

Each tool folder includes:
- **README.md** - Setup and usage guide
- **Example inputs** - Sample data to test with
- **Expected outputs** - What results should look like
- **Customization guide** - How to adapt to your data

## 🤝 Contributing

Have a useful tool to share?

**Adding a template:**
1. Create a folder: `toolkit/[tool-type]/[tool-name]/`
2. Add your file and `README.md` with:
   - What problem it solves
   - How to use it
   - Example inputs/outputs
3. Submit a [Pull Request](../../pulls)

**See [../../CONTRIBUTING.md](../../CONTRIBUTING.md)** for full guidelines

## 📊 Toolkit Status

- Excel templates: 3+ (building)
- Python scripts: 2+ (building)  
- SQL templates: 3+ (building)
- Notion templates: 2+ (building)

**Last updated:** Sept 9, 2026  
**Build status:** 🚀 Actively building during Build in Public (Sept 10-24)

## 🚀 Next Steps

- **Want to understand growth deeply?** → [Methodology Layer](../docs/02-methodology/)
- **Have a tool to contribute?** → Submit a [PR](../../pulls)
- **Have feedback?** → Fill the [community form](https://my.feishu.cn/share/base/shrcnEvCWvO9bLifOEOVlZzlyub)

---

**Start using:** Pick your role above and start with the recommended tool
