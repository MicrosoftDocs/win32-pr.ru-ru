---
description: Задает геометрию массива микрофона для схемы DSP для записи голоса.
ms.assetid: 1d91bdc8-5a09-487d-b45e-80d57a44cd0e
title: Свойство MFPKEY_WMAAECMA_MICARRAY_DESCPTR (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e433f50d9d7640575f1314c5acc13d7751fde0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692598"
---
# <a name="mfpkey_wmaaecma_micarray_descptr-property"></a><span data-ttu-id="654ed-103">МФПКЭЙ \_ вмааекма \_ микаррай \_ дескптр, свойство</span><span class="sxs-lookup"><span data-stu-id="654ed-103">MFPKEY\_WMAAECMA\_MICARRAY\_DESCPTR Property</span></span>

<span data-ttu-id="654ed-104">Задает геометрию массива микрофона для схемы DSP для записи голоса.</span><span class="sxs-lookup"><span data-stu-id="654ed-104">Specifies the microphone array geometry for the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="654ed-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="654ed-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="654ed-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="654ed-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="654ed-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="654ed-107">Data Type</span></span>

<span data-ttu-id="654ed-108">\_большой двоичный объект VT</span><span class="sxs-lookup"><span data-stu-id="654ed-108">VT\_BLOB</span></span>

## <a name="applies-to"></a><span data-ttu-id="654ed-109">Применение</span><span class="sxs-lookup"><span data-stu-id="654ed-109">Applies To</span></span>

-   [<span data-ttu-id="654ed-110">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="654ed-110">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="654ed-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="654ed-111">Remarks</span></span>

<span data-ttu-id="654ed-112">Значение этого свойства представляет собой [**ксаудионую \_ \_ \_ геометрическую структуру массива MIC**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksaudio_mic_array_geometry) .</span><span class="sxs-lookup"><span data-stu-id="654ed-112">The value of this property is a [**KSAUDIO\_MIC\_ARRAY\_GEOMETRY**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksaudio_mic_array_geometry) structure.</span></span> <span data-ttu-id="654ed-113">Эта структура определена в файле заголовка Ксмедиа. h.</span><span class="sxs-lookup"><span data-stu-id="654ed-113">This structure is defined in the header file KsMedia.h.</span></span> <span data-ttu-id="654ed-114">Чтобы получить геометрию для массива микрофона, запросите звуковое устройство \_ для \_ свойства Geometry для массива MIC кспроперти Audio, \_ \_ вызвав метод **иксконтрол:: кспроперти** на устройстве.</span><span class="sxs-lookup"><span data-stu-id="654ed-114">To get the microphone array geometry, query the audio device for the KSPROPERTY\_AUDIO\_MIC\_ARRAY\_GEOMETRY property by calling the **IKsControl::KSProperty** method on the device.</span></span> <span data-ttu-id="654ed-115">Дополнительные сведения о массивах микрофонов см. в техническом документе [Создание и использование массивов микрофонов для Windows Vista](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format).</span><span class="sxs-lookup"><span data-stu-id="654ed-115">For more information on microphone arrays, download the white paper [How to Build and Use Microphone Arrays for Windows Vista](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format).</span></span>

<span data-ttu-id="654ed-116">Задайте это свойство, если вы используете DSP в режиме фильтрации, а обработка массивов микрофонов включена.</span><span class="sxs-lookup"><span data-stu-id="654ed-116">Set this property if you are using the DSP in filter mode and microphone array processing is enabled.</span></span> <span data-ttu-id="654ed-117">При использовании DSP в режиме исходного кода DSP автоматически запрашивает у устройства сведения о геометрических данных.</span><span class="sxs-lookup"><span data-stu-id="654ed-117">If you are using the DSP in source mode, the DSP automatically queries the device for the geometry information.</span></span>

## <a name="requirements"></a><span data-ttu-id="654ed-118">Требования</span><span class="sxs-lookup"><span data-stu-id="654ed-118">Requirements</span></span>



| <span data-ttu-id="654ed-119">Требование</span><span class="sxs-lookup"><span data-stu-id="654ed-119">Requirement</span></span> | <span data-ttu-id="654ed-120">Значение</span><span class="sxs-lookup"><span data-stu-id="654ed-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="654ed-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="654ed-121">Minimum supported client</span></span><br/> | <span data-ttu-id="654ed-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="654ed-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="654ed-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="654ed-123">Minimum supported server</span></span><br/> | <span data-ttu-id="654ed-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="654ed-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="654ed-125">Header</span><span class="sxs-lookup"><span data-stu-id="654ed-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="654ed-126"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="654ed-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="654ed-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="654ed-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="654ed-128">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="654ed-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="654ed-129">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="654ed-129">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
