---
description: Демонстрирует, как реализовать команду оболочки с помощью метода CreateProcess.
title: 'Пример: команда CreateProcess'
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2939BC36-35C0-4549-9971-742CBDA02547
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8e52f251e12f0ca06bcb729407a7c8303836f9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985825"
---
# <a name="createprocess-verb-sample"></a><span data-ttu-id="14a3d-103">Пример: команда CreateProcess</span><span class="sxs-lookup"><span data-stu-id="14a3d-103">CreateProcess Verb Sample</span></span>

<span data-ttu-id="14a3d-104">Демонстрирует, как реализовать команду оболочки с помощью метода CreateProcess.</span><span class="sxs-lookup"><span data-stu-id="14a3d-104">Demonstrates how to implement a Shell verb using the CreateProcess method.</span></span>

<span data-ttu-id="14a3d-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="14a3d-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="14a3d-106">Описание</span><span class="sxs-lookup"><span data-stu-id="14a3d-106">Description</span></span>](#description)
-   [<span data-ttu-id="14a3d-107">Требования</span><span class="sxs-lookup"><span data-stu-id="14a3d-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="14a3d-108">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="14a3d-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="14a3d-109">Создание примера</span><span class="sxs-lookup"><span data-stu-id="14a3d-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="14a3d-110">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="14a3d-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="14a3d-111">Описание</span><span class="sxs-lookup"><span data-stu-id="14a3d-111">Description</span></span>

<span data-ttu-id="14a3d-112">Команды на основе CreateProcess зависят от запуска исполняемого файла и передачи ему аргумента командной строки.</span><span class="sxs-lookup"><span data-stu-id="14a3d-112">CreateProcess-based verbs depend on running a executable and passing it a command-line argument.</span></span> <span data-ttu-id="14a3d-113">Этот метод не так эффективен, как методы Дроптаржет и ExecuteCommand, но он обеспечивает желаемое поведение вне процесса.</span><span class="sxs-lookup"><span data-stu-id="14a3d-113">This method is not as powerful as the DropTarget and ExecuteCommand methods but it does achieve the desirable out-of-process behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="14a3d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="14a3d-114">Requirements</span></span>



| <span data-ttu-id="14a3d-115">Продукт</span><span class="sxs-lookup"><span data-stu-id="14a3d-115">Product</span></span>                                | <span data-ttu-id="14a3d-116">Минимальная версия продукта</span><span class="sxs-lookup"><span data-stu-id="14a3d-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="14a3d-117">Windows</span><span class="sxs-lookup"><span data-stu-id="14a3d-117">Windows</span></span>                                | <span data-ttu-id="14a3d-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="14a3d-118">Windows Vista</span></span>           |
| <span data-ttu-id="14a3d-119">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="14a3d-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="14a3d-120">7.0</span><span class="sxs-lookup"><span data-stu-id="14a3d-120">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="14a3d-121">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="14a3d-121">Downloading the Sample</span></span>

| <span data-ttu-id="14a3d-122">Расположение</span><span class="sxs-lookup"><span data-stu-id="14a3d-122">Location</span></span>      | <span data-ttu-id="14a3d-123">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="14a3d-123">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14a3d-124">GitHub</span><span class="sxs-lookup"><span data-stu-id="14a3d-124">GitHub</span></span>  | [<span data-ttu-id="14a3d-125">Пример Креатепроцессверб</span><span class="sxs-lookup"><span data-stu-id="14a3d-125">CreateProcessVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CreateProcessVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="14a3d-126">Построение образца</span><span class="sxs-lookup"><span data-stu-id="14a3d-126">Building the Sample</span></span>

<span data-ttu-id="14a3d-127">Чтобы построить образец из командной строки, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="14a3d-127">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="14a3d-128">Откройте окно командной строки и перейдите в каталог проекта **креатепроцессверб** .</span><span class="sxs-lookup"><span data-stu-id="14a3d-128">Open the command prompt window and navigate to the **CreateProcessVerb** project directory.</span></span>
2.  <span data-ttu-id="14a3d-129">Введите `msbuild CreateProcessVerb.sln`.</span><span class="sxs-lookup"><span data-stu-id="14a3d-129">Enter `msbuild CreateProcessVerb.sln`.</span></span>

<span data-ttu-id="14a3d-130">Чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):</span><span class="sxs-lookup"><span data-stu-id="14a3d-130">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="14a3d-131">Откройте проводник Windows и перейдите в каталог проекта **креатепроцессверб** .</span><span class="sxs-lookup"><span data-stu-id="14a3d-131">Open Windows Explorer and navigate to the **CreateProcessVerb** project directory.</span></span>
2.  <span data-ttu-id="14a3d-132">Дважды щелкните значок файла Креатепроцессверб. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="14a3d-132">Double-click the icon for the CreateProcessVerb.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="14a3d-133">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="14a3d-133">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="14a3d-134">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="14a3d-134">Running the Sample</span></span>

1.  <span data-ttu-id="14a3d-135">Перейдите в каталог, содержащий новый исполняемый файл, с помощью командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="14a3d-135">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="14a3d-136">В командной строке введите `CreateProcessVerb.exe` .</span><span class="sxs-lookup"><span data-stu-id="14a3d-136">At the command line, enter `CreateProcessVerb.exe`.</span></span> <span data-ttu-id="14a3d-137">Кроме того, в проводнике Windows дважды щелкните значок CreateProcessVerb.exe.</span><span class="sxs-lookup"><span data-stu-id="14a3d-137">Alternatively, from Windows Explorer double-click the icon for CreateProcessVerb.exe.</span></span>
3.  <span data-ttu-id="14a3d-138">Следуйте инструкциям в отображаемом диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="14a3d-138">Follow the instructions in the displayed dialog</span></span>

 

 



