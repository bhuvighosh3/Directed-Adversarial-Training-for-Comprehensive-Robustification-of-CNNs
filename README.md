
 ResNet50-FGSM 
|
 74.63%  
|
 63.00%   
|
 51.16%   
|
|
 ResNet50-PGD  
|
 69.55%  
|
 56.20%   
|
 36.47%   
|
|
 ResNet50-DeepFool
|
 17.20%
|
 14.24%   
|
 12.85%   
|

#### C&W Attack Performance
|
 Model & Attack 
|
 C=0.1 
|
 C=0.3 
|
 C=0.5 
|
 C=0.7 
|
|
----------------
|
-------
|
--------
|
--------
|
--------
|
|
 VGG16-CW2     
|
 21.78%
|
 18.86% 
|
 18.15% 
|
 17.84%
|
|
 ResNet50-CW2   
|
 19.43%
|
 17.95% 
|
 17.59% 
|
 17.42%
|

### Adversarial Training Results
- **VGG16 Improvements:**
  - FGSM attack resistance: 36.30% → 62.35%
  - Clean accuracy trade-off: 92.61% → 88.61%
- **ResNet50 Improvements:**
  - FGSM attack resistance: 51.16% → 78.16%
  - Clean accuracy trade-off: 96.07% → 93.23%

## Key Findings
1. ResNet50 showed higher vulnerability to adversarial attacks despite better clean data performance
2. DeepFool and C&W attacks were most effective at reducing model accuracy
3. Adversarial training improved FGSM resistance with minimal clean data accuracy loss
4. Gradient-based attacks (FGSM, PGD) were less effective than optimization-based approaches

## Future Research Directions
1. **Advanced Training Techniques:**
   - Multi-attack adversarial training
   - Hybrid dataset exploration
   - Novel loss function development

2. **Defense Mechanisms:**
   - Real-time adversarial detection
   - Robust architecture development
   - Hardware-oriented defense strategies

## Installation and Usage
git clone https://github.com/yourusername/directed-adversarial-training
