---
title: Типы данных Windows (BaseTsd.h)
description: типы данных, поддерживаемые Windows, используются для определения возвращаемых функцией значений, параметров функций и сообщений, а также членов структуры.
ms.assetid: 4553cafc-450e-4493-a4d4-cb6e2f274d46
keywords:
- типы данных
- типы данных, Windows
- API Windows
- Windows API, типы данных
- апиентри
- ATOM
- BOOL
- BOOLEAN
- BYTE
- ОБРАТНОГО вызова
- CCHAR
- CHAR
- COLORREF
- ПОСТОЯННОГО
- DWORD
- ОБЪЕКТА DWORDLONG
- DWORD_PTR
- DWORD32
- DWORD64
- FLOAT
- хакцел
- HALF_PTR
- HANDLE
- хбитмап
- хбруш
- хколорспаце
- хконв
- хконвлист
- хкурсор
- HDC
- хддедата
- хдеск
- HDROP
- хдвп
- хенхметафиле
- HFILE
- HFONT
- хгдиобж
- хглобал
- ххук
- хикон
- HINSTANCE
- HKEY
- HKL
- хлокал
- HMENU
- хметафиле
- хмодуле
- хмонитор
- хпалетте
- HPEN
- HRESULT
- HRGN
- хрсрк
- хсз
- хвинста
- HWND
- INT
- INT_PTR
- INT8
- INT16
- INT32
- INT64
- НАДЕЖНО
- LCID
- LCTYPE
- лгрпид
- LONG
- лонглонг
- LONG_PTR
- LONG32
- LONG64
- LPARAM
- лпбул
- LPBYTE
- лпколорреф
- LPCSTR
- LPCTSTR
- лпквоид
- LPCWSTR
- лпдворд
- лфандле
- лпинт
- лплонг
- LPSTR
- LPTSTR
- лпвоид
- лпворд
- LPWSTR
- LRESULT
- пбул
- пбулеан
- пбите
- пчар
- пкстр
- пктстр
- пквстр
- пдворд
- пдвордлонг
- PDWORD_PTR
- PDWORD32
- PDWORD64
- пфлоат
- PHALF_PTR
- фандле
- фкэй
- КОМАНДУ
- PINT_PTR
- PINT8
- PINT16
- PINT32
- PINT64
- плЦид
- плонг
- плонглонг
- PLONG_PTR
- PLONG32
- PLONG64
- POINTER_32
- POINTER_64
- POINTER_SIGNED
- POINTER_UNSIGNED
- пшорт
- PSIZE_T
- PSSIZE_T
- пстр
- птбите
- птчар
- птстр
- пучар
- PUHALF_PTR
- пуинт
- PUINT_PTR
- PUINT8
- PUINT16
- PUINT32
- PUINT64
- пулонг
- пулонглонг
- PULONG_PTR
- PULONG32
- PULONG64
- пушорт
- PVOID
- пвчар
- пворд
- пвстр
- QWORD
- SC_HANDLE
- SC_LOCK
- SERVICE_STATUS_HANDLE
- SHORT
- SIZE_T
- SSIZE_T
- TBYTE
- TCHAR
- учар
- UHALF_PTR
- UINT
- UINT_PTR
- UINT8
- UINT16
- ЗНАЧЕНИЕМ
- UINT64
- ULONG
- улонглонг
- ULONG_PTR
- ULONG32
- ULONG64
- UNICODE_STRING
- USHORT
- ЖУРНАЛЫ
- VOID
- WCHAR
- WINAPI
- WORD
- WPARAM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6769b5d3fd7c65eab1eef5c408ebd2e905b9677a3580774a857c68431aabd3dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412954"
---
# <a name="windows-data-types"></a>Типы данных Windows

типы данных, поддерживаемые Windows, используются для определения возвращаемых функцией значений, параметров функций и сообщений, а также членов структуры. Они определяют размер и значение этих элементов. Дополнительные сведения о базовых типах данных C/C++ см. в разделе [диапазоны типов данных](/cpp/cpp/data-type-ranges?view=vs-2019).

Следующая таблица содержит следующие типы: символ, целое число, логическое значение, указатель и маркер. Типы символьных, целочисленных и логических типов являются общими для большинства компиляторов C. Большинство имен типов указателей начинаются с префикса P или LP. Дескрипторы ссылаются на ресурс, который был загружен в память.

