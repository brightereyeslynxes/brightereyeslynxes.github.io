---
title: corpusLabe
excerpt: >-
date: '2021-01-25'
thumb_img_path: images/view1.gif
thumb_img_alt: corpusLabe
content_img_path: images/view1.gif
content_img_alt: corpusLabe
seo:
  title: corpusLabe
  description: corpusLabe
  extra:
    - name: 'og:type'
      value: article
      keyName: property
    - name: 'og:title'
      value: corpusLabe
      keyName: property
    - name: 'og:description'
      value: >-
        corpusLabe
      keyName: property
    - name: 'og:image'
      value: images/logo.png
      keyName: property
      relativeUrl: true
    - name: 'twitter:card'
      value: summary_large_image
    - name: 'twitter:title'
      value: corpusLabe
    - name: 'twitter:description'
      value: >-
        corpusLabe
    - name: 'twitter:image'
      value: images/logo.png
      relativeUrl: true
layout: post
---

**Abstract** 	

Breast cancer is the most common cancer both in developed and developing regions. Common breast cancer treatment techniques result in several impairments in women’s upper-body function, and, consequently, contribute to a decreased quality of life. 
Although some methods for monitoring and assessing do exist, an approach able to achieve early detection, promote risk-reduction and self-management, while engaging the user in an appropriate follow-up strategy, seems to be still missing.	
In this sense, it is possible to recognize that interdisciplinary collaboration is integral to the success of an effective personalized medicine program in breast cancer-related. 
The main objective of the proposed work is to explore the potentiality of edge spatial AI as part of an	exercise monitoring tool aimed at promoting risk-reduction and self-management, while engaging the user in an appropriate follow-up strategy.

**Introduction**
 
Notwithstanding continued multi-disciplinary research providing for survival rates to keep improving [1], the following reality prevails: 

> Breast cancer is the most common incident cancer among women, is the leading cause of cancer deaths, and causes the most disability adjusted life-years (DALYs) lost around the world. - (Duggan, Dvaladze, Rositch, et al. 2020)

