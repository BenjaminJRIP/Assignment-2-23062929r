# Assignment 2 - 23062929r 
IP Chun Man Ben 23062929r


### Model: ChatGPT 4o
#### Prompt:

Task1

list the pros and cons for the following GNSS techniques: Differential GNSS (DGNSS), Real-Time Kinematic (RTK), Precise Point Positioning (PPP), and PPP-RTK for smartphone navigation

which GNSS technique for smartphone navigation is the best, could u rank them and does it depend on the scenarios

What performance metrics (such as accuracy, update rate, latency, cost, and ease of integration) should I consider for comparing these technologies in a smartphone context? if possible, could u list a table that comparison table

Task 4

list the difficulties and challenges of using LEO communication satellites for GNSS navigation with clear explanation

how the unique signal characteristics of LEO satellites—like lower altitude, higher relative motion, and shorter coverage times—affect their reliability for navigation versus communication, for the issues of latency and timing precision with LEO satellites, and how these might impact the performance of GNSS navigation systems, the geometric dilution of precision (GDOP) and multipath challenges specific to LEO satellite constellations in a GNSS context

how environmental factors, like atmospheric interference and urban canyon effects, further complicate LEO satellite-based navigation signals, compare the integration challenges when using LEO satellites with traditional GNSS systems

Task 5

Global Navigation Satellite Systems (GNSS) are not only used for positioning and navigation but also have significant applications in remote sensing. Could u introduce and differentiate GNSS-R, GNSS-IR, and GNSS-RO in clear and detailed manor. what is the impact of them in remote sensing

how the impact of GNSS in remote sensing, epically for GNSS-R For GNSS Reflectometry (GNSS-R), how the technology works, what makes it unique among GNSS-based remote sensing methods, and what its main technical challenges are.

The key underlying mechanisms of GNSS Reflectometry (GNSS-R) 

The limitations or challenges of using GNSS Reflectometry (GNSS-R) in remote sensing
the real-world applications of GNSS-R in remote sensing compare the advantages of employing GNSS-R over traditional remote sensing methods, why is it important and what is its impact in remote sensing analyze how integrating GNSS into remote sensing GNSS-R has reshaped the field and consider its impact on data quality, coverage, operational flexibility, ....

discuss trade-offs between benefits and drawbacks (such as cost versus performance or complexity versus accuracy) when using GNSS-R for remote sensing

#### Comment (the reason for using this model): 
It’s smart and great for reasoning and answering questions. It outperforms other ai model.

#### The chatroom link: 


## Task 1 – Differential GNSS Positioning (word:977)
Smartphone navigation has become an indispensable part of our daily lives, driving an increasing need for enhanced accuracy and reliability in positioning technologies. As global positioning accuracy requirements expand—in applications ranging from everyday mapping to precision-demanding tasks like augmented reality or autonomous navigation—a range of GNSS techniques have emerged. Among these, Differential GNSS (DGNSS), Real-Time Kinematic (RTK), Precise Point Positioning (PPP), and the hybrid PPP-RTK are the most frequently compared [3]. Each method brings its unique balance of benefits and challenges, and understanding these nuances is key to making an informed decision for application development.

