---
title: Дескрипторы корреляции
description: Дескриптор корреляции — это строка формата, описывающая выражение, основанное на одном аргументе, связанном с другим аргументом.
ms.assetid: 9f5f5077-d6a9-4253-bddf-b8cd0c868973
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f13f0793b99b80b7abb0b493c249b30ad53d76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103891017"
---
# <a name="correlation-descriptors"></a><span data-ttu-id="0cd06-103">Дескрипторы корреляции</span><span class="sxs-lookup"><span data-stu-id="0cd06-103">Correlation Descriptors</span></span>

<span data-ttu-id="0cd06-104">Дескриптор корреляции — это строка формата, описывающая выражение, основанное на одном аргументе, связанном с другим аргументом.</span><span class="sxs-lookup"><span data-stu-id="0cd06-104">A correlation descriptor is a format string that describes an expression based on one argument related to another argument.</span></span> <span data-ttu-id="0cd06-105">Дескриптор корреляции необходим для обработки семантики, связанной с такими атрибутами, как \[ **size \_ — ()** \] , \[ **length \_ — ()** \] , \[ **Switch \_ имеет значение ()** , \] а \[ **IID \_ — ()** \] .</span><span class="sxs-lookup"><span data-stu-id="0cd06-105">A correlation descriptor is needed for handling semantics related to attributes like \[**size\_is()**\], \[**length\_is()**\], \[**switch\_is()**\] and \[**iid\_is()**\].</span></span> <span data-ttu-id="0cd06-106">Дескрипторы корреляции используются с массивами, указателями на размеры, объединениями и указателями на интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="0cd06-106">Correlation descriptors are used with arrays, sized pointers, unions, and interface pointers.</span></span> <span data-ttu-id="0cd06-107">Конечным значением выражения может быть размер, длина, discriminant объединения или указатель на IID соответственно.</span><span class="sxs-lookup"><span data-stu-id="0cd06-107">The eventual expression value can be a size, a length, a union discriminant, or a pointer to an IID, respectively.</span></span> <span data-ttu-id="0cd06-108">В терминах строк формата дескрипторы корреляции используются с массивами, объединениями и указателями интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="0cd06-108">In terms of format strings, correlation descriptors are used with arrays, unions, and interface pointers.</span></span> <span data-ttu-id="0cd06-109">Указатель размера описывается в разделе строки формата как указатель на массив.</span><span class="sxs-lookup"><span data-stu-id="0cd06-109">A sized pointer is described in format strings as a pointer to an array.</span></span>

<span data-ttu-id="0cd06-110">Существует две подпрограммы, выполняющие базовые вычисления выражений: Ндрпкомпутеконформанце используется для размеров, переключателей и IID, \* когда ндрпкомпутеварианце используется для длины.</span><span class="sxs-lookup"><span data-stu-id="0cd06-110">There are two routines performing basic expression calculations: NdrpComputeConformance is used for sizes, switches and IID\* while NdrpComputeVariance is used for lengths.</span></span> <span data-ttu-id="0cd06-111">Существует также одна подпрограммы для проверки значения корреляции для функции отказа от атак.</span><span class="sxs-lookup"><span data-stu-id="0cd06-111">There is also a single routine to perform a correlation value validation for denial-of-attack functionality.</span></span>

<span data-ttu-id="0cd06-112">Дескрипторы корреляции предназначены для поддержки только очень ограниченных выражений.</span><span class="sxs-lookup"><span data-stu-id="0cd06-112">Correlation descriptors have been designed to support only very limited expressions.</span></span> <span data-ttu-id="0cd06-113">В сложных ситуациях компилятор создает подпрограмму вычисления выражения, вызываемую ядром при необходимости.</span><span class="sxs-lookup"><span data-stu-id="0cd06-113">For complicated situations, the compiler generates an expression evaluation routine to be called by the engine when needed.</span></span>

<span data-ttu-id="0cd06-114">Дескриптор корреляции имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="0cd06-114">A correlation descriptor has the following format:</span></span>

``` syntax
correlation_type<1>
correlation_operator<1>
offset<2>
[robust_flags<2>]
```

<span data-ttu-id="0cd06-115">Тип корреляции дескриптора корреляции \_<1> состоит из двух частей: 4 верхних бита описывают, где можно найти выражение, а младшие 4 бита описывают тип значения выражения.</span><span class="sxs-lookup"><span data-stu-id="0cd06-115">The correlation descriptor correlation\_type<1> consists of two nibbles: the upper 4 bits describe where the expression can be found and the lower 4 bits describe the type of the expression value.</span></span>

