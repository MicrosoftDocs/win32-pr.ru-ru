---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 0592f7a4-cace-41b0-91e3-2811f72aeb3e
title: жобдигиталсигнатурепроцессинг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aad9dbe0ba82d219a28602178efa2e102ccf167b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998291"
---
# <a name="jobdigitalsignatureprocessing"></a><span data-ttu-id="0c01e-104">жобдигиталсигнатурепроцессинг</span><span class="sxs-lookup"><span data-stu-id="0c01e-104">JobDigitalSignatureProcessing</span></span>

<span data-ttu-id="0c01e-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="0c01e-105">This topic is not current.</span></span> <span data-ttu-id="0c01e-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0c01e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0c01e-107">Описывает настройку обработки цифровых подписей для всего задания.</span><span class="sxs-lookup"><span data-stu-id="0c01e-107">Describes configuring the digital signature processing for the entire job.</span></span> <span data-ttu-id="0c01e-108">Применяется только к содержимому, содержащему цифровые подписи.</span><span class="sxs-lookup"><span data-stu-id="0c01e-108">Applicable only to content that contains digital signatures.</span></span>

-   [<span data-ttu-id="0c01e-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="0c01e-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0c01e-110">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="0c01e-110">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="0c01e-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="0c01e-111">Element Information</span></span>



| <span data-ttu-id="0c01e-112">Имя</span><span class="sxs-lookup"><span data-stu-id="0c01e-112">Name</span></span> | <span data-ttu-id="0c01e-113">Значение</span><span class="sxs-lookup"><span data-stu-id="0c01e-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="0c01e-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="0c01e-114">Element Type</span></span> <br/>   | <span data-ttu-id="0c01e-115">Компонент</span><span class="sxs-lookup"><span data-stu-id="0c01e-115">Feature</span></span><br/> |
| <span data-ttu-id="0c01e-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="0c01e-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0c01e-117">Задание</span><span class="sxs-lookup"><span data-stu-id="0c01e-117">Job</span></span><br/>     |
| <span data-ttu-id="0c01e-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="0c01e-118">Notes</span></span> <br/>          | <span data-ttu-id="0c01e-119">Нет</span><span class="sxs-lookup"><span data-stu-id="0c01e-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="0c01e-120">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="0c01e-120">Structural Content</span></span>

<span data-ttu-id="0c01e-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="0c01e-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobDigitalSignatureProcessing">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="0c01e-122">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="0c01e-122">Structure Variables</span></span>

<span data-ttu-id="0c01e-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="0c01e-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0c01e-124">Имя</span><span class="sxs-lookup"><span data-stu-id="0c01e-124">Name</span></span>                               | <span data-ttu-id="0c01e-125">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0c01e-125">Data type</span></span>         | <span data-ttu-id="0c01e-126">Unit</span><span class="sxs-lookup"><span data-stu-id="0c01e-126">Unit</span></span>                   | <span data-ttu-id="0c01e-127">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="0c01e-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="0c01e-128">Сводка</span><span class="sxs-lookup"><span data-stu-id="0c01e-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="0c01e-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="0c01e-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="0c01e-130">строка</span><span class="sxs-lookup"><span data-stu-id="0c01e-130">string</span></span><br/> | <span data-ttu-id="0c01e-131">characters</span><span class="sxs-lookup"><span data-stu-id="0c01e-131">characters</span></span> <br/> | <span data-ttu-id="0c01e-132">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="0c01e-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="0c01e-133">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0c01e-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="0c01e-134">Имя параметра</span><span class="sxs-lookup"><span data-stu-id="0c01e-134">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="0c01e-135">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="0c01e-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="0c01e-136">строка</span><span class="sxs-lookup"><span data-stu-id="0c01e-136">string</span></span><br/> | <span data-ttu-id="0c01e-137">Недоступно</span><span class="sxs-lookup"><span data-stu-id="0c01e-137">n/a</span></span><br/>         | <span data-ttu-id="0c01e-138">True, False</span><span class="sxs-lookup"><span data-stu-id="0c01e-138">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="0c01e-139">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="0c01e-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="0c01e-140">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="0c01e-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="0c01e-141">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="0c01e-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="0c01e-142">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="0c01e-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobDigitalSignatureProcessing">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- Print the job regardless of the validity of the digital signatures. Digital signatures MAY be ignored.  -->
  <psf:Option name="psk:PrintInvalidSignatures" />
  <!-- Print the job regardless of the validity of the digital signatures.  In the event an invalid signature is encountered, an error page should print at the end of the job.  Digital signatures MUST not be ignored. -->
  <psf:Option name="psk:PrintInvalidSignaturesWithErrorReport" />
  <!-- Print the job only if all digital signatures are valid.  Digital signatures MUST not be ignored. -->
  <psf:Option name="psk:PrintOnlyValidSignatures" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="0c01e-143">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="0c01e-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c01e-144">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="0c01e-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




