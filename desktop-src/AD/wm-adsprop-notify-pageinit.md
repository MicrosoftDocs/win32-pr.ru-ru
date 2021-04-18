---
title: Сообщение WM_ADSPROP_NOTIFY_PAGEINIT (Адспроп. h)
description: Расширение страницы свойств Active Directory вызывает метод Адспропжетинитинфо для получения данных о объекте каталога, к которому применяется расширение страницы свойств.
ms.assetid: 473c5a75-d0d9-4d12-b855-63683e8cdf3f
ms.tgt_platform: multiple
keywords:
- Сообщение WM_ADSPROP_NOTIFY_PAGEINIT Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_PAGEINIT
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2718ee30cdbecec7c4e0954636aa14c75f13027
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533986"
---
# <a name="wm_adsprop_notify_pageinit-message"></a>\_Адспроп \_ уведомления WM \_ пажеинит

Расширение страницы свойств Active Directory вызывает метод [**адспропжетинитинфо**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) для получения данных о объекте каталога, к которому применяется расширение страницы свойств. Функция **адспропжетинитинфо** отправляет сообщение **WM \_ адспроп \_ Notify \_ пажеинит** в объект уведомления для достижения этого результата.


```C++
WM_ADSPROP_NOTIFY_PAGEINIT

    WPARAM wParam
    LPARAM pADsPropInitParams
    
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*HWND* 
</dt> <dd>

Маркер объекта уведомления. Это параметр *хнотифйобжект* , полученный при вызове [**адспропкреатенотифйобж**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> <dt>

*wParam* 
</dt> <dd>

Не используется.

</dd> <dt>

*падспропинитпарамс* 
</dt> <dd>

Указатель на структуру [**адспропинитпарамс**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams) , которая получает сведения об объекте каталога. Это параметр *пинитпарамс* , передаваемый в [**адспропкреатенотифйобж**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не имеет возвращаемого значения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                       |
| Header<br/>                   | <dl> <dt>Адспроп. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Сообщения в домен Active Directory Services](messages-in-active-directory-domain-services.md)
</dt> <dt>

[**адспропжетинитинфо**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo)
</dt> <dt>

[**адспропинитпарамс**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams)
</dt> </dl>

 

 





