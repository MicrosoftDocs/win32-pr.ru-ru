---
description: Каждый источник событий должен регистрировать файлы сообщений, содержащие строки описания для каждого идентификатора события, категории событий и параметра.
ms.assetid: 0c251a45-1414-4855-a6f5-86ebdfab2693
title: Файлы сообщений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44de0c91a098ab1b916a73d99a02d0d31a8b5b7690936322166e65baef4bd13c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951413"
---
# <a name="message-files"></a>Файлы сообщений

Каждый [источник событий](event-sources.md) должен регистрировать файлы сообщений, содержащие строки описания для каждого [идентификатора события](event-identifiers.md), [категории событий](event-categories.md)и [параметра](event-identifiers.md). Зарегистрируйте эти файлы в значениях реестра **евентмессажефиле**, **категоримессажефиле** и **параметермессажефиле** для источника события.

Можно создать один файл сообщения, содержащий описания идентификаторов событий, категорий и параметров, либо создать три отдельных файла сообщений. Идентификаторы сообщений для всех сообщений должны быть уникальными, независимо от того, указываются ли сообщения в одном файле или трех файлах. Несколько приложений могут совместно использовать один и тот же файл сообщения. Дополнительные сведения о файлах сообщений см. в разделе [**компилятор сообщений**](/windows/desktop/WES/message-compiler--mc-exe-). Дополнительные сведения о синтаксисе файла сообщений см. в разделе [текстовые файлы сообщений](message-text-files.md).

## <a name="example-message-file"></a>Пример файла сообщения

Ниже приведен пример файла сообщения.

``` syntax
; /* --------------------------------------------------------
; HEADER SECTION
;*/
SeverityNames=(Success=0x0:STATUS_SEVERITY_SUCCESS
               Informational=0x1:STATUS_SEVERITY_INFORMATIONAL
               Warning=0x2:STATUS_SEVERITY_WARNING
               Error=0x3:STATUS_SEVERITY_ERROR
              )
;
;
FacilityNames=(System=0x0:FACILITY_SYSTEM
               Runtime=0x2:FACILITY_RUNTIME
               Stubs=0x3:FACILITY_STUBS
               Io=0x4:FACILITY_IO_ERROR_CODE
              )
;
;/* ------------------------------------------------------------------
; MESSAGE DEFINITION SECTION
;*/

MessageIdTypedef=WORD

MessageId=0x1
SymbolicName=CAT_1
Language=English
Category 1
.

MessageId=0x2
SymbolicName=CAT_2
Language=English
Category 2
.

MessageId=0x3
SymbolicName=CAT_3
Language=English
Category 3
.

MessageIdTypedef=DWORD

MessageId=0x100
Severity=Error
Facility=Runtime
SymbolicName=MSG_COMMAND_ERR
Language=English
The command is incorrect. 
.

MessageId=0x101
Severity=Success
Facility=System
SymbolicName=MSG_STRIKE_ANY_KEY
Language=English
Press any key to continue . . . %0
.

MessageId=0x102
Severity=Error
Facility=System
SymbolicName=MSG_FILE_BAD_CONTENTS
Language=English
File %1 contains %2, which is in error
.

MessageId=0x103
Severity=Warning
Facility=System
SymbolicName=MSG_RETRYS
Language=English
There have been %1 retrys with %2 success! Disconnect from
the server and retry later.
.

MessageId=0x104
Severity=Informational
Facility=System
SymbolicName=MSG_INSERT_DISK
Language=English
Insert %%1000 in %%1001 and hit any key when ready... 
.

;/* Insert string parameters */
;

MessageId=1000
Severity=Success
Facility=System
SymbolicName=DISK
Language=English
disk%0
.

MessageId=1001
Severity=Success
Facility=System
SymbolicName=DRIVE
Language=English
drive%0
.
```

Приложение просмотра событий может использовать следующую процедуру для получения доступа к [строкам сообщений](event-identifiers.md) в библиотеке DLL сообщения.

**Получение строк описания**

1.  Вызовите функцию [**регопенкэй**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) , чтобы открыть источник события.
2.  Вызовите функцию [**процедура RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) , чтобы получить содержимое значения **евентмессажефиле** для источника события, которое представляет собой имя библиотеки DLL сообщения.
3.  Вызовите функцию [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) , чтобы загрузить библиотеку DLL сообщений, определенную на шаге 2.
4.  Вызовите функцию [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) с идентификатором сообщения, чтобы получить описание из библиотеки DLL. (Обратите внимание, что идентификаторы сообщений определены в. H-файл, созданный компилятором сообщений.) Функция **FormatMessage** заменит строки вставки, используя передаваемые значения аргументов, но не заменит строки вставки параметров. перед отображением строки необходимо заменить строки вставки параметров.

 

 
