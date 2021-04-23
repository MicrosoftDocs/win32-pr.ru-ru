---
description: Каждый источник событий должен регистрировать файлы сообщений, содержащие строки описания для каждого идентификатора события, категории событий и параметра.
ms.assetid: 0c251a45-1414-4855-a6f5-86ebdfab2693
title: Файлы сообщений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb20d5919c75f06bfd7b6db9b47216566ab6ac8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545018"
---
# <a name="message-files"></a><span data-ttu-id="850c6-103">Файлы сообщений</span><span class="sxs-lookup"><span data-stu-id="850c6-103">Message Files</span></span>

<span data-ttu-id="850c6-104">Каждый [источник событий](event-sources.md) должен регистрировать файлы сообщений, содержащие строки описания для каждого [идентификатора события](event-identifiers.md), [категории событий](event-categories.md)и [параметра](event-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="850c6-104">Each [event source](event-sources.md) should register message files that contain description strings for each [event identifier](event-identifiers.md), [event category](event-categories.md), and [parameter](event-identifiers.md).</span></span> <span data-ttu-id="850c6-105">Зарегистрируйте эти файлы в значениях реестра **евентмессажефиле**, **категоримессажефиле** и **параметермессажефиле** для источника события.</span><span class="sxs-lookup"><span data-stu-id="850c6-105">Register these files in the **EventMessageFile**, **CategoryMessageFile**, and **ParameterMessageFile** registry values for the event source.</span></span>

<span data-ttu-id="850c6-106">Можно создать один файл сообщения, содержащий описания идентификаторов событий, категорий и параметров, либо создать три отдельных файла сообщений.</span><span class="sxs-lookup"><span data-stu-id="850c6-106">You can create one message file that contains descriptions for the event identifiers, categories, and parameters, or create three separate message files.</span></span> <span data-ttu-id="850c6-107">Идентификаторы сообщений для всех сообщений должны быть уникальными, независимо от того, указываются ли сообщения в одном файле или трех файлах.</span><span class="sxs-lookup"><span data-stu-id="850c6-107">The message identifiers for all of your messages should be unique whether you specify the messages in one file or three files.</span></span> <span data-ttu-id="850c6-108">Несколько приложений могут совместно использовать один и тот же файл сообщения.</span><span class="sxs-lookup"><span data-stu-id="850c6-108">Several applications can share the same message file.</span></span> <span data-ttu-id="850c6-109">Дополнительные сведения о файлах сообщений см. в разделе [**компилятор сообщений**](/windows/desktop/WES/message-compiler--mc-exe-).</span><span class="sxs-lookup"><span data-stu-id="850c6-109">For more information on message files, see [**Message Compiler**](/windows/desktop/WES/message-compiler--mc-exe-).</span></span> <span data-ttu-id="850c6-110">Дополнительные сведения о синтаксисе файла сообщений см. в разделе [текстовые файлы сообщений](message-text-files.md).</span><span class="sxs-lookup"><span data-stu-id="850c6-110">For details on the syntax of a message file, see [Message Text Files](message-text-files.md).</span></span>

## <a name="example-message-file"></a><span data-ttu-id="850c6-111">Пример файла сообщения</span><span class="sxs-lookup"><span data-stu-id="850c6-111">Example Message File</span></span>

<span data-ttu-id="850c6-112">Ниже приведен пример файла сообщения.</span><span class="sxs-lookup"><span data-stu-id="850c6-112">The following is an example message file.</span></span>

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

<span data-ttu-id="850c6-113">Приложение просмотра событий может использовать следующую процедуру для получения доступа к [строкам сообщений](event-identifiers.md) в библиотеке DLL сообщения.</span><span class="sxs-lookup"><span data-stu-id="850c6-113">The event-viewing application can use the following procedure to gain access to the [message strings](event-identifiers.md) in the message DLL.</span></span>

<span data-ttu-id="850c6-114">**Получение строк описания**</span><span class="sxs-lookup"><span data-stu-id="850c6-114">**To obtain description strings**</span></span>

1.  <span data-ttu-id="850c6-115">Вызовите функцию [**регопенкэй**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) , чтобы открыть источник события.</span><span class="sxs-lookup"><span data-stu-id="850c6-115">Call the [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) function to open the event source.</span></span>
2.  <span data-ttu-id="850c6-116">Вызовите функцию [**процедура RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) , чтобы получить содержимое значения **евентмессажефиле** для источника события, которое представляет собой имя библиотеки DLL сообщения.</span><span class="sxs-lookup"><span data-stu-id="850c6-116">Call the [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) function to obtain the contents of the **EventMessageFile** value for the event source, which is the name of the message DLL.</span></span>
3.  <span data-ttu-id="850c6-117">Вызовите функцию [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) , чтобы загрузить библиотеку DLL сообщений, определенную на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="850c6-117">Call the [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) function to load the message DLL determined by step 2.</span></span>
4.  <span data-ttu-id="850c6-118">Вызовите функцию [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) с идентификатором сообщения, чтобы получить описание из библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="850c6-118">Call the [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) function with the message identifier to obtain the description from the DLL.</span></span> <span data-ttu-id="850c6-119">(Обратите внимание, что идентификаторы сообщений определены в. H-файл, созданный компилятором сообщений.) Функция **FormatMessage** заменит строки вставки, используя передаваемые значения аргументов, но не заменит строки вставки параметров. перед отображением строки необходимо заменить строки вставки параметров.</span><span class="sxs-lookup"><span data-stu-id="850c6-119">(Note that the messages identifiers are defined in the .H file generated by the message compiler.) The **FormatMessage** function will replace the insertion strings using the argument values that you pass but it will not replace the parameter insertion strings; you must replace the parameter insertion strings yourself before displaying the string.</span></span>

 

 
