#[UI] 레이아웃 크기(단위) 정리

 안드로이드 UI 크기를 설정하는 단위에 대해서 정리해 보려고 합니다. 
 레이아웃을 구성하는 위젯 및 폰트의 크기를 결정하는 단위는 px, in, nm, pt, dp, sp... 등
 여러가지가 있습니다. 그 여라가지 단위 중 가장 많이 사용되고 있는 dpi, px, dp(dip), sp 에 
 대해 알아보겠습니다.
 
####PX
화면에 표현되는 토트(점) 입니다. 각각의 DPI(Dot Per Inch) 마다 1인치안에 들어가는 토트(점)가 
달라지게 되고 높은 DPI 일수록 화면에 표현된 위젯이 작아지게 됩니다. 웹에서 많이 사용하는 단위로써
파편화가 심한 안드로이드 해상도에선 지양되어야 하는 단위가 아닌가 생각됩니다.

```
Px 변환식 : px = dp * (dpi / 160)
```
####DPI (Dot Per Inch)
인치당 도트를 가진 단위를 의미합니다. 예를들어 120dpi 는 1인치 안에 120개의 도트가 존재합니다.

####Dp/Dip (Density-Independent Pixels)
화면 크기를 기준으로 표현되며, 모든 사이즈의 화면에서 동일하게 표시됩니다. 160dpi 화면에 상대적입니다.
아래 표를 참고하시면 쉽게 알 수 있습니다.

1dp 기준

|DPI|LDPI(120dpi)|MDPI(160dpi)|HDPI(240dpi)|XHDPI(320dpi)|XXHDPI(480dpi)|XXXHDPI(640dpi)
| :---: | :---: | :---: | :---: | :---: | :---: | :---:
| PX|0.75px|1px|1.5px|2px|3px|4px

```
Dp 변환식 : dp = px / (density / 160)
```
####Sp (Scale-independent Pixels)
안드로이드 내에서 주로 폰트 크기에 사용됩니다. 주로라고 표현했지만, 폰트에만 사용하는게 가장 적절하다 생각됩니다.


 