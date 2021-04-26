---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: f9a00828-52df-449e-914b-4c6cd7c29f3a
title: пажефотопринтингинтент
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01d56a0b46c73bb3afdcefe96dc2131c861d5419
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997981"
---
# <a name="pagephotoprintingintent"></a><span data-ttu-id="a1197-104">пажефотопринтингинтент</span><span class="sxs-lookup"><span data-stu-id="a1197-104">PagePhotoPrintingIntent</span></span>

<span data-ttu-id="a1197-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="a1197-105">This topic is not current.</span></span> <span data-ttu-id="a1197-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a1197-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a1197-107">Указывает на высокоуровневое назначение драйвера для заполнения параметров печати фотографий.</span><span class="sxs-lookup"><span data-stu-id="a1197-107">Indicates a high-level intent to the driver for population of photo printing settings.</span></span> <span data-ttu-id="a1197-108">Эти параметры имеют ожидаемое качество вывода, которое пользователь может указать при печати фотографий.</span><span class="sxs-lookup"><span data-stu-id="a1197-108">These settings deal with the expected output quality a user may specify when printing photos.</span></span>

-   [<span data-ttu-id="a1197-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="a1197-109">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="a1197-110">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="a1197-110">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="a1197-111">XML-содержимое</span><span class="sxs-lookup"><span data-stu-id="a1197-111">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a1197-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="a1197-112">Element Information</span></span>



| <span data-ttu-id="a1197-113">Имя</span><span class="sxs-lookup"><span data-stu-id="a1197-113">Name</span></span> | <span data-ttu-id="a1197-114">Значение</span><span class="sxs-lookup"><span data-stu-id="a1197-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="a1197-115">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="a1197-115">Element Type</span></span> <br/>   | <span data-ttu-id="a1197-116">Компонент</span><span class="sxs-lookup"><span data-stu-id="a1197-116">Feature</span></span><br/> |
| <span data-ttu-id="a1197-117">Префикс области</span><span class="sxs-lookup"><span data-stu-id="a1197-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a1197-118">Страница</span><span class="sxs-lookup"><span data-stu-id="a1197-118">Page</span></span><br/>    |
| <span data-ttu-id="a1197-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="a1197-119">Notes</span></span> <br/>          | <span data-ttu-id="a1197-120">Нет</span><span class="sxs-lookup"><span data-stu-id="a1197-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="a1197-121">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="a1197-121">Structural Content</span></span>

<span data-ttu-id="a1197-122">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="a1197-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PagePhotoPrintingIntent">  
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
    <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
  </psf:Property>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="a1197-123">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="a1197-123">Structure Variables</span></span>

<span data-ttu-id="a1197-124">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="a1197-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a1197-125">Имя</span><span class="sxs-lookup"><span data-stu-id="a1197-125">Name</span></span>                               | <span data-ttu-id="a1197-126">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a1197-126">Data type</span></span>         | <span data-ttu-id="a1197-127">Unit</span><span class="sxs-lookup"><span data-stu-id="a1197-127">Unit</span></span>                  | <span data-ttu-id="a1197-128">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="a1197-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a1197-129">Сводка</span><span class="sxs-lookup"><span data-stu-id="a1197-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a1197-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="a1197-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="a1197-131">строка</span><span class="sxs-lookup"><span data-stu-id="a1197-131">string</span></span><br/> | <span data-ttu-id="a1197-132">characters</span><span class="sxs-lookup"><span data-stu-id="a1197-132">characters</span></span><br/> | <span data-ttu-id="a1197-133">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="a1197-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a1197-134">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a1197-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a1197-135">Имя параметра</span><span class="sxs-lookup"><span data-stu-id="a1197-135">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="a1197-136">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="a1197-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="a1197-137">строка</span><span class="sxs-lookup"><span data-stu-id="a1197-137">string</span></span><br/> | <span data-ttu-id="a1197-138">Недоступно</span><span class="sxs-lookup"><span data-stu-id="a1197-138">n/a</span></span><br/>        | <span data-ttu-id="a1197-139">True, False</span><span class="sxs-lookup"><span data-stu-id="a1197-139">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="a1197-140">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="a1197-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a1197-141">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="a1197-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a1197-142">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="a1197-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a1197-143">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="a1197-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PagePhotoPrintingIntent">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- No Photoprinting Intent (Allows the application to specify no intent resolution.  (PrintTicket settings should not be altered) -->
  <psf:Option name="psk:None" />
  <!-- Best Quality Photoprinting (Provided mostly for marketing reasons; utilizes the highest capabilities of the device) -->
  <psf:Option name="psk:PhotoBest" />
  <!-- Draft Quality Photoprinting (Quick, low ink volume print for proofing purposes) -->
  <psf:Option name="psk:PhotoDraft" />
  <!-- Standard Quality Photoprinting (OEM suggested settings for standard photo-printing) -->
  <psf:Option name="psk:PhotoStandard" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="a1197-144">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="a1197-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1197-145">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="a1197-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




