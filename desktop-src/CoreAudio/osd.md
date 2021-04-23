---
description: В этом примере используются основные API аудио, чтобы реализовать экран на экране, в котором показаны изменения тома в потоке вывода, который воспроизводится через устройство конечной точки отрисовки звука по умолчанию.
ms.assetid: 33a1e843-f7c7-4da9-a51e-83a3f0a6ac70
title: ОПЕРАЦИОННОЙ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c4c04daf5d2dd333a25150821a831695e06a06
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072476"
---
# <a name="osd"></a><span data-ttu-id="7e9b8-103">ОПЕРАЦИОННОЙ</span><span class="sxs-lookup"><span data-stu-id="7e9b8-103">OSD</span></span>

<span data-ttu-id="7e9b8-104">В этом примере используются основные API аудио, чтобы реализовать экран на экране, в котором показаны изменения тома в потоке вывода, который воспроизводится через устройство конечной точки отрисовки звука по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7e9b8-104">This sample uses the Core Audio APIs to implement an on-screen display that shows volume changes to the output stream that plays through the default audio-rendering endpoint device.</span></span> <span data-ttu-id="7e9b8-105">Экран отображается, когда пользователь корректирует уровень громкости в программе управления громкостью Windows Sndvol.exe и исчезает после того, как уровень тома остается неизменным в течение короткого периода.</span><span class="sxs-lookup"><span data-stu-id="7e9b8-105">The on-screen display appears when the user adjusts the volume level in the Windows volume-control program, Sndvol.exe, and it disappears after the volume level remains unchanged for a short period.</span></span>

<span data-ttu-id="7e9b8-106">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="7e9b8-106">This topic containes the following sections.</span></span>

