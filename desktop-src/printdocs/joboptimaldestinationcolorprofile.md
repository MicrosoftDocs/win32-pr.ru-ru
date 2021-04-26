---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 70790dc2-180a-4e04-91a9-a10ee76c836b
title: жобоптималдестинатионколорпрофиле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45630b2ddbe94f19905f01c508fc4d852d29566b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999257"
---
# <a name="joboptimaldestinationcolorprofile"></a><span data-ttu-id="629f2-104">жобоптималдестинатионколорпрофиле</span><span class="sxs-lookup"><span data-stu-id="629f2-104">JobOptimalDestinationColorProfile</span></span>

<span data-ttu-id="629f2-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="629f2-105">This topic is not current.</span></span> <span data-ttu-id="629f2-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="629f2-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="629f2-107">Задает оптимальный цветовой профиль, заданный текущей конфигурацией устройства.</span><span class="sxs-lookup"><span data-stu-id="629f2-107">Specifies the optimal color profile given the current device configuration.</span></span>

-   [<span data-ttu-id="629f2-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="629f2-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="629f2-109">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="629f2-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="629f2-110">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="629f2-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="629f2-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="629f2-111">Element Information</span></span>



| <span data-ttu-id="629f2-112">Имя</span><span class="sxs-lookup"><span data-stu-id="629f2-112">Name</span></span> | <span data-ttu-id="629f2-113">Значение</span><span class="sxs-lookup"><span data-stu-id="629f2-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="629f2-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="629f2-114">Element Type</span></span> <br/>   | <span data-ttu-id="629f2-115">Свойство</span><span class="sxs-lookup"><span data-stu-id="629f2-115">Property</span></span><br/> |
| <span data-ttu-id="629f2-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="629f2-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="629f2-117">Задание</span><span class="sxs-lookup"><span data-stu-id="629f2-117">Job</span></span><br/>      |
| <span data-ttu-id="629f2-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="629f2-118">Notes</span></span> <br/>          | <span data-ttu-id="629f2-119">Нет</span><span class="sxs-lookup"><span data-stu-id="629f2-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="629f2-120">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="629f2-120">Structural Content</span></span>

<span data-ttu-id="629f2-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="629f2-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:JobOptimalDestinationColorProfile">
  <psf:Property name="psk:Profile">
    <psf:Value xsi:type="xs:string">_ProfileValue_</psf:Value>
    <psf:Property name="psk:ProfileData">
      <psf:Value xsi:type="xs:string">_ProfileDataValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:Path">
      <psf:Value xsi:type="xs:string">_PathValue_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="629f2-122">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="629f2-122">Structure Variables</span></span>

<span data-ttu-id="629f2-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="629f2-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="629f2-124">Имя</span><span class="sxs-lookup"><span data-stu-id="629f2-124">Name</span></span>                            | <span data-ttu-id="629f2-125">Тип данных</span><span class="sxs-lookup"><span data-stu-id="629f2-125">Data type</span></span>         | <span data-ttu-id="629f2-126">Unit</span><span class="sxs-lookup"><span data-stu-id="629f2-126">Unit</span></span>           | <span data-ttu-id="629f2-127">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="629f2-127">Supported values</span></span>          | <span data-ttu-id="629f2-128">Сводка</span><span class="sxs-lookup"><span data-stu-id="629f2-128">Summary</span></span>                                        |
|---------------------------------|-------------------|----------------|---------------------------|------------------------------------------------|
| <span data-ttu-id="629f2-129">\_профилевалуе\_</span><span class="sxs-lookup"><span data-stu-id="629f2-129">\_ProfileValue\_</span></span><br/>     | <span data-ttu-id="629f2-130">строка</span><span class="sxs-lookup"><span data-stu-id="629f2-130">string</span></span><br/> | <span data-ttu-id="629f2-131">Недоступно</span><span class="sxs-lookup"><span data-stu-id="629f2-131">n/a</span></span><br/> | <span data-ttu-id="629f2-132">RGB, ICC, CMYK</span><span class="sxs-lookup"><span data-stu-id="629f2-132">RGB, ICC, CMYK</span></span><br/> | <span data-ttu-id="629f2-133">Задает цветовой профиль.</span><span class="sxs-lookup"><span data-stu-id="629f2-133">Specifies the color profile.</span></span><br/>        |
| <span data-ttu-id="629f2-134">\_пасвалуе\_</span><span class="sxs-lookup"><span data-stu-id="629f2-134">\_PathValue\_</span></span><br/>        | <span data-ttu-id="629f2-135">строка</span><span class="sxs-lookup"><span data-stu-id="629f2-135">string</span></span><br/> | <span data-ttu-id="629f2-136">Недоступно</span><span class="sxs-lookup"><span data-stu-id="629f2-136">n/a</span></span><br/> | <span data-ttu-id="629f2-137">Недоступно</span><span class="sxs-lookup"><span data-stu-id="629f2-137">n/a</span></span><br/>            | <span data-ttu-id="629f2-138">Указывает путь к профилю файла.</span><span class="sxs-lookup"><span data-stu-id="629f2-138">Specifies file path to the profile.</span></span><br/> |
| <span data-ttu-id="629f2-139">\_профиледатавалуе\_</span><span class="sxs-lookup"><span data-stu-id="629f2-139">\_ProfileDataValue\_</span></span><br/> | <span data-ttu-id="629f2-140">строка</span><span class="sxs-lookup"><span data-stu-id="629f2-140">string</span></span><br/> | <span data-ttu-id="629f2-141">Недоступно</span><span class="sxs-lookup"><span data-stu-id="629f2-141">n/a</span></span><br/> | <span data-ttu-id="629f2-142">Недоступно</span><span class="sxs-lookup"><span data-stu-id="629f2-142">n/a</span></span><br/>            | <span data-ttu-id="629f2-143">Содержит содержимое данных профиля.</span><span class="sxs-lookup"><span data-stu-id="629f2-143">Contains profile data content.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="629f2-144">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="629f2-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="629f2-145">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="629f2-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="629f2-146">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="629f2-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
 <psf:Property name="psk:JobOptimalDestinationColorProfile">
  <psf:Property name="psk:Profile">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    <psf:Property name="psk:ProfileData">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:Path">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="629f2-147">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="629f2-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="629f2-148">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="629f2-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




