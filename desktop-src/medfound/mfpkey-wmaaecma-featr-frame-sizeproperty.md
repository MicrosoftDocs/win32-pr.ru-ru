---
description: Указывает размер звукового кадра, используемого DSP записи речи.
ms.assetid: b414ac34-c60a-4f43-924f-43431d6ba25f
title: Свойство MFPKEY_WMAAECMA_FEATR_FRAME_SIZE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5623cf3d26b968c7e7745fa0c01c69c034505cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692603"
---
# <a name="mfpkey_wmaaecma_featr_frame_size-property"></a><span data-ttu-id="c0a3f-103">МФПКЭЙ \_ вмааекма \_ феатр \_ \_ Размер кадра</span><span class="sxs-lookup"><span data-stu-id="c0a3f-103">MFPKEY\_WMAAECMA\_FEATR\_FRAME\_SIZE Property</span></span>

<span data-ttu-id="c0a3f-104">Указывает размер звукового кадра, используемого DSP записи речи.</span><span class="sxs-lookup"><span data-stu-id="c0a3f-104">Specifies the audio frame size used by the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="c0a3f-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="c0a3f-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="c0a3f-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="c0a3f-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="c0a3f-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c0a3f-107">Data Type</span></span>

<span data-ttu-id="c0a3f-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="c0a3f-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="c0a3f-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c0a3f-109">Default Value</span></span>

<span data-ttu-id="c0a3f-110">0</span><span class="sxs-lookup"><span data-stu-id="c0a3f-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="c0a3f-111">Применение</span><span class="sxs-lookup"><span data-stu-id="c0a3f-111">Applies To</span></span>

-   [<span data-ttu-id="c0a3f-112">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="c0a3f-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="c0a3f-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c0a3f-113">Remarks</span></span>

<span data-ttu-id="c0a3f-114">Алгоритм "Отмена акустического эха" обрабатывает образцы звука PCM по одному кадру за раз.</span><span class="sxs-lookup"><span data-stu-id="c0a3f-114">The acoustic echo cancellation (AEC) algorithm processes PCM audio samples one frame at a time.</span></span> <span data-ttu-id="c0a3f-115">Значение этого свойства равно размеру звукового кадра в образцах.</span><span class="sxs-lookup"><span data-stu-id="c0a3f-115">The value of this property is the size of the audio frame, in samples.</span></span> <span data-ttu-id="c0a3f-116">Перед установкой этого свойства необходимо присвоить свойству [ \_ \_ \_ режима компонента мфпкэй вмааекма](mfpkey-wmaaecma-feature-modeproperty.md) значение Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="c0a3f-116">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="c0a3f-117">DSP для захвата голоса поддерживает следующие размеры кадров:</span><span class="sxs-lookup"><span data-stu-id="c0a3f-117">The Voice Capture DSP supports the following frame sizes:</span></span>

-   <span data-ttu-id="c0a3f-118">80</span><span class="sxs-lookup"><span data-stu-id="c0a3f-118">80</span></span>
-   <span data-ttu-id="c0a3f-119">128</span><span class="sxs-lookup"><span data-stu-id="c0a3f-119">128</span></span>
-   <span data-ttu-id="c0a3f-120">160</span><span class="sxs-lookup"><span data-stu-id="c0a3f-120">160</span></span>
-   <span data-ttu-id="c0a3f-121">240</span><span class="sxs-lookup"><span data-stu-id="c0a3f-121">240</span></span>
-   <span data-ttu-id="c0a3f-122">256</span><span class="sxs-lookup"><span data-stu-id="c0a3f-122">256</span></span>
-   <span data-ttu-id="c0a3f-123">320</span><span class="sxs-lookup"><span data-stu-id="c0a3f-123">320</span></span>

<span data-ttu-id="c0a3f-124">Если значение этого свойства равно нулю, то DSP выбирает размер кадра в зависимости от системного режима и формата выходных данных.</span><span class="sxs-lookup"><span data-stu-id="c0a3f-124">If the value of this property is zero, the DSP selects the frame size based on the system mode and the output format.</span></span>

<span data-ttu-id="c0a3f-125">Однако для лучшей производительности рекомендуется, чтобы приложения использовали значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c0a3f-125">For the best performance, however, it is recommended that applications use the default value.</span></span> <span data-ttu-id="c0a3f-126">Если режимом обработки является только массив микрофонов, значение по умолчанию — 320.</span><span class="sxs-lookup"><span data-stu-id="c0a3f-126">If the processing mode is microphone array only, the default value is 320 samples.</span></span> <span data-ttu-id="c0a3f-127">Для всех остальных режимов обработки значение по умолчанию — 160 выборки.</span><span class="sxs-lookup"><span data-stu-id="c0a3f-127">For all other processing modes, the default value is 160 samples.</span></span> <span data-ttu-id="c0a3f-128">Дополнительные сведения о режимах обработки для схемы DSP для записи голоса см. в разделе [ \_ \_ \_ режим системы мфпкэй вмааекма](mfpkey-wmaaecma-system-modeproperty.md).</span><span class="sxs-lookup"><span data-stu-id="c0a3f-128">For more information about the processing modes of the Voice Capture DSP, see [MFPKEY\_WMAAECMA\_SYSTEM\_MODE](mfpkey-wmaaecma-system-modeproperty.md).</span></span>

<span data-ttu-id="c0a3f-129">После первого вызова [**имедиаобжект:: аллокатестреамингресаурцес**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) или [**Имедиаобжект::P роцессаутпут**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput)можно прочитать это свойство, чтобы получить фактический размер кадра, даже если в [**\_ \_ \_ режиме мфпкэй вмааекма функции**](mfpkey-wmaaecma-feature-modeproperty.md) задано значение false.</span><span class="sxs-lookup"><span data-stu-id="c0a3f-129">After the first call to [**IMediaObject::AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) or [**IMediaObject::ProcessOutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput), you can read this property to get the actual frame size in use, even when [**MFPKEY\_WMAAECMA\_FEATURE\_MODE**](mfpkey-wmaaecma-feature-modeproperty.md) is false.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0a3f-130">Требования</span><span class="sxs-lookup"><span data-stu-id="c0a3f-130">Requirements</span></span>



| <span data-ttu-id="c0a3f-131">Требование</span><span class="sxs-lookup"><span data-stu-id="c0a3f-131">Requirement</span></span> | <span data-ttu-id="c0a3f-132">Значение</span><span class="sxs-lookup"><span data-stu-id="c0a3f-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0a3f-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0a3f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c0a3f-134">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c0a3f-134">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c0a3f-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0a3f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c0a3f-136">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c0a3f-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c0a3f-137">Header</span><span class="sxs-lookup"><span data-stu-id="c0a3f-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0a3f-138"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0a3f-138"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0a3f-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c0a3f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0a3f-140">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c0a3f-140">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="c0a3f-141">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="c0a3f-141">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
