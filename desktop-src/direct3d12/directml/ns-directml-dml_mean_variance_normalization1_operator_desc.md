---
UID: NS:directml.DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
title: DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
description: Выполняет функцию нормализации значения дисперсии для входного тензорные. Этот оператор вычисляет среднее и дисперсию входных тензорные для выполнения нормализации.
helpviewer_keywords:
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure
- direct3d12.dml_mean_variance_normalization1_operator_desc
- directml/DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
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
f1_keywords:
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
- directml/DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
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
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
ms.openlocfilehash: ae22b004f1e879eb020ddcfe39a5f26481a508b0
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417540"
---
# <a name="dml_mean_variance_normalization1_operator_desc-structure-directmlh"></a>Структура DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC (директмл. h)

Выполняет функцию нормализации значения дисперсии для входного тензорные. Этот оператор вычисляет среднее и дисперсию входных тензорные для выполнения нормализации. Этот оператор выполняет следующие вычисления.

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис
```cpp
struct DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC {
  const DML_TENSOR_DESC   *InputTensor;
  const DML_TENSOR_DESC   *ScaleTensor;
  const DML_TENSOR_DESC   *BiasTensor;
  const DML_TENSOR_DESC   *OutputTensor;
  UINT                    AxisCount;
  const UINT              *Axes;
  BOOL                    NormalizeVariance;
  FLOAT                   Epsilon;
  const DML_OPERATOR_DESC *FusedActivation;
};
```
## <a name="members"></a>Участники

`InputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, содержащий входные данные. Размеры тензорные должны быть `{ BatchCount, ChannelCount, Height, Width }` .

`ScaleTensor`

Тип: \_ майбенулл \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Необязательный тензорные, содержащий данные шкалы.

Если **DML_FEATURE_LEVEL** меньше **DML_FEATURE_LEVEL_4_0**, то размеры этого тензорные должны быть `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }` . Измерения Скалебатчкаунт, Скалехеигхт и Скалевидс должны либо соответствовать *инпуттенсор*, либо иметь значение 1 для автоматического вещания этих измерений во входных данных.

Если **DML_FEATURE_LEVEL** больше или равно **DML_FEATURE_LEVEL_4_0**, то любое измерение может быть установлено в 1 и автоматически рассылаться в соответствии с *инпуттенсор*.

Этот тензорные является обязательным, если используется *биастенсор* .

`BiasTensor`

Тип: \_ майбенулл \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***


Необязательный тензорные, содержащий данные смещения.

Если **DML_FEATURE_LEVEL** меньше **DML_FEATURE_LEVEL_4_0**, то размеры этого тензорные должны быть `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }` . Измерения Биасбатчкаунт, Биашеигхт и Биасвидс должны либо соответствовать *инпуттенсор*, либо иметь значение 1 для автоматического вещания этих измерений во входных данных.

Если **DML_FEATURE_LEVEL** больше или равно **DML_FEATURE_LEVEL_4_0**, то любое измерение может быть установлено в 1 и автоматически рассылаться в соответствии с *инпуттенсор*.

Этот тензорные является обязательным, если используется *скалетенсор* .

`OutputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, в который записываются результаты. Это тензорные измерения `{ BatchCount, ChannelCount, Height, Width }` .

`AxisCount`

Тип: <b> <a href="/windows/win32/winprog/windows-data-types">uint</a></b>

Число осей. Это поле определяет размер массива *осей* .

`Axes`

Тип: \_ \_ Размер поля \_ (Аксискаунт) **const [uint](../../winprog/windows-data-types.md) \*** 

Оси, вдоль которых вычисляется среднее и дисперсия.

`NormalizeVariance`

Тип: <b> <a href="/windows/win32/winprog/windows-data-types">bool</a> .</b>

**Значение true** , если слой нормализации включает вариативность в вычислении нормализации. В противном случае — **значение false**. Если **значение равно false**, то уравнение нормализации имеет значение `Output = FusedActivation(Scale * (Input - Mean) + Bias)` .

`Epsilon`

Тип: <b> <a href="/windows/win32/winprog/windows-data-types">float</a></b>

Значение Эпсилон, которое следует использовать, чтобы избежать деления на нуль. По умолчанию рекомендуется использовать значение 0,00001.

`FusedActivation`

Тип: \_ майбенулл \_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) \***

Необязательный слой активации с плавким предохранителем, применяемый после нормализации.

## <a name="remarks"></a>Remarks
**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** является надмножеством функций [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc). Здесь установка массива **осей** равна `{ 0, 2, 3 }` эквиваленту параметра *кроссчаннел*  в **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; при установке массива **осей** равным значению `{ 1, 2, 3 }` *кроссчаннел* значение **true**.

## <a name="availability"></a>Доступность
Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Ограничения тензорные

*Биастенсор*, *инпуттенсор*, *аутпуттенсор* и *Скалетенсор* должны иметь одинаковые типы *данных* и *DimensionCount*.

## <a name="tensor-support"></a>Поддержка тензорные

### <a name="dml_feature_level_3_1-and-above"></a>DML_FEATURE_LEVEL_3_1 и выше

| Тензорные | Вид | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | -------------------------- | -------------------- |
| инпуттенсор | Входные данные | от 1 до 8 | FLOAT32, FLOAT16 |
| скалетенсор | Необязательный ввод | от 1 до 8 | FLOAT32, FLOAT16 |
| биастенсор | Необязательный ввод | от 1 до 8 | FLOAT32, FLOAT16 |
| аутпуттенсор | Выходные данные | от 1 до 8 | FLOAT32, FLOAT16 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 и выше

| Тензорные | Вид | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | -------------------------- | -------------------- |
| инпуттенсор | Входные данные | 4 | FLOAT32, FLOAT16 |
| скалетенсор | Необязательный ввод | 4 | FLOAT32, FLOAT16 |
| биастенсор | Необязательный ввод | 4 | FLOAT32, FLOAT16 |
| аутпуттенсор | Выходные данные | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |

## <a name="see-also"></a>См. также раздел

[Использование операторов с плавким предохранителем для повышения производительности](../dml-fused-activations.md)