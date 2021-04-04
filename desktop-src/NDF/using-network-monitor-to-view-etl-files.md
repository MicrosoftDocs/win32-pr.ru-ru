---
title: Использование сетевого монитора для просмотра файлов ETL
description: Сетевой монитор 3,3 позволяет пользователям анализировать, фильтровать и просматривать ETL-файл (с помощью Windows Vista или более поздней версии).
ms.assetid: 932be193-70f9-48f9-95d8-18916d3b7064
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04120f860654f4859aa930f32a4711999682eaf8
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "103999801"
---
# <a name="using-network-monitor-to-view-etl-files"></a><span data-ttu-id="1e422-103">Использование сетевого монитора для просмотра файлов ETL</span><span class="sxs-lookup"><span data-stu-id="1e422-103">Using Network Monitor to View ETL Files</span></span>

<span data-ttu-id="1e422-104">[Сетевой монитор 3,3](https://connect.microsoft.com/site/sitehome.aspx?SiteID=216) позволяет пользователям анализировать, фильтровать и просматривать ETL-файл (с помощью Windows Vista или более поздней версии).</span><span class="sxs-lookup"><span data-stu-id="1e422-104">[Network Monitor 3.3](https://connect.microsoft.com/site/sitehome.aspx?SiteID=216) enables users to parse, filter, and view an ETL file (using Windows Vista or later).</span></span> <span data-ttu-id="1e422-105">(При использовании сетевой монитор 3,2 необходимо скачать и установить дополнительные средства синтаксического анализа из [CodePlex](https://www.codeplex.com/NMParsers) , чтобы отобразить события трассировки сети.)</span><span class="sxs-lookup"><span data-stu-id="1e422-105">(If using Network Monitor 3.2, you will need to download and install additional parsers from [CodePlex](https://www.codeplex.com/NMParsers) in order to render the network tracing events.)</span></span>

<span data-ttu-id="1e422-106">Коррелированные файлы ETL объединяют соответствующие события в группу.</span><span class="sxs-lookup"><span data-stu-id="1e422-106">Correlated ETL files group the relevant events together.</span></span> <span data-ttu-id="1e422-107">В илллустратион ниже показан связанный файл, Открытый в сетевой монитор с включенным диалоговым каналом.</span><span class="sxs-lookup"><span data-stu-id="1e422-107">The illlustration below shows a correlated file opened in Network Monitor, with conversation enabled.</span></span>

![Снимок экрана, на котором показана сетевой монитор с коррелированными событиями, выделенными в левом окне и Утевент из раскрывающегося списка.](images/ut-netmon1.png)

<span data-ttu-id="1e422-109">Коррелированные события группируются по действиям на левой панели.</span><span class="sxs-lookup"><span data-stu-id="1e422-109">Correlated events are grouped by activity in the left pane.</span></span> <span data-ttu-id="1e422-110">Можно выбрать событие на панели Сводка кадров, а затем щелкнуть правой кнопкой мыши, чтобы выбрать диалог на уровне событий сети.</span><span class="sxs-lookup"><span data-stu-id="1e422-110">You can select an event in the Frame Summary pane, then right-click to select the conversation at the network event level.</span></span> <span data-ttu-id="1e422-111">В левой области отобразится соответствующее действие.</span><span class="sxs-lookup"><span data-stu-id="1e422-111">This will display a related activity in the left pane.</span></span>

<span data-ttu-id="1e422-112">При выборе конкретного действия на левой панели отображается список поставщиков для коррелированных событий.</span><span class="sxs-lookup"><span data-stu-id="1e422-112">Selecting a particular activity from the left pane and expanding it will show the list of providers for the correlated events.</span></span>

![Снимок экрана, показывающий сетевой монитор с действием, выбранным на левой панели, и событиями, соответствующими этому событию в правой области.](images/ut-netmon2.png)

<span data-ttu-id="1e422-114">При выборе конкретного поставщика в левой области список событий, характерных для этого поставщика и действия, будет отображаться на панели Сводка по кадрам.</span><span class="sxs-lookup"><span data-stu-id="1e422-114">When you select a specific provider in the left pane, a list of events specific to that provider and activity will be displayed in the Frame Summary pane.</span></span>

![Снимок экрана, на котором показан конкретный поставщик, выбранный в левой области, и список событий, относящихся к поставщику, выделенному в верхней правой области.](images/ut-netmon3.png)

<span data-ttu-id="1e422-116">Фильтры можно применять в сетевой монитор, чтобы облегчить просмотр и поиск нужных событий или пакетов.</span><span class="sxs-lookup"><span data-stu-id="1e422-116">Filters can be applied in Network Monitor to make it easier to view and find the right events or packet.</span></span> <span data-ttu-id="1e422-117">Например, можно применить фильтр к выбранным событиям ошибки (например, **утевент. Header. дескриптор. Level = = 2**), чтобы отобразить их в определенном цвете.</span><span class="sxs-lookup"><span data-stu-id="1e422-117">For example, you can apply a filter to selected error events (for example, **UTEvent.Header.Descriptor.Level == 2**) to display them in a certain color.</span></span>

![Снимок экрана, показывающий диалоговое окно "изменение фильтра цвета".](images/ut-netmon4.png)

<span data-ttu-id="1e422-119">Фильтры также можно применять для пометки различных поставщиков в различных цветах, чтобы их было проще просматривать.</span><span class="sxs-lookup"><span data-stu-id="1e422-119">Filters can also be applied to mark different providers in different colors so that the results are easier to view.</span></span>

![Снимок экрана, на котором показан пример различных поставщиков, помеченных разными цветами.](images/ut-netmon5.png)

<span data-ttu-id="1e422-121">Чтобы применить фильтр, щелкните **колорфилтерс** в меню **фильтры** .</span><span class="sxs-lookup"><span data-stu-id="1e422-121">To apply a filter, click **ColorFilters** on the **Filters** menu.</span></span>

<span data-ttu-id="1e422-122">В следующей таблице приведены некоторые примеры полезных фильтров.</span><span class="sxs-lookup"><span data-stu-id="1e422-122">The following table shows some examples of useful filters.</span></span>



| <span data-ttu-id="1e422-123">Фильтр</span><span class="sxs-lookup"><span data-stu-id="1e422-123">Filter</span></span>                                                                        | <span data-ttu-id="1e422-124">Описание</span><span class="sxs-lookup"><span data-stu-id="1e422-124">Description</span></span>                                                       |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="1e422-125">Утевент. Header. дескриптор. Level = = 2</span><span class="sxs-lookup"><span data-stu-id="1e422-125">UTEvent.Header.Descriptor.Level == 2</span></span>                                          | <span data-ttu-id="1e422-126">Фильтрует только события ошибок.</span><span class="sxs-lookup"><span data-stu-id="1e422-126">Filters only error events.</span></span>                                        |
| <span data-ttu-id="1e422-127">Утевент. Header. дескриптор. Level = = 3</span><span class="sxs-lookup"><span data-stu-id="1e422-127">UTEvent.Header.Descriptor.Level == 3</span></span>                                          | <span data-ttu-id="1e422-128">Фильтрует только предупреждающие события.</span><span class="sxs-lookup"><span data-stu-id="1e422-128">Filters only warning events.</span></span>                                      |
| <span data-ttu-id="1e422-129">UTEvent.Header.Descriptor.Id = = 2001</span><span class="sxs-lookup"><span data-stu-id="1e422-129">UTEvent.Header.Descriptor.Id == 2001</span></span>                                          | <span data-ttu-id="1e422-130">Фильтруется только события с ИДЕНТИФИКАТОРом события 2001.</span><span class="sxs-lookup"><span data-stu-id="1e422-130">Filters only events with event ID 2001.</span></span>                           |
| <span data-ttu-id="1e422-131">\_МИКРОСОФТВИНДОВСВЛАНАУТОКОНФИГ WLAN</span><span class="sxs-lookup"><span data-stu-id="1e422-131">WLAN\_MicrosoftWindowsWLANAutoConfig</span></span>                                          | <span data-ttu-id="1e422-132">Фильтрует только события из службы WLAN.</span><span class="sxs-lookup"><span data-stu-id="1e422-132">Filters only events from WLAN service.</span></span>                            |
| <span data-ttu-id="1e422-133">N802 \_ микрософтвиндовснвифи</span><span class="sxs-lookup"><span data-stu-id="1e422-133">N802\_MicrosoftWindowsNWiFi</span></span>                                                   | <span data-ttu-id="1e422-134">Фильтрует только события из собственного драйвера Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="1e422-134">Filters only events from the Native Wifi driver.</span></span>                  |
| <span data-ttu-id="1e422-135">WLAN \_ МИКРОСОФТВИНДОВСВЛАНАУТОКОНФИГ и UTEvent.Header.descriptor.ID = = 2001</span><span class="sxs-lookup"><span data-stu-id="1e422-135">WLAN\_MicrosoftWindowsWLANAutoConfig AND UTEvent.Header.Descriptor.Id == 2001</span></span> | <span data-ttu-id="1e422-136">Фильтрует только события с ИДЕНТИФИКАТОРом 2001, выпущенными службой беспроводной сети.</span><span class="sxs-lookup"><span data-stu-id="1e422-136">Filters only events with event ID 2001 emitted from WLAN service.</span></span> |



 

 

 




