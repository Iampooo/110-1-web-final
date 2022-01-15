# My Card Books—給我通通記住 (Rememebro Totalum)
![](https://i.imgur.com/Sm6SLu5.png)
## Demo video
-:clapper: https://youtu.be/S13adVSS-yA
## Deploy Link
-:100: https://testingwp1101.herokuapp.com/
## Introduction
這次我們製作的是以單字卡為主體的幫助記憶程式，是以QUIZLET為參考，有鑑於市面上很多單字卡的APP都有很多廣告或是沒必要的功能，因此希望能打造一個更簡單更直接沒有太多干擾的單字卡網頁。
## User Interface
- Create new Card Book
- Delete Card Book
- Editable CardBook
- Create new Card
- Editable Card
- Delete Card
- TEST Mode

## Featured
- 首頁的單字本顯示盡量簡潔，建立新單字本時可以自訂使用不同的顏色作為分類。
![](https://i.imgur.com/Sm6SLu5.png)
- 建立新單字本時可自選封面顏色，方便區分。
![](https://i.imgur.com/8rqIHgh.png)
- 進入單字本，可以點擊加號新增字卡。點擊單字卡便可以直接編輯，操作直觀。
![](https://i.imgur.com/LFPw41T.png)
- 單字卡包含正反面，在測驗模式中可點擊翻面，確認答案。
![](https://i.imgur.com/Ba9nDrc.png)
![](https://i.imgur.com/a1C9nmD.png)
![](https://i.imgur.com/HJ7oRvq.png)

- 除了背單字外，由於卡片的正反面都是自定義的，也可以拿來做各種的測驗用途。
## FileTree

```
final/
└── frontend/
    └── src/                       --- 
        ├── App.js                 --- 
        ├── guide.js               --- 提供 route navigation
        ├── board.js               --- 初始主畫面
        ├── instance.js            --- axios api
        ├── Containers/            --- 
        |   ├── CardBook.js        --- 點進單個 CardBook 的畫面，包含 ManyCards 與 Test
        |   ├── ManyCards.js       --- 包含 DisplayCard 與 SingleCard
        |   └── Test.js            --- 測驗模式
        |
        └── Components/
            ├── CardBook.js        --- board 上的 CardBook 預覽小圖示
            ├── AddModal.js        --- 新增 CardBook 用的 component
            ├── DisplayCard.js     --- 大的單字顯示
            ├── LittleCards.js     --- 小單字卡列表
            ├── SingleCard.js      --- 小單字卡
            └── AddCardModal.js    --- 新增 SingleCard 用的 component
            
    backend/
    ├── server.js                  --- 建立後端server，連接前端、mongoDB
    ├── routes/                    
    |   ├── api/
    |   |   ├── handleCardBook.js  --- CardBook 的 API
    |   |   └── handleCard.js      --- Card 的 API
    |   └── index.js    
    |
    └── models/                    
            ├── CardBook.js        --- CardBook 的 Schema
            └── Card.js            --- Card 的 Schema
    
```
## 🔨 Packages/Tools for building 給我通通記住
- 前端：react/axios/antd/react-card-flip/styled-components/uuid
- 後端：nodemon/express/mongoose/body-parse

## Getting Started
### Installation
1. **Clone the repository**
    ```shell=
    git clone https://github.com/Iampooo/110-1-web-final
    ```
2. **Install the dependencies for the project**
    > go to the project directory (/110-1-web-final-main)
    
    ```shell=
    cd frontend
    npm install
    ```
    ```shell=
    cd ../backend
    npm install
    ```
3. **Prepare Environment Variables**

    > add these files to your backend directory
    > 1. ".env":
    > `MONGO_URL=mongodb+srv://aaabb:9876543@cluster0.ohxko.mongodb.net/final?retryWrites=true&w=majority`
    > (we have prepare our mongoDB account for you, feel free use your own mongoDB account)
    > 2. ".env_default"：
    > `MONGO_URL=`
4. **Start the project**
    > go to the project directory (/110-1-web-final-main)
    * open one terminal
    ```shell=
    npm run server
    ```

    
    
    * open another terminal
    ```shell=
    npm start
    ```
    * you can start using our app, have fun studying!
    
## Tutorial
If you haven't watched our demo video, go watch it and you'll know how easy to use our app:
>
<br>

Alternatively, the following tutorial can help you navigate through our app:
**Let's get started!**
### Main Page
![](https://i.imgur.com/Sm6SLu5.png)
##### Introduction
* The main page will display all the cardbooks you create
* Each cardbook can has properties of color, title and the number of words in it
* You can create a new cardbook
##### Do It Yourself！
* Click on the colorful part of a cardbook to enter
* Click on the trash can icon to delete it
* Press the plus button to add a new cardbook, your can decide the name and color of the cardbook
![](https://i.imgur.com/8rqIHgh.png)

### CardBook Page

* Each cardbook has two tabs: edit mode(Words) and test mode(Test)
![](https://i.imgur.com/Ru9gdz7.png)
#### Edit Mode(Words)
![](https://i.imgur.com/hT531WC.png)
* You can preview all the words in the cardbook at the top part to quickly review all the words
* Press the card to flip it
![](https://i.imgur.com/LFPw41T.png)
* You can edit all the cards at the below part
* Press the edit button to edit the front content and back content of a card
* Press the delete button to delete a card
* Press the plus button to add a new card
![](https://i.imgur.com/IpvaLox.png)
#### Test Mode
![](https://i.imgur.com/Ba9nDrc.png)
![](https://i.imgur.com/a1C9nmD.png)
* Press the "Test" tab to enter test mode
* Test mode will show you the front content of a card, press the card to see the back content (this might take a while to load all the words)
* Press "Got it" for words you know and "Uncertain" for words you don't words. Words you know will not be tested again 
* The test will end if you know all the words
![](https://i.imgur.com/HJ7oRvq.png)
