---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 3e0e2cb2-cb51-446d-a6ff-f76aa8c305f6
title: пажемедиаколор
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60c9a314bf435664d121fd35e588b62903da323e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994511"
---
# <a name="pagemediacolor"></a><span data-ttu-id="ce411-104">пажемедиаколор</span><span class="sxs-lookup"><span data-stu-id="ce411-104">PageMediaColor</span></span>

<span data-ttu-id="ce411-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="ce411-105">This topic is not current.</span></span> <span data-ttu-id="ce411-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ce411-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ce411-107">Описывает параметры цвета носителя и характеристики каждого параметра.</span><span class="sxs-lookup"><span data-stu-id="ce411-107">Describes the Media Color options and the characteristics of each option.</span></span>

-   [<span data-ttu-id="ce411-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ce411-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ce411-109">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="ce411-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="ce411-110">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="ce411-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ce411-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ce411-111">Element Information</span></span>



| <span data-ttu-id="ce411-112">Имя</span><span class="sxs-lookup"><span data-stu-id="ce411-112">Name</span></span> | <span data-ttu-id="ce411-113">Значение</span><span class="sxs-lookup"><span data-stu-id="ce411-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="ce411-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="ce411-114">Element Type</span></span> <br/>   | <span data-ttu-id="ce411-115">Компонент</span><span class="sxs-lookup"><span data-stu-id="ce411-115">Feature</span></span><br/> |
| <span data-ttu-id="ce411-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="ce411-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ce411-117">Страница</span><span class="sxs-lookup"><span data-stu-id="ce411-117">Page</span></span><br/>    |
| <span data-ttu-id="ce411-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="ce411-118">Notes</span></span> <br/>          | <span data-ttu-id="ce411-119">Нет</span><span class="sxs-lookup"><span data-stu-id="ce411-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="ce411-120">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="ce411-120">Structural Content</span></span>

<span data-ttu-id="ce411-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="ce411-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageMediaColor">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">_MediaColorsRGBValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="ce411-122">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="ce411-122">Structure Variables</span></span>

<span data-ttu-id="ce411-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="ce411-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ce411-124">Имя</span><span class="sxs-lookup"><span data-stu-id="ce411-124">Name</span></span>                               | <span data-ttu-id="ce411-125">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ce411-125">Data type</span></span>         | <span data-ttu-id="ce411-126">Unit</span><span class="sxs-lookup"><span data-stu-id="ce411-126">Unit</span></span>                  | <span data-ttu-id="ce411-127">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="ce411-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="ce411-128">Сводка</span><span class="sxs-lookup"><span data-stu-id="ce411-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ce411-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="ce411-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="ce411-130">строка</span><span class="sxs-lookup"><span data-stu-id="ce411-130">string</span></span><br/> | <span data-ttu-id="ce411-131">characters</span><span class="sxs-lookup"><span data-stu-id="ce411-131">characters</span></span><br/> | <span data-ttu-id="ce411-132">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="ce411-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ce411-133">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ce411-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ce411-134">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="ce411-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="ce411-135">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="ce411-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="ce411-136">строка</span><span class="sxs-lookup"><span data-stu-id="ce411-136">string</span></span><br/> | <span data-ttu-id="ce411-137">Недоступно</span><span class="sxs-lookup"><span data-stu-id="ce411-137">n/a</span></span><br/>        | <span data-ttu-id="ce411-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="ce411-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="ce411-139">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="ce411-139">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="ce411-140">\_медиаколорсргбвалуе\_</span><span class="sxs-lookup"><span data-stu-id="ce411-140">\_MediaColorsRGBValue\_</span></span><br/> | <span data-ttu-id="ce411-141">строка</span><span class="sxs-lookup"><span data-stu-id="ce411-141">string</span></span><br/> | <span data-ttu-id="ce411-142">Цвет sRGB</span><span class="sxs-lookup"><span data-stu-id="ce411-142">sRGB Color</span></span><br/> | <span data-ttu-id="ce411-143">\#AARRGGBB, где A, R, G, B представляют шестнадцатеричные цифры.</span><span class="sxs-lookup"><span data-stu-id="ce411-143">\#AARRGGBB where A, R, G, B represent hexadecimal digits.</span></span><br/>                                                                                                                  | <span data-ttu-id="ce411-144">Определяет цвет sRGB для листа физического носителя.</span><span class="sxs-lookup"><span data-stu-id="ce411-144">Defines the sRGB color for the physical media sheet.</span></span> <br/>             |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ce411-145">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="ce411-145">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="ce411-146">Ключевые слова общедоступной схемы печати определены в `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="ce411-146">The public Print Schema keywords are defined in the `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` namespace.</span></span> <span data-ttu-id="ce411-147">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="ce411-147">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageMediaColor">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:Black">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF000000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Blue">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF0000FF</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Brown">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFA52A2A</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Gold">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFD700</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:GoldenRod">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFDAA520</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Gray">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF808080</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Green">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF008000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Ivory">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFFFF0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NoColor">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Orange">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFA500</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Pink">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFC0CB</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Red">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFF0000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Silver">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFC0C0C0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Turquoise">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF40E0D0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Violet">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFEE82EE</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:White">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFFFFF</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Yellow">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFFF00</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a custom page color. -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="ce411-148">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="ce411-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce411-149">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="ce411-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>
