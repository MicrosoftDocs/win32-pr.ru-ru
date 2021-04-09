---
title: Макет указателя
description: Макет указателя описывает указатели структуры или массива.
ms.assetid: 1a4984c1-97b9-4e95-a17e-851b67fa94a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f26a6639b0c4b56c911be1e688995aaf3fb9d2d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888875"
---
# <a name="pointer-layout"></a><span data-ttu-id="5e53c-103">Макет указателя</span><span class="sxs-lookup"><span data-stu-id="5e53c-103">Pointer Layout</span></span>

<span data-ttu-id="5e53c-104">Макет указателя описывает указатели структуры или массива.</span><span class="sxs-lookup"><span data-stu-id="5e53c-104">Pointer layout describes pointers of a structure or an array.</span></span>

## <a name="pointer_layout"></a><span data-ttu-id="5e53c-105">\_<> макета указателя</span><span class="sxs-lookup"><span data-stu-id="5e53c-105">pointer\_layout<></span></span>

<span data-ttu-id="5e53c-106">Макет указателя \_<> поле состоит из символов формата \_ : FC PP FC, \_ за которыми следуют одно или несколько описаний указателей, как описано ниже, и завершением с помощью \_ символа конца формата FC:</span><span class="sxs-lookup"><span data-stu-id="5e53c-106">A pointer\_layout<> field consists of the format characters FC\_PP FC\_PAD followed by one or more pointer descriptions, as described later, and terminating with an FC\_END format character:</span></span>

``` syntax
FC_PP
FC_PAD
{ pointer_instance_layout<> }*
FC_END
```

<span data-ttu-id="5e53c-107">\_Макет экземпляра указателя \_<> поле — это строка формата, описывающая один или несколько экземпляров указателей.</span><span class="sxs-lookup"><span data-stu-id="5e53c-107">A pointer\_instance\_layout<> field is a format string describing single or multiple instances of pointers.</span></span> <span data-ttu-id="5e53c-108">В этих дескрипторах используются следующие поля:</span><span class="sxs-lookup"><span data-stu-id="5e53c-108">The following fields are used in these descriptors:</span></span>

-   <span data-ttu-id="5e53c-109">смещение \_ в \_ памяти</span><span class="sxs-lookup"><span data-stu-id="5e53c-109">offset\_in\_memory</span></span>

    <span data-ttu-id="5e53c-110">Смещение со знаком в расположении указателя в памяти.</span><span class="sxs-lookup"><span data-stu-id="5e53c-110">The signed offset to the pointer's location in memory.</span></span> <span data-ttu-id="5e53c-111">Для указателя, находящегося в структуре, это смещение является отрицательным смещением от конца структуры (конца неподчиненной части согласованных структур); для массивов смещение начинается с начала массива.</span><span class="sxs-lookup"><span data-stu-id="5e53c-111">For a pointer residing in a structure, this offset is a negative offset from the end of the structure (the end of the nonconformant portion of conformant structures); for arrays, the offset is from the beginning of the array.</span></span>

-   <span data-ttu-id="5e53c-112">смещение \_ в \_ буфере</span><span class="sxs-lookup"><span data-stu-id="5e53c-112">offset\_in\_buffer</span></span>

    <span data-ttu-id="5e53c-113">Смещение со знаком в позиции указателя в буфере.</span><span class="sxs-lookup"><span data-stu-id="5e53c-113">The signed offset to the pointer's location in the buffer.</span></span> <span data-ttu-id="5e53c-114">Для указателя, находящегося в структуре, это смещение является отрицательным смещением от конца структуры (конца неподчиненной части согласованных структур): для массивов смещение начинается с начала массива.</span><span class="sxs-lookup"><span data-stu-id="5e53c-114">For a pointer residing in a structure, this offset is a negative offset from the end of the structure (the end of the nonconformant portion of conformant structures): for arrays, the offset is from the beginning of the array.</span></span>

