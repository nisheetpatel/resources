---
{"dg-publish":true,"permalink":"/windows-battery-life-tips/","created":"","updated":""}
---

#windows #dell #battery #reddit

## Basic tips
- [x] Update BIOS

## My experience
### Tweaks that helped me the most
*refer to the reddit guide for details*
- Throttlestop, undervolt, c states
- One weird trick that works somehow (presumably because I couldn't fully figure out c states yet) is disabling, waiting, and re-enabling the GPU.
- I find the BatteryInfoView tool fantastic and incredibly accurate. Note that the most important statistic is the charge/discharge rate in watts. As the guide says, aim for under 10W. I could go down to 7W without wifi & chrome.

### Results
- Before:
	- Dell XPS 13 9570, 97Wh battery. Before any tweaks, I got around 3 hours with normal usage, and maybe around 4 hours if I disabled wifi and didn't use Chrome*.
	- Discharge rate: >20W always, usually 25-27W, often over 30W
- After:
	- especially without wifi and Chrome, the battery life shoots up to 10-14 hours with multiple other programs open (Obsidian, VScode, pdf readers).
	- Discharge rate: 6-7W without wifi & chrome, ~11W with.

# Reddit guide
[Ultimate windows battery life tips](https://www.reddit.com/r/thinkpad/comments/dddsqv/guide_ultimate_windows_battery_life_tips/)

This guide was so helpful that I'm pasting the contents in here to never lose it! I managed to increase the battery life of my Dell XPS 15 (2018 version) from around 3.5 hours to 9+ hours with mild use with wifi on, potentially 14+ hours with just Obsidian! 

---

_Disclaimer: Based heavily on_ [_this post_](http://forum.notebookreview.com/threads/guide-improving-battery-life-on-windows-enabling-deeper-c-states.815602/) _by Che0063 of the Notebookreview forum. All credit goes to him, I just figured I'd tailor the post to usage on modern thinkpads and make it available to users of the subreddit._

---

You can follow this guide step by step, or just partially, but **its important to read through it all** and understand the basic concept of what is the main goal, which is to create two profiles, one performance and one battery, to maximize what we get from our machines. Both can be tailored to your degree of specification, and this guide goes into high detail regarding the running on battery profile, making every single milliwatt count and going to extremes to accomplish it.

With manufacturers chasing for thin and light systems, we haven’t seen much innovation in battery capacity and soon will have laptops so thin they'll slit our fingers when we touch them. Manufacturers now think that if new hardware is more efficient then the need for a large battery has reduced. In some laptop line-ups, the battery capacity has actually _reduced,_ such as the Aspire E15 series.

To get your battery’s capacity in Whrs, multiply the voltage by the amp-hour rating. Your cell count doesn’t matter. E.g. a 11.4v 5.2Ah battery = 59Whrs.

On idle and a 0% brightness setting with no programs in the background (just windows desktop), modern & optimised:

**13" laptops with a 5th gen** **+ Y CPU** should idle at less than _3W - Aim for 2W_

**15” laptop with a 4th gen +** [u/Y](https://www.reddit.com/u/Y) **CPU** should use on average _<5W_. Less if on a 13” screen. Aim for 3.5-4W, especially with 6+ generations)

**15” laptops with HQ/HK CPUs** should aim for about _6-8W on idle_. Far more if you don’t have Optimus.

Laptops with _full-on desktop CPUs and dual 1080s will have a hard time hitting even 10-15W on idle_, I imagine. Don't get them.

Check with [BatteryInfoView](http://www.nirsoft.net/utils/battery_information_view.html) (tool required to monitor live total power consumption from the battery in Watts)

All my PCs have been laptops. This guide includes all my experiences with working with laptops and will take some time and may be quite advanced to some users. If you are not comfortable doing something, please research before doing it yourself. Some parts may be risky and (unlikely) cause software issues (Windows failing to boot, iTunes not recognising devices). I will not be responsible for any harm done to your computer. Your mileage may vary, but:**

I raised my battery life on my Xiaomi from 7hrs to 10+ hrs. Also my Teclast from 5hrs to a comfortable 7-8hrs

In 20 minutes of fiddling around with the settings, I raised the battery life of my friends’ Aspire V Nitro from 2-3hrs to 6hrs. I could have increased it more but I didn’t have the time.

## **Research**
Ensure that the display is bright enough. AT LEAST 250 nits minimum, because e.g. a 300nit screen operating at 50% screen brightness is far more efficient than a 150nit screen operating at 100% brightness

Ensure that the touchpad/keyboard is good enough. Look for Microsoft Precision touchpads, because external mice (plural for mouse) ruin battery life.

Ensure that the battery life capacity is well over 50Whrs for all-day battery life.

DO NOT purchase laptops with G-Sync, unless you can turn it off, otherwise the dedicated GPU must stay on and your battery will die.

DO NOT purchase laptops were the discrete graphics are enabled and bypass the integrated graphics. Your battery will die. **Every MILLIWATT counts.**

Yes.

That external mouse you bought everywhere with you is hogging power, causing the built in USB Hub to be constantly on, reducing C state residency, and sipping power to receive information from the mouse. Was the touchpad and its non-existent click buttons not good enough? Maybe you shouldn’t have bought that particular laptop anyway. Microsoft’s Precision certified touchpads are extremely good and handle gestures completely flawlessly. I think they beat Apple’s touchpads in terms of responsiveness. Precision Drivers can be installed on non-precision touchpads in some cases, but true Precision Touchpads are the absolute best you can get on a Windows laptop

Do you really need that keyboard backlight during the day? Oh wait, you never realised it was on because you could never see it through your bright working conditions, could you. (just turn it off). In my experience, keyboard backlights sip 0.3-1W. That could add up to well over 1hr of battery life wasted on a keyboard backlight you never used.

Avoid hubs, if you can. They sip power too. If the ports of that laptop weren’t enough for you, you shouldn’t have bought that laptop.

## **From basic, to advanced.**

_“Disable unnecessary background tasks, services, apps”_ blah blah blah **No. Actually do it.** Pressing X doesn’t help. On a few of my friends’ laptop they had all sorts of things in the background, including Skype, Discord, Steam, Intel HD Graphics Control Panel, Dolby Audio, Adobe Creative Cloud, Nvidia Control Panel, Realtek HD Audio Controller, and worst of all McAfee. All in the background. They were complaining about 2hrs of battery life. Manufacturers boast about 10+ hours of battery life, and then they ruin it themselves by preloading garbage on their devices.

Go to Task Manager (Right click taskbar)>Startup.

Disable all the things you don’t need. You should be able to disable most of the things here. I mean, is Adobe Updater really that important? And it’s not like you need Steam either because you certainly aren’t going to get good battery life whilst gaming.

[https://preview.redd.it/12bwwksialq31.png?width=820&format=png&auto=webp&s=332321abfee8d6607141a06504973c4ef64ca518](https://preview.redd.it/12bwwksialq31.png?width=820&format=png&auto=webp&s=332321abfee8d6607141a06504973c4ef64ca518)

Next, go to Services (Win+R, ‘services.msc’) and set the following Windows services to startup manually (Right click>Properties>Startup type). To find a service quickly, select any service and type on your keyboard the first few letters quickly.

**Service list removed (25-06-2019)**For more recommendations, go to [Black Viper’s Service configuration list.](http://www.blackviper.com/service-configurations/black-vipers-windows-10-service-configurations/)

All non-Microsoft services should be disabled, unless you specifically need it. Here is a good way to do so:Win+R, then type in "msconfig" without quotes, then press enter:**Warning: DO NOT modify anything you are unsure of. This may render your computer unbootable.**

Go to the Services tab, then click _"Hide all Microsoft Services"_

[https://preview.redd.it/hh1ixqznalq31.png?width=852&format=png&auto=webp&s=b071f5d1183893207e1c2538a309278767d0a57a](https://preview.redd.it/hh1ixqznalq31.png?width=852&format=png&auto=webp&s=b071f5d1183893207e1c2538a309278767d0a57a)

Essentially all programs can be disabled, unless you absolutely need it. If your life support depends on Adobe Acrobat downloading an update the instant it comes out, then enable it.**Note: This one-click 'solution' entirely disables the services. If you are worried that it may break some things, set it to 'manual' in services.msc**

Some programs also put pesky startup scripts, which are not viewable in Windows’ Startup Folder. They are hidden in Task Scheduler. To view and disable some of these scripts:

Win+R > taskschd.msc > Task Scheduler Library (on the Left side)

Now do you really need Adobe to check for updates every time you log on? Are Nvidia graphics driver updates so important to you? Most of these check for updates on startup, and depending on your usage patterns they really bog down your startup times.

[https://preview.redd.it/xvnzodtqalq31.png?width=1555&format=png&auto=webp&s=c6cd445bec18fdaaaa20655686c6fb5f94de4b74](https://preview.redd.it/xvnzodtqalq31.png?width=1555&format=png&auto=webp&s=c6cd445bec18fdaaaa20655686c6fb5f94de4b74)

## **Use Microsoft Edge + Films and TV (Basically use UWP Programs)**

Chrome is so inefficient I completely ruled it out when I did my battery test. Firefox? No, just stop. Opera? I don’t know what that is. Internet Explorer? Lol. Example:

Edge, on average, used 1W less power when running a webpage with a few ads. As well, Edge used 1.4-1.7W of CPU power when I was streaming a YouTube movie compared to 2W+ on Chrome and Firefox. You may have seen LinusTechTip’s video regarding battery life and Edge, but personally I don’t agree with his testing and his results were far different to mine. I’ve replaced Chrome and Firefox with Edge on quite a few machines (mine and my friends’) and saw quite significant gains in battery life. With the latest Spring Creators Update, Edge is better. Give it another try, please.

Watching videos? Use the built in Films and TV app in Windows. This video player is far more energy efficient than other alternatives such as VLC. When watching a 720p video, Films and TV used 1.4-1.6W of power, whilst VLC used 2.5-3W.

Chrome and Firefox both may have improved their battery life, but so has Edge. The latest build of Windows 10 (1803/Redstone 4/Spring Creators Update) supports faster browsing and better battery life.

Avoid replacing UWP programs with win32 programs if you can. If you don’t need all the features of Office, for example, you can use the mobile, UWP version of it. It loads faster and is clutter free. But of course, the Photos app is no substitute for Photoshop, for example.

## **Disable eye-candy (Skip if in a hurry)**

Desktop Windows Manager (dwm.exe) renders things related to mouse movements, window movements, animations etc. Disabling effects like shadows will reduce the amount of rendering done by dwm.exe.

To do so, go to Control Panel > System and Security > System > Advanced System Settings > Performance Settings and uncheck things you don’t need. Things especially like shadows behind windows and shadows behind mouse pointer are so useless and I never even knew there were such shadows until I discovered this ‘Performance Options’ window.

[https://preview.redd.it/rgj6eazvalq31.png?width=1125&format=png&auto=webp&s=2b9e76bd14ff4a9cd906b8d69ba3047d0678a997](https://preview.redd.it/rgj6eazvalq31.png?width=1125&format=png&auto=webp&s=2b9e76bd14ff4a9cd906b8d69ba3047d0678a997)

This will result in the dwm.exe service (The process that draws windows) less CPU

## **HIPM+DIPM+DevSleep (important)**

Host-Initiated Power Management (HIPM), Device-Initiated Power Management (DIPM), and Device Sleep (DevSleep/DevSlp) are power saving features of almost all modern hard drives. DevSleep is only available on SSDs, and generally puts the SSD into a sleep function than uses >5mW. That being said, your motherboard needs to support DevSleep. [@Vasudev](http://forum.notebookreview.com/members/677607/) got quite a bit of battery boost from this. By default, Windows only enables Host-Initiated Power Management. To change this;

Win+R > Regedit > HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Power\PowerSettings\0012ee47-9041-4b5d-9b77-535fba8b1442\0b2d69d7-a2a1-449c-9680-f91c70521c60

There should be a Description that says ‘Configures the LPM state’, as well as an ‘Attributes’ DWORD with the value 1. Change the value of‘Attributes’ to "2" As per this image:

[https://preview.redd.it/p1wbdakzalq31.png?width=1540&format=png&auto=webp&s=64e0dbb2115fbae9fe62e944f8d6466885b78dda](https://preview.redd.it/p1wbdakzalq31.png?width=1540&format=png&auto=webp&s=64e0dbb2115fbae9fe62e944f8d6466885b78dda)

Additionally, in the same subfolder, change the value of "Attributes" to "2" in these folders:d3d55efd-c1ff-424e-9dc3-441be7833010d639518a-e56d-4345-8af2-b9f32fb26109dab60367-53fe-4fbc-825e-521d069d2456

[https://preview.redd.it/r1p3tkr5blq31.png?width=1537&format=png&auto=webp&s=cc6e80c2b5260f0707ead60d2334e58f94f0034b](https://preview.redd.it/r1p3tkr5blq31.png?width=1537&format=png&auto=webp&s=cc6e80c2b5260f0707ead60d2334e58f94f0034b)


Now go to Control Panel > Hardware and Sound > Power Options > Change plan settings (of your active power plan) > Change advanced Power Settings > Hard disk > ACHI Link power Management and set it to Lowest. If that is not an option, change it to HIPM+DIPM.

[https://preview.redd.it/d0vvdty1blq31.png?width=1125&format=png&auto=webp&s=0173ac6fbc64c24c36743a50ad30955d6a4a8b19](https://preview.redd.it/d0vvdty1blq31.png?width=1125&format=png&auto=webp&s=0173ac6fbc64c24c36743a50ad30955d6a4a8b19)

And play around with these settings:

[https://preview.redd.it/z7gco178blq31.png?width=573&format=png&auto=webp&s=2a35e1dda761dc586637f37ede22aca28f7080c7](https://preview.redd.it/z7gco178blq31.png?width=573&format=png&auto=webp&s=2a35e1dda761dc586637f37ede22aca28f7080c7)

Try lowering these values (but not to 0ms) and you may see differences in your C7/C8 states. the ACHI Link Power Management especially may be beneficial. My laptop does not have a NVMe drive so changing the nVMe settings do not change anything.

**As a side effect, on some systems, such as my older Aspire V Nitro and Mi Notebook Pro, enabling DevSleep and DIPM allowed the Package C State to enter C3, using 2.1W of power on idle. Previously it idled at C2, using 2.4W. Modern mobile CPUs should idle at less than 0.5W, however. (Tested on U, Y, and HQ CPUs) More about C states below.EDIT: It seems that more people are benefiting from this than I thought. Give it a try and measure idle power consumption using** [**ThrottleStop**](http://forum.notebookreview.com/threads/the-throttlestop-guide.531329/)**.**


## **Undervolt (EXTREMELY IMPORTANT)**

You can reduce the voltage of your CPU, making it use less power. This increases battery runtime and reduces temperatures (and possibly increasing your performance if your CPU is being limited by a power or thermal limit *COUGH 8th gen U CPU on Dell XPS*). There are plenty of guides and explanations out there so have a look if you aren’t familiar. There are no downsides apart from possibly unstable system if you are lazy or stupid.

I highly recommend ThrottleStop for Intel CPUs, an extremely lightweight but powerful program made my unclewebb and backed by an equally supportive community. Download here: [http://forum.notebookreview.com/threads/the-throttlestop-guide.531329/](http://forum.notebookreview.com/threads/the-throttlestop-guide.531329/)

AMD Processor? I haven’t owned an AMD CPU based laptop in years. Apparently AMD Overdrive works, but there are some other programs written for some exact CPU lineups. (e.g. BrazosTweaker for Brazos based AMD APUs). That being said, early reports suggest that the 3000 series mobile APUs have fixed the 1st gen battery woes.

Extract the files anywhere but your Temp folders, and double click ThrottleStop.exe to start the program. For beginners, this program will be quite intimidating. Tip: Don’t click anything you don’t know about. Search the ThrottleStop thread and your question likely has been answered. In the unlikely event of you mucking up ThrottleStop, delete the ThrottleStop.ini and reboot to reset the settings.For undervolting, all you are interested in is the FIVR button (Fully Integrated Voltage Regulator). Open that up, and you should see something like this.

[https://preview.redd.it/wldjvpxfblq31.png?width=941&format=png&auto=webp&s=c563867eb5fb2531b8dcdab4e9fc4d43396a2a70](https://preview.redd.it/wldjvpxfblq31.png?width=941&format=png&auto=webp&s=c563867eb5fb2531b8dcdab4e9fc4d43396a2a70)

Here, you can go undervolt your Intel CPU. Check ‘Unlock Adjustable Voltage’ and move the slider left to decrease the voltage. Here are the estimates for the average undervolt of your CPU. Results vary heavily depending on your luck.

>7th gen U CPUs: -80mV

8th+ gen U CPUs (incl Whiskey Lake, possibly 10th gen): -100mV or more

6th+ gen HQ/HK CPU: -100mV or more

Y CPUs: 50-80mV

Ensure the undervolt is the exact same for both your CPU Core and CPU Cache. One some systems if these values are different the undervolt won’t be applied. To check if the undervolt is stable, run a Prime95, LinX, IntelBurnTest, AIDA64 Stress Test or whatever benchmark and see if your laptop crashes. If it doesn’t, keep lowering the voltages until you hit the point where your system is unstable. Then, raise the voltage by a few millivolts to ensure you have a stable undervolt. Now here’s the fun part: Sometimes a voltage will be stable under a CPU stress test, but will crash when opening something simple such as Edge. If this happens, it means your undervolt is not yet stable so you have to raise the voltage.

On some systems, you can disable TurboBoost and get an even better undervolt. On my 8250U, I can only undervolt -140mV with TurboBoost enabled, but can undervolt to -200mV with TurboBoost disabled. Obviously this results in lowered performance but its not like you needed TurboBoost on battery power anyway.

Set ThrottleStop to start on startup via creating a new task in Task Scheduler. ThrottleStop is one of few programs that are incredibly light on the system. On my laptop, ThrottleStop uses a mere 1.3MB of RAM and 0.0% CPU all the time.

## **Enable Speedshift (Meh)**

Speedshift is a technology available on 6th+ generation Intel CPUs. Basically it is a newer version of SpeedStep, allowing the CPU itself to control its frequency and power states instead of the OS. This reduces the time required for the CPU to raise its frequency and go back to its idle state, reducing power usage and decreasing latency. Intermittent tasks such as loading webpages can see benefits. On some systems, Speedshift is automatically enabled by the BIOS. But on many, they have to be manually enabled. To enable Speedshift:

Go to ThrottleStop, and check the Speed Shift -EPP box. The SST should light up in green. You can choose from a range of 0 to 255, where 0 maximises the CPU frequency at a cost of higher power consumption, but 255 reduced frequency to the point where your laptop may be unbearably slow. 128 is great for a balance, 80 is sufficient for games, and 180 is my value for battery savings. Your mileage may vary.

[https://preview.redd.it/rpb1ejxjblq31.png?width=1316&format=png&auto=webp&s=a457ebdefb0fb358df229dd47dfe55658e5fd06a](https://preview.redd.it/rpb1ejxjblq31.png?width=1316&format=png&auto=webp&s=a457ebdefb0fb358df229dd47dfe55658e5fd06a)

## **Check/Enable deeper C States [Intel] (VERY IMPORTANT)**

Once again, this is an issue faced by Intel users. I don’t know if this is experienced by Ryzen mobile APU users. Generally speaking, if you have clean reinstalled Windows (without manufacturer image) you may have this issue.

This may be the most effective battery saving tweak in this entire guide if your laptop isn’t configured correctly. Once again, open ThrottleStop (See? It’s just such a useful tool) and look at the C0% column. Your C0% state in all cores should be less than 1% on idle, if you have been correctly following this guide.

[https://preview.redd.it/kc6fdzenblq31.png?width=637&format=png&auto=webp&s=84f5632f595581f123620da66ce1da3cfd7d748b](https://preview.redd.it/kc6fdzenblq31.png?width=637&format=png&auto=webp&s=84f5632f595581f123620da66ce1da3cfd7d748b)

If your C0% is below 1%, then check your package power consumption. Is it less than 0.5W? If it is, you may skip this section. If it is above 1W, and you are certain your C0% is below 1%, then you may have an issue many users face on NotebookReview Forums. Now click this button

It should say CX (C7, C8, C9, etc)

Check that 95% of your cores are in C7. It should be.

Now check your Package C State Percent. This is where the problem lies on a lot of notebooks with incorrect drivers

Over 80% of your package should be in either C6, C7, or C8 state (maybe perhaps even C10!). Is your package idling in C2 or C3? Then you likely have a problem.

[https://preview.redd.it/cv0cximqblq31.png?width=310&format=png&auto=webp&s=4df726faf401fb52e1f48e18d71114670cc64a39](https://preview.redd.it/cv0cximqblq31.png?width=310&format=png&auto=webp&s=4df726faf401fb52e1f48e18d71114670cc64a39)

(As you can see Cores 2 and 3 are in 0.0% C0 and 100% C7 with Core 4 intermittently jumping from parked to unparked. If you have decided not to park your cores (it's not as difficult as parallel parking) then you may see your C0% at about 0.2-0.8% and C7% at about 95%+

I am still not completely sure about what exactly causes the issue, however it is thought that the cause is a generic or outdated disk-related driver. Try updating your disk controller. If you have a SATA based SSD, updating the ACHI controller may work.

Some users have reported success by uninstalling Intel Rapid Storage Technology (IRST) or installing IRST and disabling a performance related setting. Some users have reported success by enabling IRST SATA power savings.

For me, all I had to do was update the disk controller. Since I have a Samsung NVMe SSD, all I had to do was update the disk driver from a generic Microsoft one. SATA based SSD/HDDs usually benefit from an updated Intel ACHI controller.

My current tablet shipped with a generic Chinese SSD - it may have been a faulty one but it prevented the CPU from entering anything lower than C2 Package. The moment I upgraded the SSD, the system power draw dropped from 3.5W immediately to 2.5 watts. That is a huge improvement.

That being said, it may also be any other driver. Some members have reported that outdated Realtek Drivers for LAN and the card reader was the issue. Try updating any driver from its generic Microsoft one.

Alternatively, you can install every driver provided by your manufacturer. They should provide the configuration that allows your CPU to enter a deeper idle C state.

Enabling DevSleep and DIPM appears to also work on some systems. On some systems, adding and removing devices (USBs, etc) change C state residency.

If all else fails, you could try downloading a driver updater utility (yes, this is the only time I'll ever give you permission to do so) AS A LAST RESORT. Update drivers one by one to isolate the issue. Don't pay for a 'pro' version.

**Usually, just doing the update check in Lenovo Vantage will update any firmware and drivers on the machine, so take this paragraph with a grain of salt.**

After a reboot, your package should idle at C6/C7/C8, depending on your manufacturer and CPU.

Essentially, this is a driver issue most of the time. If you, after many months, have not solved the issue, it may be down to a BIOS/EC/hardware fault. Search around if anybody else has the same issue, and if they do, GET IT RETURNED ASAP W/ FULL 100% REFUND. Don't put up with manufacturer garbage.

I’ve noticed sometimes only the Power Saver power plan allows the CPU C state to drop down to C8 on my device. Try it yourself. Microsoft hid all the power plans except for balanced, so you will have to use Mobility Centre to change the settings. (Win+X > Mobility Centre)

Update for RS5/17763/Oct2019: Apparantly Microsoft has, for good, deleted any power plan other than Balanced.

Y**ou can, though, set up your own personal Power Saver power plan** from scratch and use it as a toggle when you get on battery. I usually toggle my custom power saver (the one we've been building up there) for battery and Lenovo intelligent power for plugged in usage. Do note that throttlestop settings will affect all power plans unless you set up a custom **performance** and **battery** in throttlestop itself, it's a good feature and it works automatically as you connect/disconnect the power supply. In particular, I disable turbo boost and have a fixed set of multipliers that are lower for battery use as well as a speedshift setting mentioned above, but you can set these to your own desired liking.

**All 4-5th generation U, MQ, HQ, CPUs should idle at LESS THAN 1W. 6+th gen** [u/Y](https://www.reddit.com/u/Y)**/HQ/HK/H CPUs should idle at less than 0.5W.**

## **_Advanced_** **Advanced Power Options (Meh)**

There are many hidden power options in Windows. These require the Attributes value of each key in Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Power\PowerSettings to be set to 2. After running the script below, you should see a plethora of settings enabled in Advanced Power Options. You should be interested in the processor settings. Each device is unique – one some systems some settings don’t do anything. You should find your optimal value in each setting.[Download Script here.](https://gist.github.com/Nt-gm79sp/1f8ea2c2869b988e88b4fbc183731693)[https://gist.github.com/Nt-gm79sp/1f8ea2c2869b988e88b4fbc183731693](https://gist.github.com/Nt-gm79sp/1f8ea2c2869b988e88b4fbc183731693)

## **Intel Graphics (relatively important)**

Lets be honest. Are you really going to be gaming on your Integrated Intel HD Graphics Card on battery power? No, I didn’t think so. You really don’t need your iGPU to be at a high frequency. To have better power savings:

Right Click Desktop > Intel Graphics Settings > Power**Edit: In the UWP version/after 1809: Go to Start, then type in Intel Graphics.**

And change all the settings to be Maximum Battery. Be sure to enable Display Power Saving Technology and Enhanced Power Saving Mode. Lord knows what _that_ does, but it reduces power consumption of my laptop by 1W by (presumably) reducing LED brightness and reducing contrast. If you are a graphics designer then maybe don’t enable this.Consider enabling panel self-refresh, etc.

Enabling Panel Self-Refresh can help, especially when displaying still images.

[https://preview.redd.it/irwld8g2clq31.png?width=1024&format=png&auto=webp&s=7af1a830c70a2f62a52e0b16e24c51b51531d8ab](https://preview.redd.it/irwld8g2clq31.png?width=1024&format=png&auto=webp&s=7af1a830c70a2f62a52e0b16e24c51b51531d8ab)

**Fan**With high end laptops featuring multiple fans, they can use 1W of power even on their lowest speed. Try editing the fan profile of your laptop. This can take hours to find the correct settings, and most people give up. On some laptops it is very difficult. Very few manufacturers allow users to control their fans but recommended third party fan controllers include [NoteBook FanControl.](https://github.com/hirschmann/nbfc/releases) I’ve spent over one month reading hundreds of pages of datasheets and still haven’t figured out how to control my right fan.

Each laptop is different, and I suggest searching google for the resources or spend hours, days, or even months trying to find the appropriate registers to control your fan. Most laptops don’t need this, but I find that it is completely unnecessary to have a laptop fan running when the CPU is below 45C.

## **Physically disconnect devices you don’t need**

Did you know you had a second hard drive? Both my friends didn’t. Another one knew, but it stayed empty.

If you aren’t regularly using your second hard drive, consider removing it and putting it into an external enclosure instead.

According to various datasheets, 5400RPM Hard Drives use 0.5-1W when spinning and idling, but most high end 7200RPM drives use upwards of 1W

“But Che, I’ve set my HDD to spin down/disabled it in Device Manager”

Both will result in the HDD being spun down, but the hard drive circuitry will still draw power, between 100-300mW of power. If you have programs on your HDD which you regularly access, having your HDD constantly spin up and down not only wastes power but puts unnecessary strain on your HDD motor. If you use a program frequently, consider moving it onto your SSD as they are more efficient. **Once again, disabling a device in Device Manager disables all the device’s features. It might still be kept on.**

## **Increase the longevity of your laptop battery.**

Every time you recharge your battery, you lose a tiny bit of battery capacity. This is an unavoidable effect of using any battery, and most laptop batteries are rated for 300-500 cycles before their full charge capacity drops below 80% of their design capacity. For example, after 500 cycles, a 100Whr battery will only be able to hold 80Whrs. The battery used in your laptop is likely Lithium Ion based. Tips for extending battery longevity:

Do not keep it plugged in 100% all the time like Grandma does. I see a lot of teachers lugging around power adapters and keeping their laptop plugged in all the time. Lithium Ion batteries in laptops are generally charged to 4.2 or even 4.4v **per cell** to maximise battery runtime. Unfortunately, prolonged exposure to voltages above 4v (about 80%) per cell results in permanent capacity loss.

Don’t store your laptop in warm conditions. 20C is ideal, but during operation the inner case temperature of a laptop can reach 35C. This is unavoidable, short of moving to Antarctica or using your laptop in a fridge, but high voltages and high temperatures are the absolute killers of lithium ion batteries. Don’t store your laptop in a car on a hot summer day.

Similarly, don’t constantly drain your laptop down to 0% if you can avoid it. Full discharge cycles put strain on the laptop battery. Don’t believe articles written in 1990 for Ni-MH based batteries. Laptop batteries do not require full cycling. This is actually very damaging to Li-ion batteries. It is better to have very small charge cycles. Aim to keep your battery capacity between 20% and 80%.

Physically disconnect your battery if you can. Unfortunately, on increasingly more modern laptops with embedded batteries this is no longer possible. I’m an extreme battery life pedant and want my battery to last as long as possible, both in runtime and cyclic life. I drilled a hole in the bottom of my brand-new laptop so that I could disconnect the battery.

[https://preview.redd.it/g67mh4r6clq31.jpg?width=1285&format=pjpg&auto=webp&s=ab7b8b0e486cc16df3effc9ad63a0705761fb6d4](https://preview.redd.it/g67mh4r6clq31.jpg?width=1285&format=pjpg&auto=webp&s=ab7b8b0e486cc16df3effc9ad63a0705761fb6d4)

When not using the laptop, aim to store the battery in a cool environment in a 40% state of charge. This keeps each li-ion cell to a nice 3.7-3.8v.

TLDR: **Keep battery capacity between 20% and 80%. Keep battery cool. Store in a cool place at 40% when not used. Don’t use it if you don’t have to.**

**Antiviruses**This is a little touchy. Our house has 4 computers. All of them do not have been running Antiviruses in the last 4 years, and they have had little issues with malware. Even when they do somehow get malware, I can remove it manually. Or, I can restore from a backup or reinstall Windows. I have ways to combat malware myself, so I can live with having no antivirus software installed.

Simply put, Antiviruses are a huge burden to the system. They constantly scan every program that is launched, scan every file I download, and decide to run full system scans at the most inconvenient times. They slow down boot times, annoy me with popups etc. I'm constantly having to stop scans and change settings whenever I download something that monitors my hardware, such as ThrottleStop or RW-Everything. **If you do not need an Antivirus software, don't use one**. I mean, nowadays there are very little ways malware can enter your system without you doing something very shady. It couldn't be put more simply: _Don't download from or visit shady websites._

## **Do not: (VERY IMPORTANT, PLEASE READ)**

**Do not disable your dedicated graphics card.** When you disable the graphics card, you disable every feature… including Nvidia Optimus or AMD Switchable Graphics. Instead of being completely off and using (theoretically 0W), your GPU will be constantly on but idling and unable to do anything. This consumes an extra 3+ Watts depending on what dGPU you have, which is huge. Some laptops disable Optimus completely, which results in drastically reduced battery life. Don't get those laptops.

Do not lock your CPU down to 400MHz, or whatever the lowest operating frequency point of your CPU is. This makes your laptop slow and inefficient.

Perfect scenario: Lets say it takes three trillion cycles for a webpage to load (unrealistic) – 3GHz = 3 billion cycles per second . Therefore, we can force our CPU Cores down to 500MHz and it will take 6 seconds to load the webpage (inefficient) Or, we could allow the cores to boost to 3000Mhz, and it will take only 1 second to load the webpage, at a cost of 6x the power consumption. But that is an extremely narrow-viewed way of looking at something. Your CPU’s cache will be active for 5 more seconds if it was operating at 500MHz. Your RAM will be constantly accessed for 5 more seconds. Your display would be unable to use its Panel Self-refresh for 5 more seconds. You _waiting_ for the webpage is a waste of your life, and you could have done your work done 5 seconds faster. What I’m trying to say is, other components of your device would be active for 5 more seconds (even the idle components would have been ON for 5 more seconds), and in the end having your CPU operating slowly is just inefficient. Speedshift was _designed_ to allow the CPU to rapidly boost its speed and immediately reduce power after completing a task.

_Please post your experiences after following this guide including which worked and which didn't, as well as which settings were optimal for your device. I only have 1 primary device to test everything on and it'll be nice to compile a list of the best settings for each tweak for the community._

_I hope this guide has been helpful. Good luck!_
