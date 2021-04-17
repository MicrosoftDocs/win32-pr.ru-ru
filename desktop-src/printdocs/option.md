---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: feda78d9-58e7-4668-8a25-40e5fd8ad456
title: Параметр
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 379834d12cd01847c95783d727be5dcdc6c575bf
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105713335"
---
# <a name="option"></a><span data-ttu-id="32bc0-104">Параметр</span><span class="sxs-lookup"><span data-stu-id="32bc0-104">Option</span></span>

<span data-ttu-id="32bc0-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="32bc0-105">This topic is not current.</span></span> <span data-ttu-id="32bc0-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="32bc0-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="32bc0-107">Элемент Option содержит все элементы Property и Скоредпроперти, связанные с этим параметром.</span><span class="sxs-lookup"><span data-stu-id="32bc0-107">An Option element contains all of the Property and ScoredProperty elements associated with this option.</span></span>

## <a name="element-tag"></a><span data-ttu-id="32bc0-108">Тег элемента</span><span class="sxs-lookup"><span data-stu-id="32bc0-108">Element Tag</span></span>

<Option>

## <a name="xml-attributes"></a><span data-ttu-id="32bc0-109">XML-атрибуты</span><span class="sxs-lookup"><span data-stu-id="32bc0-109">XML Attributes</span></span>

