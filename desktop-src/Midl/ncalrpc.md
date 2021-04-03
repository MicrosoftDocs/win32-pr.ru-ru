---
title: атрибут нкалрпк
description: Ключевое слово нкалрпк определяет локальное межпроцессное взаимодействие как семейство протоколов для конечной точки. Это ключевое слово является одним из допустимых имен семейств протоколов, которые должны использоваться с атрибутом \ Endpoint \.
ms.assetid: 0009f794-5c14-4484-9023-cb20c7030dc5
keywords:
- атрибут нкалрпк MIDL
topic_type:
- apiref
api_name:
- ncalrpc
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f20ae9e347303288868eeb16758736047fecc1b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987476"
---
# <a name="ncalrpc-attribute"></a><span data-ttu-id="9acdd-105">атрибут нкалрпк</span><span class="sxs-lookup"><span data-stu-id="9acdd-105">ncalrpc attribute</span></span>

<span data-ttu-id="9acdd-106">Ключевое слово **нкалрпк** определяет локальное межпроцессное взаимодействие как семейство протоколов для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="9acdd-106">The **ncalrpc** keyword identifies local interprocess communication as the protocol family for the endpoint.</span></span> <span data-ttu-id="9acdd-107">Это ключевое слово является одним из допустимых имен семейств протоколов, которые должны использоваться с **\[** [](endpoint.md) **\]** атрибутом Endpoint.</span><span class="sxs-lookup"><span data-stu-id="9acdd-107">This keyword is one of the valid protocol family names that must be used with the **\[**[**endpoint**](endpoint.md)**\]** attribute.</span></span>

``` syntax
endpoint("ncalrpc:[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="9acdd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9acdd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9acdd-109">*имя порта*</span><span class="sxs-lookup"><span data-stu-id="9acdd-109">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="9acdd-110">Строка символов, указывающая коммуникационный порт (приложение, служба или экземпляр службы), который клиент использует для выполнения межпроцессных вызовов к серверу.</span><span class="sxs-lookup"><span data-stu-id="9acdd-110">A character string that specifies the communication port (an application, a service, or an instance of a service) that a client uses to make interprocess calls to a server.</span></span> <span data-ttu-id="9acdd-111">Строка может содержать до 53 символов и не должна содержать обратную косую черту ( \) символы).</span><span class="sxs-lookup"><span data-stu-id="9acdd-111">The string can contain up to 53 characters and should not contain any backslash (\) characters.</span></span> <span data-ttu-id="9acdd-112">Имя компьютера не должно использоваться с ключевым словом **нкалрпк** .</span><span class="sxs-lookup"><span data-stu-id="9acdd-112">The computer name must not be used with the **ncalrpc** keyword.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9acdd-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9acdd-113">Remarks</span></span>

<span data-ttu-id="9acdd-114">Синтаксис локальной строки порта межпроцессного взаимодействия, как и все строки портов, определяется реализацией транспорта и не зависит от спецификации IDL.</span><span class="sxs-lookup"><span data-stu-id="9acdd-114">The syntax of the local interprocess-communication port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="9acdd-115">Компилятор MIDL выполняет ограниченную проверку синтаксиса, но не гарантирует, что указана правильная спецификация конечной точки.</span><span class="sxs-lookup"><span data-stu-id="9acdd-115">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="9acdd-116">Некоторые классы ошибок могут выводиться во время выполнения, а не во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="9acdd-116">Some classes of errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="9acdd-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="9acdd-117">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncalrpc:[myapplicationname]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="9acdd-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9acdd-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9acdd-119">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="9acdd-119">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="9acdd-120">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="9acdd-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="9acdd-121">**нкакн \_ в \_ DSP**</span><span class="sxs-lookup"><span data-stu-id="9acdd-121">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="9acdd-122">**нкакн \_ днет \_ NSP**</span><span class="sxs-lookup"><span data-stu-id="9acdd-122">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="9acdd-123">**нкакн \_ IP \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="9acdd-123">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="9acdd-124">**нкакн \_ NetBIOS- \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="9acdd-124">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="9acdd-125">**нкакн \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="9acdd-125">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="9acdd-126">**нкакн \_ имена \_ NetBIOS**</span><span class="sxs-lookup"><span data-stu-id="9acdd-126">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="9acdd-127">**нкакн \_ NetBIOS, \_ протокол TCP**</span><span class="sxs-lookup"><span data-stu-id="9acdd-127">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="9acdd-128">**нкакн \_ NP**</span><span class="sxs-lookup"><span data-stu-id="9acdd-128">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="9acdd-129">**нкакн \_ ВНС \_ SPP**</span><span class="sxs-lookup"><span data-stu-id="9acdd-129">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="9acdd-130">**нкадг \_ IP \_ UDP**</span><span class="sxs-lookup"><span data-stu-id="9acdd-130">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="9acdd-131">**нкадг \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="9acdd-131">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="9acdd-132">Строковая привязка</span><span class="sxs-lookup"><span data-stu-id="9acdd-132">String Binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 