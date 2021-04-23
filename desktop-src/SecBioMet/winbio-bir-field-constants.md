---
title: Константы WINBIO_BIR_FIELD (Винбио \_ types. h)
description: Укажите битовую маску.
ms.assetid: D8D12BCF-FEB3-4E02-B751-9F3AE5048BC1
topic_type:
- apiref
api_name:
- WINBIO_BIR_FIELD_SUBHEAD_COUNT
- WINBIO_BIR_FIELD_PRODUCT_ID
- WINBIO_BIR_FIELD_PATRON_ID
- WINBIO_BIR_FIELD_INDEX
- WINBIO_BIR_FIELD_CREATION_DATE
- WINBIO_BIR_FIELD_VALIDITY_PERIOD
- WINBIO_BIR_FIELD_BIOMETRIC_TYPE
- WINBIO_BIR_FIELD_BIOMETRIC_SUBTYPE
- WINBIO_BIR_FIELD_CBEFF_HEADER_VERSION
- WINBIO_BIR_FIELD_PATRON_HEADER_VERSION
- WINBIO_BIR_FIELD_BIOMETRIC_PURPOSE
- WINBIO_BIR_FIELD_BIOMETRIC_CONDITION
- WINBIO_BIR_FIELD_QUALITY
- WINBIO_BIR_FIELD_CREATOR
- WINBIO_BIR_FIELD_CHALLENGE
- WINBIO_BIR_FIELD_PAYLOAD
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 104710f1686f13227fbe65782c2baf9c13149650
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340730"
---
# <a name="winbio_bir_field-constants"></a><span data-ttu-id="37dad-103">\_ \_ Константы поля винбио Бир</span><span class="sxs-lookup"><span data-stu-id="37dad-103">WINBIO\_BIR\_FIELD Constants</span></span>

<span data-ttu-id="37dad-104">Для создания битовой маски для элемента **валидфиелдс** в структуре [**\_ \_ заголовка винбио Бир**](winbio-bir-header.md) используются следующие константы.</span><span class="sxs-lookup"><span data-stu-id="37dad-104">The following constants are used to create a bitmask for the **ValidFields** member of the [**WINBIO\_BIR\_HEADER**](winbio-bir-header.md) structure.</span></span>



