---
title: Массивы (RPC) (TFS)
description: Категории массива удаленного вызова процедур (RPC) включают в себя фиксированный размер, согласованность, различные, различные и сложные.
ms.assetid: 7144ec87-90f2-463a-80e4-28cb4771325f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d564a2dfd838006be1667343b14a57bdaf4b07
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388816"
---
# <a name="arrays-rpc"></a><span data-ttu-id="66adc-103">Массивы (RPC)</span><span class="sxs-lookup"><span data-stu-id="66adc-103">Arrays (RPC)</span></span>

<span data-ttu-id="66adc-104">Несколько категорий массивов определены на основе их характеристик производительности, в основном, можно ли копировать массив в блок.</span><span class="sxs-lookup"><span data-stu-id="66adc-104">Several array categories have been defined based on their performance characteristics, primarily whether the array can be block-copied.</span></span>

<span data-ttu-id="66adc-105">Для некоторых категорий, таких как массив фиксированного размера, существует два типа дескрипторов массива. они обозначаются неисправностью в названии ведущего маркера FC.</span><span class="sxs-lookup"><span data-stu-id="66adc-105">For some categories, such as a fixed-size array, two types of array descriptors exist; they are indicated by an in-fix in the name of the leading FC token.</span></span>



| <span data-ttu-id="66adc-106">Символ формата</span><span class="sxs-lookup"><span data-stu-id="66adc-106">Format character</span></span> | <span data-ttu-id="66adc-107">Описание</span><span class="sxs-lookup"><span data-stu-id="66adc-107">Description</span></span>                                                           |
|------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="66adc-108">SM</span><span class="sxs-lookup"><span data-stu-id="66adc-108">SM</span></span>               | <span data-ttu-id="66adc-109">Общий размер типа может быть представлен в 16-разрядном целочисленном типе без знака.</span><span class="sxs-lookup"><span data-stu-id="66adc-109">The type's total size can be represented in a 16-bit unsigned int.</span></span>    |
| <span data-ttu-id="66adc-110">LG</span><span class="sxs-lookup"><span data-stu-id="66adc-110">LG</span></span>               | <span data-ttu-id="66adc-111">Общий размер типа должен быть представлен в виде 32-разрядного длинного числа без знака.</span><span class="sxs-lookup"><span data-stu-id="66adc-111">The type's total size needs a 32-bit unsigned long to be represented.</span></span> |



 

<span data-ttu-id="66adc-112">Поля, общие для массивов:</span><span class="sxs-lookup"><span data-stu-id="66adc-112">Fields common to arrays:</span></span>

-   <span data-ttu-id="66adc-113">Общий \_ Размер</span><span class="sxs-lookup"><span data-stu-id="66adc-113">total\_size</span></span>

    <span data-ttu-id="66adc-114">Общий размер массива в памяти, в байтах.</span><span class="sxs-lookup"><span data-stu-id="66adc-114">Total size of the array in memory, in bytes.</span></span> <span data-ttu-id="66adc-115">Это то же самое, что и размер линии после выравнивания.</span><span class="sxs-lookup"><span data-stu-id="66adc-115">This is the same as wire size after alignment.</span></span> <span data-ttu-id="66adc-116">Общий размер вычисляется для категорий, для которых не существует проблемы заполнения, а размер — фактический размер массива.</span><span class="sxs-lookup"><span data-stu-id="66adc-116">The total size is calculated for categories for which the padding issue does not exist and the size is actual array size.</span></span>

-   <span data-ttu-id="66adc-117">\_размер элемента</span><span class="sxs-lookup"><span data-stu-id="66adc-117">element\_size</span></span>

    <span data-ttu-id="66adc-118">Общий размер в памяти одного элемента массива, включая заполнение (это может произойти только для сложных массивов).</span><span class="sxs-lookup"><span data-stu-id="66adc-118">Total size in memory of a single element of the array, including padding (this may happen for complex arrays only).</span></span>

-   <span data-ttu-id="66adc-119">\_Описание элемента</span><span class="sxs-lookup"><span data-stu-id="66adc-119">element\_description</span></span>

    <span data-ttu-id="66adc-120">Описание типа элемента массива.</span><span class="sxs-lookup"><span data-stu-id="66adc-120">Description of the array element type.</span></span>

-   <span data-ttu-id="66adc-121">\_Макет указателя</span><span class="sxs-lookup"><span data-stu-id="66adc-121">pointer\_layout</span></span>

    <span data-ttu-id="66adc-122">Дополнительные сведения см. в разделе о [макете указателя](pointer-layout-tfs.md) .</span><span class="sxs-lookup"><span data-stu-id="66adc-122">See the [Pointer Layout](pointer-layout-tfs.md) topic for more information.</span></span>

