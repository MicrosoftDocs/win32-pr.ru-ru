---
title: Требования к системе для приложений RPC-Message Queuing
description: Чтобы использовать транспорт очереди сообщений в клиентском или серверном приложении RPC, на сервере и на клиентских компьютерах должна быть установлена соответствующая Платформа операционной системы и программное обеспечение очереди сообщений.
ms.assetid: f90318a6-0be6-4e1a-a1a5-1709808b5d3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1274c888506a6868eb7ded5ba96c5f1ea8dc8b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413475"
---
# <a name="system-requirements-for-rpc-message-queuing-applications"></a><span data-ttu-id="291f6-103">Требования к системе для приложений RPC-Message Queuing</span><span class="sxs-lookup"><span data-stu-id="291f6-103">System Requirements for RPC-Message Queuing Applications</span></span>

<span data-ttu-id="291f6-104">Чтобы использовать транспорт очереди сообщений в клиентском или серверном приложении RPC, на сервере и на клиентских компьютерах должна быть установлена соответствующая Платформа операционной системы и программное обеспечение очереди сообщений.</span><span class="sxs-lookup"><span data-stu-id="291f6-104">To use the message-queuing transport in an RPC client/server application, the server and client computers must have the appropriate operating system platform and Message Queuing software installed.</span></span>

<span data-ttu-id="291f6-105">Требования для серверных компьютеров:</span><span class="sxs-lookup"><span data-stu-id="291f6-105">Requirements for server computers are:</span></span>

-   <span data-ttu-id="291f6-106">Microsoft Windows Server 2003, Windows XP или Windows 2000 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="291f6-106">Microsoft Windows Server 2003, Windows XP, or Windows 2000 or later.</span></span>
-   <span data-ttu-id="291f6-107">SQL Server версии 6,5 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="291f6-107">SQL Server version 6.5 or later.</span></span>
-   <span data-ttu-id="291f6-108">Основной контроллер предприятия или основной контроллер сайта очереди сообщений.</span><span class="sxs-lookup"><span data-stu-id="291f6-108">Message Queuing Primary Enterprise Controller or Primary Site Controller.</span></span>
-   <span data-ttu-id="291f6-109">Транспортная библиотека RPC на стороне сервера (RpcMqSvr.dll).</span><span class="sxs-lookup"><span data-stu-id="291f6-109">RPC server-side transport DLL (RpcMqSvr.dll).</span></span>

<span data-ttu-id="291f6-110">Требования для клиентских компьютеров:</span><span class="sxs-lookup"><span data-stu-id="291f6-110">Requirements for client computers are:</span></span>

-   <span data-ttu-id="291f6-111">Microsoft Windows Server 2003, Windows XP или Windows 2000 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="291f6-111">Microsoft Windows Server 2003, Windows XP, or Windows 2000 or later.</span></span>
-   <span data-ttu-id="291f6-112">Клиент очереди сообщений Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="291f6-112">Microsoft Message Queuing Client.</span></span>
-   <span data-ttu-id="291f6-113">DLL-библиотека транспорта RPC на стороне клиента (RpcMqCl.dll).</span><span class="sxs-lookup"><span data-stu-id="291f6-113">RPC client-side transport DLL (RpcMqCl.dll).</span></span>

<span data-ttu-id="291f6-114">Если компоненты MSMQ установлены на клиентских и серверных компьютерах, реестры системы автоматически настраиваются для включения транспортного протокола очереди сообщений [нкадг \_ MQ](/windows/desktop/Midl/ncadg-mq) для удаленных вызовов процедур.</span><span class="sxs-lookup"><span data-stu-id="291f6-114">When the MSMQ components are installed on the client and server computers, the system registries are automatically configured to include the [ncadg\_mq](/windows/desktop/Midl/ncadg-mq) message-queuing transport protocol for remote procedure calls.</span></span>

<span data-ttu-id="291f6-115">Чтобы создать приложение RPC-MSMQ, вам потребуется следующее:</span><span class="sxs-lookup"><span data-stu-id="291f6-115">To build your RPC-MSMQ application you need the following:</span></span>

-   <span data-ttu-id="291f6-116">Microsoft Windows Server 2003, Windows XP или Windows 2000 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="291f6-116">Microsoft Windows Server 2003, Windows XP, or Windows 2000 or later</span></span>
-   <span data-ttu-id="291f6-117">MIDL версии 3.1.76 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="291f6-117">MIDL version 3.1.76 or later.</span></span>

 

 