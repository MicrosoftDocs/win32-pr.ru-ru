---
description: После того как вы разрабатываете исходный HTML-документ со страницей ссылки на события (ERP), необходимо присвоить ему имя, прежде чем сетевой монитор сможет отобразить его в Просмотр событий.
ms.assetid: 0c668a8b-94a5-4996-8214-4629a24a8337
title: Именование страницы ссылки на события
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f9c82b153ce2c7086af3883bcf3c4b34a0e68a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664736"
---
# <a name="naming-an-event-reference-page"></a><span data-ttu-id="028b5-103">Именование страницы ссылки на события</span><span class="sxs-lookup"><span data-stu-id="028b5-103">Naming an Event Reference Page</span></span>

<span data-ttu-id="028b5-104">После того как вы разрабатываете исходный HTML-документ со страницей ссылки на события (ERP), необходимо присвоить ему имя, прежде чем сетевой монитор сможет отобразить его в Просмотр событий.</span><span class="sxs-lookup"><span data-stu-id="028b5-104">After you author an event reference page (ERP) source HTML document, you must name it before Network Monitor can display it in the Event Viewer.</span></span>

<span data-ttu-id="028b5-105">Файлы мониторинга имен и файловые ERP экспертов в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="028b5-105">Name monitor and expert ERP files with this format:</span></span>

``` syntax
<ExpertName><EventIdent>.htm (or <MonitorName><EventIdent>.htm)
```

<dl> <dt>

<span data-ttu-id="028b5-106"><span id="ExpertName"></span><span id="expertname"></span><span id="EXPERTNAME"></span>**експертнаме**</span><span class="sxs-lookup"><span data-stu-id="028b5-106"><span id="ExpertName"></span><span id="expertname"></span><span id="EXPERTNAME"></span>**ExpertName**</span></span>
</dt> <dd>

<span data-ttu-id="028b5-107">Имя файла DLL, за исключением расширения имени файла.</span><span class="sxs-lookup"><span data-stu-id="028b5-107">DLL file name, excluding the file name extension.</span></span>

</dd> <dt>

<span data-ttu-id="028b5-108"><span id="EventIdent"></span><span id="eventident"></span><span id="EVENTIDENT"></span>**евентидент**</span><span class="sxs-lookup"><span data-stu-id="028b5-108"><span id="EventIdent"></span><span id="eventident"></span><span id="EVENTIDENT"></span>**EventIdent**</span></span>
</dt> <dd>

<span data-ttu-id="028b5-109">Идентификатор события экспертного ERP.</span><span class="sxs-lookup"><span data-stu-id="028b5-109">Event identifier of the expert ERP.</span></span>

<span data-ttu-id="028b5-110">Идентификатор события также находится в элементе **евентидент** структуры **нмевентдата** .</span><span class="sxs-lookup"><span data-stu-id="028b5-110">The event identifier is also found in the **EventIdent** member of the **NMEVENTDATA** structure.</span></span>

</dd> </dl>

<span data-ttu-id="028b5-111">Дополнительные сведения о создании ERP см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="028b5-111">For more information about creating an ERP, see the following topics:</span></span>

-   [<span data-ttu-id="028b5-112">Создание страниц со ссылками на события экспертов и мониторинга</span><span class="sxs-lookup"><span data-stu-id="028b5-112">Creating Expert and Monitor Event Reference Pages</span></span>](creating-expert-and-monitor-event-reference-pages.md)
-   [<span data-ttu-id="028b5-113">Создание страницы ссылки на событие</span><span class="sxs-lookup"><span data-stu-id="028b5-113">Writing an Event Reference Page</span></span>](writing-an-event-reference-page.md)
-   [<span data-ttu-id="028b5-114">Тестирование страницы ссылки на событие</span><span class="sxs-lookup"><span data-stu-id="028b5-114">Testing an Event Reference Page</span></span>](testing-an-event-reference-page.md)

 

 