## <a name="fixed-sized-arrays"></a><span data-ttu-id="66adc-123">Массивы фиксированного размера</span><span class="sxs-lookup"><span data-stu-id="66adc-123">Fixed-sized Arrays</span></span>

<span data-ttu-id="66adc-124">Строка формата массива фиксированного размера создается для массивов, имеющих известный размер, и поэтому может быть заблокирована в буфере упаковки.</span><span class="sxs-lookup"><span data-stu-id="66adc-124">A fixed-sized array format string is generated for arrays that have a known size, and therefore may be block-copied to the marshaling buffer.</span></span> <span data-ttu-id="66adc-125">Ниже приведены два формата дескрипторов фиксированных массивов.</span><span class="sxs-lookup"><span data-stu-id="66adc-125">The two fixed array descriptor formats are as follows.</span></span>

``` syntax
FC_SMFARRAY alignment<1> 
total_size<2> 
[pointer_layout<>]  
element_description<> 
FC_END
```

<span data-ttu-id="66adc-126">и</span><span class="sxs-lookup"><span data-stu-id="66adc-126">and</span></span>

``` syntax
FC_LGFARRAY alignment<1> 
total_size<4> 
[pointer_layout<>] 
element_description<> 
FC_END
```

## <a name="conformant-array"></a><span data-ttu-id="66adc-127">Согласованный массив</span><span class="sxs-lookup"><span data-stu-id="66adc-127">Conformant Array</span></span>

<span data-ttu-id="66adc-128">Согласованный массив может быть заблокирован, если размер массива известен.</span><span class="sxs-lookup"><span data-stu-id="66adc-128">A conformant array can be block-copied once the size of the array is known.</span></span>

``` syntax
FC_CARRAY alignment<1>
element_size<2> 
conformance_description<> 
[pointer_layout<>] 
element_description<> 
FC_END
```

<span data-ttu-id="66adc-129">\_Описание соответствия<> является дескриптором корреляции и имеет 4 или 6 байт в зависимости от того, используется ли [**/robust**](/windows/desktop/Midl/-robust) .</span><span class="sxs-lookup"><span data-stu-id="66adc-129">The conformance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

## <a name="conformant-varying-array"></a><span data-ttu-id="66adc-130">Согласованный переменный массив</span><span class="sxs-lookup"><span data-stu-id="66adc-130">Conformant Varying Array</span></span>

<span data-ttu-id="66adc-131">Согласованный переменный массив также может быть скопирован в блок.</span><span class="sxs-lookup"><span data-stu-id="66adc-131">A conformant varying array can also be block-copied.</span></span>

``` syntax
FC_CVARRAY alignment<1> 
element_size<2> 
conformance_description<> 
variance_description<>  
[pointer_layout<>] 
element_description<> 
FC_END
```

<span data-ttu-id="66adc-132">\_Описание соответствия<> и описание дисперсии \_<> является дескриптором корреляции и имеет 4 или 6 байт в зависимости от того, используется ли [**/robust**](/windows/desktop/Midl/-robust) .</span><span class="sxs-lookup"><span data-stu-id="66adc-132">The conformance\_description<> and variance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

## <a name="varying-array"></a><span data-ttu-id="66adc-133">Различные массивы</span><span class="sxs-lookup"><span data-stu-id="66adc-133">Varying Array</span></span>

<span data-ttu-id="66adc-134">Различные массивы имеют две возможности в зависимости от размера массива.</span><span class="sxs-lookup"><span data-stu-id="66adc-134">The varying arrays have two possibilities depending on the size of the array.</span></span>

``` syntax
FC_SMVARRAY alignment<1>
total_size<2>  
number_elements<2> 
element_size<2> 
variance_description<> 
[pointer_layout<>] 
element_description<> 
FC_END

FC_LGVARRAY alignment<1>
total_size<4>  
number_elements<4> 
element_size<2> 
variance_description<4>
[pointer_layout<>] 
element_description<> 
FC_END
```

<span data-ttu-id="66adc-135">Описание дисперсии \_<> является дескриптором корреляции и содержит 4 или 6 байт в зависимости от используемого [**/robust**](/windows/desktop/Midl/-robust) .</span><span class="sxs-lookup"><span data-stu-id="66adc-135">The variance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on the [**/robust**](/windows/desktop/Midl/-robust) being used.</span></span>

<span data-ttu-id="66adc-136">Для различных массивов, внедренных в структуру, смещение<2> описания дисперсии \_<> является относительным смещением от положения разного массива в структуре до поля, описывающего дисперсию.</span><span class="sxs-lookup"><span data-stu-id="66adc-136">For varying arrays embedded inside of a structure, the offset<2> field of the variance\_description<> is a relative offset from the varying array's position in the structure to the variance describing field.</span></span> <span data-ttu-id="66adc-137">Смещение обычно относительно начала структуры.</span><span class="sxs-lookup"><span data-stu-id="66adc-137">The offset is typically relative to the beginning of the structure.</span></span>

