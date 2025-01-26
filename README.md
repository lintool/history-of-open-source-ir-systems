# History of Open-Source IR Systems

**January 26, 2025**

Cleaning out personal files, I discovered this gem.
Thought it'd be neat to share with the world.
Below exchange was hidden away in an email thread with Chris Buckley, Ellen Voorhees, and Donna Harman, in the context of the [Lucene for Information Access and Retrieval Research (LIARR)](https://liarr2017.github.io/) at SIGIR 2017.

Exchange here posted with the permission of all partcipants.

---

**From Me:**

I was wondering if you could provide us with a history lesson? What what I understand, SMART was the first open-source IR system made widely available for researchers? When was this, and is there a citation I can use (not of SMART in general, but of sharing the system as a toolkit).

---

**From Ellen:**

Ed Fox, Cornell CS Technical Report 83-09 "Some Considerations for Implementing the SMART Information Retrieval System Under UNIX"   https://ecommons.cornell.edu/handle/1813/6400

Chris Buckley, Cornell CS Technical Report 85-05 "Implementation of the SMART Information Retrieval System" https://ecommons.cornell.edu/handle/1813/6526

My belief is that the first SMART system to be shared widely was the later of these two systems (Chris' 1985 version).  But Ed's version was the version that moved SMART to UNIX which made the sharing possible (or, at least, vastly easier).  But I have only very fuzzy knowledge of SMART pre-1980.  Donna, did the earlier versions of SMART itself get shared outside of Cornell?

---

**From Me:**

> Chris Buckley, Cornell CS Technical Report 85-05 "Implementation of the
> SMART Information Retrieval System"
> https://ecommons.cornell.edu/handle/1813/6526

Yes, I dug this open and skimmed it - however, it says nothing about people being able to download it...

There are various places with the following FTP site:

ftp://ftp.cs.cornell.edu/pub/smart/

Which, of course, does not existing anymore...

Some more digging - searching Google scholar for the URL above, the earliest reference I could find was from 1995:

http://dl.acm.org/citation.cfm?id=215327

> "we used the unmodified SMART v11.0 software (available from Cornell at ftp://ftp.cs.cornell.edu/pub/smart)"

---

**From Donna:**

In 1967 the SMART system was spread between Harvard and Cornell, with Harvard still producing the indexing and Cornell the searching.   But the system was not shared outside, nor was it shared as late as 1973 so I think that Ed’s move to UNIX was the beginning as Ellen says.  

---

**From Chris:**

I attach the [original announcement](announce.txt) for the release of the 1985 version of SMART.  The file date is May 24, 1985 so that's probably about the right time for the initial release.  I don't have a citation for it - it got announced via usenet (netnews) as well as other places, but the usenet archives are incomplete for that era and I haven't been able to find an archived copy. I think there were roughly 120 sites that got SMART version 8 directly from us (the final copy of the official mailing list had 113 names on it), and a good number that got it indirectly.

The history of SMART releases as I remember it:

The IBM version of SMART at Cornell was worked on in the 1960s-1970s.  There was at least one attempt elsewhere to get it running; I think it was a southern US utility company (Louisiana?) that didn't work out. Around 1979-1980, Ed Fox started to re-implement it on the CS department mini-computers and I came along a year later.  We decided to use the INGRES database system as our database store - that got things working reasonably quickly, but wasn't a good long-term solution since there was too much overhead getting data in and out of the relations.  Ed started the process of taking critical procedures out of Ingres, and I continued the process after Ed graduated.  There weren't any public releases in that era, though a couple of sites were running it (Ed took a copy with him, obviously).   I finally ditched Ingres altogether, and put together the SMART Version 8 release in 1985.

SMART was never officially open source.  A couple of years after Version 8 was out, we were contacted by a company called Individual, which included ex-Salton student Harry Wu, that wanted to use SMART.  Salton and I told them they would eventually have to contact Cornell University to get approval.  Cornell didn't have any idea what they were doing, and entirely on their own, negotiated a license with Individual - I never had any contact with Cornell at all!  The first I knew anything about it, Salton forwarded a copy of the signed license that Cornell had sent him.  That gave Individual an exclusive right to use SMART for routing (SDI) for 10 years (and rights to use it thereafter)!  I was not happy.

I had many long arguments with Cornell Research Foundation over the years trying to get them to release it or at least have a standardised flat fee license for commercial use.  Their position was always that if people wanted to use SMART, there must be money in it for Cornell, and they always wanted a percentage of income (they apparently had no other non-patent protected software that had actually made them money.)

So throughout the years, officially SMART had to be gotten from us after a license was signed saying it was for research purposes only.  Sometime after SMART Version 11 (large changes to get SMART to work on TREC sized collections) was available, I put up SMART Version 8 for ftp, but I didn't think I could do more than that.  Aside from the first couple of years of SMART Version 8, we never charged for SMART - it was much easier once the Internet could handle distribution instead of having to use tapes!  But it was never officially public domain or open source.

---

**From Donna:**

Just to complete the loop, the early Cornell SMART system was documented in the SMART book, but also in ISR-10 which is in the SIGIR museum.   Here is the link to it:
https://sigir.org/files/museum/pub-10/I-1.pdf
