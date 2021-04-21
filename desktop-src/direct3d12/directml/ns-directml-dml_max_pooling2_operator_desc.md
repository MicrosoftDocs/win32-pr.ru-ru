---
UID: NS:directml.DML_MAX_POOLING2_OPERATOR_DESC
title: DML_MAX_POOLING2_OPERATOR_DESC
description: Вычисление максимального значения для элементов в скользящем окне над входным тензорные и при необходимости возвращает индексы для выбранных максимальных значений.
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
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
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_name:
- DML_MAX_POOLING2_OPERATOR_DESC
f1_keywords:
- DML_MAX_POOLING2_OPERATOR_DESC
- directml/DML_MAX_POOLING2_OPERATOR_DESC
ms.openlocfilehash: 06e4d7eb01abab9c412238e353a73607df02b219
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803665"
---
# <a name="dml_max_pooling2_operator_desc-structure-directmlh"></a>Структура DML_MAX_POOLING2_OPERATOR_DESC (директмл. h)
Вычисление максимального значения для элементов в скользящем окне над входным тензорные и при необходимости возвращает индексы для выбранных максимальных значений.

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис
```cpp
struct DML_MAX_POOLING2_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  const DML_TENSOR_DESC *OutputIndicesTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *WindowSize;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  const UINT            *Dilations;
};
```



## <a name="members"></a>Члены

`InputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Входной тензорные *размера* `{ BatchCount, ChannelCount, Height, Width }` , если *инпуттенсор. DimensionCount* равен 4, а `{ BatchCount, ChannelCount, Depth, Height, Weight } ` Если *инпуттенсор. DimensionCount* — 5.


`OutputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Выходной тензорные, в который записываются результаты. Размеры выходных тензорные можно вычислить следующим образом.

```cpp
OutputTensor->Sizes[0] = InputTensor->Sizes[0];
OutputTensor->Sizes[1] = InputTensor->Sizes[1];

for (UINT i = 0; i < DimensionCount; ++i) {
  UINT PaddedSize = InputTensor->Sizes[i + 2] + StartPadding[i] + EndPadding[i];
  OutputTensor->Sizes[i + 2] = (PaddedSize - WindowSizes[i]) / Strides[i] + 1;
}
```


`OutputIndicesTensor`

Тип: \_ майбенулл \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Необязательный выходной тензорные индексов для входных тензорные *инпуттенсор* максимальных значений, создаваемых и хранимых в *аутпуттенсор*. Эти индексные значения отсчитываются от нуля и обрабатывают входные тензорные в виде непрерывного одномерного массива. Если несколько элементов в скользящем окне имеют одинаковое значение, то более поздние значения не учитываются, а индекс указывает на первое обнаруженное значение. *Аутпуттенсор* и *аутпутиндицестенсор* имеют одинаковый размер тензорные.


`DimensionCount`

Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)

Количество пространственных измерений входного тензорные *инпуттенсор*, которое также соответствует числу измерений скользящего окна *WindowSize*. Это значение также определяет размер массивов *stride*, *стартпаддинг* и *ендпаддинг* . Он должен иметь значение 2, если *инпуттенсор* — 4d, и 3, если это a 5D тензорные.


`Strides`

Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Шаг для измерений скользящего окна размеров, если для `{ Height, Width }` *DimensionCount* задано значение 2 или `{ Depth, Height, Width }` значение 3.


`WindowSize`

Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Размеры скользящего окна в, `{ Height, Width }` Если *DimensionCount* имеет значение 2 или `{ Depth, Height, Width }` Если значение равно 3.


`StartPadding`

Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Число элементов заполнения, применяемых к началу каждого пространственного измерения входного тензорные *инпуттенсор*. Значения находятся в параметре, `{ Height, Width }` Если *DimensionCount* имеет значение 2 или `{ Depth, Height, Width }` Если значение равно 3.


`EndPadding`

Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Количество элементов заполнения, применяемых к концу каждого пространственного измерения входного тензорные *инпуттенсор*. Значения находятся в параметре, `{ Height, Width }` Если *DimensionCount* имеет значение 2 или `{ Depth, Height, Width }` Если значение равно 3.


`Dilations`

Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Значения для каждого пространственного измерения входного тензорные *инпуттенсор* , по которому выбирается элемент в скользящем окне для каждого элемента этого значения. Значения находятся в параметре, `{ Height, Width }` Если *DimensionCount* имеет значение 2 или `{ Depth, Height, Width }` Если значение равно 3.


## <a name="remarks"></a>Комментарии
**DML_MAX_POOLING2_OPERATOR_DESC** заменяет более раннюю версию [DML_MAX_POOLING_OPERATOR1_DESC](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) с дополнительным массивом констант *дилатионс*. Две версии эквивалентны, если для *дилатионс* задано значение `{ 1,1 }` для входных данных 4d или `{ 1,1,1 }` для входных функций 5D.

## <a name="availability"></a>Доступность
Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Ограничения тензорные
* *Инпуттенсор*, *аутпутиндицестенсор* и *аутпуттенсор* должны иметь одинаковые *DimensionCount*.
* *Инпуттенсор* и *аутпуттенсор* должны иметь одинаковый *тип данных*.

## <a name="tensor-support"></a>Поддержка тензорные
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 и выше
| Тензорные | Вид | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | -------------------------- | -------------------- |
| инпуттенсор | Входные данные | от 4 до 5 | FLOAT32, FLOAT16, INT8, UINT8 |
| аутпуттенсор | Выходные данные | от 4 до 5 | FLOAT32, FLOAT16, INT8, UINT8 |
| аутпутиндицестенсор | Необязательный вывод | от 4 до 5 | ЗНАЧЕНИЕМ |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 и выше
| Тензорные | Вид | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | -------------------------- | -------------------- |
| инпуттенсор | Входные данные | от 4 до 5 | FLOAT32, FLOAT16 |
| аутпуттенсор | Выходные данные | от 4 до 5 | FLOAT32, FLOAT16 |
| аутпутиндицестенсор | Необязательный вывод | от 4 до 5 | ЗНАЧЕНИЕМ |


## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Минимальная версия клиента** | Windows 10, версия 2004 (10,0; Сборка 19041) |
| **Минимальная версия сервера** | Windows Server, версия 2004 (10,0; Сборка 19041) |
| **Header** | директмл. h |