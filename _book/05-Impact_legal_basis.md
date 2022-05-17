# Effects of the Requirement for a Legal Basis for Data Processing on the Online Advertising Market

Among the numerous changes introduced by the GDPR with regard to the processing of personal data---including new rights for users, as well as new obligations for firms---the most meaningful change for the advertising industry is perhaps the requirement for firms to supply a legal basis for data processing.
As discussed above, in the advertising industry, this requirement implies that firms must inform the user about all processing activities, including tracking, and obtain the user's permission for these activities---either explicit, in cases in which consent serves as the legal basis; or implicit, in the form of non-objection to data processing, in cases in which legitimate interest serves as the legal basis.
Before the introduction of the GDPR, the default was that actors in the online advertising industry could process the user's personal data at will---and users who wished to reduce or prevent tracking could only do so by installing anti-tracking software or altering their browsers' settings.
Accordingly, the requirement to obtain user permission for data processing constitutes a profound change in the operations of the online advertising industry.
This section elaborates on how this change affects the various firms operating in the advertising market, the users themselves, and the interplay between them.
We distinguish between effects that are independent of the user's decision, i.e., granting or denying permission for data processing (Section 5.1), and those dependent on the user's decision (Section 5.2).

## Effects Independent of the Outcome of the User's Decision

### Effects of Asking for Permission

#### Effects on Firms Operating in the Online Advertising Industry

In practice, a common approach by which publishers inform users of data processing activities and obtain their permission for such activities is by implementing "cookie banners" (named after the predominant tracking technology, see Section 3.1), also referred to as "consent banners".
A publisher displays a cookie banner to the user when she first visits its website.
Figure 10 shows an example of such a cookie banner.

![Figure 10: Example of a Cookie Banner (here: www.ecodibergamo.it)](images/figure10.png "Figure 10: Example of a Cookie Banner (here: www.ecodibergamo.it)"){width="217"}

The crucial challenge for the publisher is to implement a cookie banner that is compliant with the GDPR, i.e., provides comprehensive information, and that is user-friendly, i.e., does not deter the user.
Furthermore, this information needs to cover the purposes of personal data processing and identify all firms that get access to the data.
Thus, the cookie banner can become tedious to read for the user, which can conflict with the user's aim, namely, to consume the website's content instantly.

In order to develop and implement a user-friendly and GDPR-compliant cookie banner from scratch, a publisher would need to invest in human resources like lawyers, data privacy experts, user experience designers, and web developers.
Yet, a new actor has emerged to assist publishers, particularly smaller ones, in producing such banners in a less costly manner: namely, firms that offer Consent Management Platforms (CMPs).
We describe them in more detail in Section 6.1.

#### Effects on the User

When a user visits a publisher's website for the first time, the user's browser has to load the cookie banner and the website's content.
Loading a cookie banner takes several seconds (Hils et al. 2020) and increases the time until the user can access the publisher's content.
Thus, the presence of a cookie banner can impair users' online experience, particularly when users do not have a fast Internet connection.

Furthermore, the user needs to respond to the cookie banner that requests permission for personal data processing.
Since there is no single universal design for cookie banners, the user faces various cookie banners across websites (Degeling et al. 2019).
These cookie banners differ in several dimensions, such as the position on the website, the number of layers (nested sites of the banner), and the buttons to select.
Given the interest of the online advertising industry in getting permission for all purposes, particularly tracking, profiling and targeting (Section 3.2), the publisher has an incentive to lead the user to an "accept all" decision.
Therefore, cookie banners are often designed so as to make it easy for the user to click an "accept all" or "allow all" button, i.e., to grant permission for all specified purposes of the publisher.
Such a design might entail, for example, presenting an "accept all" option on the first layer of the cookie banner, i.e., the part of the cookie banner that the user instantly sees.

