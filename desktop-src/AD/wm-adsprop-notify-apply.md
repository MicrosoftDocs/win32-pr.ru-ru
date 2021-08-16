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
ms.openlocfilehash: 6cc130a83aa77021e0be512d9b2ad27914b4c6be382c0290e082e1fbd67b8b22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024302"
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

## <a name="remarks"></a>Remarks

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

 

 





