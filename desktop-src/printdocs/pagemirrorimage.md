---
description: Сведения об элементе Пажемирроримаже, настраиваемом пользователем. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: a05357c0-6a82-42ff-b4f8-d3e0ee089055
title: пажемирроримаже
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fe917d6973fbd074111a5da7b6fe5620e7251e9
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549104"
---
# <a name="pagemirrorimage"></a><span data-ttu-id="d65e7-105">пажемирроримаже</span><span class="sxs-lookup"><span data-stu-id="d65e7-105">PageMirrorImage</span></span>

<span data-ttu-id="d65e7-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="d65e7-106">This topic is not current.</span></span> <span data-ttu-id="d65e7-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d65e7-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d65e7-108">Описывает параметр зеркального отображения выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d65e7-108">Describes the mirroring setting of the output.</span></span>

-   [<span data-ttu-id="d65e7-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="d65e7-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d65e7-110">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="d65e7-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="d65e7-111">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="d65e7-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="d65e7-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="d65e7-112">Element Information</span></span>



| <span data-ttu-id="d65e7-113">Имя</span><span class="sxs-lookup"><span data-stu-id="d65e7-113">Name</span></span> | <span data-ttu-id="d65e7-114">Значение</span><span class="sxs-lookup"><span data-stu-id="d65e7-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="d65e7-115">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="d65e7-115">Element Type</span></span> <br/>   | <span data-ttu-id="d65e7-116">Компонент</span><span class="sxs-lookup"><span data-stu-id="d65e7-116">Feature</span></span><br/> |
| <span data-ttu-id="d65e7-117">Префикс области</span><span class="sxs-lookup"><span data-stu-id="d65e7-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d65e7-118">Страница</span><span class="sxs-lookup"><span data-stu-id="d65e7-118">Page</span></span><br/>    |
| <span data-ttu-id="d65e7-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="d65e7-119">Notes</span></span> <br/>          | <span data-ttu-id="d65e7-120">Нет</span><span class="sxs-lookup"><span data-stu-id="d65e7-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="d65e7-121">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="d65e7-121">Structural Content</span></span>

<span data-ttu-id="d65e7-122">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="d65e7-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageMirrorImage">
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

## <a name="structure-variables"></a><span data-ttu-id="d65e7-123">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="d65e7-123">Structure Variables</span></span>

<span data-ttu-id="d65e7-124">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="d65e7-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d65e7-125">Имя</span><span class="sxs-lookup"><span data-stu-id="d65e7-125">Name</span></span>                               | <span data-ttu-id="d65e7-126">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d65e7-126">Data type</span></span>         | <span data-ttu-id="d65e7-127">Unit</span><span class="sxs-lookup"><span data-stu-id="d65e7-127">Unit</span></span>                  | <span data-ttu-id="d65e7-128">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="d65e7-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="d65e7-129">Итоги</span><span class="sxs-lookup"><span data-stu-id="d65e7-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="d65e7-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="d65e7-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="d65e7-131">строка</span><span class="sxs-lookup"><span data-stu-id="d65e7-131">string</span></span><br/> | <span data-ttu-id="d65e7-132">characters</span><span class="sxs-lookup"><span data-stu-id="d65e7-132">characters</span></span><br/> | <span data-ttu-id="d65e7-133">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="d65e7-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="d65e7-134">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d65e7-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="d65e7-135">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="d65e7-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="d65e7-136">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="d65e7-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="d65e7-137">строка</span><span class="sxs-lookup"><span data-stu-id="d65e7-137">string</span></span><br/> | <span data-ttu-id="d65e7-138">Н/Д</span><span class="sxs-lookup"><span data-stu-id="d65e7-138">n/a</span></span><br/>        | <span data-ttu-id="d65e7-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="d65e7-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="d65e7-140">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="d65e7-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="d65e7-141">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="d65e7-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="d65e7-142">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="d65e7-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="d65e7-143">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="d65e7-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageMirrorImage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the output should be mirrored parallel to the MediaSizeWidth direction. -->
  <psf:Option name="psk:MirrorImageWidth" />
  <!-- Specifies the output should be mirrored parallel to the MediaSizeHeight direction. -->
  <psf:Option name="psk:MirrorImageHeight" />
  <!-- Specifies the output should not be mirrored. -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="d65e7-144">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="d65e7-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d65e7-145">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="d65e7-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




