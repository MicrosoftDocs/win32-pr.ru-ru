---
description: 'Дополнительные сведения о: JET_OPENTEMPORARYTABLE Members'
title: Элементы JET_OPENTEMPORARYTABLE (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: JET_OPENTEMPORARYTABLE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable_members(v=EXCHG.10)
ms:contentKeyID: 55104223
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 934ea18663e2fd2de786bb44d32482f42fd45d38b9e6ec23e73caf815560b264
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119560074"
---
# <a name="jet_opentemporarytable-members"></a>Элементы JET_OPENTEMPORARYTABLE

Включить защищенные члены  
Включить унаследованные члены  

Коллекция параметров для метода Жетопентемпораритабле.

Тип [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) предоставляет следующие члены.

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
<td><a href="dn351224(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a></td>
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
<td><a href="dn335290(v=exchg.10).md">кбкэймост</a></td>
<td>Возвращает или задает максимальный размер ключа, представляющего заданную строку. Для управления способом усечения ключей можно задать максимальный размер ключа. Усечение ключа важно, так как это может повлиять на то, что строки считаются разными. если этот параметр имеет значение 0 или 255, то максимальный размер ключа и его семантика остаются идентичными максимальному размеру ключа, поддерживаемому Windows Server 2003. Для этого параметра также можно задать большее значение в качестве функции размера страницы базы данных для экземпляра <a href="hh596135(v=exchg.10).md">датабасепажесизе</a>. Дополнительные сведения см. в разделе <a href="dn335292(v=exchg.10).md">кэймост</a> .</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn351219(v=exchg.10).md">кбварсегмак</a></td>
<td>Возвращает или задает максимальный объем данных, который будет использоваться из любой переменной ленгсколумн для создания ключа для данной строки. Этот параметр может использоваться для управления объемом ключевого пространства, используемого любым ключевым столбцом. Это ограничение указано в байтах. Если этот параметр равен нулю или имеет то же значение, что и свойство <a href="dn335290(v=exchg.10).md">кбкэймост</a> , ограничение не действует.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn335287(v=exchg.10).md">кколумн</a></td>
<td>Возвращает или задает количество столбцов в <a href="dn351228(v=exchg.10).md">пргколумндеф</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn351232(v=exchg.10).md">грбит</a></td>
<td>Возвращает или задает параметры для временной таблицы.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn335288(v=exchg.10).md">пидксуникоде</a></td>
<td>Возвращает или задает код локали и флаги нормализации, используемые для сравнения данных любого ключевого столбца Юникода во временной таблице. Если этот параметр имеет значение null, то для сравнения всех ключевых столбцов Юникода во временной таблице будет использоваться код по умолчанию. По умолчанию используется языковой стандарт «Английский (США)». Если этот параметр имеет значение null, то для сравнения данных любого ключевого столбца Юникода во временной таблице будут использоваться флаги нормализации по умолчанию. Флаги нормализации по умолчанию: NORM_IGNORECASE, NORM_IGNOREKANATYPE и NORM_IGNOREWIDTH.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn351228(v=exchg.10).md">пргколумндеф</a></td>
<td>Возвращает или задает определения столбцов для столбцов, созданных во временной таблице.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn351233(v=exchg.10).md">пргколумнид</a></td>
<td>Возвращает или задает выходной буфер, который получает массив идентификаторов столбцов, созданных во время создания временной таблицы. Идентификаторы столбцов в этом массиве будут точно соответствовать входному массиву определений столбцов. В результате размер этого буфера должен соответствовать размеру <a href="dn351228(v=exchg.10).md">пргколумндеф</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn335293(v=exchg.10).md">TableID</a></td>
<td>Возвращает маркер таблицы для временной таблицы, созданной в результате успешного вызова Жетопентемпораритабле.</td>
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
<td><a href="dn335286(v=exchg.10).md">ToString</a></td>
<td>Возвращает <a href="/dotnet/api/system.string">строку</a> , представляющую текущий <a href="dn351217(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a>. (Переопределяет <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</td>
</tr>
</tbody>
</table>


Начало

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Класс JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)
