---
description: Определяет координаты текстуры сетки.
ms.assetid: c87eb176-b502-49b6-bc73-401cc46e8412
title: мештекстурекурдс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 974ec31f4358578277cfac46dc014f34752df46a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805303"
---
# <a name="meshtexturecoords"></a>мештекстурекурдс

Определяет координаты текстуры сетки.

``` syntax
template MeshTextureCoords
{
    < F6F23F40-7686-11cf-8F52-0040333594A3 >
    DWORD nTextureCoords;
    array Coords2d textureCoords[nTextureCoords] ;
} 
```

Где:

-   Нтекстурекурдс — число координат текстуры.
-   Array Coords2d Текстурекурдс \[ нтекстурекурдс \] — Массив координат двухмерной текстуры. См. [**Coords2d**](coords2d.md).

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Шаблоны](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



