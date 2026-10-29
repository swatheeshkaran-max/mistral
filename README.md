I am continuing a 3D boat-and-riverside modelling project in Blender. Please use all the context below.

PROJECT OBJECTIVE

Create a realistic 3D landscape integration for a floating-site project on the Seine near Bois de Boulogne, Paris.

The final image should show an insertion paysagère 3D from the opposite bank, looking toward the project site. The existing Galion is only a reference and must eventually be removed. It will be replaced by two boats, Chocolatine and Tivano, positioned parallel to the riverbank.

The work should be done in stages:
1. Model Chocolatine separately.
2. Model Tivano separately.
3. Model the riverside landscape separately.
4. Integrate both boats into the landscape.
5. Render the final view from the opposite bank.
BLENDER
- Blender version: 5.2.3.
- Use Metric units.
- 1 Blender unit = 1 metre.
- Keep all objects at real-world scale.
- Use separate collections and files:
  - chocolatine_model.blend
  - tivano_model.blend
  - riverside_landscape.blend
  - riverside_integration.blend
- Use common coordinates and document the origin/datum for each boat.
- Prefer linking or appending boat collections into the integration scene.
- Do not remodel the boats inside the landscape file.
- Scripts must be rerunnable and must not delete unrelated scene objects.
CURRENT GITHUB REPOSITORY

Existing repository:

https://github.com/swatheeshkaran-max/edf-dechargement-colis

The project materials are currently inside the mistral/ folder because a standalone Mistral repository was not available at the time.

Important files:
- mistral/README.md
- mistral/SOURCES.md
- mistral/IMAGE_MANIFEST.csv
- mistral/images/
- mistral/source_documents/official_vnf_notice_paris_bois_de_boulogne.pdf
- mistral/blender/riverside_first_draft.py
- mistral/blender/riverside_first_draft_v2.py
Use this corrected script:

https://github.com/swatheeshkaran-max/edf-dechargement-colis/blob/main/mistral/blender/riverside_first_draft_v2.py

The user may move these files into a new standalone repository called mistral.

SITE INFORMATION

Official site:

https://domaine-public-fluvial.vnf.fr/avis/plan-deau-etablissement-flottant-paris-bois-de-boulogne/

Approximate coordinates:
- Latitude: 48.8635008
- Longitude: 2.2285939
The project is near:
- 10 allée du bord de l’eau
- Bois de Boulogne
- 75016 Paris
- Seine river
The site is on the Bois de Boulogne side of the Seine. The camera should be placed on the opposite bank looking toward the project.

The official notice indicates:
- Water area: approximately 825 m².
- Maximum water envelope: approximately 55 m long × 15 m wide.
- Minimum water envelope shown in the notice: approximately 42 m × 6 m.
- Existing Galion: approximately 45 m × 7.60 m.
- Existing Galion has three levels:
  - main deck
  - upper deck
  - false/tween deck
- Existing site has gangways, mooring elements, nearby vegetation, a walking route and a small parking/access area.
- The site is flood-sensitive and subject to VNF and riverside regulations.
For the modelling context, use:
- 55 m site envelope
- 30 m upstream extension
- 30 m downstream extension
- Total riverside modelling length: approximately 115 m
Use a normal representative water level for the visual model. Set the water surface to Z = 0 unless better survey data is provided later.

COORDINATE SYSTEM

The current blockout uses:
- X = along the river
- Y = from the opposite bank toward the project bank
- Z = vertical
- Project bank approximately at Y = 0
- Water and boats toward negative Y
- Camera on the opposite bank, approximately:
  - location: (0, -68, 11)
  - looking toward: (0, 3, 2.5)
The blockout creates:
- 115 m river context
- opposite and project banks
- water plane
- project path and parking area
- 55 m × 15 m site-envelope markers
- two placeholder boats positioned parallel to the riverbank
- two simple gangways
- stylised vegetation
- camera and lighting
The placeholder boat dimensions in the blockout are approximate only:
- length: 42 m
- beam: 5.2 m
- height: 2.2 m
Do not treat these as final dimensions.

