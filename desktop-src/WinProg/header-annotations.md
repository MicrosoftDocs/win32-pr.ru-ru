---
title: Заметки заголовка
description: Заметки заголовков описывают, как функция использует свои параметры и возвращаемое значение.
ms.assetid: 4f9e42b1-2fe4-4173-946e-ab1805a96b9e
keywords:
- Windows API, заметки файла заголовка
- заметки файла заголовка
- Спекстрингс. h
- язык Standard annotation (SAL)
- _bcount
- _deref
- _deref_opt
- _ecount
- _full
- _in
- _inout
- _opt
- _out
- _part
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12ad560d00c45714d0feaa9ab2fa58ff4c985730fd563d4943ff028f561f2793
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643634"
---
# <a name="header-annotations"></a>Заметки заголовка

\[в этом разделе описываются аннотации, поддерживаемые в заголовках Windows в Windows 7. при разработке для Windows 8 следует использовать аннотации, описанные в [аннотациях SAL]( /previous-versions/visualstudio/visual-studio-2013/ms182032(v=vs.120)).\]

Заметки заголовков описывают, как функция использует свои параметры и возвращаемое значение. эти заметки были добавлены во многие файлы заголовков Windows, чтобы обеспечить правильное обращение к Windows API. если включить анализ кода, который доступен, начиная с Visual Studio 2005, компилятор выдаст предупреждения уровня 6000, если вы не вызываете эти функции в течение использования, описанного в заметках. Можно также добавить эти заметки в собственный код, чтобы убедиться, что они вызываются правильно. сведения о включении анализа кода в Visual Studio см. в документации по используемой версии Visual Studio.

Эти заметки определены в Спекстрингс. h. Они основаны на примитивах, которые являются частью стандартного языка аннотации (SAL) и реализованы с помощью `_declspec("SAL_*")` .

Существует два класса заметок: заметки буфера и дополнительные заметки.

## <a name="buffer-annotations"></a>Заметки буфера

Заметки буфера описывают, как функции используют свои указатели и могут использоваться для обнаружения переполнений буфера. Каждый параметр может использовать ноль или одну заметку буфера. Заметка буфера создается с помощью подчеркивания в начале и компонентов, описанных в следующих разделах.



| Размер буфера                                                                                  | Описание                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_size_"></span><span id="_SIZE_"></span>(*Размер*)<br/>                        | Задает общий размер буфера. Используйте с \_ бкаунт и \_ екаунт; не используйте с \_ компонентом Part. Это значение представляет собой доступное пространство; оно может быть меньше выделенного пространства.<br/> |
| <span id="_size_length_"></span><span id="_SIZE_LENGTH_"></span>(*Размер*,*Длина*)<br/> | Задает общий размер и инициализированную длину буфера. Используйте с \_ бкаунт \_ частью и \_ \_ частью екаунт. Общий размер может быть меньше выделенного пространства.<br/>              |



 



| Единицы размера буфера                                                       | Описание                                |
|-------------------------------------------------------------------------|--------------------------------------------|
| <span id="_bcount"></span><span id="_BCOUNT"></span>\_бкаунт<br/> | Размер буфера в байтах.<br/>    |
| <span id="_ecount"></span><span id="_ECOUNT"></span>\_екаунт<br/> | Размер буфера находится в элементах.<br/> |



 



| Направление                                                            | Описание                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_in"></span><span id="_IN"></span>\_окне<br/>          | Функция считывает данные из буфера. Вызывающий объект предоставляет буфер и инициализирует его.<br/>                                                                                                                          |
| <span id="_inout"></span><span id="_INOUT"></span>\_Inout<br/> | Функция выполняет чтение из буфера и запись в буфер. Вызывающий объект предоставляет буфер и инициализирует его. При использовании с \_ DEREF буфер может быть повторно выделен функцией.<br/>                                      |
| <span id="_out"></span><span id="_OUT"></span>\_заполняет<br/>       | Функция записывает данные в буфер. Если используется в возвращаемом значении или с параметром \_ DEREF, функция предоставляет буфер и инициализирует ее. В противном случае вызывающий объект предоставляет буфер, а функция инициализирует его.<br/> |



 