-   <span data-ttu-id="5e53c-115">смещение \_ к \_ массиву</span><span class="sxs-lookup"><span data-stu-id="5e53c-115">offset\_to\_array</span></span>

    <span data-ttu-id="5e53c-116">Смещение от окружающей структуры к внедренному массиву, указатели которого обрабатываются.</span><span class="sxs-lookup"><span data-stu-id="5e53c-116">Offset from an enclosing structure to the embedded array whose pointers are being handled.</span></span> <span data-ttu-id="5e53c-117">Для массивов верхнего уровня это поле всегда будет равно нулю.</span><span class="sxs-lookup"><span data-stu-id="5e53c-117">For top-level arrays, this field will always be zero.</span></span>

-   <span data-ttu-id="5e53c-118">итерации</span><span class="sxs-lookup"><span data-stu-id="5e53c-118">iterations</span></span>

    <span data-ttu-id="5e53c-119">Общее число указателей, для которых<> описан один и тот же макет.</span><span class="sxs-lookup"><span data-stu-id="5e53c-119">Total number of pointers that have the same layout<> described.</span></span>

-   <span data-ttu-id="5e53c-120">increment</span><span class="sxs-lookup"><span data-stu-id="5e53c-120">increment</span></span>

    <span data-ttu-id="5e53c-121">Увеличение между последовательными указателями во время ПОВТОРа.</span><span class="sxs-lookup"><span data-stu-id="5e53c-121">Increment between successive pointers during a REPEAT.</span></span>

-   <span data-ttu-id="5e53c-122">число \_ \_ указателей</span><span class="sxs-lookup"><span data-stu-id="5e53c-122">number\_of\_pointers</span></span>

    <span data-ttu-id="5e53c-123">Количество различных указателей в экземпляре REPEAT.</span><span class="sxs-lookup"><span data-stu-id="5e53c-123">Number of different pointers in a repeat instance.</span></span>

-   <span data-ttu-id="5e53c-124">\_Описание указателя</span><span class="sxs-lookup"><span data-stu-id="5e53c-124">pointer\_description</span></span>

    <span data-ttu-id="5e53c-125">Описание указателя.</span><span class="sxs-lookup"><span data-stu-id="5e53c-125">Pointer description.</span></span>

<span data-ttu-id="5e53c-126">Все макеты экземпляров указателей используют следующий экземпляр одиночного указателя \_<8>:</span><span class="sxs-lookup"><span data-stu-id="5e53c-126">All pointer instance layouts use the following single pointer\_instance<8>:</span></span>

``` syntax
offset_to_pointer_in_memory<2> 
offset_to_pointer_in_buffer<2> 
pointer_description<4>
```

<span data-ttu-id="5e53c-127">Ниже приведены дескрипторы экземпляров.</span><span class="sxs-lookup"><span data-stu-id="5e53c-127">The following are instance descriptors:</span></span>

<span data-ttu-id="5e53c-128">**Одиночный экземпляр указателя на простой тип:**</span><span class="sxs-lookup"><span data-stu-id="5e53c-128">**Single instance of a pointer to a simple type:**</span></span>

``` syntax
FC_NO_REPEAT FC_PAD 
pointer_instance<8>
```

<span data-ttu-id="5e53c-129">**Фиксированный указатель Repeat:**</span><span class="sxs-lookup"><span data-stu-id="5e53c-129">**Fixed repeat pointer:**</span></span>

``` syntax
FC_FIXED_REPEAT FC_PAD 
iterations<2> 
increment<2> 
offset_to_array<2> 
number_of_pointers<2>
{ pointer_instance<8> }*
```

<span data-ttu-id="5e53c-130">**Указатель на переменную Repeat:**</span><span class="sxs-lookup"><span data-stu-id="5e53c-130">**Variable repeat pointer:**</span></span>

``` syntax
FC_VARIABLE_REPEAT (FC_FIXED_OFFSET | FC_VARIABLE_OFFSET) 
increment<2> 
offset_to_array<2> 
number_of_pointers<2> 
{ pointer_instance<8> }*
```

<span data-ttu-id="5e53c-131">Для экземпляров фиксированных повторных и переменных повторений указателей существует набор смещений и описаний указателей для каждого указателя в экземпляре REPEAT.</span><span class="sxs-lookup"><span data-stu-id="5e53c-131">For fixed repeat and variable repeat pointer instances there is a set of offset and pointer descriptions for each pointer in the repeat instance.</span></span>

