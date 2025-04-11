# MaxEval

## About
In recent years, significant breakthroughs in multimodal big language models have further promoted the development of mathematical reasoning techniques, involving multiple directions such as graph reasoning, table reasoning, and geometric problem solving. However, in the teaching scenarios of high school mathematics and physics, current models still face certain challenges when dealing with mathematical chart problems for teaching purposes. Part of the reason is attributed to the fact that most of the existing training image data comes from natural scene images, rather than specially designed teaching materials; At the same time, models often exhibit "excessive reasoning" during the problem-solving process, resulting in lengthy reasoning paths that are difficult to fit the cognitive habits and learning needs of high school students. To address this situation, we have undergone strict data screening and cleaning, and have constructed and released a multimodal test dataset specifically designed for high school mathematics and physics teaching, containing 18734 questions. The test question dataset not only contains problem-solving thinking chains that meet educational needs, making it easy to evaluate the performance of multimodal big language models in Chinese education scenarios, but also can be used as training data for model alignment and fine-tuning, thus compensating for the limitations of existing datasets mainly based on English mathematical thinking chains in Chinese scenarios and helping to promote the application and promotion of multimodal big language models in teaching.

## Update

The download link will be made public on June 30, 2026, and will be fully available for download

### Table: Question Category Statistics

| Category             | Type             | Physics | Math   |
|----------------------|------------------|---------|--------|
| Question Types       | Single Choice     | 2135    | -      |
|                      | Descriptive       | 579     | 15000  |
|                      | Multiple Choice   | 550     | -      |
|                      | Fill in the Blank | 10      | -      |
|                      | Experimental      | 455     | -      |
|                      | Comprehensive     | 4       | -      |
|                      | True/False        | 1       | -      |
| Number of Photos     | 1                 | 2619    | 2527   |
|                      | 2                 | 177     | 112    |
|                      | 3                 | 49      | 32     |
|                      | 4                 | 90      | 28     |
|                      | 5+                | 121     | 83     |
| Difficulty Level     | Easy              | 8       | 560    |
|                      | Fairly Easy       | 756     | 1148   |
|                      | Medium            | 2556    | 8860   |
|                      | Fairly Hard       | 385     | 2095   |
|                      | Hard              | 29      | 1182   |
|                      | (Unknown)         | -       | 1155   |



## Sample Data

