---
title: 'Сообщения кнопки '
description: Кнопка может отправить сообщения в свое родительское окно, а родительское окно может посылать сообщения кнопке.
ms.assetid: 2d2358fb-b17d-48a9-8def-15ae8bad9162
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136310a3718f17900f604287bf78186f7c927259
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625720"
---
# <a name="button-messages"></a>Сообщения кнопки 

Кнопка может отправить сообщения в свое родительское окно, а родительское окно может посылать сообщения кнопке.

В этом разделе рассматриваются следующие темы.

-   [Отправка сообщений на кнопки](#sending-messages-to-buttons)
-   [Обработка сообщений с помощью кнопки](#handling-messages-from-a-button)
-   [Сообщения с уведомлениями от кнопок](#notification-messages-from-buttons)
-   [Цветовые сообщения для кнопок](#button-color-messages)
-   [Обработка сообщений по умолчанию для кнопки](#button-default-message-processing)
-   [Связанные темы](#related-topics)

## <a name="sending-messages-to-buttons"></a>Отправка сообщений на кнопки

Родительское окно может отсылать сообщения кнопке в перекрытом или дочернем окне с помощью функции [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) , а также передавать сообщения кнопке в диалоговом окне с помощью функций [**сенддлгитеммессаже**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea), [**чеккдлгбуттон**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton), [**чеккрадиобуттон**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton)и [**исдлгбуттончеккед**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) .

Приложение может использовать сообщение [**BM- \_ Check**](bm-getcheck.md) для получения состояния флажка или переключателя. Приложение может также использовать сообщение [**BM- \_ State**](bm-getstate.md) для получения текущих состояний кнопки (состояние проверки, состояние отправки и состояние фокусировки). Чтобы получить сведения о конкретном состоянии, используйте битовую маску в возвращенном значении состояния.

Сообщение [**BM \_ сетчекк**](bm-setcheck.md) устанавливает состояние флажка или переключателя; сообщение возвращает ноль. Сообщение [**BM \_ SETSTATE**](bm-setstate.md) устанавливает состояние принудительной отправки кнопки; это сообщение также возвращает ноль. Сообщение [**BM \_ SETSTYLE**](bm-setstyle.md) изменяет стиль кнопки. Он предназначен для изменения стилей кнопок в типе (например, при изменении флажка на автоматический флажок). Он не предназначен для изменения типов (например, изменения флажка для переключателя). Приложение не должно изменять тип кнопки с одного типа на другой.

Кнопка в стиле [**\_ точечный рисунок BS**](button-styles.md) или [**\_ значок BS**](button-styles.md) отображает точечный рисунок или значок, а не текст. Сообщение [**BM \_ сетимаже**](bm-setimage.md) связывает маркер с растровым изображением или значком с помощью кнопки. Сообщение [**BM- \_ Image**](bm-getimage.md) получает маркер для растрового изображения или значка, связанного с кнопкой.

Приложение также может использовать сообщение [**DM \_ жетдефид**](/windows/desktop/dlgbox/dm-getdefid) для получения идентификатора элемента управления "кнопка по умолчанию" в диалоговом окне. Приложение может использовать сообщение [**DM \_ сетдефид**](/windows/desktop/dlgbox/dm-setdefid) для установки кнопки отправки по умолчанию для диалогового окна.

Вызов функции [**чеккдлгбуттон**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton) или [**чеккрадиобуттон**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton) эквивалентен отправке сообщения [**BM \_ сетчекк**](bm-setcheck.md) . Вызов функции [**исдлгбуттончеккед**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) эквивалентен отправке сообщения [**BM- \_ Check**](bm-getcheck.md) .

## <a name="handling-messages-from-a-button"></a>Обработка сообщений с помощью кнопки

Уведомления из кнопки отправляются в виде [**\_ команды WM**](/windows/desktop/menurc/wm-command) или [**\_ уведомления WM notify**](wm-notify.md) . Сведения об используемом сообщении можно найти на справочной странице для каждого уведомления.

Дополнительные сведения об обработке сообщений см. в разделе [Управление сообщениями](control-messages.md). См. также сообщения кнопки.

## <a name="notification-messages-from-buttons"></a>Сообщения с уведомлениями от кнопок

Когда пользователь нажимает кнопку, ее состояние изменяется, а кнопка отправляет коды уведомлений в виде [**\_ командных сообщений WM**](/windows/desktop/menurc/wm-command) в родительское окно. Например, элемент управления "Кнопка отправки" отправляет [млрд долл \_ щелчком](bn-clicked.md) код уведомления каждый раз, когда пользователь нажимает кнопку. Во всех случаях (за исключением служб [BCN \_ хотитемчанже](bcn-hotitemchange.md)) слово с низким порядком в параметре *wParam* содержит идентификатор элемента управления, а слово с высоким порядком *wParam* содержит код уведомления, а параметр *lParam* содержит управляющий маркер окна.

Как сообщение, так и ответ родительского окна зависят от типа, стиля и текущего состояния кнопки. Ниже приведены коды уведомлений для кнопок, которые должны отслеживать и обрабатываться приложением.



| Код уведомления                                                        | Описание:                                            |
|--------------------------------------------------------------------------|--------------------------------------------------------|
| [\_ХОТИТЕМЧАНЖЕ BCN](bcn-hotitemchange.md)                              | Мышь, которая была нажата или оставлена в клиентской области кнопки. |
| [\_щелчок млрд долл](bn-clicked.md)                                            | Пользователь щелкнул кнопку.                             |
| [Млрд долл \_ ДБЛКЛК](bn-dblclk.md) или [млрд долл \_ даублекликкед](bn-doubleclicked.md) | Пользователь дважды щелкнул кнопку.                      |
| [\_Отключение млрд долл](bn-disable.md)                                            | Кнопка отключена.                                  |
| [Млрд долл \_ ОТПРАВЛЕНные](bn-pushed.md) или [млрд долл \_ хилите](bn-hilite.md)               | Пользователь отправил кнопку.                              |
| [МЛРД долл \_ киллфокус](bn-killfocus.md)                                        | Кнопка потеряла фокус клавиатуры.                    |
| [МЛРД долл \_ Заливка](bn-paint.md)                                                | Кнопка должна быть окрашена.                          |
| [МЛРД долл \_ SETFOCUS](bn-setfocus.md)                                          | Кнопка получила фокус клавиатуры.                  |
| [Млрд долл \_ Unpushd](bn-unpushed.md) или [млрд долл \_ унхилите](bn-unhilite.md)       | Кнопка больше не помещается.                        |



 

Кнопка отправляет [млрд долл \_ Disable](bn-disable.md), [млрд долл \_](bn-pushed.md) [ \_ pushd](bn-unpushed.md) , [млрд долл \_ киллфокус](bn-killfocus.md), [млрд долл \_ Paint](bn-paint.md), [млрд долл \_ SETFOCUS](bn-setfocus.md)и млрд долл неотправленные коды уведомлений только в том случае, если у него есть стиль [**\_ уведомления BS**](button-styles.md) . [Млрд долл \_](bn-dblclk.md) Коды уведомлений дблклк отправляются автоматически для кнопок [**BS \_ усербуттон**](button-styles.md), [**BS \_**](button-styles.md)и [**BS \_ овнердрав**](button-styles.md) . Другие типы кнопок отправляют млрд долл \_ дблклк только в том случае, если они имеют стиль " **BS \_** ". Все кнопки отправляют [млрд долл \_ нажатый](bn-clicked.md) код уведомления, независимо от стилей их кнопок.

Для автоматических кнопок система изменяет состояние принудительной отправки и закрашивает кнопку. В этом случае приложение обычно обрабатывает только млрд доллные коды уведомлений о [ \_ нажатии](bn-clicked.md) и [млрд долл \_ дблклк](bn-dblclk.md) . Для неавтоматических кнопок приложение обычно отвечает на код уведомления, отправляя сообщение для изменения состояния кнопки. Дополнительные сведения об отправке сообщений кнопкам см. [в разделе Отправка сообщений на кнопки](#sending-messages-to-buttons).

Когда пользователь выбирает рисуемую пользователем кнопку, кнопка отправляет родительское окно сообщение [**WM \_ DRAWITEM**](wm-drawitem.md) , содержащее идентификатор рисуемого элемента управления и сведения о его измерениях и состоянии.

## <a name="button-color-messages"></a>Цветовые сообщения для кнопок

Система предоставляет значения цвета по умолчанию для кнопок. Приложение может получить значения по умолчанию для этих цветов, вызвав функцию [**жетсисколор**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) , или задать значения, вызвав функцию [**сетсисколорс**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) . В следующей таблице показаны значения цвета кнопки по умолчанию.



| Значение               | Цвет элемента                                                                                                            |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| ЦВЕТ \_ бтнфаце      | Лицевая кнопка.                                                                                                              |
| ЦВЕТ \_ бтнхигхлигхт | Выделение области (верхняя и левая границы) кнопки.                                                                       |
| ЦВЕТ \_ бтншадов    | Область тени (Нижняя и правая границы) кнопки.                                                                      |
| ЦВЕТ \_ бтнтекст      | Обычный (несерый) текст в кнопках.                                                                                       |
| ЦВЕТ \_ грайтекст     | Отключенный (серый) текст в кнопках. Этот цвет имеет значение 0, если текущий драйвер экрана не поддерживает сплошной серый цвет. |
| \_окно цвета       | Фон окна.                                                                                                        |
| ЦВЕТ \_ WINDOWFRAME  | Фреймы окна.                                                                                                             |
| ЦВЕТная \_ WINDOWTEXT   | Текст в Windows.                                                                                                           |



 

Однако вызов [**сетсисколорс**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) влияет на все приложения, поэтому не следует вызывать эту функцию для настройки кнопок приложения.

Система отправляет сообщение [**WM \_ ктлколорбтн**](wm-ctlcolorbtn.md) в родительское окно кнопки перед рисованием кнопки. Это сообщение содержит маркер для контекста устройства кнопки и маркер дочернего окна. Родительское окно может использовать эти маркеры для изменения цветов текста и фона кнопки. Однако только рисуемые владельцем кнопки реагируют на родительское окно, обрабатывающее сообщение.

## <a name="button-default-message-processing"></a>Обработка сообщений по умолчанию для кнопки

Процедура окна для стандартного класса элемента управления "Кнопка" выполняет обработку по умолчанию для всех сообщений, которые не обрабатывает процедура элемента управления "Кнопка". Когда процедура управления кнопками возвращает **false** для любого сообщения, предопределенная процедура окна проверяет сообщения и выполняет действия по умолчанию, перечисленные в следующей таблице.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Сообщение</th>
<th>Действие по умолчанию</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="bm-click.md"><strong>BM_CLICK</strong></a></td>
<td>Отправляет кнопке <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> и <a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a> сообщение, а также отправляет родительское окно а <a href="bn-clicked.md">BN_CLICKED</a> код уведомления.</td>
</tr>
<tr class="even">
<td><a href="bm-getcheck.md"><strong>BM_GETCHECK</strong></a></td>
<td>Возвращает состояние проверки кнопки.</td>
</tr>
<tr class="odd">
<td><a href="bm-getimage.md"><strong>BM_GETIMAGE</strong></a></td>
<td>Возвращает маркер для растрового изображения или значка, связанного с кнопкой, или <strong>значение NULL</strong> , если кнопка не имеет точечного рисунка или значка.</td>
</tr>
<tr class="even">
<td><a href="bm-getstate.md"><strong>BM_GETSTATE</strong></a></td>
<td>Возвращает текущее состояние проверки, состояние отправки и состояние фокуса кнопки.</td>
</tr>
<tr class="odd">
<td><a href="bm-setcheck.md"><strong>BM_SETCHECK</strong></a></td>
<td>Задает состояние проверки для всех стилей переключателей и флажков. Если параметр <em>wParam</em> больше нуля для переключателей, то кнопке присваивается стиль <a href="/windows/desktop/winmsg/window-styles"><strong>WS_TABSTOP</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="bm-setimage.md"><strong>BM_SETIMAGE</strong></a></td>
<td>Связывает заданное изображение или маркер значка с кнопкой и возвращает маркер предыдущего точечного рисунка или значка.</td>
</tr>
<tr class="odd">
<td><a href="bm-setstate.md"><strong>BM_SETSTATE</strong></a></td>
<td>Задает состояние принудительной отправки кнопки. Для кнопок, рисуемых владельцем, в родительское окно отправляется <a href="wm-drawitem.md"><strong>WM_DRAWITEM</strong></a> сообщение, если изменилось состояние кнопки.</td>
</tr>
<tr class="even">
<td><a href="bm-setstyle.md"><strong>BM_SETSTYLE</strong></a></td>
<td>Задает стиль кнопки. Если неупорядоченное слово параметра <em>lParam</em> имеет <strong>значение true</strong>, кнопка перерисовывается.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a></td>
<td>Устанавливает флажок или автоматический флажок, когда пользователь нажимает клавиши "плюс" (+) или "равно" (=). Очищает флажок или автоматический флажок, когда пользователь нажимает клавишу "минус" (–).</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a></td>
<td>Закрашивает кнопку.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-erasebkgnd"><strong>WM_ERASEBKGND</strong></a></td>
<td>Стирает фон для рисуемых владельцем кнопок. Фон других кнопок удаляется как часть <a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a> и <a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a> обработки.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/dlgbox/wm-getdlgcode"><strong>WM_GETDLGCODE</strong></a></td>
<td>Возвращает значения, которые указывают тип входных данных, обработанных процедурой кнопки по умолчанию, как показано в следующей таблице. 
<table>
<thead>
<tr class="header">
<th>Стиль кнопки</th>
<th>Возвращаемое значение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="button-styles.md"><strong>BS_AUTOCHECKBOX</strong></a></td>
<td>DLGC_WANTCHARS | DLGC_BUTTON</td>
</tr>
<tr class="even">
<td><a href="button-styles.md"><strong>BS_AUTORADIOBUTTON</strong></a></td>
<td>DLGC_RADIOBUTTON | DLGC_BUTTON</td>
</tr>
<tr class="odd">
<td><a href="button-styles.md"><strong>BS_CHECKBOX</strong></a></td>
<td>DLGC_WANTCHARS | DLGC_BUTTON</td>
</tr>
<tr class="even">
<td><a href="button-styles.md"><strong>BS_DEFPUSHBUTTON</strong></a></td>
<td>DLGC_DEFPUSHBUTTON | DLGC_BUTTON</td>
</tr>
<tr class="odd">
<td><a href="button-styles.md"><strong>BS_GROUPBOX</strong></a></td>
<td>DLGC_STATIC</td>
</tr>
<tr class="even">
<td><a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a></td>
<td>DLGC_UNDEFPUSHBUTTON | DLGC_BUTTON</td>
</tr>
<tr class="odd">
<td><a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a></td>
<td>DLGC_RADIOBUTTON | DLGC_BUTTON</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-getfont"><strong>WM_GETFONT</strong></a></td>
<td>Возвращает маркер текущего шрифта.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-keydown"><strong>WM_KEYDOWN</strong></a></td>
<td>Помещает кнопку, если пользователь нажимает клавишу пробел.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-keyup"><strong>WM_KEYUP</strong></a></td>
<td>Освобождает захват мыши для всех вариантов, кроме клавиши TAB.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-killfocus"><strong>WM_KILLFOCUS</strong></a></td>
<td>Удаляет прямоугольник фокуса с кнопки. Для кнопок push и кнопок по умолчанию прямоугольник фокуса становится недействительным. Если кнопка имеет захват мыши, запись снимается, кнопка не нажата и все состояния отправки удаляются.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-lbuttondblclk"><strong>WM_LBUTTONDBLCLK</strong></a></td>
<td>Отправляет <a href="bn-dblclk.md">BN_DBLCLK</a> код уведомления родительскому окну для переключателей и рисуемых владельцем кнопок. Для других кнопок двойной щелчок обрабатывается как сообщение <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a></td>
<td>Выделяется кнопка, если указатель мыши находится внутри прямоугольника клиента кнопки.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a></td>
<td>Освобождает захват мыши, если кнопка была захвачена мышью.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-mousemove"><strong>WM_MOUSEMOVE</strong></a></td>
<td>Выполняет то же действие, что и <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a>, если кнопка имеет захват мыши. В противном случае никакие действия не выполняются.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-nccreate"><strong>WM_NCCREATE</strong></a></td>
<td>Превращает любую кнопку <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> в кнопку <a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-nchittest"><strong>WM_NCHITTEST</strong></a></td>
<td>Возвращает ХТТРАНСПАРЕНТ, если элемент управления "Кнопка" является полем группы.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a></td>
<td>Рисует кнопку в соответствии со стилем и текущим состоянием.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-setfocus"><strong>WM_SETFOCUS</strong></a></td>
<td>Рисует прямоугольник фокуса на кнопке, чтобы получить фокус. Для переключателей и автоматических переключателей родительскому окну отправляется <a href="bn-clicked.md">BN_CLICKED</a> код уведомления.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-setfont"><strong>WM_SETFONT</strong></a></td>
<td>Задает новый шрифт и при необходимости обновляет окно.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/winmsg/wm-settext"><strong>WM_SETTEXT</strong></a></td>
<td>Задает текст кнопки. В случае поля группы сообщение заполняет существующий текст перед перерисовкой поля группы новым текстом.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-syskeyup"><strong>WM_SYSKEYUP</strong></a></td>
<td>Освобождает захват мыши для всех вариантов, кроме клавиши TAB.</td>
</tr>
</tbody>
</table>



 

Предопределенная процедура окна передает все остальные сообщения функции [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) для обработки по умолчанию.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Управляющие сообщения](control-messages.md)
</dt> </dl>

 

 