## <a name="pointers-layout-design-issues"></a><span data-ttu-id="5e53c-132">Проблемы проектирования макетов указателей</span><span class="sxs-lookup"><span data-stu-id="5e53c-132">Pointers Layout Design Issues</span></span>

<span data-ttu-id="5e53c-133">В этом разделе рассматриваются проблемы, связанные с обработкой согласованных структур и внедренных указателей.</span><span class="sxs-lookup"><span data-stu-id="5e53c-133">This section addresses issues related to processing conformant structures and embedded pointers.</span></span> <span data-ttu-id="5e53c-134">Эта ошибка заключается в том, что компилятор создает макеты указателей для структур и массивов с некоторой избыточностью.</span><span class="sxs-lookup"><span data-stu-id="5e53c-134">The issue is that the compiler generates pointer layouts for structures and arrays with some redundancy.</span></span> <span data-ttu-id="5e53c-135">Это полезно, так как эта информация полезна, поэтому, например, согласованная структура может пройти по одному макету указателя, чтобы обслуживать все указатели из структуры и из согласованного массива, который является частью согласованной структуры.</span><span class="sxs-lookup"><span data-stu-id="5e53c-135">This is beneficial, because the information is useful and as such, for example, a conformant structure can walk one pointer layout to service all the pointers from the structure and from the conformant array being part of the conformant structure.</span></span> <span data-ttu-id="5e53c-136">Однако существуют некоторые внедренные ситуации, требующие, чтобы модуль NDR выполнил дополнительную работу по обработке всех макетов указателей в соответствующей последовательности, обрабатывая каждый указатель ровно один раз.</span><span class="sxs-lookup"><span data-stu-id="5e53c-136">However, some embedded situations exist that require the NDR engine to perform additional work to process all the pointer layouts in the proper sequence, processing each pointer exactly once.</span></span>

## <a name="what-the-compiler-generates"></a><span data-ttu-id="5e53c-137">Что создает компилятор</span><span class="sxs-lookup"><span data-stu-id="5e53c-137">What the Compiler Generates</span></span>

<span data-ttu-id="5e53c-138">Каждый объект, обсуждаемый в этом разделе, имеет указатели, поэтому, например, согласованная структура имеет указатели в части структуры, а также в элементах массива.</span><span class="sxs-lookup"><span data-stu-id="5e53c-138">Every object discussed in this section has pointers, so for example, a conformant structure has pointers in the structure part as well as in the array elements.</span></span> <span data-ttu-id="5e53c-139">Элемент является простой структурой с указателем.</span><span class="sxs-lookup"><span data-stu-id="5e53c-139">The element is a simple structure with a pointer.</span></span>

1.  <span data-ttu-id="5e53c-140">Согласованная структура, один уровень</span><span class="sxs-lookup"><span data-stu-id="5e53c-140">Conformant structure, single level</span></span>

    <span data-ttu-id="5e53c-141">Согласованный дескриптор имеет часть PP, в которой все указатели описаны как из структуры, так и из массива.</span><span class="sxs-lookup"><span data-stu-id="5e53c-141">The conformant descriptor has a PP part where all the pointers are described, both from the structure and from the array.</span></span> <span data-ttu-id="5e53c-142">Список членов имеет длину FC \_ -файла, а не указатель.</span><span class="sxs-lookup"><span data-stu-id="5e53c-142">The member list has FC\_LONG in lieu of a pointer.</span></span> <span data-ttu-id="5e53c-143">Дескриптор массива CARRAY содержит элементы с помощью встроенных \_ сложных дескрипторов без указателей.</span><span class="sxs-lookup"><span data-stu-id="5e53c-143">The CARRAY array descriptor has elements through the use of an embedded\_complex and no pointer descriptors at all.</span></span> <span data-ttu-id="5e53c-144">Элемент по-прежнему имеет единственный дескриптор указателя.</span><span class="sxs-lookup"><span data-stu-id="5e53c-144">The element still has its single pointer descriptor.</span></span> <span data-ttu-id="5e53c-145">Макет указателя предшествует макету элемента в согласованной структуре и простых дескрипторах структуры.</span><span class="sxs-lookup"><span data-stu-id="5e53c-145">Pointer layout precedes the member layout in a conformant structure and simple structure descriptors.</span></span>

