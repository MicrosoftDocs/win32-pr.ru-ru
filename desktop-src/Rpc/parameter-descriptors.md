---
title: Дескрипторы параметров
description: Как упоминалось ранее, дескрипторы параметров стилей стиля ОИФ существуют \ 8211; Oi и \ 8211;.
ms.assetid: c2dad284-abe5-4b38-b3a6-3c7373fc5b84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f6f8b19eb6632c4111547925151865b03b9adc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793207"
---
# <a name="parameter-descriptors"></a><span data-ttu-id="78902-103">Дескрипторы параметров</span><span class="sxs-lookup"><span data-stu-id="78902-103">Parameter Descriptors</span></span>

<span data-ttu-id="78902-104">Как упоминалось ранее, дескрипторы параметров стиля ( [**Oi**](/windows/desktop/Midl/-oi) и **– ОИФ** ) существуют.</span><span class="sxs-lookup"><span data-stu-id="78902-104">As mentioned previously, [**–Oi**](/windows/desktop/Midl/-oi) and **–Oif** style parameter descriptors exist.</span></span>

## <a name="the-oi-parameter-descriptors"></a><span data-ttu-id="78902-105">Дескрипторы параметров – OI</span><span class="sxs-lookup"><span data-stu-id="78902-105">The –Oi Parameter Descriptors</span></span>

<span data-ttu-id="78902-106">Для полностью интерпретируемых заглушек требуется дополнительная информация для каждого параметра в вызове RPC.</span><span class="sxs-lookup"><span data-stu-id="78902-106">Fully interpreted stubs require additional information for each of the parameters in an RPC call.</span></span> <span data-ttu-id="78902-107">Описания параметров процедуры следуют сразу после описания процедуры.</span><span class="sxs-lookup"><span data-stu-id="78902-107">The parameter descriptions of a procedure follow immediately after the description of the procedure.</span></span>

[<span data-ttu-id="78902-108">**Simple — OI**</span><span class="sxs-lookup"><span data-stu-id="78902-108">**Simple –Oi**</span></span>](/windows/desktop/Midl/-oi)

<span data-ttu-id="78902-109">**Дескрипторы параметров**</span><span class="sxs-lookup"><span data-stu-id="78902-109">**Parameter Descriptors**</span></span>

<span data-ttu-id="78902-110">Формат описания для \[  \] параметра простого типа в или возвращает:</span><span class="sxs-lookup"><span data-stu-id="78902-110">The format for the description of an \[**in**\] or return simple type parameter is:</span></span>

``` syntax
FC_IN_PARAM_BASETYPE 
simple_type<1>
```

<span data-ttu-id="78902-111">–или–</span><span class="sxs-lookup"><span data-stu-id="78902-111">–or–</span></span>

``` syntax
FC_RETURN_PARAM_BASETYPE 
simple_type<1>
```

<span data-ttu-id="78902-112">Где простой \_ тип<1> — это маркер FC, указывающий простой тип.</span><span class="sxs-lookup"><span data-stu-id="78902-112">Where simple\_type<1> is the FC token indicating the simple type.</span></span> <span data-ttu-id="78902-113">Ниже приведены коды этих кодов.</span><span class="sxs-lookup"><span data-stu-id="78902-113">The codes are as follows:</span></span>

``` syntax
4e  FC_IN_PARAM_BASETYPE 
53  FC_RETURN_PARAM_BASETYPE
```

<span data-ttu-id="78902-114">**Другие — OI**</span><span class="sxs-lookup"><span data-stu-id="78902-114">**Other –Oi**</span></span>

<span data-ttu-id="78902-115">**Дескрипторы параметров**</span><span class="sxs-lookup"><span data-stu-id="78902-115">**Parameter Descriptors**</span></span>

<span data-ttu-id="78902-116">Формат описания для всех других типов параметров:</span><span class="sxs-lookup"><span data-stu-id="78902-116">The format for the description for all other parameter types is:</span></span>

``` syntax
param_direction<1> 
stack_size<1> 
type_offset<2>
```

<span data-ttu-id="78902-117">Где \_ поле direction<1> для каждого из этих описаний должно быть одним из показанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="78902-117">Where the param\_direction<1> field for each of these descriptions must be one of those shown in the following table.</span></span>



