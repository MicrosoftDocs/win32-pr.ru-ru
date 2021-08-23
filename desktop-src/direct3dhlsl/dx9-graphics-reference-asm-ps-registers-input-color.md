---
title: Регистр цвета ввода
description: Входной регистр шейдера пикселей, содержащий цвет вершины.
ms.assetid: d2e21f87-000e-410a-aaba-172000ed1c5f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fcabc6dcf5043c23be252fe6ac25c99da505e33b7c670c95ee5672b50ddb74bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744634"
---
# <a name="input-color-register"></a>Регистр цвета ввода

Входной регистр шейдера пикселей, содержащий цвет вершины.

## <a name="syntax"></a>Синтаксис


```
dcl v#.writeMask
```



где:

-   [дкл-(SM2, SM3-PS ASM)](dcl---ps.md) является инструкцией по объявлению регистра.
-   v является входным регистром и \# является номером регистра. Количество допустимых регистров определяется версией шейдера.
-   Вритемаск определяет, какие компоненты записываются (до четырех). Допустимые компоненты: (x, y, z, w) или (r, g, b, a).

## <a name="remarks"></a>Remarks

Регистры цвета — это регистры только для чтения. Каждый регистр содержит значения RGBA из четырех компонентов, перебираемые из входных вершин. Они имеют меньшую точность, чем большинство регистров, но гарантированно содержат 8 бит неподписанных данных в диапазоне (0, + 1). В одной инструкции нельзя использовать больше одного.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Регистры](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[реестр PS 1 1 PS 1 2 PS 1 3 PS 1 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 4 регистры](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[\_ \_ регистры PS 2 0](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[\_ \_ регистры PS 2 x](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[\_ \_ регистры PS 3 0](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




