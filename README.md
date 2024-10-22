# Price Movement Prediction Model with Bidirectional LSTM

## Project Overview
A deep learning model to predict binary price movements using Bidirectional LSTM architecture. The model achieved 65% accuracy with balanced performance across both upward and downward price predictions.

## Model Architecture
- Bidirectional LSTM layers for capturing temporal patterns
- Batch normalization and dropout layers for regularization
- Binary classification output (up/down movement)

## Performance Metrics
- Overall Accuracy: 65%
- Downward Movements (Class 0):
  - Precision: 0.62
  - Recall: 0.78
  - F1-score: 0.69
- Upward Movements (Class 1):
  - Precision: 0.69
  - Recall: 0.52
  - F1-score: 0.60

## Implementation Details
- TimeSeriesSplit cross-validation for temporal data
- Early stopping and learning rate reduction callbacks
- Class weighting for balanced prediction
- Batch normalization and dropout for regularization

## Requirements
```python
tensorflow>=2.0.0
pandas
numpy
scikit-learn
matplotlib
seaborn
```

## Data Characteristics
- Dataset contains property listings from Dubai and Abu Dhabi
- Primarily consists of studios and 3-bedroom apartments (75% 3-bedroom)
- Price range: 233,000 - 14,500,000 AED
- Required cleaning and logarithmic transformation of prices
- Temporal data with seasonal patterns
- Natural language processing used for text feature extraction

## Key Market Insights
- Most active areas: JVC, JVT, Reem Island, and Shamka
- Seasonal trends: Highest activity in Q1, lowest in summer months
- Price distribution: 58% properties between 500K-2M AED
- Optimal price segment: 2-4M AED (21% of listings)
- Price variations: Highest in Palm Jumeirah, lowest in Dubai South
- Premium properties: Located in Bluewaters, Saadiyat Island, Palm Jumeirah
- Summer months offer better buying opportunities
- Views (landmark/water) significantly impact property values

This dataset helps understand the UAE real estate market dynamics, pricing patterns, and optimal sales strategies, though it could benefit from more comprehensive property types and regular updates.


## Model Evaluation
The model shows:
- Stable training loss convergence
- Strong performance in identifying downward movements (78% recall)
- Conservative approach to upward movement predictions (69% precision)
- Balanced dataset handling with 49/48 class distribution

## Future Improvements
- Feature engineering with additional technical indicators
- Hyperparameter optimization
- Ensemble methods integration
- Extended validation periods

## Author
[Tanzir Hossain]

## License
This project is licensed under the MIT License - see the LICENSE.md file for details
