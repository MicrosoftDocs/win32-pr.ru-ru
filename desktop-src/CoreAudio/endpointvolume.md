---
description: Этот пример приложения использует основные API аудио для изменения объема устройства, указанного пользователем.
ms.assetid: 2597f3b1-5339-4fd4-9938-39ff917626b4
title: ендпоинтволуме
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e89efe89035ec272c68c6a9289672a249616e23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496371"
---
# <a name="endpointvolume"></a><span data-ttu-id="45e20-103">ендпоинтволуме</span><span class="sxs-lookup"><span data-stu-id="45e20-103">EndpointVolume</span></span>

<span data-ttu-id="45e20-104">Этот пример приложения использует основные API аудио для изменения объема устройства, указанного пользователем.</span><span class="sxs-lookup"><span data-stu-id="45e20-104">This sample application uses the Core Audio APIs to change the volume of the device, as specified by the user.</span></span>

<span data-ttu-id="45e20-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="45e20-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="45e20-106">Описание</span><span class="sxs-lookup"><span data-stu-id="45e20-106">Description</span></span>](#description)
-   [<span data-ttu-id="45e20-107">Требования</span><span class="sxs-lookup"><span data-stu-id="45e20-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="45e20-108">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="45e20-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="45e20-109">Создание примера</span><span class="sxs-lookup"><span data-stu-id="45e20-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="45e20-110">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="45e20-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="45e20-111">См. также</span><span class="sxs-lookup"><span data-stu-id="45e20-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="45e20-112">Описание</span><span class="sxs-lookup"><span data-stu-id="45e20-112">Description</span></span>

<span data-ttu-id="45e20-113">В этом образце демонстрируются следующие возможности.</span><span class="sxs-lookup"><span data-stu-id="45e20-113">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="45e20-114">[API ммдевице](mmdevice-api.md) для перечисления мультимедийных устройств и выбора.</span><span class="sxs-lookup"><span data-stu-id="45e20-114">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="45e20-115">[ЕНДПОИНТВОЛУМЕ API](endpointvolume-api.md) для управления уровнями громкости конечной точки устройства.</span><span class="sxs-lookup"><span data-stu-id="45e20-115">[EndpointVolume API](endpointvolume-api.md) to control volume levels of the device endpoint.</span></span>

## <a name="requirements"></a><span data-ttu-id="45e20-116">Требования</span><span class="sxs-lookup"><span data-stu-id="45e20-116">Requirements</span></span>



| <span data-ttu-id="45e20-117">Продукт</span><span class="sxs-lookup"><span data-stu-id="45e20-117">Product</span></span>                                                        | <span data-ttu-id="45e20-118">Version</span><span class="sxs-lookup"><span data-stu-id="45e20-118">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="45e20-119">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="45e20-119">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="45e20-120">Windows 7</span><span class="sxs-lookup"><span data-stu-id="45e20-120">Windows 7</span></span> |
| <span data-ttu-id="45e20-121">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="45e20-121">Visual Studio</span></span>                                                  | <span data-ttu-id="45e20-122">2008</span><span class="sxs-lookup"><span data-stu-id="45e20-122">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="45e20-123">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="45e20-123">Downloading the Sample</span></span>

<span data-ttu-id="45e20-124">Этот образец доступен в следующих расположениях.</span><span class="sxs-lookup"><span data-stu-id="45e20-124">This sample is available in the following locations.</span></span>



| <span data-ttu-id="45e20-125">Расположение</span><span class="sxs-lookup"><span data-stu-id="45e20-125">Location</span></span>    | <span data-ttu-id="45e20-126">Путь или URL-адрес</span><span class="sxs-lookup"><span data-stu-id="45e20-126">Path/URL</span></span>                                                                                        |
|-------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45e20-127">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="45e20-127">Windows SDK</span></span> | <span data-ttu-id="45e20-128">\\Program Files \\ Microsoft SDK \\ Windows \\ v \\ 7.0 Samples \\ мультимедиа \\ Audio \\ ендпоинтволуме \\ ...</span><span class="sxs-lookup"><span data-stu-id="45e20-128">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\EndpointVolume\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="45e20-129">Построение образца</span><span class="sxs-lookup"><span data-stu-id="45e20-129">Building the Sample</span></span>

<span data-ttu-id="45e20-130">Чтобы создать пример x, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="45e20-130">To build the x sample, use the following steps:</span></span>

<span data-ttu-id="45e20-131">Чтобы создать пример Ендпоинтволумечанжер, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="45e20-131">To build the EndpointVolumeChanger sample, use the following steps:</span></span>

1.  <span data-ttu-id="45e20-132">Откройте командную оболочку для Windows SDK и перейдите в каталог примеров Ендпоинтволуме.</span><span class="sxs-lookup"><span data-stu-id="45e20-132">Open the CMD shell for the Windows SDK and change to the EndpointVolume sample directory.</span></span>
2.  <span data-ttu-id="45e20-133">Выполните команду `start EndpointVolumeChanger.sln` в каталоге ендпоинтволуме, чтобы открыть проект ендпоинтволумечанжер в окне Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="45e20-133">Run the command `start EndpointVolumeChanger.sln` in the EndpointVolume directory to open the EndpointVolumeChanger project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="45e20-134">В окне выберите конфигурацию решения для **отладки** или **выпуска** , выберите меню **Сборка** в строке меню и выберите параметр **Сборка** .</span><span class="sxs-lookup"><span data-stu-id="45e20-134">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="45e20-135">Если не открыть Visual Studio из командной оболочки для пакета SDK, Visual Studio не сможет получить доступ к среде сборки пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="45e20-135">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="45e20-136">В этом случае выборка не будет построена, если вы явно не настроили переменную среды Мссдк, которая используется в файле проекта Васапиендпоинтволуме. vcproj.</span><span class="sxs-lookup"><span data-stu-id="45e20-136">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIEndpointVolume.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="45e20-137">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="45e20-137">Running the Sample</span></span>

<span data-ttu-id="45e20-138">При успешном создании демонстрационного приложения создается исполняемый файл EndpointVolumeChanger.exe.</span><span class="sxs-lookup"><span data-stu-id="45e20-138">If you build the demo application successfully, an executable file, EndpointVolumeChanger.exe, is generated.</span></span> <span data-ttu-id="45e20-139">Чтобы запустить его, введите `EndpointVolumeChanger` в командном окне, а затем обязательные или необязательные аргументы.</span><span class="sxs-lookup"><span data-stu-id="45e20-139">To run it, type `EndpointVolumeChanger` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="45e20-140">В следующем примере показано, как включить параметр выключения звука на консольном устройстве по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="45e20-140">The following example shows how to toggle the mute setting on the default console device.</span></span>

`EndpointVolumeChanger.exe -console -m`

<span data-ttu-id="45e20-141">В следующей таблице показаны аргументы.</span><span class="sxs-lookup"><span data-stu-id="45e20-141">The following table shows the arguments.</span></span>

| <span data-ttu-id="45e20-142">Аргумент</span><span class="sxs-lookup"><span data-stu-id="45e20-142">Argument</span></span>        | <span data-ttu-id="45e20-143">Описание</span><span class="sxs-lookup"><span data-stu-id="45e20-143">Description</span></span>                                                         |
|-----------------|---------------------------------------------------------------------|
| <span data-ttu-id="45e20-144">-?</span><span class="sxs-lookup"><span data-stu-id="45e20-144">-?</span></span>              | <span data-ttu-id="45e20-145">Отображает справку.</span><span class="sxs-lookup"><span data-stu-id="45e20-145">Shows help.</span></span>                                                         |
| <span data-ttu-id="45e20-146">-H</span><span class="sxs-lookup"><span data-stu-id="45e20-146">-h</span></span>              | <span data-ttu-id="45e20-147">Отображает справку.</span><span class="sxs-lookup"><span data-stu-id="45e20-147">Shows help.</span></span>                                                         |
| -+              | <span data-ttu-id="45e20-148">Увеличивает уровень громкости на устройстве конечной точки звука на один шаг.</span><span class="sxs-lookup"><span data-stu-id="45e20-148">Increments the volume level on audio endpoint device by one step.</span></span> <span data-ttu-id="45e20-149">.</span><span class="sxs-lookup"><span data-stu-id="45e20-149">.</span></span> |
| <span data-ttu-id="45e20-150">-Up</span><span class="sxs-lookup"><span data-stu-id="45e20-150">-up</span></span>             | <span data-ttu-id="45e20-151">Увеличивает уровень громкости на устройстве конечной точки звука на один шаг.</span><span class="sxs-lookup"><span data-stu-id="45e20-151">Increments the volume level on audio endpoint device by one step.</span></span>   |
| --              | <span data-ttu-id="45e20-152">Уменьшает уровень громкости на устройстве конечной точки звука на один шаг.</span><span class="sxs-lookup"><span data-stu-id="45e20-152">Decrements the volume level on audio endpoint device by one step.</span></span>   |
| <span data-ttu-id="45e20-153">-Down</span><span class="sxs-lookup"><span data-stu-id="45e20-153">-down</span></span>           | <span data-ttu-id="45e20-154">Уменьшает уровень громкости на устройстве конечной точки звука на один шаг.</span><span class="sxs-lookup"><span data-stu-id="45e20-154">Decrements the volume level on audio endpoint device by one step.</span></span>   |
| <span data-ttu-id="45e20-155">-v</span><span class="sxs-lookup"><span data-stu-id="45e20-155">-v</span></span>              | <span data-ttu-id="45e20-156">Задает уровень главного тома на устройстве конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="45e20-156">Sets the master volume level on the audio endpoint device.</span></span>          |
| <span data-ttu-id="45e20-157">-Console</span><span class="sxs-lookup"><span data-stu-id="45e20-157">-console</span></span>        | <span data-ttu-id="45e20-158">Использовать консольное устройство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="45e20-158">Use the default console device.</span></span>                                     |
| <span data-ttu-id="45e20-159">-связь</span><span class="sxs-lookup"><span data-stu-id="45e20-159">-communications</span></span> | <span data-ttu-id="45e20-160">Используйте устройство связи по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="45e20-160">Use the default communication device.</span></span>                               |
| <span data-ttu-id="45e20-161">— мультимедиа</span><span class="sxs-lookup"><span data-stu-id="45e20-161">-multimedia</span></span>     | <span data-ttu-id="45e20-162">Используйте устройство мультимедиа по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="45e20-162">Use the default multimedia device.</span></span>                                  |
| <span data-ttu-id="45e20-163">— Конечная точка</span><span class="sxs-lookup"><span data-stu-id="45e20-163">-endpoint</span></span>       | <span data-ttu-id="45e20-164">Используйте идентификатор конечной точки, указанный в значении переключателя.</span><span class="sxs-lookup"><span data-stu-id="45e20-164">Use the endpoint identifier specified in the switch value.</span></span>          |



 

<span data-ttu-id="45e20-165">Если приложение запускается без аргументов, оно перечисляет доступные устройства и предлагает пользователю выбрать устройство.</span><span class="sxs-lookup"><span data-stu-id="45e20-165">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device.</span></span> <span data-ttu-id="45e20-166">После того как пользователь назначит устройство, приложение отобразит текущие параметры тома для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="45e20-166">After the user specifies the device, the application displays the current volume settings for the endpoint.</span></span> <span data-ttu-id="45e20-167">Для управления томом можно использовать параметры, описанные в предыдущей таблице.</span><span class="sxs-lookup"><span data-stu-id="45e20-167">The volume can be controlled by using the switches described in the preceding table.</span></span>

<span data-ttu-id="45e20-168">Дополнительные сведения об управлении уровнями громкости для устройств конечных точек звука см. в разделе [API ендпоинтволуме](endpointvolume-api.md).</span><span class="sxs-lookup"><span data-stu-id="45e20-168">For more information about controlling the volume levels of audio endpoint devices, see [EndpointVolume API](endpointvolume-api.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="45e20-169">См. также</span><span class="sxs-lookup"><span data-stu-id="45e20-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45e20-170">Примеры пакетов SDK, использующих основные API аудио</span><span class="sxs-lookup"><span data-stu-id="45e20-170">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



