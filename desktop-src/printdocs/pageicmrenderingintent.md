---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: df11ee89-fe62-4fe5-a1d6-0f925360ca39
title: пажеикмрендерингинтент
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 014213bdd2e11cc2587cef580a0b48fe03172ef0
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "104273355"
---
# <a name="pageicmrenderingintent"></a><span data-ttu-id="20e33-104">пажеикмрендерингинтент</span><span class="sxs-lookup"><span data-stu-id="20e33-104">PageICMRenderingIntent</span></span>

<span data-ttu-id="20e33-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="20e33-105">This topic is not current.</span></span> <span data-ttu-id="20e33-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="20e33-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="20e33-107">Описывает цель подготовки к просмотру, определенную спецификацией ICC v2.</span><span class="sxs-lookup"><span data-stu-id="20e33-107">Describes the rendering intent as defined by the ICC v2 Specification.</span></span> <span data-ttu-id="20e33-108">Это значение следует игнорировать, если изображение или графический элемент имеет встроенный профиль, указывающий цель отрисовки.</span><span class="sxs-lookup"><span data-stu-id="20e33-108">This value should be ignored if an image or graphical element has an embedded profile that specifies the Rendering intent.</span></span>

-   [<span data-ttu-id="20e33-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="20e33-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="20e33-110">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="20e33-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="20e33-111">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="20e33-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="20e33-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="20e33-112">Element Information</span></span>



| <span data-ttu-id="20e33-113">Имя</span><span class="sxs-lookup"><span data-stu-id="20e33-113">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="20e33-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="20e33-114">Element Type</span></span> <br/>   | <span data-ttu-id="20e33-115">Функция</span><span class="sxs-lookup"><span data-stu-id="20e33-115">Feature</span></span><br/> |
| <span data-ttu-id="20e33-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="20e33-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="20e33-117">Страница</span><span class="sxs-lookup"><span data-stu-id="20e33-117">Page</span></span><br/>    |
| <span data-ttu-id="20e33-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="20e33-118">Notes</span></span> <br/>          | <span data-ttu-id="20e33-119">Нет</span><span class="sxs-lookup"><span data-stu-id="20e33-119">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="20e33-120">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="20e33-120">Structural Content</span></span>

<span data-ttu-id="20e33-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="20e33-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="20e33-122">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="20e33-122">Structure Variables</span></span>

<span data-ttu-id="20e33-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="20e33-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="20e33-124">Имя</span><span class="sxs-lookup"><span data-stu-id="20e33-124">Name</span></span>                               | <span data-ttu-id="20e33-125">Тип данных</span><span class="sxs-lookup"><span data-stu-id="20e33-125">Data type</span></span>         | <span data-ttu-id="20e33-126">Unit</span><span class="sxs-lookup"><span data-stu-id="20e33-126">Unit</span></span>                  | <span data-ttu-id="20e33-127">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="20e33-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="20e33-128">Сводка</span><span class="sxs-lookup"><span data-stu-id="20e33-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="20e33-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="20e33-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="20e33-130">строка</span><span class="sxs-lookup"><span data-stu-id="20e33-130">string</span></span><br/> | <span data-ttu-id="20e33-131">characters</span><span class="sxs-lookup"><span data-stu-id="20e33-131">characters</span></span><br/> | <span data-ttu-id="20e33-132">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="20e33-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="20e33-133">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="20e33-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="20e33-134">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="20e33-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="20e33-135">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="20e33-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="20e33-136">строка</span><span class="sxs-lookup"><span data-stu-id="20e33-136">string</span></span><br/> | <span data-ttu-id="20e33-137">Недоступно</span><span class="sxs-lookup"><span data-stu-id="20e33-137">n/a</span></span><br/>        | <span data-ttu-id="20e33-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="20e33-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="20e33-139">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="20e33-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="20e33-140">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="20e33-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="20e33-141">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="20e33-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="20e33-142">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="20e33-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="20e33-143">См. также</span><span class="sxs-lookup"><span data-stu-id="20e33-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20e33-144">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="20e33-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




