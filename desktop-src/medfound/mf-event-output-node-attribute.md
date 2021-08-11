---
description: Определяет узел топологии для приемника потока.
ms.assetid: 9aa6ca66-5122-4d05-94b9-32be194e9eb3
title: Атрибут MF_EVENT_OUTPUT_NODE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b2cbcbc243c195deb1061417adb6d93271b328fa242b497a7fdb232f5f7695e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244713"
---
# <a name="mf_event_output_node-attribute"></a>\_ \_ Атрибут узла вывода события MF \_

Определяет узел топологии для приемника потока.

## <a name="data-type"></a>Тип данных

**UINT64**

Рассматривать как [**топоид**](topoid.md).

## <a name="remarks"></a>Remarks

Значение этого атрибута является идентификатором узла для выходного узла в текущей топологии. Чтобы получить указатель на связанный узел, вызовите [**имфтопологи:: жетнодебид**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getnodebyid) в топологии.

Этот атрибут используется со следующими событиями:

-   [месессионстреамсинкформатчанжед](mesessionstreamsinkformatchanged.md)
-   [месинкинвалидатед](mesinkinvalidated.md)

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также статью

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты событий](event-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**Имфаттрибутес:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