-   [<span data-ttu-id="7e9b8-107">Описание</span><span class="sxs-lookup"><span data-stu-id="7e9b8-107">Description</span></span>](#description)
-   [<span data-ttu-id="7e9b8-108">Требования</span><span class="sxs-lookup"><span data-stu-id="7e9b8-108">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="7e9b8-109">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="7e9b8-109">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="7e9b8-110">Создание примера</span><span class="sxs-lookup"><span data-stu-id="7e9b8-110">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="7e9b8-111">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="7e9b8-111">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="7e9b8-112">См. также</span><span class="sxs-lookup"><span data-stu-id="7e9b8-112">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="7e9b8-113">Описание</span><span class="sxs-lookup"><span data-stu-id="7e9b8-113">Description</span></span>

<span data-ttu-id="7e9b8-114">В этом образце демонстрируются следующие возможности.</span><span class="sxs-lookup"><span data-stu-id="7e9b8-114">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="7e9b8-115">[API ммдевице](mmdevice-api.md) для перечисления мультимедийных устройств и выбора.</span><span class="sxs-lookup"><span data-stu-id="7e9b8-115">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="7e9b8-116">[API аудио ендпоинтволуме](endpointvolume-api.md)</span><span class="sxs-lookup"><span data-stu-id="7e9b8-116">Audio [EndpointVolume API](endpointvolume-api.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="7e9b8-117">Требования</span><span class="sxs-lookup"><span data-stu-id="7e9b8-117">Requirements</span></span>



| <span data-ttu-id="7e9b8-118">Продукт</span><span class="sxs-lookup"><span data-stu-id="7e9b8-118">Product</span></span>                                                        | <span data-ttu-id="7e9b8-119">Version</span><span class="sxs-lookup"><span data-stu-id="7e9b8-119">Version</span></span>                |
|----------------------------------------------------------------|------------------------|
| [<span data-ttu-id="7e9b8-120">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="7e9b8-120">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="7e9b8-121">Windows Vista или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="7e9b8-121">Windows Vista or later</span></span> |
| <span data-ttu-id="7e9b8-122">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7e9b8-122">Visual Studio</span></span>                                                  | <span data-ttu-id="7e9b8-123">2005 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="7e9b8-123">2005 or later</span></span>          |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="7e9b8-124">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="7e9b8-124">Downloading the Sample</span></span>

<span data-ttu-id="7e9b8-125">Этот образец доступен в следующих расположениях.</span><span class="sxs-lookup"><span data-stu-id="7e9b8-125">This sample is available in the following locations.</span></span>



| <span data-ttu-id="7e9b8-126">Расположение</span><span class="sxs-lookup"><span data-stu-id="7e9b8-126">Location</span></span>    | <span data-ttu-id="7e9b8-127">Путь или URL-адрес</span><span class="sxs-lookup"><span data-stu-id="7e9b8-127">Path/URL</span></span>                                                                             |
|-------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7e9b8-128">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="7e9b8-128">Windows SDK</span></span> | <span data-ttu-id="7e9b8-129">\\Program Files \\ Microsoft SDK \\ Windows \\ v \\ 7.0 Samples \\ мультимедиа \\ Audio \\ OSD \\ ...</span><span class="sxs-lookup"><span data-stu-id="7e9b8-129">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\OSD\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="7e9b8-130">Построение образца</span><span class="sxs-lookup"><span data-stu-id="7e9b8-130">Building the Sample</span></span>

1.  <span data-ttu-id="7e9b8-131">Откройте командную оболочку для Windows SDK и перейдите в каталог примеров OSD.</span><span class="sxs-lookup"><span data-stu-id="7e9b8-131">Open the CMD shell for the Windows SDK and change to the OSD sample directory.</span></span>
2.  <span data-ttu-id="7e9b8-132">Выполните команду "Start OSD. sln" в каталоге OSD, чтобы открыть проект OSD в окне Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7e9b8-132">Run the command "start OSD.sln" in the OSD directory to open the OSD project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="7e9b8-133">В окне выберите конфигурацию решения для **отладки** или **выпуска** , выберите меню **Сборка** в строке меню и выберите параметр **Сборка** .</span><span class="sxs-lookup"><span data-stu-id="7e9b8-133">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="7e9b8-134">Если не открыть Visual Studio из командной оболочки для пакета SDK, Visual Studio не сможет получить доступ к среде сборки пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="7e9b8-134">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="7e9b8-135">В этом случае выборка не будет построена, если вы явно не настроили переменную среды Мссдк, которая используется в файле проекта, OSD. vcproj.</span><span class="sxs-lookup"><span data-stu-id="7e9b8-135">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, OSD.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="7e9b8-136">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="7e9b8-136">Running the Sample</span></span>

1.  <span data-ttu-id="7e9b8-137">Запустите исполняемый файл OSD, OSD.exe, в Windows Vista или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="7e9b8-137">Run the OSD executable file, OSD.exe, in Windows Vista or later.</span></span> <span data-ttu-id="7e9b8-138">Обратите внимание, что для приложения не отображается значок или окно панели задач, но можно увидеть, что процесс выполняется с помощью TaskMgr.exe.</span><span class="sxs-lookup"><span data-stu-id="7e9b8-138">Note that you will not see a system tray icon or a window for the application, but you can see the process running using TaskMgr.exe.</span></span>
2.  <span data-ttu-id="7e9b8-139">Запустите sndvol.exe, чтобы изменить или выключить том, или измените громкость с помощью клавиш управления клавиатуры или элемента управления HID.</span><span class="sxs-lookup"><span data-stu-id="7e9b8-139">Run sndvol.exe to change the volume or mute, or change the volume using keyboard controls or an HID control.</span></span> <span data-ttu-id="7e9b8-140">Отобразится пользовательский интерфейс OSD.</span><span class="sxs-lookup"><span data-stu-id="7e9b8-140">The OSD user interface is displayed.</span></span>
3.  <span data-ttu-id="7e9b8-141">Чтобы выйти из приложения, запустите TaskMgr.exe, выделите OSD.exe процесс и нажмите кнопку **завершить процесс**.</span><span class="sxs-lookup"><span data-stu-id="7e9b8-141">To exit the application, run TaskMgr.exe, highlight the OSD.exe process and click **End Process**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e9b8-142">См. также</span><span class="sxs-lookup"><span data-stu-id="7e9b8-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e9b8-143">Примеры пакетов SDK, использующих основные API аудио</span><span class="sxs-lookup"><span data-stu-id="7e9b8-143">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



