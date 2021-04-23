---
description: Демонстрируется настройка диалогового окна "файл в использовании" для отображения дополнительных сведений и параметров для файлов, открытых в данный момент в приложении.
title: 'Пример: файл используется'
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 22EFE7CC-D223-46b3-BD6B-293E3FA0BA01
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 223e0addf201f3526654a17346963b4639e0d215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345925"
---
# <a name="file-is-in-use-sample"></a><span data-ttu-id="cdfb5-103">Пример: файл используется</span><span class="sxs-lookup"><span data-stu-id="cdfb5-103">File Is In Use Sample</span></span>

<span data-ttu-id="cdfb5-104">Демонстрируется настройка диалогового окна " **файл в использовании** " для отображения дополнительных сведений и параметров для файлов, открытых в данный момент в приложении.</span><span class="sxs-lookup"><span data-stu-id="cdfb5-104">Demonstrates how to customize the **File In Use** dialog to display additional information and options for files that are currently opened in the application.</span></span>

<span data-ttu-id="cdfb5-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="cdfb5-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="cdfb5-106">Требования</span><span class="sxs-lookup"><span data-stu-id="cdfb5-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="cdfb5-107">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="cdfb5-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="cdfb5-108">Создание примера</span><span class="sxs-lookup"><span data-stu-id="cdfb5-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="cdfb5-109">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="cdfb5-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="cdfb5-110">Требования</span><span class="sxs-lookup"><span data-stu-id="cdfb5-110">Requirements</span></span>



| <span data-ttu-id="cdfb5-111">Продукт</span><span class="sxs-lookup"><span data-stu-id="cdfb5-111">Product</span></span>                                | <span data-ttu-id="cdfb5-112">Минимальная версия продукта</span><span class="sxs-lookup"><span data-stu-id="cdfb5-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="cdfb5-113">Windows</span><span class="sxs-lookup"><span data-stu-id="cdfb5-113">Windows</span></span>                                | <span data-ttu-id="cdfb5-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cdfb5-114">Windows Vista</span></span>           |
| <span data-ttu-id="cdfb5-115">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="cdfb5-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="cdfb5-116">6.1</span><span class="sxs-lookup"><span data-stu-id="cdfb5-116">6.1</span></span>                     |



 

<span data-ttu-id="cdfb5-117">Дополнительные требования см. в файле Ифилеисинусе \_sample.docx, прилагаемом к примеру.</span><span class="sxs-lookup"><span data-stu-id="cdfb5-117">For additional requirements, see the IFileIsInUse\_sample.docx file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="cdfb5-118">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="cdfb5-118">Downloading the Sample</span></span>

| <span data-ttu-id="cdfb5-119">Расположение</span><span class="sxs-lookup"><span data-stu-id="cdfb5-119">Location</span></span>      | <span data-ttu-id="cdfb5-120">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="cdfb5-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdfb5-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="cdfb5-121">GitHub</span></span>  | [<span data-ttu-id="cdfb5-122">Пример Филеисинусе</span><span class="sxs-lookup"><span data-stu-id="cdfb5-122">FileIsInUse sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/fileisinuse) |

## <a name="building-the-sample"></a><span data-ttu-id="cdfb5-123">Построение образца</span><span class="sxs-lookup"><span data-stu-id="cdfb5-123">Building the Sample</span></span>

<span data-ttu-id="cdfb5-124">Чтобы построить образец из окна командной строки:</span><span class="sxs-lookup"><span data-stu-id="cdfb5-124">To build the sample from the Command Prompt window:</span></span>

1.  <span data-ttu-id="cdfb5-125">Откройте окно командной строки и перейдите в каталог проекта **филеисинусе** .</span><span class="sxs-lookup"><span data-stu-id="cdfb5-125">Open the Command Prompt window and navigate to the **FileIsInUse** project directory.</span></span>
2.  <span data-ttu-id="cdfb5-126">Введите `msbuild FileIsInUse.sln`.</span><span class="sxs-lookup"><span data-stu-id="cdfb5-126">Enter `msbuild FileIsInUse.sln`.</span></span>

<span data-ttu-id="cdfb5-127">Чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):</span><span class="sxs-lookup"><span data-stu-id="cdfb5-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="cdfb5-128">Откройте проводник Windows и перейдите в каталог проекта **филесинусе** .</span><span class="sxs-lookup"><span data-stu-id="cdfb5-128">Open Windows Explorer and navigate to the **FilesInUse** project directory.</span></span> <span data-ttu-id="cdfb5-129">Например, полный путь установки по умолчанию — `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileIsInUse` .</span><span class="sxs-lookup"><span data-stu-id="cdfb5-129">For example, the full default installation path is `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileIsInUse`.</span></span>
2.  <span data-ttu-id="cdfb5-130">Дважды щелкните значок файла Филеисинусесампле. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="cdfb5-130">Double-click the icon for the FileIsInUseSample.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="cdfb5-131">Расширение имени файла. sln не отображается в разделе Параметры папки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cdfb5-131">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="cdfb5-132">В этом случае его можно определить по его уникальному значку или описанию типа "Microsoft Visual Studio решение".</span><span class="sxs-lookup"><span data-stu-id="cdfb5-132">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="cdfb5-133">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="cdfb5-133">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="cdfb5-134">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="cdfb5-134">Running the Sample</span></span>

1.  <span data-ttu-id="cdfb5-135">Перейдите в каталог, содержащий новый исполняемый файл, с помощью окна командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="cdfb5-135">Navigate to the directory that contains the new executable, using the command prompt window or Windows Explorer.</span></span>
2.  <span data-ttu-id="cdfb5-136">В командной строке введите `FileIsInUseSample.exe` или в проводнике Windows дважды щелкните значок FileIsInUseSample.exe.</span><span class="sxs-lookup"><span data-stu-id="cdfb5-136">At the command prompt, enter `FileIsInUseSample.exe`, or from Windows Explorer, double-click the icon for FileIsInUseSample.exe.</span></span>

<span data-ttu-id="cdfb5-137">Подробные сведения об этом примере кода см. в файле Ифилеисинусе \_sample.docx, прилагаемом к примеру.</span><span class="sxs-lookup"><span data-stu-id="cdfb5-137">For detailed information about this code sample, see the IFileIsInUse\_sample.docx file included with the sample.</span></span>

 

 



