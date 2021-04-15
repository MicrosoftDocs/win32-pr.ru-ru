---
title: Определение и изменение текущей должности
description: Определение и изменение текущей должности
ms.assetid: 20f78dcd-3259-43c2-8da3-8cfc299252e6
keywords:
- Макрос МЦивнджетстарт
- Макрос МЦивнджетенд
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84a8e7022bdfcede526a730014a07deaf22fe66d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486861"
---
# <a name="determining-and-changing-the-current-position"></a><span data-ttu-id="07714-105">Определение и изменение текущей должности</span><span class="sxs-lookup"><span data-stu-id="07714-105">Determining and Changing the Current Position</span></span>

<span data-ttu-id="07714-106">Если файл или устройство связаны с окном МЦивнд, то позиции воспроизведения изначально задаются в начале содержимого, независимо от типа носителя.</span><span class="sxs-lookup"><span data-stu-id="07714-106">When a file or device is associated with an MCIWnd window, the playback position is initially set at the start of the content, regardless of the media type.</span></span> <span data-ttu-id="07714-107">Во время воспроизведения местоположение воспроизведения перемещается линейно по содержимому и, если воспроизведение не прерывается, в итоге достигает конца содержимого.</span><span class="sxs-lookup"><span data-stu-id="07714-107">During playback, the playback position moves linearly through the content and, if playback is uninterrupted, eventually reaches the end of the content.</span></span> <span data-ttu-id="07714-108">Если происходит прерывание, текущая позиция воспроизведения — это расположение, в котором было остановлено или приостановлено воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="07714-108">If an interruption occurs, the current playback position is the location at which playback was stopped or paused.</span></span>

<span data-ttu-id="07714-109">Расположения для начала и конца содержимого можно получить с помощью макросов [**мЦивнджетстарт**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) и [**мЦивнджетенд**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) .</span><span class="sxs-lookup"><span data-stu-id="07714-109">You can retrieve the locations for the beginning and end of the content by using the [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) and [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) macros.</span></span> <span data-ttu-id="07714-110">Длину содержимого можно определить путем вычитания значения, возвращаемого функцией **мЦивнджетстарт** , из значения, возвращенного **мЦивнджетенд**, или с помощью макроса [**мЦивнджетленгс**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) .</span><span class="sxs-lookup"><span data-stu-id="07714-110">You can determine the length of the content by subtracting the value returned by **MCIWndGetStart** from the value returned by **MCIWndGetEnd**, or by using the [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) macro.</span></span> <span data-ttu-id="07714-111">Текущую точку воспроизведения можно получить с помощью макроса [**мЦивнджетпоситион**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) . также можно получить точку воспроизведения как строку, завершающуюся нулем, с помощью макроса [**мЦивнджетпоситионстринг**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) .</span><span class="sxs-lookup"><span data-stu-id="07714-111">You can retrieve the current playback position by using the [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) macro, or you can retrieve the playback position as a null-terminated string by using the [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) macro.</span></span>

<span data-ttu-id="07714-112">Чтобы изменить текущую точку воспроизведения, используйте макросы [**мЦивндхоме**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome), [**мЦивнденд**](/windows/desktop/api/Vfw/nf-vfw-mciwndend)и [**мЦивндсик**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) .</span><span class="sxs-lookup"><span data-stu-id="07714-112">To change the current playback position, use the [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome), [**MCIWndEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndend), and [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) macros.</span></span> <span data-ttu-id="07714-113">Можно переместить положение воспроизведения в начало содержимого с помощью **мЦивндхоме** или до конца содержимого с помощью **мЦивнденд**.</span><span class="sxs-lookup"><span data-stu-id="07714-113">You can move the playback position to the start of the content by using **MCIWndHome** or to the end of the content by using **MCIWndEnd**.</span></span> <span data-ttu-id="07714-114">Используйте **мЦивндсик** , чтобы переместить позицию воспроизведения в любое место содержимого.</span><span class="sxs-lookup"><span data-stu-id="07714-114">Use **MCIWndSeek** to move the playback position to any location in the content.</span></span>

<span data-ttu-id="07714-115">Можно также выполнить шаг с заходом по содержимому с помощью макроса [**мЦивндстеп**](/windows/desktop/api/Vfw/nf-vfw-mciwndstep) .</span><span class="sxs-lookup"><span data-stu-id="07714-115">You can also step through the content by using the [**MCIWndStep**](/windows/desktop/api/Vfw/nf-vfw-mciwndstep) macro.</span></span> <span data-ttu-id="07714-116">Начиная с текущей позиции воспроизведения, этот макрос перемещает позиции воспроизведения вперед или назад с указанным шагом.</span><span class="sxs-lookup"><span data-stu-id="07714-116">Beginning from the current playback position, this macro moves the playback position forward or backward by a specified increment.</span></span>

> [!Note]  
> <span data-ttu-id="07714-117">Единицы, используемые для указания расположения, зависят от различных типов носителей и устройств.</span><span class="sxs-lookup"><span data-stu-id="07714-117">The units used to specify position vary among the different media types and devices.</span></span> <span data-ttu-id="07714-118">Например, позицией воспроизведения для AVI-файлов, используемых устройством МЦИАВИ, измеряется в кадрах. расположение для воспроизведения аудио-и звукового файлов и MIDI измеряется в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="07714-118">For example, the playback position for AVI files used by the MCIAVI device is measured in frames; the playback position for CD audio, waveform-audio, and MIDI files is measured in milliseconds.</span></span>

 

<span data-ttu-id="07714-119">Устройства для других типов мультимедиа и сторонних устройств могут использовать другие единицы.</span><span class="sxs-lookup"><span data-stu-id="07714-119">Devices for other media types and third-party devices might use other units.</span></span> <span data-ttu-id="07714-120">Дополнительные сведения об определении этих единиц см. в разделе [улучшения воспроизведения](playback-enhancements.md).</span><span class="sxs-lookup"><span data-stu-id="07714-120">For information about determining these units, see [Playback Enhancements](playback-enhancements.md).</span></span>

 

 