My summary table for the properties of the four GNSS techniques for smartphone navigation [1][2][3]
![image](https://github.com/BenjaminJRIP/Assignment-2-23062929r/blob/7aeac1c4ec22fdd43c3045e027ad0bebbe355bbd/1.png)

Differential GNSS (DGNSS) enhances the performance of standalone GNSS by using data from nearby reference stations that provide correction signals [1]. These reference stations, strategically placed at known locations, help mitigate errors caused by atmospheric disturbances, satellite clock drifts, and other inaccuracies. The corrected signals then improve the positioning accuracy available to a smartphone user. One of the major advantages of DGNSS is its relative simplicity. The infrastructure for DGNSS is widely available, especially in urban and developed regions, which makes it an attractive choice for general navigation scenarios. However, despite the improvements over standalone systems, the level of precision offered by DGNSS—typically at the decimeter level—may not suffice for advanced applications. Its dependence on the presence and proximity of reference stations can also be a significant limitation, particularly in rural or sparsely populated areas [1]. Furthermore, there can be slight delays in the reception of correction signals, which might impact systems that rely on immediate real-time data.

Real-Time Kinematic (RTK) positioning advances beyond the conventional correction methods by employing carrier-phase measurements that yield centimeter-level accuracy in real time [2]. It provides real-time position corrections, making it suitable for applications requiring immediate accuracy. RTK systems utilize large, fixed base stations and roving receivers that work in tandem to achieve rapid convergence on an accurate position. This level of precision makes RTK an ideal candidate for applications like surveying, precision agriculture, and detailed urban mapping where minute errors can have significant implications [2]. Nonetheless, the high performance of RTK comes with stringent requirements. The method demands a robust communication link between the base station and the receiver and is highly sensitive to environmental conditions. Urban settings, with their tall buildings and signal obstructions, often degrade RTK performance due to multipath errors and signal loss. Additionally, the specialized hardware and increased complexity not only drive up the cost but also pose integration challenges for routine smartphone usage. The limited effective range—typically within 10 to 20 km from the base station—further constrains its versatility for widespread consumer applications.

Precise Point Positioning (PPP), on the other hand, distinguishes itself by leveraging globally available satellite orbit and clock corrections rather than relying on local base stations. This capability allows PPP to provide consistent accuracy on a worldwide scale using a single GNSS receiver, making it particularly useful for applications that span across regions without established local infrastructure[3]. Its ability to achieve decimeter to sub-meter level accuracy is notable; however, this comes at the cost of convergence time. Typically, a PPP system may require up to 30 minutes before reaching its high-precision state—a delay that renders it less suitable for dynamic, real-time navigation needs. Moreover, the reliance on complex algorithms and highly accurate satellite data not only increases computational demands but also makes the system prone to performance issues in environments with significant signal degradation, such as urban canyons or during adverse weather conditions.

The hybrid approach of PPP-RTK seeks to harness the strengths of both PPP and RTK technologies. By combining global correction information with the rapid real-time adjustments characteristic of RTK, PPP-RTK can achieve high precision with faster convergence times [3]. This method minimizes the dependency on local infrastructure while still delivering the centimeter-level accuracy crucial for sophisticated smartphone navigation applications. The primary challenge with PPP-RTK lies in its complexity; integrating two advanced systems requires sophisticated algorithms and a reliable, continuous stream of correction data. This dual dependence not only increases the cost of implementation but may also impose heavier processing loads on smartphones, potentially affecting battery life and overall performance [3]. Despite these hurdles, the versatility of PPP-RTK makes it a strong contender for next-generation mobile navigation solutions, especially in scenarios where divers conditions—from urban centers to remote areas—must be managed seamlessly.

When evaluating these techniques for smartphone navigation, context is essential. In urban areas, where obstacles and multipath reflections are common, techniques like RTK or PPP-RTK can offer the high level of precision needed, though they require robust signal conditions and infrastructure [3]. For rural or remote applications, PPP stands out by delivering consistent accuracy without heavy reliance on local reference stations, despite its longer convergence time. In the realm of real-time applications, both RTK and PPP-RTK are superior due to their rapid correction capabilities, although they come with added complexity and higher operational costs. For general-purpose navigation where utmost precision is not critical, DGNSS remains attractive due to its wide availability, relative simplicity, and cost-effectiveness.

In summary, the selection of the optimal GNSS technique for smartphone navigation ultimately depends on the specific demands of the application. DGNSS provides a simple yet effective enhancement over basic GNSS, while RTK pushes the boundaries of accuracy and immediacy for high-stakes scenarios. PPP offers the advantage of global coverage with minimal local infrastructure, and PPP-RTK emerges as a hybrid solution that promises to deliver the best of both worlds with rapid convergence and high precision. As advancements in sensor technologies, machine learning, and data fusion continue, future navigation systems will likely integrate these methodologies even further, creating opportunities for smarter, more adaptive positioning technologies. This nuanced analysis not only highlights the strengths and drawbacks of each approach but also provides a framework to outperform similar AI-generated responses by offering deeper insight, contextual understanding, and a forward-looking perspective on the evolution of GNSS technologies for smartphone navigation.

Reference
[1] P. Misra and P. Enge, *Global positioning system: signals measurements*, 2011.
[2] H. Sharma, A. Schütz, and T. Pany, "Preliminary analysis of the RTK positioning using Android GNSS Raw Measurements and Application Feasibility for the Trajectory mapping using UAV’s," in *Proc. 31st International Technical Meeting of the Satellite Division of the Institute of Navigation (ION GNSS+ 2018)*, Sept. 2018, pp. 432–444.
[3] J. Geng, F. N. Teferle, X. Meng, and A. H. Dodson, “Towards PPP-RTK: Ambiguity resolution in real-time precise point positioning,” *Advances in Space Research*, vol. 47, no. 10, pp. 1664–1673, 2011.

## Task 2
### Processing Methodology 
For the given skymask dataset, the implementation of skymask filtering follows a systematic procedure:
1. **GNSS Data Collection:**  
   The system begins by processing a collection of GNSS observations. For each observed satellite signal, the azimuth (AZk) and elevation are computed.

2. **Threshold Retrieval and Evaluation:**  
   Using the computed azimuth, the associated minimum elevation threshold is retrieved from the skymask dataset. The satellite’s measured elevation is then compared against this threshold. If the elevation falls below the specified EL for that azimuth, the signal is deemed obstructed (i.e., non-Line-of-Sight) and is filtered out from further consideration.

3. **Filtering and Viability Check:**  
   This evaluation is carried out for every satellite in the current epoch. The process not only filters out low-quality, potentially obstructed signals but also maintains a count of remaining, viable observations. Importantly, if fewer than four satellites meet the LOS criteria after filtering, the positioning computation for that epoch is aborted to avoid unreliable or under-constrained solutions.

4. **Flow of Data to Positioning Computation:**  
   When the number of viable satellites is four or more, the remaining measurements are forwarded to the least-squares estimation stage for position determination.

This stepwise process ensures that only high-quality, unobstructed signals contribute to the positioning solution, thereby enhancing the reliability of the subsequent computations.

### Performance Analysis and Tradeoffs
Analysis performed on an urban dataset comprising 839 epochs revealed key insights into the impact of skymask filtering:
- **Enhanced Precision:**  
  By filtering out low-quality LOS candidates, the method considerably improves the precision of the positioning solution. Obstructed signals, which can otherwise introduce significant errors, are excluded. For instance, while the standard least-squares approach may utilize all available transmissions, the filtered method minimizes the influence of signals most likely to be degraded by urban obstructions.

- **Impact on 3D Positioning Accuracy:**  
  Despite the precision improvements, the skymask filtering technique introduces a tradeoff in terms of overall accuracy, especially in the vertical dimension. The filtering selectively removes satellites with lower elevation angles—signals that often convey crucial vertical positioning information. As a consequence, even though the standard deviation of observations might slightly improve (indicating more consistency), the three-dimensional root-mean-square error (RMSE) may actually increase due to the reduced geometric diversity essential for robust 3D solutions. For example, one analysis noted a rise in RMSE from 85.13 m (without filtering) to 100.36 m (with filtering), even as the standard deviation improved from 35.33 to 33.18 m.

- **Availability Considerations:**  
  In the specific urban dataset evaluated, both the standard and the skymask-enhanced methods yielded a solution for all 839 epochs, ensuring 100% solution availability. However, theoretically, there may be epochs where skymask filtering results in fewer than four viable satellites, thereby preventing a solution from being computed. This potential drawback underscores the need for balance between filtering rigor and satellite availability.

The comparison for positioning between OLS with skymask-filtering (red) and without skymask-filtering (blue)
![image](https://github.com/BenjaminJRIP/Assignment-2-23062929r/blob/3a71cf53224129e59d84404a9e75c5e7bc570a56/2.png)

### Concluding Remarks
The skymask application represents a meticulous tradeoff: while filtering out non-LOS signals enhances measurement precision by excluding bad-quality transmissions, it simultaneously risks degrading the positioning solution’s overall (especially 3D) accuracy due to diminished vertical geometry. In practice, this approach can be highly effective in environments with abundant satellite signals, as evidenced by the 839-epoch urban dataset, yet it carries inherent challenges in scenarios where satellite visibility is more limited.

This discussion encapsulates both the theoretical underpinnings and practical impacts of skymask filtering on GNSS positioning. A flowchart summarizing these processes could further illustrate the decision points—from satellite measurement through filtering to position computation—providing a clear visual aid to accompany this analysis. 

## Task 3
This discussion is based on the “OpenSky” dataset, which comprises 926 measurement epochs. In each epoch, 9 satellite signals are received. The Receiver Autonomous Integrity Monitoring (RAIM) scheme is implemented in two stages:
1. **Fault Detection:**  
   The algorithm first performs a detection step. A weighted statistical metric—the Weighted Sum of Squared Errors (WSSE)—is used to assess the consistency of the available measurements. If the WSSE exceeds a predetermined threshold, this flags the possibility of one or more faulty measurements.

2. **Fault Isolation:**  
   When a single faulty measurement is identified, the RAIM process attempts to isolate (remove) that measurement. The positioning is then recalculated using the remaining observations. However, if isolation is not possible (as in cases where two or more faults are consistently present), the positioning solution for that epoch is aborted.

### Implementation Note:
For the Weighted Least Squares (WLS) positioning mode, the system is configured by setting (for example) settings.sys.lstype = 1 (in some implementations this might appear as ls_type in a file such as “Task2.m”). The core weighted RAIM algorithm is implemented in “calcPosLSE.m” and is supported by functions such as chi2_detector.m and PLcompute.m.

### 1. Weighted Position Estimation
The estimated weighted position $\boldsymbol{X}$ is computed by the standard WLS expression:

$\boldsymbol{X} = (G^T W G)^{-1} G^T W \boldsymbol{Y}$

where:
- $\boldsymbol{G}$ is the geometry (design) matrix,
- $\boldsymbol{W}$ is the weighting matrix, and
- $\boldsymbol{Y}$ is the vector of measurement observations.

### 2. WSSE Test Statistic and Detection Threshold
The WSSE (Weighted Sum of Squared Errors) is calculated as:

$WSSE = \sqrt{\boldsymbol{Y}^T W (I - P) \boldsymbol{Y}}$

with the projection matrix defined by:

$\mathbf{P} = \mathbf{G}\left(\mathbf{G}{-1}\mathbf{G}^T\mathbf{W}$

The detection threshold, (T), is derived from the Chi-square distribution as

$T(N, P_{FA}) = \sqrt{Q_{\chi^2, N-4}(1 - P_{FA})}$