<pre>
"id":"f2b9c56b-9c67-4e64-8415-9b482f317402",
"questionTypeName":"解答题",
"difficultyName":"偏难",
"content":"如图\\(1\\)，已知椭圆\\(Γ\\)的方程为\\(\\frac{x^{2}}{a^{2}}+\\frac{y^{2}}{b^{2}}=1\\left({a\\gt;b\\gt;0}\\right)\\)和椭圆\\(\\tau:\\frac{x^{2}}{4}+\\frac{y^{2}}{2}=1\\)，其中\\(A,B\\)分别是椭圆\\(\\tau\\)的左右顶点．<img src=\\"bcff03e3-8643-4895-a993-b57b22b94a00.png\\"> (1)若\\(A,B\\)恰好为椭圆\\(Γ\\)的两个焦点，椭圆\\(Γ\\)和椭圆\\(\\tau\\)有相同的离心率，求椭圆\\(Γ\\)的方程；(2)如图\\(2\\)，若椭圆\\(Γ\\)的方程为\\(\\frac{x^{2}}{8}+\\frac{y^{2}}{4}=1\\).\\(P\\)是椭圆\\(\\tau\\)上一点，射线\\(AP,BP\\)分别交椭圆\\(Γ\\)于\\(M,N\\)，连接\\(AN,BM\\)（\\(P,M,N\\)均在\\(x\\)轴上方）.求证：\\(NB,MA\\)斜率之积\\(k_{NB}⋅k_{MA}\\)为定值，求出这个定值；(3)在（2）的条件下，若\\(AN{/}{/}BM\\)，且两条平行线的斜率为\\(k\\left({k\\gt;0}\\right)\\)，求正数\\(k\\)的值．",
"analysis":"（1）由\\(\\tau:\\frac{x^{2}}{4}+\\frac{y^{2}}{2}=1\\)得：\\(A\\left({-2,0}\\right)\\)，\\(B\\left({2,0}\\right)\\)，且\\(\\tau\\)的离心率为\\(\\frac{\\sqrt[]{2}}{2}\\)；\\(\\becauseA,B\\)恰为\\(Γ\\)的两个焦点，即椭圆\\(Γ\\)的半焦距\\(c=2\\)，又椭圆\\(Γ\\)的离心率\\(e=\\frac{c}{a}=\\frac{2}{a}=\\frac{\\sqrt[]{2}}{2}\\)，\\(∴a=2\\sqrt[]{2}\\)，\\(∴b^{2}=a^{2}-c^{2}=4\\)，\\(∴\\)椭圆\\(Γ\\)的方程为：\\(\\frac{x^{2}}{8}+\\frac{y^{2}}{4}=1\\).（2）设\\(P\\left({x_{0},y_{0}}\\right)\\left({y_{0}\\gt;0}\\right)\\)，则\\(\\frac{x{_{0}^{2}}}{4}+\\frac{y{_{0}^{2}}}{2}=1\\)，即\\(y{_{0}^{2}}=2-\\frac{x{_{0}^{2}}}{2}\\)，\\(∴k_{NB}=k_{PB}=\\frac{y_{0}}{x_{0}-2}\\)，\\(k_{MA}=k_{PA}=\\frac{y_{0}}{x_{0}+2}\\)，\\(∴k_{NB}⋅k_{MA}=\\frac{y{_{0}^{2}}}{x{_{0}^{2}}-4}=\\frac{2-\\frac{x{_{0}^{2}}}{2}}{x{_{0}^{2}}-4}=\\frac{4-x{_{0}^{2}}}{2\\left({x{_{0}^{2}}-4}\\right)}=-\\frac{1}{2}\\)，\\(∴k_{NB}⋅k_{MA}\\)为定值，定值为\\(-\\frac{1}{2}\\).（3）<img src=\\"b7153c51-f940-48a4-8893-508dde67f6f3.png\\"> 设直线\\(AN\\)与椭圆\\(Γ\\)交于另一点\\(Q\\)，由椭圆对称性可知：\\(Q,M\\)关于坐标原点对称，设直线\\(AN:y=k\\left({x+2}\\right)\\)，\\(N\\left({x_{1},y_{1}}\\right)\\)，\\(Q\\left({x_{2},y_{2}}\\right)\\)，则\\(M\\left({-x_{2},-y_{2}}\\right)\\)，由\\(\\left\\{\\begin{matrix}\\begin{matrix}y=k\\left({x+2}\\right)\\\\\\frac{x^{2}}{8}+\\frac{y^{2}}{4}=1\\\\\\end{matrix}\\end{matrix}\\right.\\)得：\\(\\left({1+2k^{2}}\\right)x^{2}+8k^{2}x+8k^{2}-8=0\\)，则\\({Δ}=64k^{4}-\\left({32k^{2}-32}\\right)\\left({1+2k^{2}}\\right)=32k^{2}+32\\gt;0\\)，\\(∴x_{1}+x_{2}=-\\frac{8k^{2}}{1+2k^{2}}\\)，\\(x_{1}x_{2}=\\frac{8k^{2}-8}{1+2k^{2}}\\)，\\(∴y_{1}y_{2}=k^{2}\\left({x_{1}+2}\\right)\\left({x_{2}+2}\\right)=k^{2}\\left[x_{1}x_{2}+2\\left({x_{1}+x_{2}}\\right)+4\\right]=-\\frac{4k^{2}}{1+2k^{2}}\\)，由（2）知：\\(k_{NB}⋅k_{MA}=-\\frac{1}{2}\\)，\\(∴k_{NB}⋅k_{MA}=\\frac{y_{1}}{x_{1}-2}⋅\\frac{-y_{2}}{-x_{2}+2}=\\frac{y_{1}y_{2}}{\\left({x_{1}-2}\\right)\\left({x_{2}-2}\\right)}=\\frac{y_{1}y_{2}}{x_{1}x_{2}-2\\left({x_{1}+x_{2}}\\right)+4}\\)\\(=\\frac{-\\frac{4k^{2}}{1+2k^{2}}}{\\frac{8k^{2}-8}{1+2k^{2}}+\\frac{16k^{2}}{1+2k^{2}}+4}=\\frac{-k^{2}}{8k^{2}-1}=-\\frac{1}{2}\\)，解得：\\(k^{2}=\\frac{1}{6}\\)，又\\(k\\gt;0\\)，\\(∴k=\\frac{\\sqrt[]{6}}{6}\\).",
"answer":"",
},
</pre>


