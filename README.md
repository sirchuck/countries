# countries
Javascript and PHP country with states array


There will be mistakes!

Places like scottland use GB for the iso 2 code, which conflicts with wales and the United Kingdom so all the regions/states are listed under United Kingdom. 

Only USA has state 2 didget codes so far.

Country and State names may have spelling errors. 

If you want to help pick a country you live in and correct it. 


Layout:

 ["CountryName","ISO-2 CODE","ISO 3 CODE","UN CODE",[
    ["ISO 2 State Code","State/Region"]
  ]],

Example:
["United States of America","US","USA","840",[
   ["AL","Alabama"]
]],


POSSIBLIE USAGES: (Javascript)

// Get select options for a pulldown for all the countries
function countrySelect(){
  var o = '';
  for(var i=0;i<cs.length;i++){ o += '<option value="' + cs[i][1] + '">' + cs[i][0] + '</option>'; }
  return o;
}
// Get pulldown list for a countries states/regions Pass: ( Country )
function stateSelect(s){
  var o = '';
  for(var i=0;i<cs.length;i++){ 
    if(s == cs[i][1]){
      for(var ii=0;ii<cs[i][4].length;ii++){ o += '<option value="' + cs[i][4][ii][1] + '">' + cs[i][4][ii][1] + '</option>'; }
      return o;
    } 
  }
}
// Verify the selected state/region exists for a perticular country. Pass: ( Country, State )
function verifyState(s,ss){
  for(var i=0;i<cs.length;i++){ 
    if(s == cs[i][1]){
      for(var ii=0;ii<cs[i][4].length;ii++){ if(cs[i][4][ii][1]==ss){return true;} }
    } 
  }
  return false;
}




Converting from a javascript array to your language or database with a script shouldn't be that difficult as this is just a basic array.

Enjoy.
