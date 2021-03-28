---
description: Демонстрирует, как зарегистрировать команду, расширяющую &\# 0034; Синхронизация&\# 0034; и &\# 0034; Совместное использование \# команд&0034; на панели команд проводника Windows.
title: Синхронизация и совместное использование команд
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 78267C74-7597-4b98-9DAE-89F2FD515C6B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 734d59ce7b527ad068c03be9083ca67dfca20667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986036"
---
# <a name="sync-and-share-verbs"></a><span data-ttu-id="7e71d-103">Синхронизация и совместное использование команд</span><span class="sxs-lookup"><span data-stu-id="7e71d-103">Sync and Share Verbs</span></span>

<span data-ttu-id="7e71d-104">Демонстрирует, как зарегистрировать команду, которая расширяет команды "Sync" и "Share" на панели команд проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="7e71d-104">Demonstrates how to register a verb that extends the "Sync" and "Share" verbs in the Windows Explorer Command Bar.</span></span>

<span data-ttu-id="7e71d-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="7e71d-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="7e71d-106">Требования</span><span class="sxs-lookup"><span data-stu-id="7e71d-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="7e71d-107">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="7e71d-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="7e71d-108">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="7e71d-108">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="7e71d-109">Удаление образца</span><span class="sxs-lookup"><span data-stu-id="7e71d-109">Removing the Sample</span></span>](#removing-the-sample)

## <a name="requirements"></a><span data-ttu-id="7e71d-110">Требования</span><span class="sxs-lookup"><span data-stu-id="7e71d-110">Requirements</span></span>



| <span data-ttu-id="7e71d-111">Продукт</span><span class="sxs-lookup"><span data-stu-id="7e71d-111">Product</span></span>                                | <span data-ttu-id="7e71d-112">Минимальная версия продукта</span><span class="sxs-lookup"><span data-stu-id="7e71d-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="7e71d-113">Windows</span><span class="sxs-lookup"><span data-stu-id="7e71d-113">Windows</span></span>                                | <span data-ttu-id="7e71d-114">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7e71d-114">Windows 7</span></span>               |
| <span data-ttu-id="7e71d-115">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="7e71d-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="7e71d-116">7.0</span><span class="sxs-lookup"><span data-stu-id="7e71d-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="7e71d-117">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="7e71d-117">Downloading the Sample</span></span>

| <span data-ttu-id="7e71d-118">Расположение</span><span class="sxs-lookup"><span data-stu-id="7e71d-118">Location</span></span>      | <span data-ttu-id="7e71d-119">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="7e71d-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e71d-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="7e71d-120">GitHub</span></span>  | [<span data-ttu-id="7e71d-121">Пример Синкандшаревербс</span><span class="sxs-lookup"><span data-stu-id="7e71d-121">SyncAndShareVerbs sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/SyncAndShareVerbs) |

## <a name="running-the-sample"></a><span data-ttu-id="7e71d-122">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="7e71d-122">Running the Sample</span></span>

<span data-ttu-id="7e71d-123">Чтобы запустить пример (Sync), выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7e71d-123">To run the sample (sync):</span></span>

1.  <span data-ttu-id="7e71d-124">Перейдите к каталогу, содержащему `sync.reg` файл.</span><span class="sxs-lookup"><span data-stu-id="7e71d-124">Navigate to the directory that contains the `sync.reg` file</span></span>
2.  <span data-ttu-id="7e71d-125">Введите `sync.reg ` в командной строке или дважды щелкните значок для `sync.reg` его регистрации.</span><span class="sxs-lookup"><span data-stu-id="7e71d-125">Type `sync.reg ` at the command line, or double-click the icon for `sync.reg` register it.</span></span>
3.  <span data-ttu-id="7e71d-126">Откройте проводник Windows и выберите файл.</span><span class="sxs-lookup"><span data-stu-id="7e71d-126">Open the Windows Explorer and select a file.</span></span>
4.  <span data-ttu-id="7e71d-127">Щелкните параметр **Синхронизация** на панели команд и выберите подпараметр, например **Paint**.</span><span class="sxs-lookup"><span data-stu-id="7e71d-127">Click the **Sync** option in the Command Bar and select a suboption such as **Paint**.</span></span>

<span data-ttu-id="7e71d-128">Чтобы запустить пример (Share), сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="7e71d-128">To run the sample (share):</span></span>

1.  <span data-ttu-id="7e71d-129">Перейдите в каталог, содержащий `share.reg` файл.</span><span class="sxs-lookup"><span data-stu-id="7e71d-129">Navigate to the directory that contains the `share.reg` file.</span></span>
2.  <span data-ttu-id="7e71d-130">Введите `share.reg` в командной строке или дважды щелкните значок для `share.reg` его регистрации.</span><span class="sxs-lookup"><span data-stu-id="7e71d-130">Type `share.reg` at the command line, or double-click the icon for `share.reg` register it.</span></span>
3.  <span data-ttu-id="7e71d-131">Откройте проводник Windows и выберите файл.</span><span class="sxs-lookup"><span data-stu-id="7e71d-131">Open Windows Explorer and select a file.</span></span> <span data-ttu-id="7e71d-132">Выберите параметр **общий доступ** на панели команд.</span><span class="sxs-lookup"><span data-stu-id="7e71d-132">Click the **Share** option in the Command Bar.</span></span>
4.  <span data-ttu-id="7e71d-133">Щелкните параметр **поделиться с** на панели команд и выберите подпараметр, например **Paint**.</span><span class="sxs-lookup"><span data-stu-id="7e71d-133">Click the **Share with** option in the Command Bar and select a suboption such as **Paint**.</span></span>

## <a name="removing-the-sample"></a><span data-ttu-id="7e71d-134">Удаление образца</span><span class="sxs-lookup"><span data-stu-id="7e71d-134">Removing the Sample</span></span>

<span data-ttu-id="7e71d-135">Чтобы удалить пример (Sync), выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7e71d-135">To remove the sample (sync):</span></span>

1.  <span data-ttu-id="7e71d-136">Перейдите в каталог, содержащий файл Унинсталлсинк. reg.</span><span class="sxs-lookup"><span data-stu-id="7e71d-136">Navigate to the directory that contains the Uninstallsync.reg file.</span></span>
2.  <span data-ttu-id="7e71d-137">Введите `uninstallsync.reg` в командной строке или дважды щелкните значок для `uninstallsync.reg` .</span><span class="sxs-lookup"><span data-stu-id="7e71d-137">Type `uninstallsync.reg` at the command line, or double-click the icon for `uninstallsync.reg`.</span></span>

<span data-ttu-id="7e71d-138">Чтобы удалить пример (Share), сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="7e71d-138">To remove the sample (share):</span></span>

1.  <span data-ttu-id="7e71d-139">Перейдите в каталог, содержащий файл Унинсталлшаре. reg.</span><span class="sxs-lookup"><span data-stu-id="7e71d-139">Navigate to the directory that contains the Uninstallshare.reg file.</span></span>
2.  <span data-ttu-id="7e71d-140">Введите `uninstallshare.reg` в командной строке или дважды щелкните значок для `uninstallshare.reg.`</span><span class="sxs-lookup"><span data-stu-id="7e71d-140">Type `uninstallshare.reg` at the command line, or double-click the icon for `uninstallshare.reg.`</span></span>

 

 



