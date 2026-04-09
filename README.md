# rocket-macro-fc
A set of FreeCAD macros helpful when designing rockets

# Nosecone
---
Nosecone is a macro written to automagically(tm) create a parametric nosecone within a 
PartDesign body. The following aerodynamic profiles may be generated:

<img width="1185" height="531" alt="nosecones noseam" src="https://github.com/user-attachments/assets/2f5c81dc-f714-40fb-8b62-9ffd28b7eb11" />

(From left to right)
- Secant Ogive
- Tangent Ogive
- Parabolic
- Power Series
- Elliptical
- HAACK
- Biconic
- Conic

Nosecones parameters are input in a pop-up window:

<img width="303" height="434" alt="nosecone macro gui" src="https://github.com/user-attachments/assets/b7462ff8-7012-4a9b-a6fc-259e9b772962" />
  
## Description of Nosecone Geometry:
---
The nosecone consists of the 'profile' section, and the 'shoulder' section. The profile is the 
pointy bit, with a specified profile curve.

This curve has a given length and base diameter. The length is defined by the 'fineness ratio', 
which is the ratio between the length and base diameter, L / D.

The shoulder section is used to locate the nosecone within a rocket's body tube. It is a 
cylindrical boss behind the profile section.

If specified, the nosecone will be made hollow, with a constant wall thickness, making a much 
lighter component, with room for stowed components.

## Current Limitations:
---
- Please note: at this time, the power series nosecone is unable to solve for thickness at low 
values of n.
- Nosecones all point along the x axis; this will be changed in coming versions.

## Planned Features:
---
- Addition of a NoseCone object that allow recomputation by altering data fields.
- Arbitrary orientation
- Accepting VarSet variables as inputs

## Other:
---
For Mathematical Descriptions of profiles: https://en.wikipedia.org/wiki/Nose_cone_design
