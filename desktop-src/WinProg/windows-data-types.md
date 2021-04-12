---
title: Типы данных Windows (BaseTsd.h)
description: Типы данных, поддерживаемые Windows, используются для определения возвращаемых функцией значений, параметров функций и сообщений, а также членов структуры.
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
ms.openlocfilehash: 9bf3a23e816a78f0dcae9c2fbd6e6979b936451c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415400"
---
# <a name="windows-data-types"></a><span data-ttu-id="c85f5-280">Типы данных Windows</span><span class="sxs-lookup"><span data-stu-id="c85f5-280">Windows Data Types</span></span>

<span data-ttu-id="c85f5-281">Типы данных, поддерживаемые Windows, используются для определения возвращаемых функцией значений, параметров функций и сообщений, а также членов структуры.</span><span class="sxs-lookup"><span data-stu-id="c85f5-281">The data types supported by Windows are used to define function return values, function and message parameters, and structure members.</span></span> <span data-ttu-id="c85f5-282">Они определяют размер и значение этих элементов.</span><span class="sxs-lookup"><span data-stu-id="c85f5-282">They define the size and meaning of these elements.</span></span> <span data-ttu-id="c85f5-283">Дополнительные сведения о базовых типах данных C/C++ см. в разделе [диапазоны типов данных](/cpp/cpp/data-type-ranges?view=vs-2019).</span><span class="sxs-lookup"><span data-stu-id="c85f5-283">For more information about the underlying C/C++ data types, see [Data Type Ranges](/cpp/cpp/data-type-ranges?view=vs-2019).</span></span>

<span data-ttu-id="c85f5-284">Следующая таблица содержит следующие типы: символ, целое число, логическое значение, указатель и маркер.</span><span class="sxs-lookup"><span data-stu-id="c85f5-284">The following table contains the following types: character, integer, Boolean, pointer, and handle.</span></span> <span data-ttu-id="c85f5-285">Типы символьных, целочисленных и логических типов являются общими для большинства компиляторов C.</span><span class="sxs-lookup"><span data-stu-id="c85f5-285">The character, integer, and Boolean types are common to most C compilers.</span></span> <span data-ttu-id="c85f5-286">Большинство имен типов указателей начинаются с префикса P или LP.</span><span class="sxs-lookup"><span data-stu-id="c85f5-286">Most of the pointer-type names begin with a prefix of P or LP.</span></span> <span data-ttu-id="c85f5-287">Дескрипторы ссылаются на ресурс, который был загружен в память.</span><span class="sxs-lookup"><span data-stu-id="c85f5-287">Handles refer to a resource that has been loaded into memory.</span></span>

