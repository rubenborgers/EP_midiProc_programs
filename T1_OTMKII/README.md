# Torso T-1 and Elektron Octatrack MKII 

### Why is the program needed?
- The OT MKII audio tracks do not respond to external midi note velocity.
- The Torso T-1 has a sustain control which determines when the NOTE OFF message is sent after a pulse. The OT MKII's AMP envelope hold stage cannot be controlled by NOTE ON and NOTE OFF messages, only by CC.
- The Torso T-1 has melodic modulation capabilities which are useful for the OT MKII in the 72-127 note value range, but can also lead to the (undesirable) activation of actions associated with midi note values < 72 under strong modulation (e.g. cueing a track, start a recorder).

### Outcome:
1) OT MKII is fully responsive to external midi velocity.
2) Torso T-1 sustain controls OT MKII AMP envelope's hold in a natural way.
3) Only midi notes 72-127 remain in the stream, so only chromatic sample triggering is enabled on the OT.


