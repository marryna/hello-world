# markdown的使用笔记
- 基本语法
- 实例展示
- 使用心得

## 一、在markdown中#号代表标题的意思等同于html中<h>标签有1-6个等级
  #### 李清照
  ### 易安居士
  ##  宋代人
  # 千古第一女词人

## 二、在markdown中-（+）或者*代表无序列表等同于ul li组合
  - 李清照比较有名的词牌
  - 声声慢·寻寻觅觅
  - 如梦令·常记溪亭日暮
  - 如梦令·昨夜雨疏风骤
  - 点绛唇·蹴罢秋千
  - 点绛唇·寂寞深闺
  - 声声慢·寻寻觅觅
  - 一剪梅·红藕香残玉簟秋

## 三、 有序列表直接使用数字加上空格即可，注意文字与序号之间的空格
  1.  李清照晚年是否再婚
  2.  李清照丈夫赵明诚是否有妾室
  3.  李清照一生好赌嗜酒


## 四、 段落引用使用一个大于号>,两个嵌套引用将有两条侧边线
  > 声声慢 --- 李清照
  寻寻觅觅，冷冷清清，凄凄惨惨戚戚<br>
  乍暖还寒时候，最难将息，三杯两盏淡酒，怎敌他晚来风急</br>
  雁过也真伤心，应是旧时相识。<br>

  >> 满地黄花堆积，憔悴损，如今有谁堪摘,</br>
  守着窗儿，独自怎生得黑</br>
  梧桐更兼细雨，点点滴滴，</br>
  这次第！怎一个愁字了得？

## 五、代码块```包裹中显示代码块或四个空格位
  ```
  点绛唇---李清照

  蹴罢秋千
  起来慵懒纤纤手
  露浓花瘦，薄汗轻衣透
  见客入来
  袜划金叉溜，和羞走
  倚门回首，却把青梅嗅
  ```

## 六、三个***一条分割线
***

## 七、这里是链接

  * [李清照百度百科](http://baike.baidu.com/link?url=5aLkpNfcEEMycR2xembXGELKglhOA33XAwFhM5Y6HpLdEKkm3ivSNWlBda-DSD5i_RW7sm9npE8GOI7D47X_5DClPXYlyszhF2ZvmTB6pgMoMFDEBPe9W8K34ktpUotD)
  * [hefoni](http://www.hefoni.ltd)

## 八、** **中间字体为粗体
  **一剪梅**</br>
  **红藕香残玉簟秋,轻解罗裳，独上兰舟。云中谁寄锦书来？雁字回时，月满西楼**</br>
  **花自飘零水自流，一种相思，两处闲愁。此情无计可消除，才下眉头，却上心头**</br>

## 九、用一个* *中间字体为斜体
  *如梦令*</br>
  *昨夜雨疏风骤,浓睡不消残*</br>
  *试问卷帘人,却道海棠依旧*</br>
  *知否，知否应是绿肥红瘦*</br>

## 十、上传图片使用链接方式 本方法使用链接为自主上传github上图片获得链接,直接使用img标签
  <img src='https://raw.githubusercontent.com/marryna/hello-world/master/img/02liqingzhao.jpg' alt='介夫子'></br>
  
## 10-1 使用!+[图片描述=img的alt属性]+(url)方式
   ![图片描述](https://raw.githubusercontent.com/marryna/hello-world/master/img/01liqingzhao.jpg) 
   
   
## 十一、给一段文字中嵌套链接使用 <> 中间添加链接
李清照 <https://github.com/marryna/hello-world/blob/master/README.md> 作为中国
古代文学史上少有的女作家，其作品中所体现的爱国思想，具有积极的社会意义。
历史的角度李清照的爱国思想，代表了中国古代广大妇女追求男女平等、关心国事、热爱祖国的一个侧面，
让后人从中看到了中国古代女性情感世界的另一面。而且，她还在众多爱国作家中为女性争得了一席之地
。不仅如此，李清照还开创了女作家爱国主义创作的先河，为后世留下了一个女性爱国的光辉典范，
特别是现代女性文学的创作产生了重大影响。 现实的角度认识李清照的爱国思想，能感受到女性在
国家统一、民族团结以及社会进步等方面的巨大作用。这对于在弘扬爱国主义，高举爱国大旗，
促进民族团结、国家统一和振兴中华时充分发挥妇女的社会作用，具有十分重大的意义。

## 十二、表格输入使用|分隔开内容
|姓名       |号/字       |朝代      |代表作      |
|---------- |---------- |--------- |-------     |
|李清照     |易安居士    |宋代       |声声慢，绝句 |
|蔡文姬     |昭姬        |东汉       |悲愤诗      |
|卓文君     |不祥        |西汉       |白头吟      |
|上官婉儿   |上官昭容     |唐代       |彩书怨      |

## 十三、反斜杠\ 使符号成为普通字符如图片引用方式
  markdown图片引用方式\!\[]\()

## 十四、在``中的内容会不编译显示，起到标记作用
  `<script></script>`
  `<link>`

## 十五、李清照诗作代表
  >夏日绝句---李清照</br>
  **生当作人杰，死亦为鬼雄。**</br>
  **至今思项羽，不肯过江东。**

## 十六、卓文君《白头吟》
  >**皑如山上雪，皎若云间月**</br>
  **闻君有两意，故来相决绝**</br>
  **今日斗酒会，明月照沟渠**</br>
  **躞蹀（xie'die）御沟上，沟水东西流**</br>
  **凄凄复凄凄，嫁娶不须啼**</br>
  **愿得一人心，白首不相离**</br>
  **竹竿何袅袅，鱼尾何筛筛**</br>
  **男儿重义气，何用钱刀为**</br>
   











   
