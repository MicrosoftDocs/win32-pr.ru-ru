---
title: Сведения о синхронизации устройств
description: Сведения о синхронизации устройств
ms.assetid: 87976357-f819-41ac-9645-36e799876881
keywords:
- Проигрыватель Windows Media, синхронизация устройств
- Объектная модель проигрывателя Windows Media, синхронизация устройств
- Объектная модель, синхронизация устройств
- Элемент управления ActiveX проигрывателя Windows Media, синхронизация устройств
- Элемент управления ActiveX, синхронизация устройств
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, синхронизация устройств
- Проигрыватель Windows Media Mobile, синхронизация устройств
- синхронизация устройств, сведения
- синхронизация устройств, сведения
- синхронизация устройств, ручная перенаправление
- синхронизация устройств, ручная перенаправление
- синхронизация устройств, автоматическая синхронизация
- синхронизация устройств, автоматическая синхронизация
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ad6b6526698def2f7d58ec7afc04c8e22e89c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691200"
---
# <a name="about-device-synchronization"></a><span data-ttu-id="00e8c-116">Сведения о синхронизации устройств</span><span class="sxs-lookup"><span data-stu-id="00e8c-116">About Device Synchronization</span></span>

<span data-ttu-id="00e8c-117">В проигрывателе Windows Media 10 появилась новая модель для синхронизации мультимедийного содержимого с портативными устройствами.</span><span class="sxs-lookup"><span data-stu-id="00e8c-117">Windows Media Player 10 introduced a new model for synchronizing digital media content with portable devices.</span></span> <span data-ttu-id="00e8c-118">С точки зрения пользователя это означает, что можно указать, какие списки воспроизведения (включая автоматические списки воспроизведения) будут автоматически синхронизироваться с устройствами.</span><span class="sxs-lookup"><span data-stu-id="00e8c-118">From the user's perspective, this means you can specify which playlists (including auto playlists) synchronize automatically with devices.</span></span> <span data-ttu-id="00e8c-119">Можно также вручную передавать цифровые мультимедийные данные на устройства.</span><span class="sxs-lookup"><span data-stu-id="00e8c-119">You can also manually transfer digital media content to devices.</span></span> <span data-ttu-id="00e8c-120">С точки зрения разработчика это означает, что есть новые функциональные возможности, которые можно использовать в приложениях.</span><span class="sxs-lookup"><span data-stu-id="00e8c-120">From the developer's perspective, this means there is new functionality exposed that you can take advantage of in your applications.</span></span> <span data-ttu-id="00e8c-121">Для этого необходимо создать удаленный экземпляр элемента управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="00e8c-121">To do this, you must create a remoted instance of the Windows Media Player control.</span></span>

<span data-ttu-id="00e8c-122">Существует два способа, с помощью которых пользователь может скопировать мультимедийное содержимое на устройство:</span><span class="sxs-lookup"><span data-stu-id="00e8c-122">There are two ways a user can copy digital media content to a device:</span></span>

-   <span data-ttu-id="00e8c-123">**Ручной перенос.**</span><span class="sxs-lookup"><span data-stu-id="00e8c-123">**Manual transfer.**</span></span> <span data-ttu-id="00e8c-124">Пользователь выбирает цифровое мультимедийное содержимое в библиотеке, а затем инициирует перенос содержимого на устройство.</span><span class="sxs-lookup"><span data-stu-id="00e8c-124">The user selects digital media content in the library and then initiates a transfer of the content to the device.</span></span> <span data-ttu-id="00e8c-125">Это похоже на функциональные возможности, предоставляемые предыдущими версиями проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="00e8c-125">This is similar to the functionality provided by previous versions of Windows Media Player.</span></span> <span data-ttu-id="00e8c-126">Пакет SDK для проигрывателя Windows Media не предоставляет методы для передачи цифровых мультимедийных файлов на устройство.</span><span class="sxs-lookup"><span data-stu-id="00e8c-126">The Windows Media Player SDK does not provide methods for transferring digital media to a device.</span></span>
-   <span data-ttu-id="00e8c-127">**Автоматическая синхронизация.**</span><span class="sxs-lookup"><span data-stu-id="00e8c-127">**Automatic synchronization.**</span></span> <span data-ttu-id="00e8c-128">Пользователь указывает списки воспроизведения, которые автоматически синхронизируются с устройством.</span><span class="sxs-lookup"><span data-stu-id="00e8c-128">The user specifies playlists that automatically synchronize with the device.</span></span> <span data-ttu-id="00e8c-129">Это функция проигрывателя Windows Media 10 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="00e8c-129">This is a feature of Windows Media Player 10 or later.</span></span> <span data-ttu-id="00e8c-130">Пакет SDK для проигрывателя Windows Media предоставляет функциональные возможности для управления автоматической синхронизацией.</span><span class="sxs-lookup"><span data-stu-id="00e8c-130">The Windows Media Player SDK provides functionality for managing automatic synchronization.</span></span> <span data-ttu-id="00e8c-131">Эта функция предназначена для создания пользовательского пользовательского интерфейса для приложения, позволяющего указать способ синхронизации устройства и предоставить пользователям сведения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="00e8c-131">This functionality is designed to let you build a custom user interface for your application to specify how device synchronization happens and to provide status information to users.</span></span>

<span data-ttu-id="00e8c-132">Для работы автоматической синхронизации необходимо установить специальную связь между проигрывателем Windows Media и устройством.</span><span class="sxs-lookup"><span data-stu-id="00e8c-132">For automatic synchronization to work, a special relationship must be established between Windows Media Player and the device.</span></span> <span data-ttu-id="00e8c-133">Это отношение называется *партнерством*.</span><span class="sxs-lookup"><span data-stu-id="00e8c-133">This relationship is called a *partnership*.</span></span>

<span data-ttu-id="00e8c-134">В следующих разделах содержатся дополнительные сведения о синхронизации устройств.</span><span class="sxs-lookup"><span data-stu-id="00e8c-134">The following sections provide more information about device synchronization.</span></span>

-   [<span data-ttu-id="00e8c-135">Сведения об устройствах</span><span class="sxs-lookup"><span data-stu-id="00e8c-135">About Devices</span></span>](about-devices.md)
-   [<span data-ttu-id="00e8c-136">О партнерстве</span><span class="sxs-lookup"><span data-stu-id="00e8c-136">About Partnerships</span></span>](about-partnerships.md)
-   [<span data-ttu-id="00e8c-137">Сведения о модуле синхронизации</span><span class="sxs-lookup"><span data-stu-id="00e8c-137">About the Synchronization Engine</span></span>](about-the-synchronization-engine.md)
-   [<span data-ttu-id="00e8c-138">Сведения о синхронизации списков воспроизведения</span><span class="sxs-lookup"><span data-stu-id="00e8c-138">About Playlist Synchronization</span></span>](about-playlist-synchronization.md)

## <a name="related-topics"></a><span data-ttu-id="00e8c-139">См. также</span><span class="sxs-lookup"><span data-stu-id="00e8c-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00e8c-140">**Сведения об объектной модели проигрывателя**</span><span class="sxs-lookup"><span data-stu-id="00e8c-140">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="00e8c-141">**Реализация удаленного управления проигрывателем Windows Media**</span><span class="sxs-lookup"><span data-stu-id="00e8c-141">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> <dt>

[<span data-ttu-id="00e8c-142">**Работа с портативными устройствами**</span><span class="sxs-lookup"><span data-stu-id="00e8c-142">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