Дополнительные сведения об обработке 64-разрядных целых чисел см. в разделе [большие целые числа](large-integers.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Тип данных</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="APIENTRY"></span><span id="apientry"></span><strong>апиентри</strong></td>
<td>Соглашение о вызовах для системных функций.<br/> Этот тип объявляется в Виндеф. h следующим образом:<br/> <code>#define APIENTRY WINAPI</code><br/></td>
</tr>
<tr class="even">
<td><span id="ATOM"></span><span id="atom"></span><strong>АТОМАР</strong></td>
<td>Atom. Дополнительные сведения см. в разделе <a href="/windows/desktop/dataxchg/about-atom-tables">о таблицах Atom</a>.<br/> Этот тип объявляется в Виндеф. h следующим образом:<br/> <code>typedef WORD ATOM;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="BOOL"></span><span id="bool"></span><strong>ЛОГИЧЕСКОМ</strong></td>
<td>Логическая переменная (должна иметь <strong>значение true</strong> или <strong>false</strong>).<br/> Этот тип объявляется в Виндеф. h следующим образом:<br/> <code>typedef int BOOL;</code><br/></td>
</tr>
<tr class="even">
<td><span id="BOOLEAN"></span><span id="boolean"></span><strong>ЛОГИЧЕСКАЯ</strong></td>
<td>Логическая переменная (должна иметь <strong>значение true</strong> или <strong>false</strong>).<br/> Этот тип объявлен в WinNT. h следующим образом:<br/> <code>typedef BYTE BOOLEAN;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="BYTE"></span><span id="byte"></span><strong>ДВУХБАЙТОВЫХ</strong></td>
<td>Байт (8 бит).<br/> Этот тип объявляется в Виндеф. h следующим образом:<br/> <code>typedef unsigned char BYTE;</code><br/></td>
</tr>
<tr class="even">
<td><span id="CALLBACK"></span><span id="callback"></span><strong>ОБРАТНОГО вызова</strong></td>
<td>Соглашение о вызовах для функций обратного вызова.<br/> Этот тип объявляется в Виндеф. h следующим образом:<br/> <code>#define CALLBACK __stdcall</code><br/> Функции <strong>callback</strong>, <strong>WinAPI</strong>и <strong>апиентри</strong> используются для определения функций с помощью соглашения о вызовах __stdcall. большинство функций в API Windows объявляются с помощью <strong>WINAPI</strong>. Вы можете использовать <strong>обратный вызов</strong> для функций обратного вызова, которые реализуются, чтобы определить функцию как функцию обратного вызова.<br/></td>
</tr>
<tr class="odd">
<td><span id="CCHAR"></span><span id="cchar"></span><strong>CCHAR</strong></td>
<td>8-разрядный символ Windows (ANSI).<br/> Этот тип объявлен в WinNT. h следующим образом:<br/> <code>typedef char CCHAR;</code><br/></td>
</tr>
<tr class="even">
<td><span id="CHAR"></span><span id="char"></span><strong>ТИПА</strong></td>
<td>8-разрядный символ Windows (ANSI). Дополнительные сведения см. в разделе <a href="/windows/desktop/gdi/character-sets-used-by-fonts">наборы символов, используемые шрифтами</a>.<br/> Этот тип объявлен в WinNT. h следующим образом:<br/> <code>typedef char CHAR;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="COLORREF"></span><span id="colorref"></span><strong>COLORREF</strong></td>
<td>Значение цвета красного, зеленого, синего (RGB) (32 бит). Сведения об этом типе см. в разделе <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> .<br/> Этот тип объявляется в Виндеф. h следующим образом:<br/> <code>typedef DWORD COLORREF;</code><br/></td>
</tr>
<tr class="even">
<td><span id="CONST"></span><span id="const"></span><strong>ПОСТОЯННОГО</strong></td>
<td>Переменная, значение которой остается постоянной во время выполнения. <br/> Этот тип объявляется в Виндеф. h следующим образом:<br/> <code>#define CONST const</code><br/></td>
</tr>
<tr class="odd">
<td><span id="DWORD"></span><span id="dword"></span><strong>DWORD</strong></td>
<td>32-разрядное целое число без знака. Диапазон — от 0 до 4294967295 десятичных знаков.<br/> Этот тип объявляется в Интсафе. h следующим образом:<br/> <code>typedef unsigned long DWORD;</code><br/></td>
</tr>
<tr class="even">
<td><span id="DWORDLONG"></span><span id="dwordlong"></span><strong>ОБЪЕКТА DWORDLONG</strong></td>
<td>64-разрядное целое число без знака. Диапазон — от 0 до 18446744073709551615 Decimal.<br/> Этот тип объявляется в Интсафе. h следующим образом:<br/> <code>typedef unsigned __int64 DWORDLONG;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="DWORD_PTR"></span><span id="dword_ptr"></span><strong>DWORD_PTR</strong></td>
<td>Тип long без знака для точности указателя. Используется при приведении указателя к длинному типу для выполнения арифметических операций с указателями. (Также часто используется для общих 32-разрядных параметров, которые были расширены до 64 бит в 64-разрядной Windows.)<br/> Этот тип объявляется в Басетсд. h следующим образом:<br/> <code>typedef ULONG_PTR DWORD_PTR;</code><br/></td>
</tr>
<tr class="even">
<td><span id="DWORD32"></span><span id="dword32"></span><strong>DWORD32</strong></td>
<td>32-разрядное целое число без знака.<br/> Этот тип объявляется в Басетсд. h следующим образом:<br/> <code>typedef unsigned int DWORD32;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="DWORD64"></span><span id="dword64"></span><strong>DWORD64</strong></td>
<td>64-разрядное целое число без знака.<br/> Этот тип объявляется в Басетсд. h следующим образом:<br/> <code>typedef unsigned __int64 DWORD64;</code><br/></td>
</tr>
<tr class="even">
<td><span id="FLOAT"></span><span id="float"></span><strong>СДЕЛАТЬ</strong></td>
<td>Переменная с плавающей запятой.<br/> Этот тип объявляется в Виндеф. h следующим образом:<br/> <code>typedef float FLOAT;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="HACCEL"></span><span id="haccel"></span><strong>хакцел</strong></td>
<td>Маркер для <a href="/windows/desktop/menurc/keyboard-accelerators">таблицы сочетаний клавиш</a>.<br/> Этот тип объявляется в Виндеф. h следующим образом:<br/> <code>typedef HANDLE HACCEL;</code><br/></td>
</tr>
<tr class="even">
<td><span id="HALF_PTR"></span><span id="half_ptr"></span><strong>HALF_PTR</strong></td>
<td>Половина размера указателя. Используйте в структуре, содержащей указатель и два маленьких поля.<br/> Этот тип объявляется в Басетсд. h следующим образом:<br/> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef _WIN64
 typedef int HALF_PTR;
#else
 typedef short HALF_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="odd">
<td><span id="HANDLE"></span><span id="handle"></span><strong>СПРАВИТЬСЯ</strong></td>
<td><p>Маркер объекта.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<p><code>typedef PVOID HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span id="HBITMAP"></span><span id="hbitmap"></span><strong>хбитмап</strong></td>
<td><p>Маркер <a href="/windows/desktop/gdi/bitmaps">точечного рисунка</a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef HANDLE HBITMAP;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HBRUSH"></span><span id="hbrush"></span><strong>хбруш</strong></td>
<td><p>Дескриптор <a href="/windows/desktop/gdi/brushes">кисти</a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef HANDLE HBRUSH;</code></p></td>
</tr>
<tr class="even">
<td><span id="HCOLORSPACE"></span><span id="hcolorspace"></span><strong>хколорспаце</strong></td>
<td><p>Маркер <a href="/previous-versions//dd316799(v=vs.85)">цветового пространства</a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef HANDLE HCOLORSPACE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HCONV"></span><span id="hconv"></span><strong>хконв</strong></td>
<td><p>Маркер диалога динамического обмена данными (DDE).</p>
<p>Этот тип объявляется в Ддемл. h следующим образом:</p>
<p><code>typedef HANDLE HCONV;</code></p></td>
</tr>
<tr class="even">
<td><span id="HCONVLIST"></span><span id="hconvlist"></span><strong>хконвлист</strong></td>
<td><p>Маркер для списка сеансов DDE.</p>
<p>Этот тип объявляется в Ддемл. h следующим образом:</p>
<p><code>typedef HANDLE HCONVLIST;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HCURSOR"></span><span id="hcursor"></span><strong>хкурсор</strong></td>
<td><p><a href="/windows/desktop/menurc/cursors">Указатель на курсор</a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef HICON HCURSOR;</code></p></td>
</tr>
<tr class="even">
<td><span id="HDC"></span><span id="hdc"></span><strong>HDC</strong></td>
<td><p>Маркер <a href="/windows/desktop/gdi/device-context-types">контекста устройства</a> (DC).</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef HANDLE HDC;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HDDEDATA"></span><span id="hddedata"></span><strong>хддедата</strong></td>
<td><p>Обработчик данных DDE.</p>
<p>Этот тип объявляется в Ддемл. h следующим образом:</p>
<p><code>typedef HANDLE HDDEDATA;</code></p></td>
</tr>
<tr class="even">
<td><span id="HDESK"></span><span id="hdesk"></span><strong>хдеск</strong></td>
<td><p>Маркер <a href="/windows/desktop/winstation/desktops">рабочего стола</a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef HANDLE HDESK;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HDROP"></span><span id="hdrop"></span><strong>HDROP</strong></td>
<td><p>Маркер внутренней структуры перетаскивания.</p>
<p>Этот тип объявляется в Шеллапи. h следующим образом:</p>
<p><code>typedef HANDLE HDROP;</code></p></td>
</tr>
<tr class="even">
<td><span id="HDWP"></span><span id="hdwp"></span><strong>хдвп</strong></td>
<td><p>Указатель на структуру отложенной позицией окна.</p>
<p>Этот тип объявлен в файле WinUser. h следующим образом:</p>
<p><code>typedef HANDLE HDWP;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HENHMETAFILE"></span><span id="henhmetafile"></span><strong>хенхметафиле</strong></td>
<td><p>Маркер <a href="/windows/desktop/gdi/metafiles">расширенного метафайла</a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef HANDLE HENHMETAFILE;</code></p></td>
</tr>
<tr class="even">
<td><span id="HFILE"></span><span id="hfile"></span><strong>HFILE</strong></td>
<td><p>Обработчик для файла, открытого с помощью <a href="/windows/desktop/api/winbase/nf-winbase-openfile"><strong>OpenFile</strong></a>, а не <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea"><strong>CreateFile</strong></a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef int HFILE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HFONT"></span><span id="hfont"></span><strong>хфонт</strong></td>
<td><p>Маркер для <a href="/windows/desktop/gdi/about-fonts">шрифта</a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef HANDLE HFONT;</code></p></td>
</tr>
<tr class="even">
<td><span id="HGDIOBJ"></span><span id="hgdiobj"></span><strong>хгдиобж</strong></td>
<td><p>Маркер объекта GDI.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef HANDLE HGDIOBJ;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HGLOBAL"></span><span id="hglobal"></span><strong>хглобал</strong></td>
<td><p>Маркер глобального блока памяти.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef HANDLE HGLOBAL;</code></p></td>
</tr>
<tr class="even">
<td><span id="HHOOK"></span><span id="hhook"></span><strong>ххук</strong></td>
<td><p>Маркер <a href="/windows/desktop/winmsg/hooks">обработчика</a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef HANDLE HHOOK;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HICON"></span><span id="hicon"></span><strong>хикон</strong></td>
<td><p>Маркер для <a href="/windows/desktop/menurc/icons">значка</a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef HANDLE HICON;</code></p></td>
</tr>
<tr class="even">
<td><span id="HINSTANCE"></span><span id="hinstance"></span><strong>HINSTANCE</strong></td>
<td><p>Маркер экземпляра. Это базовый адрес модуля в памяти.</p>
<p><strong>Хмодуле</strong> и <strong>HINSTANCE</strong> уже сегодня, но в 16-разрядных Windows представлены различные вещи.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef HANDLE HINSTANCE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HKEY"></span><span id="hkey"></span><strong>HKEY</strong></td>
<td><p>Маркер раздела реестра.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef HANDLE HKEY;</code></p></td>
</tr>
<tr class="even">
<td><span id="HKL"></span><span id="hkl"></span><strong>HKL</strong></td>
<td><p>Идентификатор языка ввода.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef HANDLE HKL;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HLOCAL"></span><span id="hlocal"></span><strong>хлокал</strong></td>
<td><p>Маркер локального блока памяти.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef HANDLE HLOCAL;</code></p></td>
</tr>
<tr class="even">
<td><span id="HMENU"></span><span id="hmenu"></span><strong>HMENU</strong></td>
<td><p>Маркер <a href="/windows/desktop/menurc/menus">меню</a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef HANDLE HMENU;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HMETAFILE"></span><span id="hmetafile"></span><strong>хметафиле</strong></td>
<td><p>Маркер для <a href="/windows/desktop/gdi/metafiles">метафайла</a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef HANDLE HMETAFILE;</code></p></td>
</tr>
<tr class="even">
<td><span id="HMODULE"></span><span id="hmodule"></span><strong>хмодуле</strong></td>
<td><p>Обработчик для модуля. — Это базовый адрес модуля в памяти.</p>
<p><strong>хмодуле</strong> и <strong>HINSTANCE</strong> одинаковы в текущих версиях Windows, но в 16-разрядных Windows представлены различные вещи.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef HINSTANCE HMODULE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HMONITOR"></span><span id="hmonitor"></span><strong>хмонитор</strong></td>
<td><p>Маркер монитора.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>if(WINVER >= 0x0500) typedef HANDLE HMONITOR;</code></p></td>
</tr>
<tr class="even">
<td><span id="HPALETTE"></span><span id="hpalette"></span><strong>хпалетте</strong></td>
<td><p>Маркер для палитры.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef HANDLE HPALETTE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HPEN"></span><span id="hpen"></span><strong>хпен</strong></td>
<td><p>Указатель на <a href="/windows/desktop/gdi/pens">перо</a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef HANDLE HPEN;</code></p></td>
</tr>
<tr class="even">
<td><span id="HRESULT"></span><span id="hresult"></span><strong>СОСТАВ</strong></td>
<td><p>Коды возврата, используемые интерфейсами COM. Дополнительные сведения см. <a href="/windows/desktop/com/structure-of-com-error-codes">в разделе структура кодов ошибок COM</a>. Чтобы проверить значение <strong>HRESULT</strong> , <a href="/windows/desktop/api/winerror/nf-winerror-succeeded"><strong>Используйте макросы,</strong></a> <a href="/windows/desktop/api/winerror/nf-winerror-failed"><strong>Завершившиеся сбоем и Failed</strong></a> .</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<p><code>typedef LONG HRESULT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HRGN"></span><span id="hrgn"></span><strong>хргн</strong></td>
<td><p>Маркер для <a href="/windows/desktop/gdi/regions">региона</a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef HANDLE HRGN;</code></p></td>
</tr>
<tr class="even">
<td><span id="HRSRC"></span><span id="hrsrc"></span><strong>хрсрк</strong></td>
<td><p>Маркер ресурса.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef HANDLE HRSRC;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HSZ"></span><span id="hsz"></span><strong>хсз</strong></td>
<td><p>Маркер строки DDE.</p>
<p>Этот тип объявляется в Ддемл. h следующим образом:</p>
<p><code>typedef HANDLE HSZ;</code></p></td>
</tr>
<tr class="even">
<td><span id="HWINSTA"></span><span id="hwinsta"></span><strong>хвинста</strong></td>
<td><p>Обработчик <a href="/windows/desktop/winstation/window-stations">оконной станции</a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef HANDLE WINSTA;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HWND"></span><span id="hwnd"></span><strong>HWND</strong></td>
<td><p>Маркер <a href="/windows/desktop/winmsg/windows">окна</a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef HANDLE HWND;</code></p></td>
</tr>
<tr class="even">
<td><span id="INT"></span><span id="int"></span><strong>INT</strong></td>
<td><p>32-разрядное знаковое целое число. Диапазон значений — от-2147483648 до 2147483647.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef int INT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="INT_PTR"></span><span id="int_ptr"></span><strong>INT_PTR</strong></td>
<td><p>Целочисленный тип со знаком для точности указателя. Используется при приведении указателя на целое число для выполнения арифметических операций с указателями.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64) 
 typedef __int64 INT_PTR; 
