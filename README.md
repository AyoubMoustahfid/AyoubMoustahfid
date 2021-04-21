阿尤布·穆斯塔菲
#7231

BrahiMouissi — 19/02/2021

BrahiMouissi — 23/02/2021
sat
wach khdamti bi $slice fi size dyal array
阿尤布·穆斯塔菲 — 23/02/2021
la
阿尤布·穆斯塔菲 — 23/02/2021
exports.updateGroupMember= (req, res) => {

    let groupMember = req.groupMember;

    groupMember.participant = req.body.participant;


    groupMember.save((err, groupMember) => {

        if(err || groupMember.participant.length <= 3) {
            return res.status(400).json({
                error: "Group Created, but if you add 4 member in group for start game"
            })
        }

        res.json({
            groupMember,
            message: 'Group Member updated '
        })

    })

}
BrahiMouissi — 23/02/2021

阿尤布·穆斯塔菲 — 23/02/2021
what is this
BrahiMouissi — 23/02/2021
vitesse conx
阿尤布·穆斯塔菲 — 23/02/2021
tes vitess
BrahiMouissi — 23/02/2021
hhhhhhhhh
阿尤布·穆斯塔菲 — 23/02/2021
sifat lia method
阿尤布·穆斯塔菲 — 23/02/2021
sifat lia method
BrahiMouissi — 23/02/2021
const GrCode = async (id)=>{
    try {
        const joiInGroup = await GroupMember.findOne({_id:id})
        // console.log( joiInGroup.id_participant.length);

        return joiInGroup.id_participant.length;
    } catch (error) {
        // res.json({
        //     error: "error"
        // })
    }
}
阿尤布·穆斯塔菲 — 15/03/2021
achno 9ale allah ihambak had kamal
rah wadnia msamkine masma3te walo
BrahiMouissi — 15/03/2021
hhhhhhhhhhhhhhhhhh
golih yhdar bazaaf
阿尤布·穆斯塔菲 — 15/03/2021
hhhhhhhhhhhhh
fsbahe achno gale
masma"toch
BrahiMouissi — 15/03/2021
wlh ma3a9lt  hhhhhhhhhhhh
阿尤布·穆斯塔菲 — 15/03/2021
bsife rah hdarto wlate kiwalo
BrahiMouissi — 30/03/2021
film embarquement immediat complet
阿尤布·穆斯塔菲 — 30/03/2021
https://www.youtube.com/watch?v=5H59Py7KApU
YouTube
icanrockyourworld
Je m'appelle Funny Bear - Full French Version - Gummy Bear Song

BrahiMouissi — 30/03/2021
3alam
hhh
https://www.youtube.com/watch?v=IFtwhMK64H8
YouTube
Tesher
Tesher - Jalebi Baby (Official Lyric Video)

https://www.youtube.com/watch?v=ka8Xm5wF94g
YouTube
BAN GA
El Grande Toto Nodawanod feat WEST ft Spleux

hhhhhhhhhh
BrahiMouissi — 01/04/2021
https://preview.keenthemes.com/keen/demo3/index.html#
Keen | Dashboard
Updates and statistics
阿尤布·穆斯塔菲 — 01/04/2021
https://www.youtube.com/watch?v=aT4hBwdoEyw
YouTube
HaryPhamDev
Top 7+ Best Free React.js Admin Dashboard Templates on Github You M...

https://www.youtube.com/watch?v=4WvT2cmuZ5M
YouTube
Code Resource
Responsive Admin Dashboard Panel HTML And CSS

BrahiMouissi — 01/04/2021
l3ezz
阿尤布·穆斯塔菲 — 01/04/2021
https://www.youtube.com/watch?v=NebuhqMGsLc
YouTube
Med Issati
Building  Dashboard  for Crypto Website using Next.js , Tailwind CS...

https://www.youtube.com/watch?v=1r1-bl5oj00
YouTube
HaryPhamDev
Top 8+ Best Free Responsive ReactJS Admin Themes Template Dashboard...

