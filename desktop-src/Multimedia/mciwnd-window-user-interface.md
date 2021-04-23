---
title: Пользовательский интерфейс окна МЦивнд
description: Пользовательский интерфейс окна МЦивнд
ms.assetid: 422c5acb-bce5-4be2-96ba-5ab7f9dcc826
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98c0b11b6868828625c6c6e605f005fe842d669
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067590"
---
# <a name="mciwnd-window-user-interface"></a><span data-ttu-id="3536e-103">Пользовательский интерфейс окна МЦивнд</span><span class="sxs-lookup"><span data-stu-id="3536e-103">MCIWnd Window User Interface</span></span>

<span data-ttu-id="3536e-104">МЦивнд предоставляет дополнительные возможности для настройки вида окна МЦивнд, настройки поведения приложения и настройки производительности воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="3536e-104">MCIWnd provides additional features to adjust the look of the MCIWnd window, customize the behavior of your application, and tune playback performance.</span></span> <span data-ttu-id="3536e-105">В окно МЦивнд включены следующие функции:</span><span class="sxs-lookup"><span data-stu-id="3536e-105">The following features are included in the MCIWnd window:</span></span>

-   <span data-ttu-id="3536e-106">Панель инструментов с кнопками **воспроизведения**, **окончания**, **записи** и **меню**</span><span class="sxs-lookup"><span data-stu-id="3536e-106">A toolbar with **Play**, **Stop**, **Record** and **Menu** buttons</span></span>
-   <span data-ttu-id="3536e-107">Значение TrackBar, которое управляет размещением в содержимом воспроизведения</span><span class="sxs-lookup"><span data-stu-id="3536e-107">A trackbar that controls positioning within the playback content</span></span>
-   <span data-ttu-id="3536e-108">Всплывающее меню с общими командами</span><span class="sxs-lookup"><span data-stu-id="3536e-108">A pop-up menu containing common commands</span></span>
-   <span data-ttu-id="3536e-109">Область воспроизведения видео-и других устройств, отображающих изображения</span><span class="sxs-lookup"><span data-stu-id="3536e-109">A playback area for video and other devices that display images</span></span>

<span data-ttu-id="3536e-110">На следующем рисунке показано начальное состояние воспроизведения видео, управляемого пользователем.</span><span class="sxs-lookup"><span data-stu-id="3536e-110">The following illustration shows the initial state of user-controlled video playback.</span></span> <span data-ttu-id="3536e-111">Используемый пример файла — CLOCK.AVI.</span><span class="sxs-lookup"><span data-stu-id="3536e-111">The sample file used is CLOCK.AVI.</span></span>

![Изображение clock.avi](images/mciwnd1.gif)

<span data-ttu-id="3536e-113">Окно МЦивнд содержит область воспроизведения видео и других устройств, отображающих изображения во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="3536e-113">The MCIWnd window includes a playback area for video and other devices that display images during playback.</span></span> <span data-ttu-id="3536e-114">МЦивнд пропускает область воспроизведения на устройствах аудио-Audio, в модулях MIDI и других устройствах, которые не записываются на экран.</span><span class="sxs-lookup"><span data-stu-id="3536e-114">MCIWnd omits the playback area from waveform-audio devices, MIDI sequencers, and other devices that do not write to the display.</span></span> <span data-ttu-id="3536e-115">На следующем рисунке показана область воспроизведения аудио-звука.</span><span class="sxs-lookup"><span data-stu-id="3536e-115">The following illustration shows the waveform-audio playback area.</span></span>

![изображение окна мЦивнд](images/mciwnd4.gif)

<span data-ttu-id="3536e-117">Кнопка **воспроизвести** находится в левом нижнем углу окна мЦивнд.</span><span class="sxs-lookup"><span data-stu-id="3536e-117">The **Play** button is located in the lower-left corner of the MCIWnd window.</span></span> <span data-ttu-id="3536e-118">Он отображается при остановке содержимого.</span><span class="sxs-lookup"><span data-stu-id="3536e-118">It appears when the content is stopped.</span></span> <span data-ttu-id="3536e-119">Пользователь может воспроизвести содержимое следующими способами:</span><span class="sxs-lookup"><span data-stu-id="3536e-119">The user can play the content in the following ways:</span></span>

-   <span data-ttu-id="3536e-120">Чтобы воспроизвести содержимое из текущей позицией воспроизведения, нажмите кнопку **воспроизвести** .</span><span class="sxs-lookup"><span data-stu-id="3536e-120">To play the content from the current playback position, select the **Play** button.</span></span>
-   <span data-ttu-id="3536e-121">Чтобы воспроизвести содержимое в полноэкранном режиме с текущей позицией воспроизведения, нажмите кнопку **Воспроизведение** , удерживая нажатой клавишу CTRL.</span><span class="sxs-lookup"><span data-stu-id="3536e-121">To play the content full-screen from the current playback position, select the **Play** button while holding down the CTRL key.</span></span>
-   <span data-ttu-id="3536e-122">Чтобы воспроизвести содержимое в обратном направлении от текущей позиции воспроизведения, нажмите кнопку **Воспроизведение** , удерживая нажатой клавишу Shift.</span><span class="sxs-lookup"><span data-stu-id="3536e-122">To play the content backward from the current playback position, select the **Play** button while holding down the SHIFT key.</span></span>

