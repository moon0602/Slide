# ���[�U�X�N���v�g�̂��T��

�Г��׋���i2016/05/13�j
yamap_55

---

�ȉ��ŃX���C�h�����J���Ă��܂��B
https://slideck.io/github.com/yamap55/Slide/20160513/user_script.md

---

## �A�W�F���_
1. ���[�U�X�N���v�g�Ƃ�
2. �����b�g
3. �T���v��
4. Chrome�̏ꍇ
5. Firefox�̏ꍇ
6. �܂Ƃ�

---

## ���[�U�X�N���v�g�Ƃ�

>Web�y�[�W���J���Ƃ��ɁA�u���E�U���Ŏw�肵�Ă�����JavaScript�����s������@�\�ł��B����̃y�[�W�iGoogle�̌������ʂȂǁj���J�X�^�}�C�Y���ĕ\��������ł��܂��B
>Firefox��Greasemonkey���L���ł����A���݂͎�v�u���E�U�̂قƂ�ǂŗ��p�ł��܂��B
>[���[�UJavaScript](http://gimite.net/pukiwiki/index.php?%A5%E6%A1%BC%A5%B6JavaScript)

---

�L���ȃ��[�U�X�N���v�g���ƁAautopager���A�}�E�X�W�F�X�`���[�AGmail�̌����ڕύX�A�֗��{�^���ǉ��A�j�R�j�R����łق��ق��A�e�L�X�g�{�b�N�X�ɕ⊮���ǉ��A�y�V�̃��[���}�K�W���̃`�F�b�N�{�b�N�X���O������AJavaScript�̃Q�[���̃`�[�g��������B�B�B

---

���ł́A��̊g���@�\������܂��B

---

�ł́A���̃��[�U�X�N���v�g���Љ��̂��B

---

�ȒP�ɍ���B

---

Chrome�̊g���@�\���ȒP�ɍ��܂����A�����ƊȒP�I�iFirefox�͂�����Ɠ���B�j

---

������Ƃ������ŁA������Ƃ������B������s���ǂ��ł��������Ԃ����炷���Ŏg�p�������B

---

��̓I�ɂ́A�J�����̃A�v���P�[�V�����̃��O�C����ʂŌ����ʂ�1�N���b�N�Ń��O�C��������A�o�^��ʂœK���Ȓl����͂�����A����̃y�[�W�ɃV���[�g�J�b�g�������A�ʓ|�ȓ��͂�⊮������B

---

## �f��
- [�^�T�C�g](https://www.chi-bus.jp/)���J���B
- ���[�U�X�N���v�gon�B
    - �{���͎����ŋN������܂��B
- [�^�T�C�g](https://www.chi-bus.jp/)���J�������B
- **���I�ȕω����I**

---

## �R�[�h
```
// ==UserScript==
// @name         New Userscript
// @namespace    http://tampermonkey.net/
// @version      0.1
// @description  try to take over the world!
// @author       You
// @match        https://www.chi-bus.jp/
// @require      http://code.jquery.com/jquery-2.2.3.min.js
// @grant        none
// ==/UserScript==

(function() {
    'use strict';
    console.log("quick login start.");
    var list = ["��t�w","�Ђ܂��c�t��","�����O����"];
    var se = $("<select>").attr({"name":"hoge","id":"hoge"}).on("change",function(){$("input[name='q']").val($(this).val());}).appendTo($(".container-fluid"));
    $.each(list,function(i,v){
        se.append($("<option>").attr({"value":v}).text(v));
    });
    console.log("quick login end.");
})();
```

---

---
