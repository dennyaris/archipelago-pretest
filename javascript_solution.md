## Level 1
```
function titleCase(str) {
  return str.toLowerCase().split(' ').map(function(word) {
    return word.charAt(0).toUpperCase() + word.slice(1);
  }).join(' ');
}
```
console.log(typeof titleCase("I'm a little tea pot"));
console.log(titleCase("I'm a little tea pot"));
console.log(titleCase("sHoRt AnD sToUt"));
console.log(titleCase("SHORT AND STOUT"));

---
## Level 2
```
function delay(ms) {
    return new Promise((resolve) => setTimeout(resolve, ms));
}
```
delay(3000).then(() => console.log('runs after 3 seconds'));

---
## Level 2.5
```
function fetchData(url) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (!url) {
        reject("URL is required");
      } else {
        resolve(`Data from ${url}`);
      }
    }, 1000);
  });
}

function processData(data) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (!data) {
        reject("Data is required");
      } else {
        resolve(data.toUpperCase());
      }
    }, 1000);
  });
}

async function main() {
    try {
        const data = await fetchData("https://example.com");
        const processedData = await processData(data);
        console.log("Processed Data:", processedData);
    } catch (error) {
        console.error("Error:", error);
    }
}
main();
```

---
### Level 3
Access this [Chat Room](https://markdownlivepreview.com/).