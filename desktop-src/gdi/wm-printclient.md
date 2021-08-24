---
description: Сообщение WM \_ принтклиент отправляется в окно для запроса на прорисовку клиентской области в указанном контексте устройства, чаще всего в контексте устройства печати.
ms.assetid: 8703ee74-812a-4ca2-8ee3-a3b8779739e7
title: Сообщение WM_PRINTCLIENT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 807c12ca4d0a5fe5f1e2a12aecd3b3148d936119f72771e811fe85d5b0af3abf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717664"
---
# <a name="wm_printclient-message"></a>\_Сообщение ПРИНТКЛИЕНТ WM

Сообщение **WM \_ принтклиент** отправляется в окно для запроса на прорисовку клиентской области в указанном контексте устройства, чаще всего в контексте устройства печати.

В отличие [**от \_ Printing WM**](wm-print.md), **WM \_ принтклиент** не обрабатывается [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). Для правильного использования окно должно обрабатывать сообщение **WM \_ принтклиент** через определяемую приложением [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) функцию.


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

## <a name="remarks"></a>Remarks

Окно может обрабатывать это сообщение во многом так же, как [**WM \_ Paint**](./wm-paint.md), за исключением того, что [**бегинпаинт**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) и [**ендпаинт**](/windows/desktop/api/Winuser/nf-winuser-endpaint) не нужно вызывать (предоставляется контекст устройства), и окно должно рисовать всю клиентскую область, а не только недействительную область.

Windows, которые могут использоваться в любом месте системы, например элементы управления, должны обрабатывать это сообщение. В других окнах может быть целесообразно обработать это сообщение, так как оно относительно легко реализуется.

Функция [аниматевиндов](/windows/desktop/api/winuser/nf-winuser-animatewindow) требует, чтобы анимированное окно реализовало сообщение **WM \_ принтклиент** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о рисовании и рисовании](painting-and-drawing.md)
</dt> <dt>

[Рисование и рисование сообщений](painting-and-drawing-messages.md)
</dt> <dt>

[**аниматевиндов**](/windows/win32/api/winuser/nf-winuser-animatewindow)
</dt> <dt>

[**бегинпаинт**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
</dt> <dt>

[**ендпаинт**](/windows/desktop/api/Winuser/nf-winuser-endpaint)
</dt> <dt>

[**WM \_ Paint**](wm-paint.md)
</dt> </dl>

 

 