<span data-ttu-id="32bc0-110">В следующей таблице перечислены атрибуты XML, которые могут быть связаны с этим элементом.</span><span class="sxs-lookup"><span data-stu-id="32bc0-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="32bc0-111">Атрибут XML</span><span class="sxs-lookup"><span data-stu-id="32bc0-111">XML Attribute</span></span>          | <span data-ttu-id="32bc0-112">Сведения</span><span class="sxs-lookup"><span data-stu-id="32bc0-112">Details</span></span>                                                                                                                                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32bc0-113">ограниченного</span><span class="sxs-lookup"><span data-stu-id="32bc0-113">constrained</span></span><br/> | <span data-ttu-id="32bc0-114">Этот атрибут является необязательным для документа PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="32bc0-114">This attribute is optional for a PrintCapabilities document.</span></span><br/> <span data-ttu-id="32bc0-115">Этот атрибут указывает, доступен ли параметр для выбора или использования.</span><span class="sxs-lookup"><span data-stu-id="32bc0-115">This attribute indicates whether the Option is available for selection or use.</span></span> <span data-ttu-id="32bc0-116">Этому XML-атрибуту можно присвоить одно из следующих значений: None, Принттиккетсеттингс, Админсеттинг или Девицесеттингс.</span><span class="sxs-lookup"><span data-stu-id="32bc0-116">This XML attribute can be set to one of the following values: None, PrintTicketSettings, AdminSetting or DeviceSettings.</span></span> <br/> <span data-ttu-id="32bc0-117">См. [атрибуты XML](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="32bc0-117">See [XML Attributes](xml-attributes.md)</span></span><br/> |
| <span data-ttu-id="32bc0-118">name</span><span class="sxs-lookup"><span data-stu-id="32bc0-118">name</span></span><br/>        | <span data-ttu-id="32bc0-119">Содержит имя параметра (стандартный или закрытый)..</span><span class="sxs-lookup"><span data-stu-id="32bc0-119">Holds the name of the Option, either a standard Option or a privately-defined Option.</span></span> <span data-ttu-id="32bc0-120">XML-атрибут используется таким образом для различения экземпляров параметров.</span><span class="sxs-lookup"><span data-stu-id="32bc0-120">The XML attribute is used this way in order to differentiate between Option instances.</span></span> <br/>                                                                                                                                                        |



 

<span data-ttu-id="32bc0-121">Дополнительные сведения см. в разделе [XML Attributes](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="32bc0-121">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="32bc0-122">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="32bc0-122">Element Information</span></span>

<span data-ttu-id="32bc0-123">В следующей таблице перечислены элементы, которые могут быть родительскими для этого элемента, элементы, которые могут быть дочерними для этого элемента, и любые ограничения на сам элемент.</span><span class="sxs-lookup"><span data-stu-id="32bc0-123">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="32bc0-124">Категория</span><span class="sxs-lookup"><span data-stu-id="32bc0-124">Category</span></span>                   | <span data-ttu-id="32bc0-125">Сведения</span><span class="sxs-lookup"><span data-stu-id="32bc0-125">Details</span></span>                                                                                                                                                                                                                                                                                          |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32bc0-126">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="32bc0-126">Parent elements</span></span><br/> | <span data-ttu-id="32bc0-127">Функция</span><span class="sxs-lookup"><span data-stu-id="32bc0-127">Feature</span></span> <br/>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="32bc0-128">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="32bc0-128">Child elements</span></span><br/>  | <span data-ttu-id="32bc0-129">*Свойство* (ноль или более)</span><span class="sxs-lookup"><span data-stu-id="32bc0-129">*Property* (zero or more)</span></span><br/> <span data-ttu-id="32bc0-130">*Скоредпроперти* (ноль или более для параметров с XML-атрибутом "имя"; один или несколько для параметров, не использующих XML-атрибут "имя" \* )</span><span class="sxs-lookup"><span data-stu-id="32bc0-130">*ScoredProperty* (zero or more for Options with XML Attribute 'name'; one or more for Options not utilizing XML Attribute 'name'\*)</span></span><br/> <span data-ttu-id="32bc0-131">\* только открытые параметры, определенные в схеме печати, не могут иметь атрибут "Name", например Документнуп)</span><span class="sxs-lookup"><span data-stu-id="32bc0-131">\* only public Options defined in Print Schema can have no 'name' attribute, such as DocumentNUp)</span></span><br/> |
| <span data-ttu-id="32bc0-132">Этот элемент</span><span class="sxs-lookup"><span data-stu-id="32bc0-132">This element</span></span><br/>    | <span data-ttu-id="32bc0-133">Символьные данные не допускаются.</span><span class="sxs-lookup"><span data-stu-id="32bc0-133">No character data is permitted.</span></span><br/> <span data-ttu-id="32bc0-134">Дублирование дочерних одноуровневых элементов не разрешено.</span><span class="sxs-lookup"><span data-stu-id="32bc0-134">Duplicate child siblings are not permitted.</span></span><br/>                                                                                                                                                                                                |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="32bc0-135">Зависимости конфигурации</span><span class="sxs-lookup"><span data-stu-id="32bc0-135">Configuration Dependencies</span></span>

<span data-ttu-id="32bc0-136">Элемент определения параметра не может иметь зависимостей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="32bc0-136">An Option definition element may not have any configuration dependencies.</span></span>

## <a name="element-usage"></a><span data-ttu-id="32bc0-137">Использование элементов</span><span class="sxs-lookup"><span data-stu-id="32bc0-137">Element Usage</span></span>

<span data-ttu-id="32bc0-138">Цель элемента Option состоит в том, чтобы определить одно из состояний, которые может предположить атрибут конфигурации устройства, представленный элементом Feature.</span><span class="sxs-lookup"><span data-stu-id="32bc0-138">The purpose of the Option element is to characterize one of the states that a device configuration attribute, represented by a Feature element, can assume.</span></span> <span data-ttu-id="32bc0-139">Каждое определение элемента параметра содержит один или несколько элементов Скоредпроперти, описывающих внутреннюю или важнейшую характеристику этого параметра.</span><span class="sxs-lookup"><span data-stu-id="32bc0-139">Each Option element definition contains one or more ScoredProperty elements that describe an intrinsic or essential characteristic of that Option.</span></span> <span data-ttu-id="32bc0-140">Чтобы упростить перенос и сохранение намерения, схема печати определяет множество общих элементов функций и различные элементы параметров для каждой функции.</span><span class="sxs-lookup"><span data-stu-id="32bc0-140">To facilitate portability and preservation of intent, the Print Schema defines many common Feature elements and a variety of Option elements for each Feature.</span></span> <span data-ttu-id="32bc0-141">Поэтому важно использовать элементы параметров печати, определенные схемой, если это возможно, прежде чем создавать собственные определения параметров.</span><span class="sxs-lookup"><span data-stu-id="32bc0-141">It is therefore important to use Print Schema-defined Option elements, if at all possible, before you create your own Option definitions.</span></span> <span data-ttu-id="32bc0-142">Понимание процесса определения элементов параметров предоставляет полезные сведения о том, как документ PrintCapabilities и PrintTicket используются в Microsoft .NET Framework версии 3,0 и в архитектуре печати Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="32bc0-142">Understanding the process of defining Option elements provides useful insights into the way the PrintCapabilities document and PrintTickets are used in the Microsoft .NET Framework version 3.0 and Windows Vista printing architecture.</span></span>

## <a name="example"></a><span data-ttu-id="32bc0-143">Пример</span><span class="sxs-lookup"><span data-stu-id="32bc0-143">Example</span></span>

<span data-ttu-id="32bc0-144">В следующем примере определяется имя для параметра.</span><span class="sxs-lookup"><span data-stu-id="32bc0-144">The following example defines a name for the Option.</span></span>

``` syntax
<psf:Option name="psk:PrintFront" />
```

## <a name="related-topics"></a><span data-ttu-id="32bc0-145">См. также</span><span class="sxs-lookup"><span data-stu-id="32bc0-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32bc0-146">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="32bc0-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