<pre>
{
"id": "f22989d7-bf72-425c-a147-5e5affefa784",
"questionTypeName": "解答题",
"difficultyName": "偏难",
"content": "如图所示，足够长的U形金属框架\\(NMPQ\\)静置在倾角为\\(\\alpha =30°\\)的光滑斜面上，\\(MN\\)与\\(PQ\\)平行且相距\\(L=1{ m }\\)．垂直于斜面的匀强磁场，在分界线\\(CC\\prime\\)两侧方向相反，磁感应强度大小均为\\(B=1T\\)．金属棒\\(DD\\prime\\)紧靠绝缘立柱a，b静止在上方的磁场中，接入电路的电阻\\(R=3Ω\\)．框架在平行于斜面向上的拉力作用下，由静止开始沿斜面向下做匀加速直线运动，加速度\\(a=0.5{m}/{s} ^ {2}\\)．已知\\(MP\\)部分阻值\\(r=1Ω\\)，其余电阻忽略不计，\\(MP\\)、\\(CC\\prime\\)、\\(DD\\prime\\)均平行于斜面与水平面的交界线\\(AA\\prime\\)，金属棒与框架的质量均为\\(m=0.1{kg}\\)，它们之间接触良好，取重力加速度\\(g=10{ m }/{ s } ^ { 2 }\\)．从框架开始运动至金属棒\\(DD\\prime\\)与立柱间的弹力为零的过程，U形框架克服拉力做功\\(W=\\frac { 7 } { 15 }{ J}\\)，在该过程中，求： <img src=\\"ce6a9abd-19bd-4fab-9b05-77be044968f3.png\\"> (1)通过金属棒\\(DD\\prime\\)的电荷量； (2)金属棒\\(DD\\prime\\)中产生的焦耳热．",
 "analysis": "（1）设框架从开始运动至金属棒\\(DD\\prime\\)与立柱间的弹力为零所用时间为t 弹力为零时有\\(BIL=mgsin\\alpha\\) 解得\\(I=0.5{ A }\\) 根据闭合电路欧姆定律有\\(I=\\frac { E } { R+r }\\) 由法拉第电磁感应定律有\\(E=BLv\\) 由速度公式\\(v=at\\) 联立代入数据解得\\(t=4{ s }\\) 根据电流定义式可得\\(q= \\bar {I}⋅t=\\frac { I } { 2 }t\\) 解得通过金属棒\\(DD\\prime\\)的电荷量\\(q=1{ C }\\) （2）框架从开始运动至\\(DD\\prime\\)与立柱间的弹力为零的过程中，框架下滑的距离\\(x=\\frac { 1 } { 2 }at ^ { 2 }\\) 由动能定理得\\(mgxsin\\alpha -W-Q=\\frac { 1 } { 2 }mv ^ { 2 }\\) 那么金属棒中产生的热量为\\(Q_{ DD\\prime } =\\frac { R } { R+r }Q\\) 代入数据解得金属棒\\(DD\\prime\\)中产生的焦耳热\\(Q_{ DD\\prime } =1{ J }\\).",
},
"answer": "",
</pre>
