---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 0592f7a4-cace-41b0-91e3-2811f72aeb3e
title: жобдигиталсигнатурепроцессинг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2c60fd005f42bd3f9861e86156a7da9164a81e
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "105684824"
---
# <a name="jobdigitalsignatureprocessing"></a><span data-ttu-id="2e5d7-104">жобдигиталсигнатурепроцессинг</span><span class="sxs-lookup"><span data-stu-id="2e5d7-104">JobDigitalSignatureProcessing</span></span>

<span data-ttu-id="2e5d7-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="2e5d7-105">This topic is not current.</span></span> <span data-ttu-id="2e5d7-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2e5d7-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2e5d7-107">Описывает настройку обработки цифровых подписей для всего задания.</span><span class="sxs-lookup"><span data-stu-id="2e5d7-107">Describes configuring the digital signature processing for the entire job.</span></span> <span data-ttu-id="2e5d7-108">Применяется только к содержимому, содержащему цифровые подписи.</span><span class="sxs-lookup"><span data-stu-id="2e5d7-108">Applicable only to content that contains digital signatures.</span></span>

-   [<span data-ttu-id="2e5d7-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="2e5d7-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2e5d7-110">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="2e5d7-110">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="2e5d7-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="2e5d7-111">Element Information</span></span>



| <span data-ttu-id="2e5d7-112">Имя</span><span class="sxs-lookup"><span data-stu-id="2e5d7-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="2e5d7-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="2e5d7-113">Element Type</span></span> <br/>   | <span data-ttu-id="2e5d7-114">Функция</span><span class="sxs-lookup"><span data-stu-id="2e5d7-114">Feature</span></span><br/> |
| <span data-ttu-id="2e5d7-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="2e5d7-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2e5d7-116">Задание</span><span class="sxs-lookup"><span data-stu-id="2e5d7-116">Job</span></span><br/>     |
| <span data-ttu-id="2e5d7-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="2e5d7-117">Notes</span></span> <br/>          | <span data-ttu-id="2e5d7-118">Нет</span><span class="sxs-lookup"><span data-stu-id="2e5d7-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="2e5d7-119">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="2e5d7-119">Structural Content</span></span>

<span data-ttu-id="2e5d7-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="2e5d7-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="2e5d7-121">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="2e5d7-121">Structure Variables</span></span>

<span data-ttu-id="2e5d7-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="2e5d7-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2e5d7-123">Имя</span><span class="sxs-lookup"><span data-stu-id="2e5d7-123">Name</span></span>                               | <span data-ttu-id="2e5d7-124">Тип данных</span><span class="sxs-lookup"><span data-stu-id="2e5d7-124">Data type</span></span>         | <span data-ttu-id="2e5d7-125">Unit</span><span class="sxs-lookup"><span data-stu-id="2e5d7-125">Unit</span></span>                   | <span data-ttu-id="2e5d7-126">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="2e5d7-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="2e5d7-127">Сводка</span><span class="sxs-lookup"><span data-stu-id="2e5d7-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="2e5d7-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="2e5d7-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="2e5d7-129">строка</span><span class="sxs-lookup"><span data-stu-id="2e5d7-129">string</span></span><br/> | <span data-ttu-id="2e5d7-130">characters</span><span class="sxs-lookup"><span data-stu-id="2e5d7-130">characters</span></span> <br/> | <span data-ttu-id="2e5d7-131">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="2e5d7-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="2e5d7-132">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2e5d7-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="2e5d7-133">Имя параметра</span><span class="sxs-lookup"><span data-stu-id="2e5d7-133">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="2e5d7-134">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="2e5d7-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="2e5d7-135">строка</span><span class="sxs-lookup"><span data-stu-id="2e5d7-135">string</span></span><br/> | <span data-ttu-id="2e5d7-136">Недоступно</span><span class="sxs-lookup"><span data-stu-id="2e5d7-136">n/a</span></span><br/>         | <span data-ttu-id="2e5d7-137">True, False</span><span class="sxs-lookup"><span data-stu-id="2e5d7-137">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="2e5d7-138">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="2e5d7-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="2e5d7-139">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="2e5d7-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="2e5d7-140">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="2e5d7-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="2e5d7-141">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="2e5d7-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="2e5d7-142">См. также</span><span class="sxs-lookup"><span data-stu-id="2e5d7-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e5d7-143">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="2e5d7-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




