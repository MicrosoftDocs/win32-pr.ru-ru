---
title: Ошибки компилятора
description: Список сообщений об ошибках, созданных во время компиляции MIDL.
ms.assetid: 492eacdd-6bd1-49df-9112-3765f6c05f34
keywords:
- ошибки MIDL, ошибки компилятора
topic_type:
- apiref
api_name:
- Compiler Errors
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 56b610025d3012446daa7938e2f37c2efcf6c2ddb7edd2ee545db0a179953fad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067459"
---
# <a name="compiler-errors"></a>Ошибки компилятора

Во время компиляции MIDL создаются следующие сообщения об ошибках:



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
<td><span id="MIDL2000"></span><span id="midl2000"></span><dl> <dt><strong>MIDL2000</strong></dt> </dl></td>
<td><dl> <dt><span id="must_specify__c_ext_for_abstract_declarators"></span><span id="MUST_SPECIFY__C_EXT_FOR_ABSTRACT_DECLARATORS"></span>необходимо указать/c_ext для абстрактных деклараторов</dt> <dd> Абстрактные деклараторы представляют собой расширение Microsoft для RPC и не определяются в DCE RPC. Таким образом, если файл содержит абстрактные деклараторы, нельзя компилировать с параметром <a href="-osf.md"><strong>/ОСФ</strong></a> , который обеспечивает строгую совместимость с DCE. MIDL версии 3,0 и более поздних версий по умолчанию используют параметр <a href="-c-ext.md"><strong>/c_ext</strong></a> ; параметр <strong>/ОСФ</strong> отключает параметр <strong>/c_ext</strong> . Сведения об абстрактных деклараторах см. <a href="/windows/desktop/Rpc/the-acf-body">в тексте ACF</a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2001"></span><span id="midl2001"></span><dl> <dt><strong>MIDL2001</strong></dt> </dl></td>
<td><dl> <dt><span id="instantiation_of_data_is_illegal__you_must_use__extern__or__static_"></span><span id="INSTANTIATION_OF_DATA_IS_ILLEGAL__YOU_MUST_USE__EXTERN__OR__STATIC_"></span>Недопустимый экземпляр данных. необходимо использовать &quot; модификатор extern &quot; или &quot; static&quot;</dt> <dd> Объявление и инициализация в IDL-файле несовместимы с DCE RPC. Эта функция является расширением Microsoft, которое недоступно при компиляции в режиме DCE-Compatibility (<a href="-osf.md"><strong>/ОСФ</strong></a>).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2002"></span><span id="midl2002"></span><dl> <dt><strong>MIDL2002</strong></dt> </dl></td>
<td><dl> <dt><span id="compiler_stack_overflow"></span><span id="COMPILER_STACK_OVERFLOW"></span>переполнение стека компилятора</dt> <dd> Компилятор исчерпал пространство стека при обработке IDL-файла. Эта проблема может возникать, когда компилятор обрабатывает сложное объявление или выражение. Чтобы решить эту проблему, упростите сложное объявление или выражение.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2003"></span><span id="midl2003"></span><dl> <dt><strong>MIDL2003</strong></dt> </dl></td>
<td><dl> <dt><span id="redefinition"></span><span id="REDEFINITION"></span>Переопределение</dt> <dd> Это сообщение об ошибке может появиться в следующих случаях: тип был переопределен. прототип процедуры был переопределен. член структуры или объединения с таким именем уже существует; параметр с таким именем уже существует в прототипе.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2004"></span><span id="midl2004"></span><dl> <dt><strong>MIDL2004</strong></dt> </dl></td>
<td><dl> <dt><span id="_auto_handle__binding_will_be_used"></span><span id="_AUTO_HANDLE__BINDING_WILL_BE_USED"></span>будет использоваться привязка [auto_handle]</dt> <dd> Тип обработчика не определен как тип обработчика по умолчанию. Компилятор предполагает, что в качестве маркера привязки для указанной процедуры будет использоваться автоматический обработчик.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2005"></span><span id="midl2005"></span><dl> <dt><strong>MIDL2005</strong></dt> </dl></td>
<td><dl> <dt><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>недостаточно памяти</dt> <dd> Компилятор исчерпал память во время компиляции. Уменьшите размер или сложность IDL-файла или выделите больший объем памяти для процесса.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2006"></span><span id="midl2006"></span><dl> <dt><strong>MIDL2006</strong></dt> </dl></td>
<td><dl> <dt><span id="recursive_definition"></span><span id="RECURSIVE_DEFINITION"></span>рекурсивное определение</dt> <dd> Структура или объединение рекурсивно определены. Эта ошибка может возникать, если отсутствует спецификация указателя в определении вложенной структуры.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2007"></span><span id="midl2007"></span><dl> <dt><strong>MIDL2007</strong></dt> </dl></td>
<td><dl> <dt><span id="import_ignored__file_already_imported"></span><span id="IMPORT_IGNORED__FILE_ALREADY_IMPORTED"></span>Импорт пропущен; файл уже импортирован</dt> <dd> Импорт IDL-файла является операцией идемпотентными. Включение более одного раза не оказывает никакого воздействия. Все операции импорта, кроме первой, игнорируются.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2008"></span><span id="midl2008"></span><dl> <dt><strong>MIDL2008</strong></dt> </dl></td>
<td><dl> <dt><span id="sparse_enums_require__c_ext_or__ms_ext"></span><span id="SPARSE_ENUMS_REQUIRE__C_EXT_OR__MS_EXT"></span>для перечислений sparse требуется/c_ext или/ms_ext</dt> <dd> Присвоение значений константам перечисления не совместимо с DCE RPC. Если вы хотите использовать расширения Майкрософт для MIDL, которые позволяют назначать значения константам перечисления, нельзя выполнить компиляцию с параметром <a href="-osf.md"><strong>/ОСФ</strong></a> , который обеспечивает строгую совместимость с DCE. MIDL версии 3,0 и более поздних версий по умолчанию используют параметры <a href="-c-ext.md"><strong>/c_ext</strong></a> и <a href="-ms-ext.md"><strong>/ms_ext</strong></a> . параметр <strong>/ОСФ</strong> отключает эти параметры расширения.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2009"></span><span id="midl2009"></span><dl> <dt><strong>MIDL2009</strong></dt> </dl></td>
<td><dl> <dt><span id="undefined_symbol"></span><span id="UNDEFINED_SYMBOL"></span>неопределенный символ</dt> <dd> В выражении использован неопределенный символ. Эта ошибка может возникать при использовании неопределенного перечислимого значения.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2010"></span><span id="midl2010"></span><dl> <dt><strong>MIDL2010</strong></dt> </dl></td>
<td><dl> <dt><span id="type_used_in_ACF_file_not_defined_in_IDL_file"></span><span id="type_used_in_acf_file_not_defined_in_idl_file"></span><span id="TYPE_USED_IN_ACF_FILE_NOT_DEFINED_IN_IDL_FILE"></span>тип, используемый в файле ACF, не определен в IDL-файле</dt> <dd> Используется неопределенный тип.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2011"></span><span id="midl2011"></span><dl> <dt><strong>MIDL2011</strong></dt> </dl></td>
<td><dl> <dt><span id="unresolved_type_declaration"></span><span id="UNRESOLVED_TYPE_DECLARATION"></span>неразрешенное объявление типа</dt> <dd> Тип, указанный в поле дополнительных сведений об ошибке, не определен в других местах IDL-файла.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2012"></span><span id="midl2012"></span><dl> <dt><strong>MIDL2012</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_wide-character_constants_requires__ms_ext_or__c_ext"></span><span id="USE_OF_WIDE-CHARACTER_CONSTANTS_REQUIRES__MS_EXT_OR__C_EXT"></span>Использование констант расширенных символов требует/ms_ext или/c_ext</dt> <dd> Константы расширенных символов — это расширение Майкрософт для устройства DCE IDL. Чтобы использовать тип данных <a href="wchar-t.md"><strong>wchar_t</strong></a>, нельзя компилировать с помощью параметра <a href="-osf.md"><strong>/ОСФ</strong></a> , который переопределяет параметры командной строки компилятора MIDL по умолчанию <a href="-ms-ext.md"><strong>/ms_ext</strong></a> и <a href="-c-ext.md"><strong>/c_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2013"></span><span id="midl2013"></span><dl> <dt><strong>MIDL2013</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_wide_character_strings_requires__ms_ext_or__c_ext"></span><span id="USE_OF_WIDE_CHARACTER_STRINGS_REQUIRES__MS_EXT_OR__C_EXT"></span>использование строк расширенных символов требует/ms_ext или/c_ext</dt> <dd> Строковые константы расширенных символов — это расширение Майкрософт для устройства DCE IDL. Чтобы использовать тип данных <a href="wchar-t.md"><strong>wchar_t</strong></a>, нельзя компилировать с помощью параметра <a href="-osf.md"><strong>/ОСФ</strong></a> , который переопределяет параметры командной строки компилятора MIDL по умолчанию <a href="-ms-ext.md"><strong>/ms_ext</strong></a> и <a href="-c-ext.md"><strong>/c_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2014"></span><span id="midl2014"></span><dl> <dt><strong>MIDL2014</strong></dt> </dl></td>
<td><dl> <dt><span id="inconsistent_redefinition_of_type_wchar_t"></span><span id="INCONSISTENT_REDEFINITION_OF_TYPE_WCHAR_T"></span>непротиворечивое переопределение типа wchar_t</dt> <dd> Тип <a href="wchar-t.md"><strong>wchar_t</strong></a> был переопределен как тип, который не эквивалентен неподписанному короткому типу DOS *.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2015"></span><span id="midl2015"></span><dl> <dt><strong>MIDL2015</strong></dt> </dl></td>
<td><dl> <dt><span id="importlib_not_found"></span><span id="IMPORTLIB_NOT_FOUND"></span>importlib не найден</dt> <dd> Компилятору не удалось найти библиотеку типов, указанную в директиве [ <a href="importlib.md"><strong>importlib</strong></a>]. Убедитесь, что путь и имя библиотеки указаны правильно.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2016"></span><span id="midl2016"></span><dl> <dt><strong>MIDL2016</strong></dt> </dl></td>
<td><dl> <dt><span id="two_library_blocks"></span><span id="TWO_LIBRARY_BLOCKS"></span>два блока библиотек</dt> <dd> Два блока библиотеки (даже с разными именами) в одном и том же исходном файле являются недопустимыми. Объедините все элементы в один блок библиотеки.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2017"></span><span id="midl2017"></span><dl> <dt><strong>MIDL2017</strong></dt> </dl></td>
<td><dl> <dt><span id="the_dispinterface_statement_requires_a_definition_for_IDispatch"></span><span id="the_dispinterface_statement_requires_a_definition_for_idispatch"></span><span id="THE_DISPINTERFACE_STATEMENT_REQUIRES_A_DEFINITION_FOR_IDISPATCH"></span>для инструкции disp-интерфейса требуется определение для IDispatch</dt> <dd> Эта ошибка обычно возникает, когда файлы Stdole2. tlb или Оаидл. IDL не импортируются.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2018"></span><span id="midl2018"></span><dl> <dt><strong>MIDL2018</strong></dt> </dl></td>
<td><dl> <dt><span id="error_accessing_type_library"></span><span id="ERROR_ACCESSING_TYPE_LIBRARY"></span>Ошибка при доступе к библиотеке типов</dt> <dd> Компилятору не удалось найти указанную библиотеку типов. Убедитесь, что путь указан правильно.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2019"></span><span id="midl2019"></span><dl> <dt><strong>MIDL2019</strong></dt> </dl></td>
<td><dl> <dt><span id="error_accessing_type_info"></span><span id="ERROR_ACCESSING_TYPE_INFO"></span>Ошибка при доступе к сведениям о типе</dt> <dd> Импортированная библиотека типов повреждена, недопустима или частично построена.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2020"></span><span id="midl2020"></span><dl> <dt><strong>MIDL2020</strong></dt> </dl></td>
<td><dl> <dt><span id="error_generating_type_library"></span><span id="ERROR_GENERATING_TYPE_LIBRARY"></span>Ошибка при создании библиотеки типов</dt> <dd> Не удалось создать библиотеку типов. Одной из возможных причин этой ошибки является указание пути к IDL-файлу, длина которого превышает 126 символов. Oleaut32.dll не поддерживает имена путей длиннее 126 символов.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2021"></span><span id="midl2021"></span><dl> <dt><strong>MIDL2021</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicate_id"></span><span id="DUPLICATE_ID"></span>дублирующийся идентификатор</dt> <dd> Приложения используют оператор <a href="id.md"><strong>ID</strong></a> в IDL-файлах для указания DISPID для функций-членов. Функции элементов могут быть свойствами или методами интерфейсов или DISP. Эта ошибка означает, что IDL-файл задает один и тот же идентификатор для двух методов или свойств.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2022"></span><span id="midl2022"></span><dl> <dt><strong>MIDL2022</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_or_missing_value_for_entry_attribute"></span><span id="ILLEGAL_OR_MISSING_VALUE_FOR_ENTRY_ATTRIBUTE"></span>Недопустимое или отсутствующее значение для атрибута Entry</dt> <dd> Аргументом для атрибута записи может быть либо строка, указывающая именованная точка входа, либо порядковый номер, определяющий точку входа. Этот аргумент либо отсутствует, либо содержит недопустимое значение.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2023"></span><span id="midl2023"></span><dl> <dt><strong>MIDL2023</strong></dt> </dl></td>
<td><dl> <dt><span id="error_recovery_assumes"></span><span id="ERROR_RECOVERY_ASSUMES"></span>Предполагается восстановление после ошибки</dt> <dd> Компилятор MIDL обнаружил недопустимые символы в IDL-файле.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2024"></span><span id="midl2024"></span><dl> <dt><strong>MIDL2024</strong></dt> </dl></td>
<td><dl> <dt><span id="error_recovery_discards"></span><span id="ERROR_RECOVERY_DISCARDS"></span>ошибки, отмененные при восстановлении</dt> <dd> Компилятор MIDL обнаружил недопустимые символы в IDL-файле. Недопустимые символы будут проигнорированы.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2025"></span><span id="midl2025"></span><dl> <dt><strong>MIDL2025</strong></dt> </dl></td>
<td><dl> <dt><span id="syntax_error"></span><span id="SYNTAX_ERROR"></span>Синтаксическая ошибка</dt> <dd> Компилятор обнаружил синтаксическую ошибку в указанной строке.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2026"></span><span id="midl2026"></span><dl> <dt><strong>MIDL2026</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_recover_from_earlier_syntax_errors__aborting_compilation"></span><span id="CANNOT_RECOVER_FROM_EARLIER_SYNTAX_ERRORS__ABORTING_COMPILATION"></span>не удается выполнить восстановление после предыдущих синтаксических ошибок. прерывание компиляции</dt> <dd> Компилятор MIDL автоматически пытается выполнить восстановление после синтаксических ошибок путем добавления или удаления синтаксических элементов. Это сообщение означает, что, несмотря на попытки восстановления, компилятор обнаружил слишком много ошибок. Исправьте указанные ошибки и выполните повторную компиляцию.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2027"></span><span id="midl2027"></span><dl> <dt><strong>MIDL2027</strong></dt> </dl></td>
<td><dl> <dt><span id="unknown_pragma_option"></span><span id="UNKNOWN_PRAGMA_OPTION"></span>Неизвестный параметр директивы pragma</dt> <dd> Указанная директива pragma C не поддерживается в MIDL. Удалите директиву pragma из IDL-файла.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2028"></span><span id="midl2028"></span><dl> <dt><strong>MIDL2028</strong></dt> </dl></td>
<td><dl> <dt><span id="feature_not_implemented"></span><span id="FEATURE_NOT_IMPLEMENTED"></span>функция не реализована</dt> <dd> Функция MIDL, хотя часть определения языка, не реализована в Microsoft RPC и не поддерживается компилятором MIDL. Например, следующие функции языка не реализованы: битовом массиве, pipe и Международный тип символов. Функция нереализованного языка отображается в поле Дополнительные сведения об ошибке сообщения об ошибке.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2029"></span><span id="midl2029"></span><dl> <dt><strong>MIDL2029</strong></dt> </dl></td>
<td><dl> <dt><span id="type_not_implemented"></span><span id="TYPE_NOT_IMPLEMENTED"></span>тип не реализован</dt> <dd> Указанный тип данных, хотя и допустимое ключевое слово MIDL, не реализован в Microsoft RPC.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2030"></span><span id="midl2030"></span><dl> <dt><strong>MIDL2030</strong></dt> </dl></td>
<td><dl> <dt><span id="non-pointer_used_in_a_dereference_operation"></span><span id="NON-POINTER_USED_IN_A_DEREFERENCE_OPERATION"></span>в операции разыменования используется не указатель</dt> <dd> Тип данных, не являющийся указателем, был связан с операциями с указателями. Невозможно получить доступ к объекту через указанный элемент, не являющийся указателем.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2031"></span><span id="midl2031"></span><dl> <dt><strong>MIDL2031</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_has_a_divide_by_zero"></span><span id="EXPRESSION_HAS_A_DIVIDE_BY_ZERO"></span>выражение имеет деление на ноль</dt> <dd> Константное выражение содержит деление на ноль.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2032"></span><span id="midl2032"></span><dl> <dt><strong>MIDL2032</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_uses_incompatible_types"></span><span id="EXPRESSION_USES_INCOMPATIBLE_TYPES"></span>выражение использует несовместимые типы</dt> <dd> Левая и правая части оператора в выражении имеют несовместимые типы.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2033"></span><span id="midl2033"></span><dl> <dt><strong>MIDL2033</strong></dt> </dl></td>
<td><dl> <dt><span id="nonarray_expression_uses_index_operator"></span><span id="NONARRAY_EXPRESSION_USES_INDEX_OPERATOR"></span>немассивное выражение использует оператор индекса</dt> <dd> Выражение использует операцию индексации массива для элемента данных, который не относится к типу массива.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2034"></span><span id="midl2034"></span><dl> <dt><strong>MIDL2034</strong></dt> </dl></td>
<td><dl> <dt><span id="left-hand_side_of_expression_does_not_evaluate_to_struct_union_enum"></span><span id="LEFT-HAND_SIDE_OF_EXPRESSION_DOES_NOT_EVALUATE_TO_STRUCT_UNION_ENUM"></span>Левая часть выражения не вычисляется как структура, объединение или перечисление</dt> <dd> Прямой или косвенный оператор Reference &quot; или &quot; &quot; -> &quot; был применен к объекту данных, который не является структурой, объединением или перечислением. Невозможно получить прямую или косвенную ссылку с помощью указанного объекта.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2035"></span><span id="midl2035"></span><dl> <dt><strong>MIDL2035</strong></dt> </dl></td>
<td><dl> <dt><span id="constant_expression_expected"></span><span id="CONSTANT_EXPRESSION_EXPECTED"></span>требуется константное выражение</dt> <dd> В синтаксисе ожидалось константное выражение. Например, для границ массива требуется константное выражение. Компилятор выдает это сообщение об ошибке, если привязка массива определена с помощью переменной или неопределенного символа.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2036"></span><span id="midl2036"></span><dl> <dt><strong>MIDL2036</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_cannot_be_evaluated_at_compile_time"></span><span id="EXPRESSION_CANNOT_BE_EVALUATED_AT_COMPILE_TIME"></span>выражение не может быть вычислено во время компиляции</dt> <dd> Компилятор не может вычислить выражение во время компиляции.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2037"></span><span id="midl2037"></span><dl> <dt><strong>MIDL2037</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_not_implemented"></span><span id="EXPRESSION_NOT_IMPLEMENTED"></span>выражение не реализовано</dt> <dd> Функция, которая поддерживалась в предыдущих версиях компилятора MIDL, не поддерживается в версии компилятора, предоставляемого с Microsoft RPC. Удалить указанное выражение.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2038"></span><span id="midl2038"></span><dl> <dt><strong>MIDL2038</strong></dt> </dl></td>
<td><dl> <dt><span id="no__pointer_default__attribute_specified__assuming__unique__for_all_unattributed_pointers"></span><span id="NO__POINTER_DEFAULT__ATTRIBUTE_SPECIFIED__ASSUMING__UNIQUE__FOR_ALL_UNATTRIBUTED_POINTERS"></span>не указан атрибут [pointer_default], предполагается [unique] для всех неатрибутных указателей</dt> <dd> Компилятор MIDL предлагает три различных варианта по умолчанию для указателей, которые не имеют атрибутов указателя. Параметры функции, которые являются указателями верхнего уровня, по умолчанию имеют указатели [<a href="ref.md"><strong>ref</strong></a>]. Указатели, внедренные в структуры и указатели на другие указатели (не указатели верхнего уровня) по умолчанию имеют тип, заданный атрибутом [<a href="pointer-default.md"><strong>pointer_default</strong></a>]. Если атрибут [<strong>pointer_default</strong>] не указан, эти указатели уровня нонтоп по умолчанию имеют уникальные указатели. Это сообщение об ошибке указывает на Последнее обращение: атрибут [<strong>pointer_default</strong>] не указан, и существует по крайней мере один указатель, не являющийся указателем верхнего уровня, который будет рассматриваться как уникальный указатель. Дополнительные сведения см. в разделе <a href="/windows/desktop/Rpc/default-pointer-types">типы указателей по умолчанию</a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2039"></span><span id="midl2039"></span><dl> <dt><strong>MIDL2039</strong></dt> </dl></td>
<td><dl> <dt><span id="interface_is_not_automation_marshaling_conformant"></span><span id="INTERFACE_IS_NOT_AUTOMATION_MARSHALING_CONFORMANT"></span>интерфейс не является согласованным маршалером службы автоматизации</dt> <dd> Интерфейс не соответствует требованиям для интерфейса OLE Automation. Убедитесь, что интерфейс является производным от <strong>IUnknown</strong> или <strong>IDispatch</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2040"></span><span id="midl2040"></span><dl> <dt><strong>MIDL2040</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__only_parameter_cannot_be_a_pointer_to_an_open_structure"></span><span id="_OUT__ONLY_PARAMETER_CANNOT_BE_A_POINTER_TO_AN_OPEN_STRUCTURE"></span>[out] только параметр не может быть указателем на открытую структуру</dt> <dd> В качестве указателя на структуру используется только [<a href="out-idl.md"><strong>out</strong></a>]-параметр, который называется открытой структурой, переданный диапазон и размер которого определяются во время выполнения. Заглушка сервера не знает, сколько пространства нужно выделить для открытой структуры. Используйте указатель на указатель на открытую структуру и убедитесь, что серверное приложение выделяет достаточно места для него.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2041"></span><span id="midl2041"></span><dl> <dt><strong>MIDL2041</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__only_parameter_cannot_be_an_unsized_string"></span><span id="_OUT__ONLY_PARAMETER_CANNOT_BE_AN_UNSIZED_STRING"></span>[out] только параметр не может быть строкой без размера</dt> <dd> Массив с атрибутом String объявлен как параметр [<a href="out-idl.md"><strong>out</strong></a>] — только без спецификации размера. Заглушке сервера требуются сведения о размере для выделения памяти для строки. Можно удалить атрибут String и добавить атрибут [<a href="size-is.md"><strong>size_is</strong></a>] или изменить параметр на [<strong>in, out</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2042"></span><span id="midl2042"></span><dl> <dt><strong>MIDL2042</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__parameter_is_not_a_pointer"></span><span id="_OUT__PARAMETER_IS_NOT_A_POINTER"></span>параметр [out] не является указателем</dt> <dd> Все параметры [<a href="out-idl.md"><strong>out</strong></a>] должны быть указателями в соответствии с соглашением о вызове по значению языка программирования C. Параметр направления [<strong>out</strong>] указывает, что сервер передает клиенту значение. При использовании соглашения о вызове по значению сервер может передавать данные клиенту, только если аргумент функции является указателем.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2043"></span><span id="midl2043"></span><dl> <dt><strong>MIDL2043</strong></dt> </dl></td>
<td><dl> <dt><span id="open_structure_cannot_be_a_parameter"></span><span id="OPEN_STRUCTURE_CANNOT_BE_A_PARAMETER"></span>Открытая структура не может быть параметром</dt> <dd> Открытая структура содержит согласованный массив в качестве последнего элемента. Структура или объединение усекаются, если последний элемент этой структуры или объединения является согласованным массивом.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2044"></span><span id="midl2044"></span><dl> <dt><strong>MIDL2044</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__context_handle_generic_handle_must_be_specified_as_a_pointer_to_that_handle_type"></span><span id="_OUT__CONTEXT_HANDLE_GENERIC_HANDLE_MUST_BE_SPECIFIED_AS_A_POINTER_TO_THAT_HANDLE_TYPE"></span>[out] описатель контекста/универсальный маркер должен быть указан в качестве указателя на этот тип обработчика</dt> <dd> Обработчик контекста или определяемый пользователем параметр с атрибутом [<a href="out-idl.md"><strong>out</strong></a>] должен быть указателем на указатель.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2045"></span><span id="midl2045"></span><dl> <dt><strong>MIDL2045</strong></dt> </dl></td>
<td><dl> <dt><span id="context_handle_must_not_derive_from_a_type_that_has_the__transmit_as__attribute"></span><span id="CONTEXT_HANDLE_MUST_NOT_DERIVE_FROM_A_TYPE_THAT_HAS_THE__TRANSMIT_AS__ATTRIBUTE"></span>Описатель контекста не должен быть производным от типа, имеющего атрибут [transmit_as]</dt> <dd> Дескрипторы контекста должны передаваться как типы дескрипторов контекста. Они не могут передаваться как другие типы и не могут быть производными от [transmit_is], [<strong>represent_as</strong>], [<strong>wire_marshal</strong>] или [<strong>user_marshal</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2046"></span><span id="midl2046"></span><dl> <dt><strong>MIDL2046</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_specify_a_variable_number_of_arguments_to_a_remote_procedure"></span><span id="CANNOT_SPECIFY_A_VARIABLE_NUMBER_OF_ARGUMENTS_TO_A_REMOTE_PROCEDURE"></span>невозможно указать переменное число аргументов для удаленной процедуры</dt> <dd> Удаленные вызовы процедур, которые задают переменное число аргументов во время компиляции, несовместимы с определением устройства DCE RPC. В Microsoft RPC нельзя использовать переменное число аргументов.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2047"></span><span id="midl2047"></span><dl> <dt><strong>MIDL2047</strong></dt> </dl></td>
<td><dl> <dt><span id="named_parameter_cannot_be__void_"></span><span id="NAMED_PARAMETER_CANNOT_BE__VOID_"></span>именованный параметр не может быть &quot; void&quot;</dt> <dd> Параметр с базовым типом <a href="void.md"><strong>void</strong></a> указывается с именем.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2048"></span><span id="midl2048"></span><dl> <dt><strong>MIDL2048</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_derives_from__coclass__or__module_"></span><span id="PARAMETER_DERIVES_FROM__COCLASS__OR__MODULE_"></span>параметр является производным от &quot; класса coclass &quot; или &quot; модуля&quot;</dt> <dd> <a href="coclass.md"><strong>Компонент coclass</strong></a> указывает объект верхнего уровня, содержащий интерфейсы и disp-интерфейсов. Он не может быть передан в качестве параметра.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2049"></span><span id="midl2049"></span><dl> <dt><strong>MIDL2049</strong></dt> </dl></td>
<td><dl> <dt><span id="only_the_first_parameter_can_be_a_binding_handle__you_must_specify_the__ms_ext_switch"></span><span id="ONLY_THE_FIRST_PARAMETER_CAN_BE_A_BINDING_HANDLE__YOU_MUST_SPECIFY_THE__MS_EXT_SWITCH"></span>только первый параметр может быть маркером привязки; необходимо указать параметр/ms_ext</dt> <dd> DCE RPC позволяет использовать только первый параметр в качестве маркера привязки. При компиляции с параметром <a href="-osf.md"><strong>/ОСФ</strong></a> отключается параметр по умолчанию <a href="-ms-ext.md"><strong>/ms_ext</strong></a> , который поддерживает несколько параметров обработки и обрабатывает параметры, отличные от левого расположения.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2050"></span><span id="midl2050"></span><dl> <dt><strong>MIDL2050</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_use__comm_status__on_both_a_parameter_and_a_return_type"></span><span id="CANNOT_USE__COMM_STATUS__ON_BOTH_A_PARAMETER_AND_A_RETURN_TYPE"></span>нельзя использовать [comm_status] как для параметра, так и для типа возвращаемого значения</dt> <dd> И процедура, и один из ее параметров имеют атрибут [<a href="comm-status.md"><strong>comm_status</strong></a>]. Атрибут [<strong>comm_status</strong>] указывает, что в каждый момент времени только один объект данных может иметь тип <a href="error-status-t.md"><strong>error_status_t</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2051"></span><span id="midl2051"></span><dl> <dt><strong>MIDL2051</strong></dt> </dl></td>
<td><dl> <dt><span id="__local__attribute_on_a_procedure_requires__ms_ext"></span><span id="__LOCAL__ATTRIBUTE_ON_A_PROCEDURE_REQUIRES__MS_EXT"></span> для атрибута [local] в процедуре требуется/ms_ext</dt> <dd> Атрибут [<a href="local.md"><strong>Local</strong></a>] является расширением Microsoft для устройства DCE IDL. Чтобы использовать этот атрибут для функции, нельзя компилировать с параметром <a href="-osf.md"><strong>/ОСФ</strong></a> . Параметр <strong>/ОСФ</strong> переопределяет параметры командной строки компилятора MIDL по умолчанию <a href="-ms-ext.md"><strong>/ms_ext</strong></a> и <a href="-c-ext.md"><strong>/c_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2052"></span><span id="midl2052"></span><dl> <dt><strong>MIDL2052</strong></dt> </dl></td>
<td><dl> <dt><span id="property_attributes_may_only_be_used_with_procedures"></span><span id="PROPERTY_ATTRIBUTES_MAY_ONLY_BE_USED_WITH_PROCEDURES"></span>атрибуты свойств могут использоваться только с процедурами</dt> <dd> Неправильное использование атрибута [<a href="propget.md"><strong>propget</strong></a>], [<a href="propput.md"><strong>propput</strong></a>] или [<a href="propputref.md"><strong>propputref</strong></a>]. Убедитесь, что имя функции свойства указано правильно и что свойство и функция имеют одно и то же имя.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2053"></span><span id="midl2053"></span><dl> <dt><strong>MIDL2053</strong></dt> </dl></td>
<td><dl> <dt><span id="a_procedure_may_not_have_more_than_one_property_attribute"></span><span id="A_PROCEDURE_MAY_NOT_HAVE_MORE_THAN_ONE_PROPERTY_ATTRIBUTE"></span>процедура не может иметь более одного атрибута свойства</dt> <dd> Для функции можно указать только один из атрибутов [<a href="propget.md"><strong>propget</strong></a>], [<a href="propput.md"><strong>propput</strong></a>] или [<a href="propputref.md"><strong>propputref</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2054"></span><span id="midl2054"></span><dl> <dt><strong>MIDL2054</strong></dt> </dl></td>
<td><dl> <dt><span id="the_procedure_has_an_illegal_combination_of_operation_attributes"></span><span id="THE_PROCEDURE_HAS_AN_ILLEGAL_COMBINATION_OF_OPERATION_ATTRIBUTES"></span>процедура имеет недопустимое сочетание атрибутов операций.</dt> <dd> Некоторые атрибуты не могут использоваться в соединении с другими атрибутами. Точные требования и синтаксис атрибутов, используемых в этой процедуре, см. в справочнике по языку MIDL.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2055"></span><span id="midl2055"></span><dl> <dt><strong>MIDL2055</strong></dt> </dl></td>
<td><dl> <dt><span id="field_deriving_from_a_conformant_array_must_be_the_last_member_of_the_structure"></span><span id="FIELD_DERIVING_FROM_A_CONFORMANT_ARRAY_MUST_BE_THE_LAST_MEMBER_OF_THE_STRUCTURE"></span>поле, производное от согласованного массива, должно быть последним членом структуры</dt> <dd> Структура содержит согласованный массив, который не является последним элементом структуры. В качестве последнего элемента структуры должен использоваться согласованный массив.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2056"></span><span id="midl2056"></span><dl> <dt><strong>MIDL2056</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicate__case__label"></span><span id="DUPLICATE__CASE__LABEL"></span>Повторяющаяся метка [Case]</dt> <dd> Указана повторяющаяся метка case. Отображается повторяющаяся метка.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2057"></span><span id="midl2057"></span><dl> <dt><strong>MIDL2057</strong></dt> </dl></td>
<td><dl> <dt><span id="no__default__case_specified_for_discriminated_union"></span><span id="NO__DEFAULT__CASE_SPECIFIED_FOR_DISCRIMINATED_UNION"></span>нет варианта [default], указанного для размеченного объединения</dt> <dd> Размеченное объединение было указано без варианта по умолчанию.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2058"></span><span id="midl2058"></span><dl> <dt><strong>MIDL2058</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_cannot_be_resolved"></span><span id="ATTRIBUTE_EXPRESSION_CANNOT_BE_RESOLVED"></span>не удается разрешить выражение атрибута</dt> <dd> Не удается разрешить выражение, связанное с атрибутом. Эта ошибка обычно возникает, когда переменная, которая отображается в выражении, не определена. Например, ошибка может возникать, если переменная <em>s</em> не определена и используется атрибутом [<a href="size-is.md"><strong>size_is</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2059"></span><span id="midl2059"></span><dl> <dt><strong>MIDL2059</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_must_be_of_integral_type__no_support_for_64-bit_expressions"></span><span id="ATTRIBUTE_EXPRESSION_MUST_BE_OF_INTEGRAL_TYPE__NO_SUPPORT_FOR_64-BIT_EXPRESSIONS"></span>выражение атрибута должно иметь целочисленный тип, без поддержки 64-разрядных выражений</dt> <dd> Указанная переменная или выражение атрибута должны быть целочисленным типом. Эта ошибка возникает, когда тип атрибута-Expression не разрешается в целое число.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2060"></span><span id="midl2060"></span><dl> <dt><strong>MIDL2060</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__requires__ms_ext"></span><span id="_BYTE_COUNT__REQUIRES__MS_EXT"></span>для [byte_count] требуется/ms_ext</dt> <dd> Атрибут [<a href="byte-count.md"><strong>byte_count</strong></a>] является расширением Майкрософт для устройства DCE IDL. Для использования этого атрибута нельзя компилировать с помощью параметра <a href="-osf.md"><strong>/ОСФ</strong></a> , который переопределяет параметры компилятора MIDL по умолчанию <a href="-ms-ext.md"><strong>/ms_ext</strong></a> и <a href="-c-ext.md"><strong>/c_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2061"></span><span id="midl2061"></span><dl> <dt><strong>MIDL2061</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__can_be_applied_only_to_out_parameters_of_pointer_type"></span><span id="_BYTE_COUNT__CAN_BE_APPLIED_ONLY_TO_OUT_PARAMETERS_OF_POINTER_TYPE"></span>[byte_count] можно применять только к выходным параметрам типа указателя</dt> <dd> Атрибут [<a href="byte-count.md"><strong>byte_count</strong></a>] может применяться только к параметрам [<a href="out-idl.md"><strong>out</strong></a>], а все параметры [<strong>out</strong>] должны быть типами указателей.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2062"></span><span id="midl2062"></span><dl> <dt><strong>MIDL2062</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__cannot_be_specified_on_a_pointer_to_a_conformant_array_or_structure"></span><span id="_BYTE_COUNT__CANNOT_BE_SPECIFIED_ON_A_POINTER_TO_A_CONFORMANT_ARRAY_OR_STRUCTURE"></span>[byte_count] нельзя указывать в указателе на согласованный массив или структуру</dt> <dd> Атрибут [<a href="byte-count.md"><strong>byte_count</strong></a>] не может быть применен к согласованному массиву или структуре.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2063"></span><span id="midl2063"></span><dl> <dt><strong>MIDL2063</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_specifying_the_byte_count_is_not__in__only_or_byte_count_parameter_is_not__out__only"></span><span id="PARAMETER_SPECIFYING_THE_BYTE_COUNT_IS_NOT__IN__ONLY_OR_BYTE_COUNT_PARAMETER_IS_NOT__OUT__ONLY"></span>параметр, указывающий число байтов, не [in], или параметр числа байтов не [out].</dt> <dd> Значение, связанное с [<a href="byte-count.md"><strong>byte_count</strong></a>], должно передаваться с клиента на сервер. Он должен быть параметром [<a href="in.md"><strong>in</strong></a>]. Параметр [<strong>byte_count</strong>] не обязательно должен быть параметром [<strong>in, out</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2064"></span><span id="midl2064"></span><dl> <dt><strong>MIDL2064</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_specifying_the_byte_count_is_not_an_integral_type"></span><span id="PARAMETER_SPECIFYING_THE_BYTE_COUNT_IS_NOT_AN_INTEGRAL_TYPE"></span>параметр, указывающий число байтов, не является целочисленным типом</dt> <dd> Значение, связанное с числом байтов, должно быть целочисленным типом <a href="int.md"><strong>int</strong></a>, <a href="small.md"><strong>Small</strong></a>, <a href="short.md"><strong>Short</strong></a>или <a href="long.md"><strong>Long</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2065"></span><span id="midl2065"></span><dl> <dt><strong>MIDL2065</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__cannot_be_specified_on_a_parameter_with_size_attributes"></span><span id="_BYTE_COUNT__CANNOT_BE_SPECIFIED_ON_A_PARAMETER_WITH_SIZE_ATTRIBUTES"></span>[byte_count] нельзя указывать для параметра с атрибутами size</dt> <dd> Атрибут [<a href="byte-count.md"><strong>byte_count</strong></a>] нельзя использовать с другими атрибутами размера, такими как [<a href="size-is.md"><strong>size_is</strong></a>] или [<a href="length-is.md"><strong>length_is</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2066"></span><span id="midl2066"></span><dl> <dt><strong>MIDL2066</strong></dt> </dl></td>
<td><dl> <dt><span id="_case__expression_is_not_constant"></span><span id="_CASE__EXPRESSION_IS_NOT_CONSTANT"></span>выражение [Case] не является константой</dt> <dd> Выражение, указанное для метки case, не является константой.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2067"></span><span id="midl2067"></span><dl> <dt><strong>MIDL2067</strong></dt> </dl></td>
<td><dl> <dt><span id="_case__expression_is_not_of_integral_type"></span><span id="_CASE__EXPRESSION_IS_NOT_OF_INTEGRAL_TYPE"></span>выражение [Case] не относится к целому типу</dt> <dd> Выражение, указанное для метки case, имеет тип, отличный от Integer.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2068"></span><span id="midl2068"></span><dl> <dt><strong>MIDL2068</strong></dt> </dl></td>
<td><dl> <dt><span id="specifying__context_handle__on_a_type_other_than_void___requires__ms_ext"></span><span id="SPECIFYING__CONTEXT_HANDLE__ON_A_TYPE_OTHER_THAN_VOID___REQUIRES__MS_EXT"></span>Указание [context_handle] для типа, отличного от void *, требует/ms_ext</dt> <dd> Для совместимости с DCE-RPC описатель контекста должен быть указателем типа <strong>void *</strong>. Если вы хотите, чтобы дескрипторы контекста были связаны с типами, отличными от <strong>void *</strong>, не используйте параметр компилятора MIDL <a href="-osf.md"><strong>/ОСФ</strong></a>, который переопределяет параметр компилятора MIDL по умолчанию <a href="-ms-ext.md"><strong>/ms_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2069"></span><span id="midl2069"></span><dl> <dt><strong>MIDL2069</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_specify_more_than_one_parameter_with_each_of_comm_status_fault_status"></span><span id="CANNOT_SPECIFY_MORE_THAN_ONE_PARAMETER_WITH_EACH_OF_COMM_STATUS_FAULT_STATUS"></span>невозможно указать более одного параметра с каждым из comm_status и fault_status</dt> <dd> Процедура может иметь только один параметр с атрибутом [<a href="comm-status.md"><strong>comm_status</strong></a>]. Он может иметь не более одного параметра с атрибутом [<a href="fault-status.md"><strong>fault_status</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2070"></span><span id="midl2070"></span><dl> <dt><strong>MIDL2070</strong></dt> </dl></td>
<td><dl> <dt><span id="comm_status_fault_status_parameter_must_be_an__out__only_pointer_parameter"></span><span id="COMM_STATUS_FAULT_STATUS_PARAMETER_MUST_BE_AN__OUT__ONLY_POINTER_PARAMETER"></span>параметр comm_status/fault_status должен быть только параметром указателя [out].</dt> <dd> Типы кода ошибки [<a href="comm-status.md"><strong>comm_status</strong></a>] и [<a href="fault-status.md"><strong>fault_status</strong></a>] передаются с сервера на клиент и, следовательно, должны быть указаны в качестве параметра [<a href="out-idl.md"><strong>out</strong></a>]. В связи с ограничениями языка программирования C все параметры [<strong>out</strong>] должны быть указателями.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2071"></span><span id="midl2071"></span><dl> <dt><strong>MIDL2071</strong></dt> </dl></td>
<td><dl> <dt><span id="endpoint_syntax_error"></span><span id="ENDPOINT_SYNTAX_ERROR"></span>Синтаксическая ошибка конечной точки</dt> <dd> Неверный синтаксис конечной точки.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2072"></span><span id="midl2072"></span><dl> <dt><strong>MIDL2072</strong></dt> </dl></td>
<td><dl> <dt><span id="inapplicable_attribute"></span><span id="INAPPLICABLE_ATTRIBUTE"></span>неприменимый атрибут</dt> <dd> Указанный атрибут не может быть применен в этой конструкции. Например, атрибут String применяется к массивам <a href="char-idl.md"><strong>char</strong></a> или указателям <strong>char</strong> и не может применяться к структуре, состоящей из двух <a href="short.md"><strong>коротких</strong></a> целых чисел: <br/>
<pre class="syntax" data-space="preserve"><code>typedef [string] struct moo 
{
    short x;
    short y;
};</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2073"></span><span id="midl2073"></span><dl> <dt><strong>MIDL2073</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__requires__ms_ext"></span><span id="_ALLOCATE__REQUIRES__MS_EXT"></span>[выделение] требуется/ms_ext</dt> <dd> Атрибут <a href="allocate.md"><strong>выделения</strong></a> представляет собой расширение Microsoft, которое не определено как часть DCE RPC. Чтобы использовать этот атрибут, нельзя компилировать с помощью параметра <a href="-osf.md"><strong>/ОСФ</strong></a> , который переопределяет параметр компилятора MIDL по умолчанию <a href="-ms-ext.md"><strong>/ms_ext</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2074"></span><span id="midl2074"></span><dl> <dt><strong>MIDL2074</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid__allocate__mode"></span><span id="INVALID__ALLOCATE__MODE"></span>Недопустимый режим [выделение]</dt> <dd> Указан недопустимый режим для конструкции атрибута [<a href="allocate.md"><strong>allocate</strong></a>]. Четыре допустимых режима: single_node, all_nodes, on_null и Always.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2075"></span><span id="midl2075"></span><dl> <dt><strong>MIDL2075</strong></dt> </dl></td>
<td><dl> <dt><span id="length_attributes_cannot_be_applied_with_string_attribute"></span><span id="LENGTH_ATTRIBUTES_CANNOT_BE_APPLIED_WITH_STRING_ATTRIBUTE"></span>атрибуты длины не могут быть применены с строковым атрибутом</dt> <dd> При использовании строкового атрибута созданные файлы-заглушки вызывают функцию <strong>strlen</strong> для определения длины строки. Не используйте атрибут Length и строковый атрибут для одной и той же переменной.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2076"></span><span id="midl2076"></span><dl> <dt><strong>MIDL2076</strong></dt> </dl></td>
<td><dl> <dt><span id="_last_is__and__length_is__cannot_be_specified_at_the_same_time"></span><span id="_LAST_IS__AND__LENGTH_IS__CANNOT_BE_SPECIFIED_AT_THE_SAME_TIME"></span>нельзя указывать [last_is] и [length_is] одновременно</dt> <dd> Для одного массива указаны оба [<a href="last-is.md"><strong>last_is</strong></a>] и [<a href="length-is.md"><strong>length_is</strong></a>]. Эти атрибуты связаны следующим образом: длина = последняя первая + 1. Так как каждое значение может быть производным от другого, не указывайте оба значения.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2077"></span><span id="midl2077"></span><dl> <dt><strong>MIDL2077</strong></dt> </dl></td>
<td><dl> <dt><span id="_max_is__and__size_is__cannot_be_specified_at_the_same_time"></span><span id="_MAX_IS__AND__SIZE_IS__CANNOT_BE_SPECIFIED_AT_THE_SAME_TIME"></span>нельзя указывать [max_is] и [size_is] одновременно</dt> <dd> Для одного массива указаны оба [ <a href="max-is.md"><strong>max_is</strong></a>] и [ <a href="size-is.md"><strong>size_is</strong></a>]. Эти атрибуты связаны следующим образом: Max = size + 1. Так как каждое значение может быть производным от другого, не указывайте оба значения.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2078"></span><span id="midl2078"></span><dl> <dt><strong>MIDL2078</strong></dt> </dl></td>
<td><dl> <dt><span id="no__switch_is__attribute_specified_at_use_of_union"></span><span id="NO__SWITCH_IS__ATTRIBUTE_SPECIFIED_AT_USE_OF_UNION"></span>атрибут [switch_is] не указан при использовании объединения</dt> <dd> Для объединения не указан discriminant. Атрибут [<a href="switch-is.md"><strong>switch_is</strong></a>] указывает на discriminant, используемый для выбора из полей Union.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2079"></span><span id="midl2079"></span><dl> <dt><strong>MIDL2079</strong></dt> </dl></td>
<td><dl> <dt><span id="no__uuid__specified"></span><span id="NO__UUID__SPECIFIED"></span>не указан [UUID]</dt> <dd> Для интерфейса не указан UUID.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2080"></span><span id="midl2080"></span><dl> <dt><strong>MIDL2080</strong></dt> </dl></td>
<td><dl> <dt><span id="_uuid__ignored_on__local__interface"></span><span id="_UUID__IGNORED_ON__LOCAL__INTERFACE"></span>[UUID] игнорируется в интерфейсе [local]</dt> <dd> Использование атрибута [<a href="local.md"><strong>Local</strong></a>] в интерфейсе объектов приводит к тому, что компилятор MIDL игнорирует атрибут [<a href="uuid.md"><strong>UUID</strong></a>]. В интерфейсе RPC нельзя использовать оба атрибута.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2081"></span><span id="midl2081"></span><dl> <dt><strong>MIDL2081</strong></dt> </dl></td>
<td><dl> <dt><span id="type_mismatch_between_length_and_size_attribute_expressions"></span><span id="TYPE_MISMATCH_BETWEEN_LENGTH_AND_SIZE_ATTRIBUTE_EXPRESSIONS"></span>несоответствие типов для выражений атрибутов длины и размера</dt> <dd> Выражения атрибутов длины и размера должны быть одного типа. Например, это предупреждение выдается, когда переменная атрибута для выражения [<a href="size-is.md"><strong>size_is</strong></a>] имеет тип <strong>Long без знака</strong> , а переменная атрибута для выражения [<a href="length-is.md"><strong>length_is</strong></a>] имеет тип <a href="long.md"><strong>Long</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2082"></span><span id="midl2082"></span><dl> <dt><strong>MIDL2082</strong></dt> </dl></td>
<td><dl> <dt><span id="_string__attribute_must_be_specified__byte____char___or__wchar_t__array_or_pointer"></span><span id="_STRING__ATTRIBUTE_MUST_BE_SPECIFIED__BYTE____CHAR___OR__WCHAR_T__ARRAY_OR_POINTER"></span>атрибут [String] должен иметь указанный &quot; тип Byte, &quot; &quot; char &quot; или &quot; wchar_t &quot; массиве или указателе</dt> <dd> Атрибут String не может быть применен к указателю или массиву, базовый тип которого не является <a href="byte.md"><strong>байтом</strong></a>, типом <a href="char-idl.md"><strong>char</strong></a>или <a href="struct.md"><strong>структурой</strong></a> , в которой элементы имеют тип <strong>Byte</strong> или <strong>char</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2083"></span><span id="midl2083"></span><dl> <dt><strong>MIDL2083</strong></dt> </dl></td>
<td><dl> <dt><span id="mismatch_between_the_type_of_the__switch_is__expression_and_the_switch_type_of_the_union"></span><span id="MISMATCH_BETWEEN_THE_TYPE_OF_THE__SWITCH_IS__EXPRESSION_AND_THE_SWITCH_TYPE_OF_THE_UNION"></span>несоответствие между типом выражения [switch_is] и типом переключателя объединения</dt> <dd> Если объединение [<a href="switch-type.md"><strong>switch_type</strong></a>] не указано, тип переключателя совпадает с типом поля [<a href="switch-is.md"><strong>switch_is</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2084"></span><span id="midl2084"></span><dl> <dt><strong>MIDL2084</strong></dt> </dl></td>
<td><dl> <dt><span id="_transmit_as__must_not_be_applied_to_a_type_that_derives_from_a_context_handle"></span><span id="_TRANSMIT_AS__MUST_NOT_BE_APPLIED_TO_A_TYPE_THAT_DERIVES_FROM_A_CONTEXT_HANDLE"></span>[transmit_as] не должен применяться к типу, производному от обработчика контекста</dt> <dd> Дескрипторы контекста не могут передаваться как другие типы.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2085"></span><span id="midl2085"></span><dl> <dt><strong>MIDL2085</strong></dt> </dl></td>
<td><dl> <dt><span id="_transmit_as__must_specify_a_transmissible_type"></span><span id="_TRANSMIT_AS__MUST_SPECIFY_A_TRANSMISSIBLE_TYPE"></span>[transmit_as] должен указывать тип трансмиссибле</dt> <dd> Указанный тип [<a href="transmit-as.md"><strong>transmit_as</strong></a>] является производным от типа, который не может быть передан Microsoft RPC, например <a href="void.md"><strong>void</strong></a>, <strong>void *</strong>или <a href="int.md"><strong>int</strong></a>. Использовать определенный базовый тип RPC; в случае с <strong>типом int</strong>добавьте описатели размера, например <a href="small.md"><strong>небольшие</strong></a>, <a href="short.md"><strong>короткие</strong></a>или <a href="long.md"><strong>длинные</strong></a> , для уточнения <strong>типа int</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2086"></span><span id="midl2086"></span><dl> <dt><strong>MIDL2086</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_type_for__transmit_as__and__represent_as__must_not_be_a_pointer_or_derive_from_a_pointer"></span><span id="TRANSMITTED_TYPE_FOR__TRANSMIT_AS__AND__REPRESENT_AS__MUST_NOT_BE_A_POINTER_OR_DERIVE_FROM_A_POINTER"></span>передаваемый тип для [transmit_as] и [represent_as] не должен быть указателем или производным от указателя</dt> <dd> Передаваемый тип не может быть указателем или производным от указателя.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2087"></span><span id="midl2087"></span><dl> <dt><strong>MIDL2087</strong></dt> </dl></td>
<td><dl> <dt><span id="presented_type_for__transmit_as__and__represent_as__must_not_derive_from_a_conformant_varying_array__its_pointer_equivalent__or_a_conformant_varying_structure"></span><span id="PRESENTED_TYPE_FOR__TRANSMIT_AS__AND__REPRESENT_AS__MUST_NOT_DERIVE_FROM_A_CONFORMANT_VARYING_ARRAY__ITS_POINTER_EQUIVALENT__OR_A_CONFORMANT_VARYING_STRUCTURE"></span>представленный тип для [transmit_as] и [represent_as] не должен быть производным от согласованного или изменяющегося массива, его эквивалента указателя или соответствующей структуры.</dt> <dd> Тип, к которому применен [<a href="transmit-as.md"><strong>transmit_as</strong></a>], не может быть производным от согласованного массива или структуры (массива или структуры, размер которых определяется во время выполнения).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2088"></span><span id="midl2088"></span><dl> <dt><strong>MIDL2088</strong></dt> </dl></td>
<td><dl> <dt><span id="_uuid__format_is_incorrect"></span><span id="_UUID__FORMAT_IS_INCORRECT"></span>Недопустимый формат [UUID]</dt> <dd> Формат UUID не соответствует спецификации. UUID должен быть строкой, состоящей из пяти последовательностей шестнадцатеричных цифр длиной 8, 4, 4, 4 и 12 цифр. &quot;12345678-1234-ABCD-EF01-28A49C28F17D &quot; — допустимый UUID. Чтобы создать допустимый UUID, используйте функцию <a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidcreate"><strong>ууидкреате</strong></a> или служебную программу.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2089"></span><span id="midl2089"></span><dl> <dt><strong>MIDL2089</strong></dt> </dl></td>
<td><dl> <dt><span id="uuid_is_not_a_hexadecimal_number"></span><span id="UUID_IS_NOT_A_HEXADECIMAL_NUMBER"></span>UUID не является шестнадцатеричным числом</dt> <dd> Идентификатор UUID, указанный для интерфейса, содержит символы, недопустимые в шестнадцатеричном числовом представлении. Символы от 0 до 9 и от A до F являются допустимыми в шестнадцатеричном представлении.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2090"></span><span id="midl2090"></span><dl> <dt><strong>MIDL2090</strong></dt> </dl></td>
<td><dl> <dt><span id="optional_parameters_must_come_after_required_parameters"></span><span id="OPTIONAL_PARAMETERS_MUST_COME_AFTER_REQUIRED_PARAMETERS"></span>необязательные параметры должны следовать после обязательных параметров</dt> <dd> Описание порядка следования списков параметров см. в разделе [<a href="optional.md"><strong>необязательно</strong></a>] Справочник по языку MIDL.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2091"></span><span id="midl2091"></span><dl> <dt><strong>MIDL2091</strong></dt> </dl></td>
<td><dl> <dt><span id="_dllname__required_when__entry__is_used"></span><span id="_DLLNAME__REQUIRED_WHEN__ENTRY__IS_USED"></span>[dllname] требуется при использовании [Entry]</dt> <dd> При указании точки входа в библиотеку DLL необходимо также указать имя библиотеки DLL с помощью атрибута [<a href="dllname-str-.md"><strong>dllname</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2092"></span><span id="midl2092"></span><dl> <dt><strong>MIDL2092</strong></dt> </dl></td>
<td><dl> <dt><span id="_bindable__is_invalid_without__propget____propput___or__propputref_"></span><span id="_BINDABLE__IS_INVALID_WITHOUT__PROPGET____PROPPUT___OR__PROPPUTREF_"></span>[BIND] является недопустимым без [propget], [propput] или [propputref]</dt> <dd> Атрибут [<a href="bindable.md"><strong>BIND</strong></a>] допустим только для свойства, поэтому необходимо также указать одну из функций доступа к свойствам или свойству.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2093"></span><span id="midl2093"></span><dl> <dt><strong>MIDL2093</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with__propput__or__propputref__must_have_at_least_one_parameter"></span><span id="PROCEDURES_WITH__PROPPUT__OR__PROPPUTREF__MUST_HAVE_AT_LEAST_ONE_PARAMETER"></span>процедуры с [propput] или [propputref] должны иметь хотя бы один параметр.</dt> <dd> Процедура [<a href="propput.md"><strong>propput</strong></a>] или [ <a href="propputref.md"><strong>propputref</strong></a>] должна содержать по крайней мере параметр [<a href="in.md"><strong>in</strong></a>] с заданным свойством. для получения свойства или ссылки процедура [<a href="propget.md"><strong>propget</strong></a>] должна иметь по крайней мере параметр [<a href="out-idl.md"><strong>out</strong></a>, <a href="retval.md"><strong>retval</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2094"></span><span id="midl2094"></span><dl> <dt><strong>MIDL2094</strong></dt> </dl></td>
<td><dl> <dt><span id="_id__attribute_is_required"></span><span id="_ID__ATTRIBUTE_IS_REQUIRED"></span>атрибут [ID] является обязательным</dt> <dd> Эта функция-член, обусловленная используемым синтаксисом <a href="dispinterface.md"><strong>disp-интерфейса</strong></a> , требует DISPID, который указывается с помощью атрибута [ <a href="id.md"><strong>ID</strong></a>]. При указании <strong>disp-интерфейса</strong> с помощью свойств и методов необходимо указать DISPID для каждого свойства и метода.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2095"></span><span id="midl2095"></span><dl> <dt><strong>MIDL2095</strong></dt> </dl></td>
<td><dl> <dt><span id="interface_name_specified_in_the_ACF_does_not_match_that_specified_in_the_IDL_file"></span><span id="interface_name_specified_in_the_acf_does_not_match_that_specified_in_the_idl_file"></span><span id="INTERFACE_NAME_SPECIFIED_IN_THE_ACF_DOES_NOT_MATCH_THAT_SPECIFIED_IN_THE_IDL_FILE"></span>имя интерфейса, указанное в ACF, не соответствует значению, указанному в IDL-файле</dt> <dd> В текущем режиме компилятора имя, которое следует за ключевым словом Interface в ACF, должно совпадать с именем, которое следует за ключевым словом Interface в IDL-файле. Имена интерфейсов в файлах IDL и ACF могут отличаться при компиляции с параметром компилятора MIDL <a href="-acf.md"><strong>/АКФ</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2096"></span><span id="midl2096"></span><dl> <dt><strong>MIDL2096</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicated_attribute"></span><span id="DUPLICATED_ATTRIBUTE"></span>дублирующийся атрибут</dt> <dd> Были указаны дублирующиеся или конфликтующие атрибуты. Эта ошибка часто возникает, когда два атрибута являются взаимоисключающими. Например, нельзя одновременно использовать атрибуты [<a href="code.md"><strong>Code</strong></a>] и [<a href="nocode.md"><strong>декодирует</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2097"></span><span id="midl2097"></span><dl> <dt><strong>MIDL2097</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_with__comm_status__or__fault_status__attribute_must_be_a_pointer_to_type_error_status_t"></span><span id="PARAMETER_WITH__COMM_STATUS__OR__FAULT_STATUS__ATTRIBUTE_MUST_BE_A_POINTER_TO_TYPE_ERROR_STATUS_T"></span>параметр с атрибутом [comm_status] или [fault_status] должен быть указателем на тип error_status_t</dt> <dd> Если в качестве атрибута параметра используется [<a href="fault-status.md"><strong>fault_status</strong></a>] или [<a href="comm-status.md"><strong>comm_status</strong></a>], параметр должен быть параметром [<a href="out-idl.md"><strong>out</strong></a>] типа <a href="error-status-t.md"><strong>error_status_t</strong></a>. При возникновении ошибки сервера параметру присваивается код ошибки. После успешного завершения удаленного вызова процедура задает значение.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2098"></span><span id="midl2098"></span><dl> <dt><strong>MIDL2098</strong></dt> </dl></td>
<td><dl> <dt><span id="a__local__procedure_cannot_be_specified_in_ACF_file"></span><span id="a__local__procedure_cannot_be_specified_in_acf_file"></span><span id="A__LOCAL__PROCEDURE_CANNOT_BE_SPECIFIED_IN_ACF_FILE"></span>Процедура [local] не может быть указана в файле ACF</dt> <dd> В ACF указана локальная процедура. Локальная процедура может быть указана только в IDL-файле.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2099"></span><span id="midl2099"></span><dl> <dt><strong>MIDL2099</strong></dt> </dl></td>
<td><dl> <dt><span id="specified_type_is_not_defined_as_a_handle"></span><span id="SPECIFIED_TYPE_IS_NOT_DEFINED_AS_A_HANDLE"></span>указанный тип не определен как Handle</dt> <dd> Тип, указанный в атрибуте [<a href="implicit-handle.md"><strong>implicit_handle</strong></a>], не определен как тип обработчика. Измените определение типа или имя типа, заданное атрибутом.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2100"></span><span id="midl2100"></span><dl> <dt><strong>MIDL2100</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_undefined"></span><span id="PROCEDURE_UNDEFINED"></span>процедура не определена</dt> <dd> К процедуре в ACF был применен атрибут, а эта процедура не определена в IDL-файле.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2101"></span><span id="midl2101"></span><dl> <dt><strong>MIDL2101</strong></dt> </dl></td>
<td><dl> <dt><span id="this_parameter_does_not_exist_in_the_IDL_file"></span><span id="this_parameter_does_not_exist_in_the_idl_file"></span><span id="THIS_PARAMETER_DOES_NOT_EXIST_IN_THE_IDL_FILE"></span>Этот параметр не существует в IDL-файле</dt> <dd> Параметр, указанный в ACF, не существует в определении в IDL-файле. Все параметры, функции и определения типов, которые отображаются в ACF, должны соответствовать параметрам, функциям и типам, ранее определенным в IDL-файле.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2102"></span><span id="midl2102"></span><dl> <dt><strong>MIDL2102</strong></dt> </dl></td>
<td><dl> <dt><span id="this_array-bounds_construct_is_not_supported"></span><span id="THIS_ARRAY-BOUNDS_CONSTRUCT_IS_NOT_SUPPORTED"></span>Эта конструкция с границами массива не поддерживается</dt> <dd> В настоящее время MIDL поддерживает выражение верхней и нижней границ массива в виде массива [ниже. Upper] только если константа, указывающая нижнюю границу массива, разрешается в нулевое значение.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2103"></span><span id="midl2103"></span><dl> <dt><strong>MIDL2103</strong></dt> </dl></td>
<td><dl> <dt><span id="array_bound_specification_is_illegal"></span><span id="ARRAY_BOUND_SPECIFICATION_IS_ILLEGAL"></span>Недопустимая спецификация привязки к массиву</dt> <dd> Пользовательская спецификация границ массива для массива фиксированного размера недопустима. Пример: <br/>
<pre class="syntax" data-space="preserve"><code>typedef short Array[-1]</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2104"></span><span id="midl2104"></span><dl> <dt><strong>MIDL2104</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_to_a_conformant_array_or_an_array_that_contains_a_conformant_array_is_not_supported"></span><span id="POINTER_TO_A_CONFORMANT_ARRAY_OR_AN_ARRAY_THAT_CONTAINS_A_CONFORMANT_ARRAY_IS_NOT_SUPPORTED"></span>Указатель на совместимый массив или массив, содержащий совместимый массив, не поддерживается</dt> <dd> Недопустимое использование согласованного массива. Правила, управляющие согласованными массивами, см. в разделе <a href="/windows/desktop/Rpc/arrays-and-rpc">массивы и RPC</a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2105"></span><span id="midl2105"></span><dl> <dt><strong>MIDL2105</strong></dt> </dl></td>
<td><dl> <dt><span id="pointee_array_does_not_derive_any_size"></span><span id="POINTEE_ARRAY_DOES_NOT_DERIVE_ANY_SIZE"></span>точка или массив не является производным от какого-либо размера</dt> <dd> Согласованный массив был указан без какой-либо спецификации размера. Размер можно указать с помощью атрибута [<a href="max-is.md"><strong>max_is</strong></a>] или [<a href="size-is.md"><strong>size_is</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2106"></span><span id="midl2106"></span><dl> <dt><strong>MIDL2106</strong></dt> </dl></td>
<td><dl> <dt><span id="only_fixed_arrays_and_SAFEARRAYs_are_legal_in_a_type_library"></span><span id="only_fixed_arrays_and_safearrays_are_legal_in_a_type_library"></span><span id="ONLY_FIXED_ARRAYS_AND_SAFEARRAYS_ARE_LEGAL_IN_A_TYPE_LIBRARY"></span>в библиотеке типов допустимы только фиксированные массивы и массивы SAFEARRAY</dt> <dd> Вы использовали тип массива внутри оператора Library, который не может использоваться в библиотеке типов.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2107"></span><span id="midl2107"></span><dl> <dt><strong>MIDL2107</strong></dt> </dl></td>
<td><dl> <dt><span id="SAFEARRAYs_are_only_legal_inside_a_library_block"></span><span id="safearrays_are_only_legal_inside_a_library_block"></span><span id="SAFEARRAYS_ARE_ONLY_LEGAL_INSIDE_A_LIBRARY_BLOCK"></span>МАССИВы SAFEARRAY допустимы только внутри блока Library</dt> <dd> Компилятор MIDL не распознает SAFEARRAY как допустимый тип данных, за исключением случаев создания библиотеки типов.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2108"></span><span id="midl2108"></span><dl> <dt><strong>MIDL2108</strong></dt> </dl></td>
<td><dl> <dt><span id="badly_formed_character_constant"></span><span id="BADLY_FORMED_CHARACTER_CONSTANT"></span>неправильно сформированная символьная константа</dt> <dd> Символ конца строки не допускается в символьных константах.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2109"></span><span id="midl2109"></span><dl> <dt><strong>MIDL2109</strong></dt> </dl></td>
<td><dl> <dt><span id="end_of_file_found_in_comment"></span><span id="END_OF_FILE_FOUND_IN_COMMENT"></span>конец файла найден в комментарии</dt> <dd> В комментарии обнаружен символ конца файла.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2110"></span><span id="midl2110"></span><dl> <dt><strong>MIDL2110</strong></dt> </dl></td>
<td><dl> <dt><span id="end_of_file_found_in_string"></span><span id="END_OF_FILE_FOUND_IN_STRING"></span>конец файла найден в строке</dt> <dd> В строке обнаружен символ конца файла.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2111"></span><span id="midl2111"></span><dl> <dt><strong>MIDL2111</strong></dt> </dl></td>
<td><dl> <dt><span id="identifier_length_exceeds_31_characters"></span><span id="IDENTIFIER_LENGTH_EXCEEDS_31_CHARACTERS"></span>Длина идентификатора превышает 31 символ</dt> <dd> Длина идентификаторов ограничена 31 алфавитно-цифровыми символами. Имена идентификаторов длиннее 31 символа усекаются.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2112"></span><span id="midl2112"></span><dl> <dt><strong>MIDL2112</strong></dt> </dl></td>
<td><dl> <dt><span id="end_of_line_found_in_string"></span><span id="END_OF_LINE_FOUND_IN_STRING"></span>конец строки обнаружен в строке</dt> <dd> В строке обнаружен символ конца строки. Убедитесь, что вы включили символ двойной кавычки, который завершает строку.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2113"></span><span id="midl2113"></span><dl> <dt><strong>MIDL2113</strong></dt> </dl></td>
<td><dl> <dt><span id="string_constant_exceeds_limit_of_255_characters"></span><span id="STRING_CONSTANT_EXCEEDS_LIMIT_OF_255_CHARACTERS"></span>Строковая константа превышает ограничение в 255 символов</dt> <dd> Длина строки превышает максимально допустимую длину в 255 символов.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2114"></span><span id="midl2114"></span><dl> <dt><strong>MIDL2114</strong></dt> </dl></td>
<td><dl> <dt><span id="identifier_exceeds_limit_of_255_characters_and_has_been_truncated"></span><span id="IDENTIFIER_EXCEEDS_LIMIT_OF_255_CHARACTERS_AND_HAS_BEEN_TRUNCATED"></span>Идентификатор превышает ограничение в 255 символов и было усечено</dt> <dd> Длина идентификатора превышает максимально допустимую длину в 255 символов. Лишние символы в идентификаторе усекаются.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2115"></span><span id="midl2115"></span><dl> <dt><strong>MIDL2115</strong></dt> </dl></td>
<td><dl> <dt><span id="constant_too_big"></span><span id="CONSTANT_TOO_BIG"></span>слишком большая константа</dt> <dd> Константа слишком велика для внутреннего представления.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2116"></span><span id="midl2116"></span><dl> <dt><strong>MIDL2116</strong></dt> </dl></td>
<td><dl> <dt><span id="numerical_parsing_error"></span><span id="NUMERICAL_PARSING_ERROR"></span>Числовая ошибка синтаксического анализа</dt> <dd> Компилятору не удалось проанализировать числовой идентификатор.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2117"></span><span id="midl2117"></span><dl> <dt><strong>MIDL2117</strong></dt> </dl></td>
<td><dl> <dt><span id="error_in_opening_file"></span><span id="ERROR_IN_OPENING_FILE"></span>Ошибка при открытии файла</dt> <dd> Операционная система сообщила об ошибке при попытке открыть выходной файл. Эта ошибка может быть вызвана слишком длинным именем файловой системы или дубликатом имени файла.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2118"></span><span id="midl2118"></span><dl> <dt><strong>MIDL2118</strong></dt> </dl></td>
<td>Ошибка привязки к функции<br/></td>
</tr>
<tr class="even">
<td><span id="MIDL2119"></span><span id="midl2119"></span><dl> <dt><strong>MIDL2119</strong></dt> </dl></td>
<td>Ошибка при инициализации OLE<br/></td>
</tr>
<tr class="odd">
<td><span id="MIDL2120"></span><span id="midl2120"></span><dl> <dt><strong>MIDL2120</strong></dt> </dl></td>
<td>Ошибка при загрузке библиотеки<br/></td>
</tr>
<tr class="even">
<td><span id="MIDL2121"></span><span id="midl2121"></span><dl> <dt><strong>MIDL2121</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__only_parameter_must_not_derive_from_a_top-level__unique__or__ptr__pointer_array"></span><span id="_OUT__ONLY_PARAMETER_MUST_NOT_DERIVE_FROM_A_TOP-LEVEL__UNIQUE__OR__PTR__POINTER_ARRAY"></span>[out] только параметр не должен быть производным от указателя или массива верхнего уровня [unique] или [PTR]</dt> <dd> Уникальный указатель не может быть только [<a href="out-idl.md"><strong>out</strong></a>]-параметром. По определению уникальный указатель может меняться от <strong>null</strong> к значению, отличному от<strong>null</strong>. Никакие сведения о параметре [<strong>out</strong>] только не передаются с клиента на сервер.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2122"></span><span id="midl2122"></span><dl> <dt><strong>MIDL2122</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_is_not_applicable_to_this_non-rpcable_union"></span><span id="ATTRIBUTE_IS_NOT_APPLICABLE_TO_THIS_NON-RPCABLE_UNION"></span>атрибут не применим к этому объединению, отличному от рпкабле</dt> <dd> Только атрибуты [<a href="switch-is.md"><strong>switch_is</strong></a>] и [<a href="switch-type.md"><strong>switch_type</strong></a>] применяются к объединению, которое передается как часть удаленного вызова процедуры.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2123"></span><span id="midl2123"></span><dl> <dt><strong>MIDL2123</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_used_for_a_size_attribute_must_not_derive_from_an__out_-only_parameter"></span><span id="EXPRESSION_USED_FOR_A_SIZE_ATTRIBUTE_MUST_NOT_DERIVE_FROM_AN__OUT_-ONLY_PARAMETER"></span>выражение, используемое для атрибута size, не должно быть производным от [out]-параметра</dt> <dd> Значение параметра [<a href="out-idl.md"><strong>out</strong></a>] — только не передается на сервер и не может использоваться для определения длины или размера параметра [<a href="in.md"><strong>in</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2124"></span><span id="midl2124"></span><dl> <dt><strong>MIDL2124</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_used_for_a_length_attribute_for_an__in__parameter_cannot_derive_from_an__out_-only_parameter"></span><span id="EXPRESSION_USED_FOR_A_LENGTH_ATTRIBUTE_FOR_AN__IN__PARAMETER_CANNOT_DERIVE_FROM_AN__OUT_-ONLY_PARAMETER"></span>выражение, используемое для атрибута длины для параметра [in], не может быть производным от [out]-параметра</dt> <dd> Значение параметра [<a href="out-idl.md"><strong>out</strong></a>] — только не передается на сервер и не может использоваться для определения длины или размера параметра [<a href="in.md"><strong>in</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2125"></span><span id="midl2125"></span><dl> <dt><strong>MIDL2125</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of__int__needs__c_ext"></span><span id="USE_OF__INT__NEEDS__C_EXT"></span>использование &quot; целочисленных &quot; требований и c_ext</dt> <dd> MIDL — строго типизированный язык. Все параметры, передаваемые по сети, должны быть производными от одного из базовых типов MIDL. Тип <a href="int.md"><strong>int</strong></a> не определен как часть MIDL. Передаваемые данные должны содержать спецификатор размера: <a href="small.md"><strong>малый</strong></a>, <strong>короткий</strong>или <strong>длинный</strong>. Данные, которые не передаются по сети, могут быть добавлены в интерфейс. Используйте параметр <a href="-c-ext.md"><strong>/c_ext</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2126"></span><span id="midl2126"></span><dl> <dt><strong>MIDL2126</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_field_must_not_be__void_"></span><span id="STRUCT_UNION_FIELD_MUST_NOT_BE__VOID_"></span>поле структуры или объединения не должно быть &quot; пустым&quot;</dt> <dd> Поля в структуре или объединении должны быть объявлены с конкретным базовым типом, поддерживаемым MIDL, или типом, производным от базовых типов. Типы void не допускаются в удаленных операциях.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2127"></span><span id="midl2127"></span><dl> <dt><strong>MIDL2127</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_be_void"></span><span id="ARRAY_ELEMENT_MUST_NOT_BE_VOID"></span>элемент массива не должен быть пустым</dt> <dd> Элемент массива не может быть void.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2128"></span><span id="midl2128"></span><dl> <dt><strong>MIDL2128</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_type_qualifiers_and_or_modifiers_needs__c_ext"></span><span id="USE_OF_TYPE_QUALIFIERS_AND_OR_MODIFIERS_NEEDS__C_EXT"></span>Использование квалификаторов типа и (или) модификаторов требует/c_ext</dt> <dd> Модификаторы типа, такие как <strong>_cdecl</strong> и <strong>_far</strong> , могут быть скомпилированы только при указании параметра <a href="-c-ext.md"><strong>/c_ext</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2129"></span><span id="midl2129"></span><dl> <dt><strong>MIDL2129</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_field_must_not_derive_from_a_function"></span><span id="STRUCT_UNION_FIELD_MUST_NOT_DERIVE_FROM_A_FUNCTION"></span>поле структуры или объединения не должно быть производным от функции</dt> <dd> Поля структуры или объединения должны быть базовыми типами MIDL или типами, производными от этих базовых типов. Функции недопустимы в полях структуры или объединения.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2130"></span><span id="midl2130"></span><dl> <dt><strong>MIDL2130</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_be_a_function"></span><span id="ARRAY_ELEMENT_MUST_NOT_BE_A_FUNCTION"></span>элемент массива не должен быть функцией</dt> <dd> Элемент массива не может быть функцией.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2131"></span><span id="midl2131"></span><dl> <dt><strong>MIDL2131</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_be_a_function"></span><span id="PARAMETER_MUST_NOT_BE_A_FUNCTION"></span>параметр не должен быть функцией</dt> <dd> Параметр для удаленной процедуры должен быть переменной указанного типа. Функция не может быть параметром удаленной процедуры.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2132"></span><span id="midl2132"></span><dl> <dt><strong>MIDL2132</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_with_bit_fields_needs__c_ext"></span><span id="STRUCT_UNION_WITH_BIT_FIELDS_NEEDS__C_EXT"></span>для структуры или объединения с битовыми полями требуется/c_ext</dt> <dd> Необходимо указать параметр компилятора MIDL <a href="-c-ext.md"><strong>/c_ext</strong></a> , чтобы разрешить битовые поля в структурах, которые не передаются при удаленном вызове процедуры.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2133"></span><span id="midl2133"></span><dl> <dt><strong>MIDL2133</strong></dt> </dl></td>
<td><dl> <dt><span id="bit_field_specification_on_a_type_other_that__int__is_a_non-ANSI-compatible_extension"></span><span id="bit_field_specification_on_a_type_other_that__int__is_a_non-ansi-compatible_extension"></span><span id="BIT_FIELD_SPECIFICATION_ON_A_TYPE_OTHER_THAT__INT__IS_A_NON-ANSI-COMPATIBLE_EXTENSION"></span>Спецификация битового поля для типа, который &quot; &quot; не является совместимым с ANSI</dt> <dd> В спецификации языка программирования ANSI C не допускается применение битовых полей к нецелочисленным типам.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2134"></span><span id="midl2134"></span><dl> <dt><strong>MIDL2134</strong></dt> </dl></td>
<td><dl> <dt><span id="bit_field_specification_can_be_applied_only_to_simple__integral_types"></span><span id="BIT_FIELD_SPECIFICATION_CAN_BE_APPLIED_ONLY_TO_SIMPLE__INTEGRAL_TYPES"></span>Спецификация битового поля может применяться только к простым целочисленным типам</dt> <dd> В спецификации языка программирования ANSI C не допускается применение битовых полей к нецелочисленным типам.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2135"></span><span id="midl2135"></span><dl> <dt><strong>MIDL2135</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_field_must_not_derive_from_handle_t_or_a_context-handle"></span><span id="STRUCT_UNION_FIELD_MUST_NOT_DERIVE_FROM_HANDLE_T_OR_A_CONTEXT-HANDLE"></span>поле структуры или объединения не должно быть производным от handle_t или контекстного обработчика</dt> <dd> Дескрипторы контекста не могут передаваться как часть другой структуры. Они должны передаваться как дескрипторы контекста.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2136"></span><span id="midl2136"></span><dl> <dt><strong>MIDL2136</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_derive_from_handle_t_or_a_context_handle"></span><span id="ARRAY_ELEMENT_MUST_NOT_DERIVE_FROM_HANDLE_T_OR_A_CONTEXT_HANDLE"></span>элемент массива не должен быть производным от handle_t или маркера контекста</dt> <dd> Дескрипторы контекста не могут передаваться как часть массива.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2137"></span><span id="midl2137"></span><dl> <dt><strong>MIDL2137</strong></dt> </dl></td>
<td><dl> <dt><span id="this_specification_of_union_needs__c_ext"></span><span id="THIS_SPECIFICATION_OF_UNION_NEEDS__C_EXT"></span>Эта спецификация потребностей объединения/c_ext</dt> <dd> Объединение, которое отображается в определении интерфейса, должно быть связано с discriminant или объявлено локальным. Данные, которые не передаются по сети, могут быть неявно объявлены как локальные при использовании параметра <a href="-c-ext.md"><strong>/c_ext</strong></a> , который является стандартом MIDL. Этот IDL нельзя компилировать с помощью параметра <a href="-osf.md"><strong>/ОСФ</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2138"></span><span id="midl2138"></span><dl> <dt><strong>MIDL2138</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_an__int__must_have_size_specifier__small____short___or__long__with_the__int_"></span><span id="PARAMETER_DERIVING_FROM_AN__INT__MUST_HAVE_SIZE_SPECIFIER__SMALL____SHORT___OR__LONG__WITH_THE__INT_"></span>параметр, производный от &quot; int, &quot; должен иметь спецификатор размера &quot; Small, &quot; &quot; Short &quot; или &quot; Long &quot; с &quot; типом int&quot;</dt> <dd> Тип <a href="int.md"><strong>int</strong></a> является допустимым типом MIDL на 32-разрядных платформах, в 16-разрядных системах <strong>int</strong> должен сопровождаться спецификацией размера. Используйте один из спецификаторов размера: <a href="small.md"><strong>малый</strong></a>, <a href="short.md"><strong>короткий</strong></a>или <a href="long.md"><strong>длинный</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2139"></span><span id="midl2139"></span><dl> <dt><strong>MIDL2139</strong></dt> </dl></td>
<td><dl> <dt><span id="type_of_the_parameter_cannot_derive_from_void_or_void_"></span><span id="TYPE_OF_THE_PARAMETER_CANNOT_DERIVE_FROM_VOID_OR_VOID_"></span>тип параметра не может быть производным от void или void *</dt> <dd> MIDL — строго типизированный язык. Все параметры, передаваемые по сети, должны быть производными от одного из базовых типов MIDL. MIDL не поддерживает <a href="void.md"><strong>void</strong></a> в качестве базового типа. Необходимо изменить объявление на допустимый тип MIDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2140"></span><span id="midl2140"></span><dl> <dt><strong>MIDL2140</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_a_struct_union_containing_bit_fields_is_not_supported"></span><span id="PARAMETER_DERIVING_FROM_A_STRUCT_UNION_CONTAINING_BIT_FIELDS_IS_NOT_SUPPORTED"></span>параметр, производный от структуры или объединения, который содержит битовые поля, не поддерживается</dt> <dd> Битовые поля не определяются как допустимые типы данных с помощью DCE RPC.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2141"></span><span id="midl2141"></span><dl> <dt><strong>MIDL2141</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_a_parameter_deriving_from_a_type_containing_type-modifiers_type-qualifiers_needs__c_ext"></span><span id="USE_OF_A_PARAMETER_DERIVING_FROM_A_TYPE_CONTAINING_TYPE-MODIFIERS_TYPE-QUALIFIERS_NEEDS__C_EXT"></span>Использование параметра, производного от типа, содержащего модификаторы типа или квалификаторы типа, требуется/c_ext</dt> <dd> Использование ключевых слов, таких как « <strong>FAR</strong>», « <strong>NEAR</strong>», « <a href="const.md"><strong>const</strong></a>» и « <strong>volatile</strong> » в IDL-файле, является расширением Майкрософт для DCE RPC. Эти ключевые слова недоступны при компиляции с параметром <a href="-osf.md"><strong>/ОСФ</strong></a> , который отключает параметр расширения по умолчанию <a href="-c-ext.md"><strong>/c_ext</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2142"></span><span id="midl2142"></span><dl> <dt><strong>MIDL2142</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_derive_from_a_pointer_to_a_function"></span><span id="PARAMETER_MUST_NOT_DERIVE_FROM_A_POINTER_TO_A_FUNCTION"></span>параметр не должен быть производным от указателя на функцию</dt> <dd> Библиотеки времени выполнения RPC передают указатель и связанные с ним данные между клиентом и сервером. Указатели на функции не могут передаваться как параметры, так как функция не может передаваться по сети.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2143"></span><span id="midl2143"></span><dl> <dt><strong>MIDL2143</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_derive_from_a_nonrpccapable_union"></span><span id="PARAMETER_MUST_NOT_DERIVE_FROM_A_NONRPCCAPABLE_UNION"></span>параметр не должен наследоваться от объединения с поддержкой нонрпк</dt> <dd> Объединение должно быть связано с discriminant. Используйте атрибуты [<a href="switch-is.md"><strong>switch_is</strong></a>] и [<a href="switch-type.md"><strong>switch_type</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2144"></span><span id="midl2144"></span><dl> <dt><strong>MIDL2144</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_derives_from_an__int.__You_must_use_size_specifiers_with_the__int_"></span><span id="return_type_derives_from_an__int.__you_must_use_size_specifiers_with_the__int_"></span><span id="RETURN_TYPE_DERIVES_FROM_AN__INT.__YOU_MUST_USE_SIZE_SPECIFIERS_WITH_THE__INT_"></span>Тип возвращаемого значения является производным от &quot; int. &quot; Необходимо использовать описатели размера с &quot; типом int&quot;</dt> <dd> В 16-разрядных системах тип <a href="int.md"><strong>int</strong></a> не является допустимым типом MIDL, если он не сопровождается спецификацией размера. Используйте один из спецификаторов размера: <a href="small.md"><strong>малый</strong></a>, <a href="short.md"><strong>короткий</strong></a>или <a href="long.md"><strong>длинный</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2145"></span><span id="midl2145"></span><dl> <dt><strong>MIDL2145</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_void_pointer"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_VOID_POINTER"></span>Тип возвращаемого значения не должен быть производным от указателя void</dt> <dd> MIDL — строго типизированный язык. Все параметры, передаваемые по сети, должны быть производными от одного из базовых типов MIDL. Типы void не определены как часть MIDL. Необходимо изменить объявление на допустимый тип MIDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2146"></span><span id="midl2146"></span><dl> <dt><strong>MIDL2146</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_structure_union_containing_bit-fields"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_STRUCTURE_UNION_CONTAINING_BIT-FIELDS"></span>Тип возвращаемого значения не должен быть производным от структуры или объединения, содержащих битовые поля</dt> <dd> Битовые поля не определяются как допустимые типы данных с помощью DCE RPC.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2147"></span><span id="midl2147"></span><dl> <dt><strong>MIDL2147</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_nonrpccapable_union"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_NONRPCCAPABLE_UNION"></span>Тип возвращаемого значения не должен наследоваться от объединения с поддержкой нонрпк</dt> <dd> Объединение должно быть связано с discriminant. Используйте атрибуты [<a href="switch-is.md"><strong>switch_is</strong></a>] и [<a href="switch-type.md"><strong>switch_type</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2148"></span><span id="midl2148"></span><dl> <dt><strong>MIDL2148</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_pointer_to_a_function"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_POINTER_TO_A_FUNCTION"></span>Тип возвращаемого значения не должен быть производным от указателя на функцию</dt> <dd> Библиотеки времени выполнения RPC передают указатель и связанные с ним данные между клиентом и сервером. Указатели на функции не могут передаваться как параметры, так как RPC не определяет метод для передачи связанной функции по сети.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2149"></span><span id="midl2149"></span><dl> <dt><strong>MIDL2149</strong></dt> </dl></td>
<td><dl> <dt><span id="compound_initializers_are_not_supported"></span><span id="COMPOUND_INITIALIZERS_ARE_NOT_SUPPORTED"></span>составные инициализаторы не поддерживаются</dt> <dd> DCE RPC поддерживает только простую инициализацию. Структура или массив не могут быть инициализированы в IDL-файле.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2150"></span><span id="midl2150"></span><dl> <dt><strong>MIDL2150</strong></dt> </dl></td>
<td><dl> <dt><span id="ACF_attributes_in_the_IDL_file_need_the__app_config_switch"></span><span id="acf_attributes_in_the_idl_file_need_the__app_config_switch"></span><span id="ACF_ATTRIBUTES_IN_THE_IDL_FILE_NEED_THE__APP_CONFIG_SWITCH"></span>Для атрибутов ACF в IDL-файле требуется параметр/app_config</dt> <dd> Расширение Microsoft позволяет указать атрибуты ACF в IDL-файле. Чтобы активировать это расширение, используйте параметр <a href="-app-config.md"><strong>/app_config</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2151"></span><span id="midl2151"></span><dl> <dt><strong>MIDL2151</strong></dt> </dl></td>
<td><dl> <dt><span id="single-line_comment_needs__ms_ext_or__c_ext"></span><span id="SINGLE-LINE_COMMENT_NEEDS__MS_EXT_OR__C_EXT"></span>требуются однострочные комментарии/ms_ext или/c_ext</dt> <dd> Однострочные комментарии, в которых используется два символа косой черты (//), представляют собой расширение Майкрософт для DCE RPC. Нельзя использовать однострочные комментарии при компиляции с параметром <a href="-osf.md"><strong>/ОСФ</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2152"></span><span id="midl2152"></span><dl> <dt><strong>MIDL2152</strong></dt> </dl></td>
<td><dl> <dt><span id="_version__format_is_incorrect"></span><span id="_VERSION__FORMAT_IS_INCORRECT"></span>Недопустимый формат [версия]</dt> <dd> Номер версии интерфейса в заголовке интерфейса должен быть указан в формате <em>основной</em>. <em>дополнительный</em>номер, где каждое число может находиться в диапазоне от 0 до 65535.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2153"></span><span id="midl2153"></span><dl> <dt><strong>MIDL2153</strong></dt> </dl></td>
<td><dl> <dt><span id="_signed__needs__ms_ext_or__c_ext"></span><span id="_SIGNED__NEEDS__MS_EXT_OR__C_EXT"></span>&quot;необходимые подписанные &quot; /ms_ext или/c_ext</dt> <dd> Использование ключевого слова <a href="signed.md"><strong>подписано</strong></a> в качестве расширения Майкрософт для DCE RPC. Вы не можете использовать параметр <a href="-osf.md"><strong>/ОСФ</strong></a> , если хотите использовать эту функцию.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2154"></span><span id="midl2154"></span><dl> <dt><strong>MIDL2154</strong></dt> </dl></td>
<td><dl> <dt><span id="mismatch_in_assignment_type"></span><span id="MISMATCH_IN_ASSIGNMENT_TYPE"></span>несоответствие в типе назначения</dt> <dd> Тип переменной не соответствует типу значения, присвоенного переменной.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2155"></span><span id="midl2155"></span><dl> <dt><strong>MIDL2155</strong></dt> </dl></td>
<td><dl> <dt><span id="declaration_must_be_of_the_form__const__type__declarator_____initializing_expression_"></span><span id="DECLARATION_MUST_BE_OF_THE_FORM__CONST__TYPE__DECLARATOR_____INITIALIZING_EXPRESSION_"></span>объявление должно иметь вид: const <type><declarator> = <initializing expression></dt> <dd> Объявление несовместимо с синтаксисом DCE RPC. Используйте переключатель режима компилятора <a href="-ms-ext.md"><strong>/ms_ext</strong></a> или <a href="-c-ext.md"><strong>/c_ext</strong></a> MIDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2156"></span><span id="midl2156"></span><dl> <dt><strong>MIDL2156</strong></dt> </dl></td>
<td><dl> <dt><span id="declaration_must_have__const_"></span><span id="DECLARATION_MUST_HAVE__CONST_"></span>объявление должно иметь &quot; константу&quot;</dt> <dd> Объявления в IDL-файле должны быть константными выражениями, в которых используется ключевое слово <a href="const.md"><strong>const</strong></a>, например:<br/>
<pre class="syntax" data-space="preserve"><code>const short x = 2;</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2157"></span><span id="midl2157"></span><dl> <dt><strong>MIDL2157</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_enum_must_not_be_defined_in_a_parameter-type_specification"></span><span id="STRUCT_UNION_ENUM_MUST_NOT_BE_DEFINED_IN_A_PARAMETER-TYPE_SPECIFICATION"></span>структура, объединение или перечисление не должны быть определены в спецификации типа параметра</dt> <dd> Тип Structure, Union или Enumerate должен быть явно указан за пределами прототипа функции.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2158"></span><span id="midl2158"></span><dl> <dt><strong>MIDL2158</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__attribute_must_be_applied_only_on_non-void_pointer_types"></span><span id="_ALLOCATE__ATTRIBUTE_MUST_BE_APPLIED_ONLY_ON_NON-VOID_POINTER_TYPES"></span>атрибут [allocate] должен применяться только к типам указателей, не являющихся void</dt> <dd> Атрибут [<a href="allocate.md"><strong>allocate</strong></a>] предназначен для сложных структур данных на основе указателей. Если указан атрибут [allocate], файл заглушки обработает структуру данных, чтобы вычислить общий размер всех объектов, доступных из указателя, и все остальные указатели в структуре данных. Измените тип на тип указателя, отличный от void, или удалите атрибут [<strong>allocate</strong>] и используйте другой метод, чтобы определить размер выделения, например оператор <strong>sizeof</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2159"></span><span id="midl2159"></span><dl> <dt><strong>MIDL2159</strong></dt> </dl></td>
<td><dl> <dt><span id="array_or_equivalent_pointer_construct_cannot_derive_from_a_nonencapsulated_union"></span><span id="ARRAY_OR_EQUIVALENT_POINTER_CONSTRUCT_CANNOT_DERIVE_FROM_A_NONENCAPSULATED_UNION"></span>массив или эквивалентная конструкция указателя не может быть производной от неинкапсулированного объединения</dt> <dd> Каждое объединение должно быть связано с discriminant. Массивы объединений не допускаются, так как они не предоставляют связанные discriminant. Массивы структур, в которых структура упаковывает объединение и его discriminant, разрешены, поскольку суррогаты могут использовать discriminant для определения размера каждого объединения.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2160"></span><span id="midl2160"></span><dl> <dt><strong>MIDL2160</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_an_error_status_t_type"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_AN_ERROR_STATUS_T_TYPE"></span>поле не должно быть производным от типа error_status_t</dt> <dd> Тип <a href="error-status-t.md"><strong>error_status_t</strong></a> можно использовать только в качестве параметра или типа возвращаемого значения. Он не может быть внедрен в поле структуры или объединения.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2161"></span><span id="midl2161"></span><dl> <dt><strong>MIDL2161</strong></dt> </dl></td>
<td><dl> <dt><span id="union_has_at_least_one_arm_without_a_case_label"></span><span id="UNION_HAS_AT_LEAST_ONE_ARM_WITHOUT_A_CASE_LABEL"></span>объединение имеет по крайней мере одну ARM без метки case</dt> <dd> Объявление Union не соответствует требуемому синтаксису MIDL для объединения. Каждому armу Union требуется метка case или метка по умолчанию, выбирающая ARM объединения.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2162"></span><span id="midl2162"></span><dl> <dt><strong>MIDL2162</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_or_return_value_must_not_derive_from_a_type_that_has__ignore__applied_to_it"></span><span id="PARAMETER_OR_RETURN_VALUE_MUST_NOT_DERIVE_FROM_A_TYPE_THAT_HAS__IGNORE__APPLIED_TO_IT"></span>параметр или возвращаемое значение не должны быть производными от типа, к которому применен [Ignore]</dt> <dd> Атрибут [<a href="ignore.md"><strong>Ignore</strong></a>] является атрибутом поля, который может применяться только к полям, таким как поля структур и массивов. Атрибут [<strong>Ignore</strong>] указывает, что заглушка не должна обращаться к указателю во время передачи и не разрешена при конфликте с другими атрибутами, которые должны быть разыменованы, например [<a href="out-idl.md"><strong>out</strong></a>] параметры и возвращаемые значения функции.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2163"></span><span id="midl2163"></span><dl> <dt><strong>MIDL2163</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_already_has_a_pointer_attribute_applied_to_it"></span><span id="POINTER_ALREADY_HAS_A_POINTER_ATTRIBUTE_APPLIED_TO_IT"></span>к указателю уже применен атрибут указателя</dt> <dd> Только один из атрибутов указателя, [<a href="ref.md"><strong>ref</strong></a>], [<a href="unique.md"><strong>UNIQUE</strong></a>] или [<a href="ptr.md"><strong>ptr</strong></a>], может применяться к одному указателю.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2164"></span><span id="midl2164"></span><dl> <dt><strong>MIDL2164</strong></dt> </dl></td>
<td><dl> <dt><span id="field_parameter_must_not_derive_from_a_structure_that_is_recursive_through_a_ref_pointer"></span><span id="FIELD_PARAMETER_MUST_NOT_DERIVE_FROM_A_STRUCTURE_THAT_IS_RECURSIVE_THROUGH_A_REF_POINTER"></span>поле или параметр не должны быть производными от структуры, которая является рекурсивной с помощью ссылочного указателя</dt> <dd> По определению указатель ссылки не может иметь <strong>значение NULL</strong>. Рекурсивная структура данных, определенная с помощью указателя ссылки, не имеет элементов <strong>null</strong> , а соглашение не завершается. Используйте атрибут указателя [<a href="unique.md"><strong>UNIQUE</strong></a>], чтобы разрешить структуре данных указывать элемент <strong>null</strong> , или переопределить структуру данных как нерекурсивную структуру данных.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2165"></span><span id="midl2165"></span><dl> <dt><strong>MIDL2165</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_field_deriving_from_a_void_pointer_needs__c_ext"></span><span id="USE_OF_FIELD_DERIVING_FROM_A_VOID_POINTER_NEEDS__C_EXT"></span>использование поля, производного от void, требуется/c_ext</dt> <dd> Тип <strong>void *</strong> и другие типы и квалификаторы типа, которые не поддерживаются модулем DCE IDL, разрешены в IDL-файле только при использовании параметров компилятора MIDL по умолчанию. Использование параметра <a href="-osf.md"><strong>/ОСФ</strong></a> переопределяет это значение по умолчанию. Если необходимо компилировать в режиме совместимости с использование, необходимо переопределить тип указателя.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2166"></span><span id="midl2166"></span><dl> <dt><strong>MIDL2166</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_this_attribute_needs__ms_ext"></span><span id="USE_OF_THIS_ATTRIBUTE_NEEDS__MS_EXT"></span>Использование этого атрибута требует/ms_ext</dt> <dd> Эта функция языка является расширением Майкрософт для устройства DCE IDL. Эту функцию нельзя использовать при компиляции в режиме совместимости с использование ( <a href="-osf.md"><strong>/ОСФ</strong></a> ).<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2167"></span><span id="midl2167"></span><dl> <dt><strong>MIDL2167</strong></dt> </dl></td>
<td><dl> <dt><span id="this_attribute_only_allowed_with_new_format_type_libraries"></span><span id="THIS_ATTRIBUTE_ONLY_ALLOWED_WITH_NEW_FORMAT_TYPE_LIBRARIES"></span>Этот атрибут разрешен только в новых библиотеках типов форматирования</dt> <dd> чтобы использовать этот атрибут, требуется версия Oleaut32.dll, поставляемая с Windows 2000 или более поздней версии.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2168"></span><span id="midl2168"></span><dl> <dt><strong>MIDL2168</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_wchar_t_needs__ms_ext_or__c_ext"></span><span id="USE_OF_WCHAR_T_NEEDS__MS_EXT_OR__C_EXT"></span>Использование wchar_t потребностей и ms_ext или c_ext</dt> <dd> Тип расширенных символов представляет расширение для устройства DCE IDL. Компилятор MIDL не принимает тип расширенных символов при указании параметра <a href="-osf.md"><strong>/ОСФ</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2169"></span><span id="midl2169"></span><dl> <dt><strong>MIDL2169</strong></dt> </dl></td>
<td><dl> <dt><span id="unnamed_fields_need__ms_ext_or__c_ext"></span><span id="UNNAMED_FIELDS_NEED__MS_EXT_OR__C_EXT"></span>неименованные поля: требуется/ms_ext или/c_ext</dt> <dd> Устройство DCE IDL не поддерживает использование неименованных структур или объединений, внедренных в другие структуры или объединения. В DCE IDL всем таким внедренным полям необходимо присвоить имя. Компилятор MIDL не позволяет использовать его при указании параметра <a href="-osf.md"><strong>/ОСФ</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2170"></span><span id="midl2170"></span><dl> <dt><strong>MIDL2170</strong></dt> </dl></td>
<td><dl> <dt><span id="unnamed_fields_can_derive_only_from_struct_union_types"></span><span id="UNNAMED_FIELDS_CAN_DERIVE_ONLY_FROM_STRUCT_UNION_TYPES"></span>неименованные поля могут быть производными только от типов структуры и объединения</dt> <dd> Расширение Microsoft для устройства DCE IDL, которое поддерживает безымянные поля, применяется только к структурам и объединениям. Необходимо присвоить имя полю или переопределить поле, чтобы оно соответствовало этому ограничению.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2171"></span><span id="midl2171"></span><dl> <dt><strong>MIDL2171</strong></dt> </dl></td>
<td><dl> <dt><span id="field_of_a_union_cannot_derive_from_a_conformant_varying_array_or_its_pointer_equivalent"></span><span id="FIELD_OF_A_UNION_CANNOT_DERIVE_FROM_A_CONFORMANT_VARYING_ARRAY_OR_ITS_POINTER_EQUIVALENT"></span>поле объединения не может быть производным от согласованного или изменяющегося массива или его эквивалента указателя</dt> <dd> Согласованный массив не может использоваться отдельно в объединении, но должен сопровождаться значением, указывающим размер массива. Вместо использования массива в качестве ARM для объединения используйте структуру, состоящую из согласованного массива, и идентификатор, указывающий его размер.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2172"></span><span id="midl2172"></span><dl> <dt><strong>MIDL2172</strong></dt> </dl></td>
<td><dl> <dt><span id="no__pointer_default__attribute_specified__assuming__ptr__for_all_unattributed_pointers_in_interface"></span><span id="NO__POINTER_DEFAULT__ATTRIBUTE_SPECIFIED__ASSUMING__PTR__FOR_ALL_UNATTRIBUTED_POINTERS_IN_INTERFACE"></span>не указан атрибут [pointer_default], предполагается [PTR] для всех неатрибутных указателей в интерфейсе</dt> <dd> Реализация устройства DCE определяет, что все указатели в каждом IDL-файле должны быть связаны с атрибутами указателя. Если явный атрибут указателя не назначается параметру или типу указателя, а атрибут [<a href="pointer-default.md"><strong>pointer_default</strong></a>] не указан в IDL-файле, то с указателем связывается атрибут указателя <a href="ptr.md"><strong>ptr</strong></a> . Атрибуты указателя можно изменить с помощью явных атрибутов указателя, указав атрибут [<strong>pointer_default</strong>] или указав параметр <a href="-ms-ext.md"><strong>/ms_ext</strong></a> , чтобы изменить значение по умолчанию для указателей без атрибутов на [<a href="unique.md"><strong>UNIQUE</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2173"></span><span id="midl2173"></span><dl> <dt><strong>MIDL2173</strong></dt> </dl></td>
<td><dl> <dt><span id="initializing_expression_must_resolve_to_a_constant_expression"></span><span id="INITIALIZING_EXPRESSION_MUST_RESOLVE_TO_A_CONSTANT_EXPRESSION"></span>Инициализация выражения должна разрешаться в константное выражение</dt> <dd> Если выражение используется в качестве инициализатора, выражение должно быть константным выражением. Это справедливо во всех режимах компилятора MIDL. Выражение должно быть разрешимым во время компиляции. Укажите литеральную константу или выражение, которое разрешается в константу, а не в переменную.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2174"></span><span id="midl2174"></span><dl> <dt><strong>MIDL2174</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_must_be_of_type_integer__char__Boolean_or_enum"></span><span id="attribute_expression_must_be_of_type_integer__char__boolean_or_enum"></span><span id="ATTRIBUTE_EXPRESSION_MUST_BE_OF_TYPE_INTEGER__CHAR__BOOLEAN_OR_ENUM"></span>выражение атрибута должно иметь тип Integer, char, Boolean или enum</dt> <dd> Указанный тип не разрешается в допустимый тип переключателя. Используйте целочисленный, символьный, <a href="byte.md"><strong>байтовый</strong></a>, <a href="boolean.md"><strong>логический</strong></a>тип или тип <a href="enum.md"><strong>перечисления</strong></a> , производный от одного из этих типов.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2175"></span><span id="midl2175"></span><dl> <dt><strong>MIDL2175</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_constant"></span><span id="ILLEGAL_CONSTANT"></span>Недопустимая константа</dt> <dd> Указанная константа находится за пределами допустимого диапазона для указанного типа.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2176"></span><span id="midl2176"></span><dl> <dt><strong>MIDL2176</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_not_implemented__ignored"></span><span id="ATTRIBUTE_NOT_IMPLEMENTED__IGNORED"></span>атрибут не реализован; игнорируют</dt> <dd> Указанный атрибут не реализован в этом выпуске Microsoft RPC. Компилятор MIDL продолжит обработку IDL-файла, как если бы атрибут не присутствовал.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2177"></span><span id="midl2177"></span><dl> <dt><strong>MIDL2177</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a__ref__pointer"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A__REF__POINTER"></span>Тип возвращаемого значения не должен быть производным от указателя [ref]</dt> <dd> Возвращаемые функцией значения, определенные как типы указателей, должны быть указаны в виде [<a href="unique.md"><strong>UNIQUE</strong></a>] или <a href="ptr.md"><strong>полных</strong></a> указателей. Нельзя использовать указатели ссылок.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2178"></span><span id="midl2178"></span><dl> <dt><strong>MIDL2178</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_must_be_a_variable_name_or_a_pointer_dereference_expression_in_this_mode._You_must_specify_the__ms_ext_switch"></span><span id="attribute_expression_must_be_a_variable_name_or_a_pointer_dereference_expression_in_this_mode._you_must_specify_the__ms_ext_switch"></span><span id="ATTRIBUTE_EXPRESSION_MUST_BE_A_VARIABLE_NAME_OR_A_POINTER_DEREFERENCE_EXPRESSION_IN_THIS_MODE._YOU_MUST_SPECIFY_THE__MS_EXT_SWITCH"></span>выражение атрибута должно быть именем переменной или выражением разыменования указателя в этом режиме. Необходимо указать параметр/ms_ext</dt> <dd> Компилятору DCE IDL требуется, чтобы размер, связанный с атрибутом [<a href="size-is.md"><strong>size_is</strong></a>], был задан переменной или переменной-указателем. Если вы хотите воспользоваться преимуществом расширения Microsoft, которое позволяет определить атрибут [<strong>size_is</strong>] в константном выражении, нельзя использовать параметр компилятора <a href="-osf.md"><strong>/ОСФ</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2179"></span><span id="midl2179"></span><dl> <dt><strong>MIDL2179</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_derive_from_a_recursive_nonencapsulated_union"></span><span id="PARAMETER_MUST_NOT_DERIVE_FROM_A_RECURSIVE_NONENCAPSULATED_UNION"></span>параметр не должен быть производным от рекурсивного неинкапсулированного объединения</dt> <dd> Объединение должно включать discriminant, поэтому объединение не может иметь еще одно объединение в качестве элемента. Объединение может быть внедрено в другое объединение только в том случае, если оно является частью структуры, содержащей discriminant.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2180"></span><span id="midl2180"></span><dl> <dt><strong>MIDL2180</strong></dt> </dl></td>
<td><dl> <dt><span id="binding-handle_parameter_cannot_be__out__only"></span><span id="BINDING-HANDLE_PARAMETER_CANNOT_BE__OUT__ONLY"></span>Параметр обработчика привязки не может быть только [out]</dt> <dd> Параметр Handle, определяемый компилятором MIDL в качестве маркера привязки для этой операции, должен быть параметром [<a href="in.md"><strong>in</strong></a>]. [<a href="out-idl.md"><strong>out</strong></a>] — в клиентской заглушке не определены параметры, а на клиенте должен быть определен маркер привязки.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2181"></span><span id="midl2181"></span><dl> <dt><strong>MIDL2181</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_to_a_handle_cannot_be__unique__or__ptr_"></span><span id="POINTER_TO_A_HANDLE_CANNOT_BE__UNIQUE__OR__PTR_"></span>Указатель на маркер не может быть [unique] или [PTR]</dt> <dd> Нельзя использовать атрибуты UNIQUE и Full указателя для указателя на маркер. Эти атрибуты допускают значение <strong>null</strong>, а маркер привязки не может иметь значение <strong>null</strong>. Используйте атрибут [<a href="ref.md"><strong>ref</strong></a>], чтобы получить параметр Binding-Handle из ссылочных указателей.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2182"></span><span id="midl2182"></span><dl> <dt><strong>MIDL2182</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_that_is_not_a_binding_handle_must_not_derive_from_handle_t"></span><span id="PARAMETER_THAT_IS_NOT_A_BINDING_HANDLE_MUST_NOT_DERIVE_FROM_HANDLE_T"></span>параметр, который не является маркером привязки, не должен быть производным от handle_t</dt> <dd> Тип <a href="handle-t.md"><strong>handle_t</strong></a> -примитива не является допустимым типом данных, передаваемым по сети. Измените тип параметра на тип, отличный от <strong>handle_t</strong>, или удалите параметр.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2183"></span><span id="midl2183"></span><dl> <dt><strong>MIDL2183</strong></dt> </dl></td>
<td><dl> <dt><span id="unexpected_end_of_file_found"></span><span id="UNEXPECTED_END_OF_FILE_FOUND"></span>обнаружен непредвиденный конец файла</dt> <dd> Компилятор MIDL обнаружил конец файла, прежде чем он сможет успешно разрешить все синтаксические элементы файла. Убедитесь, что в конце файла находится завершающий правый символ скобки (}), или проверьте синтаксис.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2184"></span><span id="midl2184"></span><dl> <dt><strong>MIDL2184</strong></dt> </dl></td>
<td><dl> <dt><span id="type_deriving_from_handle_t_must_not_have__transmit_as__applied_to_it"></span><span id="TYPE_DERIVING_FROM_HANDLE_T_MUST_NOT_HAVE__TRANSMIT_AS__APPLIED_TO_IT"></span>тип, производный от handle_t, не должен иметь [transmit_as], примененный к нему</dt> <dd> Тип маркера-примитива <a href="handle-t.md"><strong>handle_t</strong></a> не передается по сети.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2185"></span><span id="midl2185"></span><dl> <dt><strong>MIDL2185</strong></dt> </dl></td>
<td><dl> <dt><span id="_context_handle__must_not_be_applied_to_a_type_that_has__handle__applied_to_it"></span><span id="_CONTEXT_HANDLE__MUST_NOT_BE_APPLIED_TO_A_TYPE_THAT_HAS__HANDLE__APPLIED_TO_IT"></span>[context_handle] не должен применяться к типу, к которому применен [Handle]</dt> <dd> Атрибуты [<a href="context-handle.md"><strong>context_handle</strong></a>] и [<a href="handle.md"><strong>Handle</strong></a>] не могут применяться к одному и тому же типу.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2186"></span><span id="midl2186"></span><dl> <dt><strong>MIDL2186</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_specified_on_a_type_deriving_from_void_or_void__"></span><span id="_HANDLE__MUST_NOT_BE_SPECIFIED_ON_A_TYPE_DERIVING_FROM_VOID_OR_VOID__"></span>[Handle] не может быть указан для типа, производного от void или void *</dt> <dd> Тип, указанный с помощью атрибута [<a href="handle.md"><strong>Handle</strong></a>], может передаваться по сети, но тип <strong>void *</strong> не является типом трансмиссибле. Тип обработчика должен разрешаться в тип, производный от базовых типов трансмиссибле.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2187"></span><span id="midl2187"></span><dl> <dt><strong>MIDL2187</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_have_either__in____out__or__in_out__in_this_mode._You_must_specify__ms_ext_or__c_ext"></span><span id="parameter_must_have_either__in____out__or__in_out__in_this_mode._you_must_specify__ms_ext_or__c_ext"></span><span id="PARAMETER_MUST_HAVE_EITHER__IN____OUT__OR__IN_OUT__IN_THIS_MODE._YOU_MUST_SPECIFY__MS_EXT_OR__C_EXT"></span>в этом режиме параметр должен иметь значение [в], [out] или [in, out]. Необходимо указать/ms_ext или/c_ext</dt> <dd> Компилятору DCE IDL требуется, чтобы все параметры имели явные параметры направления. Чтобы использовать расширения Майкрософт для устройства DCE IDL, нельзя использовать параметр <a href="-osf.md"><strong>/ОСФ</strong></a> , который переопределяет <a href="-ms-ext.md"><strong>/ms_ext</strong></a> и <a href="-c-ext.md"><strong>/c_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2188"></span><span id="midl2188"></span><dl> <dt><strong>MIDL2188</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_type_may_not_derive_from__void__for__transmit_as____represent_as____wire_marshal____user_marshal_"></span><span id="TRANSMITTED_TYPE_MAY_NOT_DERIVE_FROM__VOID__FOR__TRANSMIT_AS____REPRESENT_AS____WIRE_MARSHAL____USER_MARSHAL_"></span>передаваемый тип не может быть производным от &quot; void &quot; для [transmit_as], [represent_as], [wire_marshal], [user_marshal]</dt> <dd> Атрибут [<a href="transmit-as.md"><strong>transmit_as</strong></a>] применяется только к типам указателей. Используйте тип <strong>void *</strong> вместо <a href="void.md"><strong>void</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2189"></span><span id="midl2189"></span><dl> <dt><strong>MIDL2189</strong></dt> </dl></td>
<td><dl> <dt><span id="_void__must_be_specified_on_the_first_and_only_parameter_specification"></span><span id="_VOID__MUST_BE_SPECIFIED_ON_THE_FIRST_AND_ONLY_PARAMETER_SPECIFICATION"></span>&quot;значение void &quot; должно быть указано только для первой и только спецификации параметра</dt> <dd> Ключевое слово <a href="void.md"><strong>void</strong></a> неверно отображается с другими параметрами функции. Чтобы указать функцию без параметров, ключевое слово <strong>void</strong> должно быть единственным элементом списка параметров, как показано в следующем примере:<br/>
<pre class="syntax" data-space="preserve"><code>void Moo(void)</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2190"></span><span id="midl2190"></span><dl> <dt><strong>MIDL2190</strong></dt> </dl></td>
<td><dl> <dt><span id="_switch_is__must_be_specified_only_on_a_type_deriving_from_a_nonencapsulated_union"></span><span id="_SWITCH_IS__MUST_BE_SPECIFIED_ONLY_ON_A_TYPE_DERIVING_FROM_A_NONENCAPSULATED_UNION"></span>[switch_is] должен быть указан только для типа, производного от неинкапсулированного объединения</dt> <dd> Ключевое слово [<a href="switch-is.md"><strong>switch_is</strong></a>] неправильно применено. Его можно использовать только с <a href="nonencapsulated-unions.md">неинкапсулированными типами объединения</a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2191"></span><span id="midl2191"></span><dl> <dt><strong>MIDL2191</strong></dt> </dl></td>
<td><dl> <dt><span id="stringable_structures_are_not_implemented_in_this_version"></span><span id="STRINGABLE_STRUCTURES_ARE_NOT_IMPLEMENTED_IN_THIS_VERSION"></span>в этой версии не реализованы строковые структуры</dt> <dd> Устройство DCE IDL позволяет применять атрибут [<a href="string.md"><strong>String</strong></a>] к структуре, элементы которой состоят только из символов, байтов или типов, которые разрешаются в символы или байты. Эта функция не поддерживается в Microsoft RPC. Атрибут [<strong>String</strong>] не может быть применен к структуре в целом. Однако его можно применить к каждому отдельному массиву.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2192"></span><span id="midl2192"></span><dl> <dt><strong>MIDL2192</strong></dt> </dl></td>
<td><dl> <dt><span id="switch_type_can_only_be_integral__char__Boolean_or_enum"></span><span id="switch_type_can_only_be_integral__char__boolean_or_enum"></span><span id="SWITCH_TYPE_CAN_ONLY_BE_INTEGRAL__CHAR__BOOLEAN_OR_ENUM"></span>Тип переключателя может быть только целочисленным, char, Boolean или enum</dt> <dd> Указанный тип не разрешается в допустимый тип переключателя. Используйте целочисленный, символьный, <a href="byte.md"><strong>байтовый</strong></a>, <a href="boolean.md"><strong>логический</strong></a>тип <a href="enum.md"><strong>enum</strong></a> или тип, производный от одного из этих типов.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2193"></span><span id="midl2193"></span><dl> <dt><strong>MIDL2193</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_specified_on_a_type_deriving_from_handle_t"></span><span id="_HANDLE__MUST_NOT_BE_SPECIFIED_ON_A_TYPE_DERIVING_FROM_HANDLE_T"></span>[Handle] не может быть указан для типа, производного от handle_t</dt> <dd> Тип маркера должен быть определен с помощью одного и только одного из типов или атрибутов обработчика. Используйте тип-примитив <a href="handle-t.md"><strong>handle_t</strong></a> или атрибут [<a href="handle.md"><strong>Handle</strong></a>], но не оба. Определяемый пользователем тип обработчика должен быть трансмиссибле, но тип <strong>handle_t</strong> не передается в сети.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2194"></span><span id="midl2194"></span><dl> <dt><strong>MIDL2194</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_handle_t_must_not_be_an__out__parameter"></span><span id="PARAMETER_DERIVING_FROM_HANDLE_T_MUST_NOT_BE_AN__OUT__PARAMETER"></span>параметр, производный от handle_t, не должен быть параметром [out]</dt> <dd> Маркер типа-примитива <a href="handle-t.md"><strong>handle_t</strong></a> имеет смысл только на стороне приложения, в котором оно определено. Тип <strong>handle_t</strong> не передается в сети.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2195"></span><span id="midl2195"></span><dl> <dt><strong>MIDL2195</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_derives_from__unique__or__ptr__pointer_dereference"></span><span id="ATTRIBUTE_EXPRESSION_DERIVES_FROM__UNIQUE__OR__PTR__POINTER_DEREFERENCE"></span>выражение атрибута является производным от разыменования указателя [unique] или [PTR]</dt> <dd> Хотя атрибуты [<a href="unique.md"><strong>UNIQUE</strong></a>] и <a href="ptr.md"><strong>полные</strong></a> указатели позволяют указателям иметь значения <strong>null</strong> , выражение, определяющее размер или атрибут длины, не должно иметь значения <strong>null</strong> . При использовании указателей MIDL ограничивает выражения до указателей [<a href="ref.md"><strong>ref</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2196"></span><span id="midl2196"></span><dl> <dt><strong>MIDL2196</strong></dt> </dl></td>
<td><dl> <dt><span id="_cpp_quote__requires__ms_ext"></span><span id="_CPP_QUOTE__REQUIRES__MS_EXT"></span>&quot;cpp_quote &quot; требуется/ms_ext</dt> <dd> Атрибут <a href="cpp-quote.md"><strong>cpp_quote</strong></a> — это расширение Майкрософт для устройства DCE IDL. Не используйте параметр компилятора MIDL <a href="-osf.md"><strong>/ОСФ</strong></a>, который переопределяет <a href="-ms-ext.md"><strong>/ms_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2197"></span><span id="midl2197"></span><dl> <dt><strong>MIDL2197</strong></dt> </dl></td>
<td><dl> <dt><span id="quoted_uuid_requires__ms_ext"></span><span id="QUOTED_UUID_REQUIRES__MS_EXT"></span>для UUID требуется/ms_ext</dt> <dd> Возможность указания значения UUID в кавычках является расширением Майкрософт для устройства DCE IDL. Не используйте параметр компилятора MIDL <a href="-osf.md"><strong>/ОСФ</strong></a>, который переопределяет <a href="-ms-ext.md"><strong>/ms_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2198"></span><span id="midl2198"></span><dl> <dt><strong>MIDL2198</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_cannot_derive_from_a_nonencapsulated_union"></span><span id="RETURN_TYPE_CANNOT_DERIVE_FROM_A_NONENCAPSULATED_UNION"></span>Тип возвращаемого значения не может быть производным от неинкапсулированного объединения</dt> <dd> Неинкапсулированное объединение не может использоваться в качестве возвращаемого типа функции. Чтобы получить тип объединения, укажите тип объединения в качестве параметра [<a href="out-idl.md"><strong>out</strong></a>] или [<strong>in, out</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2199"></span><span id="midl2199"></span><dl> <dt><strong>MIDL2199</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_cannot_derive_from_a_conformant_structure"></span><span id="RETURN_TYPE_CANNOT_DERIVE_FROM_A_CONFORMANT_STRUCTURE"></span>Тип возвращаемого значения не может быть производным от согласованной структуры</dt> <dd> Размер возвращаемого типа должен быть константой. Нельзя указать в качестве типа возвращаемого значения структуру, содержащую соответствующий массив, даже если структура также включает описатель размера. Чтобы получить согласованную структуру, укажите структуру в качестве параметра [<a href="out-idl.md"><strong>out</strong></a>] или [<strong>in, out</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2200"></span><span id="midl2200"></span><dl> <dt><strong>MIDL2200</strong></dt> </dl></td>
<td><dl> <dt><span id="_transmit_as__must_not_be_applied_to_a_type_deriving_from_a_generic_handle"></span><span id="_TRANSMIT_AS__MUST_NOT_BE_APPLIED_TO_A_TYPE_DERIVING_FROM_A_GENERIC_HANDLE"></span>[transmit_as] не должен применяться к типу, производному от универсального маркера</dt> <dd> В этом выпуске атрибуты [<a href="handle.md"><strong>Handle</strong></a>] и [<a href="transmit-as.md"><strong>transmit_as</strong></a>] не могут быть объединены в одном типе.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2201"></span><span id="midl2201"></span><dl> <dt><strong>MIDL2201</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_applied_to_a_type_that_has__transmit_as__applied_to_it"></span><span id="_HANDLE__MUST_NOT_BE_APPLIED_TO_A_TYPE_THAT_HAS__TRANSMIT_AS__APPLIED_TO_IT"></span>[Handle] не должен применяться к типу, к которому применен [transmit_as]</dt> <dd> В этом выпуске атрибуты [<a href="handle.md"><strong>Handle</strong></a>] и [<a href="transmit-as.md"><strong>transmit_as</strong></a>] не могут быть объединены в одном типе.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2202"></span><span id="midl2202"></span><dl> <dt><strong>MIDL2202</strong></dt> </dl></td>
<td><dl> <dt><span id="type_specified_for_the_const_declaration_is_invalid"></span><span id="TYPE_SPECIFIED_FOR_THE_CONST_DECLARATION_IS_INVALID"></span>для объявления const указан недопустимый тип</dt> <dd> Объявления констант ограничены целыми числами, символами, расширенными символами, строковыми и логическими типами.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2203"></span><span id="midl2203"></span><dl> <dt><strong>MIDL2203</strong></dt> </dl></td>
<td><dl> <dt><span id="operand_to_the_sizeof_operator_is_not_supported"></span><span id="OPERAND_TO_THE_SIZEOF_OPERATOR_IS_NOT_SUPPORTED"></span>операнд оператора sizeof не поддерживается</dt> <dd> Компилятор MIDL поддерживает операцию <strong>sizeof</strong> только для простых типов. Указанный операнд не возвращает целочисленный тип.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2204"></span><span id="midl2204"></span><dl> <dt><strong>MIDL2204</strong></dt> </dl></td>
<td><dl> <dt><span id="this_name_already_used_as_a_const_identifier_name"></span><span id="THIS_NAME_ALREADY_USED_AS_A_CONST_IDENTIFIER_NAME"></span>Это имя уже используется как имя константного идентификатора</dt> <dd> Идентификатор ранее использовался для идентификации константы в объявлении <a href="const.md"><strong>const</strong></a> . Измените имя одного из идентификаторов так, чтобы идентификаторы были уникальными.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2205"></span><span id="midl2205"></span><dl> <dt><strong>MIDL2205</strong></dt> </dl></td>
<td><dl> <dt><span id="inconsistent_redefinition_of_type_error_status_t"></span><span id="INCONSISTENT_REDEFINITION_OF_TYPE_ERROR_STATUS_T"></span>непротиворечивое переопределение типа error_status_t</dt> <dd> Тип <a href="error-status-t.md"><strong>error_status_t</strong></a> должен разрешаться в тип <strong>без знака Long</strong>. Другие определения типов использовать нельзя.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2206"></span><span id="midl2206"></span><dl> <dt><strong>MIDL2206</strong></dt> </dl></td>
<td><dl> <dt><span id="_case__value_out_of_range_of_switch_type"></span><span id="_CASE__VALUE_OUT_OF_RANGE_OF_SWITCH_TYPE"></span>[Case] значение из диапазона типа коммутатора</dt> <dd> Значение, связанное с вариантом оператора switch, выходит за пределы допустимого диапазона для указанного типа переключателя. Например, эта ошибка возникает, когда в операторе Case используется длинное целочисленное значение для коротких целочисленных типов.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2207"></span><span id="midl2207"></span><dl> <dt><strong>MIDL2207</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_wchar_t_needs__ms_ext"></span><span id="PARAMETER_DERIVING_FROM_WCHAR_T_NEEDS__MS_EXT"></span>параметр, производный от wchar_t требуется/ms_ext</dt> <dd> Тип расширенных символов <a href="wchar-t.md"><strong>wchar_t</strong></a> — это расширение Майкрософт для устройства DCE IDL. Не используйте параметр компилятора MIDL <a href="-osf.md"><strong>/ОСФ</strong></a>, который переопределяет <a href="-ms-ext.md"><strong>/ms_ext</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2208"></span><span id="midl2208"></span><dl> <dt><strong>MIDL2208</strong></dt> </dl></td>
<td><dl> <dt><span id="this_interface_has_only_callbacks"></span><span id="THIS_INTERFACE_HAS_ONLY_CALLBACKS"></span>Этот интерфейс имеет только обратные вызовы</dt> <dd> Обратные вызовы допустимы только в контексте удаленного вызова процедуры. Интерфейс должен включать по крайней мере один прототип функции для удаленного вызова процедуры, который не включает атрибут [<a href="callback.md"><strong>callback</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2209"></span><span id="midl2209"></span><dl> <dt><strong>MIDL2209</strong></dt> </dl></td>
<td><dl> <dt><span id="redundantly_specified_attribute__ignored"></span><span id="REDUNDANTLY_SPECIFIED_ATTRIBUTE__IGNORED"></span>избыточно указанный атрибут; игнорируют</dt> <dd> Указанный атрибут был применен несколько раз. Несколько экземпляров одного и того же атрибута не учитываются.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2210"></span><span id="midl2210"></span><dl> <dt><strong>MIDL2210</strong></dt> </dl></td>
<td><dl> <dt><span id="context_handle_type_used_for_an_implicit_handle"></span><span id="CONTEXT_HANDLE_TYPE_USED_FOR_AN_IMPLICIT_HANDLE"></span>Тип обработчика контекста, используемый для неявного обработчика</dt> <dd> Тип, определенный с помощью атрибута [<a href="context-handle.md"><strong>context_handle</strong></a>], был указан как тип обработчика в атрибуте [ <a href="implicit-handle.md"><strong>implicit_handle</strong></a>]. Атрибуты не могут быть объединены таким образом.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2211"></span><span id="midl2211"></span><dl> <dt><strong>MIDL2211</strong></dt> </dl></td>
<td><dl> <dt><span id="conflicting_options_specified_for__allocate_"></span><span id="CONFLICTING_OPTIONS_SPECIFIED_FOR__ALLOCATE_"></span>для [выделения] заданы конфликтующие параметры</dt> <dd> Параметры, заданные для атрибута ACF [<a href="allocate.md"><strong>allocate</strong></a>], представляют конфликтующие директивы. Например, можно указать либо параметр all_nodes, либо параметр single_node, но не оба одновременно.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2212"></span><span id="midl2212"></span><dl> <dt><strong>MIDL2212</strong></dt> </dl></td>
<td><dl> <dt><span id="error_while_writing_to_file"></span><span id="ERROR_WHILE_WRITING_TO_FILE"></span>Ошибка при записи в файл</dt> <dd> Произошла ошибка при записи в файл. Это состояние может быть вызвано ошибками, связанными с дисковым пространством, дескрипторами файлов, ограничениями доступа к файлам и сбоями оборудования.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2213"></span><span id="midl2213"></span><dl> <dt><strong>MIDL2213</strong></dt> </dl></td>
<td><dl> <dt><span id="no_switch_type_found_at_definition_of_union__using_the__switch_is__type"></span><span id="NO_SWITCH_TYPE_FOUND_AT_DEFINITION_OF_UNION__USING_THE__SWITCH_IS__TYPE"></span>не удалось найти тип переключателя в определении объединения, используется тип [switch_is].</dt> <dd> Определение Union не включает явный атрибут [<a href="switch-type.md"><strong>switch_type</strong></a>]. Тип переменной, заданной атрибутом [<a href="switch-is.md"><strong>switch_is</strong></a>], используется в качестве типа переключателя.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2214"></span><span id="midl2214"></span><dl> <dt><strong>MIDL2214</strong></dt> </dl></td>
<td><dl> <dt><span id="semantic_check_incomplete_due_to_previous_errors"></span><span id="SEMANTIC_CHECK_INCOMPLETE_DUE_TO_PREVIOUS_ERRORS"></span>семантическая проверка не завершена из-за предыдущих ошибок</dt> <dd> Компилятор MIDL выполняет два прохода по входным файлам для разрешения всех прямых объявлений. Из-за ошибок, возникших во время первого прохода, проверка второго прохода не выполнялась. Неотчеты об ошибках, связанных с прямыми объявлениями, по-прежнему могут присутствовать в файле.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2215"></span><span id="midl2215"></span><dl> <dt><strong>MIDL2215</strong></dt> </dl></td>
<td><dl> <dt><span id="handle_parameter_or_return_type_is_not_supported_on_a__callback__procedure"></span><span id="HANDLE_PARAMETER_OR_RETURN_TYPE_IS_NOT_SUPPORTED_ON_A__CALLBACK__PROCEDURE"></span>параметр обработки или возвращаемый тип не поддерживается в процедуре [callback]</dt> <dd> Процедура [<a href="callback.md"><strong>callback</strong></a>] возникает в контексте вызова от клиента к серверу и использует тот же маркер привязки, что и исходный вызов. В функциях обратного вызова не допускаются явные параметры или возвращаемые типы обработчика привязки.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2216"></span><span id="midl2216"></span><dl> <dt><strong>MIDL2216</strong></dt> </dl></td>
<td><dl> <dt><span id="_ptr__does_not_support_aliasing_in_this_version"></span><span id="_PTR__DOES_NOT_SUPPORT_ALIASING_IN_THIS_VERSION"></span>[PTR] не поддерживает псевдонимы в этой версии</dt> <dd> Псевдоним возникает, когда доступ к данным осуществляется через более одного указателя или имени переменной. Удалите псевдоним. Дополнительные сведения см. в разделе <a href="/windows/desktop/Rpc/unique-pointers">уникальные указатели</a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2217"></span><span id="midl2217"></span><dl> <dt><strong>MIDL2217</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_already_defined_as_a_context_handle"></span><span id="PARAMETER_ALREADY_DEFINED_AS_A_CONTEXT_HANDLE"></span>параметр уже определен как контекстный обработчик</dt> <dd> Параметр был ранее определен как обработчик контекста.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2218"></span><span id="midl2218"></span><dl> <dt><strong>MIDL2218</strong></dt> </dl></td>
<td><dl> <dt><span id="_context_handle__must_not_derive_from_handle_t"></span><span id="_CONTEXT_HANDLE__MUST_NOT_DERIVE_FROM_HANDLE_T"></span>[context_handle] не должен быть производным от handle_t</dt> <dd> Три характеристики обработчика: тип <a href="handle-t.md"><strong>handle_t</strong></a>, атрибут [<a href="handle.md"><strong>Handle</strong></a>] и атрибут [<a href="context-handle.md"><strong>context_handle</strong></a>] являются взаимоисключающими. В каждый момент времени можно применить только одну характеристику типа или параметра.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2219"></span><span id="midl2219"></span><dl> <dt><strong>MIDL2219</strong></dt> </dl></td>
<td><dl> <dt><span id="array_size_exceeds_65536_bytes"></span><span id="ARRAY_SIZE_EXCEEDS_65536_BYTES"></span>Размер массива превышает 65536 байт</dt> <dd> На некоторых платформах Майкрософт максимальный размер данных трансмиссибле составляет 64 КБ. Перепроектирование приложения таким образом, чтобы все передаваемые данные помещались в пределах максимального размера трансмиссибле.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2220"></span><span id="midl2220"></span><dl> <dt><strong>MIDL2220</strong></dt> </dl></td>
<td><dl> <dt><span id="structure_size_exceeds_65536_bytes"></span><span id="STRUCTURE_SIZE_EXCEEDS_65536_BYTES"></span>Размер структуры превышает 65536 байт</dt> <dd> На некоторых платформах Майкрософт максимальный размер данных трансмиссибле составляет 64 КБ. Перепроектирование приложения таким образом, чтобы все передаваемые данные помещались в пределах максимального размера трансмиссибле.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2221"></span><span id="midl2221"></span><dl> <dt><strong>MIDL2221</strong></dt> </dl></td>
<td><dl> <dt><span id="field_of_a_nonencapsulated_union_cannot_be_another_nonencapsulated_union"></span><span id="FIELD_OF_A_NONENCAPSULATED_UNION_CANNOT_BE_ANOTHER_NONENCAPSULATED_UNION"></span>поле неинкапсулированного объединения не может быть другим неинкапсулированным объединением</dt> <dd> Для объединений, передаваемых в рамках удаленного вызова процедуры, требуется связанный элемент данных, discriminant, который выбирает ARM объединения. Объединения, вложенные в другие объединения, не предлагают discriminant. в результате они не могут передаваться в этой форме. Создайте структуру, состоящую из объединения и ее discriminant.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2222"></span><span id="midl2222"></span><dl> <dt><strong>MIDL2222</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_attribute_s__applied_on_an_embedded_array__ignored"></span><span id="POINTER_ATTRIBUTE_S__APPLIED_ON_AN_EMBEDDED_ARRAY__IGNORED"></span>атрибуты указателя применены к внедренному массиву; игнорируют</dt> <dd> Атрибут указателя может применяться к массиву только в том случае, если массив является параметром верхнего уровня. Другие атрибуты указателя, применяемые к массивам, внедренным в другие структуры данных, игнорируются.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2223"></span><span id="midl2223"></span><dl> <dt><strong>MIDL2223</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__is_illegal_on_either_the_transmitted_or_presented_type_for__transmit_as____represent_as____wire_marshal___or__user_marshal_"></span><span id="_ALLOCATE__IS_ILLEGAL_ON_EITHER_THE_TRANSMITTED_OR_PRESENTED_TYPE_FOR__TRANSMIT_AS____REPRESENT_AS____WIRE_MARSHAL___OR__USER_MARSHAL_"></span>[allocate] недопустимо для передаваемого или представленного типа для [transmit_as], [represent_as], [wire_marshal] или [user_marshal]</dt> <dd> Атрибуты [<a href="transmit-as.md"><strong>transmit_as</strong></a>] и [<a href="allocate.md"><strong>allocate</strong></a>] не могут быть применены к одному и тому же типу. Атрибут [<strong>transmit_as</strong>] различает представленные и передаваемые типы, а атрибут [<strong>allocate</strong>] предполагает, что представляемый тип совпадает с передаваемым типом.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2224"></span><span id="midl2224"></span><dl> <dt><strong>MIDL2224</strong></dt> </dl></td>
<td>в этом режиме импорта необходимо указать [switch_type]<br/></td>
</tr>
<tr class="even">
<td><span id="MIDL2225"></span><span id="midl2225"></span><dl> <dt><strong>MIDL2225</strong></dt> </dl></td>
<td><dl> <dt><span id="_implicit_handle__type_undefined__assuming_generic_handle"></span><span id="_IMPLICIT_HANDLE__TYPE_UNDEFINED__ASSUMING_GENERIC_HANDLE"></span>[implicit_handle] тип не определен; предположение универсального маркера</dt> <dd> Тип обработчика, указанный в ACF, не определен в IDL-файле. Компилятор MIDL предполагает, что тип Handle разрешается в тип маркера-примитива <a href="handle-t.md"><strong>handle_t</strong></a>. Добавьте атрибут [<a href="handle.md"><strong>Handle</strong></a>] в определение типа, если необходимо, чтобы этот обработчик работал как пользовательский или универсальный.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2226"></span><span id="midl2226"></span><dl> <dt><strong>MIDL2226</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_derive_from_error_status_t"></span><span id="ARRAY_ELEMENT_MUST_NOT_DERIVE_FROM_ERROR_STATUS_T"></span>элемент массива не должен быть производным от error_status_t</dt> <dd> В этом выпуске Microsoft RPC тип <a href="error-status-t.md"><strong>error_status_t</strong></a> может использоваться только в качестве параметра или типа возвращаемого значения. Он не может присутствовать в массивах.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2227"></span><span id="midl2227"></span><dl> <dt><strong>MIDL2227</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__illegal_on_a_type_deriving_from_a_primitive_generic_context_handle"></span><span id="_ALLOCATE__ILLEGAL_ON_A_TYPE_DERIVING_FROM_A_PRIMITIVE_GENERIC_CONTEXT_HANDLE"></span>[allocate] недопустимо для типа, производного от примитивного, универсального или контекстного маркера</dt> <dd> По проекту атрибут ACF [<a href="allocate.md"><strong>allocate</strong></a>] не может применяться к типам обработчиков.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2228"></span><span id="midl2228"></span><dl> <dt><strong>MIDL2228</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_or_presented_type_must_not_derive_from_error_status_t"></span><span id="TRANSMITTED_OR_PRESENTED_TYPE_MUST_NOT_DERIVE_FROM_ERROR_STATUS_T"></span>передаваемый или представленный тип не должен быть производным от error_status_t</dt> <dd> В этом выпуске Microsoft RPC тип <a href="error-status-t.md"><strong>error_status_t</strong></a> нельзя использовать с атрибутом [<a href="transmit-as.md"><strong>transmit_as</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2229"></span><span id="midl2229"></span><dl> <dt><strong>MIDL2229</strong></dt> </dl></td>
<td><dl> <dt><span id="discriminant_of_a_union_must_not_derive_from_a_field_with__ignore__applied_to_it"></span><span id="DISCRIMINANT_OF_A_UNION_MUST_NOT_DERIVE_FROM_A_FIELD_WITH__IGNORE__APPLIED_TO_IT"></span>discriminant объединения не должно быть производным от поля с примененным к нему [Ignore]</dt> <dd> Объединение, используемое при удаленном вызове процедуры, должно быть связано с другим элементом данных, который называется discriminant, который выбирает ARM объединения. Необходимо передать discriminant. Атрибут [<a href="ignore.md"><strong>Ignore</strong></a>] не может быть применен к объединению discriminant.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2230"></span><span id="midl2230"></span><dl> <dt><strong>MIDL2230</strong></dt> </dl></td>
<td><dl> <dt><span id="_nocode__ignored_for_server_side_since___server_none__not_specified"></span><span id="_NOCODE__IGNORED_FOR_SERVER_SIDE_SINCE___SERVER_NONE__NOT_SPECIFIED"></span>[No] игнорируется на стороне сервера, так как &quot; не указано значение "/Server" &quot;</dt> <dd> Некоторые компиляторы, поддерживающие устройства DCE, вызывают ошибку, если<a href="nocode.md"><strong>атрибут [InAttribute</strong></a>] применяется к процедуре в интерфейсе, для которого создаются файлы заглушки сервера. Так как сервер должен поддерживать все операции, [без<strong>кода</strong>] не должен применяться к процедуре в этом режиме или необходимо использовать параметр компилятора MIDL " <a href="-server.md"><strong>/Server</strong></a> нет", чтобы явно указать, что никакие серверные процедуры создаваться не будут.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2231"></span><span id="midl2231"></span><dl> <dt><strong>MIDL2231</strong></dt> </dl></td>
<td><dl> <dt><span id="no_remote_procedures_specified_in_non-_local__interface__no_client_server_stubs_will_be_generated"></span><span id="NO_REMOTE_PROCEDURES_SPECIFIED_IN_NON-_LOCAL__INTERFACE__NO_CLIENT_SERVER_STUBS_WILL_BE_GENERATED"></span>Удаленные процедуры не указаны в интерфейсе, отличном от [local]; заглушки клиента/сервера создаваться не будут</dt> <dd> Указанный интерфейс не содержит удаленных процедур, поэтому будут созданы только файлы заголовков.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2232"></span><span id="midl2232"></span><dl> <dt><strong>MIDL2232</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_default_cases_specified_for_encapsulated_union"></span><span id="TOO_MANY_DEFAULT_CASES_SPECIFIED_FOR_ENCAPSULATED_UNION"></span>для инкапсулированного объединения указано слишком много вариантов по умолчанию</dt> <dd> Инкапсулированное объединение может иметь только одно значение по умолчанию: ARM.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2233"></span><span id="midl2233"></span><dl> <dt><strong>MIDL2233</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_default_interfaces_specified_for_coclass"></span><span id="TOO_MANY_DEFAULT_INTERFACES_SPECIFIED_FOR_COCLASS"></span>для coclass задано слишком много интерфейсов по умолчанию</dt> <dd> <a href="coclass.md"><strong>Компонентный класс</strong></a> может иметь не более двух элементов [<a href="default.md"><strong>Default</strong></a>], один для представления исходящего (исходного) интерфейса или disp-интерфейса, а другой — для представления входящего (приемника) или disp-интерфейсов.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2234"></span><span id="midl2234"></span><dl> <dt><strong>MIDL2234</strong></dt> </dl></td>
<td><dl> <dt><span id="items_with__defaultvtable__must_also_have__source_"></span><span id="ITEMS_WITH__DEFAULTVTABLE__MUST_ALSO_HAVE__SOURCE_"></span>элементы с [defaultvtable] также должны иметь [source]</dt> <dd> Интерфейс <a href="defaultvtable.md"><strong>defaultvtable</strong></a> создает второй исходный интерфейс для объекта, который позволяет приемникам принимать события через таблицу V-Table.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2235"></span><span id="midl2235"></span><dl> <dt><strong>MIDL2235</strong></dt> </dl></td>
<td><dl> <dt><span id="union_specification_with_no_fields_is_illegal"></span><span id="UNION_SPECIFICATION_WITH_NO_FIELDS_IS_ILLEGAL"></span>Недопустимая спецификация объединения без полей</dt> <dd> В объединениях должно быть по крайней мере одно поле.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2236"></span><span id="midl2236"></span><dl> <dt><strong>MIDL2236</strong></dt> </dl></td>
<td><dl> <dt><span id="value_out_of_range"></span><span id="VALUE_OUT_OF_RANGE"></span>значение вне допустимого диапазона</dt> <dd> Указанное значение варианта выходит за пределы диапазона типа переключателя.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2237"></span><span id="midl2237"></span><dl> <dt><strong>MIDL2237</strong></dt> </dl></td>
<td><dl> <dt><span id="_context_handle__must_be_applied_on_a_pointer_type"></span><span id="_CONTEXT_HANDLE__MUST_BE_APPLIED_ON_A_POINTER_TYPE"></span>[context_handle] должен применяться к типу указателя</dt> <dd> Дескрипторы контекста всегда должны быть типами указателей. DCE указывает, что все дескрипторы контекста должны иметь тип <strong>void *</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2238"></span><span id="midl2238"></span><dl> <dt><strong>MIDL2238</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_handle_t"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_HANDLE_T"></span>Тип возвращаемого значения не должен быть производным от handle_t</dt> <dd>не удается вернуть <a href="handle-t.md"><strong>handle_t</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2239"></span><span id="midl2239"></span><dl> <dt><strong>MIDL2239</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_applied_to_a_type_deriving_from_a_context_handle"></span><span id="_HANDLE__MUST_NOT_BE_APPLIED_TO_A_TYPE_DERIVING_FROM_A_CONTEXT_HANDLE"></span>[Handle] не должен применяться к типу, производному от обработчика контекста</dt> <dd> Тип не может одновременно быть как обработчиком контекста, так и универсальным маркером.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2240"></span><span id="midl2240"></span><dl> <dt><strong>MIDL2240</strong></dt> </dl></td>
<td><dl> <dt><span id="field_deriving_from_an__int__must_have_size_specifier__small____short___or__long__with_the__int_"></span><span id="FIELD_DERIVING_FROM_AN__INT__MUST_HAVE_SIZE_SPECIFIER__SMALL____SHORT___OR__LONG__WITH_THE__INT_"></span>поле, производное от &quot; int &quot; , должно иметь спецификатор размера &quot; &quot; "маленький &quot; ", &quot; "короткий" или &quot; длинный &quot; с &quot; типом int&quot;</dt> <dd> Тип <a href="int.md"><strong>int</strong></a> не трансмиссибле в 16-разрядных системах, так как размер <strong>int</strong> может различаться на разных компьютерах.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2241"></span><span id="midl2241"></span><dl> <dt><strong>MIDL2241</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_void_or_void__"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_VOID_OR_VOID__"></span>поле не должно быть производным от void или void *</dt> <dd> <strong>void</strong> и <strong>void *</strong> нельзя использовать в качестве типов параметров для удаленных процедур.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2242"></span><span id="midl2242"></span><dl> <dt><strong>MIDL2242</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_structure_containing_bit-fields"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_STRUCTURE_CONTAINING_BIT-FIELDS"></span>поле не должно быть производным от структуры, содержащей битовые поля</dt> <dd> Структуры, содержащие битовые поля, не могут использоваться в качестве параметров или возвращаемых типов для удаленных процедур.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2243"></span><span id="midl2243"></span><dl> <dt><strong>MIDL2243</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_non-rpcable_union"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_NON-RPCABLE_UNION"></span>поле не должно быть производным от рпкабле объединения</dt> <dd> Для передачи необходимо указать объединение как неинкапсулированное или инкапсулированное объединение. В обычных объединениях C отсутствует discriminant, необходимый для передачи объединения по сети.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2244"></span><span id="midl2244"></span><dl> <dt><strong>MIDL2244</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_pointer_to_a_function"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_POINTER_TO_A_FUNCTION"></span>поле не должно быть производным от указателя на функцию</dt> <dd> Указатели на функции не могут быть переданы удаленным процедурам. Указатели на функции указывают на код функции, и код функции не может быть передан по сети с помощью RPC.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2245"></span><span id="midl2245"></span><dl> <dt><strong>MIDL2245</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_use__fault_status__on_both_a_parameter_and_a_return_type"></span><span id="CANNOT_USE__FAULT_STATUS__ON_BOTH_A_PARAMETER_AND_A_RETURN_TYPE"></span>нельзя использовать [fault_status] как для параметра, так и для типа возвращаемого значения</dt> <dd> Атрибут [<a href="fault-status.md"><strong>fault_status</strong></a>] может использоваться только один раз для каждой процедуры. Атрибут [<a href="comm-status.md"><strong>comm_status</strong></a>] можно использовать независимо.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2246"></span><span id="midl2246"></span><dl> <dt><strong>MIDL2246</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_too_complicated_for__Oi_modes__using__Os"></span><span id="return_type_too_complicated_for__oi_modes__using__os"></span><span id="RETURN_TYPE_TOO_COMPLICATED_FOR__OI_MODES__USING__OS"></span>слишком сложный тип возвращаемого значения для режимов/OI с помощью/OS</dt> <dd> Типы больших возвращаемых значений, передаваемые по значению, могут обрабатываться только суррогатами оптимизации <a href="-os.md"><strong>/OS</strong></a> . Заглушки для этой подпрограммы будут созданы с помощью функции оптимизации " <strong>/OS</strong> ".<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2247"></span><span id="midl2247"></span><dl> <dt><strong>MIDL2247</strong></dt> </dl></td>
<td><dl> <dt><span id="generic_handle_type_too_large_for__Oi_modes__using__Os"></span><span id="generic_handle_type_too_large_for__oi_modes__using__os"></span><span id="GENERIC_HANDLE_TYPE_TOO_LARGE_FOR__OI_MODES__USING__OS"></span>тип универсального обработчика слишком велик для режимов/OI с использованием/OS</dt> <dd> Большие универсальные типы обработки, передаваемые по значению, могут обрабатываться только суррогатами оптимизации <a href="-os.md"><strong>/OS</strong></a> . Заглушки для этой подпрограммы будут созданы с помощью функции оптимизации " <strong>/OS</strong> ".<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2248"></span><span id="midl2248"></span><dl> <dt><strong>MIDL2248</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate_all_nodes___on_an__in_out__parameter_may_orphan_the_original_memory"></span><span id="_ALLOCATE_ALL_NODES___ON_AN__IN_OUT__PARAMETER_MAY_ORPHAN_THE_ORIGINAL_MEMORY"></span>[allocate (all_nodes)] в параметре [in, out] может привести к потере исходной памяти</dt> <dd> Использование [<a href="allocate.md"><strong>allocate</strong></a>(all_nodes)] для параметра [<a href="in.md"><strong>in</strong></a>, <a href="out-idl.md"><strong>out</strong></a>] должно привести к перераспределению непрерывной памяти для направления [<strong>out</strong>], тем самым сооставляя параметр [<strong>in</strong>]. Это использование не рекомендуется.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2249"></span><span id="midl2249"></span><dl> <dt><strong>MIDL2249</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_have_a__ref__pointer_as_a_union_arm"></span><span id="CANNOT_HAVE_A__REF__POINTER_AS_A_UNION_ARM"></span>нельзя использовать указатель [ref] в качестве ARM объединения</dt> <dd> Ссылочные указатели должны всегда указывать на допустимую память, но объединение [<a href="in.md"><strong>in</strong></a>, <a href="out-idl.md"><strong>out</strong></a>] с указателем ссылки может возвращать указатель ссылки, когда в направлении [<strong>in</strong>] использовался другой тип.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2250"></span><span id="midl2250"></span><dl> <dt><strong>MIDL2250</strong></dt> </dl></td>
<td><dl> <dt><span id="return_of_context_handles_not_supported_for__Oi_modes__using__Os"></span><span id="return_of_context_handles_not_supported_for__oi_modes__using__os"></span><span id="RETURN_OF_CONTEXT_HANDLES_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>Возврат дескрипторов контекста, не поддерживаемых для режимов/Oi, с использованием/OS</dt> <dd> MIDL не поддерживает дескрипторы контекста в полностью интерпретируемых режимах оптимизации. Переключение на смешанный режим оптимизации.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2251"></span><span id="midl2251"></span><dl> <dt><strong>MIDL2251</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_the_extra__comm_status__or__fault_status__parameter_not_supported_for__Oi_modes__using__Os"></span><span id="use_of_the_extra__comm_status__or__fault_status__parameter_not_supported_for__oi_modes__using__os"></span><span id="USE_OF_THE_EXTRA__COMM_STATUS__OR__FAULT_STATUS__PARAMETER_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>использование дополнительного параметра [comm_status] или [fault_status] не поддерживается для режимов/OI с помощью/OS</dt> <dd> Атрибуты [<a href="comm-status.md"><strong>comm_status</strong></a>] и [<a href="fault-status.md"><strong>fault_status</strong></a>] могут обрабатываться только суррогатами оптимизации <a href="-os.md"><strong>/OS</strong></a> . Заглушки для этой подпрограммы будут созданы с помощью функции оптимизации " <strong>/OS</strong> ".<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2252"></span><span id="midl2252"></span><dl> <dt><strong>MIDL2252</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_an_unknown_type_for__represent_as__or__user_marshal__not_supported_for__Oi_modes__using__Os"></span><span id="use_of_an_unknown_type_for__represent_as__or__user_marshal__not_supported_for__oi_modes__using__os"></span><span id="USE_OF_AN_UNKNOWN_TYPE_FOR__REPRESENT_AS__OR__USER_MARSHAL__NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>Использование неизвестного типа для [represent_as] или [user_marshal] не поддерживается для режимов/OI с помощью/OS</dt> <dd> Использование атрибута [<a href="represent-as.md"><strong>represent_as</strong></a>] с локальным типом, который не ОПРЕДЕЛЕН в IDL-файле, или ИМПОРТИРОВАНного IDL-файла может обрабатывать только суррогаты оптимизации <a href="-os.md"><strong>/OS</strong></a> . Заглушки для этой подпрограммы будут созданы с помощью функции оптимизации " <strong>/OS</strong> ".<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2253"></span><span id="midl2253"></span><dl> <dt><strong>MIDL2253</strong></dt> </dl></td>
<td><dl> <dt><span id="array_types_with__transmit_as__or__represent_as__not_supported_on_return_type_for__Oi_modes___using__Os"></span><span id="array_types_with__transmit_as__or__represent_as__not_supported_on_return_type_for__oi_modes___using__os"></span><span id="ARRAY_TYPES_WITH__TRANSMIT_AS__OR__REPRESENT_AS__NOT_SUPPORTED_ON_RETURN_TYPE_FOR__OI_MODES___USING__OS"></span>типы массивов с [transmit_as] или [represent_as] не поддерживаются в возвращаемом типе для режимов/OI с помощью/OS</dt> <dd> Возврат массива с применением [<a href="transmit-as.md"><strong>transmit_as</strong></a>] или [<a href="represent-as.md"><strong>represent_as</strong></a>] может осуществляться только суррогатами оптимизации <a href="-os.md"><strong>/OS</strong></a> . Заглушки для этой подпрограммы будут созданы с помощью функции оптимизации " <strong>/OS</strong> ".<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2254"></span><span id="midl2254"></span><dl> <dt><strong>MIDL2254</strong></dt> </dl></td>
<td><dl> <dt><span id="array_types_with__transmit_as__or__represent_as__not_supported_pass-by-value_for__Oi_modes__using__Os"></span><span id="array_types_with__transmit_as__or__represent_as__not_supported_pass-by-value_for__oi_modes__using__os"></span><span id="ARRAY_TYPES_WITH__TRANSMIT_AS__OR__REPRESENT_AS__NOT_SUPPORTED_PASS-BY-VALUE_FOR__OI_MODES__USING__OS"></span>типы массивов с [transmit_as] или [represent_as] не поддерживаются при передаче по значению для режимов/OI с помощью/OS</dt> <dd> Это действие не поддерживается для полностью интерпретируемой оптимизации. Переключение на смешанный режим оптимизации.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2255"></span><span id="midl2255"></span><dl> <dt><strong>MIDL2255</strong></dt> </dl></td>
<td><dl> <dt><span id="_callback__requires__ms_ext"></span><span id="_CALLBACK__REQUIRES__MS_EXT"></span>[callback] требуется/ms_ext</dt> <dd> Атрибут [<a href="callback.md"><strong>callback</strong></a>] является расширением Microsoft и требует включения параметра <a href="-ms-ext.md"><strong>/ms_ext</strong></a> . Не компилируйте с помощью <a href="-osf.md"><strong>/ОСФ</strong></a>, который переопределяет <strong>/ms_ext</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2256"></span><span id="midl2256"></span><dl> <dt><strong>MIDL2256</strong></dt> </dl></td>
<td><dl> <dt><span id="circular_interface_dependency"></span><span id="CIRCULAR_INTERFACE_DEPENDENCY"></span>зависимость циклического интерфейса</dt> <dd> Этот интерфейс в качестве базового интерфейса использует сам себя (прямо или косвенно).<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2257"></span><span id="midl2257"></span><dl> <dt><strong>MIDL2257</strong></dt> </dl></td>
<td><dl> <dt><span id="only_IUnknown_may_be_used_as_the_root_interface"></span><span id="only_iunknown_may_be_used_as_the_root_interface"></span><span id="ONLY_IUNKNOWN_MAY_BE_USED_AS_THE_ROOT_INTERFACE"></span>в качестве корневого интерфейса можно использовать только IUnknown</dt> <dd> Сейчас все интерфейсы должны иметь интерфейс <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> в качестве корневого интерфейса.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2258"></span><span id="midl2258"></span><dl> <dt><strong>MIDL2258</strong></dt> </dl></td>
<td><dl> <dt><span id="_IID_IS__may_only_be_applied_to_pointers_to_interfaces"></span><span id="_iid_is__may_only_be_applied_to_pointers_to_interfaces"></span><span id="_IID_IS__MAY_ONLY_BE_APPLIED_TO_POINTERS_TO_INTERFACES"></span>[IID_IS] можно применять только к указателям на интерфейсы</dt> <dd> Атрибут [<a href="iid-is.md"><strong>iid_is</strong></a>] может применяться только к указателям на интерфейсы, хотя они могут быть указаны как указатели на <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> *.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2259"></span><span id="midl2259"></span><dl> <dt><strong>MIDL2259</strong></dt> </dl></td>
<td><dl> <dt><span id="interfaces_may_only_be_used_in_pointer-to-interface_constructs"></span><span id="INTERFACES_MAY_ONLY_BE_USED_IN_POINTER-TO-INTERFACE_CONSTRUCTS"></span>интерфейсы можно использовать только в конструкциях указателя на интерфейс</dt> <dd> Имена интерфейсов нельзя использовать, за исключением базовых интерфейсов или указателей интерфейса.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2260"></span><span id="midl2260"></span><dl> <dt><strong>MIDL2260</strong></dt> </dl></td>
<td><dl> <dt><span id="interface_pointers_must_have_a_UUID_IID"></span><span id="interface_pointers_must_have_a_uuid_iid"></span><span id="INTERFACE_POINTERS_MUST_HAVE_A_UUID_IID"></span>указатели интерфейса должны иметь UUID или IID</dt> <dd> Базовый тип выражения [<a href="iid-is.md"><strong>iid_is</strong></a>] должен быть типом UUID/GUID/IID.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2261"></span><span id="midl2261"></span><dl> <dt><strong>MIDL2261</strong></dt> </dl></td>
<td><dl> <dt><span id="definitions_and_declarations_outside_of_interface_body_requires__ms_ext"></span><span id="DEFINITIONS_AND_DECLARATIONS_OUTSIDE_OF_INTERFACE_BODY_REQUIRES__MS_EXT"></span>определения и объявления за пределами тела интерфейса требуют/ms_ext</dt> <dd> Размещение объявлений и определений за пределами тела интерфейса является расширением Microsoft и требует использования параметра <a href="-ms-ext.md"><strong>/ms_ext</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2262"></span><span id="midl2262"></span><dl> <dt><strong>MIDL2262</strong></dt> </dl></td>
<td><dl> <dt><span id="multiple_interfaces_in_one_file_requires__ms_ext"></span><span id="MULTIPLE_INTERFACES_IN_ONE_FILE_REQUIRES__MS_EXT"></span>для нескольких интерфейсов в одном файле требуется/ms_ext</dt> <dd> Использование нескольких интерфейсов в одном IDL-файле является расширением Майкрософт и недоступно при компиляции в режиме <a href="-osf.md"><strong>/ОСФ</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2263"></span><span id="midl2263"></span><dl> <dt><strong>MIDL2263</strong></dt> </dl></td>
<td><dl> <dt><span id="only_one_of__implicit_handle____auto_handle___or__explicit_handle__allowed"></span><span id="ONLY_ONE_OF__IMPLICIT_HANDLE____AUTO_HANDLE___OR__EXPLICIT_HANDLE__ALLOWED"></span>допускается только один из [implicit_handle], [auto_handle] или [explicit_handle]</dt> <dd> Каждый интерфейс может иметь только один из этих трех атрибутов.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2264"></span><span id="midl2264"></span><dl> <dt><strong>MIDL2264</strong></dt> </dl></td>
<td><dl> <dt><span id="_implicit_handle__references_a_type_which_is_not_a_handle"></span><span id="_IMPLICIT_HANDLE__REFERENCES_A_TYPE_WHICH_IS_NOT_A_HANDLE"></span>[implicit_handle] ссылается на тип, который не является маркером</dt> <dd> Неявные дескрипторы должны иметь один из типов дескрипторов.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2265"></span><span id="midl2265"></span><dl> <dt><strong>MIDL2265</strong></dt> </dl></td>
<td><dl> <dt><span id="_object__procs_may_only_be_used_with___env_win32_"></span><span id="_OBJECT__PROCS_MAY_ONLY_BE_USED_WITH___ENV_WIN32_"></span>процедуры [Object] могут использоваться только с &quot; /env Win32&quot;</dt> <dd> Интерфейсы с атрибутом [<a href="object.md"><strong>Object</strong></a>] не могут использоваться с 16-разрядными средами.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2266"></span><span id="midl2266"></span><dl> <dt><strong>MIDL2266</strong></dt> </dl></td>
<td><dl> <dt><span id="_callback__with_-env_dos_win16_not_supported_for__Oi__using__Os"></span><span id="_callback__with_-env_dos_win16_not_supported_for__oi__using__os"></span><span id="_CALLBACK__WITH_-ENV_DOS_WIN16_NOT_SUPPORTED_FOR__OI__USING__OS"></span>[callback] с-env DOS/Win16 не поддерживается для/OI с использованием/OS</dt> <dd> Обратные вызовы в 16-разрядных средах могут обрабатываться только суррогатами оптимизации <a href="-os.md"><strong>/OS</strong></a> . Заглушки для этой подпрограммы будут созданы с помощью функции оптимизации " <strong>/OS</strong> ".<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2267"></span><span id="midl2267"></span><dl> <dt><strong>MIDL2267</strong></dt> </dl></td>
<td><dl> <dt><span id="float_double_not_supported_as_top-level_parameter_for__Oi_mode__using__Os"></span><span id="float_double_not_supported_as_top-level_parameter_for__oi_mode__using__os"></span><span id="FLOAT_DOUBLE_NOT_SUPPORTED_AS_TOP-LEVEL_PARAMETER_FOR__OI_MODE__USING__OS"></span>float/Double не поддерживается в качестве параметра верхнего уровня для режима/OI с помощью/OS</dt> <dd> Типы float и Double могут обрабатываться только как параметры суррогатов оптимизации <a href="-os.md"><strong>/OS</strong></a> . Заглушки для этой подпрограммы будут созданы с помощью функции оптимизации " <strong>/OS</strong> ". Типы float и Double в структурах, массивах или объединениях по-прежнему могут обрабатываться с помощью<strong>/OS</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2268"></span><span id="midl2268"></span><dl> <dt><strong>MIDL2268</strong></dt> </dl></td>
<td><dl> <dt><span id="pointers_to_context_handles_may_not_be_used_as_return_values"></span><span id="POINTERS_TO_CONTEXT_HANDLES_MAY_NOT_BE_USED_AS_RETURN_VALUES"></span>указатели на дескрипторы контекста не могут использоваться в качестве возвращаемых значений</dt> <dd> Дескрипторы контекста должны использоваться в качестве прямых возвращаемых значений, а не косвенных возвращаемых значений.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2269"></span><span id="midl2269"></span><dl> <dt><strong>MIDL2269</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_in_an_object_interface_must_return_an_HRESULT"></span><span id="procedures_in_an_object_interface_must_return_an_hresult"></span><span id="PROCEDURES_IN_AN_OBJECT_INTERFACE_MUST_RETURN_AN_HRESULT"></span>процедуры в интерфейсе объектов должны возвращать значение HRESULT</dt> <dd> Все процедуры в объектном интерфейсе, не имеющие атрибута-[<a href="local.md"><strong>Local</strong></a>], должны возвращать <strong>значение HRESULT</strong> / <strong>SCODE</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2270"></span><span id="midl2270"></span><dl> <dt><strong>MIDL2270</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicate_UUID"></span><span id="duplicate_uuid"></span><span id="DUPLICATE_UUID"></span>дублирование UUID</dt> <dd> То же, что и UUID, должны быть уникальными.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2271"></span><span id="midl2271"></span><dl> <dt><strong>MIDL2271</strong></dt> </dl></td>
<td><dl> <dt><span id="_object__interfaces_must_derive_from_another__object__interface_such_as_IUnknown"></span><span id="_object__interfaces_must_derive_from_another__object__interface_such_as_iunknown"></span><span id="_OBJECT__INTERFACES_MUST_DERIVE_FROM_ANOTHER__OBJECT__INTERFACE_SUCH_AS_IUNKNOWN"></span>интерфейсы [Object] должны быть производными от другого интерфейса [Object], такого как IUnknown.</dt> <dd> Наследование интерфейса разрешено только при использовании интерфейсов объектов.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2272"></span><span id="midl2272"></span><dl> <dt><strong>MIDL2272</strong></dt> </dl></td>
<td><dl> <dt><span id="_async__interface_must_derive_from_another__async__interface"></span><span id="_ASYNC__INTERFACE_MUST_DERIVE_FROM_ANOTHER__ASYNC__INTERFACE"></span>(Async) интерфейс должен быть производным от другого (Async) интерфейса</dt> <dd> Интерфейсы объектов, как синхронные, так и асинхронные, должны быть производными от <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> или другого базового интерфейса OLE.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2273"></span><span id="midl2273"></span><dl> <dt><strong>MIDL2273</strong></dt> </dl></td>
<td><dl> <dt><span id="_IID_IS__expression_must_be_a_pointer_to_IID_structure"></span><span id="_iid_is__expression_must_be_a_pointer_to_iid_structure"></span><span id="_IID_IS__EXPRESSION_MUST_BE_A_POINTER_TO_IID_STRUCTURE"></span>Выражение [IID_IS] должно быть указателем на структуру IID</dt> <dd> Базовый тип выражения [<a href="iid-is.md"><strong>iid_is</strong></a>] должен быть типом UUID/GUID/IID.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2274"></span><span id="midl2274"></span><dl> <dt><strong>MIDL2274</strong></dt> </dl></td>
<td><dl> <dt><span id="_call_as__type_must_be_a__local__procedure"></span><span id="_CALL_AS__TYPE_MUST_BE_A__LOCAL__PROCEDURE"></span>[call_as] тип должен быть процедурой [local]</dt> <dd> Целевой объект типа [<a href="call-as.md"><strong>call_as</strong></a>], если он определен, должен иметь атрибут [ <a href="local.md"><strong>Local</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2275"></span><span id="midl2275"></span><dl> <dt><strong>MIDL2275</strong></dt> </dl></td>
<td><dl> <dt><span id="undefined__call_as__must_not_be_used_in_an_object_interface"></span><span id="UNDEFINED__CALL_AS__MUST_NOT_BE_USED_IN_AN_OBJECT_INTERFACE"></span>неопределенные [call_as] не должны использоваться в интерфейсе объектов</dt> <dd> Необходимо определить целевой объект типа [<a href="call-as.md"><strong>call_as</strong></a>]. Убедитесь, что предоставлены <strong>call_as</strong> подпрограммы для вызывающего и вызываемого приложений.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2276"></span><span id="midl2276"></span><dl> <dt><strong>MIDL2276</strong></dt> </dl></td>
<td><dl> <dt><span id="_auto_handle__may_not_be_used_with__encode__or__decode_"></span><span id="_AUTO_HANDLE__MAY_NOT_BE_USED_WITH__ENCODE__OR__DECODE_"></span>[auto_handle] нельзя использовать с [Encoded] или [расшифровывает]</dt> <dd> Атрибуты [ <a href="encode.md"><strong>Encoded</strong></a>] и [ <a href="decode.md"><strong>дешифровки</strong></a>] можно использовать только с явными дескрипторами или неявными дескрипторами.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2277"></span><span id="midl2277"></span><dl> <dt><strong>MIDL2277</strong></dt> </dl></td>
<td><dl> <dt><span id="normal_procedures_are_not_allowed_in_an_interface_with__encode__or__decode_"></span><span id="NORMAL_PROCEDURES_ARE_NOT_ALLOWED_IN_AN_INTERFACE_WITH__ENCODE__OR__DECODE_"></span>обычные процедуры не допускаются в интерфейсе с [Encoded] или [расшифровывает]</dt> <dd> Интерфейсы, содержащие процедуры [<a href="encode.md"><strong>Encoded</strong></a>] или [<a href="decode.md"><strong>дешифровки</strong></a>], также не могут иметь удаленных процедур.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2278"></span><span id="midl2278"></span><dl> <dt><strong>MIDL2278</strong></dt> </dl></td>
<td><dl> <dt><span id="top-level_conformance_or_variance_not_allowed_with__encode__or__decode_"></span><span id="TOP-LEVEL_CONFORMANCE_OR_VARIANCE_NOT_ALLOWED_WITH__ENCODE__OR__DECODE_"></span>соответствие или дисперсия верхнего уровня не разрешены в [Encoded] или [декодировании]</dt> <dd> Типы с соответствием верхнего уровня или вариативность не могут использовать сериализацию типа, так как не существует способа предоставить размер и увеличение. Однако структуры, содержащие их, могут использовать сериализацию типов.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2279"></span><span id="midl2279"></span><dl> <dt><strong>MIDL2279</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__parameters_may_not_have__const_"></span><span id="_OUT__PARAMETERS_MAY_NOT_HAVE__CONST_"></span>параметры [out] не могут иметь &quot; const&quot;</dt> <dd> Поскольку параметр [<a href="out-idl.md"><strong>out</strong></a>] изменяется, он не должен объявляться как константа SA.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2280"></span><span id="midl2280"></span><dl> <dt><strong>MIDL2280</strong></dt> </dl></td>
<td><dl> <dt><span id="return_values_may_not_have__const_"></span><span id="RETURN_VALUES_MAY_NOT_HAVE__CONST_"></span>возвращаемые значения не могут иметь &quot; константы&quot;</dt> <dd> Поскольку значение функции задается при возврате функции, это значение не должно объявляться как константа.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2281"></span><span id="midl2281"></span><dl> <dt><strong>MIDL2281</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_use_of__retval__attribute"></span><span id="INVALID_USE_OF__RETVAL__ATTRIBUTE"></span>Недопустимое использование &quot; &quot; атрибута retval</dt> <dd> Убедитесь, что вы не использовали атрибут [<a href="optional.md"><strong>Optional</strong></a>] и что параметр [<a href="retval.md"><strong>retval</strong></a>] является последним параметром в списке.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2282"></span><span id="midl2282"></span><dl> <dt><strong>MIDL2282</strong></dt> </dl></td>
<td><dl> <dt><span id="multiple_calling_conventions_illegal"></span><span id="MULTIPLE_CALLING_CONVENTIONS_ILLEGAL"></span>Недопустимое несколько соглашений о вызовах</dt> <dd> К одной процедуре можно применить только одно соглашение о вызовах.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2283"></span><span id="midl2283"></span><dl> <dt><strong>MIDL2283</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_illegal_on__object__procedure"></span><span id="ATTRIBUTE_ILLEGAL_ON__OBJECT__PROCEDURE"></span>Недопустимый атрибут для процедуры [Object]</dt> <dd> Указанный выше атрибут применяется только к процедурам в интерфейсах, у которых нет атрибута [<a href="object.md"><strong>Object</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2284"></span><span id="midl2284"></span><dl> <dt><strong>MIDL2284</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__interface_pointers_must_use_double_indirection"></span><span id="_OUT__INTERFACE_POINTERS_MUST_USE_DOUBLE_INDIRECTION"></span>[out] указатели интерфейса должны использовать двойное косвенное обращение</dt> <dd> Так как измененное значение является указателем на интерфейс, должен существовать другой уровень косвенного обращения над указателем, чтобы разрешить его возврат.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2285"></span><span id="midl2285"></span><dl> <dt><strong>MIDL2285</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_used_twice_as_the_caller_in__call_as_"></span><span id="PROCEDURE_USED_TWICE_AS_THE_CALLER_IN__CALL_AS_"></span>процедура используется дважды в качестве вызывающего объекта в [call_as]</dt> <dd> Данную процедуру [<a href="local.md"><strong>Local</strong></a>] можно использовать только один раз в качестве целевого объекта [<a href="call-as.md"><strong>call_as</strong></a>], чтобы избежать конфликта имен.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2286"></span><span id="midl2286"></span><dl> <dt><strong>MIDL2286</strong></dt> </dl></td>
<td><dl> <dt><span id="_call_as__target_must_have__local__in_an_object_interface"></span><span id="_CALL_AS__TARGET_MUST_HAVE__LOCAL__IN_AN_OBJECT_INTERFACE"></span>Целевой объект [call_as] должен иметь [local] в интерфейсе объектов</dt> <dd> Целью [<a href="call-as.md"><strong>call_as</strong></a>] должна быть определенная процедура [<a href="local.md"><strong>Local</strong></a>] в текущем интерфейсе.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2287"></span><span id="midl2287"></span><dl> <dt><strong>MIDL2287</strong></dt> </dl></td>
<td><dl> <dt><span id="_code__and__nocode__may_not_be_used_together"></span><span id="_CODE__AND__NOCODE__MAY_NOT_BE_USED_TOGETHER"></span>[code] и [No] нельзя использовать вместе</dt> <dd> Эти два атрибута являются противоречивыми и не могут использоваться вместе.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2288"></span><span id="midl2288"></span><dl> <dt><strong>MIDL2288</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with__maybe__or__message__attributes_may_not_have__out__params__or_return_values_must_be_of_type_HRESULT_or_error_status_t"></span><span id="procedures_with__maybe__or__message__attributes_may_not_have__out__params__or_return_values_must_be_of_type_hresult_or_error_status_t"></span><span id="PROCEDURES_WITH__MAYBE__OR__MESSAGE__ATTRIBUTES_MAY_NOT_HAVE__OUT__PARAMS__OR_RETURN_VALUES_MUST_BE_OF_TYPE_HRESULT_OR_ERROR_STATUS_T"></span>процедуры с атрибутами [возможно] или [message] не могут иметь параметры [out] или возвращаемые значения должны иметь тип HRESULT или error_status_t</dt> <dd> Поскольку процедуры [<a href="maybe.md"><strong>возможно</strong></a>] никогда не возвращают, возврат возвращаемых значений невозможен.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2289"></span><span id="midl2289"></span><dl> <dt><strong>MIDL2289</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_to_function_must_be_used"></span><span id="POINTER_TO_FUNCTION_MUST_BE_USED"></span>необходимо использовать указатель на функцию</dt> <dd> Хотя определения типа функции разрешены в режиме <a href="-c-ext.md"><strong>/c_ext</strong></a> , они могут использоваться только в качестве указателей на функции. Они никогда не могут передаваться в качестве параметра или возвращаемого значения удаленной процедуры.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2290"></span><span id="midl2290"></span><dl> <dt><strong>MIDL2290</strong></dt> </dl></td>
<td><dl> <dt><span id="functions_may_not_be_passed_in_an_RPC_operation"></span><span id="functions_may_not_be_passed_in_an_rpc_operation"></span><span id="FUNCTIONS_MAY_NOT_BE_PASSED_IN_AN_RPC_OPERATION"></span>функции не могут передаваться в операции RPC</dt> <dd> Функции и указатели функций не могут передаваться как параметры или возвращаемые значения удаленных процедур.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2291"></span><span id="midl2291"></span><dl> <dt><strong>MIDL2291</strong></dt> </dl></td>
<td><dl> <dt><span id="hyper_double_not_supported_as_return_value_for__Oi_modes__using__Os"></span><span id="hyper_double_not_supported_as_return_value_for__oi_modes__using__os"></span><span id="HYPER_DOUBLE_NOT_SUPPORTED_AS_RETURN_VALUE_FOR__OI_MODES__USING__OS"></span>Технология Hyper/Double не поддерживается в качестве возвращаемого значения для режимов/OI с помощью параметра/OS</dt> <dd> Возвращаемые значения Hyper и Double могут обрабатываться только суррогатами оптимизации <a href="-os.md"><strong>/OS</strong></a> . Заглушки для этой подпрограммы будут созданы с помощью функции оптимизации " <strong>/OS</strong> ".<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2292"></span><span id="midl2292"></span><dl> <dt><strong>MIDL2292</strong></dt> </dl></td>
<td><dl> <dt><span id="_pragma_pack_pop__without_matching__pragma_pack_push_"></span><span id="_PRAGMA_PACK_POP__WITHOUT_MATCHING__PRAGMA_PACK_PUSH_"></span>#pragma pack (POP) без соответствующего #pragma pack (Push)</dt> <dd> #Директива pragma pack (Push) и пакет #pragma (POP) должны появиться в совпадающих парах. Указано по крайней мере одно из нескольких #pragma pack (Push).<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2293"></span><span id="midl2293"></span><dl> <dt><strong>MIDL2293</strong></dt> </dl></td>
<td><dl> <dt><span id="stringable_structure_fields_must_be_byte_char_wchar_t"></span><span id="STRINGABLE_STRUCTURE_FIELDS_MUST_BE_BYTE_CHAR_WCHAR_T"></span>строковые поля структуры должны быть Byte/char/wchar_t</dt> <dd> Тип [<a href="string.md"><strong>String</strong></a>] можно применить только к структуре, поля которой имеют тип Byte, или определение типа, эквивалентное Byte.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2294"></span><span id="midl2294"></span><dl> <dt><strong>MIDL2294</strong></dt> </dl></td>
<td><dl> <dt><span id="_notify__not_supported_for__Oi_modes__using__Os"></span><span id="_notify__not_supported_for__oi_modes__using__os"></span><span id="_NOTIFY__NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>[notify] не поддерживается для режимов/OI с помощью/OS</dt> <dd> Атрибут [<a href="notify.md"><strong>Notify</strong></a>] может быть обработан только суррогатами оптимизации <a href="-os.md"><strong>/OS</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2295"></span><span id="midl2295"></span><dl> <dt><strong>MIDL2295</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle_parameter_or_return_type_is_not_supported_on_a_procedure_in_an__object__interface"></span><span id="_HANDLE_PARAMETER_OR_RETURN_TYPE_IS_NOT_SUPPORTED_ON_A_PROCEDURE_IN_AN__OBJECT__INTERFACE"></span> параметр обработки или возвращаемый тип не поддерживается для процедуры в интерфейсе [Object]</dt> <dd> Дескрипторы нельзя использовать с интерфейсами [ <a href="object.md"><strong>Object</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2296"></span><span id="midl2296"></span><dl> <dt><strong>MIDL2296</strong></dt> </dl></td>
<td><dl> <dt><span id="ANSI_C_only_allows_the_leftmost_array_bound_to_be_unspecified"></span><span id="ansi_c_only_allows_the_leftmost_array_bound_to_be_unspecified"></span><span id="ANSI_C_ONLY_ALLOWS_THE_LEFTMOST_ARRAY_BOUND_TO_BE_UNSPECIFIED"></span>ANSI C позволяет не указывать крайний левый массив</dt> <dd> В соответствии с совместимым массивом ANSI C позволяет не указывать только крайний левый (наиболее значимый) массив. Если задано несколько измерений, MIDL попытается вставить &quot; 1 &quot; в другие согласованные измерения. Если другие измерения определены в другом определении типа, это невозможно. Чтобы избежать этого, Попробуйте поместить все измерения массива в объявление массива. В любом случае, будьте осторожны с вычислениями индексации массива, выполненными компилятором. Вам может потребоваться выполнить собственные вычисления, используя фактические размеры.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2297"></span><span id="midl2297"></span><dl> <dt><strong>MIDL2297</strong></dt> </dl></td>
<td><dl> <dt><span id="by-value_union_parameters_not_supported_for__Oi_modes__using__Os"></span><span id="by-value_union_parameters_not_supported_for__oi_modes__using__os"></span><span id="BY-VALUE_UNION_PARAMETERS_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>Параметры объединения по значению не поддерживаются для режимов/OI с помощью/OS</dt> <dd> Это действие не поддерживается для полностью интерпретируемой оптимизации. Переключение на смешанный режим оптимизации.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2298"></span><span id="midl2298"></span><dl> <dt><strong>MIDL2298</strong></dt> </dl></td>
<td><dl> <dt><span id="_version__attribute_is_ignored_on_an__object__interface"></span><span id="_VERSION__ATTRIBUTE_IS_IGNORED_ON_AN__OBJECT__INTERFACE"></span>атрибут [Version] не учитывается в интерфейсе [Object]</dt> <dd> Атрибут [<a href="object.md"><strong>Object</strong></a>] определяет COM-интерфейс. Список атрибутов интерфейса для COM-интерфейса не может включать атрибут [ <a href="version.md"><strong>Version</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2299"></span><span id="midl2299"></span><dl> <dt><strong>MIDL2299</strong></dt> </dl></td>
<td><dl> <dt><span id="_size_is__or__max_is__attribute_is_invalid_on_a_fixed_array"></span><span id="_SIZE_IS__OR__MAX_IS__ATTRIBUTE_IS_INVALID_ON_A_FIXED_ARRAY"></span>Недопустимый атрибут [size_is] или [max_is] в фиксированном массиве</dt> <dd> Массивы фиксированного размера не могут использовать атрибуты <a href="size-is.md"><strong>size_is</strong></a> или <a href="max-is.md"><strong>max_is</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2300"></span><span id="midl2300"></span><dl> <dt><strong>MIDL2300</strong></dt> </dl></td>
<td><dl> <dt><span id="_encode__or__decode__are_invalid_in_an__object__interface"></span><span id="_ENCODE__OR__DECODE__ARE_INVALID_IN_AN__OBJECT__INTERFACE"></span>[Encoded] или [декодирование] недопустимы в интерфейсе [Object]</dt> <dd> Атрибут [<a href="object.md"><strong>Object</strong></a>] определяет COM-интерфейс. Атрибуты [<a href="encode.md"><strong>Encoded</strong></a>] и [ <a href="decode.md"><strong>дешифровки</strong></a>] обеспечивают сериализацию. Это значит, что вы можете предоставлять и контролировать буферы для маршалирования и распаковки данных, однако нельзя выполнять сериализацию в интерфейсах COM.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2301"></span><span id="midl2301"></span><dl> <dt><strong>MIDL2301</strong></dt> </dl></td>
<td><dl> <dt><span id="_encode__or__decode__on_a_type_requires__ms_ext"></span><span id="_ENCODE__OR__DECODE__ON_A_TYPE_REQUIRES__MS_EXT"></span>[Encoded] или [дешифровки] для типа требуется/ms_ext</dt> <dd> Сериализация не входит в спецификацию DCE-IDL. Это расширение Microsoft, которое требует использования параметра командной строки <a href="-ms-ext.md"><strong>/ms_ext</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2302"></span><span id="midl2302"></span><dl> <dt><strong>MIDL2302</strong></dt> </dl></td>
<td><dl> <dt><span id="int_not_supported_on__env_win16_or__env_dos"></span><span id="INT_NOT_SUPPORTED_ON__ENV_WIN16_OR__ENV_DOS"></span>int не поддерживается в/env Win16 или/env DOS</dt> <dd> 16-разрядные платформы Майкрософт не поддерживают использование типа <a href="int.md"><strong>int</strong></a> в IDL-файле. Уточните тип <strong>int</strong> на <a href="small.md"><strong>малый</strong></a>, <a href="short.md"><strong>короткий</strong></a>или <a href="long.md"><strong>длинный</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2303"></span><span id="midl2303"></span><dl> <dt><strong>MIDL2303</strong></dt> </dl></td>
<td><dl> <dt><span id="_bstring__may_only_be_applied_to_a_pointer_to__char__or__whchar_t_"></span><span id="_BSTRING__MAY_ONLY_BE_APPLIED_TO_A_POINTER_TO__CHAR__OR__WHCHAR_T_"></span>[bString] может применяться только к указателю на &quot; char &quot; или &quot; whchar_t&quot;</dt> <dd> Эта ошибка устарела. Он предоставляется только для обеспечения обратной совместимости.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2304"></span><span id="midl2304"></span><dl> <dt><strong>MIDL2304</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_invalid_on_a_procedure_in_an__object__interface"></span><span id="ATTRIBUTE_INVALID_ON_A_PROCEDURE_IN_AN__OBJECT__INTERFACE"></span>Недопустимый атрибут в процедуре в интерфейсе [Object]</dt> <dd> Указанный атрибут не разрешен в процедуре в COM-интерфейсе.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2305"></span><span id="midl2305"></span><dl> <dt><strong>MIDL2305</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_invalid_on_an__object__interface"></span><span id="ATTRIBUTE_INVALID_ON_AN__OBJECT__INTERFACE"></span>Недопустимый атрибут для интерфейса [Object]</dt> <dd> Указанный атрибут не допускается в COM-интерфейсе.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2306"></span><span id="midl2306"></span><dl> <dt><strong>MIDL2306</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_parameters_or_stack_too_big_for__Oi_modes__using__Os"></span><span id="too_many_parameters_or_stack_too_big_for__oi_modes__using__os"></span><span id="TOO_MANY_PARAMETERS_OR_STACK_TOO_BIG_FOR__OI_MODES__USING__OS"></span>слишком много параметров или слишком большой стек для режимов/OI с использованием/OS</dt> <dd> Это предупреждение устарело. Он предоставляется только для обеспечения обратной совместимости. Он указывает, что вызов удаленной процедуры приводит к увеличению стека размером более 64 КБ.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2307"></span><span id="midl2307"></span><dl> <dt><strong>MIDL2307</strong></dt> </dl></td>
<td><dl> <dt><span id="no_attributes_on_ACF_file_typedef__so_no_effect"></span><span id="no_attributes_on_acf_file_typedef__so_no_effect"></span><span id="NO_ATTRIBUTES_ON_ACF_FILE_TYPEDEF__SO_NO_EFFECT"></span>нет атрибутов в ACF файле typedef, без влияния</dt> <dd> IDL-файл должен содержать все операторы typedef, которые не имеют атрибутов. Они не должны находиться в файлах ACF. В противном случае компилятор MIDL интерпретирует их как избыточный и игнорирует их.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2308"></span><span id="midl2308"></span><dl> <dt><strong>MIDL2308</strong></dt> </dl></td>
<td><dl> <dt><span id="calling_conventions_other_than___stdcall_or___cdecl_not_supported_for__Oi_modes__using__Os"></span><span id="calling_conventions_other_than___stdcall_or___cdecl_not_supported_for__oi_modes__using__os"></span><span id="CALLING_CONVENTIONS_OTHER_THAN___STDCALL_OR___CDECL_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>соглашения о вызовах, отличные от __stdcall или __cdecl, не поддерживаются для режимов/OI с помощью/OS</dt> <dd> Соглашения о вызовах, такие как <strong>__pascal</strong> или <strong>__fastcall</strong> , изменяют формат стека. Режимы <a href="-oi.md"><strong>/Oi</strong></a> поддерживают только соглашения о вызовах <strong>__stdcall</strong> и <strong>__cdecl</strong> . Если необходимо использовать другие соглашения о вызовах, используйте режим <a href="-os.md"><strong>/OS</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2309"></span><span id="midl2309"></span><dl> <dt><strong>MIDL2309</strong></dt> </dl></td>
<td><dl> <dt><span id="Too_many_delegation_methods_in_the_interface__require_Windows_2000_or_greater"></span><span id="too_many_delegation_methods_in_the_interface__require_windows_2000_or_greater"></span><span id="TOO_MANY_DELEGATION_METHODS_IN_THE_INTERFACE__REQUIRE_WINDOWS_2000_OR_GREATER"></span>слишком много методов делегирования в интерфейсе, требуется Windows 2000 или более</dt> <dd> Один интерфейс может наследовать от другого. В этом случае методы базового интерфейса считаются делегированными. Ни один производный интерфейс не может содержать более 256 делегированных методов.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2310"></span><span id="midl2310"></span><dl> <dt><strong>MIDL2310</strong></dt> </dl></td>
<td><dl> <dt><span id="auto_handles_not_supported_with__env_mac_or__env_powermac"></span><span id="AUTO_HANDLES_NOT_SUPPORTED_WITH__ENV_MAC_OR__ENV_POWERMAC"></span>автоматические дескрипторы не поддерживаются для/env Mac или/env повермак</dt> <dd> При компиляции IDL-файла для Повермак нельзя использовать автоматические дескрипторы привязки. Необходимо указать явные или неявные дескрипторы.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2311"></span><span id="midl2311"></span><dl> <dt><strong>MIDL2311</strong></dt> </dl></td>
<td><dl> <dt><span id="statements_outside_library_block_are_illegal_in_mktyplib_compatibility_mode"></span><span id="STATEMENTS_OUTSIDE_LIBRARY_BLOCK_ARE_ILLEGAL_IN_MKTYPLIB_COMPATIBILITY_MODE"></span>операторы вне блока библиотеки недопустимы в режиме совместимости MkTypLib</dt> <dd> При компиляции IDL-файла может потребоваться указать параметр командной строки <a href="-mktyplib203.md"><strong>/mktyplib203</strong></a> .<br/>
<blockquote>
[!Note]<br />
Средство Mktyplib.exe устарело. Вместо этого используйте компилятор MIDL.
</blockquote>
<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2312"></span><span id="midl2312"></span><dl> <dt><strong>MIDL2312</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_syntax_unless_using_mktyplib_compatibility_mode"></span><span id="ILLEGAL_SYNTAX_UNLESS_USING_MKTYPLIB_COMPATIBILITY_MODE"></span>Недопустимый синтаксис, если не используется режим совместимости MkTypLib</dt> <dd> При компиляции IDL-файла может потребоваться указать параметр командной строки <a href="-mktyplib203.md"><strong>/mktyplib203</strong></a> .<br/>
<blockquote>
[!Note]<br />
Средство Mktyplib.exe устарело. Вместо этого используйте компилятор MIDL.
</blockquote>
<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2313"></span><span id="midl2313"></span><dl> <dt><strong>MIDL2313</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_definition__must_use_typedef_in_mktyplib_compatibility_mode"></span><span id="ILLEGAL_DEFINITION__MUST_USE_TYPEDEF_IN_MKTYPLIB_COMPATIBILITY_MODE"></span>Недопустимое определение, необходимо использовать typedef в режиме совместимости MkTypLib</dt> <dd> При компиляции IDL-файла может потребоваться указать параметр командной строки <a href="-mktyplib203.md"><strong>/mktyplib203</strong></a> .<br/>
<blockquote>
[!Note]<br />
Средство Mktyplib.exe устарело. Вместо этого используйте компилятор MIDL.
</blockquote>
<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2314"></span><span id="midl2314"></span><dl> <dt><strong>MIDL2314</strong></dt> </dl></td>
<td><dl> <dt><span id="explicit_pointer_attribute__ptr___ref__ignored_for_interface_pointers"></span><span id="EXPLICIT_POINTER_ATTRIBUTE__PTR___REF__IGNORED_FOR_INTERFACE_POINTERS"></span>явный атрибут указателя [PTR] [ref] игнорируется для указателей интерфейса</dt> <dd> Указатели на интерфейсы не могут иметь атрибуты IDL.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2315"></span><span id="midl2315"></span><dl> <dt><strong>MIDL2315</strong></dt> </dl></td>
<td>Режимы <a href="-oi.md"><strong>/Oi</strong></a> , не реализованные для повермак, переключение на <a href="-os.md"> <strong>/OS</strong></a><br/></td>
</tr>
<tr class="odd">
<td><span id="MIDL2316"></span><span id="midl2316"></span><dl> <dt><strong>MIDL2316</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_expression_type_used_in_attribute"></span><span id="ILLEGAL_EXPRESSION_TYPE_USED_IN_ATTRIBUTE"></span>в атрибуте используется недопустимый тип выражения</dt> <dd> Значение по умолчанию для указателя должно быть константой.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2317"></span><span id="midl2317"></span><dl> <dt><strong>MIDL2317</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_type_used_in_pipe"></span><span id="ILLEGAL_TYPE_USED_IN_PIPE"></span>в канале используется недопустимый тип</dt> <dd> Каналы ограничены базовыми типами данных IDL. Например, нельзя указать канал массивов.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2318"></span><span id="midl2318"></span><dl> <dt><strong>MIDL2318</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_uses_pipes__using__Oicf"></span><span id="procedure_uses_pipes__using__oicf"></span><span id="PROCEDURE_USES_PIPES__USING__OICF"></span>процедура использует каналы с помощью/Oicf</dt> <dd> Выбранный режим не поддерживает каналы. Компилятор MIDL обнаружил использование одного или нескольких каналов в интерфейсе. Таким образом, он компилирует IDL-файл в режиме <a href="-oi.md"><strong>/Oicf</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2319"></span><span id="midl2319"></span><dl> <dt><strong>MIDL2319</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_has_an_attribute_that_requires_use_of__Oif__switching_modes"></span><span id="procedure_has_an_attribute_that_requires_use_of__oif__switching_modes"></span><span id="PROCEDURE_HAS_AN_ATTRIBUTE_THAT_REQUIRES_USE_OF__OIF__SWITCHING_MODES"></span>процедура имеет атрибут, который требует использования/OIF, переключения режимов</dt> <dd> Процедуры [<a href="async.md"><strong>Async</strong></a>] необходимо компилировать в режиме <a href="-oi.md"><strong>/OIF</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2320"></span><span id="midl2320"></span><dl> <dt><strong>MIDL2320</strong></dt> </dl></td>
<td><dl> <dt><span id="conflicting_optimization_requirements__cannot_optimize"></span><span id="CONFLICTING_OPTIMIZATION_REQUIREMENTS__CANNOT_OPTIMIZE"></span>конфликтующие требования к оптимизации, не удается оптимизировать</dt> <dd> Эта ошибка часто указывает на то, что вы указали оба режима компилятора: <a href="-os.md"><strong>/OS</strong></a> и <a href="-oi.md"><strong>/Oi</strong></a> (или Variant of <strong>/Oi</strong>) MIDL. Это также может означать, что для функций, указанных в файлах IDL и ACL, требуется использовать оба режима. Для оптимизации необходимо выбрать один или другой режим.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2321"></span><span id="midl2321"></span><dl> <dt><strong>MIDL2321</strong></dt> </dl></td>
<td><dl> <dt><span id="pipes_cannot_be_array_elements__or_members_of_structures_or_unions"></span><span id="PIPES_CANNOT_BE_ARRAY_ELEMENTS__OR_MEMBERS_OF_STRUCTURES_OR_UNIONS"></span>каналы не могут быть элементами массива или членами структур или объединений</dt> <dd> Типы данных канала могут быть только параметрами верхнего уровня.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2322"></span><span id="midl2322"></span><dl> <dt><strong>MIDL2322</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_pipe_usage"></span><span id="INVALID_PIPE_USAGE"></span>Недопустимое использование канала</dt> <dd> Нельзя использовать каналы с атрибутами [<a href="transmit-as.md"><strong>transmit_as</strong></a>], [<a href="represent-as.md"><strong>represent_as</strong></a>] или [<a href="user-marshal.md"><strong>user_marshal</strong></a>]. Кроме того, нельзя использовать каналы в качестве возвращаемых типов.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2323"></span><span id="midl2323"></span><dl> <dt><strong>MIDL2323</strong></dt> </dl></td>
<td><dl> <dt><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-Oicf"></span><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-oicf"></span><span id="FEATURE_REQUIRES_THE_ADVANCED_INTERPRETED_OPTIMIZATION_OPTION__USE_-OICF"></span>для функции требуется расширенный интерпретируемый параметр оптимизации. Use-Оикф</dt> <dd> Эта ошибка означает, что для параметров командной строки компилятора MIDL, таких как <a href="-robust.md"><strong>/robust</strong></a> , требуется использовать режим <a href="-oi.md"><strong>/Oicf</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2324"></span><span id="midl2324"></span><dl> <dt><strong>MIDL2324</strong></dt> </dl></td>
<td><dl> <dt><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-Oicf"></span><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-oicf"></span><span id="FEATURE_REQUIRES_THE_ADVANCED_INTERPRETED_OPTIMIZATION_OPTION__USE_-OICF"></span>для функции требуется расширенный интерпретируемый параметр оптимизации. Use-Оикф</dt> <dd> Это предупреждение означает, что для параметров командной строки компилятора MIDL, таких как <a href="-robust.md"><strong>/robust</strong></a> , требуется использовать режим <a href="-oi.md"><strong>/Oicf</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2329"></span><span id="midl2329"></span><dl> <dt><strong>MIDL2329</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-Oic"></span><span id="the_optimization_option_is_being_phased_out__use_-oic"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-OIC"></span>этап оптимизации истекает, используйте параметр-ОИК.</dt> <dd> В командной строке MIDL был указан режим оптимизации <a href="-oi.md"><strong>/Oi1</strong></a> . Этот режим больше не поддерживается, и вместо него следует использовать <strong>/Oicf</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2330"></span><span id="midl2330"></span><dl> <dt><strong>MIDL2330</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-Oicf"></span><span id="the_optimization_option_is_being_phased_out__use_-oicf"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-OICF"></span>этап оптимизации истекает, используйте параметр-Оикф.</dt> <dd> В командной строке MIDL был указан режим оптимизации <a href="-oi.md"><strong>/Oi2</strong></a> . Этот режим больше не поддерживается, и вместо него следует использовать <strong>/Oicf</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2331"></span><span id="midl2331"></span><dl> <dt><strong>MIDL2331</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-ic"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-IC"></span>этап оптимизации истекает, используется параметр-IC</dt> <dd> Режим оптимизации I1 был указан в атрибуте [optimize] ACF. Этот режим больше не поддерживается, и вместо него следует использовать ICF.<br/> Пример файла ACF:<br/>
<pre class="syntax" data-space="preserve"><code>[optimize(&quot;i1&quot;)] roo();    //MIDL 2331</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2332"></span><span id="midl2332"></span><dl> <dt><strong>MIDL2332</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-icf"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-ICF"></span>этап оптимизации истекает, используйте параметр-ICF</dt> <dd> Режим оптимизации I2 был указан в атрибуте ACF [optimize]. Этот режим больше не поддерживается, и вместо него следует использовать ICF.<br/> Пример файла ACF:<br/>
<pre class="syntax" data-space="preserve"><code>[optimize(&quot;i2&quot;)] roo();    //MIDL 2332</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2333"></span><span id="midl2333"></span><dl> <dt><strong>MIDL2333</strong></dt> </dl></td>
<td><dl> <dt><span id="the_-old_and_-new_switches_are_obsolete__use_-oldtlb_and_-newtlb"></span><span id="THE_-OLD_AND_-NEW_SWITCHES_ARE_OBSOLETE__USE_-OLDTLB_AND_-NEWTLB"></span>Параметры-Old и-New устарели, используйте параметр-олдтлб и-невтлб.</dt> <dd> Это сообщение устарело и больше не пропускается MIDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2334"></span><span id="midl2334"></span><dl> <dt><strong>MIDL2334</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_argument_value"></span><span id="ILLEGAL_ARGUMENT_VALUE"></span>Недопустимое значение аргумента</dt> <dd> Допустимые варианты параметра командной строки/O: <a href="-os.md"><strong>/OS</strong></a>, <a href="-oi.md"><strong>/Oi</strong></a>, <strong>/ОИК</strong>, <strong>/Oicf</strong>и <strong>/OIF</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2335"></span><span id="midl2335"></span><dl> <dt><strong>MIDL2335</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_expression_type_in_constant"></span><span id="ILLEGAL_EXPRESSION_TYPE_IN_CONSTANT"></span>Недопустимый тип выражения в константе</dt> <dd> Выражение не вычисляется как константа.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2336"></span><span id="midl2336"></span><dl> <dt><strong>MIDL2336</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_expression_type_in_enum"></span><span id="ILLEGAL_EXPRESSION_TYPE_IN_ENUM"></span>Недопустимый тип выражения в enum</dt> <dd> Перечислимое значение в определении <a href="enum.md"><strong>перечисления</strong></a> не вычисляется как целочисленный тип.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2337"></span><span id="midl2337"></span><dl> <dt><strong>MIDL2337</strong></dt> </dl></td>
<td><dl> <dt><span id="unsatisfied_forward_declaration"></span><span id="UNSATISFIED_FORWARD_DECLARATION"></span>неудовлетворенное последовательное объявление</dt> <dd> Компилятору MIDL не удалось разрешить определение прямого объявления.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2338"></span><span id="midl2338"></span><dl> <dt><strong>MIDL2338</strong></dt> </dl></td>
<td><dl> <dt><span id="switches_are_contradictory"></span><span id="SWITCHES_ARE_CONTRADICTORY"></span>параметры не противоречат друг другу</dt> <dd> При компиляции IDL-файла нельзя использовать оба параметра командной строки <a href="-osf.md"><strong>/ОСФ</strong></a> и <a href="-ms-ext.md"><strong>/ms_ext</strong></a> . Необходимо выбрать один или другой.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2339"></span><span id="midl2339"></span><dl> <dt><strong>MIDL2339</strong></dt> </dl></td>
<td><dl> <dt><span id="MIDL_cannot_generate_HOOKOLE_information_for_the_non-rpc-able_union"></span><span id="midl_cannot_generate_hookole_information_for_the_non-rpc-able_union"></span><span id="MIDL_CANNOT_GENERATE_HOOKOLE_INFORMATION_FOR_THE_NON-RPC-ABLE_UNION"></span>MIDL не может создать сведения ХУКОЛЕ для объединения, не допускающего RPC-доступ</dt> <dd> Эта ошибка устарела. Он предоставляется исключительно для обеспечения обратной совместимости.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2340"></span><span id="midl2340"></span><dl> <dt><strong>MIDL2340</strong></dt> </dl></td>
<td><dl> <dt><span id="no_case_expression_found_for_union"></span><span id="NO_CASE_EXPRESSION_FOUND_FOR_UNION"></span>не найдено выражение CASE для объединения</dt> <dd> Каждое поле объединения должно содержать оператор case с константным выражением.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2341"></span><span id="midl2341"></span><dl> <dt><strong>MIDL2341</strong></dt> </dl></td>
<td><dl> <dt><span id="_user_marshal__and__wire_marshal__not_supported_with_-Oi_and_-Oic_flags__use_-Os_or_-Oicf"></span><span id="_user_marshal__and__wire_marshal__not_supported_with_-oi_and_-oic_flags__use_-os_or_-oicf"></span><span id="_USER_MARSHAL__AND__WIRE_MARSHAL__NOT_SUPPORTED_WITH_-OI_AND_-OIC_FLAGS__USE_-OS_OR_-OICF"></span>[user_marshal] и [wire_marshal] не поддерживаются с флагами-Oi и-ОИК, используйте-OS или-Оикф</dt> <dd> Для атрибутов [<a href="user-marshal.md"><strong>user_marshal</strong></a>] и [<a href="wire-marshal.md"><strong>wire_marshal</strong></a>] требуются определенные функции оптимизации, доступные только в <a href="-oi.md"><strong>/Oicf</strong></a> (прокси без кода с строками быстрого формата) или <a href="-os.md"><strong>/OS</strong></a> (маршалирование в смешанном режиме).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2342"></span><span id="midl2342"></span><dl> <dt><strong>MIDL2342</strong></dt> </dl></td>
<td><dl> <dt><span id="pipes_can_t_be_used_with_data_serialization__i.e.__encode__and_or__decode_"></span><span id="PIPES_CAN_T_BE_USED_WITH_DATA_SERIALIZATION__I.E.__ENCODE__AND_OR__DECODE_"></span>нельзя использовать каналы с сериализацией данных, например [Encoded] и/или [расшифровка]</dt> <dd> Передавать каналы в качестве параметров в процедуры, имеющие атрибуты [<a href="encode.md"><strong>Encoded</strong></a>] или [<a href="decode.md"><strong>дешифровки</strong></a>], нельзя.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2343"></span><span id="midl2343"></span><dl> <dt><strong>MIDL2343</strong></dt> </dl></td>
<td><dl> <dt><span id="all_pipe_interface_pointers_must_use_single_indirection"></span><span id="ALL_PIPE_INTERFACE_POINTERS_MUST_USE_SINGLE_INDIRECTION"></span>все указатели интерфейса канала должны использовать одиночное косвенное обращение</dt> <dd> Таким образом нельзя использовать указатель на указатель на интерфейс канала.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2344"></span><span id="midl2344"></span><dl> <dt><strong>MIDL2344</strong></dt> </dl></td>
<td><dl> <dt><span id="_iid_is____cannot_be_used_with_a_pipe_interface_pointer"></span><span id="_IID_IS____CANNOT_BE_USED_WITH_A_PIPE_INTERFACE_POINTER"></span>[iid_is ()] нельзя использовать с указателем интерфейса канала</dt> <dd> Это сообщение устарело. Это сообщение больше не используется компилятором.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2345"></span><span id="midl2345"></span><dl> <dt><strong>MIDL2345</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_or_inapplicable_-lcid_switch"></span><span id="INVALID_OR_INAPPLICABLE_-LCID_SWITCH"></span>Недопустимый или неприменимый параметр-LCID</dt> <dd> Указан недопустимый локальный идентификатор (LCID).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2346"></span><span id="midl2346"></span><dl> <dt><strong>MIDL2346</strong></dt> </dl></td>
<td><dl> <dt><span id="the_specified_lcid_is_different_from_previous_specification"></span><span id="THE_SPECIFIED_LCID_IS_DIFFERENT_FROM_PREVIOUS_SPECIFICATION"></span>указанный код языка отличается от предыдущей спецификации</dt> <dd> Значения, указанные в/LCID и [<a href="lcid.md"><strong>LCID</strong></a>], отличаются. Компилятор MIDL будет использовать определенную последнюю из них.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2347"></span><span id="midl2347"></span><dl> <dt><strong>MIDL2347</strong></dt> </dl></td>
<td><dl> <dt><span id="importlib_is_not_allowed_outside_of_a_library_block"></span><span id="IMPORTLIB_IS_NOT_ALLOWED_OUTSIDE_OF_A_LIBRARY_BLOCK"></span>importlib не разрешено за пределами блока библиотеки</dt> <dd> Все операторы [<a href="importlib.md"><strong>importlib</strong></a>] должны находиться в блоке [<a href="library.md"><strong>Library</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2348"></span><span id="midl2348"></span><dl> <dt><strong>MIDL2348</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_floating_point_value"></span><span id="INVALID_FLOATING_POINT_VALUE"></span>Недопустимое значение с плавающей точкой</dt> <dd> Эта ошибка не должна выдаваться MIDL. Если эта ошибка возникает, сообщите об ошибке в корпорацию Майкрософт, предоставив все файлы, необходимые для воспроизведения ошибки, включая файлы IDL, файлы ACF, заголовки и т. д.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2349"></span><span id="midl2349"></span><dl> <dt><strong>MIDL2349</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_member"></span><span id="INVALID_MEMBER"></span>Недопустимый член</dt> <dd> Процедуры не могут быть членами библиотеки.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2350"></span><span id="midl2350"></span><dl> <dt><strong>MIDL2350</strong></dt> </dl></td>
<td><dl> <dt><span id="possible_invalid_member"></span><span id="POSSIBLE_INVALID_MEMBER"></span>возможно, недопустимый член</dt> <dd> Чтобы быть допустимым членом библиотеки, элемент Library должен быть модулем, disp-интерфейсом, компонентным классом, оператором if, структурой, объединением, перечислением или прямым объявлением.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2351"></span><span id="midl2351"></span><dl> <dt><strong>MIDL2351</strong></dt> </dl></td>
<td><dl> <dt><span id="mismatch_in_pipe_and_interface_types"></span><span id="MISMATCH_IN_PIPE_AND_INTERFACE_TYPES"></span>несоответствие в каналах и типах интерфейсов</dt> <dd> Это сообщение устарело.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2352"></span><span id="midl2352"></span><dl> <dt><strong>MIDL2352</strong></dt> </dl></td>
<td><dl> <dt><span id="string__varying_array__conformant_array_and_full_pointer_parameters_may_be_incompatible_with_pipe_parameters_during_run_time"></span><span id="STRING__VARYING_ARRAY__CONFORMANT_ARRAY_AND_FULL_POINTER_PARAMETERS_MAY_BE_INCOMPATIBLE_WITH_PIPE_PARAMETERS_DURING_RUN_TIME"></span>строки, различные массивы, согласованные массивы и параметры полного указателя могут быть несовместимы с параметрами канала во время выполнения</dt> <dd> метод, объединяющий одну или несколько строк [in], различные массивы, согласованные массивы и параметры полного указателя, а также любой параметр канала [in] приводит к созданию заглушки, которая выполняется только для последовательностей протокола <strong>ncacn_ *</strong> и <a href="ncalrpc.md"><strong>нкалрпк</strong></a> на Windows компьютерах. Использование заглушки для вызова последовательностей протокола <strong>ncadg_ *</strong> или приема вызовов от других поставщиков использование DCE RPC может привести к сбоям на сервере во время выполнения. эта ошибка возникает, начиная с Windows Server 2003.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2353"></span><span id="midl2353"></span><dl> <dt><strong>MIDL2353</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_be_in"></span><span id="PARAMETER_MUST_BE_IN"></span>параметр должен быть в</dt> <dd> Асинхронные дескрипторы должны быть [<a href="in.md"><strong>in</strong></a>] параметрами.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2354"></span><span id="midl2354"></span><dl> <dt><strong>MIDL2354</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_type_of_an__async__object_must_be_a_double_pointer_to_an_interface"></span><span id="PARAMETER_TYPE_OF_AN__ASYNC__OBJECT_MUST_BE_A_DOUBLE_POINTER_TO_AN_INTERFACE"></span>тип параметра объекта [Async] должен быть двойным указателем на интерфейс</dt> <dd> Параметр должен иметь тип <strong>иасинкманажер</strong> * *.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2355"></span><span id="midl2355"></span><dl> <dt><strong>MIDL2355</strong></dt> </dl></td>
<td><dl> <dt><span id="incorrect_async_handle_type"></span><span id="INCORRECT_ASYNC_HANDLE_TYPE"></span>Неверный тип асинхронного обработчика</dt> <dd> Тип маркера должен быть <strong>иасинкманажер</strong> или типом, производным от <strong>иасинкманажер</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2356"></span><span id="midl2356"></span><dl> <dt><strong>MIDL2356</strong></dt> </dl></td>
<td><dl> <dt><span id="the__internal__switch_enables_unsupported_features__use_with_caution"></span><span id="THE__INTERNAL__SWITCH_ENABLES_UNSUPPORTED_FEATURES__USE_WITH_CAUTION"></span>&quot;внутренний &quot; коммутатор включает неподдерживаемые функции, используйте с осторожностью</dt> <dd> Старайтесь не использовать этот параметр.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2357"></span><span id="midl2357"></span><dl> <dt><strong>MIDL2357</strong></dt> </dl></td>
<td><dl> <dt><span id="async_procedures_cannot_use_auto_handle"></span><span id="ASYNC_PROCEDURES_CANNOT_USE_AUTO_HANDLE"></span>асинхронные процедуры не могут использовать автоматическую обработку</dt> <dd> Для процедур с атрибутом [<a href="async.md"><strong>Async</strong></a>] требуются явные дескрипторы.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2358"></span><span id="midl2358"></span><dl> <dt><strong>MIDL2358</strong></dt> </dl></td>
<td><dl> <dt><span id="error_status_t_should_have_both__comm_status__and__fault_status_"></span><span id="ERROR_STATUS_T_SHOULD_HAVE_BOTH__COMM_STATUS__AND__FAULT_STATUS_"></span>error_status_t должны иметь оба [comm_status] и [fault_status]</dt> <dd> Процедура была указана с помощью атрибутов IDL [возможно] или [message], но тип возвращаемого значения содержит только атрибуты ACF [comm_status] или [fault_status]. Требуются оба атрибута ACF.<br/> Пример файла ACF:<br/>
<pre class="syntax" data-space="preserve"><code>[comm_status] roo();    //MIDL 2358
[fault_status] bar();    //MIDL 2358
[comm_status, fault_status] baz();    //OK</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2359"></span><span id="midl2359"></span><dl> <dt><strong>MIDL2359</strong></dt> </dl></td>
<td><dl> <dt><span id="this_construct_is_only_allowed_within_a_library_block"></span><span id="THIS_CONSTRUCT_IS_ONLY_ALLOWED_WITHIN_A_LIBRARY_BLOCK"></span>Эта конструкция разрешена только в блоке библиотеки</dt> <dd> Модуль может находиться только в блоке библиотеки.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2360"></span><span id="midl2360"></span><dl> <dt><strong>MIDL2360</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_type_redefinition"></span><span id="INVALID_TYPE_REDEFINITION"></span>недопустимое переопределение типа</dt> <dd> Новый тип был рекурсивно определен для несуществующего типа.<br/> Пример<br/>
<pre class="syntax" data-space="preserve"><code>typedef roo roo[10];    //MIDL 2360</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2361"></span><span id="midl2361"></span><dl> <dt><strong>MIDL2361</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with_a__vararg__attribute_must_have_a_SAFEARRAY_VARIANT__parameter__param_order_is__vararg____lcid____retval_"></span><span id="procedures_with_a__vararg__attribute_must_have_a_safearray_variant__parameter__param_order_is__vararg____lcid____retval_"></span><span id="PROCEDURES_WITH_A__VARARG__ATTRIBUTE_MUST_HAVE_A_SAFEARRAY_VARIANT__PARAMETER__PARAM_ORDER_IS__VARARG____LCID____RETVAL_"></span>процедуры с атрибутом [vararg] должны иметь параметр SAFEARRAY (VARIANT). порядок параметров — [vararg], [LCID], [retval]</dt> <dd> Большинство параметров для процедур с атрибутом [<a href="vararg.md"><strong>vararg</strong></a>] должны находиться перед параметром <strong>SAFEARRAY (Variant)</strong> . Должен присутствовать параметр <strong>SAFEARRAY (Variant)</strong> . Если список параметров содержит параметр с атрибутом [ <a href="lcid.md"><strong>LCID</strong></a>], он должен следовать за параметром <strong>SAFEARRAY (Variant)</strong> . Если список параметров содержит параметр с атрибутом [<a href="retval.md"><strong>retval</strong></a>], он должен находиться после параметра с атрибутом [<strong>LCID</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2363"></span><span id="midl2363"></span><dl> <dt><strong>MIDL2363</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_methods_in_the_interface__requires_Windows_2000_or_greater"></span><span id="too_many_methods_in_the_interface__requires_windows_2000_or_greater"></span><span id="TOO_MANY_METHODS_IN_THE_INTERFACE__REQUIRES_WINDOWS_2000_OR_GREATER"></span>слишком много методов в интерфейсе, требуется Windows 2000 или более</dt> <dd> Компилятор MIDL не позволяет использовать более 1024 методов в интерфейсе при компиляции в режиме <a href="-oi.md"><strong>/Oicf</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2364"></span><span id="midl2364"></span><dl> <dt><strong>MIDL2364</strong></dt> </dl></td>
<td><dl> <dt><span id="switch_is_being_phased_out"></span><span id="SWITCH_IS_BEING_PHASED_OUT"></span>идет поэтапный переход</dt> <dd> Следующие параметры устарели:/<strong>хуколе</strong>,/<strong>env Win16</strong>и/<strong>env</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2365"></span><span id="midl2365"></span><dl> <dt><strong>MIDL2365</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_derive_from_IAdviseSink__IAdviseSink2__or_IAdviseSinkEx"></span><span id="cannot_derive_from_iadvisesink__iadvisesink2__or_iadvisesinkex"></span><span id="CANNOT_DERIVE_FROM_IADVISESINK__IADVISESINK2__OR_IADVISESINKEX"></span>не может быть производным от Иадвисесинк, IAdviseSink2 или Иадвисесинкекс</dt> <dd> Эти интерфейсы не могут быть расширены.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2366"></span><span id="midl2366"></span><dl> <dt><strong>MIDL2366</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_assign_a_default_value"></span><span id="CANNOT_ASSIGN_A_DEFAULT_VALUE"></span>Невозможно присвоить значение по умолчанию</dt> <dd> присвоение параметру значения по умолчанию допускается в Visual Basic, но не в C++. Если используется C++, значение по умолчанию игнорируется.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2367"></span><span id="midl2367"></span><dl> <dt><strong>MIDL2367</strong></dt> </dl></td>
<td><dl> <dt><span id="type_library_generation_for_DOS_Win16_MAC_is_not_supported"></span><span id="type_library_generation_for_dos_win16_mac_is_not_supported"></span><span id="TYPE_LIBRARY_GENERATION_FOR_DOS_WIN16_MAC_IS_NOT_SUPPORTED"></span>Создание библиотеки типов для DOS/Win16/MAC не поддерживается</dt> <dd> MIDL не поддерживает 16-разрядные библиотеки типов.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2368"></span><span id="midl2368"></span><dl> <dt><strong>MIDL2368</strong></dt> </dl></td>
<td><dl> <dt><span id="error_generating_type_library__ignored"></span><span id="ERROR_GENERATING_TYPE_LIBRARY__IGNORED"></span>Ошибка при создании библиотеки типов, игнорируется</dt> <dd> При создании библиотеки типов произошла неустранимая ошибка.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2369"></span><span id="midl2369"></span><dl> <dt><strong>MIDL2369</strong></dt> </dl></td>
<td><dl> <dt><span id="exceeded_stack_size_for__Oi__using__Os"></span><span id="exceeded_stack_size_for__oi__using__os"></span><span id="EXCEEDED_STACK_SIZE_FOR__OI__USING__OS"></span>Превышен размер стека для/OI с использованием/OS</dt> <dd> Режим оптимизации-Oi ограничен 128 байт пространства стека для параметров. Для обхода этого ограничения компилятор автоматически переключился на режим оптимизации ОС.<br/> Чтобы избежать этого предупреждения, используйте режимы оптимизации-Оикф или-OS. Режим оптимизации можно изменить в командной строке, указав параметр-Оикф или-OS вместо-Oi или добавив атрибут [optimize9 &quot; ICF &quot; )] или optimize [( &quot; s &quot; )] в функцию в файле ACF.<br/> Это предупреждение обычно происходит при передаче больших структур в качестве параметров по значению. Требуемый размер стека можно уменьшить, передав вместо него указатель на структуру.<br/> Пример<br/>
<pre class="syntax" data-space="preserve"><code>typedef struct
{
char a[127];
}
large;
//This function has a stack size of 132 (x86) or 136 (alpha) on 32-bit systems
void roo(large s, int a);    //MIDL 2360
// workaround: pass by reference
void bar (large *s, int a);</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2370"></span><span id="midl2370"></span><dl> <dt><strong>MIDL2370</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of__robust_requires__Oicf__switching_modes"></span><span id="use_of__robust_requires__oicf__switching_modes"></span><span id="USE_OF__ROBUST_REQUIRES__OICF__SWITCHING_MODES"></span>для использования/robust требуется/Oicf, переключение режимов</dt> <dd> Необходимо компилировать в режиме <a href="-oi.md"><strong>/Oicf</strong></a> при указании параметра <a href="-robust.md"><strong>/robust</strong></a> в командной строке.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2371"></span><span id="midl2371"></span><dl> <dt><strong>MIDL2371</strong></dt> </dl></td>
<td><dl> <dt><span id="incorrect_range_specified"></span><span id="INCORRECT_RANGE_SPECIFIED"></span>указан неверный диапазон</dt> <dd> Наибольшее значение, указанное в атрибуте [<a href="range.md"><strong>Range</strong></a>], меньше наименьшего значения.<br/> Пример<br/>
<pre class="syntax" data-space="preserve"><code>void roo([range(3,2)] int a);    //MIDL 2371</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2372"></span><span id="midl2372"></span><dl> <dt><strong>MIDL2372</strong></dt> </dl></td>
<td><dl> <dt><span id="_invalid_combination_of__in__only_and__out__parameters_for__async_uuid__interface"></span><span id="_INVALID_COMBINATION_OF__IN__ONLY_AND__OUT__PARAMETERS_FOR__ASYNC_UUID__INTERFACE"></span> Недопустимое сочетание [in] только параметров [in] и [out] для интерфейса [async_uuid]</dt> <dd> Для этого типа интерфейса разрешены только простые сочетания атрибутов с параметрами [<a href="in.md"><strong>in</strong></a>] или [<a href="out-idl.md"><strong>out</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2373"></span><span id="midl2373"></span><dl> <dt><strong>MIDL2373</strong></dt> </dl></td>
<td><dl> <dt><span id="DOS__Win16_and_MAC_platforms_are_not_supported_with__robust"></span><span id="dos__win16_and_mac_platforms_are_not_supported_with__robust"></span><span id="DOS__WIN16_AND_MAC_PLATFORMS_ARE_NOT_SUPPORTED_WITH__ROBUST"></span>DOS, платформы Win16 и MAC не поддерживаются с/robust</dt> <dd> MIDL поддерживает параметр <a href="-robust.md"><strong>/robust</strong></a> в Microsoft Windows 2000 или более поздней версии.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2374"></span><span id="midl2374"></span><dl> <dt><strong>MIDL2374</strong></dt> </dl></td>
<td><dl> <dt><span id="support_for_NT_3.51_style_stubless_proxies_for_object_interfaces_will_be_phased_out__use__Oif."></span><span id="support_for_nt_3.51_style_stubless_proxies_for_object_interfaces_will_be_phased_out__use__oif."></span><span id="SUPPORT_FOR_NT_3.51_STYLE_STUBLESS_PROXIES_FOR_OBJECT_INTERFACES_WILL_BE_PHASED_OUT__USE__OIF."></span>будет выдаваться поддержка прокси-серверов без заглушек в стиле NT 3,51 для интерфейсов объектов. Использование/ОИФ.</dt> <dd> Этот режим устарел. Используйте <a href="-oi.md"><strong>/OIF</strong></a> или <strong>/Oicf</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2375"></span><span id="midl2375"></span><dl> <dt><strong>MIDL2375</strong></dt> </dl></td>
<td><dl> <dt><span id="_encode__or__decode__with__robust_requires__Oicf"></span><span id="_encode__or__decode__with__robust_requires__oicf"></span><span id="_ENCODE__OR__DECODE__WITH__ROBUST_REQUIRES__OICF"></span>[Encoded] или [дешифровки] с/robust требует/Oicf</dt> <dd> Невозможно выполнить сериализацию, если указан параметр <a href="-robust.md"><strong>/robust</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2377"></span><span id="midl2377"></span><dl> <dt><strong>MIDL2377</strong></dt> </dl></td>
<td><dl> <dt><span id="conflicting_attributes_specified"></span><span id="CONFLICTING_ATTRIBUTES_SPECIFIED"></span>указаны конфликтующие атрибуты</dt> <dd> Указаны оба варианта: [<a href="context-handle-serialize.md"><strong>context_handle_serialize</strong></a>] и [<a href="context-handle-noserialize.md"><strong>context_handle_noserialize</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2378"></span><span id="midl2378"></span><dl> <dt><strong>MIDL2378</strong></dt> </dl></td>
<td><dl> <dt><span id="_serialize____noserialize__can_be_applied_to_context_handles"></span><span id="_SERIALIZE____NOSERIALIZE__CAN_BE_APPLIED_TO_CONTEXT_HANDLES"></span>[Serialize], [unserialize] можно применять к context_handles</dt> <dd> Атрибуты ACF [context_handle_serialize] или [context_handle_noserialize] могут применяться только к типам, которые являются дескрипторами контекста.<br/> Пример IDL-файла:<br/>
<pre class="syntax" data-space="preserve"><code>typedef /*[context_handle] */ void *PV;    //Note: PV is *not* a context handle.</code></pre>
Пример файла ACF:<br/>
<pre class="syntax" data-space="preserve"><code>typedef [context_handle_serialize] PV;    //MIDL 2378</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2379"></span><span id="midl2379"></span><dl> <dt><strong>MIDL2379</strong></dt> </dl></td>
<td><dl> <dt><span id="The_compiler_reached_a_limit_for_a_format_string_representation._See_documentation_for_advice."></span><span id="the_compiler_reached_a_limit_for_a_format_string_representation._see_documentation_for_advice."></span><span id="THE_COMPILER_REACHED_A_LIMIT_FOR_A_FORMAT_STRING_REPRESENTATION._SEE_DOCUMENTATION_FOR_ADVICE."></span>Компилятор достиг предела для представления строки формата. Советы см. в документации.</dt> <dd> Компилятор MIDL имеет ограничение в 64 КБ для строк формата. Эта ошибка обычно возникает, когда IDL-файлы содержат другие IDL-файлы. Составной IDL-файл, созданный всеми инструкциями include, превышает ограничения таблиц представления типов интерпретатора модуля упаковки. Попробуйте использовать директиву Import вместо директивы include в файлах IDL. Дополнительные сведения см. в разделе <a href="importing-system-header-files.md">Импорт файлов заголовков системы</a>, <a href="include.md"><strong>Включение</strong></a>и <a href="import.md"><strong>Импорт</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2380"></span><span id="midl2380"></span><dl> <dt><strong>MIDL2380</strong></dt> </dl></td>
<td><dl> <dt><span id="wire_format_may_be_incorrect__you_may_need_to_use_-ms_conf_struct__see_documentation_for_advice"></span><span id="WIRE_FORMAT_MAY_BE_INCORRECT__YOU_MAY_NEED_TO_USE_-MS_CONF_STRUCT__SEE_DOCUMENTATION_FOR_ADVICE"></span>неправильный формат подключения, возможно, потребуется использовать параметр-ms_conf_struct. Дополнительные сведения см. в документации.</dt> <dd> Компилятору MIDL не удалось создать формат трансмиссибле для данных. Одним из распространенных способов получения этой ошибки является определение <strong>ms_conf_struct</strong> внутри сложной структуры.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2381"></span><span id="midl2381"></span><dl> <dt><strong>MIDL2381</strong></dt> </dl></td>
<td><dl> <dt><span id="a_stack_size_or_an_offset_bigger_than_64_K_limit._See_documentation_for_advice."></span><span id="a_stack_size_or_an_offset_bigger_than_64_k_limit._see_documentation_for_advice."></span><span id="A_STACK_SIZE_OR_AN_OFFSET_BIGGER_THAN_64_K_LIMIT._SEE_DOCUMENTATION_FOR_ADVICE."></span>размер стека или смещение больше 64 КБ. Советы см. в документации.</dt> <dd> Вызов приводит к поборке в стеке, размер которого превышает 64 КБ. Попробуйте передать данные в более мелких блоках.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2382"></span><span id="midl2382"></span><dl> <dt><strong>MIDL2382</strong></dt> </dl></td>
<td><dl> <dt><span id="an_interpreter_mode_forced_for_64-bit_platform_"></span><span id="AN_INTERPRETER_MODE_FORCED_FOR_64-BIT_PLATFORM_"></span>режим интерпретатора, принудительно используемый для 64-разрядной платформы </dt> <dd> для 64-разрядных платформ требуется режим компиляции/Oicf.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2383"></span><span id="midl2383"></span><dl> <dt><strong>MIDL2383</strong></dt> </dl></td>
<td><dl> <dt><span id="The_array_element_size_is_bigger_than_64_KB_limit."></span><span id="the_array_element_size_is_bigger_than_64_kb_limit."></span><span id="THE_ARRAY_ELEMENT_SIZE_IS_BIGGER_THAN_64_KB_LIMIT."></span>Размер элемента массива превышает ограничение в 64 КБ.</dt> <dd> Размер всех элементов массива должен быть менее 64 КБ.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2384"></span><span id="midl2384"></span><dl> <dt><strong>MIDL2384</strong></dt> </dl></td>
<td><dl> <dt><span id="there_can_be_only_one__Icid__parameter_in_a_method__and_it_should_be_last_or_second_to_last_if_last_parameter_has__retval_"></span><span id="there_can_be_only_one__icid__parameter_in_a_method__and_it_should_be_last_or_second_to_last_if_last_parameter_has__retval_"></span><span id="THERE_CAN_BE_ONLY_ONE__ICID__PARAMETER_IN_A_METHOD__AND_IT_SHOULD_BE_LAST_OR_SECOND_TO_LAST_IF_LAST_PARAMETER_HAS__RETVAL_"></span>в методе может быть только один параметр [ИЦид], который должен быть последним или вторым, если последний параметр имеет [retval]</dt> <dd> Параметр с атрибутом [<a href="lcid.md"><strong>LCID</strong></a>] должен быть последним. Единственным исключением является наличие параметра с атрибутом [<a href="retval.md"><strong>retval</strong></a>]. При возникновении обоих этих двух секунд для последнего параметра в списке параметров должен быть атрибут [ <strong>LCID</strong>]. Последний параметр должен иметь атрибут [<strong>retval</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2385"></span><span id="midl2385"></span><dl> <dt><strong>MIDL2385</strong></dt> </dl></td>
<td><dl> <dt><span id="incorrect_syntax_for_midl_pragma"></span><span id="INCORRECT_SYNTAX_FOR_MIDL_PRAGMA"></span>Неверный синтаксис для midl_pragma</dt> <dd> Компилятор MIDL обнаружил неизвестную синтаксическую ошибку в инструкции midl_pragma.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2386"></span><span id="midl2386"></span><dl> <dt><strong>MIDL2386</strong></dt> </dl></td>
<td><dl> <dt><span id="__int3264_is_not_supported_in__osf_mode"></span><span id="__INT3264_IS_NOT_SUPPORTED_IN__OSF_MODE"></span>__int3264 не поддерживается в режиме/ОСФ</dt> <dd> Если необходимо использовать __int3264, скомпилируйте в режиме/МС-екст.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2387"></span><span id="midl2387"></span><dl> <dt><strong>MIDL2387</strong></dt> </dl></td>
<td><dl> <dt><span id="unresolved_symbol_in_type_library"></span><span id="UNRESOLVED_SYMBOL_IN_TYPE_LIBRARY"></span>неразрешенный символ в библиотеке типов</dt> <dd> Компилятору не удалось разрешить формальное объявление или ссылочный тип в библиотеке типов.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2388"></span><span id="midl2388"></span><dl> <dt><strong>MIDL2388</strong></dt> </dl></td>
<td><dl> <dt><span id="async_pipes_cannot_be_passed_by_value"></span><span id="ASYNC_PIPES_CANNOT_BE_PASSED_BY_VALUE"></span>асинхронные каналы не могут передаваться по значению</dt> <dd> Асинхронные каналы должны передаваться по ссылке или по адресу.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2389"></span><span id="midl2389"></span><dl> <dt><strong>MIDL2389</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_offset_exceed_64-KB_limit_for_interpreted_procedures"></span><span id="parameter_offset_exceed_64-kb_limit_for_interpreted_procedures"></span><span id="PARAMETER_OFFSET_EXCEED_64-KB_LIMIT_FOR_INTERPRETED_PROCEDURES"></span>смещение параметра превышает ограничение в 64 КБ для интерпретируемых процедур</dt> <dd> Эта ошибка обычно означает, что процедура имеет слишком много параметров.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2390"></span><span id="midl2390"></span><dl> <dt><strong>MIDL2390</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_array_element"></span><span id="INVALID_ARRAY_ELEMENT"></span>Недопустимый элемент массива</dt> <dd> Нельзя использовать каналы в качестве элементов массива.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2391"></span><span id="midl2391"></span><dl> <dt><strong>MIDL2391</strong></dt> </dl></td>
<td><dl> <dt><span id="dispinterface_members_must_be_methods__properties_or_interfaces"></span><span id="DISPINTERFACE_MEMBERS_MUST_BE_METHODS__PROPERTIES_OR_INTERFACES"></span>члены DISP должны быть методами, свойствами или интерфейсами</dt> <dd> Диспетчерский интерфейс не может содержать определения типов, структуры, перечисления или объединения.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2392"></span><span id="midl2392"></span><dl> <dt><strong>MIDL2392</strong></dt> </dl></td>
<td><dl> <dt><span id="_local__procedure_without__call_as_"></span><span id="_LOCAL__PROCEDURE_WITHOUT__CALL_AS_"></span>[local] процедура без [call_as]</dt> <dd> Для процедур объектов с атрибутом [<a href="local.md"><strong>Local</strong></a>] также требуется атрибут [<a href="call-as.md"><strong>call_as</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2393"></span><span id="midl2393"></span><dl> <dt><strong>MIDL2393</strong></dt> </dl></td>
<td><dl> <dt><span id="multi_dimensional_vector__switching_to__Oicf"></span><span id="multi_dimensional_vector__switching_to__oicf"></span><span id="MULTI_DIMENSIONAL_VECTOR__SWITCHING_TO__OICF"></span>многомерный вектор, переключение на/Oicf</dt> <dd> Режим оптимизации " <a href="-os.md"><strong>/OS</strong></a> " не поддерживает многомерные массивы нефиксированного размера. Компилятор автоматически переключил режим оптимизации на/<strong>оикф</strong> для этой функции. <br/> Это предупреждение можно отключить глобально, изменив режим компилятора, указав/<strong>оикф</strong> в командной строке MIDL или выполнив <strong>midl_pragma</strong> warning (Disable: 2393) в IDL-файле. Режим оптимизации можно изменить для отдельной функции, добавив атрибут [<strong>optimize ( &quot; ICF &quot; )</strong>] в функцию в файле ACF.<br/> Это предупреждение показано в следующем примере:<br/>
<pre class="syntax" data-space="preserve"><code>void roo(long s1, [size_is(s1)] long a[][30];    //MIDL2393
void bar(long s1, long s2, [size_is(s1,s2) long **a);//MIDL2393</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2395"></span><span id="midl2395"></span><dl> <dt><strong>MIDL2395</strong></dt> </dl></td>
<td><dl> <dt><span id="type_or_construct_not_supported_in_a_library_block_because_Oleaut32.dll_support_for_64-KB_polymorphic_types_is_missing"></span><span id="type_or_construct_not_supported_in_a_library_block_because_oleaut32.dll_support_for_64-kb_polymorphic_types_is_missing"></span><span id="TYPE_OR_CONSTRUCT_NOT_SUPPORTED_IN_A_LIBRARY_BLOCK_BECAUSE_OLEAUT32.DLL_SUPPORT_FOR_64-KB_POLYMORPHIC_TYPES_IS_MISSING"></span>тип или конструкция не поддерживается в блоке библиотеки, так как отсутствует поддержка Oleaut32.dll для недопустимых типов 64 КБ</dt> <dd> OLE-автоматизация не поддерживает типы с полиморфизмом (такие как _int3264, INT_PTR и т. д.). Эти типы имеют несовместимые представления данных между 32-разрядными и 64-разрядными платформами. Удаленный вызов завершится ошибкой во время выполнения на 64-разрядных платформах.<br/>
<blockquote>
[!Note]<br />
обратите внимание, что начиная с версии Windows 2000, 64-разрядные файлы tlb поддерживаются службой автоматизации OLE путем преобразования 32-разрядных данных tlb во время выполнения. Поэтому MIDL поддерживает только 32-разрядное поколение TLB.
</blockquote>
<br/> Если MIDL используется только для создания файла заголовка, параметр <a href="-notlb.md"><strong>/notlb</strong></a> ПОДАВЛЯЕТ создание TLB-файла.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2396"></span><span id="midl2396"></span><dl> <dt><strong>MIDL2396</strong></dt> </dl></td>
<td><dl> <dt><span id="old_interpreter_code_being_generated_for_64b"></span><span id="OLD_INTERPRETER_CODE_BEING_GENERATED_FOR_64B"></span>код старого интерпретатора создается для 64b</dt> <dd> Эта ошибка устарела. Если вы видите эту ошибку, сообщите об ошибке в корпорацию Майкрософт, предоставив файлы IDL, файлы ACF и полную версию MIDL-командной строки.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2397"></span><span id="midl2397"></span><dl> <dt><strong>MIDL2397</strong></dt> </dl></td>
<td><dl> <dt><span id="the_compiler_switch_is_not_supported_anymore"></span><span id="THE_COMPILER_SWITCH_IS_NOT_SUPPORTED_ANYMORE"></span>параметр компилятора больше не поддерживается</dt> <dd> Указанные коммутаторы и переключатели больше не поддерживаются.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2398"></span><span id="midl2398"></span><dl> <dt><strong>MIDL2398</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_execute_MIDL_engine"></span><span id="cannot_execute_midl_engine"></span><span id="CANNOT_EXECUTE_MIDL_ENGINE"></span>не удается выполнить модуль MIDL</dt> <dd> начиная с выпуска Windows 2000 (midl версии 5.03.279), компилятор MIDL реализуется с помощью двух исполняемых файлов: Midl.exe (драйвер) и Midlc.exe (обработчик компилятора). Эта ошибка означает, что Midl.exe не удалось запустить Midlc.exe. Убедитесь, что Midlc.exe находится в том же каталоге, что и Midl.exe, и что они имеют одинаковую версию.<br/> Ошибка могла быть вызвана копированием Midl.exe, но не Midlx.exe из последнего распространения. Выполните <strong>MIDL</strong> или <strong>мидлк</strong> в командной строке без параметров, чтобы просмотреть номер версии исполняемого файла.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2399"></span><span id="midl2399"></span><dl> <dt><strong>MIDL2399</strong></dt> </dl></td>
<td><dl> <dt><span id="bad_commands_from_driver"></span><span id="BAD_COMMANDS_FROM_DRIVER"></span>неверные команды из драйвера</dt> <dd> начиная с выпуска Windows 2000 (midl версии 5.03.279), компилятор MIDL реализуется с помощью двух исполняемых файлов: Midl.exe (драйвер) и Midlc.exe (обработчик компилятора). Эта ошибка означает, что временный файл, используемый для передачи команд из Midl.exe в Midlc.exe, отсутствует или поврежден. Убедитесь, что Midlc.exe находится в том же каталоге, что и Midl.exe, и что они имеют одинаковую версию.<br/> Ошибка могла быть вызвана попыткой запуска Midlc.exe напрямую или копированием Midl.exe, но не Midlc.exe из последнего дистрибутива. Выполните <strong>MIDL</strong> или <strong>мидлк</strong> в командной строке без параметров, чтобы просмотреть номер версии исполняемого файла.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2400"></span><span id="midl2400"></span><dl> <dt><strong>MIDL2400</strong></dt> </dl></td>
<td><dl> <dt><span id="for_ole_automation__optional_parameters_should_be_VARIANT_or_VARIANT__"></span><span id="for_ole_automation__optional_parameters_should_be_variant_or_variant__"></span><span id="FOR_OLE_AUTOMATION__OPTIONAL_PARAMETERS_SHOULD_BE_VARIANT_OR_VARIANT__"></span>для OLE Automation необязательные параметры должны быть ВАРИАНТными или ВАРИАНТными *</dt> <dd> OLE Automation требует, чтобы все [необязательные] параметры были типа <strong>Variant</strong> или <strong>Variant *</strong>.<br/> В OLE-автоматизации использование параметров, не являющихся ВАРИАНТами, может вызвать сбой вызова во время выполнения или передать неопределенные данные для параметров [<a href="optional.md"><strong>Optional</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2401"></span><span id="midl2401"></span><dl> <dt><strong>MIDL2401</strong></dt> </dl></td>
<td><dl> <dt><span id="_defaultvalue__is_applied_to_a_non-VARIANT_and__optional_._Please_remove__optional_"></span><span id="_defaultvalue__is_applied_to_a_non-variant_and__optional_._please_remove__optional_"></span><span id="_DEFAULTVALUE__IS_APPLIED_TO_A_NON-VARIANT_AND__OPTIONAL_._PLEASE_REMOVE__OPTIONAL_"></span>[DefaultValue] применяется к типу, отличному от VARIANT, и [optional]. Удалите [необязательно]</dt> <dd> Атрибут [<a href="defaultvalue.md"><strong>DefaultValue</strong></a>] подразумевает [<a href="optional.md"><strong>необязательный</strong></a>параметр]. Атрибут [ <strong>Optional</strong>] не требуется.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2402"></span><span id="midl2402"></span><dl> <dt><strong>MIDL2402</strong></dt> </dl></td>
<td><dl> <dt><span id="_optional__attribute_is_inapplicable_outside_of_a_library_block"></span><span id="_OPTIONAL__ATTRIBUTE_IS_INAPPLICABLE_OUTSIDE_OF_A_LIBRARY_BLOCK"></span>атрибут [optional] неприменим за пределами блока библиотеки</dt> <dd> Функции, подразумеваемые атрибутом [ <a href="optional.md"><strong>Optional</strong></a>], неприменимы к прокси-серверам, созданным для интерфейса за пределами блока библиотеки.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2403"></span><span id="midl2403"></span><dl> <dt><strong>MIDL2403</strong></dt> </dl></td>
<td><dl> <dt><span id="The_data_type_of_the__Icid__parameter_must_be_long"></span><span id="the_data_type_of_the__icid__parameter_must_be_long"></span><span id="THE_DATA_TYPE_OF_THE__ICID__PARAMETER_MUST_BE_LONG"></span>Тип данных параметра [ИЦид] должен быть длинным</dt> <dd> OLE Automation требует, чтобы параметры с атрибутом [<strong>иЦид</strong>] были типа <a href="long.md"><strong>Long</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2404"></span><span id="midl2404"></span><dl> <dt><strong>MIDL2404</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with__propput____propget__or__propref__can_t_have_more_than_one_required_parameter_after__optional__one"></span><span id="PROCEDURES_WITH__PROPPUT____PROPGET__OR__PROPREF__CAN_T_HAVE_MORE_THAN_ONE_REQUIRED_PARAMETER_AFTER__OPTIONAL__ONE"></span>процедуры с [propput], [propget] или [пропреф] не могут иметь более одного обязательного параметра после [необязательного] одного</dt> <dd> Не может быть более одного параметра без [<a href="optional.md"><strong>Optional</strong></a>] после последнего параметра с [<strong>Optional</strong>] при использовании [<a href="propput.md"><strong>propput</strong></a>], [<a href="propget.md"><strong>propget</strong></a>] или [ <a href="propputref.md"><strong>propputref</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2405"></span><span id="midl2405"></span><dl> <dt><strong>MIDL2405</strong></dt> </dl></td>
<td><dl> <dt><span id="_comm_status__or__fault_status__with_pickling_requires_-Oicf"></span><span id="_comm_status__or__fault_status__with_pickling_requires_-oicf"></span><span id="_COMM_STATUS__OR__FAULT_STATUS__WITH_PICKLING_REQUIRES_-OICF"></span>[comm_status] или [fault_status] с параметром выбора требуется-Оикф</dt> <dd> Режим оптимизации старого параметра-<strong>Oi</strong> не поддерживает процедуры или параметры с [ <a href="comm-status.md"><strong>comm_status</strong></a>] или [ <a href="fault-status.md"><strong>fault_status</strong></a>] с помощью выбора (то есть с помощью [ <a href="encode.md"><strong>Encoded</strong></a>] и/или [ <a href="decode.md"><strong>дешифровки</strong></a>]).<br/> Это предупреждение можно отключить глобально, указав-<strong>оикф</strong> в командной строке MIDL или для отдельной функции, добавив атрибут [optimize ( &quot; ICF:)] к функции в файле ACF.<br/> Как правило, режим оптимизации-<strong>оикф</strong> рекомендуется использовать в режиме over-<strong>Oi</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2406"></span><span id="midl2406"></span><dl> <dt><strong>MIDL2406</strong></dt> </dl></td>
<td><dl> <dt><span id="midl_driver_and_compiler_version_mismatch"></span><span id="MIDL_DRIVER_AND_COMPILER_VERSION_MISMATCH"></span>несоответствие версии драйвера MIDL и компилятора</dt> <dd> начиная с выпуска Windows 2000 (midl версии 5.03.279) компилятор MIDL реализуется с помощью двух исполняемых файлов: Midl.exe (драйвер) и Midlc.exe (обработчик компилятора). Эта ошибка означает, что версия Midl.exe не соответствует версии Midlc.exe.<br/> Ошибка могла быть вызвана копированием Midl.exe, но не Midlc.exe из последнего распространения. Выполните <strong>MIDL</strong> или <strong>мидлк</strong> в командной строке без параметров, чтобы просмотреть номер версии исполняемого файла.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2407"></span><span id="midl2407"></span><dl> <dt><strong>MIDL2407</strong></dt> </dl></td>
<td><dl> <dt><span id="no_intermediate_file_specified__use_Midl.exe"></span><span id="no_intermediate_file_specified__use_midl.exe"></span><span id="NO_INTERMEDIATE_FILE_SPECIFIED__USE_MIDL.EXE"></span>промежуточный файл не указан: используйте Midl.exe</dt> <dd> начиная с выпуска Windows 2000 (midl версии 5.03.279), компилятор MIDL реализуется с помощью двух исполняемых файлов: Midl.exe (драйвер) и Midlc.exe (обработчик компилятора). Эта ошибка означает, что Midlc.exe был запущен напрямую вместо использования Midl.exe.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2408"></span><span id="midl2408"></span><dl> <dt><strong>MIDL2408</strong></dt> </dl></td>
<td><dl> <dt><span id="processing_problem_with_a_parameter_in_a_procedure"></span><span id="PROCESSING_PROBLEM_WITH_A_PARAMETER_IN_A_PROCEDURE"></span>обработка проблемы с параметром в процедуре</dt> <dd> Эта ошибка может возникать при импорте данных из TLB, если процедура имеет недопустимый параметр. <br/> Если вы видите эту ошибку, сообщите об ошибке в корпорацию Майкрософт. Укажите файлы IDL, файлы ACF, TLB-файл и полную командную строку MIDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2409"></span><span id="midl2409"></span><dl> <dt><strong>MIDL2409</strong></dt> </dl></td>
<td><dl> <dt><span id="processing_problem_with_a_field_in_a_structure"></span><span id="PROCESSING_PROBLEM_WITH_A_FIELD_IN_A_STRUCTURE"></span>обработка проблемы с полем в структуре</dt> <dd> Эта ошибка может возникать при импорте данных из TLB, если структура имеет недопустимое поле структуры или объединения.<br/> Если вы видите эту ошибку, сообщите об ошибке в корпорацию Майкрософт. Укажите файлы IDL, файлы ACF, TLB-файл и полную командную строку MIDL.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2410"></span><span id="midl2410"></span><dl> <dt><strong>MIDL2410</strong></dt> </dl></td>
<td><dl> <dt><span id="internal_compiler_inconsistency_detected__the_format_string_offset_is_invalid._See_the_documentation_for_more_information."></span><span id="internal_compiler_inconsistency_detected__the_format_string_offset_is_invalid._see_the_documentation_for_more_information."></span><span id="INTERNAL_COMPILER_INCONSISTENCY_DETECTED__THE_FORMAT_STRING_OFFSET_IS_INVALID._SEE_THE_DOCUMENTATION_FOR_MORE_INFORMATION."></span>обнаружена несогласованность внутреннего компилятора: недопустимое смещение строки формата. Дополнительные сведения см. в документации.</dt> <dd> Компилятор MIDL обнаружил недопустимое значение во внутренних структурах данных. Это может быть вызвано рекурсивными структурами или компилятором, нарушая собственные ограничения представления внутренних данных. Чтобы выявление и/или обойти проблему, попробуйте упростить IDL-файл. Это можно сделать, упростите сложные параметры и рекурсивные структуры данных или сделав IDL-файл меньше, разделив его. Это сообщение может сопровождаться распечаткой диагностических сведений с дополнительными сведениями о проблеме.<br/> Если вы видите эту ошибку, сообщите об ошибке в корпорацию Майкрософт. Укажите файлы IDL, файлы ACF, полную командную строку MIDL и диагностические данные, если они есть.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2411"></span><span id="midl2411"></span><dl> <dt><strong>MIDL2411</strong></dt> </dl></td>
<td><dl> <dt><span id="internal_compiler_inconsistency_detected__the_type_offset_is_invalid._See_the_documentation_for_more_information."></span><span id="internal_compiler_inconsistency_detected__the_type_offset_is_invalid._see_the_documentation_for_more_information."></span><span id="INTERNAL_COMPILER_INCONSISTENCY_DETECTED__THE_TYPE_OFFSET_IS_INVALID._SEE_THE_DOCUMENTATION_FOR_MORE_INFORMATION."></span>обнаружена несогласованность внутреннего компилятора: недопустимое смещение типа. Дополнительные сведения см. в документации.</dt> <dd> Компилятор MIDL обнаружил недопустимое значение во внутренних структурах данных. Это может быть вызвано рекурсивными структурами или компилятором, нарушая собственные ограничения представления внутренних данных. Чтобы выявление и/или обойти проблему, попробуйте упростить IDL-файл. Это можно сделать, упростите сложные параметры и рекурсивные структуры данных либо сделав IDL-файл меньше, разделив его. Это сообщение может сопровождаться распечаткой диагностических сведений с дополнительными сведениями о проблеме.<br/> Если вы видите эту ошибку, сообщите об ошибке в корпорацию Майкрософт. Укажите файлы IDL, файлы ACF, полную командную строку MIDL и диагностические данные, если они есть.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2412"></span><span id="midl2412"></span><dl> <dt><strong>MIDL2412</strong></dt> </dl></td>
<td><dl> <dt><span id="SAFEARRAY_roo__syntax_is_not_supported_outside_of_the_library_block__use_LPSAFEARRAY_for_proxy"></span><span id="safearray_roo__syntax_is_not_supported_outside_of_the_library_block__use_lpsafearray_for_proxy"></span><span id="SAFEARRAY_ROO__SYNTAX_IS_NOT_SUPPORTED_OUTSIDE_OF_THE_LIBRARY_BLOCK__USE_LPSAFEARRAY_FOR_PROXY"></span>Синтаксис SAFEARRAY (Ру) не поддерживается вне блока библиотеки, используйте ЛПСАФЕАРРАЙ для прокси-сервера.</dt> <dd> Явно типизированные SAFEARRAY не разрешены вне блока библиотеки. Вместо этого используйте ЛПСАФЕАРРАЙ.<br/> В следующем примере показана эта ошибка:<br/>
<pre class="syntax" data-space="preserve"><code>void roo(SAFEARRAY(long) *a); //MIDL2412 when outside a library block
void roo(LPSAFEAEEAY a);         //OK</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2413"></span><span id="midl2413"></span><dl> <dt><strong>MIDL2413</strong></dt> </dl></td>
<td><dl> <dt><span id="bit_fields_are_not_supported"></span><span id="BIT_FIELDS_ARE_NOT_SUPPORTED"></span>битовые поля не поддерживаются</dt> <dd> Битовые поля в стиле C не поддерживаются MIDL. Это относится к созданию прокси-сервера, а также к формированию TLB.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2414"></span><span id="midl2414"></span><dl> <dt><strong>MIDL2414</strong></dt> </dl></td>
<td><dl> <dt><span id="floating_point_or_complex_return_types_with__decode__are_not_supported_in_-Oicf__using_-OI"></span><span id="floating_point_or_complex_return_types_with__decode__are_not_supported_in_-oicf__using_-oi"></span><span id="FLOATING_POINT_OR_COMPLEX_RETURN_TYPES_WITH__DECODE__ARE_NOT_SUPPORTED_IN_-OICF__USING_-OI"></span>типы возвращаемых значений с плавающей запятой или сложные значения с [декодированием] не поддерживаются в параметре-Оикф с помощью-OI</dt> <dd> Процедуры с типами возвращаемых значений с плавающей запятой или структурой и объединением не поддерживаются в списке выбора стиля Оикф. Решение для 32-разрядной версии — использовать режим оптимизации-Oi при сериализации данных (с помощью [Encoded] и/или [дешифровки]). тем не менее, так как поддержка интерпретатора стилей old-Oi и поддержки выбора выводятся после выпуска Windows 2000, использование указателей настоятельно рекомендуется в качестве решения для этой проблемы. Также обратите внимание, что, как правило, изменение метода интерфейса для использования указателя [out, ref] вместо возвращаемого значения приводит к тому, что проблема полностью совместима на канале и может быть легко скрыта от уровня приложения. <br/> Это предупреждение можно отключить глобально, указав-Oi в командной строке MIDL или для отдельной функции, добавив атрибут [optimize ( &quot; i &quot; )] к функции в файле ACF.<br/> В следующем примере показана эта ошибка:<br/> ру. IDL: <br/>
<pre class="syntax" data-space="preserve"><code>double GetDouble();</code></pre>
ру. ACF: <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
Одним из вариантов обойти это ограничение является передача параметра [out] для хранения результата вместо использования возвращаемого значения:<br/> ру. IDL: <br/>
<pre class="syntax" data-space="preserve"><code>void GetDouble([out] double *result); //top level pointer is a [ref] pointer</code></pre>
ру. ACF: <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
Как упоминалось ранее, описанное выше решение хорошо подходит не только для новых интерфейсов, но и для решения старых задач. Представление для нового &quot; выходного &quot; аргумента будет таким же, как и для возвращаемого значения (в качестве нового возвращаемого значения Обратите внимание на void).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2415"></span><span id="midl2415"></span><dl> <dt><strong>MIDL2415</strong></dt> </dl></td>
<td><dl> <dt><span id="the_return_type_is_not_supported_for_64-bit_when_using__decode_"></span><span id="THE_RETURN_TYPE_IS_NOT_SUPPORTED_FOR_64-BIT_WHEN_USING__DECODE_"></span>Тип возвращаемого значения не поддерживается для 64-bit при использовании [расшифровки]</dt> <dd> Процедуры с типами возвращаемых значений с плавающей запятой или структурой и объединением не поддерживаются в 64-разрядном режиме при выполнении сериализации данных (с использованием [ <a href="encode.md"><strong>Encoded</strong></a>] и/или [ <a href="decode.md"><strong>дешифровки</strong></a>]). Это связано со старым интерпретатором типа-Oi и сериализатором данных, который не поддерживается на 64-разрядной платформе. Дополнительные сведения см. в описании MIDL2414. <br/> В следующем примере показана эта ошибка:<br/> ру. IDL: <br/>
<pre class="syntax" data-space="preserve"><code>double GetDouble();</code></pre>
ру. ACF: <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
Ниже мы рекомендуем обойтись как для новых, так и для старых интерфейсов. Используйте параметр [out] для хранения результата вместо использования возвращаемого значения:<br/> ру. IDL: <br/>
<pre class="syntax" data-space="preserve"><code>void GetDouble([out] double *result); //top level pointer is a [ref] pointer.</code></pre>
ру. ACF: <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
Обратите внимание, что это решение полностью обратно совместимо по каналу, так как одноранговые представления указателя [ref, out] или Double совпадают с типом данных Double.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2416"></span><span id="midl2416"></span><dl> <dt><strong>MIDL2416</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_type_may_not_contain_a_full_pointer_for_either__wire_marshal__or__user_marshal_"></span><span id="TRANSMITTED_TYPE_MAY_NOT_CONTAIN_A_FULL_POINTER_FOR_EITHER__WIRE_MARSHAL__OR__USER_MARSHAL_"></span>передаваемый тип не может содержать полный указатель для [wire_marshal] или [user_marshal]</dt> <dd> Типы с атрибутами [ <a href="wire-marshal.md"><strong>wire_marshal</strong></a>] или [ <a href="user-marshal.md"><strong>user_marshal</strong></a>] не могут содержать указатели Full ([ <strong>ptr</strong>]). Используйте вместо него [ <a href="unique.md"><strong>UNIQUE</strong></a>] или [ <a href="ref.md"><strong>ref</strong></a>].<br/> В следующем примере показана эта ошибка:<br/>
<pre class="syntax" data-space="preserve"><code>typedef struct
{
    [ptr] long *a;    //Should use [ref] or [unique] instead
}
st1;
typedef [wire_marshal(st1)] struct
{
    long a;
}
st2:
void roo(st2 *s);    //MIDL2416</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2417"></span><span id="midl2417"></span><dl> <dt><strong>MIDL2417</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_type_must_either_be_a_pointer_or_have_a_constant_size_for__wire_marshal__and__user_marshal_"></span><span id="TRANSMITTED_TYPE_MUST_EITHER_BE_A_POINTER_OR_HAVE_A_CONSTANT_SIZE_FOR__WIRE_MARSHAL__AND__USER_MARSHAL_"></span>передаваемый тип должен быть либо указателем, либо иметь постоянный размер для [wire_marshal] и [user_marshal]</dt> <dd> Типы верхнего уровня с атрибутами [ <a href="wire-marshal.md"><strong>wire_marshal</strong></a>] или [ <a href="user-marshal.md"><strong>user_marshal</strong></a>] должны иметь четко определенный размер во время компиляции. Они не могут быть или содержать согласованные или изменяемые массивы.<br/> В следующем примере показана эта ошибка:<br/>
<pre class="syntax" data-space="preserve"><code>typedef struct        //Type contains variable-sized array
{
    long s;
    [size_is(s)] char a[];
}
st1;
typedef [wire_marshal(st1)] struct
{
    long a;
}
st2;
void roo(st2 *s);        //MIDL2417</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2418"></span><span id="midl2418"></span><dl> <dt><strong>MIDL2418</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with__propget__must_have_at_least_one_parameter_or_a_return_value"></span><span id="PROCEDURES_WITH__PROPGET__MUST_HAVE_AT_LEAST_ONE_PARAMETER_OR_A_RETURN_VALUE"></span>процедуры с [propget] должны иметь хотя бы один параметр или возвращаемое значение.</dt> <dd> Процедуры с атрибутом [propget] должны иметь некоторые средства для возвращения значения свойства. Они должны иметь по меньшей мере один параметр [<a href="-out.md"><strong>out</strong></a>] или возвращаемое значение.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2461"></span><span id="midl2461"></span><dl> <dt><strong>MIDL2461</strong></dt> </dl></td>
<td><dl> <dt><span id="The__readonly__attribute_was_applied_at_the_method_level."></span><span id="the__readonly__attribute_was_applied_at_the_method_level."></span><span id="THE__READONLY__ATTRIBUTE_WAS_APPLIED_AT_THE_METHOD_LEVEL."></span>Атрибут [ReadOnly] был применен на уровне метода.</dt> <dd> Атрибут [ReadOnly] может применяться только на уровне параметров.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2465"></span><span id="midl2465"></span><dl> <dt><strong>MIDL2465</strong></dt> </dl></td>
<td><dl> <dt><span id="Structures_containing_conformant_arrays_must_be_passed_by_reference"></span><span id="structures_containing_conformant_arrays_must_be_passed_by_reference"></span><span id="STRUCTURES_CONTAINING_CONFORMANT_ARRAYS_MUST_BE_PASSED_BY_REFERENCE"></span>Структуры, содержащие согласованные массивы, должны передаваться по ссылке</dt> <dd> Параметры верхнего уровня в RPC должны иметь четко определенный размер во время компиляции. Они не могут быть, а также иметь несоответствующий или неизменяемый массив. Кроме того, пользователи не могут кодировать или декодировать тип без четко определенного размера. Приложения должны передавать согласованную структуру или согласованность структуры по ссылке.<br/> В следующем примере показана эта ошибка:<br/>
<pre class="syntax" data-space="preserve"><code>typedef struct        //Type contains variable-sized array
{
    long s;
    [size_is(s)] char a[];
}
st1;
void roo(st1 s);        //MIDL2465
 
on .acf file
typedef [encode,decode] st1; //MIDL2465</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL9008"></span><span id="midl9008"></span><dl> <dt><strong>MIDL9008</strong></dt> </dl></td>
<td><dl> <dt><span id="_internal_compiler_problem__system_error_code__-_the_compiler_cannot_continue_for_an_unknown_reason._See_documentation_for_a_workaround."></span><span id="_internal_compiler_problem__system_error_code__-_the_compiler_cannot_continue_for_an_unknown_reason._see_documentation_for_a_workaround."></span><span id="_INTERNAL_COMPILER_PROBLEM__SYSTEM_ERROR_CODE__-_THE_COMPILER_CANNOT_CONTINUE_FOR_AN_UNKNOWN_REASON._SEE_DOCUMENTATION_FOR_A_WORKAROUND."></span> внутренняя проблема компилятора <system error code> - . компилятор не может продолжить работу по неизвестной причине. Дополнительные сведения см. в документации.</dt> <dd> Компилятору не удалось продолжить работу, и причина ошибки неизвестна. Шестнадцатеричный номер ошибки — это идентификатор системной ошибки. Компиляция может быть неудачной из-за внешней проблемы, например нехватки памяти. В этом случае дополнительные сведения можно найти в файле Winerror. h или NTSTATUS. h. <br/> Эта ошибка обычно возникает в двух ситуациях:<br/>
<ul>
<li>Не удалось восстановить компилятор MIDL после обнаружения ошибки в IDL-файле. Если MIDL возвращает сообщения об ошибках для IDL-файла, попробуйте исправить их и выполнить повторную компиляцию. Если сообщения об ошибках отсутствуют, возможно, произошел сбой компилятора, прежде чем он может сообщить об ошибке. Найдите синтаксическую ошибку в строке, для которой сообщается о внутренней ошибке компилятора.</li>
<li>Компилятору MIDL не удалось создать правильный код при указанном параметре оптимизации. Попробуйте изменить режимы компилятора, компиляцию в смешанном режиме (в<a href="-os.md"><strong>ОС</strong></a>) или удалить все оптимизации. Или выполните повторную компиляцию с помощью флага/NO_FORMAT_OPT, чтобы отключить оптимизацию процедур и дескрипторов типов по умолчанию MIDL.</li>
</ul>
Иногда эта ошибка возникает, даже если IDL-файл указан правильно и параметры оптимизации не используются. В этом случае попробуйте переписать раздел кода в окружении, где была обнаружена ошибка, удалив последние изменения, упростить или изменить типы данных, изменение прототипов или начать закомментировать фрагменты IDL-файла, чтобы определить код проблемы.<br/> Если ни один из этих вариантов не работает или если вы считаете, что проблема может быть связана с ошибкой в Midl.exe, сообщите Майкрософт, предоставив все необходимые сведения.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

