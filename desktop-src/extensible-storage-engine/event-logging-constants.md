---
description: 'Дополнительные сведения: константы ведения журнала событий'
title: Константы ведения журнала событий
TOCTitle: Event Logging Constants
ms:assetid: d24603a9-a9be-4700-bc20-4e3f0661e741
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294101(v=EXCHG.10)
ms:contentKeyID: 32765716
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e7ada5c71b603bf530c62d9f3af238131e305e42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702430"
---
# <a name="event-logging-constants"></a><span data-ttu-id="5b115-103">Константы ведения журнала событий</span><span class="sxs-lookup"><span data-stu-id="5b115-103">Event Logging Constants</span></span>


<span data-ttu-id="5b115-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5b115-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="event-logging-constants"></a><span data-ttu-id="5b115-105">Константы ведения журнала событий</span><span class="sxs-lookup"><span data-stu-id="5b115-105">Event Logging Constants</span></span>

<span data-ttu-id="5b115-106">Следующие константы указывают уровень детализации для сообщений журнала событий для системного параметра [JET_ParamEventLoggingLevel](./event-log-parameters.md) .</span><span class="sxs-lookup"><span data-stu-id="5b115-106">The following constants indicate the detail level for event log messages for the [JET_ParamEventLoggingLevel](./event-log-parameters.md) system parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5b115-107">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="5b115-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="5b115-108">Описание</span><span class="sxs-lookup"><span data-stu-id="5b115-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5b115-109">JET_EventLoggingDisable</span><span class="sxs-lookup"><span data-stu-id="5b115-109">JET_EventLoggingDisable</span></span><br />
<span data-ttu-id="5b115-110">0</span><span class="sxs-lookup"><span data-stu-id="5b115-110">0</span></span></p></td>
<td><p><span data-ttu-id="5b115-111">Отключает ведение журнала событий.</span><span class="sxs-lookup"><span data-stu-id="5b115-111">Disables event logging.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b115-112">JET_EventLoggingLevelMax</span><span class="sxs-lookup"><span data-stu-id="5b115-112">JET_EventLoggingLevelMax</span></span><br />
<span data-ttu-id="5b115-113">100</span><span class="sxs-lookup"><span data-stu-id="5b115-113">100</span></span></p></td>
<td><p><span data-ttu-id="5b115-114">Задает максимальный уровень, используемый для журналов событий, который в настоящее время 100 символов.</span><span class="sxs-lookup"><span data-stu-id="5b115-114">Sets the maximum level to use for event logs, which is currently 100 characters.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="5b115-115">Требования</span><span class="sxs-lookup"><span data-stu-id="5b115-115">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5b115-116"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="5b115-116"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5b115-117">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="5b115-117">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b115-118"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="5b115-118"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5b115-119">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="5b115-119">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b115-120"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="5b115-120"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5b115-121">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="5b115-121">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="5b115-122">См. также:</span><span class="sxs-lookup"><span data-stu-id="5b115-122">See Also</span></span>

[<span data-ttu-id="5b115-123">Параметры журнала событий</span><span class="sxs-lookup"><span data-stu-id="5b115-123">Event Log Parameters</span></span>](./event-log-parameters.md)
