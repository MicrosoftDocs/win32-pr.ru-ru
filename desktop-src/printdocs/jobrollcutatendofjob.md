---
description: Сведения об элементе Жоброллкутатендофжоб, который описывает метод обрезания рулонной бумаги. Накат должен быть обрезан в конце задания.
ms.assetid: 1e2cd767-685b-47d8-9020-a0a5dda63506
title: жоброллкутатендофжоб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11fdb973f3fda9fea28f64f0edb232910f2d2201
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408667"
---
# <a name="jobrollcutatendofjob"></a><span data-ttu-id="668e9-104">жоброллкутатендофжоб</span><span class="sxs-lookup"><span data-stu-id="668e9-104">JobRollCutAtEndOfJob</span></span>

<span data-ttu-id="668e9-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="668e9-105">This topic is not current.</span></span> <span data-ttu-id="668e9-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="668e9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="668e9-107">Описывает метод обрезания рулонной бумаги.</span><span class="sxs-lookup"><span data-stu-id="668e9-107">Describes the cutting method for roll paper.</span></span> <span data-ttu-id="668e9-108">Накат должен быть обрезан в конце задания.</span><span class="sxs-lookup"><span data-stu-id="668e9-108">The roll should be cut at the end of the job.</span></span>

-   [<span data-ttu-id="668e9-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="668e9-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="668e9-110">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="668e9-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="668e9-111">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="668e9-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="668e9-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="668e9-112">Element Information</span></span>



| <span data-ttu-id="668e9-113">Имя</span><span class="sxs-lookup"><span data-stu-id="668e9-113">Name</span></span> | <span data-ttu-id="668e9-114">Значение</span><span class="sxs-lookup"><span data-stu-id="668e9-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="668e9-115">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="668e9-115">Element Type</span></span> <br/>   | <span data-ttu-id="668e9-116">Компонент</span><span class="sxs-lookup"><span data-stu-id="668e9-116">Feature</span></span><br/> |
| <span data-ttu-id="668e9-117">Префикс области</span><span class="sxs-lookup"><span data-stu-id="668e9-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="668e9-118">Задание</span><span class="sxs-lookup"><span data-stu-id="668e9-118">Job</span></span><br/>     |
| <span data-ttu-id="668e9-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="668e9-119">Notes</span></span> <br/>          | <span data-ttu-id="668e9-120">Нет</span><span class="sxs-lookup"><span data-stu-id="668e9-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="668e9-121">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="668e9-121">Structural Content</span></span>

<span data-ttu-id="668e9-122">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="668e9-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobRollCutAtEndOfJobAtEndOfJob">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="668e9-123">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="668e9-123">Structure Variables</span></span>

<span data-ttu-id="668e9-124">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="668e9-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="668e9-125">Имя</span><span class="sxs-lookup"><span data-stu-id="668e9-125">Name</span></span>                               | <span data-ttu-id="668e9-126">Тип данных</span><span class="sxs-lookup"><span data-stu-id="668e9-126">Data type</span></span>         | <span data-ttu-id="668e9-127">Unit</span><span class="sxs-lookup"><span data-stu-id="668e9-127">Unit</span></span>                  | <span data-ttu-id="668e9-128">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="668e9-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="668e9-129">Итоги</span><span class="sxs-lookup"><span data-stu-id="668e9-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="668e9-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="668e9-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="668e9-131">строка</span><span class="sxs-lookup"><span data-stu-id="668e9-131">string</span></span><br/> | <span data-ttu-id="668e9-132">characters</span><span class="sxs-lookup"><span data-stu-id="668e9-132">characters</span></span><br/> | <span data-ttu-id="668e9-133">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="668e9-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="668e9-134">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="668e9-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="668e9-135">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="668e9-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="668e9-136">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="668e9-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="668e9-137">строка</span><span class="sxs-lookup"><span data-stu-id="668e9-137">string</span></span><br/> | <span data-ttu-id="668e9-138">Недоступно</span><span class="sxs-lookup"><span data-stu-id="668e9-138">n/a</span></span><br/>        | <span data-ttu-id="668e9-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="668e9-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="668e9-140">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="668e9-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="668e9-141">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="668e9-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="668e9-142">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="668e9-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="668e9-143">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="668e9-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobRollCutAtEndOfJob">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!--Specifies cutting at the edge of the image -->
  <psf:Option name="psk:CutSheetAtImageEdge" />
  <!--Specifies cutting for standard media size -->
  <psf:Option name="psk:CutSheetAtStandardMediaSize" />
  <!--Specifies no job roll cut -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="668e9-144">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="668e9-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="668e9-145">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="668e9-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




