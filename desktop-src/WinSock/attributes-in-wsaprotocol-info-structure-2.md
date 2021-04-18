---
description: XP1 \_ поддерживает \_ MULTIPOINT, XP1 \_ MultiPoint \_ \_ плоскость управления и \_ \_ \_ Параметры атрибутов плоскости данных XP1 MultiPoint в структуре сведений Winsock всапротокол \_ .
ms.assetid: 62f5b8b0-a404-49d1-b163-026f79a46845
title: Атрибуты в структуре WSAPROTOCOL_INFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e39ea2905da3228860d4fe22f5a0f0d954ce0624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711049"
---
# <a name="attributes-in-wsaprotocol_info-structure"></a><span data-ttu-id="e7928-103">Атрибуты в \_ структуре сведений всапротокол</span><span class="sxs-lookup"><span data-stu-id="e7928-103">Attributes in WSAPROTOCOL\_INFO Structure</span></span>

<span data-ttu-id="e7928-104">В соответствии с описанной выше классификацией для различения схем, используемых в элементах управления и плоскостей данных, используются три параметра атрибутов в структуре [**всапротокол \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .</span><span class="sxs-lookup"><span data-stu-id="e7928-104">In support of the taxonomy described above, three attribute parameters in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure are used to distinguish the schemes used in the control and data planes respectively:</span></span>

-   <span data-ttu-id="e7928-105">XP1 \_ поддерживает \_ MultiPoint со значением 1 указывает, что эта запись протокола поддерживает обмен данными по MULTIPOINT, а следующие два параметра имеют смысл.</span><span class="sxs-lookup"><span data-stu-id="e7928-105">XP1\_SUPPORT\_MULTIPOINT with a value of 1 indicates this protocol entry supports multipoint communications, and that the following two parameters are meaningful.</span></span>
-   <span data-ttu-id="e7928-106">XP1 \_ MULTIPOINT \_ Control \_ плоскость указывает, является ли плоскость управления корневой (значение = 1) или не является корневым (значение = 0).</span><span class="sxs-lookup"><span data-stu-id="e7928-106">XP1\_MULTIPOINT\_CONTROL\_PLANE indicates whether the control plane is rooted (value = 1) or nonrooted (value = 0).</span></span>
-   <span data-ttu-id="e7928-107">XP1 \_ MULTIPOINT \_ \_ плоскость данных указывает, является ли плоскость данных корневой (значение 1) или не является корневым (значение = 0).</span><span class="sxs-lookup"><span data-stu-id="e7928-107">XP1\_MULTIPOINT\_DATA\_PLANE indicates whether the data plane is rooted (value = 1) or nonrooted (value = 0).</span></span>

<span data-ttu-id="e7928-108">Обратите внимание, что в случае, если протокол MultiPoint поддерживал как корневой, так и некорневой плоскости данных, по одной записи для каждой из них будут отображаться две записи [**всапротокол \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .</span><span class="sxs-lookup"><span data-stu-id="e7928-108">Note that two [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entries would be present if a multipoint protocol supported both rooted and nonrooted data planes, one entry for each.</span></span>

<span data-ttu-id="e7928-109">Приложение может использовать [**всаенумпротоколс**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) , чтобы определить, поддерживается ли обмен данными MultiPoint для данного протокола, и, если да, как он поддерживается в отношении элемента управления и плоскостей данных соответственно.</span><span class="sxs-lookup"><span data-stu-id="e7928-109">The application can use [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) to discover whether multipoint communications is supported for a given protocol and, if so, how it is supported with respect to the control and data planes, respectively.</span></span>

 

 
