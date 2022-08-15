+++
title = "Solving one of the world's most pressing problems.."
date = "2021-09-06T16:29:47+05:30"
author = "Nishith P"
authorTwitter = "NishithP2004" #do not include @
cover = "cover.png"
tags = ["Machine Learning", "AI"]
keywords = ["Plastic Analyser", ""]
description = ""
showFullContent = false
readingTime = true
hideComments = false
Toc = true
+++

![Plastic Analyser](/images/Plastic_Analyser.png)

# Plastic Analyser

## ─

### Nishith P

## Overview

This idea is a **Google Cloud AutoML Vision / Teachablemachine by Google** project
will allow users to classify a given mixture of plastic wastes into Recycle Grade #
1,2,3,4,5,6 & 7 for ease of recycling and saving time.This would indirectly help in
protecting the environment from the adverse effects of plastic pollution.

## Introduction

Plastic recycling is the process of recovering scrap or waste plastic and reprocessing the
material into useful products.

When different types of plastics are melted together, they tend to phase-separate, like
oil and water, and set in these layers. The phase boundaries cause structural weakness
in the resulting material, meaning that polymer blends are useful in only limited
applications. The two most widely manufactured plastics, polypropylene and
polyethene, behave this way, which limits their utility for recycling. Each time plastic is
recycled, additional virgin materials must be added to help improve the integrity of the
material. So, even recycled plastic has new plastic material added in. The same piece of


plastic can only be recycled about 2-3 times before its quality decreases to the point
where it can no longer be used.

## Grades of Plastic (Based on Resin Number)

![PA Table 1](/images/PA_Table_1.png)

![PA Table 2](/images/PA_Table_2.png)

## Method of Recycling (ideal case)

Before recycling, most plastics are sorted according to their resin type. In the past,
plastic reclaimers used the resin identification code(RIC), a method of categorization of
polymer types, which was developed by the Society of the Plastics Industry in
1988.[citation needed] Polyethylene terephthalate, commonly referred to as PET, for
instance has a resin code of 1.

Some plastic products are also separated by colour before they are recycled. The plastic
recyclables are then shredded. These shredded fragments then undergo processes to
eliminate impurities like paper labels. This material is melted and often extruded into
the form of pellets which are then used to manufacture other products. Recycling also
keeps plastic out of landfills where it can take 500years to break down.


**1.Thermal Polymerisation:**

Scientists have estimated that the potential commodity value of waste plastic may be in
excess of $300 per ton when used in process pathways yielding high-value chemical
products or to produce electricity inefficient IGCC(Integrated Gasification Combined
Cycle) processes.

**2.Waste Plastic Pyrolysis to fuel oil:**

Plastic pyrolysis can convert petroleum-based waste streams such as plastics into fuels
and carbons.
Given below is the list of suitable plastic raw materials for pyrolysis:

```
● Mixed plastic (HDPE, LDPE, PE, PP, Nylon, Teflon, PS, ABS, FRP etc.)
● Mixed-waste plastic from waste paper mill
● Multi-layered plastic
```
**3.Heat Compression:**

Heat compression takes all unsorted, cleaned plastic in all forms, from soft plastic bags
to hard industrial waste, and mixes the load in tumblers(large rotating drums
resembling giant clothes dryers). The most obvious benefit to this method is that all
plastic is recyclable, not just matching forms. However, criticism rises from the energy
costs of rotating the drums and heating the post-melt pipes.

**4.Distributed Recycling:**

For some waste plastics, technical devices called recycle bots enable a form of
distributed recycling. Preliminary life-cycle analysis(LCA) indicates that such distributed
recycling of HDPE to make filament of 3D printers in rural regions is energetically
favourable to either using virgin resin or conventional recycling processes because of
reductions in transportation energy.

**5.Other Processes:**

A process has also been developed in which many kinds of plastic can be used as a
carbon source in the recycling of scrap steel. There is also a possibility of mixed
recycling of different plastics, which does not require their separation. It is called
compatibilization and requires the use of special chemical bridging agents compatibilizers.
It can help to keep the quality of recycled material and to skip often expensive and
inefficient preliminary scanning of waste plastics streams and their
separation/purification.

## Problem

The main problem is the classification of plastic into the **_Grades of Plastic_** mentioned
above, as it is a time consuming and manual process. It requires large manual labour
and the time is taken to recycle the plastic after classification is also quite large I.e. 2x the
time will be required to recycle the plastic.


Each household contains plastic in each and every node. Assuming that the average
Indian household uses 1kg of plastic every month and throws away 95% of it after usage
such as plastic bags, pens, shampoo bottles, etc. Then the amount of time required to
classify & recycle single households scrap is itself quite significant and hence most
treatment facilities employ the simplest & fastest option of directly incinerating it or any
Another similar easy & fast process results in the production of harmful gases that
can cause harm to the environment.

The toxic gaseous chemicals released during the burning of plastic include nitrogen oxides,
sulfur dioxide, volatile organic chemicals (VOCs), and polycyclic organic matter (POMs - a
solid residue leftover). Burning plastic also releases heavy metals and toxic chemicals
such as dioxin.
All of these would not be released by burning plastic. It depends on the kind of plastic
burnt.
PVC - polyvinyl chloride, releases HCl if it is burnt.

## Solution

I have created an ML project which I believe could be integrated into a machine which
would automatically classify the plastic into 7 grades based on the plastic codes as
mentioned above.

This would simplify the process by 50% and therefore more amounts of plastic wastes
can be classified & recycled into usable products.

I call this application as “ **_Plastic Analyser”_** which I hope will be useful essentially to
reducing the number of plastic wastes in the surroundings such as in the roadsides,
lakes, etc and would also be quite essential in protecting the environment from the
adverse effects of plastic pollution.

This app is aimed at being a support to the theme which is **“Waste Management”.** This
the application supports the theme by easier classification of plastic, excessive incineration
would be prevented, thereby reducing the number of harmful gases released into the
the environment due to its burning.

Alternatively, it can also be used by youngsters trying to understand the concept of
recycling of plastic.

## Data Collection

I have used a total of 3000 images for 7 labels.

I collected the data required from my surroundings since every household is filled with
lots of plastic be it toothpaste to writing pads;a few images of plastic articles which were
not present or for better picture clarity were taken from the Internet.


## Next Steps

The next step is to integrate it into an Android app and allow community-based data
uploads.

## Testing

#### Try this awesome project for yourself [here](https://nishithp.tech/Plastic-Analyser/).

#### Or

https://nishithp2004.github.io/Plastic-Analyser/

**Instructions:** Hold up a plastic article such as a water bottle to know its grade. (Works
Best in Desktop or PC)

Note: The project is still in development and may not be fully accurate, since the dataset
The size used was small.

### © Nishith P
