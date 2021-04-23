---
title: API поставщика протокол удаленного рабочего стола
description: API поставщика протокол удаленного рабочего стола используется для создания протокола, обеспечивающего обмен данными между службы удаленных рабочих столовной службой и несколькими клиентами.
ms.assetid: dd14c569-195e-460e-a1c3-2a74d0f49ff5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95aed1c6866f3078c3761ad8ec631ef23b43a9ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986065"
---
# <a name="remote-desktop-protocol-provider-api"></a><span data-ttu-id="3fc6c-103">API поставщика протокол удаленного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="3fc6c-103">Remote Desktop Protocol Provider API</span></span>

<span data-ttu-id="3fc6c-104">API поставщика протокол удаленного рабочего стола используется для создания протокола, обеспечивающего обмен данными между службы удаленных рабочих столовной службой и несколькими клиентами.</span><span class="sxs-lookup"><span data-stu-id="3fc6c-104">You use the Remote Desktop Protocol Provider API to create a protocol to provide communication between the Remote Desktop Services service and multiple clients.</span></span>

<span data-ttu-id="3fc6c-105">При загрузке Windows Server запускается служба службы удаленных рабочих столов (также называемая диспетчером удаленных подключений (RCM)).</span><span class="sxs-lookup"><span data-stu-id="3fc6c-105">When Windows Server loads, the Remote Desktop Services service (also known as Remote Connection Manager (RCM)) starts.</span></span> <span data-ttu-id="3fc6c-106">Служба также запускает объекты прослушивателя для поставщиков протокол удаленного рабочего стола, которые, в свою очередь, прослушивают подключения клиентов.</span><span class="sxs-lookup"><span data-stu-id="3fc6c-106">The service also starts listener objects for the Remote Desktop Protocol Providers that in turn listen for client connections.</span></span> <span data-ttu-id="3fc6c-107">Служба и поставщики протоколов — это объекты пользовательского режима, взаимодействующие с помощью интерфейсов API, которые обсуждаются в этой документации.</span><span class="sxs-lookup"><span data-stu-id="3fc6c-107">The service and the protocol providers are user-mode objects that communicate by using the APIs discussed in this documentation.</span></span> <span data-ttu-id="3fc6c-108">Поставщики протоколов могут взаимодействовать с драйверами в режиме ядра с помощью элементов управления вводом-выводом (IOCTL).</span><span class="sxs-lookup"><span data-stu-id="3fc6c-108">The protocol providers can communicate with kernel-mode drivers by using input/output controls (IOCTLs).</span></span> <span data-ttu-id="3fc6c-109">Это показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="3fc6c-109">This is shown in the following illustration.</span></span>

![Архитектура API настраиваемого протокола](images/protocol-architecture.png)

<span data-ttu-id="3fc6c-111">Корпорация Майкрософт реализовала протокол удаленного рабочего стола (RDP) для обеспечения взаимодействия между службой службы удаленных рабочих столов и клиентскими подключениями.</span><span class="sxs-lookup"><span data-stu-id="3fc6c-111">Microsoft has implemented the Remote Desktop Protocol (RDP) to provide communication between the Remote Desktop Services service and client connections.</span></span> <span data-ttu-id="3fc6c-112">Вы можете создать собственный протокол с помощью интерфейсов, структур, объединений и типов перечисления, которые составляют API поставщика протокол удаленного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="3fc6c-112">You can create your own protocol by using the interfaces, structures, unions, and enumeration types that make up the Remote Desktop Protocol Provider API.</span></span> <span data-ttu-id="3fc6c-113">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="3fc6c-113">For more information, see the following topics.</span></span>

<dl> <dt>

[<span data-ttu-id="3fc6c-114">Создание поставщика протокол удаленного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="3fc6c-114">Creating a Remote Desktop Protocol Provider</span></span>](creating-a-custom-remote-protocol.md)
</dt> <dd>

<span data-ttu-id="3fc6c-115">Сведения о создании поставщика протокол удаленного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="3fc6c-115">Information about creating a Remote Desktop Protocol Provider.</span></span> <span data-ttu-id="3fc6c-116">Диспетчер протоколов реализуется как сервер COM и регистрируется в расположении, которое выполняется при запуске службы службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="3fc6c-116">The protocol manager is implemented as a COM server and registered in a location searched when the Remote Desktop Services service starts.</span></span>

</dd> <dt>

[<span data-ttu-id="3fc6c-117">Справочник по поставщику протокол удаленного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="3fc6c-117">Remote Desktop Protocol Provider reference</span></span>](custom-remote-protocol-reference.md)
</dt> <dd>

<span data-ttu-id="3fc6c-118">Содержит интерфейсы, структуры, объединения и типы перечислений, позволяющие создавать пользовательские протокол удаленного рабочего стола (RDP).</span><span class="sxs-lookup"><span data-stu-id="3fc6c-118">Contains interfaces, structures, unions, and enumeration types that enable you to create a custom Remote Desktop Protocol (RDP).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="3fc6c-119">См. также</span><span class="sxs-lookup"><span data-stu-id="3fc6c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fc6c-120">О службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="3fc6c-120">About Remote Desktop Services</span></span>](about-terminal-services.md)
</dt> </dl>

 

 




