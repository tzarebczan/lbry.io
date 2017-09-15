---
title: How do I Publish content to LBRY?
category: getstarted
---

LBRY is a free, open, and community-driven digital marketplace which enables content sharing, monetization, discovery and consumption. Publishing in LBRY is the process by which you share your content on the network - you set the price per view (can be free too) which is paid directly to you. This process involves making a "claim" in the LBRY Blockchain which will be used to retrieve the content via a URL. Content can either be published anonymously or to a particular channel/identity which will group content together at a single location. Both channels and claims require a deposit(bid) of LBRY Credits (LBC) in order to reserve their location on the LBRY network. This deposit will be deducted from your balance as long as the claim is active. See our [naming document](https://lbry.io/faq/naming) for more information about claims and bids. 

If you don't have LBRY yet, download it [here](https://lbry.io/get).

### How do I create a Channel?

1. Open the LBRY app.
2. Once the application loads, click the `Publish` button in the top right of the screen.
3. In the `Channel Name` section click the dropdown and select `New Channel` and  declare the name you would like for your channel. For more details on different channel types, see our write up on [naming](https://lbry.io/faq/naming).
4. Once your name is selected, there is a `Deposit` section that is below. It requires a minimum bid of .0001 LBC (see more on deposits [here](https://lbry.io/faq/naming)). Please ensure that you have enough LBRY credits in your wallet to cover the bid amount.  There is also a small network fee associated with the creation of a channel. 
5. Click `Create Channel` once you have entered your bid amount. You now own `lbry://@channelnameyoubidon#Claim_ID` and `lbry://@channelnameyoubidon` (the vanity name without a claim id) if you are the highest bidder.

### How do I Publish content? 

1. Under the `Content` section click `Choose File`.
2. On your local machine, select the content you would like to upload to LBRY.  LBRY accepts any HTML5 format for streaming video, the full list can be found [here](https://developer.mozilla.org/en-US/docs/Web/HTML/Supported_media_formats). Other file types can also be uploaded, but won't be streamable via the LBRY app. 
3.Enter a `Title`, `Thumbnail URL`, and `Description` for your content.  The `Thumbnail URL` is a hyperlink to an image file which will serve as a preview for your content. It can be any image/GIF URL or you can even use [spee.ch](https://www.spee.ch) to host it.
4. Next, there is a `Language` and `Maturity` which will default to `English` and `All Ages`.  If a change is needed, click the dropdowns and select the appropriate choice. 
5. Under the `Access`, first determine if you want to make your video Free or set a price (in USD or LBC) per view. Next, select the appropriate type of license for the content you are publishing.
6. You have an option to select/create the channel you would like to publish the channel under. If one isn't selected, it will be posted anonymously.
7. Type in the URL you want the content to be found under along with a minimum of .0001 LBC minimum deposit for the upload. If you are trying to outbid a user friendly/common URL, the system will suggest a minimum bid to take over the content at that vanity URL. There may be a delay for this takeover, check out the `#content` channel on our [Slack](https://slack.lbry.io) to see this information (search for your URL). For more details regarding the URL or bid, check out our [naming document](https://lbry.io/faq/naming).
8. Read and agree to the terms of service.
9. Click `Publish`.
10. The file will process in the background and will be added to the LBRY Blockchain. Larger files will take longer to upload, please leave LBRY running while your content is in the "pending confirmation" mode(currently, this page will not automatically refresh).  You can continue using LBRY while the upload completes.

### How do I delete my content and reclaim my deposit? 

1. Click on the folder icon in the top right of the LBRY app. 
2. Click on the `Published` tab.
3. Select the content you want to remove. 
4. Click on the *...* next to the *Open* link. If you don't see Open, try re-downloading the content first. 
5. Select *Remove...*.
6. There will be two options. `Abandon the claim for this URI` and `Delete this file from my computer`. Select the option that applies.  Abandoning your claim will release the LBC back into your wallet (99% of the time you want to selec this). **Warning: Deleting content is permanent. Please make sure this is what you want to do before confirming the deletion.**
7. Click `Remove`. If you abandoned your claim, you should see the deposit back in your balance shortly. 

### How do I edit my existing Published content? 

1. Go to the `Publish` page.
2. In the `Content URL` section, type in your content URL for the claim you would like to edit.
3. Below the URL you will see text saying "You already have a claim with this name." and a link that says `Use data from my existing claim`. Click this link in order to capture your previously published data. 
4. You can now edit your claim information. Be sure to re-select the channel if it was published to one. No need to re-select the file if it's the same one. 
5. When you are done, re-confirm that you agree to the terms of service and click `Publish`.

### Can I increase my bid amount?

Yes, this is possible, but is only currently available via the API/command line [tools](https://lbry.io/quickstart/api). See the [claim_new_support](https://lbryio.github.io/lbry/cli/#claim_new_support) command. 

### How can I tell if someone is downloading my content?

Currently this is only possible if you set a price for your content - you will see transactions in your LBRY wallet as people purchase it. In the future, we will add these types of statistics to LBRY. 

### I shared my URL, but others can't download it. What's up? 

Since LBRY uses a Peer to Peer network, it may require that your PC is accessible through the internet. LBRY also runs servers to assis in content hosting, but this process may fail if your PC cannot send it to us. By default, the sharing port is set to 3333. If your network is properly configured and LBRY is running, a port status check on 3333 should pass on this [port checking tool](https://www.canyouseeme.org). If it fails, you can check if UPNP is enabled on your router or forward port 3333 manually. If you need assistance, check out the [help page](https://lbry.io/faq/how-to-report-bugs) on how to reach us.

### Where is my Channel and content saved locally?

Channels and content claims are saved to your LBRY Wallet along with your LBRY Credits. When creating new channels or content, it's a good practice to [backup your wallet](https://lbry.io/faq/how-to-backup-wallet) afterwards. 

### How and where can I share my content?

LBRY URLs can be shared to anyone, but they will require the LBRY app in order to view the content. If the content is free and public, it can be retrieved through [spee.ch](https://www.spee.ch) by going to https://spee.ch/<claimname> or https://spee.ch/<@channelname>. You can also share the content on our `#publishers` channel on [Slack](https://slack.lbry.io) where we have a vibrant community with thousands of users. 

### I'm an advanced user, is there more I can poke around with? 

Advanced users can check out the [API/CLI](https://lbryio.github.io/lbry/) documentation for command line / API options. 

### I'm confused and need some assistance, can you help?

Of course, we are always here to help! Check out our [help page](https://lbry.io/faq/how-to-report-bugs) on how to reach us. 