<span data-ttu-id="0cd06-116">Верхняя часть может иметь одно из следующих пяти значений:</span><span class="sxs-lookup"><span data-stu-id="0cd06-116">The upper nibble can have one of these five values:</span></span>

``` syntax
00  FC_NORMAL_CONFORMANCE
10  FC_POINTER_CONFORMANCE
20  FC_TOP_LEVEL_CONFORMANCE
80  FC_TOP_LEVEL_MULTID_CONFORMANCE
40  FC_CONSTANT_CONFORMANCE
```

<dl> <dt>

<span data-ttu-id="0cd06-117"><span id="FC_NORMAL_CONFORMANCE"></span><span id="fc_normal_conformance"></span>\_стандартное \_ соответствие FC</span><span class="sxs-lookup"><span data-stu-id="0cd06-117"><span id="FC_NORMAL_CONFORMANCE"></span><span id="fc_normal_conformance"></span>FC\_NORMAL\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="0cd06-118">Обычная ситуация соответствия, например, описанная в поле структуры.</span><span class="sxs-lookup"><span data-stu-id="0cd06-118">A normal case of conformance, such as that described in a field of a structure.</span></span>

</dd> <dt>

<span data-ttu-id="0cd06-119"><span id="FC_POINTER_CONFORMANCE"></span><span id="fc_pointer_conformance"></span>\_соответствие указателей FC \_</span><span class="sxs-lookup"><span data-stu-id="0cd06-119"><span id="FC_POINTER_CONFORMANCE"></span><span id="fc_pointer_conformance"></span>FC\_POINTER\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="0cd06-120">Для указателей с атрибутами (**size \_ — ()**, **length \_ — ()**), которые являются полями в структуре.</span><span class="sxs-lookup"><span data-stu-id="0cd06-120">For attributed pointers (**size\_is()**, **length\_is()**) which are fields in a structure.</span></span> <span data-ttu-id="0cd06-121">Это влияет на способ установки указателя базовой памяти.</span><span class="sxs-lookup"><span data-stu-id="0cd06-121">This affects the way the base memory pointer is set.</span></span>

</dd> <dt>

<span data-ttu-id="0cd06-122"><span id="FC_TOP_LEVEL_CONFORMANCE"></span><span id="fc_top_level_conformance"></span>\_соответствие верхнего \_ уровня \_ FC</span><span class="sxs-lookup"><span data-stu-id="0cd06-122"><span id="FC_TOP_LEVEL_CONFORMANCE"></span><span id="fc_top_level_conformance"></span>FC\_TOP\_LEVEL\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="0cd06-123">Для соответствия верхнего уровня, описываемого другим параметром.</span><span class="sxs-lookup"><span data-stu-id="0cd06-123">For top-level conformance described by another parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0cd06-124"><span id="FC_TOP_LEVEL_MULTID_CONFORMANCE"></span><span id="fc_top_level_multid_conformance"></span>\_ \_ \_ многофункциональное соответствие высокого уровня FC \_</span><span class="sxs-lookup"><span data-stu-id="0cd06-124"><span id="FC_TOP_LEVEL_MULTID_CONFORMANCE"></span><span id="fc_top_level_multid_conformance"></span>FC\_TOP\_LEVEL\_MULTID\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="0cd06-125">Для соответствия верхнего уровня многомерного массива, описываемого другим параметром.</span><span class="sxs-lookup"><span data-stu-id="0cd06-125">For top-level conformance of a multidimensional array described by another parameter.</span></span>

> [!Note]  
> <span data-ttu-id="0cd06-126">Многомерные массивы и указатели активируют переключение на [**– оикф**](/windows/desktop/Midl/-oi).</span><span class="sxs-lookup"><span data-stu-id="0cd06-126">Multidimensional sized arrays and pointers trigger a switch to [**–Oicf**](/windows/desktop/Midl/-oi).</span></span>

 

</dd> <dt>

