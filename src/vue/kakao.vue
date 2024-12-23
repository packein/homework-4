<template>
  <div>
    <h1>Welcome to My Vue App</h1>
    <!-- 카카오 로그인 버튼 -->
    <button class="kakao-login-btn" @click="kakaoLogin">카카오 로그인</button>
  </div>
</template>

<script>
export default {
  name: "MyComponent",
  methods: {
    kakaoLogin() {
      Kakao.Auth.login({
        success: (authObj) => {
          console.log("로그인 성공:", authObj);
          alert("카카오 로그인 성공!");
        },
        fail: (error) => {
          console.error("로그인 실패:", error);
          alert("카카오 로그인 실패");
        },
      });
    },
  },
};
</script>

<style>
.kakao-login-btn {
  background-color: #fee500;
  color: #3c1e1e;
  border: none;
  padding: 10px 20px;
  font-size: 16px;
  border-radius: 5px;
  cursor: pointer;
}
</style>
