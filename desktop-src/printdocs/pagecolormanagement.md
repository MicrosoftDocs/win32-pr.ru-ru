---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 27408582-9c39-4d39-8314-a495d1c7766d
title: пажеколорманажемент
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81a037b6b32ff71b53688dfd6fc8afd5f10bb69
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997661"
---
# <a name="pagecolormanagement"></a><span data-ttu-id="f1c2c-104">пажеколорманажемент</span><span class="sxs-lookup"><span data-stu-id="f1c2c-104">PageColorManagement</span></span>

<span data-ttu-id="f1c2c-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="f1c2c-105">This topic is not current.</span></span> <span data-ttu-id="f1c2c-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f1c2c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f1c2c-107">Настраивает управление цветом для текущей страницы.</span><span class="sxs-lookup"><span data-stu-id="f1c2c-107">Configures color management for the current page.</span></span> <span data-ttu-id="f1c2c-108">Это считается автоматическим в оболочке совместимости — DM \_ Икммесод Add System.</span><span class="sxs-lookup"><span data-stu-id="f1c2c-108">This is considered automatic in SHIM - DM\_ICMMethod Add System.</span></span> <span data-ttu-id="f1c2c-109">Описывает, какой компонент должен выполнять управление цветом (т. е. драйвер).</span><span class="sxs-lookup"><span data-stu-id="f1c2c-109">Describes what component should perform color management (i.e. Driver).</span></span>

-   [<span data-ttu-id="f1c2c-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f1c2c-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f1c2c-111">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="f1c2c-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="f1c2c-112">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="f1c2c-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="f1c2c-113">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f1c2c-113">Element Information</span></span>



| <span data-ttu-id="f1c2c-114">Имя</span><span class="sxs-lookup"><span data-stu-id="f1c2c-114">Name</span></span> | <span data-ttu-id="f1c2c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f1c2c-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="f1c2c-116">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="f1c2c-116">Element Type</span></span> <br/>   | <span data-ttu-id="f1c2c-117">Компонент</span><span class="sxs-lookup"><span data-stu-id="f1c2c-117">Feature</span></span><br/> |
| <span data-ttu-id="f1c2c-118">Префикс области</span><span class="sxs-lookup"><span data-stu-id="f1c2c-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f1c2c-119">Страница</span><span class="sxs-lookup"><span data-stu-id="f1c2c-119">Page</span></span><br/>    |
| <span data-ttu-id="f1c2c-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="f1c2c-120">Notes</span></span> <br/>          | <span data-ttu-id="f1c2c-121">Нет</span><span class="sxs-lookup"><span data-stu-id="f1c2c-121">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="f1c2c-122">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="f1c2c-122">Structural Content</span></span>

<span data-ttu-id="f1c2c-123">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="f1c2c-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageColorManagement">
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

## <a name="structure-variables"></a><span data-ttu-id="f1c2c-124">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="f1c2c-124">Structure Variables</span></span>

<span data-ttu-id="f1c2c-125">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="f1c2c-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f1c2c-126">Имя</span><span class="sxs-lookup"><span data-stu-id="f1c2c-126">Name</span></span>                               | <span data-ttu-id="f1c2c-127">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f1c2c-127">Data type</span></span>         | <span data-ttu-id="f1c2c-128">Unit</span><span class="sxs-lookup"><span data-stu-id="f1c2c-128">Unit</span></span>                  | <span data-ttu-id="f1c2c-129">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="f1c2c-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="f1c2c-130">Сводка</span><span class="sxs-lookup"><span data-stu-id="f1c2c-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f1c2c-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="f1c2c-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="f1c2c-132">строка</span><span class="sxs-lookup"><span data-stu-id="f1c2c-132">string</span></span><br/> | <span data-ttu-id="f1c2c-133">characters</span><span class="sxs-lookup"><span data-stu-id="f1c2c-133">characters</span></span><br/> | <span data-ttu-id="f1c2c-134">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="f1c2c-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="f1c2c-135">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f1c2c-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="f1c2c-136">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="f1c2c-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="f1c2c-137">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="f1c2c-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="f1c2c-138">строка</span><span class="sxs-lookup"><span data-stu-id="f1c2c-138">string</span></span><br/> | <span data-ttu-id="f1c2c-139">Недоступно</span><span class="sxs-lookup"><span data-stu-id="f1c2c-139">n/a</span></span><br/>        | <span data-ttu-id="f1c2c-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="f1c2c-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="f1c2c-141">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="f1c2c-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="f1c2c-142">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="f1c2c-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="f1c2c-143">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="f1c2c-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="f1c2c-144">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="f1c2c-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageColorManagement">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- Application has performed color management to the destination profile. -->
  <psf:Option name="psk:None" />
  <!--  Application has not performed color management and the device determines color management.-->
  <psf:Option name="psk:Device" />
  <!--  Application has not performed color management and the driver determines color management.-->
  <psf:Option name="psk:Driver" />
  <!--Color management is performed by the system. Not to be used when printing to XPSDrv print drivers -->
  <psf:Option name="psk:System" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="f1c2c-145">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="f1c2c-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1c2c-146">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="f1c2c-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




