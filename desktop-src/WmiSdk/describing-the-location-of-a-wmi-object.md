---
description: По сути, аналогично URL-адресу, путь к объекту WMI представляет собой строку, однозначно определяющую пространство имен на сервере, класс в пространстве имен или экземпляры класса.
ms.assetid: 7a390541-609d-4b97-b91c-1a41d21ec17d
ms.tgt_platform: multiple
title: Описание расположения объекта WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b58b58a6b668955d6eba1e4c51f6f8dccdac890
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711738"
---
# <a name="describing-the-location-of-a-wmi-object"></a>Описание расположения объекта WMI

По сути, аналогично URL-адресу, путь к объекту WMI представляет собой строку, однозначно определяющую пространство имен на сервере, класс в пространстве имен или экземпляры класса. Путь к объекту является иерархическим и содержит несколько элементов, описывающих расположение рассматриваемого объекта. Как и пути к файлам, пути к объектам WMI можно описать в полном или указанном виде относительного пути.

Пространство имен WMI-объекта указано на справочной странице инструментария WMI. Например, расположение большинства классов, поддерживаемых [поставщиками WMI CIMWin32](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers) , находится в \\ корневом \\ пространстве имен CIMV2. Следующий код PowerShell описывает вызов для получения объекта [**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) на локальном компьютере:

`Get-WmiObject -Class Win32_ComputerSystem -Namespace "root\cimv2" -ComputerName "."`

Кроме того, конкретный экземпляр логического диска [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) может иметь следующий путь из свойства [**SWbemObject. Path \_**](swbemobject-path-.md) .

`\\Machine1\root\cimv2:Win32_LogicalDisk.DeviceID="C:"`

В следующем примере показан относительный путь к этому экземпляру, как показано при отображении свойства [**релпас**](swbemobjectpath-relpath.md) объекта [**свбемобжектпас**](swbemobjectpath.md) , возвращенного вызовом [**SWbemObject. Path \_**](swbemobject-path-.md).

`Win32_LogicalDisk.DeviceID="A:"`

Обратите внимание, что **DeviceID** является ключевым свойством класса [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .

## <a name="c"></a>C++

В следующей таблице перечислены типы путей к объектам и связанные с ними методы, требующие путей к объектам.



<table>
<thead>
<tr class="header">
<th>Тип пути к объекту</th>
<th>Метод</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="describing-a-wmi-namespace-object-path.md">Пространство имен</a></td>
<td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-opennamespace"><strong>IWbemServices:: OpenNamespace</strong></a><br />
</dl></td>
</tr>
<tr class="even">
<td><a href="describing-a-class-object-path.md">Класс</a></td>
<td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod"><strong>IWbemServices:: ExecMethod</strong></a><br />
[<strong>IWbemServices:: ексекмесодасинк</strong>] (/Виндовс/десктоп/АПИ/вбемкли/НФ-вбемкли-ивбемсервицес-ексекмесодасинк)<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="describing-a-class-object-path.md">Класс</a> или <a href="describing-an-instance-object-path.md">экземпляр</a></td>
<td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject"><strong>IWbemServices:: GetObject</strong></a><br />
[<strong>IWbemServices:: жетобжектасинк</strong>] (/Виндовс/десктоп/АПИ/вбемкли/НФ-вбемкли-ивбемсервицес-жетобжектасинк)<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="describing-an-instance-object-path.md">Экземпляр</a></td>
<td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance"><strong>IWbemServices::D Елетеинстанце</strong></a><br />
[<strong>IWbemServices::D елетеинстанцеасинк</strong>] (/Виндовс/десктоп/АПИ/вбемкли/НФ-вбемкли-ивбемсервицес-делетеинстанцеасинк)<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="script"></a>Скрипт

Пути к объектам могут быть созданы несколькими способами:

-   Получите свойство метода, который возвращает объект [**свбемобжектпас**](swbemobjectpath.md) .
-   Получите свойство [**SWbemObject. Path \_**](swbemobject-path-.md) .
-   Создайте строковую переменную, содержащую путь к объекту.

В следующей таблице перечислены объекты скрипта, для которых требуются пути к объектам.



<table>
<thead>
<tr class="header">
<th>Объект скрипта</th>
<th>Метод</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="swbemservices.md"><strong>SWbemServices</strong></a></td>
<td><dl><a href="swbemservices-associatorsof.md"><strong>ассоЦиаторсоф</strong></a><br />
[<strong>АссоЦиаторсофасинк</strong>] (swbemservices-associatorsofasync.md)<br />
[<strong>Удалить</strong>] (swbemservices-delete.md)<br />
[<strong>DeleteAsync</strong>] (swbemservices-deleteasync.md)<br />
[<strong>ExecMethod</strong>] (swbemservices-execmethod.md)<br />
[<strong>Ексекмесодасинк</strong>] (swbemservices-execmethodasync.md)<br />
[<strong>Get</strong>] (swbemservices-get.md)<br />
[<strong>Async</strong>] (swbemservices-getasync.md)<br />
[<strong>Референцесто</strong>] (swbemservices-referencesto.md)<br />
[<strong>Референцестоасинк</strong>] (swbemservices-referencestoasync.md)<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="swbemobjectset.md"><strong>SWbemObjectSet</strong></a></td>
<td><dl><a href="swbemobjectset-item.md"><strong>Элемент</strong></a><br />
</dl></td>
</tr>
</tbody>
</table>



 

 

 
