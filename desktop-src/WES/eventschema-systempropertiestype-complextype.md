---
title: Сложный тип Системпропертиестипе
description: Определяет сведения, определяющие поставщик и способ его включения, событие, канал, на который было написано событие, а также системные сведения, такие как идентификатор процесса и потока.
ms.assetid: f86f7940-86cf-49ba-8f09-bf6f473d60fd
keywords:
- Журнал событий сложных типов Системпропертиестипе
topic_type:
- apiref
api_name:
- SystemPropertiesType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce78a804c52ed492bd4b2a42332f8eda36b4c3be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803191"
---
# <a name="systempropertiestype-complex-type"></a><span data-ttu-id="88ec2-104">Сложный тип Системпропертиестипе</span><span class="sxs-lookup"><span data-stu-id="88ec2-104">SystemPropertiesType Complex Type</span></span>

<span data-ttu-id="88ec2-105">Определяет сведения, определяющие поставщик и способ его включения, событие, канал, на который было написано событие, а также системные сведения, такие как идентификатор процесса и потока.</span><span class="sxs-lookup"><span data-stu-id="88ec2-105">Defines the information that identifies the provider and how it was enabled, the event, the channel to which the event was written, and system information such as the process and thread IDs.</span></span>

``` syntax
<xs:complexType name="SystemPropertiesType">
    <xs:sequence>
        <xs:element name="Provider">
            <xs:complexType>
                <xs:attribute name="Name"
                    type="anyURI"
                    use="optional"
                 />
                <xs:attribute name="Guid"
                    type="GUIDType"
                    use="optional"
                 />
                <xs:attribute name="EventSourceName"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="EventID">
            <xs:complexType>
                <xs:simpleContent>
                    <xs:extension
                        base="unsignedShort"
                    >
                        <xs:attribute name="Qualifiers"
                            type="unsignedShort"
                            use="optional"
                         />
                    </xs:extension>
                </xs:simpleContent>
            </xs:complexType>
        </xs:element>
        <xs:element name="Version"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Level"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Task"
            type="unsignedShort"
            minOccurs="0"
         />
        <xs:element name="Opcode"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Keywords"
            type="HexInt64Type"
            minOccurs="0"
         />
        <xs:element name="TimeCreated"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="SystemTime"
                    type="dateTime"
                    use="optional"
                 />
                <xs:attribute name="RawTime"
                    type="unsignedLong"
                    use="optional"
                 />
            </xs:complexType>
            <xs:key name="uniqueAtt">
                <xs:selector
                    xpath="."
                 />
                <xs:field
                    xpath="@SystemTime|@RawTime"
                 />
            </xs:key>
        </xs:element>
        <xs:element name="EventRecordID"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:simpleContent>
                    <xs:extension
                        base="unsignedLong"
                     />
                </xs:simpleContent>
            </xs:complexType>
        </xs:element>
        <xs:element name="Correlation"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="ActivityID"
                    type="GUIDType"
                    use="optional"
                 />
                <xs:attribute name="RelatedActivityID"
                    type="GUIDType"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Execution"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="ProcessID"
                    type="unsignedInt"
                    use="required"
                 />
                <xs:attribute name="ThreadID"
                    type="unsignedInt"
                    use="required"
                 />
                <xs:attribute name="ProcessorID"
                    type="unsignedByte"
                    use="optional"
                 />
                <xs:attribute name="SessionID"
                    type="unsignedInt"
                    use="optional"
                 />
                <xs:attribute name="KernelTime"
                    type="unsignedInt"
                    use="optional"
                 />
                <xs:attribute name="UserTime"
                    type="unsignedInt"
                    use="optional"
                 />
                <xs:attribute name="ProcessorTime"
                    type="unsignedInt"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Channel"
            type="anyURI"
            minOccurs="0"
         />
        <xs:element name="Computer"
            type="string"
         />
        <xs:element name="Security"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="UserID"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="88ec2-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="88ec2-106">Child elements</span></span>



| <span data-ttu-id="88ec2-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="88ec2-107">Element</span></span>                                                                         | <span data-ttu-id="88ec2-108">Тип</span><span class="sxs-lookup"><span data-stu-id="88ec2-108">Type</span></span>                                                        | <span data-ttu-id="88ec2-109">Описание</span><span class="sxs-lookup"><span data-stu-id="88ec2-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="88ec2-110">**Канал**</span><span class="sxs-lookup"><span data-stu-id="88ec2-110">**Channel**</span></span>](eventschema-channel-systempropertiestype-element.md)             | <span data-ttu-id="88ec2-111">anyURI</span><span class="sxs-lookup"><span data-stu-id="88ec2-111">anyURI</span></span>                                                      | <span data-ttu-id="88ec2-112">Канал, в который было записано событие.</span><span class="sxs-lookup"><span data-stu-id="88ec2-112">The channel to which the event was logged.</span></span><br/>                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="88ec2-113">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="88ec2-113">**Computer**</span></span>](eventschema-computer-systempropertiestype-element.md)           | <span data-ttu-id="88ec2-114">строка</span><span class="sxs-lookup"><span data-stu-id="88ec2-114">string</span></span>                                                      | <span data-ttu-id="88ec2-115">имя компьютера, на котором произошло событие.</span><span class="sxs-lookup"><span data-stu-id="88ec2-115">The name of the computer on which the event occurred.</span></span><br/>                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="88ec2-116">**Связей**</span><span class="sxs-lookup"><span data-stu-id="88ec2-116">**Correlation**</span></span>](eventschema-correlation-systempropertiestype-element.md)     |                                                             | <span data-ttu-id="88ec2-117">Идентификаторы действий, которые потребители могут использовать для группирования связанных событий.</span><span class="sxs-lookup"><span data-stu-id="88ec2-117">The activity identifiers that consumers can use to group related events together.</span></span><br/>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="88ec2-118">**EventID**</span><span class="sxs-lookup"><span data-stu-id="88ec2-118">**EventID**</span></span>](eventschema-eventid-systempropertiestype-element.md)             |                                                             | <span data-ttu-id="88ec2-119">Идентификатор, используемый поставщиком для идентификации события.</span><span class="sxs-lookup"><span data-stu-id="88ec2-119">The identifier that the provider used to identify the event.</span></span><br/>                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="88ec2-120">**евентрекордид**</span><span class="sxs-lookup"><span data-stu-id="88ec2-120">**EventRecordID**</span></span>](eventschema-eventrecordid-systempropertiestype-element.md) |                                                             | <span data-ttu-id="88ec2-121">Номер записи, назначенный событию при регистрации.</span><span class="sxs-lookup"><span data-stu-id="88ec2-121">The record number assigned to the event when it was logged.</span></span><br/>                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="88ec2-122">**Выполнение**</span><span class="sxs-lookup"><span data-stu-id="88ec2-122">**Execution**</span></span>](eventschema-execution-systempropertiestype-element.md)         |                                                             | <span data-ttu-id="88ec2-123">Содержит сведения о процессе и потоке, которые зарегистрировали событие.</span><span class="sxs-lookup"><span data-stu-id="88ec2-123">Contains information about the process and thread that logged the event.</span></span><br/>                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="88ec2-124">**Keywords**</span><span class="sxs-lookup"><span data-stu-id="88ec2-124">**Keywords**</span></span>](eventschema-keywords-systempropertiestype-element.md)           | [<span data-ttu-id="88ec2-125">**HexInt64Type**</span><span class="sxs-lookup"><span data-stu-id="88ec2-125">**HexInt64Type**</span></span>](eventschema-hexint64type-simpletype.md) | <span data-ttu-id="88ec2-126">Битовая маска ключевых слов, определенных в событии.</span><span class="sxs-lookup"><span data-stu-id="88ec2-126">A bitmask of the keywords defined in the event.</span></span> <span data-ttu-id="88ec2-127">Ключевые слова используются для классификации типов событий (например, событий, связанных с чтением данных).</span><span class="sxs-lookup"><span data-stu-id="88ec2-127">Keywords are used to classify types of events (for example, events associated with reading data).</span></span><br/>                                                                                                                                                                                 |
| [<span data-ttu-id="88ec2-128">**Уровню**</span><span class="sxs-lookup"><span data-stu-id="88ec2-128">**Level**</span></span>](eventschema-level-systempropertiestype-element.md)                 | <span data-ttu-id="88ec2-129">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="88ec2-129">unsignedByte</span></span>                                                | <span data-ttu-id="88ec2-130">Уровень серьезности, определенный в событии.</span><span class="sxs-lookup"><span data-stu-id="88ec2-130">The severity level defined in the event.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="88ec2-131">**Код операции**</span><span class="sxs-lookup"><span data-stu-id="88ec2-131">**Opcode**</span></span>](eventschema-opcode-systempropertiestype-element.md)               | <span data-ttu-id="88ec2-132">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="88ec2-132">unsignedByte</span></span>                                                | <span data-ttu-id="88ec2-133">Код операции, определенный в событии.</span><span class="sxs-lookup"><span data-stu-id="88ec2-133">The opcode defined in the event.</span></span> <span data-ttu-id="88ec2-134">Задача и код операции — это типЦиалли, используемые для определения расположения в приложении, из которого было зарегистрировано событие.</span><span class="sxs-lookup"><span data-stu-id="88ec2-134">Task and opcode are typcially used to identify the location in the application from where the event was logged.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="88ec2-135">**Поставщик**</span><span class="sxs-lookup"><span data-stu-id="88ec2-135">**Provider**</span></span>](eventschema-provider-systempropertiestype-element.md)           |                                                             | <span data-ttu-id="88ec2-136">Определяет поставщика, который зарегистрировал событие.</span><span class="sxs-lookup"><span data-stu-id="88ec2-136">Identifies the provider that logged the event.</span></span> <span data-ttu-id="88ec2-137">Атрибуты **Name** и **GUID** включаются, если поставщик использовал манифест инструментирования для определения его событий. в противном случае атрибут **евентсаурценаме** включается, если устаревший поставщик событий (с помощью API [ведения журнала событий](/windows/desktop/EventLog/event-logging) ) зарегистрировал событие.</span><span class="sxs-lookup"><span data-stu-id="88ec2-137">The **Name** and **Guid** attributes are included if the provider used an instrumentation manifest to define its events; otherwise, the **EventSourceName** attribute is included if a legacy event provider (using the [Event Logging](/windows/desktop/EventLog/event-logging) API) logged the event.</span></span><br/> |
| [<span data-ttu-id="88ec2-138">**Безопасность**</span><span class="sxs-lookup"><span data-stu-id="88ec2-138">**Security**</span></span>](eventschema-security-systempropertiestype-element.md)           |                                                             | <span data-ttu-id="88ec2-139">Указывает пользователя, который записал в журнал событие.</span><span class="sxs-lookup"><span data-stu-id="88ec2-139">Identifies the user that logged the event.</span></span><br/>                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="88ec2-140">**Задача**</span><span class="sxs-lookup"><span data-stu-id="88ec2-140">**Task**</span></span>](eventschema-task-systempropertiestype-element.md)                   | <span data-ttu-id="88ec2-141">unsignedShort</span><span class="sxs-lookup"><span data-stu-id="88ec2-141">unsignedShort</span></span>                                               | <span data-ttu-id="88ec2-142">Задача, определенная в событии.</span><span class="sxs-lookup"><span data-stu-id="88ec2-142">The task defined in the event.</span></span> <span data-ttu-id="88ec2-143">Задача и код операции обычно используются для определения расположения в приложении, из которого было зарегистрировано событие.</span><span class="sxs-lookup"><span data-stu-id="88ec2-143">Task and opcode are typically used to identify the location in the application from where the event was logged.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="88ec2-144">**TimeCreated**</span><span class="sxs-lookup"><span data-stu-id="88ec2-144">**TimeCreated**</span></span>](eventschema-timecreated-systempropertiestype-element.md)     |                                                             | <span data-ttu-id="88ec2-145">Метка времени, определяющая время записи события в журнал.</span><span class="sxs-lookup"><span data-stu-id="88ec2-145">The time stamp that identifies when the event was logged.</span></span> <span data-ttu-id="88ec2-146">Метка времени будет содержать либо атрибут **SYSTEMTIME** , либо атрибут **равтиме** .</span><span class="sxs-lookup"><span data-stu-id="88ec2-146">The time stamp will include either the **SystemTime** attribute or the **RawTime** attribute.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="88ec2-147">**Версия**</span><span class="sxs-lookup"><span data-stu-id="88ec2-147">**Version**</span></span>](schema-version-systempropertiestype-element.md)                  | <span data-ttu-id="88ec2-148">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="88ec2-148">unsignedByte</span></span>                                                | <span data-ttu-id="88ec2-149">Номер версии определения события.</span><span class="sxs-lookup"><span data-stu-id="88ec2-149">The version number of the event's definition.</span></span><br/>                                                                                                                                                                                                                                                                                     |



## <a name="attributes"></a><span data-ttu-id="88ec2-150">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="88ec2-150">Attributes</span></span>



| <span data-ttu-id="88ec2-151">Имя</span><span class="sxs-lookup"><span data-stu-id="88ec2-151">Name</span></span>              | <span data-ttu-id="88ec2-152">Тип</span><span class="sxs-lookup"><span data-stu-id="88ec2-152">Type</span></span>                                                | <span data-ttu-id="88ec2-153">Описание</span><span class="sxs-lookup"><span data-stu-id="88ec2-153">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88ec2-154">Идентификатор действия</span><span class="sxs-lookup"><span data-stu-id="88ec2-154">ActivityID</span></span>        | [<span data-ttu-id="88ec2-155">**гуидтипе**</span><span class="sxs-lookup"><span data-stu-id="88ec2-155">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="88ec2-156">Глобальный уникальный идентификатор, определяющий текущее действие.</span><span class="sxs-lookup"><span data-stu-id="88ec2-156">A globally unique identifier that identifies the current activity.</span></span> <span data-ttu-id="88ec2-157">События, опубликованные с помощью этого идентификатора, являются частью одного действия.</span><span class="sxs-lookup"><span data-stu-id="88ec2-157">The events that are published with this identifier are part of the same activity.</span></span><br/>                                                                                                                                         |
| <span data-ttu-id="88ec2-158">евентсаурценаме</span><span class="sxs-lookup"><span data-stu-id="88ec2-158">EventSourceName</span></span>   | <span data-ttu-id="88ec2-159">строка</span><span class="sxs-lookup"><span data-stu-id="88ec2-159">string</span></span>                                              | <span data-ttu-id="88ec2-160">Имя источника события, опубликовавшего событие (если источником события является устаревший API [протоколирования событий](/windows/desktop/EventLog/event-logging) ).</span><span class="sxs-lookup"><span data-stu-id="88ec2-160">The name of the event source that published the event (if the event source is from the legacy [Event Logging](/windows/desktop/EventLog/event-logging) API).</span></span><br/>                                                                                                                                                      |
| <span data-ttu-id="88ec2-161">Guid</span><span class="sxs-lookup"><span data-stu-id="88ec2-161">Guid</span></span>              | [<span data-ttu-id="88ec2-162">**гуидтипе**</span><span class="sxs-lookup"><span data-stu-id="88ec2-162">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="88ec2-163">Глобальный уникальный идентификатор, который однозначно идентифицирует поставщик.</span><span class="sxs-lookup"><span data-stu-id="88ec2-163">The globally unique identifier that uniquely identifies the provider.</span></span><br/>                                                                                                                                                                                                                        |
| <span data-ttu-id="88ec2-164">кернелтиме</span><span class="sxs-lookup"><span data-stu-id="88ec2-164">KernelTime</span></span>        | <span data-ttu-id="88ec2-165">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="88ec2-165">unsignedInt</span></span>                                         | <span data-ttu-id="88ec2-166">Затраченное время выполнения инструкций режима ядра в единицах времени ЦП.</span><span class="sxs-lookup"><span data-stu-id="88ec2-166">Elapsed execution time for kernel-mode instructions, in CPU time units.</span></span> <span data-ttu-id="88ec2-167">Если используется частный сеанс ETW, используйте значение в элементе Процессортиме.</span><span class="sxs-lookup"><span data-stu-id="88ec2-167">If you are using an ETW private session, use the value in the ProcessorTime member instead.</span></span> <span data-ttu-id="88ec2-168">Доступно только для событий, регистрируемых в файле журнала трассировки событий (ETL-файле).</span><span class="sxs-lookup"><span data-stu-id="88ec2-168">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                               |
| <span data-ttu-id="88ec2-169">Имя</span><span class="sxs-lookup"><span data-stu-id="88ec2-169">Name</span></span>              | <span data-ttu-id="88ec2-170">anyURI</span><span class="sxs-lookup"><span data-stu-id="88ec2-170">anyURI</span></span>                                              | <span data-ttu-id="88ec2-171">Имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="88ec2-171">The name of the provider.</span></span><br/>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="88ec2-172">ProcessID</span><span class="sxs-lookup"><span data-stu-id="88ec2-172">ProcessID</span></span>         | <span data-ttu-id="88ec2-173">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="88ec2-173">unsignedInt</span></span>                                         | <span data-ttu-id="88ec2-174">Указывает процесс, создавший событие.</span><span class="sxs-lookup"><span data-stu-id="88ec2-174">Identifies the process that generated the event.</span></span><br/>                                                                                                                                                                                                                                             |
| <span data-ttu-id="88ec2-175">процессорид</span><span class="sxs-lookup"><span data-stu-id="88ec2-175">ProcessorID</span></span>       | <span data-ttu-id="88ec2-176">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="88ec2-176">unsignedByte</span></span>                                        | <span data-ttu-id="88ec2-177">Идентификационный номер процессора, который обработал событие.</span><span class="sxs-lookup"><span data-stu-id="88ec2-177">The identification number for the processor that processed the event.</span></span> <span data-ttu-id="88ec2-178">Доступно только для событий, регистрируемых в файле журнала трассировки событий (ETL-файле).</span><span class="sxs-lookup"><span data-stu-id="88ec2-178">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                                                                                                                             |
| <span data-ttu-id="88ec2-179">процессортиме</span><span class="sxs-lookup"><span data-stu-id="88ec2-179">ProcessorTime</span></span>     | <span data-ttu-id="88ec2-180">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="88ec2-180">unsignedInt</span></span>                                         | <span data-ttu-id="88ec2-181">Для частных сеансов ETW — затраченное время выполнения инструкций пользовательского режима в тактах ЦП.</span><span class="sxs-lookup"><span data-stu-id="88ec2-181">For ETW private sessions, the elapsed execution time for user-mode instructions, in CPU ticks.</span></span> <span data-ttu-id="88ec2-182">Доступно только для событий, регистрируемых в файле журнала трассировки событий (ETL-файле).</span><span class="sxs-lookup"><span data-stu-id="88ec2-182">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                                                                                                    |
| <span data-ttu-id="88ec2-183">Квалификаторы</span><span class="sxs-lookup"><span data-stu-id="88ec2-183">Qualifiers</span></span>        | <span data-ttu-id="88ec2-184">**unsignedShort**</span><span class="sxs-lookup"><span data-stu-id="88ec2-184">**unsignedShort**</span></span>                                   | <span data-ttu-id="88ec2-185">Устаревший поставщик использует 32-разрядное число для обнаружения своих событий.</span><span class="sxs-lookup"><span data-stu-id="88ec2-185">A legacy provider uses a 32-bit number to identify its events.</span></span> <span data-ttu-id="88ec2-186">Если событие регистрируется устаревшим поставщиком, значение элемента **EventID** содержит 16 младших разрядов идентификатора события, а атрибут **квалификатора** содержит 16 битов идентификатора события с высоким порядковым значением.</span><span class="sxs-lookup"><span data-stu-id="88ec2-186">If the event is logged by a legacy provider, the value of **EventID** element contains the low-order 16 bits of the event identifier and the **Qualifier** attribute contains the high-order 16 bits of the event identifier.</span></span><br/> |
| <span data-ttu-id="88ec2-187">равтиме</span><span class="sxs-lookup"><span data-stu-id="88ec2-187">RawTime</span></span>           | <span data-ttu-id="88ec2-188">unsignedLong</span><span class="sxs-lookup"><span data-stu-id="88ec2-188">unsignedLong</span></span>                                        | <span data-ttu-id="88ec2-189">Значение необработанной метки времени; Формат метки времени зависит от источника времени, используемого для накопления трассировки.</span><span class="sxs-lookup"><span data-stu-id="88ec2-189">The raw time stamp value; the format of the time stamp depends on the time source used to collect the trace.</span></span> <span data-ttu-id="88ec2-190">Необработанная отметка времени обеспечивает большую точность, чем системное время.</span><span class="sxs-lookup"><span data-stu-id="88ec2-190">The raw time stamp offers higher precision than system time.</span></span> <span data-ttu-id="88ec2-191">Выходные данные отображаемого события будут содержать только необработанное время, если вы используете TraceRpt.exe с параметром-RTS.</span><span class="sxs-lookup"><span data-stu-id="88ec2-191">The rendered event output will only contain raw time if you use TraceRpt.exe with the -rts switch.</span></span><br/>                 |
| <span data-ttu-id="88ec2-192">RelatedActivityID</span><span class="sxs-lookup"><span data-stu-id="88ec2-192">RelatedActivityID</span></span> | [<span data-ttu-id="88ec2-193">**гуидтипе**</span><span class="sxs-lookup"><span data-stu-id="88ec2-193">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="88ec2-194">Глобальный уникальный идентификатор, определяющий действие, в которое был передан элемент управления.</span><span class="sxs-lookup"><span data-stu-id="88ec2-194">A globally unique identifier that identifies the activity to which control was transferred to.</span></span> <span data-ttu-id="88ec2-195">Затем связанные события будут иметь этот идентификатор в качестве идентификатора ActivityID.</span><span class="sxs-lookup"><span data-stu-id="88ec2-195">The related events would then have this identifier as their ActivityID identifier.</span></span><br/>                                                                                                            |
| <span data-ttu-id="88ec2-196">SessionID</span><span class="sxs-lookup"><span data-stu-id="88ec2-196">SessionID</span></span>         | <span data-ttu-id="88ec2-197">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="88ec2-197">unsignedInt</span></span>                                         | <span data-ttu-id="88ec2-198">Идентификационный номер сеанса сервера терминалов, в котором произошло событие.</span><span class="sxs-lookup"><span data-stu-id="88ec2-198">The identification number for the terminal server session in which the event occurred.</span></span> <span data-ttu-id="88ec2-199">Доступно только для событий, регистрируемых в файле журнала трассировки событий (ETL-файле).</span><span class="sxs-lookup"><span data-stu-id="88ec2-199">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                                                                                                            |
| <span data-ttu-id="88ec2-200">SystemTime</span><span class="sxs-lookup"><span data-stu-id="88ec2-200">SystemTime</span></span>        | <span data-ttu-id="88ec2-201">dateTime</span><span class="sxs-lookup"><span data-stu-id="88ec2-201">dateTime</span></span>                                            | <span data-ttu-id="88ec2-202">Системное время, когда событие было зарегистрировано.</span><span class="sxs-lookup"><span data-stu-id="88ec2-202">The system time of when the event was logged.</span></span><br/>                                                                                                                                                                                                                                                |
| <span data-ttu-id="88ec2-203">ThreadID</span><span class="sxs-lookup"><span data-stu-id="88ec2-203">ThreadID</span></span>          | <span data-ttu-id="88ec2-204">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="88ec2-204">unsignedInt</span></span>                                         | <span data-ttu-id="88ec2-205">Указывает поток, создавший событие.</span><span class="sxs-lookup"><span data-stu-id="88ec2-205">Identifies the thread that generated the event.</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="88ec2-206">UserID</span><span class="sxs-lookup"><span data-stu-id="88ec2-206">UserID</span></span>            | <span data-ttu-id="88ec2-207">строка</span><span class="sxs-lookup"><span data-stu-id="88ec2-207">string</span></span>                                              | <span data-ttu-id="88ec2-208">Идентификатор безопасности (SID) пользователя в строковой форме.</span><span class="sxs-lookup"><span data-stu-id="88ec2-208">The security identifier (SID) of the user in string form.</span></span><br/>                                                                                                                                                                                                                                    |
| <span data-ttu-id="88ec2-209">усертиме</span><span class="sxs-lookup"><span data-stu-id="88ec2-209">UserTime</span></span>          | <span data-ttu-id="88ec2-210">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="88ec2-210">unsignedInt</span></span>                                         | <span data-ttu-id="88ec2-211">Затраченное время выполнения инструкций пользовательского режима в единицах времени ЦП.</span><span class="sxs-lookup"><span data-stu-id="88ec2-211">Elapsed execution time for user-mode instructions, in CPU time units.</span></span> <span data-ttu-id="88ec2-212">Если используется частный сеанс ETW, используйте значение в элементе Процессортиме.</span><span class="sxs-lookup"><span data-stu-id="88ec2-212">If you are using an ETW private session, use the value in the ProcessorTime member instead.</span></span> <span data-ttu-id="88ec2-213">Доступно только для событий, регистрируемых в файле журнала трассировки событий (ETL-файле).</span><span class="sxs-lookup"><span data-stu-id="88ec2-213">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                                 |



## <a name="remarks"></a><span data-ttu-id="88ec2-214">Комментарии</span><span class="sxs-lookup"><span data-stu-id="88ec2-214">Remarks</span></span>

<span data-ttu-id="88ec2-215">По умолчанию событие содержит полное доменное имя (FQDN) компьютера.</span><span class="sxs-lookup"><span data-stu-id="88ec2-215">By default, the event contains the fully qualified domain name (FQDN) of a computer.</span></span> <span data-ttu-id="88ec2-216">Чтобы использовать NETBIOS-имя, а не полное доменное имя, необходимо создать параметр реестра DWORD с именем Компатфлагс в следующем разделе реестра и присвоить параметру Компатфлагс значение 0x2.</span><span class="sxs-lookup"><span data-stu-id="88ec2-216">To use the NETBIOS name rather than the FQDN, you must create a DWORD registry value named CompatFlags under the following registry key, and set the value of CompatFlags to 0x2.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               WINEVT
```

## <a name="requirements"></a><span data-ttu-id="88ec2-217">Требования</span><span class="sxs-lookup"><span data-stu-id="88ec2-217">Requirements</span></span>



| <span data-ttu-id="88ec2-218">Требование</span><span class="sxs-lookup"><span data-stu-id="88ec2-218">Requirement</span></span> | <span data-ttu-id="88ec2-219">Значение</span><span class="sxs-lookup"><span data-stu-id="88ec2-219">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="88ec2-220">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="88ec2-220">Minimum supported client</span></span><br/> | <span data-ttu-id="88ec2-221">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="88ec2-221">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="88ec2-222">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="88ec2-222">Minimum supported server</span></span><br/> | <span data-ttu-id="88ec2-223">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="88ec2-223">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

