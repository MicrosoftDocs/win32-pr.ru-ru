---
title: /robust, параметр
description: Параметр/robust указывает компилятору MIDL создавать дополнительные сведения для проверки ошибок, которые подсистема NDR использует для выполнения проверок целостности во время выполнения.
ms.assetid: 7a858600-ea06-4396-9a1b-240d646e8c7d
keywords:
- MIDL/robust Switch
topic_type:
- apiref
api_name:
- /robust
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 974f9530006c03a041d9d444c41f9c5ca01569c0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103889475"
---
# <a name="robust-switch"></a><span data-ttu-id="f6e42-104">/robust, параметр</span><span class="sxs-lookup"><span data-stu-id="f6e42-104">/robust switch</span></span>

<span data-ttu-id="f6e42-105">Параметр **/robust** указывает компилятору MIDL создавать дополнительные сведения для проверки ошибок, которые подсистема NDR использует для выполнения проверок целостности во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="f6e42-105">The **/robust** switch tells the MIDL compiler to generate additional error-checking information, which the NDR engine uses to perform integrity checks at run time.</span></span>

``` syntax
midl /robust {/Oicf | /Oif }
```

## <a name="switch-options"></a><span data-ttu-id="f6e42-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="f6e42-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="f6e42-107">*/Oicf*</span><span class="sxs-lookup"><span data-stu-id="f6e42-107">*/Oicf*</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="f6e42-108">*/OIF*</span><span class="sxs-lookup"><span data-stu-id="f6e42-108">*/Oif*</span></span> 
</dt> <dd>

