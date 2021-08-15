---
description: Определяет базовый цвет материала, который можно применить к полной сетке или к отдельным граням сетки. Сила — это отражающий показатель материала.
ms.assetid: vs|directx_sdk|~\material.htm
title: Материал
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d4dcb1cef7597ff7c02d16f1db311287511166c9259c89a0ea60a0c49fb7bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798971"
---
# <a name="material"></a>Материал

Определяет базовый цвет материала, который можно применить к полной сетке или к отдельным граням сетки. Сила — это отражающий показатель материала.

``` syntax
template Material
{
    < 3D82AB4D-62DA-11CF-AB39-0020AF71E433 >
    ColorRGBA faceColor;
    FLOAT power;
    ColorRGB specularColor;
    ColorRGB emissiveColor;
    [...]
} 
```

Где:

-   цвет Фацеколор-Face. Шаблон Колорргба. См. [**колорргба**](colorrgba.md).
-   экспонента отраженного цвета материала для Power Material.
-   отражающий цвет Спекуларколор-Material. Шаблон Колорргб. См. [**колорргб**](colorrgb.md).
-   цвет Емиссивеколор-Material эмиссионный. Шаблон Колорргб. См. [**колорргб**](colorrgb.md).

> [!Note]  
> Для окружающего цвета требуется альфа-компонент.

 

[**Текстурефиленаме**](texturefilename.md) — это необязательный объект данных. Если этот объект отсутствует, поверхность не текстурна.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Шаблоны](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



