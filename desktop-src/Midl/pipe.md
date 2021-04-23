---
title: атрибут pipe
description: Конструктор типа канала позволяет передавать открытый поток типизированных данных через удаленный вызов процедуры.
ms.assetid: 85b76a55-8df2-4417-9a39-3e3bf49651fc
keywords:
- атрибут канала MIDL
topic_type:
- apiref
api_name:
- pipe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0aaab8d399c99e02b5393ee9f5258da53aea491
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336977"
---
# <a name="pipe-attribute"></a><span data-ttu-id="aa108-104">атрибут pipe</span><span class="sxs-lookup"><span data-stu-id="aa108-104">pipe attribute</span></span>

<span data-ttu-id="aa108-105">Конструктор типа **канала** позволяет передавать открытый поток типизированных данных через удаленный вызов процедуры.</span><span class="sxs-lookup"><span data-stu-id="aa108-105">The **pipe** type constructor makes it possible to transmit an open-ended stream of typed data across a remote procedure call.</span></span>

``` syntax
typedef pipe element-type pipe-declarator;
```

## <a name="parameters"></a><span data-ttu-id="aa108-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="aa108-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa108-107">*Element-Type*</span><span class="sxs-lookup"><span data-stu-id="aa108-107">*element-type*</span></span> 
</dt> <dd>

<span data-ttu-id="aa108-108">Определяет размер одного элемента в буфере перемещения.</span><span class="sxs-lookup"><span data-stu-id="aa108-108">Defines the size of a single element in the transfer buffer.</span></span> <span data-ttu-id="aa108-109">*Тип элемента* может быть [базовым типом](midl-base-types.md), предопределенным \_ типом, [**структурой**](struct.md), [**перечислением 32B**](v1-enum.md)или идентификатором типа.</span><span class="sxs-lookup"><span data-stu-id="aa108-109">The *element-type* can be a [base type](midl-base-types.md), predefined\_type, [**struct**](struct.md), [**32b enum**](v1-enum.md), or type identifier.</span></span> <span data-ttu-id="aa108-110">К *\_ типам элементов* применяются некоторые ограничения, как описано в разделе примечания ниже.</span><span class="sxs-lookup"><span data-stu-id="aa108-110">Several restrictions apply to *element\_types*, as described in Remarks, below.</span></span>

</dd> <dt>

<span data-ttu-id="aa108-111">*декларатор канала*</span><span class="sxs-lookup"><span data-stu-id="aa108-111">*pipe-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="aa108-112">Указывает один или несколько идентификаторов или указателей на идентификаторы.</span><span class="sxs-lookup"><span data-stu-id="aa108-112">Specifies one or more identifiers or pointers to identifiers.</span></span> <span data-ttu-id="aa108-113">Несколько деклараторов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="aa108-113">Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa108-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aa108-114">Remarks</span></span>

<span data-ttu-id="aa108-115">Для передачи данных в обоих направлениях можно использовать конструктор типа **канала** .</span><span class="sxs-lookup"><span data-stu-id="aa108-115">You can use the **pipe** type constructor to transmit data in both directions.</span></span> <span data-ttu-id="aa108-116">Параметр **\[** [**in**](in.md) **\]** pipe позволяет серверу получать поток данных от клиента во время удаленного вызова процедуры.</span><span class="sxs-lookup"><span data-stu-id="aa108-116">An **\[**[**in**](in.md)**\]** pipe parameter allows the server to pull the data stream from the client during a remote procedure call.</span></span> <span data-ttu-id="aa108-117">Параметр **\[** [**out**](out-idl.md) **\]** pipe позволяет серверу передать поток данных обратно клиенту.</span><span class="sxs-lookup"><span data-stu-id="aa108-117">An **\[**[**out**](out-idl.md)**\]** pipe parameter allows the server to push the data stream back to the client.</span></span> <span data-ttu-id="aa108-118">Вы предоставляете клиентские подпрограммы для отправки и извлечения потока данных, а также для выделения глобального буфера данных.</span><span class="sxs-lookup"><span data-stu-id="aa108-118">You supply the client-side routines to push and pull the data stream and to allocate a global buffer for the data.</span></span> <span data-ttu-id="aa108-119">Клиентские и серверные программы-заглушки выполняют маршалирование и распаковку данных и передают в приложение ссылку на буфер.</span><span class="sxs-lookup"><span data-stu-id="aa108-119">The client and server stub routines marshal and unmarshal data and pass a reference to the buffer back to the application.</span></span>

