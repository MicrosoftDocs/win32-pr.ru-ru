---
title: Методы IDL для лучшего проектирования интерфейсов и методов
description: Рассмотрите возможность использования следующих методов языка IDL для повышения безопасности и производительности при разработке интерфейсов RPC и методов, обрабатывающих как согласованные, так и варианты данных.
ms.assetid: 651bdb5c-ad56-4526-9b7d-7165141e7ceb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b897d8d1f2f5e1c11a5328fb095341871e3689e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410869"
---
# <a name="idl-techniques-for-better-interface-and-method-design"></a><span data-ttu-id="70b78-103">Методы IDL для лучшего проектирования интерфейсов и методов</span><span class="sxs-lookup"><span data-stu-id="70b78-103">IDL Techniques for Better Interface and Method Design</span></span>

<span data-ttu-id="70b78-104">Рассмотрите возможность использования следующих методов языка IDL для повышения безопасности и производительности при разработке интерфейсов RPC и методов, обрабатывающих как согласованные, так и варианты данных.</span><span class="sxs-lookup"><span data-stu-id="70b78-104">Consider using the following IDL-specific techniques to improve security and performance when you are developing RPC interfaces and methods that handle both conformant and variant data.</span></span> <span data-ttu-id="70b78-105">Атрибуты, упоминаемые в этом разделе, являются атрибутами IDL, заданными в параметрах метода, обрабатывающих либо согласованные данные (например, \[ **размер \_** \] и \[ **максимум \_ —** \] атрибуты), либо данные типа Variant (например, \[ **длина \_** \] и \[ атрибуты **строки** \] ).</span><span class="sxs-lookup"><span data-stu-id="70b78-105">The attributes referred to in this topic are the IDL attributes set on method parameters that handle either conformant data (for example, the \[**size\_is**\] and \[**max\_is**\] attributes) or variant data (for example, the \[**length\_is**\] and \[**string**\] attributes).</span></span>

## <a name="using-the-range-attribute-with-conformant-data-parameters"></a><span data-ttu-id="70b78-106">Использование \[ атрибута Range \] с параметрами согласованных данных</span><span class="sxs-lookup"><span data-stu-id="70b78-106">Using the \[range\] Attribute with Conformant Data Parameters</span></span>

<span data-ttu-id="70b78-107">Атрибут \[ **Range** \] указывает среде выполнения RPC выполнить дополнительную проверку размера во время процесса демаршалирования данных.</span><span class="sxs-lookup"><span data-stu-id="70b78-107">The \[**range**\] attribute instructs the RPC run-time to perform additional size validation during the data unmarshaling process.</span></span> <span data-ttu-id="70b78-108">В частности, он проверяет, что указанный размер данных, переданный в качестве связанного параметра, находится в пределах указанного диапазона.</span><span class="sxs-lookup"><span data-stu-id="70b78-108">Specifically, it verifies that the supplied size of the data passed as the associated parameter is within the specified range.</span></span>

<span data-ttu-id="70b78-109">Атрибут \[ **Range** \] не влияет на формат сети.</span><span class="sxs-lookup"><span data-stu-id="70b78-109">The \[**range**\] attribute does not affect wire format.</span></span>

<span data-ttu-id="70b78-110">Если значение на линии подключения выходит за пределы допустимого диапазона, RPC выдает исключение "RPC \_ x \_ invalidd \_ или RPC \_ x \_ Bad" \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="70b78-110">If the value on wire is outside of the allowed range, RPC will throw an RPC\_X\_INVALID\_BOUND or RPC\_X\_BAD\_STUB\_DATA exception.</span></span> <span data-ttu-id="70b78-111">Это обеспечивает дополнительный уровень проверки данных и может помочь предотвратить распространенные ошибки безопасности, такие как переполнение буфера.</span><span class="sxs-lookup"><span data-stu-id="70b78-111">This provides an additional level of data validation, and can help prevent common security errors like buffer overruns.</span></span> <span data-ttu-id="70b78-112">Аналогично, использование \[ **диапазона** \] может повысить производительность приложения, поскольку согласованные данные, отмеченные им, имеют четко определенные ограничения, доступные для рассмотрения службой RPC.</span><span class="sxs-lookup"><span data-stu-id="70b78-112">Likewise, using \[**range**\] can improve application performance, since conformant data marked with it has clearly-defined constraints available for consideration by the RPC service.</span></span>

## <a name="rpc-server-stub-memory-management-rules"></a><span data-ttu-id="70b78-113">Правила управления памятью заглушки RPC-сервера</span><span class="sxs-lookup"><span data-stu-id="70b78-113">RPC Server Stub Memory Management Rules</span></span>

