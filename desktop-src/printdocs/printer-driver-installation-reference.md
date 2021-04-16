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
# <a name="printer-driver-installation-reference"></a>Справочник по установке драйвера принтера

Функции в этом разделе устанавливают и настраивают драйверы принтеров на компьютере.

## <a name="in-this-section"></a>Содержание раздела



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Функция</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="addmonitor.md"><strong>аддмонитор</strong></a><br/></td>
<td>Функция <a href="/windows/desktop/printdocs/addmonitor"><strong>аддмонитор</strong></a> устанавливает монитор локального порта и связывает файлы конфигурации, данных и монитора.<br/></td>
</tr>
<tr class="even">
<td><a href="addport.md"><strong>AddPort</strong></a><br/></td>
<td>Функция <a href="/windows/desktop/printdocs/addport"><strong>аддпорт</strong></a> добавляет имя порта в список поддерживаемых портов. Функция <strong>аддпорт</strong> экспортируется монитором порта.<br/></td>
</tr>
<tr class="odd">
<td><a href="addprinterdriver.md"><strong>аддпринтердривер</strong></a><br/></td>
<td>Функция <a href="/windows/desktop/printdocs/addprinterdriver"><strong>аддпринтердривер</strong></a> устанавливает локальный или удаленный драйвер принтера и связывает файлы конфигурации, данных и драйверов.<br/> Для большей гибкости при установке или обновлении драйверов принтеров используйте функцию <a href="addprinterdriverex.md"><strong>аддпринтердриверекс</strong></a> , так как она обеспечивает жесткое обновление, более пониженную версию, копирование только новых файлов и копирование всех файлов (независимо от отметки времени файла).<br/>
<blockquote>
[!Note]<br />
Установка драйвера принтера без пакета драйверов больше не рекомендуется. Вместо этого используйте <a href="installprinterdriverfrompackage.md"><strong>инсталлпринтердриверфромпаккаже</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="addprinterdriverex.md"><strong>аддпринтердриверекс</strong></a><br/></td>
<td>Функция <a href="/windows/desktop/printdocs/addprinterdriverex"><strong>аддпринтердриверекс</strong></a> устанавливает локальный или удаленный драйвер принтера и связывает файлы конфигурации, данных и драйверов. Помимо возможностей <a href="addprinterdriver.md"><strong>аддпринтердривер</strong></a>, у нее также есть параметры, обеспечивающие жесткое обновление, более пониженную версию, копирование только новых файлов и копирование всех файлов (независимо от отметки времени файла).<br/>
<blockquote>
[!Note]<br />
Установка драйвера принтера без пакета драйверов больше не рекомендуется. Вместо этого используйте <a href="installprinterdriverfrompackage.md"><strong>инсталлпринтердриверфромпаккаже</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="addprintprocessor.md"><strong>аддпринтпроцессор</strong></a><br/></td>
<td>Функция <a href="/windows/desktop/printdocs/addprintprocessor"><strong>аддпринтпроцессор</strong></a> устанавливает обработчик заданий печати на указанном сервере и добавляет имя обработчика печати в список поддерживаемых обработчиков печати.<br/></td>
</tr>
<tr class="even">
<td><a href="addprintprovidor.md"><strong>аддпринтпровидор</strong></a><br/></td>
<td>Функция <a href="/windows/desktop/printdocs/addprintprovidor"><strong>аддпринтпровидор</strong></a> устанавливает локальный поставщик печати и связывает файлы конфигурации, данных и поставщика.<br/></td>
</tr>
<tr class="odd">
<td><a href="coreprinterdriverinstalled.md"><strong>корепринтердриверинсталлед</strong></a><br/></td>
<td>Функция <a href="/windows/desktop/printdocs/coreprinterdriverinstalled"><strong>корепринтердриверинсталлед</strong></a> сообщает, установлен ли основной драйвер принтера с указанными GUID, датой и версией.<br/></td>
</tr>
<tr class="even">
<td><a href="deletemonitor.md"><strong>делетемонитор</strong></a><br/></td>
<td>Функция <a href="/windows/desktop/printdocs/deletemonitor"><strong>делетемонитор</strong></a> удаляет монитор портов, добавленный функцией <a href="addmonitor.md"><strong>аддмонитор</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="deleteport.md"><strong>делетепорт</strong></a><br/></td>
<td>Функция <a href="/windows/desktop/printdocs/deleteport"><strong>делетепорт</strong></a> отображает диалоговое окно, позволяющее пользователю удалить имя порта.<br/></td>
</tr>
<tr class="even">
<td><a href="deleteprinterdriver.md"><strong>делетепринтердривер</strong></a><br/></td>
<td>Функция <a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>делетепринтердривер</strong></a> удаляет указанное имя драйвера принтера из списка имен поддерживаемых драйверов на сервере.<br/> Чтобы удалить файлы, связанные с драйвером, помимо удаления указанного имени драйвера принтера из списка имен поддерживаемых драйверов для сервера, используйте функцию <a href="deleteprinterdriverex.md"><strong>делетепринтердриверекс</strong></a> .<br/> <a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>Делетепринтердривер</strong></a> удаляет драйвер, только если для указанной среды не используется ни одна версия драйвера. <a href="deleteprinterdriverex.md"><strong>Делетепринтердриверекс</strong></a> может удалять определенные версии драйвера.<br/></td>
</tr>
<tr class="odd">
<td><a href="deleteprinterdriverex.md"><strong>делетепринтердриверекс</strong></a><br/></td>
<td>Функция <a href="/windows/desktop/printdocs/deleteprinterdriverex"><strong>делетепринтердриверекс</strong></a> удаляет указанное имя драйвера принтера из списка имен поддерживаемых драйверов на сервере и удаляет файлы, связанные с драйвером. Эта функция также может удалять определенные версии драйвера.<br/></td>
</tr>
<tr class="even">
<td><a href="deleteprinterdriverpackage.md"><strong>делетепринтердриверпаккаже</strong></a><br/></td>
<td>Удаляет пакет драйвера принтера из хранилища драйверов.<br/></td>
</tr>
<tr class="odd">
<td><a href="deleteprintprocessor.md"><strong>делетепринтпроцессор</strong></a><br/></td>
<td>Функция <a href="/windows/desktop/printdocs/deleteprintprocessor"><strong>делетепринтпроцессор</strong></a> удаляет обработчик печати, добавленный функцией <a href="addprintprocessor.md"><strong>аддпринтпроцессор</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="deleteprintprovidor.md"><strong>делетепринтпровидор</strong></a><br/></td>
<td>Функция <a href="/windows/desktop/printdocs/deleteprintprovidor"><strong>делетепринтпровидор</strong></a> Удаляет поставщика печати, добавленного функцией <a href="addprintprovidor.md"><strong>аддпринтпровидор</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="enummonitors.md"><strong>енуммониторс</strong></a><br/></td>
<td>Функция <a href="/windows/desktop/printdocs/enummonitors"><strong>енуммониторс</strong></a> извлекает сведения о мониторах портов, установленных на указанном сервере.<br/></td>
</tr>
<tr class="even">
<td><a href="enumports.md"><strong>EnumPorts</strong></a><br/></td>
<td>Функция <a href="/windows/desktop/printdocs/enumports"><strong>енумпортс</strong></a> перечисляет порты, доступные для печати на указанном сервере.<br/></td>
</tr>
<tr class="odd">
<td><a href="enumprinterdrivers.md"><strong>енумпринтердриверс</strong></a><br/></td>
<td>Функция <a href="/windows/desktop/printdocs/enumprinterdrivers"><strong>енумпринтердриверс</strong></a> перечисляет драйверы принтера, установленные на указанном сервере принтера.<br/></td>
</tr>
<tr class="even">
<td><a href="enumprintprocessordatatypes.md"><strong>енумпринтпроцессордататипес</strong></a><br/></td>
<td>Функция <a href="/windows/desktop/printdocs/enumprintprocessordatatypes"><strong>енумпринтпроцессордататипес</strong></a> перечисляет типы данных, поддерживаемые указанным обработчиком печати.<br/></td>
</tr>
<tr class="odd">
<td><a href="enumprintprocessors.md"><strong>енумпринтпроцессорс</strong></a><br/></td>
<td>Функция <a href="/windows/desktop/printdocs/enumprintprocessors"><strong>енумпринтпроцессорс</strong></a> перечисляет обработчики печати, установленные на указанном сервере.<br/></td>
</tr>
<tr class="even">
<td><a href="getcoreprinterdrivers.md"><strong>жеткорепринтердриверс</strong></a><br/></td>
<td>Извлекает GUID, версию и дату указанных основных драйверов принтера и путь к их пакетам.<br/></td>
</tr>
<tr class="odd">
<td><a href="getprinterdriver.md"><strong>жетпринтердривер</strong></a><br/></td>
<td>Функция <a href="/windows/desktop/printdocs/getprinterdriver"><strong>жетпринтердривер</strong></a> извлекает данные драйвера для указанного принтера. Если драйвер не установлен на локальном компьютере, <strong>жетпринтердривер</strong> устанавливает его.<br/></td>
</tr>
<tr class="even">
<td><a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a><br/></td>
<td>Функция <a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a> извлекает данные драйвера для указанного принтера. Если драйвер не установлен на локальном компьютере, <strong>GetPrinterDriver2</strong> устанавливает его и отображает в указанном окне любой пользовательский интерфейс.<br/></td>
</tr>
<tr class="odd">
<td><a href="getprinterdriverdirectory.md"><strong>жетпринтердривердиректори</strong></a><br/></td>
<td>Функция <a href="/windows/desktop/printdocs/getprinterdriverdirectory"><strong>жетпринтердривердиректори</strong></a> извлекает путь к каталогу драйвера принтера.<br/></td>
</tr>
<tr class="even">
<td><a href="getprinterdriverpackagepath.md"><strong>жетпринтердриверпаккажепас</strong></a><br/></td>
<td>Извлекает путь к указанному пакету драйвера принтера на сервере печати.<br/></td>
</tr>
<tr class="odd">
<td><a href="getprintprocessordirectory.md"><strong>жетпринтпроцессордиректори</strong></a><br/></td>
<td>Функция <a href="/windows/desktop/printdocs/getprintprocessordirectory"><strong>жетпринтпроцессордиректори</strong></a> извлекает путь к каталогу обработчика печати на указанном сервере.<br/></td>
</tr>
<tr class="even">
<td><a href="installprinterdriverfrompackage.md"><strong>инсталлпринтердриверфромпаккаже</strong></a><br/></td>
<td>Устанавливает драйвер принтера из пакета драйверов, который находится в хранилище драйверов сервера печати.<br/></td>
</tr>
<tr class="odd">
<td><a href="uploadprinterdriverpackage.md"><strong>уплоадпринтердриверпаккаже</strong></a><br/></td>
<td>Передает драйвер принтера в хранилище драйверов сервера печати, чтобы его можно было установить путем вызова <a href="installprinterdriverfrompackage.md"><strong>инсталлпринтердриверфромпаккаже</strong></a>.<br/></td>
</tr>
</tbody>
</table>



 

 