<span data-ttu-id="f6e42-109">Эти параметры идентичны их функциональным возможностям.</span><span class="sxs-lookup"><span data-stu-id="f6e42-109">These switches are identical in their functionality.</span></span> <span data-ttu-id="f6e42-110">Они указывают прокси-метод для упаковки и использования строк быстрого формата для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="f6e42-110">They specify the codeless proxy method of marshaling and use fast format strings for improved performance.</span></span> <span data-ttu-id="f6e42-111">См. раздел/ [**Oi**](-oi.md).</span><span class="sxs-lookup"><span data-stu-id="f6e42-111">See / [**Oi**](-oi.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f6e42-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f6e42-112">Remarks</span></span>

<span data-ttu-id="f6e42-113">С помощью параметра **/robust** создаются дополнительные сведения, позволяющие подсистеме представления данных сети выполнять проверку ошибок во время выполнения для коррелированных аргументов в динамических массивах, объединениях и в указателях [**интерфейса в**](out-idl.md) приложениях DCOM.</span><span class="sxs-lookup"><span data-stu-id="f6e42-113">Using the **/robust** switch generates additional information that allows the Network Data Representation (NDR) engine to perform run-time error checking on correlated arguments in dynamic arrays, unions, and in [**out**](out-idl.md) interface pointers in DCOM applications.</span></span> <span data-ttu-id="f6e42-114">Параметр **/robust** доступен только в Windows 2000 и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="f6e42-114">The **/robust** switch is only available under WindowsÂ 2000 and later versions of Windows.</span></span>

<span data-ttu-id="f6e42-115">Коррелированный аргумент — это аргумент, который использует любой из атрибутов, позволяющих определять размер объекта данных во время выполнения: [**size \_ —**](size-is.md), [**length \_ —**](length-is.md), [**First \_ —**](first-is.md), [**Last \_ —**](last-is.md), [**Max \_ —**](max-is.md), [**Switch \_ имеет**](switch-is.md)значение, а [**IID \_ —**](iid-is.md).</span><span class="sxs-lookup"><span data-stu-id="f6e42-115">A correlated argument is an argument that uses any of the attributes that allow the size of a data object to be determined at run time: [**size\_is**](size-is.md), [**length\_is**](length-is.md), [**first\_is**](first-is.md), [**last\_is**](last-is.md), [**max\_is**](max-is.md), [**switch\_is**](switch-is.md), and [**iid\_is**](iid-is.md).</span></span> <span data-ttu-id="f6e42-116">В соответствии со спецификацией использование-DCE для телепередачи этот коррелированный аргумент появляется в двух разных местах.</span><span class="sxs-lookup"><span data-stu-id="f6e42-116">In accordance with the OSF-DCE specification for the wire representation, this correlated argument appears in two different places.</span></span> <span data-ttu-id="f6e42-117">Например, рассмотрим типичное использование **размера \_ —** атрибут:</span><span class="sxs-lookup"><span data-stu-id="f6e42-117">For example, consider a typical usage of the **size\_is** attribute:</span></span>

``` syntax
HRESULT Func1([in] long Size, 
              [in, size_is(Size)]BAR_TYPE *pBarType);
```

<span data-ttu-id="f6e42-118">В этом примере клиент передает значение Long, указывающее размер блока ЛИНЕЙЧАТых \_ типов (с точки зрения количества элементов линейчатых \_ типов), и указатель на фактический блок типов линейчатых диаграмм \_ .</span><span class="sxs-lookup"><span data-stu-id="f6e42-118">In this example, the client passes a long that specifies the size of a block of BAR\_TYPEs (in terms of number of BAR\_TYPES elements), and a pointer to the actual block of BAR\_TYPEs.</span></span> <span data-ttu-id="f6e42-119">Аргумент size сопоставляется с аргументом Пбартипе.</span><span class="sxs-lookup"><span data-stu-id="f6e42-119">The Size argument correlates with the pBarType argument.</span></span> <span data-ttu-id="f6e42-120">В соответствии со спецификацией использование-DCE аргумент size представляется в сети дважды — сначала, а затем с массивом \_ элементов типа Bar, представляющих аргумент пбартипе.</span><span class="sxs-lookup"><span data-stu-id="f6e42-120">In accordance with the OSF-DCE specification, the Size argument is represented twice on the wire—first as itself and then with the array of BAR\_TYPE elements that represent the pBarType argument.</span></span> <span data-ttu-id="f6e42-121">Каждый аргумент упаковывается независимо друг от друга в соответствии с собственным представлением передачи.</span><span class="sxs-lookup"><span data-stu-id="f6e42-121">Each argument is unmarshaled independently, according to its own wire representation.</span></span> <span data-ttu-id="f6e42-122">Как правило, аргумент size и его копия, используемые для представления части другого аргумента, имеют одинаковые значения.</span><span class="sxs-lookup"><span data-stu-id="f6e42-122">Normally, the Size argument and its copy, which is used to represent part of the other argument, have the same values.</span></span> <span data-ttu-id="f6e42-123">Однако, если аргумент size становится поврежденным (например, если блок ЛИНЕЙЧАТых типов больше \_ , чем выделенный), серверное приложение может перестать отвечать на запросы, так как в нем используется значение аргумента size для измерения входящих данных.</span><span class="sxs-lookup"><span data-stu-id="f6e42-123">However, if the Size argument becomes corrupted (for example, when the block of BAR\_TYPES is larger than what was allocated), the server application may stop responding, because it uses the value of the Size argument to measure incoming data.</span></span>

<span data-ttu-id="f6e42-124">Для реализации допустимой проверки диапазона с помощью атрибута [**Range**](range.md) требуется параметр **/robust** .</span><span class="sxs-lookup"><span data-stu-id="f6e42-124">The **/robust** switch is required to implement valid range checking with the [**range**](range.md) attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="f6e42-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="f6e42-125">Examples</span></span>

<span data-ttu-id="f6e42-126">**MIDL/robust/Oicf filename. idl**</span><span class="sxs-lookup"><span data-stu-id="f6e42-126">**midl /robust /Oicf filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="f6e42-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6e42-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6e42-128">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="f6e42-128">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="f6e42-129">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="f6e42-129">**/Oi**</span></span>](-oi.md)
</dt> <dt>

[<span data-ttu-id="f6e42-130">**разнообраз**</span><span class="sxs-lookup"><span data-stu-id="f6e42-130">**range**</span></span>](range.md)
</dt> </dl>

 

 




