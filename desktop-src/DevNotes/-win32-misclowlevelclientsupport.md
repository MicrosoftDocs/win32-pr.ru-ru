---
description: В этом разделе содержатся сведения об API низкого уровня, используемых инфраструктурой клиента Windows.
ms.assetid: 14a6e970-2032-420e-9930-a15909dbbb97
title: Поддержка прочих Low-Level клиентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11558c9994a9c622f71e803521352d1073e68c05
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895269"
---
# <a name="miscellaneous-low-level-client-support"></a>Поддержка прочих Low-Level клиентов

В этом разделе содержатся сведения об API низкого уровня, используемых инфраструктурой клиента Windows.

### <a name="functions"></a>Функции



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Раздел</th>
<th>Содержимое</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/winbase/nf-winbase-_lclose"><strong>_lclose</strong></a></td>
<td>Функция _lclose закрывает указанный файл, чтобы он больше не был доступен для чтения или записи. Эта функция обеспечивает совместимость с 16-разрядными версиями Windows. Приложения на основе Win32 должны использовать функцию CloseHandle.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winbase/nf-winbase-_lopen"><strong>_lopen</strong></a></td>
<td>Функция _lopen открывает существующий файл и устанавливает указатель файла на начало файла. Эта функция обеспечивает совместимость с 16-разрядными версиями Windows. Приложения на основе Win32 должны использовать функцию CreateFile. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winbase/nf-winbase-_lread"><strong>_lread</strong></a></td>
<td>Функция _lread считывает данные из указанного файла. Эта функция обеспечивает совместимость с 16-разрядными версиями Windows. Приложения на основе Win32 должны использовать функцию ReadFile. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-aredvdcodecsenabled"><strong>аредвдкодексенаблед</strong></a></td>
<td>Возвращает значение, указывающее, включены ли на текущем устройстве кодеки DVD.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-disableprocesswindowsghosting"><strong>дисаблепроцессвиндовсгхостинг</strong></a></td>
<td>Отключает функцию дублирования окна для вызывающего графического пользовательского интерфейса. Несинхронизированные окна — это функция диспетчера Windows, которая позволяет пользователю легко выполнять, перемещать и закрывать главное окно приложения, которое не отвечает.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediacomponentpackageinfo"><strong>жетмедиакомпонентпаккажеинфо</strong></a></td>
<td>Возвращает список свойств для всех кодеков мультимедиа, установленных в системе в соответствии с указанными требованиями.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediaextensioncommunicationfactory"><strong>жетмедиаекстенсионкоммуникатионфактори</strong></a></td>
<td>Создает фабрику связи для регистрации расширения мультимедиа.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-instantiatecomponentfrompackage"><strong>инстантиатекомпонентфромпаккаже</strong></a></td>
<td>Создает экземпляр класса в пакете приложения. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-ismediabehaviorenabled"><strong>исмедиабехавиоренаблед</strong></a></td>
<td>Возвращает значение, указывающее, включен ли режим мультимедиа, связанный с указанным GUID.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>нтклосе</strong></a></td>
<td>Не рекомендуется. Эта функция используется для закрытия указанного маркера. <a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>Нтклосе</strong></a> заменяется <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>нтдевицеиоконтролфиле</strong></a></td>
<td>Не рекомендуется. Создает дескрипторы для предоставляемых буферов и передает нетипизированные данные драйверу устройства, связанному с дескриптором файла. <a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>Нтдевицеиоконтролфиле</strong></a> заменяется <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>нтваитфорсинглеобжект</strong></a></td>
<td>Не рекомендуется. Ожидает, пока указанный объект не выйдет из состояния <code>signaled</code> . <a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>Нтваитфорсинглеобжект</strong></a> заменяется объектом <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>ртлансистрингтауникодестринг</strong></a></td>
<td>Преобразует указанную исходную строку ANSI в строку в Юникоде. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlchartointeger"><strong>ртлчартоинтежер</strong></a></td>
<td>Преобразует строку символов в целое число.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions//ff899322(v=vs.85)"><strong>ртлформаткуррентусеркэйпас</strong></a></td>
<td>Инициализирует указанный буфер строковым представлением идентификатора безопасности для текущего пользователя. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeansistring"><strong>ртлфриансистринг</strong></a></td>
<td>Освобождает строковый буфер, выделенный <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>ртлуникодестрингтоансистринг</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeoemstring"><strong>ртлфриоемстринг</strong></a></td>
<td>Освобождает строковый буфер, выделенный <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>ртлуникодестрингтуемстринг</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeunicodestring"><strong>ртлфриуникодестринг</strong></a></td>
<td>Освобождает строковый буфер, выделенный <a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>ртлансистрингтауникодестринг</strong></a> или <a href="https://msdn.microsoft.com/library/ms803011.aspx">ртлупкасеуникодестринг</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitstring"><strong>ртлинитстринг</strong></a></td>
<td>Инициализирует подсчитанную строку. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitunicodestring"><strong>ртлинитуникодестринг</strong></a></td>
<td>Инициализирует подсчитанную строку Юникода. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>ртлуникодестрингтоансистринг</strong></a></td>
<td>Преобразует указанную исходную строку Юникода в строку ANSI. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>ртлуникодестрингтуемстринг</strong></a></td>
<td>Эта функция преобразует указанную исходную строку Юникода в строку OEM. Преобразование выполняется в соответствии с кодовой страницей OEM (OCP). <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodetomultibytesize"><strong>ртлуникодетомултибитесизе</strong></a></td>
<td>Определяет, сколько байтов необходимо для представления строки Юникода в виде строки ANSI.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a></td>
<td>Функция <a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a> преобразует указанную строку Юникода в новую символьную строку, используя 8-разрядную кодовую страницу формата преобразования Юникода (UTF-8).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a></td>
<td>Функция <a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a> преобразует указанную исходную строку в строку в Юникоде, используя кодовую страницу UTF-8.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Ime/nf-ime-sendimemessageexa"><strong>сендимемессажеекс</strong></a></td>
<td>Задает действие или обработку для редактора метода ввода (IME) с помощью указанной подфункции.
<blockquote>
[!Note]<br />
Эта функция устарела и не должна использоваться.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winnls32/nf-winnls32-winnlsenableime"><strong>виннлсенаблеиме</strong></a></td>
<td>Временно включает или отключает редактор IME и в то же время включает или отключает отображение всех окон, принадлежащих редактору IME.
<blockquote>
[!Note]<br />
Эта функция устарела и не должна использоваться.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="structures"></a>Структуры



