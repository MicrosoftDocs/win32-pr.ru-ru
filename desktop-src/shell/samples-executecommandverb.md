---
description: Демонстрирует, как реализовать команду оболочки с помощью метода ExecuteCommand.
title: 'Пример: выполнение команды'
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0418318A-3E62-4690-AFB3-9B4A391C537E
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 2deeb63fc6648d07b3d870888d6d2eabc6fb0490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272973"
---
# <a name="execute-command-verb-sample"></a><span data-ttu-id="e6e54-103">Пример: выполнение команды</span><span class="sxs-lookup"><span data-stu-id="e6e54-103">Execute Command Verb Sample</span></span>

<span data-ttu-id="e6e54-104">Демонстрирует, как реализовать команду оболочки с помощью метода ExecuteCommand.</span><span class="sxs-lookup"><span data-stu-id="e6e54-104">Demonstrates how to implement a Shell verb using the ExecuteCommand method.</span></span>

<span data-ttu-id="e6e54-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="e6e54-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="e6e54-106">Описание</span><span class="sxs-lookup"><span data-stu-id="e6e54-106">Description</span></span>](#description)
-   [<span data-ttu-id="e6e54-107">Требования</span><span class="sxs-lookup"><span data-stu-id="e6e54-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="e6e54-108">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="e6e54-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="e6e54-109">Создание примера</span><span class="sxs-lookup"><span data-stu-id="e6e54-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="e6e54-110">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="e6e54-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="e6e54-111">Описание</span><span class="sxs-lookup"><span data-stu-id="e6e54-111">Description</span></span>

<span data-ttu-id="e6e54-112">Этот метод является предпочтительным для реализации команд, так как он обеспечивает наибольшую гибкость, прост и поддерживает незавершенную активацию.</span><span class="sxs-lookup"><span data-stu-id="e6e54-112">This method is preferred for verb implementations because it provides the most flexibility, is simple, and supports out-of-process activation.</span></span> <span data-ttu-id="e6e54-113">В этом примере реализуется изолированный объект серверной модели COM, но предполагается, что реализация команды будет интегрирована в существующие приложения.</span><span class="sxs-lookup"><span data-stu-id="e6e54-113">This sample implements a standalone, local server Component Object Model (COM) object, but it is expected that the verb implementation will be integrated into existing applications.</span></span> <span data-ttu-id="e6e54-114">Для этого основной объект приложения должен зарегистрировать фабрику класса для себя.</span><span class="sxs-lookup"><span data-stu-id="e6e54-114">To do so, your main application object must register a class factory for itself.</span></span> <span data-ttu-id="e6e54-115">Этот объект реализует [**интерфейс IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) для команд приложения.</span><span class="sxs-lookup"><span data-stu-id="e6e54-115">That object implements [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) for your application's verbs.</span></span> <span data-ttu-id="e6e54-116">Обратите внимание, что COM запускает приложение, если оно еще не запущено, но подключается к работающему экземпляру приложения, если оно существует.</span><span class="sxs-lookup"><span data-stu-id="e6e54-116">Note that COM launches your application if it is not already running but connects to a running instance of your application if one is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6e54-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e6e54-117">Requirements</span></span>



| <span data-ttu-id="e6e54-118">Продукт</span><span class="sxs-lookup"><span data-stu-id="e6e54-118">Product</span></span>                                | <span data-ttu-id="e6e54-119">Минимальная версия продукта</span><span class="sxs-lookup"><span data-stu-id="e6e54-119">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="e6e54-120">Windows</span><span class="sxs-lookup"><span data-stu-id="e6e54-120">Windows</span></span>                                | <span data-ttu-id="e6e54-121">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e6e54-121">Windows 7</span></span>               |
| <span data-ttu-id="e6e54-122">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="e6e54-122">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="e6e54-123">7.0</span><span class="sxs-lookup"><span data-stu-id="e6e54-123">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="e6e54-124">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="e6e54-124">Downloading the Sample</span></span>

| <span data-ttu-id="e6e54-125">Расположение</span><span class="sxs-lookup"><span data-stu-id="e6e54-125">Location</span></span>      | <span data-ttu-id="e6e54-126">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="e6e54-126">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6e54-127">GitHub</span><span class="sxs-lookup"><span data-stu-id="e6e54-127">GitHub</span></span>  | [<span data-ttu-id="e6e54-128">Пример Ексекутекоммандверб</span><span class="sxs-lookup"><span data-stu-id="e6e54-128">ExecuteCommandVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/ExecuteCommandVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="e6e54-129">Построение образца</span><span class="sxs-lookup"><span data-stu-id="e6e54-129">Building the Sample</span></span>

<span data-ttu-id="e6e54-130">Чтобы построить образец из командной строки, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e6e54-130">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="e6e54-131">Откройте окно командной строки и перейдите в каталог проекта **ексекутекоммандверб** .</span><span class="sxs-lookup"><span data-stu-id="e6e54-131">Open the command prompt window and navigate to the **ExecuteCommandVerb** project directory.</span></span>
2.  <span data-ttu-id="e6e54-132">Введите `msbuild ExecuteCommand.sln`.</span><span class="sxs-lookup"><span data-stu-id="e6e54-132">Enter `msbuild ExecuteCommand.sln`.</span></span>

<span data-ttu-id="e6e54-133">Чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):</span><span class="sxs-lookup"><span data-stu-id="e6e54-133">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="e6e54-134">Откройте проводник Windows и перейдите в каталог проекта **ексекутекоммандверб** .</span><span class="sxs-lookup"><span data-stu-id="e6e54-134">Open Windows Explorer and navigate to the **ExecuteCommandVerb** project directory.</span></span>
2.  <span data-ttu-id="e6e54-135">Дважды щелкните значок файла ExecuteCommand. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e6e54-135">Double-click the icon for the ExecuteCommand.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="e6e54-136">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="e6e54-136">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="e6e54-137">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="e6e54-137">Running the Sample</span></span>

1.  <span data-ttu-id="e6e54-138">Перейдите в каталог, содержащий новый исполняемый файл, с помощью командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="e6e54-138">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="e6e54-139">В командной строке введите `ExecuteCommand.exe` .</span><span class="sxs-lookup"><span data-stu-id="e6e54-139">At the command line, enter `ExecuteCommand.exe`.</span></span> <span data-ttu-id="e6e54-140">Кроме того, в проводнике Windows дважды щелкните значок ExecuteCommand.exe.</span><span class="sxs-lookup"><span data-stu-id="e6e54-140">Alternatively, from Windows Explorer double-click the icon for ExecuteCommand.exe.</span></span>
3.  <span data-ttu-id="e6e54-141">Следуйте инструкциям в отображаемом диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="e6e54-141">Follow the instructions in the displayed dialog</span></span>

 

 
