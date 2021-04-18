---
title: Сведения о синхронизации списков воспроизведения
description: Сведения о синхронизации списков воспроизведения
ms.assetid: bc7d52e0-7906-4b5b-82e6-a84e9c4f0ff0
keywords:
- Проигрыватель Windows Media, Синхронизация списков воспроизведения
- Объектная модель проигрывателя Windows Media, Синхронизация списков воспроизведения
- Объектная модель, Синхронизация списков воспроизведения
- Элемент управления ActiveX проигрывателя Windows Media, Синхронизация списков воспроизведения
- Элемент управления ActiveX, Синхронизация списков воспроизведения
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, Синхронизация списков воспроизведения
- Проигрыватель Windows Media Mobile, Синхронизация списков воспроизведения
- синхронизация устройств, списков воспроизведения
- синхронизация устройств, списки воспроизведения
- списки воспроизведения, синхронизация
- Списки воспроизведения метафайлов Windows Media, синхронизация
- списки воспроизведения метафайлов, синхронизация
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc019b31518fda1a49c8d3ae86f2d03c4ecefc8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336287"
---
# <a name="about-playlist-synchronization"></a><span data-ttu-id="22f7a-115">Сведения о синхронизации списков воспроизведения</span><span class="sxs-lookup"><span data-stu-id="22f7a-115">About Playlist Synchronization</span></span>

<span data-ttu-id="22f7a-116">Проигрыватель Windows Media 10 или более поздней версии предназначен для синхронизации мультимедийного содержимого с устройствами с помощью модели синхронизации списков воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="22f7a-116">Windows Media Player 10 or later is designed to synchronize digital media content to devices using a playlist synchronization model.</span></span> <span data-ttu-id="22f7a-117">Это означает, что содержимое, предназначенное для копирования на устройство, должно входить в список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="22f7a-117">This means that content intended to be copied to a device must be part of a playlist.</span></span> <span data-ttu-id="22f7a-118">Когда пользователь выбирает перенос отдельного мультимедийного содержимого с компьютера на устройство, проигрыватель Windows Media добавляет содержимое в список воспроизведения по умолчанию для копирования.</span><span class="sxs-lookup"><span data-stu-id="22f7a-118">When the user chooses to transfer individual digital media content from his or her computer to a device, Windows Media Player adds the content to a default playlist for copying.</span></span>

<span data-ttu-id="22f7a-119">API-интерфейсы синхронизации устройств проигрывателя Windows Media также предназначены для работы.</span><span class="sxs-lookup"><span data-stu-id="22f7a-119">The Windows Media Player device synchronization APIs are designed to work like this as well.</span></span> <span data-ttu-id="22f7a-120">Как и проигрыватель Windows Media, программа может предоставить пользователю список списков воспроизведения, которые он определил.</span><span class="sxs-lookup"><span data-stu-id="22f7a-120">Like Windows Media Player, your program can present the user with a list of playlists that he or she has defined.</span></span> <span data-ttu-id="22f7a-121">После этого пользователь может выбрать списки воспроизведения для синхронизации с определенным устройством и задать порядок приоритета для процесса синхронизации.</span><span class="sxs-lookup"><span data-stu-id="22f7a-121">You can then enable the user to choose which playlists to synchronize with a particular device and to set the priority order for the synchronization process.</span></span>

<span data-ttu-id="22f7a-122">Так как портативные устройства имеют ограниченную емкость хранилища, пользователь может выбрать синхронизацию большего объема мультимедийного содержимого, чем будет хранить устройство.</span><span class="sxs-lookup"><span data-stu-id="22f7a-122">Because portable devices have a limited storage capacity, it is possible for the user to choose to synchronize more digital media content than the device can store.</span></span> <span data-ttu-id="22f7a-123">Проигрыватель Windows Media синхронизирует содержимое в порядке приоритета.</span><span class="sxs-lookup"><span data-stu-id="22f7a-123">Windows Media Player synchronizes content in priority order.</span></span> <span data-ttu-id="22f7a-124">Пользователь может определить порядок приоритета с помощью диалогового окна, доступного из функции **устройства** .</span><span class="sxs-lookup"><span data-stu-id="22f7a-124">The user can define the priority order by using a dialog box that can be accessed from the **Devices** feature.</span></span> <span data-ttu-id="22f7a-125">В ответ на ввод пользователя в программу можно изменить порядок приоритета программным путем, изменив значения определенных атрибутов списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="22f7a-125">In response to user input to your program, you can change the priority order programmatically by changing the values of certain playlist attributes.</span></span> <span data-ttu-id="22f7a-126">Вместе эти атрибуты называются атрибутами *синхронизации* .</span><span class="sxs-lookup"><span data-stu-id="22f7a-126">Collectively, these attributes are called the *Sync* attributes.</span></span>

<span data-ttu-id="22f7a-127">Каждый список воспроизведения в библиотеке имеет 16 атрибутов синхронизации: **Sync01** до **Sync16**.</span><span class="sxs-lookup"><span data-stu-id="22f7a-127">Each playlist in a library has 16 synchronization attributes: **Sync01** through **Sync16**.</span></span> <span data-ttu-id="22f7a-128">Каждый атрибут представляет устройство с соответствующим индексом партнерства.</span><span class="sxs-lookup"><span data-stu-id="22f7a-128">Each attribute represents the device that has the corresponding partnership index.</span></span> <span data-ttu-id="22f7a-129">Значение каждого атрибута указывает на две вещи:</span><span class="sxs-lookup"><span data-stu-id="22f7a-129">The value of each attribute tells you two things:</span></span>

