---
title: Структура _WAVEFORMATEX
description: Структура \_WAVEFORMATEX определяет формат данных, содержащих форму звуковой волны.
ms.assetid: 2128f07a-4858-49b7-b031-16d4a84c9d32
keywords:
- _WAVEFORMATEX структура диспетчер устройств Windows Media
topic_type:
- apiref
api_name:
- _WAVEFORMATEX
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1d0ede83e22033aee8f18d11b6230e471e0dfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694855"
---
# <a name="_waveformatex-structure"></a><span data-ttu-id="9ce2f-104">\_Структура ВАВЕФОРМАТЕКС</span><span class="sxs-lookup"><span data-stu-id="9ce2f-104">\_WAVEFORMATEX structure</span></span>

<span data-ttu-id="9ce2f-105">Структура **\_ вавеформатекс** определяет формат данных звуковой волны.</span><span class="sxs-lookup"><span data-stu-id="9ce2f-105">The **\_WAVEFORMATEX** structure defines the format of waveform-audio data.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ce2f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ce2f-106">Syntax</span></span>


```C++
typedef struct _tWAVEFORMATEX {
  WORD  wFormatTag;
  WORD  nChannels;
  DWORD nSamplesPerSec;
  DWORD nAvgBytesPerSec;
  WORD  nBlockAlign;
  WORD  wBitsPerSample;
  WORD  cbSize;
} _WAVEFORMATEX;
```



## <a name="members"></a><span data-ttu-id="9ce2f-107">Члены</span><span class="sxs-lookup"><span data-stu-id="9ce2f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9ce2f-108">**вформаттаг**</span><span class="sxs-lookup"><span data-stu-id="9ce2f-108">**wFormatTag**</span></span>
</dt> <dd>

