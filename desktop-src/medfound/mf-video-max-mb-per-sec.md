---
description: Указывает на Имфтрансформ максимальную скорость обработки макроблокк в макроблоккс в секунду, которая поддерживается аппаратным кодировщиком.
ms.assetid: 1AA41DE3-C37C-41BA-9549-5F12373DDB3B
title: Атрибут MF_VIDEO_MAX_MB_PER_SEC (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbee009b50daee074241c11750e9d25240cda153
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719390"
---
# <a name="mf_video_max_mb_per_sec-attribute"></a><span data-ttu-id="e98a5-103">\_Атрибут " \_ Макс. МБ видео \_ \_ в \_ секунду"</span><span class="sxs-lookup"><span data-stu-id="e98a5-103">MF\_VIDEO\_MAX\_MB\_PER\_SEC attribute</span></span>

<span data-ttu-id="e98a5-104">Указывает на [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)максимальную скорость обработки макроблокк в макроблоккс в секунду, которая поддерживается аппаратным кодировщиком.</span><span class="sxs-lookup"><span data-stu-id="e98a5-104">Specifies, on [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform), the maximum macroblock processing rate, in macroblocks per second, that is supported by the hardware encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="e98a5-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="e98a5-105">Data type</span></span>

<span data-ttu-id="e98a5-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e98a5-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="e98a5-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e98a5-107">Remarks</span></span>

<span data-ttu-id="e98a5-108">Этот атрибут доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e98a5-108">This is a read-only attribute.</span></span>

<span data-ttu-id="e98a5-109">**Кодировщики H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="e98a5-109">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="e98a5-110">На этот атрибут влияют следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="e98a5-110">This attribute is affected by the following properties:</span></span>

-   <span data-ttu-id="e98a5-111">[MF \_ \_ \_ Уровень видео MT](mf-mt-video-level.md) (который является псевдонимом для [ \_ уровня MF \_ MT \_ MPEG2](mf-mt-mpeg2-level-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="e98a5-111">[MF\_MT\_VIDEO\_LEVEL](mf-mt-video-level.md) (which is an alias of [MF\_MT\_MPEG2\_LEVEL](mf-mt-mpeg2-level-attribute.md))</span></span>
-   [<span data-ttu-id="e98a5-112">КОДЕКАПИ \_ авенккоммонкуалитивсспид</span><span class="sxs-lookup"><span data-stu-id="e98a5-112">CODECAPI\_AVEncCommonQualityVsSpeed</span></span>](../directshow/avenccommonqualityvsspeed-property.md)
-   [<span data-ttu-id="e98a5-113">КОДЕКАПИ \_ авенкмпвдефаултбпиктурекаунт</span><span class="sxs-lookup"><span data-stu-id="e98a5-113">CODECAPI\_AVEncMPVDefaultBPictureCount</span></span>](../directshow/avencmpvdefaultbpicturecount-property.md)

<span data-ttu-id="e98a5-114">Если имеется [атрибут \_ \_ \_ уровня видео MF MT](mf-mt-video-level.md) , кодировщик должен возвращать скорость обработки для максимальной скорости и разрешения, поддерживаемые на указанном уровне.</span><span class="sxs-lookup"><span data-stu-id="e98a5-114">If the [MF\_MT\_VIDEO\_LEVEL](mf-mt-video-level.md) attribute is present, the encoder should return the processing rate for the highest bitrate and resolution supported at the specified level.</span></span> <span data-ttu-id="e98a5-115">Если \_ атрибут уровня видео MF MT отсутствует, \_ \_ он должен использовать уровень по умолчанию 4.</span><span class="sxs-lookup"><span data-stu-id="e98a5-115">If the MF\_MT\_VIDEO\_LEVEL attribute is not present then it should use a default level of 4.</span></span>

<span data-ttu-id="e98a5-116">Если установлено свойство [кодекапи \_ авенккоммонкуалитивсспид](../directshow/avenccommonqualityvsspeed-property.md) икодекапи, кодировщик должен вернуть скорость обработки, соответствующую значению, заданному для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="e98a5-116">If the [CODECAPI\_AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) ICodecAPI property has been set, the encoder should return the processing rate corresponding to the value set for this property.</span></span> <span data-ttu-id="e98a5-117">Если атрибут КОДЕКАПИ \_ авенккоммонкуалитивсспид отсутствует, он должен использовать значение по умолчанию 0, которое должно быть самым быстрым режимом обработки.</span><span class="sxs-lookup"><span data-stu-id="e98a5-117">If the CODECAPI\_AVEncCommonQualityVsSpeed attribute is not present, then it should use a default value of 0 which should be the fastest processing mode.</span></span>

<span data-ttu-id="e98a5-118">Если для свойства [кодекапи \_ авенкмпвдефаултбпиктурекаунт](../directshow/avencmpvdefaultbpicturecount-property.md) икодекапи задано допустимое и поддерживаемое значение, кодировщик должен вернуть скорость обработки, соответствующую значению, заданному для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="e98a5-118">If the [CODECAPI\_AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md) ICodecAPI property has been set to a valid and supported value, the encoder should return the processing rate corresponding the value set for this property.</span></span> <span data-ttu-id="e98a5-119">Если атрибут КОДЕКАПИ \_ авенкмпвдефаултбпиктурекаунт не пресен, t, то он должен использовать значение по умолчанию, равное 0 B кадрам.</span><span class="sxs-lookup"><span data-stu-id="e98a5-119">If the CODECAPI\_AVEncMPVDefaultBPictureCount attribute is not presen,t then it should use a default value of 0 B frames.</span></span>

<span data-ttu-id="e98a5-120">Приложение должно использовать только более низкие 28 бит.</span><span class="sxs-lookup"><span data-stu-id="e98a5-120">Only the lower 28 bits should be used by an application.</span></span> <span data-ttu-id="e98a5-121">Верхняя 4bits зарезервирована для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="e98a5-121">The upper 4bits are reserved for future use.</span></span> <span data-ttu-id="e98a5-122">Приложения должны игнорировать верхние 4 бита, и МФТС должен установить верхние 4 бита в значение 0.</span><span class="sxs-lookup"><span data-stu-id="e98a5-122">Applications should ignore the upper 4 bits and MFTs should set the upper 4 bits to 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="e98a5-123">Требования</span><span class="sxs-lookup"><span data-stu-id="e98a5-123">Requirements</span></span>



| <span data-ttu-id="e98a5-124">Требование</span><span class="sxs-lookup"><span data-stu-id="e98a5-124">Requirement</span></span> | <span data-ttu-id="e98a5-125">Значение</span><span class="sxs-lookup"><span data-stu-id="e98a5-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e98a5-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e98a5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e98a5-127">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="e98a5-127">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="e98a5-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e98a5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e98a5-129">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="e98a5-129">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="e98a5-130">Header</span><span class="sxs-lookup"><span data-stu-id="e98a5-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e98a5-131"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="e98a5-131"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e98a5-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e98a5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e98a5-133">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e98a5-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
