---
description: Содержит дополнительные данные формата для типа мультимедиа.
ms.assetid: 020832c4-40a1-4d8b-ada0-7a04ce097bce
title: Атрибут MF_MT_USER_DATA (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0196e8fea06bb84fe5a78a8b486f95864e0c6d889692dfa6f3ee9b1103da518a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012786"
---
# <a name="mf_mt_user_data-attribute"></a>\_ \_ Атрибут данных пользователя MF MT \_

Содержит дополнительные данные формата для типа мультимедиа.

## <a name="data-type"></a>Тип данных

массив байтов;

## <a name="remarks"></a>Remarks

Значение данных в этом атрибуте зависит от формата, который описывается типом мультимедиа.



| Тип формата                                                                                                           | Дополнительные данные формата                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Кодек мультимедиа.                                                                                                  | Частные данные кодека.                                                                                                                       |
| Преобразована структура [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) или [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .   | Дополнительные данные, которые появляются после структуры [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) , не включая таблицу цветов или цветовые маски. |
| Преобразована структура [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) или [**вавеформатекстенсибле**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) . | Дополнительные данные, которые отображаются после структуры звукового формата.                                                                                 |



 

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Приложения UWP для классических приложений Vista \|\]<br/>                              |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для классических приложений сервера 2008 \|\]<br/>                        |
| Заголовок<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**Имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> </dl>

 

 
