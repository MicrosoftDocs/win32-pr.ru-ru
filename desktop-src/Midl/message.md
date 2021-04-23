---
title: атрибут сообщения
description: Атрибут \ Message \ указывает, что удаленный вызов процедуры должен обрабатываться как сообщение от клиента серверу.
ms.assetid: ec616bf5-a845-4e7e-9f39-20947d2074f7
keywords:
- атрибут сообщения MIDL
topic_type:
- apiref
api_name:
- message
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 964f8dfd8652547bdf5bef25d1abe9acde8189a2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487632"
---
# <a name="message-attribute"></a><span data-ttu-id="43582-104">атрибут сообщения</span><span class="sxs-lookup"><span data-stu-id="43582-104">message attribute</span></span>

<span data-ttu-id="43582-105">Атрибут **\[ Message \]** указывает, что удаленный вызов процедуры должен обрабатываться как сообщение от клиента серверу.</span><span class="sxs-lookup"><span data-stu-id="43582-105">The **\[message\]** attribute indicates that the remote procedure call is to be treated as a message from the client to the server.</span></span>

``` syntax
[message, optional-attribute-list] void function-name(
    [in, optional-parameter-attributes] param-name,. . .);
```

## <a name="parameters"></a><span data-ttu-id="43582-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="43582-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43582-107">*список необязательных атрибутов*</span><span class="sxs-lookup"><span data-stu-id="43582-107">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="43582-108">Другие атрибуты, которые применяются к функции.</span><span class="sxs-lookup"><span data-stu-id="43582-108">Other attributes that apply to the function.</span></span> <span data-ttu-id="43582-109">**\[** [](local.md) **\]** **\[** [](nocode.md) **\]** **\[** [](code.md)**\]** **\[** [](optimize.md) **\]** С атрибутом **\[ Message \]** можно использовать только атрибуты Local, InAttribute, Code и optimize.</span><span class="sxs-lookup"><span data-stu-id="43582-109">Only the **\[**[**local**](local.md)**\]**, **\[**[**nocode**](nocode.md)**\]**, **\[**[**code**](code.md)**\],** and **\[**[**optimize**](optimize.md)**\]** attributes may be used with the **\[message\]** attribute.</span></span>

</dd> <dt>

<span data-ttu-id="43582-110">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="43582-110">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="43582-111">Имя функции, определенное в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="43582-111">The name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="43582-112">*необязательные атрибуты-Parameter*</span><span class="sxs-lookup"><span data-stu-id="43582-112">*optional-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="43582-113">Ноль или несколько атрибутов MIDL, которые будут применены к параметру.</span><span class="sxs-lookup"><span data-stu-id="43582-113">Zero or more MIDL attributes that will be applied to the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="43582-114">*Param-Name*</span><span class="sxs-lookup"><span data-stu-id="43582-114">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="43582-115">Имя параметра, определенное в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="43582-115">The name of the parameter as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43582-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="43582-116">Remarks</span></span>

<span data-ttu-id="43582-117">Как сообщения от клиента, удаленные вызовы процедур с атрибутом **\[ сообщения \]** доставляются на сервер асинхронно через транспорт очереди сообщений [**нкадг \_ MQ**](ncadg-mq.md) .</span><span class="sxs-lookup"><span data-stu-id="43582-117">As messages from the client, remote procedure calls with the **\[message\]** attribute are delivered to the server asynchronously over the [**ncadg\_mq**](ncadg-mq.md) message-queuing transport.</span></span> <span data-ttu-id="43582-118">Можно указать обмен сообщениями в синхронном режиме, указав транспортный протокол **нкадг \_ MQ** без использования атрибута **\[ \] Message** .</span><span class="sxs-lookup"><span data-stu-id="43582-118">You can indicate synchronous-mode messaging by specifying the **ncadg\_mq** transport protocol without using the **\[message\]** attribute.</span></span>

<span data-ttu-id="43582-119">При указании обмена сообщениями в асинхронном режиме атрибут **\[ Message \]** позволяет клиенту выполнить удаленный вызов процедуры и вернуться немедленно, даже если серверное приложение не отвечает.</span><span class="sxs-lookup"><span data-stu-id="43582-119">By specifying asynchronous-mode messaging, the **\[message\]** attribute allows the client to make the remote procedure call and return immediately, even when the server application is not responding.</span></span> <span data-ttu-id="43582-120">Если целевой сервер недоступен, вызов будет сохранен до тех пор, пока сервер не станет доступным.</span><span class="sxs-lookup"><span data-stu-id="43582-120">If the target server is not available, the call will be stored until the server becomes available.</span></span>

<span data-ttu-id="43582-121">Кроме того, Обмен сообщениями в асинхронном режиме позволяет управлять свойствами очереди сообщений для сервера.</span><span class="sxs-lookup"><span data-stu-id="43582-121">In addition, asynchronous-mode messaging lets you control message-queue properties of the receive queue for the server.</span></span> <span data-ttu-id="43582-122">Дополнительные сведения о выборе качества обслуживания, приоритета вызова и времени жизни вызова для серверного процесса см. в разделе [**рпкбиндингсетоптион**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption) .</span><span class="sxs-lookup"><span data-stu-id="43582-122">See [**RpcBindingSetOption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption) for more information on selecting quality of service, call priority, and call lifetime for the server process.</span></span>

