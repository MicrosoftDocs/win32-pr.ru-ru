---
description: Описывает пространство имен.
ms.assetid: 8e31526a-639f-481b-91f1-fcd376818cbf
title: элемент nameSpace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a8747a25988b880d5287d959273fa0f4d144045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544799"
---
# <a name="namespace-element"></a><span data-ttu-id="06f54-103">элемент nameSpace</span><span class="sxs-lookup"><span data-stu-id="06f54-103">nameSpace element</span></span>

<span data-ttu-id="06f54-104">Описывает пространство имен.</span><span class="sxs-lookup"><span data-stu-id="06f54-104">Describes a namespace.</span></span> <span data-ttu-id="06f54-105">Это пространство имен может использоваться для создания кода или для обработки <директивы> WSDL: Import.</span><span class="sxs-lookup"><span data-stu-id="06f54-105">This namespace may be used for code generation or for handling <wsdl:import> directives.</span></span>

## <a name="usage"></a><span data-ttu-id="06f54-106">Использование</span><span class="sxs-lookup"><span data-stu-id="06f54-106">Usage</span></span>

``` syntax
<nameSpace
  uri = "character_string">
  child elements
</nameSpace>
```

## <a name="attributes"></a><span data-ttu-id="06f54-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="06f54-107">Attributes</span></span>



| <span data-ttu-id="06f54-108">attribute</span><span class="sxs-lookup"><span data-stu-id="06f54-108">Attribute</span></span>          | <span data-ttu-id="06f54-109">Тип</span><span class="sxs-lookup"><span data-stu-id="06f54-109">Type</span></span>                         | <span data-ttu-id="06f54-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="06f54-110">Required</span></span>       | <span data-ttu-id="06f54-111">Описание</span><span class="sxs-lookup"><span data-stu-id="06f54-111">Description</span></span>                                             |
|--------------------|------------------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="06f54-112">**uri**</span><span class="sxs-lookup"><span data-stu-id="06f54-112">**uri**</span></span><br/> | <span data-ttu-id="06f54-113">Символьная \_ строка</span><span class="sxs-lookup"><span data-stu-id="06f54-113">character\_string</span></span><br/> | <span data-ttu-id="06f54-114">Да</span><span class="sxs-lookup"><span data-stu-id="06f54-114">Yes</span></span><br/> | <span data-ttu-id="06f54-115">Уникальный URI пространства имен.</span><span class="sxs-lookup"><span data-stu-id="06f54-115">The unique URI of the namespace.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="06f54-116">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="06f54-116">Child elements</span></span>



| <span data-ttu-id="06f54-117">Элемент</span><span class="sxs-lookup"><span data-stu-id="06f54-117">Element</span></span>                                               | <span data-ttu-id="06f54-118">Описание</span><span class="sxs-lookup"><span data-stu-id="06f54-118">Description</span></span>                                                                                              |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06f54-119">**Обеспечения**</span><span class="sxs-lookup"><span data-stu-id="06f54-119">**codeName**</span></span>](codename.md)<br/>               | <span data-ttu-id="06f54-120">Имя, используемое для обнаружения пространства имен в созданном коде.</span><span class="sxs-lookup"><span data-stu-id="06f54-120">The name to be used to identify the namespace in generated code.</span></span><br/> <br/>                  |
| [<span data-ttu-id="06f54-121">**макропрефикс**</span><span class="sxs-lookup"><span data-stu-id="06f54-121">**macroPrefix**</span></span>](macroprefix.md)<br/>         | <span data-ttu-id="06f54-122">Префикс, который будет использоваться в созданном коде для имен макросов в пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="06f54-122">The prefix to be used in the generated code for names of macros in the namespace.</span></span><br/> <br/> |
| [<span data-ttu-id="06f54-123">**безымян**</span><span class="sxs-lookup"><span data-stu-id="06f54-123">**name**</span></span>](name.md)<br/>                       | <span data-ttu-id="06f54-124">Полное имя в пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="06f54-124">A qualified name in the namespace.</span></span><br/> <br/>                                                |
| [<span data-ttu-id="06f54-125">**преферредпрефикс**</span><span class="sxs-lookup"><span data-stu-id="06f54-125">**preferredPrefix**</span></span>](preferredprefix.md)<br/> | <span data-ttu-id="06f54-126">Префикс, с которым должно быть сопоставлено пространство имен, чтобы сделать XML более удобочитаемым.</span><span class="sxs-lookup"><span data-stu-id="06f54-126">The prefix to which the namespace should be mapped to make the XML more readable.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="06f54-127">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="06f54-127">Child element sequence</span></span>

