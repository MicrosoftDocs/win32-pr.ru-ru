---
description: Содержит идентификатор CLSID для загрузчика топологии для сеанса мультимедиа.
ms.assetid: 672274fb-71fc-49ca-bab6-1fc4de21d17c
title: Атрибут MF_SESSION_TOPOLOADER (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb5299e058862ad2d26b1fb9debe0028aba4703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712859"
---
# <a name="mf_session_topoloader-attribute"></a>\_ \_ Атрибут ТОПОЛОАДЕР сеанса MF

Содержит идентификатор CLSID для загрузчика топологии для сеанса мультимедиа.

## <a name="data-type"></a>Тип данных

**GUID**

## <a name="remarks"></a>Комментарии

Этот атрибут можно использовать для предоставления пользовательского загрузчика топологии для сеанса мультимедиа.

Задайте этот атрибут с помощью параметра *пконфигуратион* функции [**Мфкреатемедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) или функции [**мфкреатепмпмедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .

Если этот атрибут задан, сеанс мультимедиа вызывает **CoCreateInstance** с указанным идентификатором CLSID при создании загрузчика топологии. Объект, созданный этим CLSID, должен предоставлять интерфейс [**имфтополоадер**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) .

Если этот атрибут не задан, сеанс мультимедиа создает загрузчик топологии по умолчанию, предоставленный в Media Foundation.

Загрузчик топологии должен поддерживать многопоточные подразделения. Необходимо зарегистрировать загрузчик топологии как ThreadingModel = "both". Кроме того, при использовании загрузчика топологии внутри защищенного пути к носителю (PMP) загрузчик топологии должен быть доверенным компонентом. Дополнительные сведения см. в разделе [путь к защищенному носителю](protected-media-path.md).

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: a GUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**Имфаттрибутес:: Сетгуид**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[Атрибуты сеанса мультимедиа](media-session-attributes.md)
</dt> <dt>

[Пользовательские загрузчики топологии](custom-topology-loaders.md)
</dt> </dl>

 

 




