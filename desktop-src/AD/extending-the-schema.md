---
title: Расширение схемы
description: Схема службы каталогов Active Directory определяет атрибуты и классы, используемые в службах домен Active Directory Services.
ms.assetid: 1c7c1fa7-56d9-4b2d-9c48-aa10464064bc
ms.tgt_platform: multiple
keywords:
- Active Directory, использование, схема, расширение схемы
- схема AD, расширение схемы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90c03d57468fb5275c55ce0d725a2decd7cfbf0f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "105654294"
---
# <a name="extending-the-schema"></a><span data-ttu-id="f04e3-105">Расширение схемы</span><span class="sxs-lookup"><span data-stu-id="f04e3-105">Extending the Schema</span></span>

<span data-ttu-id="f04e3-106">Схема службы каталогов Active Directory определяет атрибуты и классы, используемые в службах домен Active Directory Services.</span><span class="sxs-lookup"><span data-stu-id="f04e3-106">The Active Directory directory service schema defines the attributes and classes used in Active Directory Domain Services.</span></span> <span data-ttu-id="f04e3-107">Базовая схема, включенная в систему, содержит обширный набор определений классов, таких как **User**, **Computer** и **OrganizationalUnit**, и определения атрибутов, такие как **userPrincipalName**, **telephoneNumber** и **objectSid**.</span><span class="sxs-lookup"><span data-stu-id="f04e3-107">The base schema that is included the system contains a rich set of class definitions, such as **user**, **computer**, and **organizationalUnit**, and attribute definitions, such as **userPrincipalName**, **telephoneNumber**, and **objectSid**.</span></span> <span data-ttu-id="f04e3-108">Для большинства приложений будет достаточно существующего набора классов и атрибутов.</span><span class="sxs-lookup"><span data-stu-id="f04e3-108">The existing set of classes and attributes will be sufficient for most applications.</span></span> <span data-ttu-id="f04e3-109">Однако схема является расширяемой, что означает возможность определения новых классов и атрибутов.</span><span class="sxs-lookup"><span data-stu-id="f04e3-109">However, the schema is extensible, which means that you can define new classes and attributes.</span></span> <span data-ttu-id="f04e3-110">В этом разделе описано, как расширить схему Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f04e3-110">This section discusses how to extend the Active Directory schema.</span></span>

## <a name="when-to-extend-the-schema"></a><span data-ttu-id="f04e3-111">Когда следует расширять схему</span><span class="sxs-lookup"><span data-stu-id="f04e3-111">When to Extend the Schema</span></span>

<span data-ttu-id="f04e3-112">Если существующие классы и атрибуты не соответствуют типу данных, которые необходимо сохранить, необходимо расширить схему.</span><span class="sxs-lookup"><span data-stu-id="f04e3-112">If the existing classes and attributes do not fit with the type of data you want to store, you should extend the schema.</span></span> <span data-ttu-id="f04e3-113">Важно отметить, что добавления схемы являются постоянными; можно отключить классы и атрибуты, однако их нельзя удалить из схемы.</span><span class="sxs-lookup"><span data-stu-id="f04e3-113">It is important to note that schema additions are permanent; you can disable classes and attributes, but you can never remove them from the schema.</span></span> <span data-ttu-id="f04e3-114">Помните об этом при тестировании кода.</span><span class="sxs-lookup"><span data-stu-id="f04e3-114">Keep this in mind when you are testing code.</span></span>

<span data-ttu-id="f04e3-115">Также учитывайте размер данных, которые необходимо сохранить.</span><span class="sxs-lookup"><span data-stu-id="f04e3-115">Also consider the size of the data that you want to store.</span></span> <span data-ttu-id="f04e3-116">Корпорация Майкрософт рекомендует, чтобы значение атрибута не превышало 500 КБ, включая сумму многозначных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="f04e3-116">Microsoft recommends that no attribute value exceed 500 kilobytes, including the sum of multivalued attributes.</span></span> <span data-ttu-id="f04e3-117">Кроме того, размер объектов не должен превышать 1 МБ.</span><span class="sxs-lookup"><span data-stu-id="f04e3-117">Also, objects should not exceed 1 megabyte in size.</span></span> <span data-ttu-id="f04e3-118">Рассмотрите также количество экземпляров данных. Если добавить новый атрибут к классу [**User**](/windows/desktop/ADSchema/c-user) в системе, которая имеет 100 000 пользователей, это может использовать значительный объем пространства.</span><span class="sxs-lookup"><span data-stu-id="f04e3-118">Consider also the number of instances of the data; if you add a new attribute to the [**User**](/windows/desktop/ADSchema/c-user) class on a system that has 100,000 users, this can use up considerable space.</span></span>

<span data-ttu-id="f04e3-119">В этом разделе содержатся следующие темы:</span><span class="sxs-lookup"><span data-stu-id="f04e3-119">Topics in this section include:</span></span>

-   <span data-ttu-id="f04e3-120">Как выполнить привязку к контейнеру схемы и прочитать свойства существующих классов и атрибутов.</span><span class="sxs-lookup"><span data-stu-id="f04e3-120">How to bind to the schema container and read the properties of existing classes and attributes.</span></span>
-   <span data-ttu-id="f04e3-121">Способ и время расширения схемы путем определения новых атрибутов и классов.</span><span class="sxs-lookup"><span data-stu-id="f04e3-121">How and when to extend the schema by defining new attributes and classes.</span></span>
-   <span data-ttu-id="f04e3-122">Установка расширений схемы с помощью LDIFDE, CSVDE или программно с помощью ADSI.</span><span class="sxs-lookup"><span data-stu-id="f04e3-122">How to install schema extensions using LDIFDE, CSVDE, or programmatically with ADSI.</span></span>

<span data-ttu-id="f04e3-123">Дополнительные сведения и общие сведения о схеме Active Directory, включая сведения о реализации схемы, определениях классов и определениях атрибутов, см. в разделе [Active Directory Schema](active-directory-schema.md).</span><span class="sxs-lookup"><span data-stu-id="f04e3-123">For more information and an overview of the Active Directory schema, including information about the schema implementation, class definitions, and attribute definitions, see [Active Directory Schema](active-directory-schema.md).</span></span>

<span data-ttu-id="f04e3-124">Дополнительные сведения, включая справочные страницы по стандартным классам схемы, атрибутам и синтаксису атрибутов, см. в справочнике по Active Directory схеме в [справочнике по службам домен Active Directory](active-directory-domain-services-reference.md).</span><span class="sxs-lookup"><span data-stu-id="f04e3-124">For more information, including reference pages for the predefined schema classes, attributes, and attribute syntaxes, see the Active Directory Schema Reference in the [Active Directory Domain Services Reference](active-directory-domain-services-reference.md).</span></span>

 

 