| Раздел                                 | Содержимое                                                                                                                                                                                                                              |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**иместрукт**](/windows/win32/api/ime/ns-ime-imestruct) | Используется функцией [**сендимемессажеекс**](/windows/desktop/api/Ime/nf-ime-sendimemessageexa) для указания подфункции, выполняемой в сообщении IME и его параметрах. Эта структура также используется для получения возвращаемых значений из этих подфункций.<br/> |
| [**STRING**](/windows/desktop/api/Winternl/ns-winternl-string)       | Эта структура используется с функцией [**ртлуникодестрингтуемстринг**](/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring) . <br/>                                                                                                              |



 

### <a name="compiler-routines"></a>Подпрограммы компилятора



| Раздел                                                             | Содержимое                                                                                                     |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**\_\_Подпрограммы для \_ конкретного \_ обработчика C**](--c-specific-handler2.md) | [**\_ \_ \_ Специальный \_ обработчик c**](--c-specific-handler2.md) — это вспомогательная подпрограммы для компилятора C.<br/> |
| [\_подпрограммы аллдив](-win32-alldiv.md)                             | [ \_ подпрограммы аллдив](-win32-alldiv.md) — это вспомогательная подпрограммы для компилятора C.<br/>                     |
| [\_аллмул](-win32-allmul.md) | Умножает два **лонглонг** или **улонглонг**. |
| [\_ауллдив](-win32-aulldiv.md) | Делит два целых числа **улонглонг** . |
| [\_подпрограммы чкстк](-win32-chkstk.md)                             | [ \_ подпрограммы чкстк](-win32-chkstk.md) — это вспомогательная подпрограммы для компилятора C.<br/>                     |
