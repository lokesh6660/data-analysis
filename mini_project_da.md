# question on the given data "CAR DETAILS FROM CAR DEKHO"



```python
import pandas as pd

```


```python
df=pd.read_csv(r"C:\Users\hp\Desktop\CAR DETAILS FROM CAR DEKHO.csv")
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>name</th>
      <th>year</th>
      <th>selling_price</th>
      <th>km_driven</th>
      <th>fuel</th>
      <th>seller_type</th>
      <th>transmission</th>
      <th>owner</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Maruti 800 AC</td>
      <td>2007</td>
      <td>60000</td>
      <td>70000</td>
      <td>Petrol</td>
      <td>Individual</td>
      <td>Manual</td>
      <td>First Owner</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Maruti Wagon R LXI Minor</td>
      <td>2007</td>
      <td>135000</td>
      <td>50000</td>
      <td>Petrol</td>
      <td>Individual</td>
      <td>Manual</td>
      <td>First Owner</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Hyundai Verna 1.6 SX</td>
      <td>2012</td>
      <td>600000</td>
      <td>100000</td>
      <td>Diesel</td>
      <td>Individual</td>
      <td>Manual</td>
      <td>First Owner</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Datsun RediGO T Option</td>
      <td>2017</td>
      <td>250000</td>
      <td>46000</td>
      <td>Petrol</td>
      <td>Individual</td>
      <td>Manual</td>
      <td>First Owner</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Honda Amaze VX i-DTEC</td>
      <td>2014</td>
      <td>450000</td>
      <td>141000</td>
      <td>Diesel</td>
      <td>Individual</td>
      <td>Manual</td>
      <td>Second Owner</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>4335</th>
      <td>Hyundai i20 Magna 1.4 CRDi (Diesel)</td>
      <td>2014</td>
      <td>409999</td>
      <td>80000</td>
      <td>Diesel</td>
      <td>Individual</td>
      <td>Manual</td>
      <td>Second Owner</td>
    </tr>
    <tr>
      <th>4336</th>
      <td>Hyundai i20 Magna 1.4 CRDi</td>
      <td>2014</td>
      <td>409999</td>
      <td>80000</td>
      <td>Diesel</td>
      <td>Individual</td>
      <td>Manual</td>
      <td>Second Owner</td>
    </tr>
    <tr>
      <th>4337</th>
      <td>Maruti 800 AC BSIII</td>
      <td>2009</td>
      <td>110000</td>
      <td>83000</td>
      <td>Petrol</td>
      <td>Individual</td>
      <td>Manual</td>
      <td>Second Owner</td>
    </tr>
    <tr>
      <th>4338</th>
      <td>Hyundai Creta 1.6 CRDi SX Option</td>
      <td>2016</td>
      <td>865000</td>
      <td>90000</td>
      <td>Diesel</td>
      <td>Individual</td>
      <td>Manual</td>
      <td>First Owner</td>
    </tr>
    <tr>
      <th>4339</th>
      <td>Renault KWID RXT</td>
      <td>2016</td>
      <td>225000</td>
      <td>40000</td>
      <td>Petrol</td>
      <td>Individual</td>
      <td>Manual</td>
      <td>First Owner</td>
    </tr>
  </tbody>
</table>
<p>4340 rows × 8 columns</p>
</div>




```python
df.columns
```




    Index(['name', 'year', 'selling_price', 'km_driven', 'fuel', 'seller_type',
           'transmission', 'owner'],
          dtype='object')




```python
#1: name the car which is having the selling price more than 600000.
df[df["selling_price"]>600000]["name"]

```




    8                 Hyundai Creta 1.6 VTVT S
    12         Toyota Corolla Altis 1.8 VL CVT
    21                Hyundai Creta 1.6 VTVT S
    25         Toyota Corolla Altis 1.8 VL CVT
    27             Hyundai Venue SX Opt Diesel
                           ...                
    4311               Toyota Camry Hybrid 2.5
    4312                 Maruti Ertiga 1.5 VDI
    4313    Ford Endeavour 2.2 Titanium AT 4X2
    4332          Mahindra Scorpio S2 7 Seater
    4338      Hyundai Creta 1.6 CRDi SX Option
    Name: name, Length: 1057, dtype: object




```python
#2 name the car having manual transmission and also find how much km its driven.

