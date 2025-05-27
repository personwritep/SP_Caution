// ==UserScript==
// @name        SP Caution ⭐
// @namespace        http://tampermonkey.net/
// @version        1.2
// @description        編集画面の自動保存
// @author        Ameblo Writer User
// @match        https://blog.ameba.jp/ucs/entry/srventryupdateinput*
// @match        https://blog.ameba.jp/ucs/entry/srventryupdatedraft.do
// @match        https://blog.ameba.jp/ucs/entry/srventryinsertinput.do
// @match        https://blog.ameba.jp/ucs/entry/srventrylist*
// @icon        https://www.google.com/s2/favicons?sz=64&domain=ameblo.jp
// @grant        none
// @updateURL        https://github.com/personwritep/SP_Caution/raw/main/SP_Caution.user.js
// @downloadURL        https://github.com/personwritep/SP_Caution/raw/main/SP_Caution.user.js
// ==/UserScript==


let sp_save=localStorage.getItem('SP_save'); // 保存確認フラグ 🔵
if(!sp_save){
    localStorage.setItem('SP_save', 0); }

let sp_act=localStorage.getItem('SP_act'); // SAVEボタン押下フラグ 🔵
if(!sp_act){
    localStorage.setItem('SP_act', 0); }

let sp_id=localStorage.getItem('SP_id'); // SAVEボタン押下フラグ 🔵
if(!sp_id){
    localStorage.setItem('SP_id', 0); }

let sp_set=localStorage.getItem('SPCaution'); // 自動保存間隔 🔵
if(!sp_set){
    localStorage.setItem('SPCaution', 10); }



let path_name=location.pathname;

