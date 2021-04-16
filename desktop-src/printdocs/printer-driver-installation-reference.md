---
description: Функции в этом разделе устанавливают и настраивают драйверы принтеров на компьютере.
ms.assetid: e6aa8963-aa1a-4313-bc24-2aeb4f4b93c4
title: Справочник по установке драйвера принтера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1613725ec5c7e2dbb06710bff706ec5aa7e32dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712243"
---
# <a name="printer-driver-installation-reference"></a><span data-ttu-id="20050-103">Справочник по установке драйвера принтера</span><span class="sxs-lookup"><span data-stu-id="20050-103">Printer Driver Installation Reference</span></span>

<span data-ttu-id="20050-104">Функции в этом разделе устанавливают и настраивают драйверы принтеров на компьютере.</span><span class="sxs-lookup"><span data-stu-id="20050-104">The functions in this section install and configure printer drivers on a computer.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="20050-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="20050-105">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20050-106">Функция</span><span class="sxs-lookup"><span data-stu-id="20050-106">Function</span></span></th>
<th><span data-ttu-id="20050-107">Описание</span><span class="sxs-lookup"><span data-stu-id="20050-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="20050-108"><a href="addmonitor.md"><strong>аддмонитор</strong></a></span><span class="sxs-lookup"><span data-stu-id="20050-108"><a href="addmonitor.md"><strong>AddMonitor</strong></a></span></span><br/></td>
<td><span data-ttu-id="20050-109">Функция <a href="/windows/desktop/printdocs/addmonitor"><strong>аддмонитор</strong></a> устанавливает монитор локального порта и связывает файлы конфигурации, данных и монитора.</span><span class="sxs-lookup"><span data-stu-id="20050-109">The <a href="/windows/desktop/printdocs/addmonitor"><strong>AddMonitor</strong></a> function installs a local port monitor and links the configuration, data, and monitor files.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20050-110"><a href="addport.md"><strong>AddPort</strong></a></span><span class="sxs-lookup"><span data-stu-id="20050-110"><a href="addport.md"><strong>AddPort</strong></a></span></span><br/></td>
<td><span data-ttu-id="20050-111">Функция <a href="/windows/desktop/printdocs/addport"><strong>аддпорт</strong></a> добавляет имя порта в список поддерживаемых портов.</span><span class="sxs-lookup"><span data-stu-id="20050-111">The <a href="/windows/desktop/printdocs/addport"><strong>AddPort</strong></a> function adds the name of a port to the list of supported ports.</span></span> <span data-ttu-id="20050-112">Функция <strong>аддпорт</strong> экспортируется монитором порта.</span><span class="sxs-lookup"><span data-stu-id="20050-112">The <strong>AddPort</strong> function is exported by the port monitor.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20050-113"><a href="addprinterdriver.md"><strong>аддпринтердривер</strong></a></span><span class="sxs-lookup"><span data-stu-id="20050-113"><a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a></span></span><br/></td>
<td><span data-ttu-id="20050-114">Функция <a href="/windows/desktop/printdocs/addprinterdriver"><strong>аддпринтердривер</strong></a> устанавливает локальный или удаленный драйвер принтера и связывает файлы конфигурации, данных и драйверов.</span><span class="sxs-lookup"><span data-stu-id="20050-114">The <a href="/windows/desktop/printdocs/addprinterdriver"><strong>AddPrinterDriver</strong></a> function installs a local or remote printer driver and associates the configuration, data, and driver files.</span></span><br/> <span data-ttu-id="20050-115">Для большей гибкости при установке или обновлении драйверов принтеров используйте функцию <a href="addprinterdriverex.md"><strong>аддпринтердриверекс</strong></a> , так как она обеспечивает жесткое обновление, более пониженную версию, копирование только новых файлов и копирование всех файлов (независимо от отметки времени файла).</span><span class="sxs-lookup"><span data-stu-id="20050-115">For more flexibility in installing or upgrading printer drivers, use the <a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a> function because it allows strict upgrade, strict downgrade, copying of newer files only, and copying of all files (regardless of the file time stamps).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="20050-116">Установка драйвера принтера без пакета драйверов больше не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="20050-116">Installing a printer driver without a driver package is no longer recommended.</span></span> <span data-ttu-id="20050-117">Вместо этого используйте <a href="installprinterdriverfrompackage.md"><strong>инсталлпринтердриверфромпаккаже</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="20050-117">Use <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20050-118"><a href="addprinterdriverex.md"><strong>аддпринтердриверекс</strong></a></span><span class="sxs-lookup"><span data-stu-id="20050-118"><a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="20050-119">Функция <a href="/windows/desktop/printdocs/addprinterdriverex"><strong>аддпринтердриверекс</strong></a> устанавливает локальный или удаленный драйвер принтера и связывает файлы конфигурации, данных и драйверов.</span><span class="sxs-lookup"><span data-stu-id="20050-119">The <a href="/windows/desktop/printdocs/addprinterdriverex"><strong>AddPrinterDriverEx</strong></a> function installs a local or remote printer driver and links the configuration, data, and driver files.</span></span> <span data-ttu-id="20050-120">Помимо возможностей <a href="addprinterdriver.md"><strong>аддпринтердривер</strong></a>, у нее также есть параметры, обеспечивающие жесткое обновление, более пониженную версию, копирование только новых файлов и копирование всех файлов (независимо от отметки времени файла).</span><span class="sxs-lookup"><span data-stu-id="20050-120">Besides having the capabilities of <a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a>, it also has options that permit strict upgrade, strict downgrade, copying of newer files only, and copying of all files (regardless of file time stamps).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="20050-121">Установка драйвера принтера без пакета драйверов больше не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="20050-121">Installing a printer driver without a driver package is no longer recommended.</span></span> <span data-ttu-id="20050-122">Вместо этого используйте <a href="installprinterdriverfrompackage.md"><strong>инсталлпринтердриверфромпаккаже</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="20050-122">Use <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20050-123"><a href="addprintprocessor.md"><strong>аддпринтпроцессор</strong></a></span><span class="sxs-lookup"><span data-stu-id="20050-123"><a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a></span></span><br/></td>
<td><span data-ttu-id="20050-124">Функция <a href="/windows/desktop/printdocs/addprintprocessor"><strong>аддпринтпроцессор</strong></a> устанавливает обработчик заданий печати на указанном сервере и добавляет имя обработчика печати в список поддерживаемых обработчиков печати.</span><span class="sxs-lookup"><span data-stu-id="20050-124">The <a href="/windows/desktop/printdocs/addprintprocessor"><strong>AddPrintProcessor</strong></a> function installs a print processor on the specified server and adds the print-processor name to the list of supported print processors.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20050-125"><a href="addprintprovidor.md"><strong>аддпринтпровидор</strong></a></span><span class="sxs-lookup"><span data-stu-id="20050-125"><a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a></span></span><br/></td>
<td><span data-ttu-id="20050-126">Функция <a href="/windows/desktop/printdocs/addprintprovidor"><strong>аддпринтпровидор</strong></a> устанавливает локальный поставщик печати и связывает файлы конфигурации, данных и поставщика.</span><span class="sxs-lookup"><span data-stu-id="20050-126">The <a href="/windows/desktop/printdocs/addprintprovidor"><strong>AddPrintProvidor</strong></a> function installs a local print provider and links the configuration, data, and provider files.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20050-127"><a href="coreprinterdriverinstalled.md"><strong>корепринтердриверинсталлед</strong></a></span><span class="sxs-lookup"><span data-stu-id="20050-127"><a href="coreprinterdriverinstalled.md"><strong>CorePrinterDriverInstalled</strong></a></span></span><br/></td>
<td><span data-ttu-id="20050-128">Функция <a href="/windows/desktop/printdocs/coreprinterdriverinstalled"><strong>корепринтердриверинсталлед</strong></a> сообщает, установлен ли основной драйвер принтера с указанными GUID, датой и версией.</span><span class="sxs-lookup"><span data-stu-id="20050-128">The <a href="/windows/desktop/printdocs/coreprinterdriverinstalled"><strong>CorePrinterDriverInstalled</strong></a> function reports whether a core printer driver with a specified GUID, date, and version is installed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20050-129"><a href="deletemonitor.md"><strong>делетемонитор</strong></a></span><span class="sxs-lookup"><span data-stu-id="20050-129"><a href="deletemonitor.md"><strong>DeleteMonitor</strong></a></span></span><br/></td>
<td><span data-ttu-id="20050-130">Функция <a href="/windows/desktop/printdocs/deletemonitor"><strong>делетемонитор</strong></a> удаляет монитор портов, добавленный функцией <a href="addmonitor.md"><strong>аддмонитор</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="20050-130">The <a href="/windows/desktop/printdocs/deletemonitor"><strong>DeleteMonitor</strong></a> function removes a port monitor added by the <a href="addmonitor.md"><strong>AddMonitor</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20050-131"><a href="deleteport.md"><strong>делетепорт</strong></a></span><span class="sxs-lookup"><span data-stu-id="20050-131"><a href="deleteport.md"><strong>DeletePort</strong></a></span></span><br/></td>
<td><span data-ttu-id="20050-132">Функция <a href="/windows/desktop/printdocs/deleteport"><strong>делетепорт</strong></a> отображает диалоговое окно, позволяющее пользователю удалить имя порта.</span><span class="sxs-lookup"><span data-stu-id="20050-132">The <a href="/windows/desktop/printdocs/deleteport"><strong>DeletePort</strong></a> function displays a dialog box that allows the user to delete a port name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20050-133"><a href="deleteprinterdriver.md"><strong>делетепринтердривер</strong></a></span><span class="sxs-lookup"><span data-stu-id="20050-133"><a href="deleteprinterdriver.md"><strong>DeletePrinterDriver</strong></a></span></span><br/></td>
<td><span data-ttu-id="20050-134">Функция <a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>делетепринтердривер</strong></a> удаляет указанное имя драйвера принтера из списка имен поддерживаемых драйверов на сервере.</span><span class="sxs-lookup"><span data-stu-id="20050-134">The <a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a> function removes the specified printer-driver name from the list of names of supported drivers on a server.</span></span><br/> <span data-ttu-id="20050-135">Чтобы удалить файлы, связанные с драйвером, помимо удаления указанного имени драйвера принтера из списка имен поддерживаемых драйверов для сервера, используйте функцию <a href="deleteprinterdriverex.md"><strong>делетепринтердриверекс</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="20050-135">To delete the files associated with the driver in addition to removing the specified printer-driver name from the list of names of supported drivers for a server, use the <a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> function.</span></span><br/> <span data-ttu-id="20050-136"><a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>Делетепринтердривер</strong></a> удаляет драйвер, только если для указанной среды не используется ни одна версия драйвера.</span><span class="sxs-lookup"><span data-stu-id="20050-136"><a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a> deletes a driver only if no version of the driver is in use for the specified environment.</span></span> <span data-ttu-id="20050-137"><a href="deleteprinterdriverex.md"><strong>Делетепринтердриверекс</strong></a> может удалять определенные версии драйвера.</span><span class="sxs-lookup"><span data-stu-id="20050-137"><a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> can delete specific versions of the driver.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20050-138"><a href="deleteprinterdriverex.md"><strong>делетепринтердриверекс</strong></a></span><span class="sxs-lookup"><span data-stu-id="20050-138"><a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="20050-139">Функция <a href="/windows/desktop/printdocs/deleteprinterdriverex"><strong>делетепринтердриверекс</strong></a> удаляет указанное имя драйвера принтера из списка имен поддерживаемых драйверов на сервере и удаляет файлы, связанные с драйвером.</span><span class="sxs-lookup"><span data-stu-id="20050-139">The <a href="/windows/desktop/printdocs/deleteprinterdriverex"><strong>DeletePrinterDriverEx</strong></a> function removes the specified printer-driver name from the list of names of supported drivers on a server and deletes the files associated with the driver.</span></span> <span data-ttu-id="20050-140">Эта функция также может удалять определенные версии драйвера.</span><span class="sxs-lookup"><span data-stu-id="20050-140">This function can also delete specific versions of the driver.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20050-141"><a href="deleteprinterdriverpackage.md"><strong>делетепринтердриверпаккаже</strong></a></span><span class="sxs-lookup"><span data-stu-id="20050-141"><a href="deleteprinterdriverpackage.md"><strong>DeletePrinterDriverPackage</strong></a></span></span><br/></td>
<td><span data-ttu-id="20050-142">Удаляет пакет драйвера принтера из хранилища драйверов.</span><span class="sxs-lookup"><span data-stu-id="20050-142">Deletes a printer driver package from the driver store.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20050-143"><a href="deleteprintprocessor.md"><strong>делетепринтпроцессор</strong></a></span><span class="sxs-lookup"><span data-stu-id="20050-143"><a href="deleteprintprocessor.md"><strong>DeletePrintProcessor</strong></a></span></span><br/></td>
<td><span data-ttu-id="20050-144">Функция <a href="/windows/desktop/printdocs/deleteprintprocessor"><strong>делетепринтпроцессор</strong></a> удаляет обработчик печати, добавленный функцией <a href="addprintprocessor.md"><strong>аддпринтпроцессор</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="20050-144">The <a href="/windows/desktop/printdocs/deleteprintprocessor"><strong>DeletePrintProcessor</strong></a> function removes a print processor added by the <a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a> function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20050-145"><a href="deleteprintprovidor.md"><strong>делетепринтпровидор</strong></a></span><span class="sxs-lookup"><span data-stu-id="20050-145"><a href="deleteprintprovidor.md"><strong>DeletePrintProvidor</strong></a></span></span><br/></td>
<td><span data-ttu-id="20050-146">Функция <a href="/windows/desktop/printdocs/deleteprintprovidor"><strong>делетепринтпровидор</strong></a> Удаляет поставщика печати, добавленного функцией <a href="addprintprovidor.md"><strong>аддпринтпровидор</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="20050-146">The <a href="/windows/desktop/printdocs/deleteprintprovidor"><strong>DeletePrintProvidor</strong></a> function removes a print provider added by the <a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20050-147"><a href="enummonitors.md"><strong>енуммониторс</strong></a></span><span class="sxs-lookup"><span data-stu-id="20050-147"><a href="enummonitors.md"><strong>EnumMonitors</strong></a></span></span><br/></td>
<td><span data-ttu-id="20050-148">Функция <a href="/windows/desktop/printdocs/enummonitors"><strong>енуммониторс</strong></a> извлекает сведения о мониторах портов, установленных на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="20050-148">The <a href="/windows/desktop/printdocs/enummonitors"><strong>EnumMonitors</strong></a> function retrieves information about the port monitors installed on the specified server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20050-149"><a href="enumports.md"><strong>EnumPorts</strong></a></span><span class="sxs-lookup"><span data-stu-id="20050-149"><a href="enumports.md"><strong>EnumPorts</strong></a></span></span><br/></td>
<td><span data-ttu-id="20050-150">Функция <a href="/windows/desktop/printdocs/enumports"><strong>енумпортс</strong></a> перечисляет порты, доступные для печати на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="20050-150">The <a href="/windows/desktop/printdocs/enumports"><strong>EnumPorts</strong></a> function enumerates the ports that are available for printing on a specified server.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20050-151"><a href="enumprinterdrivers.md"><strong>енумпринтердриверс</strong></a></span><span class="sxs-lookup"><span data-stu-id="20050-151"><a href="enumprinterdrivers.md"><strong>EnumPrinterDrivers</strong></a></span></span><br/></td>
<td><span data-ttu-id="20050-152">Функция <a href="/windows/desktop/printdocs/enumprinterdrivers"><strong>енумпринтердриверс</strong></a> перечисляет драйверы принтера, установленные на указанном сервере принтера.</span><span class="sxs-lookup"><span data-stu-id="20050-152">The <a href="/windows/desktop/printdocs/enumprinterdrivers"><strong>EnumPrinterDrivers</strong></a> function enumerates the printer drivers installed on a specified printer server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20050-153"><a href="enumprintprocessordatatypes.md"><strong>енумпринтпроцессордататипес</strong></a></span><span class="sxs-lookup"><span data-stu-id="20050-153"><a href="enumprintprocessordatatypes.md"><strong>EnumPrintProcessorDatatypes</strong></a></span></span><br/></td>
<td><span data-ttu-id="20050-154">Функция <a href="/windows/desktop/printdocs/enumprintprocessordatatypes"><strong>енумпринтпроцессордататипес</strong></a> перечисляет типы данных, поддерживаемые указанным обработчиком печати.</span><span class="sxs-lookup"><span data-stu-id="20050-154">The <a href="/windows/desktop/printdocs/enumprintprocessordatatypes"><strong>EnumPrintProcessorDatatypes</strong></a> function enumerates the data types that a specified print processor supports.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20050-155"><a href="enumprintprocessors.md"><strong>енумпринтпроцессорс</strong></a></span><span class="sxs-lookup"><span data-stu-id="20050-155"><a href="enumprintprocessors.md"><strong>EnumPrintProcessors</strong></a></span></span><br/></td>
<td><span data-ttu-id="20050-156">Функция <a href="/windows/desktop/printdocs/enumprintprocessors"><strong>енумпринтпроцессорс</strong></a> перечисляет обработчики печати, установленные на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="20050-156">The <a href="/windows/desktop/printdocs/enumprintprocessors"><strong>EnumPrintProcessors</strong></a> function enumerates the print processors installed on the specified server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20050-157"><a href="getcoreprinterdrivers.md"><strong>жеткорепринтердриверс</strong></a></span><span class="sxs-lookup"><span data-stu-id="20050-157"><a href="getcoreprinterdrivers.md"><strong>GetCorePrinterDrivers</strong></a></span></span><br/></td>
<td><span data-ttu-id="20050-158">Извлекает GUID, версию и дату указанных основных драйверов принтера и путь к их пакетам.</span><span class="sxs-lookup"><span data-stu-id="20050-158">Retrieves GUID, version, and date of the specified core printer drivers and the path to their packages.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20050-159"><a href="getprinterdriver.md"><strong>жетпринтердривер</strong></a></span><span class="sxs-lookup"><span data-stu-id="20050-159"><a href="getprinterdriver.md"><strong>GetPrinterDriver</strong></a></span></span><br/></td>
<td><span data-ttu-id="20050-160">Функция <a href="/windows/desktop/printdocs/getprinterdriver"><strong>жетпринтердривер</strong></a> извлекает данные драйвера для указанного принтера.</span><span class="sxs-lookup"><span data-stu-id="20050-160">The <a href="/windows/desktop/printdocs/getprinterdriver"><strong>GetPrinterDriver</strong></a> function retrieves driver data for the specified printer.</span></span> <span data-ttu-id="20050-161">Если драйвер не установлен на локальном компьютере, <strong>жетпринтердривер</strong> устанавливает его.</span><span class="sxs-lookup"><span data-stu-id="20050-161">If the driver is not installed on the local computer, <strong>GetPrinterDriver</strong> installs it.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20050-162"><a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a></span><span class="sxs-lookup"><span data-stu-id="20050-162"><a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a></span></span><br/></td>
<td><span data-ttu-id="20050-163">Функция <a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a> извлекает данные драйвера для указанного принтера.</span><span class="sxs-lookup"><span data-stu-id="20050-163">The <a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a> function retrieves driver data for the specified printer.</span></span> <span data-ttu-id="20050-164">Если драйвер не установлен на локальном компьютере, <strong>GetPrinterDriver2</strong> устанавливает его и отображает в указанном окне любой пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="20050-164">If the driver is not installed on the local computer, <strong>GetPrinterDriver2</strong> installs it and displays any user interface to the specified window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20050-165"><a href="getprinterdriverdirectory.md"><strong>жетпринтердривердиректори</strong></a></span><span class="sxs-lookup"><span data-stu-id="20050-165"><a href="getprinterdriverdirectory.md"><strong>GetPrinterDriverDirectory</strong></a></span></span><br/></td>
<td><span data-ttu-id="20050-166">Функция <a href="/windows/desktop/printdocs/getprinterdriverdirectory"><strong>жетпринтердривердиректори</strong></a> извлекает путь к каталогу драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="20050-166">The <a href="/windows/desktop/printdocs/getprinterdriverdirectory"><strong>GetPrinterDriverDirectory</strong></a> function retrieves the path of the printer-driver directory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20050-167"><a href="getprinterdriverpackagepath.md"><strong>жетпринтердриверпаккажепас</strong></a></span><span class="sxs-lookup"><span data-stu-id="20050-167"><a href="getprinterdriverpackagepath.md"><strong>GetPrinterDriverPackagePath</strong></a></span></span><br/></td>
<td><span data-ttu-id="20050-168">Извлекает путь к указанному пакету драйвера принтера на сервере печати.</span><span class="sxs-lookup"><span data-stu-id="20050-168">Retrieves the path to the specified printer driver package on a print server.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20050-169"><a href="getprintprocessordirectory.md"><strong>жетпринтпроцессордиректори</strong></a></span><span class="sxs-lookup"><span data-stu-id="20050-169"><a href="getprintprocessordirectory.md"><strong>GetPrintProcessorDirectory</strong></a></span></span><br/></td>
<td><span data-ttu-id="20050-170">Функция <a href="/windows/desktop/printdocs/getprintprocessordirectory"><strong>жетпринтпроцессордиректори</strong></a> извлекает путь к каталогу обработчика печати на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="20050-170">The <a href="/windows/desktop/printdocs/getprintprocessordirectory"><strong>GetPrintProcessorDirectory</strong></a> function retrieves the path to the print processor directory on the specified server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20050-171"><a href="installprinterdriverfrompackage.md"><strong>инсталлпринтердриверфромпаккаже</strong></a></span><span class="sxs-lookup"><span data-stu-id="20050-171"><a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a></span></span><br/></td>
<td><span data-ttu-id="20050-172">Устанавливает драйвер принтера из пакета драйверов, который находится в хранилище драйверов сервера печати.</span><span class="sxs-lookup"><span data-stu-id="20050-172">Installs a printer driver from a driver package that is in the print server's driver store.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20050-173"><a href="uploadprinterdriverpackage.md"><strong>уплоадпринтердриверпаккаже</strong></a></span><span class="sxs-lookup"><span data-stu-id="20050-173"><a href="uploadprinterdriverpackage.md"><strong>UploadPrinterDriverPackage</strong></a></span></span><br/></td>
<td><span data-ttu-id="20050-174">Передает драйвер принтера в хранилище драйверов сервера печати, чтобы его можно было установить путем вызова <a href="installprinterdriverfrompackage.md"><strong>инсталлпринтердриверфромпаккаже</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="20050-174">Uploads a printer driver to the print server's driver store so that it can be installed by calling <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