| Косвенное обращение                                                                       | Описание                                                                                            |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="_deref"></span><span id="_DEREF"></span>\_Deref<br/>              | Чтобы получить указатель на буфер, необходимо выполнить разыменование параметра. Этот параметр не может иметь **значение NULL**.<br/> |
| <span id="_deref_opt"></span><span id="_DEREF_OPT"></span>\_Deref \_ OPT<br/> | Чтобы получить указатель на буфер, необходимо выполнить разыменование параметра. Этот параметр может принимать значение **NULL**.<br/>     |



 



| Инициализация                                                    | Описание                                                                                                              |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span id="_full"></span><span id="_FULL"></span>\_полный<br/> | Функция инициализирует весь буфер. Используйте только с выходными буферами.<br/>                                     |
| <span id="_part"></span><span id="_PART"></span>\_блок<br/> | Функция инициализирует часть буфера и явно указывает, сколько. Используйте только с выходными буферами.<br/> |



 



| Обязательный или необязательный буфер                                    | Описание                                |
|----------------------------------------------------------------|--------------------------------------------|
| <span id="_opt"></span> <span id="_OPT"></span> \_необ.<br/> | Этот параметр может принимать значение **NULL**.<br/> |



 

В следующем примере показаны аннотации для функции **GetModuleFileName** . Параметр *хмодуле* является необязательным входным параметром. Параметр *лпфиленаме* является выходным параметром. его размер в символах задается параметром *нсизе* , а его длина включает символ, завершающийся **нулем**. Параметр *нсизе* является входным параметром.


```C++
DWORD
WINAPI
GetModuleFileName(
    __in_opt HMODULE hModule,
    __out_ecount_part(nSize, return + 1) LPTSTR lpFilename,
    __in DWORD nSize
    );
```



Ниже приведены аннотации, определенные в Спекстрингс. h. Используйте сведения в приведенных выше таблицах, чтобы интерпретировать их значения.

