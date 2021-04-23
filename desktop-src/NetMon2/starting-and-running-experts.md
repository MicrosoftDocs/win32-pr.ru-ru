---
description: При нажатии кнопки Запуск экспертов из окна экспертов сетевой монитор пользовательского интерфейса запускаются эксперты, выбранные для файла записи, и вызывается функция Run. При запуске эксперт анализирует файл записи с помощью нескольких функций для работы с экспертными кадрами.
ms.assetid: 6b8a66cb-d1d6-4e19-b668-049a03a40804
title: Запуск и запуск экспертов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bd41472d286727541d26bade1942eb3b6b5c593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684538"
---
# <a name="starting-and-running-experts"></a><span data-ttu-id="bd1af-104">Запуск и запуск экспертов</span><span class="sxs-lookup"><span data-stu-id="bd1af-104">Starting and Running Experts</span></span>

<span data-ttu-id="bd1af-105">При нажатии кнопки **Запуск экспертов** из окна экспертов сетевой монитор пользовательского интерфейса запускаются эксперты, выбранные для файла записи, и вызывается функция [**Run**](run.md) .</span><span class="sxs-lookup"><span data-stu-id="bd1af-105">Clicking **Run Experts** from the Experts window of the Network Monitor UI starts the experts selected for the capture file and calls the [**Run**](run.md) function.</span></span> <span data-ttu-id="bd1af-106">При запуске эксперт анализирует файл записи с помощью нескольких функций для работы с экспертными кадрами.</span><span class="sxs-lookup"><span data-stu-id="bd1af-106">When started, the expert analyzes the capture file by using several expert frame functions.</span></span>

<span data-ttu-id="bd1af-107">Функция [**експертиндикатестатус**](expertindicatestatus.md) предоставляет сведения о состоянии эксперта.</span><span class="sxs-lookup"><span data-stu-id="bd1af-107">The [**ExpertIndicateStatus**](expertindicatestatus.md) function provides status information from the expert.</span></span> <span data-ttu-id="bd1af-108">При запуске эксперта с сетевой монитор в окне "состояние эксперта" отображаются периодически обновляемые сведения о состоянии (от 0 до 100 процента завершения).</span><span class="sxs-lookup"><span data-stu-id="bd1af-108">When you run an expert with Network Monitor, the Expert Status View window displays periodically updated status information (from 0 to 100 percent completion).</span></span>

![окно просмотра состояния эксперта](images/exview.png)

<span data-ttu-id="bd1af-110">Эксперт находится в активном состоянии до тех пор, пока данные не будут завершены после файла записи.</span><span class="sxs-lookup"><span data-stu-id="bd1af-110">The expert is active until the data completes its pass though the capture file.</span></span> <span data-ttu-id="bd1af-111">После завершения прохода появится окно Просмотр событий.</span><span class="sxs-lookup"><span data-stu-id="bd1af-111">When the pass is complete, an Event Viewer window appears.</span></span> <span data-ttu-id="bd1af-112">Информация в этом окне зависит от типа эксперта, который проанализировал данные.</span><span class="sxs-lookup"><span data-stu-id="bd1af-112">The information in this window depends on the type of expert that analyzed the data.</span></span> <span data-ttu-id="bd1af-113">На следующем рисунке показано представление эксперта по распространению свойств, в котором обобщены данные о кадрах, проанализированные экспертом.</span><span class="sxs-lookup"><span data-stu-id="bd1af-113">The following illustration shows a Property Distribution Expert view, which summarizes the frame data that the expert analyzed.</span></span>

![представление эксперта по распространению свойств](images/exview1.png)

<span data-ttu-id="bd1af-115">Второй отчет (не показан) содержит сводку результатов эксперта по пересылке протокола управления передачей (TCP).</span><span class="sxs-lookup"><span data-stu-id="bd1af-115">A second report (not shown), summarizes the results of the Transmission Control Protocol (TCP) Retransmit expert.</span></span>

<span data-ttu-id="bd1af-116">Также можно:</span><span class="sxs-lookup"><span data-stu-id="bd1af-116">You can also:</span></span>

-   <span data-ttu-id="bd1af-117">Создайте запись для страницы ссылки на событие (ERP), которая рекомендует пользователю обнаруженные условия или проблемы (как показано в окне анализ).</span><span class="sxs-lookup"><span data-stu-id="bd1af-117">Create an entry for an event reference page (ERP) that advises the user of detected conditions or problems (as shown in the Analysis window).</span></span>
-   <span data-ttu-id="bd1af-118">Создайте записи для предлагаемых исправлений или поясняющих данных, которые содержат дополнительные сведения (как показано в окне разрешения).</span><span class="sxs-lookup"><span data-stu-id="bd1af-118">Create entries for suggested fixes or explanatory data that provide additional information (as shown in the Resolution window).</span></span>

<span data-ttu-id="bd1af-119">После того, как эксперт завершит свою задачу, сетевой монитор удалит эксперт из активной памяти.</span><span class="sxs-lookup"><span data-stu-id="bd1af-119">After the expert completes its task, Network Monitor removes the expert from active memory.</span></span> <span data-ttu-id="bd1af-120">Эксперты должны использовать функции защищенной памяти, включенные в пакет средств разработки программного обеспечения (SDK) платформы. Эти функции удаляют память в случае сбоя экспертов во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="bd1af-120">Experts should use the protected memory functions included in the Platform Software Development Kit (SDK); these functions clean up memory if the experts fail during run time.</span></span>

 

 



