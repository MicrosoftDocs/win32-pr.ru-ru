---
description: Классические поставщики должны использовать MOF-файл (MOF) для публикации макета данных о событиях. Затем потребители могут считывать опубликованный макет из WMI во время выполнения и использовать его для чтения данных событий.
ms.assetid: eb3d8422-2352-47cf-9825-cba9916791a9
title: Публикация схемы событий для классического поставщика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f51cfd30d0c9d73841ca906fb81e9d544dec88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343882"
---
# <a name="publishing-your-event-schema-for-a-classic-provider"></a><span data-ttu-id="93e88-104">Публикация схемы событий для классического поставщика</span><span class="sxs-lookup"><span data-stu-id="93e88-104">Publishing Your Event Schema for a Classic Provider</span></span>

<span data-ttu-id="93e88-105">[Классические](about-event-tracing.md) поставщики должны использовать [MOF-файл](../wmisdk/managed-object-format--mof-.md) (MOF) для публикации макета данных о событиях.</span><span class="sxs-lookup"><span data-stu-id="93e88-105">[Classic](about-event-tracing.md) providers should use [Managed Object Format](../wmisdk/managed-object-format--mof-.md) (MOF) to publish the layout of their event data.</span></span> <span data-ttu-id="93e88-106">Затем потребители могут считывать опубликованный макет из WMI во время выполнения и использовать его для чтения данных событий.</span><span class="sxs-lookup"><span data-stu-id="93e88-106">Consumers can then read the published layout from WMI at runtime and use it to read the event data.</span></span>

<span data-ttu-id="93e88-107">Если вы используете MOF для публикации макета данных событий в WMI, обычно в корневом пространстве имен WMI создаются следующие три типа классов MOF \\ :</span><span class="sxs-lookup"><span data-stu-id="93e88-107">If you use MOF to publish the layout of your event data in WMI, you typically create the following three types of MOF classes in the root\\wmi namespace:</span></span>

