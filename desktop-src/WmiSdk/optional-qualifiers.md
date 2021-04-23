---
description: Необязательные квалификаторы позволяют устранить повторяющиеся ситуации, не являющиеся общими для всех реализаций, совместимых с CIM, которые не являются обязательными для интерпретации этих квалификаторов.
ms.assetid: f31162d1-25e6-494a-bc7d-f66955b514a6
ms.tgt_platform: multiple
title: Необязательные квалификаторы
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Optional
api_type:
- NA
api_location: ''
ms.openlocfilehash: 36fe1b9ceee1211a3b09ce70e03044b7af57eac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703115"
---
# <a name="optional-qualifiers"></a><span data-ttu-id="fda83-103">Необязательные квалификаторы</span><span class="sxs-lookup"><span data-stu-id="fda83-103">Optional Qualifiers</span></span>

<span data-ttu-id="fda83-104">Необязательные квалификаторы позволяют устранить повторяющиеся ситуации, не являющиеся общими для всех реализаций, совместимых с CIM, которые не являются обязательными для интерпретации этих квалификаторов.</span><span class="sxs-lookup"><span data-stu-id="fda83-104">Optional qualifiers address recurring situations not common to all CIM-compliant implementations, which are not required to interpret these qualifiers.</span></span> <span data-ttu-id="fda83-105">В спецификации указаны необязательные квалификаторы, позволяющие избежать случайных определяемых пользователем квалификаторов, которые могут возникнуть в этих повторяющихся ситуациях.</span><span class="sxs-lookup"><span data-stu-id="fda83-105">Optional qualifiers are provided in the specification to avoid random user-defined qualifiers that might occur in these recurring situations.</span></span>

<dt>

<span data-ttu-id="fda83-106"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Удален**</span><span class="sxs-lookup"><span data-stu-id="fda83-106"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Delete**</span></span>
</dt> <dd>

<span data-ttu-id="fda83-107">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="fda83-107">Data type: **boolean**</span></span>

<span data-ttu-id="fda83-108">Область применения: связи, ссылки</span><span class="sxs-lookup"><span data-stu-id="fda83-108">Applies to: associations, references</span></span>

<span data-ttu-id="fda83-109">Для ассоциаций указывает, следует ли удалять полную связь, если какой-либо из объектов, на которые ссылается ассоциация, удаляется, и если соответствующий объект, на который ссылается ассоциация, дополнен **ифделетед**.</span><span class="sxs-lookup"><span data-stu-id="fda83-109">For associations, indicates whether the qualified association must be deleted if any of the objects referenced in the association are deleted and if the respective object referenced in the association is qualified with **IfDeleted**.</span></span> <span data-ttu-id="fda83-110">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="fda83-110">The default is **FALSE**.</span></span>

<span data-ttu-id="fda83-111">Для ссылок этот квалификатор указывает, должен ли объект, на который указывает ссылка, удаляться, если ассоциация, содержащая ссылку, была удалена и дополнена с помощью **ифделетед** или если какие-либо из объектов, на которые ссылается ассоциация, дополнены **ифделетед**.</span><span class="sxs-lookup"><span data-stu-id="fda83-111">For references, this qualifier indicates whether the referenced object must be deleted if the association containing the reference is deleted and qualified with **IfDeleted**, or if any of the objects referenced in the association are deleted and the respective object referenced in the association is qualified with **IfDeleted**.</span></span>

<span data-ttu-id="fda83-112">Использование: приложения должны отмечать связи и ссылки, помеченные квалификатором **удаления** , и удалить связь или ссылку соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="fda83-112">Usage: Applications must track associations and references marked with the **Delete** qualifier and delete the association or reference appropriately.</span></span> <span data-ttu-id="fda83-113">Если объект в ассоциации удален, но не помечен с помощью **ифделетед**, связь не должна быть удалена.</span><span class="sxs-lookup"><span data-stu-id="fda83-113">If an object in the association has been deleted but is not marked with **IfDeleted**, then the association should not be deleted.</span></span>