__bcount (*Размер*)  
__bcount_opt (*Размер*)  
__deref_bcount (*Размер*)  
__deref_bcount_opt (*Размер*)  
__deref_ecount (*Размер*)  
__deref_ecount_opt (*Размер*)  
__deref_in  
__deref_in_bcount (*Размер*)  
__deref_in_bcount_opt (*Размер*)  
__deref_in_ecount (*Размер*)  
__deref_in_ecount_opt (*Размер*)  
__deref_in_opt  
__deref_inout  
__deref_inout_bcount (*Размер*)  
__deref_inout_bcount_full (*Размер*)  
__deref_inout_bcount_full_opt (*Размер*)  
__deref_inout_bcount_opt (*Размер*)  
__deref_inout_bcount_part (*Размер*,*Длина*)  
__deref_inout_bcount_part_opt (*Размер*,*Длина*)  
__deref_inout_ecount (*Размер*)  
__deref_inout_ecount_full (*Размер*)  
__deref_inout_ecount_full_opt (*Размер*)  
__deref_inout_ecount_opt (*Размер*)  
__deref_inout_ecount_part (*Размер*,*Длина*)  
__deref_inout_ecount_part_opt (*Размер*,*Длина*)  
__deref_inout_opt  
__deref_opt_bcount (*Размер*)  
__deref_opt_bcount_opt (*Размер*)  
__deref_opt_ecount (*Размер*)  
__deref_opt_ecount_opt (*Размер*)  
__deref_opt_in  
__deref_opt_in_bcount (*Размер*)  
__deref_opt_in_bcount_opt (*Размер*)  
__deref_opt_in_ecount (*Размер*)  
__deref_opt_in_ecount_opt (*Размер*)  
__deref_opt_in_opt  
__deref_opt_inout  
__deref_opt_inout_bcount (*Размер*)  
__deref_opt_inout_bcount_full (*Размер*)  
__deref_opt_inout_bcount_full_opt (*Размер*)  
__deref_opt_inout_bcount_opt (*Размер*)  
__deref_opt_inout_bcount_part (*Размер*,*Длина*)  
__deref_opt_inout_bcount_part_opt (*Размер*,*Длина*)  
__deref_opt_inout_ecount (*Размер*)  
__deref_opt_inout_ecount_full (*Размер*)  
__deref_opt_inout_ecount_full_opt (*Размер*)  
__deref_opt_inout_ecount_opt (*Размер*)  
__deref_opt_inout_ecount_part (*Размер*,*Длина*)  
__deref_opt_inout_ecount_part_opt (*Размер*,*Длина*)  
__deref_opt_inout_opt  
__deref_opt_out  
__deref_opt_out_bcount (*Размер*)  
__deref_opt_out_bcount_full (*Размер*)  
__deref_opt_out_bcount_full_opt (*Размер*)  
__deref_opt_out_bcount_opt (*Размер*)  
__deref_opt_out_bcount_part (*Размер*,*Длина*)  
__deref_opt_out_bcount_part_opt (*Размер*,*Длина*)  
__deref_opt_out_ecount (*Размер*)  
__deref_opt_out_ecount_full (*Размер*)  
__deref_opt_out_ecount_full_opt (*Размер*)  
__deref_opt_out_ecount_opt (*Размер*)  
__deref_opt_out_ecount_part (*Размер*,*Длина*)  
__deref_opt_out_ecount_part_opt (*Размер*,*Длина*)  
__deref_opt_out_opt  
__deref_out  
__deref_out_bcount (*Размер*)  
__deref_out_bcount_full (*Размер*)  
__deref_out_bcount_full_opt (*Размер*)  
__deref_out_bcount_opt (*Размер*)  
__deref_out_bcount_part (*Размер*,*Длина*)  
__deref_out_bcount_part_opt (*Размер*,*Длина*)  
__deref_out_ecount (*Размер*)  
__deref_out_ecount_full (*Размер*)  
__deref_out_ecount_full_opt (*Размер*)  
__deref_out_ecount_opt (*Размер*)  
__deref_out_ecount_part (*Размер*,*Длина*)  
__deref_out_ecount_part_opt (*Размер*,*Длина*)  
__deref_out_opt  
__ecount (*Размер*)  
__ecount_opt (*Размер*)  
__in  
__in_bcount (*Размер*)  
__in_bcount_opt (*Размер*)  
__in_ecount (*Размер*)  
__in_ecount_opt (*Размер*)  
__in_opt  
__inout  
__inout_bcount (*Размер*)  
__inout_bcount_full (*Размер*)  
__inout_bcount_full_opt (*Размер*)  
__inout_bcount_opt (*Размер*)  
__inout_bcount_part (*Размер*,*Длина*)  
__inout_bcount_part_opt (*Размер*,*Длина*)  
__inout_ecount (*Размер*)  
__inout_ecount_full (*Размер*)  
__inout_ecount_full_opt (*Размер*)  
__inout_ecount_opt (*Размер*)  
__inout_ecount_part (*Размер*,*Длина*)  
__inout_ecount_part_opt (*Размер*,*Длина*)  
__inout_opt  
__out  
__out_bcount (*Размер*)  
__out_bcount_full (*Размер*)  
__out_bcount_full_opt (*Размер*)  
__out_bcount_opt (*Размер*)  
__out_bcount_part (*Размер*,*Длина*)  
__out_bcount_part_opt (*Размер*,*Длина*)  
__out_ecount (*Размер*)  
__out_ecount_full (*Размер*)  
__out_ecount_full_opt (*Размер*)  
__out_ecount_opt (*Размер*)  
__out_ecount_part (*Размер*,*Длина*)  
__out_ecount_part_opt (*Размер*,*Длина*)  
__out_opt  

## <a name="advanced-annotations"></a>Дополнительные заметки

Дополнительные заметки содержат дополнительные сведения о параметре или возвращаемом значении. Каждый параметр или возвращаемое значение могут использовать одну или несколько дополнительных аннотаций.



