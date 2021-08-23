---
description: Задает цвета вершин для сетки, а не применяет материал на каждое лицо или на сеть.
ms.assetid: 9ffd365f-11a5-420b-af5e-6a8be79a304c
title: мешвертексколорс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 035f8d51ae692b0edd20f7b06b5ab8e756ff73d9cd8265d64700ce5374f9a15b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628334"
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

## <a name="see-also"></a>См. также

<dl> <dt>

[Шаблоны](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



