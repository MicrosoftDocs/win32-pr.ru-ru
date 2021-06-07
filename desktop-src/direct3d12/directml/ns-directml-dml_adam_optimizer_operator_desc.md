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
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418036"
---
# <a name="dml_adam_optimizer_operator_desc-structure-directmlh"></a><span data-ttu-id="2150a-104">Структура DML_ADAM_OPTIMIZER_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="2150a-104">DML_ADAM_OPTIMIZER_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="2150a-105">Выполняет вычисление обновленных весов (параметров) с помощью представленных градиентов на основе алгоритма ADAM (**ADA** птиве **M** омент оценкой).</span><span class="sxs-lookup"><span data-stu-id="2150a-105">Computes updated weights (parameters) using the supplied gradients, based on the Adam (**ADA** ptive **M** oment estimation) algorithm.</span></span> <span data-ttu-id="2150a-106">Этот оператор является оптимизатором и обычно используется на шаге обновления веса цикла обучения для выполнения спуска градиента.</span><span class="sxs-lookup"><span data-stu-id="2150a-106">This operator is an optimizer, and is typically used in the weight update step of a training loop to perform gradient descent.</span></span>

<span data-ttu-id="2150a-107">Этот оператор выполняет следующие вычисления:</span><span class="sxs-lookup"><span data-stu-id="2150a-107">This operator performs the following computation:</span></span>

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

<span data-ttu-id="2150a-108">Кроме вычисления обновленных параметров веса (возвращаемых в *аутпутпараметерстенсор*), этот оператор также возвращает обновленные первые и вторые оценки в *аутпутфирстмоменттенсор* и *аутпутсекондмоменттенсор* соответственно.</span><span class="sxs-lookup"><span data-stu-id="2150a-108">In addition to computing the updated weight parameters (returned in *OutputParametersTensor*), this operator also returns the updated first and second moment estimates in *OutputFirstMomentTensor* and *OutputSecondMomentTensor*, respectively.</span></span> <span data-ttu-id="2150a-109">Как правило, вы должны сохранить эти первые и вторые оценки и указать их в качестве входных данных на следующем этапе обучения.</span><span class="sxs-lookup"><span data-stu-id="2150a-109">Typically, you should store these first and second moment estimates, and supply them as inputs during the subsequent training step.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2150a-110">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="2150a-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="2150a-111">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="2150a-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2150a-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2150a-112">Syntax</span></span>
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

## <a name="members"></a><span data-ttu-id="2150a-113">Участники</span><span class="sxs-lookup"><span data-stu-id="2150a-113">Members</span></span>

`InputParametersTensor`

<span data-ttu-id="2150a-114">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2150a-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2150a-115">Объект тензорные, содержащий параметры (веса), к которым применяется этот оптимизатор.</span><span class="sxs-lookup"><span data-stu-id="2150a-115">A tensor containing the parameters (weights) to apply this optimizer to.</span></span> <span data-ttu-id="2150a-116">Оценка градиента, первого и второго времени, текущий шаг обучения, а также параметры *леарнинграте*, *Beta1* и *бета*, используются этим оператором для выполнения градиентной спуска по значениям веса, предоставленным в этом тензорные.</span><span class="sxs-lookup"><span data-stu-id="2150a-116">The gradient, first, and second moment estimates, current training step, as well as hyperparameters *LearningRate*, *Beta1*, and *Beta2*, are used by this operator to perform gradient descent on the weight values supplied in this tensor.</span></span>

`InputFirstMomentTensor`

<span data-ttu-id="2150a-117">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2150a-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2150a-118">Объект тензорные, содержащий первую оценку градиента для каждого значения веса.</span><span class="sxs-lookup"><span data-stu-id="2150a-118">A tensor containing the first moment estimate of the gradient for each weight value.</span></span> <span data-ttu-id="2150a-119">Эти значения обычно получаются в результате предыдущего выполнения этого оператора через *аутпутфирстмоменттенсор*.</span><span class="sxs-lookup"><span data-stu-id="2150a-119">These values are typically obtained as the result of a previous execution of this operator, via the *OutputFirstMomentTensor*.</span></span>

