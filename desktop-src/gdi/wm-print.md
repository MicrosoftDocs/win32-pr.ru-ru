---
description: Сообщение WM \_ Print отправляется в окно, чтобы запрашивать, что оно рисуется в указанном контексте устройства, чаще всего в контексте устройства печати.
ms.assetid: e6be2ecd-603a-405f-8a48-68d971e1f6de
title: Сообщение WM_PRINT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a012d26e4357a639a7eb8d7930937a06a991124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080645"
---
# <a name="wm_print-message"></a>\_Сообщение для печати WM

Сообщение **WM \_ Print** отправляется в окно, чтобы запрашивать, что оно рисуется в указанном контексте устройства, чаще всего в контексте устройства печати.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Маркер контекста устройства для рисования в.

</dd> <dt>

*lParam* 
</dt> <dd>

Параметры рисования. Этот параметр может принимать одно или несколько следующих значений.



| Значение                                                                                                                                                                  | Значение                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="PRF_CHECKVISIBLE"></span><span id="prf_checkvisible"></span><dl> <dt>**PRF \_ чекквисибле**</dt> </dl> | Отображает окно только в том случае, если оно видимо.<br/>          |
| <span id="PRF_CHILDREN"></span><span id="prf_children"></span><dl> <dt>**вложенные \_ элементы PRF**</dt> </dl>             | Рисует все видимые дочерние окна.<br/>              |
| <span id="PRF_CLIENT"></span><span id="prf_client"></span><dl> <dt>**PRF, \_ клиент**</dt> </dl>                   | Рисует клиентскую область окна.<br/>             |
| <span id="PRF_ERASEBKGND"></span><span id="prf_erasebkgnd"></span><dl> <dt>**PRF \_ ерасебкгнд**</dt> </dl>       | Стирает фон перед рисованием окна.<br/> |
| <span id="PRF_NONCLIENT"></span><span id="prf_nonclient"></span><dl> <dt>**PRF не \_ клиент**</dt> </dl>          | Рисует неклиентскую область окна.<br/>          |
| <span id="PRF_OWNED"></span><span id="prf_owned"></span><dl> <dt>**\_владелец PRF**</dt> </dl>                      | Рисует все собственные окна.<br/>                         |



 

</dd> </dl>

## <a name="remarks"></a>Примечания

Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) обрабатывает это сообщение в зависимости от того, какой параметр рисования указан: Если \_ указано PRF чекквисибле, а окно не отображается, ничего не делать, если \_ указан PRF-неклиент, нарисуйте неклиентскую область в указанном контексте устройства, если \_ указан PRF-ерасебкгнд, отправите окну сообщение [**\_ ерасебкгнд WM**](../winmsg/wm-erasebkgnd.md) , если \_ указан PRF-клиент, отправьте окно в [**сообщение \_ принтклиент WM**](wm-printclient.md) , если \_ заданы потомки PRF, отправьте каждое видимое дочернее окно в сообщение WM Print Message, если **\_** \_ задано значение "владеет" **. \_**

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о рисовании и рисовании](painting-and-drawing.md)
</dt> <dt>

[Рисование и рисование сообщений](painting-and-drawing-messages.md)
</dt> <dt>

[**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ ерасебкгнд**](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[**WM \_ принтклиент**](wm-printclient.md)
</dt> </dl>

 

 