``` syntax
(
  preferredPrefix?, 
  macroPrefix?, 
  codeName?, 
  name*
)
```

## <a name="parent-elements"></a><span data-ttu-id="06f54-128">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="06f54-128">Parent elements</span></span>



| <span data-ttu-id="06f54-129">Элемент</span><span class="sxs-lookup"><span data-stu-id="06f54-129">Element</span></span>                                     | <span data-ttu-id="06f54-130">Описание</span><span class="sxs-lookup"><span data-stu-id="06f54-130">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="06f54-131">**всдкодежен**</span><span class="sxs-lookup"><span data-stu-id="06f54-131">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="06f54-132">Корневой элемент XML-файла скрипта генератора кода WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="06f54-132">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="06f54-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="06f54-133">Remarks</span></span>

<span data-ttu-id="06f54-134">Этот элемент может использоваться для предоставления генератору кода дополнительных сведений о пространствах имен, которые встречаются в файлах WSDL и XSD, или для добавления новых пространств имен.</span><span class="sxs-lookup"><span data-stu-id="06f54-134">This element may be used to provide the code generator with additional information about namespaces that it encounters in WSDL and XSD files or to introduce new namespaces.</span></span>

<span data-ttu-id="06f54-135">Пространства имен, подразумеваемые отражением типа или указанные в WSDL-и XSD-файлах, автоматически анализируются генератором кода и не обязательно должны быть определены в скрипте явным образом.</span><span class="sxs-lookup"><span data-stu-id="06f54-135">Namespaces implied by type reflection or specified in WSDL and XSD files are parsed automatically by the code generator and do not have to be explicitly defined in the script.</span></span> <span data-ttu-id="06f54-136">В некоторых случаях этот элемент можно использовать для добавления дополнительных свойств или имен к пространству имен, на которое ссылается отражение типов или WSDL/XSD.</span><span class="sxs-lookup"><span data-stu-id="06f54-136">In some cases, this element can be used to add additional properties or names to a namespace that is referenced by type reflection or WSDL/XSD.</span></span> <span data-ttu-id="06f54-137">Генератор кода не учитывает это в качестве конфликта.</span><span class="sxs-lookup"><span data-stu-id="06f54-137">The code generator does not regard this as a conflict.</span></span>

<span data-ttu-id="06f54-138">В следующем XML-коде показан элемент nameSpace (для краткости опущены дочерние элементы).</span><span class="sxs-lookup"><span data-stu-id="06f54-138">The following XML shows a nameSpace element (with children omitted for brevity).</span></span>

``` syntax
<nameSpace uri="https://www.example.com/namespace">
  ...
</nameSpace>
```

## <a name="element-information"></a><span data-ttu-id="06f54-139">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="06f54-139">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="06f54-140">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="06f54-140">Minimum supported system</span></span><br/> | <span data-ttu-id="06f54-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="06f54-141">Windows Vista</span></span> |
| <span data-ttu-id="06f54-142">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="06f54-142">Can be empty</span></span>                        | <span data-ttu-id="06f54-143">Да</span><span class="sxs-lookup"><span data-stu-id="06f54-143">Yes</span></span>           |



 

 




