---
title: атрибут byte_count
description: Атрибут \ Byte \_ Count \ ACF является атрибутом параметра, который связывает размер в байтах с областью памяти, обозначенной указателем.
ms.assetid: 7e146888-fe7c-461c-8615-70da1e3b12cd
keywords:
- byte_count атрибута MIDL
topic_type:
- apiref
api_name:
- byte_count
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d82d34a60ea736d10c8ec5ee8a001370c6b64c6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334427"
---
# <a name="byte_count-attribute"></a><span data-ttu-id="9abc8-104">\_атрибут числа байтов</span><span class="sxs-lookup"><span data-stu-id="9abc8-104">byte\_count attribute</span></span>

<span data-ttu-id="9abc8-105">Атрибут ACF **\[ \_ Count \] -Byte** — это атрибут параметра, связывающий размер в байтах с областью памяти, обозначенной указателем.</span><span class="sxs-lookup"><span data-stu-id="9abc8-105">The **\[byte\_count\]** ACF attribute is a parameter attribute that associates a size, in bytes, with the memory area indicated by the pointer.</span></span>

``` syntax
[ function-attribute-list ] function-name(
    [byte_count(length-variable-name)] parameter-name);
    ...);
```

## <a name="parameters"></a><span data-ttu-id="9abc8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9abc8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9abc8-107">*Function-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="9abc8-107">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9abc8-108">Указывает ноль или более атрибутов функции ACF.</span><span class="sxs-lookup"><span data-stu-id="9abc8-108">Specifies zero or more ACF function attributes.</span></span>

</dd> <dt>

<span data-ttu-id="9abc8-109">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="9abc8-109">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="9abc8-110">Указывает имя функции, определенной в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="9abc8-110">Specifies the name of the function defined in the IDL file.</span></span> <span data-ttu-id="9abc8-111">Необходимо указать имя функции.</span><span class="sxs-lookup"><span data-stu-id="9abc8-111">The function name is required.</span></span>

</dd> <dt>

<span data-ttu-id="9abc8-112">*Length-переменная-имя*</span><span class="sxs-lookup"><span data-stu-id="9abc8-112">*length-variable-name*</span></span> 
</dt> <dd>

<span data-ttu-id="9abc8-113">Задает имя [**\[ \]**](in.md)одноименного параметра, указывающего размер (в байтах) области памяти, на которую ссылается *параметр parameter-name*.</span><span class="sxs-lookup"><span data-stu-id="9abc8-113">Specifies the name of the [**\[in\]**](in.md)-only parameter that specifies the size, in bytes, of the memory area referenced by *parameter-name*.</span></span>

</dd> <dt>

<span data-ttu-id="9abc8-114">*имя параметра*</span><span class="sxs-lookup"><span data-stu-id="9abc8-114">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="9abc8-115">Задает имя параметра указателя, [**\[ который \] является единственным, определенным в IDL-файле**](out-idl.md).</span><span class="sxs-lookup"><span data-stu-id="9abc8-115">Specifies the name of the [**\[out\]**](out-idl.md)-only pointer parameter defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9abc8-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9abc8-116">Remarks</span></span>

<span data-ttu-id="9abc8-117">**\[ \_ Счетчик \] байтов** атрибута ACF представляет расширение Майкрософт для устройства DCE IDL.</span><span class="sxs-lookup"><span data-stu-id="9abc8-117">The ACF attribute **\[byte\_count\]** represents a Microsoft extension to DCE IDL.</span></span> <span data-ttu-id="9abc8-118">Поэтому этот атрибут недоступен при использовании параметра компилятора MIDL [**/ОСФ**](-osf.md).</span><span class="sxs-lookup"><span data-stu-id="9abc8-118">Therefore, this attribute is not available when you use the MIDL compiler switch [**/osf**](-osf.md).</span></span>

