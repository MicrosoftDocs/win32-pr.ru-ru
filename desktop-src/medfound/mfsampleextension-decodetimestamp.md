---
description: Содержит отметку времени расшифровки (DTS) для образца.
ms.assetid: 4E0B8266-FF48-49A1-AB7B-A47C4F96AECD
title: Атрибут MFSampleExtension_DecodeTimestamp (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9676b295eb16e7cb2bb607ef4a5074d24b276d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692590"
---
# <a name="mfsampleextension_decodetimestamp-attribute"></a><span data-ttu-id="06de4-103">Мфсампликстенсион \_ декодетиместамп, атрибут</span><span class="sxs-lookup"><span data-stu-id="06de4-103">MFSampleExtension\_DecodeTimestamp attribute</span></span>

<span data-ttu-id="06de4-104">Содержит отметку времени расшифровки (DTS) для образца.</span><span class="sxs-lookup"><span data-stu-id="06de4-104">Contains the decode time stamp (DTS) for the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="06de4-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="06de4-105">Data type</span></span>

<span data-ttu-id="06de4-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="06de4-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="06de4-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="06de4-107">Remarks</span></span>

<span data-ttu-id="06de4-108">Значение атрибута — это DTS в 100-наносекундных единицах.</span><span class="sxs-lookup"><span data-stu-id="06de4-108">The value of the attribute is the DTS in 100-nanosecond units.</span></span> <span data-ttu-id="06de4-109">DTS определяется в некоторых стандартах кодирования, включая MPEG.</span><span class="sxs-lookup"><span data-stu-id="06de4-109">The DTS is defined in some encoding standards, including MPEG.</span></span> <span data-ttu-id="06de4-110">DTS определяет, когда закодированный рисунок должен быть декодирован.</span><span class="sxs-lookup"><span data-stu-id="06de4-110">The DTS specifies when the encoded picture should be decoded.</span></span> <span data-ttu-id="06de4-111">Если закодированное видео содержит кадры B, то службы DTS могут отличаться от времени презентации, так как в битовый поток рисунки в формате B отображаются в некотором порядке.</span><span class="sxs-lookup"><span data-stu-id="06de4-111">If the encoded video contains B frames, the DTS can differ from the presentation time, because B pictures appear out of temporal order in the bitstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="06de4-112">Требования</span><span class="sxs-lookup"><span data-stu-id="06de4-112">Requirements</span></span>



| <span data-ttu-id="06de4-113">Требование</span><span class="sxs-lookup"><span data-stu-id="06de4-113">Requirement</span></span> | <span data-ttu-id="06de4-114">Значение</span><span class="sxs-lookup"><span data-stu-id="06de4-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="06de4-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="06de4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="06de4-116">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="06de4-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="06de4-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="06de4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="06de4-118">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="06de4-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="06de4-119">Header</span><span class="sxs-lookup"><span data-stu-id="06de4-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="06de4-120"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="06de4-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06de4-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="06de4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06de4-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="06de4-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="06de4-123">Примеры атрибутов</span><span class="sxs-lookup"><span data-stu-id="06de4-123">Sample Attributes</span></span>](sample-attributes.md)
</dt> </dl>

 

 




