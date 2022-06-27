---
title: 'Matrix retentions - messages & media'
published: true
date: '27-06-2022 20:13'
taxonomy:
    category:
        - news
    tag:
        - server
        - matrix
        - cleanup
        - service
aura:
    author: dan
media_order: matrix_rentention-90days_vote.png
---

 "No news, no new tutorials!?" That's right!

We're working more behind the scenes at the moment and have been cleaning up the server a bit, mainly our Matrix instance. It's taking up a little of space and it was time to start doing something about it soon enough before it grew too fast. The backups were also growing rapidly, of course, so it was definitely time to do something about that.
So we looked around for projects like [synatainer](https://gitlab.com/mb-saces/synatainer/), but then the new version 1.61 of synapse came along, which also includes [media_retention](https://matrix-org.github.io/synapse/develop/usage/configuration/config_documentation.html#media_retention).

We started a poll in our [main group](https://matrix.to/#/#welcome:techsaviours.org) and we actually all chose something else, but as you can see in the picture, it was a fair decision for everyone.
After some ups and downs, we got rid of about 11 GB. Not a huge amount, but better than nothing.

We have also updated the [Privacy Policy](https://techsaviours.org/privacy-policy.html) (under Matrix users) to match the latest changes to our Matrix instance.