#else 
 typedef int INT_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="INT8"></span><span id="int8"></span><strong>INT8</strong></td>
<td><p>8-битовое целое число со знаком.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef signed char INT8;</code></p></td>
</tr>
<tr class="odd">
<td><span id="INT16"></span><span id="int16"></span><strong>INT16</strong></td>
<td><p>16-разрядное знаковое целое число.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef signed short INT16;</code></p></td>
</tr>
<tr class="even">
<td><span id="INT32"></span><span id="int32"></span><strong>ТИПА</strong></td>
<td><p>32-разрядное знаковое целое число. Диапазон значений — от-2147483648 до 2147483647.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef signed int INT32;</code></p></td>
</tr>
<tr class="odd">
<td><span id="INT64"></span><span id="int64"></span><strong>INT64</strong></td>
<td><p>64-разрядное целое число со знаком. Диапазон составляет от-9223372036854775808 до 9223372036854775807 десятичного числа.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef signed __int64 INT64;</code></p></td>
</tr>
<tr class="even">
<td><span id="LANGID"></span><span id="langid"></span><strong>НАДЕЖНО</strong></td>
<td><p>Идентификатор языка. Дополнительные сведения см. в разделе <a href="/windows/desktop/Intl/language-identifiers">идентификаторы языков</a>.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<p><code>typedef WORD LANGID;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LCID"></span><span id="lcid"></span><strong>НАМНОГО</strong></td>
<td><p>Идентификатор локали. Дополнительные сведения см. в разделе <a href="/windows/desktop/Intl/locale-identifiers">идентификаторы языкового стандарта</a>.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<p><code>typedef DWORD LCID;</code></p></td>
</tr>
<tr class="even">
<td><span id="LCTYPE"></span><span id="lctype"></span><strong>LCTYPE</strong></td>
<td><p>Тип сведений о языковых стандартах. Список см. в разделе <a href="/windows/desktop/Intl/locale-information-constants">константы сведений о языковых стандартах</a>.</p>
<p>Этот тип объявляется в Виннлс. h следующим образом:</p>
<p><code>typedef DWORD LCTYPE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LGRPID"></span><span id="lgrpid"></span><strong>лгрпид</strong></td>
<td><p>Идентификатор языковой группы. Список см. в разделе <a href="/windows/desktop/api/winnls/nf-winnls-enumlanguagegrouplocalesa"><strong>енумлангуажеграуплокалес</strong></a>.</p>
<p>Этот тип объявляется в Виннлс. h следующим образом:</p>
<p><code>typedef DWORD LGRPID;</code></p></td>
</tr>
<tr class="even">
<td><span id="LONG"></span><span id="long"></span><strong>ПОДДЕРЖИВАЕМ</strong></td>
<td><p>32-разрядное знаковое целое число. Диапазон значений — от-2147483648 до 2147483647.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<p><code>typedef long LONG;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LONGLONG"></span><span id="longlong"></span><strong>лонглонг</strong></td>
<td><p>64-разрядное целое число со знаком. Диапазон составляет от-9223372036854775808 до 9223372036854775807 десятичного числа.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if !defined(_M_IX86)
 typedef __int64 LONGLONG; 
