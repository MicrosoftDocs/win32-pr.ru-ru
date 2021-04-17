---
description: Описывает состояние растрового изображения.
ms.assetid: f7b5b714-8fc8-47b8-adec-1089b8d07081
title: Структура D3DRASTER_STATUS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRASTER_STATUS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e77ab0e6ee164eadae862ed03df5652c21ba7040
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703832"
---
# <a name="d3draster_status-structure"></a>\_Структура состояния D3DRASTER

Описывает состояние растрового изображения.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DRASTER_STATUS {
  BOOL InVBlank;
  UINT ScanLine;
} D3DRASTER_STATUS, *LPD3DRASTER_STATUS;
```



## <a name="members"></a>Члены

<dl> <dt>

**инвбланк**
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

</dd> <dd>

**Значение true** , если точечный символ находится в вертикальной пустой точке. **Значение false** , если точечный символ не находится в вертикальной пустой точке.

</dd> <dt>

**сканлине**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Если Инвбланк имеет значение **false**, то это значение представляет собой целое число, приблизительно соответствующее текущей строке сканирования, закрашенной растровым. Строки сканирования нумеруются так же, как координаты поверхности Direct3D: 0 — верхняя часть основной поверхности, расширение до значения (высота поверхности-1) в нижней части экрана.

Если Инвбланк имеет значение **true**, то это значение устанавливается равным нулю и может быть пропущено.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**жетрастерстатус**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrasterstatus)
</dt> </dl>

 

 
