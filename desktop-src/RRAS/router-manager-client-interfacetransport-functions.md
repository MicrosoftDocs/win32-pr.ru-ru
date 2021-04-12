---
title: Функции клиента диспетчера маршрутизатора (Интерфацетранспорт)
description: Используйте следующие функции для администрирования клиентов, таких как протоколы маршрутизации, на определенных интерфейсах. Эти функции также позволяют разработчикам считывать и записывать сведения об интерфейсах клиентов маршрутизатора, например протоколы маршрутизации.
ms.assetid: f7aa1b3a-465b-4305-b85e-4246a092b8aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea26224004c6cf80cc3df94496bc10747ab2255
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332803"
---
# <a name="router-manager-client-interfacetransport-functions"></a><span data-ttu-id="a6f4e-104">Функции клиента диспетчера маршрутизатора (Интерфацетранспорт)</span><span class="sxs-lookup"><span data-stu-id="a6f4e-104">Router Manager Client (InterfaceTransport) Functions</span></span>

<span data-ttu-id="a6f4e-105">Используйте следующие функции для администрирования клиентов, таких как протоколы маршрутизации, на определенных интерфейсах.</span><span class="sxs-lookup"><span data-stu-id="a6f4e-105">Use the following functions to administer clients, such as routing protocols, on particular interfaces.</span></span> <span data-ttu-id="a6f4e-106">Эти функции также позволяют разработчикам считывать и записывать сведения об интерфейсах клиентов маршрутизатора, например протоколы маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="a6f4e-106">These functions also allow a developer to read and write interface-specific information for router clients, such as routing protocols.</span></span>



| <span data-ttu-id="a6f4e-107">Функция администрирования</span><span class="sxs-lookup"><span data-stu-id="a6f4e-107">Administration function</span></span>                                                        | <span data-ttu-id="a6f4e-108">Функция настройки</span><span class="sxs-lookup"><span data-stu-id="a6f4e-108">Configuration function</span></span>                                                               |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="a6f4e-109">**мпрадмининтерфацетранспортадд**</span><span class="sxs-lookup"><span data-stu-id="a6f4e-109">**MprAdminInterfaceTransportAdd**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportadd)         | [<span data-ttu-id="a6f4e-110">**мпрконфигинтерфацетранспортадд**</span><span class="sxs-lookup"><span data-stu-id="a6f4e-110">**MprConfigInterfaceTransportAdd**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportadd)             |
| [<span data-ttu-id="a6f4e-111">**мпрадмининтерфацетранспортремове**</span><span class="sxs-lookup"><span data-stu-id="a6f4e-111">**MprAdminInterfaceTransportRemove**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportremove)   | [<span data-ttu-id="a6f4e-112">**мпрконфигинтерфацетранспортремове**</span><span class="sxs-lookup"><span data-stu-id="a6f4e-112">**MprConfigInterfaceTransportRemove**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportremove)       |
| [<span data-ttu-id="a6f4e-113">**мпрадмининтерфацетранспортжетинфо**</span><span class="sxs-lookup"><span data-stu-id="a6f4e-113">**MprAdminInterfaceTransportGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) | [<span data-ttu-id="a6f4e-114">**мпрконфигинтерфацетранспортжетинфо**</span><span class="sxs-lookup"><span data-stu-id="a6f4e-114">**MprConfigInterfaceTransportGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo)     |
| [<span data-ttu-id="a6f4e-115">**мпрадмининтерфацетранспортсетинфо**</span><span class="sxs-lookup"><span data-stu-id="a6f4e-115">**MprAdminInterfaceTransportSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) | [<span data-ttu-id="a6f4e-116">**мпрконфигинтерфацетранспортсетинфо**</span><span class="sxs-lookup"><span data-stu-id="a6f4e-116">**MprConfigInterfaceTransportSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportsetinfo)     |
| <span data-ttu-id="a6f4e-117">Нет функции администрирования</span><span class="sxs-lookup"><span data-stu-id="a6f4e-117">No administration function</span></span>                                                     | [<span data-ttu-id="a6f4e-118">**мпрконфигинтерфацетранспортенум**</span><span class="sxs-lookup"><span data-stu-id="a6f4e-118">**MprConfigInterfaceTransportEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportenum)           |
| <span data-ttu-id="a6f4e-119">Нет функции администрирования</span><span class="sxs-lookup"><span data-stu-id="a6f4e-119">No administration function</span></span>                                                     | [<span data-ttu-id="a6f4e-120">**мпрконфигинтерфацетранспортжесандле**</span><span class="sxs-lookup"><span data-stu-id="a6f4e-120">**MprConfigInterfaceTransportGetHandle**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgethandle) |



 

 

 




