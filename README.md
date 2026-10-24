# Mushroom Classification

Qo'ziqorinlarni zaharli (`p`) yoki zaharsiz (`e`) deb klassifikatsiya qilish loyihasi.

## Ma'lumotlar

Kaggle'dagi [Mushroom Classification](https://www.kaggle.com/datasets/uciml/mushroom-classification) ma'lumotlar to'plami: 8124 ta qo'ziqorin va 22 ta kategorik belgi. Notebook ma'lumotni to'g'ridan-to'g'ri internetdan yuklaydi.

## Jarayon

1. **Ma'lumotni tayyorlash:** NaN va dublikatlarni tekshirish, foydasiz `veil-type` ustunini olib tashlash (barcha qiymatlari bir xil), target ustunini `p → 1`, `e → 0` ko'rinishiga keltirish.
2. **Balans tekshiruvi:** 4208 zaharsiz va 3916 zaharli, ya'ni sinflar deyarli teng.
3. **Train/test bo'linishi:** `StratifiedShuffleSplit` (80/20).
4. **Kodlash:** barcha belgilar uchun `OneHotEncoder`.
5. **Modellar:** K-Nearest Neighbors, Decision Tree, Random Forest, Logistic Regression.
6. **Baholash:** Jaccard score, precision, recall, F1-score.

## Natija

| Model | Jaccard score |
|---|---|
| KNN | 1.000 |
| Decision Tree | 1.000 |
| Random Forest | 1.000 |
| Logistic Regression | 0.999 |

KNN, Decision Tree va Random Forest test to'plamida 100% natija ko'rsatdi, Logistic Regression esa 99.9%.

## Ishga tushirish

```bash
pip install -r requirements.txt
jupyter notebook mushroom_classification.ipynb
```
