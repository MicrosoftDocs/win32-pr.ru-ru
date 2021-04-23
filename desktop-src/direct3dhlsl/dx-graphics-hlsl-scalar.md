---
title: Скалярные типы
description: Скалярные типы
ms.assetid: bf24d27f-2720-4268-bc74-fc46afedb9aa
keywords:
- Скалярные типы HLSL
topic_type:
- apiref
api_name:
- Scalar Types
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: 7198932c6edb91e6f797b232b6c980976f3696a7
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "103820884"
---
# <a name="scalar-types"></a><span data-ttu-id="59959-104">Скалярные типы</span><span class="sxs-lookup"><span data-stu-id="59959-104">Scalar Types</span></span>


<span data-ttu-id="59959-105">HLSL поддерживает несколько скалярных типов данных:</span><span class="sxs-lookup"><span data-stu-id="59959-105">HLSL supports several scalar data types:</span></span>

-   <span data-ttu-id="59959-106">**bool** — true или false.</span><span class="sxs-lookup"><span data-stu-id="59959-106">**bool** - true or false.</span></span>
-   <span data-ttu-id="59959-107">**int** -32-разрядное целое число со знаком.</span><span class="sxs-lookup"><span data-stu-id="59959-107">**int** - 32-bit signed integer.</span></span>
-   <span data-ttu-id="59959-108">**uint** -32-битовое целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="59959-108">**uint** - 32-bit unsigned integer.</span></span>
-   <span data-ttu-id="59959-109">**DWORD** -32-битовое целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="59959-109">**dword** - 32-bit unsigned integer.</span></span>
-   <span data-ttu-id="59959-110">**половина** 16-битного значения с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="59959-110">**half** - 16-bit floating point value.</span></span> <span data-ttu-id="59959-111">Этот тип данных предоставляется только для совместимости с языком.</span><span class="sxs-lookup"><span data-stu-id="59959-111">This data type is provided only for language compatibility.</span></span> <span data-ttu-id="59959-112">Цели шейдера Direct3D 10 сопоставляют все половинные типы данных с типами данных float.</span><span class="sxs-lookup"><span data-stu-id="59959-112">Direct3D 10 shader targets map all half data types to float data types.</span></span> <span data-ttu-id="59959-113">Половина типа данных не может быть использована для равномерной глобальной переменной (используйте флаг/ЖЕК, если требуется эта функция).</span><span class="sxs-lookup"><span data-stu-id="59959-113">A half data type cannot be used on a uniform global variable (use the /Gec flag if this functionality is desired).</span></span>
-   <span data-ttu-id="59959-114">**float** -32-разрядное значение с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="59959-114">**float** - 32-bit floating point value.</span></span>
-   <span data-ttu-id="59959-115">**двойное** 64-разрядное значение с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="59959-115">**double** - 64-bit floating point value.</span></span> <span data-ttu-id="59959-116">Значения двойной точности нельзя использовать в качестве входных и выходных данных для потока.</span><span class="sxs-lookup"><span data-stu-id="59959-116">You cannot use double precision values as inputs and outputs for a stream.</span></span> <span data-ttu-id="59959-117">Чтобы передать значения двойной точности между шейдерами, объявите каждое значение **Double** как пару типов данных **uint** .</span><span class="sxs-lookup"><span data-stu-id="59959-117">To pass double precision values between shaders, declare each **double** as a pair of **uint** data types.</span></span> <span data-ttu-id="59959-118">Затем используйте функцию [**асуинт**](asuint.md) для упаковки каждого **типа Double** в пару **uint** и функции [**асдаубле**](asdouble.md) для распаковки пары **uint** s обратно в **Double**.</span><span class="sxs-lookup"><span data-stu-id="59959-118">Then, use the [**asuint**](asuint.md) function to pack each **double** into the pair of **uint** s and the [**asdouble**](asdouble.md) function to unpack the pair of **uint** s back into the **double**.</span></span>

<span data-ttu-id="59959-119">Начиная с Windows 8 HLSL также поддерживает скалярные типы данных минимальной точности.</span><span class="sxs-lookup"><span data-stu-id="59959-119">Starting with Windows 8 HLSL also supports minimum precision scalar data types.</span></span> <span data-ttu-id="59959-120">Графические драйверы могут реализовывать скалярные типы данных минимальной точности, используя любую точность, которая больше или равна заданной точности разрядов.</span><span class="sxs-lookup"><span data-stu-id="59959-120">Graphics drivers can implement minimum precision scalar data types by using any precision greater than or equal to their specified bit precision.</span></span> <span data-ttu-id="59959-121">Не рекомендуется полагаться на поведение фиксации или упаковки, зависящее от конкретной точности.</span><span class="sxs-lookup"><span data-stu-id="59959-121">We recommend not to rely on clamping or wrapping behavior that depends on specific underlying precision.</span></span> <span data-ttu-id="59959-122">Например, графический драйвер может выполнять арифметические вычисления со значением **min16float** при полной 32-разрядной точности.</span><span class="sxs-lookup"><span data-stu-id="59959-122">For example, the graphics driver might execute arithmetic on a **min16float** value at full 32-bit precision.</span></span>