<span data-ttu-id="9ce2f-109">Необходимо задать формат или форматы, поддерживаемые устройством.</span><span class="sxs-lookup"><span data-stu-id="9ce2f-109">Must be set to a format or formats supported by the device.</span></span> <span data-ttu-id="9ce2f-110">Обратите внимание, что предыдущие версии диспетчер устройств Windows Media рекомендуются с использованием \_ формата Wave вмдм \_ \_ для указания поддержки всех форматов.</span><span class="sxs-lookup"><span data-stu-id="9ce2f-110">Note that previous versions of the Windows Media Device Manager recommended using WMDM\_WAVE\_FORMAT\_ALL to indicate support for all formats.</span></span> <span data-ttu-id="9ce2f-111">Однако это не рекомендуется, так как разные проигрыватели мультимедиа будут интерпретировать это по-разному, и несколько устройств могут реально воспроизводить любой формат файла.</span><span class="sxs-lookup"><span data-stu-id="9ce2f-111">However, this is no longer recommended, as different media players will interpret this in different ways, and few devices can truly play any file format.</span></span> <span data-ttu-id="9ce2f-112">Теперь рекомендуется использовать \_ Допустимые значения свойства enum вмдм, \_ \_ \_ \_ любое значение перечисления [**\_ \_ \_ допустимых \_ \_ значений вмдм enum Prop**](wmdm-enum-prop-valid-values-form.md) , или, однако, лучше указать диапазон форматов с помощью структуры [**\_ \_ \_ диапазона значений свойств вмдм**](wmdm-prop-values-range.md) .</span><span class="sxs-lookup"><span data-stu-id="9ce2f-112">It is now recommended that you use the WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY value of the [**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**](wmdm-enum-prop-valid-values-form.md) enumeration, or better yet specify a range of formats with the [**WMDM\_PROP\_VALUES\_RANGE**](wmdm-prop-values-range.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9ce2f-113">**нчаннелс**</span><span class="sxs-lookup"><span data-stu-id="9ce2f-113">**nChannels**</span></span>
</dt> <dd>

<span data-ttu-id="9ce2f-114">Число каналов в данных аудио-сигнала.</span><span class="sxs-lookup"><span data-stu-id="9ce2f-114">Number of channels in the waveform-audio data.</span></span> <span data-ttu-id="9ce2f-115">Данные монаурал используют один канал, а стерео — два канала.</span><span class="sxs-lookup"><span data-stu-id="9ce2f-115">Monaural data uses one channel, and stereo data uses two channels.</span></span>

</dd> <dt>

<span data-ttu-id="9ce2f-116">**нсамплесперсек**</span><span class="sxs-lookup"><span data-stu-id="9ce2f-116">**nSamplesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="9ce2f-117">Частота выборки, в примерах в секунду (герц), в которой каждый канал должен воспроизводиться или записываться.</span><span class="sxs-lookup"><span data-stu-id="9ce2f-117">Sample rate, in samples per second (Hertz), at which each channel must be played or recorded.</span></span> <span data-ttu-id="9ce2f-118">Распространенные значения для **нсамплесперсек** : 8,0 Килохертз (кГц), 11,025 кгц, 22,05 кгц и 44,1 кГц.</span><span class="sxs-lookup"><span data-stu-id="9ce2f-118">Common values for **nSamplesPerSec** are 8.0 kilohertz (kHz), 11.025 kHz, 22.05 kHz, and 44.1 kHz.</span></span>

</dd> <dt>

<span data-ttu-id="9ce2f-119">**навгбитесперсек**</span><span class="sxs-lookup"><span data-stu-id="9ce2f-119">**nAvgBytesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="9ce2f-120">Требуемая средняя скорость передачи данных для тега формата (в байтах в секунду).</span><span class="sxs-lookup"><span data-stu-id="9ce2f-120">Required average data-transfer rate for the format tag, in bytes per second.</span></span> <span data-ttu-id="9ce2f-121">Программное обеспечение для воспроизведения и записи может оценивать размеры буфера с помощью элемента **навгбитесперсек** .</span><span class="sxs-lookup"><span data-stu-id="9ce2f-121">Playback and recording software can estimate buffer sizes by using the **nAvgBytesPerSec** member.</span></span>

</dd> <dt>

<span data-ttu-id="9ce2f-122">**нблоккалигн**</span><span class="sxs-lookup"><span data-stu-id="9ce2f-122">**nBlockAlign**</span></span>
</dt> <dd>

<span data-ttu-id="9ce2f-123">Выравнивание блокировки в байтах.</span><span class="sxs-lookup"><span data-stu-id="9ce2f-123">Block alignment, in bytes.</span></span> <span data-ttu-id="9ce2f-124">Выравнивание блока — это минимальная атомарная единица данных для типа формата **вформаттаг** .</span><span class="sxs-lookup"><span data-stu-id="9ce2f-124">The block alignment is the minimum atomic unit of data for the **wFormatTag** format type.</span></span> <span data-ttu-id="9ce2f-125">Программное обеспечение для воспроизведения и записи должно обрабатывать несколько **нблоккалигн** байт данных за раз.</span><span class="sxs-lookup"><span data-stu-id="9ce2f-125">Playback and recording software must process a multiple of **nBlockAlign** bytes of data at a time.</span></span> <span data-ttu-id="9ce2f-126">Данные, записываемые и прочитанные с устройства, всегда должны начинаться в начале блока.</span><span class="sxs-lookup"><span data-stu-id="9ce2f-126">Data written and read from a device must always start at the beginning of a block.</span></span> <span data-ttu-id="9ce2f-127">Например, невозможно правильно начать воспроизведение данных PCM в середине примера (то есть на границе, которая не является согласованной).</span><span class="sxs-lookup"><span data-stu-id="9ce2f-127">For example, it is not possible to correctly start playing PCM data in the middle of a sample (that is, on a boundary that is not block aligned).</span></span>

</dd> <dt>

<span data-ttu-id="9ce2f-128">**вбитсперсампле**</span><span class="sxs-lookup"><span data-stu-id="9ce2f-128">**wBitsPerSample**</span></span>
</dt> <dd>

<span data-ttu-id="9ce2f-129">Бит на выборку для типа формата **вформаттаг** .</span><span class="sxs-lookup"><span data-stu-id="9ce2f-129">Bits per sample for the **wFormatTag** format type.</span></span>

</dd> <dt>

<span data-ttu-id="9ce2f-130">**кбсизе**</span><span class="sxs-lookup"><span data-stu-id="9ce2f-130">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="9ce2f-131">Этот элемент не учитывается.</span><span class="sxs-lookup"><span data-stu-id="9ce2f-131">This member is ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9ce2f-132">Требования</span><span class="sxs-lookup"><span data-stu-id="9ce2f-132">Requirements</span></span>



| <span data-ttu-id="9ce2f-133">Требование</span><span class="sxs-lookup"><span data-stu-id="9ce2f-133">Requirement</span></span> | <span data-ttu-id="9ce2f-134">Значение</span><span class="sxs-lookup"><span data-stu-id="9ce2f-134">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9ce2f-135">Header</span><span class="sxs-lookup"><span data-stu-id="9ce2f-135">Header</span></span><br/> | <dl> <span data-ttu-id="9ce2f-136"><dt>Вмдм. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9ce2f-136"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ce2f-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ce2f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ce2f-138">**Имдспдевице:: Жетформатсуппорт**</span><span class="sxs-lookup"><span data-stu-id="9ce2f-138">**IMDSPDevice::GetFormatSupport**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)
</dt> <dt>

[<span data-ttu-id="9ce2f-139">**Имдспстораже:: Креатестораже**</span><span class="sxs-lookup"><span data-stu-id="9ce2f-139">**IMDSPStorage::CreateStorage**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-createstorage)
</dt> <dt>

[<span data-ttu-id="9ce2f-140">**Имдспстораже:: OutAttribute**</span><span class="sxs-lookup"><span data-stu-id="9ce2f-140">**IMDSPStorage::GetAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
</dt> <dt>

[<span data-ttu-id="9ce2f-141">**Ивмдмдевице:: Жетформатсуппорт**</span><span class="sxs-lookup"><span data-stu-id="9ce2f-141">**IWMDMDevice::GetFormatSupport**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport)
</dt> <dt>

[<span data-ttu-id="9ce2f-142">**Ивмдмоператион:: Жетобжектаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="9ce2f-142">**IWMDMOperation::GetObjectAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectattributes)
</dt> <dt>

[<span data-ttu-id="9ce2f-143">**Ивмдмоператион:: Сетобжектаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="9ce2f-143">**IWMDMOperation::SetObjectAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-setobjectattributes)
</dt> <dt>

[<span data-ttu-id="9ce2f-144">**Ивмдмстораже:: OutAttribute**</span><span class="sxs-lookup"><span data-stu-id="9ce2f-144">**IWMDMStorage::GetAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes)
</dt> <dt>

[<span data-ttu-id="9ce2f-145">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="9ce2f-145">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





