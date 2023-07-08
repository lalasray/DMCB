## DMCB
Benchmarking marker-based vs marker-less motion capture systems

### Motion source files.
  1. Basic Motions : s1_(walking*, acting); https://cvssp.org/data/totalcapture/ , s4_combo(1,2,3,4); http://humaneva.is.tue.mpg.de/datasets_human_2
  2. Fast Motions: s3_(walking*, freestyle); https://cvssp.org/data/totalcapture/ , Hasaposerviko, Pentozali; http://dancedb.eu/
  3. Extreme angle motions: s1;https://dfkide-my.sharepoint.com/:f:/g/personal/lara01_dfki_de/Eo4o7xAHIXpNtowdbY4EWWIBBZd9a-Bj23O4dKCCwi8qRg?e=vog0uk , lar_(1,2,3,4,5): https://poseprior.is.tue.mpg.de/

### SMPL body sources.
  1. Male_small: s_m.fbx
  2. Male_average: m_m.fbx
  3. Male_heavy: h_m.fbx
  4. Female_small: s_f.fbx
  5. Female_medium: m_f.fbx
  6. Female heavy: h_f.fbx
     
### Cloth source files.
  1. Simply Asset pack: https://blendermarket.com/products/simply-asset-packs

### Simulation Parameters.
  1. For translating kinematic based motion capture to AMASS mesh: https://github.com/vchoutas/smplify-x + https://github.com/nghorbani/soma 
  2. Soft-tissue dynamics: https://github.com/nghorbani/moshpp + https://github.com/nghorbani/amass, vertex groups can be soft body materails as defined in; softbody.txt
  3. Cloth simulation: https://blendermarket.com/products/simply-cloth
  4. Collision parmaeters: collision.txt
  5. CLoth material: Custom_mat.txt
     
### Marker based MocaP simulation:
  1. Motion retargeting: https://github.com/Meshcapade/SMPL_blender_addon + https://blendermarket.com/products/auto-rig-pro
  2. Marker pacement: Find the index nearest vertex at the front and back of each skeletal joint of the SMPL mesh after simulating desired cloth over it. (NEED TO BE DONE EVRY TIME SINCE THE VERTX INDEX LIST IS RANDOMIZED EVRY TIME)
  3. Pose extraction: extract.py
  4. Marklerless pose estimation: https://github.com/vladmandic/blazepose, https://github.com/facebookresearch/VideoPose3D
  5. Forward kinematics: https://github.com/lalasray/helper_video2bvh