2.  <span data-ttu-id="5e53c-146">Согласованная структура, два или более уровней</span><span class="sxs-lookup"><span data-stu-id="5e53c-146">Conformant structure, two or more levels</span></span>

    <span data-ttu-id="5e53c-147">Описание PP содержит указатели со всех уровней.</span><span class="sxs-lookup"><span data-stu-id="5e53c-147">The PP description has pointers from all levels.</span></span> <span data-ttu-id="5e53c-148">Он использует то же описание массива, что и внутренняя согласованная структура.</span><span class="sxs-lookup"><span data-stu-id="5e53c-148">It reuses the same array description as the internal conformant structure.</span></span> <span data-ttu-id="5e53c-149">Список членов имеет длину FC \_ -файла, а не указатель.</span><span class="sxs-lookup"><span data-stu-id="5e53c-149">The member list has FC\_LONG in lieu of a pointer.</span></span> <span data-ttu-id="5e53c-150">Внедренная структура реализуется с помощью внедренной сложной структуры.</span><span class="sxs-lookup"><span data-stu-id="5e53c-150">An embedded structure comes through the use of an embedded complex.</span></span> <span data-ttu-id="5e53c-151">Согласованный дескриптор структуры используется повторно как есть.</span><span class="sxs-lookup"><span data-stu-id="5e53c-151">The conformant structure descriptor is reused as-is.</span></span> <span data-ttu-id="5e53c-152">Размер плоской части структуры также выходит за рамки, что означает, что размер структуры верхнего уровня будет включать неструктурированный размер внедренной структуры.</span><span class="sxs-lookup"><span data-stu-id="5e53c-152">The size of the flat portion of the structure comes out complete as well, meaning that the top-level structure size would include embedded structure's flat size.</span></span>

3.  <span data-ttu-id="5e53c-153">Сложная структура, один уровень</span><span class="sxs-lookup"><span data-stu-id="5e53c-153">Complex structure, single level</span></span>

    <span data-ttu-id="5e53c-154">Элементы указателя помечаются \_ указателем FC.</span><span class="sxs-lookup"><span data-stu-id="5e53c-154">Pointer members are marked by FC\_POINTER.</span></span> <span data-ttu-id="5e53c-155">Макет указателя упрощен таким, что для каждой записи указателя FC в списке имеется дескриптор указателя (4 байта) \_ .</span><span class="sxs-lookup"><span data-stu-id="5e53c-155">Pointer layout is simplified such that there is a pointer descriptor (4 bytes) for each FC\_POINTER entry on the list.</span></span> <span data-ttu-id="5e53c-156">Макет указателя просматривается параллельно с помощью прохода по элементу, то есть \_ указатель FC вызывает обработку следующего описания указателя.</span><span class="sxs-lookup"><span data-stu-id="5e53c-156">Pointer layout is walked in parallel with a member walk, that is, an FC\_POINTER causes the next pointer description to be processed.</span></span> <span data-ttu-id="5e53c-157">Массив CARRAY имеет макет указателя со всеми дескрипторами массива, а затем элемент, используя внедренный сложный объект.</span><span class="sxs-lookup"><span data-stu-id="5e53c-157">The CARRAY array has pointer layout with all the descriptors of the array, and then element, through the use of an embedded complex.</span></span> <span data-ttu-id="5e53c-158">Дескриптор элемента используется повторно.</span><span class="sxs-lookup"><span data-stu-id="5e53c-158">The element descriptor is reused.</span></span> <span data-ttu-id="5e53c-159">Размер плоской части структуры завершается. Иными словами, плоский размер структуры верхнего уровня включает неструктурированный размер внедренной структуры.</span><span class="sxs-lookup"><span data-stu-id="5e53c-159">The size of the flat portion of the structure comes out complete; in other words, the top-level structure's flat size includes the embedded structure's flat size.</span></span> <span data-ttu-id="5e53c-160">Макет элемента предшествует макету указателя для сложных структур.</span><span class="sxs-lookup"><span data-stu-id="5e53c-160">The member layout precedes the pointer layout for complex structures.</span></span>

    <span data-ttu-id="5e53c-161">Таким образом, создаваемое описание соответствия массивов зависит от того, является ли он массивом в согласованной структуре или в сложной структуре.</span><span class="sxs-lookup"><span data-stu-id="5e53c-161">Hence, the conformant array description generation is different depending on whether it is an array inside of a conformant structure or inside a complex structure.</span></span>

