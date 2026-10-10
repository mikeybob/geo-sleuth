# United Kingdom clues

Entries use the shared format (`references/clues/README.md`). Cross-country clues that lead here (driving on the left, yellow rear / white front plates, mph speed signs) are in `references/clues/global.md`. Lookups: `clues.py lookup plate|postal-code --country gb`.

## Text and plates

### Current Great Britain number plates (2001+)
- Look for: a long European plate, black on white at the front and black on yellow at the rear; format two letters, two digits, three letters (`AB12 CDE`). Optional blue strip with `UK` and a Union Jack, older `GB`, or a blank plate with no strip. Look up the first two letters with `clues.py lookup plate <mark> --country gb`
- Points to: the DVLA local memory tag — a nation (C… = Wales, S… = Scotland) plus the issuing office city (see the table). That is where the vehicle was registered, not always where the photo is
- Strength: medium on a street with several agreeing plates; weak for a single car, a car park, a tourist spot or a motorway service area
- Counterexamples: cherished / personalised marks use arbitrary two-letter prefixes (including J, T, U, which are not area codes); personal-export plates start with X and do not mean a place; reserved letter pairs are issued as select marks and are absent from the table on purpose; Northern Ireland uses a different format (below); Irish Republic plates also have a yellow rear but a `YY-CC-NNNNN` layout; vehicles travel
- Sources: https://www.gov.uk/displaying-number-plates ; https://en.wikipedia.org/wiki/Vehicle_registration_plates_of_the_United_Kingdom

### Northern Ireland plates
- Look for: the same yellow/white colours, but a three-letter + up to four-digit mark (`ABC 1234`) rather than `AB12 CDE`; no 2001-style age digits in the middle
- Points to: Northern Ireland (the whole country), not a GB memory tag. Do not force it through the GB plate table
- Strength: medium (format to the nation)
- Counterexamples: some cherished GB marks also look irregular; older GB prefix/suffix plates can be three letters and a number; a car from NI is common in Great Britain and the Republic of Ireland
- Sources: https://en.wikipedia.org/wiki/Vehicle_registration_plates_of_Northern_Ireland

### Postcodes on shops, vans and planning notices
- Look for: a UK postcode (`SW1A 1AA`, `M1 1AE`, `CF10 1EP`) on a fascia, letterhead, van livery or site board. Look up the area letters with `clues.py lookup postal-code <code> --country gb`
- Points to: the postcode area / named post town. London lettered areas (E, EC, N, NW, SE, SW, W, WC) are the London postal district, not “south-west England”
- Strength: strong when the code is on a fixed premises in the photo; medium on a van (the depot may be elsewhere)
- Counterexamples: the named town is only the head post town — the area is larger and often crosses council and even national borders (CH, SY, TD, HR); GY / JE / IM are Crown dependencies, not the UK; non-geographic codes (BF, BX, GIR) do not locate a street
- Sources: https://en.wikipedia.org/wiki/List_of_postcode_areas_in_the_United_Kingdom

### Council, highway authority and “issued by” lines
- Look for: the council or National Highways / Transport Scotland / Welsh Government name in small print on traffic signs, roadworks boards, lamp columns, wheelie bins and planning notices (`… City Council`, `… County Council`, `London Borough of …`)
- Points to: the local authority, often district or borough
- Strength: medium when the name is a district council; a county or national-agency name is only the wider area
- Counterexamples: contractors and utility companies print their own names; a county council sign can stand inside a unitary city; London borough names are not the same as postcode areas
- Sources: general (same method as other packs: the issuing authority on the sign)

### Welsh / English bilingual official signs
- Look for: the same place or instruction in Welsh and English on a statutory sign, street-name plate or road number (Welsh often above English in Wales)
- Points to: Wales. Combine with a C… plate or a CF / LL / SA / NP / LD postcode to pick the area
- Strength: strong for the nation (official bilingual signing)
- Counterexamples: tourist labels and shop names do not count; a few English-border roads and railways show Welsh; Welsh-language signs also appear at Eisteddfod sites and Welsh institutions in England
- Sources: https://www.gov.wales/welsh-language-standards

