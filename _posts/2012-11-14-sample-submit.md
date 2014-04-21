---
category: Samples
path: '/api/samples/submit'
title: 'Submit Sample'
type: 'POST'

layout: nil
---

<div class="warning">
<b>JSON ONLY</b>: all features added 2014 and later only support JSON. XML support will be removed all together at some point in the future.
</div>

Create or edit a Sample. This is the API version of the [Submit Samples](https://submit.agvise.com/submit) page

### Parameters

<table>
    <thead>
        <tr>
            <th>Parameter</th>
            <th>Type</th>
            <th>Length</th>
            <th>Required</th>
            <th><em>Valid Values</em></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>sampleOrderType</td>
            <td>integer</td>
            <td> </td>
            <td>Yes</td>
            <td> 
                <table>
                    <tbody>
                        <tr>
                            <td><em>1</em></td>
                            <td>Conventional</td>
                        </tr>
                        <tr>
                            <td><em>2</em></td>
                            <td>Grid/Zone</td>
                        </tr>
                        <tr>
                            <td><em>3</em></td>
                            <td>Soybean Cyst Nematode</td>
                        </tr>
                    </tbody>
                </table>
            </td>
        </tr>
        <tr>
            <td>growerName</td>
            <td>string</td>
            <td>25</td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>growerAddress1</td>
            <td>string</td>
            <td>20</td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>growerAddress2</td>
            <td>string</td>
            <td>20</td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>growerCity</td>
            <td>string</td>
            <td>22</td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>growerState</td>
            <td>string</td>
            <td>2</td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>growerPostalCode</td>
            <td>string</td>
            <td>11</td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>growerAccountNumber</td>
            <td>string</td>
            <td>50</td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>growerSampler</td>
            <td>string</td>
            <td>25</td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>sampleDate</td>
            <td>date time in UTC</td>
            <td> </td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>fieldIdentifier</td>
            <td>string</td>
            <td>30</td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>fieldName</td>
            <td>string</td>
            <td>40</td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>fieldCounty</td>
            <td>string</td>
            <td>15</td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>fieldRange</td>
            <td>string</td>
            <td>15</td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>fieldTownship</td>
            <td>string</td>
            <td>15</td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>fieldSection</td>
            <td>integer</td>
            <td> </td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>fieldQuarter</td>
            <td>string</td>
            <td>15</td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>fieldTotalAcres</td>
            <td>decimal</td>
            <td> </td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>fieldYearSampled</td>
            <td>integer</td>
            <td> </td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>previousCrop</td>
            <td>string</td>
            <td>50</td>
            <td> </td>
            <td>See <b>Crops</b> list below</td>
        </tr>
        <tr>
            <td>manureApplied</td>
            <td>boolean</td>
            <td> </td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>cropSelection1</td>
            <td>string</td>
            <td>50</td>
            <td> </td>
            <td>See <b>Crops</b> list below</td>
        </tr>
        <tr>
            <td>yieldGoal1</td>
            <td>string</td>
            <td>50</td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>pkApplication1</td>
            <td>string</td>
            <td>50</td>
            <td> </td>
            <td> 
                <ul>
                    <li><em>Band</em></li>
                    <li><em>Band/Maint</em></li>
                    <li><em>Broadcast</em></li>
                    <li><em>Broadcast/Maint</em></li>
                    <li><em>University</em></li>
                    <li><em>Centrol</em></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>cropSelection2</td>
            <td>string</td>
            <td>50</td>
            <td> </td>
            <td>See <b>Crops</b> list below</td>
        </tr>
        <tr>
            <td>yieldGoal2</td>
            <td>string</td>
            <td>50</td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>pkApplication2</td>
            <td>string</td>
            <td>50</td>
            <td> </td>
            <td> 
                <ul>
                    <li><em>Band</em></li>
                    <li><em>Band/Maint</em></li>
                    <li><em>Broadcast</em></li>
                    <li><em>Broadcast/Maint</em></li>
                    <li><em>University</em></li>
                    <li><em>Centrol</em></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>cropSelection3</td>
            <td>string</td>
            <td>50</td>
            <td> </td>
            <td>See <b>Crops</b> list below</td>
        </tr>
        <tr>
            <td>yieldGoal3</td>
            <td>string</td>
            <td>50</td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>pkApplication3</td>
            <td>string</td>
            <td>50</td>
            <td> </td>
            <td> 
                <ul>
                    <li><em>Band</em></li>
                    <li><em>Band/Maint</em></li>
                    <li><em>Broadcast</em></li>
                    <li><em>Broadcast/Maint</em></li>
                    <li><em>University</em></li>
                    <li><em>Centrol</em></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>samples</td>
            <td>array of Sample</td>
            <td> </td>
            <td> </td>
            <td> </td>
        </tr>
        <tr><th colspan="5">Sample object</th></tr>
        <tr>
            <td>sampleIdentifier</td>
            <td>string</td>
            <td>50</td>
            <td>Yes</td>
            <td> </td>
        </tr>
        <tr>
            <td>uniqueIdentifier</td>
            <td>string</td>
            <td>50</td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>analysisOptions</td>
            <td>string</td>
            <td>1000</td>
            <td> </td>
            <td>See <b>Analysis Options</b> list below</td>
        </tr>
        <tr>
            <td>additionalAnalysisOptions</td>
            <td>array of string</td>
            <td> </td>
            <td> </td>
            <td>See <b>Additional Analysis Options</b> list below</td>
        </tr>
        <tr>
            <td>phosphorusOption</td>
            <td>string</td>
            <td>500</td>
            <td> </td>
            <td> 
                <ul>
                    <li><em>Olsen</em></li>
                    <li><em>Bray</em></li>
                    <li><em>Olsen &amp; Bray</em></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>depth1</td>
            <td>integer</td>
            <td> </td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>depth2</td>
            <td>integer</td>
            <td> </td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>depth3</td>
            <td>integer</td>
            <td> </td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>depth4</td>
            <td>integer</td>
            <td> </td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>startingDepthOf2nd</td>
            <td>integer</td>
            <td> </td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>acres</td>
            <td>string</td>
            <td>50</td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>previousCrop</td>
            <td>string</td>
            <td>250</td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>yieldGoal1Override</td>
            <td>string</td>
            <td>50</td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>yieldGoal2Override</td>
            <td>string</td>
            <td>50</td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>yieldGoal3Override</td>
            <td>string</td>
            <td>50</td>
            <td> </td>
            <td> </td>
        </tr>
        <tr>
            <td>electronicNumber</td>
            <td>string</td>
            <td>50</td>
            <td> </td>
            <td> </td>
        </tr>
    </tbody>
</table>

### Valid `Crops`
<ul>
    <li><em>Alfalfa</em></li>
    <li><em>Alfalfa Seed</em></li>
    <li><em>Barley</em></li>
    <li><em>Barley-Feed</em></li>
    <li><em>Barley-Malting</em></li>
    <li><em>Barley-Peas</em></li>
    <li><em>Beans-Edible</em></li>
    <li><em>Beans-Navy</em></li>
    <li><em>Beans-Pinto</em></li>
    <li><em>Brome Grass Seed</em></li>
    <li><em>Buckwheat</em></li>
    <li><em>Canary Seed</em></li>
    <li><em>Cane</em></li>
    <li><em>Canola-bu</em></li>
    <li><em>Canola-lb</em></li>
    <li><em>Carrots</em></li>
    <li><em>Chickpeas</em></li>
    <li><em>Clover or Trefoil</em></li>
    <li><em>Corn NP/CP = .10</em></li>
    <li><em>Corn NP/CP = .15</em></li>
    <li><em>Corn NP/CP = .20</em></li>
    <li><em>Corn/Soybeans</em></li>
    <li><em>Corn-Grain</em></li>
    <li><em>Corn-Silage</em></li>
    <li><em>Corn-Sweet</em></li>
    <li><em>Cotton</em></li>
    <li><em>Crambe</em></li>
    <li><em>Durum</em></li>
    <li><em>Faba Beans</em></li>
    <li><em>Fallow</em></li>
    <li><em>Flax</em></li>
    <li><em>Grapes-Established</em></li>
    <li><em>Grass Seed</em></li>
    <li><em>Grass/Alfalfa</em></li>
    <li><em>Grass/Pasture</em></li>
    <li><em>Hay Barley</em></li>
    <li><em>Lawns</em></li>
    <li><em>Lentils</em></li>
    <li><em>Millet-Grain</em></li>
    <li><em>Milo</em></li>
    <li><em>Mustard</em></li>
    <li><em>Oat Silage</em></li>
    <li><em>Oats</em></li>
    <li><em>Oats-Barley</em></li>
    <li><em>Oats-Peas</em></li>
    <li><em>Onions</em></li>
    <li><em>Peanuts</em></li>
    <li><em>Peas-Field</em></li>
    <li><em>Peas-Green</em></li>
    <li><em>Pop Corn</em></li>
    <li><em>Potatoes</em></li>
    <li><em>Potatoes-Chip</em></li>
    <li><em>Potatoes-Irr.</em></li>
    <li><em>Rye</em></li>
    <li><em>S. Beets 130/100</em></li>
    <li><em>S. Beets 6 lbs</em></li>
    <li><em>S. Beets 7 lbs</em></li>
    <li><em>Safflower</em></li>
    <li><em>Sidney Sugar</em></li>
    <li><em>SMBSC Beets</em></li>
    <li><em>Sorghum-Grain</em></li>
    <li><em>Sorghum-Hay</em></li>
    <li><em>Sorghum-Silage</em></li>
    <li><em>Soybeans</em></li>
    <li><em>Sunflower</em></li>
    <li><em>Timothy</em></li>
    <li><em>Triticale</em></li>
    <li><em>Veg. Garden</em></li>
    <li><em>Wheat-High Pro.</em></li>
    <li><em>Wheat-Low Pro.</em></li>
    <li><em>Wheat-Spring</em></li>
    <li><em>Wheat-Winter</em></li>
</ul>

### Valid `States` and `Provinces`
<table>
    <tbody>
        <tr><td><em>AL</em></td><td>Alabama</td></tr>
        <tr><td><em>AK</em></td><td>Alaska</td></tr>
        <tr><td><em>AB</em></td><td>Alberta</td></tr>
        <tr><td><em>AZ</em></td><td>Arizona</td></tr>
        <tr><td><em>AR</em></td><td>Arkansas</td></tr>
        <tr><td><em>BC</em></td><td>British Columbia</td></tr>
        <tr><td><em>CA</em></td><td>California</td></tr>
        <tr><td><em>CO</em></td><td>Colorado</td></tr>
        <tr><td><em>CT</em></td><td>Connecticut</td></tr>
        <tr><td><em>DE</em></td><td>Delaware</td></tr>
        <tr><td><em>DC</em></td><td>District of Columbia</td></tr>
        <tr><td><em>FL</em></td><td>Florida</td></tr>
        <tr><td><em>GA</em></td><td>Georgia</td></tr>
        <tr><td><em>HI</em></td><td>Hawaii</td></tr>
        <tr><td><em>ID</em></td><td>Idaho</td></tr>
        <tr><td><em>IL</em></td><td>Illinois</td></tr>
        <tr><td><em>IN</em></td><td>Indiana</td></tr>
        <tr><td><em>IA</em></td><td>Iowa</td></tr>
        <tr><td><em>KS</em></td><td>Kansas</td></tr>
        <tr><td><em>KY</em></td><td>Kentucky</td></tr>
        <tr><td><em>LA</em></td><td>Louisiana</td></tr>
        <tr><td><em>ME</em></td><td>Maine</td></tr>
        <tr><td><em>MB</em></td><td>Manitoba</td></tr>
        <tr><td><em>MD</em></td><td>Maryland</td></tr>
        <tr><td><em>MA</em></td><td>Massachusetts</td></tr>
        <tr><td><em>MI</em></td><td>Michigan</td></tr>
        <tr><td><em>MN</em></td><td>Minnesota</td></tr>
        <tr><td><em>MS</em></td><td>Mississippi</td></tr>
        <tr><td><em>MO</em></td><td>Missouri</td></tr>
        <tr><td><em>MT</em></td><td>Montana</td></tr>
        <tr><td><em>NE</em></td><td>Nebraska</td></tr>
        <tr><td><em>NV</em></td><td>Nevada</td></tr>
        <tr><td><em>NB</em></td><td>New Brunswick</td></tr>
        <tr><td><em>NH</em></td><td>New Hampshire</td></tr>
        <tr><td><em>NJ</em></td><td>New Jersey</td></tr>
        <tr><td><em>NM</em></td><td>New Mexico</td></tr>
        <tr><td><em>NY</em></td><td>New York</td></tr>
        <tr><td><em>NL</em></td><td>Newfoundland and Labrador</td></tr>
        <tr><td><em>NC</em></td><td>North Carolina</td></tr>
        <tr><td><em>ND</em></td><td>North Dakota</td></tr>
        <tr><td><em>NT</em></td><td>Northwest Territories</td></tr>
        <tr><td><em>NS</em></td><td>Nova Scotia</td></tr>
        <tr><td><em>NU</em></td><td>Nunavut</td></tr>
        <tr><td><em>OH</em></td><td>Ohio</td></tr>
        <tr><td><em>OK</em></td><td>Oklahoma</td></tr>
        <tr><td><em>ON</em></td><td>Ontario</td></tr>
        <tr><td><em>OR</em></td><td>Oregon</td></tr>
        <tr><td><em>PA</em></td><td>Pennsylvania</td></tr>
        <tr><td><em>PE</em></td><td>Prince Edward Island</td></tr>
        <tr><td><em>QC</em></td><td>Quebec</td></tr>
        <tr><td><em>RI</em></td><td>Rhode Island</td></tr>
        <tr><td><em>SK</em></td><td>Saskatchewan</td></tr>
        <tr><td><em>SC</em></td><td>South Carolina</td></tr>
        <tr><td><em>SD</em></td><td>South Dakota</td></tr>
        <tr><td><em>TN</em></td><td>Tennessee</td></tr>
        <tr><td><em>TX</em></td><td>Texas</td></tr>
        <tr><td><em>UT</em></td><td>Utah</td></tr>
        <tr><td><em>VT</em></td><td>Vermont</td></tr>
        <tr><td><em>VA</em></td><td>Virginia</td></tr>
        <tr><td><em>WA</em></td><td>Washington</td></tr>
        <tr><td><em>WV</em></td><td>West Virginia</td></tr>
        <tr><td><em>WI</em></td><td>Wisconsin</td></tr>
        <tr><td><em>WY</em></td><td>Wyoming</td></tr>
        <tr><td><em>YT</em></td><td>Yuko</td></tr>
    </tbody>
</table>

### Valid `Analysis Options`
<ul>
    <li><em>A</em></li>
    <li><em>Alafalfa</em></li>
    <li><em>ALFALFA</em></li>
    <li><em>B</em></li>
    <li><em>C</em></li>
    <li><em>C1</em></li>
    <li><em>C3</em></li>
    <li><em>C5</em></li>
    <li><em>CANOLA/SUNFLOWER</em></li>
    <li><em>Canola/Sunflowers</em></li>
    <li><em>CZ</em></li>
    <li><em>CZS</em></li>
    <li><em>DEALER DEFAULT</em></li>
    <li><em>DEALER DEFAULT</em></li>
    <li><em>E</em></li>
    <li><em>EZ</em></li>
    <li><em>EZS</em></li>
    <li><em>F</em></li>
    <li><em>N</em></li>
    <li><em>N,P</em></li>
    <li><em>N,P,K</em></li>
    <li><em>N,P,K,OM</em></li>
    <li><em>N,P,K,pH,OM,Zn</em></li>
    <li><em>N,P,K,pH,OM,Zn,S</em></li>
    <li><em>N,P,K,Zn</em></li>
    <li><em>N,P,K,Zn,OM</em></li>
    <li><em>N,P,K,Zn,S,Salts</em></li>
    <li><em>Option A</em></li>
    <li><em>Option B</em></li>
    <li><em>Option C</em></li>
    <li><em>Option C1</em></li>
    <li><em>Option C3</em></li>
    <li><em>Option C5</em></li>
    <li><em>Option CZ</em></li>
    <li><em>Option CZS</em></li>
    <li><em>Option E</em></li>
    <li><em>Option EZ</em></li>
    <li><em>Option EZS</em></li>
    <li><em>Option F</em></li>
    <li><em>Option T (no N)</em></li>
    <li><em>Option T (with N)</em></li>
    <li><em>Other</em></li>
    <li><em>P,K,pH,Buffer</em></li>
    <li><em>P,K,pH,OM</em></li>
    <li><em>P,K,pH,OM,Buffer</em></li>
    <li><em>P,K,pH,OM,CEC</em></li>
    <li><em>P,K,pH,OM,Zn</em></li>
    <li><em>P,K,pH,OM,Zn,CEC</em></li>
    <li><em>P,K,pH,OM,Zn,S</em></li>
    <li><em>P,K,pH,Zn</em></li>
    <li><em>POTATO</em></li>
    <li><em>Potato</em></li>
    <li><em>Row Crop</em></li>
    <li><em>ROW CROP</em></li>
    <li><em>SMALL GRAIN</em></li>
    <li><em>Small Grain</em></li>
    <li><em>Soy Bean (North)</em></li>
    <li><em>Soybean (South)</em></li>
    <li><em>SOYBEANS-NORTH</em></li>
    <li><em>SOYBEANS-SOUTH</em></li>
    <li><em>SUGAR BEET</em></li>
    <li><em>Sugar Beet</em></li>
    <li><em>T</em></li>
</ul>

### Valid `Additional Analysis Options`
<ul>
    <li><em>Boron</em></li>
    <li><em>Buffer pH</em></li>
    <li><em>Calcium</em></li>
    <li><em>Carbonates</em></li>
    <li><em>Chloride</em></li>
    <li><em>Copper</em></li>
    <li><em>Iron</em></li>
    <li><em>Magnesium</em></li>
    <li><em>Manganese</em></li>
    <li><em>Nitrogen</em></li>
    <li><em>Organic Matter</em></li>
    <li><em>pH</em></li>
    <li><em>Phosphorus</em></li>
    <li><em>Potassium</em></li>
    <li><em>Salts</em></li>
    <li><em>Sodium</em></li>
    <li><em>Sulfur</em></li>
    <li><em>Texture</em></li>
    <li><em>Zinc</em></li>
</ul>


### Request

```
{
    "SampleOrderID": 0,
    "SampleOrderType": 2,
    "GrowerName": "ABC Grower Name",
    "GrowerAddress1": "123 Fake St",
    "GrowerAddress2": "Suite 650",
    "GrowerCity": "Grand Forks",
    "GrowerState": "ND",
    "GrowerPostalCode": "22222",
    "GrowerAccountNumber": "0123456789",
    "GrowerSampler": "Sampler 123",
    "SampleDate": "2014-04-05T15:57:27.669Z",
    "FieldIdentifier": "123-A",
    "FieldName": "23-A Field",
    "FieldCounty": "Fargo",
    "FieldRange": "12",
    "FieldTownship": "Hatton",
    "FieldSection": 25,
    "FieldQuarter": "NE",
    "FieldTotalAcres": 902.5,
    "FieldYearSampled": 2012,
    "PreviousCrop": null,
    "ManureApplied": null,
    "CropSelection1": "Barley",
    "YieldGoal1": "90",
    "PKApplication1": "University",
    "CropSelection2": "S. Beets 6 lbs",
    "YieldGoal2": "20",
    "PKApplication2": "Broadcast",
    "CropSelection3": "Barley-Feed",
    "YieldGoal3": "80",
    "PKApplication3": "Broadcast/Maint",
    "Samples": [
    {
        "ReferenceNumber": 0,
        "SampleIdentifier": "111",
        "UniqueIdentifier": "222",
        "AnalysisOptions": "DEALER DEFAULT",
        "AdditionalAnalysisOptions": [
            "Phosphorus",
            "Potassium"
        ],
        "PhosphorusOption": "",
        "Depth1": 24,
        "Depth2": 48,
        "Depth3": null,
        "Depth4": null,
        "StartingDepthOf2nd": 24,
        "Acres": "100",
        "PreviousCrop": "Canola-bu",
        "YieldGoal1Override": "90",
        "YieldGoal2Override": "20",
        "YieldGoal3Override": "80",
        "ElectronicNumber": "98765"
    },
    {
        "ReferenceNumber": 0,
        "SampleIdentifier": "112",
        "UniqueIdentifier": "223",
        "AnalysisOptions": "DEALER DEFAULT",
        "AdditionalAnalysisOptions": [
            "Phosphorus",
            "Potassium"
        ],
        "PhosphorusOption": "",
        "Depth1": 24,
        "Depth2": 48,
        "Depth3": null,
        "Depth4": null,
        "StartingDepthOf2nd": 24,
        "Acres": "100",
        "PreviousCrop": "Canola-bu",
        "YieldGoal1Override": "90",
        "YieldGoal2Override": "20",
        "YieldGoal3Override": "80",
        "ElectronicNumber": "98765"
        }
    ]
}
```

### Response

Sends back the full details of the sample you sumbitted including the assigned SampleOrderID and sample ReferenceNumber

In order to return validiation messages, the response of this request is slightly different then the usualy way. The same ApiResponse object containing top level <em>data</em>  and <em>error</em> objects is returned for both success and failure. 

### Success

* `200 OK` on success,

```
{
    "data": {
        "sampleOrderID": 12345,
        "sampleOrderType": 2,
        ....
    }
    "error": null
}
```

### Error

Error responses are simply returning [standard HTTP error codes](http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html) along with some additional information:

```
{
    "data": null
    "error": {
        "message": "Failed to save sample data due to validation errors.",
        "validationErrors": [
            "Grower State is not a recognized value.",
            "PKApplication1 is not a recognized value.",
            "PhosphorusOption is not a recognized value.",
            "PreviousCrop is not a recognized value.",
            "AnalysisOptions is not a recognized value.",
            "AdditionalAnalysisOptions contains a value that is not recognized."
        ]
    }
}
```
