# CS 203: Software Tools & Techniques for AI
**IIT Gandhinagar**  
**Sem-II - 2024‑25**

---

## LAB 11: Quantization Techniques
**Group 7**  
- Soham Gaonkar (23110314)  
- Chaitanya Sharma (23110172)  

**GitHub Repository:**  
https://github.com/Soham-Gaonkar/STTAI-Assignment11-QuantizationTechniques

---


## Testing & Benchmarking
| Model Type            | Model Size | Total Inference Time (s) | Test Loss | Test Accuracy |
| --------------------- | ---------: | -----------------: | --------: | ------------: |
| Full Precision (FP32) | 20.19 MB   | 0.29               | 1.1674    | 0.7875        |
| Dynamic Quantized     |  5.06 MB   | 0.28               | 1.1662    | 0.7875        |
| Half Precision (FP16) | 10.10 MB   | 0.46               | 1.1672    | 0.7875        |

For average inference time , divide total inference time by number of test samples (800)

## Key Observations
- **Accuracy:** All models (FP32, FP16, INT8) maintain identical accuracy (0.7875), indicating quantization does not degrade performance.
- **Inference Speed:** Dynamic Quantization achieves the fastest inference (~0.28 s) on CPU. FP16 is slower (~0.46 s) on hardware without specialized FP16 support.
- **Model Size:** INT8 quantization yields the smallest model (5.06 MB). FP16 halves the FP32 model size (10.10 MB), while INT8 provides the greatest storage reduction.

---

## Usage
1. **Clone the repository**  
   ```bash
   git clone https://github.com/Soham-Gaonkar/STTAI-Assignment11-QuantizationTechniques.git
   cd STTAI-Assignment11-QuantizationTechniques
