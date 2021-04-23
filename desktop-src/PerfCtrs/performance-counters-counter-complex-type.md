---
description: Определяет счетчик.
ms.assetid: 8f1338c0-7ea6-4d0c-af71-51012973e4a0
title: Сложный тип счетчика
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d591d4c23b626eaf2e2bfb10b528ff7c054507df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663204"
---
# <a name="counter-complex-type"></a><span data-ttu-id="31bbc-103">Сложный тип счетчика</span><span class="sxs-lookup"><span data-stu-id="31bbc-103">counter Complex Type</span></span>

<span data-ttu-id="31bbc-104">Определяет счетчик.</span><span class="sxs-lookup"><span data-stu-id="31bbc-104">Defines a counter.</span></span>

``` syntax
<xs:complexType name="counter">
    <xs:choice
        minOccurs="0"
        maxOccurs="1"
    >
        <xs:element name="counterAttributes"
            type="man:counterAttributes"
        >
            <xs:key name="uniqueCounterAttributeName">
                <xs:selector
                    xpath="./man:counterAttribute"
                 />
                <xs:field
                    xpath="@name"
                 />
            </xs:key>
        </xs:element>
    </xs:choice>
    <xs:attribute name="symbol"
        type="man:CSymbolType"
        use="optional"
     />
    <xs:attribute name="id"
        type="man:UInt32Type"
        use="required"
     />
    <xs:attribute name="uri"
        type="xs:anyURI"
        use="required"
     />
    <xs:attribute name="name"
        use="optional"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:maxLength
                    value="1023"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="description"
        type="xs:string"
        use="optional"
     />
    <xs:attribute name="type"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="perf_counter_counter"
                 />
                <xs:enumeration
                    value="perf_counter_timer"
                 />
                <xs:enumeration
                    value="perf_counter_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_large_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_100ns_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_obj_time_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_bulk_count"
                 />
                <xs:enumeration
                    value="perf_counter_text"
                 />
                <xs:enumeration
                    value="perf_counter_rawcount"
                 />
                <xs:enumeration
                    value="perf_counter_large_rawcount"
                 />
                <xs:enumeration
                    value="perf_counter_rawcount_hex"
                 />
                <xs:enumeration
                    value="perf_counter_large_rawcount_hex"
                 />
                <xs:enumeration
                    value="perf_sample_fraction"
                 />
                <xs:enumeration
                    value="perf_sample_counter"
                 />
                <xs:enumeration
                    value="perf_counter_timer_inv"
                 />
                <xs:enumeration
                    value="perf_sample_base"
                 />
                <xs:enumeration
                    value="perf_average_timer"
                 />
                <xs:enumeration
                    value="perf_average_base"
                 />
                <xs:enumeration
                    value="perf_average_bulk"
                 />
                <xs:enumeration
                    value="perf_obj_time_timer"
                 />
                <xs:enumeration
                    value="perf_100nsec_timer"
                 />
                <xs:enumeration
                    value="perf_100nsec_timer_inv"
                 />
                <xs:enumeration
                    value="perf_counter_multi_timer"
                 />
                <xs:enumeration
                    value="perf_counter_multi_timer_inv"
                 />
                <xs:enumeration
                    value="perf_counter_multi_base"
                 />
                <xs:enumeration
                    value="perf_100nsec_multi_timer"
                 />
                <xs:enumeration
                    value="perf_100nsec_multi_timer_inv"
                 />
                <xs:enumeration
                    value="perf_raw_fraction"
                 />
                <xs:enumeration
                    value="perf_large_raw_fraction"
                 />
                <xs:enumeration
                    value="perf_raw_base"
                 />
                <xs:enumeration
                    value="perf_large_raw_base"
                 />
                <xs:enumeration
                    value="perf_elapsed_time"
                 />
                <xs:enumeration
                    value="perf_counter_delta"
                 />
                <xs:enumeration
                    value="perf_counter_large_delta"
                 />
                <xs:enumeration
                    value="perf_precision_system_timer"
                 />
                <xs:enumeration
                    value="perf_precision_100ns_timer"
                 />
                <xs:enumeration
                    value="perf_precision_object_timer"
                 />
                <xs:enumeration
                    value="perf_counter_composite"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="baseID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="detailLevel"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="standard"
                 />
                <xs:enumeration
                    value="advanced"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="defaultScale"
        use="optional"
        default="0"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:integer"
            >
                <xs:minInclusive
                    value="-10"
                 />
                <xs:maxInclusive
                    value="10"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="aggregate"
        use="optional"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="sum"
                 />
                <xs:enumeration
                    value="avg"
                 />
                <xs:enumeration
                    value="max"
                 />
                <xs:enumeration
                    value="min"
                 />
                <xs:enumeration
                    value="undefined"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="perfTimeID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="perfFreqID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="multiCounterID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="struct"
        type="man:CSymbolType"
        use="optional"
     />
    <xs:attribute name="field"
        type="man:CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="31bbc-105">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="31bbc-105">Child elements</span></span>



| <span data-ttu-id="31bbc-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="31bbc-106">Element</span></span>               | <span data-ttu-id="31bbc-107">Тип</span><span class="sxs-lookup"><span data-stu-id="31bbc-107">Type</span></span>                                                                                 | <span data-ttu-id="31bbc-108">Описание</span><span class="sxs-lookup"><span data-stu-id="31bbc-108">Description</span></span>                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31bbc-109">**каунтераттрибутес**</span><span class="sxs-lookup"><span data-stu-id="31bbc-109">**counterAttributes**</span></span> | [<span data-ttu-id="31bbc-110">**мужчина: Каунтераттрибутес**</span><span class="sxs-lookup"><span data-stu-id="31bbc-110">**man:counterAttributes**</span></span>](performance-counters-counterattributes-complex-type.md) | <span data-ttu-id="31bbc-111">Перечисляет уникальные атрибуты, указывающие, как данные счетчика отображаются в приложении-потребителе.</span><span class="sxs-lookup"><span data-stu-id="31bbc-111">Lists the unique attributes that specify how the counter data is displayed in a consumer application.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="31bbc-112">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="31bbc-112">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="31bbc-113">Имя</span><span class="sxs-lookup"><span data-stu-id="31bbc-113">Name</span></span></th>
<th><span data-ttu-id="31bbc-114">Тип</span><span class="sxs-lookup"><span data-stu-id="31bbc-114">Type</span></span></th>
<th><span data-ttu-id="31bbc-115">Описание</span><span class="sxs-lookup"><span data-stu-id="31bbc-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="31bbc-116">статистическое выражение</span><span class="sxs-lookup"><span data-stu-id="31bbc-116">aggregate</span></span></td>

<td><span data-ttu-id="31bbc-117">Статистическая функция, применяемая, если атрибут <strong>Instances</strong> набора <a href="performance-counters-counterset-complex-type.md"><strong>счетчиков</strong></a> — Глобалаггрегате, мултиплеаггрегате или глобалаггрегатехистори.</span><span class="sxs-lookup"><span data-stu-id="31bbc-117">The aggregation function to apply if the <strong>instances</strong> attribute of <a href="performance-counters-counterset-complex-type.md"><strong>counterSet</strong></a> is globalAggregate, multipleAggregate, or globalAggregateHistory.</span></span> <span data-ttu-id="31bbc-118">Ниже приведены возможные статистические функции, которые можно применять.</span><span class="sxs-lookup"><span data-stu-id="31bbc-118">The following are the possible aggregation functions that you can apply:</span></span><br/> <dl> <span data-ttu-id="31bbc-119"><dt><span id="max"></span><span id="MAX"></span>максимальной</dt> </span><span class="sxs-lookup"><span data-stu-id="31bbc-119"><dt><span id="max"></span><span id="MAX"></span>max</dt> </span></span><dd> <span data-ttu-id="31bbc-120">Возвращается максимальное значение счетчика.</span><span class="sxs-lookup"><span data-stu-id="31bbc-120">The maximum counter value is returned.</span></span><br/> </dd> <span data-ttu-id="31bbc-121"><dt><span id="min"></span><span id="MIN"></span>минимум</dt> </span><span class="sxs-lookup"><span data-stu-id="31bbc-121"><dt><span id="min"></span><span id="MIN"></span>min</dt> </span></span><dd> <span data-ttu-id="31bbc-122">Возвращается минимальное значение счетчика.</span><span class="sxs-lookup"><span data-stu-id="31bbc-122">The minimum counter value is returned.</span></span><br/> </dd> <span data-ttu-id="31bbc-123"><dt><span id="avg"></span><span id="AVG"></span>обращения</dt> </span><span class="sxs-lookup"><span data-stu-id="31bbc-123"><dt><span id="avg"></span><span id="AVG"></span>avg</dt> </span></span><dd> <span data-ttu-id="31bbc-124">Возвращается среднее значение счетчика.</span><span class="sxs-lookup"><span data-stu-id="31bbc-124">The average counter value is returned.</span></span><br/> </dd> <span data-ttu-id="31bbc-125"><dt><span id="sum"></span><span id="SUM"></span>функции</dt> </span><span class="sxs-lookup"><span data-stu-id="31bbc-125"><dt><span id="sum"></span><span id="SUM"></span>sum</dt> </span></span><dd> <span data-ttu-id="31bbc-126">Возвращается сумма значений счетчика.</span><span class="sxs-lookup"><span data-stu-id="31bbc-126">The sum of the counter values is returned.</span></span><br/> </dd> <span data-ttu-id="31bbc-127"><dt><span id="undefined"></span><span id="UNDEFINED"></span>определено</dt> </span><span class="sxs-lookup"><span data-stu-id="31bbc-127"><dt><span id="undefined"></span><span id="UNDEFINED"></span>undefined</dt> </span></span><dd> <span data-ttu-id="31bbc-128">Не вычислять этот счетчик.</span><span class="sxs-lookup"><span data-stu-id="31bbc-128">Do not aggregate this counter.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31bbc-129">басеид</span><span class="sxs-lookup"><span data-stu-id="31bbc-129">baseID</span></span></td>
<td><span data-ttu-id="31bbc-130"><a href="performance-counters-uint32type-simple-type.md"><strong>мужчина: UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="31bbc-130"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="31bbc-131">Идентификатор другого счетчика в том же наборе счетчиков, значение которого используется для вычисления значения этого счетчика.</span><span class="sxs-lookup"><span data-stu-id="31bbc-131">The identifier of another counter within the same counter set, whose value is used to calculate this counter's value.</span></span> <span data-ttu-id="31bbc-132">Базовый счетчик требуется для следующих типов счетчиков:</span><span class="sxs-lookup"><span data-stu-id="31bbc-132">The following counter types require a base counter:</span></span><br/> <dl> <span data-ttu-id="31bbc-133"><dt><span id="PERF_AVERAGE_TIMER"></span><span id="perf_average_timer"></span>PERF_AVERAGE_TIMER</dt> </span><span class="sxs-lookup"><span data-stu-id="31bbc-133"><dt><span id="PERF_AVERAGE_TIMER"></span><span id="perf_average_timer"></span>PERF_AVERAGE_TIMER</dt> </span></span><dd> <span data-ttu-id="31bbc-134">Требуется базовый счетчик PERF_AVERAGE_BASE.</span><span class="sxs-lookup"><span data-stu-id="31bbc-134">Requires the PERF_AVERAGE_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="31bbc-135"><dt><span id="PERF_AVERAGE_BULK"></span><span id="perf_average_bulk"></span>PERF_AVERAGE_BULK</dt> </span><span class="sxs-lookup"><span data-stu-id="31bbc-135"><dt><span id="PERF_AVERAGE_BULK"></span><span id="perf_average_bulk"></span>PERF_AVERAGE_BULK</dt> </span></span><dd> <span data-ttu-id="31bbc-136">Требуется базовый счетчик PERF_AVERAGE_BASE.</span><span class="sxs-lookup"><span data-stu-id="31bbc-136">Requires the PERF_AVERAGE_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="31bbc-137"><dt><span id="PERF_COUNTER_MULTI_TIMER_INV"></span><span id="perf_counter_multi_timer_inv"></span>PERF_COUNTER_MULTI_TIMER_INV</dt> </span><span class="sxs-lookup"><span data-stu-id="31bbc-137"><dt><span id="PERF_COUNTER_MULTI_TIMER_INV"></span><span id="perf_counter_multi_timer_inv"></span>PERF_COUNTER_MULTI_TIMER_INV</dt> </span></span><dd> <span data-ttu-id="31bbc-138">Требуется базовый счетчик PERF_COUNTER_MULTI_BASE.</span><span class="sxs-lookup"><span data-stu-id="31bbc-138">Requires the PERF_COUNTER_MULTI_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="31bbc-139"><dt><span id="PERF_LARGE_RAW_FRACTION"></span><span id="perf_large_raw_fraction"></span>PERF_LARGE_RAW_FRACTION</dt> </span><span class="sxs-lookup"><span data-stu-id="31bbc-139"><dt><span id="PERF_LARGE_RAW_FRACTION"></span><span id="perf_large_raw_fraction"></span>PERF_LARGE_RAW_FRACTION</dt> </span></span><dd> <span data-ttu-id="31bbc-140">Требуется базовый счетчик PERF_LARGE_RAW_BASE.</span><span class="sxs-lookup"><span data-stu-id="31bbc-140">Requires the PERF_LARGE_RAW_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="31bbc-141"><dt><span id="PERF_PRECISION_100NS_TIMER"></span><span id="perf_precision_100ns_timer"></span>PERF_PRECISION_100NS_TIMER</dt> </span><span class="sxs-lookup"><span data-stu-id="31bbc-141"><dt><span id="PERF_PRECISION_100NS_TIMER"></span><span id="perf_precision_100ns_timer"></span>PERF_PRECISION_100NS_TIMER</dt> </span></span><dd> <span data-ttu-id="31bbc-142">Требуется базовый счетчик PERF_LARGE_RAW_BASE.</span><span class="sxs-lookup"><span data-stu-id="31bbc-142">Requires the PERF_LARGE_RAW_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="31bbc-143"><dt><span id="PERF_RAW_FRACTION"></span><span id="perf_raw_fraction"></span>PERF_RAW_FRACTION</dt> </span><span class="sxs-lookup"><span data-stu-id="31bbc-143"><dt><span id="PERF_RAW_FRACTION"></span><span id="perf_raw_fraction"></span>PERF_RAW_FRACTION</dt> </span></span><dd> <span data-ttu-id="31bbc-144">Требуется базовый счетчик PERF_RAW_BASE.</span><span class="sxs-lookup"><span data-stu-id="31bbc-144">Requires the PERF_RAW_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="31bbc-145"><dt><span id="PERF_SAMPLE_FRACTION"></span><span id="perf_sample_fraction"></span>PERF_SAMPLE_FRACTION</dt> </span><span class="sxs-lookup"><span data-stu-id="31bbc-145"><dt><span id="PERF_SAMPLE_FRACTION"></span><span id="perf_sample_fraction"></span>PERF_SAMPLE_FRACTION</dt> </span></span><dd> <span data-ttu-id="31bbc-146">Требуется базовый счетчик PERF_SAMPLE_BASE.</span><span class="sxs-lookup"><span data-stu-id="31bbc-146">Requires the PERF_SAMPLE_BASE base counter.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31bbc-147">дефаултскале</span><span class="sxs-lookup"><span data-stu-id="31bbc-147">defaultScale</span></span></td>

<td><span data-ttu-id="31bbc-148">Коэффициент масштабирования, применяемый к значению счетчика (значение счетчика коэффициента \*).</span><span class="sxs-lookup"><span data-stu-id="31bbc-148">The scale factor to apply to the counter value (factor \* counter value).</span></span> <span data-ttu-id="31bbc-149">Значение по умолчанию равно нулю, если масштабирование не применяется.</span><span class="sxs-lookup"><span data-stu-id="31bbc-149">The default is zero if no scale is applied.</span></span> <span data-ttu-id="31bbc-150">Диапазон допустимых значений — от 10 до 10 (0,0000000001 до 1000000000).</span><span class="sxs-lookup"><span data-stu-id="31bbc-150">Valid values range from  10 to 10 (0.0000000001 to 1000000000).</span></span> <span data-ttu-id="31bbc-151">Если это значение равно нулю, значение масштаба равно 1; Если это значение равно 1, значение масштаба равно 10; Если это значение равно 1, масштаб имеет значение. 10; и т. д.</span><span class="sxs-lookup"><span data-stu-id="31bbc-151">If this value is zero, the scale value is 1; if this value is 1, the scale value is 10; if this value is  1, the scale value is .10; and so on.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31bbc-152">description;</span><span class="sxs-lookup"><span data-stu-id="31bbc-152">description</span></span></td>
<td><span data-ttu-id="31bbc-153"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="31bbc-153"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="31bbc-154">Краткое описание счетчика.</span><span class="sxs-lookup"><span data-stu-id="31bbc-154">A short description of the counter.</span></span> <span data-ttu-id="31bbc-155">Не нужно указывать этот атрибут, если счетчик содержит атрибут «не <a href="performance-counters-counterattribute-complex-type.md"><strong>Показывать</strong></a> ».</span><span class="sxs-lookup"><span data-stu-id="31bbc-155">You do not have to specify this attribute if the counter includes the <a href="performance-counters-counterattribute-complex-type.md"><strong>noDisplay</strong></a> attribute.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31bbc-156">detailLevel</span><span class="sxs-lookup"><span data-stu-id="31bbc-156">detailLevel</span></span></td>

<td><span data-ttu-id="31bbc-157">Указывает целевую аудиторию для сведений о счетчике.</span><span class="sxs-lookup"><span data-stu-id="31bbc-157">Specifies the target audience for the counter details.</span></span> <span data-ttu-id="31bbc-158">Допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="31bbc-158">The following are the possible values:</span></span><br/> <dl> <span data-ttu-id="31bbc-159"><dt><span id="standard"></span><span id="STANDARD"></span>Standard</dt> </span><span class="sxs-lookup"><span data-stu-id="31bbc-159"><dt><span id="standard"></span><span id="STANDARD"></span>standard</dt> </span></span><dd> <span data-ttu-id="31bbc-160">Отображение сведений о счетчике, который будет распознать обычный пользователь.</span><span class="sxs-lookup"><span data-stu-id="31bbc-160">Display details about the counter that a typical user would understand.</span></span><br/> </dd> <span data-ttu-id="31bbc-161"><dt><span id="advanced"></span><span id="ADVANCED"></span>продвинут</dt> </span><span class="sxs-lookup"><span data-stu-id="31bbc-161"><dt><span id="advanced"></span><span id="ADVANCED"></span>advanced</dt> </span></span><dd> <span data-ttu-id="31bbc-162">Отображение сведений о счетчике, который будет понятен только опытному пользователю.</span><span class="sxs-lookup"><span data-stu-id="31bbc-162">Display details about the counter that only an advanced user would understand.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31bbc-163">поле</span><span class="sxs-lookup"><span data-stu-id="31bbc-163">field</span></span></td>
<td><span data-ttu-id="31bbc-164"><a href="performance-counters-csymboltype-simple-type.md"><strong>мужчина: Ксимболтипе</strong></a></span><span class="sxs-lookup"><span data-stu-id="31bbc-164"><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></span></span></td>
<td><span data-ttu-id="31bbc-165">Имя поля в структуре, которое содержит значение счетчика.</span><span class="sxs-lookup"><span data-stu-id="31bbc-165">The name of a field within the struct that contains the counter value.</span></span> <span data-ttu-id="31bbc-166">Этот атрибут не разрешен для поставщиков пользовательского режима.</span><span class="sxs-lookup"><span data-stu-id="31bbc-166">This attribute is not allowed for user-mode providers.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31bbc-167">идентификатор</span><span class="sxs-lookup"><span data-stu-id="31bbc-167">id</span></span></td>
<td><span data-ttu-id="31bbc-168"><a href="performance-counters-uint32type-simple-type.md"><strong>мужчина: UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="31bbc-168"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="31bbc-169">Уникальный номер, определяющий счетчик в наборе счетчиков.</span><span class="sxs-lookup"><span data-stu-id="31bbc-169">A unique number that identifies the counter within the counter set.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31bbc-170">мултикаунтерид</span><span class="sxs-lookup"><span data-stu-id="31bbc-170">multiCounterID</span></span></td>
<td><span data-ttu-id="31bbc-171"><a href="performance-counters-uint32type-simple-type.md"><strong>мужчина: UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="31bbc-171"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="31bbc-172">Идентификатор другого счетчика в том же наборе счетчиков, значение множителя которого используется для вычисления значения этого счетчика.</span><span class="sxs-lookup"><span data-stu-id="31bbc-172">The identifier of another counter within the same counter set, whose multiplier value is used to calculate this counter's value.</span></span> <span data-ttu-id="31bbc-173">Для следующих типов счетчиков требуется значение множителя.</span><span class="sxs-lookup"><span data-stu-id="31bbc-173">The following counter types require a multiplier value.</span></span> <span data-ttu-id="31bbc-174">Указанный счетчик должен иметь тип PERF_COUNTER_RAWCOUNT.</span><span class="sxs-lookup"><span data-stu-id="31bbc-174">The referenced counter must be of type PERF_COUNTER_RAWCOUNT.</span></span><br/>
<ul>
<li><span data-ttu-id="31bbc-175">PERF_COUNTER_MULTI_TIMER</span><span class="sxs-lookup"><span data-stu-id="31bbc-175">PERF_COUNTER_MULTI_TIMER</span></span></li>
<li><span data-ttu-id="31bbc-176">PERF_COUNTER_MULTI_TIMER_INV</span><span class="sxs-lookup"><span data-stu-id="31bbc-176">PERF_COUNTER_MULTI_TIMER_INV</span></span></li>
<li><span data-ttu-id="31bbc-177">PERF_100NSEC_MULTI_TIMER</span><span class="sxs-lookup"><span data-stu-id="31bbc-177">PERF_100NSEC_MULTI_TIMER</span></span></li>
<li><span data-ttu-id="31bbc-178">PERF_100NSEC_MULTI_TIMER_INV</span><span class="sxs-lookup"><span data-stu-id="31bbc-178">PERF_100NSEC_MULTI_TIMER_INV</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31bbc-179">name</span><span class="sxs-lookup"><span data-stu-id="31bbc-179">name</span></span></td>

<td><span data-ttu-id="31bbc-180">Имя счетчика.</span><span class="sxs-lookup"><span data-stu-id="31bbc-180">The name of the counter.</span></span> <span data-ttu-id="31bbc-181">Имя должно быть уникальным и содержать менее 1 024 символов.</span><span class="sxs-lookup"><span data-stu-id="31bbc-181">The name must be unique and less than 1,024 characters.</span></span> <span data-ttu-id="31bbc-182">В нем учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="31bbc-182">The name is case-sensitive.</span></span> <span data-ttu-id="31bbc-183">Не нужно указывать этот атрибут, если счетчик содержит атрибут «не <a href="performance-counters-counterattribute-complex-type.md"><strong>Показывать</strong></a> ».</span><span class="sxs-lookup"><span data-stu-id="31bbc-183">You do not have to specify this attribute if the counter includes the <a href="performance-counters-counterattribute-complex-type.md"><strong>noDisplay</strong></a> attribute.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31bbc-184">перффрекид</span><span class="sxs-lookup"><span data-stu-id="31bbc-184">perfFreqID</span></span></td>
<td><span data-ttu-id="31bbc-185"><a href="performance-counters-uint32type-simple-type.md"><strong>мужчина: UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="31bbc-185"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="31bbc-186">Идентификатор другого счетчика в том же наборе счетчиков, значение частоты которого используется для вычисления значения этого счетчика.</span><span class="sxs-lookup"><span data-stu-id="31bbc-186">The identifier of another counter within the same counter set, whose frequency value is used to calculate this counter's value.</span></span> <span data-ttu-id="31bbc-187">Для следующих типов счетчиков требуется частота.</span><span class="sxs-lookup"><span data-stu-id="31bbc-187">The following counter types require a frequency.</span></span> <span data-ttu-id="31bbc-188">Тип счетчика PERF_COUNTER_LARGE_RAWCOUNT содержит значение метки времени.</span><span class="sxs-lookup"><span data-stu-id="31bbc-188">The PERF_COUNTER_LARGE_RAWCOUNT counter type contains the time stamp value.</span></span><br/>
<ul>
<li><span data-ttu-id="31bbc-189">PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</span><span class="sxs-lookup"><span data-stu-id="31bbc-189">PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</span></span></li>
<li><span data-ttu-id="31bbc-190">PERF_ELAPSED_TIME</span><span class="sxs-lookup"><span data-stu-id="31bbc-190">PERF_ELAPSED_TIME</span></span></li>
<li><span data-ttu-id="31bbc-191">PERF_OBJ_TIME_TIMER</span><span class="sxs-lookup"><span data-stu-id="31bbc-191">PERF_OBJ_TIME_TIMER</span></span></li>
<li><span data-ttu-id="31bbc-192">PERF_PRECISION_OBJECT_TIMER</span><span class="sxs-lookup"><span data-stu-id="31bbc-192">PERF_PRECISION_OBJECT_TIMER</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31bbc-193">перфтимеид</span><span class="sxs-lookup"><span data-stu-id="31bbc-193">perfTimeID</span></span></td>
<td><span data-ttu-id="31bbc-194"><a href="performance-counters-uint32type-simple-type.md"><strong>мужчина: UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="31bbc-194"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="31bbc-195">Идентификатор другого счетчика в том же наборе счетчиков, значение метки времени которого используется для вычисления значения этого счетчика.</span><span class="sxs-lookup"><span data-stu-id="31bbc-195">The identifier of another counter within the same counter set, whose time stamp value is used to calculate this counter's value.</span></span> <span data-ttu-id="31bbc-196">Для следующих типов счетчиков требуется метка времени.</span><span class="sxs-lookup"><span data-stu-id="31bbc-196">The following counter types require a time stamp.</span></span> <span data-ttu-id="31bbc-197">Тип счетчика PERF_COUNTER_LARGE_RAWCOUNT содержит значение метки времени.</span><span class="sxs-lookup"><span data-stu-id="31bbc-197">The PERF_COUNTER_LARGE_RAWCOUNT counter type contains the time stamp value.</span></span><br/>
<ul>
<li><span data-ttu-id="31bbc-198">PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</span><span class="sxs-lookup"><span data-stu-id="31bbc-198">PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</span></span></li>
<li><span data-ttu-id="31bbc-199">PERF_ELAPSED_TIME</span><span class="sxs-lookup"><span data-stu-id="31bbc-199">PERF_ELAPSED_TIME</span></span></li>
<li><span data-ttu-id="31bbc-200">PERF_OBJ_TIME_TIMER</span><span class="sxs-lookup"><span data-stu-id="31bbc-200">PERF_OBJ_TIME_TIMER</span></span></li>
<li><span data-ttu-id="31bbc-201">PERF_PRECISION_OBJECT_TIMER</span><span class="sxs-lookup"><span data-stu-id="31bbc-201">PERF_PRECISION_OBJECT_TIMER</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31bbc-202">struct</span><span class="sxs-lookup"><span data-stu-id="31bbc-202">struct</span></span></td>
<td><span data-ttu-id="31bbc-203"><a href="performance-counters-csymboltype-simple-type.md"><strong>мужчина: Ксимболтипе</strong></a></span><span class="sxs-lookup"><span data-stu-id="31bbc-203"><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></span></span></td>
<td><span data-ttu-id="31bbc-204">Имя элемента структуры, который содержит значение этого счетчика.</span><span class="sxs-lookup"><span data-stu-id="31bbc-204">The name of a struct element that contains this counter value.</span></span> <span data-ttu-id="31bbc-205">Этот атрибут не разрешен для поставщиков пользовательского режима.</span><span class="sxs-lookup"><span data-stu-id="31bbc-205">This attribute is not allowed for user-mode providers.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31bbc-206">символ</span><span class="sxs-lookup"><span data-stu-id="31bbc-206">symbol</span></span></td>
<td><span data-ttu-id="31bbc-207"><a href="performance-counters-csymboltype-simple-type.md"><strong>мужчина: Ксимболтипе</strong></a></span><span class="sxs-lookup"><span data-stu-id="31bbc-207"><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></span></span></td>
<td><span data-ttu-id="31bbc-208">Символьное имя, идентифицирующее счетчик.</span><span class="sxs-lookup"><span data-stu-id="31bbc-208">A symbolic name that identifies the counter.</span></span> <span data-ttu-id="31bbc-209">Средство <a href="ctrpp.md">КТРПП</a> создает константу, которую можно использовать при вызове функций, для которых требуется идентификатор счетчика (например, <a href="/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue"><strong>перфинкрементулонгкаунтервалуе</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="31bbc-209">The <a href="ctrpp.md">CTRPP</a> tool creates a constant that you can use when calling functions that require a counter identifier (for example, <a href="/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue"><strong>PerfIncrementULongCounterValue</strong></a>).</span></span> <span data-ttu-id="31bbc-210">Имя константы — это символьное имя.</span><span class="sxs-lookup"><span data-stu-id="31bbc-210">The name of the constant is the symbolic name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31bbc-211">тип</span><span class="sxs-lookup"><span data-stu-id="31bbc-211">type</span></span></td>

<td><span data-ttu-id="31bbc-212">Имя типа счетчика.</span><span class="sxs-lookup"><span data-stu-id="31bbc-212">The name of the counter type.</span></span> <span data-ttu-id="31bbc-213">Возможные значения см. в приведенном выше блоке синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="31bbc-213">For possible values, see the above syntax block.</span></span> <span data-ttu-id="31bbc-214">Дополнительные сведения о каждом типе см. в разделе <a href="/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)">типы счетчиков</a> в руководству по развертыванию Windows 2003.</span><span class="sxs-lookup"><span data-stu-id="31bbc-214">For details of each type, see <a href="/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)">Counter Types</a> in the Windows 2003 Deployment Guide.</span></span> <span data-ttu-id="31bbc-215">Имя чувствительно к регистру. Используйте нижний регистр.</span><span class="sxs-lookup"><span data-stu-id="31bbc-215">The name is case-sensitive use lowercase.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31bbc-216">uri</span><span class="sxs-lookup"><span data-stu-id="31bbc-216">uri</span></span></td>
<td><span data-ttu-id="31bbc-217"><strong>xs: anyURI</strong></span><span class="sxs-lookup"><span data-stu-id="31bbc-217"><strong>xs:anyURI</strong></span></span></td>
<td><span data-ttu-id="31bbc-218">Уникальный универсальный идентификатор ресурса, позволяющий пользователям получать значения счетчиков из любого расположения.</span><span class="sxs-lookup"><span data-stu-id="31bbc-218">A unique uniform resource identifier that lets users retrieve counter values from any location.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="31bbc-219">Комментарии</span><span class="sxs-lookup"><span data-stu-id="31bbc-219">Remarks</span></span>

<span data-ttu-id="31bbc-220">Для обеспечения обратной совместимости каждый счетчик в наборе счетчиков должен указывать одни и те же значения **перффрекид** и **перфтимеид** .</span><span class="sxs-lookup"><span data-stu-id="31bbc-220">To provide backwards-compatibility, each counter in the counter set should specify the same **perfFreqID** and **perfTimeID** values.</span></span>

## <a name="requirements"></a><span data-ttu-id="31bbc-221">Требования</span><span class="sxs-lookup"><span data-stu-id="31bbc-221">Requirements</span></span>



| <span data-ttu-id="31bbc-222">Требование</span><span class="sxs-lookup"><span data-stu-id="31bbc-222">Requirement</span></span> | <span data-ttu-id="31bbc-223">Значение</span><span class="sxs-lookup"><span data-stu-id="31bbc-223">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="31bbc-224">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="31bbc-224">Minimum supported client</span></span><br/> | <span data-ttu-id="31bbc-225">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="31bbc-225">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="31bbc-226">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="31bbc-226">Minimum supported server</span></span><br/> | <span data-ttu-id="31bbc-227">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="31bbc-227">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