df[df['transmission']=='Manual'][['name','km_driven']]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>name</th>
      <th>km_driven</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Maruti 800 AC</td>
      <td>70000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Maruti Wagon R LXI Minor</td>
      <td>50000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Hyundai Verna 1.6 SX</td>
      <td>100000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Datsun RediGO T Option</td>
      <td>46000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Honda Amaze VX i-DTEC</td>
      <td>141000</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>4335</th>
      <td>Hyundai i20 Magna 1.4 CRDi (Diesel)</td>
      <td>80000</td>
    </tr>
    <tr>
      <th>4336</th>
      <td>Hyundai i20 Magna 1.4 CRDi</td>
      <td>80000</td>
    </tr>
    <tr>
      <th>4337</th>
      <td>Maruti 800 AC BSIII</td>
      <td>83000</td>
    </tr>
    <tr>
      <th>4338</th>
      <td>Hyundai Creta 1.6 CRDi SX Option</td>
      <td>90000</td>
    </tr>
    <tr>
      <th>4339</th>
      <td>Renault KWID RXT</td>
      <td>40000</td>
    </tr>
  </tbody>
</table>
<p>3892 rows × 2 columns</p>
</div>




```python
#3name the list of the car having sold by first owner.


df[df['owner']=='Second Owner']['name']
```




    4                     Honda Amaze VX i-DTEC
    7                  Tata Indigo Grand Petrol
    17                    Honda Amaze VX i-DTEC
    20                 Tata Indigo Grand Petrol
    28        Chevrolet Enjoy TCDi LTZ 7 Seater
                           ...                 
    4330         Tata Indica Vista Aqua 1.4 TDI
    4333                        Maruti Ritz VDi
    4335    Hyundai i20 Magna 1.4 CRDi (Diesel)
    4336             Hyundai i20 Magna 1.4 CRDi
    4337                    Maruti 800 AC BSIII
    Name: name, Length: 1106, dtype: object




```python
#4 name the list of the car having selling price more than 10lac but manufacturring year will be 2010
a=df[df['selling_price']>1000000][['name','year']]
a[a["year"]==2010]["name"]
```




    163                    Jaguar XJ 5.0 L V8 Supercharged
    2685                          Audi Q5 2.0 TFSI Quattro
    3782                        Toyota Fortuner 3.0 Diesel
    3875    Land Rover Range Rover 4.4 Diesel LWB Vogue SE
    Name: name, dtype: object




```python
#5 find the most expensive car.
a=df["selling_price"].max()
df[df["selling_price"]==a]["name"]
```




    3872    Audi RS7 2015-2019 Sportback Performance
    Name: name, dtype: object




```python
#6 find the cheapest car.
df[df["selling_price"]==df["selling_price"].min()]["name"]
```




    2662    Ford Ikon 1.6 ZXI NXt
    Name: name, dtype: object




```python
#7 find the car which is max driven
df[df["km_driven"]==df["km_driven"].max()]["name"]
```




    1243    Maruti Swift VXI BSIII
    Name: name, dtype: object




```python
#8 find the car which is min driven
df[df["km_driven"]==df["km_driven"].min()]["name"]
```




    1312    Mahindra Quanto C6
    Name: name, dtype: object




```python
#9 what is the fule type and transmission of "Maruti car".
df[df["name"]=="Maruti 800 AC"][["name","fuel","transmission"]]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>name</th>
      <th>fuel</th>
      <th>transmission</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Maruti 800 AC</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Maruti 800 AC</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>175</th>
      <td>Maruti 800 AC</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>259</th>
      <td>Maruti 800 AC</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>372</th>
      <td>Maruti 800 AC</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>402</th>
      <td>Maruti 800 AC</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>669</th>
      <td>Maruti 800 AC</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>1284</th>
      <td>Maruti 800 AC</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>1446</th>
      <td>Maruti 800 AC</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>1726</th>
      <td>Maruti 800 AC</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>3181</th>
      <td>Maruti 800 AC</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>3215</th>
      <td>Maruti 800 AC</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>3217</th>
      <td>Maruti 800 AC</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>3259</th>
      <td>Maruti 800 AC</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>3285</th>
      <td>Maruti 800 AC</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>3314</th>
      <td>Maruti 800 AC</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>3503</th>
      <td>Maruti 800 AC</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>3630</th>
      <td>Maruti 800 AC</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>3652</th>
      <td>Maruti 800 AC</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>3740</th>
      <td>Maruti 800 AC</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>3856</th>
      <td>Maruti 800 AC</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>4088</th>
      <td>Maruti 800 AC</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>4323</th>
      <td>Maruti 800 AC</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
  </tbody>
</table>
</div>




```python
#or
df["name"].replace("Maruti 800 AC","Maruti Wagon R LXI Minor")
df[df["name"]=="Maruti Wagon R LXI Minor"][["name","fuel","transmission"]]

