---
description: Процент времени обработки данных в драйвере. Эти статистические данные могут помочь определить случаи, когда драйвер ожидает другие ресурсы.
ms.assetid: 2c613349-61eb-44aa-aa7b-3161dd1fc95e
title: Структура D3DDEVINFO_D3D9INTERFACETIMINGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9INTERFACETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: dfd6303f3682e29090db41fa83b38fc67f99121e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647837"
---
# <a name="d3ddevinfo_d3d9interfacetimings-structure"></a>\_Структура D3D9INTERFACETIMINGS D3DDEVINFO

Процент времени обработки данных в драйвере. Эти статистические данные могут помочь определить случаи, когда драйвер ожидает другие ресурсы.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DDEVINFO_D3D9INTERFACETIMINGS {
  FLOAT WaitingForGPUToUseApplicationResourceTimePercent;
  FLOAT WaitingForGPUToAcceptMoreCommandsTimePercent;
  FLOAT WaitingForGPUToStayWithinLatencyTimePercent;
  FLOAT WaitingForGPUExclusiveResourceTimePercent;
  FLOAT WaitingForGPUOtherTimePercent;
} D3DDEVINFO_D3D9INTERFACETIMINGS, *LPD3DDEVINFO_D3D9INTERFACETIMINGS;
```



## <a name="members"></a>Члены

<dl> <dt>

**ваитингфоргпутаусеаппликатионресаурцетимеперцент**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Процент времени, затраченного драйвером на завершение работы GPU с заблокированным ресурсом (и [D3DLOCK \_ донотваит](d3dlock.md) не указан).

</dd> <dt>

**ваитингфоргпутоакцептморекоммандстимеперцент**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Процент времени, которое драйвер потратил на ожидание завершения обработки некоторых команд графическим процессором, прежде чем драйвер сможет отправить дополнительные сведения. Это означает, что драйверу не хватает места для отправки команд GPU.

</dd> <dt>

**ваитингфоргпутостайвисинлатенцитимеперцент**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Процент времени, затраченного драйвером на ожидание задержки GPU, чтобы сократить до трех кадров отрисовки.

Если приложение имеет ограниченный GPU, драйвер должен задержать его, пока GPU не выйдет из трех кадров. Это не позволяет приложению постановки в очередь вызовов отрисовки, которые могут значительно увеличить задержку между вводом пользователем новых данных, а также тем, когда пользователь видит результаты этого входа. Как правило, драйвер может отформатировать [**число вызовов,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) чтобы предотвратить постановку в очередь более трех кадров для подготовки к просмотру.

</dd> <dt>

**ваитингфоргпуексклусивересаурцетимеперцент**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Процент времени, затраченного драйвером на ожидание ресурса, который не может быть конвейером (выполняется параллельно). Приложение может захотеть избежать использования неконвейерного ресурса для повышения производительности.

</dd> <dt>

**ваитингфоргпуосертимеперцент**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Процент времени, затраченного драйвером на ожидание других операций обработки GPU.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Эти метрики помогают определить время ожидания драйвера и его ожидание. Высокие проценты не обязательно являются проблемой.

Эти глобальные метрики системы могут быть не реализованы. В зависимости от конкретного оборудования Эти метрики могут не поддерживать одновременно несколько запросов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
