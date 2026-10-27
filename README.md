# IHSG-Prediction
Predicting IHSG

Alur:
1. Ambil data historis `^JKSE` dari Yahoo Finance (di-cache ke `ihsg_raw.csv`).
2. Feature engineering dari OHLCV: return & lag, moving average, RSI, volatilitas, volume, efek hari bursa.
3. Bandingkan baseline (**random walk** & **drift**) dengan 3 model ML memakai `TimeSeriesSplit` di data train.
4. Evaluasi pada holdout ±2 tahun terakhir: MAE, RMSE, MAPE, dan hit rate arah.
5. Forecast rekursif 20 hari bursa + rentang ketidakpastian, disimpan ke `ihsg_forecast.csv`.