```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>name</th>
      <th>fuel</th>
      <th>transmission</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Maruti Wagon R LXI Minor</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Maruti Wagon R LXI Minor</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>113</th>
      <td>Maruti Wagon R LXI Minor</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>275</th>
      <td>Maruti Wagon R LXI Minor</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>392</th>
      <td>Maruti Wagon R LXI Minor</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>524</th>
      <td>Maruti Wagon R LXI Minor</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>697</th>
      <td>Maruti Wagon R LXI Minor</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>1174</th>
      <td>Maruti Wagon R LXI Minor</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>1321</th>
      <td>Maruti Wagon R LXI Minor</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>1555</th>
      <td>Maruti Wagon R LXI Minor</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>2010</th>
      <td>Maruti Wagon R LXI Minor</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>2638</th>
      <td>Maruti Wagon R LXI Minor</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>2774</th>
      <td>Maruti Wagon R LXI Minor</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>3033</th>
      <td>Maruti Wagon R LXI Minor</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>3104</th>
      <td>Maruti Wagon R LXI Minor</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>3450</th>
      <td>Maruti Wagon R LXI Minor</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>3468</th>
      <td>Maruti Wagon R LXI Minor</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>3502</th>
      <td>Maruti Wagon R LXI Minor</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>3573</th>
      <td>Maruti Wagon R LXI Minor</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>3918</th>
      <td>Maruti Wagon R LXI Minor</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>4022</th>
      <td>Maruti Wagon R LXI Minor</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>4050</th>
      <td>Maruti Wagon R LXI Minor</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>4155</th>
      <td>Maruti Wagon R LXI Minor</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
    <tr>
      <th>4183</th>
      <td>Maruti Wagon R LXI Minor</td>
      <td>Petrol</td>
      <td>Manual</td>
    </tr>
  </tbody>
</table>
</div>




```python
#10 what is the selling price of 'Toyota corolla Altis 1.8 VL CVT' car.
df[df['name']=='Toyota Corolla Altis 1.8 VL CVT'][["name",'selling_price']]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>name</th>
      <th>selling_price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>12</th>
      <td>Toyota Corolla Altis 1.8 VL CVT</td>
      <td>1650000</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Toyota Corolla Altis 1.8 VL CVT</td>
      <td>1650000</td>
    </tr>
  </tbody>
</table>
</div>




```python
#11 how many car who has first owner
a=df[df["owner"]=="First Owner"]["name"]
a.shape[0]
```




    2832




```python
#12 how many car is automatic
a=df[df["transmission"]=="Automatic"]["name"]
a.shape[0]
```




    448




```python
#13 how many car is manual.
a=df[df["transmission"]=="Manual"]["name"]
a.shape[0]
```




    3892




```python
#14 how many car is sold by the dealer
a=df[df["seller_type"]=="Dealer"]["name"]
a.shape[0]

```




    994




```python
#15 how many car is sold by the individual
a=df[df["seller_type"]=="Individual"]["name"]
a.shape[0]

```




    3244




```python
#16 how many car's whose fule is petrol
a=df[df["fuel"]=="Petrol"]["name"]
a.shape[0]

```




    2123




```python
#17 how many car's whose fule is diesel
a=df[df["fuel"]=="Diesel"]["name"]
a.shape[0]

```




    2153




```python
#18 how many car's whose fule is CNG
a=df[df["fuel"]=="CNG"]["name"]
a.shape[0]
```




    40




```python
#19 which car of petrol is max Km_driven

df[df["fuel"]=="Petrol"][["name","km_driven"]].max()

```




    name         Volkswagen Vento Petrol Highline AT
    km_driven                                 806599
    dtype: object




```python
#20 which car of petrol is min Km_driven

df[df["fuel"]=="Petrol"][["name","fuel","km_driven"]].min()


```




    name         Ambassador Grand 1800 ISZ MPFI PW CL
    fuel                                       Petrol
    km_driven                                     101
    dtype: object




```python
#21 which car of diesel is max Km_driven

df[df["fuel"]=="Diesel"][["name","fuel","km_driven"]].max()

```




    name         Volvo XC60 D5 Inscription
    fuel                            Diesel
    km_driven                       560000
    dtype: object




```python
#22 which car of diesel is min Km_driven

df[df["fuel"]=="Diesel"][["name","fuel","km_driven"]].min()

```




    name         Ambassador CLASSIC 1500 DSL AC
    fuel                                 Diesel
    km_driven                                 1
    dtype: object




```python
#23 which car of CNG is max Km_driven

df[df["fuel"]=="CNG"][["name","fuel","km_driven"]].max()

```




    name         Tata Indigo CS Emax CNG GLX
    fuel                                 CNG
    km_driven                         120000
    dtype: object




```python
#24 which car of CNG is min Km_driven

df[df["fuel"]=="CNG"][["name","fuel","km_driven"]].min()

```




    name         Chevrolet Aveo 1.4 CNG
    fuel                            CNG
    km_driven                      4000
    dtype: object




```python

```
