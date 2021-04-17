---
description: Фильтр модуля подготовки MIDI отрисовывает данные MIDI из фильтра средства синтаксического анализа MIDI.
ms.assetid: 2675a21d-41d0-4095-96c4-f12f52c00d5a
title: Фильтр модуля подготовки MIDI (Windows. Devices. MIDI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MIDI
api_type:
- HeaderDef
api_location:
- windows.devices.midi.h
ms.openlocfilehash: 060bb00629b78fb1edbfbfd193aeaf7514c98ba4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689200"
---
# <a name="midi-renderer-filter"></a><span data-ttu-id="f8b9a-103">Фильтр модуля подготовки MIDI</span><span class="sxs-lookup"><span data-stu-id="f8b9a-103">MIDI Renderer Filter</span></span>

<span data-ttu-id="f8b9a-104">Фильтр модуля подготовки MIDI отрисовывает данные MIDI из фильтра [средства синтаксического анализа MIDI](midi-parser-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="f8b9a-104">The MIDI Renderer filter renders MIDI data from the [MIDI Parser](midi-parser-filter.md) filter.</span></span>



|                                          |                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8b9a-105">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="f8b9a-105">Filter Interfaces</span></span>                        | <span data-ttu-id="f8b9a-106">[**Иамклоккславе**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave), [**иамдиректсаунд**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound), [**иамресаурцеконтрол**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**ибасикаудио**](/windows/desktop/api/Control/nn-control-ibasicaudio), [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)</span><span class="sxs-lookup"><span data-stu-id="f8b9a-106">[**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave), [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound), [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)</span></span> |
| <span data-ttu-id="f8b9a-107">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="f8b9a-107">Input Pin Media Types</span></span>                    | <span data-ttu-id="f8b9a-108">MEDIATYPE \_ MIDI, медиасубтипе \_ null</span><span class="sxs-lookup"><span data-stu-id="f8b9a-108">MEDIATYPE\_Midi, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="f8b9a-109">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="f8b9a-109">Input Pin Interfaces</span></span>                     | <span data-ttu-id="f8b9a-110">[**Имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="f8b9a-110">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="f8b9a-111">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="f8b9a-111">Output Pin Media Types</span></span>                   | <span data-ttu-id="f8b9a-112">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="f8b9a-112">Not applicable</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="f8b9a-113">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="f8b9a-113">Output Pin Interfaces</span></span>                    | <span data-ttu-id="f8b9a-114">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="f8b9a-114">Not applicable</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="f8b9a-115">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="f8b9a-115">Filter CLSID</span></span>                             | <span data-ttu-id="f8b9a-116">\_АВИМИДИРЕНДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="f8b9a-116">CLSID\_AVIMIDIRender</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="f8b9a-117">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="f8b9a-117">Property Page CLSID</span></span>                      | <span data-ttu-id="f8b9a-118">Нет страницы свойств</span><span class="sxs-lookup"><span data-stu-id="f8b9a-118">No property page</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="f8b9a-119">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="f8b9a-119">Executable</span></span>                               | <span data-ttu-id="f8b9a-120">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="f8b9a-120">quartz.dll</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="f8b9a-121">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="f8b9a-121">Merit</span></span>](merit.md)                       | <span data-ttu-id="f8b9a-122">неуспешный \_ приоритет</span><span class="sxs-lookup"><span data-stu-id="f8b9a-122">MERIT\_PREFERRED</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="f8b9a-123">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="f8b9a-123">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="f8b9a-124">\_МИДИРЕНДЕРЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="f8b9a-124">CLSID\_MidiRendererCategory</span></span>                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="f8b9a-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f8b9a-125">Remarks</span></span>

<span data-ttu-id="f8b9a-126">GUID для типа формата имеет **значение NULL**, но блок форматирования содержит следующую структуру:</span><span class="sxs-lookup"><span data-stu-id="f8b9a-126">The GUID for the format type is **NULL**, but the format block contains the following structure:</span></span>


```C++
typedef struct _MIDIFORMAT {
    DWORD       dwDivision;
    DWORD       dwReserved[7];
} MIDIFORMAT, FAR * LPMIDIFORMAT;
```



<span data-ttu-id="f8b9a-127">Элемент **двдивисион** указывает деление времени файла.</span><span class="sxs-lookup"><span data-stu-id="f8b9a-127">The **dwDivision** member specifies the time division of the file.</span></span> <span data-ttu-id="f8b9a-128">Деление времени указывается в заголовке любого стандартного файла MIDI (SMF) в `MThd` блоке.</span><span class="sxs-lookup"><span data-stu-id="f8b9a-128">The time division is given in the header of any standard MIDI file (SMF), in the `MThd` chunk.</span></span> <span data-ttu-id="f8b9a-129">Модуль подготовки MIDI задает это свойство в потоке данных MIDI, вызывая функцию **мидистреампроперти** .</span><span class="sxs-lookup"><span data-stu-id="f8b9a-129">The MIDI Renderer sets this property on the MIDI data stream by calling the **midiStreamProperty** function.</span></span>

<span data-ttu-id="f8b9a-130">Примеры из фильтра средства синтаксического анализа MIDI содержат одну секунду данных MIDI.</span><span class="sxs-lookup"><span data-stu-id="f8b9a-130">Samples from the MIDI Parser filter contain one second of MIDI data.</span></span> <span data-ttu-id="f8b9a-131">Модуль подготовки MIDI использует функцию **мидистреамаут** для отображения данных MIDI.</span><span class="sxs-lookup"><span data-stu-id="f8b9a-131">The MIDI Renderer uses the **midiStreamOut** function to render the MIDI data.</span></span> <span data-ttu-id="f8b9a-132">Каждый пример представляет собой точку синхронизации: начало буфера содержит все команды, необходимые для задания правильного состояния визуализации буфера.</span><span class="sxs-lookup"><span data-stu-id="f8b9a-132">Each sample is a synchronization point: the start of the buffer contains all of the commands necessary to set the correct state for rendering that buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8b9a-133">Требования</span><span class="sxs-lookup"><span data-stu-id="f8b9a-133">Requirements</span></span>



| <span data-ttu-id="f8b9a-134">Требование</span><span class="sxs-lookup"><span data-stu-id="f8b9a-134">Requirement</span></span> | <span data-ttu-id="f8b9a-135">Значение</span><span class="sxs-lookup"><span data-stu-id="f8b9a-135">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8b9a-136">Header</span><span class="sxs-lookup"><span data-stu-id="f8b9a-136">Header</span></span><br/> | <dl> <span data-ttu-id="f8b9a-137"><dt>Windows. Devices. MIDI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8b9a-137"><dt>Windows.devices.midi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8b9a-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8b9a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8b9a-139">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="f8b9a-139">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




