---
title: Указание форматов времени
description: Указание форматов времени
ms.assetid: 11d28d63-ed3e-4137-b9d8-1681bf0e33ff
keywords:
- Макрос МЦивнджеттимеформат
- Макрос МЦивндсеттимеформат
- Макрос МЦивндусетиме
- Макрос МЦивндусефрамес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e390e811bde4d797572c19f372923906f6b738b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330059"
---
# <a name="specifying-time-formats"></a><span data-ttu-id="ff1bb-107">Указание форматов времени</span><span class="sxs-lookup"><span data-stu-id="ff1bb-107">Specifying Time Formats</span></span>

<span data-ttu-id="ff1bb-108">Типы данных мультимедиа обычно могут использовать время для обнаружения значимых позиций в содержимом.</span><span class="sxs-lookup"><span data-stu-id="ff1bb-108">Multimedia data types typically can use time to identify significant positions within their content.</span></span> <span data-ttu-id="ff1bb-109">Распространенные форматы времени: миллисекунды, дорожки и кадры; также существуют и другие менее распространенные форматы времени, такие как SMPTE (общество изображений и телевизионных специалистов) 24.</span><span class="sxs-lookup"><span data-stu-id="ff1bb-109">Common time formats are milliseconds, tracks, and frames; other less common time formats, such as SMPTE (Society of Motion Picture and Television Engineers) 24, also exist.</span></span> <span data-ttu-id="ff1bb-110">Время — это формат и справочная система для звуковых данных аудио, MIDI и CD.</span><span class="sxs-lookup"><span data-stu-id="ff1bb-110">Time is the format and reference system for waveform-audio, MIDI, and CD audio data.</span></span> <span data-ttu-id="ff1bb-111">Видео поддерживает время, даже если оно записано как последовательность кадров (поток), которая обычно воспроизводится с определенной скоростью.</span><span class="sxs-lookup"><span data-stu-id="ff1bb-111">Video supports time even though it is recorded as a sequence of frames (stream) that is typically played at a specific speed.</span></span> <span data-ttu-id="ff1bb-112">Для обозначения формата времени доступны несколько макросов.</span><span class="sxs-lookup"><span data-stu-id="ff1bb-112">Several macros are available for designating time format.</span></span>

<span data-ttu-id="ff1bb-113">Вы можете получить текущий формат времени для файла или устройства с помощью макроса [**мЦивнджеттимеформат**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="ff1bb-113">You can retrieve the current time format for a file or device by using the [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) macro.</span></span> <span data-ttu-id="ff1bb-114">Можно изменить текущий формат времени на любой другой формат времени, поддерживаемый устройством, с помощью макроса [**мЦивндсеттимеформат**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="ff1bb-114">You can change the current time format to any other time format supported by a device by using the [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) macro.</span></span> <span data-ttu-id="ff1bb-115">Или можно задать формат времени равным миллисекундам или кадрам с помощью макросов [**мЦивндусетиме**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) или [**мЦивндусефрамес**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) .</span><span class="sxs-lookup"><span data-stu-id="ff1bb-115">Or you can the set the time format to milliseconds or frames by using the [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) or [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) macros.</span></span>

> [!Note]  
> <span data-ttu-id="ff1bb-116">Непостоянное форматирование, например дорожные и SMPTE, может вызвать нестабильное поведение панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="ff1bb-116">Noncontinuous formats, such as tracks and SMPTE, can cause the toolbar to behave erratically.</span></span> <span data-ttu-id="ff1bb-117">Для этих форматов времени может потребоваться отключить панель инструментов, указав \_ стиль окна мЦивндф ноплайбар при создании окна мЦивнд.</span><span class="sxs-lookup"><span data-stu-id="ff1bb-117">For these time formats, you might want to turn off the toolbar by specifying the MCIWNDF\_NOPLAYBAR window style when creating an MCIWnd window.</span></span>

 

 

 




