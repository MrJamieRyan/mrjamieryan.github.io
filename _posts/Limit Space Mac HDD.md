---
layout: post
title: How to limit the space used by Photos and Apple Music on your Mac
author: Jamie Ryan
date: "2019-02-19 14:35:23 +0000"
---

If, like me, you subscribe to Apple Music and use iCloud Photos then you'll enjoy that both of these services sync beautifully and almost effortlessly to your Mac. However, what happens if you have lots of photos and music that you want to sync but you don't want your limited space on your HDD or SSD filling up. I have a solution.

You can "partition" your hard drive and move the libraries for Music.app and Photos.app to this new drive. Now, I've put "partition" in quotes because it's not really like it used to be. Let me explain...

When you do this on Mac OSX Catalina, the existing drive doesn't split into 2 distinct drives like it used to. Instead, it assigns a quota, that you can set to the new drive and it allows it to use anything upto and including this space. It has the added benefit though that you can resize it later. It also means that once you create this new drive, you don't immediately lose the space on the existing drive.

Say I have a 100GB Drive. Using the old method, I could partition the drive 50/50. This would give me 2 distinct partitions of 50GB each. They didn't talk to each other and were completely separate.

Now however, if I use the new method, I can give the new drive a quota, and this will only deduct the free space from the main drive when something is added to the new drive. So my main drive will be 100GB and the new drive will be 0GB. But if I add a 1GB file, those will change to 99GB and 1GB respectively. The new drive will cap out at whatever I set the quota as.

Ok Ok, so that's all well and good but why would you bother doing this? Well, Music.app and Photos.app will download content until the OS detects that the Hard Drive is nearing capacity. This is nice and a good default but it makes it hard to gauge how much free space you actually have. So by moving the libraries for each of these apps over to a new partition, you can limit how much they are able to store locally on your machine without sacrificing any functionality.

So how do you do it? Let me show you...

1. Open Disk Utility on your Mac
2. Highlight "Macintosh HD" on the left hand side of the window
3. Click Partition at the top of the window
4. Click "Add Volume" on the dialogue box that pops up
5. Name the volume. I chose "Media"
6. Leave the Format as AFPS
7. Click Size Options
8. Assign a Quota. Something you think will be big enough to store the music you want to listen to offline and also enough for a cache of photos. I have a 128GB SSD so I went for 16gb. Enter the same value in both boxes

Congratulations, you now have a media drive.
But wait! You need to tell Photos.app and Music.app to use this new drive. Let's go through that, starting with Photos.

1.Open Photos.app

2. Go to Preferences
3. Click Show In Finder
4. Copy Photos.photolibrary to the new volume
5. Once it's copied, quit Photos.app
6. Re-Open Photos.app
7. You might be prompted that you have no library. If you are, don't worry, you haven't lost anything, it just doesn't know where to find it, so let's tell it.
8. Go to Preferences
9. Click Show In Finder
10. Go to the new volume
11. Double Click Photos.photolibrary
12. Click "Use as System Photo Library"
13. Go back to preferences and click the iCloud tab
14. Check iCloud Photos and set the radio button to "Optimise Mac Storage"

Job done! Now Photos.app will intelligently manage your photos but will remain within the quota limit you set earlier, leaving the free space on Macintosh HD to be considered actual free space

Music.app is a little different but just as easy, if not easier.

1. Locate your Apple Music folder on your Mac (It's usually in your User folder)
2. Copy the folder to your new volume
3. Open Music.app
4. Open Preferences
5. Go to the Files tab
6. Under "Music Media folder location" click change
7. Select the "Apple Music" folder you just moved to the new volume
8. Click OK.

Now your Music.app will store it's files in this new volume and you don't have to worry whether "Free Space" is actually free space or if it's free space being filled with photos of that holiday 2 years ago.