if(path_name.includes('srventryupdateinput')){ // 再編集の編集画面
    let retry=0;
    let interval=setInterval(wait_target, 100);
    function wait_target(){
        retry++;
        if(retry>10){ // リトライ制限 10回 1sec
            clearInterval(interval); }
        let target=document.querySelector('.l-gHeaderLeft__link a'); // 監視 target
        if(target){
            clearInterval(interval);
            button_disp();
            auto_backup(); }}



    function button_disp(){ // 起動表示と警告ダイアログ
        sessionStorage.setItem("jslord_2", "1"); // 📛

        let lform=document.querySelector('.l-form');
        let lform_w=(lform.clientWidth)/2;


        let SVG_spch=
            '<svg id="svg_spch" viewBox="0 0 150 150">'+
            '<path d="M66 13C56 15 47 18 39 24C-12 60 18 146 82 137C92 135 '+
            '102 131 110 126C162 90 128 4 66 13M68 25C131 17 145 117 81 125C16 '+
            '133 3 34 68 25M69 40C61 41 39 58 58 61C66 63 73 47 82 57C84 60 '+
            '83 62 81 65C77 70 52 90 76 89C82 89 82 84 86 81C92 76 98 74 100 66'+
            'C105 48 84 37 69 40M70 94C58 99 66 118 78 112C90 107 82 89 70 94z">'+
            '</path></svg>';

        let disp=
            '<div id="sp_panel">'+
            '<span id="sp_save" class="sp_c">SAVE</span>'+
            '<span id="sp_pass" class="sp_c">PASS</span>'+
            '<input id="sp_time" type="number" min="2" max="30">'+
            '<span id="sp_min">min</span>'+ SVG_spch +
            '</div>'+
            '<style>'+
            '.p-submit__container > .js-submitButton[publishflg="1"] { background: #000; } '+
            '#sp_panel { position: fixed; bottom: 100px; z-index: -1; '+
            'right: calc(50vw - '+ lform_w +'px); padding: 0 10px; '+
            'font: bold 16px Meiryo; color: #fff; height: 60px; width: 210px; '+
            'background: #000; border: 1px solid #ccc; border-radius: 4px; '+
            'display: flex; justify-content: space-between; align-content: center; } '+
            '.sp_c { padding: 3px 6px 1px; margin: auto 0; '+
            'border: 1px solid #ccc; border-radius: 4px; cursor: pointer; } '+
            '.sp_c:hover { background: #b0bec5; } '+
            '#sp_time { position: relative; height: 27px; width: 48px; '+
            'margin: auto 0; padding: 1px 2px 0 4px; background: #000; '+
            'border: 1px solid #ccc; border-radius: 4px; -moz-appearance: textfield; } '+
            '#sp_time:hover { z-index: 2; -moz-appearance: unset; } '+
            'input[type=number]::-webkit-inner-spin-button { '+
            'height: 21px; margin-top: 1px; } '+
            '#sp_min { position: relative; left: -38px; bottom: -24px; height: 20px; '+
            'margin-right: -36px; font-size: 11px; } '+
            '#sp_min:hover { z-index: -1; } '+
            '#svg_spch { height: 16px; margin: 28px -4px 0 -2px; fill: #fff; '+
            'cursor: pointer; }'+
            '</style>';

        if(!document.querySelector('#sp_panel')){
            document.body.insertAdjacentHTML('beforeend', disp); }


        let sp_time=document.querySelector('#sp_time');
        if(sp_time){
            sp_time.value=sp_set; }


        let help=document.querySelector('#svg_spch');
        if(help){
            help.onclick=function(){
                let url='https://ameblo.jp/personwritep/entry-12770480518.html';
                window.open(url, '_blank'); }}

    } // button_disp()



    function auto_backup(){
        let sp_panel=document.querySelector('#sp_panel');
        let sp_save=document.querySelector('#sp_save');
        let sp_pass=document.querySelector('#sp_pass');
        let draft=document.querySelector('.js-submitButton[publishflg="1"]');
        let sp_time=document.querySelector('#sp_time');

        let alarm;

        auto_request();

        function auto_request(){
            alarm=setTimeout(()=>{
                save(); }, sp_set*60000); } // 自動タイマー設定 🔴


        function save(){
            sp_panel.style.zIndex='20';

            sp_save.onclick=function(){
                localStorage.setItem('SP_act', 1); // SAVEボタン押下のフラグをセット
                draft.click(); }

            sp_pass.onclick=function(){
                sp_panel.style.zIndex='-1';
                auto_request(); }}


        sp_time.addEventListener('input', function(){
            sp_set=sp_time.value;
            localStorage.setItem('SPCaution', sp_set); }); //  設定を更新 🔵


        draft.oncontextmenu=function(){
            clearTimeout(alarm);
            save();
            return false; }


        draft.onclick=function(event){
            if(!event.ctrlKey && !event.shiftKey){ //「下書き保存の確認画面」を表示する
                localStorage.setItem('SP_save', 1); // 確認フラグをセット
                clearTimeout(alarm);
                auto_request();

                setTimeout(()=>{
                    check_flag();
                }, 200); }

            else{ //「Ctrl+左Click」で「記事の編集・削除」を表示する
                localStorage.setItem('SP_act', 1); // SAVEボタン押下のフラグをセット
                setTimeout(()=>{
                    let entylist_url;
                    let date_input=document.querySelector('input[name="entry_created_datetime"]');
                    let date=date_input.value;
                    if(date=='current'){
                        entylist_url='https://blog.ameba.jp/ucs/entry/srventrylist.do'; }
                    else{
                        let date_q=date.slice(0, 7).replace('-', '');
                        entylist_url=
                            'https://blog.ameba.jp/ucs/entry/srventrylist.do?entry_ym=' + date_q; }

                    let entry_id=document.querySelector('input[name="entry_id"]');
                    localStorage.setItem('SP_id', entry_id.value); // 記事IDの検索フラグをセット

                    if(event.ctrlKey){
                        window.open(entylist_url); } //「記事の編集・削除」を開く
                    else if(event.shiftKey){
                        window.open(entylist_url,'_blank', 'toolbar=no'); }
                }, 200); }

        } // draft.onclick()


        function check_flag(){
            let retry=0;
            let interval=setInterval(wait_target, 200);
            function wait_target(){
                retry++;
                if(retry>30){ // 待機制限 6sec経過　通信エラー等の場合
                    clearInterval(interval);
                    red(1);
                    localStorage.setItem('SP_save', 0); }
                if(localStorage.getItem('SP_save')==0){ // 正常終了
                    clearInterval(interval);
                    red(0); }
                if(localStorage.getItem('SP_save')==2){ // 保存エラーを確認
                    clearInterval(interval);
                    red(1);
                    localStorage.setItem('SP_save', 0); }}}


        function red(n){
            let sp_panel=document.querySelector('#sp_panel');
            let sp_save=document.querySelector('#sp_save');
            if(sp_panel && sp_save){
                if(n==1){
                    sp_save.style.background='red'; }
                else{
                    sp_panel.style.zIndex='-1';
                    sp_save.style.background=''; }}
            let draft=document.querySelector('.js-submitButton[publishflg="1"]');
            if(draft){
                if(n==1){
                    draft.style.background='red'; }
                else{
                    draft.style.background='#000'; }}}

    } // auto_backup()

} // 下書き編集画面




