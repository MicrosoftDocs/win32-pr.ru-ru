---
title: дкл-(SM2, SM3-PS ASM)
description: Объявите входной регистр шейдера пикселей.
ms.assetid: d6fcd94e-80d7-4e8a-8b4f-ff86c980cc38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ad61ea8d733ed01fcd2e57ba06c38e0b3efac682
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412207"
---
# <a name="dcl---sm2-sm3---ps-asm"></a>дкл-(SM2, SM3-PS ASM)

Объявите входной регистр шейдера пикселей.

## <a name="syntax"></a>Синтаксис



|                           |
|---------------------------|
| дкл \[ \_ PP \] dest \[ . Mask\] |



 

Где:

-   \[\_PP \] является необязательной частичной точностью. См. раздел [частичная точность](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md).
-   dest — это регистр назначения. Это должен быть либо [Регистр цвета ввода](dx9-graphics-reference-asm-ps-registers-input-color.md) (VN), либо [регистр текстурной координаты](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (тн).
-   \[. Mask \] — это необязательная маска записи, которая определяет, в какие компоненты регистра назначения могут быть записаны. См. раздел " [маска записи целевого регистра](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)".

## <a name="remarks"></a>Примечания



| Версии шейдеров пикселей | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| дкл                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Все инструкции дкл должны располагаться перед первой исполняемой инструкцией.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера пикселей](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




