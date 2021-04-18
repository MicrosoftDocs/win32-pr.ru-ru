---
UID: NS:directml.DML_RESAMPLE1_OPERATOR_DESC
title: DML_RESAMPLE1_OPERATOR_DESC
description: Ресамплинг элементов из источника в целевой тензорные с использованием коэффициентов масштабирования для расчета размера целевого тензорные. Можно использовать линейный или ближайший к соседним режим интерполяции.
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
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
- DML_RESAMPLE1_OPERATOR_DESC
f1_keywords:
- DML_RESAMPLE1_OPERATOR_DESC
- directml/DML_RESAMPLE1_OPERATOR_DESC
ms.openlocfilehash: 669e828c4d8376e081ef6638aba4a13d517afd88
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719962"
---
# <a name="dml_resample1_operator_desc-structure-directmlh"></a>Структура DML_RESAMPLE1_OPERATOR_DESC (директмл. h)
Ресамплинг элементов из источника в целевой тензорные с использованием коэффициентов масштабирования для расчета размера целевого тензорные. Можно использовать линейный или ближайший к соседним режим интерполяции. Оператор поддерживает интерполяцию по нескольким измерениям, а не только к 2D. Таким образом, можно иметь одинаковый пространственный размер, но выполнять интерполяцию по каналам или по пакетам. Связь между входными и выходными координатами приведена ниже.

`OutputTensorX = (InputTensorX + InputPixelOffset) * Scale + OutputPixelOffset`

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис
```cpp
struct DML_RESAMPLE1_OPERATOR_DESC {
  const DML_TENSOR_DESC  *InputTensor;
  const DML_TENSOR_DESC  *OutputTensor;
  DML_INTERPOLATION_MODE InterpolationMode;
  UINT                   DimensionCount;
  const FLOAT            *Scales;
  const FLOAT            *InputPixelOffsets;
  const FLOAT            *OutputPixelOffsets;
};
```



## <a name="members"></a>Члены

`InputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Тензорные, содержащий входные данные.


`OutputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Тензорные для записи выходных данных.


`InterpolationMode`

Тип: [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)

Это поле определяет тип интерполяции, используемый для выбора выходных пикселей.

- **DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR**. Использует *ближайший алгоритм соседей* , который выбирает элемент ввода, ближайший к соответствующему центру пикселей для каждого выходного элемента.

- **DML_INTERPOLATION_MODE_LINEAR**. Использует алгоритм *куадрилинеар* , который вычисляет элемент Output, выполняя взвешенное среднее по 2 ближайшим соседним входным элементам на измерение. Так как все 4 измерения можно повторно вычислить, взвешенное среднее вычисляется по общему количеству 16 входных элементов для каждого выходного элемента.


`DimensionCount`

Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)

Количество значений в массивах, которые *масштабируются*, *инпутпикселоффсетс* и *аутпутпикселоффсетс* указывают на. Это значение должно соответствовать числу измерений *инпуттенсор* и *аутпуттенсор*, который должен быть равен 4.


`Scales`

Тип: \_ \_ Размер поля \_ (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***

Шкалы, применяемые при переборке входных данных, где масштабируется > 1. Увеличение масштаба изображения и масштабирование < 1 масштабирование изображения для этого измерения. Обратите внимание, что масштабы не обязательно должны быть в точности `OutputSize / InputSize` . Если входные данные после масштабирования больше, чем у границ выходных данных, мы обрезать его до размера выходных данных. С другой стороны, если входные данные после масштабирования меньше, чем граница выходных данных, края выходных данных будут обработаны.


`InputPixelOffsets`

Тип: \_ \_ Размер поля \_ (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***

Смещение, применяемое к входным точкам до повторной выборки. Если это значение равно `0` , то вместо его центра используется верхний левый угол пикселя, который обычно не дает ожидаемого результата. Для повторной выборки изображения с помощью центра пикселов и для получения того же поведения, что и [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), это значение должно быть `0.5` .


`OutputPixelOffsets`

Тип: \_ \_ Размер поля \_ (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***

Смещение, применяемое к выходным пикселям после перевыборки. Если это значение равно `0` , то вместо его центра используется верхний левый угол пикселя, который обычно не дает ожидаемого результата. Для повторной выборки изображения с помощью центра пикселов и для получения того же поведения, что и [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), это значение должно быть `-0.5` .


## <a name="remarks"></a>Комментарии
Если для *инпутпикселоффсетс* задано значение 0,5, а для *аутпутпикселоффсетс* задано значение-0,5, этот оператор эквивалентен [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc).

## <a name="availability"></a>Доступность
Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Ограничения тензорные
*Инпуттенсор* и *аутпуттенсор* должны иметь одинаковый *тип данных*.

## <a name="tensor-support"></a>Поддержка тензорные
| Тензорные | Вид | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | -------------------------- | -------------------- |
| инпуттенсор | Входные данные | 4 | FLOAT32, FLOAT16 |
| аутпуттенсор | Выходные данные | 4 | FLOAT32, FLOAT16 |


## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |