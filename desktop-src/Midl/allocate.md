---
title: выделить атрибут
description: Атрибут \ allocate \ ACF позволяет настраивать выделение и освобождение памяти для типа, определенного в IDL-файле.
ms.assetid: 1956b11f-bafa-41c3-9025-5fcbb890d1a2
keywords:
- выделить атрибут MIDL
topic_type:
- apiref
api_name:
- allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff902e34e07ebd34edcb73797baa131eec8b222
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103889507"
---
# <a name="allocate-attribute"></a><span data-ttu-id="d85fc-104">выделить атрибут</span><span class="sxs-lookup"><span data-stu-id="d85fc-104">allocate attribute</span></span>

<span data-ttu-id="d85fc-105">Атрибут **\[ allocate \]** ACF позволяет настраивать выделение и освобождение памяти для типа, определенного в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="d85fc-105">The **\[allocate\]** ACF attribute lets you customize memory allocation and deallocation for a type defined in the IDL file.</span></span>

``` syntax
typedef [allocate (allocate-option-list) [, type-attribute-list] ] type-name;
```

## <a name="parameters"></a><span data-ttu-id="d85fc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d85fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d85fc-107">*список выделения и параметров*</span><span class="sxs-lookup"><span data-stu-id="d85fc-107">*allocate-option-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d85fc-108">Указывает один или несколько параметров выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="d85fc-108">Specifies one or more memory-allocation options.</span></span> <span data-ttu-id="d85fc-109">Выберите **один или несколько узлов \_** либо один из них либо **бесплатный** или **не \_ бесплатный**, либо один из этих пар. **\_**</span><span class="sxs-lookup"><span data-stu-id="d85fc-109">Select one of either **single\_node** or **all\_nodes**, or one of either **free** or **dont\_free**, or one from each pair.</span></span> <span data-ttu-id="d85fc-110">При указании более одного параметра разделяйте параметры запятыми.</span><span class="sxs-lookup"><span data-stu-id="d85fc-110">When you specify more than one option, separate the options with commas.</span></span>

</dd> <dt>

<span data-ttu-id="d85fc-111">*Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="d85fc-111">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d85fc-112">Указывает другие необязательные атрибуты типа ACF.</span><span class="sxs-lookup"><span data-stu-id="d85fc-112">Specifies other optional ACF-type attributes.</span></span> <span data-ttu-id="d85fc-113">При указании более одного атрибута типа разделяйте параметры запятыми.</span><span class="sxs-lookup"><span data-stu-id="d85fc-113">When you specify more than one type attribute, separate the options with commas.</span></span>

</dd> <dt>

<span data-ttu-id="d85fc-114">*имя типа*</span><span class="sxs-lookup"><span data-stu-id="d85fc-114">*type-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d85fc-115">Указывает тип, определенный в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="d85fc-115">Specifies a type defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d85fc-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d85fc-116">Remarks</span></span>

<span data-ttu-id="d85fc-117">Атрибут **\[ выделения \]** имеет следующие допустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="d85fc-117">The **\[allocate\]** attribute has the following valid options.</span></span>



| <span data-ttu-id="d85fc-118">Параметр</span><span class="sxs-lookup"><span data-stu-id="d85fc-118">Option</span></span>           | <span data-ttu-id="d85fc-119">Описание</span><span class="sxs-lookup"><span data-stu-id="d85fc-119">Description</span></span>                                                           |
|------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="d85fc-120">**все \_ узлы**</span><span class="sxs-lookup"><span data-stu-id="d85fc-120">**all\_nodes**</span></span>   | <span data-ttu-id="d85fc-121">Выполняет один вызов для выделения и освобождения памяти для всех узлов.</span><span class="sxs-lookup"><span data-stu-id="d85fc-121">Makes one call to allocate and free memory for all nodes.</span></span>             |
| <span data-ttu-id="d85fc-122">**один \_ узел**</span><span class="sxs-lookup"><span data-stu-id="d85fc-122">**single\_node**</span></span> | <span data-ttu-id="d85fc-123">Делает множество отдельных вызовов для выделения и освобождения каждого узла памяти.</span><span class="sxs-lookup"><span data-stu-id="d85fc-123">Makes many individual calls to allocate and free each node of memory.</span></span> |
| <span data-ttu-id="d85fc-124">**free**</span><span class="sxs-lookup"><span data-stu-id="d85fc-124">**free**</span></span>         | <span data-ttu-id="d85fc-125">Освобождает память при возврате из заглушки сервера.</span><span class="sxs-lookup"><span data-stu-id="d85fc-125">Frees memory on return from the server stub.</span></span>                          |
| <span data-ttu-id="d85fc-126">**не \_ бесплатно**</span><span class="sxs-lookup"><span data-stu-id="d85fc-126">**dont\_free**</span></span>   | <span data-ttu-id="d85fc-127">Не освобождает память при возврате из заглушки сервера.</span><span class="sxs-lookup"><span data-stu-id="d85fc-127">Does not free memory on return from the server stub.</span></span>                  |



 

<span data-ttu-id="d85fc-128">По умолчанию заглушки могут выделять хранилище для данных, на которые ссылается уникальный или полный указатель, путем вызова метода [**\_ пользовательского \_ выделения MIDL**](midl-user-allocate-1.md) и [**\_ \_ бесплатного пользователя MIDL**](midl-user-free-1.md) по отдельности для каждого указателя.</span><span class="sxs-lookup"><span data-stu-id="d85fc-128">By default, the stubs may allocate storage for data referenced by a unique or full pointer by calling [**midl\_user\_allocate**](midl-user-allocate-1.md) and [**midl\_user\_free**](midl-user-free-1.md) individually for each pointer.</span></span>