Compared with granting permission, denying permission for data processing is often less straightforward for the user.
For example, many cookie banners do not provide a "deny all" button (Sanchez-Rola et al. 2019) on the first layer and instead require the user to open a second layer, e.g., by clicking on a "settings" button (Schmitt 2021).

Suppose the user wants to make a more differentiated decision and only wants to give or deny permission for specific purposes, such as the use of personal data for ad performance measurement.
In that case, the user also needs to access the second layer and go through all the specified purposes, selecting the ones that are acceptable to her.
Thus, the user needs to process more information and click more times than she would have to had she selected the "accept all" option (or the "deny all" option, if available).
This scenario illustrates that a decision deviating from the "accept all" option increases the user's effort and the amount of time she must wait until she can access the website's content---thereby impairing the user's online experience.

In Section 8.4, we present an empirical study that provides evidence for the number of decisions a user typically makes when faced with a cookie banner, and the average time spent making each decision.
Notably, developers have created various non-commercial tools to streamline the decision-making process, with the aim of preventing cookie banners from impairing the user experience.
We discuss these tools in Section 6.2.

Summing up, users gain benefits from the requirement for publishers to ensure that they have permission (i.e. a legal basis) for data processing, as this requirement increases users' control over their personal data---enabling users to deny permission, or provide it only for specific purposes.
Yet, at the same time, this requirement entails costs for the user, who may be subjected to a lengthy and potentially annoying decision process.
For some users, the benefits of control over one's data may outweigh the costs---whereas for others, the opposite may be the case.

### Effects of Documenting and Managing Permissions

#### Effects on Actors in the Online Advertising Industry

Regardless of whether the user has granted or denied permission for personal data processing, the publisher must document the request for permission and the user's decision.
This obligation comes with considerable costs to the publisher, requiring, for example, investments in technological infrastructure, processes, and personnel.

To illustrate these documentation costs, consider a publisher such as the German news site Focus Online (www.focus.de).
According to assessments by AGOF (a German association of online marketers), Focus Online has approximately 25 million unique monthly users (as of September 2021, www.agof.de/?wpfb_dl=8454).
Suppose that, in a given month, the publisher lacks information regarding permission decisions for about 25% of users---for example, because these users are new, or deleted their cookies.
Focus Online then has to request permission from these users and store the information regarding their decisions.
This process yields 6.25 million decisions per month (=25% \* 25 million users per month \* 1 decision per user).
Let us further assume that Focus Online collaborates with and therefore transfers personal data to 100 other actors (such as a retargeting agency or an ad exchange)---for which it must also request and store each user's permission decision (see Section 7 for more information on how these steps are accomplished).
Thus, Focus Online needs to request and store 625 million decisions per month (=6.25 million decisions per month and actor \* 100 actors) for these actors.
Overall, Focus Online needs to document 6.25 million decisions (for itself) and 625 million decisions (for other actors), in total 631.25 million decisions.
The online advertising industry, particularly IAB Europe, created the Transparency and Consent Framework (TCF) to support this documentation process.
We describe the TCF in Section 7.

In addition to the documentation costs, the GDPR induces other costs from processes that we refer to as the management of permissions for data processing.
For example, the GDPR endows the user with the rights to understand, change, and restrict personal data processing (Section 4.3).
Thus, the publisher needs to enable the user to retract or alter the permission for processing personal data and be able to delete the collected data of a user at any point in time.
Subsequently, we outline the resulting costs using the example of a publisher.
However, these costs occur similarly to all vendors that process the user's data on behalf of the publisher.

