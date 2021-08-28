---
title: Сообщение WM_SYSCOMMAND (Winuser. h)
description: Окно получает это сообщение, когда пользователь выбирает команду из меню «окно» (прежнее название — система или меню «Управление») или когда пользователь нажимает кнопку развернуть, кнопку сворачивания, кнопку восстановить или кнопку Закрыть.
ms.assetid: 82c7cc95-82d5-4f0f-8c78-ab325561b04e
keywords:
- WM_SYSCOMMAND меню сообщений и других ресурсов
topic_type:
- apiref
api_name:
- WM_SYSCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 5458a9acfa6c166764b47a2d49a5ddcc181e38ee
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482180"
---
# <a name="wm_syscommand-message"></a>\_Сообщение СИСКОММАНД WM

Окно получает это сообщение, когда пользователь выбирает команду из меню « **окно»** (прежнее название — система или меню «Управление») или когда пользователь нажимает кнопку развернуть, кнопку сворачивания, кнопку восстановить или кнопку Закрыть.


```C++
#define WM_SYSCOMMAND                   0x0112
```

## <a name="example"></a>Пример

```cpp
 case WM_SYSCOMMAND:
        if (wParam == SC_CLOSE)
        {
            EndDialog (hDlg, TRUE);
            return(TRUE);
        }
        break;

```
пример из [Windows классических примеров](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/registry/RegExplorer.c) на GitHub.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Тип запрашиваемой системной команды. Этот параметр может принимать одно из указанных ниже значений.




| Значение | Значение | 
|-------|---------|
| <span id="SC_CLOSE"></span><span id="sc_close"></span><dl><dt><strong>SC_CLOSE</strong></dt><dt>0xF060</dt></dl> | Закрывает окно.<br /> | 
| <span id="SC_CONTEXTHELP"></span><span id="sc_contexthelp"></span><dl><dt><strong>SC_CONTEXTHELP</strong></dt><dt>0xF180</dt></dl> | Изменяет курсор на вопросительный знак с помощью указателя. Если пользователь щелкает элемент управления в диалоговом окне, элемент управления получает <a href="/windows/desktop/shell/wm-help"><strong>WM_HELP</strong></a> сообщение.<br /> | 
| <span id="SC_DEFAULT"></span><span id="sc_default"></span><dl><dt><strong>SC_DEFAULT</strong></dt><dt>0xF160</dt></dl> | Выбирает элемент по умолчанию; пользователь дважды щелкнул меню окно.<br /> | 
| <span id="SC_HOTKEY"></span><span id="sc_hotkey"></span><dl><dt><strong>SC_HOTKEY</strong></dt><dt>0xF150</dt></dl> | Активирует окно, связанное с заданной приложением горячей клавишей. Параметр <em>lParam</em> определяет окно для активации.<br /> | 
| <span id="SC_HSCROLL"></span><span id="sc_hscroll"></span><dl><dt><strong>SC_HSCROLL</strong></dt><dt>0xF080</dt></dl> | Выполняет прокрутку по горизонтали.<br /> | 
| <span id="SCF_ISSECURE"></span><span id="scf_issecure"></span><dl><dt><strong>SCF_ISSECURE</strong></dt><dt>0x00000001</dt></dl> | Указывает, является ли экранная заставка безопасной. <br /> | 
| <span id="SC_KEYMENU"></span><span id="sc_keymenu"></span><dl><dt><strong>SC_KEYMENU</strong></dt><dt>0xF100</dt></dl> | Извлекает меню окна в результате нажатия клавиши. Дополнительные сведения см. в разделе "Замечания".<br /> | 
| <span id="SC_MAXIMIZE"></span><span id="sc_maximize"></span><dl><dt><strong>SC_MAXIMIZE</strong></dt><dt>0xF030</dt></dl> | Разворачивает окно.<br /> | 
| <span id="SC_MINIMIZE"></span><span id="sc_minimize"></span><dl><dt><strong>SC_MINIMIZE</strong></dt><dt>0xF020</dt></dl> | Сворачивает окно.<br /> | 
| <span id="SC_MONITORPOWER"></span><span id="sc_monitorpower"></span><dl><dt><strong>SC_MONITORPOWER</strong></dt><dt>0xF170</dt></dl> | Задает состояние отображения. Эта команда поддерживает устройства с функциями энергосбережения, такими как персональный компьютер с питанием от аккумулятора. <br /> Параметр <em>lParam</em> может иметь следующие значения:<br /><ul><li>-1 (при включении дисплея)</li><li>1 (дисплей переходит в низкую степень)</li><li>2 (отображение завершается)</li></ul> | 
| <span id="SC_MOUSEMENU"></span><span id="sc_mousemenu"></span><dl><dt><strong>SC_MOUSEMENU</strong></dt><dt>0xF090</dt></dl> | Извлекает меню окна в результате щелчка мышью.<br /> | 
| <span id="SC_MOVE"></span><span id="sc_move"></span><dl><dt><strong>SC_MOVE</strong></dt><dt>0xF010</dt></dl> | Перемещает окно.<br /> | 
| <span id="SC_NEXTWINDOW"></span><span id="sc_nextwindow"></span><dl><dt><strong>SC_NEXTWINDOW</strong></dt><dt>0xF040</dt></dl> | Переход к следующему окну.<br /> | 
| <span id="SC_PREVWINDOW"></span><span id="sc_prevwindow"></span><dl><dt><strong>SC_PREVWINDOW</strong></dt><dt>0xF050</dt></dl> | Переход к предыдущему окну.<br /> | 
| <span id="SC_RESTORE"></span><span id="sc_restore"></span><dl><dt><strong>SC_RESTORE</strong></dt><dt>0xF120</dt></dl> | Восстанавливает нормальное расположение и размер окна.<br /> | 
| <span id="SC_SCREENSAVE"></span><span id="sc_screensave"></span><dl><dt><strong>SC_SCREENSAVE</strong></dt><dt>0xF140</dt></dl> | Выполняет приложение экранной заставки, указанное в разделе [boot] файла System.ini.<br /> | 
| <span id="SC_SIZE"></span><span id="sc_size"></span><dl><dt><strong>SC_SIZE</strong></dt><dt>число 0xF000 не</dt></dl> | Изменяет размер окна.<br /> | 
| <span id="SC_TASKLIST"></span><span id="sc_tasklist"></span><dl><dt><strong>SC_TASKLIST</strong></dt><dt>0xF130</dt></dl> | Активирует меню " <strong>Пуск</strong> ".<br /> | 
| <span id="SC_VSCROLL"></span><span id="sc_vscroll"></span><dl><dt><strong>SC_VSCROLL</strong></dt><dt>0xF070</dt></dl> | Прокрутка по вертикали.<br /> | 




 