<span data-ttu-id="d85fc-129">Можно оптимизировать скорость приложения, указав параметр **все \_ узлы**.</span><span class="sxs-lookup"><span data-stu-id="d85fc-129">You can optimize the speed of your application by specifying the option **all\_nodes**.</span></span> <span data-ttu-id="d85fc-130">Этот параметр указывает заглушке вычислить размер всей памяти, на которую ссылается указатель указанного типа, и выполнить один вызов для [**\_ \_ выделения пользователю MIDL**](midl-user-allocate-1.md).</span><span class="sxs-lookup"><span data-stu-id="d85fc-130">This option directs the stub to compute the size of all memory referenced through the pointer of the specified type and to make a single call to [**midl\_user\_allocate**](midl-user-allocate-1.md).</span></span> <span data-ttu-id="d85fc-131">Заглушка освобождает память, делая один вызов для [**пользователя MIDL \_ \_ свободным**](midl-user-free-1.md).</span><span class="sxs-lookup"><span data-stu-id="d85fc-131">The stub releases the memory by making one call to [**midl\_user\_free**](midl-user-free-1.md).</span></span>

<span data-ttu-id="d85fc-132">Параметр **без \_** поддержки направляет компилятор MIDL для создания заглушки сервера, которая не вызывает для указанного типа [**функцию \_ MIDL \_ без вызова пользователя**](midl-user-free-1.md) .</span><span class="sxs-lookup"><span data-stu-id="d85fc-132">The **dont\_free** option directs the MIDL compiler to generate a server stub that does not call [**midl\_user\_free**](midl-user-free-1.md) for the specified type.</span></span> <span data-ttu-id="d85fc-133">Параметр **не \_ свободен** позволяет структурам указателей оставаться доступными для серверного приложения после завершения удаленного вызова процедуры и возврата клиенту.</span><span class="sxs-lookup"><span data-stu-id="d85fc-133">The **dont\_free** option allows the pointer structures to remain accessible to the server application after the remote procedure call has completed and returned to the client.</span></span>

<span data-ttu-id="d85fc-134">Атрибут **\[ выделения \]** приведет к тому, что любой **\[ выходной \]** параметр, который является указателем на тип, квалифицированный с параметром **все \_ узлы** , перераспределяет память при распаковке данных.</span><span class="sxs-lookup"><span data-stu-id="d85fc-134">The **\[allocate\]** attribute will cause any **\[in, out\]** parameter that is a pointer to a type qualified with the **all\_nodes** option to reallocate memory when the data is unmarshaled.</span></span> <span data-ttu-id="d85fc-135">Это приложение отвечает за освобождение памяти, выделенной ранее для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="d85fc-135">It is the responsibility of the application to free the memory allocated previously for this parameter.</span></span> <span data-ttu-id="d85fc-136">Пример:</span><span class="sxs-lookup"><span data-stu-id="d85fc-136">For example:</span></span>

``` syntax
typedef struct thistype 
{ 
    [string] char * PTHISTYPE;  
} * PTHISTYPE
HRESULT proc1 ( [in,out] PTHISTYPE * ppthistype);
```

<span data-ttu-id="d85fc-137">Тип данных ПСИСТИПЕ будет повторно выделен в [**\[ обратном \]**](out-idl.md) направлении заглушкой перед распаковкой.</span><span class="sxs-lookup"><span data-stu-id="d85fc-137">The data type PTHISTYPE will be reallocated in the [**\[out\]**](out-idl.md) direction by the stub before unmarshaling.</span></span> <span data-ttu-id="d85fc-138">Поэтому приложение должно освободить память, выделенную ранее для данных этого параметра, или произойдет утечка памяти.</span><span class="sxs-lookup"><span data-stu-id="d85fc-138">Therefore, the application must free the memory it previously allocated for this parameter's data, or a memory leak will occur.</span></span>

## <a name="examples"></a><span data-ttu-id="d85fc-139">Примеры</span><span class="sxs-lookup"><span data-stu-id="d85fc-139">Examples</span></span>

``` syntax
/* ACF file */ 
typedef [allocate(all_nodes, dont_free)] PTYPE1; 
typedef [allocate(all_nodes)] PTYPE2; 
typedef [allocate(dont_free)] PTYPE3;
```

## <a name="see-also"></a><span data-ttu-id="d85fc-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d85fc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d85fc-141">Файл конфигурации приложения (ACF)</span><span class="sxs-lookup"><span data-stu-id="d85fc-141">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="d85fc-142">**окне**</span><span class="sxs-lookup"><span data-stu-id="d85fc-142">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="d85fc-143">**\_пользовательское \_ выделение MIDL**</span><span class="sxs-lookup"><span data-stu-id="d85fc-143">**midl\_user\_allocate**</span></span>](midl-user-allocate-1.md)
</dt> <dt>

[<span data-ttu-id="d85fc-144">**\_бесплатный пользователь \_ MIDL**</span><span class="sxs-lookup"><span data-stu-id="d85fc-144">**midl\_user\_free**</span></span>](midl-user-free-1.md)
</dt> <dt>

[<span data-ttu-id="d85fc-145">**заполняет**</span><span class="sxs-lookup"><span data-stu-id="d85fc-145">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="d85fc-146">**определение**</span><span class="sxs-lookup"><span data-stu-id="d85fc-146">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




