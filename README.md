# project_lightweight
## 📁 Структура репозитория

| Файл | Описание |
|------|----------|
| `data_and_eda.ipynb` | Подготовка данных и разведочный анализ (EDA) |
| `models.ipynb` | Бенчмаркинг 7 моделей на 3 датасетах |
| `final_part.ipynb` | Анализ результатов, визуализация, SWOT |
| `FINAL_DELIVERY_ANALYST.zip` | Все результаты (CSV, PNG, отчёт) |
| `README.md` | Описание проекта и инструкция по запуску |


## 📊 Данные

Датасеты хранятся на Google Drive из-за большого размера (COCO2017 ~6GB, VisDrone ~562MB).

🔗 **Ссылка на папку с данными:** [benchmark_project](https://drive.google.com/drive/folders/1MFDlnKzoUwCKb0U17RAfzt1AH8-Zgxjg)

### Инструкция по подключению:

1. Откройте ссылку выше
2. Нажмите «**Добавить ярлык**» на свой Google Drive
3. В Colab выполните ячейку с монтированием Drive
4. Данные автоматически подгрузятся по пути `/content/drive/MyDrive/benchmark_project`

### Датасеты:

| Датасет | Изображений | Размер | Описание |
|---------|-------------|--------|----------|
| **COCO128** | 128 | ~45 MB | Быстрая отладка, подвыборка COCO2017 |
| **COCO2017** | 5,000 | ~6 GB | Основной бенчмарк (индустриальный стандарт) |
| **VisDrone** | 548 | ~562 MB | Сложный сценарий: аэросъёмка, мелкие объекты, высокая плотность |


> ⚠️ **Важно:** Без добавления ярлыка на Google Drive ноутбуки не увидят данные!
>
> ## 🎯 О проекте

В рамках проекта проведено **сравнение 7 современных lightweight-детекторов** объектов:
- YOLOv8 (nano, small, medium)
- YOLOv10 (nano, small)
- Faster R-CNN (MobileNetV3)
- SSD (MobileNetV3)

**Измеренные метрики:**
- Точность: mAP@0.5, mAP@0.5:0.95, mAP@0.75
- Скорость: FPS, средняя задержка, 95-й перцентиль

  
---

**Содержимое ZIP-архива** 

```markdown
## 📦 Содержимое FINAL_DELIVERY_ANALYST.zip

| Файл | Описание |
|------|----------|
| `FINAL_REPORT.md` | Полный отчёт с выводами |
| `benchmark_results_cleaned.csv` | Очищенные метрики (7 моделей × 3 датасета) |
| `tradeoff_analysis.png` | Точность vs скорость vs размер |
| `domain_shift_analysis.png` | Сравнение COCO2017 vs VisDrone |
| `predictions_coco2017.png` | Визуализация детекций на COCO2017 |
| `predictions_visdrone.png` | Визуализация детекций на VisDrone |
| `metrics_correlation.png` | Корреляция метрик |
| `radar_chart_top3.png` | Radar chart топ-3 моделей |
| `size_performance.png` | Качество по размерам объектов |
| `recommendation_matrix.png` | Матрица рекомендаций |
| `efficiency_ranking.png` | Рейтинг эффективности |
| `key_findings.csv` | Ключевые выводы |
