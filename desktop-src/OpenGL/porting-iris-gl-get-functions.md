---
title: Перенос функций получения для ДИАФРАГМы в ГК
description: 'IRI GL \ 0034; Get \ 0034; функции принимают следующую форму:'
ms.assetid: 5bd6aa13-b41d-4f89-91dc-cc47481ac7b7
keywords:
- Перенос GL в ГК, получение функций
- Перенос из IRI GL, получение функций
- перенос в OpenGL из IRI GL, получение функций
- Перенос по стандарту OpenGL из IRI GL, получение функций
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 594b12bb1738846b98d33137dd8b623f0405ec40
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661602"
---
# <a name="porting-iris-gl-get-functions"></a>Перенос функций получения для ДИАФРАГМы в ГК

Функции "Get" в форме IRI имеют следующий вид:

``` syntax
int getthing();
```

и

``` syntax
int getthings( int *a, int *b);
```

Код в ГК для ДИАФРАГМы, вероятно, включает вызовы функций Get, которые выглядят примерно так:

``` syntax
thing = getthing(); 
if (getthing() == THING) { /* some stuff here */ } 
getthings (&a, &b);
```

В OpenGL используется один из следующих четырех типов функций [**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) вместо эквивалентных функций IRI GL.

-   **глжетбулеанв**
-   **глжетинтежерв**
-   **глжетфлоатв**
-   **глжетдаублев**

Функции имеют следующий синтаксис:

``` syntax
glGet<Datatype>v( value, *data );
```

где *значение* имеет тип **гленум** , а данные имеют тип **глдататипе**. При вызове **глжет** и возврате типа, отличного от ожидаемого типа, тип преобразуется соответствующим образом. Полный список параметров **глжет** см. в разделе [**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md).

 

 




