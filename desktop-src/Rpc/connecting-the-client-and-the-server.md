---
title: Подключение клиента и сервера
description: Для обмена данными клиентские и серверные программы должны установить сеанс связи через сеть или сети, соединяющие их.
ms.assetid: 1164252a-7615-4958-9d2f-cf35c0db513a
keywords:
- Удаленный вызов процедур RPC, задачи, подключение клиента и сервера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98a22ea7a9a6dd30f2b9495b6d2ee868aac217f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486857"
---
# <a name="connecting-the-client-and-the-server"></a><span data-ttu-id="66dda-104">Подключение клиента и сервера</span><span class="sxs-lookup"><span data-stu-id="66dda-104">Connecting the Client and the Server</span></span>

<span data-ttu-id="66dda-105">Для обмена данными клиентские и серверные программы должны установить сеанс связи через сеть или сети, соединяющие их.</span><span class="sxs-lookup"><span data-stu-id="66dda-105">To communicate, client and server programs must establish a communication session across the network or networks that connect them.</span></span> <span data-ttu-id="66dda-106">После установления соединения клиент может вызывать удаленные процедуры в серверной программе так, как если бы они были локальными для клиентской программы.</span><span class="sxs-lookup"><span data-stu-id="66dda-106">Once they establish the connection, the client can call remote procedures in the server program as if they were local to the client program.</span></span>

<span data-ttu-id="66dda-107">В этом разделе приводятся общие сведения о том, как установить соединение между клиентами и серверами для удаленных вызовов процедур.</span><span class="sxs-lookup"><span data-stu-id="66dda-107">This section provides a conceptual overview of how to establish a connection between clients and servers for remote procedure calls.</span></span> <span data-ttu-id="66dda-108">Он не содержит подробного обсуждения этого раздела.</span><span class="sxs-lookup"><span data-stu-id="66dda-108">It does not provide an in-depth discussion of this topic.</span></span> <span data-ttu-id="66dda-109">Все концепции в этом разделе подробно описаны в последующих главах и в разделе Справочник по функциям RPC.</span><span class="sxs-lookup"><span data-stu-id="66dda-109">All of the concepts in this section are presented in detail in later chapters and in the RPC Function Reference section.</span></span>

<span data-ttu-id="66dda-110">Обсуждение, представленное в этом разделе, состоит из следующих разделов:</span><span class="sxs-lookup"><span data-stu-id="66dda-110">The discussion presented in this section is divided into the following topics:</span></span>

-   [<span data-ttu-id="66dda-111">Основная терминология привязки RPC</span><span class="sxs-lookup"><span data-stu-id="66dda-111">Essential RPC Binding Terminology</span></span>](essential-rpc-binding-terminology.md)
-   [<span data-ttu-id="66dda-112">Как сервер готовится к подключению</span><span class="sxs-lookup"><span data-stu-id="66dda-112">How the Server Prepares for a Connection</span></span>](how-the-server-prepares-for-a-connection.md)
-   [<span data-ttu-id="66dda-113">Как клиент устанавливает подключение</span><span class="sxs-lookup"><span data-stu-id="66dda-113">How the Client Establishes a Connection</span></span>](how-the-client-establishes-a-connection.md)

<span data-ttu-id="66dda-114">Обратите внимание, что в обсуждении предполагается наличие явных дескрипторов привязки.</span><span class="sxs-lookup"><span data-stu-id="66dda-114">Note that the discussion assumes explicit binding handles.</span></span> <span data-ttu-id="66dda-115">Однако если приложение использует другие типы дескрипторов привязки, может потребоваться изменить шаги, описанные в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="66dda-115">However, if your application uses other types of binding handles, you may have to modify the steps presented in this section.</span></span> <span data-ttu-id="66dda-116">Дополнительные сведения см. в разделе [Binding and Handles](binding-and-handles.md).</span><span class="sxs-lookup"><span data-stu-id="66dda-116">For more information, see [Binding and Handles](binding-and-handles.md).</span></span>

 

 




