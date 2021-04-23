---
description: В следующей таблице приведены коды ошибок, относящиеся к объектам мультимедиа Microsoft DirectX (дмос). Эти коды ошибок определены в файле заголовка Медиаерр. h.
ms.assetid: 1ded5656-084d-4315-a414-aebf4a1820dc
title: Коды ошибок DMO (Медиаерр. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d76c8cd5e7001751cd2cf9eb7da4d88b2dc100bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652215"
---
# <a name="dmo-error-codes"></a><span data-ttu-id="880b8-104">Коды ошибок DMO</span><span class="sxs-lookup"><span data-stu-id="880b8-104">DMO Error Codes</span></span>

<span data-ttu-id="880b8-105">В следующей таблице приведены коды ошибок, относящиеся к объектам мультимедиа Microsoft DirectX (дмос).</span><span class="sxs-lookup"><span data-stu-id="880b8-105">The following table contains error codes that are specific to Microsoft DirectX Media Objects (DMOs).</span></span> <span data-ttu-id="880b8-106">Эти коды ошибок определены в файле заголовка Медиаерр. h.</span><span class="sxs-lookup"><span data-stu-id="880b8-106">These error codes are defined in the header file Mediaerr.h.</span></span>



| <span data-ttu-id="880b8-107">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="880b8-107">Constant/value</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="880b8-108">Описание</span><span class="sxs-lookup"><span data-stu-id="880b8-108">Description</span></span>                                                                                                                                                         |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMO_E_INVALIDSTREAMINDEX"></span><span id="dmo_e_invalidstreamindex"></span><dl> <span data-ttu-id="880b8-109"><dt>**DMO \_ E \_ инвалидстреаминдекс**</dt> <dt>0x80040201</dt></span><span class="sxs-lookup"><span data-stu-id="880b8-109"><dt>**DMO\_E\_INVALIDSTREAMINDEX**</dt> <dt>0x80040201</dt></span></span> </dl> | <span data-ttu-id="880b8-110">Недопустимый индекс потока.</span><span class="sxs-lookup"><span data-stu-id="880b8-110">Invalid stream index.</span></span><br/>                                                                                                                                    |
| <span id="DMO_E_INVALIDTYPE"></span><span id="dmo_e_invalidtype"></span><dl> <span data-ttu-id="880b8-111"><dt>**DMO \_ E \_ инвалидтипе**</dt> <dt>0x80040202</dt></span><span class="sxs-lookup"><span data-stu-id="880b8-111"><dt>**DMO\_E\_INVALIDTYPE**</dt> <dt>0x80040202</dt></span></span> </dl>                      | <span data-ttu-id="880b8-112">Недопустимый тип носителя.</span><span class="sxs-lookup"><span data-stu-id="880b8-112">Invalid media type.</span></span><br/>                                                                                                                                      |
| <span id="DMO_E_TYPE_NOT_SET"></span><span id="dmo_e_type_not_set"></span><dl> <span data-ttu-id="880b8-113"><dt>**DMO \_ \_Тип E \_ не \_ задан**</dt> <dt>0x80040203</dt></span><span class="sxs-lookup"><span data-stu-id="880b8-113"><dt>**DMO\_E\_TYPE\_NOT\_SET**</dt> <dt>0x80040203</dt></span></span> </dl>                 | <span data-ttu-id="880b8-114">Тип носителя не задан.</span><span class="sxs-lookup"><span data-stu-id="880b8-114">Media type was not set.</span></span> <span data-ttu-id="880b8-115">Перед выполнением этой операции для одного или нескольких потоков требуется тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="880b8-115">One or more streams require a media type before this operation can be performed.</span></span><br/>                                                 |
| <span id="DMO_E_NOTACCEPTING"></span><span id="dmo_e_notaccepting"></span><dl> <span data-ttu-id="880b8-116"><dt>**DMO \_ E \_ нотакцептинг**</dt> <dt>0x80040204</dt></span><span class="sxs-lookup"><span data-stu-id="880b8-116"><dt>**DMO\_E\_NOTACCEPTING**</dt> <dt>0x80040204</dt></span></span> </dl>                   | <span data-ttu-id="880b8-117">Данные не могут быть приняты в этом потоке.</span><span class="sxs-lookup"><span data-stu-id="880b8-117">Data cannot be accepted on this stream.</span></span> <span data-ttu-id="880b8-118">Может потребоваться обработка дополнительных выходных данных. см. раздел [**имедиаобжект::P роцессинпут**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput).</span><span class="sxs-lookup"><span data-stu-id="880b8-118">You might need to process more output data; see [**IMediaObject::ProcessInput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput).</span></span><br/> |
| <span id="DMO_E_TYPE_NOT_ACCEPTED"></span><span id="dmo_e_type_not_accepted"></span><dl> <span data-ttu-id="880b8-119"><dt>**DMO \_ \_Тип E \_ не \_ принят**</dt> <dt>0x80040205</dt></span><span class="sxs-lookup"><span data-stu-id="880b8-119"><dt>**DMO\_E\_TYPE\_NOT\_ACCEPTED**</dt> <dt>0x80040205</dt></span></span> </dl>  | <span data-ttu-id="880b8-120">Тип носителя не принят.</span><span class="sxs-lookup"><span data-stu-id="880b8-120">Media type was not accepted.</span></span><br/>                                                                                                                             |
| <span id="DMO_E_NO_MORE_ITEMS"></span><span id="dmo_e_no_more_items"></span><dl> <span data-ttu-id="880b8-121"><dt>**DMO \_ Е 0x80040206 больше \_ \_ \_ элементов**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="880b8-121"><dt>**DMO\_E\_NO\_MORE\_ITEMS**</dt> <dt>0x80040206</dt></span></span> </dl>              | <span data-ttu-id="880b8-122">Индекс типа носителя выходит за пределы допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="880b8-122">Media-type index is out of range.</span></span><br/>                                                                                                                        |



## <a name="requirements"></a><span data-ttu-id="880b8-123">Требования</span><span class="sxs-lookup"><span data-stu-id="880b8-123">Requirements</span></span>



| <span data-ttu-id="880b8-124">Требование</span><span class="sxs-lookup"><span data-stu-id="880b8-124">Requirement</span></span> | <span data-ttu-id="880b8-125">Значение</span><span class="sxs-lookup"><span data-stu-id="880b8-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="880b8-126">Header</span><span class="sxs-lookup"><span data-stu-id="880b8-126">Header</span></span><br/> | <dl> <span data-ttu-id="880b8-127"><dt>Медиаерр. h</dt></span><span class="sxs-lookup"><span data-stu-id="880b8-127"><dt>Mediaerr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="880b8-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="880b8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="880b8-129">Константы DMO</span><span class="sxs-lookup"><span data-stu-id="880b8-129">DMO Constants</span></span>](dmo-constants.md)
</dt> </dl>

 

 




