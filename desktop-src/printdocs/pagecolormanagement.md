---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 27408582-9c39-4d39-8314-a495d1c7766d
title: пажеколорманажемент
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ae8d161035d23149759345e8eb139dd3fb7a48
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "105703546"
---
# <a name="pagecolormanagement"></a><span data-ttu-id="3dee4-104">пажеколорманажемент</span><span class="sxs-lookup"><span data-stu-id="3dee4-104">PageColorManagement</span></span>

<span data-ttu-id="3dee4-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="3dee4-105">This topic is not current.</span></span> <span data-ttu-id="3dee4-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3dee4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3dee4-107">Настраивает управление цветом для текущей страницы.</span><span class="sxs-lookup"><span data-stu-id="3dee4-107">Configures color management for the current page.</span></span> <span data-ttu-id="3dee4-108">Это считается автоматическим в оболочке совместимости — DM \_ Икммесод Add System.</span><span class="sxs-lookup"><span data-stu-id="3dee4-108">This is considered automatic in SHIM - DM\_ICMMethod Add System.</span></span> <span data-ttu-id="3dee4-109">Описывает, какой компонент должен выполнять управление цветом (т. е. драйвер).</span><span class="sxs-lookup"><span data-stu-id="3dee4-109">Describes what component should perform color management (i.e. Driver).</span></span>

-   [<span data-ttu-id="3dee4-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="3dee4-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3dee4-111">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="3dee4-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="3dee4-112">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="3dee4-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="3dee4-113">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="3dee4-113">Element Information</span></span>



| <span data-ttu-id="3dee4-114">Имя</span><span class="sxs-lookup"><span data-stu-id="3dee4-114">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="3dee4-115">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="3dee4-115">Element Type</span></span> <br/>   | <span data-ttu-id="3dee4-116">Функция</span><span class="sxs-lookup"><span data-stu-id="3dee4-116">Feature</span></span><br/> |
| <span data-ttu-id="3dee4-117">Префикс области</span><span class="sxs-lookup"><span data-stu-id="3dee4-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3dee4-118">Страница</span><span class="sxs-lookup"><span data-stu-id="3dee4-118">Page</span></span><br/>    |
| <span data-ttu-id="3dee4-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="3dee4-119">Notes</span></span> <br/>          | <span data-ttu-id="3dee4-120">Нет</span><span class="sxs-lookup"><span data-stu-id="3dee4-120">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="3dee4-121">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="3dee4-121">Structural Content</span></span>

<span data-ttu-id="3dee4-122">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="3dee4-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="3dee4-123">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="3dee4-123">Structure Variables</span></span>

<span data-ttu-id="3dee4-124">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="3dee4-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3dee4-125">Имя</span><span class="sxs-lookup"><span data-stu-id="3dee4-125">Name</span></span>                               | <span data-ttu-id="3dee4-126">Тип данных</span><span class="sxs-lookup"><span data-stu-id="3dee4-126">Data type</span></span>         | <span data-ttu-id="3dee4-127">Unit</span><span class="sxs-lookup"><span data-stu-id="3dee4-127">Unit</span></span>                  | <span data-ttu-id="3dee4-128">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="3dee4-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="3dee4-129">Сводка</span><span class="sxs-lookup"><span data-stu-id="3dee4-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="3dee4-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="3dee4-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="3dee4-131">строка</span><span class="sxs-lookup"><span data-stu-id="3dee4-131">string</span></span><br/> | <span data-ttu-id="3dee4-132">characters</span><span class="sxs-lookup"><span data-stu-id="3dee4-132">characters</span></span><br/> | <span data-ttu-id="3dee4-133">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="3dee4-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="3dee4-134">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3dee4-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="3dee4-135">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="3dee4-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="3dee4-136">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="3dee4-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="3dee4-137">строка</span><span class="sxs-lookup"><span data-stu-id="3dee4-137">string</span></span><br/> | <span data-ttu-id="3dee4-138">Недоступно</span><span class="sxs-lookup"><span data-stu-id="3dee4-138">n/a</span></span><br/>        | <span data-ttu-id="3dee4-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="3dee4-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="3dee4-140">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="3dee4-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="3dee4-141">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="3dee4-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="3dee4-142">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="3dee4-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="3dee4-143">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="3dee4-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="3dee4-144">См. также</span><span class="sxs-lookup"><span data-stu-id="3dee4-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3dee4-145">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="3dee4-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




