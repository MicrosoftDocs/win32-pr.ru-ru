---
title: texdp3-PS
description: Выполняет программный продукт с тремя компонентами для данных в номере регистра текстуры и набор координат текстуры, соответствующий номеру регистра назначения.
ms.assetid: 82e02f3f-4b88-4007-b4be-0c66223d9c66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 64cc14ee66123ea3e25941579b9838977a753174
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335451"
---
# <a name="texdp3---ps"></a>texdp3-PS

Выполняет программный продукт с тремя компонентами для данных в номере регистра текстуры и набор координат текстуры, соответствующий номеру регистра назначения.

## <a name="syntax"></a>Синтаксис



| texdp3 DST, src |
|-----------------|



 

где

-   DST — это регистр назначения.
-   src является исходным регистром.

## <a name="remarks"></a>Примечания



| Версии шейдеров пикселей | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texdp3                |      | x    | x    |      |      |      |       |      |       |



 

Регистры текстур должны использовать следующую последовательность.


```
 
tex    t(n)        // Define tn as a standard 3-vector (tn must be 
                   //   defined in some way before texdp3 uses it)
texdp3 t(m), t(n)  // where m > n
                   // Perform a three-component dot product between tn and 
                   //   the texture coordinate set m. The scalar result is
                   //   replicated to all components of t(m)
```



Ниже приведены более подробные сведения о том, как выполняется элемент с точкой.

Инструкция texdp3 выполняет 3-компонентный продукт с тремя компонентами и реплицирует его во все четыре цветовых канала.

t (m)<sub>RGBA</sub> = TextureCoordinates (этап m)<sub>УВВ</sub> \* t (n)<sub>RGB</sub>

## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера пикселей](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




