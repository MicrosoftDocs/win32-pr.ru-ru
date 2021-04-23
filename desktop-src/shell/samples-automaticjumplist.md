---
description: Демонстрирует добавление элементов в автоматический список переходов для приложения, включая переключение между отображением часто и последних категорий.
title: 'Пример: автоматический список переходов'
ms.topic: article
ms.date: 05/31/2018
ms.assetid: C33152FE-1322-42f8-A656-3D5FAF4B612D
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ce0b6520163fcb07bb990b7a5a9fe742d976a899
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497925"
---
# <a name="automatic-jump-list-sample"></a><span data-ttu-id="0f4da-103">Пример: автоматический список переходов</span><span class="sxs-lookup"><span data-stu-id="0f4da-103">Automatic Jump List Sample</span></span>

<span data-ttu-id="0f4da-104">Демонстрирует добавление элементов в автоматический список переходов для приложения, включая переключение между отображением часто и последних категорий.</span><span class="sxs-lookup"><span data-stu-id="0f4da-104">Demonstrates how to add items to the automatic Jump List for an application, including switching between the display of the Frequent and Recent categories.</span></span>

<span data-ttu-id="0f4da-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="0f4da-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="0f4da-106">Требования</span><span class="sxs-lookup"><span data-stu-id="0f4da-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="0f4da-107">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="0f4da-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="0f4da-108">Создание примера</span><span class="sxs-lookup"><span data-stu-id="0f4da-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="0f4da-109">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="0f4da-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="0f4da-110">См. также</span><span class="sxs-lookup"><span data-stu-id="0f4da-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="0f4da-111">Требования</span><span class="sxs-lookup"><span data-stu-id="0f4da-111">Requirements</span></span>



| <span data-ttu-id="0f4da-112">Продукт</span><span class="sxs-lookup"><span data-stu-id="0f4da-112">Product</span></span>                                | <span data-ttu-id="0f4da-113">Минимальная версия продукта</span><span class="sxs-lookup"><span data-stu-id="0f4da-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="0f4da-114">Windows</span><span class="sxs-lookup"><span data-stu-id="0f4da-114">Windows</span></span>                                | <span data-ttu-id="0f4da-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0f4da-115">Windows 7</span></span>               |
| <span data-ttu-id="0f4da-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="0f4da-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="0f4da-117">7.0</span><span class="sxs-lookup"><span data-stu-id="0f4da-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="0f4da-118">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="0f4da-118">Downloading the Sample</span></span>

| <span data-ttu-id="0f4da-119">Расположение</span><span class="sxs-lookup"><span data-stu-id="0f4da-119">Location</span></span>      | <span data-ttu-id="0f4da-120">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="0f4da-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f4da-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="0f4da-121">GitHub</span></span>  | [<span data-ttu-id="0f4da-122">Пример Аутоматикжумплист</span><span class="sxs-lookup"><span data-stu-id="0f4da-122">AutomaticJumpList sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AutomaticJumpList) |

## <a name="building-the-sample"></a><span data-ttu-id="0f4da-123">Построение образца</span><span class="sxs-lookup"><span data-stu-id="0f4da-123">Building the Sample</span></span>

<span data-ttu-id="0f4da-124">Чтобы построить образец из командной строки, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0f4da-124">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="0f4da-125">Откройте окно командной строки и перейдите в каталог проекта **аутоматикжумплист** .</span><span class="sxs-lookup"><span data-stu-id="0f4da-125">Open the command prompt window and navigate to the **AutomaticJumpList** project directory.</span></span>
2.  <span data-ttu-id="0f4da-126">Введите `msbuild AutomaticJumpListSample.sln`.</span><span class="sxs-lookup"><span data-stu-id="0f4da-126">Enter `msbuild AutomaticJumpListSample.sln`.</span></span>

<span data-ttu-id="0f4da-127">Чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):</span><span class="sxs-lookup"><span data-stu-id="0f4da-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="0f4da-128">Откройте проводник Windows и перейдите в каталог проекта **аутоматикжумплист** .</span><span class="sxs-lookup"><span data-stu-id="0f4da-128">Open Windows Explorer and navigate to the **AutomaticJumpList** project directory.</span></span>
2.  <span data-ttu-id="0f4da-129">Дважды щелкните значок файла Аутоматикжумплистсампле. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0f4da-129">Double-click the icon for the AutomaticJumpListSample.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="0f4da-130">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="0f4da-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="0f4da-131">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="0f4da-131">Running the Sample</span></span>

1.  <span data-ttu-id="0f4da-132">Перейдите в каталог, содержащий новый исполняемый файл, с помощью командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="0f4da-132">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="0f4da-133">В командной строке введите `AutomaticJumpListSample.exe` .</span><span class="sxs-lookup"><span data-stu-id="0f4da-133">At the command line, enter `AutomaticJumpListSample.exe`.</span></span> <span data-ttu-id="0f4da-134">Кроме того, в проводнике Windows дважды щелкните значок AutomaticJumpListSample.exe.</span><span class="sxs-lookup"><span data-stu-id="0f4da-134">Alternatively, from Windows Explorer double-click the icon for AutomaticJumpListSample.exe.</span></span>
3.  <span data-ttu-id="0f4da-135">Этот пример должен запускаться от имени администратора при первом запуске, чтобы он мог установить необходимые регистрации типов файлов.</span><span class="sxs-lookup"><span data-stu-id="0f4da-135">This sample must be run as an administrator the first time it is run so that it can install the necessary file type registrations.</span></span> <span data-ttu-id="0f4da-136">После регистрации типов файлов пример можно запустить от имени обычного пользователя.</span><span class="sxs-lookup"><span data-stu-id="0f4da-136">After the file types have been registered, the sample can run as a standard user.</span></span>
4.  <span data-ttu-id="0f4da-137">Выберите параметры в меню в примере приложения, включая выбор txt-или doc-документов с помощью диалогового окна **Открыть** , чтобы увидеть, как они влияют на список переходов приложения на панели задач.</span><span class="sxs-lookup"><span data-stu-id="0f4da-137">Select options from the menu in the sample application, including the selection of .txt or .doc documents through the **Open** dialog to see how they affect the application's Jump List in the taskbar.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f4da-138">См. также</span><span class="sxs-lookup"><span data-stu-id="0f4da-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f4da-139">Идентификаторы модели пользователя приложения (Аппусермоделидс)</span><span class="sxs-lookup"><span data-stu-id="0f4da-139">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> </dl>

 

 