<figure>
	<img src="../../images/incidence.png"
     alt="Worldwide incidence"
     style="float: left; margin-right: 10px;" />
	<figcaption>Fig.1 - Worldwide incidence, mortality and prevalence of main cancer sites sorted by prevalence numbers according to the World Health Organization's International Agency for Research on Cancer's Global Cancer Observatory (\url{http://gco.iarc.fr}).</figcaption>
</figure>

<p><br></p>

As breast cancer survivors (BCS) are living longer (Fig. 1), the adverse effects resulting from the
cancer treatment are more frequent. Upper body morbidity (UBM) (e.g. decreased range of motion,
muscle strength, pain and lymphedema) are among the most prevalent side effects [3].

Regarding lymphedema alone, it has been estimated that over 1 million BCS in the United
States [4] may meet the criteria for breast cancer-related lymphedema (BCRL). Lymphedema is
a swelling condition, resulting from lymphatic ablation commonly associated with breast cancer
treatment (BCT). Women who have undergone BCT are at a risk of developing BCRL during their
lifetimes, which impacts on different dimensions of a woman’s quality of life [5]. Clinical assessment
of the condition is usually performed by evaluating the difference in volume between the operated side
and the other, or, against a pre-operative measurement [6]. Objective measurement techniques in use
include bioimpedance spectroscopy, arm circumferences, water displacement or lymphoscintigraphy.
However, it was shown that some patients develop symptoms of BCRL without objective changes
in arm circumference, indicating that its incidence and impact may be underestimated [7].

On the other hand, arm/shoulder mobility, usually assessed by goniometer-based measurements
of flexion, is an objective measure of UBM that has been used in breast cancer rehabilitation, although its well established use covers much broader application scenarios (Fig. 2). More recently,
several studies proposed the use of vision and inertial based sensing solutions for UBM assessment
through the estimation of the reachable workspace based on hand and shoulder computed trajectories [8]–[12]. However, current systems of specific joint motions assessment still present limitations
as general tools for robust and reliable UBM analysis with clinical relevance, namely, performance
degradation of pose estimation for less constrained acquisition scenarios. In addition to the discussion related to the validity of the application of tools based on machine learning methods involving
data collection, there is a recurring discussion on topics such as preservation of privacy, security and
transparency, which, in the area of health care gains even more relevance [13]–[15].

<figure>
	<img src="../../images/reference.png"
     alt="reference"
     style="float: left; margin-right: 10px;" />
	<figcaption>Fig.2 - Illustration of the use of a goniometer for the quantification of shoulder range of motion.</figcaption>
</figure>

<p><br></p>

Besides UBM assessment itself, the proposed prospective surveillance model for BCS [18] highlights the importance of monitoring for functional and physical impairments commonly associated
with BCT. Also highlighted by the prospective model is the need to adopt long-term follow-up
strategies (Fig.3) supported by objective widely available assessment methods. In that sense, methods for clinical and at home use to eliminate biases and recall inaccuracies from self-reported data,
as well as achieve early detection, promote risk-reduction and self-management procedures are still
missing [19].

<figure>
	<img src="../../images/examples.png"
     alt="examples"
     style="float: left; margin-right: 10px;" />
	<figcaption>Fig.3 - Illustration of commonly recommend exercises for women after breast surgery as presented
by the Oncology Section of the American Physical Therapy Association (www.cancer.org).</figcaption>
</figure>

<p><br></p>

**Objectives**

The main objective of the proposed work is to explore the potential of edge spatial AI as part
of an exercise monitoring tool aimed at collecting clinically relevant data. Considering the breast
cancer treatment follow-up scenario as a study case, we propose to evaluate the OpenCV AI Kit
(OAK-D) against the gold standard goniometer for the determination of the range of motion for
shoulder flexion. A virtual goniometer using OAK-D is therefore to be implemented and evaluated.
In that evaluation, for a given human pose estimation approach, the impact of the depth from deep
neural inference and stereo depth camera pair estimation is to be studied in light of its ability to
provide robust measures of range of motion. Furthermore, and adding both a postural analysis and
a graphical user interface layers, a gamified virtual goniometer is to be developed and made available
for future work. Following, an overview (Fig.4) of the main tasks is presented:

<figure>
	<img src="../../images/arch.png"
     alt="arch"
     style="float: left; margin-right: 10px;" />
	<figcaption>Fig.4 - Representation of the proposed OAK-D system elements and planned 12 weeks timeline.</figcaption>
</figure>

<p><br></p>

a) **OAK-D set-up** - Familiarization with OAK-D API and OpenVINO.

b) **Human pose estimation** - Having the goal to predict a body skeleton in space, OpenVINO
Human Pose Estimation demo, OAK-D calibration data and alternative approaches to estimate
depth (stereo and monocular based) are to be tested running and serve as a baseline for the
problem of localization of human joints. In the context, the scenario of a single person being
observed is to be considered, and the working range of depth and pose recovery explored in
order to establish a reference relative placement of OAK-D and monitored human.

c) **Goniometer data test** - Implementation of a routine to enable a trained operator to trigger
the acquisition of a list of human pose joint locations followed by the computation of the maximum shoulder flexion angle from recovered human pose (Fig. 5). Considering the possibility
to use distinct approaches for depth estimation, a group of voluntary healthy subjects is to
be used in order to compare measurements of shoulder flexion against a standard goniometer.
The operator should verbally guide the voluntary subjects to perform equivalent poses for both
the moments of registering the goniometer reading and while using the OAK-D system.

<figure>
	<img src="../../images/work1.png"
     alt="work"
     style="float: left; margin-right: 10px;" />
	<figcaption>Fig.5 - Outline of the proposed goniometer data experience considering the computation of the
maximum shoulder flexion angle from a list of joints locations(T1).</figcaption>
</figure>

<p><br></p>

d) **Postural analysis** - To provide to a given user a target pose which one must try to mimic,
the task of matching human poses is to be implemented considering both the procrustes superimposition and the evaluation of shape differences in a given time window problems.

e) **Pose visualization** - Considering the pose output format resulting from the human pose
estimation methodology to be used, a simple graphical user interface is to be implemented.
Aiming at keeping the visual feedback as light and clean as possible it should be adopted a
simple body joint projection of selected parts with the possibility to highlight specific body
joints for specific situations, as well as the possibility of displaying sporadic textual messages.

