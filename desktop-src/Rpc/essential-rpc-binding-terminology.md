---
title: Основная терминология привязки RPC
description: Чтобы лучше помочь в обсуждении процесса подключения клиента/сервера, полезно ознакомиться со следующими условиями.
ms.assetid: 05aca325-87ee-4581-9152-a8a2ff7fb490
keywords:
- Удаленный вызов процедур RPC, описание, привязка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b18b8d3872c830d90079ad740505fead14c1b3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070454"
---
# <a name="essential-rpc-binding-terminology"></a><span data-ttu-id="91faa-104">Основная терминология привязки RPC</span><span class="sxs-lookup"><span data-stu-id="91faa-104">Essential RPC Binding Terminology</span></span>

<span data-ttu-id="91faa-105">Чтобы лучше помочь в обсуждении процесса подключения клиента/сервера, полезно ознакомиться со следующими условиями.</span><span class="sxs-lookup"><span data-stu-id="91faa-105">To better aid in a discussion of the client/server connection process, it is helpful to know the following terms.</span></span>

## <a name="parameters"></a><span data-ttu-id="91faa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="91faa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91faa-107"><span id="Protocol_Sequence"></span><span id="protocol_sequence"></span><span id="PROTOCOL_SEQUENCE"></span>Последовательность протокола</span><span class="sxs-lookup"><span data-stu-id="91faa-107"><span id="Protocol_Sequence"></span><span id="protocol_sequence"></span><span id="PROTOCOL_SEQUENCE"></span>Protocol Sequence</span></span>
</dt> <dd>

<span data-ttu-id="91faa-108">Когда сетевые операционные системы взаимодействуют друг с другом, они должны прослушивать и говорить на одном и том же языке.</span><span class="sxs-lookup"><span data-stu-id="91faa-108">When network operating systems communicate with each other, they must listen and speak the same language.</span></span> <span data-ttu-id="91faa-109">Эти языки называются *последовательностью протоколов*.</span><span class="sxs-lookup"><span data-stu-id="91faa-109">These languages are called *protocol sequences*.</span></span> <span data-ttu-id="91faa-110">Клиентские и серверные программы должны использовать последовательности протоколов, которые подключаются к ним в сети.</span><span class="sxs-lookup"><span data-stu-id="91faa-110">Client and server programs must use protocol sequences that the network connecting them supports.</span></span> <span data-ttu-id="91faa-111">Microsoft RPC поддерживает различные последовательности протоколов.</span><span class="sxs-lookup"><span data-stu-id="91faa-111">Microsoft RPC supports a variety of protocol sequences.</span></span> <span data-ttu-id="91faa-112">Дополнительные сведения см. [в разделе Выбор последовательности протокола](selecting-a-protocol-sequence.md), [Указание последовательностей протоколов](specifying-protocol-sequences.md)и [**конечных точек**](/windows/desktop/Midl/endpoint).</span><span class="sxs-lookup"><span data-stu-id="91faa-112">For details, see [Selecting a Protocol Sequence](selecting-a-protocol-sequence.md), [Specifying Protocol Sequences](specifying-protocol-sequences.md), and [**endpoint**](/windows/desktop/Midl/endpoint).</span></span>

</dd> <dt>

<span data-ttu-id="91faa-113"><span id="Server_Host_Computer_or_Server_Host_System"></span><span id="server_host_computer_or_server_host_system"></span><span id="SERVER_HOST_COMPUTER_OR_SERVER_HOST_SYSTEM"></span>Компьютер узла сервера или система узла сервера</span><span class="sxs-lookup"><span data-stu-id="91faa-113"><span id="Server_Host_Computer_or_Server_Host_System"></span><span id="server_host_computer_or_server_host_system"></span><span id="SERVER_HOST_COMPUTER_OR_SERVER_HOST_SYSTEM"></span>Server Host Computer or Server Host System</span></span>
</dt> <dd>

<span data-ttu-id="91faa-114">Серверная программа выполняется на главном компьютере сервера.</span><span class="sxs-lookup"><span data-stu-id="91faa-114">The server program runs on the server host computer.</span></span> <span data-ttu-id="91faa-115">Однако при работе с клиентскими и серверными вычислениями подразумевается как серверная программа, так и компьютер узла сервера в качестве сервера.</span><span class="sxs-lookup"><span data-stu-id="91faa-115">However, much literature on client/server computing refers to both the server program and the server host computer as the "server."</span></span> <span data-ttu-id="91faa-116">В результате не всегда ясно, какие из них обсуждаются.</span><span class="sxs-lookup"><span data-stu-id="91faa-116">The result is that it is not always clear which is being discussed.</span></span>

</dd> <dt>

<span data-ttu-id="91faa-117"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="91faa-117"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span>
</dt> <dd>

<span data-ttu-id="91faa-118">Серверные программы прослушивают порт или группу портов на компьютере узла сервера для клиентских запросов.</span><span class="sxs-lookup"><span data-stu-id="91faa-118">Server programs listen to a port or a group of ports on the server host computer for client requests.</span></span> <span data-ttu-id="91faa-119">Системы узла сервера поддерживают базу данных этих портов, которые называются конечными точками в RPC.</span><span class="sxs-lookup"><span data-stu-id="91faa-119">Server host systems maintain a database of these ports, which are called endpoints in RPC.</span></span> <span data-ttu-id="91faa-120">База данных называется картой конечных точек.</span><span class="sxs-lookup"><span data-stu-id="91faa-120">The database is called the endpoint map.</span></span>

</dd> <dt>

<span data-ttu-id="91faa-121"><span id="Binding"></span><span id="binding"></span><span id="BINDING"></span>Вязывания</span><span class="sxs-lookup"><span data-stu-id="91faa-121"><span id="Binding"></span><span id="binding"></span><span id="BINDING"></span>Binding</span></span>
</dt> <dd>

<span data-ttu-id="91faa-122">Клиентские программы создают привязку к серверу для установления сеанса связи.</span><span class="sxs-lookup"><span data-stu-id="91faa-122">Client programs create a binding to the server to establish a communication session.</span></span> <span data-ttu-id="91faa-123">Привязка содержит все сведения, необходимые клиентским приложениям для создания сеанса.</span><span class="sxs-lookup"><span data-stu-id="91faa-123">A binding contains all of the information the client applications needs to create the session.</span></span>

</dd> </dl>

 

 