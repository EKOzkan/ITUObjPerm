# A Modular Architecture to Enhance Object Permanence in Object Tracking  

## 📌 Overview  
This project presents a **modular pipeline architecture** to tackle **object permanence** in object tracking — particularly in scenarios where objects become **occluded, contained, or temporarily invisible**. Instead of using an end-to-end network, this work breaks the problem into interpretable, flexible, and replaceable modules.

The system is evaluated on the **CATER dataset** and introduces two additional datasets: **CATER-Action** and **CATER-Depth**, enabling experimentation with both RGB and depth-enhanced video data.

---

## 🚀 Key Features  

### 🔹 Modular Pipeline Structure  
| Module | Purpose |
|--------|---------|
| Object Tracking | Detects and tracks visible objects using enhanced DeepSort |
| Lost Object Detection | Identifies when objects disappear |
| Depth Extraction | Extracts monocular depth using Depth Anything V2 |
| Video Classification | Classifies scenarios (occluded, contained, false) using VideoMAE |
| Location Prediction | Predicts object location during invisibility |

---

## 📂 Datasets  

### 🟢 CATER-Action  
Derived from CATER, focusing on occlusion and containment scenarios. Includes both full-scene and region-focused clips.

| Class | Number of Videos |
|--------|------------------|
| Occluded | 863 |
| Contained | 147 |
| False | 448 |

Total: **1458 videos**

### 🔵 CATER-Depth  
Includes depth-enhanced versions of CATER-Action clips using Depth Anything V2, improving spatial understanding and geometric reasoning.

---

## 📊 Experimental Results  

### 🔸 Video Classification Performance  
| Dataset | Mean Accuracy | Mean F1 Score |
|---------|---------------|---------------|
| RGB | 0.9629±0.0074 | 0.9632±0.0066 |
| Depth | 0.9356±0.0099 | 0.9338±0.0094 |

Depth-based models performed closely to RGB, showing promising utility for spatial modeling.

### 🔸 Pipeline Location Prediction Accuracy  
| Scenario | Accuracy |
|----------|----------|
| Occluded | 84.6% |
| Contained | 63.6% |
| Overall | 80% |

Best performance is achieved in occlusion cases due to stable trajectory reasoning. Containment remains a challenging task.

---

## 🧠 Key Contributions  
✔️ Proposed a **flexible modular architecture** for object permanence  
✔️ Introduced **CATER-Action** and **CATER-Depth** datasets  
✔️ Evaluated depth-enhanced classification using VideoMAE  
✔️ Improved DeepSort with object dictionary, reputation scoring, and lost object buffering  

---

## 🔍 Future Directions  
- Enhance location prediction with spatial reasoning models  
- Improve containment handling using transformer-based modeling  
- Integrate temporal embedding for better identity consistency  
- Develop depth-fused multi-modal trackers  

---

## 📝 Citation  
If you use this work, please cite:

**Özkan, E.K.**  
*A Modular Architecture to Enhance Object Permanence in Object Tracking.*

---

