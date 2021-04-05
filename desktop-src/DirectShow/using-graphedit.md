---
description: Использование Графедит
ms.assetid: 91a8f111-fce4-4284-afa2-e3ea0ec35bff
title: Использование Графедит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e78118253d86a88231456b72dc8c42ed2a674f5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546055"
---
# <a name="using-graphedit"></a><span data-ttu-id="04d31-103">Использование Графедит</span><span class="sxs-lookup"><span data-stu-id="04d31-103">Using GraphEdit</span></span>

<span data-ttu-id="04d31-104">Графедит доступен в пакете средств разработки программного обеспечения (SDK) для Microsoft Windows ( <https://go.microsoft.com/fwlink/p/?linkid=62332> ).</span><span class="sxs-lookup"><span data-stu-id="04d31-104">GraphEdit is available in the Microsoft Windows Software Development Kit (SDK) (<https://go.microsoft.com/fwlink/p/?linkid=62332>).</span></span>

<span data-ttu-id="04d31-105">Имя приложения Графедит — "graphedt.exe".</span><span class="sxs-lookup"><span data-stu-id="04d31-105">The name of the GraphEdit application is "graphedt.exe".</span></span> <span data-ttu-id="04d31-106">После установки пакета SDK "graphedt.exe" находится в следующем каталоге: \[ Program Files \] \\ Microsoft SDKs \\ Windows \\ \[ Version \] \\ bin \\ .</span><span class="sxs-lookup"><span data-stu-id="04d31-106">After you install the SDK, "graphedt.exe" is located in the following directory: \[Program Files\]\\Microsoft SDKs\\Windows\\\[version\]\\Bin\\.</span></span>

<span data-ttu-id="04d31-107">Перед запуском Графедит используйте служебную программу regsvr32, чтобы зарегистрировать следующие библиотеки DLL, расположенные в одном каталоге:</span><span class="sxs-lookup"><span data-stu-id="04d31-107">Before running GraphEdit, use the regsvr32 utility to register the following DLLs, which are located in the same directory:</span></span>

-   <span data-ttu-id="04d31-108">proppage.dll</span><span class="sxs-lookup"><span data-stu-id="04d31-108">proppage.dll</span></span>
-   <span data-ttu-id="04d31-109">evrprop.dll</span><span class="sxs-lookup"><span data-stu-id="04d31-109">evrprop.dll</span></span>

<span data-ttu-id="04d31-110">Эти библиотеки DLL позволяют Графедит отображать страницы свойств для некоторых встроенных фильтров DirectShow.</span><span class="sxs-lookup"><span data-stu-id="04d31-110">These DLLs enable GraphEdit to display property pages for some of the built-in DirectShow filters.</span></span>

## <a name="build-a-file-playback-graph"></a><span data-ttu-id="04d31-111">Создание графа воспроизведения файлов</span><span class="sxs-lookup"><span data-stu-id="04d31-111">Build a File Playback Graph</span></span>

<span data-ttu-id="04d31-112">Графедит может создать граф фильтра для воспроизведения файла.</span><span class="sxs-lookup"><span data-stu-id="04d31-112">GraphEdit can build a filter graph for file playback.</span></span> <span data-ttu-id="04d31-113">Эта функция эквивалентна вызову метода [**играфбуилдер:: renderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) в приложении.</span><span class="sxs-lookup"><span data-stu-id="04d31-113">This feature is equivalent to calling the [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) method in an application.</span></span> <span data-ttu-id="04d31-114">В меню **файл** выберите команду **вывести файл мультимедиа**.</span><span class="sxs-lookup"><span data-stu-id="04d31-114">From the **File** menu, click **Render Media File**.</span></span> <span data-ttu-id="04d31-115">Графедит отображает диалоговое окно **открытия файла** .</span><span class="sxs-lookup"><span data-stu-id="04d31-115">GraphEdit displays an **Open File** dialog box.</span></span> <span data-ttu-id="04d31-116">Выберите файл мультимедиа и нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="04d31-116">Select a multimedia file and click **Open**.</span></span> <span data-ttu-id="04d31-117">Графедит создает граф фильтра для воспроизведения выбранного файла.</span><span class="sxs-lookup"><span data-stu-id="04d31-117">GraphEdit builds a filter graph to play the file you've selected.</span></span>

<span data-ttu-id="04d31-118">Можно также отобразить файл мультимедиа, расположенный по URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="04d31-118">You can also render a media file located at a URL.</span></span> <span data-ttu-id="04d31-119">В меню **файл** выберите команду **отобразить URL-адрес**.</span><span class="sxs-lookup"><span data-stu-id="04d31-119">From the **File** menu, click **Render URL**.</span></span> <span data-ttu-id="04d31-120">Графедит отображает диалоговое окно для ввода URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="04d31-120">GraphEdit displays a dialog box in which to type the URL.</span></span>

## <a name="build-a-filter-graph"></a><span data-ttu-id="04d31-121">Создание графа фильтра</span><span class="sxs-lookup"><span data-stu-id="04d31-121">Build a Filter Graph</span></span>

<span data-ttu-id="04d31-122">Графедит может создать настраиваемый граф фильтра, используя любой из фильтров, зарегистрированных в системе.</span><span class="sxs-lookup"><span data-stu-id="04d31-122">GraphEdit can build a custom filter graph, using any of the filters registered on your system.</span></span> <span data-ttu-id="04d31-123">В меню **Диаграмма** выберите команду **Вставить фильтры**.</span><span class="sxs-lookup"><span data-stu-id="04d31-123">From the **Graph** menu, click **Insert Filters**.</span></span> <span data-ttu-id="04d31-124">Откроется диалоговое окно со списком фильтров в системе, упорядоченных по категориям фильтров.</span><span class="sxs-lookup"><span data-stu-id="04d31-124">A dialog box appears with a list of the filters on your system, organized by filter category.</span></span> <span data-ttu-id="04d31-125">Графедит создает этот список из информации в реестре.</span><span class="sxs-lookup"><span data-stu-id="04d31-125">GraphEdit builds this list from information in the registry.</span></span> <span data-ttu-id="04d31-126">На следующем рисунке показано диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="04d31-126">The following illustration shows the dialog box.</span></span>

![какие фильтры нужно вставить?](images/gedit12.png)

<span data-ttu-id="04d31-128">Чтобы добавить фильтр к диаграмме, выберите имя фильтра и нажмите кнопку **Вставить фильтры** или дважды щелкните имя фильтра.</span><span class="sxs-lookup"><span data-stu-id="04d31-128">To add a filter to the graph, select the name of the filter and click the **Insert Filters** button, or double-click the filter name.</span></span> <span data-ttu-id="04d31-129">После добавления фильтров можно подключить два фильтра, перетащив указатель мыши с выходного контакта одного фильтра на входной ПИН-код другого фильтра.</span><span class="sxs-lookup"><span data-stu-id="04d31-129">After you have added the filters, you can connect two filters by dragging the mouse from one filter's output pin to another filter's input pin.</span></span> <span data-ttu-id="04d31-130">Если ПИН-коды принимают соединение, Графедит рисует стрелку, соединяющую их.</span><span class="sxs-lookup"><span data-stu-id="04d31-130">If the pins accept the connection, GraphEdit draws an arrow connecting them.</span></span>

![соединение двух фильтров](images/gedit-connect.png)

## <a name="run-the-graph"></a><span data-ttu-id="04d31-132">Запуск графа</span><span class="sxs-lookup"><span data-stu-id="04d31-132">Run the Graph</span></span>

<span data-ttu-id="04d31-133">После построения графа фильтра в поле изменить граф можно запустить граф, чтобы узнать, работает ли он правильно.</span><span class="sxs-lookup"><span data-stu-id="04d31-133">Once you have built a filter graph in Graph Edit, you can run the graph to see whether it works as you expect.</span></span> <span data-ttu-id="04d31-134">Меню **Диаграмма** содержит команды **воспроизведения**, **приостановки** и **остановки**.</span><span class="sxs-lookup"><span data-stu-id="04d31-134">The **Graph** menu contains the menu commands **Play**, **Pause**, and **Stop**.</span></span> <span data-ttu-id="04d31-135">Эти команды вызывают методы [**имедиаконтрол**](/windows/desktop/api/Control/nn-control-imediacontrol) для [**запуска**](/windows/desktop/api/Control/nf-control-imediacontrol-run), [**приостановки**](/windows/desktop/api/Control/nf-control-imediacontrol-pause)и [**остановки**](/windows/desktop/api/Control/nf-control-imediacontrol-stop)соответственно.</span><span class="sxs-lookup"><span data-stu-id="04d31-135">These commands invoke to the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) methods [**Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), [**Pause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause), and [**Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop), respectively.</span></span> <span data-ttu-id="04d31-136">Кроме того, на панели инструментов Графедит есть кнопки для этих команд:</span><span class="sxs-lookup"><span data-stu-id="04d31-136">The GraphEdit toolbar has buttons for these commands, as well:</span></span>

