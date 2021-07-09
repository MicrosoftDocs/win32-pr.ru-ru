---
description: Ознакомьтесь с элементом Пажеикмрендерингинтент, настраиваемым пользователем. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: df11ee89-fe62-4fe5-a1d6-0f925360ca39
title: пажеикмрендерингинтент
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab595bac5a7136510335167c37bc36d8a7e44056
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549182"
---
# <a name="pageicmrenderingintent"></a><span data-ttu-id="6165a-105">пажеикмрендерингинтент</span><span class="sxs-lookup"><span data-stu-id="6165a-105">PageICMRenderingIntent</span></span>

<span data-ttu-id="6165a-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="6165a-106">This topic is not current.</span></span> <span data-ttu-id="6165a-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6165a-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6165a-108">Описывает цель подготовки к просмотру, определенную спецификацией ICC v2.</span><span class="sxs-lookup"><span data-stu-id="6165a-108">Describes the rendering intent as defined by the ICC v2 Specification.</span></span> <span data-ttu-id="6165a-109">Это значение следует игнорировать, если изображение или графический элемент имеет встроенный профиль, указывающий цель отрисовки.</span><span class="sxs-lookup"><span data-stu-id="6165a-109">This value should be ignored if an image or graphical element has an embedded profile that specifies the Rendering intent.</span></span>

-   [<span data-ttu-id="6165a-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="6165a-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6165a-111">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="6165a-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="6165a-112">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="6165a-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="6165a-113">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="6165a-113">Element Information</span></span>



| <span data-ttu-id="6165a-114">Имя</span><span class="sxs-lookup"><span data-stu-id="6165a-114">Name</span></span> | <span data-ttu-id="6165a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6165a-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="6165a-116">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="6165a-116">Element Type</span></span> <br/>   | <span data-ttu-id="6165a-117">Компонент</span><span class="sxs-lookup"><span data-stu-id="6165a-117">Feature</span></span><br/> |
| <span data-ttu-id="6165a-118">Префикс области</span><span class="sxs-lookup"><span data-stu-id="6165a-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6165a-119">Страница</span><span class="sxs-lookup"><span data-stu-id="6165a-119">Page</span></span><br/>    |
| <span data-ttu-id="6165a-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="6165a-120">Notes</span></span> <br/>          | <span data-ttu-id="6165a-121">Нет</span><span class="sxs-lookup"><span data-stu-id="6165a-121">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="6165a-122">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="6165a-122">Structural Content</span></span>

<span data-ttu-id="6165a-123">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="6165a-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="6165a-124">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="6165a-124">Structure Variables</span></span>

<span data-ttu-id="6165a-125">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="6165a-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6165a-126">Имя</span><span class="sxs-lookup"><span data-stu-id="6165a-126">Name</span></span>                               | <span data-ttu-id="6165a-127">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6165a-127">Data type</span></span>         | <span data-ttu-id="6165a-128">Unit</span><span class="sxs-lookup"><span data-stu-id="6165a-128">Unit</span></span>                  | <span data-ttu-id="6165a-129">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="6165a-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="6165a-130">Итоги</span><span class="sxs-lookup"><span data-stu-id="6165a-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="6165a-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="6165a-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="6165a-132">строка</span><span class="sxs-lookup"><span data-stu-id="6165a-132">string</span></span><br/> | <span data-ttu-id="6165a-133">characters</span><span class="sxs-lookup"><span data-stu-id="6165a-133">characters</span></span><br/> | <span data-ttu-id="6165a-134">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="6165a-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="6165a-135">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6165a-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="6165a-136">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="6165a-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="6165a-137">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="6165a-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="6165a-138">строка</span><span class="sxs-lookup"><span data-stu-id="6165a-138">string</span></span><br/> | <span data-ttu-id="6165a-139">Н/Д</span><span class="sxs-lookup"><span data-stu-id="6165a-139">n/a</span></span><br/>        | <span data-ttu-id="6165a-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="6165a-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="6165a-141">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="6165a-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="6165a-142">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="6165a-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="6165a-143">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="6165a-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="6165a-144">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="6165a-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="6165a-145">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="6165a-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6165a-146">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="6165a-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




