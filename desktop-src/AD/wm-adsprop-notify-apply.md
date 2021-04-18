---
title: Сообщение WM_ADSPROP_NOTIFY_APPLY (Адспроп. h)
description: Расширение страницы свойств службы каталогов Active Directory отправляет \_ сообщение об установке WM адспроп \_ Notify \_ в объект уведомления, если страница свойств PSN \_ Применить обработчик.
ms.assetid: 3536054b-83ee-4cfa-ab54-c0af3a46289e
ms.tgt_platform: multiple
keywords:
- Сообщение WM_ADSPROP_NOTIFY_APPLY Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_APPLY
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0ccd5bb95e3f092634d54ba0534e81ded6701bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654661"
---
# <a name="wm_adsprop_notify_apply-message"></a>\_ \_ Сообщение об использовании уведомления WM адспроп \_

Расширение страницы свойств службы каталогов Active Directory отправляет сообщение об **\_ \_ \_ установке WM адспроп notify** в объект уведомления, если страница свойств PSN \_ Применить обработчик.


```C++
WM_ADSPROP_NOTIFY_APPLY

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

При добавлении страниц в оснастку консоли управления (MMC) Active Directory Manager Active Directory вкладки свойств MMC создают объекты уведомлений по вызову функции [**адспропкреатенотифйобж**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) , а затем передает этот обработчик объекта уведомления на каждую страницу свойств.

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

 

 





