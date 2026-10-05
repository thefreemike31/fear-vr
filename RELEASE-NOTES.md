# F.E.A.R. VR v1.7.2 - Ladder and body calibration hotfix

- **Important ladder fix:** tall ladders with multiple nearby floors now select
  the actual top platform before checking the standing exit. An intermediate
  floor can no longer replace the intended landing and block progression.
- **Grounded body-height calibration:** adjusting Body Height keeps the feet
  grounded and the legs animated. It adjusts upper-body height without shrinking
  the boots, legs or arm reach. New/reset body fits start at **115%**; existing
  saved values are preserved. [Body fitting guide](CALIBRATION.md#full-body-ik-and-fit-visible-body).
- Restores the head in the body-calibration mirror and improves resting arms,
  support-arm cuffs and matching hand shadows.
- **Either free hand can toggle the flashlight:** bring it to your forehead
  with Grip released, then squeeze once. Held objects and other interactions
  retain priority. [Gesture instructions](CONTROLS.md#flashlight-gesture).
- Corrects the time interval used to calculate physical grenade throws from
  sampled hand movement. No change to native slow-motion physics is claimed.

Close the game, extract the complete ZIP and choose **Setup > Upgrade**. Keep
setup-files beside Setup. Saves, calibration and language backups are preserved;
no reset is required. Package version: 1.7.2. The earlier water/ladder fix,
full-body IK, flying kick/slide, general language import and optional experimental
[OBS capture workflow](INSTALLATION.md#recording-with-obs) remain included.

The reported tall-ladder fix and body/flashlight improvements received owner
headset acceptance. Every campaign ladder, separate Steam coverage and a new
assembled-package headset run are not claimed. A minor occasional hip/arm snap
and the existing OBS control/exit follow-ups remain; see
[known limitations](KNOWN-LIMITATIONS.md).
Language import is intended to work with original language media plus its
matching 1.08 patch across languages in theory; only Spanish has official
real-media testing.
