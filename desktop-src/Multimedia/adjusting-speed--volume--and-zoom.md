---
title: Настройка скорости, объема и масштаба
description: Настройка скорости, объема и масштаба
ms.assetid: 16cfbf86-911e-4cf3-9640-69fffc09c1ed
keywords:
- Макрос МЦивндсетспид
- Макрос МЦивнджетспид
- Макрос МЦивндсетволуме
- Макрос МЦивнджетволуме
- Макрос МЦивндсетзум
- Макрос МЦивнджетзум
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f02b1e14a5153e279e3cfdf6989beade31cf6f3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410991"
---
# <a name="adjusting-speed-volume-and-zoom"></a><span data-ttu-id="22f38-109">Настройка скорости, объема и масштаба</span><span class="sxs-lookup"><span data-stu-id="22f38-109">Adjusting Speed, Volume, and Zoom</span></span>

<span data-ttu-id="22f38-110">Макрос Speed, Volume и Zoom предоставляет функциональные возможности команд **Просмотр**, **Громкость** и **скорость** в меню мЦивнд.</span><span class="sxs-lookup"><span data-stu-id="22f38-110">The speed, volume, and zoom macros provide the functionality of the **View**, **Volume**, and **Speed** commands on the MCIWnd menu.</span></span> <span data-ttu-id="22f38-111">Макросы, описанные в этом разделе, обычно используются с видео и другими устройствами, которые отображают изображения во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="22f38-111">The macros described in this section are generally used with video and other devices that display images during playback.</span></span>

<span data-ttu-id="22f38-112">Некоторые устройства поддерживают несколько изменений скорости воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="22f38-112">Some devices support multiple playback speed changes.</span></span> <span data-ttu-id="22f38-113">Скорость воспроизведения для этих устройств можно задать с помощью макроса [**мЦивндсетспид**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) .</span><span class="sxs-lookup"><span data-stu-id="22f38-113">You can set the playback speed for these devices by using the [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) macro.</span></span> <span data-ttu-id="22f38-114">Этот макрос определяет скорость воспроизведения как 1000.</span><span class="sxs-lookup"><span data-stu-id="22f38-114">This macro defines the playback speed as 1000.</span></span> <span data-ttu-id="22f38-115">Более высокие значения указывают на более быстрые скорости.</span><span class="sxs-lookup"><span data-stu-id="22f38-115">Higher values indicate faster speeds.</span></span> <span data-ttu-id="22f38-116">Низкие значения указывают на медленные скорости.</span><span class="sxs-lookup"><span data-stu-id="22f38-116">Lower values indicate slower speeds.</span></span>

<span data-ttu-id="22f38-117">Текущую скорость воспроизведения можно получить с помощью макроса [**мЦивнджетспид**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) .</span><span class="sxs-lookup"><span data-stu-id="22f38-117">You can retrieve the current playback speed by using the [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) macro.</span></span> <span data-ttu-id="22f38-118">В этом макросе используются те же значения и диапазоны, что и для **мЦивндсетспид**.</span><span class="sxs-lookup"><span data-stu-id="22f38-118">This macro uses the same values and range as those used by **MCIWndSetSpeed**.</span></span>

<span data-ttu-id="22f38-119">Некоторые устройства поддерживают изменения томов.</span><span class="sxs-lookup"><span data-stu-id="22f38-119">Some devices support volume changes.</span></span> <span data-ttu-id="22f38-120">Изменить или задать том можно с помощью макроса [**мЦивндсетволуме**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) .</span><span class="sxs-lookup"><span data-stu-id="22f38-120">You can adjust or set the volume by using the [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) macro.</span></span> <span data-ttu-id="22f38-121">Этот макрос определяет стандартный уровень громкости 1000.</span><span class="sxs-lookup"><span data-stu-id="22f38-121">This macro defines the normal volume level as 1000.</span></span> <span data-ttu-id="22f38-122">Более высокие значения указывают на громкость.</span><span class="sxs-lookup"><span data-stu-id="22f38-122">Higher values indicate louder volumes.</span></span> <span data-ttu-id="22f38-123">Более низкие значения указывают на более тихие тома.</span><span class="sxs-lookup"><span data-stu-id="22f38-123">Lower values indicate quieter volumes.</span></span>

<span data-ttu-id="22f38-124">Текущий уровень громкости можно получить с помощью макроса [**мЦивнджетволуме**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) .</span><span class="sxs-lookup"><span data-stu-id="22f38-124">You can retrieve the current volume level by using the [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) macro.</span></span> <span data-ttu-id="22f38-125">В этом макросе используются те же числовые значения и диапазоны, что и для **мЦивндсетволуме**.</span><span class="sxs-lookup"><span data-stu-id="22f38-125">This macro uses the same numerical values and range as those used by **MCIWndSetVolume**.</span></span>

<span data-ttu-id="22f38-126">Для устройств, использующих окно воспроизведения, МЦивнд поддерживает функцию масштабирования, которая задает размер образа воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="22f38-126">For devices that use a playback window, MCIWnd supports a zoom feature that sets the size of the playback image.</span></span> <span data-ttu-id="22f38-127">Размер образа воспроизведения можно задать с помощью макроса [**мЦивндсетзум**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) .</span><span class="sxs-lookup"><span data-stu-id="22f38-127">You can set the playback image size by using the [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) macro.</span></span> <span data-ttu-id="22f38-128">Макрос переопределяет размер образа воспроизведения, сохраняя постоянную пропорцию изображения.</span><span class="sxs-lookup"><span data-stu-id="22f38-128">The macro redefines the playback image size while maintaining a constant aspect ratio for the image.</span></span> <span data-ttu-id="22f38-129">Значение масштаба определяется в процентах от размера исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="22f38-129">The zoom value is defined as a percentage of the original image size.</span></span> <span data-ttu-id="22f38-130">Таким образом, 100 представляет исходный размер изображения, 50 указывает, что отображаемое изображение имеет половину его исходного размера, а 200 означает, что отображаемое изображение дважды имеет его исходный размер.</span><span class="sxs-lookup"><span data-stu-id="22f38-130">Thus, 100 represents the original image size, 50 indicates the image shown is half its original size, and 200 indicates that the image shown is twice its original size.</span></span>

<span data-ttu-id="22f38-131">Текущее значение масштаба можно получить с помощью макроса [**мЦивнджетзум**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) .</span><span class="sxs-lookup"><span data-stu-id="22f38-131">You can retrieve the current zoom value by using the [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) macro.</span></span> <span data-ttu-id="22f38-132">В этом макросе используются те же значения и диапазоны, что и для **мЦивндсетзум**.</span><span class="sxs-lookup"><span data-stu-id="22f38-132">This macro uses the same values and range as those used by **MCIWndSetZoom**.</span></span>

> [!Note]  
> <span data-ttu-id="22f38-133">Стандартные видеодрайверы MCI и аудио-файлы не поддерживают изменения громкости или скорости.</span><span class="sxs-lookup"><span data-stu-id="22f38-133">The standard MCI CD audio and waveform-audio drivers do not support volume or speed changes.</span></span>

 

 

 




