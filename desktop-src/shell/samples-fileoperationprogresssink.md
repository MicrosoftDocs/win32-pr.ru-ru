---
description: Демонстрирует использование методов интерфейса Ифилеоператионпрогресссинк для мониторинга сведений о действиях интерфейса интерфейс IFileOperation.
title: Приемник данных о ходе выполнения файловой операции
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 196ABB75-1FE0-44f5-9060-59AAB4231567
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 60e3bde90da36a6122608b463b28df670f0d2a8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080953"
---
# <a name="file-operation-progress-sink"></a><span data-ttu-id="9341d-103">Приемник данных о ходе выполнения файловой операции</span><span class="sxs-lookup"><span data-stu-id="9341d-103">File Operation Progress Sink</span></span>

<span data-ttu-id="9341d-104">Демонстрирует использование методов интерфейса [**ифилеоператионпрогресссинк**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink) для мониторинга сведений о действиях интерфейса [**интерфейс IFileOperation**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation) .</span><span class="sxs-lookup"><span data-stu-id="9341d-104">Demonstrates how to use the [**IFileOperationProgressSink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink) interface methods for monitoring the details of [**IFileOperation**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation) interface actions.</span></span>

<span data-ttu-id="9341d-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="9341d-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9341d-106">Требования</span><span class="sxs-lookup"><span data-stu-id="9341d-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="9341d-107">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="9341d-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="9341d-108">Создание примера</span><span class="sxs-lookup"><span data-stu-id="9341d-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="9341d-109">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="9341d-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="9341d-110">Требования</span><span class="sxs-lookup"><span data-stu-id="9341d-110">Requirements</span></span>



| <span data-ttu-id="9341d-111">Продукт</span><span class="sxs-lookup"><span data-stu-id="9341d-111">Product</span></span>                                | <span data-ttu-id="9341d-112">Минимальная версия продукта</span><span class="sxs-lookup"><span data-stu-id="9341d-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="9341d-113">Windows</span><span class="sxs-lookup"><span data-stu-id="9341d-113">Windows</span></span>                                | <span data-ttu-id="9341d-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9341d-114">Windows Vista</span></span>           |
| <span data-ttu-id="9341d-115">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="9341d-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="9341d-116">6.1</span><span class="sxs-lookup"><span data-stu-id="9341d-116">6.1</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="9341d-117">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="9341d-117">Downloading the Sample</span></span>

| <span data-ttu-id="9341d-118">Расположение</span><span class="sxs-lookup"><span data-stu-id="9341d-118">Location</span></span>      | <span data-ttu-id="9341d-119">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="9341d-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9341d-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="9341d-120">GitHub</span></span>  | [<span data-ttu-id="9341d-121">Пример Филеоператионпрогресссинк</span><span class="sxs-lookup"><span data-stu-id="9341d-121">FileOperationProgressSink sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/FileOperationProgressSink) |

## <a name="building-the-sample"></a><span data-ttu-id="9341d-122">Построение образца</span><span class="sxs-lookup"><span data-stu-id="9341d-122">Building the Sample</span></span>

<span data-ttu-id="9341d-123">Чтобы построить образец из окна командной строки:</span><span class="sxs-lookup"><span data-stu-id="9341d-123">To build the sample from the command prompt window:</span></span>

1.  <span data-ttu-id="9341d-124">Откройте окно командной строки и перейдите в каталог проекта **филеоператионпрогресссинк** .</span><span class="sxs-lookup"><span data-stu-id="9341d-124">Open the command prompt window and navigate to the **FileOperationProgressSink** project directory.</span></span>
2.  <span data-ttu-id="9341d-125">Введите `msbuild FileOperationProgressSinkSample.sln`.</span><span class="sxs-lookup"><span data-stu-id="9341d-125">Enter `msbuild FileOperationProgressSinkSample.sln`.</span></span>

<span data-ttu-id="9341d-126">Чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):</span><span class="sxs-lookup"><span data-stu-id="9341d-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="9341d-127">Откройте проводник Windows и перейдите в каталог проекта **филесинусе** .</span><span class="sxs-lookup"><span data-stu-id="9341d-127">Open Windows Explorer and navigate to the **FilesInUse** project directory.</span></span> <span data-ttu-id="9341d-128">Например, полный путь установки по умолчанию — `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileOperationProgressSinkSample` .</span><span class="sxs-lookup"><span data-stu-id="9341d-128">For example, the full default installation path is `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileOperationProgressSinkSample`.</span></span>
2.  <span data-ttu-id="9341d-129">Дважды щелкните значок файла Филеоператионпрогресссинксампле. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9341d-129">Double-click the icon for the FileOperationProgressSinkSample.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="9341d-130">Расширение имени файла. sln не отображается в разделе Параметры папки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9341d-130">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="9341d-131">В этом случае его можно определить по его уникальному значку или описанию типа "Microsoft Visual Studio решение".</span><span class="sxs-lookup"><span data-stu-id="9341d-131">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="9341d-132">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="9341d-132">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="9341d-133">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="9341d-133">Running the Sample</span></span>

1.  <span data-ttu-id="9341d-134">Перейдите в каталог, содержащий новый исполняемый файл, с помощью окна командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="9341d-134">Navigate to the directory that contains the new executable, using the command prompt window or Windows Explorer.</span></span>
2.  <span data-ttu-id="9341d-135">В командной строке введите `FileOperationProgressSinkSample.exe` или в проводнике Windows дважды щелкните значок FileOperationProgressSinkSample.exe.</span><span class="sxs-lookup"><span data-stu-id="9341d-135">At the command prompt, enter `FileOperationProgressSinkSample.exe`, or from Windows Explorer, double-click the icon for FileOperationProgressSinkSample.exe.</span></span>

 

 