<span data-ttu-id="2150a-120">При первом применении этого оптимизатора к набору весовых коэффициентов (например, на этапе начального обучения) значения этого тензорные обычно инициализируются нулем.</span><span class="sxs-lookup"><span data-stu-id="2150a-120">When applying this optimizer to a set of weights for the first time (for example, during the initial training step) the values of this tensor should typically be initialized to zero.</span></span> <span data-ttu-id="2150a-121">Последующие выполнения должны использовать значения, возвращенные в *аутпутфирстмоменттенсор*.</span><span class="sxs-lookup"><span data-stu-id="2150a-121">Subsequent executions should use the values returned in *OutputFirstMomentTensor*.</span></span>

<span data-ttu-id="2150a-122">*Размеры* и *тип данных* этого тензорные должны точно соответствовать параметрам *инпутпараметерстенсор*.</span><span class="sxs-lookup"><span data-stu-id="2150a-122">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`InputSecondMomentTensor`

<span data-ttu-id="2150a-123">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2150a-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2150a-124">Объект тензорные, содержащий вторую оценку градиента для каждого значения веса.</span><span class="sxs-lookup"><span data-stu-id="2150a-124">A tensor containing the second moment estimate of the gradient for each weight value.</span></span> <span data-ttu-id="2150a-125">Эти значения обычно получаются в результате предыдущего выполнения этого оператора через *аутпутсекондмоменттенсор*.</span><span class="sxs-lookup"><span data-stu-id="2150a-125">These values are typically obtained as the result of a previous execution of this operator, via the *OutputSecondMomentTensor*.</span></span>

<span data-ttu-id="2150a-126">При первом применении этого оптимизатора к набору весовых коэффициентов (например, на этапе начального обучения) значения этого тензорные обычно инициализируются нулем.</span><span class="sxs-lookup"><span data-stu-id="2150a-126">When applying this optimizer to a set of weights for the first time (for example, during the initial training step) the values of this tensor should typically be initialized to zero.</span></span> <span data-ttu-id="2150a-127">Последующие выполнения должны использовать значения, возвращенные в *аутпутсекондмоменттенсор*.</span><span class="sxs-lookup"><span data-stu-id="2150a-127">Subsequent executions should use the values returned in *OutputSecondMomentTensor*.</span></span>

<span data-ttu-id="2150a-128">*Размеры* и *тип данных* этого тензорные должны точно соответствовать параметрам *инпутпараметерстенсор*.</span><span class="sxs-lookup"><span data-stu-id="2150a-128">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`GradientTensor`

<span data-ttu-id="2150a-129">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2150a-129">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2150a-130">Градиенты, применяемые к входным параметрам (весам) для спуска линий градиента.</span><span class="sxs-lookup"><span data-stu-id="2150a-130">The gradients to apply to the input parameters (weights) for gradient descent.</span></span> <span data-ttu-id="2150a-131">Градиенты обычно получаются при обратном распространении во время обучения.</span><span class="sxs-lookup"><span data-stu-id="2150a-131">Gradients are typically obtained in a backpropagation pass during training.</span></span>

<span data-ttu-id="2150a-132">*Размеры* и *тип данных* этого тензорные должны точно соответствовать параметрам *инпутпараметерстенсор*.</span><span class="sxs-lookup"><span data-stu-id="2150a-132">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`TrainingStepTensor`

<span data-ttu-id="2150a-133">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2150a-133">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2150a-134">Скалярный тензорные, содержащий одно целочисленное значение, представляющее текущее число шагов обучения.</span><span class="sxs-lookup"><span data-stu-id="2150a-134">A scalar tensor containing a single integer value representing the current training step count.</span></span> <span data-ttu-id="2150a-135">Это значение вместе с *Beta1* и *бета* -версией используется для вычисления экспоненциального decayа в первый и второй моменты оценки десятков.</span><span class="sxs-lookup"><span data-stu-id="2150a-135">This value along with *Beta1* and *Beta2* is used to compute the exponential decay of the first and second moment estimate tensors.</span></span>