> [!Note]  
> <span data-ttu-id="9abc8-119">Атрибут **\[ количества \] байтов** больше не поддерживается в синтаксисе NDR64 из-за трудностей при оценке размера, необходимого для всех параметров [**\[ out \]**](out-idl.md) .</span><span class="sxs-lookup"><span data-stu-id="9abc8-119">The **\[byte count\]** attribute is no longer supported in NDR64 syntax due to the difficulty in estimating the size required for all [**\[out\]**](out-idl.md) parameters.</span></span>

 

<span data-ttu-id="9abc8-120">Память, на которую ссылается параметр указателя, является непрерывной и не выделяется или освобождается заглушками клиента.</span><span class="sxs-lookup"><span data-stu-id="9abc8-120">Memory referenced by the pointer parameter is contiguous and is not allocated or freed by the client stubs.</span></span> <span data-ttu-id="9abc8-121">Эта функция атрибута **\[ \_ счетчика \] байтов** позволяет создать в памяти клиента область постоянного буфера, которую можно повторно использовать в нескольких вызовах удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="9abc8-121">This feature of the **\[byte\_count\]** attribute lets you create a persistent buffer area in client memory that can be reused during more than one call to the remote procedure.</span></span>

<span data-ttu-id="9abc8-122">Возможность отключения выделения памяти заглушки клиента позволяет настроить приложение для повышения эффективности.</span><span class="sxs-lookup"><span data-stu-id="9abc8-122">The ability to turn off the client stub memory allocation lets you tune the application for efficiency.</span></span> <span data-ttu-id="9abc8-123">Например, атрибут **\[ \_ количества \] байтов** может использоваться функциями поставщиков служб, которые используют Microsoft RPC.</span><span class="sxs-lookup"><span data-stu-id="9abc8-123">For example, the **\[byte\_count\]** attribute can be used by service-provider functions that use Microsoft RPC.</span></span> <span data-ttu-id="9abc8-124">Когда пользовательское приложение вызывает API поставщика услуг и отправляет указатель на буфер, поставщик услуг может передать указатель буфера на удаленную функцию.</span><span class="sxs-lookup"><span data-stu-id="9abc8-124">When a user application calls the service-provider API and sends a pointer to a buffer, the service provider can pass the buffer pointer on to the remote function.</span></span> <span data-ttu-id="9abc8-125">Поставщик услуг может повторно использовать буфер во время нескольких удаленных вызовов, не вынуждая пользователя перераспределять область памяти.</span><span class="sxs-lookup"><span data-stu-id="9abc8-125">The service provider can reuse the buffer during multiple remote calls without forcing the user to reallocate the memory area.</span></span>

<span data-ttu-id="9abc8-126">Область памяти может содержать сложные структуры данных, состоящие из нескольких указателей.</span><span class="sxs-lookup"><span data-stu-id="9abc8-126">The memory area can contain complex data structures that consist of multiple pointers.</span></span> <span data-ttu-id="9abc8-127">Поскольку область памяти является непрерывной, приложению не нужно выполнять несколько вызовов для индивидуального освобождения каждого указателя и структуры.</span><span class="sxs-lookup"><span data-stu-id="9abc8-127">Because the memory area is contiguous, the application does not have to make several calls to individually free each pointer and structure.</span></span> <span data-ttu-id="9abc8-128">Вместо этого он может выделить или освободить область памяти с помощью одного вызова функции выделения памяти или бесплатной подпрограммы.</span><span class="sxs-lookup"><span data-stu-id="9abc8-128">Instead, it can allocate or free the memory area with one call to the memory allocation or free routine.</span></span>

<span data-ttu-id="9abc8-129">Буфер должен быть [**\[ выходным \]**](out-idl.md)параметром, а длина буфера в байтах должна быть параметром только [**\[ в \]**](in.md)режиме.</span><span class="sxs-lookup"><span data-stu-id="9abc8-129">The buffer must be an [**\[out\]**](out-idl.md)-only parameter, while the buffer length in bytes must be an [**\[in\]**](in.md)-only parameter.</span></span>