### Scottish Gaelic bilingual official signs
- Look for: Gaelic and English on a statutory road or rail sign (Gaelic usually above)
- Points to: the Highlands and the Western Isles, not “anywhere in Scotland”. Lowland Scotland is English-only on most roads
- Strength: medium (to that part of Scotland)
- Counterexamples: railway station names and visitor-centre signs exist outside the core area; Irish-language signs are the Republic of Ireland or a few NI settings, not Gaelic
- Sources: https://www.transport.gov.scot/publication/road-traffic-signs/

## Vehicles and traffic

### M, A and B road numbers
- Look for: motorway `M` numbers (blue shield), primary-route `A` numbers (green), other `A` / `B` numbers (white). A London-style circular “A40” or “North Circular” is still an A-road
- Points to: one numbered corridor. Look the route up with `osm.py route` and treat it as a line, then use a second constraint for the camera
- Strength: strong to the corridor when the number is read; the same A-number is hundreds of kilometres long
- Counterexamples: Ireland uses N / R / M with kilometre posts and a different shield; A-roads are reused as local names on signs far from the carriageway; “M25” on a lorry is not proof you can see the M25
- Sources: https://www.gov.uk/guidance/the-highway-code/road-markings

### TfL red buses and roundel
- Look for: a red double-decker or single-decker with a Transport for London roundel and a route number, or a bus stop with the same roundel
- Points to: Greater London (TfL contracted services). Read the route number and check it with `osm.py route` / a current map
- Strength: medium (to Greater London) when the roundel is readable; with a route number, to that corridor
- Counterexamples: many UK towns run red buses; heritage Routemasters and tourist buses appear outside London; TfL Overground / Elizabeth line roundels also sit in the wider TfL area, not only Zone 1
- Sources: https://tfl.gov.uk/

### Double yellow lines and zigzag crossings
- Look for: double yellow lines along the kerb (no waiting at any time); zig-zag markings on the approach to a zebra or signal crossing; a Belisha beacon (flashing amber globe) at a zebra
- Points to: a public road in the UK (or a Crown dependency / Ireland, which share parts of this vocabulary). Use it to confirm you are in this road system, then read plates and postcodes
- Strength: weak for the country alone; useful as a UK/Ireland vs continental check together with mph and yellow plates
- Counterexamples: some other countries paint yellow kerb restrictions; decorative “Belisha” lamps exist in exports and theme parks; private estates may omit the markings
- Sources: https://www.gov.uk/guidance/the-highway-code/road-markings

## Infrastructure

### Royal Mail pillar boxes
- Look for: a red cylindrical or hexagonal pillar box, or a red wall box, with a royal cypher (VR, GR, ER, CR) and a collection plate. Scottish boxes for the late Queen often used a Scottish crown rather than “E II R”
- Points to: the UK or a Crown dependency (the same red boxes were also installed in some former territories). The cypher dates the box; it does not locate the street
- Strength: weak (country-level, many lookalikes)
- Counterexamples: replica and decorative boxes worldwide; Ireland painted many boxes green after independence — a green pillar box with a British cypher is the Republic, not the UK; private “post box red” street furniture is not a Royal Mail box
- Sources: https://www.royalmail.com/

### Green roadside cabinets marked Openreach
- Look for: a green metal cabinet on the pavement or verge with an Openreach (or older BT) label and a cabinet number
- Points to: a UK (or Crown-dependency) street with Openreach plant. The cabinet number can be searched and sometimes yields a street, but treat a web hit as a hypothesis
- Strength: weak for the country; medium only after a cabinet-number search is confirmed against the scene
- Counterexamples: similar green cabinets in the Republic of Ireland (Eir) and other countries; cabinet IDs are reused in discussion posts without photos
- Sources: general

## Nations within the UK

### Which nation, before which city
- Look for: the combination of plate prefix (C… Wales, S… Scotland, NI format), bilingual signing, and postcode area admin1 from the lookup tables. England is the residual when those are absent — do not default to London
- Points to: England / Scotland / Wales / Northern Ireland as the first `board.py` split (`board.py children` once the country is set)
- Strength: medium when two of plate, postcode and official language agree
- Counterexamples: GB-format plates on holiday in another nation; CH / SY / TD / HR postcodes cross the English border; a Welsh institution in England
- Sources: this pack’s plate and postal-code tables
