# Fetch Data of Any Country
 search to help people discover “proper” countries for names that might only actually be subdivisions. The fuzziness also includes normalizing unicode accents. There’s also a bit of prioritization included to prefer matches on country names before subdivision names and have countries with more matches be listed before ones with fewer matches:

>>> import pycountry
>>> len(pycountry.countries)
249
>>> list(pycountry.countries)[0]
Country(alpha_2='AF', alpha_3='AFG', name='Afghanistan', numeric='004', official_name='Islamic Republic of Afghanistan')
>>> germany = pycountry.countries.get(alpha_2='DE')
>>> germany
Country(alpha_2='DE', alpha_3='DEU', name='Germany', numeric='276', official_name='Federal Republic of Germany')
>>> germany.alpha_2
'DE'
>>> germany.alpha_3
'DEU'
>>> germany.numeric
'276'
>>> germany.name
'Germany'
>>> germany.official_name
'Federal Republic of Germany'
