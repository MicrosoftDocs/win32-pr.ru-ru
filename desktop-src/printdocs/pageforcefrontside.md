---
description: Сведения об элементе Пажефорцефронтсиде, настраиваемом пользователем. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 0658c808-f050-41f3-90b6-2a013b616b58
title: пажефорцефронтсиде
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79f22e9ec52b7cee72e8f3a479d161e9abb765c4
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549192"
---
# <a name="pageforcefrontside"></a><span data-ttu-id="991ed-105">пажефорцефронтсиде</span><span class="sxs-lookup"><span data-stu-id="991ed-105">PageForceFrontSide</span></span>

<span data-ttu-id="991ed-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="991ed-106">This topic is not current.</span></span> <span data-ttu-id="991ed-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="991ed-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="991ed-108">Принудительное Отображение выходных данных на лицевой странице листа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="991ed-108">Forces the output to appear on the front of a media sheet.</span></span> <span data-ttu-id="991ed-109">Относится к листам мультимедиа с разными областями на каждой стороне.</span><span class="sxs-lookup"><span data-stu-id="991ed-109">Relevant to media sheets with different surfaces on each side.</span></span> <span data-ttu-id="991ed-110">В случаях, когда эта функция мешает работе с параметрами обработки (например, Документдуплекс), Пажефорцефронтсиде имеет приоритет для конкретной страницы, к которой применяется эта функция.</span><span class="sxs-lookup"><span data-stu-id="991ed-110">In cases where this feature interferes with processing options (such as DocumentDuplex), PageForceFrontSide takes precedence for the specific page to which the feature applies.</span></span>

-   [<span data-ttu-id="991ed-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="991ed-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="991ed-112">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="991ed-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="991ed-113">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="991ed-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="991ed-114">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="991ed-114">Element Information</span></span>



| <span data-ttu-id="991ed-115">Имя</span><span class="sxs-lookup"><span data-stu-id="991ed-115">Name</span></span> | <span data-ttu-id="991ed-116">Значение</span><span class="sxs-lookup"><span data-stu-id="991ed-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="991ed-117">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="991ed-117">Element Type</span></span> <br/>   | <span data-ttu-id="991ed-118">Компонент</span><span class="sxs-lookup"><span data-stu-id="991ed-118">Feature</span></span><br/> |
| <span data-ttu-id="991ed-119">Префикс области</span><span class="sxs-lookup"><span data-stu-id="991ed-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="991ed-120">Страница</span><span class="sxs-lookup"><span data-stu-id="991ed-120">Page</span></span><br/>    |
| <span data-ttu-id="991ed-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="991ed-121">Notes</span></span> <br/>          | <span data-ttu-id="991ed-122">Нет</span><span class="sxs-lookup"><span data-stu-id="991ed-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="991ed-123">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="991ed-123">Structural Content</span></span>

<span data-ttu-id="991ed-124">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="991ed-124">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="991ed-125">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="991ed-125">Structure Variables</span></span>

<span data-ttu-id="991ed-126">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="991ed-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="991ed-127">Имя</span><span class="sxs-lookup"><span data-stu-id="991ed-127">Name</span></span>                               | <span data-ttu-id="991ed-128">Тип данных</span><span class="sxs-lookup"><span data-stu-id="991ed-128">Data type</span></span>         | <span data-ttu-id="991ed-129">Unit</span><span class="sxs-lookup"><span data-stu-id="991ed-129">Unit</span></span>                  | <span data-ttu-id="991ed-130">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="991ed-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="991ed-131">Итоги</span><span class="sxs-lookup"><span data-stu-id="991ed-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="991ed-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="991ed-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="991ed-133">строка</span><span class="sxs-lookup"><span data-stu-id="991ed-133">string</span></span><br/> | <span data-ttu-id="991ed-134">characters</span><span class="sxs-lookup"><span data-stu-id="991ed-134">characters</span></span><br/> | <span data-ttu-id="991ed-135">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="991ed-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="991ed-136">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="991ed-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="991ed-137">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="991ed-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="991ed-138">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="991ed-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="991ed-139">строка</span><span class="sxs-lookup"><span data-stu-id="991ed-139">string</span></span><br/> | <span data-ttu-id="991ed-140">Н/Д</span><span class="sxs-lookup"><span data-stu-id="991ed-140">n/a</span></span><br/>        | <span data-ttu-id="991ed-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="991ed-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="991ed-142">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="991ed-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="991ed-143">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="991ed-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="991ed-144">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="991ed-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="991ed-145">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="991ed-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="991ed-146">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="991ed-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="991ed-147">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="991ed-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