-   <span data-ttu-id="22f7a-130">Следует ли синхронизировать список воспроизведения с устройством.</span><span class="sxs-lookup"><span data-stu-id="22f7a-130">Whether the playlist should be synchronized with the device.</span></span>
-   <span data-ttu-id="22f7a-131">Значение приоритета для списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="22f7a-131">The priority value for the playlist.</span></span>

<span data-ttu-id="22f7a-132">Нулевое значение указывает, что проигрыватель Windows Media не должен пытаться синхронизировать список воспроизведения с устройством.</span><span class="sxs-lookup"><span data-stu-id="22f7a-132">A value of zero indicates that Windows Media Player should not attempt to synchronize the playlist with the device.</span></span> <span data-ttu-id="22f7a-133">Любое другое значение — это номер приоритета.</span><span class="sxs-lookup"><span data-stu-id="22f7a-133">Any other value is a priority number.</span></span> <span data-ttu-id="22f7a-134">Более низкие значения получают более высокий приоритет во время синхронизации.</span><span class="sxs-lookup"><span data-stu-id="22f7a-134">Lower values receive higher priority at synchronization time.</span></span>

<span data-ttu-id="22f7a-135">Списки воспроизведения также имеют атрибут **синконли** , указывающий, доступен ли список воспроизведения только для синхронизации.</span><span class="sxs-lookup"><span data-stu-id="22f7a-135">Playlists also have a **SyncOnly** attribute that indicates whether the playlist is available only for synchronization.</span></span>

<span data-ttu-id="22f7a-136">Отдельные элементы мультимедийного содержимого содержат метаданные о синхронизации.</span><span class="sxs-lookup"><span data-stu-id="22f7a-136">Individual items of digital media content contain metadata about synchronization as well.</span></span> <span data-ttu-id="22f7a-137">При извлечении объекта **мультимедиа** из библиотеки можно проверить значение атрибута **синкстате** .</span><span class="sxs-lookup"><span data-stu-id="22f7a-137">When you retrieve a **Media** object from the library, you can inspect the value of the **SyncState** attribute.</span></span> <span data-ttu-id="22f7a-138">Этот атрибут предоставляет расширенные сведения о том, было ли содержимое успешно скопировано на устройство или не удалось скопировать содержимое, так как оно не поместится.</span><span class="sxs-lookup"><span data-stu-id="22f7a-138">This attribute provides extended information about whether the content has been successfully copied to the device or whether copying the content failed because it would not fit.</span></span>

> [!Note]  
> <span data-ttu-id="22f7a-139">Следует избегать предоставления элементов пользовательского интерфейса, позволяющих пользователю создавать списки воспроизведения из всех содержимого библиотеки для синхронизации.</span><span class="sxs-lookup"><span data-stu-id="22f7a-139">You should avoid providing user interface elements that enable the user to create playlists from all library content for synchronization.</span></span>

 

<span data-ttu-id="22f7a-140">Для оптимизации производительности проигрыватель Windows Media обеспечивает набор правил для создания списков воспроизведения синхронизации.</span><span class="sxs-lookup"><span data-stu-id="22f7a-140">To optimize performance, Windows Media Player enforces a set of rules for creating synchronization playlists.</span></span> <span data-ttu-id="22f7a-141">Программа должна создавать списки воспроизведения синхронизации только для указанного содержимого.</span><span class="sxs-lookup"><span data-stu-id="22f7a-141">Your program should only create synchronization playlists for content you provided.</span></span> <span data-ttu-id="22f7a-142">Разрешить проигрывателю Windows Media создавать списки воспроизведения для содержимого, которое пользователь добавил в библиотеку из других источников.</span><span class="sxs-lookup"><span data-stu-id="22f7a-142">Allow Windows Media Player to create synchronization playlists for content that the user added to the library from other sources.</span></span>

<span data-ttu-id="22f7a-143">В качестве альтернативы созданию пользовательского интерфейса списка воспроизведения можно предоставить пользователям диалоговое окно по умолчанию для выбора списков воспроизведения и управления партнерством для устройства.</span><span class="sxs-lookup"><span data-stu-id="22f7a-143">As an alternative to creating your own playlist user interface, you can present users with a default dialog box for choosing playlists and managing the partnership for a device.</span></span> <span data-ttu-id="22f7a-144">Для этого вызовите [ивмпсинкдевице:: шовсеттингс](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-showsettings).</span><span class="sxs-lookup"><span data-stu-id="22f7a-144">To do this, call [IWMPSyncDevice::showSettings](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-showsettings).</span></span> <span data-ttu-id="22f7a-145">При вызове этого метода проигрыватель Windows Media отображает диалоговое окно "Параметры синхронизации".</span><span class="sxs-lookup"><span data-stu-id="22f7a-145">When you invoke this method, Windows Media Player displays its synchronization settings dialog box.</span></span> <span data-ttu-id="22f7a-146">Когда пользователь закрывает диалоговое окно, проигрыватель Windows Media автоматически возвращается к предыдущему состоянию закрепления и передает управление удаленной программе.</span><span class="sxs-lookup"><span data-stu-id="22f7a-146">When the user closes the dialog box, Windows Media Player automatically returns to its prior docking state and passes control back to your remoted program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22f7a-147">См. также</span><span class="sxs-lookup"><span data-stu-id="22f7a-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22f7a-148">**Сведения о синхронизации устройств**</span><span class="sxs-lookup"><span data-stu-id="22f7a-148">**About Device Synchronization**</span></span>](about-device-synchronization.md)
</dt> <dt>

[<span data-ttu-id="22f7a-149">**Управление списками воспроизведения синхронизации**</span><span class="sxs-lookup"><span data-stu-id="22f7a-149">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> <dt>

[<span data-ttu-id="22f7a-150">**Атрибуты списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="22f7a-150">**Playlist Attributes**</span></span>](playlist-attributes.md)
</dt> </dl>

 

 




