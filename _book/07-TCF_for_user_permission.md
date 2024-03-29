---
editor_options: 
  markdown: 
    wrap: sentence
---

# Getting User Permission for Personal Data Processing via the Transparency and Consent Framework (TCF)

In this section, we delve further into the practical challenges that firms in the advertising industry face in supplying a GDPR-compliant legal basis for their data processing activities.
In particular, this section elaborates on the Transparency and Consent Framework (TCF), an industry initiative launched by IAB Europe for assisting firms in addressing the challenges for getting user permission.
We note that, in practice, the process of ensuring the GDPR compliance is similar for the two legal bases that are applicable to the advertising industry, namely, (i) a user's explicit consent, or (ii) legitimate interest for processing data (see Section 4.5 for a detailed discussion of these legal bases).
In both cases, the firm must get the user's permission for data processing, with the difference being that reliance on consent requires the user to opt-in to data processing, whereas reliance on legitimate interest requires the user not to opt-out.
For convenience and for clarity of presentation, in what follows, we generally address consent and non-objection to legitimate interest simultaneously, using the term "permission" to refer to both of these concepts.

## Challenges of Getting Permission

To get a user's permission for personal data processing, a firm has to take the following three steps: (1) specifying the purposes of data processing for which permission is being provided (Section 4.4.4); (2) handling the permission---which includes both asking for permission and storing permission; and (3) checking the permission for data transfer, i.e., verifying that any transfer of data to other firms is carried out in accordance with the permissions that the user has provided.
A firm faces challenges in each step.
Table 8 provides an overview of the three steps, the actions that each step entails, and the corresponding challenges, which we discuss in detail in what follows.
Note that in Table 8 and throughout this section, we use the term "vendors" to refer to other actors (see Section 2.4), in accordance with the terminology used by the TCF.

![Table 8: Steps, Actions, and Challenges in Getting User Permission for Personal Data Processing towards Supplying a Legal Basis under the GDPR](images_new/table8.png "Table 8: Steps, Actions, and Challenges in Getting User Permission for Personal Data Processing towards Supplying a Legal Basis under the GDPR"){width="636"}

### Challenges of Specifying Purposes for Permission

Step 1 ("specifying purposes for permission") describes how a firm tries to comply with Article 13 para.
1 point (b) of the GDPR: "Personal data shall be collected for specified, explicit and legitimate purposes." In other words, in this step, the firm must identify legitimate purposes for using the processed data and specify these purposes in a clear (explicit) manner.
Moreover, according to Article 13 para.
1 of the GDPR, a firm needs to communicate the specified purposes with its users.
Notably, it must specify and communicate the purposes of data collection not only on its own behalf but also on behalf of all firms to which it transfers users' personal data, and it must also identify these firms (Article 13, para. 1, point e): "the data controller shall [inform the data subject about] the recipients or categories of recipients of the personal data, if any."

The GDPR itself does not define which "specified, explicit and legitimate purposes" are acceptable, leaving room for interpretation.
Consequently, it is possible that ten different firms will come up with ten different ways to specify their purposes.
For example, Firm A might specify and label two purposes: (1) cookies for payment information; (2) tracking users' behavior online.
Meanwhile, Firm B might specify the same two purposes but label them differently from Firm A: (1) cookies to process payment; (2) cookies monitoring users online.
If these two firms were to collaborate, the two different labels would make it challenging to match these two purposes automatically---though the purposes are effectively identical.
In addition, the specifications can also differ substantially.
Thus, the potential for heterogeneity in purpose specification makes communication to users and between firms challenging.

In light of the above, we suggest that firms face three major challenges in the step of specifying purposes for data processing activities (Table 8): namely, specifying purposes in a manner that is (1) accurate, (2) explicit, and (3) convenient to communicate with users and other firms.

*Challenge 1: Accuracy.* In order to achieve accuracy, a firm must specify the purposes of data collection in a manner that is both GDPR-compliant and commonly accepted, thereby reducing the likelihood of misunderstanding.Achieving accuracy is challenging because the definitions and rules in the GDPR (Section 4) are abstract and open to interpretation.
Indeed, there are disparities in interpreting the GDPR compliance among the Data Protection Authorities themselves.For example, the Data Protection Authorities of the UK and Spain require that analytic cookies get consent, while Germany disagrees, and France as well as Italy allows for several exceptions (Voisin et al. 2019).
Hence, it is difficult for a firm to find a GDPR-compliant specification that is robust to all interpretations.

Another aspect that makes accuracy challenging is the possibility of heterogeneous specifications of similar purposes, as in our previous example of Firm A and Firm B. Suppose that Firm A transfers data to Firm B. In order for this transfer to take place, both firms must ensure that they have user permission for the two purposes specified by Firm B. Due to the different labels, Firm B may find it challenging to decide whether the purposes specified by Firm A accurately match its own specified purposes.

*Challenge 2: Explicitness.* The GDPR requires that a firm's data collection activities be made explicit, i.e., fully transparent to the user.
However, the GDPR does not indicate the exact information that firms must provide in order to achieve sufficient explicitness.
Accordingly, firms face the challenge of identifying which information will provide users and other firms with a sense of explicitness.

*Challenge 3: Convenient Communication.* Convenient communication entails using wording that reduces the chances of misunderstanding, while remaining concise and easily accessible to users and other firms.
Again, because the GDPR does not specify which wordings should be used to describe the various purposes of data collection, it is challenging for a firm to identify the optimal wordings in this regard.
In particular, firms may face a trade-off between using more words to achieve accuracy and making the text concise and accessible (Kulyk et al. 2020).

