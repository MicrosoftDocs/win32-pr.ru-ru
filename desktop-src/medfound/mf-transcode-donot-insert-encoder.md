---
description: Указывает, должен ли кодировщик быть включен в топологию перекодировки.
ms.assetid: 73f23aed-d1b9-4821-b1ca-0a07f02b6913
title: Атрибут MF_TRANSCODE_DONOT_INSERT_ENCODER (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92d3f8fc5dabfd3e4c55c6242ba9b8f52b6f5c2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692540"
---
# <a name="mf_transcode_donot_insert_encoder-attribute"></a><span data-ttu-id="454e1-103">MF \_ \_ не разграничения \_ Вставить \_ атрибут кодировщика</span><span class="sxs-lookup"><span data-stu-id="454e1-103">MF\_TRANSCODE\_DONOT\_INSERT\_ENCODER attribute</span></span>

<span data-ttu-id="454e1-104">Указывает, должен ли кодировщик быть включен в топологию перекодировки.</span><span class="sxs-lookup"><span data-stu-id="454e1-104">Specifies whether an encoder must be included in the transcode topology.</span></span>

<span data-ttu-id="454e1-105">Функция [**мфкреатетранскодетопологи**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) проверяет этот атрибут во время создания топологии.</span><span class="sxs-lookup"><span data-stu-id="454e1-105">The [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) function checks this attribute during topology building.</span></span> <span data-ttu-id="454e1-106">Если этот атрибут не задан, кодировщик вставляется в топологию перекодировки.</span><span class="sxs-lookup"><span data-stu-id="454e1-106">If this attribute is not set, an encoder is inserted in the transcode topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="454e1-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="454e1-107">Data type</span></span>

<span data-ttu-id="454e1-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="454e1-108">**UINT32**</span></span>



| <span data-ttu-id="454e1-109">Значение</span><span class="sxs-lookup"><span data-stu-id="454e1-109">Value</span></span>                                                                        | <span data-ttu-id="454e1-110">Значение</span><span class="sxs-lookup"><span data-stu-id="454e1-110">Meaning</span></span>                                                                                                           |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="454e1-111"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="454e1-111"><dt>0</dt></span></span> </dl> | <span data-ttu-id="454e1-112">Кодировщик вставляется в топологию перекодировки.</span><span class="sxs-lookup"><span data-stu-id="454e1-112">An encoder is inserted in the transcode topology.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="454e1-113"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="454e1-113"><dt>1</dt></span></span> </dl> | <span data-ttu-id="454e1-114">Кодировщик не включен в топологию перекодировки.</span><span class="sxs-lookup"><span data-stu-id="454e1-114">An encoder is not included in the transcode topology.</span></span> <span data-ttu-id="454e1-115">Исходный узел подключен к выходному узлу.</span><span class="sxs-lookup"><span data-stu-id="454e1-115">The source node is connected to the output node.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="454e1-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="454e1-116">Remarks</span></span>

<span data-ttu-id="454e1-117">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="454e1-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="454e1-118">Требования</span><span class="sxs-lookup"><span data-stu-id="454e1-118">Requirements</span></span>



| <span data-ttu-id="454e1-119">Требование</span><span class="sxs-lookup"><span data-stu-id="454e1-119">Requirement</span></span> | <span data-ttu-id="454e1-120">Значение</span><span class="sxs-lookup"><span data-stu-id="454e1-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="454e1-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="454e1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="454e1-122">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="454e1-122">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="454e1-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="454e1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="454e1-124">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="454e1-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="454e1-125">Header</span><span class="sxs-lookup"><span data-stu-id="454e1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="454e1-126"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="454e1-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="454e1-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="454e1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="454e1-128">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="454e1-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="454e1-129">Атрибуты Media Foundation</span><span class="sxs-lookup"><span data-stu-id="454e1-129">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