-   <span data-ttu-id="59959-123">**min16float** — минимальное 16-разрядное значение с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="59959-123">**min16float** - minimum 16-bit floating point value.</span></span>
-   <span data-ttu-id="59959-124">**min10float** — минимальное 10-разрядное значение с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="59959-124">**min10float** - minimum 10-bit floating point value.</span></span>
-   <span data-ttu-id="59959-125">**min16int** — минимальное 16-разрядное целое число со знаком.</span><span class="sxs-lookup"><span data-stu-id="59959-125">**min16int** - minimum 16-bit signed integer.</span></span>
-   <span data-ttu-id="59959-126">**min12int** — минимальное 12-разрядное целое число со знаком.</span><span class="sxs-lookup"><span data-stu-id="59959-126">**min12int** - minimum 12-bit signed integer.</span></span>
-   <span data-ttu-id="59959-127">**min16uint** — минимальное 16-разрядное целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="59959-127">**min16uint** - minimum 16-bit unsigned integer.</span></span>

<span data-ttu-id="59959-128">Дополнительные сведения о скалярных литералах см. в разделе [грамматика](dx-graphics-hlsl-appendix-grammar.md).</span><span class="sxs-lookup"><span data-stu-id="59959-128">For more information about scalar literals, see [Grammar](dx-graphics-hlsl-appendix-grammar.md).</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="59959-129">Различия между Direct3D 9 и Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="59959-129">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="59959-130">В Direct3D 10 к типу float применяются модификаторы следующих типов.</span><span class="sxs-lookup"><span data-stu-id="59959-130">In Direct3D 10, the following types are modifiers to the float type.</span></span><br/>
<ul>
<li><span data-ttu-id="59959-131"><strong>снорм float</strong> - IEEE 32-bit-разрядное число с нормализованным входом в диапазоне от 1 до 1 включительно.</span><span class="sxs-lookup"><span data-stu-id="59959-131"><strong>snorm float</strong> - IEEE 32-bit signed-normalized float in range -1 to 1 inclusive.</span></span></li>
<li><span data-ttu-id="59959-132"><strong>unorm float</strong> - IEEE 32-bit без знака, нормализованное значение с плавающей запятой в диапазоне от 0 до 1 включительно.</span><span class="sxs-lookup"><span data-stu-id="59959-132"><strong>unorm float</strong> - IEEE 32-bit unsigned-normalized float in range 0 to 1 inclusive.</span></span></li>
</ul>
<span data-ttu-id="59959-133">Например, ниже приведено 4-компонентное объявление переменной с плавающей запятой с помощью четырех компонентов.</span><span class="sxs-lookup"><span data-stu-id="59959-133">For example, here is a 4-component signed-normalized float-variable declaration.</span></span><br/> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>snorm float4 fourComponentIEEEFloat;</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



 

## <a name="string-type"></a><span data-ttu-id="59959-134">Тип строки</span><span class="sxs-lookup"><span data-stu-id="59959-134">String Type</span></span>

<span data-ttu-id="59959-135">HLSL также поддерживает **строковый** тип, который является строкой ASCII.</span><span class="sxs-lookup"><span data-stu-id="59959-135">HLSL also supports a **string** type, which is an ASCII string.</span></span> <span data-ttu-id="59959-136">Нет операций или состояний, принимающих строки, но эффекты могут запрашивать параметры строки и аннотации.</span><span class="sxs-lookup"><span data-stu-id="59959-136">There are no operations or states that accept strings, but effects can query string parameters and annotations.</span></span>

## <a name="example"></a><span data-ttu-id="59959-137">Пример</span><span class="sxs-lookup"><span data-stu-id="59959-137">Example</span></span>

```c
// top-level variable
float globalShaderVariable; 

// top-level function
void function(
in float4 position: POSITION0 // top-level argument
              )
{
  float localShaderVariable; // local variable
  function2(...)
}

void function2()
{
  ...
}
```

## <a name="see-also"></a><span data-ttu-id="59959-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59959-138">See also</span></span>



* [<span data-ttu-id="59959-139">Объявление скалярных типов</span><span class="sxs-lookup"><span data-stu-id="59959-139">Declaring Scalar Types</span></span>](./dx-graphics-hlsl-writing-shaders-9.md#declaring-shader-variables)
* [<span data-ttu-id="59959-140">Типы данных (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="59959-140">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)