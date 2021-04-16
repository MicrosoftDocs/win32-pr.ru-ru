---
description: 'Дополнительные сведения: методы транзакций'
title: 'Методы транзакции '
TOCTitle: Transaction methods
ms:assetid: Methods.T:Microsoft.Isam.Esent.Interop.Transaction
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction_methods(v=EXCHG.10)
ms:contentKeyID: 55104163
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: c926d00f785aab3a63cd8ebc7eebaf74ea5f0e23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104570391"
---
# <a name="transaction-methods"></a>Методы транзакции 

Включить защищенные члены  
Включить унаследованные члены  

Тип [транзакции](./transaction-class.md) предоставляет следующие члены.

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
<td><a href="dn351172(v=exchg.10).md">Начать</a></td>
<td>Начать транзакцию. В настоящее время этот объект не должен находиться в транзакции.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="dn350541(v=exchg.10).md">чеккобжектиснотдиспосед</a></td>
<td>Создать исключение, если этот объект был удален. (Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="dn351179(v=exchg.10).md">Commit (Коммиттрансактионгрбит)</a></td>
<td>Фиксация транзакции. Этот объект должен находиться в транзакции.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="dn351243(v=exchg.10).md">Commit (Коммиттрансактионгрбит, TimeSpan, JET_COMMIT_ID)</a></td>
<td>Фиксация транзакции. Этот объект должен находиться в транзакции.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="dn350553(v=exchg.10).md">Dispose ()</a></td>
<td>Удаляет этот объект, освобождая базовый ресурс ESENT. (Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="dn350543(v=exchg.10).md">Dispose (логическое значение)</a></td>
<td>Вызывается методом Dispose и методом завершения. (Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Равно</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="dn350552(v=exchg.10).md">Finalize</a></td>
<td>Завершает экземпляр класса Есентресаурце. (Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</td>
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
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="dn351176(v=exchg.10).md">релеасересаурце</a></td>
<td>Вызывается, когда транзакция удаляется в активном состоянии. Эта операция должна откатить транзакцию. (Переопределяет <a href="dn350545(v=exchg.10).md">есентресаурце. релеасересаурце ()</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="dn350576(v=exchg.10).md">ресаурцевасаллокатед</a></td>
<td>Вызывается подклассом при выделении ресурса. (Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="dn350577(v=exchg.10).md">ресаурцевасрелеасед</a></td>
<td>Вызывается подклассом при освобождении ресурса. (Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="dn351244(v=exchg.10).md">Откат</a></td>
<td>Откат транзакции. Этот объект должен находиться в транзакции.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="dn351181(v=exchg.10).md">ToString</a></td>
<td>Возвращает <a href="/dotnet/api/system.string">строку</a> , представляющую текущую <a href="dn351174(v=exchg.10).md">транзакцию</a>. (Переопределяет <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</td>
</tr>
</tbody>
</table>


Начало

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[класс Transaction](./transaction-class.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
