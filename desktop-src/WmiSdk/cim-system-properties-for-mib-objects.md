---
description: WMI определяет набор системных свойств, которые связаны со всеми классами и экземплярами классов в дополнение к свойствам, зависящим от класса.
ms.assetid: ea8ca4e4-9969-48fc-9b9f-5a5c8442006d
ms.tgt_platform: multiple
title: Свойства системы CIM для объектов MIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0425afecc399c3cd1399e8bf565908b1c7c5d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712112"
---
# <a name="cim-system-properties-for-mib-objects"></a>Свойства системы CIM для объектов MIB

WMI определяет набор системных свойств, которые связаны со всеми классами и экземплярами классов в дополнение к свойствам, зависящим от класса.

> [!Note]  
> Дополнительные сведения об установке поставщика см. в разделе [Настройка среды SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

Поставщик SNMP использует следующие свойства системы CIM при сопоставлении определений объектов MIB с определениями классов CIM. Чтобы поставщик SNMP полностью разрешил объект группы, должны присутствовать обязательные свойства. Сбой определения обязательного свойства возвращает ошибку.



<table>
<thead>
<tr class="header">
<th>Свойство</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>__CLASS</strong></td>
<td><strong>строка</strong> Заполнен<br/> Для экземпляров — класс, которому принадлежит объект. Для классов это имя класса.<br/></td>
</tr>
<tr class="even">
<td><strong>__DYNASTY</strong></td>
<td><strong>строка</strong> Используемых<br/> Имя класса, который является конечным базовым классом для текущего объекта (не его непосредственным родительским классом).<br/></td>
</tr>
<tr class="odd">
<td><strong>__GENUS</strong></td>
<td><strong>UInt32</strong> Заполнен<br/> Тип объекта. Доступны следующие значения:<br/> <dl> 1 = класс<br />
2 = экземпляр<br />
</dl></td>
</tr>
<tr class="even">
<td><strong>__NAMESPACE</strong></td>
<td><strong>строка</strong> Заполнен<br/> Пространство имен, в котором находится объект.<br/></td>
</tr>
<tr class="odd">
<td><strong>__PATH</strong></td>
<td><strong>строка</strong> Заполнен<br/> Абсолютный путь к объекту.<br/></td>
</tr>
<tr class="even">
<td><strong>__PROPERTYCOUNT</strong></td>
<td><strong>UInt32</strong> Заполнен<br/> Количество несистемных свойств, определенных для объекта.<br/></td>
</tr>
<tr class="odd">
<td><strong>__RELPATH</strong></td>
<td><strong>строка</strong> Заполнен<br/> Относительный путь к объекту.<br/></td>
</tr>
<tr class="even">
<td><strong>__SERVER</strong></td>
<td><strong>строка</strong> Заполнен<br/> Сервер, предоставляющий объект.<br/></td>
</tr>
<tr class="odd">
<td><strong>__SUPERCLASS</strong></td>
<td><strong>строка</strong> Используемых<br/> Непосредственный родительский класс объекта.<br/></td>
</tr>
</tbody>
</table>



 

 

 




