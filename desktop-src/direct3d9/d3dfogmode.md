---
description: Определяет константы, описывающие режим тумана.
ms.assetid: cd83c914-bc1d-4f66-b5a6-7984b7ec52cd
title: Перечисление D3DFOGMODE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFOGMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 6b94992d94779932301c271ca46dc7466344b40b68c62855d4c57bfe8b780a94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791982"
---
# <a name="d3dfogmode-enumeration"></a>Перечисление D3DFOGMODE

Определяет константы, описывающие режим тумана.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DFOGMODE { 
  D3DFOG_NONE         = 0,
  D3DFOG_EXP          = 1,
  D3DFOG_EXP2         = 2,
  D3DFOG_LINEAR       = 3,
  D3DFOG_FORCE_DWORD  = 0x7fffffff
} D3DFOGMODE, *LPD3DFOGMODE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DFOG_NONE"></span><span id="d3dfog_none"></span>**D3DFOG \_ None**
</dt> <dd>

Нет воздействия на туман.

</dd> <dt>

<span id="D3DFOG_EXP"></span><span id="d3dfog_exp"></span>**D3DFOG \_ exp**
</dt> <dd>

Воздействие тумана в экспоненциальном виде усиливается в соответствии со следующей формулой.

![Формула интенсивности эффектов тумана](images/fogexp.png)

</dd> <dt>

<span id="D3DFOG_EXP2"></span><span id="d3dfog_exp2"></span>**D3DFOG \_ EXP2**
</dt> <dd>

Воздействие тумана экспоненциально усиливается квадратом расстояния в соответствии со следующей формулой.

![Формула интенсивности влияния тумана на основе квадрата расстояния](images/fogexp2.png)

</dd> <dt>

<span id="D3DFOG_LINEAR"></span><span id="d3dfog_linear"></span>**\_Линейная D3DFOG**
</dt> <dd>

Воздействие тумана усиливается линейно между начальной и конечной точками в соответствии со следующей формулой.

![Формула интенсивности эффектов тумана на основе начальной и конечной точек](images/fogliner.png)

В настоящее время поддерживается только этот режим тумана.

</dd> <dt>

<span id="D3DFOG_FORCE_DWORD"></span><span id="d3dfog_force_dword"></span>**D3DFOG \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="remarks"></a>Remarks

Значения в этом перечислимом типе используются в \_ \_ состояниях отрисовки D3DRS ФОГТАБЛЕМОДЕ и D3DRS фогвертексмоде.

Туман может считаться мерой видимости: чем меньше значение тумана, созданное уравнением тумана, тем менее видимым является объект.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
