---
title: "CSS Snippets"
datePublished: Sun May 07 2023 18:44:25 GMT+0000 (Coordinated Universal Time)
cuid: clhdrjhs5000508mdgvlm695l
slug: css-snippets
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/6JVlSdgMacE/upload/841292b2faaf8597f016278371bd03ff.jpeg

---

## Center a div

```xml
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .container {
            font-family: Arial, Helvetica, sans-serif;
            font-size: 24px;
            margin: 25px;
            width: 350px;
            height: 250px;
            outline: dashed 1px black;
        }

        p {
            text-align: center;
        }
    </style>
</head>

<body>
    <div class="container">
        <p>Hello World!</p>
    </div>
</body>

</html>
```

## Center an image

```xml
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .center {
            display: block;
            margin-left: auto;
            margin-right: auto;
            width: 50%;
        }
    </style>
</head>

<body>
    <img src="https://image.shutterstock.com/image-photo/stock-photo-funny-british-shorthair-cat-portrait-looking-shocked-or-surprised-on-orange-background-with-copy-250nw-2097266809.jpg"
        alt="" class="center">
</body>

</html>
```

## Make text Responsive

```xml
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        @media screen and (min-width:601px) {
            h1 {
                font-size: 80px;
            }
        }

        @media screen and (max-width:600px) {
            h1 {
                font-size: 30px;
            }
        }
    </style>
</head>

<body>
    <h1>Hello World</h1>
</body>

</html>
```

## Fade-in animation

```xml
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .fade {
            opacity: 0.5;
        }

        .fade:hover {
            opacity: 1;
        }
    </style>
</head>

<body>
    <h1 class="fade">Hello, World !</h1>
</body>

</html>
```

---

| [https://uiverse.io/buttons](https://uiverse.io/buttons) |
| --- |
| [https://cubic-bezier.com/#.17,.67,.83,.67](https://cubic-bezier.com/#.17,.67,.83,.67) |
| [https://bgjar.com/](https://bgjar.com/) |
| [https://shadows.brumm.af/](https://shadows.brumm.af/) |
| [https://bennettfeely.com/clippy/](https://bennettfeely.com/clippy/) |
| [https://getwaves.io/](https://getwaves.io/) |
| [https://waitanimate.wstone.uk/](https://waitanimate.wstone.uk/) |
| [https://keyframes.app/](https://keyframes.app/) |