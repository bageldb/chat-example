<template>
  <div>
    <div class="back-grad">
      <h1 class="main-head">Lets Talk</h1>
      <div class="chat-wrap">
        <div class="user-data-wrap">
          <userinfo name="Captain America" info="leader of the avengers" profile="https://i.pinimg.com/564x/9b/76/75/9b767505f5a5df3df348a898ba4ae8bb.jpg"/>
        </div>
        <div class="chat-box">
          <div class="bubble-boxes-wrap">
            <chatline msg="No problem" />
            <chatline msg="what?????" :user="true" />
            <chatline msg="I mean..." />
            <chatline :msg="'No!!'" />
            <chatline :msg="'Problem!!'" />
          </div>
          <div class="form-block">
            <textarea
              placeholder="Type a message"
              class="text-field big"
            ></textarea>
            <input type="submit" value="Send" class="button" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import chatline from "./components/chatline.vue";
import userinfo from "./components/userinfo.vue";

export default {
  name: "App",
  components: {
    chatline,
    userinfo,
  },
};
</script>

<style>
* {
    box-sizing: border-box;
}

body {
    font-family: Montserrat, sans-serif;
    color: #000;
    font-size: 18px;
    line-height: 1.5;
    margin: 0;
    min-height: 100%;
}

textarea {
    resize: none;
}

.back-grad {
    height: 100vh;
    max-height: 620px;
    padding-top: 40px;
    background-image: linear-gradient(135deg, #5786cd, #6e4ab0);
    text-align: center;
}

.bubble-boxes-wrap {
    height: calc(100% - 75px);
}

.chat-wrap {
    display: flex;
    overflow: hidden;
    width: 94%;
    max-width: 960px;
    margin-right: auto;
    margin-left: auto;
    border-radius: 10px;
    background-color: #fff;
    box-shadow: 1px 1px 30px 0 rgba(0, 0, 0, 0.2);
}

.name {
    font-size: 20px;
    line-height: 1.5;
}

.chat-bubble {
    display: inline-block;
    padding: 10px 30px;
    border-radius: 18px 18px 18px 0px;
    background-color: #5b7ac8;
    color: #fff;
}

.user-data-wrap {
    padding: 40px 20px;
    flex: 0 264px;
}

.chat-box {
    position: relative;
    height: 600px;
    flex: 1;
    background-color: #f5f5f5;
}

.bubble-boxes-wrap {
    overflow: auto;
    padding: 40px;
}

.main-head {
    color: #fff;
    font-size: 70px;
    line-height: 1.5;
    font-weight: 900;
}

.profile-pic {
    width: 104px;
    height: 104px;
    border-radius: 100%;
    object-fit: cover;
    object-position: top;
}

.user-data {
    color: #8b8b8b;
}

.form-block {
    position: absolute;
    left: 0%;
    top: auto;
    right: 0%;
    bottom: 0%;
    margin-bottom: 0px;
    padding: 15px;
    background-color: #ebeaea;
}

.text-field {
    font-family: Montserrat, sans-serif;
    color: #000;
    font-size: 18px;
    line-height: 1.5;
    padding: 9px;
    display: inline-block;
    width: 75%;
    height: 45px;
    margin-bottom: 0px;
    float: left;
    border: 1px none #000;
    border-radius: 10px;
}

.text-field:focus {
    outline: none;
}

.button {
    font-family: Montserrat, sans-serif;
    color: white;
    font-size: 18px;
    border: none;
    min-height: 100%;
    width: 22%;
    height: 45px;
    float: right;
    border-radius: 10px;
    background-color: #5b7ac8;
    transition: all 200ms ease;
    cursor: pointer;
}

.button:hover {
    filter: brightness(90%);
}

.button:active {
    filter: brightness(80%);
}

.button:focus {
    outline: none;
}

.chat-bubble-wrap {
    margin-bottom: 10px;
    text-align: left;
    width: 100%;
}

.chat-bubble-wrap.gray {
    text-align: right;
}

.gray .chat-bubble {
    border-bottom-left-radius: 18px;
    border-bottom-right-radius: 0px;
    background-color: #ddd9d9;
    color: #000;
}

@media screen and (max-width: 991px) {
    .chat-wrap {
        height: calc(100vh - 75px);
    }

    .user-data-wrap {
        -webkit-flex-basis: 200px;
        -ms-flex-preferred-size: 200px;
        flex-basis: 200px;
    }

    .chat-box {
        height: 100%;
    }

    .main-head {
        display: none;
    }
}

@media screen and (max-width: 767px) {
    .back-grad {
        max-height: none;
    }

    .chat-bubble {
        padding: 8px 20px;
    }

    .user-data-wrap {
        display: none;
    }

    .bubble-boxes-wrap {
        padding: 20px;
    }

    body {
        font-size: 16px;
    }

    .back-grad {
        padding-top: 10px;
    }

    .chat-wrap {
        height: calc(100vh - 20px);
    }
}
</style>