---
description: Содержит идентификатор CLSID для загрузчика топологии для сеанса мультимедиа.
ms.assetid: 672274fb-71fc-49ca-bab6-1fc4de21d17c
title: Атрибут MF_SESSION_TOPOLOADER (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9568193bbdbd46485015b6e5975db26fca2b552b23b7c227576e4e6544d69af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955134"
---
# <a name="mf_session_topoloader-attribute"></a>\_ \_ Атрибут ТОПОЛОАДЕР сеанса MF

Содержит идентификатор CLSID для загрузчика топологии для сеанса мультимедиа.

## <a name="data-type"></a>Тип данных

**GUID**

## <a name="remarks"></a>Remarks

Этот атрибут можно использовать для предоставления пользовательского загрузчика топологии для сеанса мультимедиа.

Задайте этот атрибут с помощью параметра *пконфигуратион* функции [**Мфкреатемедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) или функции [**мфкреатепмпмедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .

Если этот атрибут задан, сеанс мультимедиа вызывает **CoCreateInstance** с указанным идентификатором CLSID при создании загрузчика топологии. Объект, созданный этим CLSID, должен предоставлять интерфейс [**имфтополоадер**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) .

Если этот атрибут не задан, сеанс мультимедиа создает загрузчик топологии по умолчанию, предоставленный в Media Foundation.

Загрузчик топологии должен поддерживать многопоточные подразделения. Необходимо зарегистрировать загрузчик топологии как ThreadingModel = "both". Кроме того, при использовании загрузчика топологии внутри защищенного пути к носителю (PMP) загрузчик топологии должен быть доверенным компонентом. Дополнительные сведения см. в разделе [путь к защищенному носителю](protected-media-path.md).

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также

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

 

 




