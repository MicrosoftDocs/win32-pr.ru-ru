---
description: Определяет стиль перехода между значениями анимации сетки.
ms.assetid: 4416ef28-ba6b-47ca-be7d-831daad619e5
title: Перечисление D3DXTRANSITION_TYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTRANSITION_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 0ca6ef7f9dcee8e865a1cd4089aecd1bc239d5d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000350"
---
# <a name="d3dxtransition_type-enumeration"></a>\_Перечисление типов D3DXTRANSITION

Определяет стиль перехода между значениями анимации сетки.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DXTRANSITION_TYPE { 
  D3DXTRANSITION_LINEAR         = 0x000,
  D3DXTRANSITION_EASEINEASEOUT  = 0x001,
  D3DXTRANSITION_FORCE_DWORD    = 0x7fffffff
} D3DXTRANSITION_TYPE, *LPD3DXTRANSITION_TYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DXTRANSITION_LINEAR"></span><span id="d3dxtransition_linear"></span>**\_Линейная D3DXTRANSITION**
</dt> <dd>

Линейный переход между значениями.

</dd> <dt>

<span id="D3DXTRANSITION_EASEINEASEOUT"></span><span id="d3dxtransition_easeineaseout"></span>**D3DXTRANSITION \_ еасеинеасеаут**
</dt> <dd>

Простота, удобство переноса сплайна между значениями.

</dd> <dt>

<span id="D3DXTRANSITION_FORCE_DWORD"></span><span id="d3dxtransition_force_dword"></span>**D3DXTRANSITION \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Вычисление шкалы с простотой в целях упрощения вычисляется следующим образом:

<dl> Q (t) = 2 (x-y) t ³ + 3 (y-x) t ² + x  
</dl>

где пандус — это функция Q (t) со следующими свойствами:

-   Q (t) — это Кубический сплайн.
-   Q (t) выполняет интерполяцию между x и y в диапазоне от 0 до 1.
-   Q (t) является горизонтальным, когда t = 0 и t = 1.

Математически, это преобразуется в:

<dl> Q (t) = at ³ + BT ² + CT + D (и, следовательно, Q ' (t) = 3At ² + 2Bt + C)  
2a) Q (0) = x  
2b) Q (1) = y  
3a) Q "(0) = 0  
3b) Q ' (1) = 0  
</dl>

Решение для A, B, C, D:

<dl> D = x (от 2A)  
C = 0 (из 3a)  
3A + 2B = 0 (от 3b)  
A + B = y-x (от 2b до D = x)  
</dl>

Таким образом:

<dl> A = 2 (x-y), B = 3 (y-x), C = 0, D = x  
</dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




