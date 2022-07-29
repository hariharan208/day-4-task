//Use the same rest countries and print all countries name, region, sub region and population


const request = new XMLHttpRequest();

request.open("GET","https://restcountries.com/v2/all");


request.onload = function()
{

    if (request.status>=200 && request.status<300) {
    let str = JSON.parse(this.response);

for(let i = 0 ;i<str.length;i++)

{
    console.log(`
    Name: ${str[i].name}
    Region: ${str[i].region}
    Sub Region :${str[i].subregion}
    Population : ${str[i].population}
    `)
}
    }
};


request.send();