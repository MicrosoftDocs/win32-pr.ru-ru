---
description: Указывает, применено ли видео стабилизации к видеокадру.
ms.assetid: 13F877A3-7600-400F-9071-FE1B83027355
title: Атрибут MFSampleExtension_VideoDSPMode (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 309d4b5b68455e78ba63074b9d8ec5e4cbde4fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719466"
---
# <a name="mfsampleextension_videodspmode-attribute"></a><span data-ttu-id="274ff-103">Мфсампликстенсион \_ видеодспмоде, атрибут</span><span class="sxs-lookup"><span data-stu-id="274ff-103">MFSampleExtension\_VideoDSPMode attribute</span></span>

<span data-ttu-id="274ff-104">Указывает, применено ли видео стабилизации к видеокадру.</span><span class="sxs-lookup"><span data-stu-id="274ff-104">Indicates whether video stabilization was applied to a video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="274ff-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="274ff-105">Data type</span></span>

<span data-ttu-id="274ff-106">**Мфвидеодспмоде** хранится как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="274ff-106">**MFVideoDSPMode** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="274ff-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="274ff-107">Get/set</span></span>

<span data-ttu-id="274ff-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="274ff-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="274ff-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="274ff-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="274ff-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="274ff-110">Applies to</span></span>

[<span data-ttu-id="274ff-111">**имфсампле**</span><span class="sxs-lookup"><span data-stu-id="274ff-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="274ff-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="274ff-112">Remarks</span></span>

<span data-ttu-id="274ff-113">[**Стабилизация видео MFT**](video-stabilization-mft.md) задает этот атрибут в выходных образцах, которые он создает.</span><span class="sxs-lookup"><span data-stu-id="274ff-113">The [**Video Stabilization MFT**](video-stabilization-mft.md) sets this attribute on the output samples that it produces.</span></span> <span data-ttu-id="274ff-114">Значение атрибута является значением перечисления [**мфвидеодспмоде**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) .</span><span class="sxs-lookup"><span data-stu-id="274ff-114">The value of the attribute is an [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) enumeration value.</span></span> <span data-ttu-id="274ff-115">Если значение равно **мфвидеодспмоде \_ стабилизации**, это означает, что MFT применил Image стабилизации к кадру.</span><span class="sxs-lookup"><span data-stu-id="274ff-115">If the value is **MFVideoDSPMode\_Stabilization**, it means that the MFT applied image stabilization to the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="274ff-116">Требования</span><span class="sxs-lookup"><span data-stu-id="274ff-116">Requirements</span></span>



| <span data-ttu-id="274ff-117">Требование</span><span class="sxs-lookup"><span data-stu-id="274ff-117">Requirement</span></span> | <span data-ttu-id="274ff-118">Значение</span><span class="sxs-lookup"><span data-stu-id="274ff-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="274ff-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="274ff-119">Minimum supported client</span></span><br/> | <span data-ttu-id="274ff-120">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="274ff-120">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="274ff-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="274ff-121">Minimum supported server</span></span><br/> | <span data-ttu-id="274ff-122">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="274ff-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="274ff-123">Header</span><span class="sxs-lookup"><span data-stu-id="274ff-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="274ff-124"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="274ff-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="274ff-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="274ff-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="274ff-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="274ff-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="274ff-127">Примеры атрибутов</span><span class="sxs-lookup"><span data-stu-id="274ff-127">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="274ff-128">Примеры носителей</span><span class="sxs-lookup"><span data-stu-id="274ff-128">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="274ff-129">**Стабилизация видео MFT**</span><span class="sxs-lookup"><span data-stu-id="274ff-129">**Video Stabilization MFT**</span></span>](video-stabilization-mft.md)
</dt> </dl>

 

 




