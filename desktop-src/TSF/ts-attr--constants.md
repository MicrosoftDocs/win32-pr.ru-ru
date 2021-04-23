---
title: Константы TS_ATTR_ (Текстстор. h)
description: '\_ \_ Для получения и изменения значений атрибутов документа используются константы TS attr \. Эти константы формируют возможные значения битовых флагов в методах ITextStoreACP и Итекстстореанчор.'
ms.assetid: e99a44ba-c41a-4dd7-9475-dd37159081fd
topic_type:
- apiref
api_name:
- TS_ATTR_FIND_BACKWARDS
- TS_ATTR_FIND_WANT_OFFSET
- TS_ATTR_FIND_UPDATESTART
- TS_ATTR_FIND_WANT_VALUE
- TS_ATTR_FIND_WANT_END
- TS_ATTR_FIND_HIDDEN
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa26b8a725475a3d88b07cce1dccd0ac7fa1a98e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491889"
---
# <a name="ts_attr_-constants"></a><span data-ttu-id="5569a-104">\_ \_ \* КОНСТАНТы attr TS</span><span class="sxs-lookup"><span data-stu-id="5569a-104">TS\_ATTR\_\* Constants</span></span>

<span data-ttu-id="5569a-105">\_ \_ \* Константы TS attr используются для получения и изменения значений атрибутов документа.</span><span class="sxs-lookup"><span data-stu-id="5569a-105">The TS\_ATTR\_\* constants are used to obtain and change the values of document attributes.</span></span> <span data-ttu-id="5569a-106">Эти константы формируют возможные значения битовых флагов в методах [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) и [итекстстореанчор](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) .</span><span class="sxs-lookup"><span data-stu-id="5569a-106">These constants form possible values of bitfield flags in [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) and [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) methods.</span></span>



