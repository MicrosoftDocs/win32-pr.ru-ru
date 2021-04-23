---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 2f6c51a3-003c-4d68-9e4d-9be5d325a477
title: Подключение PrintCapabilities к схеме печати
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17d2f5a34421dba2402bce1d6699f208fd58c799
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105674571"
---
# <a name="connecting-printcapabilities-with-the-print-schema"></a><span data-ttu-id="0f5c3-104">Подключение PrintCapabilities к схеме печати</span><span class="sxs-lookup"><span data-stu-id="0f5c3-104">Connecting PrintCapabilities with the Print Schema</span></span>

<span data-ttu-id="0f5c3-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="0f5c3-105">This topic is not current.</span></span> <span data-ttu-id="0f5c3-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0f5c3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0f5c3-107">Общая схема PrintCapabilities охватывает структуру, назначение и использование различных типов элементов.</span><span class="sxs-lookup"><span data-stu-id="0f5c3-107">The general PrintCapabilities Schema covers the structure, purpose, and use of the various element types.</span></span> <span data-ttu-id="0f5c3-108">Он задает атрибут Name, который используется для определения конкретных экземпляров каждого типа элемента.</span><span class="sxs-lookup"><span data-stu-id="0f5c3-108">It specifies the name attribute that is used to define specific instances of each element type.</span></span> <span data-ttu-id="0f5c3-109">Он указывает, что авторы PrintCapabilities могут использовать экземпляры элементов, определенные ключевыми словами «Print Schema», или они могут представлять собственные закрытые экземпляры, если эти закрытые экземпляры определены в пространстве имен, которое четко определено как собственное.</span><span class="sxs-lookup"><span data-stu-id="0f5c3-109">It specifies that PrintCapabilities authors may use instances of elements defined by the Print Schema Keywords, or they may introduce their own privately-defined instances, as long as these privately-defined instances are defined in a namespace that is clearly identified as their own.</span></span> <span data-ttu-id="0f5c3-110">(Авторы PrintCapabilities также могут использовать экземпляры, ранее определенные в другом частном пространстве имен.)</span><span class="sxs-lookup"><span data-stu-id="0f5c3-110">(PrintCapabilities authors may also use instances previously defined in another private namespace.)</span></span>

<span data-ttu-id="0f5c3-111">В документе «печать ключевых слов схемы» определены конкретные экземпляры каждого типа элемента, который можно использовать в документах PrintCapabilities и PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="0f5c3-111">The Print Schema Keywords document defines the specific instances of each element type available for use in PrintCapabilities documents and in PrintTickets.</span></span> <span data-ttu-id="0f5c3-112">В нем также документируется их назначение и использование.</span><span class="sxs-lookup"><span data-stu-id="0f5c3-112">It also documents their purpose and usage.</span></span> <span data-ttu-id="0f5c3-113">В документе «печать ключевых слов схемы» также определяются экземпляры нескольких типов элементов, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="0f5c3-113">The Print Schema Keywords document also defines instances of several element types, as follows:</span></span>

-   <span data-ttu-id="0f5c3-114">Экземпляры свойств и вложенных свойств, расположенные в корне документа PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="0f5c3-114">Property and subproperty instances that reside at the root of the PrintCapabilities document</span></span>

    -   <span data-ttu-id="0f5c3-115">Эти элементы описывают различные аспекты и возможности устройства, а также предоставляют общий словарь для описания устройств.</span><span class="sxs-lookup"><span data-stu-id="0f5c3-115">These elements describe the various aspects and capabilities of the device, and provide a common vocabulary for describing devices.</span></span>

-   <span data-ttu-id="0f5c3-116">Экземпляры свойств и вложенных свойств, являющиеся дочерними элементами элементов функций</span><span class="sxs-lookup"><span data-stu-id="0f5c3-116">Property and subproperty instances that are children of Feature elements</span></span>

    -   <span data-ttu-id="0f5c3-117">Эти элементы описывают различные аспекты, связанные с определенной функцией.</span><span class="sxs-lookup"><span data-stu-id="0f5c3-117">These elements describe various aspects related to a specific Feature.</span></span>