4.  <span data-ttu-id="5e53c-162">Сложная структура, 2 или более уровней, сложная комплексная</span><span class="sxs-lookup"><span data-stu-id="5e53c-162">Complex structure, 2 or more levels, complex in complex</span></span>

    <span data-ttu-id="5e53c-163">В сложной структуре верхнего уровня есть указатели на члены, а внедренная сложная структура имеет свои указатели на члены.</span><span class="sxs-lookup"><span data-stu-id="5e53c-163">Top-level complex structure has its member pointers, embedded complex structure has its member pointers.</span></span> <span data-ttu-id="5e53c-164">Дескриптор согласованной структуры используется повторно.</span><span class="sxs-lookup"><span data-stu-id="5e53c-164">The conformant structure descriptor is reused.</span></span> <span data-ttu-id="5e53c-165">Дескриптор массива из верхнего уровня представляет собой повторно используемый массив из внедренной структуры.</span><span class="sxs-lookup"><span data-stu-id="5e53c-165">The array descriptor from the top is the reused array from the embedded structure.</span></span>

5.  <span data-ttu-id="5e53c-166">Сложная структура с внедренной согласованной структурой</span><span class="sxs-lookup"><span data-stu-id="5e53c-166">Complex structure with an embedded conformant structure</span></span>

    <span data-ttu-id="5e53c-167">"Top =". Согласованная структура имеет свои указатели на члены.</span><span class="sxs-lookup"><span data-stu-id="5e53c-167">Top=level conformant structure has its member pointers.</span></span> <span data-ttu-id="5e53c-168">Согласованный дескриптор структуры используется повторно как есть.</span><span class="sxs-lookup"><span data-stu-id="5e53c-168">The conformant structure descriptor is reused as-is.</span></span> <span data-ttu-id="5e53c-169">Дескриптор массива повторно используется из внедренной согласованной структуры; Иными словами, у него нет указателей в дескрипторе массива.</span><span class="sxs-lookup"><span data-stu-id="5e53c-169">The array descriptor is reused from the embedded conformant structure; in other words, it does not have any pointers at the array descriptor.</span></span> <span data-ttu-id="5e53c-170">У элемента есть дескриптор указателя.</span><span class="sxs-lookup"><span data-stu-id="5e53c-170">The element has its pointer descriptor.</span></span>

6.  <span data-ttu-id="5e53c-171">Массивы структур с указателями</span><span class="sxs-lookup"><span data-stu-id="5e53c-171">Arrays of structures with pointers</span></span>

    <span data-ttu-id="5e53c-172">Массив простых структур с указателями создается как СМФАРРАЙ или CARRAY, в зависимости от того, имеет ли размер массив, но в обоих случаях он имеет макет указателя, который является завершенным (ФИКСИРОВАНное \_ повторение или переменная \_ repeat).</span><span class="sxs-lookup"><span data-stu-id="5e53c-172">An array of simple structures with pointers is generated as an SMFARRAY or CARRAY depending whether the array is sized, but in both cases it has a pointer layout that is complete (FIXED\_REPEAT or VARIABLE\_REPEAT).</span></span> <span data-ttu-id="5e53c-173">Макет указателя располагается перед макетом элемента.</span><span class="sxs-lookup"><span data-stu-id="5e53c-173">The pointer layout comes before the member layout.</span></span>

    <span data-ttu-id="5e53c-174">Массив сложных структур с указателями создается как ФИКТИВный \_ массив независимо от того, является ли он фиксированным или размером, а в обоих случаях не имеет макета указателя.</span><span class="sxs-lookup"><span data-stu-id="5e53c-174">An array of complex structures with pointers is generated as BOGUS\_ARRAY regardless whether it is fixed or sized, and in both cases, does not have any pointer layout.</span></span>

## <a name="what-the-ndr-engine-does"></a><span data-ttu-id="5e53c-175">Что делает модуль NDR</span><span class="sxs-lookup"><span data-stu-id="5e53c-175">What the NDR Engine Does</span></span>

