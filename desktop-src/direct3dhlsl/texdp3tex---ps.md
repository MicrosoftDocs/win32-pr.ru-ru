---
title: texdp3tex-PS
description: Выполняет программный продукт с тремя компонентами и использует результат для поиска по одномерной текстуре.
ms.assetid: vs|directx_sdk|~\texdp3tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 91014b52b04417bbb23e76988beeb0bd4c473bd1e1d116433a8fd1dbf09a47ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118788040"
---
# <a name="texdp3tex---ps"></a>texdp3tex-PS

Выполняет программный продукт с тремя компонентами и использует результат для поиска по одномерной текстуре.

## <a name="syntax"></a>Синтаксис



| texdp3tex DST, src |
|--------------------|



 

where

-   DST — это регистр назначения.
-   src является исходным регистром.

## <a name="remarks"></a>Remarks



| Версии шейдеров пикселей | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texdp3tex             |      | x    | x    |      |      |      |       |      |       |



 

Регистры текстур должны использовать следующую последовательность.


```
 
tex       t(n)        // Define tn as a standard 3-vector (tn must be 
                      // defined in some way before texdp3tex uses it)
texdp3tex t(m), t(n)  // where m > n                 
                      // Perform a three-component dot product between t(n) and 
                      // the texture coordinate set m. Use the scalar result to
                      // do a 1D texture lookup at texturestage m and place
                      // the result in t(m)
```



Ниже приведены более подробные сведения о том, как выполняется поиск с помощью точки и текстуры.

Инструкция texdp3tex выполняет 3-компонентный продукт.

u "= TextureCoordinates (этап m)<sub>УВВ</sub> \* t (n)<sub>RGB</sub>

Результат используется для выборки текстуры на этапе текстуры m с помощью одномерного поиска.

t (m)<sub>RGBA</sub> = текстуресампле (этап m)<sub>RGBA</sub> с использованием (u, 0, 0) в качестве координат

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Инструкции шейдера пикселей](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




