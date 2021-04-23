---
title: Когда следует расширять схему
description: Расширение схемы следует выполнять только в том случае, если ни один существующий класс объектов не удовлетворяет требованиям приложения. Расширение схемы является сложной операцией. изменения схемы реплицируются на каждый контроллер домена в лесу предприятия. Учтите это внимательно.
ms.assetid: 92231f31-d2af-4c3b-981e-e55cc478899d
ms.tgt_platform: multiple
keywords:
- Когда следует расширять схему Active Directory
- схема AD, когда следует расширять
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c182b346fd1e31bc549325260d9b57d75bbb63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654165"
---
# <a name="when-to-extend-the-schema"></a><span data-ttu-id="5268c-107">Когда следует расширять схему</span><span class="sxs-lookup"><span data-stu-id="5268c-107">When to Extend the Schema</span></span>

<span data-ttu-id="5268c-108">Расширение схемы следует выполнять только в том случае, если ни один существующий класс объектов не удовлетворяет требованиям приложения.</span><span class="sxs-lookup"><span data-stu-id="5268c-108">Extend the schema only if no existing object class fulfills the requirements of your application.</span></span> <span data-ttu-id="5268c-109">Расширение схемы является сложной операцией. изменения схемы реплицируются на каждый контроллер домена в лесу предприятия.</span><span class="sxs-lookup"><span data-stu-id="5268c-109">Extending the schema is a complex operation; schema changes are replicated to every domain controller in the enterprise forest.</span></span> <span data-ttu-id="5268c-110">Учтите это внимательно.</span><span class="sxs-lookup"><span data-stu-id="5268c-110">Consider this carefully.</span></span>

<span data-ttu-id="5268c-111">Схему можно расширить тремя способами:</span><span class="sxs-lookup"><span data-stu-id="5268c-111">The schema can be extended in three ways:</span></span>

-   <span data-ttu-id="5268c-112">Создать новый подкласс из существующего класса. подкласс имеет все атрибуты суперкласса и все указанные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="5268c-112">Derive a new subclass from an existing class - the subclass has all of the attributes of the superclass and any attributes you specify.</span></span> <span data-ttu-id="5268c-113">Наследование от существующего класса:</span><span class="sxs-lookup"><span data-stu-id="5268c-113">Derive from an existing class:</span></span>
    -   <span data-ttu-id="5268c-114">Если для существующего класса требуются дополнительные атрибуты, но в противном случае это приемлемо.</span><span class="sxs-lookup"><span data-stu-id="5268c-114">When the existing class requires additional attributes, but otherwise is acceptable.</span></span>
    -   <span data-ttu-id="5268c-115">Если возможность преобразования существующих объектов класса в новый класс не требуется.</span><span class="sxs-lookup"><span data-stu-id="5268c-115">When the ability to transform existing objects of the class into a new class is not required.</span></span> <span data-ttu-id="5268c-116">Невозможно добавить подкласс в существующий объект.</span><span class="sxs-lookup"><span data-stu-id="5268c-116">It is not possible to add a subclass to an existing object.</span></span>
    -   <span data-ttu-id="5268c-117">Чтобы использовать существующую оснастку диспетчера каталогов для управления расширенными атрибутами объектов.</span><span class="sxs-lookup"><span data-stu-id="5268c-117">To use the existing Directory Manager snap-in to manage the extended attributes of the objects.</span></span>
-   <span data-ttu-id="5268c-118">Добавление атрибутов в существующий класс и/или добавление родительских объектов для класса.</span><span class="sxs-lookup"><span data-stu-id="5268c-118">Add attributes to an existing class and/or add parent objects for the class.</span></span> <span data-ttu-id="5268c-119">При добавлении нескольких атрибутов выполните эту операцию структурированным образом, определив вспомогательный класс и добавив этот вспомогательный класс в существующий класс.</span><span class="sxs-lookup"><span data-stu-id="5268c-119">When adding multiple attributes, perform this operation in a structured manner by defining an auxiliary class and adding that auxiliary class to the existing class.</span></span>
-   <span data-ttu-id="5268c-120">Изменение существующего класса требуется, когда приложению требуется возможность расширения существующих объектов класса.</span><span class="sxs-lookup"><span data-stu-id="5268c-120">Modification of an existing class is required when an application requires the ability to extend existing objects of the class.</span></span> <span data-ttu-id="5268c-121">Например, чтобы добавить в объект пользователя данные, относящиеся к конкретному приложению, следует расширить класс пользователя обычным образом, так как необходимо управлять существующими пользователями, а не только специальными пользователями, созданными приложением.</span><span class="sxs-lookup"><span data-stu-id="5268c-121">For example, to add application-specific data to the User object, extend the class User normally, because you must handle existing Users and not just special Users created by your application.</span></span>
-   <span data-ttu-id="5268c-122">Создайте новый класс с необходимыми атрибутами.</span><span class="sxs-lookup"><span data-stu-id="5268c-122">Create a new class with the required attributes.</span></span> <span data-ttu-id="5268c-123">Создание нового класса; то есть класс, производный от «Top», если ни один из существующих классов не удовлетворяет эксплуатационным требованиям.</span><span class="sxs-lookup"><span data-stu-id="5268c-123">Create a new class; that is, a class derived from "Top" when no existing class fulfills the operational requirements.</span></span>

<span data-ttu-id="5268c-124">При подклассе существующего класса все элементы пользовательского интерфейса, связанные с исходным классом, не будут наследоваться подклассом.</span><span class="sxs-lookup"><span data-stu-id="5268c-124">When you subclass an existing class, any user interface items associated to the original class will not be inherited by the subclass.</span></span> <span data-ttu-id="5268c-125">Например, если создать подкласс объекта пользователя, то страницы свойств и пункты меню, связанные с пользователем, не наследуются.</span><span class="sxs-lookup"><span data-stu-id="5268c-125">For example, if you subclass a user object, the property pages and menu items associated to user are not inherited.</span></span> <span data-ttu-id="5268c-126">По этой причине предпочтительнее расширить существующий объект или создать вспомогательный класс вместо создания подкласса.</span><span class="sxs-lookup"><span data-stu-id="5268c-126">For this reason, it is preferable to extend an existing object or create an auxiliary class rather than create a subclass.</span></span>

<span data-ttu-id="5268c-127">Независимо от того, подкласс ли вы существующий класс или изменяете существующий, вам потребуется расширить средства, такие как оснастка «Active Directory пользователи и компьютеры», для управления расширенными атрибутами объектов.</span><span class="sxs-lookup"><span data-stu-id="5268c-127">Whether you subclass an existing class or modify an existing class, you will want to extend tools such as the Active Directory Users and Computers snap-in to manage the extended attributes of the objects.</span></span> <span data-ttu-id="5268c-128">Дополнительные сведения см. [в разделе Расширение пользовательского интерфейса для объектов каталога](extending-the-user-interface-for-directory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="5268c-128">For more information, see [Extending the User Interface for Directory Objects](extending-the-user-interface-for-directory-objects.md).</span></span>

 

 