| <span data-ttu-id="5569a-107">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="5569a-107">Constant/value</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="5569a-108">Описание</span><span class="sxs-lookup"><span data-stu-id="5569a-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_ATTR_FIND_BACKWARDS"></span><span id="ts_attr_find_backwards"></span><dl> <span data-ttu-id="5569a-109"><dt>**TS \_ \_Найти в \_ обратном направлении**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="5569a-109"><dt>**TS\_ATTR\_FIND\_BACKWARDS**</dt> <dt>( 0x1 )</dt></span></span> </dl>        | <span data-ttu-id="5569a-110">Поиск в обратном направлении с начального символа или позиции привязки для позиции, в которой переход выполняется в значении атрибута документа.</span><span class="sxs-lookup"><span data-stu-id="5569a-110">Search backward from the start character or anchor position for the position where a transition occurs in a document attribute value.</span></span> <span data-ttu-id="5569a-111">Значение по умолчанию — поиск вперед.</span><span class="sxs-lookup"><span data-stu-id="5569a-111">The default is search forward.</span></span><br/>                                                                                                                                                                                    |
| <span id="TS_ATTR_FIND_WANT_OFFSET"></span><span id="ts_attr_find_want_offset"></span><dl> <span data-ttu-id="5569a-112"><dt>**TS \_ ATTR \_ Поиск \_ желаемого \_ смещения**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="5569a-112"><dt>**TS\_ATTR\_FIND\_WANT\_OFFSET**</dt> <dt>( 0x2 )</dt></span></span> </dl> | <span data-ttu-id="5569a-113">Возвращает количество символов между начальным символом или позицией привязки (**акпстарт** в [ITextStoreACP:: финднекстаттртранситион](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition) или **Пастарт** в [итекстстореанчор:: финднекстаттртранситион](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) ) и позиции, в которой происходит переход по атрибуту.</span><span class="sxs-lookup"><span data-stu-id="5569a-113">Return the number of characters between the start character or anchor position (**acpStart** in [ITextStoreACP::FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition) or **paStart** in [ITextStoreAnchor::FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) ) and the position at which an attribute transition occurs.</span></span><br/> |
| <span id="TS_ATTR_FIND_UPDATESTART"></span><span id="ts_attr_find_updatestart"></span><dl> <span data-ttu-id="5569a-114"><dt>**TS \_ ATTR \_ Find \_ упдатестарт**</dt> <dt>(0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="5569a-114"><dt>**TS\_ATTR\_FIND\_UPDATESTART**</dt> <dt>( 0x4 )</dt></span></span> </dl>  | <span data-ttu-id="5569a-115">Используется функцией [итекстстореанчор:: финднекстаттртранситион](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) для размещения привязки ввода при следующем переходе атрибута, если он найден.</span><span class="sxs-lookup"><span data-stu-id="5569a-115">Used by [ITextStoreAnchor::FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) to position the input anchor at the next attribute transition, if one is found.</span></span> <span data-ttu-id="5569a-116">В противном случае входная привязка не изменяется.</span><span class="sxs-lookup"><span data-stu-id="5569a-116">Otherwise the input anchor is not modified.</span></span><br/>                                                                                                                             |
| <span id="TS_ATTR_FIND_WANT_VALUE"></span><span id="ts_attr_find_want_value"></span><dl> <span data-ttu-id="5569a-117"><dt>**TS \_ ATTR \_ найти \_ желаемое \_ значение**</dt> <dt>(0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="5569a-117"><dt>**TS\_ATTR\_FIND\_WANT\_VALUE**</dt> <dt>( 0x8 )</dt></span></span> </dl>    | <span data-ttu-id="5569a-118">Загрузить поддерживаемые значения атрибутов документа в структуру [служб терминалов \_ аттрвал](/windows/desktop/api/Textstor/ns-textstor-ts_attrval) .</span><span class="sxs-lookup"><span data-stu-id="5569a-118">Load supported document attribute values into the [TS\_ATTRVAL](/windows/desktop/api/Textstor/ns-textstor-ts_attrval) structure.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="TS_ATTR_FIND_WANT_END"></span><span id="ts_attr_find_want_end"></span><dl> <span data-ttu-id="5569a-119"><dt>**TS \_ \_Поиск \_ \_ конечного элемента**</dt> с атрибутом attr <dt>(0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="5569a-119"><dt>**TS\_ATTR\_FIND\_WANT\_END**</dt> <dt>( 0x10 )</dt></span></span> </dl>         | <span data-ttu-id="5569a-120">Используется [ITextStoreACP:: рекуестаттрстранситионингатпоситион](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition) и [Итекстстореанчор:: рекуестаттрстранситионингатпоситион](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition) для получения значений атрибута документа, заканчивающихся на указанном символе или позиции привязки.</span><span class="sxs-lookup"><span data-stu-id="5569a-120">Used by [ITextStoreACP::RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition) and [ITextStoreAnchor::RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition) to obtain the document attribute values that end at the specified character or anchor position.</span></span><br/>               |
| <span id="TS_ATTR_FIND_HIDDEN"></span><span id="ts_attr_find_hidden"></span><dl> <span data-ttu-id="5569a-121"><dt>**TS \_ \_Поиск \_ скрытого атрибута attr**</dt> <dt>(0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="5569a-121"><dt>**TS\_ATTR\_FIND\_HIDDEN**</dt> <dt>( 0x20 )</dt></span></span> </dl>                | <span data-ttu-id="5569a-122">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="5569a-122">Reserved.</span></span><br/>                                                                                                                                                                                                                                                                                                                                               |



## <a name="requirements"></a><span data-ttu-id="5569a-123">Требования</span><span class="sxs-lookup"><span data-stu-id="5569a-123">Requirements</span></span>



| <span data-ttu-id="5569a-124">Требование</span><span class="sxs-lookup"><span data-stu-id="5569a-124">Requirement</span></span> | <span data-ttu-id="5569a-125">Значение</span><span class="sxs-lookup"><span data-stu-id="5569a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5569a-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5569a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5569a-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5569a-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5569a-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5569a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5569a-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5569a-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5569a-130">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="5569a-130">Redistributable</span></span><br/>          | <span data-ttu-id="5569a-131">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="5569a-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="5569a-132">Header</span><span class="sxs-lookup"><span data-stu-id="5569a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="5569a-133"><dt>Текстстор. h</dt></span><span class="sxs-lookup"><span data-stu-id="5569a-133"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="5569a-134">IDL</span><span class="sxs-lookup"><span data-stu-id="5569a-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5569a-135"><dt>Текстстор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5569a-135"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5569a-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5569a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5569a-137">\_ATTRID TS</span><span class="sxs-lookup"><span data-stu-id="5569a-137">TS\_ATTRID</span></span>](ts-attrid.md)
</dt> <dt>

[<span data-ttu-id="5569a-138">\_АТТРВАЛ TS</span><span class="sxs-lookup"><span data-stu-id="5569a-138">TS\_ATTRVAL</span></span>](/windows/desktop/api/Textstor/ns-textstor-ts_attrval)
</dt> <dt>

[<span data-ttu-id="5569a-139">ITextStoreACP:: Финднекстаттртранситион</span><span class="sxs-lookup"><span data-stu-id="5569a-139">ITextStoreACP::FindNextAttrTransition</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition)
</dt> <dt>

[<span data-ttu-id="5569a-140">ITextStoreACP:: Рекуестаттрстранситионингатпоситион</span><span class="sxs-lookup"><span data-stu-id="5569a-140">ITextStoreACP::RequestAttrsTransitioningAtPosition</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition)
</dt> <dt>

[<span data-ttu-id="5569a-141">Итекстстореанчор:: Финднекстаттртранситион</span><span class="sxs-lookup"><span data-stu-id="5569a-141">ITextStoreAnchor::FindNextAttrTransition</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition)
</dt> <dt>

[<span data-ttu-id="5569a-142">Итекстстореанчор:: Рекуестаттрстранситионингатпоситион</span><span class="sxs-lookup"><span data-stu-id="5569a-142">ITextStoreAnchor::RequestAttrsTransitioningAtPosition</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition)
</dt> </dl>

 

 





