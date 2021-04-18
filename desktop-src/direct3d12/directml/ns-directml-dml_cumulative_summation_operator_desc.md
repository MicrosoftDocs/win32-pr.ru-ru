---
UID: NS:directml.DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
title: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
description: Суммирует элементы тензорные вдоль оси, записывая выполняющийся счетчик суммы в выходном тензорные.
helpviewer_keywords:
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure
- direct3d12.dml_cumulative_summation_operator_desc
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC, DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure, direct3d12.dml_cumulative_summation_operator_desc, directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.openlocfilehash: 955e70a8cfbb57995d77d73567238d082b96999b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719982"
---
# <a name="dml_cumulative_summation_operator_desc-structure-directmlh"></a>Структура DML_CUMULATIVE_SUMMATION_OPERATOR_DESC (директмл. h)

Суммирует элементы тензорные вдоль оси, записывая выполняющийся счетчик суммы в выходном тензорные.

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис
```cpp
struct DML_CUMULATIVE_SUMMATION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
  DML_AXIS_DIRECTION    AxisDirection;
  BOOL                  HasExclusiveSum;
};
```



## <a name="members"></a>Члены

`InputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Входной тензорные, содержащий элементы для суммирования.


`OutputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Выходной тензорные для записи итоговых суммарных сумм в. Этот тензорные должен иметь те же размеры и тип данных, что и *инпуттенсор*.


`Axis`

Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)

Индекс измерения для суммирования элементов. Это значение должно быть меньше значения параметра *DimensionCount* *инпуттенсор*.


`AxisDirection`

Тип: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**

Одно из значений перечисления [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) . Если задано значение **DML_AXIS_DIRECTION_INCREASING**, то суммирование выполняется путем просмотра тензорные вдоль указанной оси по возрастанию индекса элементов. Если задано значение **DML_AXIS_DIRECTION_DECREASING**, обратное значение равно true, а суммирование выполняется путем обхода элементов по убыванию индекса.


`HasExclusiveSum`




## <a name="remarks"></a>Комментарии
Этот оператор поддерживает выполнение на месте, что означает, что *аутпуттенсор* может использовать псевдоним *инпуттенсор* во время привязки.

## <a name="availability"></a>Доступность
Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Ограничения тензорные
*Инпуттенсор* и *аутпуттенсор* должны иметь одинаковые типы *данных* и *размеры*.

## <a name="tensor-support"></a>Поддержка тензорные
| Тензорные | Вид | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | -------------------------- | -------------------- |
| инпуттенсор | Входные данные | 4 | FLOAT32, FLOAT16, UINT32, UINT16 |
| аутпуттенсор | Выходные данные | 4 | FLOAT32, FLOAT16, UINT32, UINT16 |


## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |