---
description: Возвращает сведения об элементе option. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: feda78d9-58e7-4668-8a25-40e5fd8ad456
title: Параметр
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ac4318e6a79a3d4daa77f15901d032c66134bdd
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549382"
---
# <a name="option"></a><span data-ttu-id="9574a-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="9574a-105">Option</span></span>

<span data-ttu-id="9574a-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="9574a-106">This topic is not current.</span></span> <span data-ttu-id="9574a-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9574a-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9574a-108">Элемент Option содержит все элементы Property и Скоредпроперти, связанные с этим параметром.</span><span class="sxs-lookup"><span data-stu-id="9574a-108">An Option element contains all of the Property and ScoredProperty elements associated with this option.</span></span>

## <a name="element-tag"></a><span data-ttu-id="9574a-109">Тег элемента</span><span class="sxs-lookup"><span data-stu-id="9574a-109">Element Tag</span></span>

<Option>

## <a name="xml-attributes"></a><span data-ttu-id="9574a-110">XML-атрибуты</span><span class="sxs-lookup"><span data-stu-id="9574a-110">XML Attributes</span></span>

<span data-ttu-id="9574a-111">В следующей таблице перечислены атрибуты XML, которые могут быть связаны с этим элементом.</span><span class="sxs-lookup"><span data-stu-id="9574a-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="9574a-112">Атрибут XML</span><span class="sxs-lookup"><span data-stu-id="9574a-112">XML Attribute</span></span>          | <span data-ttu-id="9574a-113">Сведения</span><span class="sxs-lookup"><span data-stu-id="9574a-113">Details</span></span>                                                                                                                                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9574a-114">ограниченного</span><span class="sxs-lookup"><span data-stu-id="9574a-114">constrained</span></span><br/> | <span data-ttu-id="9574a-115">Этот атрибут является необязательным для документа PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="9574a-115">This attribute is optional for a PrintCapabilities document.</span></span><br/> <span data-ttu-id="9574a-116">Этот атрибут указывает, доступен ли параметр для выбора или использования.</span><span class="sxs-lookup"><span data-stu-id="9574a-116">This attribute indicates whether the Option is available for selection or use.</span></span> <span data-ttu-id="9574a-117">Этому XML-атрибуту можно присвоить одно из следующих значений: None, Принттиккетсеттингс, Админсеттинг или Девицесеттингс.</span><span class="sxs-lookup"><span data-stu-id="9574a-117">This XML attribute can be set to one of the following values: None, PrintTicketSettings, AdminSetting or DeviceSettings.</span></span> <br/> <span data-ttu-id="9574a-118">См. [атрибуты XML](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="9574a-118">See [XML Attributes](xml-attributes.md)</span></span><br/> |
| <span data-ttu-id="9574a-119">name</span><span class="sxs-lookup"><span data-stu-id="9574a-119">name</span></span><br/>        | <span data-ttu-id="9574a-120">Содержит имя параметра (стандартный или закрытый)..</span><span class="sxs-lookup"><span data-stu-id="9574a-120">Holds the name of the Option, either a standard Option or a privately-defined Option.</span></span> <span data-ttu-id="9574a-121">XML-атрибут используется таким образом для различения экземпляров параметров.</span><span class="sxs-lookup"><span data-stu-id="9574a-121">The XML attribute is used this way in order to differentiate between Option instances.</span></span> <br/>                                                                                                                                                        |



 

<span data-ttu-id="9574a-122">Дополнительные сведения см. в разделе [XML Attributes](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="9574a-122">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="9574a-123">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="9574a-123">Element Information</span></span>

<span data-ttu-id="9574a-124">В следующей таблице перечислены элементы, которые могут быть родительскими для этого элемента, элементы, которые могут быть дочерними для этого элемента, и любые ограничения на сам элемент.</span><span class="sxs-lookup"><span data-stu-id="9574a-124">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="9574a-125">Категория</span><span class="sxs-lookup"><span data-stu-id="9574a-125">Category</span></span>                   | <span data-ttu-id="9574a-126">Сведения</span><span class="sxs-lookup"><span data-stu-id="9574a-126">Details</span></span>                                                                                                                                                                                                                                                                                          |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9574a-127">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="9574a-127">Parent elements</span></span><br/> | <span data-ttu-id="9574a-128">Компонент</span><span class="sxs-lookup"><span data-stu-id="9574a-128">Feature</span></span> <br/>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="9574a-129">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9574a-129">Child elements</span></span><br/>  | <span data-ttu-id="9574a-130">*Свойство* (ноль или более)</span><span class="sxs-lookup"><span data-stu-id="9574a-130">*Property* (zero or more)</span></span><br/> <span data-ttu-id="9574a-131">*Скоредпроперти* (ноль или более для параметров с XML-атрибутом "имя"; один или несколько для параметров, не использующих XML-атрибут "имя" \* )</span><span class="sxs-lookup"><span data-stu-id="9574a-131">*ScoredProperty* (zero or more for Options with XML Attribute 'name'; one or more for Options not utilizing XML Attribute 'name'\*)</span></span><br/> <span data-ttu-id="9574a-132">\* только открытые параметры, определенные в схеме печати, не могут иметь атрибут "Name", например Документнуп)</span><span class="sxs-lookup"><span data-stu-id="9574a-132">\* only public Options defined in Print Schema can have no 'name' attribute, such as DocumentNUp)</span></span><br/> |
| <span data-ttu-id="9574a-133">Этот элемент</span><span class="sxs-lookup"><span data-stu-id="9574a-133">This element</span></span><br/>    | <span data-ttu-id="9574a-134">Символьные данные не допускаются.</span><span class="sxs-lookup"><span data-stu-id="9574a-134">No character data is permitted.</span></span><br/> <span data-ttu-id="9574a-135">Дублирование дочерних одноуровневых элементов не разрешено.</span><span class="sxs-lookup"><span data-stu-id="9574a-135">Duplicate child siblings are not permitted.</span></span><br/>                                                                                                                                                                                                |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="9574a-136">Зависимости конфигурации</span><span class="sxs-lookup"><span data-stu-id="9574a-136">Configuration Dependencies</span></span>

