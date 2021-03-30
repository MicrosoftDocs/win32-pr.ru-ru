---
title: атрибут Broadcast
description: Ключевое слово \ Broadcast \ указывает, что удаленные вызовы процедур должны отправляться на все серверы в локальной сети.
ms.assetid: 3951c80f-b7f1-457b-9eee-6e075291b27e
keywords:
- Широковещательный атрибут MIDL
topic_type:
- apiref
api_name:
- broadcast
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c2bbb724fc292a5e3942bf2b6de61b5631cdc0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334432"
---
# <a name="broadcast-attribute"></a><span data-ttu-id="26192-104">атрибут Broadcast</span><span class="sxs-lookup"><span data-stu-id="26192-104">broadcast attribute</span></span>

<span data-ttu-id="26192-105">Ключевое слово **\[ Broadcast \]** указывает, что удаленные вызовы процедур должны отправляться на все серверы в локальной сети.</span><span class="sxs-lookup"><span data-stu-id="26192-105">The keyword **\[broadcast\]** specifies that remote procedure calls be sent to all servers on a local network.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [broadcast [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="26192-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="26192-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26192-107">*Interface-список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="26192-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="26192-108">Задает список из нуля или нескольких атрибутов IDL, которые применяются к интерфейсу в целом.</span><span class="sxs-lookup"><span data-stu-id="26192-108">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="26192-109">При наличии двух или более атрибутов интерфейса они должны быть разделены запятыми.</span><span class="sxs-lookup"><span data-stu-id="26192-109">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="26192-110">*имя интерфейса*</span><span class="sxs-lookup"><span data-stu-id="26192-110">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="26192-111">Указывает имя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="26192-111">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="26192-112">*Список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="26192-112">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="26192-113">Задает дополнительные атрибуты, которые будут применены к функции.</span><span class="sxs-lookup"><span data-stu-id="26192-113">Specifies additional attributes to be applied to the function.</span></span> <span data-ttu-id="26192-114">Несколько атрибутов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="26192-114">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="26192-115">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="26192-115">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="26192-116">Указывает тип возвращаемого значения функции.</span><span class="sxs-lookup"><span data-stu-id="26192-116">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="26192-117">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="26192-117">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="26192-118">Указывает имя функции, к которой будет применен атрибут **\[ Broadcast \]** .</span><span class="sxs-lookup"><span data-stu-id="26192-118">Specifies the name of the function to which the **\[broadcast\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="26192-119">*params*</span><span class="sxs-lookup"><span data-stu-id="26192-119">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="26192-120">Список параметров функции.</span><span class="sxs-lookup"><span data-stu-id="26192-120">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="26192-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="26192-121">Remarks</span></span>

<span data-ttu-id="26192-122">Ключевое слово **\[ Broadcast \]** указывает, что подпрограммы всегда рассылаются на все серверы в сети, а не доставляются на один конкретный сервер. Клиент получает выходные данные первого ответа для успешного возврата, а последующие ответы отбрасываются.</span><span class="sxs-lookup"><span data-stu-id="26192-122">The **\[broadcast\]** keyword specifies that the routine is always broadcasted to all the servers on the network, rather than being delivered to one particular server.The client receives output from the first reply to return successfully, while subsequent replies are discarded.</span></span>

<span data-ttu-id="26192-123">Операция с атрибутом **\[ Broadcast \]** неявно является операцией [**\[ идемпотентными \]**](idempotent.md) .</span><span class="sxs-lookup"><span data-stu-id="26192-123">An operation with the **\[broadcast\]** attribute is implicitly an [**\[idempotent\]**](idempotent.md) operation.</span></span> <span data-ttu-id="26192-124">Однако атрибут **\[ Broadcast \]** указывает дополнительные свойства, которые не имеют атрибута **\[ идемпотентными \]** .</span><span class="sxs-lookup"><span data-stu-id="26192-124">However, the **\[broadcast\]** attribute specifies additional properties that functions with the **\[idempotent\]** attribute don't have.</span></span> <span data-ttu-id="26192-125">В частности, функции, использующие атрибут **\[ Broadcast \]** , указывают, что процедуру можно вызывать несколько раз в результате одного вызова удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="26192-125">Specifically, functions using the **\[broadcast\]** attribute specify that the routine can be called multiple times as the result of one remote procedure call.</span></span> <span data-ttu-id="26192-126">В то же время их можно отправить на несколько серверов.</span><span class="sxs-lookup"><span data-stu-id="26192-126">At the same time, they can be sent to multiple servers.</span></span> <span data-ttu-id="26192-127">Это отличается от атрибута **\[ идемпотентными \]** , который указывает, что только вызов может быть повторен, если он не завершен.</span><span class="sxs-lookup"><span data-stu-id="26192-127">This is different from the **\[idempotent\]** attribute, which specifies only that a call can be retried if it is not completed.</span></span>

<span data-ttu-id="26192-128">Если удаленная процедура передает свой вызов всем узлам в локальной сети, он должен использовать последовательность протокола [**нкадг \_ IP \_ UDP**](ncadg-ip-udp.md) или [**нкадг \_ IPX**](ncadg-ipx.md) .</span><span class="sxs-lookup"><span data-stu-id="26192-128">If a remote procedure broadcasts its call to all hosts on a local network, it must use either the [**ncadg\_ip\_udp**](ncadg-ip-udp.md) or the [**ncadg\_ipx**](ncadg-ipx.md) protocol sequence.</span></span> <span data-ttu-id="26192-129">Обратите внимание, что размер **\[ широковещательного \]** пакета определяется используемой службой датаграмм.</span><span class="sxs-lookup"><span data-stu-id="26192-129">Note that the size of a **\[broadcast\]** packet is determined by the datagram service in use.</span></span>

## <a name="see-also"></a><span data-ttu-id="26192-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26192-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26192-131">**idempotent**</span><span class="sxs-lookup"><span data-stu-id="26192-131">**idempotent**</span></span>](idempotent.md)
</dt> <dt>

[<span data-ttu-id="26192-132">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="26192-132">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="26192-133">**Ну**</span><span class="sxs-lookup"><span data-stu-id="26192-133">**maybe**</span></span>](maybe.md)
</dt> <dt>

[<span data-ttu-id="26192-134">**нкадг \_ IP \_ UDP**</span><span class="sxs-lookup"><span data-stu-id="26192-134">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="26192-135">**нкадг \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="26192-135">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> </dl>

 

 