<span data-ttu-id="3536e-123">Кнопка **меню** , расположенная рядом с кнопкой **Воспроизведение** , активирует меню, позволяющее пользователю открывать и закрывать AVI-файлы, а также настраивать размер изображения, скорость воспроизведения и громкость.</span><span class="sxs-lookup"><span data-stu-id="3536e-123">The **Menu** button, located next to the **Play** button, activates a menu that allows the user to open and close audio-video interleaved (AVI) files, and to adjust the image size, playback speed, and volume.</span></span> <span data-ttu-id="3536e-124">(Пользователь также может активировать меню, щелкая правой кнопкой мыши каждый раз, когда курсор находится в клиентской области окна.) Меню также содержит команды для изменения конфигурации текущего устройства, копирования содержимого воспроизведения в буфер обмена и для выполнения команд MCI.</span><span class="sxs-lookup"><span data-stu-id="3536e-124">(The user can also activate the menu by clicking the right mouse button whenever the cursor is in the client area of the window.) The menu also includes commands to change the configuration of the current device, to copy the playback content to the clipboard, and to issue MCI commands.</span></span>

<span data-ttu-id="3536e-125">Значение TrackBar справа от кнопки **меню** представляет продолжительность воспроизведения (или записи) содержимого.</span><span class="sxs-lookup"><span data-stu-id="3536e-125">The trackbar to the right of the **Menu** button represents the duration of the playback (or recorded) content.</span></span> <span data-ttu-id="3536e-126">Ползунок на TrackBar представляет текущую положение воспроизведения внутри содержимого.</span><span class="sxs-lookup"><span data-stu-id="3536e-126">The slider on the trackbar represents the current playback position within the content.</span></span> <span data-ttu-id="3536e-127">Когда ползунок располагается в левом конце TrackBar, текущая позиция воспроизведения является началом содержимого.</span><span class="sxs-lookup"><span data-stu-id="3536e-127">When the slider is positioned at the left end of the trackbar, the current playback position is the beginning of the content.</span></span> <span data-ttu-id="3536e-128">Пользователь может переместиться в другое место в содержимом, перетащив ползунок на TrackBar.</span><span class="sxs-lookup"><span data-stu-id="3536e-128">The user can move to different locations in the content by dragging the slider along the trackbar.</span></span> <span data-ttu-id="3536e-129">Кнопка " **Закрыть** " находится в левом нижнем углу окна мЦивнд.</span><span class="sxs-lookup"><span data-stu-id="3536e-129">The **Stop** button is located in the lower-left corner of the MCIWnd window.</span></span> <span data-ttu-id="3536e-130">Он отображается при воспроизведении содержимого.</span><span class="sxs-lookup"><span data-stu-id="3536e-130">It appears when the content is played.</span></span> <span data-ttu-id="3536e-131">На следующем рисунке показано, как выполняется воспроизведение видео.</span><span class="sxs-lookup"><span data-stu-id="3536e-131">The following illustration shows video playback in progress.</span></span>

![изображение воспроизведения видео](images/mciwnd2.gif)

<span data-ttu-id="3536e-133">Элементы управления МЦивнд также могут включать кнопку **записи** для устройств, которые могут записываться.</span><span class="sxs-lookup"><span data-stu-id="3536e-133">The MCIWnd controls can also include a **Record** button for devices that can record.</span></span> <span data-ttu-id="3536e-134">Кнопка **записи** помечается красным кружком и отображается только в том случае, если устройство поддерживает запись.</span><span class="sxs-lookup"><span data-stu-id="3536e-134">The **Record** button is marked with a red circle and appears only when the device is capable of recording.</span></span>

> [!Note]  
> <span data-ttu-id="3536e-135">Окно воспроизведения должно быть высвоено на границе с четырьмя пикселями для наилучшей производительности воспроизведения видео.</span><span class="sxs-lookup"><span data-stu-id="3536e-135">The playback window must be aligned on a four-pixel boundary for the best video playback performance.</span></span> <span data-ttu-id="3536e-136">Как правило, Windows автоматически выстраивает окно при его создании.</span><span class="sxs-lookup"><span data-stu-id="3536e-136">Typically, Windows aligns the window automatically when it is created.</span></span> <span data-ttu-id="3536e-137">Если пользователь перемещает или растягивает окно от первоначального положения, скорость воспроизведения видео может снизиться на половину.</span><span class="sxs-lookup"><span data-stu-id="3536e-137">If a user moves or stretches the window from its initial position, video playback speed might be reduced by half.</span></span>

 

 

 




