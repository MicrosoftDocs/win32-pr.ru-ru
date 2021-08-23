---
description: Определяет координаты текстуры сетки.
ms.assetid: c87eb176-b502-49b6-bc73-401cc46e8412
title: мештекстурекурдс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5854d4a3a7f602d560845874c3af6339ff1d5e9ebbae0f79f35f4298591ee06c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628434"
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

## <a name="see-also"></a>См. также

<dl> <dt>

[Шаблоны](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



