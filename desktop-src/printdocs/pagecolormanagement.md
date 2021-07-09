---
description: Сведения об элементе Пажеколорманажемент, настраиваемом пользователем. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 27408582-9c39-4d39-8314-a495d1c7766d
title: пажеколорманажемент
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685794f1c9bb64c8bb3e966c4ec03bcac8821369
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549232"
---
# <a name="pagecolormanagement"></a><span data-ttu-id="98de9-105">пажеколорманажемент</span><span class="sxs-lookup"><span data-stu-id="98de9-105">PageColorManagement</span></span>

<span data-ttu-id="98de9-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="98de9-106">This topic is not current.</span></span> <span data-ttu-id="98de9-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="98de9-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="98de9-108">Настраивает управление цветом для текущей страницы.</span><span class="sxs-lookup"><span data-stu-id="98de9-108">Configures color management for the current page.</span></span> <span data-ttu-id="98de9-109">Это считается автоматическим в оболочке совместимости — DM \_ Икммесод Add System.</span><span class="sxs-lookup"><span data-stu-id="98de9-109">This is considered automatic in SHIM - DM\_ICMMethod Add System.</span></span> <span data-ttu-id="98de9-110">Описывает, какой компонент должен выполнять управление цветом (т. е. драйвер).</span><span class="sxs-lookup"><span data-stu-id="98de9-110">Describes what component should perform color management (i.e. Driver).</span></span>

-   [<span data-ttu-id="98de9-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="98de9-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="98de9-112">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="98de9-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="98de9-113">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="98de9-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="98de9-114">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="98de9-114">Element Information</span></span>



| <span data-ttu-id="98de9-115">Имя</span><span class="sxs-lookup"><span data-stu-id="98de9-115">Name</span></span> | <span data-ttu-id="98de9-116">Значение</span><span class="sxs-lookup"><span data-stu-id="98de9-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="98de9-117">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="98de9-117">Element Type</span></span> <br/>   | <span data-ttu-id="98de9-118">Компонент</span><span class="sxs-lookup"><span data-stu-id="98de9-118">Feature</span></span><br/> |
| <span data-ttu-id="98de9-119">Префикс области</span><span class="sxs-lookup"><span data-stu-id="98de9-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="98de9-120">Страница</span><span class="sxs-lookup"><span data-stu-id="98de9-120">Page</span></span><br/>    |
| <span data-ttu-id="98de9-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="98de9-121">Notes</span></span> <br/>          | <span data-ttu-id="98de9-122">Нет</span><span class="sxs-lookup"><span data-stu-id="98de9-122">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="98de9-123">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="98de9-123">Structural Content</span></span>

<span data-ttu-id="98de9-124">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="98de9-124">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="98de9-125">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="98de9-125">Structure Variables</span></span>

<span data-ttu-id="98de9-126">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="98de9-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="98de9-127">Имя</span><span class="sxs-lookup"><span data-stu-id="98de9-127">Name</span></span>                               | <span data-ttu-id="98de9-128">Тип данных</span><span class="sxs-lookup"><span data-stu-id="98de9-128">Data type</span></span>         | <span data-ttu-id="98de9-129">Unit</span><span class="sxs-lookup"><span data-stu-id="98de9-129">Unit</span></span>                  | <span data-ttu-id="98de9-130">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="98de9-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="98de9-131">Итоги</span><span class="sxs-lookup"><span data-stu-id="98de9-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="98de9-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="98de9-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="98de9-133">строка</span><span class="sxs-lookup"><span data-stu-id="98de9-133">string</span></span><br/> | <span data-ttu-id="98de9-134">characters</span><span class="sxs-lookup"><span data-stu-id="98de9-134">characters</span></span><br/> | <span data-ttu-id="98de9-135">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="98de9-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="98de9-136">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="98de9-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="98de9-137">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="98de9-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="98de9-138">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="98de9-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="98de9-139">строка</span><span class="sxs-lookup"><span data-stu-id="98de9-139">string</span></span><br/> | <span data-ttu-id="98de9-140">Н/Д</span><span class="sxs-lookup"><span data-stu-id="98de9-140">n/a</span></span><br/>        | <span data-ttu-id="98de9-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="98de9-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="98de9-142">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="98de9-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="98de9-143">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="98de9-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="98de9-144">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="98de9-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="98de9-145">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="98de9-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="98de9-146">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="98de9-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98de9-147">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="98de9-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




