---
title: dcl_semantics (SM3-PS ASM)
description: Объявите ассоциацию между выходным шейдером вершин и входными данными шейдера пикселей.
ms.assetid: 4f4dc6fe-0efa-4d84-aefd-583e90ab9a61
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 91a57ec2eabbef2cd62fec8fa95fbf9d2da47a5bfcdb339bf30ed8da5b11c9ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792933"
---
# <a name="dcl_semantics-sm3---ps-asm"></a>\_семантика дкл (SM3-PS ASM)

Объявите ассоциацию между выходным шейдером вершин и входными данными шейдера пикселей.

## <a name="syntax"></a>Синтаксис

\_семантика дкл \[ \_ центроид \] DST \[ . Write \_ Mask\]



 

Где:

-   \_семантика: определяет предполагаемое использование данных и может быть любым из значений в [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (без \_ префикса D3DDECLUSAGE). Кроме того, целочисленный индекс может быть добавлен к семантике для различения параметров, использующих подобную семантику.
-   \[\_[Центроид](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md) \] является необязательным модификатором инструкции. Он поддерживается в \_ инструкциях по использованию дкл, которые объявляют входные регистры и инструкции по поиску текстур. К центроид добавляется без пробела.
-   DST: регистр назначения. См. раздел [ \_ \_ регистры PS 3 0](dx9-graphics-reference-asm-ps-registers-ps-3-0.md).
-   \_маска записи. один и тот же выходной регистр может быть объявлен несколько раз, каждый раз с уникальной маской записи (так что разные семантики могут применяться к отдельным компонентам). Однако одна и та же семантика не может использоваться несколько раз в объявлении. Это означает, что векторы должны состоять из четырех компонентов или меньше и не могут переключаться между четырьмя границами регистров (отдельные выходные регистры). При \_ использовании семантики псизе она должна иметь полную маску записи, так как она считается скалярной. При \_ использовании семантики расположения она должна иметь полную маску записи, так как необходимо записать все четыре компонента.

## <a name="remarks"></a>Remarks



| Версии шейдеров пикселей | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| \_Использование дкл            |      |      |      |      |      |      |       | x    | x     |



 

Все \_ инструкции по использованию дкл должны располагаться перед первой исполняемой инструкцией.

## <a name="declaration-examples"></a>Примеры объявлений


```
ps_3_0

; Declaring inputs
dcl_normal      v0.xyz
dcl_blendweight v0.w ; Must be same reg# as normal, matching vshader packing
dcl_texcoord1   v1.y ; Mask can be any subset of mask from vshader semantic
dcl_texcoord0   v1.zw; Has to be same reg# as texcoord1, to match vshader

; Declaring samplers
dcl_2d s0
dcl_2d s1

def c0, 0, 0, 0, 0

mov r0.x, v1.y ; texcoord1
mov r0.y, c0
texld r0, r0, s0

texld r1, v1.zw, s1
...
(output regs in ps_3_0 are same as ps_2_0: oC0-oC3, oDepth)
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Инструкции шейдера пикселей](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[Пример сглаживания](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)
</dt> </dl>

 

 
