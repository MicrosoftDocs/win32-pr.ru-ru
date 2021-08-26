---
description: 'Дополнительные сведения о: JET_OPENTEMPORARYTABLE свойствах'
title: Свойства JET_OPENTEMPORARYTABLE (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: JET_OPENTEMPORARYTABLE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable_properties(v=EXCHG.10)
ms:contentKeyID: 55104127
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: cbba2937283ab9a3d008d3bad04329d1fd42b84e0de4a1a42e2e100d99a03854
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016724"
---
# <a name="jet_opentemporarytable-properties"></a>Свойства JET_OPENTEMPORARYTABLE

Включить защищенные члены  
Включить унаследованные члены  

Тип [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) предоставляет следующие члены.

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

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Класс JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)
