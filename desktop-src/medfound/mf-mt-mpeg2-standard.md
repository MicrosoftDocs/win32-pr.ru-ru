---
description: Для типа мультимедиа, который описывает поток программы MPEG-2 (PS) или транспортного потока (TS), указывает стандарт, используемый для мультиплексирования потока.
ms.assetid: 3D4C1A81-A9BA-427F-93DB-F522A0616EAB
title: Атрибут MF_MT_MPEG2_STANDARD (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0650a68975f449ea938b41872005e11d79922393
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647298"
---
# <a name="mf_mt_mpeg2_standard-attribute"></a><span data-ttu-id="a38f4-103">\_ \_ Стандартный атрибут MF MT MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="a38f4-103">MF\_MT\_MPEG2\_STANDARD attribute</span></span>

<span data-ttu-id="a38f4-104">Для типа мультимедиа, который описывает поток программы MPEG-2 (PS) или транспортного потока (TS), указывает стандарт, используемый для мультиплексирования потока.</span><span class="sxs-lookup"><span data-stu-id="a38f4-104">For a media type that describes an MPEG-2 program stream (PS) or transport stream (TS), specifies the standard that is used to multiplex the stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="a38f4-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a38f4-105">Data type</span></span>

<span data-ttu-id="a38f4-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a38f4-106">**UINT32**</span></span>



| <span data-ttu-id="a38f4-107">Значение</span><span class="sxs-lookup"><span data-stu-id="a38f4-107">Value</span></span>                                                                                                | <span data-ttu-id="a38f4-108">Значение</span><span class="sxs-lookup"><span data-stu-id="a38f4-108">Meaning</span></span>                                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="a38f4-109"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="a38f4-109"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="a38f4-110">Стандартные MPEG-2 PS или TS.</span><span class="sxs-lookup"><span data-stu-id="a38f4-110">Standard MPEG-2 PS or TS.</span></span><br/>                                       |
| <span id="1"></span><dl> <span data-ttu-id="a38f4-111"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="a38f4-111"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="a38f4-112">Стандарт Advanced телевидение Systems Комитет (ATSC).</span><span class="sxs-lookup"><span data-stu-id="a38f4-112">Advanced Television Systems Committee (ATSC) standard.</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="a38f4-113"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="a38f4-113"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="a38f4-114">Стандарт Digital Video широковещания (DVB).</span><span class="sxs-lookup"><span data-stu-id="a38f4-114">Digital Video Broadcasting (DVB) standard.</span></span><br/>                      |
| <span id="3"></span><dl> <span data-ttu-id="a38f4-115"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="a38f4-115"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="a38f4-116">Ассоциация коммерческих отраслей (АРИБ) Standard.</span><span class="sxs-lookup"><span data-stu-id="a38f4-116">Association of Radio Industries and Businesses (ARIB) standard.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a38f4-117">Требования</span><span class="sxs-lookup"><span data-stu-id="a38f4-117">Requirements</span></span>



| <span data-ttu-id="a38f4-118">Требование</span><span class="sxs-lookup"><span data-stu-id="a38f4-118">Requirement</span></span> | <span data-ttu-id="a38f4-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a38f4-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a38f4-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a38f4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a38f4-121">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="a38f4-121">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="a38f4-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a38f4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a38f4-123">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="a38f4-123">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="a38f4-124">Header</span><span class="sxs-lookup"><span data-stu-id="a38f4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a38f4-125"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="a38f4-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a38f4-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a38f4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a38f4-127">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a38f4-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