<span data-ttu-id="0cd06-127"><span id="FC_CONSTANT_CONFORMANCE"></span><span id="fc_constant_conformance"></span>\_постоянное \_ соответствие FC</span><span class="sxs-lookup"><span data-stu-id="0cd06-127"><span id="FC_CONSTANT_CONFORMANCE"></span><span id="fc_constant_conformance"></span>FC\_CONSTANT\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="0cd06-128">Для постоянного значения.</span><span class="sxs-lookup"><span data-stu-id="0cd06-128">For a constant value.</span></span> <span data-ttu-id="0cd06-129">Компилятор предварительно вычисляет значение из константного выражения, предоставленного пользователем.</span><span class="sxs-lookup"><span data-stu-id="0cd06-129">The compiler precalculates the value from a constant expression supplied by the user.</span></span> <span data-ttu-id="0cd06-130">В этом случае последующие 3 байта в описании соответствия содержат более 3 байта с длинным описанием размера соответствия.</span><span class="sxs-lookup"><span data-stu-id="0cd06-130">When this is the case, the subsequent 3 bytes in the conformance description contain the lower 3 bytes of a long describing the conformance size.</span></span> <span data-ttu-id="0cd06-131">Дальнейшие вычисления не требуются.</span><span class="sxs-lookup"><span data-stu-id="0cd06-131">No further computation is required.</span></span>

</dd> </dl>

<span data-ttu-id="0cd06-132">Нижняя часть дает тип значения, которое необходимо извлечь из памяти:</span><span class="sxs-lookup"><span data-stu-id="0cd06-132">The lower nibble gives the type of the value that needs to be extracted from memory:</span></span>

``` syntax
FC_LONG | FC_ULONG | 
FC_SHORT | FC_USHORT | 
FC_SMALL | FC_USMALL | 
FC_HYPER
```

> [!Note]
> <span data-ttu-id="0cd06-133">64-битовые выражения не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="0cd06-133">64-bit expressions are not supported.</span></span> <span data-ttu-id="0cd06-134">FC \_ Hyper используется только для **IID \_ — ()** на 64-разрядных платформах для извлечения значения указателя для IID \* .</span><span class="sxs-lookup"><span data-stu-id="0cd06-134">FC\_HYPER is used only for **iid\_is()** on 64-bit platforms to extract the pointer value for IID\*.</span></span>
>
> <span data-ttu-id="0cd06-135">Компилятор устанавливает тип, равный нулю, для следующих случаев: константное выражение, упомянутое выше, и когда необходимо вызывать подпрограмму выражения вычисления, например, когда \_ используются постоянная \_ согласованность FC и \_ ответный вызов FC.</span><span class="sxs-lookup"><span data-stu-id="0cd06-135">The compiler sets the type nibble to zero for the following cases: constant expression mentioned above and when evaluation expression routine needs to be called, for example, when FC\_CONSTANT\_CONFORMANCE and FC\_CALLBACK are used.</span></span>

 

<span data-ttu-id="0cd06-136">Размер \_ — \_ Op<1> поле позволяет применить одну из следующих операций к переменной соответствия:</span><span class="sxs-lookup"><span data-stu-id="0cd06-136">The size\_is\_op<1> field allows for one of the following operations to be applied to the conformance variable:</span></span>

``` syntax
FC_DEREFERENCE | 
FC_DIV_2 | FC_MULT_2 | FC_SUB_1 | FC_ADD_1 | 
FC_CALLBACK
```

<span data-ttu-id="0cd06-137">\_Константа разыменования FC используется для связи с точкой, например для **\[ размера \_ ( \* pL) \]**.</span><span class="sxs-lookup"><span data-stu-id="0cd06-137">The FC\_DEREFERENCE constant is used for correlation being a pointee, like for **\[size\_is(\*pL)\]**.</span></span> <span data-ttu-id="0cd06-138">Арифметические операторы просто используют указанную константу.</span><span class="sxs-lookup"><span data-stu-id="0cd06-138">Arithmetic operators just use the indicated constant.</span></span> <span data-ttu-id="0cd06-139">\_Константа обратного вызова FC указывает, что необходимо вызвать подпрограмму вычисления выражения.</span><span class="sxs-lookup"><span data-stu-id="0cd06-139">The FC\_CALLBACK constant indicates that an expression evaluation routine needs to be called.</span></span>

<span data-ttu-id="0cd06-140">Поле offset<2> обычно является относительным смещением памяти для переменной аргумента выражения.</span><span class="sxs-lookup"><span data-stu-id="0cd06-140">The offset<2> field is typically a relative memory offset to the expression argument variable.</span></span> <span data-ttu-id="0cd06-141">Это также может быть вычисление выражения — индекс подпрограммы.</span><span class="sxs-lookup"><span data-stu-id="0cd06-141">It can also be an expression evaluation–routine index.</span></span> <span data-ttu-id="0cd06-142">Как упоминалось ранее в этом документе, для константных выражений это часть фактического, завершающего значения выражения.</span><span class="sxs-lookup"><span data-stu-id="0cd06-142">As mentioned previously in this document, for constant expressions it is a part of actual, final expression value.</span></span>

