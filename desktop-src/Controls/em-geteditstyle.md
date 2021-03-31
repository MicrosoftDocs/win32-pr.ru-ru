---
title: Сообщение EM_GETEDITSTYLE (RichEdit. h)
description: Извлекает текущие флаги изменения стиля.
ms.assetid: 568e51a4-0767-4a59-bf34-bc0281b5fe65
keywords:
- Элементы управления Windows для EM_GETEDITSTYLE сообщений
topic_type:
- apiref
api_name:
- EM_GETEDITSTYLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9264338ea525cc0165e1ed942d90654b95357b17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071739"
---
# <a name="em_geteditstyle-message"></a>\_Сообщение ЖЕТЕДИТСТИЛЕ EM

Извлекает текущие флаги изменения стиля.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает текущие флаги изменения стиля, которые могут включать одно или несколько из следующих значений:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Код возврата</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>SES_BEEPONMAXTEXT</strong></dt> </dl></td>
<td>Расширенное редактирование вызовет системный звуковой сигнал, если пользователь пытается ввести больше максимального числа символов.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_BIDI</strong></dt> </dl></td>
<td>Включает двунаправленную обработку. Этот параметр автоматически включается с помощью расширенного редактирования, если доступны следующие стили окна: <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RIGHT</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RTLREADING</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_LEFTSCROLLBAR</strong></a>. Однако этот параметр полезен для обработки этих стилей окна при использовании пользовательской реализации <a href="/windows/desktop/api/Textserv/nl-textserv-itexthost"><strong>итекссост</strong></a> (по умолчанию: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_CTFALLOWEMBED</strong></dt> </dl></td>
<td><strong>Windows XP с пакетом обновления 1 (SP1</strong>): разрешить вставку внедренных объектов с помощью TSF (по умолчанию: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_CTFALLOWPROOFING</strong></dt> </dl></td>
<td><strong>Windows XP с пакетом обновления 1 (SP1</strong>): разрешает советы по проверке правописания TSF (по умолчанию: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_CTFALLOWSMARTTAG</strong></dt> </dl></td>
<td><strong>Windows XP с пакетом обновления 1 (SP1</strong>): разрешает советы SMARTTAG для TSF (по умолчанию: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_CTFNOLOCK</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: не разрешать доступ на чтение и запись для блокировки TSF. Это приостанавливает ввод TSF. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_DEFAULTLATINLIGA</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: шрифты с лигатурой типа "Fi" отображаются с функциями OpenType по умолчанию, что приводит к улучшенному оформлению (по умолчанию: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_DRAFTMODE</strong></dt> </dl></td>
<td><strong>Windows XP с пакетом обновления 1 (SP1)</strong>: использовать шрифты режима черновика для вывода текста. Режим черновика является параметром специальных возможностей, в котором элемент управления отображает текст с одним шрифтом. шрифт определяется параметром системы для шрифта, используемого в окнах сообщений. Например, доступные пользователи могут читать текст проще, если он является однородным, а не сочетанием шрифтов и стилей (значение по умолчанию: 0). <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_EMULATE10</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: Эмуляция поведения RichEdit 1,0. <br/>
<blockquote>
[!Note]<br />
Если вы действительно хотите это поведение, используйте riched32.dll Windows вместо riched20.dll или msftedit.dll. Riched32.dll имеет больше функциональных возможностей.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_EMULATESYSEDIT</strong></dt> </dl></td>
<td>Если этот бит включен, широкие возможности редактирования попытаются эмулировать элемент управления "изменение системы" (значение по умолчанию: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_EXTENDBACKCOLOR</strong></dt> </dl></td>
<td>Расширяет цвет фона до границ прямоугольника клиента (по умолчанию: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_HIDEGRIDLINES</strong></dt> </dl></td>
<td><strong>Windows XP с пакетом обновления 1 (SP1)</strong>: Если ширина линий сетки таблицы равна нулю, линии сетки не отображаются. Это эквивалентно функции скрыть сетку в меню таблицы Word (по умолчанию: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_HYPERLINKTOOLTIPS</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: когда курсор наведен на ссылку, отобразится подсказка с адресом целевой ссылки (по умолчанию: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_LOGICALCARET</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: укажите логическую информацию о курсоре вместо точечного рисунка курсора, как описано в <a href="/windows/desktop/api/Textserv/nf-textserv-itexthost-txsetcaretpos"><strong>Итекссост:: ткссеткаретпос</strong></a> (по умолчанию: 0). <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_LOWERCASE</strong></dt> </dl></td>
<td>Преобразует все входные символы в нижний регистр (по умолчанию: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_MAPCPS</strong></dt> </dl></td>
<td>Является устаревшей. Не используйте.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_MULTISELECT</strong></dt> </dl></td>
<td><strong>Windows 8</strong>. Включение множественного выбора с индивидуальным выбором мыши при нажатии клавиши Ctrl (значение по умолчанию: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_NOEALINEHEIGHTADJUST</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: не изменять высоту строки для восточно-азиатского текста (по умолчанию: 0, что регулирует высоту линии на 15%). <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_NOFOCUSLINKNOTIFY</strong></dt> </dl></td>
<td>Отправляет <a href="en-link.md">EN_LINK</a> уведомления о ссылках, которые не имеют фокуса.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_NOIME</strong></dt> </dl></td>
<td>Запрещает редакторы IME для данного экземпляра элемента управления Rich Edit (по умолчанию: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_NOINPUTSEQUENCECHK</strong></dt> </dl></td>
<td>Если этот бит включен, то Расширенное редактирование не проверяет последовательность введенного текста. Для некоторых языков (например, тайского и вьетнамского) требуется проверка порядка входных последовательностей перед их отправкой в резервное хранилище (по умолчанию: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_SCROLLONKILLFOCUS</strong></dt> </dl></td>
<td>Когда происходит Киллфокус, прокрутите до начала текста (позиции символа, равной 0) (значение по умолчанию: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_SMARTDRAGDROP</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: Добавление или удаление пробела в соответствии с контекстом при перетаскивании текста (значение по умолчанию: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_USECRLF</strong></dt> </dl></td>
<td>Является устаревшей. Не используйте.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_WORDDRAGDROP</strong></dt> </dl></td>
<td><strong>Windows 8</strong>. Если выбран параметр Word SELECT, убедитесь, что расположение сброса находится на границе слова (по умолчанию: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_UPPERCASE</strong></dt> </dl></td>
<td>Преобразует все входные символы в верхний регистр (по умолчанию: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_USEAIMM</strong></dt> </dl></td>
<td>Использует компонент активного входного метода IMM, поставляемый с Internet Explorer 4,0 или более поздней версии (по умолчанию: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_USEATFONT</strong></dt> </dl></td>
<td><strong>Windows XP с пакетом обновления 1 (SP1)</strong>: использует шрифт @, предназначенный для вертикального текста; Он используется с стилем окна <a href="rich-edit-control-styles.md"><strong>ES_VERTICAL</strong></a> . Имя @ Font начинается с символа @, например &quot; @Batang &quot; (по умолчанию: 0, но автоматически включается для вертикального макета текста). <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_USECTF</strong></dt> </dl></td>
<td><strong>Windows XP с пакетом обновления 1 (SP1)</strong>: включает поддержку TSF. (по умолчанию: 0)<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_XLTCRCRLFTOCR</strong></dt> </dl></td>
<td>Включает перевод Кркрлфс в CR. Если этот бит включен и файл считывается в, все экземпляры КРКРЛФ будут внутренне преобразованы в жесткие запросы CR. Это повлияет на перенос текста. Обратите внимание, что если такой файл сохраняется в виде обычного текста, запросы CR будут заменены символами CRLF. Это стандарт txt для обычного текста (по умолчанию: 0, который удаляет Кркрлфс на входе). <br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Распространяемые компоненты<br/>          | Расширенное редактирование 3,0<br/>                                                              |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**EM \_ сетедитстиле**](em-seteditstyle.md)
</dt> </dl>

 