f) **Gamified goniometer prototype** - Implementation of a prototype virtual goniometer to
enable user’s independent range of motion assessment (Fig. 6). Considering as test set of
target poses of interest the shoulder stretch movement (Fig. 3) for both left and right arms,
the prototype should provide visual feedback to guide the user to repeat each movement a given
number of times. Additionally, the system should compare the user’s current and target pose,
and determine if a given interest pose was at least partially performed by the user. For each
repetition, the user’s closest pose to the target should be considered to estimate the maximum
shoulder flexion angle. An intermediate score can be computed and presented to the user
after the first pose execution, providing feedback for each repetition on whether the maximum
shoulder flexion is changing in comparison to the previous execution of the movement.

<figure>
	<img src="../../images/work2.png"
     alt="work"
     style="float: left; margin-right: 10px;" />
	<figcaption>Fig.6 - Outline of the proposed user experience for the game-like virtual goniometer.</figcaption>
</figure>

<p><br></p>

**Future work**

The three months frame defined for the competition is taken into consideration in the establishment
of the presented expected outcomes. Notwithstanding, pending the materialization of the proposed
prototype future studies are to be sought. Namely, the devise of a study of the impact of gamification
elements in the user engagement; the extension of the list of poses of interest; the use of facial
expression analysis for the score of movement completion; the study of the gamified goniometer as
a tool for promoting exercise habits in the population of breast cancer survivors by comparison to
the adhesion of a control BCS group to independent exercise promoted through only information
dissemination efforts (e.g. printed handouts); the study of human pose estimation methodologies
and performance analysis of pose recovery from multi-modal visual data.

**Closing Remarks**

The OAK-D solution provides a rather accessible opportunity to materialize computer vision and
machine learning incredible capabilities, while contributing to both the study of more fundamental
methodologies and in the solution of real world problems. Moreover, its ability to locally process
streams of visual data via deployed pipelines seems to suit conveniently identified requirements
of privacy and transparency, particularly pertinent in a context of producing clinically relevant
data. The presented study case constitutes a remarkable opportunity to evaluate the OAK-D in a
challenging context that has the potential of benefiting many worldwide.

**Bibliography**

[1] Will Tauxe. “A tumour through time”. In: Nature 527.7578 (Nov. 2015), S102–S103. doi: 10.1038/527s102a.

[2] Catherine Duggan, Allison Dvaladze, Anne F. Rositch, et al. “The Breast Health Global Initiative 2018 Global Summit on Improving Breast Healthcare Through Resource-Stratified Phased
Implementation: Methods and overview”. In: Cancer 126.S10 (2020), pp. 2339–2352. doi:
10.1002/cncr.32891.

[3] Elizabeth A. Chrischilles, Danielle Riley, Elena Letuchy, et al. “Upper extremity disability
and quality of life after breast cancer treatment in the Greater Plains Collaborative clinical
research network”. In: Breast Cancer Research and Treatment 175.3 (Mar. 2019), pp. 675–689.
doi: 10.1007/s10549-019-05184-1.

[4] Pamela Ostby, Jane Armer, Paul Dale, et al. “Surveillance Recommendations in Reducing Risk
of and Optimally Managing Breast Cancer-Related Lymphedema”. In: Journal of Personalized
Medicine 4.3 (Aug. 2014), pp. 424–447. doi: 10.3390/jpm4030424.

[5] Janine T. Hidding, Carien H. G. Beurskens, Philip J. van der Wees, et al. “Treatment Related
Impairments in Arm and Shoulder in Patients with Breast Cancer: A Systematic Review”.
In: PLoS ONE 9.5 (May 2014). Ed. by Una Macleod, e96748. doi: 10.1371/journal.pone.0096748.

[6] Jane M. Armer, Jennifer M. Hulett, Michael Bernas, et al. “Best-Practice Guidelines in Assessment, Risk Reduction, Management, and Surveillance for Post-Breast Cancer Lymphedema”.
In: Current Breast Cancer Reports 5.2 (Mar. 2013), pp. 134–144. doi: 10.1007/s12609-013-0105-0.

