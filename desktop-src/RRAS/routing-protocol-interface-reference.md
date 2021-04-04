---
title: Справочник по интерфейсу протокола маршрутизации
description: В этой документации описываются функции и структуры, используемые для реализации протокола маршрутизации в виде библиотеки DLL пользовательского режима.
ms.assetid: 0429f5ca-6574-48f5-85ab-70b4677ca539
keywords:
- RRAS службы маршрутизации и удаленного доступа, интерфейс протокола маршрутизации, Справочник
- Интерфейс протокола маршрутизации RRAS, Справочник
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9341dd8dbd304da84fd675aee92e378a44271056
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888332"
---
# <a name="routing-protocol-interface-reference"></a><span data-ttu-id="01f00-105">Справочник по интерфейсу протокола маршрутизации</span><span class="sxs-lookup"><span data-stu-id="01f00-105">Routing Protocol Interface Reference</span></span>

<span data-ttu-id="01f00-106">В этой документации описываются функции и структуры, используемые для реализации протокола маршрутизации в виде библиотеки DLL пользовательского режима.</span><span class="sxs-lookup"><span data-stu-id="01f00-106">This documentation describes the functions and structures that are used to implement a routing protocol as a user-mode DLL.</span></span>

<span data-ttu-id="01f00-107">MPR50 должен быть определен в файле make для протокола маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="01f00-107">MPR50 should be defined in the make file for the routing protocol.</span></span>

<span data-ttu-id="01f00-108">Макрос **\_ - \_ Привязка sizeof (x)** определяет размер в байтах структуры [**\_ \_ \_ сведений о привязке IP-адаптера**](/windows/desktop/api/Routprot/ns-routprot-ip_adapter_binding_info) , которая содержит количество IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="01f00-108">The **SIZEOF\_IP\_BINDING(x)** macro computes the size, in bytes, of an [**IP\_ADAPTER\_BINDING\_INFO**](/windows/desktop/api/Routprot/ns-routprot-ip_adapter_binding_info) structure that contains the number of IP addresses.</span></span>

<span data-ttu-id="01f00-109">Эти справочные элементы описаны в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="01f00-109">These reference elements are described in the following topics:</span></span>

-   [<span data-ttu-id="01f00-110">Функции интерфейса протокола маршрутизации</span><span class="sxs-lookup"><span data-stu-id="01f00-110">Routing Protocol Interface Functions</span></span>](routing-protocol-interface-functions.md)
-   [<span data-ttu-id="01f00-111">Структуры интерфейса протокола маршрутизации</span><span class="sxs-lookup"><span data-stu-id="01f00-111">Routing Protocol Interface Structures</span></span>](routing-protocol-interface-structures.md)
-   [<span data-ttu-id="01f00-112">Управление таблицами службы IPX</span><span class="sxs-lookup"><span data-stu-id="01f00-112">IPX Service Table Management</span></span>](ipx-service-table-management.md)

 

 




