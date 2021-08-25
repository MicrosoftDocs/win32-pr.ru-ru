---
description: Сообщает количество треугольников, которые были обработаны и обрезаны при обработке вершин программного обеспечения среды выполнения.
ms.assetid: 280fb5c3-3048-4208-b352-0548b13ecba2
title: Структура D3DDEVINFO_D3DVERTEXSTATS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3DVERTEXSTATS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 80edbdcdeea5df6ff020c0c4cc2179db5152c15cc4965efe6580db7fd7bdcc48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894534"
---
# <a name="d3ddevinfo_d3dvertexstats-structure"></a>\_Структура D3DVERTEXSTATS D3DDEVINFO

Сообщает количество треугольников, которые были обработаны и обрезаны при обработке вершин программного обеспечения среды выполнения.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DDEVINFO_D3DVERTEXSTATS {
  DWORD NumRenderedTriangles;
  DWORD NumExtraClippingTriangles;
} D3DDEVINFO_D3DVERTEXSTATS, *LPD3DDEVINFO_D3DVERTEXSTATS;
```



## <a name="members"></a>Члены

<dl> <dt>

**нумрендередтрианглес**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Общее число треугольников, не обрезанных в этом кадре.

</dd> <dt>

**нумекстраклиппингтрианглес**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Число новых треугольников, созданных при обрезке.

</dd> </dl>

## <a name="remarks"></a>Remarks

Используйте среду выполнения отладки и обработку вершин программного обеспечения, чтобы получить число необрезанных и обрезанных примитивов для конкретной сцены. Примитивы обычно обрезаются на основе диапазона защиты (если таковой имеется). Полоса отсечения задается с такими параметрами, как Гуардбандлефт в [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
