---
title: Атрибуты (AD DS)
description: Каждый объект в домен Active Directory Services содержит набор атрибутов, определяющих характеристики объекта.
ms.assetid: 9efa7ae1-b6a9-4b95-b031-b502772c536c
ms.tgt_platform: multiple
keywords:
- атрибуты AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56579494cdc12c2d0ad6fadbb6395d07eaec80d2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069818"
---
# <a name="attributes-ad-ds"></a><span data-ttu-id="7b61c-104">Атрибуты (AD DS)</span><span class="sxs-lookup"><span data-stu-id="7b61c-104">Attributes (AD DS)</span></span>

<span data-ttu-id="7b61c-105">Каждый объект в домен Active Directory Services содержит набор атрибутов, определяющих характеристики объекта.</span><span class="sxs-lookup"><span data-stu-id="7b61c-105">Each object in Active Directory Domain Services contains a set of attributes that define the characteristics of the object.</span></span> <span data-ttu-id="7b61c-106">Каждый атрибут описывается объектом [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) в контейнере схемы, определяющим атрибут.</span><span class="sxs-lookup"><span data-stu-id="7b61c-106">Each attribute is described by an [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) object in the schema container that defines the attribute.</span></span> <span data-ttu-id="7b61c-107">Определение атрибута включает различные данные, например типы объектов, к которым применяется атрибут, и тип синтаксиса атрибута.</span><span class="sxs-lookup"><span data-stu-id="7b61c-107">The attribute definition includes a variety of data, for example, what object types that the attribute applies to and the syntax type of the attribute.</span></span> <span data-ttu-id="7b61c-108">Дополнительные сведения об определениях схемы атрибутов см. в разделе [характеристики атрибутов](characteristics-of-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="7b61c-108">For more information about attribute schema definitions, see [Characteristics of Attributes](characteristics-of-attributes.md).</span></span>

<span data-ttu-id="7b61c-109">В следующем списке перечислены типы атрибутов, которые хранятся в службах домен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7b61c-109">The following list lists the type of attributes that are stored in Active Directory Domain Services.</span></span>

<dl> <dt>

<span data-ttu-id="7b61c-110"><span id="Domain-replicated__stored_attributes"></span><span id="domain-replicated__stored_attributes"></span><span id="DOMAIN-REPLICATED__STORED_ATTRIBUTES"></span>Реплицируемые в домене, сохраненные атрибуты</span><span class="sxs-lookup"><span data-stu-id="7b61c-110"><span id="Domain-replicated__stored_attributes"></span><span id="domain-replicated__stored_attributes"></span><span id="DOMAIN-REPLICATED__STORED_ATTRIBUTES"></span>Domain-replicated, stored attributes</span></span>
</dt> <dd>

<span data-ttu-id="7b61c-111">Некоторые атрибуты хранятся в каталоге (например, [**CN**](/windows/desktop/ADSchema/a-cn), [**нтсекуритидескриптор**](/windows/desktop/ADSchema/a-ntsecuritydescriptor)и [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)) и реплицируются на все контроллеры домена в домене.</span><span class="sxs-lookup"><span data-stu-id="7b61c-111">Some attributes are stored in the directory (such as [**cn**](/windows/desktop/ADSchema/a-cn), [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), and [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)) and replicated to all domain controllers in a domain.</span></span> <span data-ttu-id="7b61c-112">Подмножество этих атрибутов также реплицируется в глобальный каталог.</span><span class="sxs-lookup"><span data-stu-id="7b61c-112">A subset of these attributes is also replicated to the global catalog.</span></span> <span data-ttu-id="7b61c-113">При перечислении атрибутов объекта из глобального каталога возвращаются только атрибуты, реплицированные в глобальный каталог.</span><span class="sxs-lookup"><span data-stu-id="7b61c-113">If you enumerate attributes of an object from the global catalog, only the attributes replicated to the global catalog are returned.</span></span> <span data-ttu-id="7b61c-114">Некоторые атрибуты также индексируются, поскольку включение индексированного свойства в запрос повышает производительность запросов.</span><span class="sxs-lookup"><span data-stu-id="7b61c-114">Some attributes are also indexed because including an indexed property in a query improves the query performance.</span></span>

</dd> <dt>

<span data-ttu-id="7b61c-115"><span id="Non-replicated__locally_stored_attributes"></span><span id="non-replicated__locally_stored_attributes"></span><span id="NON-REPLICATED__LOCALLY_STORED_ATTRIBUTES"></span>Нереплицированные, локально сохраненные атрибуты</span><span class="sxs-lookup"><span data-stu-id="7b61c-115"><span id="Non-replicated__locally_stored_attributes"></span><span id="non-replicated__locally_stored_attributes"></span><span id="NON-REPLICATED__LOCALLY_STORED_ATTRIBUTES"></span>Non-replicated, locally stored attributes</span></span>
</dt> <dd>

<span data-ttu-id="7b61c-116">Нереплицированные атрибуты, такие как [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**Last-logon**](/windows/desktop/ADSchema/a-lastlogon)и [**Last-logoff**](/windows/desktop/ADSchema/a-lastlogoff) , хранятся на каждом контроллере домена, но не реплицируются.</span><span class="sxs-lookup"><span data-stu-id="7b61c-116">Non-replicated attributes, such as [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**Last-Logon**](/windows/desktop/ADSchema/a-lastlogon), and [**Last-Logoff**](/windows/desktop/ADSchema/a-lastlogoff) are stored on each domain controller, but are not replicated.</span></span> <span data-ttu-id="7b61c-117">Нереплицированные атрибуты — это атрибуты, относящиеся к конкретному контроллеру домена.</span><span class="sxs-lookup"><span data-stu-id="7b61c-117">The non-replicated attributes are attributes that pertain to a particular domain controller.</span></span> <span data-ttu-id="7b61c-118">Например, атрибут **последнего входа** — это последняя Дата и время проверки сетевого входа пользователя на конкретный контроллер домена, который вернул это свойство.</span><span class="sxs-lookup"><span data-stu-id="7b61c-118">For example, **Last-Logon** attribute is the last date and time that the user's network logon was validated by that particular domain controller that returned the property.</span></span> <span data-ttu-id="7b61c-119">Эти атрибуты могут быть получены таким же образом, как и атрибуты на уровне домена, описанные выше.</span><span class="sxs-lookup"><span data-stu-id="7b61c-119">These attributes can be retrieved in the same way as the domain-wide attributes described previously.</span></span> <span data-ttu-id="7b61c-120">Однако для этих атрибутов каждый контроллер домена хранит только значения, относящиеся к конкретному контроллеру домена.</span><span class="sxs-lookup"><span data-stu-id="7b61c-120">However, for these attributes, each domain controller stores only values that pertain to that particular domain controller.</span></span> <span data-ttu-id="7b61c-121">Например, чтобы получить сведения о последнем входе пользователя в домен, извлеките атрибут **последнего входа** пользователя из каждого контроллера домена в домене и найдите последнюю дату и время.</span><span class="sxs-lookup"><span data-stu-id="7b61c-121">For example, to obtain the last time that a user logged on to the domain, retrieve the **Last-Logon** attribute for the user from every domain controller in the domain and find that latest date and time.</span></span>

</dd> <dt>

<span data-ttu-id="7b61c-122"><span id="Non-stored__constructed_attributes"></span><span id="non-stored__constructed_attributes"></span><span id="NON-STORED__CONSTRUCTED_ATTRIBUTES"></span>Несохраненные, сконструированные атрибуты</span><span class="sxs-lookup"><span data-stu-id="7b61c-122"><span id="Non-stored__constructed_attributes"></span><span id="non-stored__constructed_attributes"></span><span id="NON-STORED__CONSTRUCTED_ATTRIBUTES"></span>Non-stored, constructed attributes</span></span>
</dt> <dd>

<span data-ttu-id="7b61c-123">Объект пользователя также имеет сконструированные атрибуты, которые не хранятся в каталоге, но вычисляются контроллером домена, например [**каноникалнаме**](/windows/desktop/ADSchema/a-canonicalname) и [**алловедаттрибутес**](/windows/desktop/ADSchema/a-allowedattributes).</span><span class="sxs-lookup"><span data-stu-id="7b61c-123">A user object also has constructed attributes that are not stored in the directory, but are calculated by the domain controller, such as [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname) and [**allowedAttributes**](/windows/desktop/ADSchema/a-allowedattributes).</span></span>

</dd> </dl>

 

 