<span data-ttu-id="9574a-137">Элемент определения параметра не может иметь зависимостей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="9574a-137">An Option definition element may not have any configuration dependencies.</span></span>

## <a name="element-usage"></a><span data-ttu-id="9574a-138">Использование элементов</span><span class="sxs-lookup"><span data-stu-id="9574a-138">Element Usage</span></span>

<span data-ttu-id="9574a-139">Цель элемента Option состоит в том, чтобы определить одно из состояний, которые может предположить атрибут конфигурации устройства, представленный элементом Feature.</span><span class="sxs-lookup"><span data-stu-id="9574a-139">The purpose of the Option element is to characterize one of the states that a device configuration attribute, represented by a Feature element, can assume.</span></span> <span data-ttu-id="9574a-140">Каждое определение элемента параметра содержит один или несколько элементов Скоредпроперти, описывающих внутреннюю или важнейшую характеристику этого параметра.</span><span class="sxs-lookup"><span data-stu-id="9574a-140">Each Option element definition contains one or more ScoredProperty elements that describe an intrinsic or essential characteristic of that Option.</span></span> <span data-ttu-id="9574a-141">Чтобы упростить перенос и сохранение намерения, схема печати определяет множество общих элементов функций и различные элементы параметров для каждой функции.</span><span class="sxs-lookup"><span data-stu-id="9574a-141">To facilitate portability and preservation of intent, the Print Schema defines many common Feature elements and a variety of Option elements for each Feature.</span></span> <span data-ttu-id="9574a-142">Поэтому важно использовать элементы параметров печати, определенные схемой, если это возможно, прежде чем создавать собственные определения параметров.</span><span class="sxs-lookup"><span data-stu-id="9574a-142">It is therefore important to use Print Schema-defined Option elements, if at all possible, before you create your own Option definitions.</span></span> <span data-ttu-id="9574a-143">понимание процесса определения элементов параметров предоставляет полезные сведения о том, как документ PrintCapabilities и printticket используются в архитектуре печати Microsoft платформа .NET Framework версии 3,0 и Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9574a-143">Understanding the process of defining Option elements provides useful insights into the way the PrintCapabilities document and PrintTickets are used in the Microsoft .NET Framework version 3.0 and Windows Vista printing architecture.</span></span>

## <a name="example"></a><span data-ttu-id="9574a-144">Пример</span><span class="sxs-lookup"><span data-stu-id="9574a-144">Example</span></span>

<span data-ttu-id="9574a-145">В следующем примере определяется имя для параметра.</span><span class="sxs-lookup"><span data-stu-id="9574a-145">The following example defines a name for the Option.</span></span>

``` syntax
<psf:Option name="psk:PrintFront" />
```

## <a name="related-topics"></a><span data-ttu-id="9574a-146">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="9574a-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9574a-147">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="9574a-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




