<!DOCTYPE HTML PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <meta http-equiv="Content-Type" content="text/html; charset=gb2312" />
    <title>ͼ��ѡ��ؼ�</title>
    <link href="../../css/helpstyle.css" rel="stylesheet" type="text/css" />
</head>
<body>
    <div class="biaoti">
        ͼ��ѡ��ؼ�
    </div>    
    <div class="xiaobiaoti">
        һ��ʾ������
    </div>
    <div class="zhengwen">
        ��ʾ��ͨ���Զ���ͼ��ѡ��ؼ���ʵ���˼��ز�ͬͼ��Ĺ��ܡ�
    </div>
    <div class="xiaobiaoti">
        ����ʵ��˵��:
    </div>
    <div class="zhengwen">
        1�����ݣ�ʹ��һ��OSM�������ͼ��һ��Bing��ͼ��·ͼ�㣬һ��Bing��ͼ����Ӱ��ͼ�㣬�Լ�һ��Json��ʽ����ʸ��ͼ��һ��KML��ʽʸ��ͼ��<br />
        <br />
        2��ʵ�ֲ��裺
        <br />
        <br />
        [��ͼ��ʾ]<br />
        <br />
        ��1��������ol.js��ol��һ��רΪWebGIS�ͻ��˿����ṩ��JavaScript ����������ʵ�ֱ�׼��ʽ�����ĵ�ͼ���ݷ��ʡ�OpenLayers 3��OpenLayers�����ͼ������˸�����������ơ�openlayer2��Ȼ���㷺ʹ�ã�����JavaScript���������ڷ�չ�׶ο�ʼ����������ʾ���������
        OL3�������ִ������ģʽ�ӵײ���д������ol.css���ǵ�ͼ��ʽ�ļ��������˵�ͼ��ʽ�ķ������棬���磬���ɫ��ͼ����ʽ��ͼƬ��ʽ������ͼ����ʽ���߽���ʽ��������ʽ�ȣ���ʽһ�����ʸ��Ҫ��ͼ�㡣����
        <br />
        <br />
        ��2���ٴ���һ��IDΪ��mapCon����div�㣬����������ʽ��
        <br />
        <br />
        ��3��Ȼ����body��ǩ�����д��ͼ��ʾ�Ľű���
        &nbsp; &nbsp;1)����ol.source.OSM()�࣬��ȡOSM�����ͼ��<br /><br />
        &nbsp; &nbsp;2)����ol.layer.Tile()�࣬ͨ�����ø����source������ʾOSM�����ͼ��<br /><br />
        &nbsp; &nbsp;3)����ol.source.BingMaps()�࣬ͨ�����ø����imagerySet���Ի�ȡBing��ͼ��·ͼ�������Ӱ��ͼ�㣻<br /><br />
        &nbsp; &nbsp;4)����ol.layer.Tile()�࣬ͨ�����ø����source������ʾBing��ͼ��·ͼ�������Ӱ��ͼ�㣻<br /><br />
        &nbsp; &nbsp;5)����ol.source.Vector()�࣬ͨ�����ø����url���Ի�ȡJson��ʽ��KML��ʽ���ݣ�ͨ�����ø����format���Խ������ݣ�<br /><br />
        &nbsp; &nbsp;6)����ol.layer.Vector()�࣬ͨ�����ø����source������ʾһ��Json��ʽ����ʸ��ͼ��һ��KML��ʽʸ��ͼ��<br /><br />
        &nbsp; &nbsp;7)����ol.map()�࣬ͨ�����ø����layers���Լ�������ͼ�㣬��ͨ�����ø����view����ȷ����ͼ����ʾ���ĺͼ���<br /><br />
        <br />
        [���ӿؼ�]<br />
        <br />
        ��4������ͼ��Ŀ¼��������ȡ����ͼ�����ƺ����ԣ�������ѡ��Ԫ�أ�Ϊ��ѡ�����ӱ���¼�addChangeEvent()��
        <br />
        <br />
        ��5�����ͨ���Զ����loadLayersControl(���������Զ���ͼ��ѡ��ؼ����ӵ���ͼ�����С�
    </div>
    <div class="xiaobiaoti">
        ����������/����˵��
    </div>
    <div class="zhengwen">
        <font class="Class">1��ol.Map�ࣺ</font>������һ����ͼ������<br />
        <br />
        <font class="constructorTile">1.1 ���캯����</font>
        <br />
        <div class="zhuji">
            <font class="constructor">ol.Map(options)</font><br />
            <br />
            <font class="paraDescription">����˵����</font>
            <br />
            <font class="parameter">options��</font>��object���ͣ���ѡ����øö����������ԣ��Լ�ֵ�Ե���ʽ���á�<br />
            <font class="nextParameter">��1��target��</font>��Element | string | undefined����ѡ�ָ����ͼ���ڵ���ҳdivԪ�ص�id����������У�'mapCon'������ڹ���ʱδָ������������ol.Map()���setTarget()�����Ա���Ƶ�ͼ��<br />
            <font class="nextParameter">��2��layers��</font>��Array-[ol.layer.Base] | ol.Collection[ol.layer.Base | undefined]����ѡ�ָ�����ص�ͼ�㡣���δ���壬�򽫳��ֲ�����ͼ��ĵ�ͼ��ͼ���ǰ��ṩ��˳����ֵģ������Ҫʸ��ͼ����ʾ����Ƭͼ�㶥���������λ����Ƭͼ��֮�󣩡�<br />
            <font class="nextParameter">��3��view��</font>��ol.View | undefined����ѡ����õ�ͼ��ʾ��ͼ������ڹ���ʱδָ���������ͨ��ol.Map()���setView()����ָ�������򲻻���ȡͼ��Դ��<br />
        </div>
        <font class="funDescription">1.2 ����˵����</font>
        <br />
        <div class="zhuji">
            <font class="functionName">render()��</font>�����ͼ��Ⱦ����һ֡��������<br />
            <font class="functionName">getEventPixel(event)��</font>��ȡ�������������ڵĵ�ͼ����λ�á�<br />
            <font class="nextParameter">event��</font>(event���¼���<br />
            <font class="functionName">getView()��</font>��ȡ��ͼ��ͼ������ֵΪ{ol.View}�ࡣ<br />
            <font class="functionName">addLayer(layer)��</font>����ͼͼ�����ӵ���ͼ�����С�<br />
            <font class="nextParameter">layer��</font>(ol.layer.Base����ͼͼ�㡣<br />
            <font class="functionName">removeLayer(layer)��</font>��ͼ��ӵ�ͼ�������Ƴ���<br />
            <font class="nextParameter">layer��</font>(ol.layer.Base����ͼͼ�㡣<br />
        </div>
        <font class="Class">2��ol.layer.Tile�ࣺ</font>������һ����Ƭͼ���࣬������ʾ��Ƭ��Դ����Щ��Ƭ�ṩ��Ԥ��Ⱦ���������ض��ֱ��ʵ����ż�����֯����ƬͼƬ������ɡ�<br />
        <br />
        <font class="constructorTile">2.1 ���캯����</font>
        <br />
        <div class="zhuji">
            <font class="constructor">ol.layer.Tile(options)</font><br />
            <br />
            <font class="paraDescription">����˵����</font>
            <br />
            <font class="parameter">options��</font>��object���ͣ���ѡ����øö����������ԣ��Լ�ֵ�Ե���ʽ���á�<br />
            <font class="nextParameter">��1��source��</font>��ol.source.Tile�������Ϊͼ��������Դ�������ַ��<br />
        </div>
        <font class="Class">3��ol.source.OSM�ࣺ</font>OpenStreetMap��Ƭͼ����Դ��<br />
        <br />
        <font class="constructorTile">3.1 ���캯����</font>
        <br />
        <div class="zhuji">
            <font class="constructor">ol.source.OSM(opt_options)</font><br />
            <br />
            <font class="paraDescription">����˵����</font>
            <br />
            <font class="parameter">opt_options��</font>��object���ͣ���ѡ����ø�ͼ�������ѡ��Լ�ֵ�Ե���ʽ���á�<br />
            <font class="nextParameter">��1��cacheSize��</font>��number|undefined����ѡ����û����С��<br />Ĭ����2048��<br />
            <font class="nextParameter">��2��crossOrigin��</font>��null|string|undefined����ѡ����ü�����Ƭ�Ŀ������ԡ�<br />Ĭ���������ġ�<br />
            <font class="nextParameter">��3��maxZoom��</font>��number|undefined����ѡ��������Ŵ󼶱�<br />Ĭ����19��<br />
            <font class="nextParameter">��4��opaque��</font>��boolean|undefined����ѡ�����ͼ���Ƿ��ǲ�͸���ġ�<br />Ĭ����true��<br />
            <font class="nextParameter">��5��reprojectionErrorThreshold��</font>��number|undefined����ѡ�������ͶӰ�����������������Ϊ��λ��������ֵԽ�󣬾���Խ�͡�<br />Ĭ����0.5��<br />
            <font class="nextParameter">��6��tileLoadFunction��</font>��ol.TileLoadFunctionType|undefined  ����ѡ�����ͨ��������URL������Ƭ�Ĺ��ܡ�<br />Ĭ����function(imageTile, src) {imageTile.getImage().src = src; };<br />
            <font class="nextParameter">��7��url��</font>��string|undefined����ѡ�����urlģ�塣<br />Ĭ��Ϊhttps://{a-c}.tile.openstreetmap.org/{z}/{x}/{y}.png��<br />
            <font class="nextParameter">��8��wrapX��</font>��boolean|undefined����ѡ������Ƿ��ڵ�ͼˮƽ���������ظ���<br />Ĭ����true��
        </div>
        <font class="Class">4��ol.source.BingMaps�ࣺ</font>��Ӧ��ͼ����Ƭ��Դ��<br />
        <br />
        <font class="constructorTile">4.1 ���캯����</font>
        <br />
        <div class="zhuji">
            <font class="constructor">ol.source.BingMaps(options)</font><br />
            <br />
            <font class="paraDescription">����˵����</font>
            <br />
            <font class="parameter">options��</font>��object���ͣ���ѡ����ø�ͼ�������ѡ��Լ�ֵ�Ե���ʽ���á�<br />
            <font class="nextParameter">��1��key��</font>��string���ͣ���ѡ���Ӧ��Ƭ��ͼAPI��Կ��<br />
            <font class="nextParameter">��2��imagerySet��</font>��string���ͣ���ѡ����ñ�Ӧ��Ƭ��ͼ���͡� ���磺"Road","Aerial","AerialWithLabels", "collinsBart", "ordnanceSurvey"����ϸ�������£�<br />
            <font class="nextParameter">&nbsp;&nbsp;&nbsp;"Road"��</font>���������·Ӱ��<br />
            <font class="nextParameter">&nbsp;&nbsp;&nbsp;"Aerial"��</font>����Ӱ��<br />
            <font class="nextParameter">&nbsp;&nbsp;&nbsp;"AerialWithLabels"��</font>��·���Ǻ���Ӱ��<br />
            </font>
        </div>
        <font class="Class">5��ol.layer.Vector�ࣺ</font>������ʾ�ڿͻ�����Ⱦ��ʸ�����ݡ�<br />
        <br />
        <font class="constructorTile">5.1 ���캯����</font>
        <br />
        <div class="zhuji">
            <font class="constructor">ol.layer.Vector(opt_options)</font><br />
            <br />
            <font class="paraDescription">����˵����</font>
            <br />
            <font class="parameter">opt_options��</font>��object���ͣ���ѡ����ø�ͼ�������ѡ��Լ�ֵ�Ե���ʽ���á�<br />
            <font class="nextParameter">��1��source��</font>��string����ѡ�����ʸ��ͼ��������Դ��<br />
            <font class="nextParameter">��2��style��</font>��ol.style.Style | Array-[ol.style.style] | ol.StyleFunction | undefined��ͼ����ʽ��һ��ol.style.Style����һ��ol.style.Style���飬����һ������ ol.style.Style �ĺ�����<br />
        </div>
        <font class="Class">6��ol.source.Vector�ࣺ</font>ʸ��Ҫ����Դ��<br />
        <br />
        <font class="constructorTile">6.1 ���캯����</font>
        <br />
        <div class="zhuji">
            <font class="constructor">ol.source.Vector(opt_options)</font><br />
            <br />
            <font class="paraDescription">����˵����</font>
            <br />
            <font class="parameter">opt_options��</font>��object���ͣ���ѡ����ø�ͼ�������ѡ��Լ�ֵ�Ե���ʽ���á�<br />
            <font class="nextParameter">��1��url��</font>��string | ol.FeatureUrlFunction | undefined����ѡ�ʸ��ͼ�����ݵ�url��<br />
            <font class="nextParameter">��2��format��</font>��ol.format.Feature | undefined����ѡ�url�������ú�XHR��ʽ����Ҫ��ʹ�õ����ݸ�ʽ��<br />Ĭ����δ����ġ�<br />&nbsp;&nbsp;ע�⣺���������url��formatһ��Ҫ���ã�������Ժ��ԡ�<br />
            <font class="nextParameter">��3��attribution��</font>��ol.AttributionLike | undefined����ѡ���ͼ���½ǵ� logo ���������ݡ�<br />
            <font class="nextParameter">��4��features��</font>��Array-[ol.feature] | ol.Collection-[ol.feature] | undefined����ѡ�����Ҫ�أ����ַ�����ȡ�����ݡ�<br />
            <font class="nextParameter">��5��loader��</font>��ol.FeatureLoader | undefined����ѡ�����Ҫ��ʹ�õļ��غ�����<br />
            <font class="nextParameter">��6��logo��</font>��string | olx.LogoOptions | undefined����ѡ�logo���������ݡ�<br />
            <font class="nextParameter">��7��strategy��</font>��ol.LoadingStrategy | undefined����ѡ�����Ҫ��ʹ�õĲ��ԡ�<br />Ĭ����һ���Լ�������Ҫ�ء�<br />
            <font class="nextParameter">��8��wrapX��</font>��boolean | undefined����ѡ��Ƿ��ڵ�ͼˮƽ���������ظ���<br />Ĭ���� true��<br />
        </div>
        <font class="Class">7��ol.format.GeoJSON�ࣺ</font>����GeoJSON���ݣ��������ֶ�д������<br />
        <br />
        <font class="constructorTile">7.1 ���캯����</font>
        <br />
        <div class="zhuji">
            <font class="constructor"> ol.format.GeoJSON(opt_options)</font><br />
            <br />
            <font class="paraDescription">����˵����</font>
            <br />
            <font class="parameter">opt_options��</font>��object���ͣ���ѡ����ø�ͼ�������ѡ��Լ�ֵ�Ե���ʽ���á�<br />
            <font class="nextParameter">��1��defaultDataProjection��</font>��ol.ProjectionLike����ѡ�����Ĭ������ϵ��<br />Ĭ����EPSG:4326,��Ϊ��������ϵ��<br />
            <font class="nextParameter">��2��featureProjection��</font>��ol.ProjectionLike����ѡ�ͨ��format������Ҫ������ϵ��<br />
            <font class="nextParameter">��3��geometryName��</font>��string | undefined����ѡ�����Ҫ��ʱ����Ҫ������<br />
        </div>
        <font class="Class">8��ol.format.KML�ࣺ</font>����KML���ݣ��������ֶ�д������<br />
        <br />
        <font class="constructorTile">8.1 ���캯����</font>
        <br />
        <div class="zhuji">
            <font class="constructor"> ol.format.KML(opt_options)</font><br />
            <br />
            <font class="paraDescription">����˵����</font>
            <br />
            <font class="parameter">opt_options��</font>��object���ͣ���ѡ����ø�ͼ�������ѡ��Լ�ֵ�Ե���ʽ���á�<br />
            <font class="nextParameter">��1��extractStyles��</font>��boolean | undefined����ѡ��Ƿ���ȡKML��ʽ��<br />Ĭ����true��<br />
            <font class="nextParameter">��2��showPointNames��</font>��boolean | undefined����ѡ��Ƿ���ʾ�ص������ơ�<br />Ĭ����true��<br />
            <font class="nextParameter">��3��defaultStyle��</font>��Array-[l.style.style] | undefined����ѡ�Ĭ����ʽ��<br />Ĭ��ȱʡ��ʽΪGoogle Earth��<br />
            <font class="nextParameter">��4��writeStyles��</font>��boolean | undefined����ѡ��Ƿ��KMLд����ʽ ��<br />Ĭ����true��<br />
        </div>
        <font class="Class">9��ol.View�ࣺ</font>������һ����ͼ��ʾ��ͼ�ࡣol.View�����ǵ�ͼ��ʼ���ر���Ҫ��֮һ����ʾһ���򵥵Ķ�ά��ͼ��ӳ�䣬��Ҫ���Ƶ�ͼ���û��Ľ�������������ţ����ڷֱ��ʡ���ͼ����ת�ȡ�<br />
        <br />
        <font class="constructorTile">9.1 ���캯����</font>
        <br />
        <div class="zhuji">
            <font class="constructor">ol.View(opt_options)</font><br />
            <br />
            <font class="paraDescription">����˵����</font>
            <br />
            <font class="parameter">opt_options��</font>��Object���ͣ���ѡ����øö����������ԣ��Լ�ֵ�Ե���ʽ���á�<br />
            <font class="nextParameter">��1��center��</font>��ol.Coordinate|undefined����ѡ����õ�ͼ��ʾ���ģ�<br />
            <font class="nextParameter">��2��zoom��</font>��number|undefined����ѡ����õ�ͼ����ʾ������<br />
            <font class="nextParameter">��3��minZoom��</font>��number|undefined����ѡ����õ�ͼ��С���ż�������maxZoom(��minResolution)��zoomFactorһ��ʹ�ã����ͬʱ����maxResolution,maxResolution���ȼ�����minZoom��<br />Ĭ��ֵΪ0��<br />
            <font class="nextParameter">��4��maxZoom��</font>��number|undefined����ѡ����õ�ͼ������ż�������minZoom(��maxResolution)��zoomFactorһ��ʹ�ã����ͬʱ����minResolution,minResolution���ȼ�����maxZoom��<br />Ĭ��ֵΪ28��<br />
            <font class="nextParameter">��5��rotation��</font>��number|undefined����ѡ����ó�ʼ��ͼ����ת���ȣ�˳ʱ�뷽��)��<br />Ĭ��ֵΪ0��<br />
            <font class="nextParameter">��6��projection��</font>��ol.ProjectionLike����ѡ���ͼ��ͶӰ����ϵ��<br />Ĭ��ΪEPSG:3857����ī��������ϵ��<br />
        </div>
        <font class="funDescription">9.2 ����˵����</font>
        <br />
        <div class="zhuji">
            <font class="functionName">setCenter(center)��</font>���õ�ͼ��ͼ���������ꡣ<br />
            <font class="nextParameter">center��</font>(ol.Coordinate | undefined����ͼ��ͼ���������ꡣ<br />
            <font class="functionName">setZoom(zoom)��</font>���õ�ͼ��ͼ�����ż���<br />
            <font class="nextParameter">zoom��</font>(number����ͼ��ͼ�����ż���<br />
        </div>
        <p>
            <a href="http://openlayers.org/en/latest/apidoc/" alt="OpenLayers 3 API��"
               target="_blank">ע����ϸ˵����μ�OpenLayers3 API�ֲᡣ</a>
        </p>
    </div>
</body>
</html>