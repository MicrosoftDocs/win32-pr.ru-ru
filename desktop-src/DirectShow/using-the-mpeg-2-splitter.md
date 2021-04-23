---
description: Использование разделителя MPEG-2
ms.assetid: a08e079c-41be-475a-9e88-ee46d17fe938
title: Использование разделителя MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60505ef242c2ed9c1eab3031a005a2582b99608
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663756"
---
# <a name="using-the-mpeg-2-splitter"></a><span data-ttu-id="7339c-103">Использование разделителя MPEG-2</span><span class="sxs-lookup"><span data-stu-id="7339c-103">Using the MPEG-2 Splitter</span></span>

> [!Note]  
> <span data-ttu-id="7339c-104">Начиная с Microsoft® Windows® XP, фильтр разделителя MPEG-2 является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="7339c-104">Starting in Microsoft® Windows® XP, the MPEG-2 Splitter filter is deprecated.</span></span> <span data-ttu-id="7339c-105">Вместо этого используйте [демультиплексор MPEG-2](mpeg-2-demultiplexer.md) .</span><span class="sxs-lookup"><span data-stu-id="7339c-105">Use the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) instead.</span></span>

 

<span data-ttu-id="7339c-106">Фильтр разделителя MPEG-2 поддерживает воспроизведение потоков программы MPEG-2 в режиме извлечения, которые содержат по крайней мере один из следующих типов потоков.</span><span class="sxs-lookup"><span data-stu-id="7339c-106">The MPEG-2 Splitter filter supports pull-mode playback of MPEG-2 program streams that contain at least one of the following stream types.</span></span>

-   <span data-ttu-id="7339c-107">Видео MPEG-2</span><span class="sxs-lookup"><span data-stu-id="7339c-107">MPEG-2 video</span></span>
-   <span data-ttu-id="7339c-108">Звук MPEG-2</span><span class="sxs-lookup"><span data-stu-id="7339c-108">MPEG-2 audio</span></span>
-   <span data-ttu-id="7339c-109">Dolby AC-3 аудио в кодировке, определенная для DVD-Video</span><span class="sxs-lookup"><span data-stu-id="7339c-109">Dolby AC-3 audio encoded as defined for DVD-Video</span></span>
-   <span data-ttu-id="7339c-110">ЛПКМ (линейный импульс кода с модуляцией), закодированный в соответствии с определением для DVD-Video</span><span class="sxs-lookup"><span data-stu-id="7339c-110">LPCM (Linear Pulse Code Modulated) audio encoded as defined for DVD-Video</span></span>