| Annotation                                                                                                                                               | Описание                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="__blocksOn_resource_"></span><span id="__blockson_resource_"></span><span id="__BLOCKSON_RESOURCE_"></span>\_\_Блокксон (*ресурс*)<br/> | Функции блокируют указанный ресурс.<br/>                                                                                                                                                                                                                      |
| <span id="__callback"></span><span id="__CALLBACK"></span>\_\_обратного вызова<br/>                                                                        | Функцию можно использовать в качестве указателя функции.<br/>                                                                                                                                                                                                                      |
| <span id="__checkReturn"></span><span id="__checkreturn"></span><span id="__CHECKRETURN"></span>\_\_Аннотация checkReturn применяется<br/>                               | Вызывающие объекты должны проверить возвращаемое значение.<br/>                                                                                                                                                                                                                                 |
| <span id="__format_string"></span><span id="__FORMAT_STRING"></span>\_\_\_строка формата<br/>                                                        | Параметр представляет собой строку, содержащую маркеры типа "printf-Style%".<br/>                                                                                                                                                                                                      |
| <span id="__in_awcount_expr_size_"></span><span id="__IN_AWCOUNT_EXPR_SIZE_"></span>\_\_в \_ авкаунт (*expr*,*size*)<br/>                            | Если выражение имеет значение true при выходе, то размер входного буфера указывается в байтах. Если выражение имеет значение false, то размер задается в элементах.<br/>                                                                                                                |
| <span id="__nullnullterminated"></span><span id="__NULLNULLTERMINATED"></span>\_\_нуллнуллтерминатед<br/>                                          | Доступ к буферу можно получить, добавив в него первую последовательность из двух **пустых** символов или указателей.<br/>                                                                                                                                                            |
| <span id="__nullterminated"></span><span id="__NULLTERMINATED"></span>\_\_NullTerminated<br/>                                                      | Доступ к буферу можно получить, добавив в него первый символ или указатель **null** .<br/>                                                                                                                                                                              |
| <span id="__out_awcount_expr_size_"></span><span id="__OUT_AWCOUNT_EXPR_SIZE_"></span>\_\_out \_ авкаунт (*выражение*,*Размер*)<br/>                         | Если выражение имеет значение true при выходе, размер выходного буфера указывается в байтах. Если выражение имеет значение false, то размер задается в элементах. <br/>                                                                                                              |
| <span id="__override"></span><span id="__OVERRIDE"></span>\_\_крывают<br/>                                                                        | Задает поведение переопределения в стиле C# для виртуальных методов.<br/>                                                                                                                                                                                                           |
| <span id="__reserved"></span><span id="__RESERVED"></span>\_\_процессу<br/>                                                                        | Параметр зарезервирован для будущего использования и должен быть равен нулю или иметь **значение NULL**.<br/>                                                                                                                                                                                               |
| <span id="__success_expr_"></span><span id="__SUCCESS_EXPR_"></span>\_\_успешное завершение (*expr*)<br/>                                                       | Если выражение имеет значение true при выходе, вызывающий объект может полагаться на все гарантии, заданные другими заметками. Если выражение имеет значение false, вызывающий объект не может полагаться на гарантии. Эта заметка автоматически добавляется к функциям, которые возвращают значение **HRESULT** .<br/> |
| <span id="__typefix_ctype_"></span><span id="__TYPEFIX_CTYPE_"></span>\_\_typefix (*CType*)<br/>                                                    | Рассматривайте параметр как указанный тип, а не его объявленный тип.<br/>                                                                                                                                                                                             |



 

В следующих примерах показаны буфер и дополнительные заметки для функций [**DeleteTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer), [**фриенвиронментстрингс**](/windows/desktop/api/processenv/nf-processenv-freeenvironmentstringsa)и [**UnhandledExceptionFilter**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter) .


```C++
__checkReturn
BOOL
WINAPI
DeleteTimerQueueTimer(
    __in_opt HANDLE TimerQueue,
    __in     HANDLE Timer,
    __in_opt HANDLE CompletionEvent
    );

BOOL
WINAPI
FreeEnvironmentStrings(
    __in __nullnullterminated LPTCH
    );

__callback
LONG
WINAPI
UnhandledExceptionFilter(
    __in struct _EXCEPTION_POINTERS *ExceptionInfo
    );

```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Аннотации SAL](/cpp/c-runtime-library/sal-annotations?view=vs-2019)
</dt> <dt>

[Пошаговое руководство. Проверка кода C/C++ на наличие дефектов](/visualstudio/code-quality/walkthrough-analyzing-c-cpp-code-for-defects?view=vs-2015)
</dt> </dl>

 