#else
 typedef double LONGLONG;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="LONG_PTR"></span><span id="long_ptr"></span><strong>LONG_PTR</strong></td>
<td><p>Длинный тип со знаком для точности указателя. Используется при приведении указателя к типу long для выполнения арифметических операций с указателями.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64)
 typedef __int64 LONG_PTR; 
#else
 typedef long LONG_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="LONG32"></span><span id="long32"></span><strong>LONG32</strong></td>
<td><p>32-разрядное знаковое целое число. Диапазон значений — от-2147483648 до 2147483647.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef signed int LONG32;</code></p></td>
</tr>
<tr class="even">
<td><span id="LONG64"></span><span id="long64"></span><strong>LONG64</strong></td>
<td><p>64-разрядное целое число со знаком. Диапазон составляет от-9223372036854775808 до 9223372036854775807 десятичного числа.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef __int64 LONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPARAM"></span><span id="lparam"></span><strong>LPARAM</strong></td>
<td><p>Параметр сообщения.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef LONG_PTR LPARAM;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPBOOL"></span><span id="lpbool"></span><strong>лпбул</strong></td>
<td><p>Указатель на <a href="#bool"><strong>логическое</strong></a>значение.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef BOOL far *LPBOOL;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPBYTE"></span><span id="lpbyte"></span><strong>LPBYTE</strong></td>
<td><p>Указатель на <a href="#byte"><strong>байт</strong></a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef BYTE far *LPBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPCOLORREF"></span><span id="lpcolorref"></span><strong>лпколорреф</strong></td>
<td><p>Указатель на значение <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> .</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef DWORD *LPCOLORREF;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPCSTR"></span><span id="lpcstr"></span><strong>LPCSTR</strong></td>
<td><p>указатель на константную строку, завершающуюся нулем, в 8-разрядной Windows (ANSI) символов. Дополнительные сведения см. в разделе <a href="/windows/desktop/gdi/character-sets-used-by-fonts">наборы символов, используемые шрифтами</a>.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<p><code>typedef __nullterminated CONST CHAR *LPCSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPCTSTR"></span><span id="lpctstr"></span><strong>LPCTSTR</strong></td>
<td><p><a href="#lpcwstr"><strong>Лпквстр</strong></a> , если определен <strong>Юникод</strong> , <a href="#lpcstr"><strong>LPCSTR</strong></a> в противном случае. дополнительные сведения см. в разделе <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows типы данных для строк</a>.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef LPCWSTR LPCTSTR; 
#else
 typedef LPCSTR LPCTSTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="LPCVOID"></span><span id="lpcvoid"></span><strong>лпквоид</strong></td>
