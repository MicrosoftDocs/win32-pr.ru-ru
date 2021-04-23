---
title: Сведения об объектной модели проигрывателя
description: Сведения об объектной модели проигрывателя
ms.assetid: 41a9cbce-b982-4377-a0ee-b0ca735954f5
keywords:
- Проигрыватель Windows Media, объектная модель
- Объектная модель проигрывателя Windows Media, о программе
- Объектная модель, сведения
- Элемент управления ActiveX проигрывателя Windows Media, объектная модель
- Элемент управления ActiveX, объектная модель
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, объектная модель
- Проигрыватель Windows Media Mobile, объектная модель
- пакет средств разработки программного обеспечения (SDK), объектная модель элемента управления ActiveX проигрывателя Windows Media
- Пакет SDK (пакет средств разработки программного обеспечения), объектная модель элемента управления ActiveX проигрывателя Windows Media
- Документация, объектная модель элемента управления ActiveX проигрывателя Windows Media
- Объект Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06a0ded1f25d8d08bd9e588b5384a171698d2ea2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691252"
---
# <a name="about-the-player-object-model"></a><span data-ttu-id="6b909-114">Сведения об объектной модели проигрывателя</span><span class="sxs-lookup"><span data-stu-id="6b909-114">About the Player Object Model</span></span>

