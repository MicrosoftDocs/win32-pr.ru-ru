---
title: Настройка ведения журнала ошибок API-сервера HTTP
description: Ведение журнала ошибок API-сервера HTTP управляется тремя значениями реестра в разделе \\ параметров HTTP.
ms.assetid: a7712159-939e-42e3-a8d8-73148c2f4f6e
keywords:
- API сервера HTTP, Настройка журналов ошибок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 698f6b5ae81b1933ea745789e0fae33dfc7ebce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410924"
---
# <a name="configuring-http-server-api-error-logging"></a><span data-ttu-id="bc13e-104">Настройка ведения журнала ошибок API-сервера HTTP</span><span class="sxs-lookup"><span data-stu-id="bc13e-104">Configuring HTTP Server API Error Logging</span></span>

<span data-ttu-id="bc13e-105">Ведение журнала ошибок API-сервера HTTP управляется тремя значениями реестра в разделе  \\ **параметров** HTTP, расположенном по адресу:</span><span class="sxs-lookup"><span data-stu-id="bc13e-105">The HTTP Server API error logging is controlled by three registry values under an **HTTP**\\**Parameters** key located at:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

> [!Note]  
> <span data-ttu-id="bc13e-106">Расположение и форма значений конфигурации могут измениться в будущих версиях операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="bc13e-106">The location and form of the configuration values may change in future versions of the Windows operating system.</span></span>

 

<span data-ttu-id="bc13e-107">Пользователь должен иметь права администратора или локальной системы для изменения значений реестра, а также просматривать или изменять файлы журнала и папку, в которой они находятся.</span><span class="sxs-lookup"><span data-stu-id="bc13e-107">A user must have Administrator/Local System privileges to modify the registry values, and view or modify the log files and the folder that contains them.</span></span>

<span data-ttu-id="bc13e-108">Сведения о конфигурации в значениях реестра считываются при запуске драйвера API сервера HTTP.</span><span class="sxs-lookup"><span data-stu-id="bc13e-108">Configuration information in the registry values is read when the HTTP Server API driver is started.</span></span> <span data-ttu-id="bc13e-109">В результате, если параметры изменены, драйвер должен быть остановлен и перезапущен для считывания новых значений.</span><span class="sxs-lookup"><span data-stu-id="bc13e-109">As a result, if the settings are changed the driver must be stopped and restarted to read the new values.</span></span> <span data-ttu-id="bc13e-110">Это можно сделать с помощью следующих команд консоли:</span><span class="sxs-lookup"><span data-stu-id="bc13e-110">This can be accomplished by using the following console commands:</span></span>

<span data-ttu-id="bc13e-111">**NET останавливает HTTP**</span><span class="sxs-lookup"><span data-stu-id="bc13e-111">**net stop http**</span></span>

<span data-ttu-id="bc13e-112">**NET start http**</span><span class="sxs-lookup"><span data-stu-id="bc13e-112">**net start http**</span></span>

<span data-ttu-id="bc13e-113">Имена файлов журнала задаются с помощью следующего соглашения:</span><span class="sxs-lookup"><span data-stu-id="bc13e-113">The log files are named by using the following convention:</span></span>

<span data-ttu-id="bc13e-114">**хттперр +** *SequenceNumber* **+. log**</span><span class="sxs-lookup"><span data-stu-id="bc13e-114">**httperr +** *SequenceNumber* **+ .log**</span></span>

<span data-ttu-id="bc13e-115">Например: "httperr4. log".</span><span class="sxs-lookup"><span data-stu-id="bc13e-115">For example: "httperr4.log".</span></span>

<span data-ttu-id="bc13e-116">Файлы журнала циклически передаются, если они достигли максимального размера, указанного в параметре реестра **еррорлогфилетрункатесизе** , а значение не может быть меньше одного мегабайта (МБ).</span><span class="sxs-lookup"><span data-stu-id="bc13e-116">Log files are cycled when they reach the maximum size specified by the **ErrorLogFileTruncateSize** registry value, and the value cannot be less than one megabyte (MB).</span></span>

<span data-ttu-id="bc13e-117">Если настройка журнала ошибок недействительна или происходит ошибка любого типа при записи в файлы журнала, то API-интерфейс сервера HTTP использует ведение журнала событий для уведомления администраторов о том, что регистрация ошибок не выполнялась.</span><span class="sxs-lookup"><span data-stu-id="bc13e-117">If the configuration of error logging is invalid or any kind of failure occurs while writing to the log files, the HTTP Server API uses event logging to notify administrators that error logging did not take place.</span></span>