<span data-ttu-id="aa108-120">К каналам применяются следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="aa108-120">The following restrictions apply to pipes:</span></span>

-   <span data-ttu-id="aa108-121">Элемент pipe не может быть или содержать указатель, согласованный или переменный массив, маркер или маркер контекста.</span><span class="sxs-lookup"><span data-stu-id="aa108-121">A pipe element cannot be or contain a pointer, a conformant or varying array, a handle, or a context handle.</span></span> <span data-ttu-id="aa108-122">Кроме того, в реализации каналов Майкрософт элемент pipe не может быть или содержать [**объединение**](union.md), [**перечисление 16b**](enum.md)или [**\_ \_ int3264**](--int3264.md).</span><span class="sxs-lookup"><span data-stu-id="aa108-122">Also, in the Microsoft implementation of pipes, a pipe element cannot be or contain a [**union**](union.md), a [**16b enum**](enum.md), or an [**\_\_int3264**](--int3264.md).</span></span>
-   <span data-ttu-id="aa108-123">К **\[** [**\_**](transmit-as.md) **\]** **\[** типу канала или типу элемента нельзя применять атрибуты передачи AS, [**представления \_ как, а также как**](represent-as.md) **\]** **\[** [**\_**](wire-marshal.md) **\]** тип или **\[** [**Пользовательский \_ маршалирование**](user-marshal.md) **\]** . </span><span class="sxs-lookup"><span data-stu-id="aa108-123">You cannot apply the **\[**[**transmit\_as**](transmit-as.md)**\]**, **\[**[**represent\_as**](represent-as.md)**\]**, **\[**[**wire\_marshal**](wire-marshal.md)**\]**, or **\[**[**user\_marshal**](user-marshal.md)**\]** attributes to a pipe type or to the *element-type*.</span></span>
-   <span data-ttu-id="aa108-124">Тип канала не может быть членом структуры или объединения, целью указателя или базового типа массива.</span><span class="sxs-lookup"><span data-stu-id="aa108-124">A pipe type cannot be a member of a structure or union, the target of a pointer, or the base type of an array.</span></span>
-   <span data-ttu-id="aa108-125">Тип данных, объявленный как тип канала, может использоваться только в качестве параметра удаленного вызова.</span><span class="sxs-lookup"><span data-stu-id="aa108-125">A data type declared to be a pipe type can only be used as a parameter of a remote call.</span></span>
-   <span data-ttu-id="aa108-126">Параметр канала можно передать в любом направлении по значению или по ссылке (указатель **\[** [**ref**](ref.md) **\]** ).</span><span class="sxs-lookup"><span data-stu-id="aa108-126">You can pass a pipe parameter in either direction by value or by reference (**\[**[**ref**](ref.md)**\]** pointer).</span></span> <span data-ttu-id="aa108-127">Однако атрибут PTR нельзя применять **\[** [](ptr.md) **\]** к каналу, переданному по ссылке.</span><span class="sxs-lookup"><span data-stu-id="aa108-127">However you cannot apply the **\[**[**ptr**](ptr.md)**\]** attribute to a pipe that is passed by reference.</span></span> <span data-ttu-id="aa108-128">Нельзя указать параметр канала с **\[** [**уникальным**](unique.md) **\]** или полным указателем, независимо от направления.</span><span class="sxs-lookup"><span data-stu-id="aa108-128">You cannot specify a pipe parameter with a **\[**[**unique**](unique.md)**\]** or a full pointer, regardless of direction.</span></span>
-   <span data-ttu-id="aa108-129">Нельзя использовать каналы в **\[** [](object.md) **\]** интерфейсах объектов.</span><span class="sxs-lookup"><span data-stu-id="aa108-129">You cannot use pipes in **\[**[**object**](object.md)**\]** interfaces.</span></span>
-   <span data-ttu-id="aa108-130">Атрибут идемпотентными нельзя применить **\[** [](idempotent.md) **\]** к подподпрограмме, имеющей параметр канала.</span><span class="sxs-lookup"><span data-stu-id="aa108-130">You cannot apply the **\[**[**idempotent**](idempotent.md)**\]** attribute to a routine that has a pipe parameter.</span></span>
-   <span data-ttu-id="aa108-131">Нельзя использовать атрибуты сериализации, а также **\[** [**кодировать**](encode.md) **\]** и **\[** [**декодировать**](decode.md) **\]** с помощью каналов.</span><span class="sxs-lookup"><span data-stu-id="aa108-131">You cannot use the serialization attributes, **\[**[**encode**](encode.md)**\]** and **\[**[**decode**](decode.md)**\]** with pipes.</span></span>
-   <span data-ttu-id="aa108-132">Нельзя использовать автоматические дескрипторы либо по умолчанию, либо с **\[** атрибутом [**Auto \_ Handle**](auto-handle.md) **\]** с каналами.</span><span class="sxs-lookup"><span data-stu-id="aa108-132">You cannot use automatic handles, either by default, or with the **\[**[**auto\_handle**](auto-handle.md)**\]** attribute, with pipes.</span></span>

