---
description: Демонстрирует прослушивание уведомлений об изменениях в оболочке для папки или элемента в пространстве имен проводника Windows.
title: 'Пример: отслеживание уведомлений об изменениях'
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 02A7C5B4-94F2-4c35-9290-4C816E5CF63A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5d0ac6ccb2dd2328d81b77d03bffc68dfa9a70cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265687"
---
# <a name="change-notify-watcher-sample"></a><span data-ttu-id="c0456-103">Пример: отслеживание уведомлений об изменениях</span><span class="sxs-lookup"><span data-stu-id="c0456-103">Change Notify Watcher Sample</span></span>

<span data-ttu-id="c0456-104">Демонстрирует прослушивание уведомлений об изменениях в оболочке для папки или элемента в пространстве имен проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="c0456-104">Demonstrates how to listen to Shell change notifications on a folder or item in the Windows Explorer namespace.</span></span>

<span data-ttu-id="c0456-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="c0456-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c0456-106">Требования</span><span class="sxs-lookup"><span data-stu-id="c0456-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="c0456-107">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="c0456-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="c0456-108">Создание примера</span><span class="sxs-lookup"><span data-stu-id="c0456-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="c0456-109">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="c0456-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="c0456-110">Требования</span><span class="sxs-lookup"><span data-stu-id="c0456-110">Requirements</span></span>



| <span data-ttu-id="c0456-111">Продукт</span><span class="sxs-lookup"><span data-stu-id="c0456-111">Product</span></span>                                | <span data-ttu-id="c0456-112">Минимальная версия продукта</span><span class="sxs-lookup"><span data-stu-id="c0456-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="c0456-113">Windows</span><span class="sxs-lookup"><span data-stu-id="c0456-113">Windows</span></span>                                | <span data-ttu-id="c0456-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0456-114">Windows Vista</span></span>           |
| <span data-ttu-id="c0456-115">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="c0456-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="c0456-116">7.0</span><span class="sxs-lookup"><span data-stu-id="c0456-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="c0456-117">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="c0456-117">Downloading the Sample</span></span>

| <span data-ttu-id="c0456-118">Расположение</span><span class="sxs-lookup"><span data-stu-id="c0456-118">Location</span></span>      | <span data-ttu-id="c0456-119">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="c0456-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0456-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="c0456-120">GitHub</span></span>  | [<span data-ttu-id="c0456-121">Пример Чанженотифиватчер</span><span class="sxs-lookup"><span data-stu-id="c0456-121">ChangeNotifyWatcher sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/ChangeNotifyWatcher) |

## <a name="building-the-sample"></a><span data-ttu-id="c0456-122">Построение образца</span><span class="sxs-lookup"><span data-stu-id="c0456-122">Building the Sample</span></span>

<span data-ttu-id="c0456-123">Чтобы построить образец из командной строки, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="c0456-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="c0456-124">Откройте окно командной строки и перейдите в каталог проекта **чанженотифиватчер** .</span><span class="sxs-lookup"><span data-stu-id="c0456-124">Open the command prompt window and navigate to the **ChangeNotifyWatcher** project directory.</span></span>
2.  <span data-ttu-id="c0456-125">Введите `msbuild ChangeNotifyWatcher.sln`.</span><span class="sxs-lookup"><span data-stu-id="c0456-125">Enter `msbuild ChangeNotifyWatcher.sln`.</span></span>

<span data-ttu-id="c0456-126">Чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):</span><span class="sxs-lookup"><span data-stu-id="c0456-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="c0456-127">Откройте проводник Windows и перейдите в каталог проекта **чанженотифиватчер** .</span><span class="sxs-lookup"><span data-stu-id="c0456-127">Open Windows Explorer and navigate to the **ChangeNotifyWatcher** project directory.</span></span>
2.  <span data-ttu-id="c0456-128">Дважды щелкните значок файла Чанженотифиватчер. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c0456-128">Double-click the icon for the ChangeNotifyWatcher.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="c0456-129">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="c0456-129">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="c0456-130">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="c0456-130">Running the Sample</span></span>

1.  <span data-ttu-id="c0456-131">Перейдите в каталог, содержащий новый исполняемый файл, с помощью командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="c0456-131">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="c0456-132">В командной строке введите `ChangeNotifyWatcher.exe`.</span><span class="sxs-lookup"><span data-stu-id="c0456-132">At the command prompt, enter `ChangeNotifyWatcher.exe`.</span></span> <span data-ttu-id="c0456-133">Кроме того, в проводнике Windows дважды щелкните значок ChangeNotifyWatcher.exe.</span><span class="sxs-lookup"><span data-stu-id="c0456-133">Alternatively, from Windows Explorer double-click the icon for ChangeNotifyWatcher.exe.</span></span>
3.  <span data-ttu-id="c0456-134">Чтобы продемонстрировать результат, идентификаторы модели пользователя приложения (Аппусермоделидс) выбирают папку для просмотра путем нажатия кнопки **"выбрать..."** или с помощью перетаскивания папки из окна проводника Windows в представление списка выборки.</span><span class="sxs-lookup"><span data-stu-id="c0456-134">To demonstrate the effect, Application User Model IDs (AppUserModelIDs) select a folder to watch by either clicking **"Pick..."** or by using drag-and-drop on a folder from a Windows Explorer window into the sample's list view.</span></span>

 

 



