---
description: Демонстрирует, как реализовать команду оболочки с помощью метода Дроптаржет.
title: 'Пример: команда DropTarget'
ms.topic: article
ms.date: 05/31/2018
ms.assetid: BEAD20C9-B01A-48aa-A85A-B7171383FBDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1f737c951c5bd588760dbb716859c04c0dc062fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985628"
---
# <a name="droptarget-verb-sample"></a><span data-ttu-id="a170f-103">Пример: команда DropTarget</span><span class="sxs-lookup"><span data-stu-id="a170f-103">DropTarget Verb Sample</span></span>

<span data-ttu-id="a170f-104">Демонстрирует, как реализовать команду оболочки с помощью метода Дроптаржет.</span><span class="sxs-lookup"><span data-stu-id="a170f-104">Demonstrates how to implement a Shell verb using the DropTarget method.</span></span>

<span data-ttu-id="a170f-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="a170f-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="a170f-106">Описание</span><span class="sxs-lookup"><span data-stu-id="a170f-106">Description</span></span>](#description)
-   [<span data-ttu-id="a170f-107">Требования</span><span class="sxs-lookup"><span data-stu-id="a170f-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="a170f-108">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="a170f-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="a170f-109">Создание примера</span><span class="sxs-lookup"><span data-stu-id="a170f-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="a170f-110">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="a170f-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="a170f-111">Описание</span><span class="sxs-lookup"><span data-stu-id="a170f-111">Description</span></span>

<span data-ttu-id="a170f-112">В этом примере показано, как реализовать команду оболочки с помощью метода Дроптаржет.</span><span class="sxs-lookup"><span data-stu-id="a170f-112">This sample shows how to implement a Shell verb using the DropTarget method.</span></span> <span data-ttu-id="a170f-113">Этот метод является предпочтительным для реализаций команд, которые должны работать в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a170f-113">This method is preferred for verb implementations that must work on Windows XP.</span></span> <span data-ttu-id="a170f-114">В этом примере реализуется изолированный объект модели COM, но предполагается, что реализация глагола будет интегрирована в существующие приложения.</span><span class="sxs-lookup"><span data-stu-id="a170f-114">This sample implements a standalone local server Component Object Model (COM) object but it is expected that the verb implementation will be integrated into existing applications.</span></span> <span data-ttu-id="a170f-115">Для этого основной объект приложения регистрирует фабрику класса для себя.</span><span class="sxs-lookup"><span data-stu-id="a170f-115">To do so, your main application object registers a class factory for itself.</span></span> <span data-ttu-id="a170f-116">Этот объект реализует [**интерфейс IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) для команд приложения.</span><span class="sxs-lookup"><span data-stu-id="a170f-116">That object implements [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) for your application's verbs.</span></span> <span data-ttu-id="a170f-117">Обратите внимание, что COM запускает приложение, если оно еще не запущено, но подключается к работающему экземпляру приложения, если оно существует.</span><span class="sxs-lookup"><span data-stu-id="a170f-117">Note that COM launches your application if it is not already running but connects to a running instance of your application if one is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="a170f-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a170f-118">Requirements</span></span>



| <span data-ttu-id="a170f-119">Продукт</span><span class="sxs-lookup"><span data-stu-id="a170f-119">Product</span></span>                                | <span data-ttu-id="a170f-120">Минимальная версия продукта</span><span class="sxs-lookup"><span data-stu-id="a170f-120">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="a170f-121">Windows</span><span class="sxs-lookup"><span data-stu-id="a170f-121">Windows</span></span>                                | <span data-ttu-id="a170f-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a170f-122">Windows Vista</span></span>           |
| <span data-ttu-id="a170f-123">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="a170f-123">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="a170f-124">7.0</span><span class="sxs-lookup"><span data-stu-id="a170f-124">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="a170f-125">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="a170f-125">Downloading the Sample</span></span>

| <span data-ttu-id="a170f-126">Расположение</span><span class="sxs-lookup"><span data-stu-id="a170f-126">Location</span></span>      | <span data-ttu-id="a170f-127">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="a170f-127">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a170f-128">GitHub</span><span class="sxs-lookup"><span data-stu-id="a170f-128">GitHub</span></span>  | [<span data-ttu-id="a170f-129">Пример Дроптаржетверб</span><span class="sxs-lookup"><span data-stu-id="a170f-129">DropTargetVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/DropTargetVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="a170f-130">Построение образца</span><span class="sxs-lookup"><span data-stu-id="a170f-130">Building the Sample</span></span>

<span data-ttu-id="a170f-131">Чтобы построить образец из командной строки, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="a170f-131">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="a170f-132">Откройте окно командной строки и перейдите в каталог проекта **дроптаржетверб** .</span><span class="sxs-lookup"><span data-stu-id="a170f-132">Open the command prompt window and navigate to the **DropTargetVerb** project directory.</span></span>
2.  <span data-ttu-id="a170f-133">Введите `msbuild DropTargetVerb.sln`.</span><span class="sxs-lookup"><span data-stu-id="a170f-133">Enter `msbuild DropTargetVerb.sln`.</span></span>

<span data-ttu-id="a170f-134">Чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):</span><span class="sxs-lookup"><span data-stu-id="a170f-134">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="a170f-135">Откройте проводник Windows и перейдите в каталог проекта **дроптаржетверб** .</span><span class="sxs-lookup"><span data-stu-id="a170f-135">Open Windows Explorer and navigate to the **DropTargetVerb** project directory.</span></span>
2.  <span data-ttu-id="a170f-136">Дважды щелкните значок файла Дроптаржетверб. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a170f-136">Double-click the icon for the DropTargetVerb.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="a170f-137">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="a170f-137">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="a170f-138">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="a170f-138">Running the Sample</span></span>

1.  <span data-ttu-id="a170f-139">Перейдите в каталог, содержащий новый исполняемый файл, с помощью командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="a170f-139">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="a170f-140">В командной строке введите `DropTargetVerb.exe` .</span><span class="sxs-lookup"><span data-stu-id="a170f-140">At the command line, enter `DropTargetVerb.exe`.</span></span> <span data-ttu-id="a170f-141">Кроме того, в проводнике Windows дважды щелкните значок DropTargetVerb.exe.</span><span class="sxs-lookup"><span data-stu-id="a170f-141">Alternatively, from Windows Explorer double-click the icon for DropTargetVerb.exe.</span></span>
3.  <span data-ttu-id="a170f-142">Следуйте инструкциям в отображаемом диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="a170f-142">Follow the instructions in the displayed dialog</span></span>

 

 
