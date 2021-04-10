---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 70790dc2-180a-4e04-91a9-a10ee76c836b
title: жобоптималдестинатионколорпрофиле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 954f67df5720e19de39d2c1c752c6d9eb860a502
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "104000025"
---
# <a name="joboptimaldestinationcolorprofile"></a><span data-ttu-id="ed2ea-104">жобоптималдестинатионколорпрофиле</span><span class="sxs-lookup"><span data-stu-id="ed2ea-104">JobOptimalDestinationColorProfile</span></span>

<span data-ttu-id="ed2ea-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="ed2ea-105">This topic is not current.</span></span> <span data-ttu-id="ed2ea-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ed2ea-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ed2ea-107">Задает оптимальный цветовой профиль, заданный текущей конфигурацией устройства.</span><span class="sxs-lookup"><span data-stu-id="ed2ea-107">Specifies the optimal color profile given the current device configuration.</span></span>

-   [<span data-ttu-id="ed2ea-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ed2ea-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ed2ea-109">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="ed2ea-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="ed2ea-110">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="ed2ea-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ed2ea-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ed2ea-111">Element Information</span></span>



| <span data-ttu-id="ed2ea-112">Имя</span><span class="sxs-lookup"><span data-stu-id="ed2ea-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="ed2ea-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="ed2ea-113">Element Type</span></span> <br/>   | <span data-ttu-id="ed2ea-114">Свойство</span><span class="sxs-lookup"><span data-stu-id="ed2ea-114">Property</span></span><br/> |
| <span data-ttu-id="ed2ea-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="ed2ea-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ed2ea-116">Задание</span><span class="sxs-lookup"><span data-stu-id="ed2ea-116">Job</span></span><br/>      |
| <span data-ttu-id="ed2ea-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="ed2ea-117">Notes</span></span> <br/>          | <span data-ttu-id="ed2ea-118">Нет</span><span class="sxs-lookup"><span data-stu-id="ed2ea-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="ed2ea-119">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="ed2ea-119">Structural Content</span></span>

<span data-ttu-id="ed2ea-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="ed2ea-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="ed2ea-121">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="ed2ea-121">Structure Variables</span></span>

<span data-ttu-id="ed2ea-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="ed2ea-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ed2ea-123">Имя</span><span class="sxs-lookup"><span data-stu-id="ed2ea-123">Name</span></span>                            | <span data-ttu-id="ed2ea-124">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ed2ea-124">Data type</span></span>         | <span data-ttu-id="ed2ea-125">Unit</span><span class="sxs-lookup"><span data-stu-id="ed2ea-125">Unit</span></span>           | <span data-ttu-id="ed2ea-126">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="ed2ea-126">Supported values</span></span>          | <span data-ttu-id="ed2ea-127">Сводка</span><span class="sxs-lookup"><span data-stu-id="ed2ea-127">Summary</span></span>                                        |
|---------------------------------|-------------------|----------------|---------------------------|------------------------------------------------|
| <span data-ttu-id="ed2ea-128">\_профилевалуе\_</span><span class="sxs-lookup"><span data-stu-id="ed2ea-128">\_ProfileValue\_</span></span><br/>     | <span data-ttu-id="ed2ea-129">строка</span><span class="sxs-lookup"><span data-stu-id="ed2ea-129">string</span></span><br/> | <span data-ttu-id="ed2ea-130">Недоступно</span><span class="sxs-lookup"><span data-stu-id="ed2ea-130">n/a</span></span><br/> | <span data-ttu-id="ed2ea-131">RGB, ICC, CMYK</span><span class="sxs-lookup"><span data-stu-id="ed2ea-131">RGB, ICC, CMYK</span></span><br/> | <span data-ttu-id="ed2ea-132">Задает цветовой профиль.</span><span class="sxs-lookup"><span data-stu-id="ed2ea-132">Specifies the color profile.</span></span><br/>        |
| <span data-ttu-id="ed2ea-133">\_пасвалуе\_</span><span class="sxs-lookup"><span data-stu-id="ed2ea-133">\_PathValue\_</span></span><br/>        | <span data-ttu-id="ed2ea-134">строка</span><span class="sxs-lookup"><span data-stu-id="ed2ea-134">string</span></span><br/> | <span data-ttu-id="ed2ea-135">Недоступно</span><span class="sxs-lookup"><span data-stu-id="ed2ea-135">n/a</span></span><br/> | <span data-ttu-id="ed2ea-136">Недоступно</span><span class="sxs-lookup"><span data-stu-id="ed2ea-136">n/a</span></span><br/>            | <span data-ttu-id="ed2ea-137">Указывает путь к профилю файла.</span><span class="sxs-lookup"><span data-stu-id="ed2ea-137">Specifies file path to the profile.</span></span><br/> |
| <span data-ttu-id="ed2ea-138">\_профиледатавалуе\_</span><span class="sxs-lookup"><span data-stu-id="ed2ea-138">\_ProfileDataValue\_</span></span><br/> | <span data-ttu-id="ed2ea-139">строка</span><span class="sxs-lookup"><span data-stu-id="ed2ea-139">string</span></span><br/> | <span data-ttu-id="ed2ea-140">Недоступно</span><span class="sxs-lookup"><span data-stu-id="ed2ea-140">n/a</span></span><br/> | <span data-ttu-id="ed2ea-141">Недоступно</span><span class="sxs-lookup"><span data-stu-id="ed2ea-141">n/a</span></span><br/>            | <span data-ttu-id="ed2ea-142">Содержит содержимое данных профиля.</span><span class="sxs-lookup"><span data-stu-id="ed2ea-142">Contains profile data content.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ed2ea-143">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="ed2ea-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="ed2ea-144">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="ed2ea-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="ed2ea-145">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="ed2ea-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="ed2ea-146">См. также</span><span class="sxs-lookup"><span data-stu-id="ed2ea-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed2ea-147">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="ed2ea-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




