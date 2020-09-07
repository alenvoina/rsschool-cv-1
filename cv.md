# Dmitry Dutin

### Contacts

* **VK:** [dmitrydutin](https://vk.com/dmitrydutin)
* **Telegram:** @Goslem
* **Discord:** Grozzlou#3472
* **LinkedIn:** [dmitrydutin](https://www.linkedin.com/in/dmitrydutin/)
* **Gmail:** [dmitrydutin@gmail.com](mailto:dmitrydutin@gmail.com)
* **Phone:** +375 (25) 912-60-48

### Summary 

I want to become a junior react developer at Epam.

### Skills 

* HTML5 / CSS3
* JavaScript ES2020
* SQL / MYSQL
* Bootstrap
* PHP
* Node.js
* React.js
* Laravel
* Photoshop / Figma

### Experience 

* Сourse and graduation projects at the university
* Took [second place](http://worldskills.by/index.php?id=665) in the qualifying round of the WorldSkills 2020 international competition

### Education 

**Minsk State College of Electronics**
2017 - 2021 Technician-programmer

**Itransition training center**
April 2020 - June 2020 Trainee

### English 

Pre-Intermediate (A2) in accordance with EPAM Training test results

### Code examples

Javascript

```javascript
async function uploadFile(file) {
    if (file.type !== 'image/jpeg') {
        alert('Select image!')
    } else {
        const url = 'https://api.cloudinary.com/v1_1/hajyom5vd/image/upload'
        const formData = new FormData()
        formData.append('file', file)
        formData.append('upload_preset', 'chatitransition')

        const res = await fetch(
            'https://api.cloudinary.com/v1_1/hajyom5vd/image/upload',
            {
                method: 'POST',
                body: formData
            }
        )
        const result = await res.json()

        const userId = sessionStorage.getItem('userId')
        const name = sessionStorage.getItem('name')

        socket.emit('send message', userId, name, result.secure_url)
    }
}
```
