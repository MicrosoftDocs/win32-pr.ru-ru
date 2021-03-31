---
title: Microsoft RPC
description: Microsoft RPC
ms.assetid: a9ca629a-2766-43d5-89da-73d0628b3c5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53be9d46368ae01aee25815327aafeaf7f44525b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772788"
---
# <a name="microsoft-rpc"></a><span data-ttu-id="d4c30-103">Microsoft RPC</span><span class="sxs-lookup"><span data-stu-id="d4c30-103">Microsoft RPC</span></span>

<span data-ttu-id="d4c30-104">Microsoft RPC — это модель для программирования в распределенных вычислительных средах.</span><span class="sxs-lookup"><span data-stu-id="d4c30-104">Microsoft RPC is a model for programming in a distributed computing environment.</span></span> <span data-ttu-id="d4c30-105">Целью RPC является обеспечение прозрачного взаимодействия, чтобы клиент взаимодействует непосредственно с сервером.</span><span class="sxs-lookup"><span data-stu-id="d4c30-105">The goal of RPC is to provide transparent communication so that the client appears to be directly communicating with the server.</span></span> <span data-ttu-id="d4c30-106">Реализация RPC Майкрософт совместима с RPC с открытым программным обеспечением (использование).</span><span class="sxs-lookup"><span data-stu-id="d4c30-106">Microsoft's implementation of RPC is compatible with the Open Software Foundation (OSF) Distributed Computing Environment (DCE) RPC.</span></span>

<span data-ttu-id="d4c30-107">Вы можете настроить RPC для использования одного или нескольких транспортов, одной или нескольких служб имен и одного или нескольких серверов безопасности.</span><span class="sxs-lookup"><span data-stu-id="d4c30-107">You can configure RPC to use one or more transports, one or more name services, and one or more security servers.</span></span> <span data-ttu-id="d4c30-108">Интерфейсы для этих поставщиков обрабатываются RPC.</span><span class="sxs-lookup"><span data-stu-id="d4c30-108">The interfaces to those providers are handled by RPC.</span></span> <span data-ttu-id="d4c30-109">Поскольку Microsoft RPC предназначен для работы с несколькими поставщиками, вы можете выбрать поставщиков, которые лучше подходят для вашей сети.</span><span class="sxs-lookup"><span data-stu-id="d4c30-109">Because Microsoft RPC is designed to work with multiple providers, you can choose the providers that work best for your network.</span></span> <span data-ttu-id="d4c30-110">Транспорт отвечает за передачу данных по сети.</span><span class="sxs-lookup"><span data-stu-id="d4c30-110">The transport is responsible for transmitting the data across the network.</span></span> <span data-ttu-id="d4c30-111">Служба имен принимает имя объекта, например моникер, и находит его расположение в сети.</span><span class="sxs-lookup"><span data-stu-id="d4c30-111">The name service takes an object name, such as a moniker, and finds its location on the network.</span></span> <span data-ttu-id="d4c30-112">Сервер безопасности предлагает приложениям возможность запретить доступ определенным пользователям и (или) группам.</span><span class="sxs-lookup"><span data-stu-id="d4c30-112">The security server offers applications the option of denying access to specific users and/or groups.</span></span> <span data-ttu-id="d4c30-113">Более подробные сведения о безопасности приложений см. в разделе [правила разработки интерфейсов](interface-design-rules.md) .</span><span class="sxs-lookup"><span data-stu-id="d4c30-113">See [Interface Design Rules](interface-design-rules.md) for more detailed information about application security.</span></span>

<span data-ttu-id="d4c30-114">Помимо библиотек времени выполнения RPC, Microsoft RPC включает в себя язык описания интерфейса (IDL) и его компилятор.</span><span class="sxs-lookup"><span data-stu-id="d4c30-114">In addition to the RPC run-time libraries, Microsoft RPC includes the Interface Definition Language (IDL) and its compiler.</span></span> <span data-ttu-id="d4c30-115">Хотя IDL-файл является стандартной частью RPC, корпорация Майкрософт улучшила ее функциональность для поддержки пользовательских COM-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="d4c30-115">Although the IDL file is a standard part of RPC, Microsoft has enhanced it to extend its functionality to support custom COM interfaces.</span></span> <span data-ttu-id="d4c30-116">Компилятор язык MIDL (MIDL) использует IDL-файл, описывающий пользовательский интерфейс, для создания нескольких файлов, обсуждаемых в разделе [Создание и регистрация библиотеки DLL прокси](building-and-registering-a-proxy-dll.md).</span><span class="sxs-lookup"><span data-stu-id="d4c30-116">The Microsoft Interface Definition Language (MIDL) compiler uses the IDL file that describes your custom interface to generate several files discussed in [Building and Registering a Proxy DLL](building-and-registering-a-proxy-dll.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4c30-117">См. также</span><span class="sxs-lookup"><span data-stu-id="d4c30-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4c30-118">Канал</span><span class="sxs-lookup"><span data-stu-id="d4c30-118">Channel</span></span>](channel.md)
</dt> <dt>

[<span data-ttu-id="d4c30-119">Обмен данными между объектами</span><span class="sxs-lookup"><span data-stu-id="d4c30-119">Inter-Object Communication</span></span>](inter-object-communication.md)
</dt> <dt>

[<span data-ttu-id="d4c30-120">Сведения о маршалировании</span><span class="sxs-lookup"><span data-stu-id="d4c30-120">Marshaling Details</span></span>](marshaling-details.md)
</dt> <dt>

[<span data-ttu-id="d4c30-121">Прокси</span><span class="sxs-lookup"><span data-stu-id="d4c30-121">Proxy</span></span>](proxy.md)
</dt> <dt>

[<span data-ttu-id="d4c30-122">Заглушка</span><span class="sxs-lookup"><span data-stu-id="d4c30-122">Stub</span></span>](stub.md)
</dt> </dl>

 

 




