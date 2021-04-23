---
description: Демонстрирует, как реализовать команду оболочки с помощью методов Експлореркомманд и Експлореркоммандстате.
title: 'Пример: команда в проводнике'
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2310A6AA-EAF9-4d7a-A784-04931BDC2089
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a35662c3df0e0fcddae049ccfaac2d9e3e265ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912923"
---
# <a name="explorer-command-verb-sample"></a><span data-ttu-id="58a3d-103">Пример: команда в проводнике</span><span class="sxs-lookup"><span data-stu-id="58a3d-103">Explorer Command Verb Sample</span></span>

<span data-ttu-id="58a3d-104">Демонстрирует, как реализовать команду оболочки с помощью методов Експлореркомманд и Експлореркоммандстате.</span><span class="sxs-lookup"><span data-stu-id="58a3d-104">Demonstrates how to implement a Shell verb using the ExplorerCommand and ExplorerCommandState methods.</span></span>

<span data-ttu-id="58a3d-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="58a3d-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="58a3d-106">Требования</span><span class="sxs-lookup"><span data-stu-id="58a3d-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="58a3d-107">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="58a3d-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="58a3d-108">Создание примера</span><span class="sxs-lookup"><span data-stu-id="58a3d-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="58a3d-109">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="58a3d-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="58a3d-110">Требования</span><span class="sxs-lookup"><span data-stu-id="58a3d-110">Requirements</span></span>



| <span data-ttu-id="58a3d-111">Продукт</span><span class="sxs-lookup"><span data-stu-id="58a3d-111">Product</span></span>                                | <span data-ttu-id="58a3d-112">Минимальная версия продукта</span><span class="sxs-lookup"><span data-stu-id="58a3d-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="58a3d-113">Windows</span><span class="sxs-lookup"><span data-stu-id="58a3d-113">Windows</span></span>                                | <span data-ttu-id="58a3d-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58a3d-114">Windows Vista</span></span>           |
| <span data-ttu-id="58a3d-115">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="58a3d-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="58a3d-116">7.0</span><span class="sxs-lookup"><span data-stu-id="58a3d-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="58a3d-117">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="58a3d-117">Downloading the Sample</span></span>

| <span data-ttu-id="58a3d-118">Расположение</span><span class="sxs-lookup"><span data-stu-id="58a3d-118">Location</span></span>      | <span data-ttu-id="58a3d-119">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="58a3d-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58a3d-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="58a3d-120">GitHub</span></span>  | [<span data-ttu-id="58a3d-121">Пример Експлореркоммандверб</span><span class="sxs-lookup"><span data-stu-id="58a3d-121">ExplorerCommandVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/ExplorerCommandVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="58a3d-122">Построение образца</span><span class="sxs-lookup"><span data-stu-id="58a3d-122">Building the Sample</span></span>

<span data-ttu-id="58a3d-123">Чтобы построить образец из командной строки, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="58a3d-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="58a3d-124">Откройте окно командной строки и перейдите в каталог проекта **експлореркоммандверб** .</span><span class="sxs-lookup"><span data-stu-id="58a3d-124">Open the command prompt window and navigate to the **ExplorerCommandVerb** project directory.</span></span>
2.  <span data-ttu-id="58a3d-125">Введите `msbuild ExplorerCommandVerb.sln`.</span><span class="sxs-lookup"><span data-stu-id="58a3d-125">Enter `msbuild ExplorerCommandVerb.sln`.</span></span>

<span data-ttu-id="58a3d-126">Чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):</span><span class="sxs-lookup"><span data-stu-id="58a3d-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="58a3d-127">Откройте проводник Windows и перейдите в каталог проекта **експлореркоммандверб** .</span><span class="sxs-lookup"><span data-stu-id="58a3d-127">Open Windows Explorer and navigate to the **ExplorerCommandVerb** project directory.</span></span>
2.  <span data-ttu-id="58a3d-128">Дважды щелкните значок файла Експлореркоммандверб. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="58a3d-128">Double-click the icon for the ExplorerCommandVerb.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="58a3d-129">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="58a3d-129">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="58a3d-130">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="58a3d-130">Running the Sample</span></span>

1.  <span data-ttu-id="58a3d-131">Перейдите в каталог, содержащий ExplorerCommandVerb.dll, с помощью командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="58a3d-131">Navigate to the directory that contains the ExplorerCommandVerb.dll, using the command prompt or Windows Explorer.</span></span> <span data-ttu-id="58a3d-132">Убедитесь, что используется 64-разрядный файл DLL в 64-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="58a3d-132">Make sure you use the 64-bit DLL file on 64-bit Windows.</span></span>
2.  <span data-ttu-id="58a3d-133">В командной строке введите `regsvr32.exe ExplorerCommandVerb.dll` .</span><span class="sxs-lookup"><span data-stu-id="58a3d-133">At the command line, enter `regsvr32.exe ExplorerCommandVerb.dll`.</span></span>
3.  <span data-ttu-id="58a3d-134">Если щелкнуть правой кнопкой мыши txt-файл, в контекстном меню будут отображаться две новые команды.</span><span class="sxs-lookup"><span data-stu-id="58a3d-134">Two new verbs will be shown on the context menu when you right-click a .txt file.</span></span>

 

 



