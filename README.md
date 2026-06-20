# Aryanti-Nur-Azizah_Kecerdasan-Buatan
# Diabetes Prediction using Random Forest

## Deskripsi Proyek

Proyek ini bertujuan untuk membangun model Machine Learning untuk memprediksi apakah seseorang memiliki diabetes atau tidak berdasarkan data kesehatan pasien.

Model yang digunakan dalam proyek ini adalah **Random Forest Classifier**, yaitu algoritma ensemble learning yang bekerja dengan menggabungkan banyak decision tree untuk meningkatkan akurasi prediksi.

Dataset yang digunakan adalah **Pima Indians Diabetes Dataset**, yang berisi data medis pasien seperti kadar glukosa, tekanan darah, BMI, usia, dan lainnya.

---

## Tujuan Proyek

Tujuan dari proyek ini adalah:

- Menganalisis data pasien untuk mendeteksi kemungkinan diabetes.
- Melatih model machine learning menggunakan Random Forest.
- Mengevaluasi performa model menggunakan beberapa metrik evaluasi.
- Melakukan prediksi pada data baru.

---

## Dataset

Dataset yang digunakan adalah:

**diabetes.csv**

Jumlah data: **768 baris**  
Jumlah fitur: **8 fitur**

### Fitur dalam dataset:

- Pregnancies → jumlah kehamilan
- Glucose → kadar glukosa
- BloodPressure → tekanan darah
- SkinThickness → ketebalan kulit
- Insulin → kadar insulin
- BMI → Body Mass Index
- DiabetesPedigreeFunction → faktor keturunan diabetes
- Age → usia

### Target:

- Outcome = 0 → Tidak diabetes
- Outcome = 1 → Diabetes

---

## Library yang Digunakan

```python
pandas
scikit-learn
matplotlib
```

Install library:

```bash
pip install pandas scikit-learn matplotlib
```

---

## Tahapan Proyek

### 1. Import Dataset

Dataset dibaca menggunakan pandas:

```python
df = pd.read_csv('diabetes.csv')
```

---

### 2. Preprocessing Data

Tahapan preprocessing yang dilakukan:

- Memisahkan fitur dan target
- Normalisasi data menggunakan StandardScaler

```python
X = df.drop('Outcome', axis=1)
y = df['Outcome']
```

Scaling:

```python
scaler = StandardScaler()
X = scaler.fit_transform(X)
```

---

### 3. Split Data

Data dibagi menjadi:

- 80% training data
- 20% testing data

```python
train_test_split(X, y, test_size=0.2, random_state=42)
```

---

### 4. Training Model

Model yang digunakan:

**Random Forest Classifier**

```python
model = RandomForestClassifier(n_estimators=100, random_state=42)
model.fit(X_train, y_train)
```

---

### 5. Testing dan Evaluasi

Evaluasi dilakukan menggunakan:

- Accuracy Score
- Confusion Matrix
- Classification Report

---

### 6. Prediksi Data Baru

Contoh prediksi:

```python
sample = [[6,148,72,35,0,33.6,0.627,50]]
prediction = model.predict(sample)
```

Output:

- 0 = Tidak Diabetes
- 1 = Diabetes

## Video Demonstrasi

Link Video Demo:
https://youtu.be/T2PWav4fmr4
