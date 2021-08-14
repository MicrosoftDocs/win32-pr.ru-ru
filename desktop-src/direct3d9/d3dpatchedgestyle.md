---
description: Определяет, является ли текущий режим тесселяции дискретным или непрерывным.
ms.assetid: d8055a25-6a8e-4018-a993-762f6f0e0cd3
title: Перечисление D3DPATCHEDGESTYLE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPATCHEDGESTYLE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 717139a33e260aa29bc8d0e244fa49b3cb324c5249614f513faf0624ccf21841
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987244"
---
# <a name="d3dpatchedgestyle-enumeration"></a>Перечисление D3DPATCHEDGESTYLE

Определяет, является ли текущий режим тесселяции дискретным или непрерывным.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DPATCHEDGESTYLE { 
  D3DPATCHEDGE_DISCRETE     = 0,
  D3DPATCHEDGE_CONTINUOUS   = 1,
  D3DPATCHEDGE_FORCE_DWORD  = 0x7fffffff
} D3DPATCHEDGESTYLE, *LPD3DPATCHEDGESTYLE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DPATCHEDGE_DISCRETE"></span><span id="d3dpatchedge_discrete"></span>**\_Дискретный D3DPATCHEDGE**
</dt> <dd>

Дискретный стиль ребра. В дискретном режиме можно указать тесселяцию с плавающей запятой, но оно будет усечено до целых чисел.

</dd> <dt>

<span id="D3DPATCHEDGE_CONTINUOUS"></span><span id="d3dpatchedge_continuous"></span>**D3DPATCHEDGE \_ непрерывно**
</dt> <dd>

Стиль непрерывного ребра. В непрерывном режиме тесселяция задается как значения float, которые могут быть плавно изменяться для сокращения числа "выталкивания".

</dd> <dt>

<span id="D3DPATCHEDGE_FORCE_DWORD"></span><span id="d3dpatchedge_force_dword"></span>**D3DPATCHEDGE \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="remarks"></a>Remarks

Обратите внимание, что непрерывная тесселяция создает совершенно другой шаблон тесселяции из дискретного для тех же значений тесселяции (это более очевидно в режиме каркаса). Таким образом, 4,0 непрерывная не совпадает с 4 дискретной.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




