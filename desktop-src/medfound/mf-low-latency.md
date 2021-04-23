---
description: Включает обработку с низкой задержкой в конвейере Microsoft Media Foundation.
ms.assetid: 4D11B4D6-8CFF-4850-BF8F-9019A1F79153
title: Атрибут MF_LOW_LATENCY (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d1b0a89452256f01fc893ced7dc191fd064bbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815512"
---
# <a name="mf_low_latency-attribute"></a><span data-ttu-id="28d4d-103">\_Атрибут низкой \_ задержки MF</span><span class="sxs-lookup"><span data-stu-id="28d4d-103">MF\_LOW\_LATENCY attribute</span></span>

<span data-ttu-id="28d4d-104">Включает обработку с низкой задержкой в конвейере Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="28d4d-104">Enables low-latency processing in the Microsoft Media Foundation pipeline.</span></span>

## <a name="data-type"></a><span data-ttu-id="28d4d-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="28d4d-105">Data type</span></span>

<span data-ttu-id="28d4d-106">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="28d4d-106">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="28d4d-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="28d4d-107">Get/set</span></span>

<span data-ttu-id="28d4d-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="28d4d-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="28d4d-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="28d4d-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="28d4d-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="28d4d-110">Remarks</span></span>

<span data-ttu-id="28d4d-111">Низкая задержка определяется как наименьшая возможная задержка от момента создания (или получения) данных мультимедиа до их подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="28d4d-111">Low latency is defined as the smallest possible delay from when the media data is generated (or received) to when it is rendered.</span></span> <span data-ttu-id="28d4d-112">Низкая задержка желательно для сценариев связи в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="28d4d-112">Low latency is desirable for real-time communication scenarios.</span></span> <span data-ttu-id="28d4d-113">В других сценариях, таких как локальное воспроизведение или перекодирование, обычно не следует включать режим с низкой задержкой, так как он может повлиять на качество.</span><span class="sxs-lookup"><span data-stu-id="28d4d-113">For other scenarios, such as local playback or transcoding, you typically should not enable low-latency mode, because it can affect quality.</span></span>

> [!Note]  
> <span data-ttu-id="28d4d-114">Значение GUID этого атрибута идентично свойству [кодекапи \_ авловлатенцимоде](codecapi-avlowlatencymode.md) , определенному для интерфейса [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="28d4d-114">The GUID value of this attribute is identical to the [CODECAPI\_AVLowLatencyMode](codecapi-avlowlatencymode.md) property defined for the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span>

 

<span data-ttu-id="28d4d-115">Установите этот атрибут в компонентах конвейера следующим образом:</span><span class="sxs-lookup"><span data-stu-id="28d4d-115">Set this attribute on pipeline components as follows:</span></span>

-   <span data-ttu-id="28d4d-116">Источник мультимедиа: используйте метод [**имфмедиасаурцеекс:: жетсаурцеаттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getsourceattributes) .</span><span class="sxs-lookup"><span data-stu-id="28d4d-116">Media source: Use the [**IMFMediaSourceEx::GetSourceAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getsourceattributes) method.</span></span>
-   <span data-ttu-id="28d4d-117">Преобразование Media Foundation (MFT): используйте метод [**имфтрансформ:: InAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="28d4d-117">Media Foundation transform (MFT): Use the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="28d4d-118">Для кодировщиков кодировщик может поддерживать низкую задержку через интерфейс [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="28d4d-118">For encoders, the encoder might support low latency through the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span>
-   <span data-ttu-id="28d4d-119">Приемник мультимедиа. запросите приемник мультимедиа для интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="28d4d-119">Media sink: Query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="28d4d-120">Обычно приложения не задают этот атрибут непосредственно в компонентах конвейера, а устанавливают атрибут для одного из следующих объектов:</span><span class="sxs-lookup"><span data-stu-id="28d4d-120">Applications typically do not set this attribute directly on the pipeline components, but instead set the attribute on one of the following objects:</span></span>

-   <span data-ttu-id="28d4d-121">[Сеанс мультимедиа](media-session.md): используйте параметр *пконфигуатион* функции [**мфкреатемедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) или [**мфкреатепмпмедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) или задайте атрибут в топологии.</span><span class="sxs-lookup"><span data-stu-id="28d4d-121">[Media Session](media-session.md): Use the *pConfiguation* parameter of the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) or [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function, or else set the attribute on the topology.</span></span>
-   <span data-ttu-id="28d4d-122">[Модуль чтения исходного кода](source-reader.md): Задайте атрибут в свойствах конфигурации при создании модуля чтения исходного кода.</span><span class="sxs-lookup"><span data-stu-id="28d4d-122">[Source Reader](source-reader.md): Set the attribute with the configuration properties when you create the Source Reader.</span></span> <span data-ttu-id="28d4d-123">Дополнительные сведения см. в разделе [атрибуты модуля чтения исходного кода](source-reader-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="28d4d-123">For more information, see [Source Reader Attributes](source-reader-attributes.md).</span></span>
-   <span data-ttu-id="28d4d-124">[Модуль записи приемника](sink-writer.md): Задайте атрибут в свойствах конфигурации при создании модуля записи приемника.</span><span class="sxs-lookup"><span data-stu-id="28d4d-124">[Sink Writer](sink-writer.md): Set the attribute with the configuration properties when you create the Sink Writer.</span></span> <span data-ttu-id="28d4d-125">Дополнительные сведения см. в разделе [атрибуты модуля записи приемника](sink-writer-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="28d4d-125">For more information, see [Sink Writer Attributes](sink-writer-attributes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="28d4d-126">Требования</span><span class="sxs-lookup"><span data-stu-id="28d4d-126">Requirements</span></span>



| <span data-ttu-id="28d4d-127">Требование</span><span class="sxs-lookup"><span data-stu-id="28d4d-127">Requirement</span></span> | <span data-ttu-id="28d4d-128">Значение</span><span class="sxs-lookup"><span data-stu-id="28d4d-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="28d4d-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="28d4d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="28d4d-130">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="28d4d-130">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="28d4d-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="28d4d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="28d4d-132">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="28d4d-132">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="28d4d-133">Header</span><span class="sxs-lookup"><span data-stu-id="28d4d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="28d4d-134"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="28d4d-134"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28d4d-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28d4d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28d4d-136">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="28d4d-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="28d4d-137">Атрибуты модуля записи приемника</span><span class="sxs-lookup"><span data-stu-id="28d4d-137">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> <dt>

[<span data-ttu-id="28d4d-138">Атрибуты модуля чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="28d4d-138">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> <dt>

[<span data-ttu-id="28d4d-139">Атрибуты преобразования</span><span class="sxs-lookup"><span data-stu-id="28d4d-139">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 
