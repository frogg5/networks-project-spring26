# Analysis for RTT v. Speed-of-Light

All `google.co.xx` domains resolve to nearby CDN edge servers, not machines in the target city. This compresses measured RTTs into a narrow ~168-208ish ms band regardless of distance. The ratios below reflect HTTP/CDN overhead more than they do for actual routing inefficiency.

## Question 1: Highest Inefficiency Ratio

London has the highest ratio at 3.81x then followed by Frankfurt at 3.46x. But these are the closest cities, so their small theoretical minimums (~53-59ish ms) amplify the CDN overhead into a big ratio. In actuality, both cities are well-connected. London is a terminus for transatlantic cables (TAT14, Apollo, AEconnect 1, Havfrue etc) and Frankfurt hosts DE-CIX which is one of the world's largest internet exchanges.

## Question 2: Closest to Theoretical Minimum

Sydney has the lowest ratio at 1.28x, followed by Singapore at 1.33x. The large theoretical minimums for these distant cities (~151 to 162ish ms) absorb the constant CDN overhead, producing a ratio close to ~1. Both cities benefit from strong internet+cable infrastructure. 

## Question 3: Why Does Africa Route Through Europe?

There’s little submarine cable capacity between North America and West Africa. Major cables for Lagos (SAT-3/WASC, MainOne, ACE, WACS) run from European to the south. These are remnants of colonial-era telecom infrastructure and the economics of cable deployment favoring high-traffic routes. To fix this, the region needs direct US to Africa cables and stronger local peering at African IXPs like IXPN in Lagos. Projects like Google's Equiano cable and Meta's 2Africa are steps in this direction, but the shift away from Europe-centric routing will take time.

