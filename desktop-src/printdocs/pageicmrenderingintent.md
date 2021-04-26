---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: df11ee89-fe62-4fe5-a1d6-0f925360ca39
title: пажеикмрендерингинтент
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d17eea84ba45ea7c121080f7649b03492c6f3409
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995562"
---
# <a name="pageicmrenderingintent"></a><span data-ttu-id="5600c-104">пажеикмрендерингинтент</span><span class="sxs-lookup"><span data-stu-id="5600c-104">PageICMRenderingIntent</span></span>

<span data-ttu-id="5600c-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="5600c-105">This topic is not current.</span></span> <span data-ttu-id="5600c-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5600c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5600c-107">Описывает цель подготовки к просмотру, определенную спецификацией ICC v2.</span><span class="sxs-lookup"><span data-stu-id="5600c-107">Describes the rendering intent as defined by the ICC v2 Specification.</span></span> <span data-ttu-id="5600c-108">Это значение следует игнорировать, если изображение или графический элемент имеет встроенный профиль, указывающий цель отрисовки.</span><span class="sxs-lookup"><span data-stu-id="5600c-108">This value should be ignored if an image or graphical element has an embedded profile that specifies the Rendering intent.</span></span>

-   [<span data-ttu-id="5600c-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="5600c-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5600c-110">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="5600c-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="5600c-111">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="5600c-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="5600c-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="5600c-112">Element Information</span></span>



| <span data-ttu-id="5600c-113">Имя</span><span class="sxs-lookup"><span data-stu-id="5600c-113">Name</span></span> | <span data-ttu-id="5600c-114">Значение</span><span class="sxs-lookup"><span data-stu-id="5600c-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="5600c-115">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="5600c-115">Element Type</span></span> <br/>   | <span data-ttu-id="5600c-116">Компонент</span><span class="sxs-lookup"><span data-stu-id="5600c-116">Feature</span></span><br/> |
| <span data-ttu-id="5600c-117">Префикс области</span><span class="sxs-lookup"><span data-stu-id="5600c-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5600c-118">Страница</span><span class="sxs-lookup"><span data-stu-id="5600c-118">Page</span></span><br/>    |
| <span data-ttu-id="5600c-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="5600c-119">Notes</span></span> <br/>          | <span data-ttu-id="5600c-120">Нет</span><span class="sxs-lookup"><span data-stu-id="5600c-120">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="5600c-121">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="5600c-121">Structural Content</span></span>

<span data-ttu-id="5600c-122">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="5600c-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageICMRenderingIntent">
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

## <a name="structure-variables"></a><span data-ttu-id="5600c-123">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="5600c-123">Structure Variables</span></span>

<span data-ttu-id="5600c-124">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="5600c-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5600c-125">Имя</span><span class="sxs-lookup"><span data-stu-id="5600c-125">Name</span></span>                               | <span data-ttu-id="5600c-126">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5600c-126">Data type</span></span>         | <span data-ttu-id="5600c-127">Unit</span><span class="sxs-lookup"><span data-stu-id="5600c-127">Unit</span></span>                  | <span data-ttu-id="5600c-128">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="5600c-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="5600c-129">Сводка</span><span class="sxs-lookup"><span data-stu-id="5600c-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="5600c-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="5600c-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="5600c-131">строка</span><span class="sxs-lookup"><span data-stu-id="5600c-131">string</span></span><br/> | <span data-ttu-id="5600c-132">characters</span><span class="sxs-lookup"><span data-stu-id="5600c-132">characters</span></span><br/> | <span data-ttu-id="5600c-133">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="5600c-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="5600c-134">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5600c-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="5600c-135">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="5600c-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="5600c-136">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="5600c-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="5600c-137">строка</span><span class="sxs-lookup"><span data-stu-id="5600c-137">string</span></span><br/> | <span data-ttu-id="5600c-138">Недоступно</span><span class="sxs-lookup"><span data-stu-id="5600c-138">n/a</span></span><br/>        | <span data-ttu-id="5600c-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="5600c-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="5600c-140">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="5600c-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="5600c-141">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="5600c-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="5600c-142">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="5600c-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="5600c-143">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="5600c-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageICMRenderingIntent">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!--Absolute Colorimetric Rendering intent-->
  <psf:Option name="psk:AbsoluteColorimetric" />
  <!--Relative Colorimetric Rendering intent -->
  <psf:Option name="psk:RelativeColorimetric" />
  <!--Photographs Rendering intent -->
  <psf:Option name="psk:Photographs" />
  <!--Business Graphics Rendering intent -->
  <psf:Option name="psk:BusinessGraphics" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="5600c-144">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="5600c-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5600c-145">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="5600c-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




