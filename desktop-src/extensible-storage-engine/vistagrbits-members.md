---
description: 'Дополнительные сведения о: Вистагрбитс Members'
title: Элементы Вистагрбитс (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: VistaGrbits members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits_members(v=EXCHG.10)
ms:contentKeyID: 55104213
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 56145954b504f086ff36fbe84ea26768b8e3636a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104559777"
---
# <a name="vistagrbits-members"></a>Элементы Вистагрбитс

Включить защищенные члены  
Включить унаследованные члены  

Грбитс, которые были добавлены в версию ESENT для Windows Vista.

Тип [вистагрбитс](./vistagrbits-class.md) предоставляет следующие члены.

## <a name="fields"></a>Поля

<table>
<thead>
<tr class="header">
<th> </th>
<th>name</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn351283(v=exchg.10).md">континуеафтерсав</a></td>
<td>Сеанс моментального снимка продолжится после Жетосснапшотсав и потребуется вызов функции Жетосснапшотенд.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn335364(v=exchg.10).md">индекскросспродукт</a></td>
<td>Если задать этот флаг для индекса, имеющего более одного ключевого столбца, который является многозначным, будет создана запись индекса для каждого результата перекрестного произведения всех значений в этих ключевых столбцах. В противном случае индекс будет иметь только одну запись для каждого многозначного ключевого столбца, который является многозначным столбцом, и каждая из этих элементов индекса будет использовать первое Многозначное значение из любых других ключевых столбцов, которые являются многозначными столбцами. Например, если вы указали этот флаг для индекса по столбцу A, который имеет значения &quot; Red &quot; и &quot; Blue, &quot; а столбец B имеет значения &quot; 1 и 2, то будут &quot; &quot; &quot; созданы следующие записи индекса: &quot; Red &quot; , &quot; 1 &quot; ; &quot; красный &quot; , &quot; 2 &quot; ; &quot; синий &quot; , &quot; 1 &quot; ; &quot; синий &quot; , &quot; 2 &quot; . В противном случае будут созданы следующие записи индекса: &quot; Red &quot; , &quot; 1 &quot; ; &quot; синий &quot; , &quot; 1 &quot; .</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn335368(v=exchg.10).md">индексдисалловтрункатион</a></td>
<td>При указании этого флага любое обновление индекса приведет к сбою усечения ключа с <a href="hh564840(v=exchg.10).md">кэйтрункатед</a>. В противном случае ключи будут обрезаны без уведомления.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn351285(v=exchg.10).md">индекснестедтабле</a></td>
<td>Индексировать несколько столбцов с несколькими значениями, но только со значениями одного Итагсекуенце.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn335282(v=exchg.10).md">логстреаммустексист</a></td>
<td>Журналы транзакций должны находиться в каталоге файла журнала (т. е. не может автоматически запустить новый поток).</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn335367(v=exchg.10).md">рековеривисаутундо</a></td>
<td>Выполните восстановление, но остановите на этапе отката. Позволяет воспроизводить все журналы, а позднее можно копировать и воспроизводить дополнительные журналы.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn335375(v=exchg.10).md">реплаймиссингмапентридб</a></td>
<td>Отсутствует запись схемы базы данных по умолчанию в то же расположение.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn335283(v=exchg.10).md">трункатедоне</a></td>
<td>Подсистема может пометить заголовки базы данных соответствующим образом (например, завершить полное резервное копирование), даже если вызов truncate не был завершен.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn335371(v=exchg.10).md">трункателогсафтеррековери</a></td>
<td>При успешном обратимом восстановлении усечение файлов журнала.</td>
</tr>
</tbody>
</table>


Начало

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Вистагрбитс](./vistagrbits-class.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)