### Challenges of Handling Permission

As shown in Table 8, step 2 of getting permission ("handling permission") consists of two actions: asking for user permission and storing user permission.
We note that Section 5 provides additional discussion of these actions alongside the costs that they might inflict on firms and on users, and Section 5 provides information on technological tools used to mitigate these costs.

*Action 1: Asking for Permission.* This action involves a publisher asking for the user's permission to have her data processed for the purposes that the publisher has specified.
A publisher relies on a cookie banner to ask for the user's permission (Section 5).
A user's positive response to the publisher's request implies that the publisher has obtained permission to process the user's personal data.

As discussed in previous sections, asking for user permission can be challenging for a publisher because designing and running a cookie banner on web pages requires technical knowledge that some firms lack (Section 5.1.1.1).
Moreover, a publisher must ask for permission on behalf of all the vendors to which it transfers user data for processing, as these vendors do not have direct access to the user.
It may be challenging for a publisher to centralize its vendors' heterogeneous requests for permission, as different vendors may have different specifications for purposes (as discussed in Section 7.1.1).

*Action 2: Storing Permission.* After asking a user for permission, the publisher must locally store information about the user's response---namely, whether the user has given permission for each specific purpose corresponding to each vendor.
By storing this information, the publisher can avoid re-requesting the user's consent each time the user visits its website.

Storing permission can be challenging in two ways.
First, the publisher has to find a way to encode and store the users' decisions in a small amount of space.
Indeed, a user's granular decisions on permissions can form massive amounts of information.
Publishers pass this information via HTTP requests throughout the chain of data transfer.
Since there is a size limit for such requests, a publisher has to store permission information compactly.

Second, it is challenging to store permission information in a way that enables vendors to access and read the information in a manner that is not excessively costly.
Indeed, a vendor may incur high costs to access stored permission information, particularly when it transfers such information to other vendors.
Recall that a vendor has to rely on a publisher to ask for permission on its behalf.
Suppose Vendor A transfers data to Vendor B; Vendor A has to access the publisher's permission information to see whether Vendor B has received user permission.
This process can become costly if Vendor A transfers data to many other vendors (Figure 5) and has to contact the publisher repeatedly.
In addition, if a vendor works with multiple publishers that store information in different ways, it incurs costs associated with reading various storage formats.

Aside from the challenges outlined above, publishers face challenges in keeping stored permissions up to date.
In effect, these challenges relate to the need to integrate the action of asking for permission with the action of storing permission.
Suppose a user updates her permission settings and revokes permission that she granted in the past for a particular purpose.
The publisher needs to update the permission information for each actor, and to ensure that all involved actors have the same, current information at the same point in time.
To achieve this goal, it is necessary to integrate cookie banners with storage and data processing systems.
Such integration poses both technical and legal challenges to firms.
Specifically, a firm needs an information technology expert to execute the technical aspects of the integration, and it also needs a lawyer---one who is also comfortable with information technology---to verify that the procedure is compliant with the GDPR.
Such interdisciplinary talents are rare and expensive to hire.

### Challenges of Checking Permission for Data Transfer

Step 3 ("check permission for data transfer") describes the obligation for a firm that transfers data to other parties.
Before Firm A (sender) transfers data to Firm B (receiver), Firm A has to identify Firm B's purposes for processing and verify that Firm B has permission to process the user's data for these purposes.

Carrying out this action is challenging.
As discussed in Section 7.1.1, the GDPR offers firms the flexibility to specify their own purposes for data processing, and different firms may specify similar purposes in different ways.
This diversity in specification increases the time and effort involved in the collaboration between firms.
Furthermore, it may be challenging for both firms to argue that their purposes are indeed identical.

This challenge is further complicated by the specific roles fulfilled by the firms involved in the data transfer.
For example, in a publisher-to-vendor data transfer, a publisher has to handle user permission on behalf of a vendor, and then check whether the permission it has obtained is indeed applicable to the purposes that the vendor has specified.
This procedure, entailing multiple responsibilities imposed by the GDPR, is highly complicated.
Similarly, in a vendor-to-vendor data transfer, the data-sending vendor always has to check with the publisher whether the data-receiving vendor has user permission.
This process can entail substantial effort, particularly when the vendor collaborates with many other vendors, as illustrated in Figure 5.

## Transparency and Consent Framework (TCF)

On April 25, 2018, IAB Europe launched the TCF as a means of tackling the challenges discussed in Section 7.1.
It launched an updated version of the TCF, TCF 2.0, in August 2019.
The TCF is an industry initiative, aiming at providing a solution to get user permission with guidelines and tools.
In order to adopt the solution, a firm has to register with IAB Europe, denoted as participating in TCF in the following sections.
The TCF was formulated on the basis of extensive consultation with representatives from different fields in the online advertising industry---including technology vendors (Xandr), CMPs (OneTrust), and publishers (The Telegraph).

Specifically, the TCF aims to introduce a standard that

-   creates a standardized terminology of purposes shared by all participants;

-   provides tools to facilitate asking for permission (Global Vendor List) and storing permission (Transparency and Consent String); and

-   creates a procedure to check permissions for processing personal data before transferring user data between firms.

Note that each bullet point corresponds to one of the three steps described in the previous section, and summarized in Table 8: specifying purposes for permission, handling permission, and checking permission for data transfer.

