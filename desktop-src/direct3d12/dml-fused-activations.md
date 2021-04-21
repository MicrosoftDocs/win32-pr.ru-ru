---
title: Использование совмещенных операторов для повышения производительности
description: Некоторые операторы Директмл поддерживают концепцию, известную как *Fusion*. Fusion оператора — это способ повышения производительности путем слияния одного оператора (как правило, функции активации) к другому оператору, чтобы они выполнялись вместе без необходимости обмена данными с памятью.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: bba4a9d0ef5c69976a5a344432bf82d31b00c0c7
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803992"
---
# <a name="using-fused-operators-to-improve-performance"></a><span data-ttu-id="94e21-104">Использование совмещенных операторов для повышения производительности</span><span class="sxs-lookup"><span data-stu-id="94e21-104">Using fused operators to improve performance</span></span>

<span data-ttu-id="94e21-105">Некоторые операторы Директмл поддерживают концепцию, известную как *Fusion*.</span><span class="sxs-lookup"><span data-stu-id="94e21-105">Some DirectML operators support a concept known as *fusion*.</span></span> <span data-ttu-id="94e21-106">Fusion оператора — это способ повышения производительности путем слияния одного оператора (как правило, функции активации) к другому оператору, чтобы они выполнялись вместе без необходимости обмена данными с памятью.</span><span class="sxs-lookup"><span data-stu-id="94e21-106">Operator fusion is a way to improve performance by merging one operator (typically, an activation function) into a different operator so that they are executed together without requiring a roundtrip to memory.</span></span>

## <a name="when-to-fuse-activations"></a><span data-ttu-id="94e21-107">Когда следует запредохранительить активацию</span><span class="sxs-lookup"><span data-stu-id="94e21-107">When to fuse activations</span></span>

<span data-ttu-id="94e21-108">Активация с плавким предохранителем — это оптимизация производительности.</span><span class="sxs-lookup"><span data-stu-id="94e21-108">Fused activations are a performance optimization.</span></span> <span data-ttu-id="94e21-109">Очень распространенным сценарием во многих моделях машинного обучения является применение нелинейности (функции активации) к выходным данным каждого слоя в модели.</span><span class="sxs-lookup"><span data-stu-id="94e21-109">An extremely common scenario in many machine learning (ML) models is to apply a nonlinearity (an activation function) to the output of each layer in the model.</span></span>

<span data-ttu-id="94e21-110">Обычно это требует обмена данными с графической памятью.</span><span class="sxs-lookup"><span data-stu-id="94e21-110">Ordinarily, this requires a roundtrip to graphics memory.</span></span> <span data-ttu-id="94e21-111">Например, если за свертыванием следует активация Релу без предохранителя, то GPU должен подождать, пока результаты свертки будут записаны в память GPU, прежде чем он сможет начать вычисление уровня активации Релу.</span><span class="sxs-lookup"><span data-stu-id="94e21-111">For example if a Convolution is followed by a non-fused Relu activation, then the GPU must wait for the results of the Convolution to be written into GPU memory before it can begin computing the Relu activation layer.</span></span> <span data-ttu-id="94e21-112">Так как вычислительная нагрузка большинства функций активации, как правило, невелика, такой обмен данными с графической памятью может быть узким местом производительности.</span><span class="sxs-lookup"><span data-stu-id="94e21-112">As the compute workload of most activation functions tends to be small, this roundtrip to graphics memory can be a major performance bottleneck.</span></span>

<span data-ttu-id="94e21-113">Функция Fusion позволяет выполнять функцию активации (Релу в приведенном выше примере) как часть предыдущего оператора (например, свертки).</span><span class="sxs-lookup"><span data-stu-id="94e21-113">Operator fusion allows the activation function (Relu in the above example) to be performed as part of the preceding operator (Convolution, for example).</span></span> <span data-ttu-id="94e21-114">Это позволяет GPU вычислять функцию активации, не дожидаясь, пока результаты предыдущего оператора не будут записаны в память, &mdash; что повышает производительность.</span><span class="sxs-lookup"><span data-stu-id="94e21-114">This allows the GPU to compute the activation function without waiting for the results of the preceding operator to be written into memory&mdash;and that improves performance.</span></span>

<span data-ttu-id="94e21-115">Так как активация с помощью плавких предохранителей дает тот же результат, но они выполняются быстрее во многих случаях, рекомендуется исключать уровни активации, отключая их к предшествующему оператору везде, где это возможно.</span><span class="sxs-lookup"><span data-stu-id="94e21-115">Because fused activations produce the same result, but are faster in many cases, we recommend that you eliminate activation layers by fusing them into their preceding operator wherever possible.</span></span>

## <a name="how-to-fuse-activations"></a><span data-ttu-id="94e21-116">Как выполнить плавкий активацию</span><span class="sxs-lookup"><span data-stu-id="94e21-116">How to fuse activations</span></span>

