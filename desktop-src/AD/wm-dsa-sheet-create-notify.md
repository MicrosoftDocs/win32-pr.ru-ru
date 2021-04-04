---
title: Сообщение WM_DSA_SHEET_CREATE_NOTIFY
description: Опубликовано в оснастке консоли управления Active Directory MMC для создания дополнительной страницы свойств.
ms.assetid: 878878bf-fb78-4669-b282-1dd3349f35d5
ms.tgt_platform: multiple
keywords:
- Сообщение WM_DSA_SHEET_CREATE_NOTIFY Active Directory
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CREATE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77f08424e7b39449861ec654f1ff7891c6e9c60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988733"
---
# <a name="wm_dsa_sheet_create_notify-message"></a>\_ \_ \_ \_ Сообщение об ошибке создания уведомления для листа WM DSA

В оснастке консоли управления Active Directory MMC для создания дополнительной страницы свойств отправляется сообщение **\_ \_ \_ \_ уведомления о создании сообщения об ошибке WM DSA** .

> [!Note]  
> Это значение сообщения не определено в опубликованном файле заголовка. Чтобы использовать это значение сообщения, определите его в точно указанном формате.

 


```C++
#define WM_DSA_SHEET_CREATE_NOTIFY (WM_USER + 6)
LRESULT SendMessage(
    (HWND) hwnd, 
    WM_DSA_SHEET_CREATE_NOTIFY,
    (WPARAM) wParam, 
    (LPARAM) lParam);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*HWND* 
</dt> <dd>

Обработчик окна оснастки, который будет обрабатывать это сообщение. Этот маркер получается из элемента **хвндхидден** структуры [**пропшиткфг**](propsheetcfg.md) .

</dd> <dt>

*wParam* 
</dt> <dd>

Содержит указатель на структуру [**\_ \_ \_ сведений о странице DSA sec**](dsa-sec-page-info.md) , которая определяет создаваемую дополнительную страницу свойств. Получатель сообщений должен освободить эту память с помощью функции [**функции LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) , если она больше не нужна.

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Не используется.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**пропшиткфг**](propsheetcfg.md)
</dt> <dt>

[**\_ \_ сведения о странице DSA sec \_**](dsa-sec-page-info.md)
</dt> <dt>

[**Функции LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 