In what follows, we provide a step-by-step explanation of how, in practice, a firm can use the TCF to execute each of the three steps and overcome the associated challenges.
The TCF was envisioned as a well-documented and accepted standard that should help firms to comply with the GDPR.
A Canadian initiative (www.iabcanada.com/transparency-and-consent-framework) builds upon the idea of the European initiative.
Yet, the Irish Council for Civil Liberties suspects that the TCF infringes the GDPR.
We will discuss their concerns in more detail in Section 9.4.2.

## Mitigating Challenges in Specifying Purposes for Permission

The first step in getting permission for personal data processing is to specify the purposes for such processing.
As noted in Section 7.1.1, the main challenges a firm faces in this step include formulating the specifications in a manner that is accurate, explicit, and convenient to communicate with users and other firms.
To mitigate these challenges, the TCF provides a list of Purposes, Special Purposes, Features, Special Features, and Stacks.
We elaborate on each of these concepts in what follows.

### Facilitating Accuracy of Communication

#### Purposes

As pointed out in Section 7.1.1, as the GDPR does not define precisely what a "specified, explicit and legitimate purpose" is, a firm may find it difficult to specify purposes that are GDPR-compliant under the interpretations of all parties, as well as to match its own purposes to those of other firms (in the case of data transfer between firms).
To overcome these challenges, the TCF proposes ten specific purposes, which are shown in Table 9.

![Table 9: Specification of Purposes in the Transparency and Consent Framework (TCF) 2.0](images_new/table9.png "Specification of Purposes in the Transparency and Consent Framework (TCF) 2.0"){width="565"}

TCF uses the term "Purpose" to refer to each of the ten purposes specified in Table 9.
To avoid confusion, throughout the remainder of this section, we refer to "Purpose" specified by the TCF as a "TCF purpose" and refer to a specific TCF purpose (e.g., Purpose 2) as "Purpose N" where "N" is an integer from 1 to 10.

Seven of the ten TCF purposes relate to either advertisement (Purposes 2, 3, 4, and 7) or content (Purposes 5, 6, and 8).
Moreover, the purpose specification structures for advertisement and for content are similar.

Notably, for Purposes 2--10, a firm can claim either consent or legitimate interest as the legal basis for data processing.
For Purpose 1, however---which does not indicate a broader motivation for data processing but instead refers solely to the act of storing or accessing information on a device---a firm cannot claim legitimate interest and must obtain explicit consent.
The motivation for including Purpose 1 in the list of TCF purposes is that it corresponds to the obligation of Article 5 (3) of the ePrivacy Directive (relevant for the "Planet49" decision of the European Court of Justice).
Article 5 (3) emphasizes the importance of getting user consent for storing information.

Purpose 1 is unique because data controllers cannot pursue Purpose 1 on its own but rather only in conjunction with another TCF purpose, which is an unavoidable logical outcome.
For example, if Google wishes to display an ad to a user---whether personalized (Purpose 4) or non-personalized (Purpose 2)---it must obtain consent for Purpose 1.
If the user denies consent for Purpose 1 but accepts consent for Purpose 4 and Purpose 2, Google will still drop the ad request and serve no ad, regardless of whether the ad is personalized or not (Roth 2020).
The reason is that Google relies on cookies or mobile identifiers for both non-personalized ads (e.g., for frequency capping or fraud detection) and personalized ads (targeting).
The example of Google further highlights the importance of Purpose 1.
Note that data processors might still need Purpose 1 but not any of the other TCF purposes because they rely on the legal bases established by their data controllers.
Moreover, data controllers may also declare one or more Purposes 2-10, without declaring Purpose 1 if they do not need access to the device.

With the help of the ten TCF purposes, all firms using TCF can communicate accurately with one another.
For example, when a firm mentions Purpose 4, every other firm knows that the firm is referring to "selecting personalized ads."

We note that the specifications outlined in Table 9, corresponding to ten TCF purposes, reflect TCF 2.0, which launched in August 2019.
TCF 1.0 (launched in April 2018) contained only five purposes.
TCF 2.0 made the purposes more granular, in accordance with the WP259 guideline on consent (European Data Protection Board 2020).
The guideline points out that granularity is an element of valid consent.
This adjustment to conform to legal guidelines reflects that the TCF has been improving and revising its purpose specifications.

#### Special Purposes

In addition to the ten TCF purposes outlined above, the TCF specifies two Special Purposes, defined as purposes that firms must fulfill in order to technically be able to serve ads.
Table 10 contains the two Special Purposes stipulated in TCF 2.0.
Legitimate interest is the only legal basis that is applicable to these Special Purposes, and users cannot execute the "Right to Object" to these legitimate interests (Article 21, GDPR).
The reasons are the following.
Special Purpose 1 refers to a firm's legal responsibilities, so a firm must be allowed to pursue the purpose.
Special Purpose 2 is technically necessary for delivering information over the network to an IP address.
Although the "Right to Object" to Special Purposes is not technically supported by the TCF, publishers and their partner vendors can still establish some signaling mechanism to enable the execution of the "Right to Object".

![Table 10: Specification of Special Purposes in the Transparency and Consent Framework (TCF) 2.0](images_new/table10.png "Table 10: Specification of Special Purposes in the Transparency and Consent Framework (TCF) 2.0"){width="568"}

### Facilitating Explicitness of Communication

#### Features

