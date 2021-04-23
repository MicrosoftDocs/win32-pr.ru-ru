---
description: Все реализации, совместимые с CIM, должны работать со стандартным набором квалификаторов.
ms.assetid: 671ea769-f68d-4788-96f5-c4f86ab3b00e
ms.tgt_platform: multiple
title: Стандартные квалификаторы
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Standard
api_type:
- NA
api_location: ''
ms.openlocfilehash: 710e93e53f9e414a44dc14ebafea426f5d7f9efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701986"
---
# <a name="standard-qualifiers"></a><span data-ttu-id="4cf14-103">Стандартные квалификаторы</span><span class="sxs-lookup"><span data-stu-id="4cf14-103">Standard Qualifiers</span></span>

<span data-ttu-id="4cf14-104">Все реализации, совместимые с CIM, должны работать со стандартным набором квалификаторов.</span><span class="sxs-lookup"><span data-stu-id="4cf14-104">All CIM-compliant implementations must handle a standard set of qualifiers.</span></span> <span data-ttu-id="4cf14-105">Все указанные объекты не имеют всех указанных квалификаторов.</span><span class="sxs-lookup"><span data-stu-id="4cf14-105">Any specific object does not have all of the qualifiers listed.</span></span> <span data-ttu-id="4cf14-106">Как правило, классы расширений предоставляют дополнительные квалификаторы для упрощения инициализации экземпляров классов и других операций с классом.</span><span class="sxs-lookup"><span data-stu-id="4cf14-106">Usually, extension classes supply additional qualifiers to facilitate provision of class instances and other operations on the class.</span></span>

<span data-ttu-id="4cf14-107">Поставщик должен применять квалификаторы.</span><span class="sxs-lookup"><span data-stu-id="4cf14-107">It is the responsibility of the provider to enforce the qualifiers.</span></span> <span data-ttu-id="4cf14-108">Инструментарий WMI не применяет квалификаторы, но использует их только для информирования пользователя о том, как используется свойство.</span><span class="sxs-lookup"><span data-stu-id="4cf14-108">WMI does not enforce qualifiers, but uses them only to inform the user about how the property is used.</span></span>

> [!Note]  
> <span data-ttu-id="4cf14-109">Инструментарий WMI соответствует спецификации CIM 2,5.</span><span class="sxs-lookup"><span data-stu-id="4cf14-109">WMI is compliant with the CIM 2.5 specification.</span></span>

 

<span data-ttu-id="4cf14-110">Квалификаторы имеют следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="4cf14-110">Qualifiers have the following limitations:</span></span>

-   <span data-ttu-id="4cf14-111">Не все стандартные квалификаторы можно использовать вместе.</span><span class="sxs-lookup"><span data-stu-id="4cf14-111">Not all standard qualifiers can be used together.</span></span>
-   <span data-ttu-id="4cf14-112">Не все Квалификаторы могут применяться ко всем конструкциям, таким как ассоциация или ссылка.</span><span class="sxs-lookup"><span data-stu-id="4cf14-112">Not all qualifiers can be applied to all constructs, such as association or reference.</span></span> <span data-ttu-id="4cf14-113">Эти ограничения определены в списке применимо к.</span><span class="sxs-lookup"><span data-stu-id="4cf14-113">These limitations are identified in the Applies to list.</span></span>
-   <span data-ttu-id="4cf14-114">Для конкретной конструкции, такой как ассоциация или ссылка, использование юридических квалификаторов может быть дополнительно ограничено, так как некоторые квалификаторы являются взаимоисключающими, а использование одного квалификатора может привести к некоторым ограничениям на значение другого и т. д.</span><span class="sxs-lookup"><span data-stu-id="4cf14-114">For a particular construct, such as association or reference, the use of the legal qualifiers can be further constrained because some qualifiers are mutually exclusive, the use of one qualifier may imply some restrictions on the value of another, and so on.</span></span> <span data-ttu-id="4cf14-115">Эти правила использования задокументированы.</span><span class="sxs-lookup"><span data-stu-id="4cf14-115">These usage rules are documented.</span></span>
-   <span data-ttu-id="4cf14-116">Юридические квалификаторы наследуются сущностями, такими как свойства, методы, экземпляры или подклассы, а не по связям или ссылкам.</span><span class="sxs-lookup"><span data-stu-id="4cf14-116">Legal qualifiers are inherited by entities such as properties, methods, instances, or subclasses only, not by associations or references.</span></span> <span data-ttu-id="4cf14-117">Например, квалификатор **maxlen** , применяемый к свойствам, не наследуется ссылками.</span><span class="sxs-lookup"><span data-stu-id="4cf14-117">For example, the **MaxLen** qualifier that applies to properties is not inherited by references.</span></span>

<span data-ttu-id="4cf14-118">Ниже перечислены квалификаторы WMI уровня "Стандартный".</span><span class="sxs-lookup"><span data-stu-id="4cf14-118">The following lists WMI standard qualifiers.</span></span>

<dt>

<span data-ttu-id="4cf14-119"><span id="Abstract"></span><span id="abstract"></span><span id="ABSTRACT"></span>**Выделяет**</span><span class="sxs-lookup"><span data-stu-id="4cf14-119"><span id="Abstract"></span><span id="abstract"></span><span id="ABSTRACT"></span>**Abstract**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-120">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4cf14-120">Data type: **boolean**</span></span>

<span data-ttu-id="4cf14-121">Область применения: классы, ассоциации, указания</span><span class="sxs-lookup"><span data-stu-id="4cf14-121">Applies to: classes, associations, indications</span></span>

<span data-ttu-id="4cf14-122">Указывает, является ли класс абстрактным и служит только в качестве основы для новых классов.</span><span class="sxs-lookup"><span data-stu-id="4cf14-122">Indicates whether the class is abstract and serves only as a base for new classes.</span></span> <span data-ttu-id="4cf14-123">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-123">The default is **FALSE**.</span></span> <span data-ttu-id="4cf14-124">Нельзя создавать экземпляры абстрактных классов.</span><span class="sxs-lookup"><span data-stu-id="4cf14-124">You cannot create instances of abstract classes.</span></span> <span data-ttu-id="4cf14-125">Отсутствие этого квалификатора указывает, что класс не является абстрактным; Таким образом, этот квалификатор необходим для всех абстрактных классов.</span><span class="sxs-lookup"><span data-stu-id="4cf14-125">The absence of this qualifier indicates that the class is not abstract; therefore, this qualifier is required for all abstract classes.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-126"><span id="Aggregate"></span><span id="aggregate"></span><span id="AGGREGATE"></span>**Множеств**</span><span class="sxs-lookup"><span data-stu-id="4cf14-126"><span id="Aggregate"></span><span id="aggregate"></span><span id="AGGREGATE"></span>**Aggregate**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-127">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4cf14-127">Data type: **boolean**</span></span>

<span data-ttu-id="4cf14-128">Область применения: ссылки</span><span class="sxs-lookup"><span data-stu-id="4cf14-128">Applies to: references</span></span>

<span data-ttu-id="4cf14-129">Указывает, является ли ссылка родительским компонентом статистической ассоциации.</span><span class="sxs-lookup"><span data-stu-id="4cf14-129">Indicates whether the reference is the parent component of an aggregation association.</span></span> <span data-ttu-id="4cf14-130">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-130">The default is **FALSE**.</span></span>

<span data-ttu-id="4cf14-131">Использование: квалификаторы **статистической обработки** и **статистической функции** используются совместно со   **статистической** обработкой, а **функция Aggregate** задает родительскую ссылку.</span><span class="sxs-lookup"><span data-stu-id="4cf14-131">Usage: The **Aggregation** and **Aggregate** qualifiers are used together   **Aggregation** qualifies the association, and **Aggregate** specifies the parent reference.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-132"><span id="Aggregation"></span><span id="aggregation"></span><span id="AGGREGATION"></span>**Статистической обработки**</span><span class="sxs-lookup"><span data-stu-id="4cf14-132"><span id="Aggregation"></span><span id="aggregation"></span><span id="AGGREGATION"></span>**Aggregation**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-133">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4cf14-133">Data type: **boolean**</span></span>

<span data-ttu-id="4cf14-134">Область применения: связи</span><span class="sxs-lookup"><span data-stu-id="4cf14-134">Applies to: associations</span></span>

<span data-ttu-id="4cf14-135">Указывает, является ли ассоциация агрегатом.</span><span class="sxs-lookup"><span data-stu-id="4cf14-135">Indicates whether the association is an aggregation.</span></span> <span data-ttu-id="4cf14-136">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-136">The default is **FALSE**.</span></span> <span data-ttu-id="4cf14-137">Используется со **статистическим выражением**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-137">Used with **Aggregate**.</span></span> <span data-ttu-id="4cf14-138">Этот квалификатор является обязательным для всех сопоставлений агрегатов.</span><span class="sxs-lookup"><span data-stu-id="4cf14-138">This qualifier is required for all aggregation associations.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-139"><span id="Alias"></span><span id="alias"></span><span id="ALIAS"></span>**Псевдоним**</span><span class="sxs-lookup"><span data-stu-id="4cf14-139"><span id="Alias"></span><span id="alias"></span><span id="ALIAS"></span>**Alias**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4cf14-140">Data type: **string**</span></span>

<span data-ttu-id="4cf14-141">Область применения: свойства, ссылки, методы</span><span class="sxs-lookup"><span data-stu-id="4cf14-141">Applies to: properties, references, methods</span></span>