![кнопки приостановки, воспроизведения и остановки](images/gedit-toolbar.png)

> [!Note]  
> <span data-ttu-id="04d31-138">Команда Графедит **остановить** сначала приостанавливает граф и выполняет поиск до нулевого времени (предполагая, что граф доступен для поиска).</span><span class="sxs-lookup"><span data-stu-id="04d31-138">The GraphEdit **Stop** command first pauses the graph and seeks to time zero (assuming the graph is seekable).</span></span> <span data-ttu-id="04d31-139">При воспроизведении файла это действие сбрасывает окно видео до первого кадра.</span><span class="sxs-lookup"><span data-stu-id="04d31-139">For file playback, this action resets the video window to the first frame.</span></span> <span data-ttu-id="04d31-140">Затем Графедит вызывает [**имедиаконтрол:: останавливаться**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).</span><span class="sxs-lookup"><span data-stu-id="04d31-140">Then GraphEdit calls [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).</span></span>

 

<span data-ttu-id="04d31-141">Если граф доступен для поиска, его можно найти, перетащив ползунок, расположенный под панелью инструментов.</span><span class="sxs-lookup"><span data-stu-id="04d31-141">If the graph is seekable, you can seek it by dragging the slider bar that appears below the toolbar.</span></span> <span data-ttu-id="04d31-142">При перетаскивании ползунок вызывается метод [**имедиасикинг:: сетпоситионс**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="04d31-142">Dragging the slider bar invokes the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span>

## <a name="view-property-pages"></a><span data-ttu-id="04d31-143">Просмотр страниц свойств</span><span class="sxs-lookup"><span data-stu-id="04d31-143">View Property Pages</span></span>

<span data-ttu-id="04d31-144">Некоторые фильтры поддерживают страницы пользовательских свойств, которые предоставляют пользовательский интерфейс для установки свойств фильтра.</span><span class="sxs-lookup"><span data-stu-id="04d31-144">Some filters support custom property pages, which provide a user interface for setting properties on the filter.</span></span> <span data-ttu-id="04d31-145">Чтобы просмотреть страницу свойств фильтра в Графедит, щелкните правой кнопкой мыши фильтр и выберите пункт **Свойства** во всплывающем окне.</span><span class="sxs-lookup"><span data-stu-id="04d31-145">To view a filter's property page in GraphEdit, right-click the filter and select **Properties** from the pop-up window.</span></span> <span data-ttu-id="04d31-146">Графедит отображает страницу свойств, содержащую вкладки свойств, определенные фильтром (если таковые имеются).</span><span class="sxs-lookup"><span data-stu-id="04d31-146">GraphEdit displays a property page that contains the property sheets defined by the filter (if any).</span></span> <span data-ttu-id="04d31-147">Кроме того, Графедит содержит страницу свойств для каждого ПИН-кода фильтра.</span><span class="sxs-lookup"><span data-stu-id="04d31-147">In addition, GraphEdit includes a property sheet for each pin on the filter.</span></span> <span data-ttu-id="04d31-148">Вкладки свойств закрепления определяются Графедит, а не фильтром.</span><span class="sxs-lookup"><span data-stu-id="04d31-148">The pin property sheets are defined by GraphEdit, not by the filter.</span></span> <span data-ttu-id="04d31-149">Если ПИН-код подключен, на странице свойств закрепление отображается тип носителя для соединения.</span><span class="sxs-lookup"><span data-stu-id="04d31-149">If the pin is connected, the pin property sheet displays the media type for the connection.</span></span> <span data-ttu-id="04d31-150">В противном случае в нем перечисляются предпочтительные типы носителей для ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="04d31-150">Otherwise, it lists the pin's preferred media types.</span></span>

> [!Note]  
> <span data-ttu-id="04d31-151">Чтобы использовать встроенные страницы свойств Графедит, необходимо зарегистрировать proppage.dll.</span><span class="sxs-lookup"><span data-stu-id="04d31-151">To use GraphEdit's built-in property pages, you must register proppage.dll.</span></span> <span data-ttu-id="04d31-152">Эта библиотека DLL доступна в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="04d31-152">This DLL is available in the Windows SDK.</span></span> <span data-ttu-id="04d31-153">Библиотека DLL также содержит дополнительные страницы свойств для некоторых фильтров DirectShow.</span><span class="sxs-lookup"><span data-stu-id="04d31-153">The DLL also contains additional property pages for some DirectShow filters.</span></span> <span data-ttu-id="04d31-154">Эти страницы свойств предоставляются только в целях отладки.</span><span class="sxs-lookup"><span data-stu-id="04d31-154">These property pages are provided for debugging purposes only.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="04d31-155">См. также</span><span class="sxs-lookup"><span data-stu-id="04d31-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04d31-156">Имитация построения графа с помощью Графедит</span><span class="sxs-lookup"><span data-stu-id="04d31-156">Simulating Graph Building with GraphEdit</span></span>](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



