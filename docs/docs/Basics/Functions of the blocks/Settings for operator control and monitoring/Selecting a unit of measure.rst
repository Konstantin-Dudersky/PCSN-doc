Selecting a unit of measure
===========================

Coded unit of measure
---------------------
The parameter ``XXX_Unit`` is used to specify the unit of measure for the corresponding input parameter (XXX stands for a specific parameter, for example, ``PV_Unit``). Entry is carried out in the form of a code. Exactly one unit of measure is assigned to each code and is displayed on the faceplate.

You can interconnect the ``XXX_Unit`` input parameter of a technologic block with the ``XXXUnit`` output parameter of an analog input channel block. At the analog input channel block, enter the unit of measure at the XXXUnit input parameter (XXX stands for a specific parameter, for example ``PV_InUnit``, ``PVOutUnit``).

If the parameter value of ``XXX_Unit`` is out of range (that is, the value is not defined), the faceplate displays "!undef.!" in the place of unit.


.. note::
   Special notes for channel blocks PCS7AnIn, PCS7AnOu, FbAnIn and FbAnOu

   You can use the S7_enum attribute to display the unit in plain text in the CFC editor for these blocks.


.. note::
   In block icons, the update/refresh time of the units is 1 h. If the unit is changed from CFC, the new unit will be visible in the block icon after 1 hour or if the process picture is reloaded. In faceplates, the update/refresh time of the units is 5 seconds, so the new unit will be visible after 5 s.


Overview of the units of measure
--------------------------------
The units of measure are listed in the following tables.

List of the most commonly used units of measure in accordance with IEC 61158.

.. ⁰¹²³⁴⁵⁶⁷⁸⁹-₀₁₂₃₄₅₆₇₈₉

.. list-table::
   :header-rows: 1

   * - Value
     - Display
     - Description
   * - 1000
     - K
     - Kelvin
   * - 1001
     - °C
     - Degrees Celsius
   * - 1002
     - °F
     - Degrees Fahrenheit
   * - 1005
     - °
     - Degree
   * - 1006
     - \\'
     - Minute
   * - 1007
     - \\"
     - Second
   * - 1010
     - m
     - Meter
   * - 1013
     - mm
     - Millimeter
   * - 1018
     - ft
     - Foot
   * - 1023
     - m²
     - Square meter
   * - 1038
     - L
     - Liter
   * - 1041
     - hl
     - Hectoliter
   * - 1054
     - s
     - Second
   * - 1058
     - min
     - Minute
   * - 1059
     - h
     - Hour
   * - 1060
     - d
     - Day
   * - 1061
     - m/s
     - Meters per second
   * - 1077
     - Hz
     - Hertz
   * - 1081
     - kHz
     - Kilohertz
   * - 1082
     - 1/s
     - Per second
   * - 1083
     - 1/min
     - Per minute
   * - 1088
     - kg
     - Kilogram
   * - 1092
     - t
     - Metric ton
   * - 1100
     - g/cm³
     - Grams per cubic centimeter
   * - 1105
     - g/L
     - Grams per liter
   * - 1120
     - N
     - Newton
   * - 1123
     - mN
     - Millinewton
   * - 1130
     - Pa
     - Pascal
   * - 1133
     - kPa
     - Kilopascal
   * - 1137
     - bar
     - Bar
   * - 1138
     - mbar
     - Millibar
   * - 1149
     - mmH₂O
     - Millimeters of water
   * - 1175
     - W·h
     - Watt hour
   * - 1179
     - kW·h
     - Kilowatt hour
   * - 1181
     - kcal :sub:`th`
     - Kilocalories
   * - 1190
     - kW
     - Kilowatt
   * - 1209
     - A
     - Ampere
   * - 1211
     - mA
     - Milliampere
   * - 1221
     - A·h
     - Ampere hour
   * - 1240
     - V
     - Volt
   * - 1349
     - m³/h
     - Cubic meters per hour
   * - 1353
     - L/h
     - Liters per hour
   * - 1384
     - mol
     - Mol
   * - 1422
     - pH
     - pH value


List of all units of measure in accordance with IEC 61158

