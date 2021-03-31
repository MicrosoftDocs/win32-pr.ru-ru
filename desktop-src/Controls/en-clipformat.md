---
title: Код уведомления EN_CLIPFORMAT (RichEdit. h)
description: Сообщает родительскому окну элемента управления Rich Edit, что вставка выполнялась с определенным форматом буфера обмена. Безоконный элемент управления "поле ввода" отправляет это уведомление с помощью метода Ткснотифи Итекссост.
ms.assetid: 79FE1350-4D45-447B-B705-63E966AC7F0E
keywords:
- EN_CLIPFORMAT кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_CLIPFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0430e8a4dba0b1a18f81f4e28ec67f2c93551cd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988481"
---
# <a name="en_clipformat-notification-code"></a>\_Код уведомления EN клипформат

Сообщает родительскому окну элемента управления Rich Edit, что вставка выполнялась с определенным форматом буфера обмена. Безоконный элемент управления "поле ввода" не отправляет это уведомление с помощью метода [**итекссост:: ткснотифи**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) .


```C++
EN_CLIPFORMAT

      pClipboardFmt = (CLIPBOARDFORMAT *) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

ИДЕНТИФИКАТОР окна, полученный путем вызова функции [**жетвиндовлонг**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) со \_ значением идентификатора ГВЛ.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**клипбоардформат**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat) , содержащую сведения о формате буфера обмена.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение игнорируется.

## <a name="remarks"></a>Комментарии

Чтобы получить \_ коды уведомлений EN клипформат, укажите [**енм \_ клипформат**](rich-edit-control-event-mask-flags.md) в маске, отправляемой с сообщением [**EM \_ SETEVENTMASK**](em-seteventmask.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**клипбоардформат**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat)
</dt> </dl>

 

