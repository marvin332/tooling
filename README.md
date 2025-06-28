<h1>Network</h1>
<h2>Дублирование ресурсов</h2>
<p>При проверке на дублирование смотрю на содержимое, объем ресурса после распаковки и сколько данных было передано по сети.</p>
<ul>
    <li>
        <span>captchapgrd - ресурс типа script загружается дважды</span>
        <img src="double1.png"/>
    </li>
    <li>
        <span> advanced.4fdec4f0c66230612adf.js - ресурс типа script загружен трижды</span>
        <img src="double2.png"/>
    </li>
    <li>
        <span>watch.js - ресурс типа script загружается трижды - причем первый раз по сети передается сжатый файл с большим размером, чем в остальных случаях, содержимое файлов и размер после распаковки идентичны для всех экземпляров</span>
        <img src="double3.png"/>
    </li>
    <li>
        <span> react-with-dom-and-polyfills.min.js - ресурс типа script загружен трижды</span>
        <img src="double4.png"/>
    </li>
     <li>
        <span>backend.636bb879d1085041bc19.js - ресурс типа script загружен трижды</span>
       <img src="double5.png"/>
   </li>
    <li>
        <span>ресурс типа document загружен трижды</span>
       <img src="double6.png"/>
   </li>
    <li>
        <span>шестикратно загружен bundle</span>
        <img src="double7.png"/>
    </li>
    <li>
        <span>трижды загружен document</span>
        <img src="double8.png"/>
    </li>
</ul>

<h2>Лишний размер ресурса</h2>
<ul>
    <li>
        <span>большие js или css файлы - лучшей практикой считается сведение бандлов до 200-300 кб. В этом случае лучше задуматься о code splitting</span>
        <img src="./bigSizeSrc/1.png"/>
    </li>
    <li>
        <span>тяжелые изображения: обычно стремятся к 100–200 кб, в этом случае следует задуматься о применении lazy loading и сжатии</span>
        <img src="./bigSizeSrc/2.png"/>
    </li>
    <li>
        <span>не оптимальный формат изображений png вместо webp, впрочем в данном случае не критично, изображение не слишком тяжелое</span>
        <img src="./bigSizeSrc/3.png"/>
    </li>
    <li>
        <span>все css файлы не минифицированы, в целом не критично, каждый из них не превышает 50кб</span>
    </li>
    <li>
        <span>ряд не минифицированных js, тоже не критично, имеют не большой размер</span>
        <img src="bigSizeSrc/unminified1.png"/>
        <img src="bigSizeSrc/unminified2.png"/>
    </li>
</ul>
<h2>Медленно загружающиеся ресурсы</h2>
<ul>
    <li>
        <span>На изображении видно, что самые долго загружающиеся ресурсы - изображения, возможно поможет сжатие, в случае со скриптами, можно отложить загрузку тяжелых скриптов - Async/Defer, code-splitting</span>
        <img src="./slowload/1.png"/>
    </li>
</ul>
<h2>Ресурсы, блокирующие загрузку</h2>
<ul>
    <li>
        <img src="./blockload.png"/>
    </li>
</ul>

<h1>Performance</h1>
<ul>
    <li>
        <h2>время в миллисекундах от начала навигации до события First Contentful Paint (FCP) = 502,06ms</h2>
        <img src="./Perfomance/FCP.png"/>
    </li>
    <li>
        <h2>время в миллисекундах от начала навигации до события Largest Contentful Paint (LCP) = 502,06ms</h2>
        <img src="./Perfomance/LSP.png"/>
    </li>
    <li>
        <h2>время в миллисекундах от начала навигации до события DOM Content Loaded (DCL) = 649,75ms</h2>
        <img src="./Perfomance/DSL.png"/>
    </li>
    <li>
        <h2>время в миллисекундах от начала навигации до события Load (L) = 3720ms</h2>
        <img src="./Perfomance/L.png"/>
    </li>
    <li>
        <h2>елемент LSP</h2>
        <img src="./Perfomance/LSP_element.png"/>
    </li>
    <li>
        <h2>сколько времени в миллисекундах тратится на разные этапы обработки документа (Loading, Scripting, Rendering, Painting)</h2>
        <h2>Loading = 6ms</h2>
        <h2>Scripting = 104ms</h2>
        <h2>Rendering = 155ms</h2>
        <h2>Painting = 8ms</h2>
        <img src="./Perfomance/time.png"/>
    </li>
</ul>

<h1>Coverage</h1>

<ul>
    <li>
        <h2>Вкладка Coverage</h2>
        <img src="./coverage/coverage.png"/>
    </li>
    <li>
        <h2>Объем не используемого CSS = 391.6 KB</h2>
        <img src="./coverage/unusedCSS.png"/>
    </li>
    <li>
        <h2>Объем не используемого JS = 1172.7 KB</h2>
        <img src="./coverage/unusedJS.png"/>
    </li>
</ul>