if(path_name.includes('entry/srventrylist')){ //「記事の編集・削除」のリスト検索
    if(sp_id!=0){
        let entry_id=document.querySelectorAll('input[name="entry_id"]');
        let entry_item=document.querySelectorAll('.entry-item');

        let index=-1;
        for(let k=0; k<entry_id.length; k++){
            if(entry_id[k].value==sp_id){
                index=k; }}

        if(index!=-1){
            localStorage.setItem('SP_id', 0); // 検索フラグをリセットして停止
            entry_item[index].style.outline='2px solid #2196f3';
            entry_item[index].style.zIndex='2'; }
        else{
            let next=document.querySelector('.pagingArea .next');
            if(next && !next.classList.contains('disabled')){
                next.click(); }
            else{ // 記事が見つからなかった場合
                localStorage.setItem('SP_id', 0); }}} // 検索フラグをリセットして停止

} //「記事の編集・削除」のリスト検索




if(path_name.includes('srventryupdatedraft.do')){ // 下書き保存確認画面
    let Complete=document.querySelector('.entryComplete');
    if(Complete){
        localStorage.setItem('SP_save', 0); // 確認フラグをセット

        if(localStorage.getItem('SP_act')==1){ // SAVEボタン押下のフラグ
            localStorage.setItem('SP_act', 0); // フラグをリセット
            setTimeout(()=>{
                window.close();
            }, 100);
        }} // SAVEボタン押下時のみ、確認画面を自動削除

    let p_error=document.querySelector('.p-error');
    if(p_error){
        localStorage.setItem('SP_save', 2); // エラーの確認フラグをセット
        localStorage.setItem('SP_act', 0); } // SAVEボタン押下のフラグをリセット

} // 下書き保存確認画面




if(path_name.includes('srventryinsertinput')){ // 新規編集の編集画面
    button_disp();

    function button_disp(){ // 起動表示と警告ダイアログ
        let lform=document.querySelector('.l-form');
        let lform_w=(lform.clientWidth)/2;

        let disp=
            '<div id="sp_panel">'+
            '新規作成の編集画面の場合は<br>未保存記事の復元が可能です'+
            '</div>'+
            '<style>'+
            '.js-submitButton[publishflg="1"] { background: #000 !important; } '+
            '#sp_panel { position: fixed; bottom: 100px; z-index: -1; '+
            'right: calc(50vw - '+ lform_w +'px); padding: 6px 10px 4px; '+
            'font: normal 16px/20px Meiryo; color: #fff; height: auto; width: 210px; '+
            'background: #000; border: 1px solid #ccc; border-radius: 4px; '+
            'display: flex; justify-content: space-between; align-content: center; } '+
            '</style>';

        if(!document.querySelector('#sp_panel')){
            document.body.insertAdjacentHTML('beforeend', disp); }
    } // button_disp()


    let draft=document.querySelector('.js-submitButton[publishflg="1"]');
    let sp_panel=document.querySelector('#sp_panel');
    if(draft && sp_panel){
        draft.onmouseenter=()=>{
            sp_panel.style.zIndex='20'; }

        draft.onmouseleave=()=>{
            sp_panel.style.zIndex='-1'; }}

} // 新規編集の編集画面