-   <span data-ttu-id="0f5c3-118">Экземпляры свойств и вложенных свойств, являющиеся дочерними элементами параметров</span><span class="sxs-lookup"><span data-stu-id="0f5c3-118">Property and subproperty instances that are children of Option elements</span></span>

    -   <span data-ttu-id="0f5c3-119">Эти элементы описывают различные аспекты и возможности устройства, зависящие от параметра, выбранного для конкретного компонента.</span><span class="sxs-lookup"><span data-stu-id="0f5c3-119">These elements describe the various aspects and capabilities of the device that are dependent on the Option selected for a specific Feature.</span></span> <span data-ttu-id="0f5c3-120">Они могут быть заменены экземплярами свойств, расположенными в корне документа PrintCapabilities, но в некоторых случаях предлагают дополнительное удобство.</span><span class="sxs-lookup"><span data-stu-id="0f5c3-120">These could be replaced by Property instances located at the root of the PrintCapabilities document, but offer additional convenience in some cases.</span></span> <span data-ttu-id="0f5c3-121">Дополнительные сведения см. в разделе [Добавление экземпляров свойств](adding-property-instances.md).</span><span class="sxs-lookup"><span data-stu-id="0f5c3-121">For more information, see [Adding Property Instances](adding-property-instances.md).</span></span>

<!-- -->

-   <span data-ttu-id="0f5c3-122">Экземпляры Скоредпроперти</span><span class="sxs-lookup"><span data-stu-id="0f5c3-122">ScoredProperty instances</span></span>

    -   <span data-ttu-id="0f5c3-123">Экземпляры Скоредпроперти определяют язык, используемый для определения параметра.</span><span class="sxs-lookup"><span data-stu-id="0f5c3-123">ScoredProperty instances define the language that is used to characterize an Option.</span></span> <span data-ttu-id="0f5c3-124">Экземпляры Скоредпроперти, определенные в ключевых словах схемы Print, позволяют экземплярам параметров, написанным множеством разных сторон, быть переносимыми для многих устройств, а также для понимания любым другим драйвером устройства или PrintCapabilities или поставщиком PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="0f5c3-124">The ScoredProperty instances defined in the Print Schema Keywords make it possible for Option instances written by many different parties for many devices to be portable, and to be understood by any other device driver or PrintCapabilities or PrintTicket provider.</span></span>

-   <span data-ttu-id="0f5c3-125">Экземпляры значений Скоредпроперти</span><span class="sxs-lookup"><span data-stu-id="0f5c3-125">ScoredProperty Value instances</span></span>

    -   <span data-ttu-id="0f5c3-126">Эти экземпляры значений предоставляются по той же причине, что предоставляются экземпляры Скоредпроперти.</span><span class="sxs-lookup"><span data-stu-id="0f5c3-126">These Value instances are provided for the same reason that ScoredProperty instances are provided.</span></span>

-   <span data-ttu-id="0f5c3-127">Экземпляры компонентов</span><span class="sxs-lookup"><span data-stu-id="0f5c3-127">Feature instances</span></span>

    -   <span data-ttu-id="0f5c3-128">Каждый параметр должен принадлежать к определенному компоненту, тем самым запросив, что сама функция должна быть определена.</span><span class="sxs-lookup"><span data-stu-id="0f5c3-128">Each Option must belong to a specific Feature, thereby requiring the Feature itself to be defined.</span></span>

-   <span data-ttu-id="0f5c3-129">Экземпляры Параметердеф</span><span class="sxs-lookup"><span data-stu-id="0f5c3-129">ParameterDef instances</span></span>

    -   <span data-ttu-id="0f5c3-130">Экземпляр Параметердеф, предоставляемый с помощью ключевых слов схемы печати, также определяет значение для каждого свойства, содержащегося в нем.</span><span class="sxs-lookup"><span data-stu-id="0f5c3-130">A Print Schema Keywords-supplied ParameterDef instance also defines a Value for each Property contained in it.</span></span> <span data-ttu-id="0f5c3-131">Поставщик PrintCapabilities может изменить экземпляры значений для экземпляров свойств, которые могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="0f5c3-131">The PrintCapabilities provider is free to modify the Value instances for those Property instances that can be changed.</span></span> <span data-ttu-id="0f5c3-132">Сведения о том, какие экземпляры свойств могут быть изменены и какие из них нельзя изменить (являются неизменяемыми), см. в разделе [элементы параметердеф и параметеринит](parameterdef-and-parameterinit-elements.md).</span><span class="sxs-lookup"><span data-stu-id="0f5c3-132">For information about which Property instances can be changed, and which cannot be changed (are immutable), see [ParameterDef and ParameterInit Elements](parameterdef-and-parameterinit-elements.md).</span></span>

