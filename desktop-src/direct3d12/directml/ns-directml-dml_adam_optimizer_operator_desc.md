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
ms.openlocfilehash: a4acd26f5174bf6c6ae53f5edfdc28cc6c9b1a3d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719907"
---
# <a name="dml_adam_optimizer_operator_desc-structure-directmlh"></a><span data-ttu-id="e032f-104">Структура DML_ADAM_OPTIMIZER_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="e032f-104">DML_ADAM_OPTIMIZER_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="e032f-105">Выполняет вычисление обновленных весов (параметров) с помощью представленных градиентов на основе алгоритма ADAM (**ADA** птиве **M** омент оценкой).</span><span class="sxs-lookup"><span data-stu-id="e032f-105">Computes updated weights (parameters) using the supplied gradients, based on the Adam (**ADA** ptive **M** oment estimation) algorithm.</span></span> <span data-ttu-id="e032f-106">Этот оператор является оптимизатором и обычно используется на шаге обновления веса цикла обучения для выполнения спуска градиента.</span><span class="sxs-lookup"><span data-stu-id="e032f-106">This operator is an optimizer, and is typically used in the weight update step of a training loop to perform gradient descent.</span></span>

<span data-ttu-id="e032f-107">Этот оператор выполняет следующие вычисления:</span><span class="sxs-lookup"><span data-stu-id="e032f-107">This operator performs the following computation:</span></span>

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

<span data-ttu-id="e032f-108">Кроме вычисления обновленных параметров веса (возвращаемых в *аутпутпараметерстенсор*), этот оператор также возвращает обновленные первые и вторые оценки в *аутпутфирстмоменттенсор* и *аутпутсекондмоменттенсор* соответственно.</span><span class="sxs-lookup"><span data-stu-id="e032f-108">In addition to computing the updated weight parameters (returned in *OutputParametersTensor*), this operator also returns the updated first and second moment estimates in *OutputFirstMomentTensor* and *OutputSecondMomentTensor*, respectively.</span></span> <span data-ttu-id="e032f-109">Как правило, вы должны сохранить эти первые и вторые оценки и указать их в качестве входных данных на следующем этапе обучения.</span><span class="sxs-lookup"><span data-stu-id="e032f-109">Typically, you should store these first and second moment estimates, and supply them as inputs during the subsequent training step.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e032f-110">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="e032f-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="e032f-111">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="e032f-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e032f-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e032f-112">Syntax</span></span>
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

## <a name="members"></a><span data-ttu-id="e032f-113">Члены</span><span class="sxs-lookup"><span data-stu-id="e032f-113">Members</span></span>

`InputParametersTensor`

<span data-ttu-id="e032f-114">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e032f-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e032f-115">Объект тензорные, содержащий параметры (веса), к которым применяется этот оптимизатор.</span><span class="sxs-lookup"><span data-stu-id="e032f-115">A tensor containing the parameters (weights) to apply this optimizer to.</span></span> <span data-ttu-id="e032f-116">Оценка градиента, первого и второго времени, текущий шаг обучения, а также параметры *леарнинграте*, *Beta1* и *бета*, используются этим оператором для выполнения градиентной спуска по значениям веса, предоставленным в этом тензорные.</span><span class="sxs-lookup"><span data-stu-id="e032f-116">The gradient, first, and second moment estimates, current training step, as well as hyperparameters *LearningRate*, *Beta1*, and *Beta2*, are used by this operator to perform gradient descent on the weight values supplied in this tensor.</span></span>

`InputFirstMomentTensor`

<span data-ttu-id="e032f-117">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e032f-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e032f-118">Объект тензорные, содержащий первую оценку градиента для каждого значения веса.</span><span class="sxs-lookup"><span data-stu-id="e032f-118">A tensor containing the first moment estimate of the gradient for each weight value.</span></span> <span data-ttu-id="e032f-119">Эти значения обычно получаются в результате предыдущего выполнения этого оператора через *аутпутфирстмоменттенсор*.</span><span class="sxs-lookup"><span data-stu-id="e032f-119">These values are typically obtained as the result of a previous execution of this operator, via the *OutputFirstMomentTensor*.</span></span>

