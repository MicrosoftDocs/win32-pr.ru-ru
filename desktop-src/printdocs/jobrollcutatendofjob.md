---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 1e2cd767-685b-47d8-9020-a0a5dda63506
title: жоброллкутатендофжоб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 178b045546552048b2a66a1c0824645c1720b1a7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993941"
---
# <a name="jobrollcutatendofjob"></a><span data-ttu-id="b4223-104">жоброллкутатендофжоб</span><span class="sxs-lookup"><span data-stu-id="b4223-104">JobRollCutAtEndOfJob</span></span>

<span data-ttu-id="b4223-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="b4223-105">This topic is not current.</span></span> <span data-ttu-id="b4223-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b4223-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b4223-107">Описывает метод обрезания рулонной бумаги.</span><span class="sxs-lookup"><span data-stu-id="b4223-107">Describes the cutting method for roll paper.</span></span> <span data-ttu-id="b4223-108">Накат должен быть обрезан в конце задания.</span><span class="sxs-lookup"><span data-stu-id="b4223-108">The roll should be cut at the end of the job.</span></span>

-   [<span data-ttu-id="b4223-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b4223-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b4223-110">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="b4223-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="b4223-111">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="b4223-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="b4223-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b4223-112">Element Information</span></span>



| <span data-ttu-id="b4223-113">Имя</span><span class="sxs-lookup"><span data-stu-id="b4223-113">Name</span></span> | <span data-ttu-id="b4223-114">Значение</span><span class="sxs-lookup"><span data-stu-id="b4223-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="b4223-115">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="b4223-115">Element Type</span></span> <br/>   | <span data-ttu-id="b4223-116">Компонент</span><span class="sxs-lookup"><span data-stu-id="b4223-116">Feature</span></span><br/> |
| <span data-ttu-id="b4223-117">Префикс области</span><span class="sxs-lookup"><span data-stu-id="b4223-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b4223-118">Задание</span><span class="sxs-lookup"><span data-stu-id="b4223-118">Job</span></span><br/>     |
| <span data-ttu-id="b4223-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="b4223-119">Notes</span></span> <br/>          | <span data-ttu-id="b4223-120">Нет</span><span class="sxs-lookup"><span data-stu-id="b4223-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="b4223-121">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="b4223-121">Structural Content</span></span>

<span data-ttu-id="b4223-122">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="b4223-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="b4223-123">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="b4223-123">Structure Variables</span></span>

<span data-ttu-id="b4223-124">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="b4223-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b4223-125">Имя</span><span class="sxs-lookup"><span data-stu-id="b4223-125">Name</span></span>                               | <span data-ttu-id="b4223-126">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b4223-126">Data type</span></span>         | <span data-ttu-id="b4223-127">Unit</span><span class="sxs-lookup"><span data-stu-id="b4223-127">Unit</span></span>                  | <span data-ttu-id="b4223-128">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="b4223-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="b4223-129">Сводка</span><span class="sxs-lookup"><span data-stu-id="b4223-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="b4223-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="b4223-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="b4223-131">строка</span><span class="sxs-lookup"><span data-stu-id="b4223-131">string</span></span><br/> | <span data-ttu-id="b4223-132">characters</span><span class="sxs-lookup"><span data-stu-id="b4223-132">characters</span></span><br/> | <span data-ttu-id="b4223-133">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="b4223-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="b4223-134">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b4223-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="b4223-135">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="b4223-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="b4223-136">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="b4223-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="b4223-137">строка</span><span class="sxs-lookup"><span data-stu-id="b4223-137">string</span></span><br/> | <span data-ttu-id="b4223-138">Недоступно</span><span class="sxs-lookup"><span data-stu-id="b4223-138">n/a</span></span><br/>        | <span data-ttu-id="b4223-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="b4223-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="b4223-140">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="b4223-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="b4223-141">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="b4223-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="b4223-142">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="b4223-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="b4223-143">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="b4223-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="b4223-144">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="b4223-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4223-145">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="b4223-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




