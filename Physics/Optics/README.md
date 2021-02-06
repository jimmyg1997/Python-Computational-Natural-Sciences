# ❓PROBLEM STATEMENT

Arrange a combination of **6** thin lenses in order to make a high quality image from an object that is **8m** away from the front lens of the camera. 
The distance between the last lens to the image is **15 cm**. The height of the object is equal to **2m** and the image height might be varied from **0.5 cm to 3.5 cm** in order to fit to the physical size of the camera screen.
We will use **sperichal double convex lenses**

# 📝 PAPERS & REFERENCES used
We will use the theory and approach of the Flerackers et al. (1984) paper : **Combination of thin lenses-a computer oriented method**. In this paper, the image distances are calculated for up to **3** lenses. We will write a code for finding the image produced from a combination of **6** lenses.


# 💡 SOLUTION
```xml
<?xml version="1.0" encoding="UTF-8"?>
<mxfile host="app.diagrams.net" modified="2021-02-06T20:08:48.253Z" agent="5.0 (Macintosh; Intel Mac OS X 10_12_6) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/88.0.4324.146 Safari/537.36" etag="OmhzvMw4Z7LD8vUTOl5q" version="14.2.9" type="device">
  <diagram id="znQlFSOFQaeHU9nwjITa" name="Page-1">
    <mxGraphModel dx="1583" dy="742" grid="1" gridSize="10" guides="1" tooltips="1" connect="1" arrows="1" fold="1" page="1" pageScale="1" pageWidth="827" pageHeight="1169" math="0" shadow="0">
      <root>
        <mxCell id="0" />
        <mxCell id="1" parent="0" />
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-2" value="&lt;b&gt;OBJECT&lt;/b&gt;" style="shape=cylinder3;whiteSpace=wrap;html=1;boundedLbl=1;backgroundOutline=1;size=15;" vertex="1" parent="1">
          <mxGeometry x="60" y="300" width="60" height="80" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-3" value="" style="endArrow=classic;html=1;strokeWidth=2;fillColor=#f8cecc;strokeColor=#b85450;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="50" y="380" as="sourcePoint" />
            <mxPoint x="50" y="300" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-4" value="&lt;b&gt;h = 2m&lt;/b&gt;" style="text;html=1;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;whiteSpace=wrap;rounded=0;" vertex="1" parent="1">
          <mxGeometry x="-14" y="340" width="62" height="20" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-6" value="" style="endArrow=none;html=1;strokeWidth=6;fillColor=#dae8fc;strokeColor=#6c8ebf;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="50" y="380" as="sourcePoint" />
            <mxPoint x="1150" y="375" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-7" value="" style="shape=trapezoid;perimeter=trapezoidPerimeter;whiteSpace=wrap;html=1;fixedSize=1;rotation=-90;" vertex="1" parent="1">
          <mxGeometry x="368.75" y="371.25" width="142.5" height="10" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-8" value="" style="shape=trapezoid;perimeter=trapezoidPerimeter;whiteSpace=wrap;html=1;fixedSize=1;rotation=90;" vertex="1" parent="1">
          <mxGeometry x="378.75" y="371.25" width="142.5" height="10" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-11" value="" style="shape=image;verticalLabelPosition=bottom;labelBackgroundColor=#ffffff;verticalAlign=top;aspect=fixed;imageAspect=0;image=data:image/jpeg,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;" vertex="1" parent="1">
          <mxGeometry x="140" y="10" width="225" height="225" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-12" value="" style="shape=trapezoid;perimeter=trapezoidPerimeter;whiteSpace=wrap;html=1;fixedSize=1;rotation=-90;" vertex="1" parent="1">
          <mxGeometry x="488.25" y="368.75" width="142.5" height="10" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-13" value="" style="shape=trapezoid;perimeter=trapezoidPerimeter;whiteSpace=wrap;html=1;fixedSize=1;rotation=90;" vertex="1" parent="1">
          <mxGeometry x="498.25" y="368.75" width="142.5" height="10" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-14" value="" style="shape=trapezoid;perimeter=trapezoidPerimeter;whiteSpace=wrap;html=1;fixedSize=1;rotation=-90;" vertex="1" parent="1">
          <mxGeometry x="608.5" y="367.5" width="142.5" height="10" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-15" value="" style="shape=trapezoid;perimeter=trapezoidPerimeter;whiteSpace=wrap;html=1;fixedSize=1;rotation=90;" vertex="1" parent="1">
          <mxGeometry x="618.5" y="367.5" width="142.5" height="10" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-18" value="" style="shape=trapezoid;perimeter=trapezoidPerimeter;whiteSpace=wrap;html=1;fixedSize=1;rotation=-90;" vertex="1" parent="1">
          <mxGeometry x="728.5" y="367.5" width="142.5" height="10" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-19" value="" style="shape=trapezoid;perimeter=trapezoidPerimeter;whiteSpace=wrap;html=1;fixedSize=1;rotation=90;" vertex="1" parent="1">
          <mxGeometry x="738.5" y="367.5" width="142.5" height="10" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-20" value="" style="shape=trapezoid;perimeter=trapezoidPerimeter;whiteSpace=wrap;html=1;fixedSize=1;rotation=-90;" vertex="1" parent="1">
          <mxGeometry x="848.5" y="367.5" width="142.5" height="10" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-21" value="" style="shape=trapezoid;perimeter=trapezoidPerimeter;whiteSpace=wrap;html=1;fixedSize=1;rotation=90;" vertex="1" parent="1">
          <mxGeometry x="858.75" y="366.25" width="142.5" height="10" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-22" value="" style="shape=trapezoid;perimeter=trapezoidPerimeter;whiteSpace=wrap;html=1;fixedSize=1;rotation=-90;" vertex="1" parent="1">
          <mxGeometry x="969" y="367.5" width="142.5" height="10" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-23" value="" style="shape=trapezoid;perimeter=trapezoidPerimeter;whiteSpace=wrap;html=1;fixedSize=1;rotation=90;" vertex="1" parent="1">
          <mxGeometry x="979" y="367.5" width="142.5" height="10" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-25" value="" style="endArrow=classic;startArrow=classic;html=1;strokeWidth=1;dashed=1;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="50" y="400" as="sourcePoint" />
            <mxPoint x="434" y="400" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-26" value="&lt;b&gt;s&lt;sub&gt;1&lt;/sub&gt; = 8m&lt;/b&gt;" style="text;html=1;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;whiteSpace=wrap;rounded=0;" vertex="1" parent="1">
          <mxGeometry x="230" y="410" width="80" height="20" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-27" value="&lt;b&gt;o&lt;sub&gt;1&lt;/sub&gt;&lt;/b&gt;" style="text;html=1;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;whiteSpace=wrap;rounded=0;" vertex="1" parent="1">
          <mxGeometry x="70" y="270" width="40" height="20" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-29" value="" style="endArrow=none;html=1;strokeWidth=3;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="499" y="380" as="sourcePoint" />
            <mxPoint x="499" y="320" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-30" value="" style="endArrow=classic;startArrow=classic;html=1;strokeWidth=1;dashed=1;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="456" y="400" as="sourcePoint" />
            <mxPoint x="500" y="400" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-32" value="&lt;b&gt;i&lt;sub&gt;1&lt;/sub&gt; = o&lt;sub&gt;2&lt;/sub&gt;&lt;/b&gt;" style="text;html=1;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;whiteSpace=wrap;rounded=0;" vertex="1" parent="1">
          <mxGeometry x="460" y="290" width="80" height="20" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-34" value="" style="endArrow=classic;startArrow=classic;html=1;strokeWidth=1;dashed=1;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="500" y="400" as="sourcePoint" />
            <mxPoint x="554" y="400" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-36" value="" style="endArrow=none;html=1;strokeWidth=3;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="620" y="380" as="sourcePoint" />
            <mxPoint x="620" y="320" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-38" value="" style="endArrow=none;html=1;strokeWidth=3;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="742.5" y="380" as="sourcePoint" />
            <mxPoint x="742.5" y="320" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-39" value="" style="endArrow=none;html=1;strokeWidth=3;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="852.5" y="380" as="sourcePoint" />
            <mxPoint x="852.5" y="320" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-40" value="" style="endArrow=none;html=1;strokeWidth=3;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="1150" y="377.5" as="sourcePoint" />
            <mxPoint x="1150" y="317.5" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-41" value="" style="endArrow=none;html=1;strokeWidth=3;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="987.5" y="377.5" as="sourcePoint" />
            <mxPoint x="987.5" y="317.5" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-42" value="" style="endArrow=classic;startArrow=classic;html=1;strokeWidth=1;dashed=1;fillColor=#f8cecc;strokeColor=#b85450;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="445" y="270" as="sourcePoint" />
            <mxPoint x="565" y="270" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-43" value="" style="endArrow=none;html=1;strokeWidth=1;exitX=0;exitY=0;exitDx=0;exitDy=0;fillColor=#f5f5f5;strokeColor=#666666;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="445.30787878787874" y="304" as="sourcePoint" />
            <mxPoint x="445.52" y="250" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-46" value="" style="endArrow=classic;startArrow=classic;html=1;strokeWidth=1;dashed=1;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="575.5" y="400" as="sourcePoint" />
            <mxPoint x="615.5" y="400" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-47" value="&lt;b&gt;s&lt;sub&gt;1&lt;/sub&gt;&#39; = ?&amp;nbsp; &amp;nbsp;s&lt;sub&gt;2&lt;/sub&gt; = ?&lt;/b&gt;" style="text;html=1;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;whiteSpace=wrap;rounded=0;" vertex="1" parent="1">
          <mxGeometry x="450" y="410" width="110" height="20" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-49" value="&lt;b&gt;s&lt;sub&gt;2&lt;/sub&gt;&#39; = ?&amp;nbsp; &amp;nbsp;s&lt;sub&gt;3&lt;/sub&gt; = ?&lt;/b&gt;" style="text;html=1;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;whiteSpace=wrap;rounded=0;" vertex="1" parent="1">
          <mxGeometry x="570" y="410" width="110" height="20" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-50" value="" style="endArrow=classic;startArrow=classic;html=1;strokeWidth=1;dashed=1;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="615.5" y="400" as="sourcePoint" />
            <mxPoint x="675" y="400" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-51" value="" style="endArrow=classic;startArrow=classic;html=1;strokeWidth=1;dashed=1;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="695.5000000000001" y="400" as="sourcePoint" />
            <mxPoint x="742" y="400" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-52" value="" style="endArrow=classic;startArrow=classic;html=1;strokeWidth=1;dashed=1;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="742" y="400" as="sourcePoint" />
            <mxPoint x="795" y="400" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-53" value="&lt;b&gt;i&lt;sub&gt;2&lt;/sub&gt; = o&lt;sub&gt;3&lt;/sub&gt;&lt;/b&gt;" style="text;html=1;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;whiteSpace=wrap;rounded=0;" vertex="1" parent="1">
          <mxGeometry x="580.76" y="290" width="80" height="20" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-57" value="&lt;b&gt;s&lt;sub&gt;3&lt;/sub&gt;&#39; = ?&amp;nbsp; &amp;nbsp;s&lt;sub&gt;4&lt;/sub&gt; = ?&lt;/b&gt;" style="text;html=1;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;whiteSpace=wrap;rounded=0;" vertex="1" parent="1">
          <mxGeometry x="690" y="410" width="110" height="20" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-58" value="&lt;b&gt;i&lt;sub&gt;3&lt;/sub&gt; = o&lt;sub&gt;4&lt;/sub&gt;&lt;/b&gt;" style="text;html=1;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;whiteSpace=wrap;rounded=0;" vertex="1" parent="1">
          <mxGeometry x="700.69" y="290" width="80" height="20" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-62" value="&lt;b&gt;i&lt;sub&gt;4&lt;/sub&gt; = o&lt;sub&gt;5&lt;/sub&gt;&lt;/b&gt;" style="text;html=1;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;whiteSpace=wrap;rounded=0;" vertex="1" parent="1">
          <mxGeometry x="820.21" y="291" width="80" height="20" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-69" value="" style="endArrow=classic;startArrow=classic;html=1;strokeWidth=1;dashed=1;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="814" y="400" as="sourcePoint" />
            <mxPoint x="853" y="400" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-70" value="" style="endArrow=classic;startArrow=classic;html=1;strokeWidth=1;dashed=1;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="853" y="400" as="sourcePoint" />
            <mxPoint x="916" y="400" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-71" value="&lt;b&gt;s&lt;sub&gt;4&lt;/sub&gt;&#39; = ?&amp;nbsp; &amp;nbsp;s&lt;sub&gt;5&lt;/sub&gt; = ?&lt;/b&gt;" style="text;html=1;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;whiteSpace=wrap;rounded=0;" vertex="1" parent="1">
          <mxGeometry x="805.21" y="410" width="110" height="20" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-72" value="&lt;b&gt;i&lt;sub&gt;5&lt;/sub&gt; = o&lt;sub&gt;6&lt;/sub&gt;&lt;/b&gt;" style="text;html=1;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;whiteSpace=wrap;rounded=0;" vertex="1" parent="1">
          <mxGeometry x="940.21" y="292" width="80" height="20" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-76" value="" style="endArrow=classic;startArrow=classic;html=1;strokeWidth=1;dashed=1;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="936.21" y="400" as="sourcePoint" />
            <mxPoint x="987" y="400" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-77" value="" style="endArrow=classic;startArrow=classic;html=1;strokeWidth=1;dashed=1;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="987.5" y="400" as="sourcePoint" />
            <mxPoint x="1035" y="400" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-78" value="&lt;b&gt;s&lt;sub&gt;5&lt;/sub&gt;&#39; = ?&amp;nbsp; &amp;nbsp;s&lt;sub&gt;6&lt;/sub&gt; = ?&lt;/b&gt;" style="text;html=1;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;whiteSpace=wrap;rounded=0;" vertex="1" parent="1">
          <mxGeometry x="930" y="410" width="110" height="20" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-79" value="" style="endArrow=classic;startArrow=classic;html=1;strokeWidth=1;dashed=1;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="1057" y="400" as="sourcePoint" />
            <mxPoint x="1150" y="400" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-80" value="&lt;b&gt;s&lt;sub&gt;6&lt;/sub&gt;&#39; = 0.015&lt;/b&gt;" style="text;html=1;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;whiteSpace=wrap;rounded=0;" vertex="1" parent="1">
          <mxGeometry x="1050" y="410" width="110" height="20" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-81" value="&lt;b&gt;i&lt;sub&gt;6&lt;/sub&gt;&lt;/b&gt;" style="text;html=1;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;whiteSpace=wrap;rounded=0;" vertex="1" parent="1">
          <mxGeometry x="1108" y="292" width="80" height="20" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-82" value="&lt;b&gt;&lt;font color=&quot;#cc0000&quot;&gt;d = ?&lt;/font&gt;&lt;/b&gt;" style="text;html=1;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;whiteSpace=wrap;rounded=0;" vertex="1" parent="1">
          <mxGeometry x="482.5" y="240" width="45" height="20" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-86" value="&lt;b&gt;&lt;font color=&quot;#cc0000&quot;&gt;d = ?&lt;/font&gt;&lt;/b&gt;" style="text;html=1;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;whiteSpace=wrap;rounded=0;" vertex="1" parent="1">
          <mxGeometry x="602.5" y="240" width="45" height="20" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-87" value="&lt;b&gt;&lt;font color=&quot;#cc0000&quot;&gt;d = ?&lt;/font&gt;&lt;/b&gt;" style="text;html=1;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;whiteSpace=wrap;rounded=0;" vertex="1" parent="1">
          <mxGeometry x="722.5" y="240" width="45" height="20" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-88" value="&lt;b&gt;&lt;font color=&quot;#cc0000&quot;&gt;d = ?&lt;/font&gt;&lt;/b&gt;" style="text;html=1;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;whiteSpace=wrap;rounded=0;" vertex="1" parent="1">
          <mxGeometry x="837.71" y="240" width="45" height="20" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-89" value="&lt;b&gt;&lt;font color=&quot;#cc0000&quot;&gt;d = ?&lt;/font&gt;&lt;/b&gt;" style="text;html=1;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;whiteSpace=wrap;rounded=0;" vertex="1" parent="1">
          <mxGeometry x="962.5" y="240" width="45" height="20" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-91" value="" style="endArrow=none;html=1;strokeWidth=1;fillColor=#f5f5f5;strokeColor=#666666;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="50" y="600" as="sourcePoint" />
            <mxPoint x="50.20999999999998" y="383.71" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-92" value="" style="endArrow=none;html=1;strokeWidth=1;exitX=0;exitY=0;exitDx=0;exitDy=0;fillColor=#f5f5f5;strokeColor=#666666;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="564.9978787878788" y="307" as="sourcePoint" />
            <mxPoint x="565.21" y="253" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-93" value="" style="endArrow=none;html=1;strokeWidth=1;exitX=0;exitY=0;exitDx=0;exitDy=0;fillColor=#f5f5f5;strokeColor=#666666;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="685.3078787878787" y="304.9999999999999" as="sourcePoint" />
            <mxPoint x="685.5200000000002" y="251" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-94" value="" style="endArrow=classic;startArrow=classic;html=1;strokeWidth=1;dashed=1;fillColor=#f8cecc;strokeColor=#b85450;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="566" y="270" as="sourcePoint" />
            <mxPoint x="686" y="270" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-95" value="" style="endArrow=none;html=1;strokeWidth=1;exitX=0;exitY=0;exitDx=0;exitDy=0;fillColor=#f5f5f5;strokeColor=#666666;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="805.2078787878787" y="306.9999999999999" as="sourcePoint" />
            <mxPoint x="805.4200000000002" y="253" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-96" value="" style="endArrow=classic;startArrow=classic;html=1;strokeWidth=1;dashed=1;fillColor=#f8cecc;strokeColor=#b85450;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="686" y="270" as="sourcePoint" />
            <mxPoint x="806" y="270" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-97" value="" style="endArrow=none;html=1;strokeWidth=1;exitX=0;exitY=0;exitDx=0;exitDy=0;fillColor=#f5f5f5;strokeColor=#666666;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="924.8378787878787" y="306.9999999999999" as="sourcePoint" />
            <mxPoint x="925.0500000000002" y="253" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-98" value="" style="endArrow=classic;startArrow=classic;html=1;strokeWidth=1;dashed=1;fillColor=#f8cecc;strokeColor=#b85450;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="805.21" y="270" as="sourcePoint" />
            <mxPoint x="925.21" y="270" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-99" value="" style="endArrow=none;html=1;strokeWidth=1;exitX=0;exitY=0;exitDx=0;exitDy=0;fillColor=#f5f5f5;strokeColor=#666666;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="1045.3378787878787" y="306.9999999999999" as="sourcePoint" />
            <mxPoint x="1045.5500000000002" y="253" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-100" value="" style="endArrow=classic;startArrow=classic;html=1;strokeWidth=1;dashed=1;fillColor=#f8cecc;strokeColor=#b85450;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="925" y="270" as="sourcePoint" />
            <mxPoint x="1045" y="270" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-101" value="" style="endArrow=none;html=1;strokeWidth=1;fillColor=#f5f5f5;strokeColor=#666666;entryX=1;entryY=1;entryDx=0;entryDy=0;" edge="1" parent="1" target="xC9nd3o2VzPg7UcMz8dj-8">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="445" y="600" as="sourcePoint" />
            <mxPoint x="444.78000000000003" y="450.00000000000006" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-105" value="" style="endArrow=none;html=1;strokeWidth=1;fillColor=#f5f5f5;strokeColor=#666666;entryX=1;entryY=1;entryDx=0;entryDy=0;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="564.26" y="599.5" as="sourcePoint" />
            <mxPoint x="564.26" y="447" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-106" value="" style="endArrow=none;html=1;strokeWidth=1;fillColor=#f5f5f5;strokeColor=#666666;entryX=1;entryY=1;entryDx=0;entryDy=0;" edge="1" parent="1" target="xC9nd3o2VzPg7UcMz8dj-15">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="685" y="599.5" as="sourcePoint" />
            <mxPoint x="685" y="447" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-107" value="" style="endArrow=none;html=1;strokeWidth=1;fillColor=#f5f5f5;strokeColor=#666666;entryX=1;entryY=1;entryDx=0;entryDy=0;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="805.4599999999999" y="600.75" as="sourcePoint" />
            <mxPoint x="805.2099999999999" y="445" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-108" value="" style="endArrow=none;html=1;strokeWidth=1;fillColor=#f5f5f5;strokeColor=#666666;entryX=1;entryY=1;entryDx=0;entryDy=0;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="925.0699999999999" y="599.75" as="sourcePoint" />
            <mxPoint x="924.8199999999999" y="444" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-109" value="" style="endArrow=none;html=1;strokeWidth=1;fillColor=#f5f5f5;strokeColor=#666666;entryX=1;entryY=1;entryDx=0;entryDy=0;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="1045.25" y="600.75" as="sourcePoint" />
            <mxPoint x="1045" y="445" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-110" value="" style="endArrow=none;html=1;strokeWidth=1;fillColor=#f5f5f5;strokeColor=#666666;entryX=1;entryY=1;entryDx=0;entryDy=0;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="500" y="600" as="sourcePoint" />
            <mxPoint x="499.5800000000001" y="376.2500000000001" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-111" value="" style="endArrow=none;html=1;strokeWidth=1;fillColor=#f5f5f5;strokeColor=#666666;entryX=1;entryY=1;entryDx=0;entryDy=0;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="620.21" y="600" as="sourcePoint" />
            <mxPoint x="619.7900000000002" y="376.2500000000001" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-113" value="" style="endArrow=none;html=1;strokeWidth=1;fillColor=#f5f5f5;strokeColor=#666666;entryX=1;entryY=1;entryDx=0;entryDy=0;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="742.9200000000001" y="600" as="sourcePoint" />
            <mxPoint x="742.5000000000002" y="376.2500000000001" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-114" value="" style="endArrow=none;html=1;strokeWidth=1;fillColor=#f5f5f5;strokeColor=#666666;entryX=1;entryY=1;entryDx=0;entryDy=0;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="852.9200000000001" y="600" as="sourcePoint" />
            <mxPoint x="852.5000000000002" y="376.2500000000001" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-115" value="" style="endArrow=none;html=1;strokeWidth=1;fillColor=#f5f5f5;strokeColor=#666666;entryX=1;entryY=1;entryDx=0;entryDy=0;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="987.4200000000001" y="600" as="sourcePoint" />
            <mxPoint x="987.0000000000002" y="376.2500000000001" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-116" value="" style="endArrow=none;html=1;strokeWidth=1;fillColor=#f5f5f5;strokeColor=#666666;entryX=1;entryY=1;entryDx=0;entryDy=0;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="1150.42" y="600" as="sourcePoint" />
            <mxPoint x="1150.0000000000002" y="376.2500000000001" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-117" value="" style="endArrow=classic;html=1;strokeWidth=1;fillColor=#d5e8d4;strokeColor=#82b366;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="50" y="450" as="sourcePoint" />
            <mxPoint x="444" y="450" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-119" value="" style="endArrow=classic;html=1;strokeWidth=1;fillColor=#d5e8d4;strokeColor=#82b366;exitX=0.657;exitY=1.024;exitDx=0;exitDy=0;exitPerimeter=0;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="50.56000000000003" y="460.48" as="sourcePoint" />
            <mxPoint x="500" y="460" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-120" value="" style="endArrow=classic;html=1;strokeWidth=1;fillColor=#d5e8d4;strokeColor=#82b366;exitX=0.657;exitY=1.024;exitDx=0;exitDy=0;exitPerimeter=0;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="50.56000000000006" y="470.48" as="sourcePoint" />
            <mxPoint x="564" y="470" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-121" value="" style="endArrow=classic;html=1;strokeWidth=1;fillColor=#d5e8d4;strokeColor=#82b366;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="50" y="480" as="sourcePoint" />
            <mxPoint x="620" y="480" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-122" value="" style="endArrow=classic;html=1;strokeWidth=1;fillColor=#d5e8d4;strokeColor=#82b366;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="50" y="490" as="sourcePoint" />
            <mxPoint x="685" y="490" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-123" value="" style="endArrow=classic;html=1;strokeWidth=1;fillColor=#d5e8d4;strokeColor=#82b366;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="50" y="500" as="sourcePoint" />
            <mxPoint x="740" y="500" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-124" value="" style="endArrow=classic;html=1;strokeWidth=1;fillColor=#d5e8d4;strokeColor=#82b366;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="50" y="510" as="sourcePoint" />
            <mxPoint x="805" y="510" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-125" value="" style="endArrow=classic;html=1;strokeWidth=1;fillColor=#d5e8d4;strokeColor=#82b366;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="50" y="520" as="sourcePoint" />
            <mxPoint x="852" y="520" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-126" value="" style="endArrow=classic;html=1;strokeWidth=1;fillColor=#d5e8d4;strokeColor=#82b366;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="50" y="530" as="sourcePoint" />
            <mxPoint x="925" y="530" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-127" value="" style="endArrow=classic;html=1;strokeWidth=1;fillColor=#d5e8d4;strokeColor=#82b366;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="50" y="540" as="sourcePoint" />
            <mxPoint x="986" y="540" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-128" value="" style="endArrow=classic;html=1;strokeWidth=1;fillColor=#d5e8d4;strokeColor=#82b366;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="50" y="550" as="sourcePoint" />
            <mxPoint x="1045" y="550" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-129" value="" style="endArrow=classic;html=1;strokeWidth=1;fillColor=#d5e8d4;strokeColor=#82b366;" edge="1" parent="1">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="50" y="560" as="sourcePoint" />
            <mxPoint x="1149" y="560" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-131" value="&lt;meta charset=&quot;utf-8&quot;&gt;&lt;b style=&quot;color: rgb(0, 0, 0); font-family: helvetica; font-style: normal; letter-spacing: normal; text-align: center; text-indent: 0px; text-transform: none; word-spacing: 0px; background-color: rgb(248, 249, 250); font-size: 7px;&quot;&gt;x&lt;sub&gt;1&lt;/sub&gt;&lt;/b&gt;" style="text;whiteSpace=wrap;html=1;" vertex="1" parent="1">
          <mxGeometry x="38" y="434" width="10" height="30" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-132" value="&lt;b style=&quot;color: rgb(0 , 0 , 0) ; font-family: &amp;#34;helvetica&amp;#34; ; font-style: normal ; letter-spacing: normal ; text-align: center ; text-indent: 0px ; text-transform: none ; word-spacing: 0px ; background-color: rgb(248 , 249 , 250) ; font-size: 7px&quot;&gt;x&lt;sub&gt;i1&lt;/sub&gt;&lt;/b&gt;" style="text;whiteSpace=wrap;html=1;" vertex="1" parent="1">
          <mxGeometry x="38" y="444" width="10" height="30" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-133" value="&lt;b style=&quot;color: rgb(0 , 0 , 0) ; font-family: &amp;#34;helvetica&amp;#34; ; font-style: normal ; letter-spacing: normal ; text-align: center ; text-indent: 0px ; text-transform: none ; word-spacing: 0px ; background-color: rgb(248 , 249 , 250) ; font-size: 7px&quot;&gt;x&lt;sub&gt;2&lt;/sub&gt;&lt;/b&gt;" style="text;whiteSpace=wrap;html=1;" vertex="1" parent="1">
          <mxGeometry x="38" y="454" width="10" height="30" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-134" value="&lt;b style=&quot;color: rgb(0 , 0 , 0) ; font-family: &amp;#34;helvetica&amp;#34; ; font-style: normal ; letter-spacing: normal ; text-align: center ; text-indent: 0px ; text-transform: none ; word-spacing: 0px ; background-color: rgb(248 , 249 , 250) ; font-size: 7px&quot;&gt;x&lt;sub&gt;i2&lt;/sub&gt;&lt;/b&gt;" style="text;whiteSpace=wrap;html=1;" vertex="1" parent="1">
          <mxGeometry x="38" y="464" width="10" height="30" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-135" value="&lt;b style=&quot;color: rgb(0 , 0 , 0) ; font-family: &amp;#34;helvetica&amp;#34; ; font-style: normal ; letter-spacing: normal ; text-align: center ; text-indent: 0px ; text-transform: none ; word-spacing: 0px ; background-color: rgb(248 , 249 , 250) ; font-size: 7px&quot;&gt;x&lt;sub&gt;3&lt;/sub&gt;&lt;/b&gt;" style="text;whiteSpace=wrap;html=1;" vertex="1" parent="1">
          <mxGeometry x="38" y="474" width="10" height="30" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-136" value="&lt;b style=&quot;color: rgb(0 , 0 , 0) ; font-family: &amp;#34;helvetica&amp;#34; ; font-style: normal ; letter-spacing: normal ; text-align: center ; text-indent: 0px ; text-transform: none ; word-spacing: 0px ; background-color: rgb(248 , 249 , 250) ; font-size: 7px&quot;&gt;x&lt;sub&gt;i3&lt;/sub&gt;&lt;/b&gt;" style="text;whiteSpace=wrap;html=1;" vertex="1" parent="1">
          <mxGeometry x="38" y="484" width="10" height="30" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-137" value="&lt;b style=&quot;color: rgb(0 , 0 , 0) ; font-family: &amp;#34;helvetica&amp;#34; ; font-style: normal ; letter-spacing: normal ; text-align: center ; text-indent: 0px ; text-transform: none ; word-spacing: 0px ; background-color: rgb(248 , 249 , 250) ; font-size: 7px&quot;&gt;x&lt;sub&gt;4&lt;/sub&gt;&lt;/b&gt;" style="text;whiteSpace=wrap;html=1;" vertex="1" parent="1">
          <mxGeometry x="38" y="494" width="10" height="30" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-138" value="&lt;b style=&quot;color: rgb(0 , 0 , 0) ; font-family: &amp;#34;helvetica&amp;#34; ; font-style: normal ; letter-spacing: normal ; text-align: center ; text-indent: 0px ; text-transform: none ; word-spacing: 0px ; background-color: rgb(248 , 249 , 250) ; font-size: 7px&quot;&gt;x&lt;sub&gt;i4&lt;/sub&gt;&lt;/b&gt;" style="text;whiteSpace=wrap;html=1;" vertex="1" parent="1">
          <mxGeometry x="38" y="504" width="10" height="30" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-139" value="&lt;b style=&quot;color: rgb(0 , 0 , 0) ; font-family: &amp;#34;helvetica&amp;#34; ; font-style: normal ; letter-spacing: normal ; text-align: center ; text-indent: 0px ; text-transform: none ; word-spacing: 0px ; background-color: rgb(248 , 249 , 250) ; font-size: 7px&quot;&gt;x&lt;sub&gt;5&lt;/sub&gt;&lt;/b&gt;" style="text;whiteSpace=wrap;html=1;" vertex="1" parent="1">
          <mxGeometry x="38" y="514" width="10" height="30" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-140" value="&lt;b style=&quot;color: rgb(0 , 0 , 0) ; font-family: &amp;#34;helvetica&amp;#34; ; font-style: normal ; letter-spacing: normal ; text-align: center ; text-indent: 0px ; text-transform: none ; word-spacing: 0px ; background-color: rgb(248 , 249 , 250) ; font-size: 7px&quot;&gt;x&lt;sub&gt;i5&lt;/sub&gt;&lt;/b&gt;" style="text;whiteSpace=wrap;html=1;" vertex="1" parent="1">
          <mxGeometry x="38" y="524" width="10" height="30" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-141" value="&lt;b style=&quot;color: rgb(0 , 0 , 0) ; font-family: &amp;#34;helvetica&amp;#34; ; font-style: normal ; letter-spacing: normal ; text-align: center ; text-indent: 0px ; text-transform: none ; word-spacing: 0px ; background-color: rgb(248 , 249 , 250) ; font-size: 7px&quot;&gt;x&lt;sub&gt;6&lt;/sub&gt;&lt;/b&gt;" style="text;whiteSpace=wrap;html=1;" vertex="1" parent="1">
          <mxGeometry x="38" y="534" width="10" height="30" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-142" value="&lt;b style=&quot;color: rgb(0 , 0 , 0) ; font-family: &amp;#34;helvetica&amp;#34; ; font-style: normal ; letter-spacing: normal ; text-align: center ; text-indent: 0px ; text-transform: none ; word-spacing: 0px ; background-color: rgb(248 , 249 , 250) ; font-size: 7px&quot;&gt;x&lt;sub&gt;i6&lt;/sub&gt;&lt;/b&gt;" style="text;whiteSpace=wrap;html=1;" vertex="1" parent="1">
          <mxGeometry x="38" y="544" width="10" height="30" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-144" value="&lt;b&gt;h&#39;&amp;nbsp;&lt;/b&gt;&lt;b style=&quot;color: rgb(32 , 33 , 36) ; font-family: &amp;#34;arial&amp;#34; , sans-serif ; font-size: 14px ; text-align: left ; background-color: rgb(255 , 255 , 255)&quot;&gt;∈ [0.005 , 0.035]&lt;/b&gt;" style="text;html=1;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;whiteSpace=wrap;rounded=0;" vertex="1" parent="1">
          <mxGeometry x="1160" y="330" width="130" height="20" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-145" value="&lt;b&gt;&lt;font color=&quot;#cc0000&quot;&gt;f = ?&lt;/font&gt;&lt;/b&gt;" style="text;html=1;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;whiteSpace=wrap;rounded=0;" vertex="1" parent="1">
          <mxGeometry x="424.5" y="220" width="45" height="20" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-146" value="&lt;b&gt;&lt;font color=&quot;#cc0000&quot;&gt;f = ?&lt;/font&gt;&lt;/b&gt;" style="text;html=1;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;whiteSpace=wrap;rounded=0;" vertex="1" parent="1">
          <mxGeometry x="543" y="220" width="45" height="20" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-147" value="&lt;b&gt;&lt;font color=&quot;#cc0000&quot;&gt;f = ?&lt;/font&gt;&lt;/b&gt;" style="text;html=1;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;whiteSpace=wrap;rounded=0;" vertex="1" parent="1">
          <mxGeometry x="663.25" y="220" width="45" height="20" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-149" value="&lt;b&gt;&lt;font color=&quot;#cc0000&quot;&gt;f = ?&lt;/font&gt;&lt;/b&gt;" style="text;html=1;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;whiteSpace=wrap;rounded=0;" vertex="1" parent="1">
          <mxGeometry x="784" y="220" width="45" height="20" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-150" value="&lt;b&gt;&lt;font color=&quot;#cc0000&quot;&gt;f = ?&lt;/font&gt;&lt;/b&gt;" style="text;html=1;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;whiteSpace=wrap;rounded=0;" vertex="1" parent="1">
          <mxGeometry x="907.5" y="220" width="45" height="20" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-151" value="&lt;b&gt;&lt;font color=&quot;#cc0000&quot;&gt;f = ?&lt;/font&gt;&lt;/b&gt;" style="text;html=1;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;whiteSpace=wrap;rounded=0;" vertex="1" parent="1">
          <mxGeometry x="1027.75" y="220" width="45" height="20" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-153" value="&lt;font size=&quot;1&quot;&gt;&lt;b&gt;&lt;u style=&quot;font-size: 24px&quot;&gt;COMBINATION OF THIN (DOUBLE CONVEX) LENSES&lt;/u&gt;&lt;/b&gt;&lt;/font&gt;" style="text;html=1;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;whiteSpace=wrap;rounded=0;" vertex="1" parent="1">
          <mxGeometry x="310" y="20" width="847.79" height="20" as="geometry" />
        </mxCell>
        <mxCell id="xC9nd3o2VzPg7UcMz8dj-154" value="&lt;i&gt;double convex lens&amp;nbsp;&lt;br&gt;[ focal point/ image at the RIGHT]&lt;/i&gt;" style="text;html=1;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;whiteSpace=wrap;rounded=0;" vertex="1" parent="1">
          <mxGeometry x="148.75" y="240" width="220" height="20" as="geometry" />
        </mxCell>
      </root>
    </mxGraphModel>
  </diagram>
</mxfile>
```


<center><a href="https://ibb.co/4jjY4pR"><img src="https://i.ibb.co/0ffFYry/7.png" alt="7" border="0"></a><br /><a target='_blank' href='https://imgbb.com/'></a><br /> </center>

<center><a href="https://ibb.co/ZKYcX5T"><img src="https://i.ibb.co/L6J9Rmp/8.png" alt="8" border="0"></a></center>

<center><a href="https://ibb.co/sHQYMqw"><img src="https://i.ibb.co/Kw7v3Wq/9.png" alt="9" border="0"></a></center>


# Explanations



| **Definition**| **Explanation**|
|:-:|:-:|
|**Lens**|Optical Lenses are optical components designed to focus or diverge light. |
|**Double Convex Lens**|Double-Convex Lenses have positive focal lengths, along with two convex surfaces with equal radii|
|**Focal Point**|The point at which all radiation coming from a single direction and passing through a lens or striking a mirror converges|
|**Optical Image**|Optical image, the apparent reproduction of an object, formed by a lens or mirror system from reflected, refracted, or diffracted light waves|
|**Lens Thickness**| An ideal thin lens with two surfaces of equal curvature would have zero optical power, meaning that it would neither converge nor diverge light. A lens whose thickness is not negligible is called a thick lens|