<span data-ttu-id="5e53c-176">В этом разделе описывается поведение механизма NDR.</span><span class="sxs-lookup"><span data-stu-id="5e53c-176">This section describes the NDR engine behavior.</span></span>

<span data-ttu-id="5e53c-177">**Проход упаковки**</span><span class="sxs-lookup"><span data-stu-id="5e53c-177">**The marshaling pass**</span></span>

1.  <span data-ttu-id="5e53c-178">Согласованные структуры и внедренная согласованная структура.</span><span class="sxs-lookup"><span data-stu-id="5e53c-178">Conformant structures and embedded conformant structure.</span></span>

    <span data-ttu-id="5e53c-179">Структура верхнего уровня ведет себя как структура с одним уровнем.</span><span class="sxs-lookup"><span data-stu-id="5e53c-179">The top-level structure behaves like a single-level structure.</span></span>

2.  <span data-ttu-id="5e53c-180">Внедренная комплексная структура с согласованным массивом</span><span class="sxs-lookup"><span data-stu-id="5e53c-180">Embedded complex structure with conformant array</span></span>

    <span data-ttu-id="5e53c-181">Любая сложная структура заставляет внешнюю структуру быть сложной.</span><span class="sxs-lookup"><span data-stu-id="5e53c-181">Any complex structure forces the outer structure to be a complex structure.</span></span> <span data-ttu-id="5e53c-182">Внедренная структура никогда не маршалирует свой массив.</span><span class="sxs-lookup"><span data-stu-id="5e53c-182">Embedded structure never marshals its array.</span></span> <span data-ttu-id="5e53c-183">Каждая структура всегда проходит через внедренные указатели, просто упаковывая элементы и элемент, происходящий в качестве \_ указателя FC.</span><span class="sxs-lookup"><span data-stu-id="5e53c-183">Every structure always goes through embedded pointers by simply marshaling members and a member happening to be an FC\_POINTER.</span></span>

3.  <span data-ttu-id="5e53c-184">Сложная структура с согласованной структурой</span><span class="sxs-lookup"><span data-stu-id="5e53c-184">Complex structure with conformant structure</span></span>

    <span data-ttu-id="5e53c-185">Самая верхняя встроенная согласованная структура выполняет упаковку согласованного массива и всех поинтис.</span><span class="sxs-lookup"><span data-stu-id="5e53c-185">The top-most embedded conformant structure marshals the conformant array and all the pointees.</span></span> <span data-ttu-id="5e53c-186">Модуль NDR никогда не имеет более глубокой вложенной согласованной структуры, если таковые имеются. Это упрощает решение, так как согласованная структура является конечным объектом до того момента, когда происходит маршалирование внедренных объектов.</span><span class="sxs-lookup"><span data-stu-id="5e53c-186">The NDR engine never descends to deeper nested conformant structures if there are any; this simplifies the solution, as a conformant structure is a leaf object as far as the marshaling of embedded objects is concerned.</span></span> <span data-ttu-id="5e53c-187">Сложная структура верхнего уровня пропускает упаковку массива.</span><span class="sxs-lookup"><span data-stu-id="5e53c-187">The top-level complex structure skips the array marshaling.</span></span>

<span data-ttu-id="5e53c-188">**Распаковка, буфсизинг и освобождение проходов**</span><span class="sxs-lookup"><span data-stu-id="5e53c-188">**Unmarshaling, bufsizing and freeing passes**</span></span>

<span data-ttu-id="5e53c-189">Демаршалирование является симметричным для маршалирования; Первая операция, выполняемая для сложных структур, заключается в том, чтобы определить расположение поинтис в буфере с помощью вызова функции **ндркомплексструктбуфферсизе** .</span><span class="sxs-lookup"><span data-stu-id="5e53c-189">Unmarshaling is symmetrical to marshaling; the first operation it performs for complex structures is to find out the pointees' location in the buffer by means of calling the **NdrComplexStructBufferSize** function.</span></span> <span data-ttu-id="5e53c-190">Затем он демаршалирует поинтис в параллельном режиме, что позволяет использовать ту же схему для правильного распаковки поинтис.</span><span class="sxs-lookup"><span data-stu-id="5e53c-190">It then unmarshals pointees in parallel, enabling the same scheme for unmarshaling the pointees correctly to be used.</span></span> <span data-ttu-id="5e53c-191">Не должно быть путаницы по размеру объектов и объединений. образ памяти не должен использоваться для размеров объектов и объединений только для содержимого буфера.</span><span class="sxs-lookup"><span data-stu-id="5e53c-191">There should be no confusion about sized objects and unions; the memory image should not be used for sized objects and unions, just for the buffer contents.</span></span>