<td><p>Указатель на константу любого типа.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef CONST void *LPCVOID;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPCWSTR"></span><span id="lpcwstr"></span><strong>лпквстр</strong></td>
<td><p>Указатель на константную строку из 16-разрядных символов Юникода, завершающуюся нулем. Дополнительные сведения см. в разделе <a href="/windows/desktop/gdi/character-sets-used-by-fonts">наборы символов, используемые шрифтами</a>.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<p><code>typedef CONST WCHAR *LPCWSTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPDWORD"></span><span id="lpdword"></span><strong>лпдворд</strong></td>
<td><p>Указатель на <a href="#dword"><strong>DWORD</strong></a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef DWORD *LPDWORD;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPHANDLE"></span><span id="lphandle"></span><strong>лфандле</strong></td>
<td><p>Указатель на <a href="#handle"><strong>маркер</strong></a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef HANDLE *LPHANDLE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPINT"></span><span id="lpint"></span><strong>лпинт</strong></td>
<td><p>Указатель на <a href="#int"><strong>тип int</strong></a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef int *LPINT;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPLONG"></span><span id="lplong"></span><strong>лплонг</strong></td>
<td><p>Указатель на значение <a href="#long"><strong>типа Long</strong></a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef long *LPLONG;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPSTR"></span><span id="lpstr"></span><strong>LPSTR</strong></td>
<td><p>указатель на строку, завершающуюся нулем или 8-разрядную Windows (ANSI) символов. Дополнительные сведения см. в разделе <a href="/windows/desktop/gdi/character-sets-used-by-fonts">наборы символов, используемые шрифтами</a>.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<p><code>typedef CHAR *LPSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPTSTR"></span><span id="lptstr"></span><strong>LPTSTR</strong></td>
<td><p><a href="#lpwstr"><strong>LPWSTR</strong></a> , если определен <strong>Юникод</strong> , <a href="#lpstr"><strong>LPSTR</strong></a> в противном случае. дополнительные сведения см. в разделе <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows типы данных для строк</a>.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef LPWSTR LPTSTR;
#else
 typedef LPSTR LPTSTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="LPVOID"></span><span id="lpvoid"></span><strong>лпвоид</strong></td>
<td><p>Указатель на любой тип.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef void *LPVOID;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPWORD"></span><span id="lpword"></span><strong>лпворд</strong></td>
<td><p>Указатель на <a href="#word"><strong>слово</strong></a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef WORD *LPWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPWSTR"></span><span id="lpwstr"></span><strong>LPWSTR</strong></td>
<td><p>Указатель на строку из 16-разрядных символов Юникода, завершающуюся нулем. Дополнительные сведения см. в разделе <a href="/windows/desktop/gdi/character-sets-used-by-fonts">наборы символов, используемые шрифтами</a>.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<p><code>typedef WCHAR *LPWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="LRESULT"></span><span id="lresult"></span><strong>LRESULT</strong></td>
<td><p>Подписанный результат обработки сообщения.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef LONG_PTR LRESULT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PBOOL"></span><span id="pbool"></span><strong>пбул</strong></td>
<td><p>Указатель на <a href="#bool"><strong>логическое</strong></a>значение.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef BOOL *PBOOL;</code></p></td>
</tr>
<tr class="even">
<td><span id="PBOOLEAN"></span><span id="pboolean"></span><strong>пбулеан</strong></td>
<td><p>Указатель на <a href="#boolean"><strong>логическое значение</strong></a>.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<p><code>typedef BOOLEAN *PBOOLEAN;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PBYTE"></span><span id="pbyte"></span><strong>пбите</strong></td>
<td><p>Указатель на <a href="#byte"><strong>байт</strong></a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef BYTE *PBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span id="PCHAR"></span><span id="pchar"></span><strong>пчар</strong></td>
<td><p>Указатель на <a href="#char"><strong>символ</strong></a>.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<p><code>typedef CHAR *PCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PCSTR"></span><span id="pcstr"></span><strong>пкстр</strong></td>
<td><p>указатель на константную строку, завершающуюся нулем, в 8-разрядной Windows (ANSI) символов. Дополнительные сведения см. в разделе <a href="/windows/desktop/gdi/character-sets-used-by-fonts">наборы символов, используемые шрифтами</a>.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<p><code>typedef CONST CHAR *PCSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="PCTSTR"></span><span id="pctstr"></span><strong>пктстр</strong></td>
<td><p><a href="#pcwstr"><strong>Пквстр</strong></a> , если определен <strong>Юникод</strong> , <a href="#pcstr"><strong>пкстр</strong></a> в противном случае. дополнительные сведения см. в разделе <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows типы данных для строк</a>.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef LPCWSTR PCTSTR;
#else
 typedef LPCSTR PCTSTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="PCWSTR"></span><span id="pcwstr"></span><strong>пквстр</strong></td>
<td><p>Указатель на константную строку из 16-разрядных символов Юникода, завершающуюся нулем. Дополнительные сведения см. в разделе <a href="/windows/desktop/gdi/character-sets-used-by-fonts">наборы символов, используемые шрифтами</a>.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<p><code>typedef CONST WCHAR *PCWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="PDWORD"></span><span id="pdword"></span><strong>пдворд</strong></td>
<td><p>Указатель на <a href="#dword"><strong>DWORD</strong></a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef DWORD *PDWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PDWORDLONG"></span><span id="pdwordlong"></span><strong>пдвордлонг</strong></td>
<td><p>Указатель на <a href="#dwordlong"><strong>объекта dwordlong</strong></a>.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<p><code>typedef DWORDLONG *PDWORDLONG;</code></p></td>
</tr>
<tr class="even">
<td><span id="PDWORD_PTR"></span><span id="pdword_ptr"></span><strong>PDWORD_PTR</strong></td>
<td><p>Указатель на <a href="#dword_ptr"><strong>DWORD_PTR</strong></a>.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef DWORD_PTR *PDWORD_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PDWORD32"></span><span id="pdword32"></span><strong>PDWORD32</strong></td>
<td><p>Указатель на <a href="#dword32"><strong>DWORD32</strong></a>.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef DWORD32 *PDWORD32;</code></p></td>
</tr>
<tr class="even">
<td><span id="PDWORD64"></span><span id="pdword64"></span><strong>PDWORD64</strong></td>
<td><p>Указатель на <a href="#dword64"><strong>DWORD64</strong></a>.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef DWORD64 *PDWORD64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PFLOAT"></span><span id="pfloat"></span><strong>пфлоат</strong></td>
<td><p>Указатель на число с <a href="#float"><strong>плавающей запятой</strong></a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef FLOAT *PFLOAT;</code></p></td>
</tr>
<tr class="even">
<td><span id="PHALF_PTR"></span><span id="phalf_ptr"></span><strong>PHALF_PTR</strong></td>
<td><p>Указатель на <a href="#half_ptr"><strong>HALF_PTR</strong></a>.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef _WIN64
 typedef HALF_PTR *PHALF_PTR;
#else
 typedef HALF_PTR *PHALF_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="PHANDLE"></span><span id="phandle"></span><strong>фандле</strong></td>
