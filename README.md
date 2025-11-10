**Gaussian Noise Denoising Comparison**

**1. Setup: Load image and add Gaussian noise**  
In this section, a grayscale image (cameraman.tif) is loaded and converted to a double format. Gaussian noise with standard deviation **σ = 0.04** is added to simulate sensor or transmission noise.  
**Screenshot:** Original and Noisy images.

**2. Traditional Filter (Wiener filter)**  
The **Wiener filter** is a classical adaptive method used to reduce Gaussian noise while preserving edges. It adjusts the smoothing level based on local image variance, which helps to avoid over-blurring.  
**Screenshot:** Traditional (Wiener) Filter result.

**3. AI Filter (DnCNN pre-trained network)**  
The **DnCNN model** is a deep learning-based denoising network pre-trained for Gaussian noise removal. It automatically learns complex features and typically preserves more fine detail and texture than traditional filters.  
**Screenshot:** AI (DnCNN) Filter result.

**4. Quantitative Evaluation (PSNR and SSIM)**  
**PSNR (Peak Signal-to-Noise Ratio)** and **SSIM (Structural Similarity Index)** are computed to measure the quality of the denoised images compared to the original.  
Higher **PSNR** means less noise, and higher **SSIM** indicates better structural preservation.  
Typical results:  
- **Noisy Image:** **PSNR ≈ 28 dB**, **SSIM ≈ 0.75**  
- **Wiener Filter:** **PSNR ≈ 32 dB**, **SSIM ≈ 0.85**  
- **DnCNN Filter:** **PSNR ≈ 36 dB**, **SSIM ≈ 0.90** or higher  
**Screenshot:** Command Window output showing **PSNR** and **SSIM** values.

**5. Visual Observation**  
By observing the filtered images, the **Wiener filter** effectively smooths the noise but slightly blurs edges and textures. The **DnCNN AI filter** achieves better overall restoration, maintaining sharpness and detail while removing most of the noise.  
**Screenshot:** Comparison figure with Original, Noisy, Wiener, and DnCNN results.
