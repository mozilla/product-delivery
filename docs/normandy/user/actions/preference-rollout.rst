preference-rollout: Controlled deployment of features
=====================================================

The ``preference-rollout`` action was created to simplify deploying features
and functionality outside of the standard release schedule.  It replaces the
high overhead and risky process of developing system addons to release
features.

Since preference-rollout builds on Normandy's filter expressions we are able to
precisely target users and control the rate of rollout.  This opens up several
use cases that were difficult or costly to do before:

1. Schedule and align feature availability for a specific date or cohort of users
1. Reduce risk of a new feature by gradually increasing availability
1. Enable a feature for a specific portion of the user population
1. Disable features that are having a negative impact on users


Persistance
-----------

Preferences changed by a rollout are permanent.  Once a preference has been
changed it will stick across version updates and any recipe changes like
disabling or changing filter settings.

The permanent nature of preference-rollouts makes it quite different from a
``preference-experiment``.  They are designed to be a deployment tool and not
an experimental one.  Use a pref-experiment to determine the right value and a
pref-rollout to set users to it.

There are only two things that can complete a preference rollout, a rollback or
graduation.

-- ??


Limitations
-----------

- only supports restartless features
- no branching or control.  -- it is not an experimental tool


Rolling Back
------------

A ``preference-rollback`` is a discrete action from ``preference-rollout``.
When Firefox sees a rollback recipe it will revert all changes it has made to
preferences.

After a rollback it is not possible to restart the rollout.  A new rollout
recipe will need to be created.

Graduation
----------


Rollout states
--------------

 - active
 - rolled-back
 - graduated

Telemetry
---------

- telemetry events sent
- telemetry graduated

Arguments
---------
Slug
   A unique identifier for the rollout, used in telemetry and in rollbacks.
Preferences
   A list of preferences to be changed in the rollout.

