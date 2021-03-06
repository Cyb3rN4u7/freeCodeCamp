---
id: bad87fee1348bd9aeda08726
title: Delete Your jQuery Functions
required:
  - link: 'https://cdnjs.cloudflare.com/ajax/libs/animate.css/3.2.0/animate.css'
challengeType: 6
forumTopicId: 17561
localeTitle: 删除 jQuery 函数
---

## Description
<section id='description'>
这些动画开始看起来很酷，但是有时可能会让用户分心。
请删除<code>document ready function</code>内的三个 jQuery 函数，但保留<code>document ready function</code>本身。
</section>

## Instructions
<section id='instructions'>

</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: 删除<code>document ready function</code>中的三个 jQuery 函数。
    testString: assert(code.match(/\{\s*\}\);/g));
  - text: 保持<code>script</code>标签不变。
    testString: assert(code.match(/<script>/g));
  - text: 保持<code>$&#40document&#41.ready&#40function&#40&#41 {</code>在<code>script</code>标签的开头不变。
    testString: assert(code.match(/\$\(document\)\.ready\(function\(\)\s?\{/g));
  - text: "保持 'document ready function' 用<code>&#125;&#41;</code>闭合。"
    testString: assert(code.match(/.*\s*\}\);/g));
  - text: 保持<code>script</code>标签闭合。
    testString: assert(code.match(/<\/script>/g) && code.match(/<script/g) && code.match(/<\/script>/g).length === code.match(/<script/g).length);

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='html-seed'>

```html
<script>
  $(document).ready(function() {
    $("button").addClass("animated bounce");
    $(".well").addClass("animated shake");
    $("#target3").addClass("animated fadeOut");

  });
</script>

<!-- 请修改本行以上的代码 -->

<div class="container-fluid">
  <h3 class="text-primary text-center">jQuery Playground</h3>
  <div class="row">
    <div class="col-xs-6">
      <h4>#left-well</h4>
      <div class="well" id="left-well">
        <button class="btn btn-default target" id="target1">#target1</button>
        <button class="btn btn-default target" id="target2">#target2</button>
        <button class="btn btn-default target" id="target3">#target3</button>
      </div>
    </div>
    <div class="col-xs-6">
      <h4>#right-well</h4>
      <div class="well" id="right-well">
        <button class="btn btn-default target" id="target4">#target4</button>
        <button class="btn btn-default target" id="target5">#target5</button>
        <button class="btn btn-default target" id="target6">#target6</button>
      </div>
    </div>
  </div>
</div>
```

</div>



</section>

## Solution
<section id='solution'>

```html
<script>
  $(document).ready(function() {

  });
</script>

<!-- Only change code above this line. -->

<div class="container-fluid">
  <h3 class="text-primary text-center">jQuery Playground</h3>
  <div class="row">
    <div class="col-xs-6">
      <h4>#left-well</h4>
      <div class="well" id="left-well">
        <button class="btn btn-default target" id="target1">#target1</button>
        <button class="btn btn-default target" id="target2">#target2</button>
        <button class="btn btn-default target" id="target3">#target3</button>
      </div>
    </div>
    <div class="col-xs-6">
      <h4>#right-well</h4>
      <div class="well" id="right-well">
        <button class="btn btn-default target" id="target4">#target4</button>
        <button class="btn btn-default target" id="target5">#target5</button>
        <button class="btn btn-default target" id="target6">#target6</button>
      </div>
    </div>
  </div>
</div>
```

</section>