<span data-ttu-id="43582-123">К атрибуту **\[ Message \]** также применяются следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="43582-123">The following restrictions also apply to the **\[message\]** attribute:</span></span>

-   <span data-ttu-id="43582-124">Служба очередей сообщений Майкрософт должна быть реализована в системах клиента и сервера, и системы должны быть видимы друг с другом, как определено в области установки очереди сообщений.</span><span class="sxs-lookup"><span data-stu-id="43582-124">Microsoft Message Queuing must be implemented in the client and server systems and the systems must be visible to each other as determined by the scope of the message queue installation.</span></span>
-   <span data-ttu-id="43582-125">Привязка должна использовать хорошо известные конечные точки и транспортный протокол [**нкадг \_ MQ**](ncadg-mq.md) .</span><span class="sxs-lookup"><span data-stu-id="43582-125">The binding must use well-known endpoints and the [**ncadg\_mq**](ncadg-mq.md) transport protocol.</span></span>
-   <span data-ttu-id="43582-126">Функция не может содержать выходные параметры или тип возвращаемого значения, отличный от [**void**](void.md).</span><span class="sxs-lookup"><span data-stu-id="43582-126">The function cannot contain output parameters or a return type other than [**void**](void.md).</span></span> <span data-ttu-id="43582-127">Обратите внимание, что Последнее ограничение делает атрибут **\[ сообщения \]** непригодным для методов интерфейса COM (Object) в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="43582-127">Note that the latter restriction makes the **\[message\]** attribute unsuitable for COM (object) interface methods, at this time.</span></span> <span data-ttu-id="43582-128">Следующий выпуск MIDL позволяет функциям **\[ \] сообщений** возвращать \_ состояние ошибки \_ t или HRESULT.</span><span class="sxs-lookup"><span data-stu-id="43582-128">The next release of MIDL will permit **\[message\]** functions to return error\_status\_t or HRESULT.</span></span>
-   <span data-ttu-id="43582-129">Любой интерфейс, содержащий хотя бы один вызов **\[ \] сообщения** , должен быть зарегистрирован путем вызова [**рпксерверрегистериф**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) или [**рпксерверрегистерифекс**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterifex) перед вызовом [**рпксерверусепротсекепекс (нкадг \_ MQ)**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqepex).</span><span class="sxs-lookup"><span data-stu-id="43582-129">Any interface that contains at least one **\[message\]** call must be registered by calling [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) or [**RpcServerRegisterIfEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterifex) before calling [**RpcServerUseProtseqEpEx(ncadg\_mq)**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqepex).</span></span> <span data-ttu-id="43582-130">В противном случае вызовы, ожидающие очереди для сервера, будут считываться перед регистрацией интерфейса, и вызовы завершатся ошибкой.</span><span class="sxs-lookup"><span data-stu-id="43582-130">Otherwise, calls that were waiting on the queue for the server will be read before the interface is registered, and the calls will fail.</span></span>

## <a name="examples"></a><span data-ttu-id="43582-131">Примеры</span><span class="sxs-lookup"><span data-stu-id="43582-131">Examples</span></span>

``` syntax
[message] void DisplayString(
    [in, string] char * p1);
 
[message] void VarDataArray(
    [in, size_is(iSize)] ARRAY_TYPE lpMyArray,
    [in] int iSize,
    [in] unsigned long ulChksum);
```

## <a name="see-also"></a><span data-ttu-id="43582-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43582-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43582-133">**приведен**</span><span class="sxs-lookup"><span data-stu-id="43582-133">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="43582-134">**Языковые**</span><span class="sxs-lookup"><span data-stu-id="43582-134">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="43582-135">**нкадг \_ MQ**</span><span class="sxs-lookup"><span data-stu-id="43582-135">**ncadg\_mq**</span></span>](ncadg-mq.md)
</dt> <dt>

[<span data-ttu-id="43582-136">**nocode**</span><span class="sxs-lookup"><span data-stu-id="43582-136">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="43582-137">**увеличить**</span><span class="sxs-lookup"><span data-stu-id="43582-137">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="43582-138">Очередь сообщений RPC</span><span class="sxs-lookup"><span data-stu-id="43582-138">RPC Message Queuing</span></span>](/windows/desktop/Rpc/rpc-message-queuing)
</dt> <dt>

[<span data-ttu-id="43582-139">**рпкбиндингсетоптион**</span><span class="sxs-lookup"><span data-stu-id="43582-139">**RpcBindingSetOption**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption)
</dt> <dt>

[<span data-ttu-id="43582-140">**рпкбиндингинкоптион**</span><span class="sxs-lookup"><span data-stu-id="43582-140">**RpcBindingInqOption**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqoption)
</dt> <dt>

[<span data-ttu-id="43582-141">**void**</span><span class="sxs-lookup"><span data-stu-id="43582-141">**void**</span></span>](void.md)
</dt> </dl>

 

 