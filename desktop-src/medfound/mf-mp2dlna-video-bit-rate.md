---
description: Указывает максимальную скорость видеопотока для приемника мультимедиа Digital живая Network Alliance (DLNA).
ms.assetid: 5805f930-6cbd-4089-a052-522b4d152cc1
title: Атрибут MF_MP2DLNA_VIDEO_BIT_RATE (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 503625e6879b202f3fcd1f38bce38ebf48677d77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263627"
---
# <a name="mf_mp2dlna_video_bit_rate-attribute"></a><span data-ttu-id="5a32a-103">\_ \_ \_ Атрибут частоты разрядов видео MF MP2DLNA \_</span><span class="sxs-lookup"><span data-stu-id="5a32a-103">MF\_MP2DLNA\_VIDEO\_BIT\_RATE attribute</span></span>

<span data-ttu-id="5a32a-104">Указывает максимальную скорость видеопотока для приемника мультимедиа Digital живая Network Alliance (DLNA).</span><span class="sxs-lookup"><span data-stu-id="5a32a-104">Specifies the maximum video bit rate for the Digital Living Network Alliance (DLNA) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="5a32a-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5a32a-105">Data type</span></span>

<span data-ttu-id="5a32a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5a32a-106">**UINT32**</span></span>

<span data-ttu-id="5a32a-107">Значение является целевой максимальной скоростью потока для закодированного видеопотока в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="5a32a-107">The value is the target maximum bit rate for the encoded video stream, in bits per second.</span></span> <span data-ttu-id="5a32a-108">Максимальное значение — 9800000 (9,8 Мбит/с), которое также является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5a32a-108">The maximum value is 9800000 (9.8 Mbps), which is also the default value.</span></span>

## <a name="getset"></a><span data-ttu-id="5a32a-109">Get/Set</span><span class="sxs-lookup"><span data-stu-id="5a32a-109">Get/set</span></span>

<span data-ttu-id="5a32a-110">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="5a32a-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="5a32a-111">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="5a32a-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="5a32a-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5a32a-112">Remarks</span></span>

<span data-ttu-id="5a32a-113">Чтобы задать этот атрибут для приемника мультимедиа DLNA, запросите приемник мультимедиа для интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="5a32a-113">To set this attribute on the DLNA media sink, query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="5a32a-114">Задайте атрибут перед началом потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="5a32a-114">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a32a-115">Требования</span><span class="sxs-lookup"><span data-stu-id="5a32a-115">Requirements</span></span>



| <span data-ttu-id="5a32a-116">Требование</span><span class="sxs-lookup"><span data-stu-id="5a32a-116">Requirement</span></span> | <span data-ttu-id="5a32a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="5a32a-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a32a-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5a32a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5a32a-119">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5a32a-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5a32a-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5a32a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5a32a-121">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5a32a-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5a32a-122">Header</span><span class="sxs-lookup"><span data-stu-id="5a32a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a32a-123"><dt>Mfmp2dlna. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a32a-123"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a32a-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a32a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a32a-125">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5a32a-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




