let url="https://api.openweathermap.org/data/2.5/weather?&units=metric&q=";
let key="fe44ecb5ac50c51fbb62bc8ef09a6cfb";
let btn=document.querySelector("#search-icon");

let box=document.querySelector(".box");
let cityEle=document.querySelector("#city");
let temp=document.querySelector("#deg");
let humidity=document.querySelector(".humidvalue");
let wind=document.querySelector(".windvalue")
let inp=document.querySelector("#search");
let tempImg=document.querySelector("temp-img");

async function weather(city){
    let res=await axios.get(url+city+`&appid=${key}`);
    // if(Response.status==404){
    //     document.querySelector(".error").style.display="block";
    //    document.querySelector("main-box").style.display="none";
    //     box.style.display="none";
    // }
    
    let data=res.data
    console.log(data);
    cityEle.innerText=data.name;
    console.log(city);
    deg.innerText=Math.round(data.main.temp)+`°c`;
    humidity.innerText=data.main.humidity+`%`;
    wind.innerText=data.wind.speed+`km\h`
    console.log(deg);
    console.log(humidity);
    console.log(wind);
}
btn.addEventListener("click",()=>{
    let cityvalue=inp.value;
    inp.value="";
    console.log("clicked me")
    weather(cityvalue);
    document.querySelector(".main-box").style.display="block";
    box.style.height="500px";

})