<span data-ttu-id="2150a-136">Как правило, значение шага обучения начинается с 0 в начале обучения и увеличивается на 1 для каждого последующего этапа обучения.</span><span class="sxs-lookup"><span data-stu-id="2150a-136">Typically the training step value starts at 0 at the beginning of training, and is incremented by 1 on each successive training step.</span></span> <span data-ttu-id="2150a-137">Этот оператор не обновляет значение шага обучения; Это необходимо сделать вручную, например с помощью [DML_OPERATOR_ELEMENT_WISE_ADD](/windows/win32/api/directml/ns-directml-dml_element_wise_add_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="2150a-137">This operator doesn't update the training step value; you should do that manually, for example using [DML_OPERATOR_ELEMENT_WISE_ADD](/windows/win32/api/directml/ns-directml-dml_element_wise_add_operator_desc).</span></span>

<span data-ttu-id="2150a-138">Этот тензорные должен быть скалярным (то есть все *размеры* равны 1) и иметь тип данных [**DML_TENSOR_DATA_TYPE_UINT32**](/windows/win32/api/directml/ne-directml-dml_tensor_data_type).</span><span class="sxs-lookup"><span data-stu-id="2150a-138">This tensor must be a scalar (that is, all *Sizes* equal to 1) and have data type [**DML_TENSOR_DATA_TYPE_UINT32**](/windows/win32/api/directml/ne-directml-dml_tensor_data_type).</span></span>

`OutputParametersTensor`

<span data-ttu-id="2150a-139">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2150a-139">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2150a-140">Выходной тензорные, содержащий обновленные значения параметра (веса) после применения спуска градиента.</span><span class="sxs-lookup"><span data-stu-id="2150a-140">An output tensor that holds the updated parameter (weight) values after gradient descent is applied.</span></span>

<span data-ttu-id="2150a-141">Во время привязки этому тензорныеу может быть присвоен псевдоним подходящего входного тензорные, который можно использовать для выполнения обновления на месте этого тензорные.</span><span class="sxs-lookup"><span data-stu-id="2150a-141">During binding, this tensor is permitted to alias an eligible input tensor, which can be used to perform an in-place update of this tensor.</span></span> <span data-ttu-id="2150a-142">Дополнительные сведения см. в разделе ["Примечания"](#remarks) .</span><span class="sxs-lookup"><span data-stu-id="2150a-142">See the [Remarks](#remarks) section for more details.</span></span>

<span data-ttu-id="2150a-143">*Размеры* и *тип данных* этого тензорные должны точно соответствовать параметрам *инпутпараметерстенсор*.</span><span class="sxs-lookup"><span data-stu-id="2150a-143">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`OutputFirstMomentTensor`

<span data-ttu-id="2150a-144">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2150a-144">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2150a-145">Выходной тензорные, содержащий обновленные первые оценки.</span><span class="sxs-lookup"><span data-stu-id="2150a-145">An output tensor containing updated first moment estimates.</span></span> <span data-ttu-id="2150a-146">Вы должны сохранить значения этого тензорные и указать их в *инпутфирстмоменттенсор* на следующем этапе обучения.</span><span class="sxs-lookup"><span data-stu-id="2150a-146">You should store the values of this tensor, and supply them in *InputFirstMomentTensor* during the subsequent training step.</span></span>

<span data-ttu-id="2150a-147">Во время привязки этому тензорныеу может быть присвоен псевдоним подходящего входного тензорные, который можно использовать для выполнения обновления на месте этого тензорные.</span><span class="sxs-lookup"><span data-stu-id="2150a-147">During binding, this tensor is permitted to alias an eligible input tensor, which can be used to perform an in-place update of this tensor.</span></span> <span data-ttu-id="2150a-148">Дополнительные сведения см. в разделе ["Примечания"](#remarks) .</span><span class="sxs-lookup"><span data-stu-id="2150a-148">See the [Remarks](#remarks) section for more details.</span></span>

<span data-ttu-id="2150a-149">*Размеры* и *тип данных* этого тензорные должны точно соответствовать параметрам *инпутпараметерстенсор*.</span><span class="sxs-lookup"><span data-stu-id="2150a-149">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`OutputSecondMomentTensor`

<span data-ttu-id="2150a-150">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2150a-150">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2150a-151">Выходной тензорные, содержащий обновленные секунды оценки.</span><span class="sxs-lookup"><span data-stu-id="2150a-151">An output tensor containing updated second moment estimates.</span></span> <span data-ttu-id="2150a-152">Вы должны сохранить значения этого тензорные и указать их в *инпутсекондмоменттенсор* на следующем этапе обучения.</span><span class="sxs-lookup"><span data-stu-id="2150a-152">You should store the values of this tensor and supply them in *InputSecondMomentTensor* during the subsequent training step.</span></span>

<span data-ttu-id="2150a-153">Во время привязки этому тензорныеу может быть присвоен псевдоним подходящего входного тензорные, который можно использовать для выполнения обновления на месте этого тензорные.</span><span class="sxs-lookup"><span data-stu-id="2150a-153">During binding, this tensor is permitted to alias an eligible input tensor, which can be used to perform an in-place update of this tensor.</span></span> <span data-ttu-id="2150a-154">Дополнительные сведения см. в разделе ["Примечания"](#remarks) .</span><span class="sxs-lookup"><span data-stu-id="2150a-154">See the [Remarks](#remarks) section for more details.</span></span>

<span data-ttu-id="2150a-155">*Размеры* и *тип данных* этого тензорные должны точно соответствовать параметрам *инпутпараметерстенсор*.</span><span class="sxs-lookup"><span data-stu-id="2150a-155">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`LearningRate`

<span data-ttu-id="2150a-156">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="2150a-156">Type: **float**</span></span>

<span data-ttu-id="2150a-157">Темп обучения, который также часто называют *размером шага*.</span><span class="sxs-lookup"><span data-stu-id="2150a-157">The learning rate, also commonly referred to as the *step size*.</span></span> <span data-ttu-id="2150a-158">Скорость обучения — это параметр, определяющий величину обновления веса вдоль вектора градиента на каждом шаге обучения.</span><span class="sxs-lookup"><span data-stu-id="2150a-158">The learning rate is a hyperparameter that determines the magnitude of the weight update along the gradient vector on each training step.</span></span>

`Beta1`

<span data-ttu-id="2150a-159">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="2150a-159">Type: **float**</span></span>

<span data-ttu-id="2150a-160">Параметр «Decay», представляющий экспоненциальную коэффициент оценки в первый момент градиента.</span><span class="sxs-lookup"><span data-stu-id="2150a-160">A hyperparameter representing the exponential decay rate of the gradient's first moment estimate.</span></span> <span data-ttu-id="2150a-161">Это значение должно находиться в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="2150a-161">This value should be between 0.0 and 1.0.</span></span> <span data-ttu-id="2150a-162">Значение 0.9 f является типичным.</span><span class="sxs-lookup"><span data-stu-id="2150a-162">A value of 0.9f is typical.</span></span>

`Beta2`

<span data-ttu-id="2150a-163">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="2150a-163">Type: **float**</span></span>

<span data-ttu-id="2150a-164">Параметр "Decay", представляющий экспоненциальную частоту времени в секундах для градиента.</span><span class="sxs-lookup"><span data-stu-id="2150a-164">A hyperparameter representing the exponential decay rate of the gradient's second moment estimate.</span></span> <span data-ttu-id="2150a-165">Это значение должно находиться в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="2150a-165">This value should be between 0.0 and 1.0.</span></span> <span data-ttu-id="2150a-166">Значение 0,999 f является типичным.</span><span class="sxs-lookup"><span data-stu-id="2150a-166">A value of 0.999f is typical.</span></span>

`Epsilon`

<span data-ttu-id="2150a-167">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="2150a-167">Type: **float**</span></span>

<span data-ttu-id="2150a-168">Небольшое значение, используемое для обеспечения цифровой устойчивости, предотвращая деление на ноль.</span><span class="sxs-lookup"><span data-stu-id="2150a-168">A small value used to help numerical stability by preventing division-by-zero.</span></span> <span data-ttu-id="2150a-169">Для 32-разрядных входных данных с плавающей запятой типичные значения включают 1E-8 или `FLT_EPSILON` .</span><span class="sxs-lookup"><span data-stu-id="2150a-169">For 32-bit floating-point inputs, typical values include 1e-8 or `FLT_EPSILON`.</span></span>

## <a name="remarks"></a><span data-ttu-id="2150a-170">Remarks</span><span class="sxs-lookup"><span data-stu-id="2150a-170">Remarks</span></span>
<span data-ttu-id="2150a-171">Этот оператор поддерживает выполнение на месте, что означает, что каждому выходному тензорныеу может быть присвоен псевдоним подходящего входного тензорные во время привязки.</span><span class="sxs-lookup"><span data-stu-id="2150a-171">This operator supports in-place execution, meaning that each output tensor is permitted to alias an eligible input tensor during binding.</span></span> <span data-ttu-id="2150a-172">Например, можно привязать один и тот же ресурс для *инпутпараметерстенсор* и *аутпутпараметерстенсор* , чтобы обеспечить эффективное обновление входных параметров на месте.</span><span class="sxs-lookup"><span data-stu-id="2150a-172">For example, it's possible to bind the same resource for both the *InputParametersTensor* and *OutputParametersTensor* in order to effectively achieve an in-place update of the input parameters.</span></span> <span data-ttu-id="2150a-173">Все входные десятки этого оператора, за исключением *траинингстептенсор*, могут быть псевдонимами таким образом.</span><span class="sxs-lookup"><span data-stu-id="2150a-173">All of this operator's input tensors, with the exception of the *TrainingStepTensor*, are eligible to be aliased in this way.</span></span>

## <a name="availability"></a><span data-ttu-id="2150a-174">Доступность</span><span class="sxs-lookup"><span data-stu-id="2150a-174">Availability</span></span>
<span data-ttu-id="2150a-175">Этот оператор появился в `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="2150a-175">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="2150a-176">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="2150a-176">Tensor constraints</span></span>
* <span data-ttu-id="2150a-177">*Градиенттенсор*, *инпутфирстмоменттенсор*, *инпутпараметерстенсор*, *инпутсекондмоменттенсор*, *OutputFirstMomentTensor*, *OutputParametersTensor*, *OutputSecondMomentTensor* и *TrainingStepTensor* должны иметь одинаковый *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="2150a-177">*GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor*, *OutputSecondMomentTensor*, and *TrainingStepTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="2150a-178">*Градиенттенсор*, *инпутфирстмоменттенсор*, *инпутпараметерстенсор*, *инпутсекондмоменттенсор*, *OutputFirstMomentTensor*, *OutputParametersTensor* и *OutputSecondMomentTensor* должны иметь одинаковые *размеры*.</span><span class="sxs-lookup"><span data-stu-id="2150a-178">*GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor*, and *OutputSecondMomentTensor* must have the same *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="2150a-179">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="2150a-179">Tensor support</span></span>
| <span data-ttu-id="2150a-180">Тензорные</span><span class="sxs-lookup"><span data-stu-id="2150a-180">Tensor</span></span> | <span data-ttu-id="2150a-181">Вид</span><span class="sxs-lookup"><span data-stu-id="2150a-181">Kind</span></span> | <span data-ttu-id="2150a-182">Измерения</span><span class="sxs-lookup"><span data-stu-id="2150a-182">Dimensions</span></span> | <span data-ttu-id="2150a-183">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="2150a-183">Supported dimension counts</span></span> | <span data-ttu-id="2150a-184">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="2150a-184">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="2150a-185">инпутпараметерстенсор</span><span class="sxs-lookup"><span data-stu-id="2150a-185">InputParametersTensor</span></span> | <span data-ttu-id="2150a-186">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2150a-186">Input</span></span> | <span data-ttu-id="2150a-187">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="2150a-187">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="2150a-188">4</span><span class="sxs-lookup"><span data-stu-id="2150a-188">4</span></span> | <span data-ttu-id="2150a-189">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="2150a-189">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="2150a-190">инпутфирстмоменттенсор</span><span class="sxs-lookup"><span data-stu-id="2150a-190">InputFirstMomentTensor</span></span> | <span data-ttu-id="2150a-191">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2150a-191">Input</span></span> | <span data-ttu-id="2150a-192">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="2150a-192">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="2150a-193">4</span><span class="sxs-lookup"><span data-stu-id="2150a-193">4</span></span> | <span data-ttu-id="2150a-194">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="2150a-194">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="2150a-195">инпутсекондмоменттенсор</span><span class="sxs-lookup"><span data-stu-id="2150a-195">InputSecondMomentTensor</span></span> | <span data-ttu-id="2150a-196">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2150a-196">Input</span></span> | <span data-ttu-id="2150a-197">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="2150a-197">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="2150a-198">4</span><span class="sxs-lookup"><span data-stu-id="2150a-198">4</span></span> | <span data-ttu-id="2150a-199">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="2150a-199">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="2150a-200">градиенттенсор</span><span class="sxs-lookup"><span data-stu-id="2150a-200">GradientTensor</span></span> | <span data-ttu-id="2150a-201">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2150a-201">Input</span></span> | <span data-ttu-id="2150a-202">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="2150a-202">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="2150a-203">4</span><span class="sxs-lookup"><span data-stu-id="2150a-203">4</span></span> | <span data-ttu-id="2150a-204">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="2150a-204">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="2150a-205">траинингстептенсор</span><span class="sxs-lookup"><span data-stu-id="2150a-205">TrainingStepTensor</span></span> | <span data-ttu-id="2150a-206">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2150a-206">Input</span></span> | <span data-ttu-id="2150a-207">{1, 1, 1, 1}</span><span class="sxs-lookup"><span data-stu-id="2150a-207">{ 1, 1, 1, 1 }</span></span> | <span data-ttu-id="2150a-208">4</span><span class="sxs-lookup"><span data-stu-id="2150a-208">4</span></span> | <span data-ttu-id="2150a-209">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="2150a-209">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="2150a-210">аутпутпараметерстенсор</span><span class="sxs-lookup"><span data-stu-id="2150a-210">OutputParametersTensor</span></span> | <span data-ttu-id="2150a-211">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="2150a-211">Output</span></span> | <span data-ttu-id="2150a-212">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="2150a-212">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="2150a-213">4</span><span class="sxs-lookup"><span data-stu-id="2150a-213">4</span></span> | <span data-ttu-id="2150a-214">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="2150a-214">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="2150a-215">аутпутфирстмоменттенсор</span><span class="sxs-lookup"><span data-stu-id="2150a-215">OutputFirstMomentTensor</span></span> | <span data-ttu-id="2150a-216">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="2150a-216">Output</span></span> | <span data-ttu-id="2150a-217">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="2150a-217">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="2150a-218">4</span><span class="sxs-lookup"><span data-stu-id="2150a-218">4</span></span> | <span data-ttu-id="2150a-219">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="2150a-219">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="2150a-220">аутпутсекондмоменттенсор</span><span class="sxs-lookup"><span data-stu-id="2150a-220">OutputSecondMomentTensor</span></span> | <span data-ttu-id="2150a-221">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="2150a-221">Output</span></span> | <span data-ttu-id="2150a-222">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="2150a-222">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="2150a-223">4</span><span class="sxs-lookup"><span data-stu-id="2150a-223">4</span></span> | <span data-ttu-id="2150a-224">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="2150a-224">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="2150a-225">Требования</span><span class="sxs-lookup"><span data-stu-id="2150a-225">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="2150a-226">**Header**</span><span class="sxs-lookup"><span data-stu-id="2150a-226">**Header**</span></span> | <span data-ttu-id="2150a-227">директмл. h</span><span class="sxs-lookup"><span data-stu-id="2150a-227">directml.h</span></span> |