<span data-ttu-id="c85f5-288">Дополнительные сведения об обработке 64-разрядных целых чисел см. в разделе [большие целые числа](large-integers.md).</span><span class="sxs-lookup"><span data-stu-id="c85f5-288">For more information about handling 64-bit integers, see [Large Integers](large-integers.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c85f5-289">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c85f5-289">Data type</span></span></th>
<th><span data-ttu-id="c85f5-290">Описание</span><span class="sxs-lookup"><span data-stu-id="c85f5-290">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c85f5-291"><span id="APIENTRY"></span><span id="apientry"></span><strong>апиентри</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-291"><span id="APIENTRY"></span><span id="apientry"></span><strong>APIENTRY</strong></span></span></td>
<td><span data-ttu-id="c85f5-292">Соглашение о вызовах для системных функций.</span><span class="sxs-lookup"><span data-stu-id="c85f5-292">The calling convention for system functions.</span></span><br/> <span data-ttu-id="c85f5-293">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-293">This type is declared in WinDef.h as follows:</span></span><br/> <code>#define APIENTRY WINAPI</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-294"><span id="ATOM"></span><span id="atom"></span><strong>АТОМАР</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-294"><span id="ATOM"></span><span id="atom"></span><strong>ATOM</strong></span></span></td>
<td><span data-ttu-id="c85f5-295">Atom.</span><span class="sxs-lookup"><span data-stu-id="c85f5-295">An atom.</span></span> <span data-ttu-id="c85f5-296">Дополнительные сведения см. в разделе <a href="/windows/desktop/dataxchg/about-atom-tables">о таблицах Atom</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-296">For more information, see <a href="/windows/desktop/dataxchg/about-atom-tables">About Atom Tables</a>.</span></span><br/> <span data-ttu-id="c85f5-297">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-297">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef WORD ATOM;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-298"><span id="BOOL"></span><span id="bool"></span><strong>ЛОГИЧЕСКОМ</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-298"><span id="BOOL"></span><span id="bool"></span><strong>BOOL</strong></span></span></td>
<td><span data-ttu-id="c85f5-299">Логическая переменная (должна иметь <strong>значение true</strong> или <strong>false</strong>).</span><span class="sxs-lookup"><span data-stu-id="c85f5-299">A Boolean variable (should be <strong>TRUE</strong> or <strong>FALSE</strong>).</span></span><br/> <span data-ttu-id="c85f5-300">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-300">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef int BOOL;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-301"><span id="BOOLEAN"></span><span id="boolean"></span><strong>ЛОГИЧЕСКАЯ</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-301"><span id="BOOLEAN"></span><span id="boolean"></span><strong>BOOLEAN</strong></span></span></td>
<td><span data-ttu-id="c85f5-302">Логическая переменная (должна иметь <strong>значение true</strong> или <strong>false</strong>).</span><span class="sxs-lookup"><span data-stu-id="c85f5-302">A Boolean variable (should be <strong>TRUE</strong> or <strong>FALSE</strong>).</span></span><br/> <span data-ttu-id="c85f5-303">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-303">This type is declared in WinNT.h as follows:</span></span><br/> <code>typedef BYTE BOOLEAN;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-304"><span id="BYTE"></span><span id="byte"></span><strong>ДВУХБАЙТОВЫХ</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-304"><span id="BYTE"></span><span id="byte"></span><strong>BYTE</strong></span></span></td>
<td><span data-ttu-id="c85f5-305">Байт (8 бит).</span><span class="sxs-lookup"><span data-stu-id="c85f5-305">A byte (8 bits).</span></span><br/> <span data-ttu-id="c85f5-306">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-306">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef unsigned char BYTE;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-307"><span id="CALLBACK"></span><span id="callback"></span><strong>ОБРАТНОГО вызова</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-307"><span id="CALLBACK"></span><span id="callback"></span><strong>CALLBACK</strong></span></span></td>
<td><span data-ttu-id="c85f5-308">Соглашение о вызовах для функций обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="c85f5-308">The calling convention for callback functions.</span></span><br/> <span data-ttu-id="c85f5-309">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-309">This type is declared in WinDef.h as follows:</span></span><br/> <code>#define CALLBACK __stdcall</code><br/> <span data-ttu-id="c85f5-310">Функции <strong>callback</strong>, <strong>WinAPI</strong>и <strong>апиентри</strong> используются для определения функций с помощью соглашения о вызовах __stdcall.</span><span class="sxs-lookup"><span data-stu-id="c85f5-310"><strong>CALLBACK</strong>, <strong>WINAPI</strong>, and <strong>APIENTRY</strong> are all used to define functions with the __stdcall calling convention.</span></span> <span data-ttu-id="c85f5-311">Большинство функций в API Windows объявляются с помощью <strong>WinAPI</strong>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-311">Most functions in the Windows API are declared using <strong>WINAPI</strong>.</span></span> <span data-ttu-id="c85f5-312">Вы можете использовать <strong>обратный вызов</strong> для функций обратного вызова, которые реализуются, чтобы определить функцию как функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="c85f5-312">You may wish to use <strong>CALLBACK</strong> for the callback functions that you implement to help identify the function as a callback function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-313"><span id="CCHAR"></span><span id="cchar"></span><strong>CCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-313"><span id="CCHAR"></span><span id="cchar"></span><strong>CCHAR</strong></span></span></td>
<td><span data-ttu-id="c85f5-314">8-разрядный символ Windows (ANSI).</span><span class="sxs-lookup"><span data-stu-id="c85f5-314">An 8-bit Windows (ANSI) character.</span></span><br/> <span data-ttu-id="c85f5-315">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-315">This type is declared in WinNT.h as follows:</span></span><br/> <code>typedef char CCHAR;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-316"><span id="CHAR"></span><span id="char"></span><strong>ТИПА</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-316"><span id="CHAR"></span><span id="char"></span><strong>CHAR</strong></span></span></td>
<td><span data-ttu-id="c85f5-317">8-разрядный символ Windows (ANSI).</span><span class="sxs-lookup"><span data-stu-id="c85f5-317">An 8-bit Windows (ANSI) character.</span></span> <span data-ttu-id="c85f5-318">Дополнительные сведения см. в разделе <a href="/windows/desktop/gdi/character-sets-used-by-fonts">наборы символов, используемые шрифтами</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-318">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span><br/> <span data-ttu-id="c85f5-319">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-319">This type is declared in WinNT.h as follows:</span></span><br/> <code>typedef char CHAR;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-320"><span id="COLORREF"></span><span id="colorref"></span><strong>COLORREF</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-320"><span id="COLORREF"></span><span id="colorref"></span><strong>COLORREF</strong></span></span></td>
<td><span data-ttu-id="c85f5-321">Значение цвета красного, зеленого, синего (RGB) (32 бит).</span><span class="sxs-lookup"><span data-stu-id="c85f5-321">The red, green, blue (RGB) color value (32 bits).</span></span> <span data-ttu-id="c85f5-322">Сведения об этом типе см. в разделе <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c85f5-322">See <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> for information on this type.</span></span><br/> <span data-ttu-id="c85f5-323">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-323">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef DWORD COLORREF;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-324"><span id="CONST"></span><span id="const"></span><strong>ПОСТОЯННОГО</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-324"><span id="CONST"></span><span id="const"></span><strong>CONST</strong></span></span></td>
<td><span data-ttu-id="c85f5-325">Переменная, значение которой остается постоянной во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="c85f5-325">A variable whose value is to remain constant during execution.</span></span> <br/> <span data-ttu-id="c85f5-326">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-326">This type is declared in WinDef.h as follows:</span></span><br/> <code>#define CONST const</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-327"><span id="DWORD"></span><span id="dword"></span><strong>DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-327"><span id="DWORD"></span><span id="dword"></span><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="c85f5-328">32-разрядное целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="c85f5-328">A 32-bit unsigned integer.</span></span> <span data-ttu-id="c85f5-329">Диапазон — от 0 до 4294967295 десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="c85f5-329">The range is 0 through 4294967295 decimal.</span></span><br/> <span data-ttu-id="c85f5-330">Этот тип объявляется в Интсафе. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-330">This type is declared in IntSafe.h as follows:</span></span><br/> <code>typedef unsigned long DWORD;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-331"><span id="DWORDLONG"></span><span id="dwordlong"></span><strong>ОБЪЕКТА DWORDLONG</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-331"><span id="DWORDLONG"></span><span id="dwordlong"></span><strong>DWORDLONG</strong></span></span></td>
<td><span data-ttu-id="c85f5-332">64-разрядное целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="c85f5-332">A 64-bit unsigned integer.</span></span> <span data-ttu-id="c85f5-333">Диапазон — от 0 до 18446744073709551615 Decimal.</span><span class="sxs-lookup"><span data-stu-id="c85f5-333">The range is 0 through 18446744073709551615 decimal.</span></span><br/> <span data-ttu-id="c85f5-334">Этот тип объявляется в Интсафе. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-334">This type is declared in IntSafe.h as follows:</span></span><br/> <code>typedef unsigned __int64 DWORDLONG;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-335"><span id="DWORD_PTR"></span><span id="dword_ptr"></span><strong>DWORD_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-335"><span id="DWORD_PTR"></span><span id="dword_ptr"></span><strong>DWORD_PTR</strong></span></span></td>
<td><span data-ttu-id="c85f5-336">Тип long без знака для точности указателя.</span><span class="sxs-lookup"><span data-stu-id="c85f5-336">An unsigned long type for pointer precision.</span></span> <span data-ttu-id="c85f5-337">Используется при приведении указателя к длинному типу для выполнения арифметических операций с указателями.</span><span class="sxs-lookup"><span data-stu-id="c85f5-337">Use when casting a pointer to a long type to perform pointer arithmetic.</span></span> <span data-ttu-id="c85f5-338">(Также часто используется для общих 32-разрядных параметров, которые были расширены до 64 бит в 64-разрядной версии Windows.)</span><span class="sxs-lookup"><span data-stu-id="c85f5-338">(Also commonly used for general 32-bit parameters that have been extended to 64 bits in 64-bit Windows.)</span></span><br/> <span data-ttu-id="c85f5-339">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-339">This type is declared in BaseTsd.h as follows:</span></span><br/> <code>typedef ULONG_PTR DWORD_PTR;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-340"><span id="DWORD32"></span><span id="dword32"></span><strong>DWORD32</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-340"><span id="DWORD32"></span><span id="dword32"></span><strong>DWORD32</strong></span></span></td>
<td><span data-ttu-id="c85f5-341">32-разрядное целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="c85f5-341">A 32-bit unsigned integer.</span></span><br/> <span data-ttu-id="c85f5-342">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-342">This type is declared in BaseTsd.h as follows:</span></span><br/> <code>typedef unsigned int DWORD32;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-343"><span id="DWORD64"></span><span id="dword64"></span><strong>DWORD64</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-343"><span id="DWORD64"></span><span id="dword64"></span><strong>DWORD64</strong></span></span></td>
<td><span data-ttu-id="c85f5-344">64-разрядное целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="c85f5-344">A 64-bit unsigned integer.</span></span><br/> <span data-ttu-id="c85f5-345">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-345">This type is declared in BaseTsd.h as follows:</span></span><br/> <code>typedef unsigned __int64 DWORD64;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-346"><span id="FLOAT"></span><span id="float"></span><strong>СДЕЛАТЬ</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-346"><span id="FLOAT"></span><span id="float"></span><strong>FLOAT</strong></span></span></td>
<td><span data-ttu-id="c85f5-347">Переменная с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="c85f5-347">A floating-point variable.</span></span><br/> <span data-ttu-id="c85f5-348">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-348">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef float FLOAT;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-349"><span id="HACCEL"></span><span id="haccel"></span><strong>хакцел</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-349"><span id="HACCEL"></span><span id="haccel"></span><strong>HACCEL</strong></span></span></td>
<td><span data-ttu-id="c85f5-350">Маркер для <a href="/windows/desktop/menurc/keyboard-accelerators">таблицы сочетаний клавиш</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-350">A handle to an <a href="/windows/desktop/menurc/keyboard-accelerators">accelerator table</a>.</span></span><br/> <span data-ttu-id="c85f5-351">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-351">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef HANDLE HACCEL;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-352"><span id="HALF_PTR"></span><span id="half_ptr"></span><strong>HALF_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-352"><span id="HALF_PTR"></span><span id="half_ptr"></span><strong>HALF_PTR</strong></span></span></td>
<td><span data-ttu-id="c85f5-353">Половина размера указателя.</span><span class="sxs-lookup"><span data-stu-id="c85f5-353">Half the size of a pointer.</span></span> <span data-ttu-id="c85f5-354">Используйте в структуре, содержащей указатель и два маленьких поля.</span><span class="sxs-lookup"><span data-stu-id="c85f5-354">Use within a structure that contains a pointer and two small fields.</span></span><br/> <span data-ttu-id="c85f5-355">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-355">This type is declared in BaseTsd.h as follows:</span></span><br/> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c85f5-356">C++</span><span class="sxs-lookup"><span data-stu-id="c85f5-356">C++</span></span></th>
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
<td><span data-ttu-id="c85f5-357"><span id="HANDLE"></span><span id="handle"></span><strong>СПРАВИТЬСЯ</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-357"><span id="HANDLE"></span><span id="handle"></span><strong>HANDLE</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-358">Маркер объекта.</span><span class="sxs-lookup"><span data-stu-id="c85f5-358">A handle to an object.</span></span></p>
<p><span data-ttu-id="c85f5-359">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-359">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef PVOID HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-360"><span id="HBITMAP"></span><span id="hbitmap"></span><strong>хбитмап</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-360"><span id="HBITMAP"></span><span id="hbitmap"></span><strong>HBITMAP</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-361">Маркер <a href="/windows/desktop/gdi/bitmaps">точечного рисунка</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-361">A handle to a <a href="/windows/desktop/gdi/bitmaps">bitmap</a>.</span></span></p>
<p><span data-ttu-id="c85f5-362">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-362">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HBITMAP;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-363"><span id="HBRUSH"></span><span id="hbrush"></span><strong>хбруш</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-363"><span id="HBRUSH"></span><span id="hbrush"></span><strong>HBRUSH</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-364">Дескриптор <a href="/windows/desktop/gdi/brushes">кисти</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-364">A handle to a <a href="/windows/desktop/gdi/brushes">brush</a>.</span></span></p>
<p><span data-ttu-id="c85f5-365">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-365">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HBRUSH;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-366"><span id="HCOLORSPACE"></span><span id="hcolorspace"></span><strong>хколорспаце</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-366"><span id="HCOLORSPACE"></span><span id="hcolorspace"></span><strong>HCOLORSPACE</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-367">Маркер <a href="/previous-versions//dd316799(v=vs.85)">цветового пространства</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-367">A handle to a <a href="/previous-versions//dd316799(v=vs.85)">color space</a>.</span></span></p>
<p><span data-ttu-id="c85f5-368">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-368">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HCOLORSPACE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-369"><span id="HCONV"></span><span id="hconv"></span><strong>хконв</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-369"><span id="HCONV"></span><span id="hconv"></span><strong>HCONV</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-370">Маркер диалога динамического обмена данными (DDE).</span><span class="sxs-lookup"><span data-stu-id="c85f5-370">A handle to a dynamic data exchange (DDE) conversation.</span></span></p>
<p><span data-ttu-id="c85f5-371">Этот тип объявляется в Ддемл. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-371">This type is declared in Ddeml.h as follows:</span></span></p>
<p><code>typedef HANDLE HCONV;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-372"><span id="HCONVLIST"></span><span id="hconvlist"></span><strong>хконвлист</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-372"><span id="HCONVLIST"></span><span id="hconvlist"></span><strong>HCONVLIST</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-373">Маркер для списка сеансов DDE.</span><span class="sxs-lookup"><span data-stu-id="c85f5-373">A handle to a DDE conversation list.</span></span></p>
<p><span data-ttu-id="c85f5-374">Этот тип объявляется в Ддемл. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-374">This type is declared in Ddeml.h as follows:</span></span></p>
<p><code>typedef HANDLE HCONVLIST;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-375"><span id="HCURSOR"></span><span id="hcursor"></span><strong>хкурсор</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-375"><span id="HCURSOR"></span><span id="hcursor"></span><strong>HCURSOR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-376"><a href="/windows/desktop/menurc/cursors">Указатель на курсор</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-376">A handle to a <a href="/windows/desktop/menurc/cursors">cursor</a>.</span></span></p>
<p><span data-ttu-id="c85f5-377">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-377">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HICON HCURSOR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-378"><span id="HDC"></span><span id="hdc"></span><strong>HDC</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-378"><span id="HDC"></span><span id="hdc"></span><strong>HDC</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-379">Маркер <a href="/windows/desktop/gdi/device-context-types">контекста устройства</a> (DC).</span><span class="sxs-lookup"><span data-stu-id="c85f5-379">A handle to a <a href="/windows/desktop/gdi/device-context-types">device context</a> (DC).</span></span></p>
<p><span data-ttu-id="c85f5-380">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-380">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HDC;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-381"><span id="HDDEDATA"></span><span id="hddedata"></span><strong>хддедата</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-381"><span id="HDDEDATA"></span><span id="hddedata"></span><strong>HDDEDATA</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-382">Обработчик данных DDE.</span><span class="sxs-lookup"><span data-stu-id="c85f5-382">A handle to DDE data.</span></span></p>
<p><span data-ttu-id="c85f5-383">Этот тип объявляется в Ддемл. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-383">This type is declared in Ddeml.h as follows:</span></span></p>
<p><code>typedef HANDLE HDDEDATA;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-384"><span id="HDESK"></span><span id="hdesk"></span><strong>хдеск</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-384"><span id="HDESK"></span><span id="hdesk"></span><strong>HDESK</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-385">Маркер <a href="/windows/desktop/winstation/desktops">рабочего стола</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-385">A handle to a <a href="/windows/desktop/winstation/desktops">desktop</a>.</span></span></p>
<p><span data-ttu-id="c85f5-386">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-386">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HDESK;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-387"><span id="HDROP"></span><span id="hdrop"></span><strong>HDROP</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-387"><span id="HDROP"></span><span id="hdrop"></span><strong>HDROP</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-388">Маркер внутренней структуры перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="c85f5-388">A handle to an internal drop structure.</span></span></p>
<p><span data-ttu-id="c85f5-389">Этот тип объявляется в Шеллапи. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-389">This type is declared in ShellApi.h as follows:</span></span></p>
<p><code>typedef HANDLE HDROP;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-390"><span id="HDWP"></span><span id="hdwp"></span><strong>хдвп</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-390"><span id="HDWP"></span><span id="hdwp"></span><strong>HDWP</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-391">Указатель на структуру отложенной позицией окна.</span><span class="sxs-lookup"><span data-stu-id="c85f5-391">A handle to a deferred window position structure.</span></span></p>
<p><span data-ttu-id="c85f5-392">Этот тип объявлен в файле WinUser. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-392">This type is declared in WinUser.h as follows:</span></span></p>
<p><code>typedef HANDLE HDWP;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-393"><span id="HENHMETAFILE"></span><span id="henhmetafile"></span><strong>хенхметафиле</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-393"><span id="HENHMETAFILE"></span><span id="henhmetafile"></span><strong>HENHMETAFILE</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-394">Маркер <a href="/windows/desktop/gdi/metafiles">расширенного метафайла</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-394">A handle to an <a href="/windows/desktop/gdi/metafiles">enhanced metafile</a>.</span></span></p>
<p><span data-ttu-id="c85f5-395">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-395">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HENHMETAFILE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-396"><span id="HFILE"></span><span id="hfile"></span><strong>HFILE</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-396"><span id="HFILE"></span><span id="hfile"></span><strong>HFILE</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-397">Обработчик для файла, открытого с помощью <a href="/windows/desktop/api/winbase/nf-winbase-openfile"><strong>OpenFile</strong></a>, а не <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea"><strong>CreateFile</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-397">A handle to a file opened by <a href="/windows/desktop/api/winbase/nf-winbase-openfile"><strong>OpenFile</strong></a>, not <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea"><strong>CreateFile</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-398">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-398">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef int HFILE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-399"><span id="HFONT"></span><span id="hfont"></span><strong>хфонт</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-399"><span id="HFONT"></span><span id="hfont"></span><strong>HFONT</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-400">Маркер для <a href="/windows/desktop/gdi/about-fonts">шрифта</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-400">A handle to a <a href="/windows/desktop/gdi/about-fonts">font</a>.</span></span></p>
<p><span data-ttu-id="c85f5-401">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-401">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HFONT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-402"><span id="HGDIOBJ"></span><span id="hgdiobj"></span><strong>хгдиобж</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-402"><span id="HGDIOBJ"></span><span id="hgdiobj"></span><strong>HGDIOBJ</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-403">Маркер объекта GDI.</span><span class="sxs-lookup"><span data-stu-id="c85f5-403">A handle to a GDI object.</span></span></p>
<p><span data-ttu-id="c85f5-404">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-404">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HGDIOBJ;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-405"><span id="HGLOBAL"></span><span id="hglobal"></span><strong>хглобал</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-405"><span id="HGLOBAL"></span><span id="hglobal"></span><strong>HGLOBAL</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-406">Маркер глобального блока памяти.</span><span class="sxs-lookup"><span data-stu-id="c85f5-406">A handle to a global memory block.</span></span></p>
<p><span data-ttu-id="c85f5-407">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-407">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HGLOBAL;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-408"><span id="HHOOK"></span><span id="hhook"></span><strong>ххук</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-408"><span id="HHOOK"></span><span id="hhook"></span><strong>HHOOK</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-409">Маркер <a href="/windows/desktop/winmsg/hooks">обработчика</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-409">A handle to a <a href="/windows/desktop/winmsg/hooks">hook</a>.</span></span></p>
<p><span data-ttu-id="c85f5-410">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-410">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HHOOK;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-411"><span id="HICON"></span><span id="hicon"></span><strong>хикон</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-411"><span id="HICON"></span><span id="hicon"></span><strong>HICON</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-412">Маркер для <a href="/windows/desktop/menurc/icons">значка</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-412">A handle to an <a href="/windows/desktop/menurc/icons">icon</a>.</span></span></p>
<p><span data-ttu-id="c85f5-413">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-413">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HICON;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-414"><span id="HINSTANCE"></span><span id="hinstance"></span><strong>HINSTANCE</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-414"><span id="HINSTANCE"></span><span id="hinstance"></span><strong>HINSTANCE</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-415">Маркер экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c85f5-415">A handle to an instance.</span></span> <span data-ttu-id="c85f5-416">Это базовый адрес модуля в памяти.</span><span class="sxs-lookup"><span data-stu-id="c85f5-416">This is the base address of the module in memory.</span></span></p>
<p><span data-ttu-id="c85f5-417"><strong>Хмодуле</strong> и <strong>HINSTANCE</strong> уже сегодня, но в 16-разрядных окнах представлены различные вещи.</span><span class="sxs-lookup"><span data-stu-id="c85f5-417"><strong>HMODULE</strong> and <strong>HINSTANCE</strong> are the same today, but represented different things in 16-bit Windows.</span></span></p>
<p><span data-ttu-id="c85f5-418">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-418">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HINSTANCE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-419"><span id="HKEY"></span><span id="hkey"></span><strong>HKEY</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-419"><span id="HKEY"></span><span id="hkey"></span><strong>HKEY</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-420">Маркер раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="c85f5-420">A handle to a registry key.</span></span></p>
<p><span data-ttu-id="c85f5-421">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-421">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HKEY;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-422"><span id="HKL"></span><span id="hkl"></span><strong>HKL</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-422"><span id="HKL"></span><span id="hkl"></span><strong>HKL</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-423">Идентификатор языка ввода.</span><span class="sxs-lookup"><span data-stu-id="c85f5-423">An input locale identifier.</span></span></p>
<p><span data-ttu-id="c85f5-424">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-424">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HKL;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-425"><span id="HLOCAL"></span><span id="hlocal"></span><strong>хлокал</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-425"><span id="HLOCAL"></span><span id="hlocal"></span><strong>HLOCAL</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-426">Маркер локального блока памяти.</span><span class="sxs-lookup"><span data-stu-id="c85f5-426">A handle to a local memory block.</span></span></p>
<p><span data-ttu-id="c85f5-427">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-427">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HLOCAL;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-428"><span id="HMENU"></span><span id="hmenu"></span><strong>HMENU</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-428"><span id="HMENU"></span><span id="hmenu"></span><strong>HMENU</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-429">Маркер <a href="/windows/desktop/menurc/menus">меню</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-429">A handle to a <a href="/windows/desktop/menurc/menus">menu</a>.</span></span></p>
<p><span data-ttu-id="c85f5-430">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-430">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HMENU;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-431"><span id="HMETAFILE"></span><span id="hmetafile"></span><strong>хметафиле</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-431"><span id="HMETAFILE"></span><span id="hmetafile"></span><strong>HMETAFILE</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-432">Маркер для <a href="/windows/desktop/gdi/metafiles">метафайла</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-432">A handle to a <a href="/windows/desktop/gdi/metafiles">metafile</a>.</span></span></p>
<p><span data-ttu-id="c85f5-433">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-433">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HMETAFILE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-434"><span id="HMODULE"></span><span id="hmodule"></span><strong>хмодуле</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-434"><span id="HMODULE"></span><span id="hmodule"></span><strong>HMODULE</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-435">Обработчик для модуля.</span><span class="sxs-lookup"><span data-stu-id="c85f5-435">A handle to a module.</span></span> <span data-ttu-id="c85f5-436">— Это базовый адрес модуля в памяти.</span><span class="sxs-lookup"><span data-stu-id="c85f5-436">The is the base address of the module in memory.</span></span></p>
<p><span data-ttu-id="c85f5-437"><strong>Хмодуле</strong> и <strong>HINSTANCE</strong> одинаковы в текущих версиях Windows, но в 16-разрядных окнах представлены различные вещи.</span><span class="sxs-lookup"><span data-stu-id="c85f5-437"><strong>HMODULE</strong> and <strong>HINSTANCE</strong> are the same in current versions of Windows, but represented different things in 16-bit Windows.</span></span></p>
<p><span data-ttu-id="c85f5-438">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-438">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HINSTANCE HMODULE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-439"><span id="HMONITOR"></span><span id="hmonitor"></span><strong>хмонитор</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-439"><span id="HMONITOR"></span><span id="hmonitor"></span><strong>HMONITOR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-440">Маркер монитора.</span><span class="sxs-lookup"><span data-stu-id="c85f5-440">A handle to a display monitor.</span></span></p>
<p><span data-ttu-id="c85f5-441">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-441">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>if(WINVER >= 0x0500) typedef HANDLE HMONITOR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-442"><span id="HPALETTE"></span><span id="hpalette"></span><strong>хпалетте</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-442"><span id="HPALETTE"></span><span id="hpalette"></span><strong>HPALETTE</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-443">Маркер для палитры.</span><span class="sxs-lookup"><span data-stu-id="c85f5-443">A handle to a palette.</span></span></p>
<p><span data-ttu-id="c85f5-444">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-444">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HPALETTE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-445"><span id="HPEN"></span><span id="hpen"></span><strong>хпен</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-445"><span id="HPEN"></span><span id="hpen"></span><strong>HPEN</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-446">Указатель на <a href="/windows/desktop/gdi/pens">перо</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-446">A handle to a <a href="/windows/desktop/gdi/pens">pen</a>.</span></span></p>
<p><span data-ttu-id="c85f5-447">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-447">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HPEN;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-448"><span id="HRESULT"></span><span id="hresult"></span><strong>СОСТАВ</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-448"><span id="HRESULT"></span><span id="hresult"></span><strong>HRESULT</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-449">Коды возврата, используемые интерфейсами COM.</span><span class="sxs-lookup"><span data-stu-id="c85f5-449">The return codes used by COM interfaces.</span></span> <span data-ttu-id="c85f5-450">Дополнительные сведения см. <a href="/windows/desktop/com/structure-of-com-error-codes">в разделе структура кодов ошибок COM</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-450">For more information, see <a href="/windows/desktop/com/structure-of-com-error-codes">Structure of the COM Error Codes</a>.</span></span> <span data-ttu-id="c85f5-451">Чтобы проверить значение <strong>HRESULT</strong> , <a href="/windows/desktop/api/winerror/nf-winerror-succeeded"><strong>Используйте макросы,</strong></a> <a href="/windows/desktop/api/winerror/nf-winerror-failed"><strong>Завершившиеся сбоем и Failed</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c85f5-451">To test an <strong>HRESULT</strong> value, use the <a href="/windows/desktop/api/winerror/nf-winerror-failed"><strong>FAILED</strong></a> and <a href="/windows/desktop/api/winerror/nf-winerror-succeeded"><strong>SUCCEEDED</strong></a> macros.</span></span></p>
<p><span data-ttu-id="c85f5-452">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-452">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef LONG HRESULT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-453"><span id="HRGN"></span><span id="hrgn"></span><strong>хргн</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-453"><span id="HRGN"></span><span id="hrgn"></span><strong>HRGN</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-454">Маркер для <a href="/windows/desktop/gdi/regions">региона</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-454">A handle to a <a href="/windows/desktop/gdi/regions">region</a>.</span></span></p>
<p><span data-ttu-id="c85f5-455">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-455">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HRGN;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-456"><span id="HRSRC"></span><span id="hrsrc"></span><strong>хрсрк</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-456"><span id="HRSRC"></span><span id="hrsrc"></span><strong>HRSRC</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-457">Маркер ресурса.</span><span class="sxs-lookup"><span data-stu-id="c85f5-457">A handle to a resource.</span></span></p>
<p><span data-ttu-id="c85f5-458">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-458">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HRSRC;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-459"><span id="HSZ"></span><span id="hsz"></span><strong>хсз</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-459"><span id="HSZ"></span><span id="hsz"></span><strong>HSZ</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-460">Маркер строки DDE.</span><span class="sxs-lookup"><span data-stu-id="c85f5-460">A handle to a DDE string.</span></span></p>
<p><span data-ttu-id="c85f5-461">Этот тип объявляется в Ддемл. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-461">This type is declared in Ddeml.h as follows:</span></span></p>
<p><code>typedef HANDLE HSZ;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-462"><span id="HWINSTA"></span><span id="hwinsta"></span><strong>хвинста</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-462"><span id="HWINSTA"></span><span id="hwinsta"></span><strong>HWINSTA</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-463">Обработчик <a href="/windows/desktop/winstation/window-stations">оконной станции</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-463">A handle to a <a href="/windows/desktop/winstation/window-stations">window station</a>.</span></span></p>
<p><span data-ttu-id="c85f5-464">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-464">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE WINSTA;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-465"><span id="HWND"></span><span id="hwnd"></span><strong>HWND</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-465"><span id="HWND"></span><span id="hwnd"></span><strong>HWND</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-466">Маркер <a href="/windows/desktop/winmsg/windows">окна</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-466">A handle to a <a href="/windows/desktop/winmsg/windows">window</a>.</span></span></p>
<p><span data-ttu-id="c85f5-467">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-467">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HWND;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-468"><span id="INT"></span><span id="int"></span><strong>INT</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-468"><span id="INT"></span><span id="int"></span><strong>INT</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-469">32-разрядное знаковое целое число.</span><span class="sxs-lookup"><span data-stu-id="c85f5-469">A 32-bit signed integer.</span></span> <span data-ttu-id="c85f5-470">Диапазон значений — от-2147483648 до 2147483647.</span><span class="sxs-lookup"><span data-stu-id="c85f5-470">The range is -2147483648 through 2147483647 decimal.</span></span></p>
<p><span data-ttu-id="c85f5-471">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-471">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef int INT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-472"><span id="INT_PTR"></span><span id="int_ptr"></span><strong>INT_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-472"><span id="INT_PTR"></span><span id="int_ptr"></span><strong>INT_PTR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-473">Целочисленный тип со знаком для точности указателя.</span><span class="sxs-lookup"><span data-stu-id="c85f5-473">A signed integer type for pointer precision.</span></span> <span data-ttu-id="c85f5-474">Используется при приведении указателя на целое число для выполнения арифметических операций с указателями.</span><span class="sxs-lookup"><span data-stu-id="c85f5-474">Use when casting a pointer to an integer to perform pointer arithmetic.</span></span></p>
<p><span data-ttu-id="c85f5-475">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-475">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c85f5-476">C++</span><span class="sxs-lookup"><span data-stu-id="c85f5-476">C++</span></span></th>
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
<td><span data-ttu-id="c85f5-477"><span id="INT8"></span><span id="int8"></span><strong>INT8</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-477"><span id="INT8"></span><span id="int8"></span><strong>INT8</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-478">8-битовое целое число со знаком.</span><span class="sxs-lookup"><span data-stu-id="c85f5-478">An 8-bit signed integer.</span></span></p>
<p><span data-ttu-id="c85f5-479">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-479">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed char INT8;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-480"><span id="INT16"></span><span id="int16"></span><strong>INT16</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-480"><span id="INT16"></span><span id="int16"></span><strong>INT16</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-481">16-разрядное знаковое целое число.</span><span class="sxs-lookup"><span data-stu-id="c85f5-481">A 16-bit signed integer.</span></span></p>
<p><span data-ttu-id="c85f5-482">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-482">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed short INT16;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-483"><span id="INT32"></span><span id="int32"></span><strong>ТИПА</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-483"><span id="INT32"></span><span id="int32"></span><strong>INT32</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-484">32-разрядное знаковое целое число.</span><span class="sxs-lookup"><span data-stu-id="c85f5-484">A 32-bit signed integer.</span></span> <span data-ttu-id="c85f5-485">Диапазон значений — от-2147483648 до 2147483647.</span><span class="sxs-lookup"><span data-stu-id="c85f5-485">The range is -2147483648 through 2147483647 decimal.</span></span></p>
<p><span data-ttu-id="c85f5-486">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-486">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed int INT32;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-487"><span id="INT64"></span><span id="int64"></span><strong>INT64</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-487"><span id="INT64"></span><span id="int64"></span><strong>INT64</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-488">64-разрядное целое число со знаком.</span><span class="sxs-lookup"><span data-stu-id="c85f5-488">A 64-bit signed integer.</span></span> <span data-ttu-id="c85f5-489">Диапазон составляет от-9223372036854775808 до 9223372036854775807 десятичного числа.</span><span class="sxs-lookup"><span data-stu-id="c85f5-489">The range is -9223372036854775808 through 9223372036854775807 decimal.</span></span></p>
<p><span data-ttu-id="c85f5-490">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-490">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed __int64 INT64;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-491"><span id="LANGID"></span><span id="langid"></span><strong>НАДЕЖНО</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-491"><span id="LANGID"></span><span id="langid"></span><strong>LANGID</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-492">Идентификатор языка.</span><span class="sxs-lookup"><span data-stu-id="c85f5-492">A language identifier.</span></span> <span data-ttu-id="c85f5-493">Дополнительные сведения см. в разделе <a href="/windows/desktop/Intl/language-identifiers">идентификаторы языков</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-493">For more information, see <a href="/windows/desktop/Intl/language-identifiers">Language Identifiers</a>.</span></span></p>
<p><span data-ttu-id="c85f5-494">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-494">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef WORD LANGID;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-495"><span id="LCID"></span><span id="lcid"></span><strong>НАМНОГО</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-495"><span id="LCID"></span><span id="lcid"></span><strong>LCID</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-496">Идентификатор локали.</span><span class="sxs-lookup"><span data-stu-id="c85f5-496">A locale identifier.</span></span> <span data-ttu-id="c85f5-497">Дополнительные сведения см. в разделе <a href="/windows/desktop/Intl/locale-identifiers">идентификаторы языкового стандарта</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-497">For more information, see <a href="/windows/desktop/Intl/locale-identifiers">Locale Identifiers</a>.</span></span></p>
<p><span data-ttu-id="c85f5-498">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-498">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef DWORD LCID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-499"><span id="LCTYPE"></span><span id="lctype"></span><strong>LCTYPE</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-499"><span id="LCTYPE"></span><span id="lctype"></span><strong>LCTYPE</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-500">Тип сведений о языковых стандартах.</span><span class="sxs-lookup"><span data-stu-id="c85f5-500">A locale information type.</span></span> <span data-ttu-id="c85f5-501">Список см. в разделе <a href="/windows/desktop/Intl/locale-information-constants">константы сведений о языковых стандартах</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-501">For a list, see <a href="/windows/desktop/Intl/locale-information-constants">Locale Information Constants</a>.</span></span></p>
<p><span data-ttu-id="c85f5-502">Этот тип объявляется в Виннлс. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-502">This type is declared in WinNls.h as follows:</span></span></p>
<p><code>typedef DWORD LCTYPE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-503"><span id="LGRPID"></span><span id="lgrpid"></span><strong>лгрпид</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-503"><span id="LGRPID"></span><span id="lgrpid"></span><strong>LGRPID</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-504">Идентификатор языковой группы.</span><span class="sxs-lookup"><span data-stu-id="c85f5-504">A language group identifier.</span></span> <span data-ttu-id="c85f5-505">Список см. в разделе <a href="/windows/desktop/api/winnls/nf-winnls-enumlanguagegrouplocalesa"><strong>енумлангуажеграуплокалес</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-505">For a list, see <a href="/windows/desktop/api/winnls/nf-winnls-enumlanguagegrouplocalesa"><strong>EnumLanguageGroupLocales</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-506">Этот тип объявляется в Виннлс. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-506">This type is declared in WinNls.h as follows:</span></span></p>
<p><code>typedef DWORD LGRPID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-507"><span id="LONG"></span><span id="long"></span><strong>ПОДДЕРЖИВАЕМ</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-507"><span id="LONG"></span><span id="long"></span><strong>LONG</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-508">32-разрядное знаковое целое число.</span><span class="sxs-lookup"><span data-stu-id="c85f5-508">A 32-bit signed integer.</span></span> <span data-ttu-id="c85f5-509">Диапазон значений — от-2147483648 до 2147483647.</span><span class="sxs-lookup"><span data-stu-id="c85f5-509">The range is -2147483648 through 2147483647 decimal.</span></span></p>
<p><span data-ttu-id="c85f5-510">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-510">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef long LONG;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-511"><span id="LONGLONG"></span><span id="longlong"></span><strong>лонглонг</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-511"><span id="LONGLONG"></span><span id="longlong"></span><strong>LONGLONG</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-512">64-разрядное целое число со знаком.</span><span class="sxs-lookup"><span data-stu-id="c85f5-512">A 64-bit signed integer.</span></span> <span data-ttu-id="c85f5-513">Диапазон составляет от-9223372036854775808 до 9223372036854775807 десятичного числа.</span><span class="sxs-lookup"><span data-stu-id="c85f5-513">The range is -9223372036854775808 through 9223372036854775807 decimal.</span></span></p>
<p><span data-ttu-id="c85f5-514">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-514">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c85f5-515">C++</span><span class="sxs-lookup"><span data-stu-id="c85f5-515">C++</span></span></th>
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
<td><span data-ttu-id="c85f5-516"><span id="LONG_PTR"></span><span id="long_ptr"></span><strong>LONG_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-516"><span id="LONG_PTR"></span><span id="long_ptr"></span><strong>LONG_PTR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-517">Длинный тип со знаком для точности указателя.</span><span class="sxs-lookup"><span data-stu-id="c85f5-517">A signed long type for pointer precision.</span></span> <span data-ttu-id="c85f5-518">Используется при приведении указателя к типу long для выполнения арифметических операций с указателями.</span><span class="sxs-lookup"><span data-stu-id="c85f5-518">Use when casting a pointer to a long to perform pointer arithmetic.</span></span></p>
<p><span data-ttu-id="c85f5-519">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-519">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c85f5-520">C++</span><span class="sxs-lookup"><span data-stu-id="c85f5-520">C++</span></span></th>
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
<td><span data-ttu-id="c85f5-521"><span id="LONG32"></span><span id="long32"></span><strong>LONG32</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-521"><span id="LONG32"></span><span id="long32"></span><strong>LONG32</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-522">32-разрядное знаковое целое число.</span><span class="sxs-lookup"><span data-stu-id="c85f5-522">A 32-bit signed integer.</span></span> <span data-ttu-id="c85f5-523">Диапазон значений — от-2147483648 до 2147483647.</span><span class="sxs-lookup"><span data-stu-id="c85f5-523">The range is -2147483648 through 2147483647 decimal.</span></span></p>
<p><span data-ttu-id="c85f5-524">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-524">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed int LONG32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-525"><span id="LONG64"></span><span id="long64"></span><strong>LONG64</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-525"><span id="LONG64"></span><span id="long64"></span><strong>LONG64</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-526">64-разрядное целое число со знаком.</span><span class="sxs-lookup"><span data-stu-id="c85f5-526">A 64-bit signed integer.</span></span> <span data-ttu-id="c85f5-527">Диапазон составляет от-9223372036854775808 до 9223372036854775807 десятичного числа.</span><span class="sxs-lookup"><span data-stu-id="c85f5-527">The range is -9223372036854775808 through 9223372036854775807 decimal.</span></span></p>
<p><span data-ttu-id="c85f5-528">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-528">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef __int64 LONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-529"><span id="LPARAM"></span><span id="lparam"></span><strong>LPARAM</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-529"><span id="LPARAM"></span><span id="lparam"></span><strong>LPARAM</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-530">Параметр сообщения.</span><span class="sxs-lookup"><span data-stu-id="c85f5-530">A message parameter.</span></span></p>
<p><span data-ttu-id="c85f5-531">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-531">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef LONG_PTR LPARAM;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-532"><span id="LPBOOL"></span><span id="lpbool"></span><strong>лпбул</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-532"><span id="LPBOOL"></span><span id="lpbool"></span><strong>LPBOOL</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-533">Указатель на <a href="#bool"><strong>логическое</strong></a>значение.</span><span class="sxs-lookup"><span data-stu-id="c85f5-533">A pointer to a <a href="#bool"><strong>BOOL</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-534">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-534">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef BOOL far *LPBOOL;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-535"><span id="LPBYTE"></span><span id="lpbyte"></span><strong>LPBYTE</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-535"><span id="LPBYTE"></span><span id="lpbyte"></span><strong>LPBYTE</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-536">Указатель на <a href="#byte"><strong>байт</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-536">A pointer to a <a href="#byte"><strong>BYTE</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-537">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-537">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef BYTE far *LPBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-538"><span id="LPCOLORREF"></span><span id="lpcolorref"></span><strong>лпколорреф</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-538"><span id="LPCOLORREF"></span><span id="lpcolorref"></span><strong>LPCOLORREF</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-539">Указатель на значение <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c85f5-539">A pointer to a <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> value.</span></span></p>
<p><span data-ttu-id="c85f5-540">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-540">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef DWORD *LPCOLORREF;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-541"><span id="LPCSTR"></span><span id="lpcstr"></span><strong>LPCSTR</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-541"><span id="LPCSTR"></span><span id="lpcstr"></span><strong>LPCSTR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-542">Указатель на константную строку, завершающуюся нулем, в 8-разрядных символах Windows (ANSI).</span><span class="sxs-lookup"><span data-stu-id="c85f5-542">A pointer to a constant null-terminated string of 8-bit Windows (ANSI) characters.</span></span> <span data-ttu-id="c85f5-543">Дополнительные сведения см. в разделе <a href="/windows/desktop/gdi/character-sets-used-by-fonts">наборы символов, используемые шрифтами</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-543">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="c85f5-544">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-544">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef __nullterminated CONST CHAR *LPCSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-545"><span id="LPCTSTR"></span><span id="lpctstr"></span><strong>LPCTSTR</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-545"><span id="LPCTSTR"></span><span id="lpctstr"></span><strong>LPCTSTR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-546"><a href="#lpcwstr"><strong>Лпквстр</strong></a> , если определен <strong>Юникод</strong> , <a href="#lpcstr"><strong>LPCSTR</strong></a> в противном случае.</span><span class="sxs-lookup"><span data-stu-id="c85f5-546">An <a href="#lpcwstr"><strong>LPCWSTR</strong></a> if <strong>UNICODE</strong> is defined, an <a href="#lpcstr"><strong>LPCSTR</strong></a> otherwise.</span></span> <span data-ttu-id="c85f5-547">Дополнительные сведения см. в разделе <a href="/windows/desktop/Intl/windows-data-types-for-strings">типы данных Windows для строк</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-547">For more information, see <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Data Types for Strings</a>.</span></span></p>
<p><span data-ttu-id="c85f5-548">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-548">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c85f5-549">C++</span><span class="sxs-lookup"><span data-stu-id="c85f5-549">C++</span></span></th>
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
<td><span data-ttu-id="c85f5-550"><span id="LPCVOID"></span><span id="lpcvoid"></span><strong>лпквоид</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-550"><span id="LPCVOID"></span><span id="lpcvoid"></span><strong>LPCVOID</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-551">Указатель на константу любого типа.</span><span class="sxs-lookup"><span data-stu-id="c85f5-551">A pointer to a constant of any type.</span></span></p>
<p><span data-ttu-id="c85f5-552">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-552">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef CONST void *LPCVOID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-553"><span id="LPCWSTR"></span><span id="lpcwstr"></span><strong>лпквстр</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-553"><span id="LPCWSTR"></span><span id="lpcwstr"></span><strong>LPCWSTR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-554">Указатель на константную строку из 16-разрядных символов Юникода, завершающуюся нулем.</span><span class="sxs-lookup"><span data-stu-id="c85f5-554">A pointer to a constant null-terminated string of 16-bit Unicode characters.</span></span> <span data-ttu-id="c85f5-555">Дополнительные сведения см. в разделе <a href="/windows/desktop/gdi/character-sets-used-by-fonts">наборы символов, используемые шрифтами</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-555">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="c85f5-556">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-556">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CONST WCHAR *LPCWSTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-557"><span id="LPDWORD"></span><span id="lpdword"></span><strong>лпдворд</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-557"><span id="LPDWORD"></span><span id="lpdword"></span><strong>LPDWORD</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-558">Указатель на <a href="#dword"><strong>DWORD</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-558">A pointer to a <a href="#dword"><strong>DWORD</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-559">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-559">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef DWORD *LPDWORD;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-560"><span id="LPHANDLE"></span><span id="lphandle"></span><strong>лфандле</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-560"><span id="LPHANDLE"></span><span id="lphandle"></span><strong>LPHANDLE</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-561">Указатель на <a href="#handle"><strong>маркер</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-561">A pointer to a <a href="#handle"><strong>HANDLE</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-562">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-562">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE *LPHANDLE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-563"><span id="LPINT"></span><span id="lpint"></span><strong>лпинт</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-563"><span id="LPINT"></span><span id="lpint"></span><strong>LPINT</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-564">Указатель на <a href="#int"><strong>тип int</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-564">A pointer to an <a href="#int"><strong>INT</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-565">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-565">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef int *LPINT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-566"><span id="LPLONG"></span><span id="lplong"></span><strong>лплонг</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-566"><span id="LPLONG"></span><span id="lplong"></span><strong>LPLONG</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-567">Указатель на значение <a href="#long"><strong>типа Long</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-567">A pointer to a <a href="#long"><strong>LONG</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-568">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-568">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef long *LPLONG;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-569"><span id="LPSTR"></span><span id="lpstr"></span><strong>LPSTR</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-569"><span id="LPSTR"></span><span id="lpstr"></span><strong>LPSTR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-570">Указатель на строку в 8-разрядных символах Windows (ANSI), завершающуюся нулем.</span><span class="sxs-lookup"><span data-stu-id="c85f5-570">A pointer to a null-terminated string of 8-bit Windows (ANSI) characters.</span></span> <span data-ttu-id="c85f5-571">Дополнительные сведения см. в разделе <a href="/windows/desktop/gdi/character-sets-used-by-fonts">наборы символов, используемые шрифтами</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-571">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="c85f5-572">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-572">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CHAR *LPSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-573"><span id="LPTSTR"></span><span id="lptstr"></span><strong>LPTSTR</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-573"><span id="LPTSTR"></span><span id="lptstr"></span><strong>LPTSTR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-574"><a href="#lpwstr"><strong>LPWSTR</strong></a> , если определен <strong>Юникод</strong> , <a href="#lpstr"><strong>LPSTR</strong></a> в противном случае.</span><span class="sxs-lookup"><span data-stu-id="c85f5-574">An <a href="#lpwstr"><strong>LPWSTR</strong></a> if <strong>UNICODE</strong> is defined, an <a href="#lpstr"><strong>LPSTR</strong></a> otherwise.</span></span> <span data-ttu-id="c85f5-575">Дополнительные сведения см. в разделе <a href="/windows/desktop/Intl/windows-data-types-for-strings">типы данных Windows для строк</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-575">For more information, see <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Data Types for Strings</a>.</span></span></p>
<p><span data-ttu-id="c85f5-576">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-576">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c85f5-577">C++</span><span class="sxs-lookup"><span data-stu-id="c85f5-577">C++</span></span></th>
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
<td><span data-ttu-id="c85f5-578"><span id="LPVOID"></span><span id="lpvoid"></span><strong>лпвоид</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-578"><span id="LPVOID"></span><span id="lpvoid"></span><strong>LPVOID</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-579">Указатель на любой тип.</span><span class="sxs-lookup"><span data-stu-id="c85f5-579">A pointer to any type.</span></span></p>
<p><span data-ttu-id="c85f5-580">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-580">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef void *LPVOID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-581"><span id="LPWORD"></span><span id="lpword"></span><strong>лпворд</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-581"><span id="LPWORD"></span><span id="lpword"></span><strong>LPWORD</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-582">Указатель на <a href="#word"><strong>слово</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-582">A pointer to a <a href="#word"><strong>WORD</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-583">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-583">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef WORD *LPWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-584"><span id="LPWSTR"></span><span id="lpwstr"></span><strong>LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-584"><span id="LPWSTR"></span><span id="lpwstr"></span><strong>LPWSTR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-585">Указатель на строку из 16-разрядных символов Юникода, завершающуюся нулем.</span><span class="sxs-lookup"><span data-stu-id="c85f5-585">A pointer to a null-terminated string of 16-bit Unicode characters.</span></span> <span data-ttu-id="c85f5-586">Дополнительные сведения см. в разделе <a href="/windows/desktop/gdi/character-sets-used-by-fonts">наборы символов, используемые шрифтами</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-586">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="c85f5-587">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-587">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef WCHAR *LPWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-588"><span id="LRESULT"></span><span id="lresult"></span><strong>LRESULT</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-588"><span id="LRESULT"></span><span id="lresult"></span><strong>LRESULT</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-589">Подписанный результат обработки сообщения.</span><span class="sxs-lookup"><span data-stu-id="c85f5-589">Signed result of message processing.</span></span></p>
<p><span data-ttu-id="c85f5-590">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-590">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef LONG_PTR LRESULT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-591"><span id="PBOOL"></span><span id="pbool"></span><strong>пбул</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-591"><span id="PBOOL"></span><span id="pbool"></span><strong>PBOOL</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-592">Указатель на <a href="#bool"><strong>логическое</strong></a>значение.</span><span class="sxs-lookup"><span data-stu-id="c85f5-592">A pointer to a <a href="#bool"><strong>BOOL</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-593">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-593">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef BOOL *PBOOL;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-594"><span id="PBOOLEAN"></span><span id="pboolean"></span><strong>пбулеан</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-594"><span id="PBOOLEAN"></span><span id="pboolean"></span><strong>PBOOLEAN</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-595">Указатель на <a href="#boolean"><strong>логическое значение</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-595">A pointer to a <a href="#boolean"><strong>BOOLEAN</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-596">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-596">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef BOOLEAN *PBOOLEAN;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-597"><span id="PBYTE"></span><span id="pbyte"></span><strong>пбите</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-597"><span id="PBYTE"></span><span id="pbyte"></span><strong>PBYTE</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-598">Указатель на <a href="#byte"><strong>байт</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-598">A pointer to a <a href="#byte"><strong>BYTE</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-599">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-599">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef BYTE *PBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-600"><span id="PCHAR"></span><span id="pchar"></span><strong>пчар</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-600"><span id="PCHAR"></span><span id="pchar"></span><strong>PCHAR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-601">Указатель на <a href="#char"><strong>символ</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-601">A pointer to a <a href="#char"><strong>CHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-602">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-602">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CHAR *PCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-603"><span id="PCSTR"></span><span id="pcstr"></span><strong>пкстр</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-603"><span id="PCSTR"></span><span id="pcstr"></span><strong>PCSTR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-604">Указатель на константную строку, завершающуюся нулем, в 8-разрядных символах Windows (ANSI).</span><span class="sxs-lookup"><span data-stu-id="c85f5-604">A pointer to a constant null-terminated string of 8-bit Windows (ANSI) characters.</span></span> <span data-ttu-id="c85f5-605">Дополнительные сведения см. в разделе <a href="/windows/desktop/gdi/character-sets-used-by-fonts">наборы символов, используемые шрифтами</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-605">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="c85f5-606">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-606">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CONST CHAR *PCSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-607"><span id="PCTSTR"></span><span id="pctstr"></span><strong>пктстр</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-607"><span id="PCTSTR"></span><span id="pctstr"></span><strong>PCTSTR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-608"><a href="#pcwstr"><strong>Пквстр</strong></a> , если определен <strong>Юникод</strong> , <a href="#pcstr"><strong>пкстр</strong></a> в противном случае.</span><span class="sxs-lookup"><span data-stu-id="c85f5-608">A <a href="#pcwstr"><strong>PCWSTR</strong></a> if <strong>UNICODE</strong> is defined, a <a href="#pcstr"><strong>PCSTR</strong></a> otherwise.</span></span> <span data-ttu-id="c85f5-609">Дополнительные сведения см. в разделе <a href="/windows/desktop/Intl/windows-data-types-for-strings">типы данных Windows для строк</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-609">For more information, see <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Data Types for Strings</a>.</span></span></p>
<p><span data-ttu-id="c85f5-610">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-610">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c85f5-611">C++</span><span class="sxs-lookup"><span data-stu-id="c85f5-611">C++</span></span></th>
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
<td><span data-ttu-id="c85f5-612"><span id="PCWSTR"></span><span id="pcwstr"></span><strong>пквстр</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-612"><span id="PCWSTR"></span><span id="pcwstr"></span><strong>PCWSTR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-613">Указатель на константную строку из 16-разрядных символов Юникода, завершающуюся нулем.</span><span class="sxs-lookup"><span data-stu-id="c85f5-613">A pointer to a constant null-terminated string of 16-bit Unicode characters.</span></span> <span data-ttu-id="c85f5-614">Дополнительные сведения см. в разделе <a href="/windows/desktop/gdi/character-sets-used-by-fonts">наборы символов, используемые шрифтами</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-614">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="c85f5-615">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-615">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CONST WCHAR *PCWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-616"><span id="PDWORD"></span><span id="pdword"></span><strong>пдворд</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-616"><span id="PDWORD"></span><span id="pdword"></span><strong>PDWORD</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-617">Указатель на <a href="#dword"><strong>DWORD</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-617">A pointer to a <a href="#dword"><strong>DWORD</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-618">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-618">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef DWORD *PDWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-619"><span id="PDWORDLONG"></span><span id="pdwordlong"></span><strong>пдвордлонг</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-619"><span id="PDWORDLONG"></span><span id="pdwordlong"></span><strong>PDWORDLONG</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-620">Указатель на <a href="#dwordlong"><strong>объекта dwordlong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-620">A pointer to a <a href="#dwordlong"><strong>DWORDLONG</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-621">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-621">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef DWORDLONG *PDWORDLONG;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-622"><span id="PDWORD_PTR"></span><span id="pdword_ptr"></span><strong>PDWORD_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-622"><span id="PDWORD_PTR"></span><span id="pdword_ptr"></span><strong>PDWORD_PTR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-623">Указатель на <a href="#dword_ptr"><strong>DWORD_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-623">A pointer to a <a href="#dword_ptr"><strong>DWORD_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-624">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-624">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef DWORD_PTR *PDWORD_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-625"><span id="PDWORD32"></span><span id="pdword32"></span><strong>PDWORD32</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-625"><span id="PDWORD32"></span><span id="pdword32"></span><strong>PDWORD32</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-626">Указатель на <a href="#dword32"><strong>DWORD32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-626">A pointer to a <a href="#dword32"><strong>DWORD32</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-627">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-627">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef DWORD32 *PDWORD32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-628"><span id="PDWORD64"></span><span id="pdword64"></span><strong>PDWORD64</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-628"><span id="PDWORD64"></span><span id="pdword64"></span><strong>PDWORD64</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-629">Указатель на <a href="#dword64"><strong>DWORD64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-629">A pointer to a <a href="#dword64"><strong>DWORD64</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-630">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-630">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef DWORD64 *PDWORD64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-631"><span id="PFLOAT"></span><span id="pfloat"></span><strong>пфлоат</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-631"><span id="PFLOAT"></span><span id="pfloat"></span><strong>PFLOAT</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-632">Указатель на число с <a href="#float"><strong>плавающей запятой</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-632">A pointer to a <a href="#float"><strong>FLOAT</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-633">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-633">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef FLOAT *PFLOAT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-634"><span id="PHALF_PTR"></span><span id="phalf_ptr"></span><strong>PHALF_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-634"><span id="PHALF_PTR"></span><span id="phalf_ptr"></span><strong>PHALF_PTR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-635">Указатель на <a href="#half_ptr"><strong>HALF_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-635">A pointer to a <a href="#half_ptr"><strong>HALF_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-636">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-636">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c85f5-637">C++</span><span class="sxs-lookup"><span data-stu-id="c85f5-637">C++</span></span></th>
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
<td><span data-ttu-id="c85f5-638"><span id="PHANDLE"></span><span id="phandle"></span><strong>фандле</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-638"><span id="PHANDLE"></span><span id="phandle"></span><strong>PHANDLE</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-639">Указатель на <a href="#handle"><strong>маркер</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-639">A pointer to a <a href="#handle"><strong>HANDLE</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-640">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-640">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef HANDLE *PHANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-641"><span id="PHKEY"></span><span id="phkey"></span><strong>фкэй</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-641"><span id="PHKEY"></span><span id="phkey"></span><strong>PHKEY</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-642">Указатель на <a href="#hkey"><strong>hKey</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-642">A pointer to an <a href="#hkey"><strong>HKEY</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-643">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-643">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HKEY *PHKEY;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-644"><span id="PINT"></span><span id="pint"></span><strong>КОМАНДУ</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-644"><span id="PINT"></span><span id="pint"></span><strong>PINT</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-645">Указатель на <a href="#int"><strong>тип int</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-645">A pointer to an <a href="#int"><strong>INT</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-646">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-646">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef int *PINT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-647"><span id="PINT_PTR"></span><span id="pint_ptr"></span><strong>PINT_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-647"><span id="PINT_PTR"></span><span id="pint_ptr"></span><strong>PINT_PTR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-648">Указатель на <a href="#int_ptr"><strong>INT_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-648">A pointer to an <a href="#int_ptr"><strong>INT_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-649">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-649">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT_PTR *PINT_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-650"><span id="PINT8"></span><span id="pint8"></span><strong>PINT8</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-650"><span id="PINT8"></span><span id="pint8"></span><strong>PINT8</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-651">Указатель на <a href="#int8"><strong>INT8</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-651">A pointer to an <a href="#int8"><strong>INT8</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-652">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-652">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT8 *PINT8;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-653"><span id="PINT16"></span><span id="pint16"></span><strong>PINT16</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-653"><span id="PINT16"></span><span id="pint16"></span><strong>PINT16</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-654">Указатель на значение <a href="#int16"><strong>INT16</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-654">A pointer to an <a href="#int16"><strong>INT16</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-655">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-655">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT16 *PINT16;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-656"><span id="PINT32"></span><span id="pint32"></span><strong>PINT32</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-656"><span id="PINT32"></span><span id="pint32"></span><strong>PINT32</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-657">Указатель на <a href="#int32"><strong>Int32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-657">A pointer to an <a href="#int32"><strong>INT32</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-658">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-658">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT32 *PINT32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-659"><span id="PINT64"></span><span id="pint64"></span><strong>PINT64</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-659"><span id="PINT64"></span><span id="pint64"></span><strong>PINT64</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-660">Указатель на <a href="#int64"><strong>Int64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-660">A pointer to an <a href="#int64"><strong>INT64</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-661">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-661">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT64 *PINT64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-662"><span id="PLCID"></span><span id="plcid"></span><strong>плЦид</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-662"><span id="PLCID"></span><span id="plcid"></span><strong>PLCID</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-663">Указатель на <a href="#lcid"><strong>код языка</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-663">A pointer to an <a href="#lcid"><strong>LCID</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-664">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-664">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef PDWORD PLCID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-665"><span id="PLONG"></span><span id="plong"></span><strong>плонг</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-665"><span id="PLONG"></span><span id="plong"></span><strong>PLONG</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-666">Указатель на значение <a href="#long"><strong>типа Long</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-666">A pointer to a <a href="#long"><strong>LONG</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-667">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-667">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef LONG *PLONG;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-668"><span id="PLONGLONG"></span><span id="plonglong"></span><strong>плонглонг</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-668"><span id="PLONGLONG"></span><span id="plonglong"></span><strong>PLONGLONG</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-669">Указатель на <a href="#longlong"><strong>лонглонг</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-669">A pointer to a <a href="#longlong"><strong>LONGLONG</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-670">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-670">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef LONGLONG *PLONGLONG;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-671"><span id="PLONG_PTR"></span><span id="plong_ptr"></span><strong>PLONG_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-671"><span id="PLONG_PTR"></span><span id="plong_ptr"></span><strong>PLONG_PTR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-672">Указатель на <a href="#long_ptr"><strong>LONG_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-672">A pointer to a <a href="#long_ptr"><strong>LONG_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-673">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-673">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef LONG_PTR *PLONG_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-674"><span id="PLONG32"></span><span id="plong32"></span><strong>PLONG32</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-674"><span id="PLONG32"></span><span id="plong32"></span><strong>PLONG32</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-675">Указатель на <a href="#long32"><strong>LONG32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-675">A pointer to a <a href="#long32"><strong>LONG32</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-676">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-676">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef LONG32 *PLONG32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-677"><span id="PLONG64"></span><span id="plong64"></span><strong>PLONG64</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-677"><span id="PLONG64"></span><span id="plong64"></span><strong>PLONG64</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-678">Указатель на <a href="#long64"><strong>LONG64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-678">A pointer to a <a href="#long64"><strong>LONG64</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-679">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-679">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef LONG64 *PLONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-680"><span id="POINTER_32"></span><span id="pointer_32"></span><strong>POINTER_32</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-680"><span id="POINTER_32"></span><span id="pointer_32"></span><strong>POINTER_32</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-681">32-разрядный указатель.</span><span class="sxs-lookup"><span data-stu-id="c85f5-681">A 32-bit pointer.</span></span> <span data-ttu-id="c85f5-682">В 32-разрядной системе это собственный указатель.</span><span class="sxs-lookup"><span data-stu-id="c85f5-682">On a 32-bit system, this is a native pointer.</span></span> <span data-ttu-id="c85f5-683">В 64-разрядной системе это усеченный 64-разрядный указатель.</span><span class="sxs-lookup"><span data-stu-id="c85f5-683">On a 64-bit system, this is a truncated 64-bit pointer.</span></span></p>
<p><span data-ttu-id="c85f5-684">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-684">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c85f5-685">C++</span><span class="sxs-lookup"><span data-stu-id="c85f5-685">C++</span></span></th>
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
<td><span data-ttu-id="c85f5-686"><span id="POINTER_64"></span><span id="pointer_64"></span><strong>POINTER_64</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-686"><span id="POINTER_64"></span><span id="pointer_64"></span><strong>POINTER_64</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-687">64-разрядный указатель.</span><span class="sxs-lookup"><span data-stu-id="c85f5-687">A 64-bit pointer.</span></span> <span data-ttu-id="c85f5-688">В 64-разрядной системе это собственный указатель.</span><span class="sxs-lookup"><span data-stu-id="c85f5-688">On a 64-bit system, this is a native pointer.</span></span> <span data-ttu-id="c85f5-689">В 32-разрядной системе это расширенный по знаку 32-разрядный указатель.</span><span class="sxs-lookup"><span data-stu-id="c85f5-689">On a 32-bit system, this is a sign-extended 32-bit pointer.</span></span></p>
<p><span data-ttu-id="c85f5-690">Обратите внимание, что нельзя считать, что состояние старших битов указателя не является надежным.</span><span class="sxs-lookup"><span data-stu-id="c85f5-690">Note that it is not safe to assume the state of the high pointer bit.</span></span></p>
<p><span data-ttu-id="c85f5-691">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-691">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c85f5-692">C++</span><span class="sxs-lookup"><span data-stu-id="c85f5-692">C++</span></span></th>
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
<td><span data-ttu-id="c85f5-693"><span id="POINTER_SIGNED"></span><span id="pointer_signed"></span><strong>POINTER_SIGNED</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-693"><span id="POINTER_SIGNED"></span><span id="pointer_signed"></span><strong>POINTER_SIGNED</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-694">Указатель со знаком.</span><span class="sxs-lookup"><span data-stu-id="c85f5-694">A signed pointer.</span></span></p>
<p><span data-ttu-id="c85f5-695">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-695">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>#define POINTER_SIGNED __sptr</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-696"><span id="POINTER_UNSIGNED"></span><span id="pointer_unsigned"></span><strong>POINTER_UNSIGNED</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-696"><span id="POINTER_UNSIGNED"></span><span id="pointer_unsigned"></span><strong>POINTER_UNSIGNED</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-697">Указатель без знака.</span><span class="sxs-lookup"><span data-stu-id="c85f5-697">An unsigned pointer.</span></span></p>
<p><span data-ttu-id="c85f5-698">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-698">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>#define POINTER_UNSIGNED __uptr</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-699"><span id="PSHORT"></span><span id="pshort"></span><strong>пшорт</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-699"><span id="PSHORT"></span><span id="pshort"></span><strong>PSHORT</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-700">Указатель на <a href="#short"><strong>короткий</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-700">A pointer to a <a href="#short"><strong>SHORT</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-701">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-701">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef SHORT *PSHORT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-702"><span id="PSIZE_T"></span><span id="psize_t"></span><strong>PSIZE_T</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-702"><span id="PSIZE_T"></span><span id="psize_t"></span><strong>PSIZE_T</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-703">Указатель на <a href="#size_t"><strong>SIZE_T</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-703">A pointer to a <a href="#size_t"><strong>SIZE_T</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-704">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-704">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef SIZE_T *PSIZE_T;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-705"><span id="PSSIZE_T"></span><span id="pssize_t"></span><strong>PSSIZE_T</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-705"><span id="PSSIZE_T"></span><span id="pssize_t"></span><strong>PSSIZE_T</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-706">Указатель на <a href="#ssize_t"><strong>SSIZE_T</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-706">A pointer to a <a href="#ssize_t"><strong>SSIZE_T</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-707">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-707">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef SSIZE_T *PSSIZE_T;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-708"><span id="PSTR"></span><span id="pstr"></span><strong>пстр</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-708"><span id="PSTR"></span><span id="pstr"></span><strong>PSTR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-709">Указатель на строку в 8-разрядных символах Windows (ANSI), завершающуюся нулем.</span><span class="sxs-lookup"><span data-stu-id="c85f5-709">A pointer to a null-terminated string of 8-bit Windows (ANSI) characters.</span></span> <span data-ttu-id="c85f5-710">Дополнительные сведения см. в разделе <a href="/windows/desktop/gdi/character-sets-used-by-fonts">наборы символов, используемые шрифтами</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-710">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="c85f5-711">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-711">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CHAR *PSTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-712"><span id="PTBYTE"></span><span id="ptbyte"></span><strong>птбите</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-712"><span id="PTBYTE"></span><span id="ptbyte"></span><strong>PTBYTE</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-713">Указатель на <a href="#tbyte"><strong>тбите</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-713">A pointer to a <a href="#tbyte"><strong>TBYTE</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-714">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-714">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef TBYTE *PTBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-715"><span id="PTCHAR"></span><span id="ptchar"></span><strong>птчар</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-715"><span id="PTCHAR"></span><span id="ptchar"></span><strong>PTCHAR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-716">Указатель на <a href="#tchar"><strong>TCHAR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-716">A pointer to a <a href="#tchar"><strong>TCHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-717">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-717">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef TCHAR *PTCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-718"><span id="PTSTR"></span><span id="ptstr"></span><strong>птстр</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-718"><span id="PTSTR"></span><span id="ptstr"></span><strong>PTSTR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-719"><a href="#pwstr"><strong>Пвстр</strong></a> , если определен <strong>Юникод</strong> , <a href="#pstr"><strong>ПСТР</strong></a> в противном случае.</span><span class="sxs-lookup"><span data-stu-id="c85f5-719">A <a href="#pwstr"><strong>PWSTR</strong></a> if <strong>UNICODE</strong> is defined, a <a href="#pstr"><strong>PSTR</strong></a> otherwise.</span></span> <span data-ttu-id="c85f5-720">Дополнительные сведения см. в разделе <a href="/windows/desktop/Intl/windows-data-types-for-strings">типы данных Windows для строк</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-720">For more information, see <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Data Types for Strings</a>.</span></span></p>
<p><span data-ttu-id="c85f5-721">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-721">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c85f5-722">C++</span><span class="sxs-lookup"><span data-stu-id="c85f5-722">C++</span></span></th>
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
<td><span data-ttu-id="c85f5-723"><span id="PUCHAR"></span><span id="puchar"></span><strong>пучар</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-723"><span id="PUCHAR"></span><span id="puchar"></span><strong>PUCHAR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-724">Указатель на <a href="#uchar"><strong>Учар</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-724">A pointer to a <a href="#uchar"><strong>UCHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-725">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-725">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef UCHAR *PUCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-726"><span id="PUHALF_PTR"></span><span id="puhalf_ptr"></span><strong>PUHALF_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-726"><span id="PUHALF_PTR"></span><span id="puhalf_ptr"></span><strong>PUHALF_PTR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-727">Указатель на <a href="#uhalf_ptr"><strong>UHALF_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-727">A pointer to a <a href="#uhalf_ptr"><strong>UHALF_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-728">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-728">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c85f5-729">C++</span><span class="sxs-lookup"><span data-stu-id="c85f5-729">C++</span></span></th>
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
<td><span data-ttu-id="c85f5-730"><span id="PUINT"></span><span id="puint"></span><strong>пуинт</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-730"><span id="PUINT"></span><span id="puint"></span><strong>PUINT</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-731">Указатель на <a href="#uint"><strong>uint</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-731">A pointer to a <a href="#uint"><strong>UINT</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-732">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-732">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef UINT *PUINT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-733"><span id="PUINT_PTR"></span><span id="puint_ptr"></span><strong>PUINT_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-733"><span id="PUINT_PTR"></span><span id="puint_ptr"></span><strong>PUINT_PTR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-734">Указатель на <a href="#uint_ptr"><strong>UINT_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-734">A pointer to a <a href="#uint_ptr"><strong>UINT_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-735">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-735">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT_PTR *PUINT_PTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-736"><span id="PUINT8"></span><span id="puint8"></span><strong>PUINT8</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-736"><span id="PUINT8"></span><span id="puint8"></span><strong>PUINT8</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-737">Указатель на <a href="#uint8"><strong>UINT8</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-737">A pointer to a <a href="#uint8"><strong>UINT8</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-738">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-738">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT8 *PUINT8;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-739"><span id="PUINT16"></span><span id="puint16"></span><strong>PUINT16</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-739"><span id="PUINT16"></span><span id="puint16"></span><strong>PUINT16</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-740">Указатель на <a href="#uint16"><strong>UINT16</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-740">A pointer to a <a href="#uint16"><strong>UINT16</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-741">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-741">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT16 *PUINT16;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-742"><span id="PUINT32"></span><span id="puint32"></span><strong>PUINT32</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-742"><span id="PUINT32"></span><span id="puint32"></span><strong>PUINT32</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-743">Указатель на <a href="#uint32"><strong>UINT32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-743">A pointer to a <a href="#uint32"><strong>UINT32</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-744">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-744">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT32 *PUINT32;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-745"><span id="PUINT64"></span><span id="puint64"></span><strong>PUINT64</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-745"><span id="PUINT64"></span><span id="puint64"></span><strong>PUINT64</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-746">Указатель на <a href="#uint64"><strong>UINT64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-746">A pointer to a <a href="#uint64"><strong>UINT64</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-747">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-747">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT64 *PUINT64;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-748"><span id="PULONG"></span><span id="pulong"></span><strong>пулонг</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-748"><span id="PULONG"></span><span id="pulong"></span><strong>PULONG</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-749">Указатель на <a href="#ulong"><strong>ulong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-749">A pointer to a <a href="#ulong"><strong>ULONG</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-750">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-750">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef ULONG *PULONG;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-751"><span id="PULONGLONG"></span><span id="pulonglong"></span><strong>пулонглонг</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-751"><span id="PULONGLONG"></span><span id="pulonglong"></span><strong>PULONGLONG</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-752">Указатель на <a href="#ulonglong"><strong>улонглонг</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-752">A pointer to a <a href="#ulonglong"><strong>ULONGLONG</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-753">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-753">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef ULONGLONG *PULONGLONG;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-754"><span id="PULONG_PTR"></span><span id="pulong_ptr"></span><strong>PULONG_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-754"><span id="PULONG_PTR"></span><span id="pulong_ptr"></span><strong>PULONG_PTR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-755">Указатель на <a href="#ulong_ptr"><strong>ULONG_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-755">A pointer to a <a href="#ulong_ptr"><strong>ULONG_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-756">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-756">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef ULONG_PTR *PULONG_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-757"><span id="PULONG32"></span><span id="pulong32"></span><strong>PULONG32</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-757"><span id="PULONG32"></span><span id="pulong32"></span><strong>PULONG32</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-758">Указатель на <a href="#ulong32"><strong>ULONG32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-758">A pointer to a <a href="#ulong32"><strong>ULONG32</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-759">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-759">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef ULONG32 *PULONG32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-760"><span id="PULONG64"></span><span id="pulong64"></span><strong>PULONG64</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-760"><span id="PULONG64"></span><span id="pulong64"></span><strong>PULONG64</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-761">Указатель на <a href="#ulong64"><strong>ULONG64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-761">A pointer to a <a href="#ulong64"><strong>ULONG64</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-762">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-762">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef ULONG64 *PULONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-763"><span id="PUSHORT"></span><span id="pushort"></span><strong>пушорт</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-763"><span id="PUSHORT"></span><span id="pushort"></span><strong>PUSHORT</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-764">Указатель на <a href="#ushort"><strong>UShort</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-764">A pointer to a <a href="#ushort"><strong>USHORT</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-765">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-765">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef USHORT *PUSHORT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-766"><span id="PVOID"></span><span id="pvoid"></span><strong>PVOID</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-766"><span id="PVOID"></span><span id="pvoid"></span><strong>PVOID</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-767">Указатель на любой тип.</span><span class="sxs-lookup"><span data-stu-id="c85f5-767">A pointer to any type.</span></span></p>
<p><span data-ttu-id="c85f5-768">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-768">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef void *PVOID;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-769"><span id="PWCHAR"></span><span id="pwchar"></span><strong>пвчар</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-769"><span id="PWCHAR"></span><span id="pwchar"></span><strong>PWCHAR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-770">Указатель на <a href="#wchar"><strong>WCHAR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-770">A pointer to a <a href="#wchar"><strong>WCHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-771">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-771">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef WCHAR *PWCHAR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-772"><span id="PWORD"></span><span id="pword"></span><strong>пворд</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-772"><span id="PWORD"></span><span id="pword"></span><strong>PWORD</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-773">Указатель на <a href="#word"><strong>слово</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-773">A pointer to a <a href="#word"><strong>WORD</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-774">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-774">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef WORD *PWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-775"><span id="PWSTR"></span><span id="pwstr"></span><strong>пвстр</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-775"><span id="PWSTR"></span><span id="pwstr"></span><strong>PWSTR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-776">Указатель на строку из 16-разрядных символов Юникода, завершающуюся нулем.</span><span class="sxs-lookup"><span data-stu-id="c85f5-776">A pointer to a null-terminated string of 16-bit Unicode characters.</span></span> <span data-ttu-id="c85f5-777">Дополнительные сведения см. в разделе <a href="/windows/desktop/gdi/character-sets-used-by-fonts">наборы символов, используемые шрифтами</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-777">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="c85f5-778">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-778">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef WCHAR *PWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-779"><span id="QWORD"></span><span id="qword"></span><strong>QWORD</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-779"><span id="QWORD"></span><span id="qword"></span><strong>QWORD</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-780">64-разрядное целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="c85f5-780">A 64-bit unsigned integer.</span></span></p>
<p><span data-ttu-id="c85f5-781">Этот тип объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-781">This type is declared as follows:</span></span></p>
<p><code>typedef unsigned __int64 QWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-782"><span id="SC_HANDLE"></span><span id="sc_handle"></span><strong>SC_HANDLE</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-782"><span id="SC_HANDLE"></span><span id="sc_handle"></span><strong>SC_HANDLE</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-783">Маркер базы данных диспетчера управления службами.</span><span class="sxs-lookup"><span data-stu-id="c85f5-783">A handle to a service control manager database.</span></span> <span data-ttu-id="c85f5-784">Дополнительные сведения см. в разделе <a href="/windows/desktop/Services/scm-handles">дескрипторы SCM</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-784">For more information, see <a href="/windows/desktop/Services/scm-handles">SCM Handles</a>.</span></span></p>
<p><span data-ttu-id="c85f5-785">Этот тип объявляется в Винсвк. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-785">This type is declared in WinSvc.h as follows:</span></span></p>
<p><code>typedef HANDLE SC_HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-786"><span id="SC_LOCK"></span><span id="sc_lock"></span><strong>SC_LOCK</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-786"><span id="SC_LOCK"></span><span id="sc_lock"></span><strong>SC_LOCK</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-787">Блокировка базы данных диспетчера управления службами.</span><span class="sxs-lookup"><span data-stu-id="c85f5-787">A lock to a service control manager database.</span></span> <span data-ttu-id="c85f5-788">Дополнительные сведения см. в разделе <a href="/windows/desktop/Services/scm-handles">дескрипторы SCM</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-788">For more information, see <a href="/windows/desktop/Services/scm-handles">SCM Handles</a>.</span></span></p>
<p><span data-ttu-id="c85f5-789">Этот тип объявляется в Винсвк. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-789">This type is declared in WinSvc.h as follows:</span></span></p>
<p><code>typedef LPVOID SC_LOCK;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-790"><span id="SERVICE_STATUS_HANDLE"></span><span id="service_status_handle"></span><strong>SERVICE_STATUS_HANDLE</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-790"><span id="SERVICE_STATUS_HANDLE"></span><span id="service_status_handle"></span><strong>SERVICE_STATUS_HANDLE</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-791">Маркер для значения состояния службы.</span><span class="sxs-lookup"><span data-stu-id="c85f5-791">A handle to a service status value.</span></span> <span data-ttu-id="c85f5-792">Дополнительные сведения см. в разделе <a href="/windows/desktop/Services/scm-handles">дескрипторы SCM</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-792">For more information, see <a href="/windows/desktop/Services/scm-handles">SCM Handles</a>.</span></span></p>
<p><span data-ttu-id="c85f5-793">Этот тип объявляется в Винсвк. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-793">This type is declared in WinSvc.h as follows:</span></span></p>
<p><code>typedef HANDLE SERVICE_STATUS_HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-794"><span id="SHORT"></span><span id="short"></span><strong>ПРОМЕЖУТОК</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-794"><span id="SHORT"></span><span id="short"></span><strong>SHORT</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-795">16-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="c85f5-795">A 16-bit integer.</span></span> <span data-ttu-id="c85f5-796">Диапазон значений — от-32768 до 32767.</span><span class="sxs-lookup"><span data-stu-id="c85f5-796">The range is -32768 through 32767 decimal.</span></span></p>
<p><span data-ttu-id="c85f5-797">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-797">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef short SHORT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-798"><span id="SIZE_T"></span><span id="size_t"></span><strong>SIZE_T</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-798"><span id="SIZE_T"></span><span id="size_t"></span><strong>SIZE_T</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-799">Максимальное число байтов, на которое может указывать указатель.</span><span class="sxs-lookup"><span data-stu-id="c85f5-799">The maximum number of bytes to which a pointer can point.</span></span> <span data-ttu-id="c85f5-800">Используется для подсчета, который должен охватывать полный диапазон указателя.</span><span class="sxs-lookup"><span data-stu-id="c85f5-800">Use for a count that must span the full range of a pointer.</span></span></p>
<p><span data-ttu-id="c85f5-801">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-801">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef ULONG_PTR SIZE_T;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-802"><span id="SSIZE_T"></span><span id="ssize_t"></span><strong>SSIZE_T</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-802"><span id="SSIZE_T"></span><span id="ssize_t"></span><strong>SSIZE_T</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-803">Подписанная версия <a href="#size_t"><strong>SIZE_T</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-803">A signed version of <a href="#size_t"><strong>SIZE_T</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-804">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-804">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef LONG_PTR SSIZE_T;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-805"><span id="TBYTE"></span><span id="tbyte"></span><strong>тбите</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-805"><span id="TBYTE"></span><span id="tbyte"></span><strong>TBYTE</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-806">Значение <a href="#wchar"><strong>WCHAR</strong></a> , если задан <strong>Юникод</strong> , в противном случае — <a href="#char"><strong>символ</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c85f5-806">A <a href="#wchar"><strong>WCHAR</strong></a> if <strong>UNICODE</strong> is defined, a <a href="#char"><strong>CHAR</strong></a> otherwise.</span></span></p>
<p><span data-ttu-id="c85f5-807">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-807">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c85f5-808">C++</span><span class="sxs-lookup"><span data-stu-id="c85f5-808">C++</span></span></th>
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
<td><span data-ttu-id="c85f5-809"><span id="TCHAR"></span><span id="tchar"></span><strong>ГОЛОВК</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-809"><span id="TCHAR"></span><span id="tchar"></span><strong>TCHAR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-810">Значение <a href="#wchar"><strong>WCHAR</strong></a> , если задан <strong>Юникод</strong> , в противном случае — <a href="#char"><strong>символ</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c85f5-810">A <a href="#wchar"><strong>WCHAR</strong></a> if <strong>UNICODE</strong> is defined, a <a href="#char"><strong>CHAR</strong></a> otherwise.</span></span></p>
<p><span data-ttu-id="c85f5-811">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-811">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c85f5-812">C++</span><span class="sxs-lookup"><span data-stu-id="c85f5-812">C++</span></span></th>
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
<td><span data-ttu-id="c85f5-813"><span id="UCHAR"></span><span id="uchar"></span><strong>учар</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-813"><span id="UCHAR"></span><span id="uchar"></span><strong>UCHAR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-814"><a href="#char"><strong>Знак</strong></a>без знака.</span><span class="sxs-lookup"><span data-stu-id="c85f5-814">An unsigned <a href="#char"><strong>CHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-815">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-815">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned char UCHAR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-816"><span id="UHALF_PTR"></span><span id="uhalf_ptr"></span><strong>UHALF_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-816"><span id="UHALF_PTR"></span><span id="uhalf_ptr"></span><strong>UHALF_PTR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-817"><a href="#half_ptr"><strong>HALF_PTR</strong></a>без знака.</span><span class="sxs-lookup"><span data-stu-id="c85f5-817">An unsigned <a href="#half_ptr"><strong>HALF_PTR</strong></a>.</span></span> <span data-ttu-id="c85f5-818">Используйте в структуре, содержащей указатель и два маленьких поля.</span><span class="sxs-lookup"><span data-stu-id="c85f5-818">Use within a structure that contains a pointer and two small fields.</span></span></p>
<p><span data-ttu-id="c85f5-819">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-819">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c85f5-820">C++</span><span class="sxs-lookup"><span data-stu-id="c85f5-820">C++</span></span></th>
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
<td><span data-ttu-id="c85f5-821"><span id="UINT"></span><span id="uint"></span><strong>UINT</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-821"><span id="UINT"></span><span id="uint"></span><strong>UINT</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-822">Целое число без <a href="#int"><strong>знака.</strong></a></span><span class="sxs-lookup"><span data-stu-id="c85f5-822">An unsigned <a href="#int"><strong>INT</strong></a>.</span></span> <span data-ttu-id="c85f5-823">Диапазон — от 0 до 4294967295 десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="c85f5-823">The range is 0 through 4294967295 decimal.</span></span></p>
<p><span data-ttu-id="c85f5-824">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-824">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned int UINT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-825"><span id="UINT_PTR"></span><span id="uint_ptr"></span><strong>UINT_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-825"><span id="UINT_PTR"></span><span id="uint_ptr"></span><strong>UINT_PTR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-826"><a href="#int_ptr"><strong>INT_PTR</strong></a>без знака.</span><span class="sxs-lookup"><span data-stu-id="c85f5-826">An unsigned <a href="#int_ptr"><strong>INT_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-827">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-827">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c85f5-828">C++</span><span class="sxs-lookup"><span data-stu-id="c85f5-828">C++</span></span></th>
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
<td><span data-ttu-id="c85f5-829"><span id="UINT8"></span><span id="uint8"></span><strong>UINT8</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-829"><span id="UINT8"></span><span id="uint8"></span><strong>UINT8</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-830"><a href="#int8"><strong>INT8</strong></a>без знака.</span><span class="sxs-lookup"><span data-stu-id="c85f5-830">An unsigned <a href="#int8"><strong>INT8</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-831">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-831">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned  char UINT8;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-832"><span id="UINT16"></span><span id="uint16"></span><strong>UINT16</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-832"><span id="UINT16"></span><span id="uint16"></span><strong>UINT16</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-833">Неподписанная <a href="#int16"><strong>INT16</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-833">An unsigned <a href="#int16"><strong>INT16</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-834">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-834">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned  short UINT16;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-835"><span id="UINT32"></span><span id="uint32"></span><strong>ЗНАЧЕНИЕМ</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-835"><span id="UINT32"></span><span id="uint32"></span><strong>UINT32</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-836"><a href="#int32"><strong>Int32</strong></a>без знака.</span><span class="sxs-lookup"><span data-stu-id="c85f5-836">An unsigned <a href="#int32"><strong>INT32</strong></a>.</span></span> <span data-ttu-id="c85f5-837">Диапазон — от 0 до 4294967295 десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="c85f5-837">The range is 0 through 4294967295 decimal.</span></span></p>
<p><span data-ttu-id="c85f5-838">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-838">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned int UINT32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-839"><span id="UINT64"></span><span id="uint64"></span><strong>UINT64</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-839"><span id="UINT64"></span><span id="uint64"></span><strong>UINT64</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-840"><a href="#int64"><strong>Int64</strong></a>без знака.</span><span class="sxs-lookup"><span data-stu-id="c85f5-840">An unsigned <a href="#int64"><strong>INT64</strong></a>.</span></span> <span data-ttu-id="c85f5-841">Диапазон — от 0 до 18446744073709551615 Decimal.</span><span class="sxs-lookup"><span data-stu-id="c85f5-841">The range is 0 through 18446744073709551615 decimal.</span></span></p>
<p><span data-ttu-id="c85f5-842">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-842">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef usigned __int 64 UINT64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-843"><span id="ULONG"></span><span id="ulong"></span><strong>ULONG</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-843"><span id="ULONG"></span><span id="ulong"></span><strong>ULONG</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-844"><a href="#long"><strong>Длинное</strong></a>целое без знака.</span><span class="sxs-lookup"><span data-stu-id="c85f5-844">An unsigned <a href="#long"><strong>LONG</strong></a>.</span></span> <span data-ttu-id="c85f5-845">Диапазон — от 0 до 4294967295 десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="c85f5-845">The range is 0 through 4294967295 decimal.</span></span></p>
<p><span data-ttu-id="c85f5-846">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-846">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned long ULONG;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-847"><span id="ULONGLONG"></span><span id="ulonglong"></span><strong>улонглонг</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-847"><span id="ULONGLONG"></span><span id="ulonglong"></span><strong>ULONGLONG</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-848">64-разрядное целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="c85f5-848">A 64-bit unsigned integer.</span></span> <span data-ttu-id="c85f5-849">Диапазон — от 0 до 18446744073709551615 Decimal.</span><span class="sxs-lookup"><span data-stu-id="c85f5-849">The range is 0 through 18446744073709551615 decimal.</span></span></p>
<p><span data-ttu-id="c85f5-850">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-850">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c85f5-851">C++</span><span class="sxs-lookup"><span data-stu-id="c85f5-851">C++</span></span></th>
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
<td><span data-ttu-id="c85f5-852"><span id="ULONG_PTR"></span><span id="ulong_ptr"></span><strong>ULONG_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-852"><span id="ULONG_PTR"></span><span id="ulong_ptr"></span><strong>ULONG_PTR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-853"><a href="#long_ptr"><strong>LONG_PTR</strong></a>без знака.</span><span class="sxs-lookup"><span data-stu-id="c85f5-853">An unsigned <a href="#long_ptr"><strong>LONG_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="c85f5-854">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-854">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c85f5-855">C++</span><span class="sxs-lookup"><span data-stu-id="c85f5-855">C++</span></span></th>
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
<td><span data-ttu-id="c85f5-856"><span id="ULONG32"></span><span id="ulong32"></span><strong>ULONG32</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-856"><span id="ULONG32"></span><span id="ulong32"></span><strong>ULONG32</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-857">Неподписанный <a href="#long32"><strong>LONG32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-857">An unsigned <a href="#long32"><strong>LONG32</strong></a>.</span></span> <span data-ttu-id="c85f5-858">Диапазон — от 0 до 4294967295 десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="c85f5-858">The range is 0 through 4294967295 decimal.</span></span></p>
<p><span data-ttu-id="c85f5-859">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-859">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned int ULONG32;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-860"><span id="ULONG64"></span><span id="ulong64"></span><strong>ULONG64</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-860"><span id="ULONG64"></span><span id="ulong64"></span><strong>ULONG64</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-861">Неподписанный <a href="#long64"><strong>LONG64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-861">An unsigned <a href="#long64"><strong>LONG64</strong></a>.</span></span> <span data-ttu-id="c85f5-862">Диапазон — от 0 до 18446744073709551615 Decimal.</span><span class="sxs-lookup"><span data-stu-id="c85f5-862">The range is 0 through 18446744073709551615 decimal.</span></span></p>
<p><span data-ttu-id="c85f5-863">Этот тип объявляется в Басетсд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-863">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned __int64 ULONG64;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-864"><span id="UNICODE_STRING"></span><span id="unicode_string"></span><strong>UNICODE_STRING</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-864"><span id="UNICODE_STRING"></span><span id="unicode_string"></span><strong>UNICODE_STRING</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-865">Строка Юникода.</span><span class="sxs-lookup"><span data-stu-id="c85f5-865">A Unicode string.</span></span></p>
<p><span data-ttu-id="c85f5-866">Этот тип объявляется в Винтернл. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-866">This type is declared in Winternl.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c85f5-867">C++</span><span class="sxs-lookup"><span data-stu-id="c85f5-867">C++</span></span></th>
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
<td><span data-ttu-id="c85f5-868"><span id="USHORT"></span><span id="ushort"></span><strong>USHORT</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-868"><span id="USHORT"></span><span id="ushort"></span><strong>USHORT</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-869"><a href="#short"><strong>Короткое</strong></a>целое без знака.</span><span class="sxs-lookup"><span data-stu-id="c85f5-869">An unsigned <a href="#short"><strong>SHORT</strong></a>.</span></span> <span data-ttu-id="c85f5-870">Диапазон — от 0 до 65535 десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="c85f5-870">The range is 0 through 65535 decimal.</span></span></p>
<p><span data-ttu-id="c85f5-871">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-871">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned short USHORT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-872"><span id="USN"></span><span id="usn"></span><strong>ЖУРНАЛЫ</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-872"><span id="USN"></span><span id="usn"></span><strong>USN</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-873">Порядковый номер обновления (USN).</span><span class="sxs-lookup"><span data-stu-id="c85f5-873">An update sequence number (USN).</span></span></p>
<p><span data-ttu-id="c85f5-874">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-874">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef LONGLONG USN;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-875"><span id="VOID"></span><span id="void"></span><strong>VOID</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-875"><span id="VOID"></span><span id="void"></span><strong>VOID</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-876">Любой тип.</span><span class="sxs-lookup"><span data-stu-id="c85f5-876">Any type.</span></span></p>
<p><span data-ttu-id="c85f5-877">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-877">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>#define VOID void</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-878"><span id="WCHAR"></span><span id="wchar"></span><strong>WCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-878"><span id="WCHAR"></span><span id="wchar"></span><strong>WCHAR</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-879">16-разрядный символ Юникода.</span><span class="sxs-lookup"><span data-stu-id="c85f5-879">A 16-bit Unicode character.</span></span> <span data-ttu-id="c85f5-880">Дополнительные сведения см. в разделе <a href="/windows/desktop/gdi/character-sets-used-by-fonts">наборы символов, используемые шрифтами</a>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-880">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="c85f5-881">Этот тип объявлен в WinNT. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-881">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef wchar_t WCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-882"><span id="WINAPI"></span><span id="winapi"></span><strong>WINAPI</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-882"><span id="WINAPI"></span><span id="winapi"></span><strong>WINAPI</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-883">Соглашение о вызовах для системных функций.</span><span class="sxs-lookup"><span data-stu-id="c85f5-883">The calling convention for system functions.</span></span></p>
<p><span data-ttu-id="c85f5-884">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-884">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>#define WINAPI __stdcall</code></p>
<p><span data-ttu-id="c85f5-885">Функции <strong>callback</strong>, <strong>WinAPI</strong>и <strong>апиентри</strong> используются для определения функций с помощью соглашения о вызовах __stdcall.</span><span class="sxs-lookup"><span data-stu-id="c85f5-885"><strong>CALLBACK</strong>, <strong>WINAPI</strong>, and <strong>APIENTRY</strong> are all used to define functions with the __stdcall calling convention.</span></span> <span data-ttu-id="c85f5-886">Большинство функций в API Windows объявляются с помощью <strong>WinAPI</strong>.</span><span class="sxs-lookup"><span data-stu-id="c85f5-886">Most functions in the Windows API are declared using <strong>WINAPI</strong>.</span></span> <span data-ttu-id="c85f5-887">Вы можете использовать <strong>обратный вызов</strong> для функций обратного вызова, которые реализуются, чтобы определить функцию как функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="c85f5-887">You may wish to use <strong>CALLBACK</strong> for the callback functions that you implement to help identify the function as a callback function.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c85f5-888"><span id="WORD"></span><span id="word"></span><strong>СЛОВАМ</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-888"><span id="WORD"></span><span id="word"></span><strong>WORD</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-889">16-разрядное целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="c85f5-889">A 16-bit unsigned integer.</span></span> <span data-ttu-id="c85f5-890">Диапазон — от 0 до 65535 десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="c85f5-890">The range is 0 through 65535 decimal.</span></span></p>
<p><span data-ttu-id="c85f5-891">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-891">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned short WORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c85f5-892"><span id="WPARAM"></span><span id="wparam"></span><strong>WPARAM</strong></span><span class="sxs-lookup"><span data-stu-id="c85f5-892"><span id="WPARAM"></span><span id="wparam"></span><strong>WPARAM</strong></span></span></td>
<td><p><span data-ttu-id="c85f5-893">Параметр сообщения.</span><span class="sxs-lookup"><span data-stu-id="c85f5-893">A message parameter.</span></span></p>
<p><span data-ttu-id="c85f5-894">Этот тип объявляется в Виндеф. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c85f5-894">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef UINT_PTR WPARAM;</code></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="c85f5-895">Требования</span><span class="sxs-lookup"><span data-stu-id="c85f5-895">Requirements</span></span>



| <span data-ttu-id="c85f5-896">Требование</span><span class="sxs-lookup"><span data-stu-id="c85f5-896">Requirement</span></span> | <span data-ttu-id="c85f5-897">Значение</span><span class="sxs-lookup"><span data-stu-id="c85f5-897">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c85f5-898">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c85f5-898">Minimum supported client</span></span><br/> | <span data-ttu-id="c85f5-899">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c85f5-899">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="c85f5-900">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c85f5-900">Minimum supported server</span></span><br/> | <span data-ttu-id="c85f5-901">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c85f5-901">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                |
| <span data-ttu-id="c85f5-902">Header</span><span class="sxs-lookup"><span data-stu-id="c85f5-902">Header</span></span><br/>                   | <dl> <span data-ttu-id="c85f5-903"><dt>Басетсд. h; </dt> <dt>Виндеф. h; </dt> Файл <dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="c85f5-903"><dt>BaseTsd.h; </dt> <dt>WinDef.h; </dt> <dt>WinNT.h</dt></span></span> </dl> |
