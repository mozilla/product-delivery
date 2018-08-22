# Shield Glossary

## Introduction

In the greater [Shield project](https://wiki.mozilla.org/Firefox/Shield),
with the code projects [Normandy](https://github.com/mozilla/normandy) and
[Delivery Console](https://github.com/mozilla/delivery-console/) in mind,
there are a lot of different terms to remember and understand.

Here we try
to list them with the goal of...:

1. Getting everyone to use the same terms

2. Understanding what they are and how they're different to each other

3. Make it easier to people new to the using the projects and people
   coding the code for the services



## Glossary

* **Addon Studies**

    * When you first install an extension, then a recipe that sends the data to supply the extension to do a study.
    * *Alias:* Opt Out Studies

* **Delivery Console**

    * Web UI interface for administering the content in Normandy.
    * https://github.com/mozilla/delivery-console/
    * *Alias:* DC

* **Feature Flagging**

    * A project to improve the functionality of overriding and making preferences available at all for new features.
    * The objective is to make adding and flipping preferences safer.
    * *Alias:* Feature Gating

* **Filter Expression**

    * A JEXL string stored in Normandy, as part of recipes, that the Normandy Client reads to determine whether a certain client should invoke the action.
    * *Alias:* JEXL, MozJEXL

* **Heartbeat**

    * A type of study where that uses code shipped in the client (part of `mozilla-central`) already.
    * https://mana.mozilla.org/wiki/display/strategyandinsights/Heartbeat
    * Data for the Heartbeat comes from creating recipies.
    * *Alias:* Heartbeat Study

* **Normandy**

    * The Django server that hosts and serves recipes.
    * https://github.com/mozilla/normandy

* **Normandy Client**

    * The code inside Firefox that talks to Normandy about what actions to take inside the client.

* **Pioneer Studies**

    * Users have to manually install this addon. Once installed it sends a lot of information about what the user does.
    * https://addons.mozilla.org/en-US/firefox/addon/firefox-pioneer/
    * Shipped as an **Addon Study**
    * User has to manually uninstall this to opt out.
    * The Telemetry data sent is encrypted and on the Data Tools side, only select few can see and analyze the data.
    * Pioneer Studies are a type of **Addon Study**

* **Preference Experiment Studies**

    * A recipe that triggers an actual (and permanent) change in the preferences of the client but unlike **Preference Rollback** and **Preference Rollout** these changes are automatically rolled back when the study ends.
    * Not a permanent change.
    * *Alias:* Preference Flip Studies

* **Preference Rollback**

    * Very similar to **Preference Rollout** except it changes the preference back to what it was before.
    * *QUESTION: Does it know what the preference value was before?*

* **Preference Rollout**

    * A recipe that triggers an actual (and permanent) change in the preferences of the client.
    * *Alias:* Pref Rollout

* **Strategy and Insights**

    * The Mozilla team that prepares, creates, and monitors the Shield studies.
    * https://mana.mozilla.org/wiki/display/strategyandinsights
    * *Alias:* S&I

* **Telemetry**

    * In the context of the Normandy Client; it piggybacks on the Telemetry pings that are sent from the client to Mozilla's Telemetry ingestion servers. The data used in the Telemetry pings can be used as part of filter expressions.
