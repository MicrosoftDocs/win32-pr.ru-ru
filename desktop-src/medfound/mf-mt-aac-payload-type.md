---
description: Указывает тип полезных данных для потока расширенного кодирования звука (AAC).
ms.assetid: a032fcf4-2584-4047-adbd-d94d4fc4e841
title: Атрибут MF_MT_AAC_PAYLOAD_TYPE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3edba98bdac54b12fb6e3e44fb67373f7fce6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721013"
---
# <a name="mf_mt_aac_payload_type-attribute"></a><span data-ttu-id="36087-103">\_ \_ \_ Атрибут типа полезных данных MF MT AAC \_</span><span class="sxs-lookup"><span data-stu-id="36087-103">MF\_MT\_AAC\_PAYLOAD\_TYPE attribute</span></span>

<span data-ttu-id="36087-104">Указывает тип полезных данных для потока расширенного кодирования звука (AAC).</span><span class="sxs-lookup"><span data-stu-id="36087-104">Specifies the payload type of an Advanced Audio Coding (AAC) stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="36087-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="36087-105">Data type</span></span>

<span data-ttu-id="36087-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="36087-106">**UINT32**</span></span>

<span data-ttu-id="36087-107">Возможны следующие значения.</span><span class="sxs-lookup"><span data-stu-id="36087-107">The following values are possible.</span></span>



| <span data-ttu-id="36087-108">Значение</span><span class="sxs-lookup"><span data-stu-id="36087-108">Value</span></span>                                                                        | <span data-ttu-id="36087-109">Значение</span><span class="sxs-lookup"><span data-stu-id="36087-109">Meaning</span></span>                                                                                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="36087-110"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="36087-110"><dt>0</dt></span></span> </dl> | <span data-ttu-id="36087-111">Поток содержит только элементы необработанных \_ \_ блоков данных.</span><span class="sxs-lookup"><span data-stu-id="36087-111">The stream contains raw\_data\_block elements only.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="36087-112"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="36087-112"><dt>1</dt></span></span> </dl> | <span data-ttu-id="36087-113">Поток транспорта аудиоданных (ADTS).</span><span class="sxs-lookup"><span data-stu-id="36087-113">Audio Data Transport Stream (ADTS).</span></span> <span data-ttu-id="36087-114">Поток содержит \_ последовательность ADTs, определенную MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="36087-114">The stream contains an adts\_sequence, as defined by MPEG-2.</span></span><br/>                       |
| <dl> <span data-ttu-id="36087-115"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="36087-115"><dt>2</dt></span></span> </dl> | <span data-ttu-id="36087-116">Формат обмена звуковых данных (АДИФ).</span><span class="sxs-lookup"><span data-stu-id="36087-116">Audio Data Interchange Format (ADIF).</span></span> <span data-ttu-id="36087-117">Поток содержит \_ последовательность Адиф, определенную MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="36087-117">The stream contains an adif\_sequence, as defined by MPEG-2.</span></span><br/>                     |
| <dl> <span data-ttu-id="36087-118"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="36087-118"><dt>3</dt></span></span> </dl> | <span data-ttu-id="36087-119">Поток содержит потоковый транспорт MPEG-4 с уровнем синхронизации (УРОВНЯМИ гарантии) и уровнем мультиплексирования (ЛАТМ).</span><span class="sxs-lookup"><span data-stu-id="36087-119">The stream contains an MPEG-4 audio transport stream with a synchronization layer (LOAS) and a multiplex layer (LATM).</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="36087-120">Get/Set</span><span class="sxs-lookup"><span data-stu-id="36087-120">Get/set</span></span>

<span data-ttu-id="36087-121">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="36087-121">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="36087-122">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="36087-122">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="36087-123">Применение</span><span class="sxs-lookup"><span data-stu-id="36087-123">Applies To</span></span>

[<span data-ttu-id="36087-124">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="36087-124">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="36087-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36087-125">Remarks</span></span>

<span data-ttu-id="36087-126">\_ \_ \_ Тип полезных данных AAC MF MT \_ не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="36087-126">MF\_MT\_AAC\_PAYLOAD\_TYPE is optional.</span></span> <span data-ttu-id="36087-127">Если этот атрибут не указан, используется значение по умолчанию 0, указывающее, что поток содержит только элементы необработанных \_ \_ блоков данных.</span><span class="sxs-lookup"><span data-stu-id="36087-127">If this attribute is not specified, the default value 0 is used, which specifies the stream contains raw\_data\_block elements only.</span></span>

<span data-ttu-id="36087-128">Применяется только к **мфаудиоформат \_ AAC**.</span><span class="sxs-lookup"><span data-stu-id="36087-128">Applies only to **MFAudioFormat\_AAC**.</span></span>

<span data-ttu-id="36087-129">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="36087-129">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="36087-130">Требования</span><span class="sxs-lookup"><span data-stu-id="36087-130">Requirements</span></span>



| <span data-ttu-id="36087-131">Требование</span><span class="sxs-lookup"><span data-stu-id="36087-131">Requirement</span></span> | <span data-ttu-id="36087-132">Значение</span><span class="sxs-lookup"><span data-stu-id="36087-132">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="36087-133">Header</span><span class="sxs-lookup"><span data-stu-id="36087-133">Header</span></span><br/> | <dl> <span data-ttu-id="36087-134"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="36087-134"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36087-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36087-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36087-136">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="36087-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="36087-137">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="36087-137">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




