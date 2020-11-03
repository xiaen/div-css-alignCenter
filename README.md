# div-垂直水平居中

  html结构

    <div style="width: 300px; height: 300px; background-color: gray;" class="wrap">
        <div style="width: 100px; height: 100px; background-color: hotpink;" class="box"></div>
    </div>



/* 第一种 */

flex布局

​	 .wrap {

​    display: flex;

​    align-items: center;

​    justify-content: center;

}



  /* 第二种 */

定位 + margin

​	.wrap {

​    position: relative;

  }

  .box {

​    position: absolute;

​    top: 0;

​    left: 0;

​    right: 0;

​    bottom: 0;

​    margin: auto;

  } 



  /* 第三种 */

定位 + transform

   .wrap {

​    position: relative;

  }

  .box {

​    position: absolute;

​    top: 50%;

​    left: 50%;

​    transform: translate(-50%, -50%);

  } 



  /* 第四种 */

定位 + margin负值

   .wrap {

​    position: relative;

  }

  .box {

​    position: absolute;

​    top: 50%;

​    left: 50%;

​    margin: -50px 0 0 -50px;

  } 



  /* 第五种 */

table-cell + vertical-align + text-align

   .wrap {

​    display: table-cell;

​    vertical-align: middle;

​    text-align: center;

  }

  .box {

​    display: inline-block;

  } 



  /* 第六种 */

利用overflow: hidden;抵消margin

   .wrap {

​    overflow: hidden;

  }

  .box {

​    margin: 50% auto;

​    transform: translateY(-50%);

  } 



  /* 第七种 */

line-height === height 垂直居中， 子div使用vertical-align: middle;

   .wrap {

​    text-align: center;

​    line-height: 300px;

  }

  .box {

​    display: inline-block;

​    vertical-align: middle;

  } 



  /* 第八种 */

新方法，使用grid

   .wrap {

​    display: grid;

  }

  .box {

​    align-self: center;

​    justify-self: center;

  } 