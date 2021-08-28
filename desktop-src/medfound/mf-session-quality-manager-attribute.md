---
description: Содержит идентификатор CLSID диспетчера качества для сеанса мультимедиа.
ms.assetid: 24b4a5e3-84f1-44d0-a8ac-75c127ec8a8a
title: Атрибут MF_SESSION_QUALITY_MANAGER (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 049ecde194f7cccf97460ac99c566815d43b222132f72b70a0874719fc663c07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117691584"
---
# <a name="mf_session_quality_manager-attribute"></a>\_ \_ Атрибут диспетчера качества сеанса MF \_

Содержит идентификатор CLSID диспетчера качества для сеанса мультимедиа.

## <a name="data-type"></a>Тип данных

**GUID**

## <a name="remarks"></a>Remarks

Этот атрибут можно использовать для предоставления пользовательского диспетчера качества для сеанса мультимедиа.

Задайте этот атрибут с помощью параметра *пконфигуратион* функции [**мфкреатемедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) или [**мфкреатепмпмедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .

Если этот атрибут задан, сеанс мультимедиа вызывает **CoCreateInstance** с указанным идентификатором CLSID для создания диспетчера качества. Объект, созданный этим CLSID, должен предоставлять интерфейс [**имфкуалитиманажер**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager) .

Если этот атрибут не задан, сеанс мультимедиа создает диспетчер качества по умолчанию, предоставленный в Media Foundation.

Если вы хотите запустить сеанс мультимедиа без диспетчера качества, присвойте этому атрибуту **\_ значение GUID NULL**.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



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
</dt> </dl>

 

 




