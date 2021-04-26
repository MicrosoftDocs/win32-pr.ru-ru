---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 52f02fc1-56fb-404d-8939-df3a4b21570d
title: пажеориентатион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a94fb97ad1e64c7f55fd9520ed8a648a74f550
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997541"
---
# <a name="pageorientation"></a><span data-ttu-id="71f6a-104">пажеориентатион</span><span class="sxs-lookup"><span data-stu-id="71f6a-104">PageOrientation</span></span>

<span data-ttu-id="71f6a-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="71f6a-105">This topic is not current.</span></span> <span data-ttu-id="71f6a-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="71f6a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="71f6a-107">Описывает ориентацию листа физического носителя.</span><span class="sxs-lookup"><span data-stu-id="71f6a-107">Describes the orientation of the physical media sheet.</span></span>



| <span data-ttu-id="71f6a-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="71f6a-108">Option</span></span>                       | <span data-ttu-id="71f6a-109">Определение</span><span class="sxs-lookup"><span data-stu-id="71f6a-109">Definition</span></span>                                                                                              |
|------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71f6a-110">Альбомная</span><span class="sxs-lookup"><span data-stu-id="71f6a-110">Landscape</span></span> <br/>        | <span data-ttu-id="71f6a-111">Содержимое поворачивается на странице 90?? градусы CCW относительно стандартной (книжной) ориентации.</span><span class="sxs-lookup"><span data-stu-id="71f6a-111">Content is rotated on the page 90??degrees CCW relative to standard (portrait) orientation.</span></span><br/>  |
| <span data-ttu-id="71f6a-112">Книжная</span><span class="sxs-lookup"><span data-stu-id="71f6a-112">Portrait</span></span> <br/>         | <span data-ttu-id="71f6a-113">Стандартная ориентация.</span><span class="sxs-lookup"><span data-stu-id="71f6a-113">Standard Orientation.</span></span><br/>                                                                        |
| <span data-ttu-id="71f6a-114">реверселандскапе</span><span class="sxs-lookup"><span data-stu-id="71f6a-114">ReverseLandscape</span></span> <br/> | <span data-ttu-id="71f6a-115">Содержимое поворачивается на странице 270?? градусы CCW относительно стандартной (книжной) ориентации.</span><span class="sxs-lookup"><span data-stu-id="71f6a-115">Content is rotated on the page 270??degrees CCW relative to standard (portrait) orientation.</span></span><br/> |
| <span data-ttu-id="71f6a-116">реверсепортраит</span><span class="sxs-lookup"><span data-stu-id="71f6a-116">ReversePortrait</span></span> <br/>  | <span data-ttu-id="71f6a-117">Содержимое поворачивается на странице 180?? градусы относительно стандартной (книжной) ориентации.</span><span class="sxs-lookup"><span data-stu-id="71f6a-117">Content is rotated on the page 180??degrees relative to standard (portrait) orientation.</span></span><br/>     |



 

-   [<span data-ttu-id="71f6a-118">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="71f6a-118">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="71f6a-119">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="71f6a-119">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="71f6a-120">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="71f6a-120">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="71f6a-121">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="71f6a-121">Element Information</span></span>



| <span data-ttu-id="71f6a-122">Имя</span><span class="sxs-lookup"><span data-stu-id="71f6a-122">Name</span></span> | <span data-ttu-id="71f6a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="71f6a-123">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71f6a-124">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="71f6a-124">Element Type</span></span> <br/>   | <span data-ttu-id="71f6a-125">Компонент</span><span class="sxs-lookup"><span data-stu-id="71f6a-125">Feature</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="71f6a-126">Префикс области</span><span class="sxs-lookup"><span data-stu-id="71f6a-126">Scoping Prefix</span></span> <br/> | <span data-ttu-id="71f6a-127">Страница</span><span class="sxs-lookup"><span data-stu-id="71f6a-127">Page</span></span><br/>                                                                                                                                                                                         |
| <span data-ttu-id="71f6a-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="71f6a-128">Notes</span></span> <br/>          | <span data-ttu-id="71f6a-129">Если устройство принтера поддерживает только одно альбомное направление, а это направление называется "Обратная альбомная", то ориентация страницы по-прежнему будет считаться "альбомной".</span><span class="sxs-lookup"><span data-stu-id="71f6a-129">If a Printer Device can only support one landscape direction and this direction is referred to as "Reverse Landscape", then the page orientation will still be considered to be "Landscape".</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="71f6a-130">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="71f6a-130">Structural Content</span></span>

<span data-ttu-id="71f6a-131">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="71f6a-131">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageOrientation">
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

## <a name="structure-variables"></a><span data-ttu-id="71f6a-132">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="71f6a-132">Structure Variables</span></span>

<span data-ttu-id="71f6a-133">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="71f6a-133">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="71f6a-134">Имя</span><span class="sxs-lookup"><span data-stu-id="71f6a-134">Name</span></span>                               | <span data-ttu-id="71f6a-135">Тип данных</span><span class="sxs-lookup"><span data-stu-id="71f6a-135">Data type</span></span>         | <span data-ttu-id="71f6a-136">Unit</span><span class="sxs-lookup"><span data-stu-id="71f6a-136">Unit</span></span>                  | <span data-ttu-id="71f6a-137">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="71f6a-137">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="71f6a-138">Сводка</span><span class="sxs-lookup"><span data-stu-id="71f6a-138">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="71f6a-139">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="71f6a-139">\_OptionName\_</span></span><br/>          | <span data-ttu-id="71f6a-140">строка</span><span class="sxs-lookup"><span data-stu-id="71f6a-140">string</span></span><br/> | <span data-ttu-id="71f6a-141">characters</span><span class="sxs-lookup"><span data-stu-id="71f6a-141">characters</span></span><br/> | <span data-ttu-id="71f6a-142">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="71f6a-142">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="71f6a-143">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="71f6a-143">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="71f6a-144">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="71f6a-144">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="71f6a-145">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="71f6a-145">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="71f6a-146">строка</span><span class="sxs-lookup"><span data-stu-id="71f6a-146">string</span></span><br/> | <span data-ttu-id="71f6a-147">Недоступно</span><span class="sxs-lookup"><span data-stu-id="71f6a-147">n/a</span></span><br/>        | <span data-ttu-id="71f6a-148">True, False.</span><span class="sxs-lookup"><span data-stu-id="71f6a-148">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="71f6a-149">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="71f6a-149">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="71f6a-150">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="71f6a-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="71f6a-151">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="71f6a-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="71f6a-152">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="71f6a-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageOrientation">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Content is rotated on the page 90??degrees CCW relative to standard (portrait) orientation.??-->
  <psf:Option name="psk:Landscape" />
  <!-- Standard Orientation-->
  <psf:Option name="psk:Portrait" />
  <!-- Content is rotated on the page 270??degrees CCW relative to standard (portrait) orientation??-->
  <psf:Option name="psk:ReverseLandscape" />
  <!-- Content is rotated on the page 180??degrees relative to standard (portrait) orientation??-->
  <psf:Option name="psk:ReversePortrait" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="71f6a-153">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="71f6a-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71f6a-154">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="71f6a-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




