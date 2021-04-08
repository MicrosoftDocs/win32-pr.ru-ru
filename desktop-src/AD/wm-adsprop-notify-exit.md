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
ms.openlocfilehash: 32d74ef4b7dfa525cfb77a6d89499837cbfac8f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989199"
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

## <a name="remarks"></a>Комментарии

Объект уведомления удалит себя в ответ на это сообщение. При отправке этого сообщения обработчик объекта уведомления должен считаться недопустимым.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                       |
| Header<br/>                   | <dl> <dt>Адспроп. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**адспропкреатенотифйобж**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[Сообщения в домен Active Directory Services](messages-in-active-directory-domain-services.md)
</dt> </dl>

 

 





