<!DOCTYPE html>
<html>
<head>
  <title>实时观察粉丝数</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin: 30px;
    }

    h1 {
      color: #007bff;
    }

    #followersCount {
      font-size: 24px;
      font-weight: bold;
      color: #28a745;
    }
  </style>
</head>
<body>
  <h1>实时观察粉丝数：</h1>
  <p>当前粉丝数：<span id="followersCount">0</span></p>

  <script>
    function getFollowersCount() {
      // 这里编写获取实时粉丝数的逻辑
      // 这里暂时使用随机数模拟实时粉丝数的变化
      return Math.floor(Math.random() * 1000); // 随机生成一个 0 到 1000 的整数
    }

    function updateFollowersCount() {
      const followersCountSpan = document.getElementById('followersCount');
      const followersCount = getFollowersCount();
      followersCountSpan.innerText = followersCount;
    }

    // 每隔 5 秒钟更新一次粉丝数的显示
    setInterval(updateFollowersCount, 5000); // 5000 毫秒即 5 秒钟
  </script>
</body>
</html>

