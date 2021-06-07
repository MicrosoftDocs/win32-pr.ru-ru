---
UID: NS:directml.DML_NONZERO_COORDINATES_OPERATOR_DESC
title: DML_NONZERO_COORDINATES_OPERATOR_DESC
description: Выполняет вычисление N-мерных координат всех ненулевых элементов входного тензорные.
helpviewer_keywords:
- DML_NONZERO_COORDINATES_OPERATOR_DESC
- DML_NONZERO_COORDINATES_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_NONZERO_COORDINATES_OPERATOR_DESC, DML_NONZERO_COORDINATES_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
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
- DML_NONZERO_COORDINATES_OPERATOR_DESC
- directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
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
- DML_NONZERO_COORDINATES_OPERATOR_DESC
ms.openlocfilehash: 39463ba57bc90b35d5ac5dc7fc43993169137221
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417533"
---
# <a name="dml_nonzero_coordinates_operator_desc-structure-directmlh"></a>Структура DML_NONZERO_COORDINATES_OPERATOR_DESC (директмл. h)

Выполняет вычисление N-мерных координат всех ненулевых элементов входного тензорные.

Этот оператор создает MxN матрицу значений, где каждая строка M содержит N-мерный координату ненулевого значения из входных данных. При использовании входных данных **FLOAT32** или **FLOAT16** отрицательные и положительные 0 (0,0 f и-0.0 f) обрабатываются как нули в целях данного оператора.

Оператор требует, чтобы размер *аутпуткурдинатестенсор* был достаточно большим, чтобы соответствовать наихудшему сценарию, где каждый элемент входных данных не равен нулю. Этот оператор возвращает количество ненулевых элементов через *аутпуткаунттенсор*, которые вызывающие объекты могут проверить, чтобы определить количество координат, записанных в *аутпуткурдинатестенсор*.

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис

```cpp
struct DML_NONZERO_COORDINATES_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputCountTensor;
  const DML_TENSOR_DESC* OutputCoordinatesTensor;
};
```

## <a name="members"></a>Участники

`InputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Входной тензорные.

`OutputCountTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Выходной тензорные, содержащий количество ненулевых элементов во входном тензорные. Этот тензорные должен быть скалярным, то &mdash; есть размеры этого тензорные должны быть 1. Тип этого тензорные должен быть **UINT32**.

`OutputCoordinatesTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Выходной тензорные, содержащий N-мерных координат элементов ввода, которые не равны нулю. 

Этот тензорные должен иметь *размеры* `{1,1,M,N}` (если значение *DimensionCount* равно 4) или `{1,1,1,M,N}` (если *DimensionCount* равно 5), где M — общее число элементов в *инпуттенсор*, а N — больше или равно *эффективному рангу* *инпуттенсор*, вплоть до *DimensionCount* входного значения.

Эффективный ранг тензорные определяется *DimensionCountом* того, что тензорные за исключением ведущих измерений размера 1. Например, тензорные с размером `{1,2,3,4}` имеет эффективный ранг 3, как и тензорные с размерами `{1,1,5,5,5}` . Тензорные с размером `{1,1,1,1}` имеет действующий ранг 0.

Рассмотрим *инпуттенсор* с *размерами* `{1,1,12,5}` . Этот входной тензорные содержит 60 элементов и имеет эффективный ранг 2. В этом примере все допустимые размеры *аутпуткурдинатестенсор* имеют форму `{1,1,60,N}` , где N >= 2, но не больше, чем *DimensionCount* (4 в этом примере).

Координаты, записанные в этот тензорные, гарантированно упорядочиваются по возрастанию индексов элементов. Например, если входные тензорные имеют 3 ненулевые значения в координатах {1,0} , {1,2} , и {0,5} , значения, записанные *в аутпуткурдинатестенсор* , будут иметь значение `[[0,5], [1,0], [1,2]]` .

Хотя для этого тензорные требуется, чтобы измерение M было равно числу элементов во входном тензорные, этот оператор записывает в этот тензорные не более Аутпуткаунт элементов. Аутпуткаунт возвращается через скалярный *аутпуткаунттенсор*.

> [!NOTE]
> Оставшиеся элементы этого тензорные за пределами Аутпуткаунт не определены после завершения этого оператора. Не следует полагаться на значения этих элементов.

## <a name="example"></a>Пример

```
InputTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
[[1.0f,  0.0f, 0.0f,  2.0f],
 [-0.0f, 3.5f, 0.0f, -5.2f]]

OutputCountTensor: (Sizes:{1,1,1,1}, DataType:UINT32)
[4]

OutputCoordinatesTensor: (Sizes:{1,1,8,3}, DataType:UINT32)
[[0, 0, 0],
 [0, 0, 3],
 [0, 1, 1],
 [0, 1, 3],
 [0, 0, 0], // 
 [0, 0, 0], // Values in rows >= OutputCountTensor (4 in
 [0, 0, 0], // this case) are left undefined
 [0, 0, 0]] // 
```

## <a name="availability"></a>Доступность
Этот оператор появился в `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Ограничения тензорные
*Инпуттенсор*, *аутпуткурдинатестенсор* и `OutputCountTensor` должны иметь одинаковый *DimensionCount*.

## <a name="tensor-support"></a>Поддержка тензорные
| Тензорные | Вид | Измерения | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| инпуттенсор | Входные данные | {[D0], D1, D2, D3, D4} | от 4 до 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| аутпуткаунттенсор | Выходные данные | {[1], 1, 1, 1, 1} | от 4 до 5 | ЗНАЧЕНИЕМ |
| аутпуткурдинатестенсор | Выходные данные | {[1], 1, 1, M, N} | от 4 до 5 | ЗНАЧЕНИЕМ |

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |