---
title: Сообщение WM_ADSPROP_NOTIFY_EXIT (Адспроп. h)
description: Расширение страницы свойств Active Directory отправляет \_ сообщение о выходе WM адспроп \_ Notify \_ в объект уведомления, когда объект уведомления больше не требуется.
ms.assetid: b0f58c73-8953-412d-b801-bf34967fe0b4
ms.tgt_platform: multiple
keywords:
- Сообщение WM_ADSPROP_NOTIFY_EXIT Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_EXIT
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e144bb0b24112cabe1a806d4c746aac07708443665c0f457df8756be36d80b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181968"
---
# <a name="wm_adsprop_notify_exit-message"></a>\_ \_ Сообщение о выходе из уведомления WM адспроп \_

Расширение страницы свойств Active Directory отправляет сообщение о **\_ \_ \_ выходе WM адспроп notify** в объект уведомления, когда объект уведомления больше не требуется.


```C++
WM_ADSPROP_NOTIFY_EXIT

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*HWND* 
</dt> <dd>

Маркер объекта уведомления. Чтобы получить этот маркер, вызовите [**адспропкреатенотифйобж**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> <dt>

*wParam* 
</dt> <dd>

Не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не имеет возвращаемого значения.

## <a name="remarks"></a>Remarks

Объект уведомления удалит себя в ответ на это сообщение. При отправке этого сообщения обработчик объекта уведомления должен считаться недопустимым.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                       |
| Header<br/>                   | <dl> <dt>Адспроп. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**адспропкреатенотифйобж**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[Сообщения в домен Active Directory Services](messages-in-active-directory-domain-services.md)
</dt> </dl>

 

 





