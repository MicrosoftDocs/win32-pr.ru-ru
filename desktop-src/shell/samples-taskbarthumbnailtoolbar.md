---
description: Демонстрируется панель инструментов эскизов, активный элемент управления ToolBar, внедренный в предварительный просмотр эскизов окна, который используется для предоставления доступа к ключевым командам окна без выполнения восстановления пользователем или активации окна приложения.
title: 'Пример: панель инструментов эскизов на панели задач'
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4936FF67-19EE-4963-BE4C-3D40350C64A9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e61208f15772a43138e6cd7a38fd6327445bdfa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985821"
---
# <a name="taskbar-thumbnail-toolbar-sample"></a><span data-ttu-id="eba67-103">Пример: панель инструментов эскизов на панели задач</span><span class="sxs-lookup"><span data-stu-id="eba67-103">Taskbar Thumbnail Toolbar Sample</span></span>

<span data-ttu-id="eba67-104">Демонстрируется панель инструментов эскизов, активный элемент управления ToolBar, внедренный в предварительный просмотр эскизов окна, который используется для предоставления доступа к ключевым командам окна без выполнения восстановления пользователем или активации окна приложения.</span><span class="sxs-lookup"><span data-stu-id="eba67-104">Demonstrates a thumbnail toolbar, an active toolbar control embedded in a window's thumbnail preview, used to provide access to a window's key commands without making the user restore or activate the application's window.</span></span>

