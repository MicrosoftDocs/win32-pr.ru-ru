---
title: Присвоение имен атрибутам и классам
description: Этот раздел содержит рекомендации по именованию атрибутов и классов.
ms.assetid: ccbc2859-332f-4ded-9125-5bf507cad960
ms.tgt_platform: multiple
keywords:
- Присвоение имен атрибутам и классам
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bfd2614033e12f68ba2727cc7aec689c16071e
ms.sourcegitcommit: 02e6e0b58720bf6b77797dd7a9ddc11c95f42b33
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/21/2020
ms.locfileid: "105654391"
---
# <a name="naming-attributes-and-classes"></a><span data-ttu-id="f0173-104">Присвоение имен атрибутам и классам</span><span class="sxs-lookup"><span data-stu-id="f0173-104">Naming Attributes and Classes</span></span>

<span data-ttu-id="f0173-105">Этот раздел содержит рекомендации по именованию атрибутов и классов.</span><span class="sxs-lookup"><span data-stu-id="f0173-105">This topic includes guidelines for naming attributes and classes.</span></span>

<span data-ttu-id="f0173-106">Чтобы создать новый класс или атрибут, придерживайтесь следующих правил именования:</span><span class="sxs-lookup"><span data-stu-id="f0173-106">To create a new class or attribute, adhere to the following naming rules:</span></span>

-   <span data-ttu-id="f0173-107">Используйте одно и то же имя для свойств **CN** и **LDAPDisplayName** нового объекта **attributeSchema** или **classSchema** .</span><span class="sxs-lookup"><span data-stu-id="f0173-107">Use the same name for both the **cn** and **lDAPDisplayName** properties of a new **attributeSchema** or **classSchema** object.</span></span>
-   <span data-ttu-id="f0173-108">Найдите название компании с префиксом в нижнем регистре в первом разделе имени.</span><span class="sxs-lookup"><span data-stu-id="f0173-108">Identify the company with a lower-case prefix in the first section of the name.</span></span> <span data-ttu-id="f0173-109">Этот префикс может быть DNS-именем, акронимом или другой строкой, однозначно идентифицирующей компанию.</span><span class="sxs-lookup"><span data-stu-id="f0173-109">This prefix can be a DNS name, acronym, or other string that uniquely identifies the company.</span></span> <span data-ttu-id="f0173-110">Префикс гарантирует, что все атрибуты и классы для конкретной компании будут отображаться последовательно при просмотре схемы.</span><span class="sxs-lookup"><span data-stu-id="f0173-110">The prefix ensures that all attributes and classes for a specific company are displayed consecutively when browsing the schema.</span></span>
-   <span data-ttu-id="f0173-111">Если вы разрабатываете расширение схемы в качестве независимого поставщика программного обеспечения, добавьте сокращенное название продукта префикса.</span><span class="sxs-lookup"><span data-stu-id="f0173-111">If you are developing a schema extension as an independent software vendor, add an abbreviation of the product name of the prefix.</span></span> <span data-ttu-id="f0173-112">Это добавляет различие между несколькими продуктами, содержащими расширения схемы LDAP.</span><span class="sxs-lookup"><span data-stu-id="f0173-112">This adds distinction between multiple products that contain LDAP schema extensions.</span></span>
-   <span data-ttu-id="f0173-113">Используйте дефис в качестве следующего символа после префикса.</span><span class="sxs-lookup"><span data-stu-id="f0173-113">Use a hyphen as the next character after the prefix.</span></span>
-   <span data-ttu-id="f0173-114">Укажите имя атрибута или класса, уникальное в пределах атрибутов компании после дефиса.</span><span class="sxs-lookup"><span data-stu-id="f0173-114">Specify an attribute or class name that is unique within the company's attributes after the hyphen.</span></span> <span data-ttu-id="f0173-115">Эта часть общего имени должна быть описательной.</span><span class="sxs-lookup"><span data-stu-id="f0173-115">This part of the common-name should be descriptive.</span></span> <span data-ttu-id="f0173-116">Не используйте имена нелогично, которые не имеют смысла для разработчиков и средств просмотра схемы.</span><span class="sxs-lookup"><span data-stu-id="f0173-116">Do not use illogical names that are meaningless to developers and viewers of the schema.</span></span>

<span data-ttu-id="f0173-117">Например, если вымышленная компания Fabrikam расширила схему путем добавления атрибута для хранения идентификатора электронной почты, **CN** и **lDAPDisplayName** нового атрибута могут иметь значение «Fabrikam-воицемаилид».</span><span class="sxs-lookup"><span data-stu-id="f0173-117">For example, if the fictitious Fabrikam company extended the schema by adding an attribute for storing a voice-mail identifier, the **cn** and **lDAPDisplayName** of the new attribute could be "fabrikam-VoiceMailID".</span></span>

<span data-ttu-id="f0173-118">Если атрибут **lDAPDisplayName** атрибута или класса не указан, система использует **CN** для его создания.</span><span class="sxs-lookup"><span data-stu-id="f0173-118">If the **lDAPDisplayName** of an attribute or class is not specified, the system uses the **cn** to generate one.</span></span> <span data-ttu-id="f0173-119">Однако системный алгоритм создания имени может привести к конфликтам имен или именам, которые трудно считать.</span><span class="sxs-lookup"><span data-stu-id="f0173-119">However, the system algorithm for generating the name may result in name collisions or names that are difficult to read.</span></span> <span data-ttu-id="f0173-120">Чтобы избежать этих проблем, рекомендуется явно указать атрибут **lDAPDisplayName** для всех атрибутов и классов.</span><span class="sxs-lookup"><span data-stu-id="f0173-120">To avoid these problems, it is recommended that an **lDAPDisplayName** be explicitly specified for all attributes and classes.</span></span>

<span data-ttu-id="f0173-121">В целях разработки и тестирования может быть желательно добавить суффикс версии к **CN** и **lDAPDisplayName**, например "Fabrikam-воицемаилид-001".</span><span class="sxs-lookup"><span data-stu-id="f0173-121">For development and testing purposes, it may be desirable to append a version suffix to the **cn** and **lDAPDisplayName**, for example, "fabrikam-VoiceMailID-001".</span></span> <span data-ttu-id="f0173-122">В распределенной среде разработки и тестирования суффикс версии позволяет разработчикам одновременно запускать несколько версий программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="f0173-122">In a distributed development/test environment, a version suffix enables developers to run multiple versions of their software simultaneously.</span></span> <span data-ttu-id="f0173-123">После завершения тестирования Переименуйте атрибут или класс, чтобы удалить суффикс.</span><span class="sxs-lookup"><span data-stu-id="f0173-123">After testing is complete, rename the attribute or class to remove the suffix.</span></span>

<span data-ttu-id="f0173-124">Удалить уничтоженные версии расширений схемы невозможно, но можно отключить их и переименовать с помощью маскировки имен.</span><span class="sxs-lookup"><span data-stu-id="f0173-124">It is not possible to delete defunct versions of a schema extensions, but it is possible to disable them and rename them with obscure names.</span></span> <span data-ttu-id="f0173-125">Дополнительные сведения см. в разделе [Отключение существующих классов и атрибутов](disabling-existing-classes-and-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="f0173-125">For more information, see [Disabling Existing Classes and Attributes](disabling-existing-classes-and-attributes.md).</span></span>

 

 




