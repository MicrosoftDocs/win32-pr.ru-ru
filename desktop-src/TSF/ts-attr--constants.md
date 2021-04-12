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
# <a name="ts_attr_-constants"></a>\_ \_ \* КОНСТАНТы attr TS

\_ \_ \* Константы TS attr используются для получения и изменения значений атрибутов документа. Эти константы формируют возможные значения битовых флагов в методах [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) и [итекстстореанчор](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) .



| Константа/значение                                                                                                                                                                                                                                                 | Описание                                                                                                                                                                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_ATTR_FIND_BACKWARDS"></span><span id="ts_attr_find_backwards"></span><dl> <dt>**TS \_ \_Найти в \_ обратном направлении**</dt> <dt>(0x1)</dt> </dl>        | Поиск в обратном направлении с начального символа или позиции привязки для позиции, в которой переход выполняется в значении атрибута документа. Значение по умолчанию — поиск вперед.<br/>                                                                                                                                                                                    |
| <span id="TS_ATTR_FIND_WANT_OFFSET"></span><span id="ts_attr_find_want_offset"></span><dl> <dt>**TS \_ ATTR \_ Поиск \_ желаемого \_ смещения**</dt> <dt>(0x2)</dt> </dl> | Возвращает количество символов между начальным символом или позицией привязки (**акпстарт** в [ITextStoreACP:: финднекстаттртранситион](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition) или **Пастарт** в [итекстстореанчор:: финднекстаттртранситион](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) ) и позиции, в которой происходит переход по атрибуту.<br/> |
| <span id="TS_ATTR_FIND_UPDATESTART"></span><span id="ts_attr_find_updatestart"></span><dl> <dt>**TS \_ ATTR \_ Find \_ упдатестарт**</dt> <dt>(0x4)</dt> </dl>  | Используется функцией [итекстстореанчор:: финднекстаттртранситион](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) для размещения привязки ввода при следующем переходе атрибута, если он найден. В противном случае входная привязка не изменяется.<br/>                                                                                                                             |
| <span id="TS_ATTR_FIND_WANT_VALUE"></span><span id="ts_attr_find_want_value"></span><dl> <dt>**TS \_ ATTR \_ найти \_ желаемое \_ значение**</dt> <dt>(0x8)</dt> </dl>    | Загрузить поддерживаемые значения атрибутов документа в структуру [служб терминалов \_ аттрвал](/windows/desktop/api/Textstor/ns-textstor-ts_attrval) .<br/>                                                                                                                                                                                                                                                              |
| <span id="TS_ATTR_FIND_WANT_END"></span><span id="ts_attr_find_want_end"></span><dl> <dt>**TS \_ \_Поиск \_ \_ конечного элемента**</dt> с атрибутом attr <dt>(0x10)</dt> </dl>         | Используется [ITextStoreACP:: рекуестаттрстранситионингатпоситион](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition) и [Итекстстореанчор:: рекуестаттрстранситионингатпоситион](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition) для получения значений атрибута документа, заканчивающихся на указанном символе или позиции привязки.<br/>               |
| <span id="TS_ATTR_FIND_HIDDEN"></span><span id="ts_attr_find_hidden"></span><dl> <dt>**TS \_ \_Поиск \_ скрытого атрибута attr**</dt> <dt>(0x20)</dt> </dl>                | Зарезервировано.<br/>                                                                                                                                                                                                                                                                                                                                               |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Распространяемые компоненты<br/>          | TSF 1,0 в Windows 2000 профессиональная<br/>                                         |
| Header<br/>                   | <dl> <dt>Текстстор. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Текстстор. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[\_ATTRID TS](ts-attrid.md)
</dt> <dt>

[\_АТТРВАЛ TS](/windows/desktop/api/Textstor/ns-textstor-ts_attrval)
</dt> <dt>

[ITextStoreACP:: Финднекстаттртранситион](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition)
</dt> <dt>

[ITextStoreACP:: Рекуестаттрстранситионингатпоситион](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition)
</dt> <dt>

[Итекстстореанчор:: Финднекстаттртранситион](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition)
</dt> <dt>

[Итекстстореанчор:: Рекуестаттрстранситионингатпоситион](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition)
</dt> </dl>

 

 





