---
description: Задает цвета вершин для сетки, а не применяет материал на каждое лицо или на сеть.
ms.assetid: 9ffd365f-11a5-420b-af5e-6a8be79a304c
title: мешвертексколорс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba55d601b29e0962c5d56e86ae052c454bf3adc7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104416557"
---
# <a name="meshvertexcolors"></a>мешвертексколорс

Задает цвета вершин для сетки, а не применяет материал на каждое лицо или на сеть.

``` syntax
template MeshVertexColors
{
    <1630B821-7842-11cf-8F52-0040333594A3>
    DWORD nVertexColors;
    array IndexColor vertexColors[nVertexColors];
} 
```

Где:

-   Нвертексколорс — число цветов. Это соответствует количеству вершин в сетке.
-   Array Индексколор Вертексколорс \[ нвертексколорс \] -массив индексированных цветов. См. [**индекседколор**](indexedcolor.md).

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Шаблоны](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



