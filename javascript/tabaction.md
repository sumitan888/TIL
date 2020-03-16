# 今日覚えたというか調べたこと
<html>
<div class="tab-panel">
    <!--タブ-->
    <ul class="tab-group">
        <li class="tab tab-A is-active">Tab-A</li>
        <li class="tab tab-B">Tab-B</li>
        <li class="tab tab-C">Tab-C</li>
    </ul>
    
    <!--タブを切り替えて表示するコンテンツ-->
  <div class="panel-group">
        <div class="panel tab-A is-show">Content-A</div>
        <div class="panel tab-B">Content-B</div>
        <div class="panel tab-C">Content-C</div>
    </div>
</div>

<css>
.tab-group{
    display: flex;
    justify-content: center;
}
.tab{
    flex-grow: 1;
    padding:5px;
    list-style:none;
    border:solid 1px #CCC;
    text-align:center;
    cursor:pointer;
}
.panel-group{
    height:100px;
    border:solid 1px #CCC;
    border-top:none;
    background:#eee;
}
.panel{
    display:none;
}
.tab.is-active{
    background:#F00;
    color:#FFF;
    transition: all 0.2s ease-out;
}
.panel.is-show{
    display:block;
}


Resources
<javascript>
document.addEventListener('DOMContentLoaded', function(){
    // タブに対してクリックイベントを適用
    const tabs = document.getElementsByClassName('tab');
    for(let i = 0; i < tabs.length; i++) {
        tabs[i].addEventListener('click', tabSwitch);
    }

    // タブをクリックすると実行する関数
    function tabSwitch(){
        // タブのclassの値を変更
        document.getElementsByClassName('is-active')[0].classList.remove('is-active');
        this.classList.add('is-active');
        // コンテンツのclassの値を変更
        document.getElementsByClassName('is-show')[0].classList.remove('is-show');
        const arrayTabs = Array.prototype.slice.call(tabs);
        const index = arrayTabs.indexOf(this);
        document.getElementsByClassName('panel')[index].classList.add('is-show');
    };
});
