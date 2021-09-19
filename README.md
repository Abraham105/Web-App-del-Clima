# Web del el clima API "openweathermap"

## Introduction

> Esta es una app sencilla que mediante una busqueda que puedes hacer tu mismo te dara el clima en tu ciudad "que esperas Probala" 

>This is a simple app that through a search that you can do yourself will give you the weather in your city "what are you waiting for? Try it"

## Code Samples

> Aqui esta la parte mas importante del codigo 

```  js
 async function search(query) {
  try {
    const response = await fetch(`${api.url}?q=${query}&appid=${api.key}&lang=es`);
    const data = await response.json();
    // const icon = `https://s3-us-west-2.amazonaws.com/s.cdpn.io/162656/${
    //     weather[0]["icon"]
    //   }.svg`;
    card.style.display = 'block';
    city.innerHTML = `${data.name}, ${data.sys.country}`;
    data.innerHTML = (new Date()).toLocaleDateString();
    temp.innerHTML = `${toCelsius(data.main.temp)}c`;
    weather.innerHTML = data.weather[0].description;
    range.innerHTML = `${toCelsius(data.main.temp_min)}c / ${toCelsius(data.main.temp_max)}c`;
    updateImages(data);
  } catch (err) {
    console.log(err);
     swal({
      title: "Ho noo!!",
      text: "No encontramos tu ciudad!!",
      icon: "error",
      button: "Volver a intertar",
    });
  }
}
 }
```
# Espero que te guste 



<h3 align="center">Languages used in this project</h3>
<p align="center"> <a href="https://www.w3schools.com/css/" target="_blank"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" alt="css3" width="40" height="40"/> </a> <a href="https://www.w3.org/html/" target="_blank"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" alt="html5" width="40" height="40"/> </a> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="javascript" width="40" height="40"/> </a> </p>




<h3 align="center">Contact</h3>
<p align="center">
<a href="https://linkedin.com/in/abrahan-rivero-b2a1191ba" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="abrahan rivero" height="30" width="40" /></a>
</p>