| <span data-ttu-id="78902-118">Hex</span><span class="sxs-lookup"><span data-stu-id="78902-118">Hex</span></span> | <span data-ttu-id="78902-119">Flag</span><span class="sxs-lookup"><span data-stu-id="78902-119">Flag</span></span>                          | <span data-ttu-id="78902-120">Значение</span><span class="sxs-lookup"><span data-stu-id="78902-120">Meaning</span></span>                                                     |
|-----|-------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="78902-121">4d</span><span class="sxs-lookup"><span data-stu-id="78902-121">4d</span></span>  | <span data-ttu-id="78902-122">FC \_ в \_ param</span><span class="sxs-lookup"><span data-stu-id="78902-122">FC\_IN\_PARAM</span></span>                 | <span data-ttu-id="78902-123">Параметр in.</span><span class="sxs-lookup"><span data-stu-id="78902-123">An in parameter.</span></span>                                            |
| <span data-ttu-id="78902-124">50</span><span class="sxs-lookup"><span data-stu-id="78902-124">50</span></span>  | <span data-ttu-id="78902-125">\_ \_ выходной \_ параметр FC</span><span class="sxs-lookup"><span data-stu-id="78902-125">FC\_IN\_OUT\_PARAM</span></span>            | <span data-ttu-id="78902-126">Параметр in/out.</span><span class="sxs-lookup"><span data-stu-id="78902-126">An in/out parameter.</span></span>                                        |
| <span data-ttu-id="78902-127">51</span><span class="sxs-lookup"><span data-stu-id="78902-127">51</span></span>  | <span data-ttu-id="78902-128">\_выходной \_ параметр FC</span><span class="sxs-lookup"><span data-stu-id="78902-128">FC\_OUT\_PARAM</span></span>                | <span data-ttu-id="78902-129">Выходной параметр.</span><span class="sxs-lookup"><span data-stu-id="78902-129">An out parameter.</span></span>                                           |
| <span data-ttu-id="78902-130">52</span><span class="sxs-lookup"><span data-stu-id="78902-130">52</span></span>  | <span data-ttu-id="78902-131">FC \_ return \_ param</span><span class="sxs-lookup"><span data-stu-id="78902-131">FC\_RETURN\_PARAM</span></span>             | <span data-ttu-id="78902-132">Возвращаемое значение процедуры.</span><span class="sxs-lookup"><span data-stu-id="78902-132">A procedure return value.</span></span>                                   |
| <span data-ttu-id="78902-133">4F</span><span class="sxs-lookup"><span data-stu-id="78902-133">4f</span></span>  | <span data-ttu-id="78902-134">FC \_ в \_ param \_ без \_ бесплатных \_ inst</span><span class="sxs-lookup"><span data-stu-id="78902-134">FC\_IN\_PARAM\_NO\_FREE\_INST</span></span> | <span data-ttu-id="78902-135">В xmit/представитель в качестве параметра, для которого не выполняется освобождение.</span><span class="sxs-lookup"><span data-stu-id="78902-135">An in xmit/rep as a parameter for which no freeing is made.</span></span> |



 

<span data-ttu-id="78902-136">Размер стека \_<1> — это размер параметра в стеке, выраженный в виде числа целочисленных параметров, занимаемых параметром в стеке.</span><span class="sxs-lookup"><span data-stu-id="78902-136">The stack\_size<1> is the size of the parameter on the stack, expressed as the number of integers the parameter occupies on the stack.</span></span>

> [!Note]  
> <span data-ttu-id="78902-137">Режим [**– Oi**](/windows/desktop/Midl/-oi) не поддерживается на 64-разрядных платформах.</span><span class="sxs-lookup"><span data-stu-id="78902-137">The [**–Oi**](/windows/desktop/Midl/-oi) mode is not supported on 64-bit platforms.</span></span>

 

<span data-ttu-id="78902-138">Смещение типа \_<2> поле является смещением в таблице строк формата типа, которое указывает дескриптор типа для аргумента.</span><span class="sxs-lookup"><span data-stu-id="78902-138">The type\_offset<2> field is the offset in the type format string table, indicating the type descriptor for the argument.</span></span>

## <a name="the-oif-parameter-descriptors"></a><span data-ttu-id="78902-139">Дескрипторы параметров – ОИФ</span><span class="sxs-lookup"><span data-stu-id="78902-139">The –Oif Parameter Descriptors</span></span>