The TCF further specifies several Features.
Features are not purposes in themselves.
They are methods to process data related to one or more TCF purposes.
Features are technically necessary to achieve certain TCF purposes; once the user has given permission for a particular TCF purpose, she does not need to provide additional permission for the associated Features.
Note that a Feature is always linked to a TCF purpose and if there is no legal basis supporting that TCF purpose, the Feature has no meaning.
Features require no legal basis, and information about them is provided to the user solely as a means of improving communication explicitness, that is, to provide the user with information about the methods that firms will apply to the user's data to achieve the approved (Special) Purposes.
Table 11 contains the content of the Features.

![Table 11: Specification of Features in the Transparency and Consent Framework (TCF) 2.0](images_new/table11.png "Table 11: Specification of Features in the Transparency and Consent Framework (TCF) 2.0"){width="633"}

#### Special Features

Apart from Features, the TCF also contains Special Features.
Special Features are similar to Features because firms may use them as a technical means of implementing one or more TCF purposes.
However, Special Features are more privacy intrusive than Features are (e.g., precise geolocation), meaning that they relate to processing of data that may be more sensitive to a user.
Therefore, a firm can only use the Special Features with consent as a legal basis.
Table 12 shows the two Special Features.

![Table 12: Specification of Special Features in the Transparency and Consent Framework (TCF) 2.0](images_new/table12.png "Table 12: Specification of Special Features in the Transparency and Consent Framework (TCF) 2.0"){width="647"}

Figure 15 summarizes the differences in legal bases for Purposes, Special Purposes, Features, and Special Features in TCF.
A green cell indicates that a particular legal basis (column) is applicable to a particular (Special) Purpose or (Special) Feature (row).
In almost all cases in which a particular legal basis applies, the user has the right to make a decision, i.e., to provide/deny consent, or to accept/object to the legitimate interest.
The only exception is for Special Purposes, which are grounded in the legal basis of legitimate interest, and to which the user cannot object.

![Figure 15: Legal Bases for (Special) Purposes and (Special) Features in the Transparency and Consent Framework (TCF) 2.0](images_new/figure15.png "Figure 15: Legal Bases for (Special) Purposes and (Special) Features in the Transparency and Consent Framework (TCF) 2.0"){width="622"}

### Facilitating Convenience of Communication with Stacks

To provide firms with a simplified way to ask for permission, requiring users to make fewer decisions without sacrificing granular information or choices, TCF proposes Stacks---pre-defined groups of TCF purposes and/or Special Features.
The TCF 2.0 Policy defines 42 Stacks that a publisher can choose to display on its cookie banner.
Table 13 provides an example of a TCF Stack, labeled as Stack 2.
If a publisher uses Stack 2, the publisher displays the name of the Stack "Basic ads and ad measurement" in the first layer of the User Interface (UI).
The publisher usually displays the Stack description and corresponding TCF in a further layer, e.g., on a separate page.
By choosing "Yes" for this Stack, a user simultaneously gives consent to Purpose 2 and to Purpose 7.
As indicated by some DPAs (e.g., CNIL in France), displaying Stacks instead of TCF purposes improves the convenience of communication between the publisher and the user because the user has to make fewer decisions (just one instead of two decisions in the Stack 2 example).
Nevertheless, the TCF still requires publishers to enable granular choices for each TCF purpose.
Part of the convenience brought by the TCF might also be that users get progressively used to semi-standardized interfaces and standardized terminology so that they are increasingly efficient in making their choices over time.

![Table 13: Example of a Stack in the Transparency and Consent Framework (TCF) 2.0](images_new/table13.png "Table 13: Example of a Stack in the Transparency and Consent Framework (TCF) 2.0"){width="612"}

Note that different Stacks may contain overlapping TCF purposes.
When selecting from the pool of 42 Stacks, a publisher cannot choose Stacks with the same TCF purpose.
For example, Stack 2 contains Purposes 2 and 7; Stack 3 contains Purposes 2, 3, and 4.
A publisher cannot include Stack 2 and Stack 3 simultaneously, as both Stacks include Purpose 2.
If a publisher were to include both Stacks, it might obtain conflicting responses from users, e.g., if a user accepts Stack 2 but denies permission for Stack 3.
For the same reason, a publisher cannot present a particular TCF purpose both as part of a Stack and outside of a Stack simultaneously.
To sum up, the TCF assists firms in overcoming the challenges associated with specifying purposes for personal data processing.
Specifically, it enhances (i) accuracy of specification---by providing a standardized, clearly defined, and granular set of (Special) Purposes; (ii) explicitness---by providing clear descriptions of (Special) Features that are technically necessary for the fulfillment of the specified Purposes; and (iii) convenience of communication---by creating groups of TCF purposes and/or Special Features, called Stacks, which are presented concisely and that enable users to make decisions on multiple TCF purposes simultaneously.
Furthermore, the TCF is very clear about the applicable legal basis and possible user decisions for each scenario.

## Mitigating Challenges in Handling Permission

The second step in getting permission for personal data processing is handling permission, via (1) asking for permission, and (2) storing permission.
There are several challenges a firm faces in these actions (Table 8).
The TCF provides tools to mitigate the challenges, which we will introduce in this section.

### Facilitating Asking for Permission

#### Global Vendor List (GVL)

The requirements that a firm must fulfill under the TCF in order to handle permission for data processing vary depending on whether the firm is a publisher (Section 2.1) or a vendor (Section 2.4).
The critical difference between a publisher and a vendor in handling permission is that a publisher has direct contact with a user and asks for permission on its own, whereas a vendor has no direct contact with a user and needs to rely on a publisher to ask for user permission on the vendor's behalf.

