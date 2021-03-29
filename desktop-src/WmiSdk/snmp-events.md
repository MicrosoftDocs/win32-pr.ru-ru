---
description: Поставщик SNMP поддерживает запись в файлы журналов и в отладчик.
ms.assetid: 66627927-2eee-4d56-a74b-f86147ad7711
ms.tgt_platform: multiple
title: События SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94b133d2fc81c76949439b3e1f26d1fc448f0b13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647257"
---
# <a name="snmp-events"></a><span data-ttu-id="80521-103">События SNMP</span><span class="sxs-lookup"><span data-stu-id="80521-103">SNMP Events</span></span>

<span data-ttu-id="80521-104">Поставщик SNMP поддерживает запись в файлы журналов и в отладчик.</span><span class="sxs-lookup"><span data-stu-id="80521-104">The SNMP provider supports writing to log files and to the debugger.</span></span>

> [!Note]  
> <span data-ttu-id="80521-105">Дополнительные сведения об установке поставщика см. в разделе [Настройка среды SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="80521-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="80521-106">Ряд разделов и значений реестра определяет уровень и тип ведения журнала, создаваемого в данный момент:</span><span class="sxs-lookup"><span data-stu-id="80521-106">A number of registry keys and values define the level and type of logging currently being generated:</span></span>

-   <span data-ttu-id="80521-107">Отладка</span><span class="sxs-lookup"><span data-stu-id="80521-107">Debugging</span></span>

    <span data-ttu-id="80521-108">Раздел **реестра \_ hKey \_ \\ Software Machine \\ \\ \\ providers регистратор \\ поставщиков Microsoft WBEM** содержит значение ведения журнала, которое указывает, можно ли записывать информацию в отладчик.</span><span class="sxs-lookup"><span data-stu-id="80521-108">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\MICROSOFT\\WBEM\\PROVIDERS\\LOGGING** registry key contains the logging value that indicates whether information can be written to the debugger.</span></span> <span data-ttu-id="80521-109">Значение ведения журнала задается как 0, чтобы отключить вывод отладки, или 1, чтобы включить его.</span><span class="sxs-lookup"><span data-stu-id="80521-109">The logging value is set either to 0 to disable debugging output or 1 to enable it.</span></span> <span data-ttu-id="80521-110">Ведение журнала — это \_ значение reg DWORD.</span><span class="sxs-lookup"><span data-stu-id="80521-110">Logging is a REG\_DWORD value.</span></span>

-   <span data-ttu-id="80521-111">Ведение журнала</span><span class="sxs-lookup"><span data-stu-id="80521-111">Logging</span></span>

    <span data-ttu-id="80521-112">В разделе реестра **hKey \_ Local \_ Machine \\ Software ( \\ поставщики Microsoft \\ WBEM \\ \\ \\** ), в котором содержится журнал ВБЕМСНМП, хранятся все сведения, относящиеся к поставщику SNMP.</span><span class="sxs-lookup"><span data-stu-id="80521-112">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\MICROSOFT\\WBEM\\PROVIDERS\\LOGGING\\WBEMSNMP** registry key holds all of the logging information specific to the SNMP provider.</span></span> <span data-ttu-id="80521-113">В следующей таблице перечислены значения, связанные с этим ключом.</span><span class="sxs-lookup"><span data-stu-id="80521-113">The following table lists the values associated with this key.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="80521-114">Значение</span><span class="sxs-lookup"><span data-stu-id="80521-114">Value</span></span></th>
<th><span data-ttu-id="80521-115">Описание</span><span class="sxs-lookup"><span data-stu-id="80521-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="80521-116">Тип</span><span class="sxs-lookup"><span data-stu-id="80521-116">Type</span></span></td>
<td><span data-ttu-id="80521-117"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="80521-117"><strong>REG_SZ</strong></span></span><br/> <span data-ttu-id="80521-118">Принимает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="80521-118">Takes one of the following values:</span></span><br/> <span data-ttu-id="80521-119">&quot;FILE &quot; = (по умолчанию) отправляет выходные данные отладки в файл.</span><span class="sxs-lookup"><span data-stu-id="80521-119">&quot;File&quot; = (Default) Sends debugging output to a file.</span></span><br/> <span data-ttu-id="80521-120">&quot;Отладчик &quot; = отправляет выходные данные отладки в отладчик.</span><span class="sxs-lookup"><span data-stu-id="80521-120">&quot;Debugger&quot; = Sends debugging output to the debugger.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="80521-121">MaxFileSize</span><span class="sxs-lookup"><span data-stu-id="80521-121">MaxFileSize</span></span></td>
<td><span data-ttu-id="80521-122"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="80521-122"><strong>REG_DWORD</strong></span></span><br/> <span data-ttu-id="80521-123">Принимает целочисленные значения от 1024 до 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="80521-123">Takes integer values from 1024 to 2^32-1.</span></span> <span data-ttu-id="80521-124">Значение — это максимально допустимый размер файла журнала в байтах.</span><span class="sxs-lookup"><span data-stu-id="80521-124">The value is the maximum allowed size in bytes for the log file.</span></span> <span data-ttu-id="80521-125">Если менее 1024, механизм ведения журнала использует значение 1024.</span><span class="sxs-lookup"><span data-stu-id="80521-125">If less than 1024, the logging mechanism uses a value of 1024.</span></span> <span data-ttu-id="80521-126">Для этого значения рекомендуется минимальный размер в 8 КБ.</span><span class="sxs-lookup"><span data-stu-id="80521-126">A minimum size of 8 KB is recommended for this value.</span></span> <span data-ttu-id="80521-127">Когда файл достигает размера, указанного параметром MaxFileSize, имя файла добавляется в начале символа "~" и создается новый файл.</span><span class="sxs-lookup"><span data-stu-id="80521-127">When the file reaches the size specified by MaxFileSize, the file name is prepended with a '~' character and a new file is created.</span></span> <span data-ttu-id="80521-128">Таким образом, максимальный объем места на диске, необходимый для ведения журнала, вдвое больше этого значения.</span><span class="sxs-lookup"><span data-stu-id="80521-128">Therefore, the maximum disk space required for logging is twice this value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="80521-129">Файл</span><span class="sxs-lookup"><span data-stu-id="80521-129">File</span></span></td>
<td><span data-ttu-id="80521-130"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="80521-130"><strong>REG_SZ</strong></span></span><br/> <span data-ttu-id="80521-131">Определяет имя файла, в который отправляются выходные данные отладки, если для типа ведения журнала задано значение "File".</span><span class="sxs-lookup"><span data-stu-id="80521-131">Defines the name of the file to which the debugging output is sent when the logging type is set to 'File'.</span></span> <span data-ttu-id="80521-132">Значение по умолчанию — " <WBEMLOGS> \вбемснмп.лог."</span><span class="sxs-lookup"><span data-stu-id="80521-132">The default value is '<WBEMLOGS>\wbemsnmp.log.'</span></span> <span data-ttu-id="80521-133">Если <WBEMLOGS> каталог не может быть определен из раздела реестра WMI, по умолчанию используется значение "к:\вбемснмп.лог".</span><span class="sxs-lookup"><span data-stu-id="80521-133">If the <WBEMLOGS> directory cannot be determined from the WMI registry section, the value defaults to 'c:\wbemsnmp.log'.</span></span> <span data-ttu-id="80521-134">Если используется общая папка, например \\ мачине\шаре\вбемснмп.лог или м:\вбемснмп.лог, где M: — \\ мачине\шаре, то учетная запись локальной системы, на которой запускается WMI, должна иметь права доступа для чтения и записи к \\ мачине\шаре.</span><span class="sxs-lookup"><span data-stu-id="80521-134">If a share is used, such as \\machine\share\wbemsnmp.log or M:\wbemsnmp.log where M: is \\machine\share, the local SYSTEM account on which WMI runs must have read/write access rights to the \\machine\share.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="80521-135">Level</span><span class="sxs-lookup"><span data-stu-id="80521-135">Level</span></span></td>
<td><span data-ttu-id="80521-136"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="80521-136"><strong>REG_DWORD</strong></span></span><br/> <span data-ttu-id="80521-137">Принимает целочисленные значения от 0 до 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="80521-137">Takes integer values from 0 through 2^32-1.</span></span> <span data-ttu-id="80521-138">Значение представляет собой логическую маску, состоящую из 32 бит.</span><span class="sxs-lookup"><span data-stu-id="80521-138">The value is a logical mask consisting of 32 bits.</span></span> <span data-ttu-id="80521-139">Следующие битовые маски объединяются для определения типа создаваемых выходных данных отладки:</span><span class="sxs-lookup"><span data-stu-id="80521-139">The following bit masks are combined to define the type of debugging output generated:</span></span><br/>
<ul>
<li><span data-ttu-id="80521-140">0: вызов метода <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> поставщика класса SNMP</span><span class="sxs-lookup"><span data-stu-id="80521-140">0: SNMP class provider <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> method invocations</span></span></li>
<li><span data-ttu-id="80521-141">1: реализация поставщика классов SNMP</span><span class="sxs-lookup"><span data-stu-id="80521-141">1: SNMP class provider implementation</span></span></li>
<li><span data-ttu-id="80521-142">2: вызов метода <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> поставщика экземпляров SNMP</span><span class="sxs-lookup"><span data-stu-id="80521-142">2: SNMP instance provider <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> method invocations</span></span></li>
<li><span data-ttu-id="80521-143">3: реализация поставщика экземпляров SNMP</span><span class="sxs-lookup"><span data-stu-id="80521-143">3: SNMP instance provider implementation</span></span></li>
<li><span data-ttu-id="80521-144">4: Библиотека классов SNMP</span><span class="sxs-lookup"><span data-stu-id="80521-144">4: SNMP class library</span></span></li>
<li><span data-ttu-id="80521-145">5: SNMP СМИР</span><span class="sxs-lookup"><span data-stu-id="80521-145">5: SNMP SMIR</span></span></li>
<li><span data-ttu-id="80521-146">6: корреляция SNMP</span><span class="sxs-lookup"><span data-stu-id="80521-146">6: SNMP correlator</span></span></li>
<li><span data-ttu-id="80521-147">7: код сопоставления типов SNMP</span><span class="sxs-lookup"><span data-stu-id="80521-147">7: SNMP type mapping code</span></span></li>
<li><span data-ttu-id="80521-148">8: потоковый код SNMP</span><span class="sxs-lookup"><span data-stu-id="80521-148">8: SNMP threading code</span></span></li>
<li><span data-ttu-id="80521-149">9: интерфейсы и реализация поставщика событий SNMP</span><span class="sxs-lookup"><span data-stu-id="80521-149">9: SNMP event provider interfaces and implementation</span></span></li>
</ul>
<span data-ttu-id="80521-150">Задайте для параметра Level (2 ^ 0 + 2 ^ 8 =) 257 для операций, включающих <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>вызовы методов SSL</strong></a> класса SNMP и операции с использованием потокового кода SNMP.</span><span class="sxs-lookup"><span data-stu-id="80521-150">Set Level to (2^0 + 2^8=) 257 for operations involving calls to the SNMP class provider <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> methods, and operations using SNMP threading code.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




