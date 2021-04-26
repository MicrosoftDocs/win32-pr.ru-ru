---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 0658c808-f050-41f3-90b6-2a013b616b58
title: пажефорцефронтсиде
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e363050034137bcfb3ff2b779ecda05200865312
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996941"
---
# <a name="pageforcefrontside"></a><span data-ttu-id="db442-104">пажефорцефронтсиде</span><span class="sxs-lookup"><span data-stu-id="db442-104">PageForceFrontSide</span></span>

<span data-ttu-id="db442-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="db442-105">This topic is not current.</span></span> <span data-ttu-id="db442-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="db442-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="db442-107">Принудительное Отображение выходных данных на лицевой странице листа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="db442-107">Forces the output to appear on the front of a media sheet.</span></span> <span data-ttu-id="db442-108">Относится к листам мультимедиа с разными областями на каждой стороне.</span><span class="sxs-lookup"><span data-stu-id="db442-108">Relevant to media sheets with different surfaces on each side.</span></span> <span data-ttu-id="db442-109">В случаях, когда эта функция мешает работе с параметрами обработки (например, Документдуплекс), Пажефорцефронтсиде имеет приоритет для конкретной страницы, к которой применяется эта функция.</span><span class="sxs-lookup"><span data-stu-id="db442-109">In cases where this feature interferes with processing options (such as DocumentDuplex), PageForceFrontSide takes precedence for the specific page to which the feature applies.</span></span>

-   [<span data-ttu-id="db442-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="db442-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="db442-111">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="db442-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="db442-112">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="db442-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="db442-113">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="db442-113">Element Information</span></span>



| <span data-ttu-id="db442-114">Имя</span><span class="sxs-lookup"><span data-stu-id="db442-114">Name</span></span> | <span data-ttu-id="db442-115">Значение</span><span class="sxs-lookup"><span data-stu-id="db442-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="db442-116">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="db442-116">Element Type</span></span> <br/>   | <span data-ttu-id="db442-117">Компонент</span><span class="sxs-lookup"><span data-stu-id="db442-117">Feature</span></span><br/> |
| <span data-ttu-id="db442-118">Префикс области</span><span class="sxs-lookup"><span data-stu-id="db442-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="db442-119">Страница</span><span class="sxs-lookup"><span data-stu-id="db442-119">Page</span></span><br/>    |
| <span data-ttu-id="db442-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="db442-120">Notes</span></span> <br/>          | <span data-ttu-id="db442-121">Нет</span><span class="sxs-lookup"><span data-stu-id="db442-121">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="db442-122">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="db442-122">Structural Content</span></span>

<span data-ttu-id="db442-123">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="db442-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageForceFrontSide">
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

## <a name="structure-variables"></a><span data-ttu-id="db442-124">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="db442-124">Structure Variables</span></span>

<span data-ttu-id="db442-125">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="db442-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="db442-126">Имя</span><span class="sxs-lookup"><span data-stu-id="db442-126">Name</span></span>                               | <span data-ttu-id="db442-127">Тип данных</span><span class="sxs-lookup"><span data-stu-id="db442-127">Data type</span></span>         | <span data-ttu-id="db442-128">Unit</span><span class="sxs-lookup"><span data-stu-id="db442-128">Unit</span></span>                  | <span data-ttu-id="db442-129">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="db442-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="db442-130">Сводка</span><span class="sxs-lookup"><span data-stu-id="db442-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="db442-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="db442-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="db442-132">строка</span><span class="sxs-lookup"><span data-stu-id="db442-132">string</span></span><br/> | <span data-ttu-id="db442-133">characters</span><span class="sxs-lookup"><span data-stu-id="db442-133">characters</span></span><br/> | <span data-ttu-id="db442-134">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="db442-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="db442-135">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="db442-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="db442-136">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="db442-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="db442-137">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="db442-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="db442-138">строка</span><span class="sxs-lookup"><span data-stu-id="db442-138">string</span></span><br/> | <span data-ttu-id="db442-139">Недоступно</span><span class="sxs-lookup"><span data-stu-id="db442-139">n/a</span></span><br/>        | <span data-ttu-id="db442-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="db442-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="db442-141">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="db442-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="db442-142">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="db442-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="db442-143">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="db442-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="db442-144">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="db442-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageForceFrontSide">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies output is restricted to the front side of the sheet. -->
  <psf:Option name="psk:ForceFrontSide" />
  <!-- Specifies no output restrictions.  -->
  <psf:Option name="psk:None" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="db442-145">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="db442-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db442-146">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="db442-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




