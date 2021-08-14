---
description: 'Дополнительные сведения о: Server2003Grbits Fields'
title: Поля Server2003Grbits (Microsoft. ISAM. ESENT. Interop. server2003)
TOCTitle: Server2003Grbits fields
ms:assetid: Fields.T:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits_fields(v=EXCHG.10)
ms:contentKeyID: 55104210
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 77db94da9f3a5dbec982b31c0ea3d673ffb6228a58f81adf644ff498a2cf4f84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118071676"
---
# <a name="server2003grbits-fields"></a>Поля Server2003Grbits

Включить защищенные члены  
Включить унаследованные члены  

Тип [Server2003Grbits](./server2003grbits-class.md) предоставляет следующие члены.

## <a name="fields"></a>Поля

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
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn351203(v=exchg.10).md">енумератеигнореусердефинеддефаулт</a></td>
<td>Если данный столбец отсутствует в записи и имеет определенное пользователем значение по умолчанию, значение столбца не будет возвращено. Этот параметр предотвратит вызов функции обратного вызова, которая будет вычислять определенное пользователем значение по умолчанию для столбца, при перечислении значений для этого столбца.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn351284(v=exchg.10).md">форвардонли</a></td>
<td>Этот параметр запрашивает создание временной таблицы только в том случае, если диспетчер временных таблиц может использовать реализацию, оптимизированную для промежуточных результатов запроса. Если любая характеристика временной таблицы не позволит использовать эту оптимизацию, операция завершится с JET_errCannotMaterializeForwardOnlySort. Побочный результат этого параметра — Разрешить временной таблице содержать записи с повторяющимися ключами индекса. Дополнительные сведения см. в разделе <a href="hh558517(v=exchg.10).md">UNIQUE</a> .</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></td>
<td>Все транзакции, ранее зафиксированные любым сеансом, которые еще не были сброшены в файл журнала транзакций, будут сброшены немедленно. Этот API будет ожидать, пока транзакции не будут сброшены перед возвратом в вызывающий объект. Этот параметр может использоваться, даже если сеанс в данный момент не находится в транзакции. Этот параметр нельзя использовать в сочетании с любым другим параметром.</td>
</tr>
</tbody>
</table>


Начало

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Server2003Grbits](./server2003grbits-class.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop. server2003](./microsoft.isam.esent.interop.server2003-namespace.md)
