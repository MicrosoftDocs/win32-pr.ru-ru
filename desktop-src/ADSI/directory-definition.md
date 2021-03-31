---
title: Определение каталога
description: В примере компонента поставщика используется относительно простая структура каталога для пояснения связи между компонентами и отображения минимальных требований, необходимых для поставщика ADSI.
ms.assetid: d8dcd255-4a17-4c80-a749-61c1af605dba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6156f2e1ab89b34f009f1a86e5de011c20cf9503
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887560"
---
# <a name="directory-definition"></a><span data-ttu-id="fe916-103">Определение каталога</span><span class="sxs-lookup"><span data-stu-id="fe916-103">Directory Definition</span></span>

<span data-ttu-id="fe916-104">В примере компонента поставщика используется относительно простая структура каталога для пояснения связи между компонентами и отображения минимальных требований, необходимых для поставщика ADSI.</span><span class="sxs-lookup"><span data-stu-id="fe916-104">The example provider component uses a relatively simple directory design to clarify the relationship between components and to show the minimum requirements necessary to be an ADSI provider.</span></span>

<span data-ttu-id="fe916-105">Каталог для примера компонента поставщика состоит из двух корневых узлов: "Сиэтл" и "Торонто".</span><span class="sxs-lookup"><span data-stu-id="fe916-105">The "directory" for the example provider component consists of two root nodes: "Seattle" and "Toronto".</span></span> <span data-ttu-id="fe916-106">Сиэтл содержит еще два подуровне, "Бельвью" и "Redmond".</span><span class="sxs-lookup"><span data-stu-id="fe916-106">Seattle contains two more sublevels, "Bellevue" and "Redmond".</span></span> <span data-ttu-id="fe916-107">Каждая из этих записей содержит несколько учетных записей пользователей.</span><span class="sxs-lookup"><span data-stu-id="fe916-107">Each of these entries contains several user accounts.</span></span> <span data-ttu-id="fe916-108">Запись "Торонто" не имеет дополнительных подуровней, но непосредственно содержит несколько учетных записей пользователей.</span><span class="sxs-lookup"><span data-stu-id="fe916-108">The "Toronto" entry has no further sublevels, but directly contains several user accounts.</span></span> <span data-ttu-id="fe916-109">На следующем рисунке показаны два корневых узла, подключенных к сети.</span><span class="sxs-lookup"><span data-stu-id="fe916-109">The following figure shows these two root nodes connected to a network.</span></span>

![Определение каталога](images/dssmdo.png)

<span data-ttu-id="fe916-111">В иерархических терминах узел пространства имен содержит "Сиэтл" и "Торонто".</span><span class="sxs-lookup"><span data-stu-id="fe916-111">In hierarchical terms, the Namespace node contains "Seattle" and "Toronto".</span></span> <span data-ttu-id="fe916-112">"Сиэтл" содержит "Бельвью" и "Redmond".</span><span class="sxs-lookup"><span data-stu-id="fe916-112">"Seattle" contains "Bellevue" and "Redmond".</span></span> <span data-ttu-id="fe916-113">"Бельвью" и "Redmond" содержат набор учетных записей пользователей.</span><span class="sxs-lookup"><span data-stu-id="fe916-113">"Bellevue" and "Redmond" each contain a set of user accounts.</span></span> <span data-ttu-id="fe916-114">"Торонто" напрямую содержит учетные записи пользователей без промежуточных узлов Организации.</span><span class="sxs-lookup"><span data-stu-id="fe916-114">"Toronto" directly contains the user accounts with no intermediate organizational nodes.</span></span>

<span data-ttu-id="fe916-115">Пример компонента поставщика представляет эту структуру только с двумя Active Directoryными типами объектов: объектом-контейнером и конечным объектом.</span><span class="sxs-lookup"><span data-stu-id="fe916-115">The example provider component represents this structure with only two Active Directory object types: a container object and a leaf object.</span></span> <span data-ttu-id="fe916-116">"Сиэтл", "Торонто", "Бельвью" и "Redmond" являются объектами-контейнерами, а каждая учетная запись пользователя является конечным объектом.</span><span class="sxs-lookup"><span data-stu-id="fe916-116">"Seattle", "Toronto", "Bellevue", and "Redmond" are container objects and each user account is a leaf object.</span></span>

<span data-ttu-id="fe916-117">В примере компонента поставщика создается класс схемы с именем "подразделение" для типа объекта контейнера и класс схемы с именем "User" для учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="fe916-117">The example provider component creates a schema class called "Organizational Unit" for a container object type and a schema class called "User" for a user account.</span></span>

<span data-ttu-id="fe916-118">Свойства каждого класса схемы, их методы и правила, управляющие отношениями включения для этих объектов, определяются в [управлении схемой](schema-management.md).</span><span class="sxs-lookup"><span data-stu-id="fe916-118">The properties for each schema class, their methods, and the rules that govern the containment relationships for these objects are all defined in [Schema Management](schema-management.md).</span></span>

 

 




