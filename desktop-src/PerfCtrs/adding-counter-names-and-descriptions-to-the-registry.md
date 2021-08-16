---
description: Имена и описания всех объектов производительности и их счетчиков хранятся в реестре.
ms.assetid: 6fdaccb0-45bc-48f2-8f63-3df0bdf1dca4
title: Добавление в реестр имен и описаний счетчиков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e58333e9694b9aa74ff1d5ade6a399aaa813e7735ea315be529587e813fec0fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117794059"
---
# <a name="adding-counter-names-and-descriptions-to-the-registry"></a>Добавление в реестр имен и описаний счетчиков

> [!IMPORTANT]
> Из-за существенных ограничений производительности и надежности метод предоставления данных счетчиков производительности, описанных в этом разделе, может быть изменен или недоступен в будущем. Вместо этого корпорация Майкрософт рекомендует использовать метод, описанный в разделе [предоставление данных счетчиков с помощью версии 2,0](providing-counter-data-using-version-2-0.md) для создания новых счетчиков производительности и переноса существующих счетчиков производительности для использования этого метода.

Имена и описания всех объектов производительности v1 и их счетчиков должны быть установлены в системе. Чтобы сохранить имена и описания объектов и счетчиков из [поставщика v1](providing-counter-data.md), выполните следующие действия.

