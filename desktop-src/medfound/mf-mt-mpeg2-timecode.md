---
description: Для типа мультимедиа, описывающего транспортный поток MPEG-2, указывает, что транспортные пакеты содержат 4-байтовый код времени.
ms.assetid: B172E7A8-5757-49B7-A784-FAFC7E904A4C
title: Атрибут MF_MT_MPEG2_TIMECODE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bc9db5d7b3c6e94f7845bec2bd98c569d1b1f9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265362"
---
# <a name="mf_mt_mpeg2_timecode-attribute"></a><span data-ttu-id="0636f-103">Атрибут времени с кодом MF \_ MT \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="0636f-103">MF\_MT\_MPEG2\_TIMECODE attribute</span></span>

<span data-ttu-id="0636f-104">Для типа мультимедиа, описывающего транспортный поток MPEG-2, указывает, что транспортные пакеты содержат 4-байтовый код времени.</span><span class="sxs-lookup"><span data-stu-id="0636f-104">For a media type that describes an MPEG-2 transport stream (TS), specifies the transport packets contain a 4-byte time code.</span></span>

## <a name="data-type"></a><span data-ttu-id="0636f-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0636f-105">Data type</span></span>

<span data-ttu-id="0636f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0636f-106">**UINT32**</span></span>



| <span data-ttu-id="0636f-107">Значение</span><span class="sxs-lookup"><span data-stu-id="0636f-107">Value</span></span>                                                                                                | <span data-ttu-id="0636f-108">Значение</span><span class="sxs-lookup"><span data-stu-id="0636f-108">Meaning</span></span>                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="0636f-109"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="0636f-109"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="0636f-110">Код времени не добавляется.</span><span class="sxs-lookup"><span data-stu-id="0636f-110">No time code is added.</span></span><br/>                                                                                                              |
| <span id="1"></span><dl> <span data-ttu-id="0636f-111"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="0636f-111"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="0636f-112">В начале каждого транспортного пакета добавляется 4-байтовый код времени.</span><span class="sxs-lookup"><span data-stu-id="0636f-112">A 4-byte time code is added at the start of each transport packet.</span></span> <span data-ttu-id="0636f-113">Этот код времени необходим для некоторых стандартов цифрового телевидения.</span><span class="sxs-lookup"><span data-stu-id="0636f-113">This time code is required by some digital television standards.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0636f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="0636f-114">Requirements</span></span>



| <span data-ttu-id="0636f-115">Требование</span><span class="sxs-lookup"><span data-stu-id="0636f-115">Requirement</span></span> | <span data-ttu-id="0636f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="0636f-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0636f-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0636f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0636f-118">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="0636f-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="0636f-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0636f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0636f-120">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="0636f-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="0636f-121">Header</span><span class="sxs-lookup"><span data-stu-id="0636f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0636f-122"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="0636f-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0636f-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0636f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0636f-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0636f-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




