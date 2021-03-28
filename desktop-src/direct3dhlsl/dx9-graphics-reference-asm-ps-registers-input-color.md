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
ms.openlocfilehash: 73ea16c5aa6b49bce59fe51905734344e4e1cffb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411434"
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

## <a name="remarks"></a>Примечания

Регистры цвета — это регистры только для чтения. Каждый регистр содержит значения RGBA из четырех компонентов, перебираемые из входных вершин. Они имеют меньшую точность, чем большинство регистров, но гарантированно содержат 8 бит неподписанных данных в диапазоне (0, + 1). В одной инструкции нельзя использовать больше одного.

## <a name="related-topics"></a>См. также

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

 

 




