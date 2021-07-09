---
description: Проверьте элемент Пажефотопринтингинтент, настраиваемый пользователем. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: f9a00828-52df-449e-914b-4c6cd7c29f3a
title: пажефотопринтингинтент
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1cf9ae587062efc68b953f5931b55147940b1b
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548982"
---
# <a name="pagephotoprintingintent"></a><span data-ttu-id="ac8af-105">пажефотопринтингинтент</span><span class="sxs-lookup"><span data-stu-id="ac8af-105">PagePhotoPrintingIntent</span></span>

<span data-ttu-id="ac8af-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="ac8af-106">This topic is not current.</span></span> <span data-ttu-id="ac8af-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ac8af-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ac8af-108">Указывает на высокоуровневое назначение драйвера для заполнения параметров печати фотографий.</span><span class="sxs-lookup"><span data-stu-id="ac8af-108">Indicates a high-level intent to the driver for population of photo printing settings.</span></span> <span data-ttu-id="ac8af-109">Эти параметры имеют ожидаемое качество вывода, которое пользователь может указать при печати фотографий.</span><span class="sxs-lookup"><span data-stu-id="ac8af-109">These settings deal with the expected output quality a user may specify when printing photos.</span></span>

-   [<span data-ttu-id="ac8af-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ac8af-110">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="ac8af-111">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="ac8af-111">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="ac8af-112">XML-содержимое</span><span class="sxs-lookup"><span data-stu-id="ac8af-112">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ac8af-113">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ac8af-113">Element Information</span></span>



| <span data-ttu-id="ac8af-114">Имя</span><span class="sxs-lookup"><span data-stu-id="ac8af-114">Name</span></span> | <span data-ttu-id="ac8af-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ac8af-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="ac8af-116">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="ac8af-116">Element Type</span></span> <br/>   | <span data-ttu-id="ac8af-117">Компонент</span><span class="sxs-lookup"><span data-stu-id="ac8af-117">Feature</span></span><br/> |
| <span data-ttu-id="ac8af-118">Префикс области</span><span class="sxs-lookup"><span data-stu-id="ac8af-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ac8af-119">Страница</span><span class="sxs-lookup"><span data-stu-id="ac8af-119">Page</span></span><br/>    |
| <span data-ttu-id="ac8af-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="ac8af-120">Notes</span></span> <br/>          | <span data-ttu-id="ac8af-121">Нет</span><span class="sxs-lookup"><span data-stu-id="ac8af-121">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="ac8af-122">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="ac8af-122">Structural Content</span></span>

<span data-ttu-id="ac8af-123">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="ac8af-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="ac8af-124">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="ac8af-124">Structure Variables</span></span>

<span data-ttu-id="ac8af-125">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="ac8af-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ac8af-126">Имя</span><span class="sxs-lookup"><span data-stu-id="ac8af-126">Name</span></span>                               | <span data-ttu-id="ac8af-127">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ac8af-127">Data type</span></span>         | <span data-ttu-id="ac8af-128">Unit</span><span class="sxs-lookup"><span data-stu-id="ac8af-128">Unit</span></span>                  | <span data-ttu-id="ac8af-129">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="ac8af-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="ac8af-130">Итоги</span><span class="sxs-lookup"><span data-stu-id="ac8af-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ac8af-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="ac8af-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="ac8af-132">строка</span><span class="sxs-lookup"><span data-stu-id="ac8af-132">string</span></span><br/> | <span data-ttu-id="ac8af-133">characters</span><span class="sxs-lookup"><span data-stu-id="ac8af-133">characters</span></span><br/> | <span data-ttu-id="ac8af-134">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="ac8af-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ac8af-135">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ac8af-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ac8af-136">Имя параметра</span><span class="sxs-lookup"><span data-stu-id="ac8af-136">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="ac8af-137">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="ac8af-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="ac8af-138">строка</span><span class="sxs-lookup"><span data-stu-id="ac8af-138">string</span></span><br/> | <span data-ttu-id="ac8af-139">Н/Д</span><span class="sxs-lookup"><span data-stu-id="ac8af-139">n/a</span></span><br/>        | <span data-ttu-id="ac8af-140">True, False</span><span class="sxs-lookup"><span data-stu-id="ac8af-140">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="ac8af-141">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="ac8af-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ac8af-142">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="ac8af-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="ac8af-143">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="ac8af-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="ac8af-144">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="ac8af-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="ac8af-145">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="ac8af-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac8af-146">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="ac8af-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