<span data-ttu-id="78902-140">Существует два возможных формата описания параметра: одно для базовых типов, другое — для всех других типов.</span><span class="sxs-lookup"><span data-stu-id="78902-140">There are two possible formats for a parameter description, one for base types, another for all other types.</span></span>

<span data-ttu-id="78902-141">Базовые типы:</span><span class="sxs-lookup"><span data-stu-id="78902-141">Base types:</span></span>

``` syntax
PARAM_ATTRIBUTES<2> 
stack_offset<2> 
type_format_char<1> 
unused<1>
```

<span data-ttu-id="78902-142">Другие возможности:</span><span class="sxs-lookup"><span data-stu-id="78902-142">Other:</span></span>

``` syntax
PARAM_ATTRIBUTES<2> 
stack_offset<2> 
type_offset<2>
```

<span data-ttu-id="78902-143">В обоих \_ смещениях стека<2> указывает смещение в стеке виртуальных аргументов в байтах.</span><span class="sxs-lookup"><span data-stu-id="78902-143">In both stack\_offset<2> indicates the offset on the virtual argument stack, in bytes.</span></span> <span data-ttu-id="78902-144">Для базовых типов тип аргумента указывается непосредственно символом формата, соответствующим типу.</span><span class="sxs-lookup"><span data-stu-id="78902-144">For base types, the argument type is given directly by the format character corresponding to the type.</span></span> <span data-ttu-id="78902-145">Для других типов \_ смещение типа<2> предоставляет смещение в таблице строк формата типа, где находится дескриптор типа для аргумента.</span><span class="sxs-lookup"><span data-stu-id="78902-145">For other types, the type\_offset<2> field gives the offset in the type format string table where the type descriptor for the argument is located.</span></span>

<span data-ttu-id="78902-146">Поле атрибута параметра определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="78902-146">The parameter attribute field is defined as follows:</span></span>

``` syntax
typedef struct
  {
  unsigned short  MustSize            : 1;    // 0x0001
  unsigned short  MustFree            : 1;    // 0x0002
  unsigned short  IsPipe              : 1;    // 0x0004
  unsigned short  IsIn                : 1;    // 0x0008
  unsigned short  IsOut               : 1;    // 0x0010
  unsigned short  IsReturn            : 1;    // 0x0020
  unsigned short  IsBasetype          : 1;    // 0x0040
  unsigned short  IsByValue           : 1;    // 0x0080
  unsigned short  IsSimpleRef         : 1;    // 0x0100
  unsigned short  IsDontCallFreeInst  : 1;    // 0x0200
  unsigned short  SaveForAsyncFinish  : 1;    // 0x0400
  unsigned short  Unused              : 2;
  unsigned short  ServerAllocSize     : 3;    // 0xe000
  } PARAM_ATTRIBUTES, *PPARAM_ATTRIBUTES;
```

