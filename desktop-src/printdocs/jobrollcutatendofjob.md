---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 1e2cd767-685b-47d8-9020-a0a5dda63506
title: жоброллкутатендофжоб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62eda63fe0d801bc1039af2c514c284440b1be47
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "105713353"
---
# <a name="jobrollcutatendofjob"></a><span data-ttu-id="a4767-104">жоброллкутатендофжоб</span><span class="sxs-lookup"><span data-stu-id="a4767-104">JobRollCutAtEndOfJob</span></span>

<span data-ttu-id="a4767-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="a4767-105">This topic is not current.</span></span> <span data-ttu-id="a4767-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a4767-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a4767-107">Описывает метод обрезания рулонной бумаги.</span><span class="sxs-lookup"><span data-stu-id="a4767-107">Describes the cutting method for roll paper.</span></span> <span data-ttu-id="a4767-108">Накат должен быть обрезан в конце задания.</span><span class="sxs-lookup"><span data-stu-id="a4767-108">The roll should be cut at the end of the job.</span></span>

-   [<span data-ttu-id="a4767-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="a4767-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a4767-110">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="a4767-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a4767-111">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="a4767-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a4767-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="a4767-112">Element Information</span></span>



| <span data-ttu-id="a4767-113">Имя</span><span class="sxs-lookup"><span data-stu-id="a4767-113">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="a4767-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="a4767-114">Element Type</span></span> <br/>   | <span data-ttu-id="a4767-115">Функция</span><span class="sxs-lookup"><span data-stu-id="a4767-115">Feature</span></span><br/> |
| <span data-ttu-id="a4767-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="a4767-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a4767-117">Задание</span><span class="sxs-lookup"><span data-stu-id="a4767-117">Job</span></span><br/>     |
| <span data-ttu-id="a4767-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="a4767-118">Notes</span></span> <br/>          | <span data-ttu-id="a4767-119">Нет</span><span class="sxs-lookup"><span data-stu-id="a4767-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="a4767-120">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="a4767-120">Structural Content</span></span>

<span data-ttu-id="a4767-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="a4767-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="a4767-122">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="a4767-122">Structure Variables</span></span>

<span data-ttu-id="a4767-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="a4767-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a4767-124">Имя</span><span class="sxs-lookup"><span data-stu-id="a4767-124">Name</span></span>                               | <span data-ttu-id="a4767-125">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a4767-125">Data type</span></span>         | <span data-ttu-id="a4767-126">Unit</span><span class="sxs-lookup"><span data-stu-id="a4767-126">Unit</span></span>                  | <span data-ttu-id="a4767-127">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="a4767-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a4767-128">Сводка</span><span class="sxs-lookup"><span data-stu-id="a4767-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a4767-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="a4767-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="a4767-130">строка</span><span class="sxs-lookup"><span data-stu-id="a4767-130">string</span></span><br/> | <span data-ttu-id="a4767-131">characters</span><span class="sxs-lookup"><span data-stu-id="a4767-131">characters</span></span><br/> | <span data-ttu-id="a4767-132">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="a4767-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a4767-133">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a4767-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a4767-134">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="a4767-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="a4767-135">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="a4767-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="a4767-136">строка</span><span class="sxs-lookup"><span data-stu-id="a4767-136">string</span></span><br/> | <span data-ttu-id="a4767-137">Недоступно</span><span class="sxs-lookup"><span data-stu-id="a4767-137">n/a</span></span><br/>        | <span data-ttu-id="a4767-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="a4767-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="a4767-139">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="a4767-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a4767-140">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="a4767-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a4767-141">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="a4767-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a4767-142">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="a4767-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="a4767-143">См. также</span><span class="sxs-lookup"><span data-stu-id="a4767-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4767-144">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="a4767-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




