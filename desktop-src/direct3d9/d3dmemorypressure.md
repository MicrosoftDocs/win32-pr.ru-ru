---
description: Содержит данные для отчетов о нехватке памяти.
ms.assetid: bdf65d35-281f-4795-a2c1-0d4e91bfa7bc
title: Структура D3DMEMORYPRESSURE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMEMORYPRESSURE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5917d1e61817f401106ae14aa5a0f98cd75b0d42
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713755"
---
# <a name="d3dmemorypressure-structure-d3d9typesh"></a>Структура D3DMEMORYPRESSURE (D3d9types. h)

Содержит данные для отчетов о нехватке памяти.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _D3DMEMORYPRESSURE {
  UINT64 BytesEvictedFromProcess;
  UINT64 SizeOfInefficientAllocation;
  DWORD  LevelOfEfficiency;
} D3DMEMORYPRESSURE;
```



## <a name="members"></a>Члены

<dl> <dt>

**битесевиктедфромпроцесс**
</dt> <dd>

Тип: **[ **UINT64**](../winprog/windows-data-types.md)**

</dd> <dd>

Число байтов, которые были исключены процессом во время выполнения запроса.

</dd> <dt>

**сизеофинеффиЦиенталлокатион**
</dt> <dd>

Тип: **[ **UINT64**](../winprog/windows-data-types.md)**

</dd> <dd>

Общее число байтов, помещенных в неоптимальные сегменты памяти из-за недостаточного места в предпочтительных сегментах памяти.

</dd> <dt>

**левелофеффиЦиенци**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Общая эффективность выделения памяти, помещенных в неоптимальную память. Значение выражается в процентах. Например, значение 95 указывает, что выделения, помещаемые в непредпочтительные сегменты памяти, имеют эффективность 95%. Это число не должно считаться точным измерением.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