<span data-ttu-id="6b909-115">Элемент управления проигрывателя Microsoft Windows Media — это стандартный элемент управления ActiveX, использующий технологию модели COM (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="6b909-115">The Microsoft Windows Media Player control is a standard ActiveX control that uses Microsoft Component Object Model (COM) technology.</span></span> <span data-ttu-id="6b909-116">Функция проигрывателя Windows Media по-прежнему преобразуется в набор программных интерфейсов, которые следуют стандартным правилам COM.</span><span class="sxs-lookup"><span data-stu-id="6b909-116">The Windows Media Player functionality is distilled into a set of programming interfaces that follows standard COM guidelines.</span></span> <span data-ttu-id="6b909-117">Эти интерфейсы можно программировать на стандартной веб-странице HTML, используя объектную модель проигрывателя с Microsoft JScript или Microsoft Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="6b909-117">You can program these interfaces on a standard HTML webpage using the Player control object model with Microsoft JScript or Microsoft Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="6b909-118">Кроме того, их можно программировать в обложках с помощью Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="6b909-118">You can also program them in skins by using Microsoft JScript.</span></span> <span data-ttu-id="6b909-119">Если вы хотите создать пользовательскую программу, содержащую элемент управления, можно использовать один из нескольких языков, включая Visual Basic, C++ и C#.</span><span class="sxs-lookup"><span data-stu-id="6b909-119">If you want to create a custom program that embeds the control, you can use one of several languages, including Visual Basic, C++, and C#.</span></span>

<span data-ttu-id="6b909-120">Элемент управления ActiveX проигрывателя Windows Media устанавливается вместе с проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6b909-120">The Windows Media Player ActiveX control is installed with Windows Media Player.</span></span> <span data-ttu-id="6b909-121">Элемент управления Player не устанавливается вместе с пакетом SDK проигрывателя Windows Media и не может распространяться отдельно.</span><span class="sxs-lookup"><span data-stu-id="6b909-121">The Player control is not installed with the Windows Media Player SDK and cannot be redistributed separately.</span></span> <span data-ttu-id="6b909-122">Конкретные функции, доступные в коде, зависят от версии проигрывателя Windows Media, установленного пользователем.</span><span class="sxs-lookup"><span data-stu-id="6b909-122">The particular features available to your code depend on which version of Windows Media Player the user has installed.</span></span> <span data-ttu-id="6b909-123">В [справочнике по объектной модели для сценариев](object-model-reference-for-scripting.md) и [объектной модели для C++](object-model-reference-for-c.md) содержатся сведения о требованиях к версии для каждого свойства, метода и события.</span><span class="sxs-lookup"><span data-stu-id="6b909-123">The [Object Model Reference for Scripting](object-model-reference-for-scripting.md) and [Object Model Reference for C++](object-model-reference-for-c.md) include version requirement information for each property, method, and event.</span></span>

<span data-ttu-id="6b909-124">В следующих разделах содержатся общие сведения об объектной модели проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6b909-124">The following sections provide overview information about the Windows Media Player object model.</span></span>



| <span data-ttu-id="6b909-125">Section</span><span class="sxs-lookup"><span data-stu-id="6b909-125">Section</span></span>                                                                                        | <span data-ttu-id="6b909-126">Описание</span><span class="sxs-lookup"><span data-stu-id="6b909-126">Description</span></span>                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b909-127">Объектная модель проигрывателя для языков сценариев</span><span class="sxs-lookup"><span data-stu-id="6b909-127">Player Object Model for Scripting Languages</span></span>](player-object-model-for-scripting-languages.md) | <span data-ttu-id="6b909-128">В этом разделе описываются объекты, доступные в объектной модели.</span><span class="sxs-lookup"><span data-stu-id="6b909-128">This section describes the objects available in the object model.</span></span>                                                                                             |
| [<span data-ttu-id="6b909-129">Сведения о версиях моделей объектов</span><span class="sxs-lookup"><span data-stu-id="6b909-129">About the Object Model Versions</span></span>](about-the-object-model-versions.md)                         | <span data-ttu-id="6b909-130">В этом разделе описывается, какие элементы объектной модели были добавлены в каждую версию с момента появления проигрывателя Windows Media 7,0.</span><span class="sxs-lookup"><span data-stu-id="6b909-130">This section details which object model items have been added in each version since the introduction of Windows Media Player 7.0.</span></span>                             |
| [<span data-ttu-id="6b909-131">Свойства, методы и события</span><span class="sxs-lookup"><span data-stu-id="6b909-131">Properties, Methods, and Events</span></span>](properties--methods-and-events.md)                          | <span data-ttu-id="6b909-132">В этом разделе описываются свойства, методы и события.</span><span class="sxs-lookup"><span data-stu-id="6b909-132">This section explains properties, methods, and events.</span></span>                                                                                                        |
| [<span data-ttu-id="6b909-133">Поддерживаемые протоколы и типы файлов</span><span class="sxs-lookup"><span data-stu-id="6b909-133">Supported Protocols and File Types</span></span>](supported-protocols-and-file-types.md)                   | <span data-ttu-id="6b909-134">В этом разделе перечислены протоколы и типы файлов, поддерживаемые проигрывателем Windows Media и управляющей объектной моделью проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6b909-134">This section lists the protocols and file types supported by Windows Media Player and the Windows Media Player control object model.</span></span>                          |
| [<span data-ttu-id="6b909-135">Сведения о библиотеке</span><span class="sxs-lookup"><span data-stu-id="6b909-135">About the Library</span></span>](about-the-library.md)                                                     | <span data-ttu-id="6b909-136">В этом разделе описывается библиотека проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6b909-136">This section describes the Windows Media Player library.</span></span>                                                                                                      |
| [<span data-ttu-id="6b909-137">Использование HTML с проигрывателем Windows Media</span><span class="sxs-lookup"><span data-stu-id="6b909-137">Using HTML with Windows Media Player</span></span>](using-html-with-windows-media-player.md)               | <span data-ttu-id="6b909-138">В этом разделе описаны различные способы обеспечения совместной работы проигрывателя Windows Media и HTML.</span><span class="sxs-lookup"><span data-stu-id="6b909-138">This section describes the various ways to make Windows Media Player and HTML work together.</span></span>                                                                  |
| [<span data-ttu-id="6b909-139">Внедрение элемента управления проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="6b909-139">Embedding the Windows Media Player Control</span></span>](embedding-the-windows-media-player-control.md)   | <span data-ttu-id="6b909-140">В этом разделе описываются различные способы внедрения элемента управления проигрывателя Windows Media в Microsoft Office документы и пользовательские программы.</span><span class="sxs-lookup"><span data-stu-id="6b909-140">This section describes the various ways to embed the Windows Media Player control in Microsoft Office documents and in custom programs.</span></span>                       |
| [<span data-ttu-id="6b909-141">Сведения о синхронизации устройств</span><span class="sxs-lookup"><span data-stu-id="6b909-141">About Device Synchronization</span></span>](about-device-synchronization.md)                               | <span data-ttu-id="6b909-142">В этом разделе описаны функциональные возможности, предоставляемые проигрывателем Windows Media 10 или более поздней версии для передачи цифрового мультимедийного содержимого на портативные устройства.</span><span class="sxs-lookup"><span data-stu-id="6b909-142">This section describes the functionality provided by the Windows Media Player 10 or later control for transferring digital media content to portable devices.</span></span> |
| [<span data-ttu-id="6b909-143">Сведения о записи компакт-дисков</span><span class="sxs-lookup"><span data-stu-id="6b909-143">About CD Burning</span></span>](about-cd-burning.md)                                                       | <span data-ttu-id="6b909-144">В этом разделе описаны функциональные возможности, предоставляемые элементом управления проигрывателя Windows Media для создания компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="6b909-144">This section describes the functionality provided by the Windows Media Player control for creating CDs.</span></span>                                                       |
| [<span data-ttu-id="6b909-145">О копировании компакт-дисков</span><span class="sxs-lookup"><span data-stu-id="6b909-145">About CD Ripping</span></span>](about-cd-ripping.md)                                                       | <span data-ttu-id="6b909-146">В этом разделе описаны функциональные возможности, предоставляемые элементом управления проигрывателя Windows Media для копирования дорожек с аудио компакт-диска на компьютер пользователя.</span><span class="sxs-lookup"><span data-stu-id="6b909-146">This section describes the functionality provided by the Windows Media Player control for copying tracks from audio CDs to the user's computer.</span></span>               |
| [<span data-ttu-id="6b909-147">О мониторинге папок</span><span class="sxs-lookup"><span data-stu-id="6b909-147">About Folder Monitoring</span></span>](about-folder-monitoring.md)                                         | <span data-ttu-id="6b909-148">В этом разделе описаны функциональные возможности, предоставляемые элементом управления проигрывателя Windows Media для управления процессами мониторинга папки проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="6b909-148">This section describes the functionality provided by the Windows Media Player control for controlling the Player's folder monitoring processes.</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="6b909-149">См. также</span><span class="sxs-lookup"><span data-stu-id="6b909-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b909-150">**Объектная модель проигрывателя Windows Media**</span><span class="sxs-lookup"><span data-stu-id="6b909-150">**Windows Media Player Object Model**</span></span>](windows-media-player-object-model.md)
</dt> </dl>

 

 




