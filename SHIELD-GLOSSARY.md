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

    * An extension is uploaded that is self-contained. The Normandy recipe
      contains the URL to the extension.
    * *Alias:* Opt Out Studies

* **Delivery Console**

    * Web UI interface for administering the content in Normandy.
    * https://github.com/mozilla/delivery-console/
    * *Alias:* DC

* **Feature Flagging**

    * A project to improve the functionality of overriding and making preferences
      available at all for new features.
    * The objective is to make adding and flipping preferences safer.
    * *Alias:* Feature Gating

* **Filter Expression**

    * A JEXL string stored in Normandy, as part of recipes, that the Normandy
      Client reads to determine whether a certain client should invoke the action.

* **Heartbeat**

    * Heartbeat is an action that gives a prompt to a user.
    * https://mana.mozilla.org/wiki/display/strategyandinsights/Heartbeat
    * Data for the Heartbeat comes from creating recipies.
    * *Alias:* Heartbeat Study

* **Normandy Client**

    * The code inside Firefox that talks to Normandy about what actions to take
      inside the client.

* **Normandy Server**

    * The Django server that hosts and serves recipes.
    * https://github.com/mozilla/normandy

* **Pioneer Studies**

    * Users have to manually install a dummy addon.
    * Once installed, addons are installed automatically by Normandy.
    * https://addons.mozilla.org/en-US/firefox/addon/firefox-pioneer/
    * Pioneer Studies are a type of **Addon Study**
    * User has to manually uninstall this to opt out.
    * The Telemetry data sent is encrypted and on the Data Tools side, only
      select few can see and analyze the data.

* **Preference Rollback**

    * Very similar to **Preference Rollout** except it changes the preference
      back to what it was before.
    * Always paired with a Preference Rollout that it undoes.

* **Preference Rollout**

    * A recipe that triggers an actual (and permanent) change in the preferences of the client.
    * *Alias:* Pref Rollout

* **Preference Studies**

    * A recipe that triggers a change in the preferences of the client, but
      unlike **Preference Rollback** and **Preference Rollout** these changes
      are automatically rolled back when the study ends.
    * Not a permanent change.
    * *Alias:* Preference Flip Studies, Preference Experiment Studies


* **Strategy and Insights**

    * The Mozilla team that prepares, creates, and monitors the Shield studies.
    * https://mana.mozilla.org/wiki/display/strategyandinsights
    * *Alias:* S&I

* **Telemetry**

    * In the context of the Normandy Client; it uses the Telemetry pings
      that are sent from the client to Mozilla's Telemetry ingestion servers.
    * Telemetry is unrelated from Normandy but Normandy can use it (its API) in
      Filter Expressions.