- [Создайте h-файл заголовка](#creating-a-symbolic-constants-h-file) , содержащий символьные константы для смещения объектов и счетчиков.
- [Создайте файл инициализации (.INI)](#creating-an-initialization-ini-file) , содержащий строки.
- При установке компонента [запустите средство **lodctr**](#running-the-lodctr-tool) , чтобы установить имена и описания в реестр.
- При удалении компонента запустите средство lodctr, чтобы удалить имена и описания из реестра.

## <a name="creating-a-symbolic-constants-h-file"></a>Создание файла символьных констант (. h)

Создайте h-файл заголовка, который определяет константы (макросы) для смещения объектов и счетчиков, предоставляемых поставщиком. Заголовок. h используется в качестве входных данных для программы **lodctr** во время установки поставщика, а также может использоваться кодом C/C++ поставщика.

Постоянные значения должны быть последовательными, даже числами, начинающимися с нуля. Сгруппируйте константы по объектам (т. е. запустите каждую группу с смещением объекта, затем следуйте смещениям счетчиков для этого объекта).

Константы в заголовке определяют порядок, в котором счетчики добавляются к имени и тексту справки в реестре. Поставщик использует смещения, чтобы определить, какой объект запрашивается, и значения индекса, используемые при возврате данных. Дополнительные сведения см. в разделе [Реализация опенперформанцедата](implementing-openperformancedata.md).

Ниже приведен пример символьного файла константы с именем Каунтероффсетс. h, который используется в примере [создания библиотеки DLL расширения производительности](creating-a-performance-extension-dll.md) .

```C++
#ifndef OFFSETS_H
#define OFFSETS_H

// Symbol file that defines constant values for the objects
// and counters that the provider provides. The counters should be
// grouped by object.

#define TRANSFER_OBJECT      0 // First object must be at offset 0.
#define BYTES_SENT           2 // Counters for the object follow.
#define AVAILABLE_BANDWIDTH  4 // Offsets must be even numbers.

// Not required, but for convenience in implementing the Open function:
#define LAST_TRANSFER_OBJECT_COUNTER_OFFSET  AVAILABLE_BANDWIDTH

#define PEER_OBJECT          6 // Second object must be at the next offset.
#define BYTES_SERVED         8 // Counter for the second object.

// Not required, but for convenience in implementing the Open function:
#define LAST_PEER_OBJECT_COUNTER_OFFSET  BYTES_SERVED

#endif // OFFSETS_H
```

## <a name="creating-an-initialization-ini-file"></a>Создание файла инициализации (.INI)

Файл инициализации (.INI) содержит имя и строки справки для каждого объекта и счетчика, определенные в файле символов. Файл .INI используется в качестве входных данных для **lodctr** во время установки поставщика.

Файл .INI должен быть закодирован как UTF-16LE (с меткой порядка байтов) и должен иметь следующие разделы и ключи:

```ini
[info]
drivername=ServiceKeyName
symbolfile=SymbolFile.h
trusted=(Unused)

[objects]
<symbol>_<langid>_NAME=(Unused)

[languages]
<langid>=(Unused)

[text]
<symbol>_<langid>_NAME=Name
<symbol>_<langid>_HELP=Description
```

### <a name="info-section"></a>раздел [info]

В `[info]` разделе содержатся общие сведения о поставщике. Ключи раздела определяются следующим образом.

|Ключ|Описание
|---|-----------
|**Имя_драйвера**| Укажите имя ключа производительности поставщика, расположенного в реестре раздела `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` . Сведения о создании этого ключа см. в разделе [Создание ключа производительности приложения](creating-the-applications-performance-key.md).
|**симболфиле**| Укажите файл заголовка. h, содержащий символьные значения объектов и счетчиков поставщика. Во время установки (при вызове **lodctr**) файл заголовка должен находиться в том же каталоге, что и файл .INI.
|**Доверитель**| Если включить этот ключ в `[info]` раздел, **lodctr** добавит в ключ производительности значение реестра кода проверки библиотеки с двоичной подписью библиотеки DLL производительности. Когда библиотека PERFLIB вызывает библиотеку DLL, она сравнивает подпись с библиотекой DLL, чтобы определить, была ли изменена библиотека DLL. Значение **доверенного** ключа игнорируется.

`DriverName`Ключи и `SymbolFile` являются обязательными.

### <a name="objects-section"></a>[Objects], раздел

В `[objects]` разделе содержится список объектов производительности, поддерживаемых поставщиком. Используется для определения того, относится ли каждый символ из `[text]` раздела к объекту или счетчику.

Для каждого объекта (CounterSet), поддерживаемого поставщиком, добавьте один ключ с именем `<symbol>_<langid>_NAME=` в `[objects]` раздел, где `<symbol>` — это имя объекта, а `<langid>` — идентификатор языка одного из поддерживаемых языков. Значение игнорируется.

> [!IMPORTANT]
> `[objects]`Раздел улучшает производительность системы. Хотя раздел «объекты» является необязательным, всегда следует включать этот раздел в файл .INI. Если включить этот раздел, то библиотека DLL производительности будет вызываться только в том случае, если вы поддерживаете запрошенный объект. Если раздел «объекты» не включен, то библиотека DLL вызывается для каждого запроса, так как система не знает, какие объекты поддерживает поставщик. Если раздел объекта не включен, **lodctr** создает в журнале событий приложений сообщение о том, что .INI файл не содержит секцию объектов. Идентификатор события этого сообщения — 2000.

### <a name="languages-section"></a>[языки], раздел

`[languages]`Раздел содержит список идентификаторов языков для каждого языка, для которого поставщик предоставляет имена и строки справки. Все поставщики должны поддерживать `009` (английский).

Для каждого поддерживаемого языка добавьте один ключ с именем `<langid>=` . Значение не учитывается, но в целях документации значение обычно устанавливается в соответствии с именем соответствующего языка, например `009=English` .

Для большинства языков следует использовать основной идентификатор языка. Полный список идентификаторов языков находится в файле заголовка WinNT. h под заголовком «Основные идентификаторы языка». Преобразовать значение, найденное в Winnt. h, в последовательность из 3 шестнадцатеричных цифр, удалив `0x` префикс и добавив начальные `0` цифры, пока последовательность не сойдет из 3 цифр. Например, чтобы указать строки на английском языке (0x9), используйте 009. Чтобы указать итальянские строки (0x10), используйте 010.

Для китайского и португальского языков требуются идентификаторы основного и подязыкового языка. Используйте 404, 804, 416 или 816 вместо 004 или 016.

### <a name="text-section"></a>раздел [текст]

`[text]`Раздел содержит имя и строки справки для объектов и счетчиков.

Для каждого объекта или счетчика, а также для каждого поддерживаемого языка необходимо указать ключ имени (содержащий имя или строку заголовка для объекта или счетчика), а также ввести ключ справки (содержащий описание или строку описания для объекта или счетчика). Ключи должны иметь имена `<symbol>_<langid>_NAME` и `<symbol>_<langid>_HELP` , где `<symbol>` — символьная константа для объекта или счетчика (как определено в символьном файле Constant. h), а `<langid>` — идентификатор языка, используемый для этой строки.

Например, строки на английском языке для счетчика с символом будут `MY_COUNTER` указаны следующим образом:

```ini
MY_COUNTER_009_NAME=My Counter
MY_COUNTER_009_HELP=Description for My Counter.
```

Текстовые ключи могут отображаться в любом порядке. Текстовые строки не должны содержать символы форматирования, например символы табуляции.

### <a name="example-ini-file"></a>Пример INI-файла

Ниже приведен пример файла инициализации, который используется в примере [создания библиотеки DLL расширения производительности](creating-a-performance-extension-dll.md) .

```ini
[info]
drivername=MyApplication
symbolfile=CounterOffsets.h
trusted=

[objects]
TRANSFER_OBJECT_009_NAME=
PEER_OBJECT_009_NAME=

[languages]
009=English
00C=French

[text]

// English strings

TRANSFER_OBJECT_009_NAME=Transfer
TRANSFER_OBJECT_009_HELP=Provides information related to transferring files.

BYTES_SENT_009_NAME=Bytes Sent
BYTES_SENT_009_HELP=Number of bytes sent in the last transfer.

AVAILABLE_BANDWIDTH_009_NAME=Available Bandwidth
AVAILABLE_BANDWIDTH_009_HELP=Available bandwidth on the network, in bytes.

PEER_OBJECT_009_NAME=Peer
PEER_OBJECT_009_HELP=Provides information related to peer-caching.

BYTES_SERVED_009_NAME=Bytes Served
BYTES_SERVED_009_HELP=Number of bytes served from the cache.

// French strings

TRANSFER_OBJECT_00C_NAME=Transfert
TRANSFER_OBJECT_00C_HELP=Fournit des informations liées aux transferts de fichiers.

BYTES_SENT_00C_NAME=Octets Envoyés
BYTES_SENT_00C_HELP=Nombre d'octets envoyés dans le dernier transfert.

AVAILABLE_BANDWIDTH_00C_NAME=Bande Passante Disponible
AVAILABLE_BANDWIDTH_00C_HELP=Bande passante disponible sur le réseau, en octets.

PEER_OBJECT_00C_NAME=Pair
PEER_OBJECT_00C_HELP=Fournit des informations liées é mise en cache homologue.

BYTES_SERVED_00C_NAME=Octets Servis
BYTES_SERVED_00C_HELP=Le nombre d'octets servis du cache.
```

## <a name="running-the-lodctr-tool"></a>Запуск средства lodctr

Чтобы загрузить имена и строки справки, определенные в файле .INI (во время установки поставщика), запустите средство **lodctr** из папки, содержащей файл .INI и файл заголовка. Средство входит в состав компьютера. Необходимо запустить **lodctr** с повышенными привилегиями. Параметр для **lodctr** — это путь к файлу .INI. Например, `lodctr "C:\Program Files\MyCompany\MyProvider\MyProvider.ini"`.

Чтобы выгрузить имена и строки справки (во время удаления), запустите средство **lodctr** . Необходимо запустить **lodctr** с повышенными привилегиями. Параметр для **lodctr** — это имя_драйвера поставщика (имя ключа производительности поставщика). Например, `unlodctr "MyProvider"`.

Перед запуском **lodctr** убедитесь, что в приложении есть запись в разделе " **службы** ". Дополнительные сведения см. [в разделе Создание ключа производительности приложения](creating-the-applications-performance-key.md). Если раздел не существует, **lodctr** не будет обновлять реестр с именами и описаниями.

В качестве альтернативы запуску **lodctr** можно вызвать [**лоадперфкаунтертекстстрингс**](/windows/win32/api/loadperf/nf-loadperf-loadperfcountertextstringsw) (определенную в LoadPerf. h) из программы установки, чтобы загрузить описания имен счетчиков. Затем можно вызвать [**унлоадперфкаунтертекстстрингс**](/windows/win32/api/loadperf/nf-loadperf-unloadperfcountertextstringsw) во время удаления.

Служебная программа **lodctr** копирует строки из файла .INI в **счетчики** и значения реестра **справки** в соответствующих подразделах языка. Если соответствующий языковой ключ не существует, строки для этого языка не копируются. Программа также обновляет **последний счетчик** и Последнее значение **справки** . Имена и описания счетчиков производительности хранятся в следующем расположении в реестре.

```
HKEY_LOCAL_MACHINE
   \SOFTWARE
      \Microsoft
         \Windows NT
            \CurrentVersion
               \Perflib
                  Last Counter = highest counter index
                  Last Help = highest help index
                  \009
                     Counters = 2 System 4 Memory...
                     Help = 3 The System Object Type...
                  \supported language, other than English
                     Counters = ...
                     Help = ...
```

Помимо добавления значений в раздел **PerfLib** , средство **lodctr** также добавляет следующие значения в узел **службы** для приложения. В большинстве случаев приложение и поставщик будут иметь связь «один к одному». Однако поставщик может предоставлять данные счетчиков для нескольких приложений, поэтому ключ основан на приложении, а не на поставщике.

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \MyApplication
               \Performance
                  First Counter = lowest counter index assigned to provider
                  First Help = lowest help index assigned to provider
                  Last Counter = highest counter index assigned to provider
                  Last Help = highest help index assigned to provider
                  Object List = list of object index values if the .INI includes the [objects] section
                  Library Validation Code = if the [info] section contains a "trusted" key
```
