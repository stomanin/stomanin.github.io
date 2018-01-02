---
title: "Integration between Drupal and CDS: is that ready yet?"
layout: post
date: 2012-09-04 00:00
image: /assets/images/markdown.jpg
headerImage: false
tag:
- CERN
- change
- Drupal
- CERN Document Server 
category: blog
author: stomanin
description: "Integration between Drupal and CDS"
# jemoji: '<img class="emoji" title=":ramen:" alt=":ramen:" src="https://assets.github.com/images/icons/emoji/unicode/1f35c.png" height="20" width="20" align="absmiddle">'
---

<small>This post was originally posted on the [CERN Change Blog](https://web.archive.org/web/20161102015242/http://change.web.cern.ch/) at <http://change-archive.web.cern.ch/blog/silvia-tomanin/integration-between-drupal-and-cds-ready-yet></small>

---


One of the things we are trying to figure out for our new Drupal site – and for the whole Drupal infrastructure in general – is how to integrate Drupal with applications used at CERN (SSO, [Indico](http://entice.web.cern.ch/projects/indico-feeds), [Search](http://entice.web.cern.ch/projects/drupal-search), [LDAP](http://entice.web.cern.ch/projects/ldap)). We discussed Drupal and CDS in a series of recent ENTICE meetings. So have the two systems been integrated yet? When will this be ready?

We are currently working on a new interface to let Drupal – and perhaps, other applications at CERN – communicate.

We have two goals for the interface:

1. **Let users embed CDS documents on Drupal sites**
2. **Let users manage the "basket" of CDS documents from Drupal, keeping the information synchronized on the two systems.** _Every CDS document comes with a set of attributes that are editable from CDS, and that can be kept up to date or not, depending on how the user wants to use the information. You might want to display an image in a blog post along with a caption from CDS, for example, but keep the option to override it with a custom version._  
Point 2 is stil under development but we have been working on embedding CDS documents in Drupal for some time now and tried many possible approaches. A technique we are currently testing that's giving good results is integration using the [oEmbed](http://oembed.com/) module (from the CDS side) and the [Media](http://drupal.org/project/media) module (Drupal side).

Media allows users to manage a library of media files - including audio, video, and text documents on Drupal. oEmbed is a format that allows an embedded representation of a URL on third-party sites. With the integration of CDS the user will be able to display embedded content and integrate it with the Drupal system (let's think about the [Drupal Image styles](http://drupal.org/documentation/modules/image) or the [file entities](http://drupal.org/project/file_entity) for example) just knowing the link to that resource, without need to parse the resource directly.

We are currently testing this method on several sites (you can see some examples here, some of which integrate content from other sources such as Youtube or Flickr) and once the workflow for media integration is stable, [Ludmila](http://change-archive.web.cern.ch/blog/61) and I will present it to the ENTICE meeting. The oEmbed APIs have been just pushed to production on CDS, so this will be ready to go live on the Drupal environment after approval at the next ENTICE meeting. 

---

<small>This post was originally posted on the [CERN Change Blog](https://web.archive.org/web/20161102015242/http://change.web.cern.ch/) at <http://change-archive.web.cern.ch/blog/silvia-tomanin/integration-between-drupal-and-cds-ready-yet></small>

