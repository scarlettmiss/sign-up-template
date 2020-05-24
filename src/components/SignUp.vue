<template>
  <div class="container">
    <div class="left">
      <img src="@/assets/left-image.png" />
    </div>
    <div class="right">
      <div class="member">
        <span>already a member ? </span>
        <router-link to="/">Sign in</router-link>
      </div>
      <div class="form-template">
        <h1 class="title">Sign up to this website</h1>
        <div class="buttons">
          <div class="buttonn" id="google-button">
            <img src="@/assets/google-plus(1).svg" /><span id="google-text"
              >Sign Up With Google</span
            >
          </div>
          <div class="buttonn" id="facebook-button">
            <img src="@/assets/facebook(1).svg" /><span id="facebook-text"
              >Sign Up With Facebook</span
            >
          </div>
        </div>
        <div class="line"><span>Or</span></div>
        <form class="name-form">
          <label for="fname">First name</label>
          <label for="lname">Last name</label>
          <br />
          <input type="text" id="fname" name="fname" />
          <input type="text" id="lname" name="lname" />
          <br />
          <label for="mail">Email Adress</label><br />
          <input type="email" id="email" name="email" />
          <br />
          <label for="password">Password</label><br />
          <input type="password" id="password" name="password" /><br />
          <input type="checkbox" id="terms" name="terms" value="accept" />
          <label for="terms" id="terms-label"
            >Creating an acount means you are okey with our
            <router-link to="/">Terms of Service Privacy Policy</router-link>
            and our
            <router-link to="/"
              >Default Notification Settings</router-link
            ></label
          ><br />
          <input type="submit" value="Create Account" />
        </form>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
$base-blue: #5e84eb;
$hover-color: #222b66;
$light-font: #7f7f7f;
$back: #fff;
.container {
  margin: 0;
  width: 80vw;
  height: 80vh;
  left: 20vh;
  top: 10vh;
  position: absolute;
  font-family: "Roboto";
}
.container {
  .left {
    float: left;
    width: 30%;
    height: 100%;
    img {
      width: 100%;
      height: 100%;
      border-radius: 5px 0 0px 5px;
    }
  }
}
.container {
  .right {
    float: right;
    width: 70%;
    height: 100%;
    background-color: $back;
    border-radius: 0 5px 5px 0;
  }
}
.container {
  .right {
    .member {
      text-align: right;
      margin: 40px;
      font-size: 1rem;
      font-weight: 600;
      color: $light-font;
      a:link,
      a:visited {
        color: $base-blue;
        text-decoration: none;
      }
      a:hover {
        color: $hover-color;
        text-decoration: none;
      }
    }
    .form-template {
      margin-left: 10%;
      text-align: left;

      .title {
        font-size: 2rem;
        font-weight: 900;
        margin: 30px 0 15px;
      }

      .buttons {
        .buttonn {
          margin-left: -5px;
          margin-right: 20px;
          position: relative;
          width: 30px;
          height: 50px;
          border-radius: 10px;
          display: inline-block;
          transition: width 0.4s cubic-bezier(0.87, 0.11, 0.33, 1),
            background-color 0.5s ease;
          will-change: width;
          &:hover {
            width: 200px;
            background-color: #4385f5;
            transition: width 0.4s cubic-bezier(0.87, 0.11, 0.33, 1),
              background-color 0.5s ease;
            img {
              filter: invert(100%) sepia(100%) saturate(0%) hue-rotate(288deg)
                brightness(102%) contrast(102%);
            }
          }
        }
        span {
          display: none;
          font-size: 0;
        }
        img {
          width: 35px;
          height: 50px;
          filter: invert(39%) sepia(0%) saturate(4%) hue-rotate(79deg)
            brightness(98%) contrast(91%);
          margin-left: 5px;
          margin-right: 20px;
        }
      }
      #google-button:hover {
        #google-text {
          position: absolute;
          display: inline;
          padding: 18px 0px;
          color: #fff;
          font-size: 0.8rem;
          font-weight: 700;
          width: 200px;
        }
      }
      #facebook-button:hover {
        #facebook-text {
          position: absolute;
          display: inline;
          padding: 18px 0px;
          color: #fff;
          font-size: 0.8rem;
          font-weight: 700;
          width: 200px;
        }
      }

      .line {
        text-align: center;
        border-bottom: 1px solid #000;
        line-height: 0.1em;
        margin: 15px 15% 30px;
        margin-left: 0;
        span {
          background: $back;
          padding: 0 50px;
          font-size: 1.3rem;
          font-weight: 700;
        }
      }

      form {
        label {
          font-size: 1.3rem;
          font-weight: 700;
          color: $light-font;
          margin-right: 5%;
          // display: inline;
          margin-right: 36%;
        }
        input {
          font-size: 1rem;
          font-weight: 600;
          color: #666;
          width: 38%;
          height: 50px;
          // display: inline;
          margin-top: 10px;
          margin-right: 75px;
          margin-bottom: 20px;
          border-radius: 10px;
          border: 2px solid #ccc;
          box-sizing: border-box;
          padding: 10px 20px;
          background-color: $back;
        }
        input:focus {
          border: 2px solid #aaa;
          border-radius: 10px;
          outline: none;
          background-color: $back;
        }
        input[type="checkbox"] {
          width: 25px;
          height: 30px;
          margin-right: 60px;
          display: inline;
        }

        input[type="submit"] {
          width: 30%;
          border: none;
          background-color: #ea4c89;
          color: #fff;
          font-weight: 700;
          font-size: 1rem;
          margin-top: 20px;
        }
        #email,
        #password {
          width: 85%;
          margin-right: 0;
        }

        #terms-label {
          display: inline;
          font-size: 1rem;
          position: absolute;
          margin-top: 8px;
          margin-right: 10%;
        }
      }
    }
  }
}
</style>
