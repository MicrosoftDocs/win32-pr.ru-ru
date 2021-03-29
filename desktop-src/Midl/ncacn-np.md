---
title: атрибут ncacn_np
description: '\_Ключевое слово нкакн NP определяет именованные каналы в качестве семейства протоколов для конечной точки.'
ms.assetid: 02961bb8-faf0-42e5-b134-dd2983e6d146
keywords:
- ncacn_np атрибута MIDL
topic_type:
- apiref
api_name:
- ncacn_np
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84634e6bb5d2b634439be767ad44749291cffe11
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791202"
---
# <a name="ncacn_np-attribute"></a><span data-ttu-id="d19f7-104">\_атрибут нкакн NP</span><span class="sxs-lookup"><span data-stu-id="d19f7-104">ncacn\_np attribute</span></span>

<span data-ttu-id="d19f7-105">Ключевое слово **нкакн \_ NP** определяет именованные каналы в качестве семейства протоколов для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="d19f7-105">The **ncacn\_np** keyword identifies named pipes as the protocol family for the endpoint.</span></span>

``` syntax
endpoint("ncacn_np:server-name[\\pipe\\pipe-name]")
```

## <a name="parameters"></a><span data-ttu-id="d19f7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d19f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d19f7-107">*имя сервера*</span><span class="sxs-lookup"><span data-stu-id="d19f7-107">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d19f7-108">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="d19f7-108">Optional.</span></span> <span data-ttu-id="d19f7-109">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="d19f7-109">Specifies the name of the server.</span></span> <span data-ttu-id="d19f7-110">Символы обратной косой черты необязательны.</span><span class="sxs-lookup"><span data-stu-id="d19f7-110">Backslash characters are optional.</span></span>

</dd> <dt>

<span data-ttu-id="d19f7-111">*имя канала*</span><span class="sxs-lookup"><span data-stu-id="d19f7-111">*pipe-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d19f7-112">Указывает допустимое имя канала.</span><span class="sxs-lookup"><span data-stu-id="d19f7-112">Specifies a valid pipe name.</span></span> <span data-ttu-id="d19f7-113">Допустимое имя канала — это строка, содержащая идентификаторы, разделенные символами обратной косой черты.</span><span class="sxs-lookup"><span data-stu-id="d19f7-113">A valid pipe name is a string containing identifiers separated by backslash characters.</span></span> <span data-ttu-id="d19f7-114">Первый идентификатор должен быть [**pipe**](pipe.md).</span><span class="sxs-lookup"><span data-stu-id="d19f7-114">The first identifier must be [**pipe**](pipe.md).</span></span> <span data-ttu-id="d19f7-115">Каждый идентификатор должен быть отделен двумя символами обратной косой черты.</span><span class="sxs-lookup"><span data-stu-id="d19f7-115">Each identifier must be separated by two backslash characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d19f7-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d19f7-116">Remarks</span></span>

<span data-ttu-id="d19f7-117">Сервер создает экземпляр именованного канала, который затем доступен любому клиенту.</span><span class="sxs-lookup"><span data-stu-id="d19f7-117">A server creates an instance of a named pipe that is then available to any client.</span></span> <span data-ttu-id="d19f7-118">Когда клиент пытается подключиться, существующий экземпляр связывается с этим клиентом.</span><span class="sxs-lookup"><span data-stu-id="d19f7-118">When a client attempts to connect, the existing instance is associated with that client.</span></span> <span data-ttu-id="d19f7-119">Прежде чем другой клиент сможет подключиться, сервер должен создать другой экземпляр именованного канала.</span><span class="sxs-lookup"><span data-stu-id="d19f7-119">Before another client can connect, the server must create another instance of the named pipe.</span></span> <span data-ttu-id="d19f7-120">Если клиент пытается выполнить привязку к серверу до создания нового экземпляра, вызов привязки, [**рпкбиндингфромстрингбиндинг**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding), может завершиться ошибкой с сообщением об ошибке " \_ сервер RPC S \_ занят" \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d19f7-120">If a client tries to bind to the server before the new instance is created, the binding call, [**RpcBindingFromStringBinding**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding), may fail with the error message RPC\_S\_SERVER\_TOO\_BUSY.</span></span> <span data-ttu-id="d19f7-121">Поэтому необходимо убедиться, что клиентское приложение обрабатывает случай, когда сервер слишком занят и не может принять соединение.</span><span class="sxs-lookup"><span data-stu-id="d19f7-121">Therefore, you need to make sure that your client application handles the case where the server is too busy to accept a connection.</span></span> <span data-ttu-id="d19f7-122">Клиент должен автоматически повторить попытку, предложить пользователю выполнить действие или завершиться неудачно.</span><span class="sxs-lookup"><span data-stu-id="d19f7-122">The client should automatically retry, prompt the user for a course of action, or fail gracefully.</span></span>

<span data-ttu-id="d19f7-123">Синтаксис строки порта именованного канала, как и все строки портов, определяется реализацией транспорта и не зависит от спецификации IDL.</span><span class="sxs-lookup"><span data-stu-id="d19f7-123">The syntax of the named-pipe port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="d19f7-124">Компилятор MIDL выполняет ограниченную проверку синтаксиса, но не гарантирует, что указана правильная спецификация конечной точки.</span><span class="sxs-lookup"><span data-stu-id="d19f7-124">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="d19f7-125">Некоторые классы ошибок могут выводиться во время выполнения, а не во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="d19f7-125">Some classes of errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="d19f7-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="d19f7-126">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_np:[\\pipe\\stove\\hat]") 
] 
interface iface1
{
    // Interface definition statements.
}

[
    uuid(87654321-4000-2006-0000-20000000001b), 
    version(1.1), 
    endpoint("ncacn_np:\\\\myotherserver[\\pipe\\corncob]") 
] 
interface iface2
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="d19f7-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d19f7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d19f7-128">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="d19f7-128">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="d19f7-129">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="d19f7-129">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="d19f7-130">**нкакн \_ в \_ DSP**</span><span class="sxs-lookup"><span data-stu-id="d19f7-130">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="d19f7-131">**нкакн \_ днет \_ NSP**</span><span class="sxs-lookup"><span data-stu-id="d19f7-131">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="d19f7-132">**нкакн \_ IP \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="d19f7-132">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="d19f7-133">**нкакн \_ NetBIOS- \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="d19f7-133">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="d19f7-134">**нкакн \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="d19f7-134">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="d19f7-135">**нкакн \_ имена \_ NetBIOS**</span><span class="sxs-lookup"><span data-stu-id="d19f7-135">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="d19f7-136">**нкакн \_ NetBIOS, \_ протокол TCP**</span><span class="sxs-lookup"><span data-stu-id="d19f7-136">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="d19f7-137">**нкакн \_ ВНС \_ SPP**</span><span class="sxs-lookup"><span data-stu-id="d19f7-137">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="d19f7-138">**нкалрпк**</span><span class="sxs-lookup"><span data-stu-id="d19f7-138">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="d19f7-139">**нкадг \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="d19f7-139">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="d19f7-140">**нкадг \_ IP \_ UDP**</span><span class="sxs-lookup"><span data-stu-id="d19f7-140">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="d19f7-141">**Строковая привязка**</span><span class="sxs-lookup"><span data-stu-id="d19f7-141">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 