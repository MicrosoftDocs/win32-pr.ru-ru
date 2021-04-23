---
description: Содержит пример поля описания для файла MP4 или 3GP.
ms.assetid: ea157988-bd15-465c-bd6a-6d33cc1a0323
title: Атрибут MF_MT_MPEG4_SAMPLE_DESCRIPTION (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4620ae0b50a2c6f2dae7663aab0c49f13bc5a162
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912163"
---
# <a name="mf_mt_mpeg4_sample_description-attribute"></a><span data-ttu-id="68e6e-103">\_ \_ \_ Атрибут описания примера "MF MT MPEG4" \_</span><span class="sxs-lookup"><span data-stu-id="68e6e-103">MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION attribute</span></span>

<span data-ttu-id="68e6e-104">Содержит пример поля описания для файла MP4 или 3GP.</span><span class="sxs-lookup"><span data-stu-id="68e6e-104">Contains the sample description box for an MP4 or 3GP file.</span></span>

## <a name="data-type"></a><span data-ttu-id="68e6e-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="68e6e-105">Data type</span></span>

<span data-ttu-id="68e6e-106">**ДВУХБАЙТОВЫХ\[\]**</span><span class="sxs-lookup"><span data-stu-id="68e6e-106">**BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="68e6e-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="68e6e-107">Get/set</span></span>

<span data-ttu-id="68e6e-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес::-BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="68e6e-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="68e6e-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="68e6e-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="68e6e-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="68e6e-110">Applies to</span></span>

[<span data-ttu-id="68e6e-111">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="68e6e-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="68e6e-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68e6e-112">Remarks</span></span>

<span data-ttu-id="68e6e-113">В поле Описание примера описывается кодировка, используемая для потока в файле.</span><span class="sxs-lookup"><span data-stu-id="68e6e-113">The sample description box describes the encoding used for a stream in the file.</span></span>

<span data-ttu-id="68e6e-114">Источник файлов MPEG-4 задает этот атрибут для типа носителя для каждого потока.</span><span class="sxs-lookup"><span data-stu-id="68e6e-114">The MPEG-4 file source sets this attribute on the media type for each stream.</span></span> <span data-ttu-id="68e6e-115">Значением атрибута является необработанные данные в поле Описание образца.</span><span class="sxs-lookup"><span data-stu-id="68e6e-115">The value of the attribute is the raw data in the sample description box.</span></span> <span data-ttu-id="68e6e-116">Если источник файла MPEG-4 может выполнить синтаксический анализ образца описания, он также добавляет сведения о формате в тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="68e6e-116">If the MPEG-4 file source can parse the sample description, it also adds the format details to the media type.</span></span> <span data-ttu-id="68e6e-117">В противном случае приложение или декодер должны проанализировать пример описания в \_ \_ \_ \_ атрибуте описания образца Description MF.</span><span class="sxs-lookup"><span data-stu-id="68e6e-117">Otherwise, the application or the decoder must parse the sample description from the MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION attribute.</span></span>

<span data-ttu-id="68e6e-118">При задании этого атрибута в приемнике MPEG-4 с помощью метода [**имфмедиатипехандлер:: сеткуррентмедиатипе**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) данные для атрибута с описанием в формате MF, \_ записанные в виде \_ \_ описания образца, \_ не должны изменяться после отправки одного или нескольких выборок в приемник в соответствующем потоке [**имфстреамсинк::P роцесссампле**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) .</span><span class="sxs-lookup"><span data-stu-id="68e6e-118">When setting this attribute on MPEG-4 sink through [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) method, the data for the attribute MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION should not change after one or more samples have been sent to the sink on the corresponding stream's [**IMFStreamSink::ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) interface.</span></span>

<span data-ttu-id="68e6e-119">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="68e6e-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="68e6e-120">Требования</span><span class="sxs-lookup"><span data-stu-id="68e6e-120">Requirements</span></span>



| <span data-ttu-id="68e6e-121">Требование</span><span class="sxs-lookup"><span data-stu-id="68e6e-121">Requirement</span></span> | <span data-ttu-id="68e6e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="68e6e-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="68e6e-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68e6e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="68e6e-124">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="68e6e-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="68e6e-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68e6e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="68e6e-126">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="68e6e-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="68e6e-127">Header</span><span class="sxs-lookup"><span data-stu-id="68e6e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="68e6e-128"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="68e6e-128"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68e6e-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68e6e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68e6e-130">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="68e6e-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="68e6e-131">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="68e6e-131">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




