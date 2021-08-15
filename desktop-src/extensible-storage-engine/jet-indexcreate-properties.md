---
description: 'Дополнительные сведения о: JET_INDEXCREATE свойствах'
title: Свойства JET_INDEXCREATE
TOCTitle: JET_INDEXCREATE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate_properties(v=EXCHG.10)
ms:contentKeyID: 55103645
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 0669d00b9c28e5299c5b9f55f0931ec7d22921eddad5e2b6b4876199057d111d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118254271"
---
# <a name="jet_indexcreate-properties"></a>Свойства JET_INDEXCREATE

Включить защищенные члены  
Включить унаследованные члены  

Тип [JET_INDEXCREATE](./jet-indexcreate-class.md) предоставляет следующие члены.

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
<td>Возвращает или задает максимально допустимый размер (в байтах) для ключей в индексе. Минимальный поддерживаемый максимальный размер ключа — JET_cbKeyMostMin (255), который является устаревшим максимальным размером ключа. Максимальный размер ключа зависит от размера страницы базы данных <a href="hh596135(v=exchg.10).md">датабасепажесизе</a>. Максимальный размер ключа можно получить с помощью <a href="dn351156(v=exchg.10).md">кэймост</a>. этот параметр пропускается в Windows XP и Windows Server 2003. В отличие от неуправляемого API, <strong>индекскэймост ()</strong> (JET_bitIndexKeyMost) не требуется, он будет добавлен автоматически.</td>
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

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс JET_INDEXCREATE](./jet-indexcreate-class.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