## <a name="complex-arrays"></a><span data-ttu-id="66adc-138">Сложные массивы</span><span class="sxs-lookup"><span data-stu-id="66adc-138">Complex Arrays</span></span>

<span data-ttu-id="66adc-139">Сложный массив — это любой массив с элементом, который предотвращает копирование блока, и, таким образом, необходимо выполнить дополнительное действие.</span><span class="sxs-lookup"><span data-stu-id="66adc-139">A complex array is any array with an element that prevents it from being block-copied, and as such, additional action needs to be taken.</span></span> <span data-ttu-id="66adc-140">Эти элементы делают массив сложным:</span><span class="sxs-lookup"><span data-stu-id="66adc-140">These elements make an array complex:</span></span>

-   <span data-ttu-id="66adc-141">простые типы: ENUM16, \_ \_ INT3264 (только на 64-разрядных платформах), интеграл с \[ [ **диапазоном**](/windows/desktop/Midl/range)\]</span><span class="sxs-lookup"><span data-stu-id="66adc-141">simple types: ENUM16, \_\_INT3264 (on 64-bit platforms only), an integral with \[[**range**](/windows/desktop/Midl/range)\]</span></span>
-   <span data-ttu-id="66adc-142">ссылки и указатели интерфейса (все указатели на 64-разрядных платформах)</span><span class="sxs-lookup"><span data-stu-id="66adc-142">reference and interface pointers (all pointers on 64-bit platforms)</span></span>
-   <span data-ttu-id="66adc-143">объединения</span><span class="sxs-lookup"><span data-stu-id="66adc-143">unions</span></span>
-   <span data-ttu-id="66adc-144">сложные структуры (см. раздел описание сложной структуры для получения полного списка причин сложной структуры).</span><span class="sxs-lookup"><span data-stu-id="66adc-144">complex structures (see the Complex Structure Description topic for a full list of reasons for a structure to be complex)</span></span>
-   <span data-ttu-id="66adc-145">элементы, определенные с помощью \[ [**передачи \_ в виде**](/windows/desktop/Midl/transmit-as) \] , \[ [**пользовательского \_ маршалирования**](/windows/desktop/Midl/user-marshal)\]</span><span class="sxs-lookup"><span data-stu-id="66adc-145">elements defined with \[[**transmit\_as**](/windows/desktop/Midl/transmit-as)\], \[[**user\_marshal**](/windows/desktop/Midl/user-marshal)\]</span></span>
-   <span data-ttu-id="66adc-146">Все многомерные массивы, имеющие по крайней мере одно согласованное и (или) изменяющееся измерение, являются сложными независимо от типа базового элемента.</span><span class="sxs-lookup"><span data-stu-id="66adc-146">All multidimensional arrays with at least one conformant and/or varying dimension are complex regardless of the underlying element type.</span></span>

<span data-ttu-id="66adc-147">Описание сложного массива выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="66adc-147">The complex array description is as follows:</span></span>

``` syntax
FC_BOGUS_ARRAY alignment<1> 
number_of_elements<2> 
conformance_description<> 
variance_description<> 
element_description<> 
FC_END
```

<span data-ttu-id="66adc-148">Число \_ элементов, \_<2> поле, равно нулю, если массив является согласованным.</span><span class="sxs-lookup"><span data-stu-id="66adc-148">The number\_of\_elements<2> field is zero if the array is conformant.</span></span>

<span data-ttu-id="66adc-149">\_Описание соответствия<> и описание дисперсии \_<> является дескриптором корреляции и имеет 4 или 6 байт в зависимости от того, используется ли [**/robust**](/windows/desktop/Midl/-robust) .</span><span class="sxs-lookup"><span data-stu-id="66adc-149">The conformance\_description<> and variance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span> <span data-ttu-id="66adc-150">Если массив имеет соответствие и/или дисперсия, \_ Описание соответствия<> и/или описания дисперсии \_<> поля имеют допустимые описания, в противном случае первые 4 байта дескриптора корреляции имеют значение 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="66adc-150">If the array has conformance and/or variance then the conformance\_description<> and/or variance\_description<> field(s) have valid descriptions, otherwise the first 4 bytes of the correlation descriptor are set to 0xFFFFFFFF.</span></span> <span data-ttu-id="66adc-151">Флаги, при их наличии, устанавливаются в ноль.</span><span class="sxs-lookup"><span data-stu-id="66adc-151">The flags, when present, are set to zero.</span></span>

 

 
