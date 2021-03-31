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
# <a name="determining-the-classes-associated-with-an-object-instance"></a><span data-ttu-id="48c31-103">Определение классов, связанных с экземпляром объекта</span><span class="sxs-lookup"><span data-stu-id="48c31-103">Determining the Classes Associated With an Object Instance</span></span>

<span data-ttu-id="48c31-104">Каждый объект в домен Active Directory Services имеет два атрибута, значения которых указывают иерархию классов объектов, экземпляром которых является объект.</span><span class="sxs-lookup"><span data-stu-id="48c31-104">Every object in Active Directory Domain Services has two attributes whose values identify the hierarchy of object classes of which the object is an instance.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="48c31-105">attribute</span><span class="sxs-lookup"><span data-stu-id="48c31-105">Attribute</span></span></th>
<th><span data-ttu-id="48c31-106">Описание</span><span class="sxs-lookup"><span data-stu-id="48c31-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48c31-107"><strong>структуралобжекткласс</strong></span><span class="sxs-lookup"><span data-stu-id="48c31-107"><strong>structuralObjectClass</strong></span></span></td>
<td><span data-ttu-id="48c31-108">Определяет структурные и абстрактные классы, экземпляр которых является объектом.</span><span class="sxs-lookup"><span data-stu-id="48c31-108">Identifies the structural and abstract classes of which the object is an instance.</span></span> <span data-ttu-id="48c31-109">Например, значения для объекта пользователя могут быть:</span><span class="sxs-lookup"><span data-stu-id="48c31-109">For example, the values for a user object can be:</span></span>
<ul>
<li><span data-ttu-id="48c31-110"><strong>В начало</strong></span><span class="sxs-lookup"><span data-stu-id="48c31-110"><strong>top</strong></span></span></li>
<li><span data-ttu-id="48c31-111"><strong>person</strong></span><span class="sxs-lookup"><span data-stu-id="48c31-111"><strong>person</strong></span></span></li>
<li><span data-ttu-id="48c31-112"><strong>организатионалперсон</strong></span><span class="sxs-lookup"><span data-stu-id="48c31-112"><strong>organizationalPerson</strong></span></span></li>
<li><span data-ttu-id="48c31-113"><strong>user</strong></span><span class="sxs-lookup"><span data-stu-id="48c31-113"><strong>user</strong></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48c31-114"><strong>Атрибута</strong></span><span class="sxs-lookup"><span data-stu-id="48c31-114"><strong>objectClass</strong></span></span></td>
<td><span data-ttu-id="48c31-115">Определяет классы, входящие в <strong>структуралобжекткласс</strong>, а также любые вспомогательные классы, подключаемые динамически.</span><span class="sxs-lookup"><span data-stu-id="48c31-115">Identifies the classes included in <strong>structuralObjectClass</strong>, plus any auxiliary classes that are dynamically attached.</span></span> <span data-ttu-id="48c31-116">Например, если к &quot; &quot; объекту пользователя присоединен вспомогательный класс ТС, значения могут быть такими:</span><span class="sxs-lookup"><span data-stu-id="48c31-116">For example, if a &quot;vehicle&quot; auxiliary class is attached to a user object, the values can be:</span></span>
<ul>
<li><span data-ttu-id="48c31-117"><strong>В начало</strong></span><span class="sxs-lookup"><span data-stu-id="48c31-117"><strong>top</strong></span></span></li>
<li><span data-ttu-id="48c31-118"><strong>средством</strong></span><span class="sxs-lookup"><span data-stu-id="48c31-118"><strong>vehicle</strong></span></span></li>
<li><span data-ttu-id="48c31-119"><strong>person</strong></span><span class="sxs-lookup"><span data-stu-id="48c31-119"><strong>person</strong></span></span></li>
<li><span data-ttu-id="48c31-120"><strong>организатионалперсон</strong></span><span class="sxs-lookup"><span data-stu-id="48c31-120"><strong>organizationalPerson</strong></span></span></li>
<li><span data-ttu-id="48c31-121"><strong>user</strong></span><span class="sxs-lookup"><span data-stu-id="48c31-121"><strong>user</strong></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="48c31-122">Имейте в виду, что ни один из этих атрибутов не включает вспомогательные классы, статически связываемые с классами объектов, экземплярами которых является объект.</span><span class="sxs-lookup"><span data-stu-id="48c31-122">Be aware that neither of these attributes include auxiliary classes that are statically linked with the object classes of which the object is an instance.</span></span> <span data-ttu-id="48c31-123">Например, вспомогательный класс **секуритипринЦипал** статически связывается с классом **пользователя** , так как он включен в значения **системауксилиарикласс** объекта user **classSchema** ; Он не включается ни в один из атрибутов **objectClass** или **структуралобжекткласс** экземпляров класса User.</span><span class="sxs-lookup"><span data-stu-id="48c31-123">For example, the **securityPrincipal** auxiliary class is statically linked with the **user** class because it is included in the **systemAuxiliaryClass** values of the user **classSchema** object; it is not included in either the **objectClass** or **structuralObjectClass** attributes of instances of the user class.</span></span>

 

 




