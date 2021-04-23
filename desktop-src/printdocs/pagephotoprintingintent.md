---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: f9a00828-52df-449e-914b-4c6cd7c29f3a
title: пажефотопринтингинтент
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3985d6f21d0d7731d1c08d080d64a4948b58196d
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "104547495"
---
# <a name="pagephotoprintingintent"></a><span data-ttu-id="cf292-104">пажефотопринтингинтент</span><span class="sxs-lookup"><span data-stu-id="cf292-104">PagePhotoPrintingIntent</span></span>

<span data-ttu-id="cf292-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="cf292-105">This topic is not current.</span></span> <span data-ttu-id="cf292-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="cf292-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="cf292-107">Указывает на высокоуровневое назначение драйвера для заполнения параметров печати фотографий.</span><span class="sxs-lookup"><span data-stu-id="cf292-107">Indicates a high-level intent to the driver for population of photo printing settings.</span></span> <span data-ttu-id="cf292-108">Эти параметры имеют ожидаемое качество вывода, которое пользователь может указать при печати фотографий.</span><span class="sxs-lookup"><span data-stu-id="cf292-108">These settings deal with the expected output quality a user may specify when printing photos.</span></span>

-   [<span data-ttu-id="cf292-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="cf292-109">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="cf292-110">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="cf292-110">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="cf292-111">XML-содержимое</span><span class="sxs-lookup"><span data-stu-id="cf292-111">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="cf292-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="cf292-112">Element Information</span></span>



| <span data-ttu-id="cf292-113">Имя</span><span class="sxs-lookup"><span data-stu-id="cf292-113">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="cf292-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="cf292-114">Element Type</span></span> <br/>   | <span data-ttu-id="cf292-115">Функция</span><span class="sxs-lookup"><span data-stu-id="cf292-115">Feature</span></span><br/> |
| <span data-ttu-id="cf292-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="cf292-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="cf292-117">Страница</span><span class="sxs-lookup"><span data-stu-id="cf292-117">Page</span></span><br/>    |
| <span data-ttu-id="cf292-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="cf292-118">Notes</span></span> <br/>          | <span data-ttu-id="cf292-119">Нет</span><span class="sxs-lookup"><span data-stu-id="cf292-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="cf292-120">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="cf292-120">Structural Content</span></span>

<span data-ttu-id="cf292-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="cf292-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="cf292-122">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="cf292-122">Structure Variables</span></span>

<span data-ttu-id="cf292-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="cf292-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="cf292-124">Имя</span><span class="sxs-lookup"><span data-stu-id="cf292-124">Name</span></span>                               | <span data-ttu-id="cf292-125">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cf292-125">Data type</span></span>         | <span data-ttu-id="cf292-126">Unit</span><span class="sxs-lookup"><span data-stu-id="cf292-126">Unit</span></span>                  | <span data-ttu-id="cf292-127">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="cf292-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="cf292-128">Сводка</span><span class="sxs-lookup"><span data-stu-id="cf292-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="cf292-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="cf292-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="cf292-130">строка</span><span class="sxs-lookup"><span data-stu-id="cf292-130">string</span></span><br/> | <span data-ttu-id="cf292-131">characters</span><span class="sxs-lookup"><span data-stu-id="cf292-131">characters</span></span><br/> | <span data-ttu-id="cf292-132">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="cf292-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="cf292-133">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cf292-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="cf292-134">Имя параметра</span><span class="sxs-lookup"><span data-stu-id="cf292-134">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="cf292-135">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="cf292-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="cf292-136">строка</span><span class="sxs-lookup"><span data-stu-id="cf292-136">string</span></span><br/> | <span data-ttu-id="cf292-137">Недоступно</span><span class="sxs-lookup"><span data-stu-id="cf292-137">n/a</span></span><br/>        | <span data-ttu-id="cf292-138">True, False</span><span class="sxs-lookup"><span data-stu-id="cf292-138">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="cf292-139">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="cf292-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="cf292-140">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="cf292-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="cf292-141">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="cf292-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="cf292-142">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="cf292-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="cf292-143">См. также</span><span class="sxs-lookup"><span data-stu-id="cf292-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf292-144">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="cf292-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




