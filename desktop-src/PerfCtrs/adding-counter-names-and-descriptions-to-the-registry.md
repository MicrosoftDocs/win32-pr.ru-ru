---
description: Имена и описания всех объектов производительности и их счетчиков хранятся в реестре.
ms.assetid: 6fdaccb0-45bc-48f2-8f63-3df0bdf1dca4
title: Добавление в реестр имен и описаний счетчиков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e9d2c97ebe80a8ef2a8396ca42583cbad874859
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663258"
---
# <a name="adding-counter-names-and-descriptions-to-the-registry"></a><span data-ttu-id="20f26-103">Добавление в реестр имен и описаний счетчиков</span><span class="sxs-lookup"><span data-stu-id="20f26-103">Adding Counter Names and Descriptions to the Registry</span></span>

> [!IMPORTANT]
> <span data-ttu-id="20f26-104">Из-за существенных ограничений производительности и надежности метод предоставления данных счетчиков производительности, описанных в этом разделе, может быть изменен или недоступен в будущем.</span><span class="sxs-lookup"><span data-stu-id="20f26-104">Due to significant performance and reliability limitations, the method for providing performance counter data that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="20f26-105">Вместо этого корпорация Майкрософт рекомендует использовать метод, описанный в разделе [предоставление данных счетчиков с помощью версии 2,0](providing-counter-data-using-version-2-0.md) для создания новых счетчиков производительности и переноса существующих счетчиков производительности для использования этого метода.</span><span class="sxs-lookup"><span data-stu-id="20f26-105">Instead, Microsoft recommends that you use the method described in [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md) for creating new performance counters and that you migrate existing performance counters to use that method.</span></span>

<span data-ttu-id="20f26-106">Имена и описания всех объектов производительности v1 и их счетчиков должны быть установлены в системе.</span><span class="sxs-lookup"><span data-stu-id="20f26-106">The names and descriptions of all V1 performance objects and their counters must be installed the system.</span></span> <span data-ttu-id="20f26-107">Чтобы сохранить имена и описания объектов и счетчиков из [поставщика v1](providing-counter-data.md), выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="20f26-107">To store names and descriptions for the objects and counters from your [V1 provider](providing-counter-data.md):</span></span>

