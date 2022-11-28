<template>
  <main class="main bg-dark">
    <div class="container">
      <form class="search-form">
        <div class="form-control">
          <input type="text" placeholder="Search..." />
          <button>
            <svg
              width="16"
              height="16"
              viewBox="0 0 16 16"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
              class="search-icon"
            >
              <path
                d="M6.3833 12.8767C7.76953 12.8767 9.04785 12.4285 10.0938 11.6814L14.0283 15.616C14.2109 15.7986 14.4517 15.8899 14.709 15.8899C15.2485 15.8899 15.6304 15.4749 15.6304 14.9436C15.6304 14.6946 15.5474 14.4539 15.3647 14.2795L11.4551 10.3616C12.2769 9.28247 12.7666 7.94604 12.7666 6.49341C12.7666 2.98218 9.89453 0.110107 6.3833 0.110107C2.88037 0.110107 0 2.97388 0 6.49341C0 10.0046 2.87207 12.8767 6.3833 12.8767ZM6.3833 11.4988C3.64404 11.4988 1.37793 9.23267 1.37793 6.49341C1.37793 3.75415 3.64404 1.48804 6.3833 1.48804C9.12256 1.48804 11.3887 3.75415 11.3887 6.49341C11.3887 9.23267 9.12256 11.4988 6.3833 11.4988Z"
                fill="#000"
                fill-opacity="0.6"
              />
            </svg>
          </button>
        </div>
      </form>

      <section class="weather-content">
        <h1 class="weather-city">Moscow</h1>
        <p class="weather-temp">-5°</p>
        <p class="weather-desc">Snow</p>
      </section>
    </div>
  </main>
</template>

<style>
@import url(https://fonts.googleapis.com/css?family=Roboto:100,300,regular,500,700,900&display=swap);
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  font-family: Roboto, sans-serif;
  min-height: 100vh;
  width: 100%;
}
main {
  min-height: 100vh;
  background-repeat: no-repeat;
  background-position: center center;
  background-size: cover;
}
main.bg-dark {
  background-image: url("./assets/img/bg-dark.jpg");
}
.container {
  max-width: 1140px;
  margin: 0 auto;
  padding: 0 1rem;
}
.search-form {
  padding: 2rem 0;
}
.form-control {
  position: relative;
}
.search-form input {
  width: 100%;
  padding: 0.5rem 1rem;
  background: linear-gradient(
    168.44deg,
    rgba(46, 51, 90, 0.26) 1.62%,
    rgba(28, 27, 51, 0.26) 95.72%
  );
  box-shadow: inset 0px 4px 4px rgba(0, 0, 0, 0.25);
  border-radius: 10px;
  border: none;

  font-family: inherit;
  font-weight: 400;
  font-size: 1rem;
  line-height: 1.3;
  color: rgba(235, 235, 245, 0.8);
  outline: none;

  transition: 0.3s;
}

.search-form input::placeholder {
  font-family: inherit;
  color: rgba(235, 235, 245, 0.8);
}

.search-form input:active,
.search-form input:focus,
.search-form input:hover {
  box-shadow: inset 0px 2px 10px rgba(0, 0, 0, 0.25),
    0 4px 4px rgba(255, 255, 255, 0.25);
}

.search-form button {
  position: absolute;
  width: 30px;
  height: 30px;
  right: 0.5rem;
  top: 50%;
  transform: translateY(-50%);
  border: none;
  background: transparent;
  outline: none;
  cursor: pointer;
  transition: 0.3s;
}
.search-icon path {
  fill: rgba(235, 235, 245, 0.8);
  transition: 0.3s;
}

.search-form button:hover .search-icon path,
.search-form button:focus .search-icon path {
  fill: #fff;
}

.weather-content {
  padding-top: 5rem;
  text-align: center;
}

.weather-city {
  font-weight: 400;
  font-size: 2.5rem;
  line-height: 1.2;
  color: #ffffff;
}
.weather-temp {
  font-weight: 200;
  font-size: 6rem;
  color: #ffffff;
}
.weather-desc {
  font-weight: 600;
  font-size: 1.5rem;
  line-height: 1.2;
  color: rgba(235, 235, 245, 0.8);
}
</style>