<span data-ttu-id="7339c-111">Список типов мультимедиа, поддерживаемых разделителем MPEG-2, см. в разделе [типы мультимедиа разделителя MPEG-2](mpeg-2-splitter-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="7339c-111">For a list of media types that the MPEG-2 Splitter supports, see [MPEG-2 Splitter Media Types](mpeg-2-splitter-media-types.md).</span></span>

<span data-ttu-id="7339c-112">Разделитель MPEG-2 не анализирует потоки транспорта.</span><span class="sxs-lookup"><span data-stu-id="7339c-112">The MPEG-2 Splitter does not parse transport streams.</span></span> <span data-ttu-id="7339c-113">Используйте фильтр демультиплексора MPEG-2 для транспортных потоков (только режим принудительной отправки).</span><span class="sxs-lookup"><span data-stu-id="7339c-113">Use the MPEG-2 Demultiplexer filter for transport streams (push mode only).</span></span>

<span data-ttu-id="7339c-114">**Метки времени**</span><span class="sxs-lookup"><span data-stu-id="7339c-114">**Time Stamps**</span></span>

<span data-ttu-id="7339c-115">При воспроизведении потоков программы MPEG-2 фильтр разделителя MPEG-2 рассматривает первую ссылку на системные часы в качестве источника времени для любого потока.</span><span class="sxs-lookup"><span data-stu-id="7339c-115">When playing back MPEG-2 program streams, the MPEG-2 Splitter filter treats the first system clock reference it encounters as the time origin of any stream.</span></span> <span data-ttu-id="7339c-116">Это отличается от [разделителя потока MPEG-1](mpeg-1-stream-splitter-filter.md), который использует метки времени представления.</span><span class="sxs-lookup"><span data-stu-id="7339c-116">This differs from the [MPEG-1 Stream Splitter](mpeg-1-stream-splitter-filter.md), which uses presentation time stamps.</span></span> <span data-ttu-id="7339c-117">Метод [**иампарсе:: жетпарсетиме**](/previous-versions/windows/desktop/api/Amparse/nf-amparse-iamparse-getparsetime) возвращает (возможно, оценочное) время системных часов для обработанных данных.</span><span class="sxs-lookup"><span data-stu-id="7339c-117">The [**IAMParse::GetParseTime**](/previous-versions/windows/desktop/api/Amparse/nf-amparse-iamparse-getparsetime) method returns the (possibly estimated) stream system clock time for the data it has processed.</span></span>

<span data-ttu-id="7339c-118">Если фильтр разделителя MPEG-2 встречает входной пример со свойством ненепрерывности (свойство ненепрерывности может быть задано с помощью [**имедиасампле:: сетдисконтинуити**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) или [**IMediaSample2:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties)), он пропускает данные до тех пор, пока не найдет первый пакет в данных и настроит свои отметки времени, чтобы ссылка на системные часы (SCR) для этого пакета считалась идентичной для времени SCR до прекращения поддержки.</span><span class="sxs-lookup"><span data-stu-id="7339c-118">If the MPEG-2 splitter filter encounters an input sample with the discontinuity property set (the discontinuity property can be set by using [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) or [**IMediaSample2::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties)), it skips data until it finds the first pack in the data and adjusts its time stamps so that the system clock reference (SCR) for that pack is considered identical to the SCR time before the discontinuity.</span></span> <span data-ttu-id="7339c-119">Если часы SCR отображаются либо для перехода назад, либо для перехода вперед на несколько секунд, то (в строке со спецификацией потоковой передачи MPEG-2) это также рассматривается как ненепрерывность часов и вычитается видимое несоответствие часов из отметок времени, передаваемых нисходящим фильтрам.</span><span class="sxs-lookup"><span data-stu-id="7339c-119">If the SCR clock appears either to jump backward or to jump forward by more than a second, then (in line with the MPEG-2 program stream specification), this is also treated as a clock discontinuity and the apparent clock discrepancy is subtracted from the time stamps passed to downstream filters.</span></span>

<span data-ttu-id="7339c-120">**Выбор потока**</span><span class="sxs-lookup"><span data-stu-id="7339c-120">**Stream Selection**</span></span>

<span data-ttu-id="7339c-121">При воспроизведении потока программы MPEG-2 выбирается первый поток видео и первый найденный аудиопоток, проходящий через поток программы.</span><span class="sxs-lookup"><span data-stu-id="7339c-121">When playing back the MPEG-2 program stream, the first video stream and first audio stream found traversing the program stream are chosen.</span></span> <span data-ttu-id="7339c-122">Поддерживается до одного звука и один выходной ПИН-код видео.</span><span class="sxs-lookup"><span data-stu-id="7339c-122">Up to one audio and one video output pin are supported.</span></span> <span data-ttu-id="7339c-123">С помощью интерфейса [**иамстреамселект**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect) можно выбрать различные потоки одного типа вплоть до числа, указанного в заголовке системы.</span><span class="sxs-lookup"><span data-stu-id="7339c-123">Through the [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect) interface, different streams of the same type can be selected up to the number specified by the audio limit in the system header.</span></span> <span data-ttu-id="7339c-124">Для звука MPEG-2 в настоящий момент предполагается, что потоки формируют непрерывный диапазон, начиная с Stream 0xC0.</span><span class="sxs-lookup"><span data-stu-id="7339c-124">For MPEG-2 audio, it is currently assumed the streams form a contiguous range starting at stream 0xC0.</span></span>

<span data-ttu-id="7339c-125">**Поддерживаемые интерфейсы**</span><span class="sxs-lookup"><span data-stu-id="7339c-125">**Supported Interfaces**</span></span>

<span data-ttu-id="7339c-126">Фильтр разделителя MPEG-2 поддерживает следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="7339c-126">The MPEG-2 splitter filter supports the following interfaces.</span></span>

-   <span data-ttu-id="7339c-127">[**Иампарсе**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse).</span><span class="sxs-lookup"><span data-stu-id="7339c-127">[**IAMParse**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse).</span></span> <span data-ttu-id="7339c-128">Только потоковая передача MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="7339c-128">MPEG-2 program stream only.</span></span>
-   <span data-ttu-id="7339c-129">[**Иамстреамселект**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect).</span><span class="sxs-lookup"><span data-stu-id="7339c-129">[**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect).</span></span> <span data-ttu-id="7339c-130">Только потоковая передача MPEG-2, только звуковые потоки.</span><span class="sxs-lookup"><span data-stu-id="7339c-130">MPEG-2 program stream only, audio streams only.</span></span>
-   <span data-ttu-id="7339c-131">[**Имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking).</span><span class="sxs-lookup"><span data-stu-id="7339c-131">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking).</span></span> <span data-ttu-id="7339c-132">Включает поиск в режиме Byte.</span><span class="sxs-lookup"><span data-stu-id="7339c-132">Includes byte mode seeking.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7339c-133">См. также</span><span class="sxs-lookup"><span data-stu-id="7339c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7339c-134">Поддержка MPEG-2 в DirectShow</span><span class="sxs-lookup"><span data-stu-id="7339c-134">MPEG-2 Support in DirectShow</span></span>](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