BrahiMouissi — 05/04/2021
https://myaccount.google.com/lesssecureapps?pli=1&rapt=AEjHL4MvtJIYxaTLSle-k4XuueCKyILbQbFpQ3dt4MN_Nq4QOdd-Puy7TSTH3nPYBo4UztnYTHvGCpNtxYWjWiS4WV8ozrvQ9Q
阿尤布·穆斯塔菲 — 05/04/2021
    
      if(error){
          return res.status(400).json({
              error: error.details[0].message
          })
      } 
BrahiMouissi — 05/04/2021
// Auth 
export * from './Login';

// Includes 
export * from './includes/Navbar';
export * from './includes/NavFixed';
Afficher plus
index.js
1 Ko
import React, { Component } from 'react';
import logo from '../img/logo.png';
import {Formik} from 'formik';
import * as Yup from 'yup';

import {
Afficher plus
Login.jsx
7 Ko
阿尤布·穆斯塔菲 — 05/04/2021
{
  "name": "electron-app",
  "version": "1.0.0",
  "description": "My Electron application description",
  "main": "src/index.js",
  "scripts": {
Afficher plus
package.json
1 Ko
阿尤布·穆斯塔菲 — 06/04/2021
Cart.js
import React from 'react'

import { useSelector, useDispatch } from 'react-redux'

import { incProductCount, decProductCount, removeProduct } from './../actions/cartActions'

Afficher plus
message.txt
5 Ko
cartReducer.js
let items = JSON.parse(localStorage.getItem('cart')) || []

let myState = {
    products: items,
    count: items.reduce((total, product) => total + product.count, 0)
}

const cartReducer = (state = myState, action) => {

    switch(action.type) {
            
            case 'ADDITEM': {
                return { ...state, products: action.payload, count: action.payload.reduce((total, p) => total + p.count, 0) }
            }

            case 'INCPRODUCTCOUNT': {

                return {
                    ...state,
                    products: action.payload,
                    count: state.count + 1
                }

            }


            case 'DECPRODUCTCOUNT': {

                    return {
                        ...state,
                        products: action.payload,
                        count: state.count - 1
                    }

             }


             case 'REMOVE_PRODUCT': {

                    return {
                        ...state,
                        products: action.payload,
                        count: action.payload.reduce((total, p) => total + p.count, 0)
                    }

            }

            
            default: {
                return state
            }

        }
}

export default cartReducer;
cartAction.js
  import { uniqBy } from 'lodash'
  

  export const addToCart = (item) => {
    
    let items = JSON.parse(localStorage.getItem('cart')) || [];

      items = uniqBy([{...item, count: 1}, ...items], '_id');

      localStorage.setItem('cart', JSON.stringify(items));

      return {

        type: 'ADDITEM',
        payload: items
          
      }
  }

  export const incProductCount = (item) => {

        let items = JSON.parse(localStorage.getItem('cart'));

        items = items.map(product => product._id === item._id ? {...item, count: product.count + 1} : product)

        localStorage.setItem('cart', JSON.stringify(items));

        return {
            type: 'INCPRODUCTCOUNT',
            payload: items
        }

  }


  export const decProductCount = (item) => {

     if(item.count > 1) {

         let items = JSON.parse(localStorage.getItem('cart'));
    
         items = items.map(product => product._id === item._id ? {...item, count: product.count - 1} : product)
    
         localStorage.setItem('cart', JSON.stringify(items));
    
         return {
             type: 'DECPRODUCTCOUNT',
             payload: items
         }
     }

     return {type: null}
      
}


export const removeProduct = (id) => {

    let items = JSON.parse(localStorage.getItem('cart'));
    
    items = items.filter(product => product._id !== id)

    localStorage.setItem('cart', JSON.stringify(items));

    return {
        type: 'REMOVE_PRODUCT',
        payload: items
    }

}
阿尤布·穆斯塔菲 — 06/04/2021
Type de fichier joint : unknown
favicon.ico
3.78 KB
阿尤布·穆斯塔菲 — 12/04/2021
const storage = multer.diskStorage({
  destination: function (req, file, cb) {
    cb(null, "../Frontend-ecommerce-platform/public/uploads");
  },
  filename: function (req, file, cb) {
    cb(null, new Date().toISOString().replace(/:/g, "-") + file.originalname);
  },
});
const uploadImage = multer({
  storage: storage,
  limits: {
    fileSize: 600000,
  },
  fileFilter(req, file, cb) {
    if (file.mimetype === "image/png" || "image/jpg") {
      cb(null, true);
    } else {
      cb(new Error("Please upload an image."));
    }
  },
});
阿尤布·穆斯塔菲 — 12/04/2021
exports.addAds = async (req, res, next) => {
  const ads = new Ads({
    picture: req.files[0].filename,
    pricing: req.body.pricing,
    startDate: req.body.startDate,
    endDate: req.body.endDate,
  });

  try {
    const savedAd = await ads.save();
    res.status(201).send(savedAd);
  } catch (error) {
    res.send(400).send({ message: error.message });
  }
};
BrahiMouissi — 13/04/2021
https://github.com/MS-brahim/vuejs-b1
GitHub
MS-brahim/vuejs-b1
Contribute to MS-brahim/vuejs-b1 development by creating an account on GitHub.

阿尤布·穆斯塔菲 — Aujourd’hui à 10:01
https://github.com/WebDevSimplified/Realtime-Simple-Chat-App
GitHub
WebDevSimplified/Realtime-Simple-Chat-App
Contribute to WebDevSimplified/Realtime-Simple-Chat-App development by creating an account on GitHub.

BrahiMouissi — Aujourd’hui à 10:50
``````
## Hi there 👋 You are welcome to my Github



- 🔭 I’m currently working on PRF && PP
- 🌱 I’m currently learning MERN Stack
Afficher plus
message.txt
3 Ko
 
## Hi there 👋 You are welcome to my Github



- 🔭 I’m currently working on PRF && PP
- 🌱 I’m currently learning MERN Stack



## ⚡ Technologies



![Php](https://img.shields.io/badge/-php-black?style=flat-square&logo=php)
![JavaScript](https://img.shields.io/badge/-JavaScript-black?style=flat-square&logo=javascript)
![MongoDB](https://img.shields.io/badge/-MongoDB-black?style=flat-square&logo=mongodb)
![Express](https://img.shields.io/badge/-Express-black?style=flat-square&logo=Express)
![React](https://img.shields.io/badge/-React-black?style=flat-square&logo=react)
![Nodejs](https://img.shields.io/badge/-Nodejs-black?style=flat-square&logo=Node.js)
![Vue.js](https://img.shields.io/badge/-Vue.js-430098?style=flat-square&logo=Vue.js)
![HTML5](https://img.shields.io/badge/-HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/-CSS3-1572B6?style=flat-square&logo=css3)
![Sass](https://img.shields.io/badge/-Sass-430098?style=flat-square&logo=sass)
![Bootstrap](https://img.shields.io/badge/-Bootstrap-563D7C?style=flat-square&logo=bootstrap)
![Git](https://img.shields.io/badge/-Git-black?style=flat-square&logo=git)
![Heroku](https://img.shields.io/badge/-Heroku-430098?style=flat-square&logo=heroku)

![Google Cloud](https://img.shields.io/badge/Google%20Cloud-black?style=flat-square&logo=google-cloud)

<!-- ![GitHub](https://img.shields.io/badge/-GitHub-181717?style=flat-square&logo=github)
![BitBucket](https://img.shields.io/badge/-BitBucket-darkblue?style=flat-square&logo=bitbucket)--!>


<!--
**MS-brahim/MS-brahim** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

[![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=ms-brahim)](https://github.com/ms-brahim/github-readme-stats)




