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
# <a name="using-fused-operators-to-improve-performance"></a>Использование совмещенных операторов для повышения производительности

Некоторые операторы Директмл поддерживают концепцию, известную как *Fusion*. Fusion оператора — это способ повышения производительности путем слияния одного оператора (как правило, функции активации) к другому оператору, чтобы они выполнялись вместе без необходимости обмена данными с памятью.

## <a name="when-to-fuse-activations"></a>Когда следует запредохранительить активацию

Активация с плавким предохранителем — это оптимизация производительности. Очень распространенным сценарием во многих моделях машинного обучения является применение нелинейности (функции активации) к выходным данным каждого слоя в модели.

Обычно это требует обмена данными с графической памятью. Например, если за свертыванием следует активация Релу без предохранителя, то GPU должен подождать, пока результаты свертки будут записаны в память GPU, прежде чем он сможет начать вычисление уровня активации Релу. Так как вычислительная нагрузка большинства функций активации, как правило, невелика, такой обмен данными с графической памятью может быть узким местом производительности.

Функция Fusion позволяет выполнять функцию активации (Релу в приведенном выше примере) как часть предыдущего оператора (например, свертки). Это позволяет GPU вычислять функцию активации, не дожидаясь, пока результаты предыдущего оператора не будут записаны в память, &mdash; что повышает производительность.

Так как активация с помощью плавких предохранителей дает тот же результат, но они выполняются быстрее во многих случаях, рекомендуется исключать уровни активации, отключая их к предшествующему оператору везде, где это возможно.

## <a name="how-to-fuse-activations"></a>Как выполнить плавкий активацию

Операторы, поддерживающие активацию с плавким предохранителем, имеют дополнительный необязательный параметр в структуре операторов `const DML_OPERATOR_DESC* FusedActivation` . Пример свертки, например, поддерживает активацию с плавким предохранителем и имеет соответствующий *фуседактиватион* в описании оператора (см. [DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)).

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

Чтобы запредохранительить активацию, создайте [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) , описывающий тип активации с плавким предохранителем. Например, для плавкий функции Релу правильный тип оператора будет [DML_OPERATOR_ACTIVATION_RELU](/windows/win32/api/directml/ne-directml-dml_operator_type).

> [!NOTE]
> При конструировании описания оператора для функции активации необходимо установить параметры *инпуттенсор* и *аутпуттенсор* для функции активации в **значение NULL**.

## <a name="example"></a>Пример

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

В качестве полного примера [Пример директмлсуперресолутион](https://github.com/microsoft/DirectML/tree/master/Samples) использует активацию с плавким предохранителем для повышения производительности.

## <a name="operators-that-support-fused-activation"></a>Операторы, поддерживающие активацию с плавким предохранителем

* [DML_OPERATOR_CONVOLUTION](/windows/win32/api/directml/ne-directml-dml_operator_type)
* **DML_OPERATOR_GEMM**
* **DML_OPERATOR_BATCH_NORMALIZATION**
* **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION** и **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**
* **DML_OPERATOR_ELEMENT_WISE_ADD1**

## <a name="activations-that-are-supported-for-fusion"></a>Активации, которые поддерживаются для Fusion

* [DML_OPERATOR_ACTIVATION_ELU](/windows/win32/api/directml/ne-directml-dml_operator_type)
* **DML_OPERATOR_ACTIVATION_HARD_SIGMOID**
* **DML_OPERATOR_ACTIVATION_IDENTITY**
* **DML_OPERATOR_ACTIVATION_LEAKY_RELU**
* **DML_OPERATOR_ACTIVATION_LINEAR**
* **DML_OPERATOR_ACTIVATION_PARAMETRIC_SOFTPLUS**
* **DML_OPERATOR_ACTIVATION_RELU**
* **DML_OPERATOR_ACTIVATION_SCALED_ELU**
* **DML_OPERATOR_ACTIVATION_SCALED_TANH**
* **DML_OPERATOR_ACTIVATION_SIGMOID**
* **DML_OPERATOR_ACTIVATION_SOFTPLUS**
* **DML_OPERATOR_ACTIVATION_SOFTSIGN**
* **DML_OPERATOR_ACTIVATION_TANH**
* **DML_OPERATOR_ACTIVATION_THRESHOLDED_RELU**
* **DML_OPERATOR_ACTIVATION_SHRINK**
* **DML_OPERATOR_ACTIVATION_CELU**

Ни один из операторов, отсутствующих в этом списке, не поддерживает активацию с плавким предохранителем.

## <a name="see-also"></a>См. также раздел

* [Пример Директмлсуперресолутион](https://github.com/microsoft/DirectML/tree/master/Samples)    
* [DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)