<span data-ttu-id="e032f-120">При первом применении этого оптимизатора к набору весовых коэффициентов (например, на этапе начального обучения) значения этого тензорные обычно инициализируются нулем.</span><span class="sxs-lookup"><span data-stu-id="e032f-120">When applying this optimizer to a set of weights for the first time (for example, during the initial training step) the values of this tensor should typically be initialized to zero.</span></span> <span data-ttu-id="e032f-121">Последующие выполнения должны использовать значения, возвращенные в *аутпутфирстмоменттенсор*.</span><span class="sxs-lookup"><span data-stu-id="e032f-121">Subsequent executions should use the values returned in *OutputFirstMomentTensor*.</span></span>

<span data-ttu-id="e032f-122">*Размеры* и *тип данных* этого тензорные должны точно соответствовать параметрам *инпутпараметерстенсор*.</span><span class="sxs-lookup"><span data-stu-id="e032f-122">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`InputSecondMomentTensor`

<span data-ttu-id="e032f-123">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e032f-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e032f-124">Объект тензорные, содержащий вторую оценку градиента для каждого значения веса.</span><span class="sxs-lookup"><span data-stu-id="e032f-124">A tensor containing the second moment estimate of the gradient for each weight value.</span></span> <span data-ttu-id="e032f-125">Эти значения обычно получаются в результате предыдущего выполнения этого оператора через *аутпутсекондмоменттенсор*.</span><span class="sxs-lookup"><span data-stu-id="e032f-125">These values are typically obtained as the result of a previous execution of this operator, via the *OutputSecondMomentTensor*.</span></span>

<span data-ttu-id="e032f-126">При первом применении этого оптимизатора к набору весовых коэффициентов (например, на этапе начального обучения) значения этого тензорные обычно инициализируются нулем.</span><span class="sxs-lookup"><span data-stu-id="e032f-126">When applying this optimizer to a set of weights for the first time (for example, during the initial training step) the values of this tensor should typically be initialized to zero.</span></span> <span data-ttu-id="e032f-127">Последующие выполнения должны использовать значения, возвращенные в *аутпутсекондмоменттенсор*.</span><span class="sxs-lookup"><span data-stu-id="e032f-127">Subsequent executions should use the values returned in *OutputSecondMomentTensor*.</span></span>

<span data-ttu-id="e032f-128">*Размеры* и *тип данных* этого тензорные должны точно соответствовать параметрам *инпутпараметерстенсор*.</span><span class="sxs-lookup"><span data-stu-id="e032f-128">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`GradientTensor`

<span data-ttu-id="e032f-129">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e032f-129">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e032f-130">Градиенты, применяемые к входным параметрам (весам) для спуска линий градиента.</span><span class="sxs-lookup"><span data-stu-id="e032f-130">The gradients to apply to the input parameters (weights) for gradient descent.</span></span> <span data-ttu-id="e032f-131">Градиенты обычно получаются при обратном распространении во время обучения.</span><span class="sxs-lookup"><span data-stu-id="e032f-131">Gradients are typically obtained in a backpropagation pass during training.</span></span>

<span data-ttu-id="e032f-132">*Размеры* и *тип данных* этого тензорные должны точно соответствовать параметрам *инпутпараметерстенсор*.</span><span class="sxs-lookup"><span data-stu-id="e032f-132">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`TrainingStepTensor`

<span data-ttu-id="e032f-133">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e032f-133">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e032f-134">Скалярный тензорные, содержащий одно целочисленное значение, представляющее текущее число шагов обучения.</span><span class="sxs-lookup"><span data-stu-id="e032f-134">A scalar tensor containing a single integer value representing the current training step count.</span></span> <span data-ttu-id="e032f-135">Это значение вместе с *Beta1* и *бета* -версией используется для вычисления экспоненциального decayа в первый и второй моменты оценки десятков.</span><span class="sxs-lookup"><span data-stu-id="e032f-135">This value along with *Beta1* and *Beta2* is used to compute the exponential decay of the first and second moment estimate tensors.</span></span>