-   [<span data-ttu-id="93e88-108">Класс MOF поставщика</span><span class="sxs-lookup"><span data-stu-id="93e88-108">A provider MOF class</span></span>](#provider-mof-classes)
-   [<span data-ttu-id="93e88-109">Один или несколько классов MOF событий</span><span class="sxs-lookup"><span data-stu-id="93e88-109">One or more event MOF classes</span></span>](#event-mof-classes)
-   [<span data-ttu-id="93e88-110">Класс MOF одного или нескольких типов событий</span><span class="sxs-lookup"><span data-stu-id="93e88-110">One or more event type MOF classes</span></span>](#event-type-mof-classes)

## <a name="provider-mof-classes"></a><span data-ttu-id="93e88-111">Классы MOF поставщика</span><span class="sxs-lookup"><span data-stu-id="93e88-111">Provider MOF classes</span></span>

<span data-ttu-id="93e88-112">При публикации макета данных события необходимо создать класс MOF, определяющий поставщика.</span><span class="sxs-lookup"><span data-stu-id="93e88-112">If you publish the layout of your event data, you must create a MOF class that identifies your provider.</span></span> <span data-ttu-id="93e88-113">Этот класс должен быть производным от класса **евенттраце** MOF и должен быть пустым (без свойств или методов).</span><span class="sxs-lookup"><span data-stu-id="93e88-113">This class must derive from the **EventTrace** MOF class and must be empty (no properties or methods).</span></span> <span data-ttu-id="93e88-114">Класс также должен включать квалификатор **GUID** , который уникальным образом идентифицирует поставщик.</span><span class="sxs-lookup"><span data-stu-id="93e88-114">The class must also include the **Guid** qualifier which uniquely identifies the provider.</span></span> <span data-ttu-id="93e88-115">Это тот же идентификатор GUID, который вы используете при вызове функции [**регистертрацегуидс**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) для регистрации поставщика.</span><span class="sxs-lookup"><span data-stu-id="93e88-115">This is the same GUID you use when you calling the [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function to register your provider.</span></span>

## <a name="event-mof-classes"></a><span data-ttu-id="93e88-116">Классы событий MOF</span><span class="sxs-lookup"><span data-stu-id="93e88-116">Event MOF classes</span></span>

<span data-ttu-id="93e88-117">Класс событий MOF определяет класс событий, предоставляемых поставщиком.</span><span class="sxs-lookup"><span data-stu-id="93e88-117">An event MOF class defines a class of events that the provider provides.</span></span> <span data-ttu-id="93e88-118">Этот класс является производным от класса MOF поставщика и должен быть пустым (без свойств или методов).</span><span class="sxs-lookup"><span data-stu-id="93e88-118">This class derives from the provider MOF class and must be empty (no properties or methods).</span></span> <span data-ttu-id="93e88-119">Класс также должен включать квалификатор **GUID** , который однозначно определяет класс событий, определяемых его дочерними классами.</span><span class="sxs-lookup"><span data-stu-id="93e88-119">The class must also include the **Guid** qualifier which uniquely identifies the class of events that its child classes define.</span></span> <span data-ttu-id="93e88-120">Поставщик использует этот же идентификатор GUID при задании элемента **GUID** структуры [**\_ \_ заголовка трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) .</span><span class="sxs-lookup"><span data-stu-id="93e88-120">The provider uses this same GUID when setting the **Guid** member of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure.</span></span>

## <a name="event-type-mof-classes"></a><span data-ttu-id="93e88-121">Классы MOF типа событий</span><span class="sxs-lookup"><span data-stu-id="93e88-121">Event type MOF classes</span></span>

<span data-ttu-id="93e88-122">Класс MOF типа события определяет фактические данные события.</span><span class="sxs-lookup"><span data-stu-id="93e88-122">An event type MOF class defines the actual event data.</span></span> <span data-ttu-id="93e88-123">Этот класс является производным от родительского класса событий MOF.</span><span class="sxs-lookup"><span data-stu-id="93e88-123">This class derives from its parent event MOF class.</span></span> <span data-ttu-id="93e88-124">При присвоении имени классу MOF типа события используется имя класса MOF события в начале типа события имя класса MOF.</span><span class="sxs-lookup"><span data-stu-id="93e88-124">When naming the event type MOF class, the convention is to use the event MOF class name at the beginning of the event type MOF class name.</span></span> <span data-ttu-id="93e88-125">Например, если имя класса MOF события — Хвконфиг, а класс событий MOF представляет сведения о ЦП, следует присвоить классу MOF типа события, Хвконфиг \_ CPU.</span><span class="sxs-lookup"><span data-stu-id="93e88-125">For example, if the event MOF class name is HWConfig and the event type MOF class represents CPU information, you should name the event type MOF class, HWConfig\_CPU.</span></span>

<span data-ttu-id="93e88-126">Используйте квалификатор **EventType** в классе события типа MOF для задания типа события.</span><span class="sxs-lookup"><span data-stu-id="93e88-126">Use the **EventType** qualifier on the event type MOF class to identify the event type.</span></span> <span data-ttu-id="93e88-127">Если несколько типов событий используют одни и те же данные событий, они могут использовать один и тот же класс MOF.</span><span class="sxs-lookup"><span data-stu-id="93e88-127">If multiple event types use the same event data, they can use the same MOF class.</span></span> <span data-ttu-id="93e88-128">Поставщик использует то же значение типа события для указания события при задании члена **класса. Type** в структуре [**\_ \_ заголовка трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) .</span><span class="sxs-lookup"><span data-stu-id="93e88-128">The provider uses the same event type value to identify the event when setting the **Class.Type** member of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure.</span></span>

<span data-ttu-id="93e88-129">Класс MOF типа события содержит свойства.</span><span class="sxs-lookup"><span data-stu-id="93e88-129">The event type MOF class contains properties.</span></span> <span data-ttu-id="93e88-130">Порядок этих свойств определяет макет данных события.</span><span class="sxs-lookup"><span data-stu-id="93e88-130">The order of these properties define the layout of the event data.</span></span> <span data-ttu-id="93e88-131">В следующей таблице указаны типы данных и квалификаторы, которые можно использовать для определения свойств.</span><span class="sxs-lookup"><span data-stu-id="93e88-131">The following table identifies the data types and qualifiers you can use to define the properties.</span></span> <span data-ttu-id="93e88-132">Дополнительные сведения о квалификаторах свойств и классов, которые можно использовать, см. в разделе [Квалификаторы MOF для трассировки событий](event-tracing-mof-qualifiers.md).</span><span class="sxs-lookup"><span data-stu-id="93e88-132">For more information on the property and class qualifiers that you can use, see [Event Tracing MOF Qualifiers](event-tracing-mof-qualifiers.md).</span></span>



| <span data-ttu-id="93e88-133">Тип данных</span><span class="sxs-lookup"><span data-stu-id="93e88-133">Data type</span></span>              | <span data-ttu-id="93e88-134">Квалификаторы</span><span class="sxs-lookup"><span data-stu-id="93e88-134">Qualifiers</span></span>                        | <span data-ttu-id="93e88-135">Описание</span><span class="sxs-lookup"><span data-stu-id="93e88-135">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93e88-136">**sint8**, **Uint8**</span><span class="sxs-lookup"><span data-stu-id="93e88-136">**sint8**, **uint8**</span></span>   | <span data-ttu-id="93e88-137">**Формат**</span><span class="sxs-lookup"><span data-stu-id="93e88-137">**Format**</span></span>                        | <span data-ttu-id="93e88-138">Объявляет 1-байтовое десятичное целое число.</span><span class="sxs-lookup"><span data-stu-id="93e88-138">Declares a 1-byte decimal integer.</span></span> <span data-ttu-id="93e88-139">Чтобы объявить символ ANSI, используйте квалификатор **формата** и присвойте ему значение "c".</span><span class="sxs-lookup"><span data-stu-id="93e88-139">To declare an ANSI character, use the **Format** qualifier and set its value to "c".</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="93e88-140">**sint16**, **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93e88-140">**sint16**, **uint16**</span></span> | <span data-ttu-id="93e88-141">**Формат**</span><span class="sxs-lookup"><span data-stu-id="93e88-141">**Format**</span></span>                        | <span data-ttu-id="93e88-142">Объявляет 2-байтовое десятичное целое число.</span><span class="sxs-lookup"><span data-stu-id="93e88-142">Declares a 2-byte decimal integer.</span></span> <span data-ttu-id="93e88-143">Чтобы указать, что число является шестнадцатеричным числом, используйте квалификатор **формата** .</span><span class="sxs-lookup"><span data-stu-id="93e88-143">To indicate the number is a hexadecimal number, use the **Format** qualifier.</span></span> <span data-ttu-id="93e88-144">Например, Format ("x").</span><span class="sxs-lookup"><span data-stu-id="93e88-144">For example, format("x").</span></span>                                                                                                                                                                               |
| <span data-ttu-id="93e88-145">**Sint32**, **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93e88-145">**sint32**, **uint32**</span></span> | <span data-ttu-id="93e88-146">**Формат**</span><span class="sxs-lookup"><span data-stu-id="93e88-146">**Format**</span></span>                        | <span data-ttu-id="93e88-147">Объявляет 4-байтовое десятичное целое число.</span><span class="sxs-lookup"><span data-stu-id="93e88-147">Declares a 4-byte decimal integer.</span></span> <span data-ttu-id="93e88-148">Чтобы указать, что число является шестнадцатеричным числом, используйте квалификатор **формата** и присвойте ему значение "x".</span><span class="sxs-lookup"><span data-stu-id="93e88-148">To indicate the number is a hexadecimal number, use the **Format** qualifier and set its value to "x".</span></span>                                                                                                                                                                                |
| <span data-ttu-id="93e88-149">**sint64**, **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93e88-149">**sint64**, **uint64**</span></span> | <span data-ttu-id="93e88-150">**Формат**</span><span class="sxs-lookup"><span data-stu-id="93e88-150">**Format**</span></span>                        | <span data-ttu-id="93e88-151">Объявляет 8-байтовое десятичное целое число.</span><span class="sxs-lookup"><span data-stu-id="93e88-151">Declares a 8-byte decimal integer.</span></span> <span data-ttu-id="93e88-152">Чтобы указать, что число является шестнадцатеричным числом, используйте квалификатор **формата** и присвойте ему значение "x".</span><span class="sxs-lookup"><span data-stu-id="93e88-152">To indicate the number is a hexadecimal number, use the **Format** qualifier and set its value to "x".</span></span>                                                                                                                                                                                |
| <span data-ttu-id="93e88-153">**boolean**</span><span class="sxs-lookup"><span data-stu-id="93e88-153">**boolean**</span></span>            |                                   | <span data-ttu-id="93e88-154">Объявляет логическое значение.</span><span class="sxs-lookup"><span data-stu-id="93e88-154">Declares a Boolean value.</span></span> <span data-ttu-id="93e88-155">Потребитель события должен интерпретировать значение как BOOL (4-байтовое целое число).</span><span class="sxs-lookup"><span data-stu-id="93e88-155">The event consumer should interpret the value as BOOL (4-byte integer).</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="93e88-156">**char16**</span><span class="sxs-lookup"><span data-stu-id="93e88-156">**char16**</span></span>             |                                   | <span data-ttu-id="93e88-157">Объявляет широкий символ.</span><span class="sxs-lookup"><span data-stu-id="93e88-157">Declares a wide character.</span></span> <span data-ttu-id="93e88-158">Потребитель событий должен интерпретировать Char16 массивы в событиях ядра как строки расширенных символов.</span><span class="sxs-lookup"><span data-stu-id="93e88-158">The event consumer should interpret char16 arrays in kernel events as wide character strings.</span></span> <span data-ttu-id="93e88-159">(Используйте размер массива для копирования строки.</span><span class="sxs-lookup"><span data-stu-id="93e88-159">(Use the array size to copy the string.</span></span> <span data-ttu-id="93e88-160">Некоторые строки могут содержать начальные символы NULL.)</span><span class="sxs-lookup"><span data-stu-id="93e88-160">Some strings may contain leading NULL characters.)</span></span>                                                                                                      |
| <span data-ttu-id="93e88-161">**object**</span><span class="sxs-lookup"><span data-stu-id="93e88-161">**object**</span></span>             | <span data-ttu-id="93e88-162">**Расширение**</span><span class="sxs-lookup"><span data-stu-id="93e88-162">**Extension**</span></span>                     | <span data-ttu-id="93e88-163">Объявляет двоичный BLOB-объект.</span><span class="sxs-lookup"><span data-stu-id="93e88-163">Declares a binary blob.</span></span> <span data-ttu-id="93e88-164">Квалификатор **расширения** указывает тип данных в большом двоичном объекте.</span><span class="sxs-lookup"><span data-stu-id="93e88-164">The **Extension** qualifier indicates the type of data in the blob.</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="93e88-165">**string**</span><span class="sxs-lookup"><span data-stu-id="93e88-165">**string**</span></span>             | <span data-ttu-id="93e88-166">**Формат**, **стрингтерминатион**</span><span class="sxs-lookup"><span data-stu-id="93e88-166">**Format**, **StringTermination**</span></span> | <span data-ttu-id="93e88-167">Объявляет строковое значение.</span><span class="sxs-lookup"><span data-stu-id="93e88-167">Declares a string value.</span></span> <span data-ttu-id="93e88-168">Чтобы указать, что строка является строкой расширенных символов, используйте квалификатор **формата** и задайте для его значения значение w.</span><span class="sxs-lookup"><span data-stu-id="93e88-168">To indicate the string is a wide-character string use the **Format** qualifier and set its value to "w".</span></span> <span data-ttu-id="93e88-169">Строка считается строкой ANSI, если не указан квалификатор **формата** .</span><span class="sxs-lookup"><span data-stu-id="93e88-169">The string is considered an ANSI string if you do not specify the **Format** qualifier.</span></span> <span data-ttu-id="93e88-170">Чтобы указать, как завершается строка, используйте квалификатор **стрингтерминатион** .</span><span class="sxs-lookup"><span data-stu-id="93e88-170">To indicate how the string is terminated, use the **StringTermination** qualifier.</span></span> <br/> |



 

<span data-ttu-id="93e88-171">Чтобы указать массив, можно использовать квадратные скобки, \[ \] .</span><span class="sxs-lookup"><span data-stu-id="93e88-171">To specify an array, you can use square brackets, \[\].</span></span> <span data-ttu-id="93e88-172">Квадратные скобки могут включать размер массива.</span><span class="sxs-lookup"><span data-stu-id="93e88-172">The square brackets can include the size of the array.</span></span> <span data-ttu-id="93e88-173">Например:</span><span class="sxs-lookup"><span data-stu-id="93e88-173">For example:</span></span>

`[WmiDataId(1), read] uint8 MyGuid[16];`

<span data-ttu-id="93e88-174">Квалификатор **Max** также можно использовать для указания размера массива.</span><span class="sxs-lookup"><span data-stu-id="93e88-174">You can also use the **Max** qualifier to specify the size of an array.</span></span> <span data-ttu-id="93e88-175">Например:</span><span class="sxs-lookup"><span data-stu-id="93e88-175">For example:</span></span>

`[WmiDataId(1), Max(16), read] uint8 MyGuid[];`

<span data-ttu-id="93e88-176">При включении размера массива в квадратные скобки компилятор MOF создает для вас квалификатор Max.</span><span class="sxs-lookup"><span data-stu-id="93e88-176">If you include the size of the array in the square brackets, the MOF compiler generates the Max qualifier for you.</span></span>

<span data-ttu-id="93e88-177">Важно использовать квалификатор **Description** для каждого свойства.</span><span class="sxs-lookup"><span data-stu-id="93e88-177">It is important that you use the **Description** qualifier for each property.</span></span> <span data-ttu-id="93e88-178">Описание должно содержать отображаемое имя, которое потребитель может использовать при отображении значений свойств.</span><span class="sxs-lookup"><span data-stu-id="93e88-178">The description should contain a display name that the consumer can use when displaying the property values.</span></span>

<span data-ttu-id="93e88-179">В следующем примере показано содержимое MOF-файла, описывающего класс MOF, события и типа события.</span><span class="sxs-lookup"><span data-stu-id="93e88-179">The following example shows the contents of a MOF file that describes a provider, event, and event type MOF class.</span></span>

``` syntax
#pragma namespace("\\\\.\\root\\wmi")

[dynamic: ToInstance, Description("Defines my event provider"),
 Guid("{7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}")]
class MyProvider : EventTrace
{
};

[dynamic: ToInstance, Description("Defines a category of events that my provider logs."): Amended,
 Guid("{B49D5931-AD85-4070-B1B1-3F81F1532875}")]
class MyCategory : MyProvider
{
};

[dynamic: ToInstance, Description("Defines an event within the category of events that my provider logs."): Amended,
 EventType(1)]
class MyCategory_MyEvent : MyCategory
{
    [WmiDataId(1), Description("Cost factor"): Amended, read] sint32 Cost;
    [WmiDataId(2), Description("Index values"): Amended, read] uint32 Indices[3];
    [WmiDataId(3), Description("Signature"): Amended, read, StringTermination("NullTerminated"), Format("w")] string Signature;
    [WmiDataId(4), Description("Is complete copy"): Amended, read] boolean IsComplete;
    [WmiDataId(5), Description("Class identifier"): Amended, read, Extension("Guid")] object ID;
};
```

<span data-ttu-id="93e88-180">Обратите внимание, что имена классов типа "поставщик", "событие" и "тип события" должны быть уникальными в пределах всего пространства имен.</span><span class="sxs-lookup"><span data-stu-id="93e88-180">Note that the provider, event, and event type MOF class names must be unique within the entire namespace.</span></span> <span data-ttu-id="93e88-181">Чтобы избежать конфликтов имен, следует использовать уникальные и описательные имена для всех имен классов.</span><span class="sxs-lookup"><span data-stu-id="93e88-181">To avoid naming conflicts, you should use unique and descriptive name for all class names.</span></span> <span data-ttu-id="93e88-182">Свойства класса также должны быть описательными и уникальными в пределах иерархии классов — дочерний класс, содержащий то же имя свойства, что и родительский класс, перезаписывает свойство родительского класса.</span><span class="sxs-lookup"><span data-stu-id="93e88-182">Class properties should also be descriptive and unique within its class hierarchy—a child class that contains the same property name as a parent class overwrites the property of the parent class.</span></span>

<span data-ttu-id="93e88-183">Определив классы MOF, используйте компилятор MOF для создания схемы событий и добавления ее в репозиторий CIM.</span><span class="sxs-lookup"><span data-stu-id="93e88-183">After defining your MOF classes, use the MOF compiler to generate your event schema and add it to the CIM repository.</span></span> <span data-ttu-id="93e88-184">Затем потребители могут считывать схему из репозитория и программно считывать данные о событиях.</span><span class="sxs-lookup"><span data-stu-id="93e88-184">Consumers can then read the schema from the repository and programmatically read the event data.</span></span> <span data-ttu-id="93e88-185">Полное описание синтаксиса MOF и использование компилятора MOF (Mofcomp.exe) для добавления классов MOF в репозиторий CIM см. в разделе [MOF-файл](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="93e88-185">For a complete description of the MOF syntax and using the MOF compiler (Mofcomp.exe) to add your MOF classes to the CIM repository, see [Managed Object Format](../wmisdk/managed-object-format--mof-.md).</span></span> <span data-ttu-id="93e88-186">Сведения об использовании Wbemtest.exe для доступа к репозиторию CIM см. в разделе [инструментарий управления Windows (WMI)](../wmisdk/wmi-start-page.md) (WMI).</span><span class="sxs-lookup"><span data-stu-id="93e88-186">For information on using Wbemtest.exe to access the CIM repository, see [Windows Management Instrumentation](../wmisdk/wmi-start-page.md) (WMI).</span></span>

## <a name="versioning-mof-class"></a><span data-ttu-id="93e88-187">Управление версиями класс MOF</span><span class="sxs-lookup"><span data-stu-id="93e88-187">Versioning MOF class</span></span>

<span data-ttu-id="93e88-188">При добавлении или изменении класса MOF типа события в соглашении используется версия класса MOF события и его дочерние классы MOF.</span><span class="sxs-lookup"><span data-stu-id="93e88-188">If you add or change an event type MOF class, the convention is to version both the event MOF class and its child event type MOF classes.</span></span> <span data-ttu-id="93e88-189">Чтобы получить версию текущего класса MOF события, добавьте \_ VN в имя класса, где n — это добавочный номер, начинающийся с 0.</span><span class="sxs-lookup"><span data-stu-id="93e88-189">To version the current event MOF class, append \_Vn to the class name, where n is an incremental number starting at 0.</span></span> <span data-ttu-id="93e88-190">Если это первая редакция класса, добавьте \_ v0 к имени класса.</span><span class="sxs-lookup"><span data-stu-id="93e88-190">If this is the first revision to the class, append \_V0 to the class name.</span></span> <span data-ttu-id="93e88-191">Необходимо также добавить в класс квалификатор **евентверсион** .</span><span class="sxs-lookup"><span data-stu-id="93e88-191">You must also add the **EventVersion** qualifier to the class.</span></span> <span data-ttu-id="93e88-192">Используйте тот же номер версии, который использовался в имени класса для значения квалификатора **евентверсион** .</span><span class="sxs-lookup"><span data-stu-id="93e88-192">Use the same version number you used in the class name for the value of the **EventVersion** qualifier.</span></span>

<span data-ttu-id="93e88-193">Новая версия класса MOF события должна использовать то же имя и квалификатор **GUID** , что и исходный класс.</span><span class="sxs-lookup"><span data-stu-id="93e88-193">The new version of the event MOF class must use the same name and **Guid** qualifier as the original class.</span></span> <span data-ttu-id="93e88-194">Новый класс может дополнительно добавить квалификатор **евентверсион** .</span><span class="sxs-lookup"><span data-stu-id="93e88-194">The new class may optionally add the **EventVersion** qualifier.</span></span> <span data-ttu-id="93e88-195">Класс MOF события, не содержащий квалификатор **евентверсион** , считается последней версией, или если все версии класса содержат квалификатор **евентверсион** , то класс с самым высоким номером версии считается последней версией.</span><span class="sxs-lookup"><span data-stu-id="93e88-195">The event MOF class that does not contain the **EventVersion** qualifier is considered the latest version, or if all the versions of the class contain an **EventVersion** qualifier, then the class with the highest version number is considered the latest version.</span></span> <span data-ttu-id="93e88-196">Поставщик использует член **класса. Version** структуры [**\_ \_ заголовка трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) для выявления версии события, включаемого в трассировку.</span><span class="sxs-lookup"><span data-stu-id="93e88-196">The provider uses the **Class.Version** member of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure to identify the version of the event included in the trace.</span></span>

<span data-ttu-id="93e88-197">В следующем примере показано, как выполнить версию класса MOF события.</span><span class="sxs-lookup"><span data-stu-id="93e88-197">The following example shows how to version an event MOF class.</span></span>

``` syntax
#pragma namespace("\\\\.\\root\\wmi")
#pragma classflags("forceupdate")

[dynamic: ToInstance, Description("Defines my event provider"),
 Guid("{7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}")]
class MyProvider : EventTrace
{
};

[dynamic: ToInstance, Description("Defines a category of events that my provider logs."),
 Guid("{B49D5931-AD85-4070-B1B1-3F81F1532875}"),
 EventVersion(1)]
class MyCategory : MyProvider
{
};

[dynamic: ToInstance, Description("Defines an event within the category of events that my provider logs."): Amended,
 EventType(1),
 EventName("MyEvent")]
class MyCategory_MyEvent : MyCategory
{
    [WmiDataId(1), Description("Cost factor"): Amended, read] sint32 Cost;
    [WmiDataId(2), Description("Index values"): Amended, read] uint32 Indices[3];
    [WmiDataId(3), Description("Signature"): Amended, read, StringTermination("NullTerminated"), Format("w")] string Signature;
    [WmiDataId(4), Description("Is complete copy"): Amended, read] boolean IsComplete;
    [WmiDataId(5), Description("Identifier"): Amended, read, Extension("Guid")] object ID;
    [WmiDataId(6), Description("Buffer Size"): Amended, read] uint32 Size;
};

[dynamic: ToInstance, Description("Defines a category of events that my provider logs."): Amended,
 Guid("{B49D5931-AD85-4070-B1B1-3F81F1532875}"),
 EventVersion(0)]
class MyCategory_V0 : MyProvider
{
};

[dynamic: ToInstance, Description("Defines an event within the category of events that my provider logs."): Amended,
 EventType(1)]
class MyCategory_V0_MyEvent : MyCategory_V0
{
    [WmiDataId(1), Description("Cost factor"): Amended, read] sint32 Cost;
    [WmiDataId(2), Description("Index values"): Amended, read] uint32 Indices[3];
    [WmiDataId(3), Description("Signature"): Amended, read, StringTermination("NullTerminated"), Format("w")] string Signature;
    [WmiDataId(4), Description("Is complete copy"): Amended, read] boolean IsComplete;
    [WmiDataId(5), Description("Identifier"): Amended, read, Extension("Guid")] object ID;
};
```

 

 