<span data-ttu-id="5e53c-192">Флаги, используемые для правильного маршалирования и распаковки, используются аналогичным образом в буфсизинг и освобождаются, чтобы гарантировать, что поинтис проводятся ровно один раз.</span><span class="sxs-lookup"><span data-stu-id="5e53c-192">The flags used to perform marshaling and unmarshaling correctly are used in the same way in bufsizing and freeing to make sure that pointees are walked exactly once.</span></span>

<span data-ttu-id="5e53c-193">**Архитектуре Pass**</span><span class="sxs-lookup"><span data-stu-id="5e53c-193">**Endianess pass**</span></span>

<span data-ttu-id="5e53c-194">Сначала архитектуре-проход похож на упаковку и распаковку; для обработки сложных структур требуются два прохода.</span><span class="sxs-lookup"><span data-stu-id="5e53c-194">At first, the endianess pass is somewhat similar to marshaling/unmarshaling; two passes are required to process complex structures.</span></span> <span data-ttu-id="5e53c-195">Первый проход преобразует плоскую часть и находит в буфере расположение поинтис, аналогичное тому, как буфсизинг выполняет эту операцию для распаковки.</span><span class="sxs-lookup"><span data-stu-id="5e53c-195">First pass converts the flat part and finds the pointees' location in the buffer similar to how bufsizing performs this operation for unmarshaling.</span></span> <span data-ttu-id="5e53c-196">Затем второй проход преобразует поинтис.</span><span class="sxs-lookup"><span data-stu-id="5e53c-196">The second pass then converts the pointees.</span></span>

<span data-ttu-id="5e53c-197">Архитектуре передается следующим образом: Каждая структура и каждый элемент должны быть пошаговыми, пока конечный элемент или элемент не является простым типом.</span><span class="sxs-lookup"><span data-stu-id="5e53c-197">Endianess passes differ in the following manner: every structure and every member has to be stepped until the leaf member or element is a simple type.</span></span> <span data-ttu-id="5e53c-198">Это отличается от распаковки; Например, при распаковке не требуется обрабатывать согласованные структуры, встроенные в согласованные структуры, или любой член согласованной структуры.</span><span class="sxs-lookup"><span data-stu-id="5e53c-198">This is different from unmarshaling; in unmarshaling, for example, there is never a need to process conformant structures embedded in conformant structures, or any member of the conformant structure, for that matter.</span></span> <span data-ttu-id="5e53c-199">Еще одна причина заключается в том, что преобразование не является идемпотентными операцией, поэтому проход распаковки может повторить детрансляцию некоторых частей без ущерба, в то время как преобразование должно выполняться на основе строгого простого типа.</span><span class="sxs-lookup"><span data-stu-id="5e53c-199">Another issue is that the conversion is not an idempotent operation—hence the unmarshaling pass could redo unmarshaling of some pieces without harm, while conversion has to be performed on a strictly once-per-any-simple-type basis.</span></span>

<span data-ttu-id="5e53c-200">Следовательно, алгоритм архитектуре можно суммировать следующим образом.</span><span class="sxs-lookup"><span data-stu-id="5e53c-200">Hence, the endianess algorithm can be summarized as the following.</span></span> <span data-ttu-id="5e53c-201">NDR имеет концепцию согласованной структуры верхнего уровня и флаг, помечающий это соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="5e53c-201">NDR has a notion of the top-level conformant structure and a flag to mark that, as appropriate.</span></span> <span data-ttu-id="5e53c-202">Во время первого прохода, например для преобразования плоской части и получения расположения поинтис, это понятие использовать не будет.</span><span class="sxs-lookup"><span data-stu-id="5e53c-202">When walking the first time, such as to convert the flat portion and to obtain the location of the pointees, this notion would not be used.</span></span> <span data-ttu-id="5e53c-203">ОНД рассматривает плоские части всех уровней структур и никогда не подключается к обработке указателей.</span><span class="sxs-lookup"><span data-stu-id="5e53c-203">NDR would descend through the flat parts of all levels of structures and never venture into pointer processing.</span></span> <span data-ttu-id="5e53c-204">Наконец, ОНД будет плоско преобразовывать массив в верхний уровень.</span><span class="sxs-lookup"><span data-stu-id="5e53c-204">Finally, NDR would flat convert the array at the top-level.</span></span>

