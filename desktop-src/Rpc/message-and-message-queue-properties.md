---
title: Свойства очереди сообщений и сообщений
description: Сообщение имеет свойства, которые определяют метку, текст сообщения и ряд параметров.
ms.assetid: d0c9126e-a2c6-4d70-b87a-154a570899fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0139a588b52f1de1de43d8ec50aebdaf57b995ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330952"
---
# <a name="message-and-message-queue-properties"></a><span data-ttu-id="b4597-103">Свойства очереди сообщений и сообщений</span><span class="sxs-lookup"><span data-stu-id="b4597-103">Message and Message Queue Properties</span></span>

<span data-ttu-id="b4597-104">Сообщение имеет свойства, которые определяют метку, текст сообщения и ряд параметров.</span><span class="sxs-lookup"><span data-stu-id="b4597-104">A message has properties, which specify a label, a message body, and a number of options.</span></span> <span data-ttu-id="b4597-105">К параметрам свойств сообщений могут относиться качество обслуживания, приоритет, ведение журнала, уровни конфиденциальности и проверки подлинности, а также время существования сообщения.</span><span class="sxs-lookup"><span data-stu-id="b4597-105">Message property options can include quality of service, priority, journaling, privacy and authentication levels, and the lifetime of the message.</span></span> <span data-ttu-id="b4597-106">В обычных (не использующих RPC) приложениях очереди сообщений эти свойства указываются путем вызова функций API MSMQ или методов объектов COM, которые описаны в документации по пакету SDK для MSMQ.</span><span class="sxs-lookup"><span data-stu-id="b4597-106">In conventional (non-RPC) message-queuing applications, you specify these properties by calling the MSMQ API functions or COM object methods, which are described in the MSMQ SDK documentation.</span></span> <span data-ttu-id="b4597-107">Клиентские приложения RPC могут задавать определенные свойства для вызовов удаленных процедур путем вызова [**рпкбиндингсетоптион**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) и [**рпкбиндингсетаусинфо**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span><span class="sxs-lookup"><span data-stu-id="b4597-107">RPC client applications can set certain properties for remote procedure calls by calling [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) and [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span> <span data-ttu-id="b4597-108">После установки свойства остаются в силе для каждого сообщения, пока клиентское приложение не выполнит их сброс.</span><span class="sxs-lookup"><span data-stu-id="b4597-108">Once set, the properties remain in effect for each message until the client application resets them.</span></span>

<span data-ttu-id="b4597-109">Очередь сообщений имеет свой собственный набор свойств, помимо сообщений.</span><span class="sxs-lookup"><span data-stu-id="b4597-109">A message queue has its own set of properties, apart from those of the messages.</span></span> <span data-ttu-id="b4597-110">Эти свойства уникально идентифицируют очередь и определяют класс службы, предоставляемый очередью, уровни конфиденциальности и проверки подлинности, необходимые для сообщений в этой очереди, а также сведения о том, должны ли сообщения быть частью распределенной транзакции.</span><span class="sxs-lookup"><span data-stu-id="b4597-110">These properties uniquely identify a queue and define the class of service that the queue provides, the privacy and authentication levels required for messages in this queue, and whether the messages are to be part of a distributed transaction.</span></span> <span data-ttu-id="b4597-111">Как и в случае со свойствами сообщения, свойства очереди сообщений указываются путем вызова функций API MSMQ или методов объектов COM, которые описаны в документации MSMQ.</span><span class="sxs-lookup"><span data-stu-id="b4597-111">As with message properties, you specify the properties of a message queue by calling the MSMQ API functions or COM object methods, which are described in the MSMQ documentation.</span></span> <span data-ttu-id="b4597-112">Однако серверное приложение RPC может задавать свойства собственной очереди получения при вызове [**рпксерверусепротсекепекс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) для установки привязки.</span><span class="sxs-lookup"><span data-stu-id="b4597-112">However, an RPC server application can specify properties of its own receive queue when it calls [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) to establish the binding.</span></span>

 

 




