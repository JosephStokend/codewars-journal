# Kyu 6: [Kata Title Here]
**Date:** 2026-10-27 | **Language:** JavaScript | **Topic:** Battery Bars

## 1. The Problem (Briefly)
Need to filter out strings and return only numbers from a mixed array.

## 2. My Solution
```javascript
function batteryBars(percent) {
  let barra = "#", puntos = ".";
  let cant_barra, cant_puntos=5, mensaje;
  
  if(percent < 20){
    cant_barra = 0;
    cant_puntos-= cant_barra;
  } else if (percent < 40){
    cant_barra = 1;
    cant_puntos-= cant_barra;
  } else if (percent < 60){
    cant_barra = 2;
    cant_puntos-= cant_barra;
  } else if (percent < 80){
    cant_barra = 3;
    cant_puntos-= cant_barra;
  } else if (percent < 100){
    cant_barra = 4;
    cant_puntos-= cant_barra;
  } else {
    cant_barra = 5;
    cant_puntos-= cant_barra;
  }
  
  mensaje = '['+barra.repeat(cant_barra)+puntos.repeat(cant_puntos)+']'; 
  return mensaje;
}
```

## 2. Example of a Best Practice Solution
```javascript
function batteryBars(p) {
  r = Math.floor(p / 20);
  return `[${"#".repeat(r)}${".".repeat(5 - r)}]`;
}
```

## 3. What I Learned from "Best Practices"
The top solution used the `${}` formatting method to simplify the final string.
The top solution used string methods and `Math` class methods.