<span data-ttu-id="fda83-114">Это правило использования должно быть проверено, если определена модель безопасности CIM.</span><span class="sxs-lookup"><span data-stu-id="fda83-114">This usage rule must be verified when the CIM security model is defined.</span></span>

</dd> <dt>

<span data-ttu-id="fda83-115"><span id="Expensive"></span><span id="expensive"></span><span id="EXPENSIVE"></span>**Дорогостоящ**</span><span class="sxs-lookup"><span data-stu-id="fda83-115"><span id="Expensive"></span><span id="expensive"></span><span id="EXPENSIVE"></span>**Expensive**</span></span>
</dt> <dd>

<span data-ttu-id="fda83-116">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="fda83-116">Data type: **boolean**</span></span>

<span data-ttu-id="fda83-117">Область применения: свойства, ссылки, классы, ассоциации, методы</span><span class="sxs-lookup"><span data-stu-id="fda83-117">Applies to: properties, references, classes, associations, methods</span></span>

<span data-ttu-id="fda83-118">Указывает, требует ли подразумеваемое действие расширенных вычислений.</span><span class="sxs-lookup"><span data-stu-id="fda83-118">Indicates whether the implied action requires extensive computation.</span></span> <span data-ttu-id="fda83-119">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="fda83-119">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="fda83-120"><span id="IfDeleted"></span><span id="ifdeleted"></span><span id="IFDELETED"></span>**ифделетед**</span><span class="sxs-lookup"><span data-stu-id="fda83-120"><span id="IfDeleted"></span><span id="ifdeleted"></span><span id="IFDELETED"></span>**IfDeleted**</span></span>
</dt> <dd>

<span data-ttu-id="fda83-121">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="fda83-121">Data type: **boolean**</span></span>

<span data-ttu-id="fda83-122">Область применения: связи и ссылки</span><span class="sxs-lookup"><span data-stu-id="fda83-122">Applies to: associations and references</span></span>

<span data-ttu-id="fda83-123">Указывает, должны ли удаляться все объекты в ассоциации, квалифицированные с помощью **Delete** , при удалении упоминаемого объекта или ассоциации.</span><span class="sxs-lookup"><span data-stu-id="fda83-123">Indicates whether all objects within an association that is qualified by **Delete** must be deleted if the referenced object or the association is deleted.</span></span> <span data-ttu-id="fda83-124">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="fda83-124">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="fda83-125"><span id="Indexed"></span><span id="indexed"></span><span id="INDEXED"></span>**Индексированного**</span><span class="sxs-lookup"><span data-stu-id="fda83-125"><span id="Indexed"></span><span id="indexed"></span><span id="INDEXED"></span>**Indexed**</span></span>
</dt> <dd>

<span data-ttu-id="fda83-126">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="fda83-126">Data type: **boolean**</span></span>

<span data-ttu-id="fda83-127">Область применения: свойства, методы</span><span class="sxs-lookup"><span data-stu-id="fda83-127">Applies to: properties, methods</span></span>

<span data-ttu-id="fda83-128">Указывает, следует ли индексировать свойство класса.</span><span class="sxs-lookup"><span data-stu-id="fda83-128">Indicates whether a class property should be indexed.</span></span> <span data-ttu-id="fda83-129">При применении к свойствам в классах, размещенных в репозитории, это имеет значение только создание (во время создания класса) быстрого поиска запроса для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="fda83-129">When applied to properties in classes hosted by the repository, this only has the meaning of creating (at the time of class creation) a fast secondary query lookup for that property.</span></span>

