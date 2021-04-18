---
title: Элемент группы VML
description: Элемент группы VML
ms.assetid: 536c2380-2583-4fe8-a92e-c539de209a70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33c128fddb5f070c9dbb6bbbd92c172cd58f5bce
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413120"
---
# <a name="vml-group-element"></a>Элемент группы VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет группу, которую можно использовать для получения фигур.

Этот элемент поддерживает те же атрибуты, что и фигура, за исключением следующих:

-   **служеб**
-   **type**
-   **разница**
-   **путь**
-   **spid**
-   **данной**
-   **чромакэй**
-   **заштриховывать**
-   **строкеколор**
-   **строкевеигхт**
-   **указал**
-   **FillColor**
-   **спт**
-   **рулеинитиатор**
-   **рулепрокси**
-   **коннектортипе**
-   **бвмоде**
-   **бвпуре**
-   **бвнормал**
-   **форцедаш**
-   **олеикон**
-   **преферрелативе**
-   **OLEDB**

С **группой** можно использовать только следующие подэлементы.

-   **Группа**
-   **шапетипе**
-   **Фигурная**
-   **Блокировка**

**Пример**

В следующем примере показано, как определить группу.


```HTML
<!-- Include the VML behavior -->
<style>v\: * { behavior: url(#default#VML);display:inline-block }</style>

<!-- Declare the VML namespace -->
<xml:namespace ns="urn:schemas-microsoft-com:vml" prefix="v"/>

<v:group id="group1" style="left:10px;top:10px;width:50px;height:50px;"
  coordorigin="0,0" coordsize="6000,6000">

<v:shape id="_x0000_s2051"
  style='position:relative;left:234.75pt;top:208.875pt;width:235.25pt;height:128.875pt'
  coordsize="3765,2060"
  path="m1285,251l1126,469,580,1009,,1285,25,1412,93,1547,194,1673,1017,2026,2312,2060,3209,1756,3765,1388,3278,680,3059,319,2976,,1285,251,1285,251xe"
  fillcolor="#bcbcd6" stroked="f">
  <v:path arrowok="t"/>
 </v:shape>

 <v:shape id="_x0000_s2052" style='position:relative;left:314.625pt;
  top:140.5pt;width:104pt;height:102pt' coordsize="1663,1633"
  path="m0,1355l177,1498,353,1582,840,1633,1378,1498,1663,1295,1545,456,1260,10,1025,,656,260,253,874,,1355,,1355xe"
  fillcolor="#99ebff" stroked="f">
  <v:path arrowok="t"/>
 </v:shape>

</v:group>
```





 

 