<span data-ttu-id="70b78-114">При создании IDL-файлов для приложения с поддержкой RPC важно понимать правила управления памятью заглушки RPC-сервера.</span><span class="sxs-lookup"><span data-stu-id="70b78-114">It is important to understand RPC server stub memory management rules when creating the IDL files for an RPC-enabled application.</span></span> <span data-ttu-id="70b78-115">Приложения могут улучшить использование ресурсов сервера с помощью \[ **диапазона** \] в сочетании с согласованными данными, как указано выше, а также намеренно избегать применения атрибутов IDL данных переменной длины, таких как \[ **\_ ,** например, длины, \] к согласованным данным.</span><span class="sxs-lookup"><span data-stu-id="70b78-115">Applications can improve server resource utilization by using \[**range**\] in conjunction with conformant data as indicated above, as well as deliberately avoiding the application of variable-length data IDL attributes like like \[**length\_is**\] to conformant data.</span></span>

<span data-ttu-id="70b78-116">Применение \[ **длины \_** не \] рекомендуется для полей структуры данных, определенных в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="70b78-116">The application of \[**length\_is**\] to data structure fields defined in an IDL file is not recommended.</span></span>

## <a name="best-practices-for-variable-length-data-parameters"></a><span data-ttu-id="70b78-117">Рекомендации по использованию параметров данных переменной длины</span><span class="sxs-lookup"><span data-stu-id="70b78-117">Best Practices for Variable-length Data Parameters</span></span>

<span data-ttu-id="70b78-118">Ниже приведены некоторые рекомендации, которые следует учитывать при определении атрибутов IDL для структур данных с переменным размером, параметров и полей методов.</span><span class="sxs-lookup"><span data-stu-id="70b78-118">The following are several best practices to consider when defining the IDL attributes for variable-sized data structures, method parameters and fields.</span></span>

-   <span data-ttu-id="70b78-119">Используйте раннее корреляцию.</span><span class="sxs-lookup"><span data-stu-id="70b78-119">Use early correlation.</span></span> <span data-ttu-id="70b78-120">Обычно лучше определить параметр или поле размера переменной, чтобы оно наблюдаться сразу после целочисленного типа управления.</span><span class="sxs-lookup"><span data-stu-id="70b78-120">It is generally better to define the variable size parameter or field such that it occurs immediately after the controlling integral type.</span></span>

    <span data-ttu-id="70b78-121">Например,</span><span class="sxs-lookup"><span data-stu-id="70b78-121">For example,</span></span>

    ``` syntax
    earlyCorr
    (
    [in, range(MIN_COUNT, MAX_COUNT)] long size, 
    [in,size_is(size)] char *pv
    );
    ```

    <span data-ttu-id="70b78-122">лучше, чем</span><span class="sxs-lookup"><span data-stu-id="70b78-122">is better than</span></span>

    ``` syntax
    lateCorr
    (
    [in,size_is(size)] char *pv, 
    [in, range(MIN_COUNT, MAX_COUNT)] long size)
    );
    ```

    <span data-ttu-id="70b78-123">Where **еарликорр** объявляет параметр size непосредственно перед параметром данных переменной длины, а **латекорр** объявляет параметр size после него.</span><span class="sxs-lookup"><span data-stu-id="70b78-123">wherein **earlyCorr** declares the size parameter immediately before the variable-length data parameter, and **lateCorr** declares the size parameter after it.</span></span> <span data-ttu-id="70b78-124">Использование раннего соответствия повышает производительность в целом, особенно в тех случаях, когда метод вызывается часто.</span><span class="sxs-lookup"><span data-stu-id="70b78-124">Using early correspondence improves performance overall, especially in cases where the method is called frequently.</span></span>

-   <span data-ttu-id="70b78-125">Для параметров, помеченных \[ атрибутом **out \_ , Size** \] и, где длина данных известна на стороне клиента или когда клиент имеет приемлемую верхнюю границу, определение метода должно быть похоже на следующее с точки зрения атрибутов и последовательности параметров:</span><span class="sxs-lookup"><span data-stu-id="70b78-125">For parameters marked with the \[**out, size\_is**\] attribute tuple, and where the data length is known on the client side or where the client has a reasonable upper bound, the method definition should be similar to the following in terms of parameter attribution and sequence:</span></span>

    ``` syntax
    outKnownSize
    (
    [in,range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out,size_is(lSize)] UserDataType * pArr
    );
    ```

    <span data-ttu-id="70b78-126">В этом случае клиент предоставляет буфер фиксированного размера для *Парр*, позволяя службе RPC на стороне сервера выделить буфер достаточного размера с хорошей степенью гарантии.</span><span class="sxs-lookup"><span data-stu-id="70b78-126">In this case, the client provides a fixed size buffer for *pArr*, allowing the server-side RPC service to allocate a reasonably-sized buffer with a good degree of assurance.</span></span> <span data-ttu-id="70b78-127">Обратите внимание, что в примере данные получаются с сервера ( \[ **out** \] ).</span><span class="sxs-lookup"><span data-stu-id="70b78-127">Note that in the example the data is received from the server (\[**out**\]).</span></span> <span data-ttu-id="70b78-128">Определение аналогично тому, что данные передаются на сервер ( \[ **в** \] ).</span><span class="sxs-lookup"><span data-stu-id="70b78-128">The definition is similar for data passed to the server (\[**in**\]).</span></span>