<span data-ttu-id="0f5c3-133">Важно отметить, что схема PrintCapabilities не содержит имен экземпляров параметров.</span><span class="sxs-lookup"><span data-stu-id="0f5c3-133">It is important to note the PrintCapabilities Schema does not name any Option instances.</span></span> <span data-ttu-id="0f5c3-134">Экземпляры параметров характеризуются только экземплярами Скоредпроперти, созданными в целом.</span><span class="sxs-lookup"><span data-stu-id="0f5c3-134">Option instances are characterized solely by their ScoredProperty instances taken as a whole.</span></span> <span data-ttu-id="0f5c3-135">Распространенное заблуждение заключается в том, что использование атрибута Name для определения параметра определяет экземпляры параметров, но это неверно.</span><span class="sxs-lookup"><span data-stu-id="0f5c3-135">A common misconception is that using the 'name' attribute to define an Option identifies Option instances, but this is incorrect.</span></span> <span data-ttu-id="0f5c3-136">Элементы Option не обязательно должны быть уникальными для экземпляров параметров одноуровневого узла и не используют атрибут Name для определения требуемого параметра.</span><span class="sxs-lookup"><span data-stu-id="0f5c3-136">Option elements are not required to be unique for sibling Option instances, nor is using the 'name' attribute to define an Option required.</span></span>

<span data-ttu-id="0f5c3-137">В документе «печать ключевых слов схемы» определяется стандартное пространство имен, которому принадлежат все атрибуты имени экземпляра в схемах PrintCapabilities и PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="0f5c3-137">The Print Schema Keywords document defines a standard namespace to which all instance name attributes in the PrintCapabilities and PrintTicket schemas belong.</span></span> <span data-ttu-id="0f5c3-138">Все теги типов элементов и XML-атрибуты, используемые типами элементов, также принадлежат этому пространству имен.</span><span class="sxs-lookup"><span data-stu-id="0f5c3-138">All element type tags and XML Attributes used by the element types also belong to this namespace.</span></span>

<span data-ttu-id="0f5c3-139">Для каждого экземпляра, определенного в схеме PrintCapabilities, схема PrintCapabilities задает как атрибут имени, так и расположение экземпляра.</span><span class="sxs-lookup"><span data-stu-id="0f5c3-139">For each instance defined in the PrintCapabilities Schema, the PrintCapabilities Schema specifies both the name attribute and the location of the instance.</span></span> <span data-ttu-id="0f5c3-140">Поставщик и клиент должны сохранить оба варианта при использовании этого экземпляра в своем документе PrintCapabilities или PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="0f5c3-140">The provider and client must preserve both when using this instance in their PrintCapabilities document or PrintTicket.</span></span>

<span data-ttu-id="0f5c3-141">В документе о ключевых словах «Печать схемы» некоторые экземпляры обозначаются как обязательные.</span><span class="sxs-lookup"><span data-stu-id="0f5c3-141">The Print Schema Keywords document designates some instances as mandatory.</span></span> <span data-ttu-id="0f5c3-142">Эти экземпляры должны присутствовать в каждом документе PrintCapabilities и должны быть правильно инициализированы с допустимыми значениями.</span><span class="sxs-lookup"><span data-stu-id="0f5c3-142">These instances must appear in every PrintCapabilities document and must be properly initialized with valid Values.</span></span> <span data-ttu-id="0f5c3-143">Все экземпляры в ключевых словах схемы Print, которые не предназначены как обязательные, являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="0f5c3-143">All instances in the Print Schema Keywords that are not designated as mandatory are optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f5c3-144">См. также</span><span class="sxs-lookup"><span data-stu-id="0f5c3-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f5c3-145">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="0f5c3-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