<span data-ttu-id="4cf14-142">Альтернативное имя для свойства или метода в схеме.</span><span class="sxs-lookup"><span data-stu-id="4cf14-142">Alternate name for a property or method in the schema.</span></span> <span data-ttu-id="4cf14-143">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-143">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-144"><span id="ArrayType"></span><span id="arraytype"></span><span id="ARRAYTYPE"></span>**ArrayType**</span><span class="sxs-lookup"><span data-stu-id="4cf14-144"><span id="ArrayType"></span><span id="arraytype"></span><span id="ARRAYTYPE"></span>**ArrayType**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4cf14-145">Data type: **string**</span></span>

<span data-ttu-id="4cf14-146">Область применения: свойства, параметры</span><span class="sxs-lookup"><span data-stu-id="4cf14-146">Applies to: properties, parameters</span></span>

<span data-ttu-id="4cf14-147">Тип полного массива.</span><span class="sxs-lookup"><span data-stu-id="4cf14-147">Type of the qualified array.</span></span>

<span data-ttu-id="4cf14-148">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="4cf14-148">Valid values are:</span></span>

-   <span data-ttu-id="4cf14-149">контейнер (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4cf14-149">bag (default)</span></span>
-   <span data-ttu-id="4cf14-150">индексированные</span><span class="sxs-lookup"><span data-stu-id="4cf14-150">indexed</span></span>
-   <span data-ttu-id="4cf14-151">упорядоченного</span><span class="sxs-lookup"><span data-stu-id="4cf14-151">ordered</span></span>

<span data-ttu-id="4cf14-152">Использование: Примените этот тип квалификатора только к свойствам и параметрам, которые являются массивами (определяемыми с помощью синтаксиса скобок).</span><span class="sxs-lookup"><span data-stu-id="4cf14-152">Usage: Apply this type of qualifier only to properties and parameters that are arrays (defined by using bracket syntax).</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-153"><span id="BitMap"></span><span id="bitmap"></span><span id="BITMAP"></span>**Массив**</span><span class="sxs-lookup"><span data-stu-id="4cf14-153"><span id="BitMap"></span><span id="bitmap"></span><span id="BITMAP"></span>**BitMap**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-154">Тип данных: **массив строк**</span><span class="sxs-lookup"><span data-stu-id="4cf14-154">Data type: **string array**</span></span>

<span data-ttu-id="4cf14-155">Область применения: свойства, методы, параметры</span><span class="sxs-lookup"><span data-stu-id="4cf14-155">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="4cf14-156">Сопоставьте значительные позиции, где каждая значимая позиция может быть "on" или "OFF".</span><span class="sxs-lookup"><span data-stu-id="4cf14-156">Map of significant bit positions where each significant position can be "on" or "off".</span></span> <span data-ttu-id="4cf14-157">Каждый бит "на" соответствует соответствующему значению в массиве **битвалуес** .</span><span class="sxs-lookup"><span data-stu-id="4cf14-157">Each "on" bit maps to a corresponding value in the **BitValues** array.</span></span> <span data-ttu-id="4cf14-158">Наличие нескольких битов "on" указывает несколько одновременных значений в массиве **битвалуес** .</span><span class="sxs-lookup"><span data-stu-id="4cf14-158">By having multiple bits "on", multiple concurrent values in the **BitValues** array are indicated.</span></span> <span data-ttu-id="4cf14-159">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-159">The default is **NULL**.</span></span>

<span data-ttu-id="4cf14-160">Дополнительные сведения см. в разделе [BitMap и битвалуес](bitmap-and-bitvalues.md).</span><span class="sxs-lookup"><span data-stu-id="4cf14-160">For more information, see [BitMap and BitValues](bitmap-and-bitvalues.md).</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-161"><span id="BitValues"></span><span id="bitvalues"></span><span id="BITVALUES"></span>**битвалуес**</span><span class="sxs-lookup"><span data-stu-id="4cf14-161"><span id="BitValues"></span><span id="bitvalues"></span><span id="BITVALUES"></span>**BitValues**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-162">Тип данных: **массив строк**</span><span class="sxs-lookup"><span data-stu-id="4cf14-162">Data type: **string array**</span></span>

<span data-ttu-id="4cf14-163">Область применения: свойства, методы, параметры</span><span class="sxs-lookup"><span data-stu-id="4cf14-163">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="4cf14-164">Преобразование значения битовой координаты в связанную **строку**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-164">Translation of a bit position value into an associated **string**.</span></span> <span data-ttu-id="4cf14-165">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-165">The default is **NULL**.</span></span>

<span data-ttu-id="4cf14-166">Дополнительные сведения см. в разделе [BitMap и битвалуес](bitmap-and-bitvalues.md).</span><span class="sxs-lookup"><span data-stu-id="4cf14-166">For more information, see [BitMap and BitValues](bitmap-and-bitvalues.md).</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-167"><span id="Constructor"></span><span id="constructor"></span><span id="CONSTRUCTOR"></span>**Конструктор**</span><span class="sxs-lookup"><span data-stu-id="4cf14-167"><span id="Constructor"></span><span id="constructor"></span><span id="CONSTRUCTOR"></span>**Constructor**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-168">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4cf14-168">Data type: **boolean**</span></span>

<span data-ttu-id="4cf14-169">Область применения: методы</span><span class="sxs-lookup"><span data-stu-id="4cf14-169">Applies to: methods</span></span>

<span data-ttu-id="4cf14-170">Указывает, создает ли метод экземпляры.</span><span class="sxs-lookup"><span data-stu-id="4cf14-170">Indicates whether the method creates instances.</span></span> <span data-ttu-id="4cf14-171">Эти методы не ограничиваются обработкой одного экземпляра или одного класса.</span><span class="sxs-lookup"><span data-stu-id="4cf14-171">These methods are not constrained to acting on a single instance or a single class.</span></span> <span data-ttu-id="4cf14-172">Например, конструктор может создавать экземпляры ассоциации, а также экземпляры класса, определяющие конструктор.</span><span class="sxs-lookup"><span data-stu-id="4cf14-172">For example, a constructor can create association instances as well as instances of the class that defines the constructor.</span></span>

<span data-ttu-id="4cf14-173">Квалификатор **конструктора** предназначен только для информации и не ожидается, что он действует диспетчером объектов.</span><span class="sxs-lookup"><span data-stu-id="4cf14-173">The **Constructor** qualifier is intended for information only and it is not expected that it is acted on by the object manager.</span></span> <span data-ttu-id="4cf14-174">Диспетчеру объектов не обязательно вызывать методы конструктора при создании объекта.</span><span class="sxs-lookup"><span data-stu-id="4cf14-174">The object manager does not have to call constructor methods when an object is created.</span></span> <span data-ttu-id="4cf14-175">Кроме того, при вызове конструктора диспетчер объектов не должен вызывать методы конструктора, определенные для любого родительского класса исходного класса.</span><span class="sxs-lookup"><span data-stu-id="4cf14-175">Also when a constructor is called, the object manager does not have to invoke any constructor methods defined for any parent class of the original class.</span></span> <span data-ttu-id="4cf14-176">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-176">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-177"><span id="CreateBy"></span><span id="createby"></span><span id="CREATEBY"></span>**креатеби**</span><span class="sxs-lookup"><span data-stu-id="4cf14-177"><span id="CreateBy"></span><span id="createby"></span><span id="CREATEBY"></span>**CreateBy**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-178">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4cf14-178">Data type: **string**</span></span>

<span data-ttu-id="4cf14-179">Область применения: классы</span><span class="sxs-lookup"><span data-stu-id="4cf14-179">Applies to: classes</span></span>

<span data-ttu-id="4cf14-180">Имя метода, с помощью которого создаются экземпляры этого класса.</span><span class="sxs-lookup"><span data-stu-id="4cf14-180">Name of the method by which instances of this class are created.</span></span> <span data-ttu-id="4cf14-181">Значение может быть либо "PutInstance", либо именем другого метода, который создает экземпляры.</span><span class="sxs-lookup"><span data-stu-id="4cf14-181">The value is either "PutInstance" or the name of another method that creates the instances.</span></span> <span data-ttu-id="4cf14-182">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-182">The default is **NULL**.</span></span>

<span data-ttu-id="4cf14-183">Использование: этот квалификатор можно использовать только при наличии квалификатора **суппортскреате** .</span><span class="sxs-lookup"><span data-stu-id="4cf14-183">Usage: This qualifier can only be used if the **SupportsCreate** qualifier is present.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-184"><span id="DeleteBy"></span><span id="deleteby"></span><span id="DELETEBY"></span>**делетеби**</span><span class="sxs-lookup"><span data-stu-id="4cf14-184"><span id="DeleteBy"></span><span id="deleteby"></span><span id="DELETEBY"></span>**DeleteBy**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-185">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4cf14-185">Data type: **string**</span></span>

<span data-ttu-id="4cf14-186">Область применения: классы</span><span class="sxs-lookup"><span data-stu-id="4cf14-186">Applies to: classes</span></span>

<span data-ttu-id="4cf14-187">Имя метода, с помощью которого удаляются экземпляры этого класса.</span><span class="sxs-lookup"><span data-stu-id="4cf14-187">Name of the method by which instances of this class are deleted.</span></span> <span data-ttu-id="4cf14-188">Значение может быть либо "DeleteInstance", либо именем другого метода, который удаляет экземпляры.</span><span class="sxs-lookup"><span data-stu-id="4cf14-188">The value is either "DeleteInstance", or the name of another method that deletes the instances.</span></span> <span data-ttu-id="4cf14-189">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-189">The default is **NULL**.</span></span>

<span data-ttu-id="4cf14-190">Использование: этот квалификатор можно использовать только при наличии квалификатора **суппортсделете** .</span><span class="sxs-lookup"><span data-stu-id="4cf14-190">Usage: This qualifier can only be used if the **SupportsDelete** qualifier is present.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="4cf14-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-192">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4cf14-192">Data type: **string**</span></span>

<span data-ttu-id="4cf14-193">Применимо к: Any</span><span class="sxs-lookup"><span data-stu-id="4cf14-193">Applies to: any</span></span>

<span data-ttu-id="4cf14-194">Описание именованного элемента.</span><span class="sxs-lookup"><span data-stu-id="4cf14-194">Description of a named element.</span></span> <span data-ttu-id="4cf14-195">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-195">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-196"><span id="Destructor"></span><span id="destructor"></span><span id="DESTRUCTOR"></span>**Использовал**</span><span class="sxs-lookup"><span data-stu-id="4cf14-196"><span id="Destructor"></span><span id="destructor"></span><span id="DESTRUCTOR"></span>**Destructor**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-197">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4cf14-197">Data type: **boolean**</span></span>

<span data-ttu-id="4cf14-198">Область применения: методы</span><span class="sxs-lookup"><span data-stu-id="4cf14-198">Applies to: methods</span></span>

<span data-ttu-id="4cf14-199">Указывает, удаляет ли метод экземпляры.</span><span class="sxs-lookup"><span data-stu-id="4cf14-199">Indicates whether the method deletes instances.</span></span> <span data-ttu-id="4cf14-200">Методы, использующие квалификатор **деструктора** , удаляют экземпляры, к которым применяется деструктор, и не ограничиваются обработкой одного экземпляра или класса.</span><span class="sxs-lookup"><span data-stu-id="4cf14-200">Methods using the **Destructor** qualifier delete the instance(s) to which the destructor is applied, and are not constrained to acting on a single instance or class.</span></span> <span data-ttu-id="4cf14-201">Например, деструктор может удалять экземпляры ассоциации, а также экземпляры класса, определяющие деструктор.</span><span class="sxs-lookup"><span data-stu-id="4cf14-201">For example, a destructor might delete association instances as well as instances of the class that defines the destructor.</span></span>

<span data-ttu-id="4cf14-202">Квалификатор **деструктора** предназначен только для информации и не ожидается, что он действует диспетчером объектов.</span><span class="sxs-lookup"><span data-stu-id="4cf14-202">The **Destructor** qualifier is intended for information only and it is not expected that it is acted on by the object manager.</span></span> <span data-ttu-id="4cf14-203">При удалении экземпляра диспетчер объектов не обязан вызвать метод, имеющий квалификатор **деструктора** .</span><span class="sxs-lookup"><span data-stu-id="4cf14-203">There is no obligation for the object manager to call a method that has the **Destructor** qualifier when an instance is deleted.</span></span> <span data-ttu-id="4cf14-204">Кроме того, при вызове деструктора диспетчеру объектов не нужно вызывать методы деструктора, определенные для любого родительского класса исходного класса.</span><span class="sxs-lookup"><span data-stu-id="4cf14-204">Also, when a destructor is called, the object manager does not have to invoke any destructor methods defined for any parent class of the original class.</span></span> <span data-ttu-id="4cf14-205">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-205">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-206"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="4cf14-206"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-207">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4cf14-207">Data type: **string**</span></span>

<span data-ttu-id="4cf14-208">Применимо к: Any</span><span class="sxs-lookup"><span data-stu-id="4cf14-208">Applies to: any</span></span>

<span data-ttu-id="4cf14-209">Имя, отображаемое в пользовательском интерфейсе, а не фактическое имя элемента.</span><span class="sxs-lookup"><span data-stu-id="4cf14-209">Name displayed in the UI instead of the actual name of the element.</span></span> <span data-ttu-id="4cf14-210">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-210">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-211"><span id="EmbeddedInstance"></span><span id="embeddedinstance"></span><span id="EMBEDDEDINSTANCE"></span>**ембеддединстанце**</span><span class="sxs-lookup"><span data-stu-id="4cf14-211"><span id="EmbeddedInstance"></span><span id="embeddedinstance"></span><span id="EMBEDDEDINSTANCE"></span>**EmbeddedInstance**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-212">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4cf14-212">Data type: **string**</span></span>

<span data-ttu-id="4cf14-213">Применимо к: Any</span><span class="sxs-lookup"><span data-stu-id="4cf14-213">Applies to: any</span></span>

<span data-ttu-id="4cf14-214">Элемент уточненного строкового типа содержит внедренный экземпляр.</span><span class="sxs-lookup"><span data-stu-id="4cf14-214">The qualified string type element contains an embedded instance.</span></span> <span data-ttu-id="4cf14-215">Значение квалификатора указывает имя класса CIM в том же пространстве имен, что и класс, которому принадлежит квалифицированный элемент.</span><span class="sxs-lookup"><span data-stu-id="4cf14-215">The qualifier value specifies the name of a CIM class in the same namespace as the class owning the qualified element.</span></span> <span data-ttu-id="4cf14-216">Внедренный экземпляр — это экземпляр указанного класса, включая экземпляры его подклассов.</span><span class="sxs-lookup"><span data-stu-id="4cf14-216">The embedded instance is an instance of the specified class, including instances of its subclasses.</span></span> <span data-ttu-id="4cf14-217">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-217">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-218"><span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Калибр**</span><span class="sxs-lookup"><span data-stu-id="4cf14-218"><span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Gauge**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-219">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4cf14-219">Data type: **boolean**</span></span>

<span data-ttu-id="4cf14-220">Применимо к: Any</span><span class="sxs-lookup"><span data-stu-id="4cf14-220">Applies to: any</span></span>

<span data-ttu-id="4cf14-221">Указывает, представляет ли свойство неотрицательное целое число, которое может увеличиваться или уменьшаться, но не должно превышать максимальное значение.</span><span class="sxs-lookup"><span data-stu-id="4cf14-221">Indicates whether the property represents a non-negative integer, which can increase or decrease, but never exceed a maximum value.</span></span> <span data-ttu-id="4cf14-222">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-222">The default is **FALSE**.</span></span>

<span data-ttu-id="4cf14-223">Максимальное значение свойства не может быть больше 2 ^*n* -1.</span><span class="sxs-lookup"><span data-stu-id="4cf14-223">The maximum value of the property cannot be greater than 2^*n* - 1.</span></span> <span data-ttu-id="4cf14-224">*N* может иметь значение 8, 16, 32 или 64 в зависимости от типа данных свойства, к которому применяется этот квалификатор.</span><span class="sxs-lookup"><span data-stu-id="4cf14-224">*N* can be 8, 16, 32, or 64 depending on the data type of the property to which this qualifier is applied.</span></span> <span data-ttu-id="4cf14-225">Значение датчика имеет максимальное значение всякий раз, когда смоделированная информация больше или равна этому максимальному значению.</span><span class="sxs-lookup"><span data-stu-id="4cf14-225">The value of a gauge has its maximum value whenever the information being modeled is greater or equal to that maximum value.</span></span> <span data-ttu-id="4cf14-226">Если сведения, смоделированные в дальнейшем, уменьшится ниже максимального значения, датчик также сокращается.</span><span class="sxs-lookup"><span data-stu-id="4cf14-226">If the information being modeled subsequently decreases below the maximum value, the gauge also decreases.</span></span> <span data-ttu-id="4cf14-227">Этот квалификатор применим только к свойствам с типом данных Integer без знака.</span><span class="sxs-lookup"><span data-stu-id="4cf14-227">This qualifier is applicable only to properties with an unsigned integer data type.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-228"><span id="In"></span><span id="in"></span><span id="IN"></span>**Окне**</span><span class="sxs-lookup"><span data-stu-id="4cf14-228"><span id="In"></span><span id="in"></span><span id="IN"></span>**In**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-229">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4cf14-229">Data type: **boolean**</span></span>

<span data-ttu-id="4cf14-230">Область применения: параметры</span><span class="sxs-lookup"><span data-stu-id="4cf14-230">Applies to: parameters</span></span>

<span data-ttu-id="4cf14-231">Указывает, используется ли параметр для передачи значений в метод.</span><span class="sxs-lookup"><span data-stu-id="4cf14-231">Indicates whether the parameter is used to pass values to a method.</span></span> <span data-ttu-id="4cf14-232">Значение по умолчанию — **true**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-232">The default is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-233"><span id="In__Out"></span><span id="in__out"></span><span id="IN__OUT"></span>**В, out**</span><span class="sxs-lookup"><span data-stu-id="4cf14-233"><span id="In__Out"></span><span id="in__out"></span><span id="IN__OUT"></span>**In, Out**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-234">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4cf14-234">Data type: **boolean**</span></span>

<span data-ttu-id="4cf14-235">Область применения: параметры</span><span class="sxs-lookup"><span data-stu-id="4cf14-235">Applies to: parameters</span></span>

<span data-ttu-id="4cf14-236">Указывает, является ли параметр входным и выходным.</span><span class="sxs-lookup"><span data-stu-id="4cf14-236">Indicates whether the parameter is both an input and output parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-237"><span id="Key"></span><span id="key"></span><span id="KEY"></span>[**Раздел**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="4cf14-237"><span id="Key"></span><span id="key"></span><span id="KEY"></span>[**Key**](key-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-238">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4cf14-238">Data type: **boolean**</span></span>

<span data-ttu-id="4cf14-239">Область применения: свойства, ссылки</span><span class="sxs-lookup"><span data-stu-id="4cf14-239">Applies to: properties, references</span></span>

<span data-ttu-id="4cf14-240">Указывает, является ли свойство частью обработчика пространства имен.</span><span class="sxs-lookup"><span data-stu-id="4cf14-240">Indicates whether the property is part of the namespace handle.</span></span> <span data-ttu-id="4cf14-241">Если квалификатор [**ключа**](key-qualifier.md) имеется в нескольких свойствах, то все эти свойства вместе формируют ключ (составной ключ).</span><span class="sxs-lookup"><span data-stu-id="4cf14-241">If more than one property has the [**Key**](key-qualifier.md) qualifier, then all such properties collectively form the key (a compound key).</span></span> <span data-ttu-id="4cf14-242">При совместном использовании ключевые свойства должны предоставлять уникальную ссылку на каждый экземпляр класса.</span><span class="sxs-lookup"><span data-stu-id="4cf14-242">When taken together, the key properties must supply a unique reference for each class instance.</span></span> <span data-ttu-id="4cf14-243">Если этот квалификатор размещается в свойстве, то допускается только значение **true** .</span><span class="sxs-lookup"><span data-stu-id="4cf14-243">If this qualifier is placed on a property, only the value **TRUE** is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-244"><span id="Lazy"></span><span id="lazy"></span><span id="LAZY"></span>**Явно**</span><span class="sxs-lookup"><span data-stu-id="4cf14-244"><span id="Lazy"></span><span id="lazy"></span><span id="LAZY"></span>**Lazy**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-245">Область применения: свойства</span><span class="sxs-lookup"><span data-stu-id="4cf14-245">Applies to: properties</span></span>

<span data-ttu-id="4cf14-246">Указывает, что свойство может возвращать ресурсы и требует большого количества процессорного времени и памяти.</span><span class="sxs-lookup"><span data-stu-id="4cf14-246">Indicates that the property is resource-intensive to return and requires a lot of processor time and memory.</span></span> <span data-ttu-id="4cf14-247">WMI повышает производительность запросов, не пытаясь вернуть свойства, помеченные квалификатором **Lazy** .</span><span class="sxs-lookup"><span data-stu-id="4cf14-247">WMI improves the performance of queries by not attempting to return the properties marked with the **Lazy** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-248"><span id="MappingStrings"></span><span id="mappingstrings"></span><span id="MAPPINGSTRINGS"></span>**маппингстрингс**</span><span class="sxs-lookup"><span data-stu-id="4cf14-248"><span id="MappingStrings"></span><span id="mappingstrings"></span><span id="MAPPINGSTRINGS"></span>**MappingStrings**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-249">Тип данных: **массив строк**</span><span class="sxs-lookup"><span data-stu-id="4cf14-249">Data type: **string array**</span></span>

<span data-ttu-id="4cf14-250">Область применения: классы, свойства, ассоциации, указания, ссылки</span><span class="sxs-lookup"><span data-stu-id="4cf14-250">Applies to: classes, properties, associations, indications, references</span></span>

<span data-ttu-id="4cf14-251">Набор значений, указывающий путь к расположению, где можно найти дополнительные сведения о происхождении свойства, класса, ассоциации, указания или ссылки.</span><span class="sxs-lookup"><span data-stu-id="4cf14-251">Set of values that indicate a path to a location where you can find more information about the origin of a property, class, association, indication, or reference.</span></span> <span data-ttu-id="4cf14-252">Строка сопоставления может быть путем к каталогу, URL-адресом, ключом реестра, включаемым файлом, ссылкой на класс CIM или другим форматом.</span><span class="sxs-lookup"><span data-stu-id="4cf14-252">The mapping string can be a directory path, a URL, a registry key, an include file, reference to a CIM class, or some other format.</span></span> <span data-ttu-id="4cf14-253">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-253">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-254"><span id="Max"></span><span id="max"></span><span id="MAX"></span>**Максимальной**</span><span class="sxs-lookup"><span data-stu-id="4cf14-254"><span id="Max"></span><span id="max"></span><span id="MAX"></span>**Max**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-255">Тип данных: **int**</span><span class="sxs-lookup"><span data-stu-id="4cf14-255">Data type: **int**</span></span>

<span data-ttu-id="4cf14-256">Область применения: ссылки</span><span class="sxs-lookup"><span data-stu-id="4cf14-256">Applies to: references</span></span>

<span data-ttu-id="4cf14-257">Максимальное число значений, которое может иметь данная ссылка для каждого набора других ссылочных значений в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="4cf14-257">Maximum number of values a given reference can have for each set of other reference values in the association.</span></span> <span data-ttu-id="4cf14-258">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-258">The default is **NULL**.</span></span> <span data-ttu-id="4cf14-259">Например, если Ассоциация связывает экземпляры с экземплярами B и в каждом экземпляре B должно быть не более одного экземпляра, то ссылка на объект должен иметь максимум один квалификатор.</span><span class="sxs-lookup"><span data-stu-id="4cf14-259">For example, if an association relates A instances to B instances and there must be at most one A instance for each B instance, then the reference to A should have a maximum of one qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-260"><span id="MaxLen"></span><span id="maxlen"></span><span id="MAXLEN"></span>**MaxLen**</span><span class="sxs-lookup"><span data-stu-id="4cf14-260"><span id="MaxLen"></span><span id="maxlen"></span><span id="MAXLEN"></span>**MaxLen**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-261">Тип данных: **int**</span><span class="sxs-lookup"><span data-stu-id="4cf14-261">Data type: **int**</span></span>

<span data-ttu-id="4cf14-262">Область применения: свойства, методы, параметры</span><span class="sxs-lookup"><span data-stu-id="4cf14-262">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="4cf14-263">Максимальная длина **строкового** элемента данных (в символах) и указание поддержки массивов фиксированной длины.</span><span class="sxs-lookup"><span data-stu-id="4cf14-263">Maximum length (in characters) of a **string** data item and indicates support of fixed-length arrays.</span></span>

<span data-ttu-id="4cf14-264">Если обнаружен массив фиксированной длины, квалификатор **maxlen** содержит фиксированную длину, найденную во время синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="4cf14-264">If a fixed-length array is encountered, the **MaxLen** qualifier contains the fixed length found during parsing.</span></span> <span data-ttu-id="4cf14-265">При обнаружении массива переменной длины этот квалификатор не используется.</span><span class="sxs-lookup"><span data-stu-id="4cf14-265">If a variable-length array is encountered, then this qualifier is not used.</span></span> <span data-ttu-id="4cf14-266">**Maxlen** используется для предложения максимального количества элементов, которые должны храниться в массиве.</span><span class="sxs-lookup"><span data-stu-id="4cf14-266">**MaxLen** is used to suggest the maximum number of elements that should be stored in an array.</span></span> <span data-ttu-id="4cf14-267">При переопределении значения по умолчанию можно указать любое целочисленное значение без знака (**UInt32**).</span><span class="sxs-lookup"><span data-stu-id="4cf14-267">When overriding the default value, any unsigned integer value (**uint32**) can be specified.</span></span> <span data-ttu-id="4cf14-268">Значение **null** (по умолчанию) подразумевает неограниченную длину.</span><span class="sxs-lookup"><span data-stu-id="4cf14-268">A value of **NULL** (default) implies unlimited length.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-269"><span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>**MaxValue**</span><span class="sxs-lookup"><span data-stu-id="4cf14-269"><span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>**MaxValue**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-270">Тип данных: **int**</span><span class="sxs-lookup"><span data-stu-id="4cf14-270">Data type: **int**</span></span>

<span data-ttu-id="4cf14-271">Область применения: свойства, методы, параметры</span><span class="sxs-lookup"><span data-stu-id="4cf14-271">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="4cf14-272">Максимальное значение объекта.</span><span class="sxs-lookup"><span data-stu-id="4cf14-272">Maximum value of the object.</span></span> <span data-ttu-id="4cf14-273">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-273">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-274"><span id="Min"></span><span id="min"></span><span id="MIN"></span>**Минимум**</span><span class="sxs-lookup"><span data-stu-id="4cf14-274"><span id="Min"></span><span id="min"></span><span id="MIN"></span>**Min**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-275">Тип данных: **int**</span><span class="sxs-lookup"><span data-stu-id="4cf14-275">Data type: **int**</span></span>

<span data-ttu-id="4cf14-276">Область применения: ссылки</span><span class="sxs-lookup"><span data-stu-id="4cf14-276">Applies to: references</span></span>

<span data-ttu-id="4cf14-277">Минимальное количество элементов ссылки (минимальное число значений, которое может иметь данная ссылка для каждого набора других ссылочных значений в ассоциации).</span><span class="sxs-lookup"><span data-stu-id="4cf14-277">Minimum cardinality of the reference (the minimum number of values a given reference can have for each set of other reference values in the association).</span></span> <span data-ttu-id="4cf14-278">Значение по умолчанию равно 0.</span><span class="sxs-lookup"><span data-stu-id="4cf14-278">The default is 0.</span></span>

<span data-ttu-id="4cf14-279">Например, если Ассоциация связывает экземпляры с экземплярами B, и для каждого экземпляра B должен существовать хотя бы один экземпляр, то ссылка на объект должен иметь минимум один квалификатор.</span><span class="sxs-lookup"><span data-stu-id="4cf14-279">For example, if an association relates A instances to B instances, and there must be at least one A instance for each B instance, then the reference to A should have a minimum of one qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-280"><span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>**MinValue**</span><span class="sxs-lookup"><span data-stu-id="4cf14-280"><span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>**MinValue**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-281">Тип данных: **int**</span><span class="sxs-lookup"><span data-stu-id="4cf14-281">Data type: **int**</span></span>

<span data-ttu-id="4cf14-282">Область применения: свойства, методы, параметры</span><span class="sxs-lookup"><span data-stu-id="4cf14-282">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="4cf14-283">Указывает минимальное значение объекта.</span><span class="sxs-lookup"><span data-stu-id="4cf14-283">Indicates the minimum value of the object.</span></span> <span data-ttu-id="4cf14-284">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-284">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-285"><span id="ModelCorrespondence"></span><span id="modelcorrespondence"></span><span id="MODELCORRESPONDENCE"></span>**моделкорреспонденце**</span><span class="sxs-lookup"><span data-stu-id="4cf14-285"><span id="ModelCorrespondence"></span><span id="modelcorrespondence"></span><span id="MODELCORRESPONDENCE"></span>**ModelCorrespondence**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-286">Тип данных: **массив строк**</span><span class="sxs-lookup"><span data-stu-id="4cf14-286">Data type: **string array**</span></span>

<span data-ttu-id="4cf14-287">Область применения: свойства</span><span class="sxs-lookup"><span data-stu-id="4cf14-287">Applies to: properties</span></span>

<span data-ttu-id="4cf14-288">Набор значений, указывающих на соответствие свойству объекта и другим свойствам в схеме CIM.</span><span class="sxs-lookup"><span data-stu-id="4cf14-288">Set of values that indicate correspondence between an object's property and other properties in the CIM schema.</span></span> <span data-ttu-id="4cf14-289">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-289">The default is **NULL**.</span></span>

<span data-ttu-id="4cf14-290">Свойства объекта определяются с помощью следующего синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="4cf14-290">Object properties are identified using the following syntax.</span></span>

<span data-ttu-id="4cf14-291"><schema name> "\_" <class or association name> "." <property name></span><span class="sxs-lookup"><span data-stu-id="4cf14-291"><schema name> "\_" <class or association name> "." <property name></span></span>

</dd> <dt>

<span data-ttu-id="4cf14-292"><span id="Nonlocal"></span><span id="nonlocal"></span><span id="NONLOCAL"></span>**Нелокальное**</span><span class="sxs-lookup"><span data-stu-id="4cf14-292"><span id="Nonlocal"></span><span id="nonlocal"></span><span id="NONLOCAL"></span>**Nonlocal**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-293">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4cf14-293">Data type: **string**</span></span>

<span data-ttu-id="4cf14-294">Область применения: ссылки</span><span class="sxs-lookup"><span data-stu-id="4cf14-294">Applies to: references</span></span>

<span data-ttu-id="4cf14-295">Расположение экземпляра, значение которого <*намеспацетипе*>://<*намеспацехандле*> значение по умолчанию равно **null**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-295">Location of an instance, the value of which is <*namespacetype*>://<*namespacehandle*> The default is **NULL**.</span></span>

<span data-ttu-id="4cf14-296">Использование: этот квалификатор нельзя использовать с квалификатором **нонлокалтипе** .</span><span class="sxs-lookup"><span data-stu-id="4cf14-296">Usage: This qualifier cannot be used with the **NonlocalType** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-297"><span id="NonlocalType"></span><span id="nonlocaltype"></span><span id="NONLOCALTYPE"></span>**нонлокалтипе**</span><span class="sxs-lookup"><span data-stu-id="4cf14-297"><span id="NonlocalType"></span><span id="nonlocaltype"></span><span id="NONLOCALTYPE"></span>**NonlocalType**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-298">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4cf14-298">Data type: **string**</span></span>

<span data-ttu-id="4cf14-299">Область применения: ссылки</span><span class="sxs-lookup"><span data-stu-id="4cf14-299">Applies to: references</span></span>

<span data-ttu-id="4cf14-300">Тип расположения экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4cf14-300">Type of location of an instance.</span></span> <span data-ttu-id="4cf14-301">Его значение — <namespacetype> .</span><span class="sxs-lookup"><span data-stu-id="4cf14-301">Its value is <namespacetype>.</span></span> <span data-ttu-id="4cf14-302">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-302">The default is **NULL**.</span></span>

<span data-ttu-id="4cf14-303">Использование: этот квалификатор не может использоваться с **нелокальным** квалификатором.</span><span class="sxs-lookup"><span data-stu-id="4cf14-303">Usage: This qualifier cannot be used with the **Nonlocal** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-304"><span id="NullValue"></span><span id="nullvalue"></span><span id="NULLVALUE"></span>**NullValue**</span><span class="sxs-lookup"><span data-stu-id="4cf14-304"><span id="NullValue"></span><span id="nullvalue"></span><span id="NULLVALUE"></span>**NullValue**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-305">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4cf14-305">Data type: **string**</span></span>

<span data-ttu-id="4cf14-306">Область применения: свойства</span><span class="sxs-lookup"><span data-stu-id="4cf14-306">Applies to: properties</span></span>

<span data-ttu-id="4cf14-307">Значение, указывающее, что связанное свойство имеет значение **null** (свойство не имеет допустимого или осмысленного значения).</span><span class="sxs-lookup"><span data-stu-id="4cf14-307">Value that indicates that the associated property is **NULL** (the property does not have a valid or meaningful value).</span></span> <span data-ttu-id="4cf14-308">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-308">The default is **NULL**.</span></span>

<span data-ttu-id="4cf14-309">Правила и ограничения, используемые для определения значений **null** , совпадают с соглашениями, применимыми к квалификатору **ValueMap** .</span><span class="sxs-lookup"><span data-stu-id="4cf14-309">The conventions and restrictions used for defining **NULL** values are the same as those applicable to the **ValueMap** qualifier.</span></span> <span data-ttu-id="4cf14-310">Обратите внимание, что квалификатор не может быть переопределен.</span><span class="sxs-lookup"><span data-stu-id="4cf14-310">Note this qualifier cannot be overridden.</span></span> <span data-ttu-id="4cf14-311">Неоправданно разрешите подклассу возвращать другое значение **null** по сравнению с родительским классом.</span><span class="sxs-lookup"><span data-stu-id="4cf14-311">It is unreasonable to permit a subclass to return a different **NULL** value than that of the parent class.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-312"><span id="Out"></span><span id="out"></span><span id="OUT"></span>**Заполняет**</span><span class="sxs-lookup"><span data-stu-id="4cf14-312"><span id="Out"></span><span id="out"></span><span id="OUT"></span>**Out**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-313">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4cf14-313">Data type: **boolean**</span></span>

<span data-ttu-id="4cf14-314">Область применения: параметры</span><span class="sxs-lookup"><span data-stu-id="4cf14-314">Applies to: parameters</span></span>

<span data-ttu-id="4cf14-315">Указывает, возвращает ли параметр значения из метода.</span><span class="sxs-lookup"><span data-stu-id="4cf14-315">Indicates whether the parameter returns values from a method.</span></span> <span data-ttu-id="4cf14-316">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-316">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-317"><span id="Override"></span><span id="override"></span><span id="OVERRIDE"></span>**Крывают**</span><span class="sxs-lookup"><span data-stu-id="4cf14-317"><span id="Override"></span><span id="override"></span><span id="OVERRIDE"></span>**Override**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-318">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4cf14-318">Data type: **string**</span></span>

<span data-ttu-id="4cf14-319">Область применения: свойства, методы, ссылки</span><span class="sxs-lookup"><span data-stu-id="4cf14-319">Applies to: properties, methods, references</span></span>

<span data-ttu-id="4cf14-320">Родительский класс или подчиненная конструкция (свойство, метод или ссылка), переопределяемая свойством, методом или ссылкой на то же имя в производном классе.</span><span class="sxs-lookup"><span data-stu-id="4cf14-320">Parent class or subordinate construct (property, method, or reference) which is overridden by the property, method, or reference of the same name in the derived class.</span></span> <span data-ttu-id="4cf14-321">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-321">The default is **NULL**.</span></span>

<span data-ttu-id="4cf14-322">Формат будет следующим:</span><span class="sxs-lookup"><span data-stu-id="4cf14-322">The format is:</span></span>

<span data-ttu-id="4cf14-323">\[<> *класса* . \] < *подчиненная конструкция*></span><span class="sxs-lookup"><span data-stu-id="4cf14-323">\[<*class*>.\]<*subordinate construct*></span></span>

<span data-ttu-id="4cf14-324">Если имя класса пропущено, переопределение применяется к подчиненной конструкции в родительском классе в иерархии классов.</span><span class="sxs-lookup"><span data-stu-id="4cf14-324">If the class name is omitted, the override applies to the subordinate construct in the parent class in the class hierarchy.</span></span>

<span data-ttu-id="4cf14-325">Использование. квалификатор **переопределения** может ссылаться только на конструкции, основанные только на той же мета модели.</span><span class="sxs-lookup"><span data-stu-id="4cf14-325">Usage: The **Override** qualifier can refer to constructs based on the same meta model only.</span></span> <span data-ttu-id="4cf14-326">Не допускается изменение имени или подписи конструкции во время операции переопределения.</span><span class="sxs-lookup"><span data-stu-id="4cf14-326">It is not allowed to change a construct name or signature during an override operation.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-327"><span id="OverrideValue"></span><span id="overridevalue"></span><span id="OVERRIDEVALUE"></span>**оверридевалуе**</span><span class="sxs-lookup"><span data-stu-id="4cf14-327"><span id="OverrideValue"></span><span id="overridevalue"></span><span id="OVERRIDEVALUE"></span>**OverrideValue**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-328">Область применения: классы</span><span class="sxs-lookup"><span data-stu-id="4cf14-328">Applies to: classes</span></span>

<span data-ttu-id="4cf14-329">Указывает, переопределяет ли значение свойства подкласса значение в родительском классе.</span><span class="sxs-lookup"><span data-stu-id="4cf14-329">Indicates whether the property value on a subclass overrides the value in a parent class.</span></span> <span data-ttu-id="4cf14-330">Функциональное приведение заключается в том, что при выполнении запроса к родительскому классу и если предложение **WHERE** включает это свойство, родительский элемент должен возвращать экземпляр с переопределенным значением.</span><span class="sxs-lookup"><span data-stu-id="4cf14-330">The functional implication is that, if you perform a query against the parent class, and if your **WHERE** clause includes this property, the parent must return an instance with the overridden value.</span></span> <span data-ttu-id="4cf14-331">В результате система управления Windows настраивает предложение **WHERE** запроса, отправляемого в родительский класс, чтобы исключить ссылки на это свойство.</span><span class="sxs-lookup"><span data-stu-id="4cf14-331">As a result, Windows Management adjusts the **WHERE** clause of the query sent to the parent class to exclude references to this property.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-332"><span id="Propagated"></span><span id="propagated"></span><span id="PROPAGATED"></span>**Распространяются**</span><span class="sxs-lookup"><span data-stu-id="4cf14-332"><span id="Propagated"></span><span id="propagated"></span><span id="PROPAGATED"></span>**Propagated**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-333">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4cf14-333">Data type: **string**</span></span>

<span data-ttu-id="4cf14-334">Область применения: свойства</span><span class="sxs-lookup"><span data-stu-id="4cf14-334">Applies to: properties</span></span>

<span data-ttu-id="4cf14-335">Имя распространяемого ключа.</span><span class="sxs-lookup"><span data-stu-id="4cf14-335">Name of the key being propagated.</span></span> <span data-ttu-id="4cf14-336">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-336">The default is **NULL**.</span></span>

<span data-ttu-id="4cf14-337">Использование этого квалификатора предполагает наличие только одного слабого квалификатора в ссылке, где содержащий класс является целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="4cf14-337">Use of this qualifier assumes the existence of only one weak qualifier on a reference that has the containing class as its target.</span></span> <span data-ttu-id="4cf14-338">Связанное свойство должно иметь то же значение, что и свойство, именуемое квалификатором в классе на другой стороне слабой ассоциации.</span><span class="sxs-lookup"><span data-stu-id="4cf14-338">The associated property must have the same value as the property named by the qualifier in the class on the other side of the weak association.</span></span> <span data-ttu-id="4cf14-339">Формат будет следующим:</span><span class="sxs-lookup"><span data-stu-id="4cf14-339">The format is:</span></span>

<span data-ttu-id="4cf14-340">\[<> *класса* . \] < *подчиненная конструкция*></span><span class="sxs-lookup"><span data-stu-id="4cf14-340">\[<*class*>.\]<*subordinate construct*></span></span>

<span data-ttu-id="4cf14-341">Использование: Если используется **распространенный** квалификатор, необходимо указать квалификатор [**ключа**](key-qualifier.md) со значением **true**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-341">Usage: When the **Propagated** qualifier is used, the [**Key**](key-qualifier.md) qualifier must be specified with a value of **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-342"><span id="Read"></span><span id="read"></span><span id="READ"></span>**Просмотр**</span><span class="sxs-lookup"><span data-stu-id="4cf14-342"><span id="Read"></span><span id="read"></span><span id="READ"></span>**Read**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-343">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4cf14-343">Data type: **boolean**</span></span>

<span data-ttu-id="4cf14-344">Область применения: свойства</span><span class="sxs-lookup"><span data-stu-id="4cf14-344">Applies to: properties</span></span>

<span data-ttu-id="4cf14-345">Указывает, доступно ли свойство для чтения.</span><span class="sxs-lookup"><span data-stu-id="4cf14-345">Indicates whether the property is readable.</span></span> <span data-ttu-id="4cf14-346">Значение по умолчанию — **true**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-346">The default is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-347"><span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>**Обязательно**</span><span class="sxs-lookup"><span data-stu-id="4cf14-347"><span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>**Required**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-348">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4cf14-348">Data type: **boolean**</span></span>

<span data-ttu-id="4cf14-349">Область применения: свойства</span><span class="sxs-lookup"><span data-stu-id="4cf14-349">Applies to: properties</span></span>

<span data-ttu-id="4cf14-350">Указывает, требуется ли для свойства значение, отличное от NULL.</span><span class="sxs-lookup"><span data-stu-id="4cf14-350">Indicates whether a non-null value is required for the property.</span></span> <span data-ttu-id="4cf14-351">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-351">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-352"><span id="Revision"></span><span id="revision"></span><span id="REVISION"></span>**Редакции**</span><span class="sxs-lookup"><span data-stu-id="4cf14-352"><span id="Revision"></span><span id="revision"></span><span id="REVISION"></span>**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-353">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4cf14-353">Data type: **string**</span></span>

<span data-ttu-id="4cf14-354">Область применения: классы, ассоциации, указания, схемы</span><span class="sxs-lookup"><span data-stu-id="4cf14-354">Applies to: classes, associations, indications, schemas</span></span>

<span data-ttu-id="4cf14-355">Дополнительный номер редакции объекта схемы.</span><span class="sxs-lookup"><span data-stu-id="4cf14-355">Minor revision number of the schema object.</span></span> <span data-ttu-id="4cf14-356">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-356">The default is **NULL**.</span></span>

<span data-ttu-id="4cf14-357">Использование: квалификатор **версии** должен присутствовать, чтобы указать основной номер версии при использовании квалификатора **редакции** .</span><span class="sxs-lookup"><span data-stu-id="4cf14-357">Usage: The **Version** qualifier must be present to supply the major version number when the **Revision** qualifier is used.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-358"><span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>**Схемы**</span><span class="sxs-lookup"><span data-stu-id="4cf14-358"><span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>**Schema**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-359">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4cf14-359">Data type: **string**</span></span>

<span data-ttu-id="4cf14-360">Область применения: свойства, методы</span><span class="sxs-lookup"><span data-stu-id="4cf14-360">Applies to: properties, methods</span></span>

<span data-ttu-id="4cf14-361">Имя схемы, в которой определен компонент.</span><span class="sxs-lookup"><span data-stu-id="4cf14-361">Name of the schema in which the feature is defined.</span></span> <span data-ttu-id="4cf14-362">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-362">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-363"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>**Источника**</span><span class="sxs-lookup"><span data-stu-id="4cf14-363"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>**Source**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-364">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4cf14-364">Data type: **string**</span></span>

<span data-ttu-id="4cf14-365">Область применения: классы, ассоциации, указания, ссылки</span><span class="sxs-lookup"><span data-stu-id="4cf14-365">Applies to: classes, associations, indications, references</span></span>

<span data-ttu-id="4cf14-366">Расположение экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4cf14-366">Location of an instance.</span></span> <span data-ttu-id="4cf14-367">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-367">The default is **NULL**.</span></span>

<span data-ttu-id="4cf14-368">Значение квалификатора — <*намеспацетипе*>://<*намеспацехандле*>.</span><span class="sxs-lookup"><span data-stu-id="4cf14-368">The qualifier's value is <*namespacetype*>://<*namespacehandle*>.</span></span>

<span data-ttu-id="4cf14-369">Использование: квалификатор **источника** не может использоваться с квалификатором **sourceType** .</span><span class="sxs-lookup"><span data-stu-id="4cf14-369">Usage: The **Source** qualifier cannot be used with the **SourceType** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-370"><span id="SourceType"></span><span id="sourcetype"></span><span id="SOURCETYPE"></span>**SourceType**</span><span class="sxs-lookup"><span data-stu-id="4cf14-370"><span id="SourceType"></span><span id="sourcetype"></span><span id="SOURCETYPE"></span>**SourceType**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-371">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4cf14-371">Data type: **string**</span></span>

<span data-ttu-id="4cf14-372">Область применения: классы, ассоциации, указания, ссылки</span><span class="sxs-lookup"><span data-stu-id="4cf14-372">Applies to: classes, associations, indications, references</span></span>

<span data-ttu-id="4cf14-373">Тип расположения экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4cf14-373">Type of location of an instance.</span></span> <span data-ttu-id="4cf14-374">Значение этого квалификатора — <*намеспацетипе*>.</span><span class="sxs-lookup"><span data-stu-id="4cf14-374">The value of this qualifier is <*namespacetype*>.</span></span> <span data-ttu-id="4cf14-375">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-375">The default is **NULL**.</span></span>

<span data-ttu-id="4cf14-376">Использование: квалификатор **sourceType** не может использоваться с квалификатором **источника** .</span><span class="sxs-lookup"><span data-stu-id="4cf14-376">Usage: The **SourceType** qualifier cannot be used with the **Source** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-377"><span id="SupportsCreate"></span><span id="supportscreate"></span><span id="SUPPORTSCREATE"></span>**суппортскреате**</span><span class="sxs-lookup"><span data-stu-id="4cf14-377"><span id="SupportsCreate"></span><span id="supportscreate"></span><span id="SUPPORTSCREATE"></span>**SupportsCreate**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-378">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4cf14-378">Data type: **boolean**</span></span>

<span data-ttu-id="4cf14-379">Область применения: классы</span><span class="sxs-lookup"><span data-stu-id="4cf14-379">Applies to: classes</span></span>

<span data-ttu-id="4cf14-380">Указывает, поддерживает ли класс создание экземпляров.</span><span class="sxs-lookup"><span data-stu-id="4cf14-380">Indicates whether the class supports the creation of instances.</span></span> <span data-ttu-id="4cf14-381">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-381">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-382"><span id="SupportsDelete"></span><span id="supportsdelete"></span><span id="SUPPORTSDELETE"></span>**суппортсделете**</span><span class="sxs-lookup"><span data-stu-id="4cf14-382"><span id="SupportsDelete"></span><span id="supportsdelete"></span><span id="SUPPORTSDELETE"></span>**SupportsDelete**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-383">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4cf14-383">Data type: **boolean**</span></span>

<span data-ttu-id="4cf14-384">Область применения: классы</span><span class="sxs-lookup"><span data-stu-id="4cf14-384">Applies to: classes</span></span>

<span data-ttu-id="4cf14-385">Указывает, поддерживает ли класс удаление экземпляров.</span><span class="sxs-lookup"><span data-stu-id="4cf14-385">Indicates whether the class supports the deletion of instances.</span></span> <span data-ttu-id="4cf14-386">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-386">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-387"><span id="SupportsUpdate"></span><span id="supportsupdate"></span><span id="SUPPORTSUPDATE"></span>**суппортсупдате**</span><span class="sxs-lookup"><span data-stu-id="4cf14-387"><span id="SupportsUpdate"></span><span id="supportsupdate"></span><span id="SUPPORTSUPDATE"></span>**SupportsUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-388">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4cf14-388">Data type: **boolean**</span></span>

<span data-ttu-id="4cf14-389">Область применения: классы</span><span class="sxs-lookup"><span data-stu-id="4cf14-389">Applies to: classes</span></span>

<span data-ttu-id="4cf14-390">Указывает, поддерживает ли класс изменение (обновление) экземпляров.</span><span class="sxs-lookup"><span data-stu-id="4cf14-390">Indicates whether the class supports the modification (updating) of instances.</span></span> <span data-ttu-id="4cf14-391">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-391">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-392"><span id="Terminal"></span><span id="terminal"></span><span id="TERMINAL"></span>**Терминалов**</span><span class="sxs-lookup"><span data-stu-id="4cf14-392"><span id="Terminal"></span><span id="terminal"></span><span id="TERMINAL"></span>**Terminal**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-393">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4cf14-393">Data type: **boolean**</span></span>

<span data-ttu-id="4cf14-394">Область применения: классы</span><span class="sxs-lookup"><span data-stu-id="4cf14-394">Applies to: classes</span></span>

<span data-ttu-id="4cf14-395">Указывает, может ли класс содержать подклассы.</span><span class="sxs-lookup"><span data-stu-id="4cf14-395">Indicates whether the class can have subclasses.</span></span> <span data-ttu-id="4cf14-396">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-396">The default is **FALSE**.</span></span>

<span data-ttu-id="4cf14-397">Если подкласс объявлен, компилятор выдает ошибку.</span><span class="sxs-lookup"><span data-stu-id="4cf14-397">If a subclass is declared, the compiler generates an error.</span></span>

<span data-ttu-id="4cf14-398">Использование: этот квалификатор не может сосуществовать с **абстрактным** квалификатором.</span><span class="sxs-lookup"><span data-stu-id="4cf14-398">Usage: This qualifier cannot coexist with the **Abstract** qualifier.</span></span> <span data-ttu-id="4cf14-399">Если указаны как **терминал** , так и **абстрактные** квалификаторы, компилятор выдает ошибку.</span><span class="sxs-lookup"><span data-stu-id="4cf14-399">If both the **Terminal** and **Abstract** qualifiers are specified, the compiler generates an error.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-400"><span id="Units"></span><span id="units"></span><span id="UNITS"></span>**Комплект**</span><span class="sxs-lookup"><span data-stu-id="4cf14-400"><span id="Units"></span><span id="units"></span><span id="UNITS"></span>**Units**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-401">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4cf14-401">Data type: **string**</span></span>

<span data-ttu-id="4cf14-402">Область применения: свойства, методы, параметры</span><span class="sxs-lookup"><span data-stu-id="4cf14-402">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="4cf14-403">Тип единицы измерения, в которой выражается связанный элемент данных.</span><span class="sxs-lookup"><span data-stu-id="4cf14-403">Type of unit in which the associated data item is expressed.</span></span> <span data-ttu-id="4cf14-404">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-404">The default is **NULL**.</span></span>

<span data-ttu-id="4cf14-405">Например, элемент данных размера может иметь значение "байт" для **единиц**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-405">For example, a size data item might have a value of "bytes" for **Units**.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-406"><span id="ValueMap"></span><span id="valuemap"></span><span id="VALUEMAP"></span>**ValueMap**</span><span class="sxs-lookup"><span data-stu-id="4cf14-406"><span id="ValueMap"></span><span id="valuemap"></span><span id="VALUEMAP"></span>**ValueMap**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-407">Тип данных: **массив строк**</span><span class="sxs-lookup"><span data-stu-id="4cf14-407">Data type: **string array**</span></span>

<span data-ttu-id="4cf14-408">Область применения: свойства, методы, параметры</span><span class="sxs-lookup"><span data-stu-id="4cf14-408">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="4cf14-409">Набор допустимых значений для свойства, типа возвращаемого значения метода или параметра метода.</span><span class="sxs-lookup"><span data-stu-id="4cf14-409">Set of permissible values for a property, method return type, or method parameter.</span></span> <span data-ttu-id="4cf14-410">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-410">The default is **NULL**.</span></span>

<span data-ttu-id="4cf14-411">Использование. Этот квалификатор можно использовать отдельно или в сочетании с квалификатором **Values** .</span><span class="sxs-lookup"><span data-stu-id="4cf14-411">Usage: This qualifier can be used alone or in combination with the **Values** qualifier.</span></span> <span data-ttu-id="4cf14-412">При использовании в сочетании с квалификатором **Values** расположение значения в массиве **ValueMap** предоставляет расположение соответствующей записи в массиве **Values** .</span><span class="sxs-lookup"><span data-stu-id="4cf14-412">When used in combination with the **Values** qualifier, the location of the value in the **ValueMap** array provides the location of the corresponding entry in the **Values** array.</span></span> <span data-ttu-id="4cf14-413">Используйте квалификатор **ValueMap** только со строковыми и целыми значениями.</span><span class="sxs-lookup"><span data-stu-id="4cf14-413">Use the **ValueMap** qualifier only with string and integer values.</span></span> <span data-ttu-id="4cf14-414">Синтаксис для представления целочисленного значения в массиве карт значений состоит из \[ + \| = \] цифр \[ \* \] .</span><span class="sxs-lookup"><span data-stu-id="4cf14-414">The syntax for representing an integer value in the value map array is \[+\|=\]digit\[\*digit\].</span></span> <span data-ttu-id="4cf14-415">Содержимое, максимальное число разрядов и представленное значение ограничено типом связанного свойства.</span><span class="sxs-lookup"><span data-stu-id="4cf14-415">The content, maximum number of digits, and represented value are constrained by the type of the associated property.</span></span> <span data-ttu-id="4cf14-416">Например, значение Uint8 не может быть подписано, должно быть меньше четырех цифр и должно представлять меньше 256.</span><span class="sxs-lookup"><span data-stu-id="4cf14-416">For example, uint8 may not be signed, must be less than four digits, and must represent a value less than 256.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-417"><span id="Values"></span><span id="values"></span><span id="VALUES"></span>**Данные**</span><span class="sxs-lookup"><span data-stu-id="4cf14-417"><span id="Values"></span><span id="values"></span><span id="VALUES"></span>**Values**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-418">Тип данных: **массив строк**</span><span class="sxs-lookup"><span data-stu-id="4cf14-418">Data type: **string array**</span></span>

<span data-ttu-id="4cf14-419">Область применения: свойства, методы, параметры</span><span class="sxs-lookup"><span data-stu-id="4cf14-419">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="4cf14-420">Набор значений, преобразуя целочисленное значение в связанную строку.</span><span class="sxs-lookup"><span data-stu-id="4cf14-420">Set of values translating an integer value into an associated string.</span></span> <span data-ttu-id="4cf14-421">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-421">The default is **NULL**.</span></span>

<span data-ttu-id="4cf14-422">Это свойство также указывает массив строковых значений, которые должны быть сопоставлены со свойством перечисления.</span><span class="sxs-lookup"><span data-stu-id="4cf14-422">This property also specifies an array of string values to be mapped to an enumeration property.</span></span> <span data-ttu-id="4cf14-423">Этот квалификатор можно применить либо к целочисленному свойству, либо к строковому свойству, и сопоставление может быть неявным или явным.</span><span class="sxs-lookup"><span data-stu-id="4cf14-423">This qualifier can be applied to either an integer property or a string property, and the mapping can be implicit or explicit.</span></span> <span data-ttu-id="4cf14-424">Если сопоставление является неявным, значения целочисленного или строкового свойства представляют порядковые позиции в массиве **Values** .</span><span class="sxs-lookup"><span data-stu-id="4cf14-424">If the mapping is implicit, integer or string property values represent ordinal positions in the **Values** array.</span></span> <span data-ttu-id="4cf14-425">Если сопоставление является явным, свойство должно быть целым числом, а значения допустимых свойств перечислены в массиве, определенном квалификатором **ValueMap** .</span><span class="sxs-lookup"><span data-stu-id="4cf14-425">If the mapping is explicit, the property must be an integer, and valid property values are listed in the array defined by the **ValueMap** qualifier.</span></span> <span data-ttu-id="4cf14-426">Дополнительные сведения см. в разделе [значение Map](value-map.md).</span><span class="sxs-lookup"><span data-stu-id="4cf14-426">For more information, see [Value Map](value-map.md).</span></span>

<span data-ttu-id="4cf14-427">Если квалификатор **ValueMap** отсутствует, массив **Values** индексируется (относительный от нуля), используя значение в связанном свойстве, типе возвращаемого значения метода или параметре метода.</span><span class="sxs-lookup"><span data-stu-id="4cf14-427">If a **ValueMap** qualifier is not present, the **Values** array is indexed (zero-relative) by using the value in the associated property, method return type, or method parameter.</span></span> <span data-ttu-id="4cf14-428">Если указан квалификатор **ValueMap** , то индекс значений определяется расположением значения свойства в сопоставлении значений.</span><span class="sxs-lookup"><span data-stu-id="4cf14-428">If a **ValueMap** qualifier is present, the values index is defined by the location of the property value in the value map.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-429"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Версия**</span><span class="sxs-lookup"><span data-stu-id="4cf14-429"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-430">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4cf14-430">Data type: **string**</span></span>

<span data-ttu-id="4cf14-431">Область применения: классы, схемы, ассоциации, указания</span><span class="sxs-lookup"><span data-stu-id="4cf14-431">Applies to: classes, schemas, associations, indications</span></span>

<span data-ttu-id="4cf14-432">Основной номер версии объекта схемы.</span><span class="sxs-lookup"><span data-stu-id="4cf14-432">Major version number of the schema object.</span></span> <span data-ttu-id="4cf14-433">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-433">The default is **NULL**.</span></span> <span data-ttu-id="4cf14-434">Номер версии увеличивается при внесении изменений в схему, которая изменяет интерфейс.</span><span class="sxs-lookup"><span data-stu-id="4cf14-434">The version number is incremented when changes are made to the schema that alter the interface.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-435"><span id="Weak"></span><span id="weak"></span><span id="WEAK"></span>**Безопасные**</span><span class="sxs-lookup"><span data-stu-id="4cf14-435"><span id="Weak"></span><span id="weak"></span><span id="WEAK"></span>**Weak**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-436">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4cf14-436">Data type: **boolean**</span></span>

<span data-ttu-id="4cf14-437">Область применения: ссылки</span><span class="sxs-lookup"><span data-stu-id="4cf14-437">Applies to: references</span></span>

<span data-ttu-id="4cf14-438">Указывает, включают ли ключи упоминаемого класса ключи других участников ассоциации.</span><span class="sxs-lookup"><span data-stu-id="4cf14-438">Indicates whether the keys of the referenced class include the keys of the other participants in the association.</span></span> <span data-ttu-id="4cf14-439">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-439">The default is **FALSE**.</span></span>

<span data-ttu-id="4cf14-440">Этот квалификатор используется, когда удостоверение упоминаемого класса зависит от удостоверения других участников ассоциации.</span><span class="sxs-lookup"><span data-stu-id="4cf14-440">This qualifier is used when the identity of the referenced class depends on the identity of the other participants in the association.</span></span> <span data-ttu-id="4cf14-441">Ни одна ссылка на любой заданный класс может быть ненадежной.</span><span class="sxs-lookup"><span data-stu-id="4cf14-441">No more than one reference to any given class can be weak.</span></span> <span data-ttu-id="4cf14-442">Другие классы в ассоциации должны определять ключ.</span><span class="sxs-lookup"><span data-stu-id="4cf14-442">The other classes in the association must define a key.</span></span> <span data-ttu-id="4cf14-443">Ключи других классов в ассоциации повторяются в упоминаемом классе и помечаются с помощью **распространяемого** квалификатора.</span><span class="sxs-lookup"><span data-stu-id="4cf14-443">The keys of the other classes in the association are repeated in the referenced class and are tagged with a **Propagated** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-444"><span id="Write"></span><span id="write"></span><span id="WRITE"></span>**Будет**</span><span class="sxs-lookup"><span data-stu-id="4cf14-444"><span id="Write"></span><span id="write"></span><span id="WRITE"></span>**Write**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-445">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4cf14-445">Data type: **boolean**</span></span>

<span data-ttu-id="4cf14-446">Область применения: свойства</span><span class="sxs-lookup"><span data-stu-id="4cf14-446">Applies to: properties</span></span>

<span data-ttu-id="4cf14-447">Указывает, что приложения или скрипты могут изменять значение свойства.</span><span class="sxs-lookup"><span data-stu-id="4cf14-447">Indicates that applications or scripts can change the property value.</span></span> <span data-ttu-id="4cf14-448">Учетная запись, которая запускает приложение, должна иметь доступ к пространству имен, содержащему экземпляры класса.</span><span class="sxs-lookup"><span data-stu-id="4cf14-448">The account that runs the application must have access to the namespace that contains instances of the class.</span></span> <span data-ttu-id="4cf14-449">Реализация поставщика может также ограничить доступ к данным поставщика.</span><span class="sxs-lookup"><span data-stu-id="4cf14-449">The provider implementation may also limit access to provider data.</span></span> <span data-ttu-id="4cf14-450">Значение **true** указывает, что свойство доступно для чтения и записи для потребителей, которым разрешен доступ к WMI и поставщику.</span><span class="sxs-lookup"><span data-stu-id="4cf14-450">A value of **TRUE** indicates that the property is readable and writeable by consumers that are allowed access by WMI and the provider.</span></span> <span data-ttu-id="4cf14-451">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-451">The default is **FALSE**.</span></span>

<span data-ttu-id="4cf14-452">Свойство, у которого нет квалификатора **записи** , может быть доступно для записи.</span><span class="sxs-lookup"><span data-stu-id="4cf14-452">A property that lacks the **Write** qualifier may still be writeable.</span></span> <span data-ttu-id="4cf14-453">Реализация поставщика может разрешить изменение любых свойств в классах поставщика, независимо от наличия квалификатора **записи** .</span><span class="sxs-lookup"><span data-stu-id="4cf14-453">The provider implementation may allow any properties in the provider classes to be changed, whether the **Write** qualifier is present.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-454"><span id="WriteAtCreate"></span><span id="writeatcreate"></span><span id="WRITEATCREATE"></span>**вритеаткреате**</span><span class="sxs-lookup"><span data-stu-id="4cf14-454"><span id="WriteAtCreate"></span><span id="writeatcreate"></span><span id="WRITEATCREATE"></span>**WriteAtCreate**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-455">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4cf14-455">Data type: **boolean**</span></span>

<span data-ttu-id="4cf14-456">Область применения: свойства</span><span class="sxs-lookup"><span data-stu-id="4cf14-456">Applies to: properties</span></span>

<span data-ttu-id="4cf14-457">Указывает, может ли свойство быть доступно для записи при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4cf14-457">Indicates whether the property is writeable at instance creation.</span></span> <span data-ttu-id="4cf14-458">Этот квалификатор можно использовать в сочетании с квалификатором **вритеаткреате** .</span><span class="sxs-lookup"><span data-stu-id="4cf14-458">This qualifier may be used in conjunction with the **WriteAtCreate** qualifier.</span></span> <span data-ttu-id="4cf14-459">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-459">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4cf14-460"><span id="WriteAtUpdate"></span><span id="writeatupdate"></span><span id="WRITEATUPDATE"></span>**вритеатупдате**</span><span class="sxs-lookup"><span data-stu-id="4cf14-460"><span id="WriteAtUpdate"></span><span id="writeatupdate"></span><span id="WRITEATUPDATE"></span>**WriteAtUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="4cf14-461">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4cf14-461">Data type: **boolean**</span></span>

<span data-ttu-id="4cf14-462">Область применения: свойства</span><span class="sxs-lookup"><span data-stu-id="4cf14-462">Applies to: properties</span></span>

<span data-ttu-id="4cf14-463">Указывает, может ли свойство быть доступно для записи при обновлении экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4cf14-463">Indicates whether the property is writeable at instance update.</span></span> <span data-ttu-id="4cf14-464">Этот квалификатор можно использовать в сочетании с квалификатором **вритеаткреате** .</span><span class="sxs-lookup"><span data-stu-id="4cf14-464">This qualifier may be used in conjunction with the **WriteAtCreate** qualifier.</span></span> <span data-ttu-id="4cf14-465">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="4cf14-465">The default is **FALSE**.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="4cf14-466">Примеры</span><span class="sxs-lookup"><span data-stu-id="4cf14-466">Examples</span></span>

<span data-ttu-id="4cf14-467">Дополнительные сведения о получении квалификаторов см. в примере кода PowerShell [Get-вмиклассмесодсандвритаблевмипропертиес](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) в коллекции TechNet.</span><span class="sxs-lookup"><span data-stu-id="4cf14-467">For more information on retrieving qualifiers, see the [Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) PowerShell code sample on the TechNet Gallery.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cf14-468">Требования</span><span class="sxs-lookup"><span data-stu-id="4cf14-468">Requirements</span></span>



| <span data-ttu-id="4cf14-469">Требование</span><span class="sxs-lookup"><span data-stu-id="4cf14-469">Requirement</span></span> | <span data-ttu-id="4cf14-470">Значение</span><span class="sxs-lookup"><span data-stu-id="4cf14-470">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="4cf14-471">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4cf14-471">Minimum supported client</span></span><br/> | <span data-ttu-id="4cf14-472">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4cf14-472">Windows Vista</span></span><br/>       |
| <span data-ttu-id="4cf14-473">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4cf14-473">Minimum supported server</span></span><br/> | <span data-ttu-id="4cf14-474">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4cf14-474">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4cf14-475">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4cf14-475">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cf14-476">Квалификаторы WMI</span><span class="sxs-lookup"><span data-stu-id="4cf14-476">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="4cf14-477">Добавление квалификатора</span><span class="sxs-lookup"><span data-stu-id="4cf14-477">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

 




