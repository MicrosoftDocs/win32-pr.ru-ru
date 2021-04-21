---
UID: NS:directml.DML_ADAM_OPTIMIZER_OPERATOR_DESC
title: DML_ADAM_OPTIMIZER_OPERATOR_DESC
description: Выполняет вычисление обновленных весов (параметров) с помощью представленных градиентов на основе алгоритма ADAM (**ADA** птиве **M** омент оценкой). Этот оператор является оптимизатором и обычно используется на шаге обновления веса цикла обучения для выполнения спуска градиента.
helpviewer_keywords:
- DML_ADAM_OPTIMIZER_OPERATOR_DESC
- DML_ADAM_OPTIMIZER_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ADAM_OPTIMIZER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ADAM_OPTIMIZER_OPERATOR_DESC, DML_ADAM_OPTIMIZER_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ADAM_OPTIMIZER_OPERATOR_DESC
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
- DML_ADAM_OPTIMIZER_OPERATOR_DESC
- directml/DML_ADAM_OPTIMIZER_OPERATOR_DESC
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
- DML_ADAM_OPTIMIZER_OPERATOR_DESC
ms.openlocfilehash: 9943f70bd3d62faf57f4eca83f9f09ce0119881a
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803532"
---
# <a name="dml_adam_optimizer_operator_desc-structure-directmlh"></a>Структура DML_ADAM_OPTIMIZER_OPERATOR_DESC (директмл. h)

Выполняет вычисление обновленных весов (параметров) с помощью представленных градиентов на основе алгоритма ADAM (**ADA** птиве **M** омент оценкой). Этот оператор является оптимизатором и обычно используется на шаге обновления веса цикла обучения для выполнения спуска градиента.

Этот оператор выполняет следующие вычисления:

```
X = InputParametersTensor
M = InputFirstMomentTensor
V = InputSecondMomentTensor
G = GradientTensor
T = TrainingStepTensor

// Compute updated first and second moment estimates.
M = Beta1 * M + (1.0 - Beta1) * G
V = Beta2 * V + (1.0 - Beta2) * G * G

// Compute bias correction factor for first and second moment estimates.
Alpha = sqrt(1.0 - pow(Beta2, T)) / (1.0 - pow(Beta1, T))

X -= LearningRate * Alpha * M / (sqrt(V) + Epsilon)

OutputParametersTensor = X
OutputFirstMomentTensor = M
OutputSecondMomentTensor = V
```

Кроме вычисления обновленных параметров веса (возвращаемых в *аутпутпараметерстенсор*), этот оператор также возвращает обновленные первые и вторые оценки в *аутпутфирстмоменттенсор* и *аутпутсекондмоменттенсор* соответственно. Как правило, вы должны сохранить эти первые и вторые оценки и указать их в качестве входных данных на следующем этапе обучения.

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис
```cpp
struct DML_ADAM_OPTIMIZER_OPERATOR_DESC
{ 
  const DML_TENSOR_DESC* InputParametersTensor;
  const DML_TENSOR_DESC* InputFirstMomentTensor;
  const DML_TENSOR_DESC* InputSecondMomentTensor;
  const DML_TENSOR_DESC* GradientTensor;
  const DML_TENSOR_DESC* TrainingStepTensor;
  const DML_TENSOR_DESC* OutputParametersTensor;
  const DML_TENSOR_DESC* OutputFirstMomentTensor;
  const DML_TENSOR_DESC* OutputSecondMomentTensor;
  FLOAT LearningRate;
  FLOAT Beta1;
  FLOAT Beta2;
  FLOAT Epsilon;
};
```

## <a name="members"></a>Члены

`InputParametersTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, содержащий параметры (веса), к которым применяется этот оптимизатор. Оценка градиента, первого и второго времени, текущий шаг обучения, а также параметры *леарнинграте*, *Beta1* и *бета*, используются этим оператором для выполнения градиентной спуска по значениям веса, предоставленным в этом тензорные.

`InputFirstMomentTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, содержащий первую оценку градиента для каждого значения веса. Эти значения обычно получаются в результате предыдущего выполнения этого оператора через *аутпутфирстмоменттенсор*.

При первом применении этого оптимизатора к набору весовых коэффициентов (например, на этапе начального обучения) значения этого тензорные обычно инициализируются нулем. Последующие выполнения должны использовать значения, возвращенные в *аутпутфирстмоменттенсор*.

*Размеры* и *тип данных* этого тензорные должны точно соответствовать параметрам *инпутпараметерстенсор*.

`InputSecondMomentTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, содержащий вторую оценку градиента для каждого значения веса. Эти значения обычно получаются в результате предыдущего выполнения этого оператора через *аутпутсекондмоменттенсор*.

При первом применении этого оптимизатора к набору весовых коэффициентов (например, на этапе начального обучения) значения этого тензорные обычно инициализируются нулем. Последующие выполнения должны использовать значения, возвращенные в *аутпутсекондмоменттенсор*.

*Размеры* и *тип данных* этого тензорные должны точно соответствовать параметрам *инпутпараметерстенсор*.

`GradientTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Градиенты, применяемые к входным параметрам (весам) для спуска линий градиента. Градиенты обычно получаются при обратном распространении во время обучения.

