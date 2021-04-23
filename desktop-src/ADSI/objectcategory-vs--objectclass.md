---
title: objectCategory и objectClass
description: Атрибуты objectCategory и objectClass могут ссылаться на данный класс схемы объекта Directory.
ms.assetid: 66dadedb-61e4-4184-9b87-0fff036a94d9
ms.tgt_platform: multiple
keywords:
- objectCategory и objectClass ADSI
- атрибуты Аси, поиск по атрибутам objectCategory и objectClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbbb8c5fe737b7c81193a75cdae6b772db64e69c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067321"
---
# <a name="objectcategory-vs-objectclass"></a><span data-ttu-id="37d45-105">objectCategory и objectClass</span><span class="sxs-lookup"><span data-stu-id="37d45-105">objectCategory vs. objectClass</span></span>

<span data-ttu-id="37d45-106">Атрибуты **objectCategory** и **objectClass** могут ссылаться на данный класс схемы объекта Directory.</span><span class="sxs-lookup"><span data-stu-id="37d45-106">Both the **objectCategory** and **objectClass** attributes can refer to a given schema class of a directory object.</span></span> <span data-ttu-id="37d45-107">Однако существует важное различие между ними в семантике.</span><span class="sxs-lookup"><span data-stu-id="37d45-107">However, there is an important distinction in semantics between the two.</span></span> <span data-ttu-id="37d45-108">"objectClass = радости" относится к таким объектам каталога, в которых "радость" представляет любой класс в иерархии классов объектов.</span><span class="sxs-lookup"><span data-stu-id="37d45-108">"objectClass=joy" refers to such directory objects in which "joy" represents any class in the object class hierarchy.</span></span> <span data-ttu-id="37d45-109">«objectCategory = радости», с другой стороны, относится к объектам каталога, в которых «радость» определяет конкретный класс в иерархии классов объектов.</span><span class="sxs-lookup"><span data-stu-id="37d45-109">"objectCategory=joy", on the other hand, refers to those directory objects in which "joy" identifies a specific class in the object class hierarchy.</span></span>

<span data-ttu-id="37d45-110">**objectClass** может принимать несколько значений, тогда как **objectCategory** принимает одно значение.</span><span class="sxs-lookup"><span data-stu-id="37d45-110">**objectClass** can take multiple values whereas **objectCategory** takes a single value.</span></span> <span data-ttu-id="37d45-111">По этой причине **objectCategory** лучше подходит для сопоставления типов объектов в поиске по каталогу.</span><span class="sxs-lookup"><span data-stu-id="37d45-111">Because of this, **objectCategory** is better suited for type matching of objects in a directory search.</span></span> <span data-ttu-id="37d45-112">ADSI использует его в качестве критерия сопоставления по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="37d45-112">ADSI uses this as the default matching criterion.</span></span> <span data-ttu-id="37d45-113">Поиск, использующий один **objectClass** , не масштабируется до больших баз данных.</span><span class="sxs-lookup"><span data-stu-id="37d45-113">Searches using one **objectClass** are not scalable to large databases.</span></span> <span data-ttu-id="37d45-114">ADSI поддерживает синтаксис "(objectCategory = Сомедн)" и "(objectCategory = \_ отображаемое \_ имя LDAP \_ для \_ класса)".</span><span class="sxs-lookup"><span data-stu-id="37d45-114">ADSI supports "(objectCategory=SomeDN)" and "(objectCategory=Ldap\_Display\_Name\_of\_Class)" syntaxes.</span></span>

<span data-ttu-id="37d45-115">Исключением является то, что фильтр поиска LDAP "(objectClass = \* )" не задает поиск в классе Object, а только проверяет наличие объектов.</span><span class="sxs-lookup"><span data-stu-id="37d45-115">The exception to all of this is that the LDAP search filter "(objectClass=\*)" does not specify a search on object class, but merely tests for the presence of the objects.</span></span>

 

 