<span data-ttu-id="eba67-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="eba67-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="eba67-106">Описание</span><span class="sxs-lookup"><span data-stu-id="eba67-106">Description</span></span>](#description)
-   [<span data-ttu-id="eba67-107">Требования</span><span class="sxs-lookup"><span data-stu-id="eba67-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="eba67-108">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="eba67-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="eba67-109">Создание примера</span><span class="sxs-lookup"><span data-stu-id="eba67-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="eba67-110">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="eba67-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="eba67-111">См. также</span><span class="sxs-lookup"><span data-stu-id="eba67-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="eba67-112">Описание</span><span class="sxs-lookup"><span data-stu-id="eba67-112">Description</span></span>

<span data-ttu-id="eba67-113">В этом примере показано, как предоставить простую панель инструментов для предварительного просмотра эскизов панели задач.</span><span class="sxs-lookup"><span data-stu-id="eba67-113">This sample shows how to provide a simple toolbar to a taskbar thumbnail preview.</span></span> <span data-ttu-id="eba67-114">Панель инструментов состоит из трех кнопок.</span><span class="sxs-lookup"><span data-stu-id="eba67-114">The toolbar consists of three buttons.</span></span> <span data-ttu-id="eba67-115">При нажатии кнопки отображается окно подтверждения активации кнопки.</span><span class="sxs-lookup"><span data-stu-id="eba67-115">Clicking a button displays a window to confirm that the button was activated.</span></span> <span data-ttu-id="eba67-116">Демонстрируются следующие интерфейсы API:</span><span class="sxs-lookup"><span data-stu-id="eba67-116">The following APIs are demonstrated:</span></span>

-   [<span data-ttu-id="eba67-117">**ITaskbarList3:: Сумббараддбуттонс**</span><span class="sxs-lookup"><span data-stu-id="eba67-117">**ITaskbarList3::ThumbBarAddButtons**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbaraddbuttons)
-   [<span data-ttu-id="eba67-118">**ITaskbarList3:: Сумббарсетимажелист**</span><span class="sxs-lookup"><span data-stu-id="eba67-118">**ITaskbarList3::ThumbBarSetImageList**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarsetimagelist)
-   <span data-ttu-id="eba67-119">Структура [**сумббуттон**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton)</span><span class="sxs-lookup"><span data-stu-id="eba67-119">[**THUMBBUTTON**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton) structure</span></span>

## <a name="requirements"></a><span data-ttu-id="eba67-120">Требования</span><span class="sxs-lookup"><span data-stu-id="eba67-120">Requirements</span></span>



| <span data-ttu-id="eba67-121">Продукт</span><span class="sxs-lookup"><span data-stu-id="eba67-121">Product</span></span>                                | <span data-ttu-id="eba67-122">Минимальная версия продукта</span><span class="sxs-lookup"><span data-stu-id="eba67-122">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="eba67-123">Windows</span><span class="sxs-lookup"><span data-stu-id="eba67-123">Windows</span></span>                                | <span data-ttu-id="eba67-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="eba67-124">Windows 7</span></span>               |
| <span data-ttu-id="eba67-125">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="eba67-125">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="eba67-126">7.0</span><span class="sxs-lookup"><span data-stu-id="eba67-126">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="eba67-127">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="eba67-127">Downloading the Sample</span></span>

| <span data-ttu-id="eba67-128">Расположение</span><span class="sxs-lookup"><span data-stu-id="eba67-128">Location</span></span>      | <span data-ttu-id="eba67-129">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="eba67-129">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eba67-130">GitHub</span><span class="sxs-lookup"><span data-stu-id="eba67-130">GitHub</span></span>  | [<span data-ttu-id="eba67-131">Пример Таскбарсумбнаилтулбар</span><span class="sxs-lookup"><span data-stu-id="eba67-131">TaskbarThumbnailToolbar sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TaskbarThumbnailToolbar) |

## <a name="building-the-sample"></a><span data-ttu-id="eba67-132">Построение образца</span><span class="sxs-lookup"><span data-stu-id="eba67-132">Building the Sample</span></span>

<span data-ttu-id="eba67-133">Чтобы построить образец из командной строки, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="eba67-133">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="eba67-134">Откройте окно командной строки и перейдите в каталог проекта **таскбарсумбнаилтулбар** .</span><span class="sxs-lookup"><span data-stu-id="eba67-134">Open the command prompt window and navigate to the **TaskbarThumbnailToolbar** project directory.</span></span>
2.  <span data-ttu-id="eba67-135">Введите `msbuild ThumbnailToolbar.sln`.</span><span class="sxs-lookup"><span data-stu-id="eba67-135">Enter `msbuild ThumbnailToolbar.sln`.</span></span>

<span data-ttu-id="eba67-136">Чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):</span><span class="sxs-lookup"><span data-stu-id="eba67-136">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="eba67-137">Откройте проводник Windows и перейдите в каталог проекта **таскбарсумбнаилтулбар** .</span><span class="sxs-lookup"><span data-stu-id="eba67-137">Open Windows Explorer and navigate to the **TaskbarThumbnailToolbar** project directory.</span></span>
2.  <span data-ttu-id="eba67-138">Дважды щелкните значок файла Сумбнаилтулбар. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="eba67-138">Double-click the icon for the ThumbnailToolbar.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="eba67-139">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="eba67-139">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="eba67-140">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="eba67-140">Running the Sample</span></span>

1.  <span data-ttu-id="eba67-141">Перейдите в каталог, содержащий новый исполняемый файл (например, `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarThumbnailToolbar\Debug` ), с помощью командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="eba67-141">Navigate to the directory that contains the new executable file (for instance, `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarThumbnailToolbar\Debug`), using the command prompt or Windows Explorer.</span></span>

    -   <span data-ttu-id="eba67-142">При использовании командной строки введите `ThumbnailToolbar.exe` .</span><span class="sxs-lookup"><span data-stu-id="eba67-142">If using the command line, enter `ThumbnailToolbar.exe`.</span></span>
    -   <span data-ttu-id="eba67-143">Если используется проводник Windows, дважды щелкните значок для ThumbnailToolbar.exe.</span><span class="sxs-lookup"><span data-stu-id="eba67-143">If using Windows Explorer, double-click the icon for ThumbnailToolbar.exe.</span></span>

    <span data-ttu-id="eba67-144">Откроется новое окно со связанной кнопкой панели задач.</span><span class="sxs-lookup"><span data-stu-id="eba67-144">A new window will open, with an associated taskbar button.</span></span>

2.  <span data-ttu-id="eba67-145">Наведите указатель мыши на кнопку **сумбнаилтулбар** на панели задач, чтобы отображалось окно предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="eba67-145">Hover the cursor over the **ThumbnailToolbar** taskbar button so that the preview displays.</span></span> <span data-ttu-id="eba67-146">Щелкните одну из трех кнопок (зеленый, желтый, красный), показанную на панели инструментов предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="eba67-146">Click one of the three buttons (green, yellow, red) shown in the preview's toolbar.</span></span>
3.  <span data-ttu-id="eba67-147">Выберите **выход** в меню **файл** окна, чтобы завершить работу программы.</span><span class="sxs-lookup"><span data-stu-id="eba67-147">Choose **Exit** from the window's **File** menu to end the program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eba67-148">См. также</span><span class="sxs-lookup"><span data-stu-id="eba67-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eba67-149">Расширения панели задач</span><span class="sxs-lookup"><span data-stu-id="eba67-149">Taskbar Extensions</span></span>](taskbar-extensions.md)
</dt> </dl>

 

 