<span data-ttu-id="fda83-130">Допускается только значение **true** (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="fda83-130">Only the value **TRUE** (default) is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="fda83-131"><span id="Invisible"></span><span id="invisible"></span><span id="INVISIBLE"></span>**Видн**</span><span class="sxs-lookup"><span data-stu-id="fda83-131"><span id="Invisible"></span><span id="invisible"></span><span id="INVISIBLE"></span>**Invisible**</span></span>
</dt> <dd>

<span data-ttu-id="fda83-132">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="fda83-132">Data type: **boolean**</span></span>

<span data-ttu-id="fda83-133">Область применения: связи, свойства, методы, ссылки, классы</span><span class="sxs-lookup"><span data-stu-id="fda83-133">Applies to: associations, properties, methods, references, classes</span></span>

<span data-ttu-id="fda83-134">Указывает, определена ли ассоциация только для внутренних целей (например, для определения семантики зависимостей) и не должна отображаться (например, в Maps).</span><span class="sxs-lookup"><span data-stu-id="fda83-134">Indicates whether the association is defined only for internal purposes (for example, for definition of dependency semantics) and should not be displayed (for example, in maps).</span></span> <span data-ttu-id="fda83-135">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="fda83-135">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="fda83-136"><span id="Large"></span><span id="large"></span><span id="LARGE"></span>**Достаточ**</span><span class="sxs-lookup"><span data-stu-id="fda83-136"><span id="Large"></span><span id="large"></span><span id="LARGE"></span>**Large**</span></span>
</dt> <dd>

<span data-ttu-id="fda83-137">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="fda83-137">Data type: **boolean**</span></span>

<span data-ttu-id="fda83-138">Область применения: свойства, классы</span><span class="sxs-lookup"><span data-stu-id="fda83-138">Applies to: properties, classes</span></span>

<span data-ttu-id="fda83-139">Указывает, требуется ли для свойства или класса большой объем дискового пространства.</span><span class="sxs-lookup"><span data-stu-id="fda83-139">Indicates whether the property or class requires a large amount of storage space.</span></span> <span data-ttu-id="fda83-140">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="fda83-140">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="fda83-141"><span id="Not_Null"></span><span id="not_null"></span><span id="NOT_NULL"></span>**Не \_ null**</span><span class="sxs-lookup"><span data-stu-id="fda83-141"><span id="Not_Null"></span><span id="not_null"></span><span id="NOT_NULL"></span>**Not\_Null**</span></span>
</dt> <dd>

<span data-ttu-id="fda83-142">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="fda83-142">Data type: **boolean**</span></span>

<span data-ttu-id="fda83-143">Область применения: свойства</span><span class="sxs-lookup"><span data-stu-id="fda83-143">Applies to: properties</span></span>

<span data-ttu-id="fda83-144">Указывает, может ли свойство класса принимать значение **null** (**VT \_ null**).</span><span class="sxs-lookup"><span data-stu-id="fda83-144">Indicates whether a class property cannot take on a value of **NULL** (**VT\_NULL**).</span></span> <span data-ttu-id="fda83-145">Допускается только значение **true** (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="fda83-145">Only the value **TRUE** (default) is allowed.</span></span>

<span data-ttu-id="fda83-146">Если этот квалификатор указан, Инструментарий WMI не разрешает создание экземпляров со свойством, имеющим значение **null**, а свойства **null** возвращают **\_ \_ Недопустимый \_ код ошибки WBEM E** .</span><span class="sxs-lookup"><span data-stu-id="fda83-146">If this qualifier is specified, WMI does not allow creation of instances with the property set to **NULL**, and **NULL** properties return the **WBEM\_E\_ILLEGAL\_NULL** error code.</span></span>

<span data-ttu-id="fda83-147">Обратите внимание, что [**ключ**](standard-qualifiers.md) и **индексированные** квалификаторы уже подразумевают это поведение.</span><span class="sxs-lookup"><span data-stu-id="fda83-147">Note that the [**Key**](standard-qualifiers.md) and **Indexed** qualifiers already imply this behavior.</span></span>

</dd> <dt>

<span data-ttu-id="fda83-148"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Поставщики**</span><span class="sxs-lookup"><span data-stu-id="fda83-148"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Provider**</span></span>
</dt> <dd>

<span data-ttu-id="fda83-149">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fda83-149">Data type: **string**</span></span>

<span data-ttu-id="fda83-150">Применимо к: Any</span><span class="sxs-lookup"><span data-stu-id="fda83-150">Applies to: Any</span></span>

<span data-ttu-id="fda83-151">Указывает, что элемент схемы является динамическим и, таким словами, заполняется поставщиком.</span><span class="sxs-lookup"><span data-stu-id="fda83-151">Indication that the schema element is dynamic and thus populated by a provider.</span></span> <span data-ttu-id="fda83-152">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="fda83-152">The default is **NULL**.</span></span> <span data-ttu-id="fda83-153">Этот квалификатор является зависящим от реализации обработчиком для инструментирования.</span><span class="sxs-lookup"><span data-stu-id="fda83-153">This qualifier is an implementation-specific handle to the instrumentation.</span></span>

</dd> <dt>

<span data-ttu-id="fda83-154"><span id="Experimental"></span><span id="experimental"></span><span id="EXPERIMENTAL"></span>**Проб**</span><span class="sxs-lookup"><span data-stu-id="fda83-154"><span id="Experimental"></span><span id="experimental"></span><span id="EXPERIMENTAL"></span>**Experimental**</span></span>
</dt> <dd>

<span data-ttu-id="fda83-155">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="fda83-155">Data type: **boolean**</span></span>

<span data-ttu-id="fda83-156">Применимо к: Any</span><span class="sxs-lookup"><span data-stu-id="fda83-156">Applies to: any</span></span>

<span data-ttu-id="fda83-157">Указывает, что указанный элемент был предложен как часть будущего выпуска схем CIM, но еще не является частью стандартной схемы.</span><span class="sxs-lookup"><span data-stu-id="fda83-157">Indicates that the specified element has been proposed to be a part of a future release of the CIM Schemas, but is not yet part of the standard Schema.</span></span> <span data-ttu-id="fda83-158">Вместо этого элемент доступен пользователям для экспериментов, реализации и предоставления отзывов о.</span><span class="sxs-lookup"><span data-stu-id="fda83-158">Instead, the element is available for users to experiment, implement, and provide feedback on.</span></span> <span data-ttu-id="fda83-159">В зависимости от отзывов элемент может добавляться в стандартный, как представленный, измененный или удаленный.</span><span class="sxs-lookup"><span data-stu-id="fda83-159">Based on feedback, the element may added to the standard as presented, modified, or removed.</span></span> <span data-ttu-id="fda83-160">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="fda83-160">The default is **FALSE**.</span></span> <span data-ttu-id="fda83-161">Реализация не должна поддерживать элемент с этим квалификатором.</span><span class="sxs-lookup"><span data-stu-id="fda83-161">An implementation does not have to support an element with this qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="fda83-162"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="fda83-162"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="fda83-163">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fda83-163">Data type: **string**</span></span>

<span data-ttu-id="fda83-164">Область применения: свойства, ссылки, методы, параметры</span><span class="sxs-lookup"><span data-stu-id="fda83-164">Applies to: properties, references, methods, parameters</span></span>

<span data-ttu-id="fda83-165">Конкретный тип, назначенный элементу данных.</span><span class="sxs-lookup"><span data-stu-id="fda83-165">Specific type assigned to a data item.</span></span> <span data-ttu-id="fda83-166">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="fda83-166">The default is **NULL**.</span></span>

<span data-ttu-id="fda83-167">Использование. необходимо использовать квалификатор **синтакстипе** с этим квалификатором.</span><span class="sxs-lookup"><span data-stu-id="fda83-167">Usage: You must use the **SyntaxType** qualifier with this qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="fda83-168"><span id="SyntaxType"></span><span id="syntaxtype"></span><span id="SYNTAXTYPE"></span>**синтакстипе**</span><span class="sxs-lookup"><span data-stu-id="fda83-168"><span id="SyntaxType"></span><span id="syntaxtype"></span><span id="SYNTAXTYPE"></span>**SyntaxType**</span></span>
</dt> <dd>

<span data-ttu-id="fda83-169">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fda83-169">Data type: **string**</span></span>

<span data-ttu-id="fda83-170">Область применения: свойства, ссылки, методы, параметры</span><span class="sxs-lookup"><span data-stu-id="fda83-170">Applies to: properties, references, methods, parameters</span></span>

<span data-ttu-id="fda83-171">Формат квалификатора **синтаксиса** .</span><span class="sxs-lookup"><span data-stu-id="fda83-171">Format of the **Syntax** qualifier.</span></span> <span data-ttu-id="fda83-172">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="fda83-172">The default is **NULL**.</span></span>

<span data-ttu-id="fda83-173">Использование. необходимо использовать квалификатор **синтаксиса** с этим квалификатором.</span><span class="sxs-lookup"><span data-stu-id="fda83-173">Usage: You must use the **Syntax** qualifier with this qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="fda83-174"><span id="TriggerType"></span><span id="triggertype"></span><span id="TRIGGERTYPE"></span>**TriggerType может принимать**</span><span class="sxs-lookup"><span data-stu-id="fda83-174"><span id="TriggerType"></span><span id="triggertype"></span><span id="TRIGGERTYPE"></span>**TriggerType**</span></span>
</dt> <dd>

<span data-ttu-id="fda83-175">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fda83-175">Data type: **string**</span></span>

<span data-ttu-id="fda83-176">Область применения: классы, свойства, методы, ассоциации, указания, ссылки</span><span class="sxs-lookup"><span data-stu-id="fda83-176">Applies to: classes, properties, methods, associations, indications, references</span></span>

<span data-ttu-id="fda83-177">Обстоятельства, при которых срабатывает триггер.</span><span class="sxs-lookup"><span data-stu-id="fda83-177">Circumstances under which a trigger is fired.</span></span> <span data-ttu-id="fda83-178">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="fda83-178">The default is **NULL**.</span></span> <span data-ttu-id="fda83-179">Типы триггеров зависят от конструкции мета-модели.</span><span class="sxs-lookup"><span data-stu-id="fda83-179">The trigger types vary by meta-model construct.</span></span>

<span data-ttu-id="fda83-180">Для классов и ассоциаций допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fda83-180">For classes and associations, the legal values are:</span></span>

<span data-ttu-id="fda83-181">Создание</span><span class="sxs-lookup"><span data-stu-id="fda83-181">Create</span></span>

<span data-ttu-id="fda83-182">Удалить</span><span class="sxs-lookup"><span data-stu-id="fda83-182">Delete</span></span>

<span data-ttu-id="fda83-183">Update</span><span class="sxs-lookup"><span data-stu-id="fda83-183">Update</span></span>

<span data-ttu-id="fda83-184">Access</span><span class="sxs-lookup"><span data-stu-id="fda83-184">Access</span></span>

<span data-ttu-id="fda83-185">Для свойств и ссылок допустимы следующие значения: Update и Access.</span><span class="sxs-lookup"><span data-stu-id="fda83-185">For properties and references, the legal values are: Update and Access.</span></span>

<span data-ttu-id="fda83-186">Для методов допустимые значения: до и после.</span><span class="sxs-lookup"><span data-stu-id="fda83-186">For methods, the legal values are Before and After.</span></span>

<span data-ttu-id="fda83-187">Для обозначений выдается допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="fda83-187">For indications, the legal value is Thrown.</span></span>

</dd> <dt>

<span data-ttu-id="fda83-188"><span id="UnknownValues"></span><span id="unknownvalues"></span><span id="UNKNOWNVALUES"></span>**ункновнвалуес**</span><span class="sxs-lookup"><span data-stu-id="fda83-188"><span id="UnknownValues"></span><span id="unknownvalues"></span><span id="UNKNOWNVALUES"></span>**UnknownValues**</span></span>
</dt> <dd>

<span data-ttu-id="fda83-189">Тип данных: **массив строк**</span><span class="sxs-lookup"><span data-stu-id="fda83-189">Data type: **string array**</span></span>

<span data-ttu-id="fda83-190">Область применения: свойства</span><span class="sxs-lookup"><span data-stu-id="fda83-190">Applies to: properties</span></span>

<span data-ttu-id="fda83-191">Набор значений, указывающий, что значение связанного свойства неизвестно (свойство не может рассматриваться как имеющее допустимое или осмысленное значение).</span><span class="sxs-lookup"><span data-stu-id="fda83-191">Set of values indicating that the value of the associated property is unknown (the property cannot be considered as having a valid or meaningful value).</span></span> <span data-ttu-id="fda83-192">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="fda83-192">The default is **NULL**.</span></span>

<span data-ttu-id="fda83-193">Правила и ограничения, используемые для определения неизвестных значений, совпадают с соглашениями, применимыми к квалификатору [**ValueMap**](standard-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="fda83-193">The conventions and restrictions used for defining unknown values are the same as those applicable to the [**ValueMap**](standard-qualifiers.md) qualifier.</span></span>

<span data-ttu-id="fda83-194">Обратите внимание, что этот квалификатор не может быть переопределен.</span><span class="sxs-lookup"><span data-stu-id="fda83-194">Note that this qualifier cannot be overridden.</span></span> <span data-ttu-id="fda83-195">Неразумно разрешите подкласс обрабатывать значение как известное значение, если в каком-либо родительском классе он считается неизвестным.</span><span class="sxs-lookup"><span data-stu-id="fda83-195">It is unreasonable to permit a subclass to treat a value as a known value when it is treated as unknown by some parent class.</span></span>

</dd> <dt>

<span data-ttu-id="fda83-196"><span id="UnsupportedValues"></span><span id="unsupportedvalues"></span><span id="UNSUPPORTEDVALUES"></span>**унсуппортедвалуес**</span><span class="sxs-lookup"><span data-stu-id="fda83-196"><span id="UnsupportedValues"></span><span id="unsupportedvalues"></span><span id="UNSUPPORTEDVALUES"></span>**UnsupportedValues**</span></span>
</dt> <dd>

<span data-ttu-id="fda83-197">Тип данных: **массив строк**</span><span class="sxs-lookup"><span data-stu-id="fda83-197">Data type: **string array**</span></span>

<span data-ttu-id="fda83-198">Область применения: свойства</span><span class="sxs-lookup"><span data-stu-id="fda83-198">Applies to: properties</span></span>

<span data-ttu-id="fda83-199">Набор значений, указывающий, что значение связанного свойства не поддерживается (свойство не может рассматриваться как имеющее допустимое или осмысленное значение).</span><span class="sxs-lookup"><span data-stu-id="fda83-199">Set of values indicating that the value of the associated property is unsupported (the property cannot be considered as having a valid or meaningful value).</span></span> <span data-ttu-id="fda83-200">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="fda83-200">The default is **NULL**.</span></span>

<span data-ttu-id="fda83-201">Правила и ограничения, используемые для определения неподдерживаемых значений, совпадают с соглашениями, применимыми к квалификатору [**ValueMap**](standard-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="fda83-201">The conventions and restrictions used for defining unsupported values are the same as those applicable to the [**ValueMap**](standard-qualifiers.md) qualifier.</span></span>

<span data-ttu-id="fda83-202">Обратите внимание, что квалификатор не может быть переопределен.</span><span class="sxs-lookup"><span data-stu-id="fda83-202">Note this qualifier cannot be overridden.</span></span> <span data-ttu-id="fda83-203">Неразумно разрешите подкласс обрабатывать значение как поддерживаемое значение, которое считается неизвестным для какого-либо родительского класса.</span><span class="sxs-lookup"><span data-stu-id="fda83-203">It is unreasonable to permit a subclass to treat a value as a supported value that is treated as unknown by some parent class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fda83-204">Требования</span><span class="sxs-lookup"><span data-stu-id="fda83-204">Requirements</span></span>



| <span data-ttu-id="fda83-205">Требование</span><span class="sxs-lookup"><span data-stu-id="fda83-205">Requirement</span></span> | <span data-ttu-id="fda83-206">Значение</span><span class="sxs-lookup"><span data-stu-id="fda83-206">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="fda83-207">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fda83-207">Minimum supported client</span></span><br/> | <span data-ttu-id="fda83-208">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fda83-208">Windows Vista</span></span><br/>       |
| <span data-ttu-id="fda83-209">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fda83-209">Minimum supported server</span></span><br/> | <span data-ttu-id="fda83-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fda83-210">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fda83-211">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fda83-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fda83-212">Квалификаторы WMI</span><span class="sxs-lookup"><span data-stu-id="fda83-212">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="fda83-213">Добавление квалификатора</span><span class="sxs-lookup"><span data-stu-id="fda83-213">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

 