<td><p>Указатель на <a href="#handle"><strong>маркер</strong></a>.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<p><code>typedef HANDLE *PHANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span id="PHKEY"></span><span id="phkey"></span><strong>фкэй</strong></td>
<td><p>Указатель на <a href="#hkey"><strong>hKey</strong></a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef HKEY *PHKEY;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PINT"></span><span id="pint"></span><strong>КОМАНДУ</strong></td>
<td><p>Указатель на <a href="#int"><strong>тип int</strong></a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef int *PINT;</code></p></td>
</tr>
<tr class="even">
<td><span id="PINT_PTR"></span><span id="pint_ptr"></span><strong>PINT_PTR</strong></td>
<td><p>Указатель на <a href="#int_ptr"><strong>INT_PTR</strong></a>.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef INT_PTR *PINT_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PINT8"></span><span id="pint8"></span><strong>PINT8</strong></td>
<td><p>Указатель на <a href="#int8"><strong>INT8</strong></a>.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef INT8 *PINT8;</code></p></td>
</tr>
<tr class="even">
<td><span id="PINT16"></span><span id="pint16"></span><strong>PINT16</strong></td>
<td><p>Указатель на значение <a href="#int16"><strong>INT16</strong></a>.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef INT16 *PINT16;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PINT32"></span><span id="pint32"></span><strong>PINT32</strong></td>
<td><p>Указатель на <a href="#int32"><strong>Int32</strong></a>.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef INT32 *PINT32;</code></p></td>
</tr>
<tr class="even">
<td><span id="PINT64"></span><span id="pint64"></span><strong>PINT64</strong></td>
<td><p>Указатель на <a href="#int64"><strong>Int64</strong></a>.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef INT64 *PINT64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PLCID"></span><span id="plcid"></span><strong>плЦид</strong></td>
<td><p>Указатель на <a href="#lcid"><strong>код языка</strong></a>.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<p><code>typedef PDWORD PLCID;</code></p></td>
</tr>
<tr class="even">
<td><span id="PLONG"></span><span id="plong"></span><strong>плонг</strong></td>
<td><p>Указатель на значение <a href="#long"><strong>типа Long</strong></a>.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<p><code>typedef LONG *PLONG;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PLONGLONG"></span><span id="plonglong"></span><strong>плонглонг</strong></td>
<td><p>Указатель на <a href="#longlong"><strong>лонглонг</strong></a>.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<p><code>typedef LONGLONG *PLONGLONG;</code></p></td>
</tr>
<tr class="even">
<td><span id="PLONG_PTR"></span><span id="plong_ptr"></span><strong>PLONG_PTR</strong></td>
<td><p>Указатель на <a href="#long_ptr"><strong>LONG_PTR</strong></a>.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef LONG_PTR *PLONG_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PLONG32"></span><span id="plong32"></span><strong>PLONG32</strong></td>
<td><p>Указатель на <a href="#long32"><strong>LONG32</strong></a>.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef LONG32 *PLONG32;</code></p></td>
</tr>
<tr class="even">
<td><span id="PLONG64"></span><span id="plong64"></span><strong>PLONG64</strong></td>
<td><p>Указатель на <a href="#long64"><strong>LONG64</strong></a>.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef LONG64 *PLONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="POINTER_32"></span><span id="pointer_32"></span><strong>POINTER_32</strong></td>
<td><p>32-разрядный указатель. В 32-разрядной системе это собственный указатель. В 64-разрядной системе это усеченный 64-разрядный указатель.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64)
#define POINTER_32 __ptr32
#else
#define POINTER_32
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="POINTER_64"></span><span id="pointer_64"></span><strong>POINTER_64</strong></td>
<td><p>64-разрядный указатель. В 64-разрядной системе это собственный указатель. В 32-разрядной системе это расширенный по знаку 32-разрядный указатель.</p>
<p>Обратите внимание, что нельзя считать, что состояние старших битов указателя не является надежным.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if (_MSC_VER >= 1300)
#define POINTER_64 __ptr64
#else
#define POINTER_64
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="POINTER_SIGNED"></span><span id="pointer_signed"></span><strong>POINTER_SIGNED</strong></td>
<td><p>Указатель со знаком.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>#define POINTER_SIGNED __sptr</code></p></td>
</tr>
<tr class="even">
<td><span id="POINTER_UNSIGNED"></span><span id="pointer_unsigned"></span><strong>POINTER_UNSIGNED</strong></td>
<td><p>Указатель без знака.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>#define POINTER_UNSIGNED __uptr</code></p></td>
</tr>
<tr class="odd">
<td><span id="PSHORT"></span><span id="pshort"></span><strong>пшорт</strong></td>
<td><p>Указатель на <a href="#short"><strong>короткий</strong></a>.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<p><code>typedef SHORT *PSHORT;</code></p></td>
</tr>
<tr class="even">
<td><span id="PSIZE_T"></span><span id="psize_t"></span><strong>PSIZE_T</strong></td>
<td><p>Указатель на <a href="#size_t"><strong>SIZE_T</strong></a>.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef SIZE_T *PSIZE_T;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PSSIZE_T"></span><span id="pssize_t"></span><strong>PSSIZE_T</strong></td>
<td><p>Указатель на <a href="#ssize_t"><strong>SSIZE_T</strong></a>.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef SSIZE_T *PSSIZE_T;</code></p></td>
</tr>
<tr class="even">
<td><span id="PSTR"></span><span id="pstr"></span><strong>пстр</strong></td>
<td><p>указатель на строку, завершающуюся нулем или 8-разрядную Windows (ANSI) символов. Дополнительные сведения см. в разделе <a href="/windows/desktop/gdi/character-sets-used-by-fonts">наборы символов, используемые шрифтами</a>.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<p><code>typedef CHAR *PSTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PTBYTE"></span><span id="ptbyte"></span><strong>птбите</strong></td>
<td><p>Указатель на <a href="#tbyte"><strong>тбите</strong></a>.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<p><code>typedef TBYTE *PTBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span id="PTCHAR"></span><span id="ptchar"></span><strong>птчар</strong></td>
<td><p>Указатель на <a href="#tchar"><strong>TCHAR</strong></a>.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<p><code>typedef TCHAR *PTCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PTSTR"></span><span id="ptstr"></span><strong>птстр</strong></td>
<td><p><a href="#pwstr"><strong>Пвстр</strong></a> , если определен <strong>Юникод</strong> , <a href="#pstr"><strong>ПСТР</strong></a> в противном случае. дополнительные сведения см. в разделе <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows типы данных для строк</a>.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef LPWSTR PTSTR;
#else typedef LPSTR PTSTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="PUCHAR"></span><span id="puchar"></span><strong>пучар</strong></td>
<td><p>Указатель на <a href="#uchar"><strong>Учар</strong></a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef UCHAR *PUCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUHALF_PTR"></span><span id="puhalf_ptr"></span><strong>PUHALF_PTR</strong></td>
<td><p>Указатель на <a href="#uhalf_ptr"><strong>UHALF_PTR</strong></a>.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef _WIN64
 typedef UHALF_PTR *PUHALF_PTR;
#else
 typedef UHALF_PTR *PUHALF_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="PUINT"></span><span id="puint"></span><strong>пуинт</strong></td>
