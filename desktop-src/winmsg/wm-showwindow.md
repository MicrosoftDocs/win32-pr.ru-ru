---
description: Посылается окну, когда окно будет скрыто или показано.
ms.assetid: dea7c9aa-eba7-4b93-a4c5-9b2d36999780
title: Сообщение WM_SHOWWINDOW (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbca6cbb4c73ff1cad31754b1b581e0c892970e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345572"
---
# <a name="wm_showwindow-message"></a>\_Сообщение об ошибке WM SHOWWINDOW

Посылается окну, когда окно будет скрыто или показано.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_SHOWWINDOW                   0x0018
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Указывает, отображается ли окно. Если параметр *wParam* имеет **значение true**, окно отображается. Если параметр *wParam* имеет **значение false**, окно скрывается.

</dd> <dt>

*lParam* 
</dt> <dd>

Состояние отображаемого окна. Если параметр *lParam* равен нулю, сообщение было отправлено из-за вызова функции [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) ; в противном случае *lParam* имеет одно из следующих значений.



| Значение                                                                                                                                                                                                                         | Значение                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="SW_OTHERUNZOOM"></span><span id="sw_otherunzoom"></span><dl> <dt>**SW \_ ОСЕРУНЗУМ**</dt> <dt>4</dt> </dl>       | Выполняется обнаружение окна, так как окно развертывания было восстановлено или уменьшено.<br/> |
| <span id="SW_OTHERZOOM"></span><span id="sw_otherzoom"></span><dl> <dt>**SW \_ ОСЕРЗУМ**</dt> <dt>2</dt> </dl>             | Окно охватывается другим окном, которое было развернуто.<br/>             |
| <span id="SW_PARENTCLOSING"></span><span id="sw_parentclosing"></span><dl> <dt>**SW \_ ПАРЕНТКЛОСИНГ**</dt> <dt>1</dt> </dl> | Окно-владелец окна свернется.<br/>                                      |
| <span id="SW_PARENTOPENING"></span><span id="sw_parentopening"></span><dl> <dt>**SW \_ ПАРЕНТОПЕНИНГ**</dt> <dt>3</dt> </dl> | Окно-владелец окна восстанавливается.<br/>                                       |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **lResult**

Если приложение обрабатывает это сообщение, оно должно вернуть ноль.

## <a name="remarks"></a>Комментарии

Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) скрывает или отображает окно, как указано в сообщении. Если окно имеет стиль " [**WS \_ Visible**](window-styles.md) " при его создании, окно получает это сообщение после его создания, но до его отображения. Окно также получает это сообщение, когда состояние видимости изменяется функцией [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) или [**шововнедпопупс**](/windows/win32/api/winuser/nf-winuser-showownedpopups) .

Сообщение об ошибке **WM \_ SHOWWINDOW** не отправляется в следующих случаях:

-   При создании перекрывающегося окна верхнего уровня с помощью стиля [**WS \_ Maximize**](window-styles.md) или **WS \_ Minimize** .
-   При указании флага **SW \_ шовнормал** в вызове функции [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**шововнедпопупс**](/windows/win32/api/winuser/nf-winuser-showownedpopups)
</dt> <dt>

[**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow)
</dt> <dt>

**Зрения**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
