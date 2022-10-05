The resulting files from [xml2ucm](https://github.com/ford-prefect/xml2ucm) currently need some changes to work.

msm8952-snd-card.conf:

* `Syntax 2` needs adding to the top
* Some controls need to be commented as the Android config references ones that don't exist (at least on my device)
* Some other controls (Voice Rx/Tx, Voip Rx/Tx) error: `Cannot read the given element from control default`

HiFi:

* `Comment` in `SectionModifier` needs removing as it causes a parser error  
  This is a bug in alsa-lib that should be fixed in v1.2.5.2 ([commit](https://github.com/alsa-project/alsa-lib/commit/ea5481296f281625ef6517208ebf6e41b5fd838c))

