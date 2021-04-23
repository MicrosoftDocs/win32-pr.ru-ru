---
description: Поставщик сети — это библиотека DLL, которая позволяет операционной системе Windows взаимодействовать с другими видами сетей, например Novell. Это клиент драйвера Windows Внет.
ms.assetid: d316f159-4fe3-4b78-9efc-177906875918
title: API поставщика сети
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc68184f60639a603614cbaf71631a2521012cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647537"
---
# <a name="network-provider-api"></a><span data-ttu-id="88426-104">API поставщика сети</span><span class="sxs-lookup"><span data-stu-id="88426-104">Network Provider API</span></span>

<span data-ttu-id="88426-105">Поставщик сети — это библиотека DLL, которая позволяет операционной системе Windows взаимодействовать с другими видами сетей, например Novell.</span><span class="sxs-lookup"><span data-stu-id="88426-105">A network provider is a DLL that enables the Windows operating system to interact with other kinds of networks, such as Novell.</span></span> <span data-ttu-id="88426-106">Это клиент драйвера Windows Внет.</span><span class="sxs-lookup"><span data-stu-id="88426-106">It is a client of the Windows WNet driver.</span></span> <span data-ttu-id="88426-107">Поставщик сети реализует действия, связанные с сетью, такие как создание подключения, и предоставляет общий интерфейс для Windows.</span><span class="sxs-lookup"><span data-stu-id="88426-107">A network provider implements network-specific actions, such as making a connection, and exposes a common interface to Windows.</span></span> <span data-ttu-id="88426-108">Этот интерфейс называется API поставщика сети и состоит из функций, реализованных поставщиком сети.</span><span class="sxs-lookup"><span data-stu-id="88426-108">This interface is called the Network Provider API and consists of functions implemented by the network provider.</span></span> <span data-ttu-id="88426-109">Вы можете создать библиотеку DLL поставщика сети для поддержки новых сетевых протоколов.</span><span class="sxs-lookup"><span data-stu-id="88426-109">You can create a network provider DLL to support new network protocols.</span></span>

<span data-ttu-id="88426-110">Так как каждая сеть предоставляет общий интерфейс через свой поставщик, Windows может взаимодействовать с несколькими типами сетей, не зная сведений о реализации конкретной сети.</span><span class="sxs-lookup"><span data-stu-id="88426-110">Because each network exposes a common interface through its provider, Windows can interact with several types of networks without knowing their network-specific implementation details.</span></span>

<span data-ttu-id="88426-111">[*Маршрутизатор с несколькими поставщиками*](../secgloss/m-gly.md) (MPR) обрабатывает связь со всеми различными сетевыми поставщиками в системе и предоставляет пользователю интегрированную сеть.</span><span class="sxs-lookup"><span data-stu-id="88426-111">The [*Multiple Provider Router*](../secgloss/m-gly.md) (MPR) handles communication with all of the various network providers on the system and presents an integrated network to the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88426-112">См. также</span><span class="sxs-lookup"><span data-stu-id="88426-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88426-113">Поставщики сети</span><span class="sxs-lookup"><span data-stu-id="88426-113">Network Providers</span></span>](network-providers.md)
</dt> <dt>

[<span data-ttu-id="88426-114">Диспетчер учетных данных</span><span class="sxs-lookup"><span data-stu-id="88426-114">Credential Manager</span></span>](credential-manager.md)
</dt> <dt>

[<span data-ttu-id="88426-115">Маршрутизатор с несколькими поставщиками</span><span class="sxs-lookup"><span data-stu-id="88426-115">Multiple Provider Router</span></span>](multiple-provider-router.md)
</dt> <dt>

[<span data-ttu-id="88426-116">Функции, реализованные поставщиками сети</span><span class="sxs-lookup"><span data-stu-id="88426-116">Functions Implemented by Network Providers</span></span>](functions-implemented-by-network-providers.md)
</dt> <dt>

[<span data-ttu-id="88426-117">API управления учетными данными</span><span class="sxs-lookup"><span data-stu-id="88426-117">Credential Management API</span></span>](credential-management-api.md)
</dt> <dt>

[<span data-ttu-id="88426-118">API уведомления о соединении</span><span class="sxs-lookup"><span data-stu-id="88426-118">Connection Notification API</span></span>](connection-notification-api.md)
</dt> </dl>

 

 
