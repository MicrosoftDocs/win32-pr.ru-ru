---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 3894d9fa-2bf7-447a-bac3-e72a0fdb7187
title: жобдевицелангуаже
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66b9f85b44ae9fdc6efb66ce5b72bb68c5187790
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998301"
---
# <a name="jobdevicelanguage"></a><span data-ttu-id="ce5ad-104">жобдевицелангуаже</span><span class="sxs-lookup"><span data-stu-id="ce5ad-104">JobDeviceLanguage</span></span>

<span data-ttu-id="ce5ad-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="ce5ad-105">This topic is not current.</span></span> <span data-ttu-id="ce5ad-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ce5ad-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ce5ad-107">Описывает языки устройств, поддерживаемые для отправки данных с драйвера на физическое устройство.</span><span class="sxs-lookup"><span data-stu-id="ce5ad-107">Describes the device languages supported for sending data from driver to physical device.</span></span> <span data-ttu-id="ce5ad-108">Часто это называется «языком описания страниц».</span><span class="sxs-lookup"><span data-stu-id="ce5ad-108">This is often called "Page Description Language".</span></span> <span data-ttu-id="ce5ad-109">Это ключевое слово определяет, какой язык описания страниц поддерживается драйвером и физическим устройством.</span><span class="sxs-lookup"><span data-stu-id="ce5ad-109">This keyword defines what page description language is supported by the driver and physical device.</span></span>

