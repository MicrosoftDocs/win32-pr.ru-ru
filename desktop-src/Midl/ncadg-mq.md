---
title: атрибут ncadg_mq
description: '\_Ключевое слово нкадг MQ определяет службы очередей сообщений Майкрософт (MSMQ) в качестве транспортного протокола для конечной точки. Этот протокол устарел и не должен использоваться в новых приложениях.'
ms.assetid: 7472fc47-c1f0-4578-8aef-b655505e0563
keywords:
- ncadg_mq атрибута MIDL
topic_type:
- apiref
api_name:
- ncadg_mq
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0acc433b55ba9f3c6d8919bef9b8db470bc0f5a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987426"
---
# <a name="ncadg_mq-attribute"></a><span data-ttu-id="0abc2-105">нкадг \_ MQ, атрибут</span><span class="sxs-lookup"><span data-stu-id="0abc2-105">ncadg\_mq attribute</span></span>

<span data-ttu-id="0abc2-106">Ключевое слово **нкадг \_ MQ** определяет службы очередей сообщений Майкрософт (MSMQ) в качестве транспортного протокола для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="0abc2-106">The **ncadg\_mq** keyword identifies Microsoft Message Queuing Services (MSMQ) as the transport protocol for the endpoint.</span></span> <span data-ttu-id="0abc2-107">Этот протокол устарел и не должен использоваться в новых приложениях.</span><span class="sxs-lookup"><span data-stu-id="0abc2-107">This protocol is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncadg_mq:server-name")
```

## <a name="parameters"></a><span data-ttu-id="0abc2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0abc2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0abc2-109">*имя сервера*</span><span class="sxs-lookup"><span data-stu-id="0abc2-109">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="0abc2-110">Указывает имя сервера или узла, компьютер.</span><span class="sxs-lookup"><span data-stu-id="0abc2-110">Specifies the name of the server, or host, computer.</span></span> <span data-ttu-id="0abc2-111">Имя является символьной строкой и может быть полным доменным именем.</span><span class="sxs-lookup"><span data-stu-id="0abc2-111">The name is a character string and may be a fully qualified domain name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0abc2-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0abc2-112">Remarks</span></span>

<span data-ttu-id="0abc2-113">Чтобы использовать транспортный протокол **нкадг \_ MQ** , компоненты MSMQ должны быть полностью установлены, а клиентские и серверные системы должны быть доступны через протоколы MQ.</span><span class="sxs-lookup"><span data-stu-id="0abc2-113">In order to use the **ncadg\_mq** transport protocol, the MSMQ components must be fully installed and the client and server systems must be reachable through the MQ protocols.</span></span>

<span data-ttu-id="0abc2-114">Протокол **нкадг \_ MQ** не поддерживает динамические конечные точки или [**широковещательные**](broadcast.md) вызовы.</span><span class="sxs-lookup"><span data-stu-id="0abc2-114">The **ncadg\_mq** protocol does not support dynamic endpoints or [**broadcast**](broadcast.md) calls.</span></span> <span data-ttu-id="0abc2-115">Как и в случае с другими протоколами датаграмм, **нкадг \_ MQ** не поддерживает обратные вызовы; любые функции, использующие атрибут [**обратного вызова**](callback.md) , завершатся ошибкой.</span><span class="sxs-lookup"><span data-stu-id="0abc2-115">As with other datagram protocols, **ncadg\_mq** does not support callbacks; any functions using the [**callback**](callback.md) attribute will fail.</span></span>

> [!Note]  
> <span data-ttu-id="0abc2-116">Это семейство протоколов не поддерживается в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0abc2-116">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="0abc2-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="0abc2-117">Examples</span></span>

<span data-ttu-id="0abc2-118">Синтаксис протокола очереди сообщений определяется независимо от спецификации IDL.</span><span class="sxs-lookup"><span data-stu-id="0abc2-118">The syntax of the message-queue protocol is defined independently of the IDL specification.</span></span> <span data-ttu-id="0abc2-119">Компилятор MIDL выполняет некоторую проверку синтаксиса, но не гарантирует, что указана правильная спецификация конечной точки.</span><span class="sxs-lookup"><span data-stu-id="0abc2-119">The MIDL compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="0abc2-120">Некоторые ошибки могут выводиться во время выполнения, а не во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="0abc2-120">Some errors may be reported at run time rather than during compilation.</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_mq:rainier") 
]
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="0abc2-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0abc2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0abc2-122">**транслировать**</span><span class="sxs-lookup"><span data-stu-id="0abc2-122">**broadcast**</span></span>](broadcast.md)
</dt> <dt>

[<span data-ttu-id="0abc2-123">**обратный вызов**</span><span class="sxs-lookup"><span data-stu-id="0abc2-123">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="0abc2-124">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="0abc2-124">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="0abc2-125">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="0abc2-125">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="0abc2-126">**Сообщение**</span><span class="sxs-lookup"><span data-stu-id="0abc2-126">**message**</span></span>](message.md)
</dt> <dt>

[<span data-ttu-id="0abc2-127">Очередь сообщений RPC</span><span class="sxs-lookup"><span data-stu-id="0abc2-127">RPC Message Queuing</span></span>](/windows/desktop/Rpc/rpc-message-queuing)
</dt> <dt>

[<span data-ttu-id="0abc2-128">Строковая привязка</span><span class="sxs-lookup"><span data-stu-id="0abc2-128">String Binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 