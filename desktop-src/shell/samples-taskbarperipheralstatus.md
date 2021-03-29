---
description: Демонстрирует наложение значков на панели задач и индикатор выполнения.
title: 'Пример: статус периферийных элементов на панели задач'
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E4B693FB-EE7D-47d0-A5D8-91205AD4A3DC
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 793c09853e3174f426b7b41685f2593daaae9b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997890"
---
# <a name="taskbar-peripheral-status-sample"></a><span data-ttu-id="e4f3f-103">Пример: статус периферийных элементов на панели задач</span><span class="sxs-lookup"><span data-stu-id="e4f3f-103">Taskbar Peripheral Status Sample</span></span>

<span data-ttu-id="e4f3f-104">Демонстрирует наложение значков на панели задач и индикатор выполнения.</span><span class="sxs-lookup"><span data-stu-id="e4f3f-104">Demonstrates taskbar icon overlays and progress bars.</span></span>

<span data-ttu-id="e4f3f-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="e4f3f-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="e4f3f-106">Описание</span><span class="sxs-lookup"><span data-stu-id="e4f3f-106">Description</span></span>](#description)
-   [<span data-ttu-id="e4f3f-107">Требования</span><span class="sxs-lookup"><span data-stu-id="e4f3f-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="e4f3f-108">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="e4f3f-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="e4f3f-109">Создание примера</span><span class="sxs-lookup"><span data-stu-id="e4f3f-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="e4f3f-110">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="e4f3f-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="e4f3f-111">См. также</span><span class="sxs-lookup"><span data-stu-id="e4f3f-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="e4f3f-112">Описание</span><span class="sxs-lookup"><span data-stu-id="e4f3f-112">Description</span></span>

<span data-ttu-id="e4f3f-113">В этом образце создается пример кнопки на панели задач, на которой демонстрируется использование [**ITaskbarList3:: сетоверлайикон**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setoverlayicon) , что позволяет применять различные наложения, выбранные в меню.</span><span class="sxs-lookup"><span data-stu-id="e4f3f-113">This sample creates an example taskbar button on which it demonstrates the use of [**ITaskbarList3::SetOverlayIcon**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setoverlayicon) by allowing you to apply various overlays chosen from a menu.</span></span>

<span data-ttu-id="e4f3f-114">В примере также предусмотрена возможность имитации индикатора хода выполнения на кнопке, демонстрирующий использование [**ITaskbarList3:: сетпрогрессстате**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressstate) и [**ITaskbarList3:: сетпрогрессвалуе**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue) путем отображения на первом неопределенном ИНДИКАТОРе выполнения (тбпф \_ неопределенного), а затем является нормальным пропорциональным индикатором (тбпф \_ нормальным).</span><span class="sxs-lookup"><span data-stu-id="e4f3f-114">The sample also provides the option of simulating a progress indicator on the button, demonstrating the use of [**ITaskbarList3::SetProgressState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressstate) and [**ITaskbarList3::SetProgressValue**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue) by showing at first an indeterminate progress indicator (TBPF\_INDETERMINATE), and then a normal proportional indicator (TBPF\_NORMAL).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4f3f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="e4f3f-115">Requirements</span></span>



| <span data-ttu-id="e4f3f-116">Продукт</span><span class="sxs-lookup"><span data-stu-id="e4f3f-116">Product</span></span>                                | <span data-ttu-id="e4f3f-117">Минимальная версия продукта</span><span class="sxs-lookup"><span data-stu-id="e4f3f-117">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="e4f3f-118">Windows</span><span class="sxs-lookup"><span data-stu-id="e4f3f-118">Windows</span></span>                                | <span data-ttu-id="e4f3f-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4f3f-119">Windows 7</span></span>               |
| <span data-ttu-id="e4f3f-120">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="e4f3f-120">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="e4f3f-121">7.0</span><span class="sxs-lookup"><span data-stu-id="e4f3f-121">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="e4f3f-122">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="e4f3f-122">Downloading the Sample</span></span>

| <span data-ttu-id="e4f3f-123">Расположение</span><span class="sxs-lookup"><span data-stu-id="e4f3f-123">Location</span></span>      | <span data-ttu-id="e4f3f-124">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="e4f3f-124">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4f3f-125">GitHub</span><span class="sxs-lookup"><span data-stu-id="e4f3f-125">GitHub</span></span>  | [<span data-ttu-id="e4f3f-126">Пример Таскбарперифералстатус</span><span class="sxs-lookup"><span data-stu-id="e4f3f-126">TaskBarPeripheralStatus sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TaskbarPeripheralStatus) |

## <a name="building-the-sample"></a><span data-ttu-id="e4f3f-127">Построение образца</span><span class="sxs-lookup"><span data-stu-id="e4f3f-127">Building the Sample</span></span>

<span data-ttu-id="e4f3f-128">Чтобы построить образец из командной строки, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e4f3f-128">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="e4f3f-129">Откройте окно командной строки и перейдите в каталог проекта **таскбарперифералстатус** .</span><span class="sxs-lookup"><span data-stu-id="e4f3f-129">Open the command prompt window and navigate to the **TaskbarPeripheralStatus** project directory.</span></span>
2.  <span data-ttu-id="e4f3f-130">Введите `msbuild PeripheralStatus.sln`.</span><span class="sxs-lookup"><span data-stu-id="e4f3f-130">Enter `msbuild PeripheralStatus.sln`.</span></span>

<span data-ttu-id="e4f3f-131">Чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):</span><span class="sxs-lookup"><span data-stu-id="e4f3f-131">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="e4f3f-132">Откройте проводник Windows и перейдите в каталог проекта **таскбарперифералстатус** .</span><span class="sxs-lookup"><span data-stu-id="e4f3f-132">Open Windows Explorer and navigate to the **TaskbarPeripheralStatus** project directory.</span></span>
2.  <span data-ttu-id="e4f3f-133">Дважды щелкните значок файла Перифералстатус. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e4f3f-133">Double-click the icon for the PeripheralStatus.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="e4f3f-134">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="e4f3f-134">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="e4f3f-135">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="e4f3f-135">Running the Sample</span></span>

1.  <span data-ttu-id="e4f3f-136">Перейдите в каталог, содержащий новый исполняемый файл (например, `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarPeripheralStatus\Win32\Debug` ), с помощью командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="e4f3f-136">Navigate to the directory that contains the new executable file (for instance, `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarPeripheralStatus\Win32\Debug`), using the command prompt or Windows Explorer.</span></span>

    -   <span data-ttu-id="e4f3f-137">При использовании командной строки введите `PeripheralStatus.exe` .</span><span class="sxs-lookup"><span data-stu-id="e4f3f-137">If using the command line, enter `PeripheralStatus.exe`.</span></span>
    -   <span data-ttu-id="e4f3f-138">Если используется проводник Windows, дважды щелкните значок для PeripheralStatus.exe.</span><span class="sxs-lookup"><span data-stu-id="e4f3f-138">If using Windows Explorer, double-click the icon for PeripheralStatus.exe.</span></span>

    <span data-ttu-id="e4f3f-139">Откроется новое окно со связанной кнопкой панели задач.</span><span class="sxs-lookup"><span data-stu-id="e4f3f-139">A new window will open, with an associated taskbar button.</span></span>

2.  <span data-ttu-id="e4f3f-140">Чтобы продемонстрировать наложенные слои, выберите **Overlay 1** или **Overlay 2** в меню **состояния периферийных устройств** окна.</span><span class="sxs-lookup"><span data-stu-id="e4f3f-140">To demonstrate overlays, choose **Overlay 1** or **Overlay 2** from the window's **Peripheral Status** menu.</span></span> <span data-ttu-id="e4f3f-141">Выбранное наложение отображается на кнопке панели задач.</span><span class="sxs-lookup"><span data-stu-id="e4f3f-141">The chosen overlay appears on the taskbar button.</span></span> <span data-ttu-id="e4f3f-142">Чтобы удалить наложение, нажмите кнопку **очистить наложение**.</span><span class="sxs-lookup"><span data-stu-id="e4f3f-142">To remove the overlay, choose **Clear Overlay**.</span></span>
3.  <span data-ttu-id="e4f3f-143">Чтобы продемонстрировать индикатор выполнения, выберите пункт **имитировать ход выполнения** в меню **состояния периферийных устройств** окна.</span><span class="sxs-lookup"><span data-stu-id="e4f3f-143">To demonstrate the progress bar, choose **Simulate Progress** from the window's **Peripheral Status** menu.</span></span> <span data-ttu-id="e4f3f-144">Кнопка панели задач покажет индикатор неопределенного хода выполнения, а затем переключается на нормальный индикатор.</span><span class="sxs-lookup"><span data-stu-id="e4f3f-144">The taskbar button will show an indeterminate progress indicator then switch to a normal indicator.</span></span>
4.  <span data-ttu-id="e4f3f-145">Выберите **выход** в меню **файл** окна, чтобы завершить работу программы.</span><span class="sxs-lookup"><span data-stu-id="e4f3f-145">Choose **Exit** from the window's **File** menu to end the program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4f3f-146">См. также</span><span class="sxs-lookup"><span data-stu-id="e4f3f-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4f3f-147">Расширения панели задач</span><span class="sxs-lookup"><span data-stu-id="e4f3f-147">Taskbar Extensions</span></span>](taskbar-extensions.md)
</dt> </dl>

 

 