-   [<span data-ttu-id="ce5ad-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ce5ad-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ce5ad-111">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="ce5ad-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="ce5ad-112">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="ce5ad-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ce5ad-113">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ce5ad-113">Element Information</span></span>



| <span data-ttu-id="ce5ad-114">Имя</span><span class="sxs-lookup"><span data-stu-id="ce5ad-114">Name</span></span> | <span data-ttu-id="ce5ad-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ce5ad-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="ce5ad-116">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="ce5ad-116">Element Type</span></span> <br/>   | <span data-ttu-id="ce5ad-117">Компонент</span><span class="sxs-lookup"><span data-stu-id="ce5ad-117">Feature</span></span><br/> |
| <span data-ttu-id="ce5ad-118">Префикс области</span><span class="sxs-lookup"><span data-stu-id="ce5ad-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ce5ad-119">Задание</span><span class="sxs-lookup"><span data-stu-id="ce5ad-119">Job</span></span><br/>     |
| <span data-ttu-id="ce5ad-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="ce5ad-120">Notes</span></span> <br/>          | <span data-ttu-id="ce5ad-121">Нет</span><span class="sxs-lookup"><span data-stu-id="ce5ad-121">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="ce5ad-122">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="ce5ad-122">Structural Content</span></span>

<span data-ttu-id="ce5ad-123">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="ce5ad-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobDeviceLanguage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_value_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_LanguageEncodingValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_LanguageVersionValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="ce5ad-124">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="ce5ad-124">Structure Variables</span></span>

<span data-ttu-id="ce5ad-125">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="ce5ad-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ce5ad-126">Имя</span><span class="sxs-lookup"><span data-stu-id="ce5ad-126">Name</span></span>                                 | <span data-ttu-id="ce5ad-127">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ce5ad-127">Data type</span></span>         | <span data-ttu-id="ce5ad-128">Unit</span><span class="sxs-lookup"><span data-stu-id="ce5ad-128">Unit</span></span>                  | <span data-ttu-id="ce5ad-129">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="ce5ad-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="ce5ad-130">Сводка</span><span class="sxs-lookup"><span data-stu-id="ce5ad-130">Summary</span></span>                                                                      |
|--------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ce5ad-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="ce5ad-131">\_OptionName\_</span></span><br/>            | <span data-ttu-id="ce5ad-132">строка</span><span class="sxs-lookup"><span data-stu-id="ce5ad-132">string</span></span><br/> | <span data-ttu-id="ce5ad-133">characters</span><span class="sxs-lookup"><span data-stu-id="ce5ad-133">characters</span></span><br/> | <span data-ttu-id="ce5ad-134">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="ce5ad-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ce5ad-135">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ce5ad-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ce5ad-136">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="ce5ad-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="ce5ad-137">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="ce5ad-137">\_IdentityOptionValue\_</span></span><br/>   | <span data-ttu-id="ce5ad-138">строка</span><span class="sxs-lookup"><span data-stu-id="ce5ad-138">string</span></span><br/> | <span data-ttu-id="ce5ad-139">Недоступно</span><span class="sxs-lookup"><span data-stu-id="ce5ad-139">n/a</span></span><br/>        | <span data-ttu-id="ce5ad-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="ce5ad-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="ce5ad-141">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="ce5ad-141">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="ce5ad-142">\_лангуажелевелвалуе\_</span><span class="sxs-lookup"><span data-stu-id="ce5ad-142">\_LanguageLevelValue\_</span></span><br/>    | <span data-ttu-id="ce5ad-143">строка</span><span class="sxs-lookup"><span data-stu-id="ce5ad-143">string</span></span><br/> | <span data-ttu-id="ce5ad-144">Недоступно</span><span class="sxs-lookup"><span data-stu-id="ce5ad-144">n/a</span></span><br/>        | <span data-ttu-id="ce5ad-145">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="ce5ad-145">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="ce5ad-146">Задает языковой уровень (например, уровень PS 2).</span><span class="sxs-lookup"><span data-stu-id="ce5ad-146">Specifies the language level (for example, PS Level 2).</span></span><br/>           |
| <span data-ttu-id="ce5ad-147">\_лангуажеенкодингвалуе\_</span><span class="sxs-lookup"><span data-stu-id="ce5ad-147">\_LanguageEncodingValue\_</span></span><br/> | <span data-ttu-id="ce5ad-148">строка</span><span class="sxs-lookup"><span data-stu-id="ce5ad-148">string</span></span><br/> | <span data-ttu-id="ce5ad-149">Недоступно</span><span class="sxs-lookup"><span data-stu-id="ce5ad-149">n/a</span></span><br/>        | <span data-ttu-id="ce5ad-150">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="ce5ad-150">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="ce5ad-151">Задает кодировку языка (например, ISOLatin1).</span><span class="sxs-lookup"><span data-stu-id="ce5ad-151">Specifies the language encoding (for example, ISOLatin1).</span></span><br/>         |
| <span data-ttu-id="ce5ad-152">\_лангуажеверсионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="ce5ad-152">\_LanguageVersionValue\_</span></span><br/>  | <span data-ttu-id="ce5ad-153">строка</span><span class="sxs-lookup"><span data-stu-id="ce5ad-153">string</span></span><br/> | <span data-ttu-id="ce5ad-154">Недоступно</span><span class="sxs-lookup"><span data-stu-id="ce5ad-154">n/a</span></span><br/>        | <span data-ttu-id="ce5ad-155">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="ce5ad-155">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="ce5ad-156">Указывает версию языка.</span><span class="sxs-lookup"><span data-stu-id="ce5ad-156">Specifies the language version.</span></span><br/>                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ce5ad-157">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="ce5ad-157">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="ce5ad-158">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="ce5ad-158">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="ce5ad-159">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="ce5ad-159">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobDeviceLanguage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!--Specifies device language is XPS-->
  <psf:Option name="psk:XPS">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specifies device language is PC-PR201 -->
  <psf:Option name="psk:_201PL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ART -->
  <psf:Option name="psk:ART">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ASCII -->
  <psf:Option name="psk:ASCII">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is CaPSL-->
  <psf:Option name="psk:CaPSL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ESC/P2-->
  <psf:Option name="psk:ESCP2">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ESC/Page-->
  <psf:Option name="psk:ESCPage">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is HP-GL/2-->
  <psf:Option name="psk:HPGL2">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is KPDL -->
  <psf:Option name="psk:KPDL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is KS -->
  <psf:Option name="psk:KS">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is KSSM -->
  <psf:Option name="psk:KSSM">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL -->
  <psf:Option name="psk:PCL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL5c -->
  <psf:Option name="psk:PCL5c">
    <psf:ScoredProperty name="LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL5e -->
  <psf:Option name="psk:PCL5e">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL-XL -->
  <psf:Option name="psk:PCL-XL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PostScript -->
  <psf:Option name="psk:PostScript">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PPDS -->
  <psf:Option name="psk:PPDS">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is RPDL -->
  <psf:Option name="psk:RPDL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is RTL -->
  <psf:Option name="psk:RTL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="ce5ad-160">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="ce5ad-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce5ad-161">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="ce5ad-161">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




