---
UID: NS:directml.DML_ROI_ALIGN_OPERATOR_DESC
title: DML_ROI_ALIGN_OPERATOR_DESC
description: Выполняет операцию по согласованию рентабельности инвестиций, как описано в [документе Mask R-CNN](https://arxiv.org/abs/1703.06870). В целом операция извлекает кадрирование из входного изображения тензорные и изменяет их размер на общий размер выходных данных, заданный последними 2 измерениями *аутпуттенсор* , используя указанный *интерполатионмоде*.
helpviewer_keywords:
- DML_ROI_ALIGN_OPERATOR_DESC
- DML_ROI_ALIGN_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ROI_ALIGN_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ROI_ALIGN_OPERATOR_DESC, DML_ROI_ALIGN_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ROI_ALIGN_OPERATOR_DESC
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
- DML_ROI_ALIGN_OPERATOR_DESC
- directml/DML_ROI_ALIGN_OPERATOR_DESC
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
- DML_ROI_ALIGN_OPERATOR_DESC
ms.openlocfilehash: b9004a77d3b325dd3394d1a3a6b596e94997e9fd
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804009"
---
# <a name="dml_roi_align_operator_desc-structure-directmlh"></a>Структура DML_ROI_ALIGN_OPERATOR_DESC (директмл. h)

Выполняет операцию по согласованию рентабельности инвестиций, как описано в [документе Mask R-CNN](https://arxiv.org/abs/1703.06870). В целом операция извлекает кадрирование из входного изображения тензорные и изменяет их размер на общий размер выходных данных, заданный последними 2 измерениями *аутпуттенсор* , используя указанный *интерполатионмоде*.

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис

```cpp
struct DML_ROI_ALIGN_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* ROITensor;
  const DML_TENSOR_DESC* BatchIndicesTensor;
  const DML_TENSOR_DESC* OutputTensor;
  DML_REDUCE_FUNCTION ReductionFunction;
  DML_INTERPOLATION_MODE InterpolationMode;
  FLOAT SpatialScaleX;
  FLOAT SpatialScaleY;
  FLOAT OutOfBoundsInputValue;
  UINT MinimumSamplesPerOutput;
  UINT MaximumSamplesPerOutput;
};
```

## <a name="members"></a>Члены

`InputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, содержащий входные данные с измерениями `{ BatchCount, ChannelCount, InputHeight, InputWidth }` .

`ROITensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Тензорные, содержащий интересующие Вас регионы (окупаемость инвестиций). Допустимые размеры `ROITensor` : `{ NumROIs, 4 }` , `{ 1, NumROIs, 4 }` или `{ 1, 1, NumROIs, 4 }` . Для каждой РЕНТАБЕЛЬности значения будут являться координатами верхнего левого и нижнего правого угла в порядке `[x1, y1, x2, y2]` .

`BatchIndicesTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, содержащий индексы пакетной службы для извлечения РОИС из. Допустимые размеры `BatchIndicesTensor` : `{ NumROIs }` , `{ 1, NumROIs }` , `{ 1, 1, NumROIs }` или `{ 1, 1, 1, NumROIs }` . Каждое значение является индексом пакета из *инпуттенсор*. Поведение не определено, если значения находятся за пределами диапазона [0, Батчкаунт).

`OutputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, содержащий выходные данные. Ожидаемые размеры *аутпуттенсор* : `{ NumROIs, ChannelCount, OutputHeight, OutputWidth }` .

`ReductionFunction`

Тип: **[DML_REDUCE_FUNCTION](/windows/win32/api/directml/ne-directml-dml_reduce_function)**

Функция сокращения, используемая при сокращении всех входных выборок, которые вносят вклад в элемент Output ([DML_REDUCE_FUNCTION_AVERAGE](/windows/win32/api/directml/ne-directml-dml_reduce_function) или **DML_REDUCE_FUNCTION_MAX**). Количество выборок, которые необходимо уменьшить, ограничено *минимумсамплеспераутпут* и *максимумсамплеспераутпут*.

`InterpolationMode`

Тип: **[DML_INTERPOLATION_MODE](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)**

Режим интерполяции, используемый при изменении размера регионов.

- [DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR](/windows/win32/api/directml/ne-directml-dml_interpolation_mode). Использует *ближайший алгоритм соседей* , который выбирает элемент ввода, ближайший к соответствующему центру пикселей для каждого выходного элемента.
- **DML_INTERPOLATION_MODE_LINEAR**. Использует алгоритм *билинейной* , который вычисляет элемент Output, выполняя взвешенное среднее по 2 ближайшим соседним входным элементам на измерение. Так как размер изменяется только для двух измерений, взвешенное среднее вычисляется по общему числу из 4 входных элементов для каждого выходного элемента.

`SpatialScaleX`

Тип: <b> <a href="/windows/win32/winprog/windows-data-types">float</a></b>

Компонент X (или Width) коэффициента масштабирования для умножения координат *роитенсор* на, чтобы сделать их пропорциональными для *инпусеигхт* и *инпутвидс*. Например, если *роитенсор* содержит нормализованные координаты (значения в диапазоне [0.. 1]), то *спатиалскалекс* обычно имеют то же значение, что и *инпутвидс*.

`SpatialScaleY`

Тип: <b> <a href="/windows/win32/winprog/windows-data-types">float</a></b>

Компонент Y (или Height) коэффициента масштабирования для умножения координат *роитенсор* на, чтобы сделать их пропорциональными для *инпусеигхт* и *инпутвидс*. Например, если *роитенсор* содержит нормализованные координаты (значения в диапазоне [0.. 1]), *спатиалскалэй* обычно имеют то же значение, что и *инпусеигхт*.

`OutOfBoundsInputValue`

Тип: <b> <a href="/windows/win32/winprog/windows-data-types">float</a></b>

Значение для чтения из *инпуттенсор* , если РОИС выходит за границы *инпуттенсор*. Это может произойти, если значения, полученные после масштабирования *роитенсор* по *спатиалскалекс* и *Спатиалскалэй* , больше *инпутвидс* и *инпусеигхт*.

`MinimumSamplesPerOutput`

Тип: <b> <a href="/windows/win32/winprog/windows-data-types">uint</a></b>

Минимальное число выборок входных данных, используемых для каждого выходного элемента. Оператор вычислит количество входных выборок `ScaledCropSize / OutputSize` , а затем получит его в *Минимумсамплеспераутпут* и *максимумсамплеспераутпут*.

`MaximumSamplesPerOutput`

Тип: <b> <a href="/windows/win32/winprog/windows-data-types">uint</a></b>

Максимальное число выборок входных данных, используемых для каждого элемента Output. Оператор вычислит количество входных выборок `ScaledCropSize / OutputSize` , а затем получит его в *Минимумсамплеспераутпут* и *максимумсамплеспераутпут*.

## <a name="availability"></a>Доступность
Этот оператор появился в `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Ограничения тензорные
*Инпуттенсор*, *аутпуттенсор* и *Роитенсор* должны иметь одинаковый *тип данных*.

## <a name="tensor-support"></a>Поддержка тензорные
| Тензорные | Вид | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | -------------------------- | -------------------- |
| инпуттенсор | Входные данные | 4 | FLOAT32, FLOAT16 |
| роитенсор | Входные данные | от 2 до 4 | FLOAT32, FLOAT16 |
| батчиндицестенсор | Входные данные | от 1 до 4 | ЗНАЧЕНИЕМ |
| аутпуттенсор | Выходные данные | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |