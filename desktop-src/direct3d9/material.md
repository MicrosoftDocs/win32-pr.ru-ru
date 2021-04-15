---
description: Определяет базовый цвет материала, который можно применить к полной сетке или к отдельным граням сетки. Сила — это отражающий показатель материала.
ms.assetid: vs|directx_sdk|~\material.htm
title: Материал
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54c13d201152350a8a61950bb609f73cbdb2a3aa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494280"
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

 

 



