---
description: Демонстрирует, как управлять поведением группирования панели задач в окнах приложения с помощью свойства System.AppUserModel.ID.
title: 'Пример: свойство окна идентификатора модели пользователя приложения'
ms.topic: article
ms.date: 05/31/2018
ms.assetid: D4B22B3F-C849-4b5f-BDA0-FB42D7E0E4C9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 42544992248143c95ae905db39fe854b27751862
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985832"
---
# <a name="application-user-model-id-appid-window-property-sample"></a><span data-ttu-id="4d2c2-103">Пример свойства окна идентификатора модели пользователя приложения (AppID)</span><span class="sxs-lookup"><span data-stu-id="4d2c2-103">Application User Model ID (AppID) Window Property Sample</span></span>

<span data-ttu-id="4d2c2-104">Демонстрирует, как управлять поведением группирования панели задач в окнах приложения с помощью свойства [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) .</span><span class="sxs-lookup"><span data-stu-id="4d2c2-104">Demonstrates how to control the taskbar grouping behavior of an application's windows through the [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) property.</span></span>

<span data-ttu-id="4d2c2-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="4d2c2-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="4d2c2-106">Описание</span><span class="sxs-lookup"><span data-stu-id="4d2c2-106">Description</span></span>](#description)
-   [<span data-ttu-id="4d2c2-107">Требования</span><span class="sxs-lookup"><span data-stu-id="4d2c2-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="4d2c2-108">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="4d2c2-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="4d2c2-109">Создание примера</span><span class="sxs-lookup"><span data-stu-id="4d2c2-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="4d2c2-110">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="4d2c2-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="4d2c2-111">См. также</span><span class="sxs-lookup"><span data-stu-id="4d2c2-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="4d2c2-112">Описание</span><span class="sxs-lookup"><span data-stu-id="4d2c2-112">Description</span></span>

<span data-ttu-id="4d2c2-113">В этом примере показано, как задать свойство [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) с помощью реализации [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) окна, полученной с помощью [**шжетпропертисторефорвиндов**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow).</span><span class="sxs-lookup"><span data-stu-id="4d2c2-113">This sample shows how to set the [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) property through the use of the window's [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) implementation, which is obtained through [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d2c2-114">Требования</span><span class="sxs-lookup"><span data-stu-id="4d2c2-114">Requirements</span></span>



| <span data-ttu-id="4d2c2-115">Продукт</span><span class="sxs-lookup"><span data-stu-id="4d2c2-115">Product</span></span>                                | <span data-ttu-id="4d2c2-116">Минимальная версия продукта</span><span class="sxs-lookup"><span data-stu-id="4d2c2-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="4d2c2-117">Windows</span><span class="sxs-lookup"><span data-stu-id="4d2c2-117">Windows</span></span>                                | <span data-ttu-id="4d2c2-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4d2c2-118">Windows 7</span></span>               |
| <span data-ttu-id="4d2c2-119">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="4d2c2-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="4d2c2-120">7.0</span><span class="sxs-lookup"><span data-stu-id="4d2c2-120">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="4d2c2-121">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="4d2c2-121">Downloading the Sample</span></span>

| <span data-ttu-id="4d2c2-122">Расположение</span><span class="sxs-lookup"><span data-stu-id="4d2c2-122">Location</span></span>      | <span data-ttu-id="4d2c2-123">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="4d2c2-123">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d2c2-124">GitHub</span><span class="sxs-lookup"><span data-stu-id="4d2c2-124">GitHub</span></span>  | [<span data-ttu-id="4d2c2-125">Пример Аппусермоделидвиндовпроперти</span><span class="sxs-lookup"><span data-stu-id="4d2c2-125">AppUserModelIDWindowProperty sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AppUserModelIDWindowProperty) |


## <a name="building-the-sample"></a><span data-ttu-id="4d2c2-126">Построение образца</span><span class="sxs-lookup"><span data-stu-id="4d2c2-126">Building the Sample</span></span>

<span data-ttu-id="4d2c2-127">Чтобы построить образец из командной строки, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="4d2c2-127">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="4d2c2-128">Откройте окно командной строки и перейдите в каталог проекта **аппусермоделидвиндовпроперти** .</span><span class="sxs-lookup"><span data-stu-id="4d2c2-128">Open the command prompt window and navigate to the **AppUserModelIDWindowProperty** project directory.</span></span>
2.  <span data-ttu-id="4d2c2-129">Введите `msbuild AppUserModelIDWindowProperty.sln`.</span><span class="sxs-lookup"><span data-stu-id="4d2c2-129">Enter `msbuild AppUserModelIDWindowProperty.sln`.</span></span>

<span data-ttu-id="4d2c2-130">Чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):</span><span class="sxs-lookup"><span data-stu-id="4d2c2-130">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="4d2c2-131">Откройте проводник Windows и перейдите в каталог проекта **аппусермоделидвиндовпроперти** .</span><span class="sxs-lookup"><span data-stu-id="4d2c2-131">Open Windows Explorer and navigate to the **AppUserModelIDWindowProperty** project directory.</span></span>
2.  <span data-ttu-id="4d2c2-132">Дважды щелкните значок файла Аппусермоделидвиндовпроперти. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="4d2c2-132">Double-click the icon for the AppUserModelIDWindowProperty.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="4d2c2-133">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="4d2c2-133">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="4d2c2-134">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="4d2c2-134">Running the Sample</span></span>

1.  <span data-ttu-id="4d2c2-135">Перейдите в каталог, содержащий новый исполняемый файл, с помощью командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="4d2c2-135">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="4d2c2-136">В командной строке введите `AppUserModelIDWindowProperty.exe` .</span><span class="sxs-lookup"><span data-stu-id="4d2c2-136">At the command line, enter `AppUserModelIDWindowProperty.exe`.</span></span> <span data-ttu-id="4d2c2-137">Кроме того, в проводнике Windows дважды щелкните значок AppUserModelIDWindowProperty.exe.</span><span class="sxs-lookup"><span data-stu-id="4d2c2-137">Alternatively, from Windows Explorer double-click the icon for AppUserModelIDWindowProperty.exe.</span></span>
3.  <span data-ttu-id="4d2c2-138">Чтобы продемонстрировать, что идентификаторы модели пользователя приложения влияют на группировку панели задач, запустите по крайней мере три экземпляра приложения одновременно.</span><span class="sxs-lookup"><span data-stu-id="4d2c2-138">To demonstrate the effect Application User Model IDs (AppUserModelIDs) have on taskbar grouping, launch at least three instances of the application at the same time.</span></span>
4.  <span data-ttu-id="4d2c2-139">Используйте меню, чтобы задать другой AppUserModelID для каждого из трех окон.</span><span class="sxs-lookup"><span data-stu-id="4d2c2-139">Use the menu to set a different AppUserModelID on each of the three windows.</span></span> <span data-ttu-id="4d2c2-140">Обратите внимание, что каждый отдельный AppUserModelID приводит к отдельной кнопке панели задач, и Windows может изменить свою личность во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="4d2c2-140">Notice that each separate AppUserModelID results in a separate taskbar button and that windows can change their identity at runtime.</span></span>
5.  <span data-ttu-id="4d2c2-141">Установите для второго AppUserModelID по меньшей мере два окна.</span><span class="sxs-lookup"><span data-stu-id="4d2c2-141">Set at least two windows to the second AppUserModelID.</span></span> <span data-ttu-id="4d2c2-142">Обратите внимание, что они перемещаются в одну группу панели задач.</span><span class="sxs-lookup"><span data-stu-id="4d2c2-142">Notice that they both move into the same taskbar group.</span></span>
6.  <span data-ttu-id="4d2c2-143">Откройте окно **свойств панели задач и меню "Пуск** ", щелкнув правой кнопкой мыши панель задач и выбрав пункт **свойства** в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="4d2c2-143">Open the **Taskbar and Start Menu Properties** window by right-clicking the taskbar and selecting **Properties** in the context menu.</span></span> <span data-ttu-id="4d2c2-144">Измените **кнопки панели задач:** раскрывающийся список **объединение при заполнении панели задач** и **никогда не будет объединять** значения.</span><span class="sxs-lookup"><span data-stu-id="4d2c2-144">Change the **Taskbar buttons:** drop-down between the **Combine when taskbar is full** and **Never combine** values.</span></span> <span data-ttu-id="4d2c2-145">Обратите внимание, что каждое окно может получить отдельную кнопку, но кнопки группируются по AppUserModelID.</span><span class="sxs-lookup"><span data-stu-id="4d2c2-145">Notice that each window can get a separate button, but that the buttons are grouped by AppUserModelID.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d2c2-146">См. также</span><span class="sxs-lookup"><span data-stu-id="4d2c2-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d2c2-147">Идентификаторы модели пользователя приложения (Аппусермоделидс)</span><span class="sxs-lookup"><span data-stu-id="4d2c2-147">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> </dl>

 

 
