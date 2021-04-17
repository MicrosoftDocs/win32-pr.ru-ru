---
title: Сообщение WM_ADSPROP_SHEET_CREATE
description: Отправляется в объект уведомления для создания дополнительной страницы свойств в оснастке консоли управления Active Directory MMC.
ms.assetid: 3efa25f2-cd39-44f8-952e-203f1519ce2c
ms.tgt_platform: multiple
keywords:
- Сообщение WM_ADSPROP_SHEET_CREATE Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_SHEET_CREATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b540ffd87d4350a323577ff5fa317e94f9271f2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534223"
---
# <a name="wm_adsprop_sheet_create-message"></a>\_Сообщение о \_ создании листа WM адспроп \_

Сообщение **о \_ \_ \_ создании адспроп листа WM** отправляется в объект уведомления для создания дополнительной страницы свойств в оснастке консоли управления (MMC) Active Directory.

> [!Note]  
> Это значение сообщения не определено в опубликованном файле заголовка. Чтобы использовать это значение сообщения, необходимо определить его самостоятельно в указанном формате.

 


```C++
#define WM_ADSPROP_SHEET_CREATE (WM_USER + 1108)
LRESULT SendMessage( (HWND)   hwnd, 
                     (UINT)   WM_ADSPROP_SHEET_CREATE,
                     (WPARAM) wParam, 
                     (LPARAM) lParam);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*HWND* 
</dt> <dd>

Маркер объекта уведомления. Чтобы получить этот маркер, вызовите [**адспропкреатенотифйобж**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> <dt>

*wParam* 
</dt> <dd>

Содержит указатель на структуру [**\_ \_ \_ сведений о странице DSA sec**](dsa-sec-page-info.md) , которая определяет создаваемую вторичную страницу. Только одну вторичную страницу свойств можно создать с сообщением **\_ \_ \_ CREATE адспроп листа WM** , поэтому структура [**Дсобжектнамес**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) может содержать только одну структуру [**дсобжект**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) .

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется. Должен иметь **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение для этого сообщения всегда равно нулю.

## <a name="remarks"></a>Комментарии

Вызывающий объект должен выделить [**структуру \_ \_ \_ сведений о странице DSA sec**](dsa-sec-page-info.md) , строку заголовка и все строки [**Дсобжект**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) , используя один вызов функции [**локалаллок**](/windows/desktop/api/winbase/nf-winbase-localalloc) . Сообщение **о \_ \_ \_ создании адспроп листа WM** — это асинхронное сообщение, поэтому оно будет возвращаться перед созданием дополнительного листа. По этой причине память должна остаться неизменной после возвращения сообщения. Получатель освободит эту память с помощью одного вызова функции [**функции LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) после создания дополнительного листа.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ПАРЕНСВНД кфстр DS \_**](cfstr-ds-parenthwnd.md)
</dt> <dt>

[**\_ \_ сведения о странице DSA sec \_**](dsa-sec-page-info.md)
</dt> <dt>

[**дсобжектнамес**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[**дсобжект**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> <dt>

[**локалаллок**](/windows/desktop/api/winbase/nf-winbase-localalloc)
</dt> <dt>

[**Функции LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 

