---
title: Функции интерфейса маршрутизатора
description: Используйте следующие функции для администрирования интерфейсов на маршрутизаторе.
ms.assetid: e988753e-908a-4c42-aad3-dd9f641c90a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a5318eedfbc3a04c13549012fda3bd4d93b4d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328232"
---
# <a name="router-interface-functions"></a><span data-ttu-id="b0561-103">Функции интерфейса маршрутизатора</span><span class="sxs-lookup"><span data-stu-id="b0561-103">Router Interface Functions</span></span>

<span data-ttu-id="b0561-104">Используйте следующие функции для администрирования интерфейсов на маршрутизаторе.</span><span class="sxs-lookup"><span data-stu-id="b0561-104">Use the following functions to administer interfaces on the router.</span></span>



| <span data-ttu-id="b0561-105">Функция администрирования</span><span class="sxs-lookup"><span data-stu-id="b0561-105">Administration Function</span></span>                                          | <span data-ttu-id="b0561-106">Функция настройки</span><span class="sxs-lookup"><span data-stu-id="b0561-106">Configuration Function</span></span>                                             |
|------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="b0561-107">**мпрадмининтерфацекреате**</span><span class="sxs-lookup"><span data-stu-id="b0561-107">**MprAdminInterfaceCreate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate)       | [<span data-ttu-id="b0561-108">**мпрконфигинтерфацекреате**</span><span class="sxs-lookup"><span data-stu-id="b0561-108">**MprConfigInterfaceCreate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacecreate)       |
| [<span data-ttu-id="b0561-109">**мпрадмининтерфацеделете**</span><span class="sxs-lookup"><span data-stu-id="b0561-109">**MprAdminInterfaceDelete**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete)       | [<span data-ttu-id="b0561-110">**мпрконфигинтерфацеделете**</span><span class="sxs-lookup"><span data-stu-id="b0561-110">**MprConfigInterfaceDelete**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacedelete)       |
| [<span data-ttu-id="b0561-111">**мпрадмининтерфацеенум**</span><span class="sxs-lookup"><span data-stu-id="b0561-111">**MprAdminInterfaceEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfaceenum)           | [<span data-ttu-id="b0561-112">**мпрконфигинтерфацеенум**</span><span class="sxs-lookup"><span data-stu-id="b0561-112">**MprConfigInterfaceEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfaceenum)           |
| [<span data-ttu-id="b0561-113">**мпрадмининтерфацежесандле**</span><span class="sxs-lookup"><span data-stu-id="b0561-113">**MprAdminInterfaceGetHandle**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacegethandle) | [<span data-ttu-id="b0561-114">**мпрконфигинтерфацежесандле**</span><span class="sxs-lookup"><span data-stu-id="b0561-114">**MprConfigInterfaceGetHandle**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacegethandle) |
| [<span data-ttu-id="b0561-115">**мпрадмининтерфацежетинфо**</span><span class="sxs-lookup"><span data-stu-id="b0561-115">**MprAdminInterfaceGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacegetinfo)     | [<span data-ttu-id="b0561-116">**мпрконфигинтерфацежетинфо**</span><span class="sxs-lookup"><span data-stu-id="b0561-116">**MprConfigInterfaceGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacegetinfo)     |
| [<span data-ttu-id="b0561-117">**мпрадмининтерфацесетинфо**</span><span class="sxs-lookup"><span data-stu-id="b0561-117">**MprAdminInterfaceSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo)     | [<span data-ttu-id="b0561-118">**мпрконфигинтерфацесетинфо**</span><span class="sxs-lookup"><span data-stu-id="b0561-118">**MprConfigInterfaceSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo)     |



 

<span data-ttu-id="b0561-119">Эти функции влияют на сами интерфейсы, а не на клиенты, работающие в интерфейсах.</span><span class="sxs-lookup"><span data-stu-id="b0561-119">These functions affect the interfaces themselves, not clients running on the interfaces.</span></span> <span data-ttu-id="b0561-120">По этой причине ни одна из функций не требует от вызывающей стороны указания конкретного транспорта (IP или IPX); Хотя клиенты (например, протоколы маршрутизации) связаны с определенными транспортами, сами интерфейсы не являются.</span><span class="sxs-lookup"><span data-stu-id="b0561-120">For this reason, none of the functions require the caller to specify a particular transport (IP or IPX); although clients (such as routing protocols) are associated with particular transports, the interfaces themselves are not.</span></span>

<span data-ttu-id="b0561-121">Эти функции непосредственно обрабатываются с помощью DIM.</span><span class="sxs-lookup"><span data-stu-id="b0561-121">These functions are handled directly by DIM.</span></span> <span data-ttu-id="b0561-122">Они не используют диспетчеры маршрутизаторов.</span><span class="sxs-lookup"><span data-stu-id="b0561-122">They do not utilize the router managers.</span></span>

<span data-ttu-id="b0561-123">Функции [**мпрадмининтерфацекреате**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate) и [**мпрадмининтерфацеделете**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete) не могут создавать или удалять интерфейсы локальной сети.</span><span class="sxs-lookup"><span data-stu-id="b0561-123">The [**MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate) and [**MprAdminInterfaceDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete) functions cannot create or delete LAN interfaces.</span></span> <span data-ttu-id="b0561-124">Они могут только создавать или удалять интерфейсы вызова по требованию.</span><span class="sxs-lookup"><span data-stu-id="b0561-124">They can only create or delete demand-dial interfaces.</span></span> <span data-ttu-id="b0561-125">Список типов интерфейсов см. в разделе [**\_ \_ тип интерфейса маршрутизатора**](/windows/desktop/api/Mprapi/ne-mprapi-router_interface_type) .</span><span class="sxs-lookup"><span data-stu-id="b0561-125">See [**ROUTER\_INTERFACE\_TYPE**](/windows/desktop/api/Mprapi/ne-mprapi-router_interface_type) for a list of interface types.</span></span>

 

 




