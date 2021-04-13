---
title: Код уведомления EN_LINK (RichEdit. h)
description: Форматированный элемент управления "поле ввода" отправляет \_ коды уведомлений о ссылках на короткое время при получении различных сообщений, например, когда пользователь нажимает кнопку мыши или когда указатель мыши находится над текстом, имеющим \_ результат CFE.
ms.assetid: 67f02908-957e-4d91-8a70-70399ce9cf2e
keywords:
- EN_LINK кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_LINK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec0eeb134804f671502d4cd3abbe2cb6995194af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492447"
---
# <a name="en_link-notification-code"></a>\_Код уведомления о ссылке EN

Форматированный элемент управления "поле ввода" отправляет \_ коды уведомлений о ссылках на короткое время при получении различных сообщений, например, когда пользователь нажимает кнопку мыши или когда указатель мыши находится над текстом, имеющим результат **CFE \_** . Безоконный элемент управления "поле ввода" не отправляет это уведомление с помощью метода [**итекссост:: ткснотифи**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) . Родительское окно элемента управления получает этот код уведомления через сообщение [**\_ уведомления WM**](wm-notify.md) .


```C++
EN_LINK

    penLink = (ENLINK *) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

ИДЕНТИФИКАТОР окна, полученный путем вызова функции [**жетвиндовлонг**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) со \_ значением идентификатора ГВЛ.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**енлинк**](/windows/desktop/api/Richedit/ns-richedit-enlink) . Структура содержит структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , сведения о коде уведомления и структуру [**чарранже**](/windows/desktop/api/Richedit/ns-richedit-charrange) , которая указывает диапазон символов, имеющих результат **\_ связи CFE** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ноль, чтобы разрешить элементу управления продолжать нормальную обработку сообщения.

Возврат ненулевого значения для предотвращения обработки сообщения элементом управления.

**Windows 8**: возврат **\_ ссылки en \_ \_ по умолчанию используется** для направления элемента управления Rich Edit для выполнения действия по умолчанию.

## <a name="remarks"></a>Комментарии

Чтобы получать коды уведомлений по **\_ ссылке** , если ссылка имеет фокус, укажите флаг [**\_ ссылки енм**](rich-edit-control-event-mask-flags.md) в маске, отправленной с сообщением [**EM \_ SETEVENTMASK**](em-seteventmask.md) .

Если ссылка не имеет фокуса, для получения кодов уведомлений по **короткой \_ ссылке** укажите флаг **SES \_ нофокуслинкнотифи** в маске, отправляемой с сообщением [**\_ сетедитстиле EM**](em-seteditstyle.md) .

Форматированный элемент управления "поле ввода" отправляет коды уведомления о **\_ ссылке** , когда он получает следующие сообщения, когда указатель мыши находится над текстом, имеющим результат **CFE \_ Link** :

-   [**WM \_ лбуттондблклк**](/windows/desktop/inputdev/wm-lbuttondblclk)
-   [**WM \_ лбуттондовн**](/windows/desktop/inputdev/wm-lbuttondown)
-   [**WM \_ лбуттонуп**](/windows/desktop/inputdev/wm-lbuttonup)
-   [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)
-   [**WM \_ рбуттондблклк**](/windows/desktop/inputdev/wm-rbuttondblclk)
-   [**WM \_ рбуттондовн**](/windows/desktop/inputdev/wm-rbuttondown)
-   [**WM \_ рбуттонуп**](/windows/desktop/inputdev/wm-rbuttonup)
-   [**WM \_ сеткурсор**](/windows/desktop/menurc/wm-setcursor)

Как правило, **CFE \_ ссылка** определяет диапазон текста, который содержит URL-адрес. Приложения могут управлять \_ кодом уведомления о ссылке, изменяя указатель мыши, когда он находится над URL-адресом, или запустив браузер для просмотра расположения, определенного URL-адресом.

Если вы отправляете сообщение [**EM \_ аутаурлдетект**](em-autourldetect.md) для включения автоматического обнаружения URL-адресов, элемент управления Rich Editing автоматически **устанавливает для измененного текста значение, \_** которое он идентифицирует как URL-адрес.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**чарранже**](/windows/desktop/api/Richedit/ns-richedit-charrange)
</dt> <dt>

[**EM \_ аутаурлдетект**](em-autourldetect.md)
</dt> <dt>

[**енлинк**](/windows/desktop/api/Richedit/ns-richedit-enlink)
</dt> <dt>

[**ITextRange2:: SetURL**](/windows/desktop/api/Tom/nf-tom-itextrange2-seturl)
</dt> <dt>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> </dl>

 

