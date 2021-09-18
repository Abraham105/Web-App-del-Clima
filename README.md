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

## You can find me 😁:
[Portfolio](https://www.abrahandev.web.app)
