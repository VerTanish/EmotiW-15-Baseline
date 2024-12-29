# EmotiW-15-Baseline
Tanish Verma, 2022532

**Shortcomings**
1. Only utilised 1/4th of the data available due to limited resources, owing to some loss in accuracy.
2. To maintain consistency due to varying video lengths, only 100 frames of each video were considered for feature extraction (padding was done if frames were less), causing some loss of valuable information (again, a tradeoff).
3. In feature extraction, face detection and face alignment (affine transformation or rotation to align eyes) are used, however, the paper suggested using fiducial points (using Intraface, which is no longer available), so again some crucial information was not extracted.
4. The Confusion Matrix of chi2 SVM showed heavy imbalance in the predictions, indicating chi2 squared kernel was not appropriate, but showed somewhat better results on a standard rbf kernel. Furthermore, CNN tends to do better than SVM in multimodal classification because of spatial information, so some of the results of other approaches in the paper which utilised CNN did better than the SVM approach.