[7] Andrea L. Pusic, Yeliz Cemal, Claudia Albornoz, et al. “Quality of life among breast cancer
patients with lymphedema: a systematic review of patient-reported outcome instruments and
outcomes”. In: Journal of Cancer Survivorship 7.1 (Dec. 2012), pp. 83–92. doi: 10.1007/s11764-012-0247-5.

[8] Hossein Mousavi Hondori and Maryam Khademi. “A Review on Technical and Clinical Impact of Microsoft Kinect on Physical Therapy and Rehabilitation”. In: Journal of Medical
Engineering 2014 (Dec. 2014), pp. 1–16. doi: 10.1155/2014/846514.

[9] M.E. Huber, A.L. Seitz, M. Leeser, et al. “Validity and reliability of Kinect skeleton for measuring shoulder joint angles: a feasibility study”. In: Physiotherapy 101.4 (Dec. 2015), pp. 389–393. doi: 10.1016/j.physio.2015.02.002.

[10] Burakhan C¸ ubuk¸cu, U˘gur Y¨uzge¸c, Raif Zileli, et al. “Reliability and validity analyzes of Kinect
V2 based measurement system for shoulder motions”. In: Medical Engineering & Physics 76
(Feb. 2020), pp. 20–31. doi: 10.1016/j.medengphy.2019.10.017.

[11] Justin W. L. Keogh, Alistair Cox, Sarah Anderson, et al. “Reliability and validity of clinically
accessible smartphone applications to measure joint range of motion: A systematic review”.
In: PLOS ONE 14.5 (May 2019). Ed. by Juliane M¨uller, e0215806. doi: 10.1371/journal.
pone.0215806.

[12] Bojan Milosevic, Alberto Leardini, and Elisabetta Farella. “Kinect and wearable inertial sensors for motor rehabilitation programs at home: state of the art and an experimental comparison”. In: BioMedical Engineering OnLine 19.1 (Apr. 2020). doi: 10.1186/s12938-020-
00762-7.

[13] Danton S. Char, Michael D. Abramoff, and Chris Feudtner. “Identifying Ethical Considerations
for Machine Learning Healthcare Applications”. In: The American Journal of Bioethics 20.11
(Oct. 2020), pp. 7–17. doi: 10.1080/15265161.2020.1819469.

[14] Georgios A. Kaissis, Marcus R. Makowski, Daniel R¨uckert, et al. “Secure, privacy-preserving
and federated machine learning in medical imaging”. In: Nature Machine Intelligence 2.6 (June
2020), pp. 305–311. doi: 10.1038/s42256-020-0186-1.

[15] Sebastian Vollmer, Bilal A Mateen, Gergo Bohner, et al. “Machine learning and artificial
intelligence research for patient benefit: 20 critical questions on transparency, replicability,
ethics, and effectiveness”. In: BMJ (Mar. 2020), p. l6927. doi: 10.1136/bmj.l6927.

[16] A Williams Andrews and Richard W Bohannon. “Decreased Shoulder Range of Motion on
Paretic Side After Stroke”. In: Physical Therapy 69.9 (Sept. 1989), pp. 768–772. doi: 10 .
1093/ptj/69.9.768.

[17] Morey J. Kolber, Cydne Fuller, Jessica Marshall, et al. “The reliability and concurrent validity
of scapular plane shoulder elevation measurements using a digital inclinometer and goniometer”. In: Physiotherapy Theory and Practice 28.2 (July 2011), pp. 161–168. doi: 10.3109/09593985.2011.574203.

[18] Nicole L. Stout, Jill M. Binkley, Kathryn H. Schmitz, et al. “A prospective surveillance model
for rehabilitation for women with breast cancer”. In: Cancer 118.S8 (Apr. 2012), pp. 2191–2200. doi: 10.1002/cncr.27476.

[19] C A Hudis and L Jones. “Promoting exercise after a cancer diagnosis: easier said than done”.
In: British Journal of Cancer 110.4 (Feb. 2014), pp. 829–830. doi: 10.1038/bjc.2014.12.