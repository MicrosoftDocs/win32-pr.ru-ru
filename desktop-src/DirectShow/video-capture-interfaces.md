---
description: Интерфейсы видеозаписи
ms.assetid: a7ec6607-d6fe-4cf4-b3f2-8636c4d15982
title: Интерфейсы видеозаписи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c88ab86833a3570789dee311b36d49f382c9cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673450"
---
# <a name="video-capture-interfaces"></a><span data-ttu-id="bdc3f-103">Интерфейсы видеозаписи</span><span class="sxs-lookup"><span data-stu-id="bdc3f-103">Video Capture Interfaces</span></span>

<span data-ttu-id="bdc3f-104">Эти интерфейсы поддерживают видеозапись, используя Microsoft® устройства с Windows® Driver Model (WDM) или устаревшее приложение Microsoft® Video для устройств Windows® (VFW).</span><span class="sxs-lookup"><span data-stu-id="bdc3f-104">These interfaces support video capture, using Microsoft® Windows® Driver Model (WDM) devices or legacy Microsoft® Video for Windows® (VFW) devices.</span></span>



| <span data-ttu-id="bdc3f-105">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="bdc3f-105">Interface</span></span>                                                        | <span data-ttu-id="bdc3f-106">Описание</span><span class="sxs-lookup"><span data-stu-id="bdc3f-106">Description</span></span>                                                                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bdc3f-107">**иаманалогвидеодекодер**</span><span class="sxs-lookup"><span data-stu-id="bdc3f-107">**IAMAnalogVideoDecoder**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamanalogvideodecoder)           | <span data-ttu-id="bdc3f-108">Управление цифрами видео на карте записи видео WDM.</span><span class="sxs-lookup"><span data-stu-id="bdc3f-108">Control video digitization on a WDM video capture card.</span></span>                                                      |
| [<span data-ttu-id="bdc3f-109">**иамбуффернеготиатион**</span><span class="sxs-lookup"><span data-stu-id="bdc3f-109">**IAMBufferNegotiation**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)             | <span data-ttu-id="bdc3f-110">Управление способом выделения буфера с помощью ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="bdc3f-110">Control how a pin allocates buffers.</span></span>                                                                         |
| [<span data-ttu-id="bdc3f-111">**иамкопикаптурефилепрогресс**</span><span class="sxs-lookup"><span data-stu-id="bdc3f-111">**IAMCopyCaptureFileProgress**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamcopycapturefileprogress) | <span data-ttu-id="bdc3f-112">Интерфейс обратного вызова для получения сведений о ходе операции копирования файла.</span><span class="sxs-lookup"><span data-stu-id="bdc3f-112">Callback interface to receive the progress of a file copy operation.</span></span>                                         |
| [<span data-ttu-id="bdc3f-113">**иамкроссбар**</span><span class="sxs-lookup"><span data-stu-id="bdc3f-113">**IAMCrossbar**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar)                               | <span data-ttu-id="bdc3f-114">Создание аппаратного подключения между источником аудио-или видеопотока WDM и устройством записи WDM.</span><span class="sxs-lookup"><span data-stu-id="bdc3f-114">Create a hardware connection between a WDM audio or video source and a WDM capture device.</span></span>                   |
| [<span data-ttu-id="bdc3f-115">**иамдроппедфрамес**</span><span class="sxs-lookup"><span data-stu-id="bdc3f-115">**IAMDroppedFrames**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes)                     | <span data-ttu-id="bdc3f-116">Запросите фильтр записи о производительности захвата.</span><span class="sxs-lookup"><span data-stu-id="bdc3f-116">Query a capture filter about capture performance.</span></span>                                                            |
| [<span data-ttu-id="bdc3f-117">**иамстреамконтрол**</span><span class="sxs-lookup"><span data-stu-id="bdc3f-117">**IAMStreamControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol)                     | <span data-ttu-id="bdc3f-118">Управление временем запуска и окончания отдельных потоков.</span><span class="sxs-lookup"><span data-stu-id="bdc3f-118">Control the start and stop times of individual streams.</span></span>                                                      |
| [<span data-ttu-id="bdc3f-119">**иамстреамконфиг**</span><span class="sxs-lookup"><span data-stu-id="bdc3f-119">**IAMStreamConfig**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)                       | <span data-ttu-id="bdc3f-120">Запросите и задайте формат вывода фильтра записи.</span><span class="sxs-lookup"><span data-stu-id="bdc3f-120">Query and set the capture filter's output format.</span></span>                                                            |
| [<span data-ttu-id="bdc3f-121">**иамвфвкаптуредиалогс**</span><span class="sxs-lookup"><span data-stu-id="bdc3f-121">**IAMVfwCaptureDialogs**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs)             | <span data-ttu-id="bdc3f-122">Отображение диалоговых окон, предоставляемых драйверами записи VFW.</span><span class="sxs-lookup"><span data-stu-id="bdc3f-122">Display the dialog boxes provided by VFW capture drivers.</span></span>                                                    |
| [<span data-ttu-id="bdc3f-123">**иамвидеоконтрол**</span><span class="sxs-lookup"><span data-stu-id="bdc3f-123">**IAMVideoControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol)                       | <span data-ttu-id="bdc3f-124">Управление изображением с устройства записи.</span><span class="sxs-lookup"><span data-stu-id="bdc3f-124">Control the picture from a capture device.</span></span>                                                                   |
| [<span data-ttu-id="bdc3f-125">**иамвидеопрокамп**</span><span class="sxs-lookup"><span data-stu-id="bdc3f-125">**IAMVideoProcAmp**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)                       | <span data-ttu-id="bdc3f-126">Настройте качество видеосигнала, например яркость, контрастность, цветовой тон, насыщенность, гамма и четкость.</span><span class="sxs-lookup"><span data-stu-id="bdc3f-126">Adjust the qualities of a video signal, such as brightness, contrast, hue, saturation, gamma, and sharpness.</span></span> |
| [<span data-ttu-id="bdc3f-127">**ICaptureGraphBuilder2**</span><span class="sxs-lookup"><span data-stu-id="bdc3f-127">**ICaptureGraphBuilder2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)           | <span data-ttu-id="bdc3f-128">Создание графов фильтра для видеозаписи.</span><span class="sxs-lookup"><span data-stu-id="bdc3f-128">Build filter graphs for video capture.</span></span>                                                                       |
| [<span data-ttu-id="bdc3f-129">**IFileSinkFilter2**</span><span class="sxs-lookup"><span data-stu-id="bdc3f-129">**IFileSinkFilter2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2)                     | <span data-ttu-id="bdc3f-130">Укажите имя и атрибуты выходного файла.</span><span class="sxs-lookup"><span data-stu-id="bdc3f-130">Specify the name and attributes of an output file.</span></span>                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="bdc3f-131">См. также</span><span class="sxs-lookup"><span data-stu-id="bdc3f-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdc3f-132">Интерфейсы управления внешними устройствами</span><span class="sxs-lookup"><span data-stu-id="bdc3f-132">External Device Control Interfaces</span></span>](external-device-control-interfaces.md)
</dt> <dt>

[<span data-ttu-id="bdc3f-133">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="bdc3f-133">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