> [!Note]  
> <span data-ttu-id="aa108-133">Компилятор MIDL поддерживает каналы только в режиме [**/OIF**](-oi.md) .</span><span class="sxs-lookup"><span data-stu-id="aa108-133">The MIDL compiler supports pipes in [**/Oif**](-oi.md) mode only.</span></span>

 

<span data-ttu-id="aa108-134">Дополнительные сведения о реализации подпрограмм с параметрами канала см. в разделе [каналы](/windows/desktop/Rpc/pipes) в руководстве и Справочнике по программированию RPC.</span><span class="sxs-lookup"><span data-stu-id="aa108-134">For more information on implementing routines with pipe parameters, see [Pipes](/windows/desktop/Rpc/pipes) in the RPC Programmer's Guide and Reference.</span></span>

## <a name="examples"></a><span data-ttu-id="aa108-135">Примеры</span><span class="sxs-lookup"><span data-stu-id="aa108-135">Examples</span></span>

``` syntax
typedef pipe unsigned char UCHAR_PIPE1, UCHAR_PIPE2;
 
//SIMPLE_STRUCT defined elsewhere
typedef pipe SIMPLE_STRUCT SIMPLE_STRUCT_PIPE;
```

## <a name="see-also"></a><span data-ttu-id="aa108-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa108-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa108-137">**Автоматическая \_ работа**</span><span class="sxs-lookup"><span data-stu-id="aa108-137">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="aa108-138">Базовые типы MIDL</span><span class="sxs-lookup"><span data-stu-id="aa108-138">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="aa108-139">**декодировать**</span><span class="sxs-lookup"><span data-stu-id="aa108-139">**decode**</span></span>](decode.md)
</dt> <dt>

[<span data-ttu-id="aa108-140">**шифровать**</span><span class="sxs-lookup"><span data-stu-id="aa108-140">**encode**</span></span>](encode.md)
</dt> <dt>

[<span data-ttu-id="aa108-141">**перечисления**</span><span class="sxs-lookup"><span data-stu-id="aa108-141">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="aa108-142">**idempotent**</span><span class="sxs-lookup"><span data-stu-id="aa108-142">**idempotent**</span></span>](idempotent.md)
</dt> <dt>

[<span data-ttu-id="aa108-143">**окне**</span><span class="sxs-lookup"><span data-stu-id="aa108-143">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="aa108-144">**объектами**</span><span class="sxs-lookup"><span data-stu-id="aa108-144">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="aa108-145">**заполняет**</span><span class="sxs-lookup"><span data-stu-id="aa108-145">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="aa108-146">**ptr**</span><span class="sxs-lookup"><span data-stu-id="aa108-146">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="aa108-147">**ref**</span><span class="sxs-lookup"><span data-stu-id="aa108-147">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="aa108-148">**представлять \_ как**</span><span class="sxs-lookup"><span data-stu-id="aa108-148">**represent\_as**</span></span>](represent-as.md)
</dt> <dt>

[<span data-ttu-id="aa108-149">**struct**</span><span class="sxs-lookup"><span data-stu-id="aa108-149">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="aa108-150">**передать \_ как**</span><span class="sxs-lookup"><span data-stu-id="aa108-150">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="aa108-151">**однозначно**</span><span class="sxs-lookup"><span data-stu-id="aa108-151">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="aa108-152">**Пользовательская \_ Упаковка**</span><span class="sxs-lookup"><span data-stu-id="aa108-152">**user\_marshal**</span></span>](user-marshal.md)
</dt> <dt>

[<span data-ttu-id="aa108-153">**проводное \_ маршалирование**</span><span class="sxs-lookup"><span data-stu-id="aa108-153">**wire\_marshal**</span></span>](wire-marshal.md)
</dt> </dl>

 

 