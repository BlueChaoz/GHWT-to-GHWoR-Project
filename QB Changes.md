### Tasks
- [ ] Code 4x4 Animations for Drum Textures
- [ ] Scale tex\models\highway\Note_Hit01.dds
- [x] Scale tex\models\Highway\sidebar01.dds
- [ ] Port qb code to "[All in One Mod](http://www.fretsonfire.net/forums/viewtopic.php?f=28&t=58997)" qb
- [ ] Create Animated Drihscol Notes (Essentially D7X v3)

### GHWT "qb.pak.xen" "qb.pab.xen" "dbg.pak.xen" using modified [QueenBee 1.9](https://cdn.discordapp.com/attachments/233523599464464396/246402850136129547/ModifiedQueenBee1.9.zip)
#### Changes will be in Bold text

**scripts\guitar\guitar_material.qb**

 Item                         | Id                  | Value         | Changes
:---------------------------- | :------------------ | :------------ | :---
· · StructItemQBKey           | Name                | dummy
· · **[StructItemQBKey]**     | Template            | ~~ImmediateMode_AlphaFade_UI_3Pass~~ | **AnimatedTexture_UI_3Pass**
· · **[StructItemQBKey]**     | technique           | ~~UI_Col_Tex_2D~~ | **Loop**
· · **[StructItemQBKey]**     | blendmode           | blend
· · `StructItemQBKeyString`        | MaterialProps       | material_props
StructItemStruct              | base_props          |
· ArrayStruct                 |                     |
· · StructHeader              |                     |
· · · [StructItemQBKey]       | Name                | m_sampPass0Diffuse
· · · [StructItemQBKey]       | TextureProperty     | `tex\models\highway\button_grey_Base01.dds`
· · StructHeader              |                     |
· · · [StructItemQBKey]       | Name                | m_sampPass1Diffuse
· · · [StructItemQBKey]       | TextureProperty     | `tex\models\highway\button_grey_Collar01.dds`
· · StructHeader              |                     |
· · · [StructItemQBKey]       | Name                | m_psPass2MaterialColor
· · · **[StructItemQBKey]**   | TextureProperty     | ~~col_half_alpha~~ | **col_white**
· · StructHeader              |                     |
· · · [StructItemQBKey]       | Name                | m_sampPass2Diffuse
· · · [StructItemQBKey]       | TextureProperty     | `tex\models\highway\Button_Grey_Highlight_01.dds`
· · StructHeader              |                     |
· · · [StructItemQBKey]       | Name                | m_startFade
· · · [StructItemQBKey]       | VectorProperty      | `tex\models\highway\Button_Grey_Highlight_01.dds`
