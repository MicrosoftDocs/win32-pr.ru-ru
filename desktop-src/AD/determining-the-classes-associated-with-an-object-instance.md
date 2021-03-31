---
title: Определение классов, связанных с экземпляром объекта
description: Каждый объект в домен Active Directory Services имеет два атрибута, значения которых указывают иерархию классов объектов, экземпляром которых является объект.
ms.assetid: bb46f165-8c6e-4af1-b387-e0e30a4c6226
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67bc3fe900170e4a856d996f7e373918f242df2e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486628"
---
# <a name="determining-the-classes-associated-with-an-object-instance"></a>Определение классов, связанных с экземпляром объекта

Каждый объект в домен Active Directory Services имеет два атрибута, значения которых указывают иерархию классов объектов, экземпляром которых является объект.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>структуралобжекткласс</strong></td>
<td>Определяет структурные и абстрактные классы, экземпляр которых является объектом. Например, значения для объекта пользователя могут быть:
<ul>
<li><strong>В начало</strong></li>
<li><strong>person</strong></li>
<li><strong>организатионалперсон</strong></li>
<li><strong>user</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Атрибута</strong></td>
<td>Определяет классы, входящие в <strong>структуралобжекткласс</strong>, а также любые вспомогательные классы, подключаемые динамически. Например, если к &quot; &quot; объекту пользователя присоединен вспомогательный класс ТС, значения могут быть такими:
<ul>
<li><strong>В начало</strong></li>
<li><strong>средством</strong></li>
<li><strong>person</strong></li>
<li><strong>организатионалперсон</strong></li>
<li><strong>user</strong></li>
</ul></td>
</tr>
</tbody>
</table>



 

Имейте в виду, что ни один из этих атрибутов не включает вспомогательные классы, статически связываемые с классами объектов, экземплярами которых является объект. Например, вспомогательный класс **секуритипринЦипал** статически связывается с классом **пользователя** , так как он включен в значения **системауксилиарикласс** объекта user **classSchema** ; Он не включается ни в один из атрибутов **objectClass** или **структуралобжекткласс** экземпляров класса User.

 

 




