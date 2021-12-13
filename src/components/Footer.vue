<template>
  <footer id="footer">
    <div>
      <h4>email</h4>
      <p><a href="mailto:wndus24088@naver.com">wndus24088@naver.com</a></p>
    </div>
    <div>
      <h4>Kakao</h4>
      <p><a href="/">@wndus2408</a></p>
    </div>
    <div>
      <h4>social</h4>
      <ul>
        <!-- <li><a href="/">Youtube</a></li> -->
        <li><a href="https://www.instagram.com/ajooyeon/">Instargram</a></li>
        <li><a href="https://github.com/jooo21">Github</a></li>
        <li>
          <a href="https://aajy-000.gitbook.io/study-javascript/">GitBook</a>
        </li>
        <li>
          <a
            href="https://scarlet-raja-602.notion.site/notion-448a75949f87499aa8929e39bfebc200"
            >Notion</a
          >
        </li>
        <!-- <li><a href="/">Referecne</a></li> -->
        <!-- <li><a href="/">Tutorials</a></li> -->
        <!-- <li><a href="/">CSS</a></li> -->
      </ul>
    </div>
  </footer>
</template>

<style lang="scss">
#footer {
  position: fixed;
  left: 0;
  bottom: 0;
  z-index: 1200;
  width: 100%;
  color: #fff;
  border-top: 1px solid #2e2e30;
  font-family: "Rajdhani", "Chosunilbo_myungjo";
  font-weight: 500;
  background: #000;
  display: flex;
  align-items: center;
  bottom: 0;

  div {
    text-align: center;
    padding: 30px;

    h4,
    p,
    ul {
      display: inline-block;
    }

    h4 {
      font-family: "Rajdhani", "Chosunilbo_myungjo";
      font-weight: 500;
      opacity: 0.6;
      padding: 0 10px;
    }
  }

  div:nth-child(1) {
    flex: 1 1 25%;
    border-right: 1px solid #2e2e30;
  }

  div:nth-child(2) {
    flex: 1 1 20%;
    border-right: 1px solid #2e2e30;
  }

  div:nth-child(3) {
    flex: 1 1 55%;

    li {
      display: inline-block;
      padding: 0 10px;
    }
  }
}
</style>
