---
title: Справочник по API вспомогательной функции маршрутизации подключения по требованию
description: В следующих разделах приводятся сведения о вспомогательной службе маршрутизации подключений по требованию.
ms.assetid: 39AFFD16-488E-4CA3-9161-9424F0D15948
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3049c62d7784af6430e8b93240ec79464b098043
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104133038"
---
# <a name="on-demand-connection-routing-helper-api-reference"></a><span data-ttu-id="9241e-103">Справочник по API вспомогательной функции маршрутизации подключения по требованию</span><span class="sxs-lookup"><span data-stu-id="9241e-103">On Demand Connection Routing Helper API reference</span></span>

<span data-ttu-id="9241e-104">В следующих разделах приводятся сведения о вспомогательной службе маршрутизации подключений по требованию.</span><span class="sxs-lookup"><span data-stu-id="9241e-104">The following topics provide details for the On Demand Connection Routing Helper.</span></span>



| <span data-ttu-id="9241e-105">Справочник</span><span class="sxs-lookup"><span data-stu-id="9241e-105">Reference</span></span>                                                                          | <span data-ttu-id="9241e-106">Описание</span><span class="sxs-lookup"><span data-stu-id="9241e-106">Description</span></span>                                                                                                                                                                 |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9241e-107">**ондеманджетраутингхинт**</span><span class="sxs-lookup"><span data-stu-id="9241e-107">**OnDemandGetRoutingHint**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandgetroutinghint)                           | <span data-ttu-id="9241e-108">Найдите место назначения в кэше запросов маршрутов и, если найдено совпадение, возвращает соответствующий идентификатор интерфейса.</span><span class="sxs-lookup"><span data-stu-id="9241e-108">Look up a destination in the Route Request cache and, if a match is found, returns the corresponding Interface ID.</span></span><br/>                                               |
| [<span data-ttu-id="9241e-109">**ондемандрегистернотификатион**</span><span class="sxs-lookup"><span data-stu-id="9241e-109">**OnDemandRegisterNotification**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandregisternotification)               | <span data-ttu-id="9241e-110">Регистрация для получения уведомлений при изменении кэша запросов маршрутов.</span><span class="sxs-lookup"><span data-stu-id="9241e-110">Register to be notified when the Route Requests cache is modified.</span></span><br/>                                                                                               |
| [<span data-ttu-id="9241e-111">**ондемандунрегистернотификатион**</span><span class="sxs-lookup"><span data-stu-id="9241e-111">**OnDemandUnregisterNotification**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandunregisternotification)           | <span data-ttu-id="9241e-112">Отмените регистрацию для получения уведомлений и очистите ресурсы.</span><span class="sxs-lookup"><span data-stu-id="9241e-112">Unregister for notifications and clean up resources.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="9241e-113">**\_контекст интерфейса \_ net**</span><span class="sxs-lookup"><span data-stu-id="9241e-113">**NET\_INTERFACE\_CONTEXT**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context)                           | <span data-ttu-id="9241e-114">Контекст интерфейса, который является частью структуры [**\_ \_ \_ таблицы контекста интерфейса NET**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table) .</span><span class="sxs-lookup"><span data-stu-id="9241e-114">The interface context that is part of the [**NET\_INTERFACE\_CONTEXT\_TABLE**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table) structure.</span></span><br/>                                       |
| [<span data-ttu-id="9241e-115">**\_ \_ Таблица контекста интерфейса \_ net**</span><span class="sxs-lookup"><span data-stu-id="9241e-115">**NET\_INTERFACE\_CONTEXT\_TABLE**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table)              | <span data-ttu-id="9241e-116">Таблица структур [**\_ \_ контекста интерфейса NET**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context) .</span><span class="sxs-lookup"><span data-stu-id="9241e-116">The table of [**NET\_INTERFACE\_CONTEXT**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context) structures.</span></span><br/>                                                                                |
| [<span data-ttu-id="9241e-117">**жетинтерфацеконтексттаблефорхостнаме**</span><span class="sxs-lookup"><span data-stu-id="9241e-117">**GetInterfaceContextTableForHostName**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) | <span data-ttu-id="9241e-118">Эта функция получает таблицу контекста интерфейса для заданного имени узла и фильтра профиля подключения.</span><span class="sxs-lookup"><span data-stu-id="9241e-118">This function retrieves an interface context table for the given hostname and connection profile filter.</span></span><br/>                                                         |
| [<span data-ttu-id="9241e-119">**фриинтерфацеконтексттабле**</span><span class="sxs-lookup"><span data-stu-id="9241e-119">**FreeInterfaceContextTable**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-freeinterfacecontexttable)                     | <span data-ttu-id="9241e-120">Эта функция освобождает таблицу контекста интерфейса, полученную с помощью функции [**жетинтерфацеконтексттаблефорхостнаме**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) .</span><span class="sxs-lookup"><span data-stu-id="9241e-120">This function frees the interface context table retrieved using the [**GetInterfaceContextTableForHostName**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) function.</span></span><br/> |



 

 

 