<span data-ttu-id="9abc8-130">Укажите буфер, достаточно большой для размещения всех параметров [**\[ out \]**](out-idl.md) .</span><span class="sxs-lookup"><span data-stu-id="9abc8-130">Specify a buffer that is large enough to contain all the [**\[out\]**](out-idl.md) parameters.</span></span> <span data-ttu-id="9abc8-131">Из-за скрытого заполнения используйте переоценки, а не точные значения счетчиков.</span><span class="sxs-lookup"><span data-stu-id="9abc8-131">Because of hidden padding, use overestimates rather than exact counts.</span></span> <span data-ttu-id="9abc8-132">Например, 4-байтовые указатели расмаршалируются на границе с четырьмя байтами на 32-разрядных платформах и 8-байтовых указателях на 8-байтовой границе на 64-разрядных платформах.</span><span class="sxs-lookup"><span data-stu-id="9abc8-132">For example, 4-byte pointers are unmarshaled on a 4-byte aligned boundary on 32-bit platforms and 8-byte pointers on an 8-byte boundary on 64-bit platforms.</span></span> <span data-ttu-id="9abc8-133">Таким образом, выравнивание, которое будет выполняться суррогатными заглушками, должно быть учетом в пространстве для буфера.</span><span class="sxs-lookup"><span data-stu-id="9abc8-133">Therefore, the alignment padding the stubs will perform must be accounted for in the space for the buffer.</span></span> <span data-ttu-id="9abc8-134">Кроме того, уровни упаковки, используемые при компиляции на языке C, могут различаться.</span><span class="sxs-lookup"><span data-stu-id="9abc8-134">In addition, packing levels used during C-language compilation can vary.</span></span> <span data-ttu-id="9abc8-135">Используйте значение счетчика байтов, которое учитывает дополнительные байты упаковки, добавленные для уровня упаковки, используемого при компиляции на языке C.</span><span class="sxs-lookup"><span data-stu-id="9abc8-135">Use a byte count value that accounts for additional packing bytes added for the packing level used during C-language compilation.</span></span> <span data-ttu-id="9abc8-136">Надежная практика, охватывающая как 32-разрядные, так и 64 разрядные платформы, предполагает, что каждый объект, поступающий в блок большой памяти, начинается с адреса, кратного 8.</span><span class="sxs-lookup"><span data-stu-id="9abc8-136">A safe practice that covers both 32 bit platforms and 64 bit platforms is to assume that each object going into the big memory block starts at an address that is a multiple of 8.</span></span>

## <a name="examples"></a><span data-ttu-id="9abc8-137">Примеры</span><span class="sxs-lookup"><span data-stu-id="9abc8-137">Examples</span></span>

``` syntax
/* IDL file */ 
HRESULT proc1([in] unsigned long length, 
              [out] struct my_struct * pMyStruct); 
 
/* ACF file */ 
proc1([byte_count(length)] pMyStruct);
```

## <a name="see-also"></a><span data-ttu-id="9abc8-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9abc8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9abc8-139">Файл конфигурации приложения (ACF)</span><span class="sxs-lookup"><span data-stu-id="9abc8-139">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="9abc8-140">**окне**</span><span class="sxs-lookup"><span data-stu-id="9abc8-140">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="9abc8-141">**Длина \_ равна**</span><span class="sxs-lookup"><span data-stu-id="9abc8-141">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="9abc8-142">**/осф**</span><span class="sxs-lookup"><span data-stu-id="9abc8-142">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="9abc8-143">**заполняет**</span><span class="sxs-lookup"><span data-stu-id="9abc8-143">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="9abc8-144">**размер \_ равен**</span><span class="sxs-lookup"><span data-stu-id="9abc8-144">**size\_is**</span></span>](size-is.md)
</dt> </dl>

 

 




