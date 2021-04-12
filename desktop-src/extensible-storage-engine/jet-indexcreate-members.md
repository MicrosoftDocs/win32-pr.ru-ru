---
description: 'Дополнительные сведения о: JET_INDEXCREATE Members'
title: Элементы JET_INDEXCREATE
TOCTitle: JET_INDEXCREATE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate_members(v=EXCHG.10)
ms:contentKeyID: 55103641
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: cbe9ce962221db30c8cdae90461fa55fc0baea19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272125"
---
# <a name="jet_indexcreate-members"></a>Элементы JET_INDEXCREATE

Включить защищенные члены  
Включить унаследованные члены  

Содержит сведения, необходимые для создания индекса по данным в базе данных ESE. Содержит сведения, необходимые для создания индекса по данным в базе данных ESE.

Тип [JET_INDEXCREATE](./jet-indexcreate-class.md) предоставляет следующие члены.

## <a name="constructors"></a>Конструкторы

<table>
<thead>
<tr class="header">
<th> </th>
<th>Имя</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="dn335115(v=exchg.10).md">JET_INDEXCREATE</a></td>
<td></td>
</tr>
</tbody>
</table>


Начало

## <a name="properties"></a>Свойства

<table>
<thead>
<tr class="header">
<th> </th>
<th>Имя</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn335122(v=exchg.10).md">cbKey</a></td>
<td>Возвращает или задает длину (в символах) Сзкэй, включая два завершающих значения NULL.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn335156(v=exchg.10).md">кбкэймост</a></td>
<td>Возвращает или задает максимально допустимый размер (в байтах) для ключей в индексе. Минимальный поддерживаемый максимальный размер ключа — JET_cbKeyMostMin (255), который является устаревшим максимальным размером ключа. Максимальный размер ключа зависит от размера страницы базы данных <a href="hh596135(v=exchg.10).md">датабасепажесизе</a>. Максимальный размер ключа можно получить с помощью <a href="dn351156(v=exchg.10).md">кэймост</a>. Этот параметр не учитывается в Windows XP и Windows Server 2003. В отличие от неуправляемого API, <strong>индекскэймост ()</strong> (JET_bitIndexKeyMost) не требуется, он будет добавлен автоматически.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn335158(v=exchg.10).md">кбварсегмак</a></td>
<td>Возвращает или задает максимальную длину (в байтах) каждого столбца для хранения в индексе.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn335118(v=exchg.10).md">ккондитионалколумн</a></td>
<td>Возвращает или задает количество условных столбцов.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn335157(v=exchg.10).md">Err</a></td>
<td>Возвращает или задает код ошибки из создания этого индекса.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn335119(v=exchg.10).md">грбит</a></td>
<td>Возвращает или задает параметры создания индекса.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn335159(v=exchg.10).md">пидксуникоде</a></td>
<td>Возвращает или задает необязательные параметры сравнения Юникода.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn335120(v=exchg.10).md">пспацехинтс</a></td>
<td>Возвращает или задает размещение, Обслуживание и указания по использованию пространства.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn335160(v=exchg.10).md">ргкондитионалколумн</a></td>
<td>Возвращает или задает необязательные условные столбцы.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn335121(v=exchg.10).md">сзиндекснаме</a></td>
<td>Возвращает или задает имя создаваемого индекса.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn335161(v=exchg.10).md">сзкэй</a></td>
<td>Возвращает или задает описание ключа индекса. Это строка токенов с разделителями null, заканчивающаяся символом двойной точности null. Каждый маркер имеет форму [Direction-name], где параметр Direction-Specification имеет значение &quot; + &quot; или &quot; - &quot; . Например, Сзкэй &quot; + abc\0-def\0 + ghi\0 &quot; будет индексировать три столбца &quot; ABC &quot; (в порядке возрастания), &quot; DEF &quot; (в убывающем порядке) и &quot; GHI &quot; (в порядке возрастания).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn335162(v=exchg.10).md">улденсити</a></td>
<td>Возвращает или задает плотность индекса.</td>
</tr>
</tbody>
</table>


Начало

## <a name="methods"></a>Методы

<table>
<thead>
<tr class="header">
<th> </th>
<th>Имя</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="dn335116(v=exchg.10).md">контентекуалс</a></td>
<td>Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="dn335153(v=exchg.10).md">дипклоне</a></td>
<td>Возвращает глубокую копию объекта.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Равно</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">мембервисеклоне</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="dn335154(v=exchg.10).md">ToString</a></td>
<td>Создает строковое представление экземпляра. (Переопределяет <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</td>
</tr>
</tbody>
</table>


Начало

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс JET_INDEXCREATE](./jet-indexcreate-class.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
