### Introduction
This is the recorded responeses simulated using FEM software DIANA FEA (V10.3), which models a three-story two-bay reinforced concrete planar frame. 100 ground motions are applied at the base, and the accelerations at the center of each story and the ground is recorded. Damage states are modeled as the reduction of stiffnesses of columns of stories. The unit of recorded responses is mm/sec<sup>2. 

### Organization
Each folder contains 100 simulations of a damage state. The damage state for each folder is listed below:

* `Undamage/`: No damage;
* `1_80%/`: 80% (i.e., 20% reduction) of the original stiffness of 1<sup>st</sup> story columns;
* `1_90%/`: 90% (i.e., 10% reduction) of the original stiffness of 1<sup>st</sup> story columns;
* `2_80%/`: 80% of the original stiffness of 2<sup>nd</sup>columns;
* `2_90%/`: 90% of the original stiffness of 2<sup>nd</sup> story columns;
* `3_80%/`: 80% of the original stiffness of 3<sup>rd</sup> story columns;
* `3_90%/`: 90% of the original stiffness of 3<sup>rd</sup> story columns;

### File format
Arrays of `.npy` file is in the shape of `(steps, 4)`, where the 4 columns corresponds to the accelerations of ground, roof of the 1<sup>st</sup> story, roof of the 2<sup>nd</sup> and roof of the 3<sup>rd</sup> story (i.e., roof of the structure).
