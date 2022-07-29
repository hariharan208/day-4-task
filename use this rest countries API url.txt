


//Use the rest countries API url -> https://restcountries.eu/rest/v2/all and display all the country flags in console


const request = new XMLHttpRequest();

request.open("GET","https://restcountries.com/v2/all");


request.onload = function()
{

    if (request.status>=200 && request.status<300) {
    let str = JSON.parse(this.response);

for(let i = 0 ;i<str.length;i++)

{
console.log(`
Country Name: ${str[i].name}
Flag : ${str[i].flag}
`)
}
    }
};


request.send();