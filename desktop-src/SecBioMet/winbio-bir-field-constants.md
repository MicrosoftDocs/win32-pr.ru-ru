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
# <a name="winbio_bir_field-constants"></a>\_ \_ Константы поля винбио Бир

Для создания битовой маски для элемента **валидфиелдс** в структуре [**\_ \_ заголовка винбио Бир**](winbio-bir-header.md) используются следующие константы.



| Константа/значение                                                                                                                                                                                                                                                                                           | Описание                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_BIR_FIELD_SUBHEAD_COUNT"></span><span id="winbio_bir_field_subhead_count"></span><dl> <dt>**Винбио \_ \_ \_ \_ Число подголовков полей Бир**</dt> <dt>0x0001</dt> </dl>                          | В соответствии с НИСТИР 6529 — A обычная биометрическая среда форматов Exchange (КБЕФФ) патрон формат A, но не используется.<br/> |
| <span id="WINBIO_BIR_FIELD_PRODUCT_ID"></span><span id="winbio_bir_field_product_id"></span><dl> <dt>**Винбио \_ \_Поле Бир \_ Product \_ ID**</dt> <dt>0x0002</dt> </dl>                                   | Элемент **ProductID** является допустимым.<br/>                                                                                                 |
| <span id="WINBIO_BIR_FIELD_PATRON_ID"></span><span id="winbio_bir_field_patron_id"></span><dl> <dt>**Винбио \_ Бир \_ поле \_ патрон с \_ идентификатором**</dt> <dt>0x0004</dt> </dl>                                      | Предоставляется для соответствия с НИСТИР 6529-A, КБЕФФ патрон Format а, но не используется.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_INDEX"></span><span id="winbio_bir_field_index"></span><dl> <dt>**Винбио \_ Бир \_ \_ Индекс поля**</dt> <dt>0x0008</dt> </dl>                                                   | Предоставляется для соответствия с НИСТИР 6529-A, КБЕФФ патрон Format а, но не используется.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CREATION_DATE"></span><span id="winbio_bir_field_creation_date"></span><dl> <dt>**Винбио \_ \_ \_ \_ Дата создания поля Бир**</dt> <dt>0x0010</dt> </dl>                          | Член **CreationDate** допустим.<br/>                                                                                              |
| <span id="WINBIO_BIR_FIELD_VALIDITY_PERIOD"></span><span id="winbio_bir_field_validity_period"></span><dl> <dt>**Винбио \_ Бир \_ \_ срока действия \_ поля**</dt> <dt>0x0020</dt> </dl>                    | Элемент **валидитипериод** является допустимым.<br/>                                                                                            |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_TYPE"></span><span id="winbio_bir_field_biometric_type"></span><dl> <dt>**Винбио \_ \_ \_ Биометрическая \_ тип Бир поля**</dt> <dt>0x0040</dt> </dl>                       | Член **типа** является допустимым.<br/>                                                                                                      |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_SUBTYPE"></span><span id="winbio_bir_field_biometric_subtype"></span><dl> <dt>**Винбио \_ 0x0080 \_ \_ биометрического \_ типа Бир поля**</dt> <dt></dt> </dl>              | Элемент **подтипа** является допустимым.<br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_CBEFF_HEADER_VERSION"></span><span id="winbio_bir_field_cbeff_header_version"></span><dl> <dt>**Винбио \_ Бир \_ \_ заголовок кбефф \_ поля \_ версии**</dt> <dt>0x0100</dt> </dl>    | Элемент **хеадерверсион** является допустимым.<br/>                                                                                             |
| <span id="WINBIO_BIR_FIELD_PATRON_HEADER_VERSION"></span><span id="winbio_bir_field_patron_header_version"></span><dl> <dt>**Винбио \_ Бир \_ \_ заголовок патрон \_ поля \_ версии**</dt> <dt>0x0200</dt> </dl> | Элемент **патронхеадерверсион** является допустимым.<br/>                                                                                       |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_PURPOSE"></span><span id="winbio_bir_field_biometric_purpose"></span><dl> <dt>**Винбио \_ \_ \_ Биометрическое \_ Назначение поля Бир**</dt> <dt>0x0400</dt> </dl>              | Член **назначения** является допустимым.<br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_CONDITION"></span><span id="winbio_bir_field_biometric_condition"></span><dl> <dt>**Винбио \_ Бир \_ \_ \_ условие БИОметрического метрики**</dt> <dt>0x0800</dt> </dl>        | Предоставляется для соответствия с НИСТИР 6529-A, КБЕФФ патрон Format а, но не используется.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_QUALITY"></span><span id="winbio_bir_field_quality"></span><dl> <dt>**Винбио \_ Бир \_ \_ качества поля**</dt> <dt>0x1000</dt> </dl>                                             | Элемент **Quality** является допустимым.<br/>                                                                                               |
| <span id="WINBIO_BIR_FIELD_CREATOR"></span><span id="winbio_bir_field_creator"></span><dl> <dt>**Винбио \_ \_ \_ Создатель поля Бир**</dt> <dt>0x2000</dt> </dl>                                             | Предоставляется для соответствия с НИСТИР 6529-A, КБЕФФ патрон Format а, но не используется.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CHALLENGE"></span><span id="winbio_bir_field_challenge"></span><dl> <dt>**Винбио \_ \_ \_ Запрос поля Бир**</dt> <dt>0x4000</dt> </dl>                                       | Предоставляется для соответствия с НИСТИР 6529-A, КБЕФФ патрон Format а, но не используется.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_PAYLOAD"></span><span id="winbio_bir_field_payload"></span><dl> <dt>**Винбио \_ \_ \_ Полезные данные поля Бир**</dt> <dt>0x8000</dt> </dl>                                             | Предоставляется для соответствия с НИСТИР 6529-A, КБЕФФ патрон Format а, но не используется.<br/>                                                   |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                                    |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Винбио \_ types. h (include винбио. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы клиентского приложения](client-application-constants.md)
</dt> </dl>

 

 