| <span data-ttu-id="37dad-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="37dad-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="37dad-106">Описание</span><span class="sxs-lookup"><span data-stu-id="37dad-106">Description</span></span>                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_BIR_FIELD_SUBHEAD_COUNT"></span><span id="winbio_bir_field_subhead_count"></span><dl> <span data-ttu-id="37dad-107"><dt>**Винбио \_ \_ \_ \_ Число подголовков полей Бир**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="37dad-107"><dt>**WINBIO\_BIR\_FIELD\_SUBHEAD\_COUNT**</dt> <dt>0x0001</dt></span></span> </dl>                          | <span data-ttu-id="37dad-108">В соответствии с НИСТИР 6529 — A обычная биометрическая среда форматов Exchange (КБЕФФ) патрон формат A, но не используется.</span><span class="sxs-lookup"><span data-stu-id="37dad-108">Provided for conformity with NISTIR 6529-A, the Common Biometric Exchange Formats Framework (CBEFF) Patron Format A, but not used.</span></span><br/> |
| <span id="WINBIO_BIR_FIELD_PRODUCT_ID"></span><span id="winbio_bir_field_product_id"></span><dl> <span data-ttu-id="37dad-109"><dt>**Винбио \_ \_Поле Бир \_ Product \_ ID**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="37dad-109"><dt>**WINBIO\_BIR\_FIELD\_PRODUCT\_ID**</dt> <dt>0x0002</dt></span></span> </dl>                                   | <span data-ttu-id="37dad-110">Элемент **ProductID** является допустимым.</span><span class="sxs-lookup"><span data-stu-id="37dad-110">The **ProductId** member is valid.</span></span><br/>                                                                                                 |
| <span id="WINBIO_BIR_FIELD_PATRON_ID"></span><span id="winbio_bir_field_patron_id"></span><dl> <span data-ttu-id="37dad-111"><dt>**Винбио \_ Бир \_ поле \_ патрон с \_ идентификатором**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="37dad-111"><dt>**WINBIO\_BIR\_FIELD\_PATRON\_ID**</dt> <dt>0x0004</dt></span></span> </dl>                                      | <span data-ttu-id="37dad-112">Предоставляется для соответствия с НИСТИР 6529-A, КБЕФФ патрон Format а, но не используется.</span><span class="sxs-lookup"><span data-stu-id="37dad-112">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_INDEX"></span><span id="winbio_bir_field_index"></span><dl> <span data-ttu-id="37dad-113"><dt>**Винбио \_ Бир \_ \_ Индекс поля**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="37dad-113"><dt>**WINBIO\_BIR\_FIELD\_INDEX**</dt> <dt>0x0008</dt></span></span> </dl>                                                   | <span data-ttu-id="37dad-114">Предоставляется для соответствия с НИСТИР 6529-A, КБЕФФ патрон Format а, но не используется.</span><span class="sxs-lookup"><span data-stu-id="37dad-114">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CREATION_DATE"></span><span id="winbio_bir_field_creation_date"></span><dl> <span data-ttu-id="37dad-115"><dt>**Винбио \_ \_ \_ \_ Дата создания поля Бир**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="37dad-115"><dt>**WINBIO\_BIR\_FIELD\_CREATION\_DATE**</dt> <dt>0x0010</dt></span></span> </dl>                          | <span data-ttu-id="37dad-116">Член **CreationDate** допустим.</span><span class="sxs-lookup"><span data-stu-id="37dad-116">The **CreationDate** member is valid.</span></span><br/>                                                                                              |
| <span id="WINBIO_BIR_FIELD_VALIDITY_PERIOD"></span><span id="winbio_bir_field_validity_period"></span><dl> <span data-ttu-id="37dad-117"><dt>**Винбио \_ Бир \_ \_ срока действия \_ поля**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="37dad-117"><dt>**WINBIO\_BIR\_FIELD\_VALIDITY\_PERIOD**</dt> <dt>0x0020</dt></span></span> </dl>                    | <span data-ttu-id="37dad-118">Элемент **валидитипериод** является допустимым.</span><span class="sxs-lookup"><span data-stu-id="37dad-118">The **ValidityPeriod** member is valid.</span></span><br/>                                                                                            |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_TYPE"></span><span id="winbio_bir_field_biometric_type"></span><dl> <span data-ttu-id="37dad-119"><dt>**Винбио \_ \_ \_ Биометрическая \_ тип Бир поля**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="37dad-119"><dt>**WINBIO\_BIR\_FIELD\_BIOMETRIC\_TYPE**</dt> <dt>0x0040</dt></span></span> </dl>                       | <span data-ttu-id="37dad-120">Член **типа** является допустимым.</span><span class="sxs-lookup"><span data-stu-id="37dad-120">The **Type** member is valid.</span></span><br/>                                                                                                      |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_SUBTYPE"></span><span id="winbio_bir_field_biometric_subtype"></span><dl> <span data-ttu-id="37dad-121"><dt>**Винбио \_ 0x0080 \_ \_ биометрического \_ типа Бир поля**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="37dad-121"><dt>**WINBIO\_BIR\_FIELD\_BIOMETRIC\_SUBTYPE**</dt> <dt>0x0080</dt></span></span> </dl>              | <span data-ttu-id="37dad-122">Элемент **подтипа** является допустимым.</span><span class="sxs-lookup"><span data-stu-id="37dad-122">The **Subtype** member is valid.</span></span><br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_CBEFF_HEADER_VERSION"></span><span id="winbio_bir_field_cbeff_header_version"></span><dl> <span data-ttu-id="37dad-123"><dt>**Винбио \_ Бир \_ \_ заголовок кбефф \_ поля \_ версии**</dt> <dt>0x0100</dt></span><span class="sxs-lookup"><span data-stu-id="37dad-123"><dt>**WINBIO\_BIR\_FIELD\_CBEFF\_HEADER\_VERSION**</dt> <dt>0x0100</dt></span></span> </dl>    | <span data-ttu-id="37dad-124">Элемент **хеадерверсион** является допустимым.</span><span class="sxs-lookup"><span data-stu-id="37dad-124">The **HeaderVersion** member is valid.</span></span><br/>                                                                                             |
| <span id="WINBIO_BIR_FIELD_PATRON_HEADER_VERSION"></span><span id="winbio_bir_field_patron_header_version"></span><dl> <span data-ttu-id="37dad-125"><dt>**Винбио \_ Бир \_ \_ заголовок патрон \_ поля \_ версии**</dt> <dt>0x0200</dt></span><span class="sxs-lookup"><span data-stu-id="37dad-125"><dt>**WINBIO\_BIR\_FIELD\_PATRON\_HEADER\_VERSION**</dt> <dt>0x0200</dt></span></span> </dl> | <span data-ttu-id="37dad-126">Элемент **патронхеадерверсион** является допустимым.</span><span class="sxs-lookup"><span data-stu-id="37dad-126">The **PatronHeaderVersion** member is valid.</span></span><br/>                                                                                       |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_PURPOSE"></span><span id="winbio_bir_field_biometric_purpose"></span><dl> <span data-ttu-id="37dad-127"><dt>**Винбио \_ \_ \_ Биометрическое \_ Назначение поля Бир**</dt> <dt>0x0400</dt></span><span class="sxs-lookup"><span data-stu-id="37dad-127"><dt>**WINBIO\_BIR\_FIELD\_BIOMETRIC\_PURPOSE**</dt> <dt>0x0400</dt></span></span> </dl>              | <span data-ttu-id="37dad-128">Член **назначения** является допустимым.</span><span class="sxs-lookup"><span data-stu-id="37dad-128">The **Purpose** member is valid.</span></span><br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_CONDITION"></span><span id="winbio_bir_field_biometric_condition"></span><dl> <span data-ttu-id="37dad-129"><dt>**Винбио \_ Бир \_ \_ \_ условие БИОметрического метрики**</dt> <dt>0x0800</dt></span><span class="sxs-lookup"><span data-stu-id="37dad-129"><dt>**WINBIO\_BIR\_FIELD\_BIOMETRIC\_CONDITION**</dt> <dt>0x0800</dt></span></span> </dl>        | <span data-ttu-id="37dad-130">Предоставляется для соответствия с НИСТИР 6529-A, КБЕФФ патрон Format а, но не используется.</span><span class="sxs-lookup"><span data-stu-id="37dad-130">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_QUALITY"></span><span id="winbio_bir_field_quality"></span><dl> <span data-ttu-id="37dad-131"><dt>**Винбио \_ Бир \_ \_ качества поля**</dt> <dt>0x1000</dt></span><span class="sxs-lookup"><span data-stu-id="37dad-131"><dt>**WINBIO\_BIR\_FIELD\_QUALITY**</dt> <dt>0x1000</dt></span></span> </dl>                                             | <span data-ttu-id="37dad-132">Элемент **Quality** является допустимым.</span><span class="sxs-lookup"><span data-stu-id="37dad-132">The **DataQuality** member is valid.</span></span><br/>                                                                                               |
| <span id="WINBIO_BIR_FIELD_CREATOR"></span><span id="winbio_bir_field_creator"></span><dl> <span data-ttu-id="37dad-133"><dt>**Винбио \_ \_ \_ Создатель поля Бир**</dt> <dt>0x2000</dt></span><span class="sxs-lookup"><span data-stu-id="37dad-133"><dt>**WINBIO\_BIR\_FIELD\_CREATOR**</dt> <dt>0x2000</dt></span></span> </dl>                                             | <span data-ttu-id="37dad-134">Предоставляется для соответствия с НИСТИР 6529-A, КБЕФФ патрон Format а, но не используется.</span><span class="sxs-lookup"><span data-stu-id="37dad-134">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CHALLENGE"></span><span id="winbio_bir_field_challenge"></span><dl> <span data-ttu-id="37dad-135"><dt>**Винбио \_ \_ \_ Запрос поля Бир**</dt> <dt>0x4000</dt></span><span class="sxs-lookup"><span data-stu-id="37dad-135"><dt>**WINBIO\_BIR\_FIELD\_CHALLENGE**</dt> <dt>0x4000</dt></span></span> </dl>                                       | <span data-ttu-id="37dad-136">Предоставляется для соответствия с НИСТИР 6529-A, КБЕФФ патрон Format а, но не используется.</span><span class="sxs-lookup"><span data-stu-id="37dad-136">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_PAYLOAD"></span><span id="winbio_bir_field_payload"></span><dl> <span data-ttu-id="37dad-137"><dt>**Винбио \_ \_ \_ Полезные данные поля Бир**</dt> <dt>0x8000</dt></span><span class="sxs-lookup"><span data-stu-id="37dad-137"><dt>**WINBIO\_BIR\_FIELD\_PAYLOAD**</dt> <dt>0x8000</dt></span></span> </dl>                                             | <span data-ttu-id="37dad-138">Предоставляется для соответствия с НИСТИР 6529-A, КБЕФФ патрон Format а, но не используется.</span><span class="sxs-lookup"><span data-stu-id="37dad-138">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="37dad-139">Требования</span><span class="sxs-lookup"><span data-stu-id="37dad-139">Requirements</span></span>



| <span data-ttu-id="37dad-140">Требование</span><span class="sxs-lookup"><span data-stu-id="37dad-140">Requirement</span></span> | <span data-ttu-id="37dad-141">Значение</span><span class="sxs-lookup"><span data-stu-id="37dad-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37dad-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="37dad-142">Minimum supported client</span></span><br/> | <span data-ttu-id="37dad-143">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="37dad-143">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="37dad-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="37dad-144">Minimum supported server</span></span><br/> | <span data-ttu-id="37dad-145">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="37dad-145">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="37dad-146">Header</span><span class="sxs-lookup"><span data-stu-id="37dad-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="37dad-147"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="37dad-147"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37dad-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="37dad-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37dad-149">Константы клиентского приложения</span><span class="sxs-lookup"><span data-stu-id="37dad-149">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





