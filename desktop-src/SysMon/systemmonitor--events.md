---
title: События Системмонитор
description: Класс Системмонитор содержит следующие события.
ms.assetid: 64d9befd-5ea0-4888-b0fb-cff889f1d188
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 94247cf81fcaf57f373c731cd4eaf06a3ca897ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661481"
---
# <a name="systemmonitor-events"></a><span data-ttu-id="a4d84-103">События Системмонитор</span><span class="sxs-lookup"><span data-stu-id="a4d84-103">SystemMonitor Events</span></span>

<span data-ttu-id="a4d84-104">Класс [**системмонитор**](systemmonitor.md) имеет следующие события:</span><span class="sxs-lookup"><span data-stu-id="a4d84-104">The [**SystemMonitor**](systemmonitor.md) class has the following events:</span></span>

-   [<span data-ttu-id="a4d84-105">**онкаунтераддед**</span><span class="sxs-lookup"><span data-stu-id="a4d84-105">**OnCounterAdded**</span></span>](systemmonitor-oncounteradded.md)
-   [<span data-ttu-id="a4d84-106">**онкаунтерделетед**</span><span class="sxs-lookup"><span data-stu-id="a4d84-106">**OnCounterDeleted**</span></span>](-systemmonitor-oncounterdeleted.md)
-   [<span data-ttu-id="a4d84-107">**онкаунтерселектед**</span><span class="sxs-lookup"><span data-stu-id="a4d84-107">**OnCounterSelected**</span></span>](-systemmonitor-oncounterselected.md)
-   [<span data-ttu-id="a4d84-108">**ондблкликк**</span><span class="sxs-lookup"><span data-stu-id="a4d84-108">**OnDblClick**</span></span>](-systemmonitor-ondblclick.md)
-   [<span data-ttu-id="a4d84-109">**онсамплеколлектед**</span><span class="sxs-lookup"><span data-stu-id="a4d84-109">**OnSampleCollected**</span></span>](-systemmonitor-onsamplecollected.md)

> [!Note]  
> <span data-ttu-id="a4d84-110">Необходимо возвратить из обработчика событий до истечения [**интервала обновления**](systemmonitor-updateinterval.md) . в противном случае СИСМОН отображает окно сообщения, указывающее пользователю, что ему не удалось выполнить выборку значений счетчиков для предыдущего интервала обновления.</span><span class="sxs-lookup"><span data-stu-id="a4d84-110">You must return from the event handler before the [**update interval**](systemmonitor-updateinterval.md) expires; otherwise, SYSMON displays a message box indicating to the user that it was unable to sample counter values for the previous update interval.</span></span>

 

 

 




