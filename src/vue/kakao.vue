methods: {
  kakaoLogin() {
    Kakao.Auth.login({
      success: (authObj) => {
        console.log('로그인 성공:', authObj);
        alert('카카오 로그인에 성공했습니다!');
      },
      fail: (error) => {
        console.error('로그인 실패:', error);
        alert('카카오 로그인에 실패했습니다.');
      },
    });
  }
}