<td><p>Указатель на <a href="#uint"><strong>uint</strong></a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef UINT *PUINT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUINT_PTR"></span><span id="puint_ptr"></span><strong>PUINT_PTR</strong></td>
<td><p>Указатель на <a href="#uint_ptr"><strong>UINT_PTR</strong></a>.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef UINT_PTR *PUINT_PTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="PUINT8"></span><span id="puint8"></span><strong>PUINT8</strong></td>
<td><p>Указатель на <a href="#uint8"><strong>UINT8</strong></a>.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef UINT8 *PUINT8;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUINT16"></span><span id="puint16"></span><strong>PUINT16</strong></td>
<td><p>Указатель на <a href="#uint16"><strong>UINT16</strong></a>.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef UINT16 *PUINT16;</code></p></td>
</tr>
<tr class="even">
<td><span id="PUINT32"></span><span id="puint32"></span><strong>PUINT32</strong></td>
<td><p>Указатель на <a href="#uint32"><strong>UINT32</strong></a>.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef UINT32 *PUINT32;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUINT64"></span><span id="puint64"></span><strong>PUINT64</strong></td>
<td><p>Указатель на <a href="#uint64"><strong>UINT64</strong></a>.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef UINT64 *PUINT64;</code></p></td>
</tr>
<tr class="even">
<td><span id="PULONG"></span><span id="pulong"></span><strong>пулонг</strong></td>
<td><p>Указатель на <a href="#ulong"><strong>ulong</strong></a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef ULONG *PULONG;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PULONGLONG"></span><span id="pulonglong"></span><strong>пулонглонг</strong></td>
<td><p>Указатель на <a href="#ulonglong"><strong>улонглонг</strong></a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef ULONGLONG *PULONGLONG;</code></p></td>
</tr>
<tr class="even">
<td><span id="PULONG_PTR"></span><span id="pulong_ptr"></span><strong>PULONG_PTR</strong></td>
<td><p>Указатель на <a href="#ulong_ptr"><strong>ULONG_PTR</strong></a>.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef ULONG_PTR *PULONG_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PULONG32"></span><span id="pulong32"></span><strong>PULONG32</strong></td>
<td><p>Указатель на <a href="#ulong32"><strong>ULONG32</strong></a>.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef ULONG32 *PULONG32;</code></p></td>
</tr>
<tr class="even">
<td><span id="PULONG64"></span><span id="pulong64"></span><strong>PULONG64</strong></td>
<td><p>Указатель на <a href="#ulong64"><strong>ULONG64</strong></a>.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef ULONG64 *PULONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUSHORT"></span><span id="pushort"></span><strong>пушорт</strong></td>
<td><p>Указатель на <a href="#ushort"><strong>UShort</strong></a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef USHORT *PUSHORT;</code></p></td>
</tr>
<tr class="even">
<td><span id="PVOID"></span><span id="pvoid"></span><strong>PVOID</strong></td>
<td><p>Указатель на любой тип.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<p><code>typedef void *PVOID;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PWCHAR"></span><span id="pwchar"></span><strong>пвчар</strong></td>
<td><p>Указатель на <a href="#wchar"><strong>WCHAR</strong></a>.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<p><code>typedef WCHAR *PWCHAR;</code></p></td>
</tr>
<tr class="even">
<td><span id="PWORD"></span><span id="pword"></span><strong>пворд</strong></td>
<td><p>Указатель на <a href="#word"><strong>слово</strong></a>.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef WORD *PWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PWSTR"></span><span id="pwstr"></span><strong>пвстр</strong></td>
<td><p>Указатель на строку из 16-разрядных символов Юникода, завершающуюся нулем. Дополнительные сведения см. в разделе <a href="/windows/desktop/gdi/character-sets-used-by-fonts">наборы символов, используемые шрифтами</a>.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<p><code>typedef WCHAR *PWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="QWORD"></span><span id="qword"></span><strong>QWORD</strong></td>
<td><p>64-разрядное целое число без знака.</p>
<p>Этот тип объявляется следующим образом:</p>
<p><code>typedef unsigned __int64 QWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="SC_HANDLE"></span><span id="sc_handle"></span><strong>SC_HANDLE</strong></td>
<td><p>Маркер базы данных диспетчера управления службами. Дополнительные сведения см. в разделе <a href="/windows/desktop/Services/scm-handles">дескрипторы SCM</a>.</p>
<p>Этот тип объявляется в Винсвк. h следующим образом:</p>
<p><code>typedef HANDLE SC_HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span id="SC_LOCK"></span><span id="sc_lock"></span><strong>SC_LOCK</strong></td>
<td><p>Блокировка базы данных диспетчера управления службами. Дополнительные сведения см. в разделе <a href="/windows/desktop/Services/scm-handles">дескрипторы SCM</a>.</p>
<p>Этот тип объявляется в Винсвк. h следующим образом:</p>
<p><code>typedef LPVOID SC_LOCK;</code></p></td>
</tr>
<tr class="odd">
<td><span id="SERVICE_STATUS_HANDLE"></span><span id="service_status_handle"></span><strong>SERVICE_STATUS_HANDLE</strong></td>
<td><p>Маркер для значения состояния службы. Дополнительные сведения см. в разделе <a href="/windows/desktop/Services/scm-handles">дескрипторы SCM</a>.</p>
<p>Этот тип объявляется в Винсвк. h следующим образом:</p>
<p><code>typedef HANDLE SERVICE_STATUS_HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span id="SHORT"></span><span id="short"></span><strong>ПРОМЕЖУТОК</strong></td>
<td><p>16-разрядное целое число. Диапазон значений — от-32768 до 32767.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<p><code>typedef short SHORT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="SIZE_T"></span><span id="size_t"></span><strong>SIZE_T</strong></td>
<td><p>Максимальное число байтов, на которое может указывать указатель. Используется для подсчета, который должен охватывать полный диапазон указателя.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef ULONG_PTR SIZE_T;</code></p></td>
</tr>
<tr class="even">
<td><span id="SSIZE_T"></span><span id="ssize_t"></span><strong>SSIZE_T</strong></td>
<td><p>Подписанная версия <a href="#size_t"><strong>SIZE_T</strong></a>.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef LONG_PTR SSIZE_T;</code></p></td>
</tr>
<tr class="odd">
<td><span id="TBYTE"></span><span id="tbyte"></span><strong>тбите</strong></td>
<td><p>Значение <a href="#wchar"><strong>WCHAR</strong></a> , если задан <strong>Юникод</strong> , в противном случае — <a href="#char"><strong>символ</strong></a> .</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef WCHAR TBYTE;
#else
 typedef unsigned char TBYTE;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="TCHAR"></span><span id="tchar"></span><strong>ГОЛОВК</strong></td>
<td><p>Значение <a href="#wchar"><strong>WCHAR</strong></a> , если задан <strong>Юникод</strong> , в противном случае — <a href="#char"><strong>символ</strong></a> .</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef WCHAR TCHAR;
#else
 typedef char TCHAR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="UCHAR"></span><span id="uchar"></span><strong>учар</strong></td>
