---
title: Атрибуты MultiPoint в WSAPROTOCOL_INFO
description: Атрибуты MultiPoint в \_ структуре сведений всапротокол включают в себя \_ XP1 support \_ MultiPoint, XP1 \_ MULTIPOINT \_ Control \_ плоскость и XP1 \_ MULTIPOINT \_ плоскость данных \_ .
ms.assetid: f1bd5aa1-e705-4eaf-9436-fed0ea03f113
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baedcd07f53db462eb090217b53d93a1a4aa8c34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809730"
---
# <a name="multipoint-attributes-in-wsaprotocol_info"></a><span data-ttu-id="dcc61-103">Атрибуты MultiPoint в WSAPROTOCOL_INFO</span><span class="sxs-lookup"><span data-stu-id="dcc61-103">Multipoint attributes in WSAPROTOCOL_INFO</span></span>

<span data-ttu-id="dcc61-104">Для различения различных схем, используемых в элементах управления и плоскостях данных, в структуре [**\_ сведений всапротокол**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) определены три параметра атрибутов.</span><span class="sxs-lookup"><span data-stu-id="dcc61-104">Three attribute parameters are defined in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure in order to distinguish the different schemes used in the control and data planes, respectively:</span></span>

-   <span data-ttu-id="dcc61-105">XP1 \_ поддерживает \_ MultiPoint со значением 1 указывает, что эта запись протокола поддерживает обмен данными по MULTIPOINT, а следующие два параметра имеют смысл.</span><span class="sxs-lookup"><span data-stu-id="dcc61-105">XP1\_SUPPORT\_MULTIPOINT with a value of 1 indicates this protocol entry supports multipoint communications, and that the following two parameters are meaningful.</span></span>
-   <span data-ttu-id="dcc61-106">XP1 \_ MULTIPOINT \_ Control \_ плоскость указывает, является ли плоскость управления корневой (значение = 1) или не является корневым (значение = 0).</span><span class="sxs-lookup"><span data-stu-id="dcc61-106">XP1\_MULTIPOINT\_CONTROL\_PLANE indicates whether the control plane is rooted (value = 1) or nonrooted (value = 0).</span></span>
-   <span data-ttu-id="dcc61-107">XP1 \_ MULTIPOINT \_ \_ плоскость данных указывает, является ли плоскость данных корневой (значение 1) или не является корневым (значение = 0).</span><span class="sxs-lookup"><span data-stu-id="dcc61-107">XP1\_MULTIPOINT\_DATA\_PLANE indicates whether the data plane is rooted (value = 1) or nonrooted (value = 0).</span></span>

<span data-ttu-id="dcc61-108">Если протокол MultiPoint поддерживал как корневой, так и некорневой плоскости данных, по одной записи для каждой из них будут отображаться две записи [**всапротокол \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .</span><span class="sxs-lookup"><span data-stu-id="dcc61-108">Two [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entries would be present if a multipoint protocol supported both rooted and nonrooted data planes, one entry for each.</span></span>

 

 
