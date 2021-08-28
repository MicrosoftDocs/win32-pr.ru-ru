---
title: Использование BITS из .NET с помощью ссылок на библиотеки DLL
description: В следующих примерах показано, как вызывать интерфейс COM BITS из программы .NET.
ms.assetid: 1058970C-CE81-47D6-950E-3B6289E956B6
ms.topic: article
ms.date: 11/13/2018
ms.openlocfilehash: 00f7d6287d86dd1816d7e4b0a7c6e18c9ae4916c5c85b01d0280758cf9d00b5b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529154"
---
# <a name="calling-into-bits-from-net-and-c-using-reference-dlls"></a>Вызов битов из .NET и C# с помощью справочника DLL

одним из способов вызова классов COM bits из программы .net является создание ссылочного файла DLL, начиная с файлов [IDL](/windows/desktop/Midl/midl-start-page) (язык определения интерфейса) в Windows SDK с помощью средств [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) и [TLBIMP](/dotnet/framework/tools/tlbimp-exe-type-library-importer) . Библиотека ссылок — это набор оболочек классов для классов COM BITS. Затем можно использовать классы-оболочки непосредственно из .NET.

альтернативой использованию автоматически создаваемых ссылок на библиотеки dll является использование сторонней сторонней оболочки .net разрядов от [GitHub](https://github.com/) и [NuGet](https://www.nuget.org/). Эти оболочки часто имеют более естественный стиль программирования .NET, но могут отставать от изменений и обновлений в интерфейсах BITS.

## <a name="creating-the-reference-dlls"></a>Создание ссылок на библиотеки DLL
### <a name="bits-idl-files"></a>IDL-файлы BITS

Вы начнете с набора IDL-файлов BITS. Это файлы, полностью определяющие COM-интерфейс BITS. файлы находятся в каталоге **Windows kit** и имеют имя bits. idl (например, bits10_2. idl), за исключением *файла версии 1,0*, который просто является bits. idl. По мере создания новых версий BITS также создаются новые файлы IDL для битов.

Также может потребоваться изменить копию IDL-файлов пакета SDK, чтобы использовать функции BITS, которые не преобразуются автоматически в эквиваленты .NET. Возможные изменения IDL-файлов обсуждаются далее в.

Файлы IDL в БИТАХ содержат несколько других IDL-файлов по ссылке. Они также вложены, поэтому при использовании одной версии она включает в себя все более ранние версии.

Для каждой версии BITS, которую необходимо нацелить в программе, потребуется одна ссылка на библиотеку DLL для этой версии. Например, если вы хотите написать программу, которая работает в БИТАХ 1,5 и выше, но имеет дополнительные функции при наличии службы BITS 10,2, необходимо преобразовать файлы bits1_5. idl и bits10_2. idl.


### <a name="midl-and-tlbimp-utilities"></a>MIDL и служебные программы TLBIMP

Программа [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) (язык MIDL) ПРЕОБРАЗУЕТ IDL-файлы, описывающие интерфейс COM BITS, в файл TLB (библиотеки типов). Средство MIDL зависит от программы CL (препроцессора C) для правильного чтения файла языка IDL. программа CL является частью Visual Studio и устанавливается при включении функций C/C++ в установку Visual Studio.

Программа MIDL, как правило, создает набор файлов C и H (код языка C и язык C). Эти дополнительные файлы можно отключить, отправив выходные данные на устройство NUL:. Например, при настройке параметра/dlldata NUL: будет отключено создание файла DLLDATA. c. В приведенных ниже примерах команд показано, какие параметры должны иметь значение NUL:.

Программа [Tlbimp](/dotnet/framework/tools/tlbimp-exe-type-library-importer) (средство импорта библиотек типов) СЧИТЫВАЕТ файл TLB и создает соответствующий справочный файл DLL. 


### <a name="example-commands-for-midl-and-tlbimp"></a>Примеры команд для MIDL и TLBIMP

Это пример полного набора команд для создания набора справочных файлов. возможно, вам потребуется изменить команды на основе Visual Studio и Windows SDK установки и в зависимости от того, какие функции BITS и целевые версии ос вы используете. 

В примере создается каталог для размещения ссылок на DLL-файлы и создается переменная среды БИТСТЕМП, указывающая на этот каталог. 

затем команды запускают файл vsdevcmd.bat, созданный установщиком Visual Studio. В этом файле BAT будут настроены пути и некоторые переменные среды, чтобы выполнялись команды MIDL и TLBIMP. он также настраивает переменные виндовссдкдир и виндовссдклибверсион, чтобы они указывали на самые последние Windows SDK каталоги.

```console
REM Create a working directory
REM You can select a different directory based on your needs.
SET BITSTEMP=C:\BITSTEMPDIR
MKDIR "%BITSTEMP%"

REM Run the VsDevCmd.bat file to locate the Windows
REM SDK directory and the tools directories
REM This will be different for different versions of
REM Visual Studio

CALL "C:\Program Files (x86)\Microsoft Visual Studio\2017\Enterprise\Common7\Tools\vsdevcmd.bat"

REM Run the MIDL command on the desired BITS IDL file
REM This will generate a TLB file for the TLBIMP command
REM The IDL file will be different depending on which
REM set of BITS interfaces you need to use.
REM Run the MIDL command once per reference file
REM that you will need to explicitly use.
PUSHD .
CD /D "%WindowsSdkDir%Include\%WindowsSDKLibVersion%um"

MIDL  /I ..\shared /out "%BITSTEMP%" bits1_5.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits4_0.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits5_0.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits10_1.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits10_2.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:

REM Run the TLBIMP command on the resulting TLB file(s)
REM Try to keep a parallel set of names.
TLBIMP "%BITSTEMP%"\bits1_5.tlb /out: "%BITSTEMP%"\BITSReference1_5.dll
TLBIMP "%BITSTEMP%"\bits4_0.tlb /out: "%BITSTEMP%"\BITSReference4_0.dll
TLBIMP "%BITSTEMP%"\bits5_0.tlb /out: "%BITSTEMP%"\BITSReference5_0.dll
TLBIMP "%BITSTEMP%"\bits10_1.tlb /out: "%BITSTEMP%"\BITSReference10_1.dll
TLBIMP "%BITSTEMP%"\bits10_2.tlb /out: "%BITSTEMP%"\BITSReference10_2.dll
DEL "%BITSTEMP%"\bits*.tlb
POPD

```
После выполнения этих команд у вас будет набор справочных библиотек DLL в каталоге БИТСТЕМП.

### <a name="adding-the-reference-dlls-to-your-project"></a>Добавление ссылочных библиотек DLL в проект

Чтобы использовать ссылочную библиотеку DLL в проекте C#, откройте проект C# в Visual Studio. В обозреватель решений щелкните правой кнопкой мыши ссылки и выберите команду Добавить ссылку. Затем нажмите кнопку обзора, а затем кнопку Добавить. Перейдите в каталог со ссылками на библиотеки DLL, выберите их и нажмите кнопку Добавить. В окне диспетчера ссылок будут проверены ссылочные библиотеки DLL. Затем нажмите кнопку ОК.

Библиотеки DLL ссылок на BITS теперь добавляются в проект.

Информация в файлах DLL ссылок будет внедрена в окончательную программу. Вам не нужно поставлять файлы DLL ссылок в вашу программу; Вам нужно просто поставлять .EXE. 

Можно изменить, внедряются ли ссылочные библиотеки DLL в окончательный исполняемый файл. Используйте свойство [Внедрить типы взаимодействия](/dotnet/framework/interop/how-to-add-references-to-type-libraries) , чтобы задать, будут ли внедрены ссылочные библиотеки DLL. Это можно сделать на основе каждой ссылки. Значение по умолчанию — true для внедрения библиотек DLL.

## <a name="modifying-idl-files-for-more-complete-net-code"></a>Изменение IDL-файлов для более полного кода .NET

Файлы IDL (язык MIDL) BITS можно использовать без изменений, чтобы сделать DLL-файл Баккграундкопиманажер. Однако результирующая DLL-библиотека .NET не будет содержать некоторые непреобразованные объединения и имеет трудные имена для некоторых структур и перечислений. В этом разделе описаны некоторые изменения, которые можно сделать, чтобы сделать библиотеку DLL .NET более полной и удобной для использования.

### <a name="simpler-enum-names"></a>Более простые имена перечислений

IDL-файлы BITS обычно определяют перечисляемые значения следующим образом:
```
    typedef enum
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```
BG_AUTH_TARGET — имя определения типа; фактическое перечисление не называется. Обычно это не вызывает проблем с кодом C, но не подходит для использования с программой .NET. Новое имя будет создано автоматически, но оно может выглядеть так, как _MIDL___MIDL_itf_bits4_0_0005_0001_0001, а не как удобное для восприятия значение. Эту проблему можно устранить, обновив файлы MIDL, включив в них имя перечисления.

```
    typedef enum BG_AUTH_TARGET
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```

Имя перечисления может совпадать с именем typedef. Некоторые программисты имеют соглашение об именовании, где они различаются (например, при вводе символа подчеркивания перед именем перечисления), но это будет путать только переводы .NET. 

### <a name="string-types-in-unions"></a>Строковые типы в объединениях

Файлы IDL-файлов BITS передают строки с помощью LPWSTR (длинный указатель на строку расширенных символов). Хотя это работает при передаче параметров функции (например, метод Job. Pval ([out] LPWSTR *)), он не работает, если строки являются частью объединения. Например, файл bits5_0. idl включает в себя BITS_FILE_PROPERTY_VALUEное объединение:

```
typedef [switch_type(BITS_FILE_PROPERTY_ID)] union
{
    [case( BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS )]
        LPWSTR String;
}
BITS_FILE_PROPERTY_VALUE;
```

Поле LPWSTR не будет включаться в версию .NET объединения. Чтобы устранить эту проблему, измените параметр LPWSTR на WCHAR *. Итоговое поле (называемое строкой) будет передано как IntPtr. Преобразуйте его в строку, используя System. Runtime. InteropServices. Marshal. Птртострингауто (значение. Строка); Method.

### <a name="unions-in-structures"></a>Объединения в структурах

Иногда объединения, внедренные в структуры, не будут включены в структуру. Например, в Bits1_5. idl BG_AUTH_CREDENTIALS определяется следующим образом:
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        [switch_is(Scheme)] BG_AUTH_CREDENTIALS_UNION Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

BG_AUTH_CREDENTIALS_UNION определяется как объединение следующим образом:
```
    typedef [switch_type(BG_AUTH_SCHEME)] union
    {
            [case( BG_AUTH_SCHEME_BASIC, BG_AUTH_SCHEME_DIGEST, BG_AUTH_SCHEME_NTLM,
            BG_AUTH_SCHEME_NEGOTIATE, BG_AUTH_SCHEME_PASSPORT )] BG_BASIC_CREDENTIALS Basic;
            [default] ;
    } BG_AUTH_CREDENTIALS_UNION;
```
Поле учетные данные в BG_AUTH_CREDENTIALS не будет включаться в определение класса .NET.

Обратите внимание, что UNION определяется так, чтобы всегда быть BG_BASIC_CREDENTIALS независимо от BG_AUTH_SCHEME. Поскольку объединение не используется в качестве объединения, можно просто передать BG_BASIC_CREDENTIALS следующим образом:
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        BG_BASIC_CREDENTIALS Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

## <a name="using-bits-from-c"></a>Использование битов из C #

### <a name="recommended-using-statement"></a>Рекомендуемая инструкция using

Настройка некоторых инструкций using в C# сокращает количество символов, которые необходимо ввести для использования различных версий BITS. Имя "Битсреференце" берется из имени справочной библиотеки DLL.

```csharp
// Set up the BITS namespaces
using BITS = BITSReference1_5;
using BITS4 = BITSReference4_0;
using BITS5 = BITSReference5_0;
using BITS10_2 = BITSReference10_2;
```

### <a name="quick-sample-download-a-file"></a>Краткий пример: скачивание файла

Ниже приведен короткий, но полный фрагмент кода C# для загрузки файла из URL-адреса. 

```csharp
    var mgr = new BITS.BackgroundCopyManager1_5();
    BITS.GUID jobGuid;
    BITS.IBackgroundCopyJob job;
    mgr.CreateJob("Quick download", BITS.BG_JOB_TYPE.BG_JOB_TYPE_DOWNLOAD, out jobGuid, out job);
    job.AddFile("https://aka.ms/WinServ16/StndPDF", @"C:\Server2016.pdf");
    job.Resume();
    bool jobIsFinal = false;
    while (!jobIsFinal)
    {
        BITS.BG_JOB_STATE state;
        job.GetState(out state);
        switch (state)
        {
            case BITS.BG_JOB_STATE.BG_JOB_STATE_ERROR:
            case BITS.BG_JOB_STATE.BG_JOB_STATE_TRANSFERRED:
                job.Complete();
                break;

            case BITS.BG_JOB_STATE.BG_JOB_STATE_CANCELLED:
            case BITS.BG_JOB_STATE.BG_JOB_STATE_ACKNOWLEDGED:
                jobIsFinal = true;
                break;
            default:
                Task.Delay(500); // delay a little bit
                break;
        }
    }
    // Job is complete
```

В этом примере кода создается диспетчер BITS с именем диспетчера. Он непосредственно соответствует интерфейсу [ибаккграундкопиманажер](/windows/desktop/api/bits/nn-bits-ibackgroundcopymanager) . 

В диспетчере создается новое задание. Задание является выходным параметром метода CreateJob. Кроме того, передано имя задания (которое не обязательно должно быть уникальным) и тип загрузки, который является заданием скачивания. Также заполняется идентификатор GUID BITS для идентификатора задания.

После создания задания добавьте новый файл загрузки в задание с помощью метода AddFile. Необходимо передать две строки: одну для удаленного файла (URL-адрес или общую папку), а другой — для локального файла. 

После добавления файла вызовите для задания команду Resume, чтобы запустить его. Затем код ждет, пока задание находится в конечном состоянии (ошибка или передано), а затем завершается.

### <a name="bits-versions-casting-and-queryinterface"></a>Версии BITS, приведение и QueryInterface

Вы обнаружите, что часто приходится использовать как раннюю версию объекта BITS, так и более позднюю версию в программе.  

Например, при создании объекта задания вы получите использованием метода ibackgroundcopyjob (часть версии BITS 1,0), даже если вы делаете это с помощью более свежего объекта Manager и доступен более новый объект использованием метода ibackgroundcopyjob. Поскольку метод CreateJob не принимает интерфейс для более новой версии, вы не можете напрямую сделать более свежую версию.

Используйте приведение к .NET для преобразования старого объекта типа в более новый объект типа. Приведение будет автоматически вызывать QueryInterface COM, как нужно. 

В этом примере имеется объект BITS использованием метода ibackgroundcopyjob с именем Job, и мы хотим преобразовать его в объект IBackgroundCopyJob5 с именем «job5», чтобы мы могли вызвать метод-свойство BITS 5,0. Мы просто приведен к типу IBackgroundCopyJob5 следующим образом:

```csharp
var job5 = (BITS5.IBackgroundCopyJob5)job;
```

Переменная job5 будет инициализирована .NET с помощью правильного QueryInterface. 

Если код может выполняться в системе, которая не поддерживает определенную версию BITS, можно попробовать выполнить приведение и перехватить System. InvalidCastException. 

```csharp
BITS5.IBackgroundCopyJob5 job5 = null;
try
{
    job5 = (BITS5.IBackgroundCopyJob5)Job;
}
catch (System.InvalidCastException)
{
    ; // Must be running an earlier version of BITS
}
```

Распространенной проблемой является попытка привести к неправильному виду объекта. Система .NET не знает о реальной связи между интерфейсами BITS. Если запрашивается неправильный тип интерфейса, .NET попытается сделать его для вас и завершится ошибкой InvalidCastException и HResult 0x80004002 (E_NOINTERFACE).

### <a name="working-with-bits-versions-10_1-and-10_2"></a>Работа с версиями BITS 10_1 и 10_2

в некоторых версиях Windows 10 нельзя напрямую создать объект BITS ибаккграундкопиманажер с помощью интерфейсов 10,1 или 10,2. Вместо этого необходимо использовать несколько версий справочных файлов DLL Баккграундкопиманажер. Например, можно использовать версию 1,5 для создания объекта Ибаккграундкопиманажер, а затем привести результирующее задание или объекты файлов с помощью версий 10,1 или 10,2.

