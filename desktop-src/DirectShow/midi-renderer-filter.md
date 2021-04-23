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
ms.openlocfilehash: 5fa27ceda0c249f88f4684979382495167cb9238
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909412"
---
# <a name="midi-renderer-filter"></a><span data-ttu-id="7997a-103">Фильтр модуля подготовки MIDI</span><span class="sxs-lookup"><span data-stu-id="7997a-103">MIDI Renderer Filter</span></span>

<span data-ttu-id="7997a-104">Фильтр модуля подготовки MIDI отрисовывает данные MIDI из фильтра [средства синтаксического анализа MIDI](midi-parser-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="7997a-104">The MIDI Renderer filter renders MIDI data from the [MIDI Parser](midi-parser-filter.md) filter.</span></span>



| <span data-ttu-id="7997a-105">Метка</span><span class="sxs-lookup"><span data-stu-id="7997a-105">Label</span></span> | <span data-ttu-id="7997a-106">Значение</span><span class="sxs-lookup"><span data-stu-id="7997a-106">Value</span></span> |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7997a-107">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="7997a-107">Filter Interfaces</span></span>                        | <span data-ttu-id="7997a-108">[**Иамклоккславе**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave), [**иамдиректсаунд**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound), [**иамресаурцеконтрол**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**ибасикаудио**](/windows/desktop/api/Control/nn-control-ibasicaudio), [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)</span><span class="sxs-lookup"><span data-stu-id="7997a-108">[**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave), [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound), [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)</span></span> |
| <span data-ttu-id="7997a-109">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="7997a-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="7997a-110">MEDIATYPE \_ MIDI, медиасубтипе \_ null</span><span class="sxs-lookup"><span data-stu-id="7997a-110">MEDIATYPE\_Midi, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="7997a-111">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="7997a-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="7997a-112">[**Имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="7997a-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="7997a-113">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="7997a-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="7997a-114">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="7997a-114">Not applicable</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="7997a-115">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="7997a-115">Output Pin Interfaces</span></span>                    | <span data-ttu-id="7997a-116">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="7997a-116">Not applicable</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="7997a-117">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="7997a-117">Filter CLSID</span></span>                             | <span data-ttu-id="7997a-118">\_АВИМИДИРЕНДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="7997a-118">CLSID\_AVIMIDIRender</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="7997a-119">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="7997a-119">Property Page CLSID</span></span>                      | <span data-ttu-id="7997a-120">Нет страницы свойств</span><span class="sxs-lookup"><span data-stu-id="7997a-120">No property page</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="7997a-121">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="7997a-121">Executable</span></span>                               | <span data-ttu-id="7997a-122">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="7997a-122">quartz.dll</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="7997a-123">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="7997a-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="7997a-124">неуспешный \_ приоритет</span><span class="sxs-lookup"><span data-stu-id="7997a-124">MERIT\_PREFERRED</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="7997a-125">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="7997a-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="7997a-126">\_МИДИРЕНДЕРЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="7997a-126">CLSID\_MidiRendererCategory</span></span>                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="7997a-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7997a-127">Remarks</span></span>

<span data-ttu-id="7997a-128">GUID для типа формата имеет **значение NULL**, но блок форматирования содержит следующую структуру:</span><span class="sxs-lookup"><span data-stu-id="7997a-128">The GUID for the format type is **NULL**, but the format block contains the following structure:</span></span>


```C++
typedef struct _MIDIFORMAT {
    DWORD       dwDivision;
    DWORD       dwReserved[7];
} MIDIFORMAT, FAR * LPMIDIFORMAT;
```



<span data-ttu-id="7997a-129">Элемент **двдивисион** указывает деление времени файла.</span><span class="sxs-lookup"><span data-stu-id="7997a-129">The **dwDivision** member specifies the time division of the file.</span></span> <span data-ttu-id="7997a-130">Деление времени указывается в заголовке любого стандартного файла MIDI (SMF) в `MThd` блоке.</span><span class="sxs-lookup"><span data-stu-id="7997a-130">The time division is given in the header of any standard MIDI file (SMF), in the `MThd` chunk.</span></span> <span data-ttu-id="7997a-131">Модуль подготовки MIDI задает это свойство в потоке данных MIDI, вызывая функцию **мидистреампроперти** .</span><span class="sxs-lookup"><span data-stu-id="7997a-131">The MIDI Renderer sets this property on the MIDI data stream by calling the **midiStreamProperty** function.</span></span>

<span data-ttu-id="7997a-132">Примеры из фильтра средства синтаксического анализа MIDI содержат одну секунду данных MIDI.</span><span class="sxs-lookup"><span data-stu-id="7997a-132">Samples from the MIDI Parser filter contain one second of MIDI data.</span></span> <span data-ttu-id="7997a-133">Модуль подготовки MIDI использует функцию **мидистреамаут** для отображения данных MIDI.</span><span class="sxs-lookup"><span data-stu-id="7997a-133">The MIDI Renderer uses the **midiStreamOut** function to render the MIDI data.</span></span> <span data-ttu-id="7997a-134">Каждый пример представляет собой точку синхронизации: начало буфера содержит все команды, необходимые для задания правильного состояния визуализации буфера.</span><span class="sxs-lookup"><span data-stu-id="7997a-134">Each sample is a synchronization point: the start of the buffer contains all of the commands necessary to set the correct state for rendering that buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="7997a-135">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="7997a-135">Requirements</span></span>



| <span data-ttu-id="7997a-136">Требование</span><span class="sxs-lookup"><span data-stu-id="7997a-136">Requirement</span></span> | <span data-ttu-id="7997a-137">Значение</span><span class="sxs-lookup"><span data-stu-id="7997a-137">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7997a-138">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7997a-138">Header</span></span><br/> | <dl> <span data-ttu-id="7997a-139"><dt>Windows. Devices. MIDI. h</dt></span><span class="sxs-lookup"><span data-stu-id="7997a-139"><dt>Windows.devices.midi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7997a-140">См. также</span><span class="sxs-lookup"><span data-stu-id="7997a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7997a-141">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="7997a-141">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




