---
title: Сообщение WM_ADSPROP_NOTIFY_PAGEHWND (Адспроп. h)
description: Расширение страницы свойств службы каталогов Active Directory вызывает метод Адспропсесвнд для информирования объекта уведомления об маркере окна страницы свойств.
ms.assetid: eb8bf525-cd7f-44d0-a0f9-43178a29c443
ms.tgt_platform: multiple
keywords:
- Сообщение WM_ADSPROP_NOTIFY_PAGEHWND Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_PAGEHWND
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d74ef2db993d2a3daf10f69687b8f3525ef80a87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137190"
---
# <a name="wm_adsprop_notify_pagehwnd-message"></a>\_Адспроп \_ уведомления WM \_ пажехвнд

Расширение страницы свойств службы каталогов Active Directory вызывает метод [**адспропсесвнд**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) для информирования объекта уведомления об маркере окна страницы свойств. Функция **адспропсесвнд** отправляет сообщение **WM \_ адспроп \_ Notify \_ пажехвнд** объекту уведомления, который информирует объект уведомления об маркере окна страницы свойств.


```C++
WM_ADSPROP_NOTIFY_PAGEHWND

    WPARAM hPage
    LPARAM ptzTitle
    
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хнотифйобж* 
</dt> <dd>

Маркер объекта уведомления. Чтобы получить этот маркер, вызовите [**адспропкреатенотифйобж**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> <dt>

*хпаже* 
</dt> <dd>

Описатель окна страницы свойств.

</dd> <dt>

*птзтитле* 
</dt> <dd>

Указатель на заканчивающийся нулем буфер **WCHAR** , который содержит заголовок страницы свойств.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не имеет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Расширение страницы свойств Active Directory обычно вызывает функцию [**адспропсесвнд**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) при обработке сообщения [**WM \_ инитдиалог**](../dlgbox/wm-initdialog.md) .

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

[**адспропсесвнд**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd)
</dt> <dt>

[**адспропкреатенотифйобж**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[**WM \_ инитдиалог**](../dlgbox/wm-initdialog.md)
</dt> </dl>

 

