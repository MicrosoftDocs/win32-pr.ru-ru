---
description: Интерфейсы аудиозаписи и подготовки к просмотру
ms.assetid: 79b42ffd-703a-4a7c-bb2d-5cfc2fbeb16c
title: Интерфейсы аудиозаписи и подготовки к просмотру
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f941c1220f1adc06a686d702e9db21095a8cb7e6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673089"
---
# <a name="audio-capture-and-rendering-interfaces"></a><span data-ttu-id="46b3b-103">Интерфейсы аудиозаписи и подготовки к просмотру</span><span class="sxs-lookup"><span data-stu-id="46b3b-103">Audio Capture and Rendering Interfaces</span></span>

<span data-ttu-id="46b3b-104">Эти интерфейсы поддерживают запись звука и отрисовку в DirectShow</span><span class="sxs-lookup"><span data-stu-id="46b3b-104">These interfaces support audio capture and rendering in DirectShow</span></span>



| <span data-ttu-id="46b3b-105">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="46b3b-105">Interface</span></span>                                              | <span data-ttu-id="46b3b-106">Описание</span><span class="sxs-lookup"><span data-stu-id="46b3b-106">Description</span></span>                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46b3b-107">**иамаудиоинпутмиксер**</span><span class="sxs-lookup"><span data-stu-id="46b3b-107">**IAMAudioInputMixer**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer)       | <span data-ttu-id="46b3b-108">Получите доступ к аналоговым входным данным на звуковой плате системы и настройте такие характеристики, как моно или стерео, уровень Mix, уровень панорамы, громкость, частота высоких частот и низкие значения.</span><span class="sxs-lookup"><span data-stu-id="46b3b-108">Access the analog inputs on the system's sound card and adjust characteristics, such as mono or stereo, mix level, pan level, loudness, treble, and bass.</span></span> |
| [<span data-ttu-id="46b3b-109">**иамаудиорендерерстатс**</span><span class="sxs-lookup"><span data-stu-id="46b3b-109">**IAMAudioRendererStats**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats) | <span data-ttu-id="46b3b-110">Получение статистических сведений о производительности аудио рендереринг.</span><span class="sxs-lookup"><span data-stu-id="46b3b-110">Get statistical performance information about audio renderering.</span></span>                                                                                          |
| [<span data-ttu-id="46b3b-111">**иамбуффернеготиатион**</span><span class="sxs-lookup"><span data-stu-id="46b3b-111">**IAMBufferNegotiation**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)   | <span data-ttu-id="46b3b-112">Управление тем, как фильтр записи звука выделяет буферы.</span><span class="sxs-lookup"><span data-stu-id="46b3b-112">Control how the audio capture filter allocates buffers.</span></span>                                                                                                   |
| [<span data-ttu-id="46b3b-113">**иамклоккславе**</span><span class="sxs-lookup"><span data-stu-id="46b3b-113">**IAMClockSlave**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamclockslave)                 | <span data-ttu-id="46b3b-114">Контролируйте допуск модуля подготовки звука, если он соответствует тарифам с другими часами.</span><span class="sxs-lookup"><span data-stu-id="46b3b-114">Control the tolerance of an audio renderer when it matches rates with another clock.</span></span>                                                                      |
| [<span data-ttu-id="46b3b-115">**иамдиректсаунд**</span><span class="sxs-lookup"><span data-stu-id="46b3b-115">**IAMDirectSound**</span></span>](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound)               | <span data-ttu-id="46b3b-116">Позволяет приложению указать, какое окно имеет фокус для управления воспроизведением звука DirectSound.</span><span class="sxs-lookup"><span data-stu-id="46b3b-116">Enables an application to specify which window has focus for controlling DirectSound audio playback.</span></span>                                                      |
| [<span data-ttu-id="46b3b-117">**иамресаурцеконтрол**</span><span class="sxs-lookup"><span data-stu-id="46b3b-117">**IAMResourceControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol)       | <span data-ttu-id="46b3b-118">Держите ресурс звукового устройства, прежде чем он понадобится.</span><span class="sxs-lookup"><span data-stu-id="46b3b-118">Hold an audio device resource before it is needed.</span></span>                                                                                                        |
| [<span data-ttu-id="46b3b-119">**иамстреамконфиг**</span><span class="sxs-lookup"><span data-stu-id="46b3b-119">**IAMStreamConfig**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)             | <span data-ttu-id="46b3b-120">Запросите и задайте формат вывода фильтра записи.</span><span class="sxs-lookup"><span data-stu-id="46b3b-120">Query and set the capture filter's output format.</span></span>                                                                                                         |
| [<span data-ttu-id="46b3b-121">**ибасикаудио**</span><span class="sxs-lookup"><span data-stu-id="46b3b-121">**IBasicAudio**</span></span>](/windows/desktop/api/Control/nn-control-ibasicaudio)                     | <span data-ttu-id="46b3b-122">Задайте громкость звукового выхода и баланс.</span><span class="sxs-lookup"><span data-stu-id="46b3b-122">Set audio output volume and balance.</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="46b3b-123">См. также</span><span class="sxs-lookup"><span data-stu-id="46b3b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46b3b-124">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="46b3b-124">Interfaces</span></span>](interfaces.md)
</dt> </dl>

 

 