<span data-ttu-id="5e53c-205">Во второй раз флаг будет использоваться для обозначения прохода встроенного указателя, чтобы избежать появления более глубоких уровней согласованных структур, а затем самой лучшей согласованной структуры.</span><span class="sxs-lookup"><span data-stu-id="5e53c-205">When walking the second time, the flag would be used to mark the embedded pointer's pass to avoid entering deeper levels of the conformant structures, then the top-most conformant structure.</span></span> <span data-ttu-id="5e53c-206">Таким образом, флаг принудительно вызовет общее поведение маршалинга и демаршалинга, что позволяет избежать убывания на более глубоком уровне согласованных структур.</span><span class="sxs-lookup"><span data-stu-id="5e53c-206">In this way, the flag would force the common marshaling/unmarshaling behavior, which is to avoid descending into deeper levels of conformant structures.</span></span>

<span data-ttu-id="5e53c-207">Второй проход для сложных структур с совместимыми массивами работает следующим образом: сложные структуры работают по общему принципу. Это означает, что более глубокие уровни никогда не просматривает или не пропускают согласованный размер или их согласованные массивы, а просто проведут их члены, не затрагивая массив.</span><span class="sxs-lookup"><span data-stu-id="5e53c-207">The second pass for complex structures with conformant arrays works as follows: the complex structures work the common way; which means deeper levels would never look at or skip their conformant size or their conformant arrays, and would rather simply walk their members without touching the array.</span></span>

<span data-ttu-id="5e53c-208">Для сложных структур с согласованными структурами согласованная структура должна быть осведомлена о том, является ли она верхним уровнем и является ли она сложной структурой.</span><span class="sxs-lookup"><span data-stu-id="5e53c-208">For complex structures with conformant structures, the conformant structure must be aware whether it is top level, and whether it is in a complex structure.</span></span> <span data-ttu-id="5e53c-209">Плоская часть массива обрабатывается с помощью самой верхней согласованной структуры.</span><span class="sxs-lookup"><span data-stu-id="5e53c-209">The flat portion of the array is processed by the top-most conformant structure.</span></span> <span data-ttu-id="5e53c-210">На втором этапе самая лучшая согласованная структура пропускает плоскую часть и просматривает макет указателя и возвращает.</span><span class="sxs-lookup"><span data-stu-id="5e53c-210">On the second pass, the top-most conformant structure would skip the flat portion and go through the pointer layout and return.</span></span> <span data-ttu-id="5e53c-211">Самая сложная структура будет пропускать свою плоскую часть, а также пропускать макет указателя.</span><span class="sxs-lookup"><span data-stu-id="5e53c-211">The top-most complex structure would skip its flat portion, and would also skip the pointer layout.</span></span>

<span data-ttu-id="5e53c-212">**Надежный аспект архитектуреных обзоров**</span><span class="sxs-lookup"><span data-stu-id="5e53c-212">**The robust aspect of the endianess walks**</span></span>

<span data-ttu-id="5e53c-213">Архитектуре проходит проверку на наличие стандартных условий, готовых к заполнению буфера, и выполняет другие проверки некоррелированной природы.</span><span class="sxs-lookup"><span data-stu-id="5e53c-213">The endianess walk checks for the usual out-of-the-buffer conditions and performs other checks of an uncorrelated nature.</span></span> <span data-ttu-id="5e53c-214">С помощью этого шага невозможно выполнить проверки, нацеленные на коррелированные значения (например, аргумент размера и соответствующий размер); они выполняются позже, при распаковке.</span><span class="sxs-lookup"><span data-stu-id="5e53c-214">The checks aimed at correlated values (such as the sizing argument versus the conformant size) cannot be performed using this step; they are performed later, when unmarshaling.</span></span>

 

 