- <span data-ttu-id="20f26-108">[Создайте h-файл заголовка](#creating-a-symbolic-constants-h-file) , содержащий символьные константы для смещения объектов и счетчиков.</span><span class="sxs-lookup"><span data-stu-id="20f26-108">[Create a .h header file](#creating-a-symbolic-constants-h-file) that contains the symbolic constants for the offsets to your objects and counters.</span></span>
- <span data-ttu-id="20f26-109">[Создайте инициализацию (. INI-файл)](#creating-an-initialization-ini-file) , содержащий строки.</span><span class="sxs-lookup"><span data-stu-id="20f26-109">[Create an initialization (.INI) file](#creating-an-initialization-ini-file) that contains the strings.</span></span>
- <span data-ttu-id="20f26-110">При установке компонента [запустите средство **lodctr**](#running-the-lodctr-tool) , чтобы установить имена и описания в реестр.</span><span class="sxs-lookup"><span data-stu-id="20f26-110">When installing your component, [run the **lodctr** tool](#running-the-lodctr-tool) to install the names and descriptions into the registry.</span></span>
- <span data-ttu-id="20f26-111">При удалении компонента запустите средство lodctr, чтобы удалить имена и описания из реестра.</span><span class="sxs-lookup"><span data-stu-id="20f26-111">When uninstalling your component, run the unlodctr tool to remove the names and descriptions from the registry.</span></span>

## <a name="creating-a-symbolic-constants-h-file"></a><span data-ttu-id="20f26-112">Создание файла символьных констант (. h)</span><span class="sxs-lookup"><span data-stu-id="20f26-112">Creating a symbolic constants (.h) file</span></span>

<span data-ttu-id="20f26-113">Создайте h-файл заголовка, который определяет константы (макросы) для смещения объектов и счетчиков, предоставляемых поставщиком.</span><span class="sxs-lookup"><span data-stu-id="20f26-113">Create a .h header file that defines constants (macros) for the offsets to the objects and counters that your provider provides.</span></span> <span data-ttu-id="20f26-114">Заголовок. h используется в качестве входных данных для программы **lodctr** во время установки поставщика, а также может использоваться кодом C/C++ поставщика.</span><span class="sxs-lookup"><span data-stu-id="20f26-114">The .h header is used as input to **lodctr** during installation of your provider, and may also be used by the C/C++ code of your provider.</span></span>

<span data-ttu-id="20f26-115">Постоянные значения должны быть последовательными, даже числами, начинающимися с нуля.</span><span class="sxs-lookup"><span data-stu-id="20f26-115">The constant values must be consecutive, even numbers beginning with zero.</span></span> <span data-ttu-id="20f26-116">Сгруппируйте константы по объектам (т. е. запустите каждую группу с смещением объекта, затем следуйте смещениям счетчиков для этого объекта).</span><span class="sxs-lookup"><span data-stu-id="20f26-116">Group the constants by objects (i.e. start each group with the object offset, then follow with the offsets of the counters for that object).</span></span>

<span data-ttu-id="20f26-117">Константы в заголовке определяют порядок, в котором счетчики добавляются к имени и тексту справки в реестре.</span><span class="sxs-lookup"><span data-stu-id="20f26-117">The constants in the header determine the order in which the counters are added to the name and help text in the registry.</span></span> <span data-ttu-id="20f26-118">Поставщик использует смещения, чтобы определить, какой объект запрашивается, и значения индекса, используемые при возврате данных.</span><span class="sxs-lookup"><span data-stu-id="20f26-118">The provider uses the offsets to determine which object is being queried and the index values to use when returning the data.</span></span> <span data-ttu-id="20f26-119">Дополнительные сведения см. в разделе [Реализация опенперформанцедата](implementing-openperformancedata.md).</span><span class="sxs-lookup"><span data-stu-id="20f26-119">For details, see [Implementing OpenPerformanceData](implementing-openperformancedata.md).</span></span>

<span data-ttu-id="20f26-120">Ниже приведен пример символьного файла константы с именем Каунтероффсетс. h, который используется в примере [создания библиотеки DLL расширения производительности](creating-a-performance-extension-dll.md) .</span><span class="sxs-lookup"><span data-stu-id="20f26-120">The following shows an example of a symbolic constant file, named CounterOffsets.h, that is used in the [Creating a Performance Extension DLL](creating-a-performance-extension-dll.md) example.</span></span>

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

## <a name="creating-an-initialization-ini-file"></a><span data-ttu-id="20f26-121">Создание инициализации (. INI-файл)</span><span class="sxs-lookup"><span data-stu-id="20f26-121">Creating an initialization (.INI) file</span></span>

<span data-ttu-id="20f26-122">Инициализация (. INI) содержит имя и строки справки для каждого объекта и счетчика, определенные в файле символов.</span><span class="sxs-lookup"><span data-stu-id="20f26-122">The initialization (.INI) file contains the name and help strings for each object and counter defined in your symbol file.</span></span> <span data-ttu-id="20f26-123">Тот. INI-файл используется в качестве входных данных для **lodctr** во время установки поставщика.</span><span class="sxs-lookup"><span data-stu-id="20f26-123">The .INI file is used as input to **lodctr** during installation of your provider.</span></span>

<span data-ttu-id="20f26-124">Тот. Файл INI должен быть закодирован как UTF-16LE (с меткой порядка следования байтов) и содержать следующие разделы и ключи:</span><span class="sxs-lookup"><span data-stu-id="20f26-124">The .INI file should be encoded as UTF-16LE (with byte order mark) and should have the following sections and keys:</span></span>

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

### <a name="info-section"></a><span data-ttu-id="20f26-125">раздел [info]</span><span class="sxs-lookup"><span data-stu-id="20f26-125">[info] section</span></span>

<span data-ttu-id="20f26-126">В `[info]` разделе содержатся общие сведения о поставщике.</span><span class="sxs-lookup"><span data-stu-id="20f26-126">The `[info]` section contains general information about the provider.</span></span> <span data-ttu-id="20f26-127">Ключи раздела определяются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="20f26-127">The section keys are defined as follows:</span></span>

|<span data-ttu-id="20f26-128">Ключ</span><span class="sxs-lookup"><span data-stu-id="20f26-128">Key</span></span>|<span data-ttu-id="20f26-129">Описание</span><span class="sxs-lookup"><span data-stu-id="20f26-129">Description</span></span>
|---|-----------
|<span data-ttu-id="20f26-130">**Имя_драйвера**</span><span class="sxs-lookup"><span data-stu-id="20f26-130">**DriverName**</span></span>| <span data-ttu-id="20f26-131">Укажите имя ключа производительности поставщика, расположенного в реестре раздела `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` .</span><span class="sxs-lookup"><span data-stu-id="20f26-131">Specify the name of the provider's performance key located in the registry under the `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` key.</span></span> <span data-ttu-id="20f26-132">Сведения о создании этого ключа см. в разделе [Создание ключа производительности приложения](creating-the-applications-performance-key.md).</span><span class="sxs-lookup"><span data-stu-id="20f26-132">For information on creating this key, see [Creating the Application's Performance Key](creating-the-applications-performance-key.md).</span></span>
|<span data-ttu-id="20f26-133">**симболфиле**</span><span class="sxs-lookup"><span data-stu-id="20f26-133">**SymbolFile**</span></span>| <span data-ttu-id="20f26-134">Укажите файл заголовка. h, содержащий символьные значения объектов и счетчиков поставщика.</span><span class="sxs-lookup"><span data-stu-id="20f26-134">Specify the .h header file that contains symbolic values of your provider's objects and counters.</span></span> <span data-ttu-id="20f26-135">Во время установки (при вызове **lodctr**) файл заголовка должен находиться в том же каталоге, что и. INI-файл.</span><span class="sxs-lookup"><span data-stu-id="20f26-135">During installation (when invoking **lodctr**), the header file must be in the same directory as the .INI file.</span></span>
|<span data-ttu-id="20f26-136">**Доверитель**</span><span class="sxs-lookup"><span data-stu-id="20f26-136">**Trusted**</span></span>| <span data-ttu-id="20f26-137">Если включить этот ключ в `[info]` раздел, **lodctr** добавит в ключ производительности значение реестра кода проверки библиотеки с двоичной подписью библиотеки DLL производительности.</span><span class="sxs-lookup"><span data-stu-id="20f26-137">If you include this key in the `[info]` section, **lodctr** will add a Library Validation Code registry value to your performance key with a binary signature of your performance DLL.</span></span> <span data-ttu-id="20f26-138">Когда библиотека PERFLIB вызывает библиотеку DLL, она сравнивает подпись с библиотекой DLL, чтобы определить, была ли изменена библиотека DLL.</span><span class="sxs-lookup"><span data-stu-id="20f26-138">When PERFLIB calls your DLL it compares the signature with your DLL to determine if the DLL has been modified.</span></span> <span data-ttu-id="20f26-139">Значение **доверенного** ключа игнорируется.</span><span class="sxs-lookup"><span data-stu-id="20f26-139">The value of the **Trusted** key is ignored.</span></span>

<span data-ttu-id="20f26-140">`DriverName`Ключи и `SymbolFile` являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="20f26-140">The `DriverName` and `SymbolFile` keys are required.</span></span>

### <a name="objects-section"></a><span data-ttu-id="20f26-141">[Objects], раздел</span><span class="sxs-lookup"><span data-stu-id="20f26-141">[objects] section</span></span>

<span data-ttu-id="20f26-142">В `[objects]` разделе содержится список объектов производительности, поддерживаемых поставщиком.</span><span class="sxs-lookup"><span data-stu-id="20f26-142">The `[objects]` section provides a list of the performance objects that the provider supports.</span></span> <span data-ttu-id="20f26-143">Используется для определения того, относится ли каждый символ из `[text]` раздела к объекту или счетчику.</span><span class="sxs-lookup"><span data-stu-id="20f26-143">This is used to determine whether each symbol from the `[text]` section refers an object or a counter.</span></span>

<span data-ttu-id="20f26-144">Для каждого объекта (CounterSet), поддерживаемого поставщиком, добавьте один ключ с именем `<symbol>_<langid>_NAME=` в `[objects]` раздел, где `<symbol>` — это имя объекта, а `<langid>` — идентификатор языка одного из поддерживаемых языков.</span><span class="sxs-lookup"><span data-stu-id="20f26-144">For each object (counterset) supported by your provider, add one key named `<symbol>_<langid>_NAME=` to the `[objects]` section, where `<symbol>` is the name of the object and `<langid>` is the language id of one of the supported languages.</span></span> <span data-ttu-id="20f26-145">Значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="20f26-145">The value is ignored.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="20f26-146">`[objects]`Раздел улучшает производительность системы.</span><span class="sxs-lookup"><span data-stu-id="20f26-146">The `[objects]` section improves the performance of the system.</span></span> <span data-ttu-id="20f26-147">Хотя раздел «объекты» является необязательным, всегда следует включать этот раздел в. INI-файл.</span><span class="sxs-lookup"><span data-stu-id="20f26-147">Although the objects section is optional, you should always include this section in your .INI file.</span></span> <span data-ttu-id="20f26-148">Если включить этот раздел, то библиотека DLL производительности будет вызываться только в том случае, если вы поддерживаете запрошенный объект.</span><span class="sxs-lookup"><span data-stu-id="20f26-148">If you include this section, your performance DLL is called only if you support the requested object.</span></span> <span data-ttu-id="20f26-149">Если раздел «объекты» не включен, то библиотека DLL вызывается для каждого запроса, так как система не знает, какие объекты поддерживает поставщик.</span><span class="sxs-lookup"><span data-stu-id="20f26-149">If you do not include the objects section, your DLL is called for every query because the system does not know which objects your provider supports.</span></span> <span data-ttu-id="20f26-150">Если раздел объекта не включен, **lodctr** создает в журнале событий приложений сообщение о том, что. INI-файл не содержит секцию объектов.</span><span class="sxs-lookup"><span data-stu-id="20f26-150">If the object section is not included, **lodctr** generates a message in the application event log stating that the .INI file did not contain an objects section.</span></span> <span data-ttu-id="20f26-151">Идентификатор события этого сообщения — 2000.</span><span class="sxs-lookup"><span data-stu-id="20f26-151">The event identifier of this message is 2000.</span></span>

### <a name="languages-section"></a><span data-ttu-id="20f26-152">[языки], раздел</span><span class="sxs-lookup"><span data-stu-id="20f26-152">[languages] section</span></span>

<span data-ttu-id="20f26-153">`[languages]`Раздел содержит список идентификаторов языков для каждого языка, для которого поставщик предоставляет имена и строки справки.</span><span class="sxs-lookup"><span data-stu-id="20f26-153">The `[languages]` section provides a list of the language identifiers of each language for which your provider supplies name and help strings.</span></span> <span data-ttu-id="20f26-154">Все поставщики должны поддерживать `009` (английский).</span><span class="sxs-lookup"><span data-stu-id="20f26-154">All providers should support `009` (English).</span></span>

<span data-ttu-id="20f26-155">Для каждого поддерживаемого языка добавьте один ключ с именем `<langid>=` .</span><span class="sxs-lookup"><span data-stu-id="20f26-155">For each supported language, add one key named `<langid>=`.</span></span> <span data-ttu-id="20f26-156">Значение не учитывается, но в целях документации значение обычно устанавливается в соответствии с именем соответствующего языка, например `009=English` .</span><span class="sxs-lookup"><span data-stu-id="20f26-156">The value is ignored, but for documentation purposes the value is normally set to the name of the corresponding language, e.g. `009=English`.</span></span>

<span data-ttu-id="20f26-157">Для большинства языков следует использовать основной идентификатор языка.</span><span class="sxs-lookup"><span data-stu-id="20f26-157">For most languages, you should use the primary language identifier.</span></span> <span data-ttu-id="20f26-158">Полный список идентификаторов языков находится в файле заголовка WinNT. h под заголовком «Основные идентификаторы языка».</span><span class="sxs-lookup"><span data-stu-id="20f26-158">The complete list of language identifiers is in the Winnt.h header file, under the heading "Primary Language Ids."</span></span> <span data-ttu-id="20f26-159">Преобразовать значение, найденное в Winnt. h, в последовательность из 3 шестнадцатеричных цифр, удалив `0x` префикс и добавив начальные `0` цифры, пока последовательность не сойдет из 3 цифр.</span><span class="sxs-lookup"><span data-stu-id="20f26-159">Convert the value found in Winnt.h into a sequence of 3 hexadecimal digits by removing the `0x` prefix and adding leading `0` digits until the sequence is 3 digits long.</span></span> <span data-ttu-id="20f26-160">Например, чтобы указать строки на английском языке (0x9), используйте 009.</span><span class="sxs-lookup"><span data-stu-id="20f26-160">For example, to specify English strings (0x9), use 009.</span></span> <span data-ttu-id="20f26-161">Чтобы указать итальянские строки (0x10), используйте 010.</span><span class="sxs-lookup"><span data-stu-id="20f26-161">To specify Italian strings (0x10), use 010.</span></span>

<span data-ttu-id="20f26-162">Для китайского и португальского языков требуются идентификаторы основного и подязыкового языка.</span><span class="sxs-lookup"><span data-stu-id="20f26-162">Chinese and Portuguese languages require both the primary and sublanguage identifiers.</span></span> <span data-ttu-id="20f26-163">Используйте 404, 804, 416 или 816 вместо 004 или 016.</span><span class="sxs-lookup"><span data-stu-id="20f26-163">Use 404, 804, 416, or 816 instead of 004 or 016.</span></span>

### <a name="text-section"></a><span data-ttu-id="20f26-164">раздел [текст]</span><span class="sxs-lookup"><span data-stu-id="20f26-164">[text] section</span></span>

<span data-ttu-id="20f26-165">`[text]`Раздел содержит имя и строки справки для объектов и счетчиков.</span><span class="sxs-lookup"><span data-stu-id="20f26-165">The `[text]` section provides the name and help strings for your objects and counters.</span></span>

<span data-ttu-id="20f26-166">Для каждого объекта или счетчика, а также для каждого поддерживаемого языка необходимо указать ключ имени (содержащий имя или строку заголовка для объекта или счетчика), а также ввести ключ справки (содержащий описание или строку описания для объекта или счетчика).</span><span class="sxs-lookup"><span data-stu-id="20f26-166">For each object or counter, and for each supported language, you must provide a NAME key (containing the name or title string for your object or counter) and you may optionally provide a HELP key (containing the description or explanation string for your object or counter).</span></span> <span data-ttu-id="20f26-167">Ключи должны иметь имена `<symbol>_<langid>_NAME` и `<symbol>_<langid>_HELP` , где `<symbol>` — символьная константа для объекта или счетчика (как определено в символьном файле Constant. h), а `<langid>` — идентификатор языка, используемый для этой строки.</span><span class="sxs-lookup"><span data-stu-id="20f26-167">The keys should be named `<symbol>_<langid>_NAME` and `<symbol>_<langid>_HELP`, where `<symbol>` is the symbolic constant for the object or counter (as defined in the symbolic constant .h file), and `<langid>` is the language identifier used for this string.</span></span>

<span data-ttu-id="20f26-168">Например, строки на английском языке для счетчика с символом будут `MY_COUNTER` указаны следующим образом:</span><span class="sxs-lookup"><span data-stu-id="20f26-168">For example, the English strings for a counter with symbol `MY_COUNTER` would be specified as:</span></span>

```ini
MY_COUNTER_009_NAME=My Counter
MY_COUNTER_009_HELP=Description for My Counter.
```

<span data-ttu-id="20f26-169">Текстовые ключи могут отображаться в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="20f26-169">The text keys can appear in any order.</span></span> <span data-ttu-id="20f26-170">Текстовые строки не должны содержать символы форматирования, например символы табуляции.</span><span class="sxs-lookup"><span data-stu-id="20f26-170">The text strings should not contain formatting characters such as tabs.</span></span>

### <a name="example-ini-file"></a><span data-ttu-id="20f26-171">Пример INI-файла</span><span class="sxs-lookup"><span data-stu-id="20f26-171">Example INI file</span></span>

<span data-ttu-id="20f26-172">Ниже приведен пример файла инициализации, который используется в примере [создания библиотеки DLL расширения производительности](creating-a-performance-extension-dll.md) .</span><span class="sxs-lookup"><span data-stu-id="20f26-172">The following is an example of an initialization file that is used in the [Creating a Performance Extension DLL](creating-a-performance-extension-dll.md) sample.</span></span>

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

## <a name="running-the-lodctr-tool"></a><span data-ttu-id="20f26-173">Запуск средства lodctr</span><span class="sxs-lookup"><span data-stu-id="20f26-173">Running the Lodctr tool</span></span>

<span data-ttu-id="20f26-174">Для загрузки имен и строк справки, определенных в. INI-файл (во время установки поставщика) запустите средство **lodctr** из папки, в которой находится. INI-файл и заголовочный файл.</span><span class="sxs-lookup"><span data-stu-id="20f26-174">To load the names and help strings defined in your .INI file (during the installation of your provider), run the **lodctr** tool from the folder that contains your .INI file and header file.</span></span> <span data-ttu-id="20f26-175">Средство входит в состав компьютера.</span><span class="sxs-lookup"><span data-stu-id="20f26-175">The tool is included with the computer.</span></span> <span data-ttu-id="20f26-176">Необходимо запустить **lodctr** с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="20f26-176">You must run **lodctr** with elevated privileges.</span></span> <span data-ttu-id="20f26-177">Параметр для **lodctr** — это путь к. INI-файл.</span><span class="sxs-lookup"><span data-stu-id="20f26-177">The parameter to **lodctr** is the path to your .INI file.</span></span> <span data-ttu-id="20f26-178">Например, `lodctr "C:\Program Files\MyCompany\MyProvider\MyProvider.ini"`.</span><span class="sxs-lookup"><span data-stu-id="20f26-178">For example, `lodctr "C:\Program Files\MyCompany\MyProvider\MyProvider.ini"`.</span></span>

<span data-ttu-id="20f26-179">Чтобы выгрузить имена и строки справки (во время удаления), запустите средство **lodctr** .</span><span class="sxs-lookup"><span data-stu-id="20f26-179">To unload the names and help strings (during uninstall), run the **unlodctr** tool.</span></span> <span data-ttu-id="20f26-180">Необходимо запустить **lodctr** с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="20f26-180">You must run **unlodctr** with elevated privileges.</span></span> <span data-ttu-id="20f26-181">Параметр для **lodctr** — это имя_драйвера поставщика (имя ключа производительности поставщика).</span><span class="sxs-lookup"><span data-stu-id="20f26-181">The parameter to **unlodctr** is the DriverName of your provider (the name of the provider's performance key).</span></span> <span data-ttu-id="20f26-182">Например, `unlodctr "MyProvider"`.</span><span class="sxs-lookup"><span data-stu-id="20f26-182">For example, `unlodctr "MyProvider"`.</span></span>

<span data-ttu-id="20f26-183">Перед запуском **lodctr** убедитесь, что в приложении есть запись в разделе " **службы** ".</span><span class="sxs-lookup"><span data-stu-id="20f26-183">Before running **lodctr**, be sure that your application has an entry under the **Services** key.</span></span> <span data-ttu-id="20f26-184">Дополнительные сведения см. [в разделе Создание ключа производительности приложения](creating-the-applications-performance-key.md).</span><span class="sxs-lookup"><span data-stu-id="20f26-184">For details, see [Creating the Application's Performance Key](creating-the-applications-performance-key.md).</span></span> <span data-ttu-id="20f26-185">Если раздел не существует, **lodctr** не будет обновлять реестр с именами и описаниями.</span><span class="sxs-lookup"><span data-stu-id="20f26-185">If the key does not exist, **lodctr** will not update the registry with your names and descriptions.</span></span>

<span data-ttu-id="20f26-186">В качестве альтернативы запуску **lodctr** можно вызвать [**лоадперфкаунтертекстстрингс**](/windows/win32/api/loadperf/nf-loadperf-loadperfcountertextstringsw) (определенную в LoadPerf. h) из программы установки, чтобы загрузить описания имен счетчиков.</span><span class="sxs-lookup"><span data-stu-id="20f26-186">As an alternative to running **lodctr**, you can call [**LoadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-loadperfcountertextstringsw) (defined in Loadperf.h) from your installation program to load your counter names descriptions.</span></span> <span data-ttu-id="20f26-187">Затем можно вызвать [**унлоадперфкаунтертекстстрингс**](/windows/win32/api/loadperf/nf-loadperf-unloadperfcountertextstringsw) во время удаления.</span><span class="sxs-lookup"><span data-stu-id="20f26-187">You can then call [**UnloadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-unloadperfcountertextstringsw) during uninstall.</span></span>

<span data-ttu-id="20f26-188">Служебная программа **lodctr** копирует строки из. INI-файл к **счетчикам** и значения реестра **справки** в подразделах соответствующего языка.</span><span class="sxs-lookup"><span data-stu-id="20f26-188">The **lodctr** utility copies the strings from the .INI file to the **Counters** and **Help** registry values under the appropriate language subkeys.</span></span> <span data-ttu-id="20f26-189">Если соответствующий языковой ключ не существует, строки для этого языка не копируются.</span><span class="sxs-lookup"><span data-stu-id="20f26-189">If the corresponding language subkey does not exist, the strings for that language are not copied.</span></span> <span data-ttu-id="20f26-190">Программа также обновляет **последний счетчик** и Последнее значение **справки** .</span><span class="sxs-lookup"><span data-stu-id="20f26-190">The utility also updates the **Last Counter** and **Last Help** value.</span></span> <span data-ttu-id="20f26-191">Имена и описания счетчиков производительности хранятся в следующем расположении в реестре.</span><span class="sxs-lookup"><span data-stu-id="20f26-191">The performance counter names and descriptions are stored in the following location in the registry.</span></span>

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

<span data-ttu-id="20f26-192">Помимо добавления значений в раздел **PerfLib** , средство **lodctr** также добавляет следующие значения в узел **службы** для приложения.</span><span class="sxs-lookup"><span data-stu-id="20f26-192">In addition to adding values under the **PerfLib** key, the **lodctr** tool also adds the following values to the **Services** node for the application.</span></span> <span data-ttu-id="20f26-193">В большинстве случаев приложение и поставщик будут иметь связь «один к одному». Однако поставщик может предоставлять данные счетчиков для нескольких приложений, поэтому ключ основан на приложении, а не на поставщике.</span><span class="sxs-lookup"><span data-stu-id="20f26-193">In most cases, the application and provider will have a one-to-one relationship; however, it is possible for a provider to provide counter data for multiple applications, which is why the key is based on the application and not the provider.</span></span>

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