<span data-ttu-id="0cd06-143">Интерпретация поля offset<2> в качестве смещения памяти зависит от сложности выражения, расположения переменной выражения и в случае массива, независимо от того, является ли массив указателем с атрибутом.</span><span class="sxs-lookup"><span data-stu-id="0cd06-143">The interpretation of the offset<2> field as memory offset depends on the complexity of the expression, the location of the expression variable, and in the case of an array, whether the array is actually an attributed pointer.</span></span>

<span data-ttu-id="0cd06-144">Если массив является указателем с атрибутами, а переменная соответствия является полем в структуре, Поле Offset содержит смещение от начала структуры до поля, описывающего соответствие.</span><span class="sxs-lookup"><span data-stu-id="0cd06-144">If the array is an attributed pointer and the conformance variable is a field in a structure, the offset field contains the offset from the beginning of the structure to the conformance-describing field.</span></span> <span data-ttu-id="0cd06-145">Если массив не является указателем с атрибутом, а переменная соответствия является полем в структуре, Поле Offset содержит смещение от конца несогласованной части структуры к полю, описывающему соответствие.</span><span class="sxs-lookup"><span data-stu-id="0cd06-145">If the array is not an attributed pointer and the conformance variable is a field in a structure, the offset field contains the offset from the end of the nonconformant part of the structure to the conformance-describing field.</span></span> <span data-ttu-id="0cd06-146">Как правило, согласованный массив находится в конце структуры.</span><span class="sxs-lookup"><span data-stu-id="0cd06-146">Typically, the conformant array is at the end of the structure.</span></span>

<span data-ttu-id="0cd06-147">Для соответствия верхнего уровня поле offset содержит смещение от расположения первого параметра заглушки в стеке с параметром, описывающим соответствие.</span><span class="sxs-lookup"><span data-stu-id="0cd06-147">For top-level conformance, the offset field contains the offset from the stub's first parameter's location on the stack to the parameter that describes the conformance.</span></span> <span data-ttu-id="0cd06-148">Он не используется в режиме **операционной системы** .</span><span class="sxs-lookup"><span data-stu-id="0cd06-148">This is not used in **–Os** mode.</span></span> <span data-ttu-id="0cd06-149">Существуют другие исключения для интерпретации поля смещения. такие исключения описаны в описании этих типов.</span><span class="sxs-lookup"><span data-stu-id="0cd06-149">There are other exceptions to the interpretation of the offset field; such exceptions are described in the description of those types.</span></span>

<span data-ttu-id="0cd06-150">Если offset<2> используется с \_ обратным вызовом FC, он содержит индекс в таблице подпрограммы вычисления выражений, созданной компилятором.</span><span class="sxs-lookup"><span data-stu-id="0cd06-150">When offset<2> is used with FC\_CALLBACK, it contains an index in the expression evaluation routine table generated by the compiler.</span></span> <span data-ttu-id="0cd06-151">Сообщение-заглушку передается в подпрограмму оценки, которая затем выполняет вычисление значения соответствия и присваивает его полю MaxCount сообщения-заглушки.</span><span class="sxs-lookup"><span data-stu-id="0cd06-151">The stub message is passed to the evaluation routine, which then computes the conformance value and assigns it to the MaxCount field of the stub message.</span></span>

<span data-ttu-id="0cd06-152">\_Для Windows 2000 был добавлен надежный флаг<2> для поддержки [**/robust**](/windows/desktop/Midl/-robust), например функции «отказ в атаке».</span><span class="sxs-lookup"><span data-stu-id="0cd06-152">The robust\_flags<2> field has been added for Windows 2000 to support [**/robust**](/windows/desktop/Midl/-robust), such as the denial-of-attacks feature.</span></span> <span data-ttu-id="0cd06-153">В первом байте определены следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="0cd06-153">The following flags are defined on the first byte:</span></span>

``` syntax
typedef  struct  _NDR_CORRELATION_FLAGS
  {
  unsigned char   Early     : 1;
  unsigned char   Split     : 1;
  unsigned char   IsIidIs   : 1;
  unsigned char   DontCheck : 1;
  unsigned char   Unused    : 4;
  } NDR_CORRELATION_FLAGS;
```

