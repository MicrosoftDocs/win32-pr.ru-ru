---
description: Процент времени обработки данных в конвейере.
ms.assetid: eb9dec27-2e45-4897-92af-8415c8fa08d4
title: Структура D3DDEVINFO_D3D9PIPELINETIMINGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9PIPELINETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 4d938fd2e1ca0f52d2ea7787f54b430a84907ad5f04f066bc90f0867825745a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676744"
---
# <a name="d3ddevinfo_d3d9pipelinetimings-structure"></a>\_Структура D3D9PIPELINETIMINGS D3DDEVINFO

Процент времени обработки данных в конвейере.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DDEVINFO_D3D9PIPELINETIMINGS {
  FLOAT VertexProcessingTimePercent;
  FLOAT PixelProcessingTimePercent;
  FLOAT OtherGPUProcessingTimePercent;
  FLOAT GPUIdleTimePercent;
} D3DDEVINFO_D3D9PIPELINETIMINGS, *LPD3DDEVINFO_D3D9PIPELINETIMINGS;
```



## <a name="members"></a>Члены

<dl> <dt>

**вертекспроцессингтимеперцент**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Процент времени, затраченного на выполнение шейдеров вершин.

</dd> <dt>

**пикселпроцессингтимеперцент**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Процент времени, затраченного на выполнение шейдеров пикселей.

</dd> <dt>

**осергпупроцессингтимеперцент**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Процент времени, затраченного на выполнение другой обработки.

</dd> <dt>

**гпуидлетимеперцент**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Процент времени, при котором ничего не обрабатывается.

</dd> </dl>

## <a name="remarks"></a>Remarks

Для оптимальной производительности рекомендуется использовать сбалансированную нагрузку.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
