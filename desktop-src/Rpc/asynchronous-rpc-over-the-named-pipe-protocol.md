---
title: Асинхронный RPC по протоколу Named-Pipe
description: Если в качестве транспортного протокола используются именованные каналы (нкакн \_ NP), следует избегать разрешения большого количества бездействующих ожидающих вызовов на сервере.
ms.assetid: a1d0f758-91bc-4821-9a82-64ba6ce575ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf46f9e1c2ea5eb3fe20203db274233f5c10dec5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987808"
---
# <a name="asynchronous-rpc-over-the-named-pipe-protocol"></a><span data-ttu-id="d0023-103">Асинхронный RPC по протоколу Named-Pipe</span><span class="sxs-lookup"><span data-stu-id="d0023-103">Asynchronous RPC over the Named-Pipe Protocol</span></span>

<span data-ttu-id="d0023-104">Если в качестве транспортного протокола используются именованные каналы ([**нкакн \_ NP**](/windows/desktop/Midl/ncacn-np)), следует избегать разрешения большого количества бездействующих ожидающих вызовов на сервере.</span><span class="sxs-lookup"><span data-stu-id="d0023-104">If you use named pipes ([**ncacn\_np**](/windows/desktop/Midl/ncacn-np)) as your transport protocol, you should avoid allowing a large number of idle pending calls on the server.</span></span> <span data-ttu-id="d0023-105">При использовании именованных каналов каждый клиент, ожидающий ответа, будет иметь ожидающий именованный канал, считанный на сервере, каждый из которых требует определенного объема памяти ядра.</span><span class="sxs-lookup"><span data-stu-id="d0023-105">With named pipes, each client waiting for a reply will have a pending named pipe read on the server, each of which requires a certain amount of kernel memory.</span></span>

<span data-ttu-id="d0023-106">Например, вы не хотите использовать вызов уведомления для нового сообщения электронной почты с помощью транспорта именованных каналов, так как такой вызов останется ожидающим, даже когда клиенты бездействуют, а память ядра может быть исчерпана.</span><span class="sxs-lookup"><span data-stu-id="d0023-106">For example, you would not want to use a notification call for new e-mail with the named-pipe transport, because such a call would remain pending even when clients are idle, and kernel memory could be depleted.</span></span> <span data-ttu-id="d0023-107">Обратите внимание, что это не проблема с другими протоколами, ориентированными на подключения, например [**нкакн \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp).</span><span class="sxs-lookup"><span data-stu-id="d0023-107">Note that this is not a problem with the other connection-oriented protocols, such as [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp).</span></span>

<span data-ttu-id="d0023-108">Так как именованные каналы являются транспортным протоколом, приложение может использовать их, указав [**нкакн \_ NP**](/windows/desktop/Midl/ncacn-np) в качестве протокола в привязке строк.</span><span class="sxs-lookup"><span data-stu-id="d0023-108">Since named pipes are a transport protocol, your application can use them by specifying [**ncacn\_np**](/windows/desktop/Midl/ncacn-np) as the protocol in a string binding.</span></span> <span data-ttu-id="d0023-109">Дополнительные сведения об именованных каналах см. в разделе [именованные каналы](/windows/desktop/ipc/named-pipes).</span><span class="sxs-lookup"><span data-stu-id="d0023-109">For more information on named pipes, see [Named Pipes](/windows/desktop/ipc/named-pipes).</span></span> <span data-ttu-id="d0023-110">Дополнительные сведения о создании привязок строк см. в разделе [использование строковых привязок](finding-server-host-systems.md).</span><span class="sxs-lookup"><span data-stu-id="d0023-110">For details on creating string bindings, see [Using String Bindings](finding-server-host-systems.md).</span></span>

 

 