Section 7.1.2 points out that asking for permission is challenging.
To obtain permission, a vendor must tell its partner publishers the purposes for which it requires such permission.
As a publisher cooperates with many vendors, a publisher has to centralize all the vendors' requests for permission.
The heterogeneity of vendors and their respective requests makes centralizing vendor permission challenging.
Within the TCF, vendors disclose their required purposes uniformly via a registration process.
The standardized registration process and the standardized purpose specification introduced in Section 7.3 simplify the challenge of centralizing vendor permission requests.

To register with the TCF, a vendor must have a sufficient reputation (e.g., be a member in good standing with some industry associations) and pay an annual fee of 1500€.
A vendor who registers with the TCF discloses which of the TCF-specified (Special) Purposes and (Special) Features (Table 9 - Table 12) it pursues.
At the same time, the vendor also decides which legal basis to use for each of these (Special) Purposes and (Special) Features.
When declaring legitimate interest as the legal basis in the GVL, vendors have to attest that they have carried out adequate Legitimate Interests Assessments (LIA) that operate a balancing between user and vendor interests.
IAB Europe provides guidance on how to do this.

After receiving the registration application of a vendor, IAB Europe verifies the vendor's identity and the vendor's ability to maintain its service while sticking to TCF regulations.
Approved vendors appear on the Global Vendor List (GVL) (www.iabeurope.eu/vendor-list-tcf-v2-0).
The GVL is a list of TCF-registered vendors and the respective (Special) Purposes and (Special) Features each vendor uses.
The GVL is publicly available via its official website and updated weekly, enhancing each vendor's data processing transparency.

Note that the verification process conducted by IAB Europe provides no warranty of GDPR compliance.
In other words, the TCF does not certify that its approved vendors are entirely GDPR-compliant.

From the GVL, a publisher knows what TCF purposes each vendor pursues, and with which legal basis.
Then, a publisher chooses the vendors it intends to collaborate with from the GVL (hereafter referred to as partner vendors).
By default, the purposes that each vendor pursues according to the GVL apply to all publishers.
If a publisher prefers a legal basis for a specific TCF purpose that is different from the one specified by a particular vendor, the publisher can use Publisher Restrictions to modify the way they collaborate.
For example, if a particular vendor uses legitimate interest for Purpose 3, a publisher can restrict the TCF purpose and require consent.
In this way, a publisher and a vendor can collaborate more flexibly.

If a vendor changes the (Special) Purposes and (Special) Features it uses, it needs to update its information provided to IAB Europe.
These updates are included in the next weekly update of GVL.
By being connected to the GVL, all publishers automatically have access to the most recent version available via their CMPs (which are also registered with the TCF; see Section 7.4.1.2).
Yet, suppose the update requires more permissions, because of an additional (Special) Purposes and (Special) Features, an additional vendor, or a change of the legal basis from legitimate interest to consent.
In that case, the publisher needs to ask all users again for their permission.

To sum up, TCF's registration process and the GVL standardize how a vendor discloses its purposes to publishers.
Furthermore, the process and the GVL provide an efficient means for publishers to centralize and manage permissions for their partner vendors.

#### Consent Management Platforms (CMPs) Registered with the TCF

To ask for user permission, a publisher needs to equip its website with a cookie banner.
As a firm faces technical challenges in designing and running a cookie banner (Section 7.1.1), a publisher relies on a CMP (Section 6.1) that registers with the TCF to assist in designing and running a cookie banner.
Like a vendor, a CMP also has to submit a registration application to the TCF and pay an annual fee of 1500€.
IAB Europe verifies whether the technical operation of a CMP is compliant with TCF regulations.
Again, passing the verification does not guarantee complete GDPR compliance for a CMP.
If a publisher participates in the TCF, it must use a CMP from the publicly available list of TCF-registered CMPs.
A publisher can use a commercial CMP service or register its own (private) CMP.
As of November 2021, there are 170 registered CMPs in the TCF.
53 (31%) of them are private CMPs.

A TCF-registered CMP provides technical support to design and run a cookie banner.
More importantly, only TCF-registered CMPs can create, update and store the Transparency and Consent String, a tool to store consent, which we will introduce in the following subsection.

TCF-registered CMPs must follow the TCF guidelines.
IAB Europe randomly audits CMPs for proper TCF implementation on publishers' websites and can admonish the CMP if violations occur.
After three warnings, TCF can suspend a CMP, which means that all the publishers can no longer use the suspended CMP.
Thus, IAB Europe creates a strong incentive for CMPs to ensure that the publishers correctly implement TCF when using their service.

### Facilitating Storing Permission with Transparency and Consent String (TC String)

Storing consent for a user is technically challenging for two reasons.
First, there is a lot of information to store.
For example, for each purpose of each vendor, a user can decide whether to provide permission for that purpose or not.
Second, publishers have to store permission information in a manner that enables vendors to access and read the stored information easily.
The TCF created the Transparency and Consent string (TC string) to cope with these two problems.

The TC string is a piece of encoded character string capturing and storing all information about a user's permission decisions and other privacy preferences for a publisher.
The TC string includes (1) (Special) Purposes and (Special) Features of each vendor cooperating with the publisher, (2) status of user permission (consent or non-objection to legitimate interest) to process data per purpose per vendor, (3) metadata and other restrictions (e.g., the time when the TC string was created).

