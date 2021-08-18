---
title: Сообщение WM_ADSPROP_NOTIFY_ERROR (Адспроп. h)
description: Сообщение об ошибке WM \_ адспроп \_ Notify \_ добавляет сообщение об ошибке в список сообщений об ошибках, которые отображаются путем вызова функции адспропшоверрордиалог.
ms.assetid: 7abf1b3d-5abe-42cd-baeb-1bf863c7f04d
ms.tgt_platform: multiple
keywords:
- Сообщение WM_ADSPROP_NOTIFY_ERROR Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_ERROR
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52f88cd4c60dcfcceed60ca644f7c59f65bee16e344cc17664e8b4be1ee18fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024292"
---
# <a name="wm_adsprop_notify_error-message"></a>\_ \_ \_ Сообщение об ошибке АДСПРОП для уведомления WM

Сообщение об ошибке **WM \_ адспроп \_ Notify \_** добавляет сообщение об ошибке в список сообщений об ошибках, которые отображаются путем вызова функции [**адспропшоверрордиалог**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) .


```C++
WM_ADSPROP_NOTIFY_ERROR

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*HWND* 
</dt> <dd>

Маркер объекта уведомления. Это параметр *хнотифйобжект* , полученный [**адспропкреатенотифйобж**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> <dt>

*wParam* 
</dt> <dd>

Не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**адспроперрор**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror) , содержащую данные сообщения об ошибке.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не имеет возвращаемого значения.

## <a name="remarks"></a>Remarks

Функция [**адспропсендеррормессаже**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) является предпочтительным методом отправки этого сообщения.

Сообщения об ошибках, добавленные сообщением **\_ \_ \_ об ошибке с уведомлением WM адспроп** , накапливаются до вызова [**адспропшоверрордиалог**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) . **Адспропшоверрордиалог** объединяет и отображает накопленные сообщения об ошибках. При отклонении диалогового окна об ошибке накопленные сообщения об ошибках удаляются.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                       |
| Заголовок<br/>                   | <dl> <dt>Адспроп. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Сообщения в домен Active Directory Services](messages-in-active-directory-domain-services.md)
</dt> <dt>

[**адспроперрор**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror)
</dt> <dt>

[**адспропсендеррормессаже**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage)
</dt> <dt>

[**адспропшоверрордиалог**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog)
</dt> </dl>

 

 