</dd> <dt>

*lParam* 
</dt> <dd>

Слово нижнего порядка задает горизонтальное расположение курсора в экранных координатах, если команда меню окна выбрана с мышью. В противном случае этот параметр не используется.

Слово в высоком порядке указывает вертикальное расположение курсора в экранных координатах, если команда меню окна выбрана с мышью. Этот параметр равен 1, если команда выбрана с помощью системного ускорителя, или нуль при использовании назначенной клавиши.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Приложение должно вернуть нуль, если оно обрабатывает это сообщение.

## <a name="remarks"></a>Комментарии

Чтобы получить координаты положения в координатах экрана, используйте следующий код:


```
xPos = GET_X_LPARAM(lParam);    // horizontal position 
yPos = GET_Y_LPARAM(lParam);    // vertical position
```



Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) выполняет запрос меню окна для предопределенных действий, указанных в предыдущей таблице.

В сообщениях **WM \_ сискомманд** четыре младшие биты параметра *wParam* используются системой внутри системы. Чтобы получить правильный результат при проверке значения *wParam*, приложение должно объединить значение 0xFFF0 с значением *wParam* с помощью побитового оператора и.

Пункты меню в меню окно можно изменить с помощью функций [**жетсистеммену**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu), [**аппендмену**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**инсертмену**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), [**модифимену**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**инсертменуитем**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema)и [**сетменуитеминфо**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) . Приложения, изменяющие меню окна, должны обрабатывать сообщения **WM \_ сискомманд** .

Приложение может выполнять любую системную команду в любое время, передавая сообщение **WM \_ Сискомманд** в [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). Все сообщения **WM \_ сискомманд** , не обрабатываемые приложением, должны передаваться в **дефвиндовпрок**. Все значения команд, добавленные приложением, должны обрабатываться приложением и не могут быть переданы в **дефвиндовпрок**.

Если защита паролем включена политикой, экранная заставка запускается независимо от того, какое действие выполняет приложение с уведомлением **SC \_ скринсаве** , даже если оно не передается в [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

Сочетания клавиш, определенные для выбора элементов из меню "окно", преобразуются в сообщения **WM \_ сискомманд** . все остальные сочетания клавиш переводятся в [**\_ Командные сообщения WM**](wm-command.md) .

Если параметр *wParam* имеет значение **SC \_ кэймену**, то параметр *lParam* содержит код символа ключа, который используется с клавишей Alt для вывода всплывающего меню. Например, если нажать клавиши ALT + F, чтобы отобразить всплывающее окно файла **, \_ сискомманд WM** с параметром *wParam* , равным **SC \_ кэймену** и *lParam* , равным "F".

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**аппендмену**](/windows/desktop/api/Winuser/nf-winuser-appendmenua)
</dt> <dt>

[**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**ПОЛУЧИТЬ \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**ПОЛУЧИТЬ \_ lParam для Y \_**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**жетсистеммену**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu)
</dt> <dt>

[**инсертмену**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)
</dt> <dt>

[**модифимену**](/windows/desktop/api/Winuser/nf-winuser-modifymenua)
</dt> <dt>

[**\_команда WM**](wm-command.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Сочетания клавиш](keyboard-accelerators.md)
</dt> </dl>