<span data-ttu-id="0cd06-154">Ранний флаг означает раннее и позднее корреляцию.</span><span class="sxs-lookup"><span data-stu-id="0cd06-154">The Early flag indicates early versus late correlation.</span></span> <span data-ttu-id="0cd06-155">Ранняя корреляция заключается в том, что аргумент выражения предшествует описанному аргументу, например, аргумент размера находится перед аргументом указателя размера.</span><span class="sxs-lookup"><span data-stu-id="0cd06-155">An early correlation is when the expression argument precedes the described argument, for example a size argument is before a sized pointer argument.</span></span> <span data-ttu-id="0cd06-156">Позднее корреляция происходит, когда аргумент выражения поступает после связанного аргумента.</span><span class="sxs-lookup"><span data-stu-id="0cd06-156">A late correlation is when the expression argument comes after the related argument.</span></span> <span data-ttu-id="0cd06-157">Подсистема выполняет проверку значений раннего корреляции прямо сейчас. значения поздней корреляции сохраняются для проверки после завершения распаковки.</span><span class="sxs-lookup"><span data-stu-id="0cd06-157">The engine performs validation of early correlation values right away, the late correlation values are stored for checking after unmarshaling is done.</span></span>

<span data-ttu-id="0cd06-158">Флаг разбиения указывает на асинхронное разбиение между \[ \] \[ аргументами in и out \] .</span><span class="sxs-lookup"><span data-stu-id="0cd06-158">The Split flag indicates an async split among \[in\] and \[out\] arguments.</span></span> <span data-ttu-id="0cd06-159">Например, аргумент размера может быть в, \[ \] пока указатель имеет размер \[ \] .</span><span class="sxs-lookup"><span data-stu-id="0cd06-159">For example, a size argument may be \[in\] while the sized pointer may be \[out\].</span></span> <span data-ttu-id="0cd06-160">В асинхронном контексте DCOM эти аргументы находятся в разных стеках, поэтому подсистема должна быть осведомлена об этом.</span><span class="sxs-lookup"><span data-stu-id="0cd06-160">In the DCOM async context, these arguments happen to be on different stacks, so the engine must be aware of this.</span></span>

<span data-ttu-id="0cd06-161">Флаг Исиидис указывает, что **IID \_ имеет значение ()** корреляции.</span><span class="sxs-lookup"><span data-stu-id="0cd06-161">The IsIidIs flag indicates an **iid\_is()** correlation.</span></span> <span data-ttu-id="0cd06-162">Подпрограммы Ндркомпутеконформанце привлекают указатель на IID в качестве значения выражения, но подпрограммы проверки не могут сравнивать такие значения (они будут указателями), поэтому флаг указывает на необходимость сравнения фактического идентификаторов IID.</span><span class="sxs-lookup"><span data-stu-id="0cd06-162">The NdrComputeConformance routine is tricked to obtain a pointer to IID as an expression value, but the validation routine cannot compare such values (they would be pointers) and so the flag indicates that actual IIDs need to be compared.</span></span>

### <a name="variance-description-and-other-array-attributes"></a><span data-ttu-id="0cd06-163">Описание дисперсии и другие атрибуты массива</span><span class="sxs-lookup"><span data-stu-id="0cd06-163">Variance Description and Other Array Attributes</span></span>

<span data-ttu-id="0cd06-164">Формат поля Описание дисперсии идентичен полю описание соответствия.</span><span class="sxs-lookup"><span data-stu-id="0cd06-164">The variance description field format is identical to the conformance description field.</span></span> <span data-ttu-id="0cd06-165">Разница заключается в том, что модуль доставки NDR использует другое поле сообщения-заглушки как временную переменную.</span><span class="sxs-lookup"><span data-stu-id="0cd06-165">The difference is that a different stub message field is used by the NDR engine as a temporary variable.</span></span> <span data-ttu-id="0cd06-166">В случае с описанием дисперсии это оцениваемая длина, и соответствующее поле называется Актуалленгс.</span><span class="sxs-lookup"><span data-stu-id="0cd06-166">In the case of variance description, it is the length that is evaluated and the corresponding field is called ActualLength.</span></span>

<span data-ttu-id="0cd06-167">С вариативностью начальное смещение обычно равно нулю и подсистема настроена соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="0cd06-167">With variance, the starting offset is typically zero and the engine is tuned accordingly.</span></span> <span data-ttu-id="0cd06-168">Если к стандартному массиву применяется **первый атрибут \_ ()** , то принудительный обратный вызов подпрограммы вычисления выражения является обязательным.</span><span class="sxs-lookup"><span data-stu-id="0cd06-168">If the **first\_is()** attribute is applied to a conformant varying array, a callback to an expression evaluation routine is forced.</span></span>

 

 