Only TCF-registered CMPs can create and update a TC string.
All information in the TC string is encoded in a space-efficient manner so as to enable the TC string to be passed between firms via HTTP GET requests with a storage limit.
All publishers within the TCF use TC strings to store consent.
All publishers and vendors rely on the Application Programming Interface (API) of a TCF-registered CMP to decode and read TC strings.
Thus, in effect, the TCF enables all firms to "speak the same language" when transmitting and reading information on user permissions (the TC string).

### Integrating Asking for Permission and Storing Permission

Combining cookie banners, information storage, and data processing in a harmonized way is challenging because it involves technical knowledge from many fields.
The TCF attempts to provide a standardized procedure to integrate these different fields, relying on the components described in previous sections (e.g., TCF specification of purposes, TCF tools to facilitate asking for and storing permission).

We describe this TCF procedure in detail with three representative cases summarized in Table 14.
For these cases, we assume that one user visits a publisher five days in a row and once a day, and that consent is the legal basis for all pursued purposes.
We arrange the cases from simple to complex in chronological order from Day 1 to Day 5.

![Table 14: Overview of Cases of Asking for and Storing Consent under the Transparency and Consent Framework (TCF)](images_new/table14.png "Table 14: Overview of Cases of Asking for and Storing Consent under the Transparency and Consent Framework (TCF)"){width="631"}

Case 1 is a simple example to help understand how a TC string works.
A publisher asks a user for consent on its own behalf and stores consent for the user.
Case 2 is a general case describing how a publisher asks for and stores consent on behalf of its partner vendor.
Case 3 is a case explaining how actors affect each other when having different consent statuses.
For example, a vendor may lose access to a user's data if its partner vendor does not have the user's consent.
To make the examples more intuitive, we use figures visualizing how consent information is asked for and stored.

#### Case 1: A Publisher Obtains Consent on its own Behalf

Case 1 captures the most straightforward case of collecting and storing consent, visualized in Figure 16.
Day 1 describes what happens on the user's first visit to a publisher's website, and Day 2 depicts the user's second visit.
On Day 1, User X visits Publisher A for the first time.
Publisher A has no partner vendor, so it only needs user consent for itself to pursue its specified TCF purposes---in our example, Purpose 6 (select personalized content) and Purpose 8 (measure content performance) (Table 9).

![Figure 16: Process of Getting Consent under the Transparency and Consent Framework (TCF) for Case 1](images/figure16-01.JPG "Figure 16: Process of Getting Consent under the Transparency and Consent Framework (TCF) for Case 1")

When User X arrives at the publisher's website (Step 1 in Figure 16), Publisher A contacts its CMP, CMP A, via a CMP tag, a JavaScript tag added to the website of Publisher A (Step 2).
Then, the CMP code runs on the page and checks whether a TC string corresponding to Publisher A exists in User X's local storage (e.g., a first-party cookie) (Step 3).
As this is User X's first visit to Publisher A, no such TC string is found.
In such a case, CMP A shows a cookie banner on the website, e.g., as shown in Figure 10.
The simplified cookie banner shown in Figure 16 (Step 4) lists out the two TCF purposes covered in our example: selecting personalized content and measuring content performance.

Next (Step 5 in Figure 16), User X makes choices on the cookie banner for each purpose, a "No" for personalized content and a "Yes" for performance measurement.
Then, CMP A creates a TC string for User X--Publisher A by encoding the consent information according to the standard (Step 6).
Publisher A stores the TC string locally on the device of User X (Step 7).
In Step 8, Publisher A relies on its CMP API to decode the TC string.
Then, Publisher A knows which purpose User X allows it to pursue, which we visualize in the yellow box of "Privacy Preference Information" in the center.
Eventually, Publisher A can measure content performance based on User X's data but cannot provide any personalized content to User X.

On Day 2, User X visits the publisher for the second time.
Steps 1-3 in Figure 16 remain unchanged.
Assuming that User X has not deleted local storage since the previous visit, CMP A can detect the previously saved TC string and decode it for Publisher A. In other words, there is no need to show the cookie banner and go through Steps 4-7 again.
As long as User X does not change consent information on the privacy policy page, Publisher A will rely on the stored consent information without re-obtaining permission.
Overall, asking for and storing user consent in the simplest Case 1 is already a complicated procedure.

#### Case 2: A Publisher Obtains Consent on Behalf of a Vendor

Case 2, visualized in Figure 17, captures how a publisher asks for and stores consent on behalf of a vendor.
Day 3 describes the first-visit example under the new assumptions, while Day 4 illustrates the second-visit example.
On Day 3, Publisher A decides to offer ad slots on its website to monetize its content with ad revenue.
Therefore, Publisher A chooses an ad tech vendor, Vendor S, from the GVL as its partner and notifies CMP A about this change.
In this example, Vendor S is a Demand Side Platform (DSP) where a publisher lists its advertising inventory for advertisers to buy.
Vendor S pursues two purposes with users' personal data: Purpose 2 (select basic ads) and Purpose 4 (select personalized ads) in Table 9.

![Figure 17: Process of Asking for and Storing Consent under the Transparency and Consent Framework (TCF) for Case 2](images/figure17.JPG "Figure 17: Process of Asking for and Storing Consent under the Transparency and Consent Framework (TCF) for Case 2")

