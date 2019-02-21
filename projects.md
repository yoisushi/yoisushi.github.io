---
layout: default
title: Projects
---

<div class="post">

  <h1 class="pageTitle">My Projects</h1>
  
  <div class="timeline-wrapper">

    <!-- 第一筆 -->
    <div class="timeline-step active">

      <div class="step-header">
	<div class="step-icon"></div>
	<!-- <div class="step-text"> -->
	  <h3><span style="color: #2e8b57">2016~2017</span><br/>[科技部大專生研究計畫] 一個有效的匿名雙向認證與金鑰協商方法</h3>
	<!-- </div> -->
      </div>

      <div class="step-content">
	<div class="step-connector">
	</div>

	<div class="step-inner">
	  <h3>計畫說明</h3>
	  <p>本計畫擬實作一個效能與安全兼具，且<b>適用於任何裝置</b>的 <code>匿名雙向認證</code> 與 <code>金鑰協商方法</code> ，以確保機密分享與安全認證，提供似<b>小型私人 PKI 驗證</b>、<b>PGP</b> 的功能。</p>
	  <h3>實作說明</h3>
	  <p>將 Prosanta Gope 與 Tzonelih Hwang 於 2015 年底新近發表的
	    <b> “An efficient mutual authentication and key agreement scheme preserving strong anonymity of the mobile user in global mobility networks” </b>
	     一論文中的認證方式實作於ASP.NET的網站應用程式中，<code>Mobile User</code> (MU)、<code>Foreign agent</code> (FA) 與 <code>Home agent</code> (HA) 之程式皆架設於不同的網站中，以跨站傳輸認證來模擬不同角色的三方互相進行傳輸與認證的過程，並比對三方計算的結果是否一致與正確，進而算出 <b>Session Key (會期金鑰)</b>。</p>
	  <h3>所用技術</h3>
	  <ul>
	    <li>ASP.NET C#</li>
	    <li>JsonP 跨站傳輸</li>
	    <li>以 SHA256、互斥或運算 及 AES256 做加密</li>
	  </ul>
	  <h3>相關連結</h3>
	  <p>[1] <a href="文章連結">詳細圖文說明</a></p>
	</div>
      </div>
    </div>

    <!-- 第二筆 -->
    <div class="timeline-step active">

      <div class="step-header">
        <div class="step-icon"></div>
        <!-- <div class="step-text"> -->
	 <h3><span style="color: #2e8b57">2016</span><br/>[畢業專題] 會議秘書 (Responsive Web App)</h3>
	<!-- </div> -->
      </div>

      <div class="step-content">
        <div class="step-connector">
        </div>

        <div class="step-inner">
	  <h3>功能說明</h3>
          <p>為了使會議的進行更加流暢及便利，故決定開發一個<b>整合性</b>與方便性兼具的軟體。在 <code>會議記錄</code> 與 <code>線上共同編輯</code> 方面，搭配了 <code>語音辨識</code> 功能，增進會議記錄的效率，並可於會議期間進行視訊成員的 <code>視訊錄影</code> ，便於保存會議影音紀錄；除此之外，亦可使用網站中的聊天室與其他員工聯絡，進行 <code>文字的即時通訊</code> 。無論使用任何裝置，皆可透過進入我們系統的網頁，查看 <code>會議提醒</code> 及 <code>行事曆</code>，迅速確認一切有關會議的事項。</p>
	  <h3>所用技術</h3>
	  <ul>
	    <li>繪製 UseCase、流程圖、DFD、UML類別圖、活動圖做系統分析與設計</li>
	    <li>ASP.NET C# + IIS Web Service</li>
	    <li>以 W3CSS 框架資源設計前端介面、響應式網頁</li>
	    <li>以 Web RTC API 做網頁上的即時串流多人視訊，並能將視訊存成MP4格式</li>
	    <li>以 Google Speech API 完成語音辨識功能</li>
	    <li>以 jQuery Ajax 結合 SQL Server 儲存、修改行事曆事項</li>
	    <li>以 Node.js 實作網頁即時聊天功能</li>
	    <li class="websec">網頁安全方面：</li>
	    <ul>
	      <li class="websec">Input 表單處 (如：登入頁面的TextBox) 內含防止 SQL Injection 攻擊的程式</li>
	      <li class="websec">登入密碼以 SHA256 加密</li>
	      <li class="websec">各頁面皆有後端 Session 驗證以防有心人士未通過驗證進入系統，網站以 SSL 加密保護</li>
	    </ul>
	  </ul>
	  <h3>相關連結</h3>
	  <p>[1] <a href="文章連結">詳細圖文說明</a></p>
        </div>
      </div>
    </div>    

    <!-- 第三筆 -->
    <div class="timeline-step active">

        <div class="step-header">
            <div class="step-icon"></div>
            <!-- <div class="step-text"> -->
	      <h3><span style="color: #2e8b57">2016</span><br/>[課堂專題] 隨你搭 (Android App)</h3>
	    <!-- </div> -->
        </div>

        <div class="step-content">
            <div class="step-connector">
            </div>

            <div class="step-inner">
	      <h3>功能說明</h3>
              <p>
		提供一個 <code>虛擬試衣</code> 的平台，供網路消費者可足不出戶就能利用本系統 <code>透過個人照片</code> 、預設模特兒的圖片來<code>穿搭衣服</code> ，享受網拍也能提供立即試穿的服務，試穿後亦可選擇 <code>購買穿搭商品</code>、<code>儲存穿搭圖片</code>。<br/>
		點選清單內的衣物與配件等商品，能以 <code>拖曳</code> 方式拉至自訂的個人全身照或預設 Model 身上，並可<code>調整商品大小</code>以便模擬真實試衣之情境。
	      </p>
	      <h3>所用技術</h3>
	      <ul>
		<li>Java (IDE 使用 Android Studio)</li>
		<li>用 JDBC (Java Database Connectivity) 技術連結 SQL Server</li>
	      </ul>
	      <H3>相關連結</h3>
	      <p>[1] <a href="文章連結">詳細圖文說明</a></p>
            </div>
        </div>
    </div>
    
  </div>
</div>