<td><p><a href="#char"><strong>Знак</strong></a>без знака.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef unsigned char UCHAR;</code></p></td>
</tr>
<tr class="even">
<td><span id="UHALF_PTR"></span><span id="uhalf_ptr"></span><strong>UHALF_PTR</strong></td>
<td><p><a href="#half_ptr"><strong>HALF_PTR</strong></a>без знака. Используйте в структуре, содержащей указатель и два маленьких поля.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef _WIN64
 typedef unsigned int UHALF_PTR;
#else
 typedef unsigned short UHALF_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="UINT"></span><span id="uint"></span><strong>UINT</strong></td>
<td><p>Целое число без <a href="#int"><strong>знака.</strong></a> Диапазон — от 0 до 4294967295 десятичных знаков.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef unsigned int UINT;</code></p></td>
</tr>
<tr class="even">
<td><span id="UINT_PTR"></span><span id="uint_ptr"></span><strong>UINT_PTR</strong></td>
<td><p><a href="#int_ptr"><strong>INT_PTR</strong></a>без знака.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64)
 typedef unsigned __int64 UINT_PTR;
#else
 typedef unsigned int UINT_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="UINT8"></span><span id="uint8"></span><strong>UINT8</strong></td>
<td><p><a href="#int8"><strong>INT8</strong></a>без знака.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef unsigned  char UINT8;</code></p></td>
</tr>
<tr class="even">
<td><span id="UINT16"></span><span id="uint16"></span><strong>UINT16</strong></td>
<td><p>Неподписанная <a href="#int16"><strong>INT16</strong></a>.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef unsigned  short UINT16;</code></p></td>
</tr>
<tr class="odd">
<td><span id="UINT32"></span><span id="uint32"></span><strong>ЗНАЧЕНИЕМ</strong></td>
<td><p><a href="#int32"><strong>Int32</strong></a>без знака. Диапазон — от 0 до 4294967295 десятичных знаков.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef unsigned int UINT32;</code></p></td>
</tr>
<tr class="even">
<td><span id="UINT64"></span><span id="uint64"></span><strong>UINT64</strong></td>
<td><p><a href="#int64"><strong>Int64</strong></a>без знака. Диапазон — от 0 до 18446744073709551615 Decimal.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef usigned __int 64 UINT64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="ULONG"></span><span id="ulong"></span><strong>ULONG</strong></td>
<td><p><a href="#long"><strong>Длинное</strong></a>целое без знака. Диапазон — от 0 до 4294967295 десятичных знаков.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef unsigned long ULONG;</code></p></td>
</tr>
<tr class="even">
<td><span id="ULONGLONG"></span><span id="ulonglong"></span><strong>улонглонг</strong></td>
<td><p>64-разрядное целое число без знака. Диапазон — от 0 до 18446744073709551615 Decimal.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if !defined(_M_IX86)
 typedef unsigned __int64 ULONGLONG;
#else
 typedef double ULONGLONG;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="ULONG_PTR"></span><span id="ulong_ptr"></span><strong>ULONG_PTR</strong></td>
<td><p><a href="#long_ptr"><strong>LONG_PTR</strong></a>без знака.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64)
 typedef unsigned __int64 ULONG_PTR;
#else
 typedef unsigned long ULONG_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="ULONG32"></span><span id="ulong32"></span><strong>ULONG32</strong></td>
<td><p>Неподписанный <a href="#long32"><strong>LONG32</strong></a>. Диапазон — от 0 до 4294967295 десятичных знаков.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef unsigned int ULONG32;</code></p></td>
</tr>
<tr class="odd">
<td><span id="ULONG64"></span><span id="ulong64"></span><strong>ULONG64</strong></td>
<td><p>Неподписанный <a href="#long64"><strong>LONG64</strong></a>. Диапазон — от 0 до 18446744073709551615 Decimal.</p>
<p>Этот тип объявляется в Басетсд. h следующим образом:</p>
<p><code>typedef unsigned __int64 ULONG64;</code></p></td>
</tr>
<tr class="even">
<td><span id="UNICODE_STRING"></span><span id="unicode_string"></span><strong>UNICODE_STRING</strong></td>
<td><p>Строка Юникода.</p>
<p>Этот тип объявляется в Винтернл. h следующим образом:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>typedef struct _UNICODE_STRING {
  USHORT  Length;
  USHORT  MaximumLength;
  PWSTR  Buffer;
} UNICODE_STRING;
typedef UNICODE_STRING *PUNICODE_STRING;
typedef const UNICODE_STRING *PCUNICODE_STRING;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="USHORT"></span><span id="ushort"></span><strong>USHORT</strong></td>
<td><p><a href="#short"><strong>Короткое</strong></a>целое без знака. Диапазон — от 0 до 65535 десятичных знаков.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef unsigned short USHORT;</code></p></td>
</tr>
<tr class="even">
<td><span id="USN"></span><span id="usn"></span><strong>ЖУРНАЛЫ</strong></td>
<td><p>Порядковый номер обновления (USN).</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<p><code>typedef LONGLONG USN;</code></p></td>
</tr>
<tr class="odd">
<td><span id="VOID"></span><span id="void"></span><strong>VOID</strong></td>
<td><p>Любой тип.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<p><code>#define VOID void</code></p></td>
</tr>
<tr class="even">
<td><span id="WCHAR"></span><span id="wchar"></span><strong>WCHAR</strong></td>
<td><p>16-разрядный символ Юникода. Дополнительные сведения см. в разделе <a href="/windows/desktop/gdi/character-sets-used-by-fonts">наборы символов, используемые шрифтами</a>.</p>
<p>Этот тип объявлен в WinNT. h следующим образом:</p>
<p><code>typedef wchar_t WCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="WINAPI"></span><span id="winapi"></span><strong>WINAPI</strong></td>
<td><p>Соглашение о вызовах для системных функций.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>#define WINAPI __stdcall</code></p>
<p>Функции <strong>callback</strong>, <strong>WinAPI</strong>и <strong>апиентри</strong> используются для определения функций с помощью соглашения о вызовах __stdcall. большинство функций в API Windows объявляются с помощью <strong>WINAPI</strong>. Вы можете использовать <strong>обратный вызов</strong> для функций обратного вызова, которые реализуются, чтобы определить функцию как функцию обратного вызова.</p></td>
</tr>
<tr class="even">
<td><span id="WORD"></span><span id="word"></span><strong>СЛОВАМ</strong></td>
<td><p>16-разрядное целое число без знака. Диапазон — от 0 до 65535 десятичных знаков.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef unsigned short WORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="WPARAM"></span><span id="wparam"></span><strong>WPARAM</strong></td>
<td><p>Параметр сообщения.</p>
<p>Этот тип объявляется в Виндеф. h следующим образом:</p>
<p><code>typedef UINT_PTR WPARAM;</code></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                                                                                                                                                         |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                                                                                                                                |
| Header<br/>                   | <dl> <dt>Басетсд. h; </dt> <dt>Виндеф. h; </dt> Файл <dt>Winnt. h</dt> </dl> |
