---
title: Сообщение WM_DSA_SHEET_CLOSE_NOTIFY
description: Отправляется в оснастку консоли управления Active Directory MMC при удалении дополнительной страницы свойств.
ms.assetid: 74271550-e1f7-4576-a04f-52d5b7c619cb
ms.tgt_platform: multiple
keywords:
- Сообщение WM_DSA_SHEET_CLOSE_NOTIFY Active Directory
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CLOSE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f840790de51ce712b33fc9a9611934e8be9a76a35a0fc01a4ce0abe4ba040d2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181677"
---
# <a name="wm_dsa_sheet_close_notify-message"></a>\_ \_ \_ Сообщение о закрытии страницы WM DSA \_

При удалении дополнительной страницы свойств в оснастке консоли управления Active Directory MMC отправляется сообщение об ошибке **\_ Close (закрыть) \_ листа \_ \_ WM DSA** .

> [!Note]  
> Это значение сообщения не определено в опубликованном файле заголовка. Чтобы использовать это значение сообщения, необходимо определить его самостоятельно в указанном формате.

 


```C++
#define WM_DSA_SHEET_CLOSE_NOTIFY (WM_USER + 5)
```




```C++
LRESULT SendMessage( (HWND)   hwnd, 
                     (UINT)   WM_DSA_SHEET_CLOSE_NOTIFY,
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

Содержит определяемое приложением 32-разрядное значение. Это значение берется из элемента **впарамшитклосе** структуры [**пропшиткфг**](propsheetcfg.md) .

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение для этого сообщения не используется.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**пропшиткфг**](propsheetcfg.md)
</dt> </dl>

 

 





