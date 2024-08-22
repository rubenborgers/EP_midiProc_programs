# Torso T-1 and Elektron Octatrack MKII 

### Why is the program needed?
- The OT MKII audio tracks do not respond to external midi note velocity.
- The Torso T-1 has a sustain control which affects when the NOTE OFF message is sent after a pulse. The OT MKII's AMP envelope hold stage cannot be controlled by NOTE ON and NOTE OFF messages, only by CC.
- Note values below 71 trigger a variety of possibly undesired actions in the OT MKII (e.g. cueing a track, start a recorder). As the Torso T-1 can widely modulate the note values, it can also dive into this range.  

### The program "EP_PRG_T1_OT" implements the following midi processing (all midi channels):
1) Maps midi velocity to the CC for the "vol" parameter of the AMP envelope.
2) Maps NOTE ON and NOTE OFF to the CC for the "hold" parameter of the AMP envelope.
3) Filters out midi note values below 71.

### Outcome:
1) OT MKII is fully responsive to external midi velocity.
2) Torso T-1 sustain controls OT MKII AMP envelope's hold in a natural way.
3) OT MKII only receives midi notes 71-127, so only chromatic sample triggering is enabled.


