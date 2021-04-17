---
description: Указывает сведения о кадре длинных ссылок (LTR) и возвращается в образце выходных данных.
ms.assetid: 0632D780-C56B-4FDB-8A76-B7A7DE414242
title: Атрибут MFSampleExtension_LongTermReferenceFrameInfo (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3af85ffa5876cdf58a21a6933c46f460c23e7456
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105684794"
---
# <a name="mfsampleextension_longtermreferenceframeinfo-attribute"></a><span data-ttu-id="ea394-103">Мфсампликстенсион \_ лонгтермреференцефрамеинфо, атрибут</span><span class="sxs-lookup"><span data-stu-id="ea394-103">MFSampleExtension\_LongTermReferenceFrameInfo attribute</span></span>

<span data-ttu-id="ea394-104">Указывает сведения о кадре длинных ссылок (LTR) и возвращается в образце выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ea394-104">Specifies Long Term Reference (LTR) frame info and is returned on the output sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="ea394-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ea394-105">Data type</span></span>

<span data-ttu-id="ea394-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ea394-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="ea394-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ea394-107">Remarks</span></span>

<span data-ttu-id="ea394-108">**Кодировщики H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="ea394-108">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="ea394-109">Кодировщики должны возвращать этот атрибут в примере Output, когда приложение управляет кадрами LTR, которые задаются параметром [кодекапи \_ авенквидеолтрбуфферконтрол](codecapi-avencvideoltrbuffercontrol.md).</span><span class="sxs-lookup"><span data-stu-id="ea394-109">Encoders shall return this attribute on the output sample when the application controls LTR frames, which is specified by [CODECAPI\_AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).</span></span>

<span data-ttu-id="ea394-110">Мфсампликстенсион \_ лонгтермреференцефрамеинфо возвращает до двух полей.</span><span class="sxs-lookup"><span data-stu-id="ea394-110">MFSampleExtension\_LongTermReferenceFrameInfo returns up to two fields.</span></span>

<span data-ttu-id="ea394-111">Первое поле, бит \[ 0.. 15 \] , *лонгтермфрамеидкс* , связанное с выходным кадром, если он ПОМЕЧЕН как рамка слева.</span><span class="sxs-lookup"><span data-stu-id="ea394-111">The first field, bits\[0..15\], is *LongTermFrameIdx* associated with the output frame if it is marked as a LTR frame.</span></span> <span data-ttu-id="ea394-112">Первое значение — 0xFFFF, если выходной кадр является коротким ссылочным кадром или кадром, не являющимся ссылкой.</span><span class="sxs-lookup"><span data-stu-id="ea394-112">The first value is 0xffff, if this output frame is a short term reference frame or a non-reference frame.</span></span>

<span data-ttu-id="ea394-113">Второе поле (бит \[ 16.31 \] ) — это битовая карта, состоящая из *макснумлтрфрамес* большого числа битов, которые УКАЗЫВАЮТ, какие кадры LTR использовались для кодирования этого выходного кадра, начиная с бита 16.</span><span class="sxs-lookup"><span data-stu-id="ea394-113">The second field, bits\[16..31\], is a bitmap consisting of *MaxNumLTRFrames* many bits that indicate which LTR frame(s) were used for encoding this output frame, starting from bit 16.</span></span> <span data-ttu-id="ea394-114">Остальные биты должны быть установлены в значение 0.</span><span class="sxs-lookup"><span data-stu-id="ea394-114">The rest of bits shall be set to 0.</span></span> <span data-ttu-id="ea394-115">Второе значение равно 0, если выходной фрейм не кодируется с помощью каких-либо фреймов LTR.</span><span class="sxs-lookup"><span data-stu-id="ea394-115">The second value is 0 if this output frame is not encoded using any LTR frames.</span></span> <span data-ttu-id="ea394-116">*Макснумлтрфрамес* — максимальное число кадров LTR, заданное через [кодекапи \_ авенквидеолтрбуфферконтрол](codecapi-avencvideoltrbuffercontrol.md).</span><span class="sxs-lookup"><span data-stu-id="ea394-116">*MaxNumLTRFrames* is the maximum number of LTR frames set through [CODECAPI\_AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ea394-117">Требования</span><span class="sxs-lookup"><span data-stu-id="ea394-117">Requirements</span></span>



| <span data-ttu-id="ea394-118">Требование</span><span class="sxs-lookup"><span data-stu-id="ea394-118">Requirement</span></span> | <span data-ttu-id="ea394-119">Значение</span><span class="sxs-lookup"><span data-stu-id="ea394-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ea394-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ea394-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ea394-121">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="ea394-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="ea394-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ea394-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ea394-123">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="ea394-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="ea394-124">Header</span><span class="sxs-lookup"><span data-stu-id="ea394-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea394-125"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea394-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea394-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ea394-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea394-127">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ea394-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




