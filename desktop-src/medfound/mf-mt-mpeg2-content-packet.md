---
description: Для типа мультимедиа, описывающего транспортный поток MPEG-2, указывает, содержат ли транспортные пакеты заголовки пакетов содержимого.
ms.assetid: 527B965D-4330-4DCB-B6DA-32D6BCDF5515
title: Атрибут MF_MT_MPEG2_CONTENT_PACKET (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acb297081a150ab3aa5b842be9b5792d849e2457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911191"
---
# <a name="mf_mt_mpeg2_content_packet-attribute"></a><span data-ttu-id="1bf71-103">\_ \_ \_ Атрибут пакета содержимого MF MT MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="1bf71-103">MF\_MT\_MPEG2\_CONTENT\_PACKET attribute</span></span>

<span data-ttu-id="1bf71-104">Для типа мультимедиа, описывающего транспортный поток MPEG-2, указывает, содержат ли транспортные пакеты заголовки пакетов содержимого.</span><span class="sxs-lookup"><span data-stu-id="1bf71-104">For a media type that describes an MPEG-2 transport stream (TS), specifies whether the transport packets contain Content Packet headers.</span></span>

## <a name="data-type"></a><span data-ttu-id="1bf71-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1bf71-105">Data type</span></span>

<span data-ttu-id="1bf71-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1bf71-106">**UINT32**</span></span>



| <span data-ttu-id="1bf71-107">Значение</span><span class="sxs-lookup"><span data-stu-id="1bf71-107">Value</span></span>                                                                                                | <span data-ttu-id="1bf71-108">Значение</span><span class="sxs-lookup"><span data-stu-id="1bf71-108">Meaning</span></span>                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="1bf71-109"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="1bf71-109"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="1bf71-110">Заголовки пакетов содержимого не добавляются.</span><span class="sxs-lookup"><span data-stu-id="1bf71-110">No Content Packet headers are added.</span></span><br/>                                                                                                                                                                    |
| <span id="1"></span><dl> <span data-ttu-id="1bf71-111"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="1bf71-111"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="1bf71-112">При 200 – 1000 миллисекундах в начало транспортного пакета добавляется 14-байтовый заголовок пакета содержимого, который определяется ассоциацией радиоотраслей и бизнес-АРИБ.</span><span class="sxs-lookup"><span data-stu-id="1bf71-112">At 200–1000 millisecond intervals, a 14-byte Content Packet header is added to the beginning of the transport packet, as defined by the Association of Radio Industries and Businesses (ARIB) standard.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1bf71-113">Требования</span><span class="sxs-lookup"><span data-stu-id="1bf71-113">Requirements</span></span>



| <span data-ttu-id="1bf71-114">Требование</span><span class="sxs-lookup"><span data-stu-id="1bf71-114">Requirement</span></span> | <span data-ttu-id="1bf71-115">Значение</span><span class="sxs-lookup"><span data-stu-id="1bf71-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1bf71-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1bf71-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1bf71-117">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="1bf71-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="1bf71-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1bf71-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1bf71-119">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="1bf71-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="1bf71-120">Header</span><span class="sxs-lookup"><span data-stu-id="1bf71-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bf71-121"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bf71-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bf71-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1bf71-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bf71-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1bf71-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




