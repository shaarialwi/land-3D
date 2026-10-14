# MRANTI Park Spatial Explorer

## Open and publish
Open index.html directly in Chrome, Edge or Safari. No installation or API key is required.

1. Unzip this package.
2. Create a GitHub repository, for example mranti-park-3d.
3. Upload index.html to the repository root (not the ZIP). The JSON and README are optional reference files; the HTML contains the data already.
4. In the repository, open Settings > Pages.
5. Under Build and deployment, choose Deploy from a branch, then main and / (root). Save.
6. Wait for the deployment to finish and open the URL shown by GitHub Pages, usually https://YOUR-USERNAME.github.io/mranti-park-3d/.

## Controls
Drag the map to rotate and adjust tilt. Shift-drag pans. Scroll or use + / − to zoom. Click a polygon or select an outline from the list. Search temporary IDs such as P001 or the DXF entity handle. The sliders control extrusion and view angle. Open lines can be hidden; 2D gives a top view.

## Source and limitations
Source: Lots Mranti GIS WGS Closed PL.dxf.
146 LWPOLYLINE entities on the Lots layer: 126 marked closed and 20 open. All 2,821 vertices are retained; none have arc bulges. Open lines remain open and are not turned into land parcels. IDs P001–P146 follow DXF entity order and are NOT official plot numbers.

The source has no plot names, land use, building geometry or heights. Colours distinguish geometry visually, not zoning or ownership. Extrusion is a uniform illustrative display height, not a surveyed measurement. No terrain or building model is implied. Overlapping or nested source polygons are retained; no cadastral topology validation has been performed.

Coordinates are interpreted as longitude/latitude based on the WGS filename and ranges (101.6733–101.7049, 3.0380–3.0591). DXF units are unspecified and CRS is unconfirmed. The viewer uses a local approximate metre projection centred on the source extent. N* indicates north under this interpretation. Do not use this prototype for survey measurements or legal boundaries.

The map is a static HTML Canvas 3D projection of extruded source geometry. No third-party runtime dependencies, remote imagery, login or backend are required. The site has no data editing or saving functionality. Browser execution has not been visually verified in this environment; automated checks cover source counts, JS syntax, rendering calls and key controls.

## Next data to add
A mapping of CAD handle to official plot name, land use and display colour; confirmed CRS; building footprints and measured heights for a more detailed park model.