.. list-table::
   :header-rows: 1

   * - Value
     - Display
     - Description
   * - 1000
     - K
     - Kelvin
   * - 1001
     - °C
     - Degrees Celsius
   * - 1002
     - °F
     - Degrees Fahrenheit
   * - 1003
     - °R
     - Degree Rankine
   * - 1004
     - rad
     - Radian
   * - 1005
     - °
     - Degree
   * - 1006
     - \\'
     - Minute
   * - 1007
     - \\"
     - Second
   * - 1008
     - gon
     - Gon
   * - 1009
     - r
     - Revolution
   * - 1010
     - m
     - Meter
   * - 1011
     - km
     - Kilometer
   * - 1012
     - cm
     - Centimeter
   * - 1013
     - mm
     - Millimeter
   * - 1014
     - μm
     - Micrometer
   * - 1015
     - nm
     - Nanometer
   * - 1016
     - pm
     - Picometer
   * - 1017
     - Å
     - Angstrom
   * - 1018
     - ft
     - Foot
   * - 1019
     - in
     - Inch
   * - 1020
     - yd
     - Yard
   * - 1021
     - mile
     - Mile
   * - 1022
     - nautical mile
     - Nautical mile
   * - 1023
     - m²
     - Square meter
   * - 1024
     - km²
     - Square kilometer
   * - 1025
     - cm²
     - Square centimeter
   * - 1026
     - dm²
     - Square decimeter
   * - 1027
     - mm²
     - Square millimeter
   * - 1028
     - a
     - Are
   * - 1029
     - ha
     - Hectare
   * - 1030
     - in²
     - Square inch
   * - 1031
     - ft²
     - Square foot
   * - 1032
     - yd²
     - Square yard
   * - 1033
     - mile²
     - Square mile
   * - 1034
     - m³
     - Cubic meter
   * - 1035
     - dm³
     - Cubic decimeter
   * - 1036
     - cm³
     - Cubic centimeter
   * - 1037
     - mm³
     - Cubic millimeter
   * - 1038
     - L
     - Liter
   * - 1039
     - cl
     - Centiliter
   * - 1040
     - ml
     - Milliliter
   * - 1041
     - hl
     - Hectoliter
   * - 1042
     - in³
     - Cubic inch
   * - 1043
     - ft³
     - Cubic foot
   * - 1044
     - yd³
     - Cubic yard
   * - 1045
     - mile³
     - Cubic mile
   * - 1046
     - pint
     - Pint
   * - 1047
     - quart
     - Quart
   * - 1048
     - gal
     - US gallon
   * - 1049
     - ImpGal
     - Imperial gallon
   * - 1050
     - bushel
     - Bushel
   * - 1051
     - bbl
     - Barrel = 42 gallons
   * - 1052
     - bbl(liq)
     - Liquid barrel = 31.5 gallons
   * - 1053
     - ft³ std.
     - Standard cubic foot
   * - 1054
     - s
     - Second
   * - 1055
     - ks
     - Kilosecond
   * - 1056
     - ms
     - Millisecond
   * - 1057
     - μs
     - Microsecond
   * - 1058
     - min
     - Minute
   * - 1059
     - h
     - Hour
   * - 1060
     - d
     - Day
   * - 1061
     - m/s
     - Meters per second
   * - 1062
     - mm/s
     - Millimeters per second
   * - 1063
     - m/h
     - Meters per hour
   * - 1064
     - km/h
     - Kilometers per hour
   * - 1065
     - knot
     - Knot
   * - 1066
     - in/s
     - Inches per second
   * - 1067
     - ft/s
     - Feet per second
   * - 1068
     - yd/s
     - Yards per second
   * - 1069
     - in/min
     - Inches per minute
   * - 1070
     - ft/min
     - Feet per minute
   * - 1071
     - yd/min
     - Yards per minute
   * - 1072
     - in/h
     - Inches per hour
   * - 1073
     - ft/h
     - Feet per hour
   * - 1074
     - yd/h
     - Yards per hour
   * - 1075
     - mi/h
     - Miles per hour
   * - 1076
     - m/s²
     - Meter/second squared
   * - 1077
     - Hz
     - Hertz
   * - 1078
     - THz
     - Terahertz
   * - 1079
     - GHz
     - Gigahertz
   * - 1080
     - MHz
     - Megahertz
   * - 1081
     - kHz
     - Kilohertz
   * - 1082
     - 1/s
     - Per second
   * - 1083
     - 1/min
     - Per minute
   * - 1084
     - r/s
     - Revolutions per second
   * - 1085
     - rpm
     - Revolutions per minute
   * - 1086
     - rad/s
     - Radians per second
   * - 1087
     - 1/s²
     - Per second squared
   * - 1088
     - kg
     - Kilogram
   * - 1089
     - g
     - Gram
   * - 1090
     - mg
     - Milligram
   * - 1091
     - Mg
     - Megagram
   * - 1092
     - t
     - Metric ton
   * - 1093
     - oz
     - Ounce
   * - 1094
     - lb
     - Pound
   * - 1095
     - STon
     - US ton (short ton)
   * - 1096
     - LTon
     - British ton (long ton)
   * - 1097
     - kg/m³
     - Kilograms per cubic meter
   * - 1098
     - Mg/dm³
     - Megagrams per cubic meter
   * - 1099
     - kg/dm³
     - Kilograms per cubic decimeter
   * - 1100
     - g/cm³
     - Grams per cubic centimeter
   * - 1101
     - g/m³
     - Grams per cubic meter
   * - 1102
     - t/m³
     - Metric tons per cubic meter
   * - 1103
     - kg/L
     - Kilogram per liter
   * - 1104
     - g/ml
     - Grams per milliliter
   * - 1105
     - g/L
     - Grams per liter
   * - 1106
     - lb/in³
     - Pounds per cubic inch
   * - 1107
     - lb/ft³
     - Pounds per cubic foot
   * - 1108
     - lb/gal
     - Pounds per US gallon
   * - 1109
     - STon/yd³
     - US tons per cubic yard
   * - 1110
     - °Twad
     - Degree Twaddell
   * - 1111
     - °Baum (hv)
     - Degree Baumé (heavy)
   * - 1112
     - °Baum (lt)
     - Degree Baumé (light)
   * - 1113
     - °API
     - Degrees API
   * - 1114
     - SGU
     - Specific gravity units
   * - 1115
     - kg/m
     - Kilograms per meter
   * - 1116
     - mg/m
     - Milligrams per meter
   * - 1117
     - tex
     - Tex
   * - 1118
     - kg·m²
     - Kilograms per square meter
   * - 1119
     - kg·m/s
     - Kilograms per meter per second
   * - 1120
     - N
     - Newton
   * - 1121
     - MN
     - Meganewton
   * - 1122
     - kN
     - Kilonewton
   * - 1123
     - mN
     - Millinewton
   * - 1124
     - μN
     - Micronewton
   * - 1125
     - kg·m²/s
     - Kilograms per square meter per second
   * - 1126
     - N·m
     - Newton meter
   * - 1127
     - MN·m
     - Meganewton meter
   * - 1128
     - kN·m
     - Kilonewton meter
   * - 1129
     - mN·m
     - Millinewton meter
   * - 1130
     - Pa
     - Pascal
   * - 1131
     - GPa
     - Gigapascal
   * - 1132
     - MPa
     - Megapascal
   * - 1133
     - kPa
     - Kilopascal
   * - 1134
     - mPa
     - Millipascal
   * - 1135
     - μPa
     - Micropascal
   * - 1136
     - hPa
     - Hectopascal
   * - 1137
     - bar
     - Bar
   * - 1138
     - mbar
     - Millibar
   * - 1139
     - torr
     - Torr
   * - 1140
     - atm
     - Atmosphere
   * - 1141
     - psi
     - Pounds per square inch
   * - 1142
     - psia
     - Pounds per square inch (absolute)
   * - 1143
     - psig
     - Pounds per square inch (gauge)
   * - 1144
     - g/cm²
     - Grams per square centimeter
   * - 1145
     - kg/cm²
     - Kilograms per square centimeter
   * - 1146
     - inH₂O
     - Inches of water
   * - 1147
     - inH₂O (4°C)
     - Inches of water at 4 degrees Celsius
   * - 1148
     - inH₂O (68°F)
     - Inches of water at 68 degrees Fahrenheit
   * - 1149
     - mmH₂O
     - Millimeters of water1
   * - 1150
     - mmH₂O (4°C)
     - Millimeters of water at 4 degrees Celsius1
   * - 1151
     - mmH₂O (68°F)
     - Millimeters of water at 68 degrees Fahrenheit1
   * - 1152
     - ftH₂O
     - Feet of water1
   * - 1153
     - ftH₂O (4°C)
     - Feet of water at 4 degrees Celsius1
   * - 1154
     - ftH₂O (68°F)
     - Feet of water at 68 degrees Fahrenheit1
   * - 1155
     - inHg
     - Inches of mercury
   * - 1156
     - inHg (0°C)
     - Inches of mercury at 0 degrees Celsius
   * - 1157
     - mmHg
     - Millimeters of mercury
   * - 1158
     - mmHg (0°C)
     - Millimeters of mercury at 0 degrees Celsius
   * - 1159
     - Pa·s
     - Pascal second
   * - 1160
     - m²/s
     - Square meters per second
   * - 1161
     - P
     - Poise
   * - 1162
     - cP
     - Centipoise
   * - 1163
     - St
     - Stokes
   * - 1164
     - cSt
     - Centistokes
   * - 1165
     - N/m
     - Newtons per meter
   * - 1166
     - mN/m
     - Millinewtons per meter
   * - 1167
     - J
     - Joule
   * - 1168
     - EJ
     - Exajoule
   * - 1169
     - PJ
     - Petajoule
   * - 1170
     - TJ
     - Terajoule
   * - 1171
     - GJ
     - Gigajoule
   * - 1172
     - MJ
     - Megajoule
   * - 1173
     - kJ
     - Kilojoule
   * - 1174
     - mJ
     - Millijoule
   * - 1175
     - W·h
     - Watt hour
   * - 1176
     - TW·h
     - Terawatt hour
   * - 1177
     - GW·h
     - Gigawatt hour
   * - 1178
     - MW·h
     - Megawatt hour
   * - 1179
     - kW·h
     - Kilowatt hour
   * - 1180
     - calth
     - Calorie (thermo chemical)1
   * - 1181
     - kcal :sub:`th`
     - Kilocalorie (thermo chemical)1
   * - 1182
     - Mcalth
     - Megacalorie (thermo chemical)1
   * - 1183
     - Btuth
     - British thermal unit1
   * - 1184
     - datherm
     - Decatherm
   * - 1185
     - ft·lbf
     - Foot pound
   * - 1186
     - W
     - Watt
   * - 1187
     - TW
     - Terawatt
   * - 1188
     - GW
     - Gigawatt
   * - 1189
     - MW
     - Megawatt
   * - 1190
     - kW
     - Kilowatt
   * - 1191
     - mW
     - Milliwatt
   * - 1192
     - μW
     - Microwatt
   * - 1193
     - nW
     - Nanowatt
   * - 1194
     - pW
     - Picowatt
   * - 1195
     - Mcalth/h
     - Megacalorie per hour1
   * - 1196
     - MJ/h
     - Megajoule per hour
   * - 1197
     - Btuth/h
     - British thermal units per hour1
   * - 1198
     - hp
     - Horsepower
   * - 1199
     - W/(m·K)
     - Watts per meter kelvin
   * - 1200
     - W/(m²·K)
     - Watts per (square meter kelvin)
   * - 1201
     - m²·K/W
     - Square meters kelvin per Watt
   * - 1202
     - J/K
     - Joules per kelvin
   * - 1203
     - kJ/K
     - Kilojoules per kelvin
   * - 1204
     - J/(kg·K)
     - Joules per (kilogram kelvin)
   * - 1205
     - kJ/(kg·K)
     - Kilojoules per (kilogram kelvin)
   * - 1206
     - J/kg
     - Joules per kilogram
   * - 1207
     - MJ/kg
     - Megajoules per kilogram
   * - 1208
     - kJ/kg
     - Kilojoules per kilogramm
   * - 1209
     - A
     - Ampere
   * - 1210
     - kA
     - Kiloampere
   * - 1211
     - mA
     - Milliampere
   * - 1212
     - μA
     - Microampere
   * - 1213
     - nA
     - Nanoampere
   * - 1214
     - pA
     - Picoampere
   * - 1215
     - C
     - Coulomb
   * - 1216
     - MC
     - Megacoulomb
   * - 1217
     - kC
     - Kilocoulomb
   * - 1218
     - μC
     - Microcoulomb
   * - 1219
     - nC
     - Nanocoulomb
   * - 1220
     - pC
     - Picocoulomb
   * - 1221
     - A·h
     - Ampere hour
   * - 1222
     - C/m³
     - Coulombs per cubic meter
   * - 1223
     - C/mm³
     - Coulombs per cubic millimeter
   * - 1224
     - C/cm³
     - Coulombs per cubic centimeter
   * - 1225
     - kC/m³
     - Kilocoulombs per cubic meter
   * - 1226
     - mC/m³
     - Millicoulombs per cubic meter
   * - 1227
     - μC/m³
     - Microcoulombs per cubic meter
   * - 1228
     - C/m²
     - Coulombs per square meter
   * - 1229
     - C/mm²
     - Coulombs per square millimeter
   * - 1230
     - C/cm²
     - Coulombs per square centimeter
   * - 1231
     - kC/m²
     - Kilocoulombs per square meter
   * - 1232
     - mC/m²
     - Millicoulombs per square meter
   * - 1233
     - μC/m²
     - Microcoulombs per square meter
   * - 1234
     - V/m
     - Volts per meter
   * - 1235
     - MV/m
     - Megavolts per meter
   * - 1236
     - kV/m
     - Kilovolts per meter
   * - 1237
     - V/cm
     - Volts per centimeter
   * - 1238
     - mV/m
     - Millivolts per meter
   * - 1239
     - μV/m
     - Microvolts per meter
   * - 1240
     - V
     - Volt
   * - 1241
     - MV
     - Megavolt
   * - 1242
     - kV
     - Kilovolt
   * - 1243
     - mV
     - Millivolt
   * - 1244
     - μV
     - Microvolt
   * - 1245
     - F
     - Farad
   * - 1246
     - mF
     - Millifarad
   * - 1247
     - μF
     - Microfarad
   * - 1248
     - nF
     - Nanofarad
   * - 1249
     - pF
     - Picofarad
   * - 1250
     - F/m
     - Farad per meter
   * - 1251
     - μF/m
     - Microfarad per meter
   * - 1252
     - nF/m
     - Nanofarad per meter
   * - 1253
     - pF/m
     - Picofarad per meter
   * - 1254
     - C·m
     - Coulomb meter
   * - 1255
     - A/m²
     - Amperes per square meter
   * - 1256
     - MA/m²
     - Megaamperes per square meter
   * - 1257
     - A/cm²
     - Amperes per square centimeter
   * - 1258
     - kA/m²
     - Kiloamperes per square meter
   * - 1259
     - A/m
     - Amperes per meter
   * - 1260
     - kA/m
     - Kiloamperes per meter
   * - 1261
     - A/cm
     - Amperes per centimeter
   * - 1262
     - T
     - Tesla
   * - 1263
     - mT
     - Millitesla
   * - 1264
     - μT
     - Microtesla
   * - 1265
     - nT
     - Nanotesla
   * - 1266
     - Wb
     - Weber
   * - 1267
     - mWb
     - Milliweber
   * - 1268
     - Wb/m
     - Webers per meter
   * - 1269
     - kWb/m
     - Kilowebers per meter
   * - 1270
     - H
     - Henry
   * - 1271
     - mH
     - Millihenry
   * - 1272
     - μH
     - Microhenry
   * - 1273
     - nH
     - Nanohenry
   * - 1274
     - pH
     - Picohenry
   * - 1275
     - H/m
     - Henries per meter
   * - 1276
     - μH/m
     - Microhenries per meter
   * - 1277
     - nH/m
     - Nanohenries per meter
   * - 1278
     - A·m²
     - Ampere square meters
   * - 1279
     - N·m²/A
     - Newton meter squared per ampere
   * - 1280
     - Wb·m
     - Weber meter
   * - 1281
     - Ω
     - Ohm1
   * - 1282
     - GΩ
     - Gigaohm1
   * - 1283
     - MΩ
     - Megaohm1
   * - 1284
     - kΩ
     - Kiloohm1
   * - 1285
     - mΩ
     - Milliohm1
   * - 1286
     - μΩ
     - Microohm1
   * - 1287
     - S
     - Siemens
   * - 1288
     - kS
     - Kilosiemens
   * - 1289
     - mS
     - Millisiemens
   * - 1290
     - μS
     - Microsiemens
   * - 1291
     - Ω·m
     - Ohms times meters1
   * - 1292
     - GΩ·m
     - Gigaohms times meters1
   * - 1293
     - MΩ·m
     - Megaohms times meters1
   * - 1294
     - kΩ·m
     - Kiloohms times meters1
   * - 1295
     - Ω·cm
     - Ohms times centimeters1
   * - 1296
     - mΩ·m
     - Milliohms times meters1
   * - 1297
     - μΩ·m
     - Microohms times meters1
   * - 1298
     - nΩ·m
     - Nanoohms times meters1
   * - 1299
     - S/m
     - Siemens per meter
   * - 1300
     - MS/m
     - Megasiemens per meter
   * - 1301
     - kS/m
     - Kilosiemens per meter
   * - 1302
     - mS/cm
     - Millisiemens per centimeter
   * - 1303
     - μS/mm
     - Microsiemens per millimeter
   * - 1304
     - 1/H
     - Per henry
   * - 1305
     - sr
     - Steradian
   * - 1306
     - W/sr
     - Watts per steradian
   * - 1307
     - W/(sr·m²)
     - Watts per (steradian square meter)
   * - 1308
     - W/(m²)
     - Watts per square meter
   * - 1309
     - lm
     - Lumen
   * - 1310
     - lm·s
     - Lumen second
   * - 1311
     - lm·h
     - Lumen hour
   * - 1312
     - lm/m²
     - Lumens per square meter
   * - 1313
     - lm/W
     - Lumens per watt
   * - 1314
     - lx
     - Lux
   * - 1315
     - lx·s
     - Lux second
   * - 1316
     - cd
     - Candela
   * - 1317
     - cd/m²
     - Candela per square meter
   * - 1318
     - g/s
     - Grams per second
   * - 1319
     - g/min
     - Grams per minute
   * - 1320
     - g/h
     - Grams per hour
   * - 1321
     - g/d
     - Grams per day
   * - 1322
     - kg/s
     - Kilograms per second
   * - 1323
     - kg/min
     - Kilograms per minute
   * - 1324
     - kg/h
     - Kilograms per hour
   * - 1325
     - kg/d
     - Kilograms per day
   * - 1326
     - t/s
     - Metric tons per second
   * - 1327
     - t/min
     - Metric tons per minute
   * - 1328
     - t/h
     - Metric tons per hour
   * - 1329
     - t/d
     - Metric tons per day
   * - 1330
     - lb/s
     - Pounds per second
   * - 1331
     - lb/min
     - Pounds per minute
   * - 1332
     - lb/h
     - Pounds per hour
   * - 1333
     - lb/d
     - Pounds per day
   * - 1334
     - STon/s
     - US tons per second
   * - 1335
     - STon/min
     - US tons per minute
   * - 1336
     - STon/h
     - US tons per hour
   * - 1337
     - STon/d
     - US tons per day
   * - 1338
     - LTon/s
     - British tons per second
   * - 1339
     - LTon/min
     - British tons per minute
   * - 1340
     - LTon/h
     - British tons per hour
   * - 1341
     - LTon/d
     - British tons per day
   * - 1342
     - %
     - Percent
   * - 1343
     - % sol/wt
     - Percentage solids per weight unit
   * - 1344
     - % sol/vol
     - Percentage solids per volume unit
   * - 1345
     - % stm qual
     - Percentage steam quality
   * - 1346
     - °Plato
     - Degree plato
   * - 1347
     - m³/s
     - Cubic meters per second
   * - 1348
     - m³/min
     - Cubic meters per minute
   * - 1349
     - m³/h
     - Cubic meters per hour
   * - 1350
     - m³/d
     - Cubic meters per day
   * - 1351
     - L/s
     - Liters per second
   * - 1352
     - L/min
     - Liters per minute
   * - 1353
     - L/h
     - Liters per hour
   * - 1354
     - L/d
     - Liters per day
   * - 1355
     - ML/d
     - Megaliters per day
   * - 1356
     - ft³/s
     - Cubic feet per second
   * - 1357
     - ft³/m
     - Cubic feet per minute
   * - 1358
     - ft³/h
     - Cubic feet per hour
   * - 1359
     - ft³/d
     - Cubic feet per day
   * - 1360
     - ft³/min std
     - Standard cubic feet per minute
   * - 1361
     - ft³/h std
     - Standard cubic feet per hour
   * - 1362
     - gal/s
     - US gallons per second
   * - 1363
     - gal/min
     - US gallons per minute
   * - 1364
     - gal/h
     - US gallons per hour
   * - 1365
     - gal/d
     - US gallons per day
   * - 1366
     - Mgal/d
     - Mega US gallons per day
   * - 1367
     - ImpGal/s
     - Imperial gallons per second
   * - 1368
     - ImpGal/min
     - Imperial gallons per minute
   * - 1369
     - ImpGal/h
     - Imperial gallons per hour
   * - 1370
     - ImpGal/d
     - Imperial gallons per day
   * - 1371
     - bbl/s
     - Barrels per second
   * - 1372
     - bbl/min
     - Barrels per minute
   * - 1373
     - bbl/h
     - Barrels per hour
   * - 1374
     - bbl/d
     - Barrels per day
   * - 1375
     - W/m²
     - Watts per square meter
   * - 1376
     - mW/m²
     - Milliwatts per square meter
   * - 1377
     - μW/m²
     - Microwatts per square meter
   * - 1378
     - pW/m²
     - Picowatts per square meter
   * - 1379
     - Pa·s/m³
     - Pascal seconds per cubic meter
   * - 1380
     - N·s/m
     - Newton seconds per meter
   * - 1381
     - Pa·s/m
     - Pascal seconds per meter
   * - 1382
     - B
     - Bel
   * - 1383
     - dB
     - Decibel
   * - 1384
     - mol
     - Mol
   * - 1385
     - kmol
     - Kilomole
   * - 1386
     - mmol
     - Millimole
   * - 1387
     - μmol
     - Micromole
   * - 1388
     - kg/mol
     - Kilograms per mole
   * - 1389
     - g/mol
     - Grams per mole
   * - 1390
     - m³/mol
     - Cubic meters per mole
   * - 1391
     - dm³/mol
     - Cubic decimeters per mole
   * - 1392
     - cm³/mol
     - Cubic centimeters per mole
   * - 1393
     - L/mol
     - Liters per mole
   * - 1394
     - J/mol
     - Joules per mole
   * - 1395
     - kJ/mol
     - Kilojoules per mole
   * - 1396
     - J/(mol·K)
     - Joules per mole kelvin
   * - 1397
     - mol/m³
     - Moles per cubic meter
   * - 1398
     - mol/dm³
     - Moles per cubic decimeter
   * - 1399
     - mol/L
     - Moles per liter
   * - 1400
     - mol/kg
     - Moles per kilogram
   * - 1401
     - mmol/kg
     - Millimoles per kilogram
   * - 1402
     - Bq
     - Becquerel
   * - 1403
     - MBq
     - Megabecquerel
   * - 1404
     - kBq
     - Kilobecquerel
   * - 1405
     - Bq/kg
     - Becquerels per kilogram
   * - 1406
     - kBq/kg
     - Kilobecquerels per kilogram
   * - 1407
     - MBq/kg
     - Megabecquerels per kilogram
   * - 1408
     - Gy
     - Gray
   * - 1409
     - mGy
     - Milligray
   * - 1410
     - rd
     - Rad
   * - 1411
     - Sv
     - Sievert
   * - 1412
     - mSv
     - Millisievert
   * - 1413
     - rem
     - Rem
   * - 1414
     - C/kg
     - Coulombs per kilogram
   * - 1415
     - mC/kg
     - Millicoulombs per kilogram
   * - 1416
     - R
     - Röntgen
   * - 1417
     - 1/Jm³
     - Density of magnetic energy
   * - 1418
     - e/Vm³
     -
   * - 1419
     - m³/C
     - Cubic meters per coulomb
   * - 1420
     - V/K
     - Volts per kelvin
   * - 1421
     - mV/K
     - Millivolts per kelvin
   * - 1422
     - pH
     - pH value
   * - 1423
     - ppm
     - Parts per million
   * - 1424
     - ppb
     - Parts per billion
   * - 1425
     - ppth
     - Parts per trillion
   * - 1426
     - °Brix
     - Degrees Brix
   * - 1427
     - °Ball
     - Degrees Balling
   * - 1428
     - proof/vol
     - Proof per volume
   * - 1429
     - proof/mass
     - Proof per mass
   * - 1430
     - lb/ImpGal
     - Pounds per Imperial gallon
   * - 1431
     - kcal :sub:`th`/s
     - Kilocalories per second1
   * - 1432
     - kcal :sub:`th`/min
     - Kilocalories per minute1
   * - 1433
     - kcal :sub:`th`/h
     - Kilocalories per hour1
   * - 1434
     - kcal :sub:`th`/d
     - Kilocalories per day1
   * - 1435
     - Mcal :sub:`th`/s
     - Megacalories per second1
   * - 1436
     - Mcal :sub:`th`/min
     - Megacalories per minute1
   * - 1437
     - Mcal :sub:`th`/d
     - Megacalories per day1
   * - 1438
     - kJ/s
     - Kilojoules per second
   * - 1439
     - kJ/min
     - Kilojoules per minute
   * - 1440
     - kJ/h
     - Kilojoule per hour
   * - 1441
     - kJ/d
     - Kilojoules per day
   * - 1442
     - MJ/s
     - Megajoules per second
   * - 1443
     - MJ/min
     - Megajoules per minute
   * - 1444
     - MJ/d
     - Megajoules per day
   * - 1445
     - Btu :sub:`th`/s
     - British thermal units per second1
   * - 1446
     - Btu :sub:`th`/min
     - British thermal units per minute1
   * - 1447
     - Btu :sub:`th`/d
     - British thermal units per day1
   * - 1448
     - μgal/s
     - Micro US gallons per second
   * - 1449
     - mgal/s
     - Milli US gallons per second
   * - 1450
     - kgal/s
     - Kilo US gallons per second
   * - 1451
     - Mgal/s
     - Mega US gallons per second
   * - 1452
     - μgal/min
     - Micro US gallons per minute
   * - 1453
     - mgal/min
     - Milli US gallons per minute
   * - 1454
     - kgal/min
     - Kilo US gallons per minute
   * - 1455
     - Mgal/min
     - Mega US gallons per minute
   * - 1456
     - μgal/h
     - Micro US gallons per hour
   * - 1457
     - mgal/h
     - Milli US gallons per hour
   * - 1458
     - kgal/h
     - Kilo US gallons per hour
   * - 1459
     - Mgal/h
     - Mega US gallons per hour
   * - 1460
     - μgal/d
     - Micro US gallons per day
   * - 1461
     - mgal/d
     - Milli US gallons per day
   * - 1462
     - kgal/d
     - Kilo US gallons per day
   * - 1463
     - μImpGal/s
     - Micro Imperial gallons per second
   * - 1464
     - mImpGal/s
     - Milli Imperial gallons per second
   * - 1465
     - kImpGal/s
     - Kilo Imperial gallons per second
   * - 1466
     - MImpGal/s
     - Mega Imperial gallons per second
   * - 1467
     - μImpGal/min
     - Micro Imperial gallons per minute
   * - 1468
     - mImpGal/min
     - Milli Imperial gallons per minute
   * - 1469
     - kImpGal/min
     - Kilo Imperial gallons per minute
   * - 1470
     - MImpGal/min
     - Mega Imperial gallons per minute
   * - 1471
     - μImpGal/h
     - Micro Imperial gallons per hour
   * - 1472
     - mImpGal/h
     - Milli Imperial gallons per hour
   * - 1473
     - kImpGal/h
     - Kilo Imperial gallons per hour
   * - 1474
     - MImpGal/h
     - Mega Imperial gallons per hour
   * - 1475
     - μImpgal/d
     - Micro Imperial gallons per day
   * - 1476
     - mImpgal/d
     - Milli Imperial gallons per day
   * - 1477
     - kImpgal/d
     - Kilo Imperial gallons per day
   * - 1478
     - MImpgal/d
     - Mega Imperial gallons per day
   * - 1479
     - μbbl/s
     - Microbarrels per second
   * - 1480
     - mbbl/s
     - Millibarrels per second
   * - 1481
     - kbbl/s
     - Kilobarrels per second
   * - 1482
     - Mbbl/s
     - Megabarrels per second
   * - 1483
     - μbbl/min
     - Microbarrels per minute
   * - 1484
     - mbbl/min
     - Millibarrels per minute
   * - 1485
     - kbbl/min
     - Kilobarrels per minute
   * - 1486
     - Mbbl/min
     - Megabarrels per minute
   * - 1487
     - μbbl/h
     - Microbarrels per hour
   * - 1488
     - mbbl/h
     - Millibarrels per hour
   * - 1489
     - kbbl/h
     - Kilobarrels per hour
   * - 1490
     - Mbbl/h
     - Megabarrels per hour
   * - 1491
     - μbbl/d
     - Microbarrels per day
   * - 1492
     - mbbl/d
     - Millibarrels per day
   * - 1493
     - kbbl/d
     - Kilobarrels per day
   * - 1494
     - Mbbl/d
     - Megabarrels per day
   * - 1495
     - μm³/s
     - Cubic micrometers per second
   * - 1496
     - mm³/s
     - Cubic millimeters per second
   * - 1497
     - km³/s
     - Cubic kilometers per second
   * - 1498
     - Mm³/s
     - Cubic megameters per second
   * - 1499
     - μm³/min
     - Cubic micrometers per minute
   * - 1500
     - mm³/min
     - Cubic millimeters per minute
   * - 1501
     - km³/min
     - Cubic kilometers per minute
   * - 1502
     - mm³/min
     - Cubic megameters per minute
   * - 1503
     - µm³/h
     - Cubic micrometers per minute
   * - 1504
     - mm³/h
     - Cubic millimeters per minute
   * - 1505
     - km³/h
     - Cubic kilometers per minute
   * - 1506
     - Mm³/h
     - Cubic megameters per minute
   * - 1507
     - µm³/d
     - Cubic micrometers per day
   * - 1508
     - mm³/d
     - Cubic millimeters per day
   * - 1509
     - km³/d
     - Cubic kilometers per day
   * - 1510
     - Mm³/d
     - Cubic megameters per day
   * - 1511
     - cm³/s
     - Cubic centimeters per second
   * - 1512
     - cm³/min
     - Cubic centimeters per minute
   * - 1513
     - cm³/h
     - Cubic centimeters per hour
   * - 1514
     - cm³/d
     - Cubic centimeters per day
   * - 1515
     - kcal :sub:`th`/kg
     - Kilocalories per kilogram1
   * - 1516
     - Btu :sub:`th`/lb
     - British thermal units per pound1
   * - 1517
     - kL
     - Kiloliter
   * - 1518
     - kL/min
     - Kiloliters per minute
   * - 1519
     - kL/h
     - Kiloliters per hour
   * - 1520
     - kL/d
     - Kiloliters per day
   * - 1551
     - S/cm
     - Siemens per centimeter
   * - 1552
     - µS/cm
     - Microsiemens per centimeter
   * - 1553
     - mS/m
     - Millisiemens per meter
   * - 1554
     - µS/m
     - Microsiemens per meter
   * - 1555
     - MΩ · cm
     - Megaohm centimeter1
   * - 1556
     - kΩ · cm
     - Kiloohm centimeter1
   * - 1557
     - Weight%
     - Weight percent
   * - 1558
     - mg/L
     - Milligram per liter
   * - 1559
     - µg/L
     - Microgram per liter
   * - 1560
     - %Sat
     - -
   * - 1561
     - vpm
     - -
   * - 1562
     - %vol
     - Volume percent
   * - 1563
     - ml/min
     - Milliliters per minute
   * - 1564
     - mg/dm³
     - Milligrams per cubic centimeter
   * - 1565
     - mg/L
     - Milligram per liter
   * - 1566
     - mg/m³
     - Milligrams per cubic meter
   * - 1567
     - ct
     - Carat (jewels) = 200.0·10-6 kg
   * - 1568
     - lb (tr)
     - Pound (troy or apothecary) = 0.3732417216 kg
   * - 1569
     - oz (tr)
     - Ounce (troy or apothecary) = 1/12 lb (tr)
   * - 1570
     - fl oz (U.S.)
     - Ounce (U.S. fluid) = (1/128) gal
   * - 1571
     - cm³
     - Cubic centimeter = 10-6 m3
   * - 1572
     - af
     - acre foot = 43560 ft³
   * - 1573
     - m³ normal
     - Cubic meter
   * - 1574
     - L normal
     - Liter
   * - 1575
     - m³ std.
     - Standard cubic meter
   * - 1576
     - L std.
     - Standard liter
   * - 1577
     - ml/s
     - Milliliters per second
   * - 1578
     - ml/h
     - Milliliters per hour
   * - 1579
     - ml/d
     - Milliliters per day
   * - 1580
     - af/s
     - Acre foot per second
   * - 1581
     - af/min
     - Acre foot per minute
   * - 1582
     - af/h
     - Acre foot per hour
   * - 1583
     - af/d
     - Acre foot per day
   * - 1584
     - fl oz (U.S.)/s
     - Ounces per second
   * - 1585
     - fl oz (U.S.) /min
     - Ounces per minute
   * - 1586
     - fl oz (U.S.)/h
     - Ounces per hour
   * - 1587
     - fl oz (U.S.)/d
     - Ounces per day
   * - 1588
     - m³/s normal
     - Standard cubic meters per second
   * - 1589
     - m³/min normal
     - Standard cubic meters per minute
   * - 1590
     - m³/h normal
     - Standard cubic meters per hour
   * - 1591
     - m³/d normal
     - Standard cubic meters per day
   * - 1592
     - L/s normal
     - Standard liters per second
   * - 1593
     - L/min normal
     - Standard liters per minute
   * - 1594
     - L/h normal
     - Standard liters per hour
   * - 1595
     - L/d normal
     - Standard liters per second
   * - 1596
     - m³/s std.
     - Standard cubic meters per second
   * - 1597
     - m³/min std.
     - Standard cubic meters per minute
   * - 1598
     - m³/h std.
     - Standard cubic meters per hour
   * - 1599
     - m³/d std.
     - Standard cubic meters per day
   * - 1600
     - L/s std.
     - Standard liters per second
   * - 1601
     - L/min std.
     - Standard liters per minute
   * - 1602
     - L/h std.
     - Standard liters per hour
   * - 1603
     - L/d std.
     - Standard liters per day
   * - 1604
     - ft³/s std.
     - Standard cubic feet per second
   * - 1605
     - ft³/d std.
     - Standard cubic feet per day
   * - 1606
     - oz/s
     - Ounces per second
   * - 1607
     - oz/min
     - Ounces per minute
   * - 1608
     - oz/h
     - Ounces per hour
   * - 1609
     - oz/d
     - Ounces per day
   * - 1610
     - Paa
     - Pascal (absolute)
   * - 1611
     - Pag
     - Pascal (gauge)
   * - 1612
     - GPaa
     - Gigapasacal (absolute)
   * - 1613
     - GPag
     - Gigapascal (gauge)
   * - 1614
     - MPaa
     - Megapascal (absolute)
   * - 1615
     - MPag
     - Megapascal (gauge)
   * - 1616
     - kPaa
     - Kilopascal (absolute)
   * - 1617
     - kPag
     - Kilopascal (gauge)
   * - 1618
     - mPaa
     - Millipascal (absolute)
   * - 1619
     - mPag
     - Millipascal (gauge)
   * - 1620
     - μPaa
     - Micropascal (absolute)
   * - 1621
     - μPag
     - Micropascal (gauge)
   * - 1622
     - hPaa
     - Hectopascal (absolute)
   * - 1623
     - hPag
     - Hectopascal (gauge)
   * - 1624
     - gf/cm²a
     -
   * - 1625
     - gf/cm²g
     -
   * - 1626
     - kgf/cm²a
     -
   * - 1627
     - kgf/cm²g
     -
   * - 1628
     - SD4°C
     - Standard density at 4°C
   * - 1629
     - SD15°C
     - Standard density at 15°C
   * - 1630
     - SD20°C
     - Standard density at 20°C
   * - 1631
     - PS
     - Metric horsepower
   * - 1632
     - ppt
     - Parts per trillion = 1012
   * - 1633
     - hl/s
     - Hectoliters per second
   * - 1634
     - hl/min
     - Hectoliters per minute
   * - 1635
     - hl/h
     - Hectoliters per hour
   * - 1636
     - hl/d
     - Hectoliters per day
   * - 1637
     - bbl (liq)/s
     - Barrels (US liquid) per second
   * - 1638
     - bbl (liq)/min
     - Barrels (US liquid) per minute
   * - 1639
     - bbl (liq)/h
     - Barrels (US liquid) per hour
   * - 1640
     - bbl (liq)/d
     - Barrels (US liquid) per day
   * - 1641
     - bbl (fed)
     - Barrel (U.S. federal) = 31 gallons
   * - 1642
     - bbl (fed)/s
     - Barrels (US federal) per second
   * - 1643
     - bbl (fed)/min
     - Barrels (US federal) per minute
   * - 1644
     - bbl (fed)/h
     - Barrels (US federal) per hour
   * - 1645
     - bbl (fed)/d
     - Barrels (US federal) per day
   * - 1998
     - Unknown unit
     - To be used when the unit of measure is not known during configuration
   * - 1999
     - Special
     - Special units

