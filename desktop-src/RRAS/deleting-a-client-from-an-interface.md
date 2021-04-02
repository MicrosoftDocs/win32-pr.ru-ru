---
title: Удаление клиента из интерфейса
description: Чтобы удалить клиент (например, протокол маршрутизации) из определенного интерфейса, используйте либо Мпрадмининтерфацетранспортжетинфо, либо Мпрконфигинтерфацетранспортжетинфо, чтобы получить всю информацию о клиенте для интерфейса.
ms.assetid: 22fd7233-a242-49c2-8c26-59b415c73af2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 585a37920b59f47a0c933427d7218d08a61bed9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986637"
---
# <a name="deleting-a-client-from-an-interface"></a><span data-ttu-id="84ddc-103">Удаление клиента из интерфейса</span><span class="sxs-lookup"><span data-stu-id="84ddc-103">Deleting a Client from an Interface</span></span>

<span data-ttu-id="84ddc-104">Чтобы удалить клиент (например, протокол маршрутизации) из определенного интерфейса, используйте либо [**мпрадмининтерфацетранспортжетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) , либо [**мпрконфигинтерфацетранспортжетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo) , чтобы получить всю информацию о клиенте для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="84ddc-104">To delete a client, such as a routing protocol, from a particular interface, use either [**MprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) or [**MprConfigInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo) to retrieve all the client information for the interface.</span></span> <span data-ttu-id="84ddc-105">Используйте [**мпринфоблоккремове**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockremove) , чтобы удалить блок сведений для удаляемого клиента.</span><span class="sxs-lookup"><span data-stu-id="84ddc-105">Use [**MprInfoBlockRemove**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockremove) to remove the information block for the client to be deleted.</span></span> <span data-ttu-id="84ddc-106">Затем используйте [**мпринфоблоккадд**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockadd) , чтобы добавить блок нулевой длины для удаляемого клиента.</span><span class="sxs-lookup"><span data-stu-id="84ddc-106">Then use [**MprInfoBlockAdd**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockadd) to add a zero-length block for the client to be deleted.</span></span> <span data-ttu-id="84ddc-107">Наконец, используйте [**мпрадмининтерфацетранспортсетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) или [**мпрконфигинтерфацетранспортсетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportsetinfo) , чтобы сохранить данные обратно на работающем маршрутизаторе или в реестре.</span><span class="sxs-lookup"><span data-stu-id="84ddc-107">Finally, use [**MprAdminInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) or [**MprConfigInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportsetinfo) to save the information back to either the running router or the registry.</span></span>

<span data-ttu-id="84ddc-108">Если Диспетчер маршрутизации получает для клиента блок сведений об нулевой длине интерфейса, он знает, что этот клиент будет удален из интерфейса.</span><span class="sxs-lookup"><span data-stu-id="84ddc-108">If the router manager receives a zero-length interface information block for a client, it knows to delete that client from the interface.</span></span> <span data-ttu-id="84ddc-109">Диспетчер маршрутизатора удаляет клиент, вызывая реализацию [**делетеинтерфаце**](/windows/desktop/api/Routprot/nc-routprot-pdelete_interface)клиента.</span><span class="sxs-lookup"><span data-stu-id="84ddc-109">The router manager deletes the client by calling the client's implementation of [**DeleteInterface**](/windows/desktop/api/Routprot/nc-routprot-pdelete_interface).</span></span> <span data-ttu-id="84ddc-110">Обратите внимание на важное различие между передачей информационного заголовка, который не содержит информационного блока для клиента, и передачи заголовка данных, содержащего информационный блок нулевой длины для клиента.</span><span class="sxs-lookup"><span data-stu-id="84ddc-110">Note the important distinction between passing an information header that does not contain an information block for a client, and passing an information header that contains a zero-length information block for the client.</span></span> <span data-ttu-id="84ddc-111">В первом случае диспетчер маршрутизатора не предпринимает никаких действий с клиентом.</span><span class="sxs-lookup"><span data-stu-id="84ddc-111">In the first case, the router manager takes no action with respect to the client.</span></span> <span data-ttu-id="84ddc-112">Во втором случае диспетчер маршрутизатора удаляет клиент из интерфейса.</span><span class="sxs-lookup"><span data-stu-id="84ddc-112">In the second case, the router manager deletes the client from the interface.</span></span>

 

 