<span data-ttu-id="bc13e-118">Значения конфигурации реестра описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="bc13e-118">Registry configuration values are described in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bc13e-119">Значение реестра</span><span class="sxs-lookup"><span data-stu-id="bc13e-119">Registry Value</span></span></th>
<th><span data-ttu-id="bc13e-120">Описание</span><span class="sxs-lookup"><span data-stu-id="bc13e-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bc13e-121"><span id="EnableErrorLogging"></span><span id="enableerrorlogging"></span><span id="ENABLEERRORLOGGING"></span>енаблиррорлоггинг</span><span class="sxs-lookup"><span data-stu-id="bc13e-121"><span id="EnableErrorLogging"></span><span id="enableerrorlogging"></span><span id="ENABLEERRORLOGGING"></span>EnableErrorLogging</span></span><br/></td>
<td><span data-ttu-id="bc13e-122"><strong>Параметр DWORD</strong> , для которого можно задать <strong>значение true</strong> , чтобы включить ведение журнала ошибок, или <strong>false</strong> для отключения.</span><span class="sxs-lookup"><span data-stu-id="bc13e-122">A <strong>DWORD</strong> that can be set to <strong>TRUE</strong> to enable error logging, or <strong>FALSE</strong> to disable it.</span></span> <span data-ttu-id="bc13e-123">Значение по умолчанию — <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc13e-123">The default value is <strong>TRUE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc13e-124"><span id="ErrorLogFileTruncateSize"></span><span id="errorlogfiletruncatesize"></span><span id="ERRORLOGFILETRUNCATESIZE"></span>еррорлогфилетрункатесизе</span><span class="sxs-lookup"><span data-stu-id="bc13e-124"><span id="ErrorLogFileTruncateSize"></span><span id="errorlogfiletruncatesize"></span><span id="ERRORLOGFILETRUNCATESIZE"></span>ErrorLogFileTruncateSize</span></span><br/></td>
<td><span data-ttu-id="bc13e-125">Значение <strong>типа DWORD</strong> , указывающее максимальный размер файла журнала ошибок в байтах.</span><span class="sxs-lookup"><span data-stu-id="bc13e-125">A <strong>DWORD</strong> that specifies the maximum size of an error log file, in bytes.</span></span> <span data-ttu-id="bc13e-126">Значение по умолчанию — 1 МБ (0x100000).</span><span class="sxs-lookup"><span data-stu-id="bc13e-126">The default value is one MB (0x100000).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="bc13e-127">Указанное значение не может быть меньше значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bc13e-127">The specified value cannot be smaller than the default value.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc13e-128"><span id="ErrorLoggingDir"></span><span id="errorloggingdir"></span><span id="ERRORLOGGINGDIR"></span>еррорлоггингдир</span><span class="sxs-lookup"><span data-stu-id="bc13e-128"><span id="ErrorLoggingDir"></span><span id="errorloggingdir"></span><span id="ERRORLOGGINGDIR"></span>ErrorLoggingDir</span></span><br/></td>
<td><span data-ttu-id="bc13e-129"><strong>Строка</strong> , указывающая папку, в которой API-сервер HTTP помещает свои файлы журнала.</span><span class="sxs-lookup"><span data-stu-id="bc13e-129">A <strong>String</strong> that specifies the folder under which the HTTP Server API places its logging files.</span></span> <br/> <span data-ttu-id="bc13e-130">API сервера HTTP создает вложенную папку с именем &quot; хттперр &quot; в указанной папке, в которую помещаются файлы журнала.</span><span class="sxs-lookup"><span data-stu-id="bc13e-130">The HTTP Server API creates a subfolder named &quot;HTTPERR&quot; under the specified folder into which the log files are placed.</span></span> <span data-ttu-id="bc13e-131">Эта вложенная папка и файлы журналов получают те же параметры разрешений, что означает, что администраторы и учетные записи локальной системы имеют полный доступ, а другие пользователи не имеют доступа.</span><span class="sxs-lookup"><span data-stu-id="bc13e-131">This subfolder and the log files receive the same permission settings, which means that Administrator and Local System Accounts have full access, while other users do not have access.</span></span><br/> <span data-ttu-id="bc13e-132">Если папка не указана в реестре, папка по умолчанию имеет следующий адрес:</span><span class="sxs-lookup"><span data-stu-id="bc13e-132">If a folder is not specified in the registry, the default folder is the following:</span></span><br/> <span data-ttu-id="bc13e-133">&quot;%SystemRoot%\System32\LogFiles&quot;</span><span class="sxs-lookup"><span data-stu-id="bc13e-133">&quot;%SystemRoot%\System32\LogFiles&quot;</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="bc13e-134">Значение строки Еррорлоггингдир должно быть полным путем, но может содержать &quot; % systemroot% &quot; .</span><span class="sxs-lookup"><span data-stu-id="bc13e-134">The ErrorLoggingDir string value must be a fully qualified path, but it can contain &quot;%SystemRoot%&quot;.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

 

 