IMAGE AND SOURCE MATERIALS

The verified project images are stored in:

mistral/images/

They include:
- official VNF Galion river-facing view
- official VNF site plan
- official location map
- official aerial site context
- official aerial Galion footprint
The source PDF is:

mistral/source_documents/official_vnf_notice_paris_bois_de_boulogne.pdf

Use the images for geometry, vegetation, bank form, river orientation, gangway position and visual character. Do not use unrelated generic images. Satellite and Street View images may be used as reference only; do not assume they are suitable final textures without permission.

BOAT MODELLING

The two boats to be modelled are:
1. Chocolatine
2. Tivano
The existing Galion must be removed from the final concept and replaced with these two boats.

For each boat, model in a separate Blender file first. Keep the boat collection organised:
- hull
- deck
- superstructure
- cargo/tank areas if visible
- tween/intermediate decks if relevant
- gangway connection
- mooring points
- navigation/safety elements visible from the final camera
The Chocolatine technical PDF is:

BATCHOC-EPD-INCENDIE-Ind-A-2014.03.12-TF Copy.pdf

It is an A3 technical/fire-safety/deck plan. It is useful for understanding:
- deck arrangement
- longitudinal section
- internal layout
- visible superstructure
- fire and safety equipment locations
The user calls this boat Chocolatine. The title block may contain a slightly different spelling such as BATCHOC/Chocolaté. Treat the user’s name “Chocolatine” as the working name unless the technical source proves otherwise.

This PDF is not sufficient by itself for a precise external hull model. Before final modelling, obtain or verify:
- length overall
- beam
- draft
- hull side profile
- plan/top view
- bow and stern shape
- deck heights
- superstructure dimensions
- gangway location
- mooring locations
- photos of the real boat
- visible crane/equipment, if present
No complete Tivano technical model has been provided yet. Ask for Tivano drawings, dimensions or photographs before claiming dimensional accuracy.

LANDSCAPE MODELLING

The final landscape should include:
- Seine water surface
- opposite bank viewpoint
- project bank
- vegetation on both banks
- riverside path
- nearby access/parking
- bank edge and quay condition
- gangways
- mooring points
- site envelope
- two parallel boats
- realistic lighting and camera perspective
The camera should reproduce an architectural landscape-integration image rather than a top-down engineering view.

The final render should show the surrounding river and vegetation clearly enough to understand how the two boats sit in the landscape.

CURRENT SCRIPT ERROR

The first long script was pasted incompletely into Blender and stopped at:

def look_at(obj, target):

This produced:

IndentationError: expected an indented block after function definition

Use the complete corrected file:

mistral/blender/riverside_first_draft_v2.py

Open it directly in Blender’s Text Editor instead of copying a very long script through chat.

Do not rerun the original setup script after landscape objects exist because the original setup clears the scene. The v2 draft script only removes objects with the DRAFT2_ prefix and is safer to rerun.

MODELLING WORKFLOW

First:
1. Build Chocolatine as a separate real-scale model.
2. Build Tivano as a separate real-scale model.
3. Check each model from:
   - side view
   - top view
   - opposite-bank camera view
4. Create the landscape blockout.
5. Replace the placeholder boats with the finished boat collections.
6. Position both boats inside the official 55 m × 15 m site envelope.
7. Add gangways and mooring connections.
8. Test the final camera from the opposite bank.
9. Render a first integration image.
10. Refine terrain, vegetation, water, materials and lighting.
REMAINING INFORMATION NEEDED

Before precise boat integration, obtain:
- Chocolatine external dimensions and photographs
- Tivano external dimensions and photographs
- exact boat orientation
- exact mooring and gangway positions
- whether either boat has a crane or visible loading equipment
- intended separation between the two boats
- whether the boats should be shown loaded or empty
- preferred season, weather and time of day for the final render
When information is missing, use clearly labelled placeholders and assumptions. Do not present approximate placeholder geometry as verified real geometry.
