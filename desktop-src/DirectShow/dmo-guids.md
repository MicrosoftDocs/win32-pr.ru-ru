---
description: В следующей таблице перечислены глобальные уникальные идентификаторы (GUID), определенные для категорий объектов Microsoft DirectX Media (DMO). Эти идентификаторы GUID определяются в файле заголовка Дморег. h и экспортируются библиотекой Дмогуидс. lib.
ms.assetid: d67debd0-8ecb-41ab-bc6c-b27cba97c65a
title: GUID DMO (Дморег. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c10d5bd917d6368d398362e76ffa9ea8255933ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651863"
---
# <a name="dmo-guids"></a><span data-ttu-id="36add-104">GUID DMO</span><span class="sxs-lookup"><span data-stu-id="36add-104">DMO GUIDs</span></span>

<span data-ttu-id="36add-105">В следующей таблице перечислены глобальные уникальные идентификаторы (GUID), определенные для категорий объектов Microsoft DirectX Media (DMO).</span><span class="sxs-lookup"><span data-stu-id="36add-105">The following table lists the globally unique identifiers (GUIDs) defined for Microsoft DirectX Media Object (DMO) categories.</span></span> <span data-ttu-id="36add-106">Эти идентификаторы GUID определяются в файле заголовка Дморег. h и экспортируются библиотекой Дмогуидс. lib.</span><span class="sxs-lookup"><span data-stu-id="36add-106">These GUIDs are defined in the header file Dmoreg.h and exported by the Dmoguids.lib library.</span></span>

<span data-ttu-id="36add-107">Чтобы перечислить дмос, зарегистрированные в категории, передайте соответствующий идентификатор GUID функции [**дмоенум**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) .</span><span class="sxs-lookup"><span data-stu-id="36add-107">To enumerate the DMOs registered in a category, pass the corresponding GUID to the [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) function.</span></span>



| <span data-ttu-id="36add-108">Идентификатор GUID</span><span class="sxs-lookup"><span data-stu-id="36add-108">GUID</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="36add-109">Описание</span><span class="sxs-lookup"><span data-stu-id="36add-109">Description</span></span>                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------|
| <span id="DMOCATEGORY_AUDIO_DECODER"></span><span id="dmocategory_audio_decoder"></span><dl> <span data-ttu-id="36add-110"><dt>**\_декодер дмокатегори Audio \_**</dt></span><span class="sxs-lookup"><span data-stu-id="36add-110"><dt>**DMOCATEGORY\_AUDIO\_DECODER**</dt></span></span> </dl>                       | <span data-ttu-id="36add-111">Декодер звука</span><span class="sxs-lookup"><span data-stu-id="36add-111">Audio decoder</span></span><br/>        |
| <span id="DMOCATEGORY_AUDIO_EFFECT"></span><span id="dmocategory_audio_effect"></span><dl> <span data-ttu-id="36add-112"><dt>**ДМОКАТЕГОРИный \_ звуковой \_ результат**</dt></span><span class="sxs-lookup"><span data-stu-id="36add-112"><dt>**DMOCATEGORY\_AUDIO\_EFFECT**</dt></span></span> </dl>                          | <span data-ttu-id="36add-113">Звуковой результат</span><span class="sxs-lookup"><span data-stu-id="36add-113">Audio effect</span></span><br/>         |
| <span id="DMOCATEGORY_AUDIO_ENCODER"></span><span id="dmocategory_audio_encoder"></span><dl> <span data-ttu-id="36add-114"><dt>**\_КОДИРОВЩИК дмокатегори Audio \_**</dt></span><span class="sxs-lookup"><span data-stu-id="36add-114"><dt>**DMOCATEGORY\_AUDIO\_ENCODER**</dt></span></span> </dl>                       | <span data-ttu-id="36add-115">Кодировщик звука</span><span class="sxs-lookup"><span data-stu-id="36add-115">Audio encoder</span></span><br/>        |
| <span id="DMOCATEGORY_VIDEO_DECODER"></span><span id="dmocategory_video_decoder"></span><dl> <span data-ttu-id="36add-116"><dt>**\_декодер видео \_ дмокатегори**</dt></span><span class="sxs-lookup"><span data-stu-id="36add-116"><dt>**DMOCATEGORY\_VIDEO\_DECODER**</dt></span></span> </dl>                       | <span data-ttu-id="36add-117">Видеодекодер</span><span class="sxs-lookup"><span data-stu-id="36add-117">Video decoder</span></span><br/>        |
| <span id="DMOCATEGORY_VIDEO_EFFECT"></span><span id="dmocategory_video_effect"></span><dl> <span data-ttu-id="36add-118"><dt>**ДМОКАТЕГОРИ \_ видео \_**</dt></span><span class="sxs-lookup"><span data-stu-id="36add-118"><dt>**DMOCATEGORY\_VIDEO\_EFFECT**</dt></span></span> </dl>                          | <span data-ttu-id="36add-119">Видеодействие</span><span class="sxs-lookup"><span data-stu-id="36add-119">Video effect</span></span><br/>         |
| <span id="DMOCATEGORY_VIDEO_ENCODER"></span><span id="dmocategory_video_encoder"></span><dl> <span data-ttu-id="36add-120"><dt>**\_кодировщик видео \_ дмокатегори**</dt></span><span class="sxs-lookup"><span data-stu-id="36add-120"><dt>**DMOCATEGORY\_VIDEO\_ENCODER**</dt></span></span> </dl>                       | <span data-ttu-id="36add-121">Кодировщик видео</span><span class="sxs-lookup"><span data-stu-id="36add-121">Video encoder</span></span><br/>        |
| <span id="DMOCATEGORY_AUDIO_CAPTURE_EFFECT"></span><span id="dmocategory_audio_capture_effect"></span><dl> <span data-ttu-id="36add-122"><dt>**ДМОКАТЕГОРИ \_ аудиозаписи \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="36add-122"><dt>**DMOCATEGORY\_AUDIO\_CAPTURE\_EFFECT**</dt></span></span> </dl> | <span data-ttu-id="36add-123">Результат записи звука</span><span class="sxs-lookup"><span data-stu-id="36add-123">Audio capture effect</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="36add-124">Требования</span><span class="sxs-lookup"><span data-stu-id="36add-124">Requirements</span></span>



| <span data-ttu-id="36add-125">Требование</span><span class="sxs-lookup"><span data-stu-id="36add-125">Requirement</span></span> | <span data-ttu-id="36add-126">Значение</span><span class="sxs-lookup"><span data-stu-id="36add-126">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="36add-127">Header</span><span class="sxs-lookup"><span data-stu-id="36add-127">Header</span></span><br/> | <dl> <span data-ttu-id="36add-128"><dt>Дморег. h</dt></span><span class="sxs-lookup"><span data-stu-id="36add-128"><dt>Dmoreg.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36add-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36add-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36add-130">Константы DMO</span><span class="sxs-lookup"><span data-stu-id="36add-130">DMO Constants</span></span>](dmo-constants.md)
</dt> </dl>

 

 




