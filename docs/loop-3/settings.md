# Settings

The Settings screen, shown in the graphic below, is reached by tapping the gear icon in the [Toolbar](displays_v3.md#toolbar) on the app [home screen](displays_v3.md#main-loop-screen).

![settings screen for loop 3](img/loop-3-settings.svg){width="250"}
{align="center"}

Each section and row on the Settings screen is described below.

## Closed Loop

The user can select closed loop or open loop using this slider. When you first start Loop, we encourage you to leave this slider disabled and become familiar with the app using [Open Loop](../operation/loop/open-loop.md) mode.

![slider to enable or disable closed loop](img/loop-3-setting-loop-mode.svg){width="500"}
{align="center"}


No automatic (closed loop) adjustment of insulin will occur and the slider will be disabled under the following conditions.

* No Pump added
* No CGM added
* User set a [Manual Temp Basal](omnipod.md#manual-temp-basal)
* User suspended insulin delivery (planned - might not be in effect yet)

### Recommended Insulin

With every loop cycle - typically every 5 minutes - Loop updates the glucose prediction using

* CGM or Fingerstick glucose value (no older than 15 minutes)
* COB from meal entries
* IOB from previous insulin delivery
* Your [Therapy Settings](therapy-settings.md)

Based on this prediction, Loop calculates a modification to insulin dosing to bring the user into the desired correction range. This can be a reduction in basal to raise the glucose prediction or a recommended bolus, subject to Delivery Limits, to lower the prediction. The glucose prediction is shown in the [Glucose Chart](displays_v3.md#charts) along with the measured glucose values.

* When in Open Loop, no automated action is taken.
* When in Closed Loop, automated action is taken based on the selected Dosing Strategy.

If you find this confusing, read how to [Think Like a Loop](https://loopkit.github.io/looptips/how-to/think-like-loop/) on the LoopTips website.

## Dosing Strategy

This row gives you the ability to select Dosing Strategy. The Dosing Strategy only affects the method by which the recommended bolus - if any - is delivered. The current selection is noted underneath the Dosing Strategy label. The default (initial) value for this setting is Temp Basal Only. Tap on the arrow to the right to modify your selection.

![Dosing Strategy selection screen](img/loop-3-setting-dosing-strategy.svg){width="500"}
{align="center"}

!!! quote "Words in Graphic"
    **Temp Basal Only:**
    Loop will set temporary basal rates to increase and decrease insulin delivery.
    
    **Automatic Bolus:**
    Loop will automatically bolus when insulin needs are above scheduled basal, and will use temporary basal rates when needed to reduce insulin delivery below scheduled basal.


Regardless of the Dosing Strategy selected, when glucose is below target or predicted to go below target, Loop decreases basal insulin using Temporary Basal.

**Temp Basal Only:** Subject to your Delivery Limits, Loop will deliver the Recommended Bolus over 30 minutes using positive temp basals (i.e., increase over your scheduled basal rate) to increase your IOB. 

**Automatic Bolus:** Subject to your Delivery Limits, you receive 40% of the Recommended Bolus at every loop cycle.

### Automatic Bolus

When you first start Loop, we encourage you to leave Dosing Strategy set to Temp Basal Only until you are sure your settings are dialed in.

The Automatic Bolus selection causes Loop to provide 40% of the recommended dose as a bolus at the beginning of each Loop cycle (when a CGM reading comes in). This is a faster method of getting the recommended insulin delivered. When Loop delivers extra insulin, the scheduled basal rate continues unchanged.

As with all Loop versions, you can manually bolus at any time by pressing the Bolus icon in the center of Loop's Main Screen.  Any bolus recommendation that you see when you press the Bolus icon will be 100% of the Recommended Bolus.


## Configuration

The Configuration section allows entry to the following screens:

### [Therapy Settings](therapy-settings.md)

There's a LoopDocs page devoted to therapy settings. Click on the link to get to that page: [Therapy Settings](therapy-settings.md).

#### Add Pump for Therapy Settings

!!! question "But I don't see Therapy Settings!"
    Therapy Settings is only accessible in the [Settings](#settings) screen when you have a pump connected to Loop.

    * Loop needs to know the parameters for the pump
    * There are several options presented below

#### Option 1: Prep for Pods

If you add an Omnipod (requires RileyLink) or Omnipod DASH up to the `Pair Pod` screen and then cancel, Loop will use the common Omnipod details to allow you to modify your Therapy Settings.

#### Option 2: Prep for Medtronic

If you need to modify Therapy Settings before connecting to a Medtronic pump:

* Add the Insulin Pump Simulator
    * Tap on the Pump in settings or the HUD to bring up the control screen
    * Select the type of Medtronic
    * Adjust the Therapy Settings as required
* Delete the Insulin Pump Simulator

#### Option 3: Simulate Loop

If you want to use Loop in parallel with your current method of dosing insulin.

* Add the Insulin Pump Simulator
* Tap on the Pump in settings or the HUD to bring up the control screen
* Choose the type of pump you wish to simulate (notice each pump has specific basal rates and ranges available)
* For best fidelity, use a real CGM (if available on the same phone) or set up the CGM to be from Dexcom Share or Nightscout
* For every meal or correction, you can echo that meal or correction with Loop using the simulated pump - watch and learn from recommendations and predictions

### Pump

The information about the pump section is detailed on several different pages. Follow the links below:

* [Add or Modify Pump](add-pump.md)
* [Omnipod or Omnipod DASH](omnipod.md) Status and Commands
* [Medtronic](medtronic.md) Status and Commands

### [CGM Settings](add-cgm.md)

The information about the CGM is found on the [Add or Modify CGM](add-cgm.md) page.

## Services

The Services section allows additions of other services such Nightscout, Loggly and Amplitude.

Please refer to the [Optional: Service](../operation/loop-settings/services.md) page.

## Support

The Support section enables the user to provide output data about the app. This information can be very helpful to folks trying to assist with problem reports.

The graphic below shows the screen provided when you tap on the Support row at the bottom of the Settings screen.

![settings support screen](img/loop-3-setting-support.svg){width="250"}
{align="center"}

### `Issue Report`

Tap on the `Issue Report` row, on the graphic above, to create a Loop Report text file with a lot of useful information for the mentors or developers if they need to assist you in solving a problem. This covers 84-hours (to enable a full pod history for users of Omnipod or Omnipod DASH). When you tap that row, you'll see a message that the file is loading.  That message never goes away but the rest of the page fills in fairly quickly. After that happens, use the up arrow to see various options to send it to yourself.

!!! note "Issue vs `Issue Report`"
    Be aware:
    
    * Issue (on github) is used to report code problems
    * `Issue Report` is an action in Loop app to provide information you may need when you ask for help: refer to [How to Find Help](../intro/loopdocs-how-to.md#how-to-find-help)

It's a good idea to use the `Issue Report` button and save it along with a screen shot if you think you will ask for help.  You can always discard these if you resolve the problem on your own.

### Submit Bug Report

Tap on the `Submit Bug Report` row to bring up one of the two views shown in the graphic below.  The left view is if you do not have a github account (or the phone is not signed in to your account). The right view is if your github credentials are available.

In either case, the first action should be to add a term or phrase to the search box (red rectangle) to see if your issue has already been reported and to read the status if it has been reported.  Please refer to the [GitHub Issues](../troubleshooting/overview.md#github-issues) section for more information.

![settings support screen when submitting a bug report](img/loop-3-setting-support-bug.svg){width="500"}
{align="center"}

!!! warning "Not for Build or Settings Help"
    Submit Bug Report should be used when you believe there is an error in the code.

    * Use [How to Find Help](../intro/loopdocs-how-to.md#how-to-find-help) instead for these cases:
        * Trouble building
        * Trouble pairing a pod
        * Trouble with red loops
        * RileyLink is not working
        * Trouble adjusting your settings

### Export Critical Event Logs

The last row creates a zip (compressed file) with detailed app information over a 7-day period. It is stored in a different format from the Loop Report and provides critical information to the developers when troubleshooting. Once the compressed file is created, you can then send it to yourself and later share it with the developers if they request it.  You can always discard these if you resolve the problem on your own.
