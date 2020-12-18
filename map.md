```python
import folium
phone_map = folium.Map()
```


```python
# Top three smart phone companies by market share in 2016
companies = [
    {'loc': [37.4970,  127.0266], 'label': 'Samsung: 20.5 %'},
    {'loc': [37.3318, -122.0311], 'label': 'Apple: 14.4 %'},
    {'loc': [22.5431,  114.0579], 'label': 'Huawei: 8.9%'}] 

# Adding markers to the map
for company in companies:
    marker = folium.Marker(location=company['loc'], popup = company['label'])
    marker.add_to(phone_map)

    phone_map
```