When User X visits Publisher A, the CMP tag code runs and checks whether a TC string with complete consent information exists.
Although a TC string for Publisher A exists, the explicit consent is missing for Vendor S to process User X's data, as Vendor S has only recently been added.
Thus, CMP A shows a new cookie banner to User X. The new cookie banner contains the TCF purposes for Vendor S and Publisher A. To make the illustration concise, we exclude the procedure of acquiring consent for Publisher A itself, which the Case 1 example has already described.
User X sees Vendor S and its TCF purposes on the cookie banner and chooses a "Yes" for basic ad selection and a "No" for personalized ad selection.
In Step 6, CMP A encodes the consent information into a new TC string for User X--Publisher A. Then, Publisher A saves the new TC string in the local storage of User X.

In Step 8, Publisher A signals Vendor S an ad call via a vendor tag.
Before processing User X's data, Vendor S reads the TC string via the CMP API and knows that it can only use User X's data to select basic ads.
Then, Vendor S serves basic ads to Publisher A for User X in Step 12.
On Day 4, User X visits Publisher A once more.
In this scenario, similar to the scenario described for Day 2 (for Case 1), if User X has not deleted the TC string in the local storage, Publisher A and Vendor S can rely on the previously saved permissions as given.
In other words, no cookie banner pops up, saving Steps 4-7.

#### Case 3: A Publisher Obtains Consent on Behalf of Multiple Vendors

Case 3, visualized in Figure 18, captures how a publisher asks for and stores consent on behalf of multiple vendors.
Day 5 describes the first-visit example under the new assumptions.
On Day 5, Publisher A starts to sell the ad slots via another ad tech vendor, Vendor P, an ad exchange.
Thus, Vendor S (DSP) can now only buy ad slots via Vendor P (ad exchange).
Both Vendor S and Vendor P use personal data to select basic (Purpose 2) ads and personalized ads (Purpose 4).
Again, Publisher A informs CMP A about the recent addition of Vendor P and its TCF purposes.

![Figure 18: Process of Getting Consent under the Transparency and Consent Framework (TCF) for Case 3](images/figure18.JPG "Figure 18: Process of Getting Consent under the Transparency and Consent Framework (TCF) for Case 3")

When User X visits Publisher A, Steps 1-3 occur again.
As in the scenario described for Day 3 (Case 2), CMP A checks the local storage of User X and finds out that there are vendors and TCF purposes for which the user has not yet provided consent decisions.
Therefore, CMP A shows a new cookie banner to User X with purposes and features for Publisher A, Vendor S, and Vendor P. We again neglect the procedures of asking for and storing consent for Publisher A itself for conciseness.
Assume that User X ticks "Yes" for basic ad selection for Vendor S only, and "No" for the remaining TCF purposes, as displayed in the simplified banner in Figure 18.
CMP A encodes the consent information into a new TC string, decoded and interpreted via the CMP API by Publisher A, Vendor S, and Vendor P.

When the vendor tag on the website runs in Step 8, Publisher A sends an ad call to Vendor P. However, Vendor P cannot use User X's data for either of the TCF purposes.
Consequently, Vendor S has no access to the data, even though it has user consent for basic ad selection.
The dashed grey arrow in Step 12 captures the loss of access to user data.
This situation implies that, in Step 14, Vendor S can no longer show a basic ad that, according to the user's permission decisions, it would otherwise have been able to show for User X.

#### Example Procedures: Concluding Remarks

To keep our example simple and concise, we illustrated the elementary cases of a publisher obtaining consent only on its own behalf, for one vendor, or for two vendors.
Even with our simplified focus, the procedures described were quite complex---Cases 2 and 3 even more so than Case 1.
In reality, the complex interplay between publishers and vendors requires the technical solutions for these cases to be even more sophisticated than outlined.
The TCF assists in mitigating this complexity by providing actors in the online advertising industry with clear procedures for integrating permission requests and permission storage.

Nevertheless, the current TCF procedure cannot take care of every connection in the complex interplay.
For example, it is not strictly supervised whether vendors delete the received personal data when a user withdraws her consent or when she wants to have her personal data deleted.

## Mitigating Challenges in Checking Permission for Data Transfer

The third step of getting permission for personal data processing is checking permission for data transfer, i.e., ensuring that data-sending and data-receiving firms have permission for identical purposes for transferring personal data---and that the permissions for each purpose correspond to identical legal bases (i.e., consent or legitimate interest).
This procedure of matching purpose specifications and legal bases can be technically challenging.
TCF attempts to mitigate these challenges by providing standardized checking and matching procedures, which we will introduce in what follows.

### Facilitating Checking Permission for Publishers

In this section, we discuss the case where a publisher transfers data to other vendors.
Recall that a vendor within the TCF discloses, through the GVL, which of the (Special) Purposes and (Special) Features (Table 9 - Table 12) it uses.
A vendor also decides which legal basis to use to support each purpose it pursues.
A vendor can only support Purpose 1 with consent.
To support Purposes 2-10 (Table 9), a vendor has three options: (1) use only consent, (2) use only legitimate interest, (3) use either consent or legitimate interest.
For the purposes supported by either consent or legitimate interest, a vendor sets a default legal basis.
Then, it is the partner publisher who decides which legal basis to use for the vendor.
Note that a firm can only use one legal basis to support one purpose.

More formally, for each purpose (Table 9) except for Purpose 1, a vendor has five options:

-   Pursue the purpose and support with only consent as the legal basis.

-   Pursue the purpose and support with only legitimate interest as the legal basis.

-   Pursue the purpose and support with legitimate interest by default, but consent also feasible as the legal basis.

-   Pursue the purpose and support with consent by default, but legitimate interest also feasible as the legal basis.

-   Do not pursue the purpose.