Returning to our example, let us assume that, in a given month, only 0.5% of all Focus Online's users retract their permission and request the deletion of their personal data.
In this case, Focus Online would need to provide data for 125,000 users (= 0.5% \* 25 million users).
Suppose this provision is a manual process, i.e., a service or back-office employee individually updates the database for each user's data and then sends each user an individual email.
Then, the resulting personnel cost would be extremely high.
For example, assuming a minimum duration of 3 minutes per user, the resulting total duration of this work would be 375,000 minutes (=125,000 users \* 3 minutes per user), i.e., 6,250 hours, equivalent to 260 days or 8.5 months of non-stop work just to respond to all requests from one month.
In a country like Germany, where the gross minimum wage per hour in 2021 is 9.50€, the corresponding gross cost for personnel is equal to 59,375€ per month, or 712,500€ per year.
These estimates represent a lower bound, given that the calculation was based on the minimum wage and neglected non-wage labor costs such as health insurance.
Therefore, it seems beneficial for firms to invest in processes and IT infrastructure that automate the described process.

The fashion retailer Zalando is an example of a firm that enables users to submit an online request for information about and deletion of their stored data, as Figure 11 illustrates.
Notably, even this technologically advanced retailer outlines that it can take up to 30 days (the maximum allowed duration) to provide a user with the stored data.
Thus, it is evident that a publisher might incur immense costs to comply with the user's right to information.
Overall, we can conclude that the GDPR has induced new and substantial costs for the online advertising industry.

![Figure 11: Example of a Data Request (here Zalando)](images/figure11.png "Figure 11: Example of a Data Request (here Zalando)"){width="614"}

#### Effects on the User

