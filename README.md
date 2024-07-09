# Alcohol outlets in Baltimore

For a reporting project, I've been looking at alcohol outlets in Baltimore. The city sent me their most recent "master list" of the businesses licensed to sell alcohol, including their name and address. **File: 240520_Baltimore_master.csv**

I geocoded the data, looked at values that didn't code propertly, and integrated cleaning code and ultimately some manual changes to get them all to generate latitude and longituded. **Jupyter notebook: Baltimore alcohol cleaning and geocoding.**

Then with a big boost to start from TA Thomas, I identifed outlets with particular license-types that are not allowed to be in residential areas, but appear to be. **Jupyter notebook: identifying zoning**

I output a list of these irregular outlets. And I pushed the data — first from Python to CSV, then to Geojson, then to Mapbox — into a map that shows the residentially zoned areas, the alcohol outlets, those the Baltimore City government concedes are out of conformance with zoning law, and the couple dozen outlets that appear to be based on my analysis. 

<iframe width='100%' height='400px' src="https://api.mapbox.com/styles/v1/tedalcorn/cly9350pm00lg01r1hpel7y3x.html?title=false&access_token=pk.eyJ1IjoidGVkYWxjb3JuIiwiYSI6ImNseGRpNGdvNzA2enUyanBzbGI2YTRjNjIifQ.Z92PAuKJ9CpLevlKT0y9vw&zoomwheel=false#13.51/39.2935/-76.63234" title="Baltimore liquor licenses" style="border:none;"></iframe>
