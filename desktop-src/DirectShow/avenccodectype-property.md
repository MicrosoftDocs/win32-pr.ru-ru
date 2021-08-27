---
description: Задает схему кодирования.
ms.assetid: a26951d6-67fb-43fb-849f-331416e9d7c2
title: Свойство Авенккодектипе (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3727ff8cc2a59208d63874de173e3e44e89e3e6f2ebc37201218f9656aa09cd4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084614"
---
# <a name="avenccodectype-property"></a>Авенккодектипе, свойство

Задает схему кодирования.

Это свойство доступно для чтения и записи.

## <a name="data-type"></a>Тип данных

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>GUID свойства

**КОДЕКАПИ \_ авенккодектипе**

## <a name="property-value"></a>Значение свойства

Значение этого свойства является строкой **BSTR** , содержащей строковое представление идентификатора GUID. Определены следующие идентификаторы GUID.



| Идентификатор GUID                                      | Описание                                        |
|-------------------------------------------|----------------------------------------------------|
| КОДЕКАПИ \_ GUID \_ авенкдолбидигиталконсумер | Звук цифрового потребителя Dolby                       |
| КОДЕКАПИ \_ GUID \_ авенкдолбидигиталплус     | Dolby Digital Plus Audio                           |
| КОДЕКАПИ \_ GUID \_ авенкдолбидигиталпро      | Dolby digital Pro audio                            |
| КОДЕКАПИ \_ GUID \_ авенкдтс                  | Аудио службы DTS                                          |
| КОДЕКАПИ \_ GUID \_ авенкдтшд                | DTS — аудио HD                                       |
| КОДЕКАПИ \_ GUID \_ авенкдв                   | Видео DV                                           |
| КОДЕКАПИ \_ GUID \_ AVEncH264Video            | Видео H. 264                                        |
| КОДЕКАПИ \_ GUID \_ авенкмлп                  | Звук упаковки меридианов без потерь (MLP)              |
| КОДЕКАПИ \_ GUID \_ AVEncMPEG1Audio           | Аудио MPEG-1                                       |
| КОДЕКАПИ \_ GUID \_ AVEncMPEG1Video           | Видео MPEG-1                                       |
| КОДЕКАПИ \_ GUID \_ AVEncMPEG2Audio           | Звук MPEG-2                                       |
| КОДЕКАПИ \_ GUID \_ AVEncMPEG2Video           | Видео MPEG-2                                       |
| КОДЕКАПИ \_ GUID \_ авенкпкм                  | Звук PCM                                          |
| КОДЕКАПИ \_ GUID \_ авенксддс                 | Аудио динамический цифровой звук (SDD) Sony            |
| КОДЕКАПИ \_ GUID \_ авенквмалосслесс          | Windows Аудио Media Audio 9 без потерь               |
| КОДЕКАПИ \_ GUID \_ авенквмапро               | Windows аудио Media audio 9 Professional (WMA Pro) Audio |
| КОДЕКАПИ \_ GUID \_ авенквмавоице             | Windows Голосовой звук Media Audio 9                  |
| КОДЕКАПИ \_ GUID \_ авенквмв                  | Windows Мультимедийное видео                                |
| КОДЕКАПИ \_ GUID \_ AVEndMPEG4Video           | Видео MPEG-4                                       |



 

## <a name="remarks"></a>Remarks

Приложения могут установить это свойство, чтобы указать используемую схему кодирования. Кодеки также могут возвращать это свойство как возможность.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional приложения \[ UWP для классических приложений \|\]<br/>                     |
| Минимальная версия сервера<br/> | \[приложения UWP для классических приложений Windows 2000 \|\]<br/>                           |
| Заголовок<br/>                   | <dl> <dt>Кодекапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Свойства кодека API](codec-api-properties.md)
</dt> <dt>

[**Интерфейс Икодекапи**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




