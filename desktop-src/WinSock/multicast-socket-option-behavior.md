---
description: На этой странице описывается поведение параметров сокета многоадресной рассылки в зависимости от различных состояний параметров сокета.
ms.assetid: a411e831-7b28-4ab5-a09a-650db99a7cd5
title: Поведение параметра сокета многоадресной рассылки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fd10094750bea59b844ad1fcdac70be0c7f9646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072742"
---
# <a name="multicast-socket-option-behavior"></a>Поведение параметра сокета многоадресной рассылки

На этой странице описывается поведение параметров сокета многоадресной рассылки в зависимости от различных состояний параметров сокета.

Например, на этой странице описывается поведение, когда \_ \_ параметр сокета членства в источнике для IP-адреса \_ установлен на сокете, для которого параметр IP-адрес \_ добавления \_ \_ членства уже установлен с указанной парой Group/Source в том же сетевом интерфейсе. Ему разрешается вызывать членство в IP-адресе для \_ \_ \_ одной и той же группы в другом сетевом интерфейсе.

Эта страница помогает правильно разрабатывать и устранять неполадки многоадресных приложений сокетов Windows. 

<table>
<thead>
<tr class="header">
<th>Начальный параметр сокета</th>
<th>Конфликт последующего параметра сокета</th>
<th>Возвращена ошибка</th>
<th>Комментарии</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4">IP_ADD_MEMBERSHIP $ {REMOVE} $<br />
</td>
<td>IP_ADD_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Не вызывайте IP_ADD_MEMBERSHIP с одной и той же группой более одного раза в одном сетевом интерфейсе.</td>
</tr>
<tr class="even">
<td>IP_ADD_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Не вызывайте IP_ADD_SOURCE_MEMBERSHIP с той же группой, которая ранее вызывалась с IP_ADD_MEMBERSHIP в одном сетевом интерфейсе.</td>

</tr>
<tr class="odd">
<td>IP_DROP_SOURCE_MEMBERSHIP</td>
<td>всаеинвал</td>
<td>Вместо этого используйте IP_BLOCK_SOURCE.</td>

</tr>
<tr class="even">
<td>IP_UNBLOCK_SOURCE</td>
<td>всаеинвал</td>
<td>Возвращает ошибку при попытке разблокировать пару "Группа-источник", которая ранее не была заблокирована в том же сетевом интерфейсе.</td>

</tr>
<tr class="odd">
<td>IP_DROP_MEMBERSHIP</td>
<td>Любой последующий вызов в той же группе или группе, либо к исходной паре</td>
<td>всаеинвал</td>
<td>Выполнение вызовов параметра сокета для группы или группы или исходной пары, не находящихся в списке включения (из-за удаления членства или других), приводит к ошибке.</td>
</tr>
<tr class="even">
<td rowspan="3">IP_ADD_SOURCE_MEMBERSHIP $ {REMOVE} $<br />
</td>
<td>IP_ADD_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Не вызывайте IP_ADD_MEMBERSHIP с той же группой, которая ранее вызывалась с IP_ADD_SOURCE_MEMBERSHIP в одном сетевом интерфейсе.</td>
</tr>
<tr class="odd">
<td>IP_ADD_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Не вызывайте IP_ADD_SOURCE_MEMBERSHIP с той же группой или исходной парой, которая ранее вызывалась с IP_ADD_SOURCE_MEMBERSHIP в одном сетевом интерфейсе.</td>

</tr>
<tr class="even">
<td>IP_UNBLOCK_SOURCE</td>
<td>всаеинвал</td>
<td>Возвращает ошибку при попытке разблокировать пару "Группа-источник", которая ранее не была заблокирована в том же сетевом интерфейсе.</td>

</tr>
<tr class="odd">
<td rowspan="2">IP_DROP_SOURCE_MEMBERSHIP $ {REMOVE} $<br />
</td>
<td>IP_UNBLOCK_SOURCE</td>
<td>всаеинвал</td>
<td>Возвращает ошибку при попытке разблокировать пару "Группа-источник", которая ранее не была заблокирована в том же сетевом интерфейсе.</td>
</tr>
<tr class="even">
<td>IP_DROP_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Возвращает ошибку при попытке удалить пару "Группа-источник", которая не находится в списке включения в том же сетевом интерфейсе.</td>

</tr>
<tr class="odd">
<td rowspan="3">IP_BLOCK_SOURCE $ {REMOVE} $<br />
</td>
<td>IP_BLOCK_SOURCE</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Возвращает ошибку при попытке заблокировать пару "Группа-источник", которая уже заблокирована в том же сетевом интерфейсе.</td>
</tr>
<tr class="even">
<td>IP_ADD_SOURCE_MEMBERSHIP</td>
<td>всаеинвал</td>
<td>Вместо этого используйте IP_UNBLOCK_SOURCE.</td>

</tr>
<tr class="odd">
<td>IP_ADD_MEMBERSHIP</td>
<td>всаеинвал</td>
<td>Вместо этого используйте IP_UNBLOCK_SOURCE.</td>

</tr>
<tr class="even">
<td>IP_UNBLOCK_SOURCE</td>
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Возвращает ошибку при попытке разблокировать пару "Группа-источник", которая не находится в списке заблокированных в том же сетевом интерфейсе.</td>
</tr>
</tbody>
</table>



 

 

 