Documenting all firms that collect the user's personal data is crucial for enabling the user to exercise full control over these data.
Assume, for example, that a user decides to apply online for new health insurance.
Some online insurance providers might have already tracked the user online and targeted the users with ads.
The user may, at one time, have granted permission to the various health-related publishers to process her data, e.g., for the purpose of receiving personalized content.
The insurance providers can use the data that was previously collected for advertising to tailor their offers (O'Neil 2016), e.g., set the price of the offer.
Such data might include, for example, the health-related publishers the user visited, which exact content the user viewed, and on which health-related ads the user clicked.
But now, before the health insurance application, the user wishes to retract the permission and have the collected data deleted.
Therefore, the user needs to know precisely which health-related publishers collected her data and which other actors were involved in the data processing, i.e., which other actors also got access to the data.

Assume that 10% of all unique publishers the user visits are health-related.
If we further assume that the average user visits 50 unique publishers per month, then the user is estimated to visit 5 unique health-related publishers per month (= 10% of health-related publishers \* 50 unique publishers).
If each of these publishers has connections to 100 other actors, the user would need to keep a monthly record of 5 publishers and 250 other actors (=5 publishers \* 100 other actors per publisher of which 50% overlap).
Thus, we conclude that the user also faces high costs for managing her permissions.

## Effects Dependent on the Outome of the User's Decision

We continue by outlining how users' decisions to grant versus deny permission for data processing affect firms operating in the advertising industry, as well as the users themselves.
We focus on two extreme cases: the case in which the user grants permission for all personal data processing (e.g., chooses the "accept all" option in response to a cookie banner); and the case in which the user denies permission for all personal data processing (e.g., chooses the "deny all" option).

### Effects of Granting Permission

#### Effects on Firms Operating in the Online Advertising Industry

If a user grants the publisher permission for all processing of personal data (e.g., by choosing the "accept all" option), then the publisher (and other actors with which it collaborates) can track, profile, and target the user for the purposes the publisher has specified.
This level of access is similar to what the publisher would have been able to achieve before the GDPR---with the difference being that the publisher has the user's informed permission to engage in its data processing activities, and has made these activities more transparent to the user.
Indeed, in this case, the publisher has a legal basis that supports the lawfulness of its personal data processing activities, in accordance with the GDPR's specifications.

Given the many advantages that the online advertising industry derives from tracking, profiling, and targeting, an advertiser will likely prefer to display ads with a publisher where users can be tracked, profiled, and targeted rather than with a publisher for which these practices are not possible.
Thus, the publisher gains a competitive advantage from having a large share of users who provide consent to tracking, profiling and targeting.
The percentage of users who permit such activities is referred to as the publisher's "consent rate" (in %).

#### Effects on the User

A user who chooses the "accept all" option receives targeted ads and personalized content.
Such personalization enhances the likelihood that the user will be exposed to ads and content that are "relevant", i.e., aligned with her interests (Boerman et al. 2017).
Increased relevance of ads and content, in turn, improves the user's online experience.

Personalization of ads and content comes at a certain cost to users.
First, when more firms have access to a user's personal data, the risk of potential misuse of the data increases.
Moreover, if the user wishes to actively keep track of the firms that process his data---e.g., so that he will be able to delete the data later on---then any provision of consent translates into additional effort that the user must invest.
Recall, however, that the user grants or denies consent on a case-by-case basis to each publisher---and thus can mitigate these concerns, to some extent, by selecting the individual publishers to whom he wishes to grant the opportunity to feature targeted ads and personalized content.
For example, such consent may benefit the user when he visits publishers that provide content directly related to his hobbies (e.g., travel magazines) but may be less useful on other types of websites.

### Effects of Denying Permission

#### Effects on Actors in the Online Advertising Industry

If a user chooses to deny consent for any data processing, the publisher (and other actors with whom the publisher collaborates) cannot track, profile, or target the individual user.
The inability to track users limits advertisers' activity (in comparison to the situation pre-GDPR, or, alternatively, situations in which users provide consent).
For example, the advertiser cannot "retarget" the user---a term that refers to displaying ads to users who have previously visited an advertiser's website without purchasing.
Moreover, the advertiser has no information about which ads a user saw in the past.
Thus, the advertiser is not able to conduct recency or frequency capping and cannot learn about the user's interactions with specific ads at different points in time, for example, for attribution modeling.
Consequently, advertising along the specific customer journey of a user is almost impossible.
At best, the advertiser can target groups of users, such as in contextual targeting or when advertising at different points in time.

The inability to target users is likely to diminish the performance of the advertiser's ads and to increase ad wastage.
These effects, in turn, may (i) diminish the advertiser's willingness to pay for online advertising; and (ii) provide the advertiser with an incentive to shift its budget to other types of advertising.
These reactions ultimately decrease ad prices.
Empirical evidence suggests that ad prices are 40%-50% lower for users for whom tracking is disabled, as compared with users for whom tracking is enabled (Johnson, Shriver, and Du 2020; Laub, Miller, and Skiera 2022).

Lower ad prices imply less revenue for the publisher---meaning that the publisher has fewer means to finance the website's content.
Consequently, the publisher's content quality decreases, potentially attracting fewer users (Shiller, Waldfogel, and Ryan 2018).
This decrease in the number of users, in turn, reduces the number of ad impressions that the publisher can sell---further diminishing the publisher's ad revenue.
However, viewing fewer ads, for example, by blocking some ads using an ad blocker but allowlisting others, can lead to a higher news consumption (Yan, Miller, and Skiera 2022).

There are notable examples of publishers that increased their revenue without user-tracking, such as Netherland's public broadcaster (Nederlandse Publieke Omroep (NPO)).
In essence, NPO draw benefits from two developments when refraining from third-party tracking technologies.
First, they improved their contextual targeting capabilities, which attracted advertisers to buy NPO's ad inventory even without user-tracking.
Second, they cut out ad tech vendors that were involved in user-tracking and behaviorally targeted ads.
Thus, NPO managed to increase their revenue without requiring the consent of the users.
However, the well-documented empirical results of Johnson, Shriver, and Du (2020) and Laub, Miller, and Skiera (2022) point in a different direction.

A lack of permission to track users may further diminish the attractiveness of the publisher's content---and thereby decrease its user base---because of the publisher's inability to (i) personalize the content of the website (e.g., by personalizing the content ranking) and (ii) measure the success of the website's content for an individual user (e.g., Ho and Bodoff 2014).
For example, without permission for tracking, the publisher can no longer observe when and where a user leaves the website and make improvements to retain the user's interest.

Together, these effects indicate that a user's denial of permission for personal data processing ---resulting from the GDPR's requirement for a legal basis for data processing---induces a threat of revenue loss for actors in the advertising industry.
In particular, the advertiser experiences more ad wastage---though it may be able to offset such wastage by paying lower ad prices.
The publisher, in turn, suffers a loss, with the precise effect largely depending on the consent rate of the publisher.
In other words, the publisher is more affected by the GDPR than the advertiser, and the publisher is the actor with a greater interest in obtaining the user's permission for tracking.

#### Effects on the User

For the user, an obvious consequence of denying consent for personal data processing is exposure to non-personalized content and ads---which may be less relevant to the user's interests compared with personalized content and ads (which the user would be more likely to have viewed before the GDPR, when tracking was the default).
A consequence that is less obvious for most users is the possibility of a decrease in the quality of free online content---as a result of lower ad revenues, according to the logic outlined above.

Publishers might further respond to decreasing ad revenues by charging for their content, or by adopting innovative approaches such as so-called cookie paywalls (referred to by some German and Austrian publishers as the "PUR model")---which offers users a choice between either accepting the website's tracking or paying for a tracking-free (and sometimes even ad-free) version of the website (Müller-Tribbensee, Miller, and Skiera 2022).
The PUR model has gained popularity, especially among content providers such as the news website Washington Post (see Figure 12).
Yet, it is not entirely clear whether this model is compatible with the GDPR's requirement that, to serve as a legal basis for tracking, the user's consent must be freely given (meaning that the user's capacity to access a website cannot be contingent on the provision of consent).
Indeed, requiring the user to accept tracking in order to access free content seems to negate the idea of freely given consent.
Yet publishers might argue that the user is, in fact, free to make a choice---as she can access the content while still avoiding tracking by paying the publisher's stated price.
Some Data Protection Authorities, such as the ones in Austria and in Hamburg, have decided that the PUR model is valid as long as the price for the content is reasonably low.
In this case, the user is considered to have a choice between paying with data or with money for the publisher's content.

![Figure 12: Example of the PUR Model (here: www.washingtonpost.com)](images/figure12.png "Figure 12: Example of the PUR Model (here: www.washingtonpost.com)"){width="638"}

Several industry actors have proposed an alternative model in which, instead of paying to access a publisher's website with data or money, users sell the rights to process their personal data, i.e., allow tracking, in exchange for money.
For some users, this approach could be an attractive alternative to denying permission.
A significant obstacle to this approach is that the user typically does not know the data's value (Lischka and Kenning 2020).
Moreover, the opportunity to sell data in exchange for money is not universally available; firms adopting this model have begun to emerge only recently.
We discuss industry initiatives that picked up this approach and tackled these obstacles in Section 9.1.

## Main Takeaways

The main takeaways from Section 5 are:

-   The requirement for a legal basis for data processing in the advertising industry---in the form of either explicit permission (consent) for data processing or implicit permission (legitimate interest)---provides users with more control over their personal data, enabling them to determine how much tracking, profiling, and targeting to allow, if any.
    Yet this benefit comes with costs for actors in the advertising industry, as well as for the users themselves.

-   Regardless of whether users provide or deny permission for data processing, publishers face high costs for requesting such permission (e.g., through cookie banners) and managing information on users' decisions.

-   The very need to decide whether to provide permission, as well as to track and manage such decisions, also entails costs for users, which may worsen the user's online experience.

-   If the user grants (as opposed to denying) permission for data processing, the user likely receives ads and content of higher relevance, but shares more personal data with a variety of firms, which represents a loss of privacy.

-   If the user denies permission,

    -   the advertiser has less data to improve online advertising performance and becomes less willing to pay for online advertising;

    -   the publisher, in turn, faces a threat of lower revenue from online advertising to finance its free content.
        Thus, a high consent rate represents a competitive advantage for a publisher;

    -   the quantity and quality of the content that the user can access for free may be lower than they would have been had the user provided permission.