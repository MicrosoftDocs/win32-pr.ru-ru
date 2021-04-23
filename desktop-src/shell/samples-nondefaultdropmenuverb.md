---
description: Демонстрирует расширение контекстного меню перетаскивания (иногда называемое контекстным меню).
title: Пример NonDefaultDropMenuVerb
ms.topic: article
ms.date: 05/31/2018
ms.assetid: F19B7561-D280-41df-A829-15960FEB12F8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9d326e012fb78b04fd542f88d49c370e8aeab613
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347932"
---
# <a name="nondefaultdropmenuverb-sample"></a><span data-ttu-id="2f0b9-103">Пример NonDefaultDropMenuVerb</span><span class="sxs-lookup"><span data-stu-id="2f0b9-103">NonDefaultDropMenuVerb Sample</span></span>

<span data-ttu-id="2f0b9-104">Демонстрирует расширение контекстного меню перетаскивания (иногда называемое контекстным меню).</span><span class="sxs-lookup"><span data-stu-id="2f0b9-104">Demonstrates how to extend the drag-and-drop shortcut menu (sometimes referred to as a context menu).</span></span>

<span data-ttu-id="2f0b9-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="2f0b9-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="2f0b9-106">Требования</span><span class="sxs-lookup"><span data-stu-id="2f0b9-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="2f0b9-107">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="2f0b9-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="2f0b9-108">Создание примера</span><span class="sxs-lookup"><span data-stu-id="2f0b9-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="2f0b9-109">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="2f0b9-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="2f0b9-110">Требования</span><span class="sxs-lookup"><span data-stu-id="2f0b9-110">Requirements</span></span>



| <span data-ttu-id="2f0b9-111">Продукт</span><span class="sxs-lookup"><span data-stu-id="2f0b9-111">Product</span></span>                                | <span data-ttu-id="2f0b9-112">Минимальная версия продукта</span><span class="sxs-lookup"><span data-stu-id="2f0b9-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="2f0b9-113">Windows</span><span class="sxs-lookup"><span data-stu-id="2f0b9-113">Windows</span></span>                                | <span data-ttu-id="2f0b9-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f0b9-114">Windows Vista</span></span>           |
| <span data-ttu-id="2f0b9-115">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="2f0b9-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="2f0b9-116">7.0</span><span class="sxs-lookup"><span data-stu-id="2f0b9-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="2f0b9-117">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="2f0b9-117">Downloading the Sample</span></span>

| <span data-ttu-id="2f0b9-118">Расположение</span><span class="sxs-lookup"><span data-stu-id="2f0b9-118">Location</span></span>      | <span data-ttu-id="2f0b9-119">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="2f0b9-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f0b9-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="2f0b9-120">GitHub</span></span>  | [<span data-ttu-id="2f0b9-121">Пример Нондефаултдропменуверб</span><span class="sxs-lookup"><span data-stu-id="2f0b9-121">NonDefaultDropMenuVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NonDefaultDropMenuVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="2f0b9-122">Построение образца</span><span class="sxs-lookup"><span data-stu-id="2f0b9-122">Building the Sample</span></span>

<span data-ttu-id="2f0b9-123">Чтобы построить образец из командной строки, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="2f0b9-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="2f0b9-124">Откройте окно командной строки и перейдите в каталог проекта **нондефаултдропменуверб** .</span><span class="sxs-lookup"><span data-stu-id="2f0b9-124">Open the command prompt window and navigate to the **NonDefaultDropMenuVerb** project directory.</span></span>
2.  <span data-ttu-id="2f0b9-125">Введите `msbuild NonDefaultDropMenuVerb.sln`.</span><span class="sxs-lookup"><span data-stu-id="2f0b9-125">Enter `msbuild NonDefaultDropMenuVerb.sln`.</span></span>

<span data-ttu-id="2f0b9-126">Чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):</span><span class="sxs-lookup"><span data-stu-id="2f0b9-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="2f0b9-127">Откройте проводник Windows и перейдите в каталог проекта **нондефаултдропменуверб** .</span><span class="sxs-lookup"><span data-stu-id="2f0b9-127">Open Windows Explorer and navigate to the **NonDefaultDropMenuVerb** project directory.</span></span>
2.  <span data-ttu-id="2f0b9-128">Дважды щелкните значок файла Нондефаултдропменуверб. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="2f0b9-128">Double-click the icon for the NonDefaultDropMenuVerb.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="2f0b9-129">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="2f0b9-129">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="2f0b9-130">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="2f0b9-130">Running the Sample</span></span>

1.  <span data-ttu-id="2f0b9-131">Перейдите в каталог, содержащий новый файл DLL, с помощью командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="2f0b9-131">Navigate to the directory that contains the new DLL file, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="2f0b9-132">Скопируйте NonDefaultDropMenuVerb.dll в системный каталог (например, C: \\ Windows \\ System32).</span><span class="sxs-lookup"><span data-stu-id="2f0b9-132">Copy NonDefaultDropMenuVerb.dll to the System directory (for example, C:\\Windows\\System32).</span></span>
3.  <span data-ttu-id="2f0b9-133">В командной строке введите `regedit NonDefaultDropMenuVerb.reg` .</span><span class="sxs-lookup"><span data-stu-id="2f0b9-133">At a command prompt, enter `regedit NonDefaultDropMenuVerb.reg`.</span></span>
4.  <span data-ttu-id="2f0b9-134">Используйте правую кнопку мыши, чтобы перетащить файл из одной папки в другую.</span><span class="sxs-lookup"><span data-stu-id="2f0b9-134">Use the right mouse button to drag a file from one folder to another.</span></span> <span data-ttu-id="2f0b9-135">Вы увидите дополнительные пункты меню для операции DROP.</span><span class="sxs-lookup"><span data-stu-id="2f0b9-135">You will see additional menu items for the drop operation.</span></span>

 

 