<span data-ttu-id="94e21-117">Операторы, поддерживающие активацию с плавким предохранителем, имеют дополнительный необязательный параметр в структуре операторов `const DML_OPERATOR_DESC* FusedActivation` .</span><span class="sxs-lookup"><span data-stu-id="94e21-117">Operators that support fused activations have an additional optional parameter in their operator struct, `const DML_OPERATOR_DESC* FusedActivation`.</span></span> <span data-ttu-id="94e21-118">Пример свертки, например, поддерживает активацию с плавким предохранителем и имеет соответствующий *фуседактиватион* в описании оператора (см. [DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="94e21-118">Convolution, for example, supports fused activation, and it has a corresponding *FusedActivation* in its operator description (see [DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)).</span></span>

```cpp
struct DML_CONVOLUTION_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* FilterTensor;
    \_Maybenull\_ const DML_TENSOR_DESC* BiasTensor;
    const DML_TENSOR_DESC* OutputTensor;
    DML_CONVOLUTION_MODE Mode;
    DML_CONVOLUTION_DIRECTION Direction;
    UINT DimensionCount;
    _Field_size_(DimensionCount) const UINT* Strides;
    _Field_size_(DimensionCount) const UINT* Dilations;
    _Field_size_(DimensionCount) const UINT* StartPadding;
    _Field_size_(DimensionCount) const UINT* EndPadding;
    _Field_size_(DimensionCount) const UINT* OutputPadding;
    UINT GroupCount;
    \_Maybenull\_ const DML_OPERATOR_DESC* FusedActivation;
};
```

<span data-ttu-id="94e21-119">Чтобы запредохранительить активацию, создайте [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) , описывающий тип активации с плавким предохранителем.</span><span class="sxs-lookup"><span data-stu-id="94e21-119">To fuse an activation, construct a [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) that describes the type of activation to be fused.</span></span> <span data-ttu-id="94e21-120">Например, для плавкий функции Релу правильный тип оператора будет [DML_OPERATOR_ACTIVATION_RELU](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="94e21-120">For example to fuse a Relu function, the correct operator type would be [DML_OPERATOR_ACTIVATION_RELU](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span>

> [!NOTE]
> <span data-ttu-id="94e21-121">При конструировании описания оператора для функции активации необходимо установить параметры *инпуттенсор* и *аутпуттенсор* для функции активации в **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="94e21-121">When constructing the operator description for the activation function, you must set the *InputTensor* and *OutputTensor* parameters for the activation function to **NULL**.</span></span>

## <a name="example"></a><span data-ttu-id="94e21-122">Пример</span><span class="sxs-lookup"><span data-stu-id="94e21-122">Example</span></span>

```cpp
DML_ACTIVATION_LEAKY_RELU_OPERATOR_DESC leakyReluDesc;
leakyReluDesc.InputTensor = nullptr;
leakyReluDesc.OutputTensor = nullptr;
leakyReluDesc.Alpha = 0.01f;

DML_OPERATOR_DESC activationDesc = { DML_OPERATOR_ACTIVATION_LEAKY_RELU, &leakyReluDesc };

DML_CONVOLUTION_OPERATOR_DESC convDesc;
// ...
convDesc.FusedActivation = &activationDesc;
```

<span data-ttu-id="94e21-123">В качестве полного примера [Пример директмлсуперресолутион](https://github.com/microsoft/DirectML/tree/master/Samples) использует активацию с плавким предохранителем для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="94e21-123">For a complete example, the [DirectMLSuperResolution sample](https://github.com/microsoft/DirectML/tree/master/Samples) utilizes fused activations to improve performance.</span></span>

## <a name="operators-that-support-fused-activation"></a><span data-ttu-id="94e21-124">Операторы, поддерживающие активацию с плавким предохранителем</span><span class="sxs-lookup"><span data-stu-id="94e21-124">Operators that support fused activation</span></span>

* [<span data-ttu-id="94e21-125">DML_OPERATOR_CONVOLUTION</span><span class="sxs-lookup"><span data-stu-id="94e21-125">DML_OPERATOR_CONVOLUTION</span></span>](/windows/win32/api/directml/ne-directml-dml_operator_type)
* <span data-ttu-id="94e21-126">**DML_OPERATOR_GEMM**</span><span class="sxs-lookup"><span data-stu-id="94e21-126">**DML_OPERATOR_GEMM**</span></span>
* <span data-ttu-id="94e21-127">**DML_OPERATOR_BATCH_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="94e21-127">**DML_OPERATOR_BATCH_NORMALIZATION**</span></span>
* <span data-ttu-id="94e21-128">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION** и **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="94e21-128">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION** and **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="94e21-129">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span><span class="sxs-lookup"><span data-stu-id="94e21-129">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span></span>

## <a name="activations-that-are-supported-for-fusion"></a><span data-ttu-id="94e21-130">Активации, которые поддерживаются для Fusion</span><span class="sxs-lookup"><span data-stu-id="94e21-130">Activations that are supported for fusion</span></span>

* [<span data-ttu-id="94e21-131">DML_OPERATOR_ACTIVATION_ELU</span><span class="sxs-lookup"><span data-stu-id="94e21-131">DML_OPERATOR_ACTIVATION_ELU</span></span>](/windows/win32/api/directml/ne-directml-dml_operator_type)
* <span data-ttu-id="94e21-132">**DML_OPERATOR_ACTIVATION_HARD_SIGMOID**</span><span class="sxs-lookup"><span data-stu-id="94e21-132">**DML_OPERATOR_ACTIVATION_HARD_SIGMOID**</span></span>
* <span data-ttu-id="94e21-133">**DML_OPERATOR_ACTIVATION_IDENTITY**</span><span class="sxs-lookup"><span data-stu-id="94e21-133">**DML_OPERATOR_ACTIVATION_IDENTITY**</span></span>
* <span data-ttu-id="94e21-134">**DML_OPERATOR_ACTIVATION_LEAKY_RELU**</span><span class="sxs-lookup"><span data-stu-id="94e21-134">**DML_OPERATOR_ACTIVATION_LEAKY_RELU**</span></span>
* <span data-ttu-id="94e21-135">**DML_OPERATOR_ACTIVATION_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="94e21-135">**DML_OPERATOR_ACTIVATION_LINEAR**</span></span>
* <span data-ttu-id="94e21-136">**DML_OPERATOR_ACTIVATION_PARAMETRIC_SOFTPLUS**</span><span class="sxs-lookup"><span data-stu-id="94e21-136">**DML_OPERATOR_ACTIVATION_PARAMETRIC_SOFTPLUS**</span></span>
* <span data-ttu-id="94e21-137">**DML_OPERATOR_ACTIVATION_RELU**</span><span class="sxs-lookup"><span data-stu-id="94e21-137">**DML_OPERATOR_ACTIVATION_RELU**</span></span>
* <span data-ttu-id="94e21-138">**DML_OPERATOR_ACTIVATION_SCALED_ELU**</span><span class="sxs-lookup"><span data-stu-id="94e21-138">**DML_OPERATOR_ACTIVATION_SCALED_ELU**</span></span>
* <span data-ttu-id="94e21-139">**DML_OPERATOR_ACTIVATION_SCALED_TANH**</span><span class="sxs-lookup"><span data-stu-id="94e21-139">**DML_OPERATOR_ACTIVATION_SCALED_TANH**</span></span>
* <span data-ttu-id="94e21-140">**DML_OPERATOR_ACTIVATION_SIGMOID**</span><span class="sxs-lookup"><span data-stu-id="94e21-140">**DML_OPERATOR_ACTIVATION_SIGMOID**</span></span>
* <span data-ttu-id="94e21-141">**DML_OPERATOR_ACTIVATION_SOFTPLUS**</span><span class="sxs-lookup"><span data-stu-id="94e21-141">**DML_OPERATOR_ACTIVATION_SOFTPLUS**</span></span>
* <span data-ttu-id="94e21-142">**DML_OPERATOR_ACTIVATION_SOFTSIGN**</span><span class="sxs-lookup"><span data-stu-id="94e21-142">**DML_OPERATOR_ACTIVATION_SOFTSIGN**</span></span>
* <span data-ttu-id="94e21-143">**DML_OPERATOR_ACTIVATION_TANH**</span><span class="sxs-lookup"><span data-stu-id="94e21-143">**DML_OPERATOR_ACTIVATION_TANH**</span></span>
* <span data-ttu-id="94e21-144">**DML_OPERATOR_ACTIVATION_THRESHOLDED_RELU**</span><span class="sxs-lookup"><span data-stu-id="94e21-144">**DML_OPERATOR_ACTIVATION_THRESHOLDED_RELU**</span></span>
* <span data-ttu-id="94e21-145">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="94e21-145">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
* <span data-ttu-id="94e21-146">**DML_OPERATOR_ACTIVATION_CELU**</span><span class="sxs-lookup"><span data-stu-id="94e21-146">**DML_OPERATOR_ACTIVATION_CELU**</span></span>

<span data-ttu-id="94e21-147">Ни один из операторов, отсутствующих в этом списке, не поддерживает активацию с плавким предохранителем.</span><span class="sxs-lookup"><span data-stu-id="94e21-147">Any operators not in this list are not supported for fused activation.</span></span>

## <a name="see-also"></a><span data-ttu-id="94e21-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94e21-148">See also</span></span>

* [<span data-ttu-id="94e21-149">Пример Директмлсуперресолутион</span><span class="sxs-lookup"><span data-stu-id="94e21-149">DirectMLSuperResolution sample</span></span>](https://github.com/microsoft/DirectML/tree/master/Samples)    
* [<span data-ttu-id="94e21-150">DML_CONVOLUTION_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="94e21-150">DML_CONVOLUTION_OPERATOR_DESC</span></span>](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)