-   <span data-ttu-id="78902-147">Бит **мустсизе** задается только в том случае, если параметр должен иметь размер.</span><span class="sxs-lookup"><span data-stu-id="78902-147">The **MustSize** bit is set only if the parameter must be sized.</span></span>
-   <span data-ttu-id="78902-148">Бит **мустфри** устанавливается, если сервер должен вызвать \* подпрограммы ндрфри параметра.</span><span class="sxs-lookup"><span data-stu-id="78902-148">The **MustFree** bit is set if the server must call the parameter's NdrFree\* routine.</span></span>
-   <span data-ttu-id="78902-149">Бит **иссимплереф** задается для параметра, который является указателем ссылки на что-либо, кроме другого указателя, и не имеет выделенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="78902-149">The **IsSimpleRef** bit is set for a parameter that is a reference pointer to anything other than another pointer, and which has no allocate attributes.</span></span> <span data-ttu-id="78902-150">Для такого типа,<> поле смещения типа описания параметра \_ , за исключением указателя ссылки на базовый тип, предоставляет смещение для типа референт; указатель ссылки просто пропускается.</span><span class="sxs-lookup"><span data-stu-id="78902-150">For such a type, the parameter description's type\_offset<> field, except for a reference pointer to a base type, provides the offset to the referent's type; the reference pointer is simply skipped.</span></span>
-   <span data-ttu-id="78902-151">Бит **исдонткаллфриинст** задается для определенных \_ параметров представления как параметры, подпрограммы бесплатных экземпляров которых не должны вызываться.</span><span class="sxs-lookup"><span data-stu-id="78902-151">The **IsDontCallFreeInst** bit is set for certain represent\_as parameters whose free instance routines should not be called.</span></span>
-   <span data-ttu-id="78902-152">Биты **сервераллоксизе** не равны нулю, если параметр находится в, а также находится в \[  \] \[  \] \[  \] указателе на указатель или на enum16, и инициализируется в стеке интерпретатора сервера вместо того, чтобы использовать вызов **I \_ рпкаллокате**.</span><span class="sxs-lookup"><span data-stu-id="78902-152">The **ServerAllocSize** bits are nonzero if the parameter is \[**out**\], \[**in**\], or \[**in,out**\] pointer to pointer, or pointer to enum16, and will be initialized on the server interpreter's stack, rather than using a call to **I\_RpcAllocate**.</span></span> <span data-ttu-id="78902-153">Если не равно нулю, это значение умножается на 8, чтобы получить число байтов для параметра.</span><span class="sxs-lookup"><span data-stu-id="78902-153">If nonzero, this value is multiplied by 8 to get the number of bytes for the parameter.</span></span> <span data-ttu-id="78902-154">Обратите внимание, что это означает, что для указателя всегда выделяется по меньшей мере 8 байт.</span><span class="sxs-lookup"><span data-stu-id="78902-154">Note that doing so means at least 8 bytes are always allocated for a pointer.</span></span>
-   <span data-ttu-id="78902-155">Бит **исбасетипе** устанавливается для простых типов, которые маршалируются с помощью цикла интерпретатора [**-ОИФ**](/windows/desktop/Midl/-oi) "основной".</span><span class="sxs-lookup"><span data-stu-id="78902-155">The **IsBasetype** bit is set for simple types that are being marshaled by the main [**–Oif**](/windows/desktop/Midl/-oi) interpreter loop.</span></span> <span data-ttu-id="78902-156">В частности, простой тип с атрибутом Range в нем не помечается как базовый тип, чтобы принудительно выполнять упаковку подпрограммы диапазона посредством диспетчеризации с помощью \_ токена диапазона FC.</span><span class="sxs-lookup"><span data-stu-id="78902-156">In particular, a simple type with a range attribute on it is not flagged as a base type in order to force the range routine marshaling through dispatching using an FC\_RANGE token.</span></span>
-   <span data-ttu-id="78902-157">Бит **исбивалуе** задается для составных типов, отправляемых по значению, но не задается для простых типов, независимо от того, является ли аргумент указателем.</span><span class="sxs-lookup"><span data-stu-id="78902-157">The **IsByValue** bit is set for compound types being sent by value, but is not set for simple types, regardless of whether the argument is a pointer.</span></span> <span data-ttu-id="78902-158">Составные типы, для которых оно задано, — это структуры, объединения, [**передачи \_ как**](/windows/desktop/Midl/transmit-as), которые [**представляют \_ собой**](/windows/desktop/Midl/represent-as) [**проводной \_**](/windows/desktop/Midl/wire-marshal) и SAFEARRAY.</span><span class="sxs-lookup"><span data-stu-id="78902-158">The compound types for which it is set are structures, unions, [**transmit\_as**](/windows/desktop/Midl/transmit-as), [**represent\_as**](/windows/desktop/Midl/represent-as), [**wire\_marshal**](/windows/desktop/Midl/wire-marshal) and SAFEARRAY.</span></span> <span data-ttu-id="78902-159">В целом, бит был представлен для преимуществ основного цикла интерпретатора в интерпретаторе [**– оикф**](/windows/desktop/Midl/-oi) , чтобы гарантировать правильную разыменование непростых аргументов (называемых аргументами составного типа).</span><span class="sxs-lookup"><span data-stu-id="78902-159">In general, the bit was introduced for the benefit of the main interpreter loop in the [**–Oicf**](/windows/desktop/Midl/-oi) interpreter, to ensure the nonsimple arguments (referred to as compound type arguments) are properly dereferenced.</span></span> <span data-ttu-id="78902-160">Этот бит никогда не использовался в предыдущих версиях интерпретатора.</span><span class="sxs-lookup"><span data-stu-id="78902-160">This bit was never used in previous versions of the interpreter.</span></span>

 

 