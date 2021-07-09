---
description: Проверьте элемент Пажедестинатионколорпрофиле, настраиваемый пользователем. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 1a6ff76a-0818-464a-bf75-534dc7ea383f
title: пажедестинатионколорпрофиле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 026c12e8b6e322f024c3603abc97b0e4e0413d5b
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549222"
---
# <a name="pagedestinationcolorprofile"></a><span data-ttu-id="2da87-105">пажедестинатионколорпрофиле</span><span class="sxs-lookup"><span data-stu-id="2da87-105">PageDestinationColorProfile</span></span>

<span data-ttu-id="2da87-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="2da87-106">This topic is not current.</span></span> <span data-ttu-id="2da87-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2da87-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2da87-108">Определяет характеристики цветового профиля назначения.</span><span class="sxs-lookup"><span data-stu-id="2da87-108">Defines the characteristics of the destination color profile.</span></span> <span data-ttu-id="2da87-109">Описывает, будет ли приложение или драйвер выбирать используемый цветовой профиль назначения.</span><span class="sxs-lookup"><span data-stu-id="2da87-109">Describes whether the application or driver selects the destination color profile to be used.</span></span>

-   [<span data-ttu-id="2da87-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="2da87-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2da87-111">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="2da87-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="2da87-112">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="2da87-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="2da87-113">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="2da87-113">Element Information</span></span>



| <span data-ttu-id="2da87-114">Имя</span><span class="sxs-lookup"><span data-stu-id="2da87-114">Name</span></span> | <span data-ttu-id="2da87-115">Значение</span><span class="sxs-lookup"><span data-stu-id="2da87-115">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2da87-116">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="2da87-116">Element Type</span></span> <br/>   | <span data-ttu-id="2da87-117">Компонент</span><span class="sxs-lookup"><span data-stu-id="2da87-117">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="2da87-118">Префикс области</span><span class="sxs-lookup"><span data-stu-id="2da87-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2da87-119">Страница</span><span class="sxs-lookup"><span data-stu-id="2da87-119">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="2da87-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="2da87-120">Notes</span></span> <br/>          | <span data-ttu-id="2da87-121">Потребители, совместимые с XPS, должны обеспечить, чтобы ссылка URI для ресурса, такого как изображение или цветовой профиль в документе возможностей печати или PrintTicket, ссылалась на имя части (относительный URI для корня пакета) в том же пакете документа XPS, который содержит итоговый PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="2da87-121">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="2da87-122">Совместимый потребитель XPS не должен использовать URI, который не соответствует синтаксису имени части.</span><span class="sxs-lookup"><span data-stu-id="2da87-122">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="2da87-123">Эти параметры относятся к формату XPS.</span><span class="sxs-lookup"><span data-stu-id="2da87-123">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="2da87-124">URI, на которые есть ссылки в документе возможностей печати или PrintTicket, не должны разрешаться как URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="2da87-124">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="2da87-125">Это небезопасно, так как они могут не распознаться должным образом и могут создавать опасные риски безопасности для драйвера и операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2da87-125">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="2da87-126">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="2da87-126">Structural Content</span></span>

<span data-ttu-id="2da87-127">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="2da87-127">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageDestinationColorProfile">
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

## <a name="structure-variables"></a><span data-ttu-id="2da87-128">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="2da87-128">Structure Variables</span></span>

<span data-ttu-id="2da87-129">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="2da87-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2da87-130">Имя</span><span class="sxs-lookup"><span data-stu-id="2da87-130">Name</span></span>                               | <span data-ttu-id="2da87-131">Тип данных</span><span class="sxs-lookup"><span data-stu-id="2da87-131">Data type</span></span>         | <span data-ttu-id="2da87-132">Unit</span><span class="sxs-lookup"><span data-stu-id="2da87-132">Unit</span></span>                  | <span data-ttu-id="2da87-133">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="2da87-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="2da87-134">Итоги</span><span class="sxs-lookup"><span data-stu-id="2da87-134">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="2da87-135">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="2da87-135">\_OptionName\_</span></span><br/>          | <span data-ttu-id="2da87-136">строка</span><span class="sxs-lookup"><span data-stu-id="2da87-136">string</span></span><br/> | <span data-ttu-id="2da87-137">characters</span><span class="sxs-lookup"><span data-stu-id="2da87-137">characters</span></span><br/> | <span data-ttu-id="2da87-138">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="2da87-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="2da87-139">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2da87-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="2da87-140">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="2da87-140">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="2da87-141">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="2da87-141">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="2da87-142">строка</span><span class="sxs-lookup"><span data-stu-id="2da87-142">string</span></span><br/> | <span data-ttu-id="2da87-143">Н/Д</span><span class="sxs-lookup"><span data-stu-id="2da87-143">n/a</span></span><br/>        | <span data-ttu-id="2da87-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="2da87-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="2da87-145">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="2da87-145">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="2da87-146">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="2da87-146">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="2da87-147">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="2da87-147">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="2da87-148">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="2da87-148">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageDestinationColorProfile">
  <!-- Application specifies the destination profile to be used. -->
  <psf:Option name="psk:Application">
    <!-- Destination profile used to perform color management. -->
    <psf:ScoredProperty name="psk:DestinationColorProfileURI">
      <psf:ParameterRef name="psk:PageDestinationColorProfileURI" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:DestinationColorProfileEmbedded">
      <psf:ParameterRef name="psk:PageDestinationColorProfileEmbedded" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Driver selects the destination profile that best matches its current configuration. -->
  <psf:Option name="psk:DriverConfiguration" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="2da87-149">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="2da87-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2da87-150">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="2da87-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




