---
description: Операционная система Windows накапливает набор операционных статистических данных для рабочих станций и серверов с момента запуска службы рабочей станции или сервера.
ms.assetid: 4e0217bf-7550-40a2-b47c-8e898a586005
title: Статистические функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce62e12f3c4894ba86ff5e5aaaa38801d272195c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674111"
---
# <a name="statistics-functions"></a><span data-ttu-id="2f004-103">Статистические функции</span><span class="sxs-lookup"><span data-stu-id="2f004-103">Statistics Functions</span></span>

<span data-ttu-id="2f004-104">Операционная система Windows накапливает набор операционных статистических данных для рабочих станций и серверов с момента запуска службы рабочей станции или сервера.</span><span class="sxs-lookup"><span data-stu-id="2f004-104">The Windows operating system accumulates a set of operating statistics for workstations and servers from the time that the workstation or server service is started.</span></span> <span data-ttu-id="2f004-105">Чтобы получить эти статистические данные, можно вызвать следующую функцию статистики управления сетью.</span><span class="sxs-lookup"><span data-stu-id="2f004-105">To retrieve these statistics, you can call the following network management statistics function.</span></span>



| <span data-ttu-id="2f004-106">Функция</span><span class="sxs-lookup"><span data-stu-id="2f004-106">Function</span></span>                                     | <span data-ttu-id="2f004-107">Описание</span><span class="sxs-lookup"><span data-stu-id="2f004-107">Description</span></span>                                                                                 |
|----------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f004-108">**нетстатистиксжет**</span><span class="sxs-lookup"><span data-stu-id="2f004-108">**NetStatisticsGet**</span></span>](/windows/desktop/api/Lmstats/nf-lmstats-netstatisticsget) | <span data-ttu-id="2f004-109">Извлекает операционную статистику для службы. поддерживает службы рабочей станции и сервера.</span><span class="sxs-lookup"><span data-stu-id="2f004-109">Retrieves operating statistics for a service; supports the workstation and server services.</span></span> |



 

<span data-ttu-id="2f004-110">Функция **нетстатистиксжет** возвращает структуру [**stat \_ Workstation \_ 0**](/windows/win32/api/lmstats/ns-lmstats-stat_workstation_0-r1) при запросе статистики рабочей станции. функция возвращает структуру [**\_ сервера stat \_ 0**](/windows/desktop/api/Lmstats/ns-lmstats-stat_server_0) при запросе статистики сервера.</span><span class="sxs-lookup"><span data-stu-id="2f004-110">The **NetStatisticsGet** function returns a [**STAT\_WORKSTATION\_0**](/windows/win32/api/lmstats/ns-lmstats-stat_workstation_0-r1) structure when workstation statistics are requested; the function returns a [**STAT\_SERVER\_0**](/windows/desktop/api/Lmstats/ns-lmstats-stat_server_0) structure when server statistics are requested.</span></span>

 

 