Table 15 provides an example of the legal bases for the pursued TCF purposes of a specific vendor (Emerse Sverige AB), who pursues Purposes 1--9 and does not pursue Purpose 10.
The vendor uses only consent to support Purpose 1, Purpose 3, and Purpose 4.
The vendor uses only legitimate interest to support Purpose 7 and Purpose 8.
The vendor uses either consent or legitimate interest to support Purpose 2 and Purpose 9, and in both cases the default legal basis is legitimate interest.

![Table 15: Legal Bases for Purposes under TCF Specification of an Example Vendor (here: Emerse Sverige AB)](images_new/table15.png "Legal Bases for Purposes under TCF Specification of an Example Vendor (here: Emerse Sverige AB)"){width="634"}

A publisher has three options for the vendor for each purpose:

-   Desire the vendor to pursue the purpose and support with consent as the legal basis.

-   Desire the vendor to pursue the purpose and support with legitimate interest as the legal basis.

-   Desire the vendor not to pursue the purpose.

Given that a publisher has requested permission for data processing on the vendor's behalf for a particular purpose, there are four options for the decision that a user can make:

In cases in which consent serves as the legal basis:

-   Give consent to process data for the purpose (accept consent).

-   Do not give consent to process data for the purpose (deny consent).

In cases in which legitimate interest serves as the legal basis:

-   Accept legitimate interest to process data for the purpose (accept legitimate interest).

-   Execute the "Right to Object" to legitimate interest to process data for the purpose (deny legitimate interest).

Thus, given that a publisher has a relationship with a vendor (i.e., intends to transfer user data to the vendor in accordance with TCF procedures), and given a particular TCF purpose, various outcomes can be obtained with regard to data transfer for that purpose.
The outcome depends on the combination of (1) the option selected by the vendor, (2) the option selected by the publisher, and (3) the user's decision, given the option selected by the publisher.
In particular, seven outcomes are possible (see Figure 19); we classify these outcomes into "Deal" and "No Deal." "Deal" means that a user's personal data are ultimately transferred for processing, while "No Deal" means that neither data transfer nor data processing takes place.

The seven outcomes are as follows:

-   Deal to transfer data upon consent.

-   Deal to transfer data upon legitimate interest.

-   No deal due to mismatched legal basis.

-   No deal due to mismatched pursuit status.

-   No deal due to no pursuit.

-   No deal due to no user consent.

-   No deal due to user's objection to legitimate interest.

![Figure 19: Outcomes of Actions from a Publisher, a Vendor, and a User When a Publisher Transfers Data to a Vendor](images_new/figure19.png "Outcomes of Actions from a Publisher, a Vendor, and a User When a Publisher Transfers Data to a Vendor"){width="625"}

In Figure 19, the cells in green represent a successful deal to transfer data from a publisher to a vendor for one of the purposes.
The cells in red denote a failed deal to transfer data because the user does not give permission.
The white cells represent no deal to transfer data because of a mismatch in the legal basis between what the publisher expects and what the vendor supports for the purpose.
The cells in grey denote no deal to transfer data because either the publisher or the vendor, or both of them, do not pursue that purpose.

Overall, the TCF's standardized matching and checking procedure helps to ensure that a legal basis exists for a specified, explicit and legitimate purpose wherever data flows.

### Facilitating Checking Permission for Data Transfer Between Vendors

In this section, we discuss the case where a vendor transfers data to another vendor.
Checking the permission to process and transfer data is more straightforward for a vendor-to-vendor case than a publisher-to-vendor case.
A vendor cannot use restrictions to adjust the legal basis for another vendor but only accepts whatever is disclosed in the GVL and stored in the TC string.
Hence, a vendor can be in one of three states: (1) has user permission to process and transfer data (accept consent or accept legitimate interest), (2) does not have user permission to process and transfer data (deny consent or deny legitimate interest), or (3) does not pursue the purpose.

![Figure 20: Outcomes of States of Two Vendors When a Vendor Transfers Data to another Vendor](images_new/figure20.png "Figure 20: Outcomes of States of Two Vendors When a Vendor Transfers Data to another Vendor"){width="578"}

Figure 20 summarizes the outcomes of data transfer between vendors.
A vendor can only transfer personal data to another vendor if both vendors have the user's permissions, captured by the green cell.
The cells in red depict a failed deal to transfer data because at least one of the vendors lacks user permission to process data for the purpose.
The cells in grey represent no deal as at least one of the vendors does not pursue the purpose with user data.

## Main Takeaways

The main takeaways from Section 7 are:

-   A firm goes through three steps when getting permission for data processing, in order to supply a legal basis: (1) specifying purposes for data processing, (2) asking for and storing permission for the specified purposes, (3) checking permission for data transfer.

-   The online advertising industry faces challenges for each of the three steps involved in getting permission for processing of personal data.

-   The TCF is an industry initiative launched by IAB Europe, intending to tackle the challenges involved in getting permission for data processing by building up a standard for all participants to follow.

-   TCF creates a uniform specification of purposes for data processing, shared by all participants, to prevent misunderstanding and help firms communicate conveniently with users and other firms.

-   The TCF provides a Global Vendor List (GVL) to help vendors disclose their purposes, and publishers centralize and manage permission on behalf of their partner vendors.

-   The TCF created the Transparency Consent string (TC string) to store, update and exchange a user's permission in a standardized way.

-   The TCF provides no warranty for the GDPR compliance.
    Moreover, even with the help of the TCF, the procedure to handle and check permission remains complicated.