*Размеры* и *тип данных* этого тензорные должны точно соответствовать параметрам *инпутпараметерстенсор*.

`TrainingStepTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Скалярный тензорные, содержащий одно целочисленное значение, представляющее текущее число шагов обучения. Это значение вместе с *Beta1* и *бета* -версией используется для вычисления экспоненциального decayа в первый и второй моменты оценки десятков.

Как правило, значение шага обучения начинается с 0 в начале обучения и увеличивается на 1 для каждого последующего этапа обучения. Этот оператор не обновляет значение шага обучения; Это необходимо сделать вручную, например с помощью [DML_OPERATOR_ELEMENT_WISE_ADD](/windows/win32/api/directml/ns-directml-dml_element_wise_add_operator_desc).

Этот тензорные должен быть скалярным (то есть все *размеры* равны 1) и иметь тип данных [**DML_TENSOR_DATA_TYPE_UINT32**](/windows/win32/api/directml/ne-directml-dml_tensor_data_type).

`OutputParametersTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Выходной тензорные, содержащий обновленные значения параметра (веса) после применения спуска градиента.

Во время привязки этому тензорныеу может быть присвоен псевдоним подходящего входного тензорные, который можно использовать для выполнения обновления на месте этого тензорные. Дополнительные сведения см. в разделе ["Примечания"](#remarks) .

*Размеры* и *тип данных* этого тензорные должны точно соответствовать параметрам *инпутпараметерстенсор*.

`OutputFirstMomentTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Выходной тензорные, содержащий обновленные первые оценки. Вы должны сохранить значения этого тензорные и указать их в *инпутфирстмоменттенсор* на следующем этапе обучения.

Во время привязки этому тензорныеу может быть присвоен псевдоним подходящего входного тензорные, который можно использовать для выполнения обновления на месте этого тензорные. Дополнительные сведения см. в разделе ["Примечания"](#remarks) .

*Размеры* и *тип данных* этого тензорные должны точно соответствовать параметрам *инпутпараметерстенсор*.

`OutputSecondMomentTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Выходной тензорные, содержащий обновленные секунды оценки. Вы должны сохранить значения этого тензорные и указать их в *инпутсекондмоменттенсор* на следующем этапе обучения.

Во время привязки этому тензорныеу может быть присвоен псевдоним подходящего входного тензорные, который можно использовать для выполнения обновления на месте этого тензорные. Дополнительные сведения см. в разделе ["Примечания"](#remarks) .

*Размеры* и *тип данных* этого тензорные должны точно соответствовать параметрам *инпутпараметерстенсор*.

`LearningRate`

Тип: **float**

Темп обучения, который также часто называют *размером шага*. Скорость обучения — это параметр, определяющий величину обновления веса вдоль вектора градиента на каждом шаге обучения.

`Beta1`

Тип: **float**

Параметр «Decay», представляющий экспоненциальную коэффициент оценки в первый момент градиента. Это значение должно находиться в диапазоне от 0,0 до 1,0. Значение 0.9 f является типичным.

`Beta2`

Тип: **float**

Параметр "Decay", представляющий экспоненциальную частоту времени в секундах для градиента. Это значение должно находиться в диапазоне от 0,0 до 1,0. Значение 0,999 f является типичным.

`Epsilon`

Тип: **float**

Небольшое значение, используемое для обеспечения цифровой устойчивости, предотвращая деление на ноль. Для 32-разрядных входных данных с плавающей запятой типичные значения включают 1E-8 или `FLT_EPSILON` .

## <a name="remarks"></a>Комментарии
Этот оператор поддерживает выполнение на месте, что означает, что каждому выходному тензорныеу может быть присвоен псевдоним подходящего входного тензорные во время привязки. Например, можно привязать один и тот же ресурс для *инпутпараметерстенсор* и *аутпутпараметерстенсор* , чтобы обеспечить эффективное обновление входных параметров на месте. Все входные десятки этого оператора, за исключением *траинингстептенсор*, могут быть псевдонимами таким образом.

## <a name="availability"></a>Доступность
Этот оператор появился в `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Ограничения тензорные
* *Градиенттенсор*, *инпутфирстмоменттенсор*, *инпутпараметерстенсор*, *инпутсекондмоменттенсор*, *OutputFirstMomentTensor*, *OutputParametersTensor*, *OutputSecondMomentTensor* и *TrainingStepTensor* должны иметь одинаковый *тип данных*.
* *Градиенттенсор*, *инпутфирстмоменттенсор*, *инпутпараметерстенсор*, *инпутсекондмоменттенсор*, *OutputFirstMomentTensor*, *OutputParametersTensor* и *OutputSecondMomentTensor* должны иметь одинаковые *размеры*.

## <a name="tensor-support"></a>Поддержка тензорные
| Тензорные | Вид | Измерения | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| инпутпараметерстенсор | Входные данные | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |
| инпутфирстмоменттенсор | Входные данные | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |
| инпутсекондмоменттенсор | Входные данные | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |
| градиенттенсор | Входные данные | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |
| траинингстептенсор | Входные данные | {1, 1, 1, 1} | 4 | FLOAT32, FLOAT16 |
| аутпутпараметерстенсор | Выходные данные | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |
| аутпутфирстмоменттенсор | Выходные данные | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |
| аутпутсекондмоменттенсор | Выходные данные | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |