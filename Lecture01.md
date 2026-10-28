# Cloud Computing Basics & Design Principles

---

## Cloud Kya Hota Hai

### 1. Definition

- **Cloud** ka matlab hai **internet ke zariye computing resources** (servers, storage, database, networking) **zaroorat par (on-demand)** lena.
- Apna server khareedne ki jagah hum **AWS jaisi company se rent par** lete hain.
- Hum **sirf utna paisa dete hain jitna use karte hain** (**pay-as-you-go**).
- *Misal:* Bijli ki tarah. Aap apna power plant nahi lagate, bas **bill dete ho jitni bijli use ki**.

### 2. Cloud ke faide

- **Sasta start:** pehle se mehnge hardware ki zaroorat nahi.
- **Jaldi setup:** server minutes me ready ho jata hai.
- **Zaroorat ke hisaab se kam ya zyada** kar sakte hain.
- **Duniya bhar me** kahin se bhi access.

---

## Cloud Service Models

### 1. IaaS (Infrastructure as a Service)

- AWS **laptop, servers aur storage** deta hai.
- **OS, code, hosting aur settings** user ko **khud manage** karni parti hain.
- **Sab se zyada control**, lekin **sab se zyada zimmedari** bhi user par.
- *Misal:* **Amazon EC2**

### 2. PaaS (Platform as a Service)

- AWS **infrastructure aur OS khud sambhalta hai**.
- User sirf **apna code aur app** par kaam karta hai.
- *Misal:* **AWS Elastic Beanstalk**

### 3. SaaS (Software as a Service)

- **Tayyar software** jo seedha **use** karna hota hai, kuch install ya manage nahi karna.
- **Sab se kam control**, lekin **sab se aasan**.
- *Misal:* **Gmail**, **Dropbox**

### 4. Teeno me farq

| | IaaS | PaaS | SaaS |
|---|---|---|---|
| **Control** | Sab se zyada | Darmiyana | Sab se kam |
| **User ki zimmedari** | OS, code, hosting | Sirf code aur app | Sirf use karna |
| **Misal** | EC2 | Elastic Beanstalk | Gmail |

> 💡 **Yaad rakhne ka tareeqa:** Pizza ki tarah. **IaaS** = kachha saman le kar ghar par banao, **PaaS** = tayyar dough, topping khud lagao, **SaaS** = tayyar pizza mangwa lo.

---

## Cloud Deployment Models

### 1. Cloud (All-in Cloud)

- Aap ki **poori application cloud me** chalti hai.
- Ise **cloud-based** ya **all-in cloud** bhi kehte hain.
- Apna koi physical server nahi rakhna parta.
- *Misal:* Ek **naya startup** jo sab kuch AWS par chalata hai.

### 2. On-Premises (Private Cloud)

- **Apne hi office ya data center** me servers lagana aur khud manage karna.
- Ise aksar **private cloud** bhi kaha jata hai.
- **Poora control** aap ke paas, lekin **kharcha aur maintenance zyada**.
- *Misal:* **Bank** jo apna data apne server room me rakhta hai.

### 3. Hybrid

- **Cloud aur on-premises dono ka mix.**
- Hassas data **apne server** par, baqi kaam **cloud** par.
- *Misal:* Customer ka **private data office me**, aur **website cloud par**.

### 4. Teeno me farq

| | Cloud | On-Premises | Hybrid |
|---|---|---|---|
| **Servers kahan** | AWS ke data center | Apne office | Dono jagah |
| **Control** | Kam | Zyada | Darmiyana |
| **Kharcha** | Use ke hisaab se | Pehle se zyada | Mix |

---

## Design Principles

### 1. Scalability

- System ki **barhte load ko handle** karne ki salahiyat.
- **Vertical Scaling (Scale Up):** **ek hi server ko taqatwar** banana (zyada CPU, RAM). Ek limit hoti hai.
- **Horizontal Scaling (Scale Out):** **aur servers jodna.** Ye cloud me zyada use hota hai.

| | Vertical | Horizontal |
|---|---|---|
| **Kaise** | Server bara karo | Servers ki ginti barhao |
| **Limit** | Hai | Bohat zyada |
| **Misal** | RAM 8 GB se 32 GB | 1 server se 5 servers |

### 2. Elasticity

- Load ke hisaab se **khud-ba-khud barhna aur ghatna.**
- Load kam hone par resources **wapis kam** ho jate hain, is se **paisa bachta hai.**
- *Misal:* Sale ke din **servers barh jayen**, raat ko **wapis kam.**
- **Farq:** Scalability sirf **barhne ki ability** hai, Elasticity **barhna aur ghatna dono** hai.

### 3. High Availability (HA)

- System **hamesha available** rahe aur **downtime kam se kam ho.**
- Is k liye **aksar ek se zyada jagah (multiple Availability Zones)** par system chalate hain.
- Isay percentage me napte hain, jaise **99.99% uptime.**
- *Misal:* Ek server kharab ho jaye to **doosra foran kaam sambhal le.**

### 4. Single Point of Failure (SPOF)

- Wo **ek hissa** jis ke kharab hone se **poora system band** ho jaye.
- *Misal:* Sirf **ek server** par website chal rahi ho.
- **Hal:** **Redundancy**, yani ek ki jagah **do ya zyada** rakhna.

### 5. Fault Tolerance

- Koi hissa kharab ho jaye tab bhi system **bina ruke chalta rahe.**
- Ye **High Availability se zyada mazboot** hai: HA me **thora downtime** ho sakta hai, Fault Tolerance me **koi interruption nahi.**
- *Misal:* Jahaz ke **do engine**, ek band ho to doosra jahaz ko chalata rehta hai.

### 6. Disaster Recovery (DR)

- **Bari tabahi** (data center band, aag, cyber attack) ke **baad system wapis laane** ka plan.
- Is me **backups** aur **doosre region me copy** rakhte hain.
- Do cheezein dekhi jati hain:
  - **RTO:** system **kitni jaldi wapis** chalna chahiye.
  - **RPO:** **kitne purane data tak** ka nuqsan bardasht hai.

---

## Quick Revision

| Topic | Ek line me |
|---|---|
| **Cloud** | Internet se on-demand computing, pay-as-you-go |
| **IaaS** | Infrastructure do, baqi sab khud (EC2) |
| **PaaS** | Platform do, sirf code khud (Elastic Beanstalk) |
| **SaaS** | Tayyar software (Gmail) |
| **Cloud / On-Premises / Hybrid** | Sab cloud par / sab apne paas / dono ka mix |
| **Vertical Scaling** | Server bara karna |
| **Horizontal Scaling** | Servers barhana |
| **Elasticity** | Load ke hisaab se barhna aur ghatna |
| **High Availability** | Kam se kam downtime |
| **SPOF** | Ek hissa jis se sab band ho jaye |
| **Fault Tolerance** | Kharabi par bhi bina ruke chalna |
| **Disaster Recovery** | Tabahi k baad system wapis laana |