<span data-ttu-id="e032f-136">Как правило, значение шага обучения начинается с 0 в начале обучения и увеличивается на 1 для каждого последующего этапа обучения.</span><span class="sxs-lookup"><span data-stu-id="e032f-136">Typically the training step value starts at 0 at the beginning of training, and is incremented by 1 on each successive training step.</span></span> <span data-ttu-id="e032f-137">Этот оператор не обновляет значение шага обучения; Это необходимо сделать вручную, например с помощью [DML_OPERATOR_ELEMENT_WISE_ADD](/windows/win32/api/directml/ns-directml-dml_element_wise_add_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="e032f-137">This operator doesn't update the training step value; you should do that manually, for example using [DML_OPERATOR_ELEMENT_WISE_ADD](/windows/win32/api/directml/ns-directml-dml_element_wise_add_operator_desc).</span></span>

<span data-ttu-id="e032f-138">Этот тензорные должен быть скалярным (то есть все *размеры* равны 1) и иметь тип данных [**DML_TENSOR_DATA_TYPE_UINT32**](/windows/win32/api/directml/ne-directml-dml_tensor_data_type).</span><span class="sxs-lookup"><span data-stu-id="e032f-138">This tensor must be a scalar (that is, all *Sizes* equal to 1) and have data type [**DML_TENSOR_DATA_TYPE_UINT32**](/windows/win32/api/directml/ne-directml-dml_tensor_data_type).</span></span>

`OutputParametersTensor`

<span data-ttu-id="e032f-139">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e032f-139">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e032f-140">Выходной тензорные, содержащий обновленные значения параметра (веса) после применения спуска градиента.</span><span class="sxs-lookup"><span data-stu-id="e032f-140">An output tensor that holds the updated parameter (weight) values after gradient descent is applied.</span></span>

<span data-ttu-id="e032f-141">Во время привязки этому тензорныеу может быть присвоен псевдоним подходящего входного тензорные, который можно использовать для выполнения обновления на месте этого тензорные.</span><span class="sxs-lookup"><span data-stu-id="e032f-141">During binding, this tensor is permitted to alias an eligible input tensor, which can be used to perform an in-place update of this tensor.</span></span> <span data-ttu-id="e032f-142">Дополнительные сведения см. в разделе ["Примечания"](#remarks) .</span><span class="sxs-lookup"><span data-stu-id="e032f-142">See the [Remarks](#remarks) section for more details.</span></span>

<span data-ttu-id="e032f-143">*Размеры* и *тип данных* этого тензорные должны точно соответствовать параметрам *инпутпараметерстенсор*.</span><span class="sxs-lookup"><span data-stu-id="e032f-143">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`OutputFirstMomentTensor`

<span data-ttu-id="e032f-144">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e032f-144">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e032f-145">Выходной тензорные, содержащий обновленные первые оценки.</span><span class="sxs-lookup"><span data-stu-id="e032f-145">An output tensor containing updated first moment estimates.</span></span> <span data-ttu-id="e032f-146">Вы должны сохранить значения этого тензорные и указать их в *инпутфирстмоменттенсор* на следующем этапе обучения.</span><span class="sxs-lookup"><span data-stu-id="e032f-146">You should store the values of this tensor, and supply them in *InputFirstMomentTensor* during the subsequent training step.</span></span>

<span data-ttu-id="e032f-147">Во время привязки этому тензорныеу может быть присвоен псевдоним подходящего входного тензорные, который можно использовать для выполнения обновления на месте этого тензорные.</span><span class="sxs-lookup"><span data-stu-id="e032f-147">During binding, this tensor is permitted to alias an eligible input tensor, which can be used to perform an in-place update of this tensor.</span></span> <span data-ttu-id="e032f-148">Дополнительные сведения см. в разделе ["Примечания"](#remarks) .</span><span class="sxs-lookup"><span data-stu-id="e032f-148">See the [Remarks](#remarks) section for more details.</span></span>

<span data-ttu-id="e032f-149">*Размеры* и *тип данных* этого тензорные должны точно соответствовать параметрам *инпутпараметерстенсор*.</span><span class="sxs-lookup"><span data-stu-id="e032f-149">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`OutputSecondMomentTensor`

<span data-ttu-id="e032f-150">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e032f-150">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e032f-151">Выходной тензорные, содержащий обновленные секунды оценки.</span><span class="sxs-lookup"><span data-stu-id="e032f-151">An output tensor containing updated second moment estimates.</span></span> <span data-ttu-id="e032f-152">Вы должны сохранить значения этого тензорные и указать их в *инпутсекондмоменттенсор* на следующем этапе обучения.</span><span class="sxs-lookup"><span data-stu-id="e032f-152">You should store the values of this tensor and supply them in *InputSecondMomentTensor* during the subsequent training step.</span></span>

<span data-ttu-id="e032f-153">Во время привязки этому тензорныеу может быть присвоен псевдоним подходящего входного тензорные, который можно использовать для выполнения обновления на месте этого тензорные.</span><span class="sxs-lookup"><span data-stu-id="e032f-153">During binding, this tensor is permitted to alias an eligible input tensor, which can be used to perform an in-place update of this tensor.</span></span> <span data-ttu-id="e032f-154">Дополнительные сведения см. в разделе ["Примечания"](#remarks) .</span><span class="sxs-lookup"><span data-stu-id="e032f-154">See the [Remarks](#remarks) section for more details.</span></span>

<span data-ttu-id="e032f-155">*Размеры* и *тип данных* этого тензорные должны точно соответствовать параметрам *инпутпараметерстенсор*.</span><span class="sxs-lookup"><span data-stu-id="e032f-155">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`LearningRate`

<span data-ttu-id="e032f-156">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="e032f-156">Type: **float**</span></span>

<span data-ttu-id="e032f-157">Темп обучения, который также часто называют *размером шага*.</span><span class="sxs-lookup"><span data-stu-id="e032f-157">The learning rate, also commonly referred to as the *step size*.</span></span> <span data-ttu-id="e032f-158">Скорость обучения — это параметр, определяющий величину обновления веса вдоль вектора градиента на каждом шаге обучения.</span><span class="sxs-lookup"><span data-stu-id="e032f-158">The learning rate is a hyperparameter that determines the magnitude of the weight update along the gradient vector on each training step.</span></span>

`Beta1`

<span data-ttu-id="e032f-159">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="e032f-159">Type: **float**</span></span>

<span data-ttu-id="e032f-160">Параметр «Decay», представляющий экспоненциальную коэффициент оценки в первый момент градиента.</span><span class="sxs-lookup"><span data-stu-id="e032f-160">A hyperparameter representing the exponential decay rate of the gradient's first moment estimate.</span></span> <span data-ttu-id="e032f-161">Это значение должно находиться в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="e032f-161">This value should be between 0.0 and 1.0.</span></span> <span data-ttu-id="e032f-162">Значение 0.9 f является типичным.</span><span class="sxs-lookup"><span data-stu-id="e032f-162">A value of 0.9f is typical.</span></span>

`Beta2`

<span data-ttu-id="e032f-163">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="e032f-163">Type: **float**</span></span>

<span data-ttu-id="e032f-164">Параметр "Decay", представляющий экспоненциальную частоту времени в секундах для градиента.</span><span class="sxs-lookup"><span data-stu-id="e032f-164">A hyperparameter representing the exponential decay rate of the gradient's second moment estimate.</span></span> <span data-ttu-id="e032f-165">Это значение должно находиться в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="e032f-165">This value should be between 0.0 and 1.0.</span></span> <span data-ttu-id="e032f-166">Значение 0,999 f является типичным.</span><span class="sxs-lookup"><span data-stu-id="e032f-166">A value of 0.999f is typical.</span></span>

`Epsilon`

<span data-ttu-id="e032f-167">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="e032f-167">Type: **float**</span></span>

<span data-ttu-id="e032f-168">Небольшое значение, используемое для обеспечения цифровой устойчивости, предотвращая деление на ноль.</span><span class="sxs-lookup"><span data-stu-id="e032f-168">A small value used to help numerical stability by preventing division-by-zero.</span></span> <span data-ttu-id="e032f-169">Для 32-разрядных входных данных с плавающей запятой типичные значения включают 1E-8 или `FLT_EPSILON` .</span><span class="sxs-lookup"><span data-stu-id="e032f-169">For 32-bit floating-point inputs, typical values include 1e-8 or `FLT_EPSILON`.</span></span>

## <a name="remarks"></a><span data-ttu-id="e032f-170">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e032f-170">Remarks</span></span>
<span data-ttu-id="e032f-171">Этот оператор поддерживает выполнение на месте, что означает, что каждому выходному тензорныеу может быть присвоен псевдоним подходящего входного тензорные во время привязки.</span><span class="sxs-lookup"><span data-stu-id="e032f-171">This operator supports in-place execution, meaning that each output tensor is permitted to alias an eligible input tensor during binding.</span></span> <span data-ttu-id="e032f-172">Например, можно привязать один и тот же ресурс для *инпутпараметерстенсор* и *аутпутпараметерстенсор* , чтобы обеспечить эффективное обновление входных параметров на месте.</span><span class="sxs-lookup"><span data-stu-id="e032f-172">For example, it's possible to bind the same resource for both the *InputParametersTensor* and *OutputParametersTensor* in order to effectively achieve an in-place update of the input parameters.</span></span> <span data-ttu-id="e032f-173">Все входные десятки этого оператора, за исключением *траинингстептенсор*, могут быть псевдонимами таким образом.</span><span class="sxs-lookup"><span data-stu-id="e032f-173">All of this operator's input tensors, with the exception of the *TrainingStepTensor*, are eligible to be aliased in this way.</span></span>

## <a name="availability"></a><span data-ttu-id="e032f-174">Доступность</span><span class="sxs-lookup"><span data-stu-id="e032f-174">Availability</span></span>
<span data-ttu-id="e032f-175">Этот оператор появился в `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="e032f-175">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="e032f-176">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="e032f-176">Tensor constraints</span></span>
* <span data-ttu-id="e032f-177">*Градиенттенсор*, *инпутфирстмоменттенсор*, *инпутпараметерстенсор*, *инпутсекондмоменттенсор*, *OutputFirstMomentTensor*, *OutputParametersTensor*, *OutputSecondMomentTensor* и *TrainingStepTensor* должны иметь одинаковый *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="e032f-177">*GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor*, *OutputSecondMomentTensor*, and *TrainingStepTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="e032f-178">*Градиенттенсор*, *инпутфирстмоменттенсор*, *инпутпараметерстенсор*, *инпутсекондмоменттенсор*, *OutputFirstMomentTensor*, *OutputParametersTensor* и *OutputSecondMomentTensor* должны иметь одинаковые *размеры*.</span><span class="sxs-lookup"><span data-stu-id="e032f-178">*GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor*, and *OutputSecondMomentTensor* must have the same *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="e032f-179">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="e032f-179">Tensor support</span></span>
| <span data-ttu-id="e032f-180">Тензорные</span><span class="sxs-lookup"><span data-stu-id="e032f-180">Tensor</span></span> | <span data-ttu-id="e032f-181">Вид</span><span class="sxs-lookup"><span data-stu-id="e032f-181">Kind</span></span> | <span data-ttu-id="e032f-182">Измерения</span><span class="sxs-lookup"><span data-stu-id="e032f-182">Dimensions</span></span> | <span data-ttu-id="e032f-183">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="e032f-183">Supported dimension counts</span></span> | <span data-ttu-id="e032f-184">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="e032f-184">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="e032f-185">инпутпараметерстенсор</span><span class="sxs-lookup"><span data-stu-id="e032f-185">InputParametersTensor</span></span> | <span data-ttu-id="e032f-186">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e032f-186">Input</span></span> | <span data-ttu-id="e032f-187">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="e032f-187">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="e032f-188">4</span><span class="sxs-lookup"><span data-stu-id="e032f-188">4</span></span> | <span data-ttu-id="e032f-189">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e032f-189">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="e032f-190">инпутфирстмоменттенсор</span><span class="sxs-lookup"><span data-stu-id="e032f-190">InputFirstMomentTensor</span></span> | <span data-ttu-id="e032f-191">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e032f-191">Input</span></span> | <span data-ttu-id="e032f-192">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="e032f-192">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="e032f-193">4</span><span class="sxs-lookup"><span data-stu-id="e032f-193">4</span></span> | <span data-ttu-id="e032f-194">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e032f-194">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="e032f-195">инпутсекондмоменттенсор</span><span class="sxs-lookup"><span data-stu-id="e032f-195">InputSecondMomentTensor</span></span> | <span data-ttu-id="e032f-196">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e032f-196">Input</span></span> | <span data-ttu-id="e032f-197">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="e032f-197">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="e032f-198">4</span><span class="sxs-lookup"><span data-stu-id="e032f-198">4</span></span> | <span data-ttu-id="e032f-199">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e032f-199">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="e032f-200">градиенттенсор</span><span class="sxs-lookup"><span data-stu-id="e032f-200">GradientTensor</span></span> | <span data-ttu-id="e032f-201">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e032f-201">Input</span></span> | <span data-ttu-id="e032f-202">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="e032f-202">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="e032f-203">4</span><span class="sxs-lookup"><span data-stu-id="e032f-203">4</span></span> | <span data-ttu-id="e032f-204">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e032f-204">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="e032f-205">траинингстептенсор</span><span class="sxs-lookup"><span data-stu-id="e032f-205">TrainingStepTensor</span></span> | <span data-ttu-id="e032f-206">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e032f-206">Input</span></span> | <span data-ttu-id="e032f-207">{1, 1, 1, 1}</span><span class="sxs-lookup"><span data-stu-id="e032f-207">{ 1, 1, 1, 1 }</span></span> | <span data-ttu-id="e032f-208">4</span><span class="sxs-lookup"><span data-stu-id="e032f-208">4</span></span> | <span data-ttu-id="e032f-209">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e032f-209">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="e032f-210">аутпутпараметерстенсор</span><span class="sxs-lookup"><span data-stu-id="e032f-210">OutputParametersTensor</span></span> | <span data-ttu-id="e032f-211">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="e032f-211">Output</span></span> | <span data-ttu-id="e032f-212">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="e032f-212">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="e032f-213">4</span><span class="sxs-lookup"><span data-stu-id="e032f-213">4</span></span> | <span data-ttu-id="e032f-214">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e032f-214">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="e032f-215">аутпутфирстмоменттенсор</span><span class="sxs-lookup"><span data-stu-id="e032f-215">OutputFirstMomentTensor</span></span> | <span data-ttu-id="e032f-216">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="e032f-216">Output</span></span> | <span data-ttu-id="e032f-217">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="e032f-217">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="e032f-218">4</span><span class="sxs-lookup"><span data-stu-id="e032f-218">4</span></span> | <span data-ttu-id="e032f-219">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e032f-219">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="e032f-220">аутпутсекондмоменттенсор</span><span class="sxs-lookup"><span data-stu-id="e032f-220">OutputSecondMomentTensor</span></span> | <span data-ttu-id="e032f-221">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="e032f-221">Output</span></span> | <span data-ttu-id="e032f-222">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="e032f-222">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="e032f-223">4</span><span class="sxs-lookup"><span data-stu-id="e032f-223">4</span></span> | <span data-ttu-id="e032f-224">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e032f-224">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="e032f-225">Требования</span><span class="sxs-lookup"><span data-stu-id="e032f-225">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e032f-226">**Header**</span><span class="sxs-lookup"><span data-stu-id="e032f-226">**Header**</span></span> | <span data-ttu-id="e032f-227">директмл. h</span><span class="sxs-lookup"><span data-stu-id="e032f-227">directml.h</span></span> |