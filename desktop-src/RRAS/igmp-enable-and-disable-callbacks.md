---
title: Включение и отключение обратных вызовов IGMP
description: Диспетчер групп многоадресной рассылки использует два обратных вызова для протокола IGMP для координации изменений в правах владения интерфейсом от IGMP к протоколу маршрутизации и от протокола маршрутизации к IGMP.
ms.assetid: e4b2be85-6c67-4801-9905-eb1990d4bbb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aa58e9b65c67ac5946f5f5e54e611565e59d8c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890944"
---
# <a name="igmp-enable-and-disable-callbacks"></a><span data-ttu-id="977fb-103">Включение и отключение обратных вызовов IGMP</span><span class="sxs-lookup"><span data-stu-id="977fb-103">IGMP Enable and Disable Callbacks</span></span>

<span data-ttu-id="977fb-104">Диспетчер групп многоадресной рассылки использует два обратных вызова для протокола IGMP для координации изменений в правах владения интерфейсом от IGMP к протоколу маршрутизации и от протокола маршрутизации к IGMP.</span><span class="sxs-lookup"><span data-stu-id="977fb-104">The multicast group manager uses two callbacks to IGMP to coordinate changes in interface ownership from IGMP to a routing protocol, and from a routing protocol to IGMP.</span></span> <span data-ttu-id="977fb-105">Обратные вызовы позволяют IGMP сосуществовать в интерфейсе с другим протоколом маршрутизации, например ДВМРП.</span><span class="sxs-lookup"><span data-stu-id="977fb-105">The callbacks enable IGMP to coexist on an interface with another routing protocol, such as DVMRP.</span></span>

<span data-ttu-id="977fb-106">После изменения владельца интерфейса Диспетчер групп многоадресной рассылки сначала вызывает обратный вызов [**\_ \_ \_ обратного вызова пмгм Disable IGMP**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback) .</span><span class="sxs-lookup"><span data-stu-id="977fb-106">After the ownership of an interface changes, the multicast group manager first invokes the [**PMGM\_DISABLE\_IGMP\_CALLBACK**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback) callback.</span></span> <span data-ttu-id="977fb-107">IGMP должен прерывать Добавление и удаление членства в группах на указанном интерфейсе до тех пор, пока диспетчер групп многоадресной рассылки не вызовет обратный вызов [**\_ \_ \_ обратного вызова IGMP пмгм**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) .</span><span class="sxs-lookup"><span data-stu-id="977fb-107">IGMP must stop adding and deleting group memberships on the specified interface until the multicast group manager invokes the [**PMGM\_ENABLE\_IGMP\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) callback.</span></span>

<span data-ttu-id="977fb-108">Диспетчер групп многоадресной рассылки вызывает обратный вызов [**пмгм \_ включения \_ \_ обратного вызова IGMP**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) после изменения прав на владение интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="977fb-108">The multicast group manager invokes the [**PMGM\_ENABLE\_IGMP\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) callback after the change of interface ownership is complete.</span></span>

 

 