-   <span data-ttu-id="70b78-129">В ситуациях, когда серверный компонент RPC-приложения определяет длину данных, определение метода должно выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="70b78-129">For situations where the server-side component of an RPC application decides the data length, the method definition should be similar to the following:</span></span>

    ``` syntax
    typedef [range(MIN_COUNT,MAX_COUNT)] long RANGED_LONG;

    outUnknownSize
    (
    [out] RANGED_LONG *pSize,
    [out,size_is(,*pSize)] UserDataType **ppArr
    );
    ```

    <span data-ttu-id="70b78-130">**С \_ диапазоном LONG** — это тип, определенный для заглушек клиента и сервера, и указанного размера, который клиент может правильно предвидеть.</span><span class="sxs-lookup"><span data-stu-id="70b78-130">**RANGED\_LONG** is a type defined for both the client and server stubs, and of a specified size the client can correctly anticipate.</span></span> <span data-ttu-id="70b78-131">В этом примере клиент передает *ппарр* как **null**, а компонент серверного приложения RPC выделяет правильный объем памяти.</span><span class="sxs-lookup"><span data-stu-id="70b78-131">In the example, the client passes *ppArr* as **NULL**, and the RPC server application component allocates the correct amount of memory.</span></span> <span data-ttu-id="70b78-132">После возврата служба RPC на стороне клиента выделяет память для возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="70b78-132">Upon return, the RPC service on the client side allocates the memory for the returned data.</span></span>

-   <span data-ttu-id="70b78-133">Если клиент хочет отправить подмножество большого согласованного массива на сервер, приложение может указать размер подмножества, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="70b78-133">If the client wants to send a subset of a large conformant array to the server, the application can specify the size of the subset as demonstrated in the following example:</span></span>

    ``` syntax
    inConformantVaryingArray
    (
    [in,range(MIN_COUNT,MAX_COUNT)] long lSize,
    [in] long lLength, 
    [in,size_is(lSize), length_is(lLength)] UserDataType *pArr
    );
    ```

    <span data-ttu-id="70b78-134">Таким образом, RPC будет передавать только элементы *лленгс* массива по каналу передачи.</span><span class="sxs-lookup"><span data-stu-id="70b78-134">This way RPC will only transmit *lLength* elements of the array across the wire.</span></span> <span data-ttu-id="70b78-135">Однако это определение заставляет службу RPC выделять память размером *лсизе* на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="70b78-135">However, this definition forces the RPC service to allocate memory of size *lSize* on the server side.</span></span>

-   <span data-ttu-id="70b78-136">Если компонент клиентского приложения определяет максимальный размер массива, который может быть возвращен сервером, но позволяет серверу передавать подмножество этого массива, приложение может указать такое поведение, определив IDL, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="70b78-136">If the client application component determines the maximum size of an array the server can return, but allows the server to transmit a subset of that array, the application can specify such a behavior by defining the IDL similar to the following example:</span></span>

    ``` syntax
    inMaxSizeOutLength
    (
    [in, range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out] long *pLength,
    [out,size_is(lSize), length_is(*pLength)] UserDataType *pArr
    );
    ```

    <span data-ttu-id="70b78-137">Компонент клиентского приложения задает максимальный размер массива, а сервер указывает, сколько элементов он передает клиенту.</span><span class="sxs-lookup"><span data-stu-id="70b78-137">The client application component specifies the maximum size of the array, and the server specifies how many elements it transmits back to the client.</span></span>

-   <span data-ttu-id="70b78-138">Если компонент серверного приложения должен вернуть строку в компонент клиентского приложения и если клиент знает максимальный размер, возвращаемый сервером, приложение может использовать согласованный строковый тип, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="70b78-138">If the server application component needs to return a string to the client application component, and if the client knows the maximum size to be returned from the server, the application can use a conformant string type as demonstrated in the following example:</span></span>

    ``` syntax
    outStringKnownSize
    (
    [in,range(MIN_COUNT, MAX_STRING)] long lSize,
    [out,size_is(lSize),string] wchar_t *pString
    );
    ```

-   <span data-ttu-id="70b78-139">Если компонент клиентского приложения не должен управлять размером строки, служба RPC может специально выделить память, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="70b78-139">If the client application component should not control the size of the string, the RPC service can specifically allocate the memory as demonstrated in the following example:</span></span>

    ``` syntax
    outStringUnknownSize
    (
    [out] LPWSTR *ppStr
    );
    ```

    <span data-ttu-id="70b78-140">При вызове метода RPC компонент клиентского приложения должен задать для *Ппстр* **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="70b78-140">The client application component must set *ppStr* to **NULL** on when calling the RPC method.</span></span>

 

 




