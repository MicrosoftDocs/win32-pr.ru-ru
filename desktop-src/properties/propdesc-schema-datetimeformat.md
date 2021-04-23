---
description: 'Указывает, как Ипропертидескриптион:: Форматфордисплай должен форматировать значение свойства в виде строки. Это применимо только в том случае <displayInfo displayType=&\#0034;DateTime&\#0034;> , если.'
ms.assetid: c290fb2e-ef5b-4dea-ba42-7c9e273a89dc
title: dateTimeFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 091898f77f4dcc37bbe65515f8606104a4d968bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263878"
---
# <a name="datetimeformat"></a><span data-ttu-id="84ff3-104">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="84ff3-104">dateTimeFormat</span></span>

<span data-ttu-id="84ff3-105">Указывает, как [**ипропертидескриптион:: форматфордисплай**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) должен форматировать значение свойства в виде строки.</span><span class="sxs-lookup"><span data-stu-id="84ff3-105">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="84ff3-106">Это применимо только в том случае <displayInfo displayType="DateTime"> , если.</span><span class="sxs-lookup"><span data-stu-id="84ff3-106">This is applicable only if <displayInfo displayType="DateTime">.</span></span> <span data-ttu-id="84ff3-107">Для каждого элемента [displayInfo](./propdesc-schema-displayinfo.md) должен быть только один элемент [DateTimeFormat]() .</span><span class="sxs-lookup"><span data-stu-id="84ff3-107">There should be only one [dateTimeFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="84ff3-108">При наличии нескольких элементов используется последний из них.</span><span class="sxs-lookup"><span data-stu-id="84ff3-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="84ff3-109">Если элемент [DateTimeFormat]() не указан, к описанию свойства применяются параметры атрибута по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="84ff3-109">If no [dateTimeFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="84ff3-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84ff3-110">Syntax</span></span>


```
      <!-- dateTimeFormat -->
      <xs:element name="dateTimeFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="General"/>
                <xs:enumeration value="Month"/>
                <xs:enumeration value="YearMonth"/>
                <xs:enumeration value="Year"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatTimeAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="ShortTime"/>
                <xs:enumeration value="LongTime"/>
                <xs:enumeration value="HideTime"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatDateAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="ShortDate"/>
                <xs:enumeration value="LongDate"/>
                <xs:enumeration value="HideDate"/>
                <xs:enumeration value="RelativeShortDate"/>
                <xs:enumeration value="RelativeLongDate"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
        </xs:complexType>
      </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="84ff3-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="84ff3-111">Element Information</span></span>



| <span data-ttu-id="84ff3-112">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="84ff3-112">Parent Element</span></span>                                   | <span data-ttu-id="84ff3-113">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="84ff3-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="84ff3-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="84ff3-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="84ff3-115">Нет</span><span class="sxs-lookup"><span data-stu-id="84ff3-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="84ff3-116">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="84ff3-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="84ff3-117">Атрибут</span><span class="sxs-lookup"><span data-stu-id="84ff3-117">Attribute</span></span></th>
<th><span data-ttu-id="84ff3-118">Описание</span><span class="sxs-lookup"><span data-stu-id="84ff3-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="84ff3-119">форматас</span><span class="sxs-lookup"><span data-stu-id="84ff3-119">formatAs</span></span></td>
<td><span data-ttu-id="84ff3-120">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="84ff3-120">Public.</span></span> <span data-ttu-id="84ff3-121">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="84ff3-121">Optional.</span></span> <span data-ttu-id="84ff3-122">Значение по умолчанию — &quot; General &quot; .</span><span class="sxs-lookup"><span data-stu-id="84ff3-122">Default is &quot;General&quot;.</span></span> <span data-ttu-id="84ff3-123">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="84ff3-123">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="84ff3-124">Значение</span><span class="sxs-lookup"><span data-stu-id="84ff3-124">Value</span></span></th>
<th><span data-ttu-id="84ff3-125">Значение</span><span class="sxs-lookup"><span data-stu-id="84ff3-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="84ff3-126">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="84ff3-126">General</span></span></td>
<td><span data-ttu-id="84ff3-127">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="84ff3-127">Default.</span></span> <span data-ttu-id="84ff3-128">Форматирует значение даты и времени с помощью <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shformatdatetimea"><strong>шформатдатетиме</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="84ff3-128">Formats the date-time value using <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shformatdatetimea"><strong>SHFormatDateTime</strong></a>.</span></span> <span data-ttu-id="84ff3-129">Используйте атрибуты <em>форматтимеас</em> и <em>форматдатеас</em> для указания способа форматирования даты и времени.</span><span class="sxs-lookup"><span data-stu-id="84ff3-129">Use the <em>formatTimeAs</em> and <em>formatDateAs</em> attributes to specify how the time and date are formatted.</span></span> <span data-ttu-id="84ff3-130">Требует, чтобы тип свойства был типом DateTime.</span><span class="sxs-lookup"><span data-stu-id="84ff3-130">Requires the property type to be DateTime.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84ff3-131">Месяц</span><span class="sxs-lookup"><span data-stu-id="84ff3-131">Month</span></span></td>
<td><span data-ttu-id="84ff3-132">Форматирует значение как один из месяцев года.</span><span class="sxs-lookup"><span data-stu-id="84ff3-132">Formats the value as one of the months of the year.</span></span> <span data-ttu-id="84ff3-133">Требует, чтобы тип свойства был Int32.</span><span class="sxs-lookup"><span data-stu-id="84ff3-133">Requires the property type to be Int32.</span></span> <span data-ttu-id="84ff3-134">Значение должно храниться как числовое значение, равное 1, представляющему первый месяц года.</span><span class="sxs-lookup"><span data-stu-id="84ff3-134">The value must be stored as a numeric value with 1 representing the first month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84ff3-135">еармонс</span><span class="sxs-lookup"><span data-stu-id="84ff3-135">YearMonth</span></span></td>
<td><span data-ttu-id="84ff3-136">Форматирует значение как &quot; год-месяц &quot; .</span><span class="sxs-lookup"><span data-stu-id="84ff3-136">Formats the value as &quot;Year - Month&quot;.</span></span> <span data-ttu-id="84ff3-137">Требует, чтобы тип свойства был Int32.</span><span class="sxs-lookup"><span data-stu-id="84ff3-137">Requires the property type to be Int32.</span></span> <span data-ttu-id="84ff3-138">Значение должно храниться таким, что два старших байта указывают год, а младшие два байта указывают месяц.</span><span class="sxs-lookup"><span data-stu-id="84ff3-138">The value must be stored such that the two highest bytes specify the year and the lower two bytes specify the month.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84ff3-139">Year;</span><span class="sxs-lookup"><span data-stu-id="84ff3-139">Year</span></span></td>
<td><span data-ttu-id="84ff3-140">Форматирует значение как простую строку.</span><span class="sxs-lookup"><span data-stu-id="84ff3-140">Formats the value as a simple string.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84ff3-141">форматтимеас</span><span class="sxs-lookup"><span data-stu-id="84ff3-141">formatTimeAs</span></span></td>
<td><span data-ttu-id="84ff3-142">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="84ff3-142">Public.</span></span> <span data-ttu-id="84ff3-143">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="84ff3-143">Optional.</span></span> <span data-ttu-id="84ff3-144">Значение по умолчанию — &quot; шорттиме &quot; .</span><span class="sxs-lookup"><span data-stu-id="84ff3-144">Default is &quot;ShortTime&quot;.</span></span> <span data-ttu-id="84ff3-145">Задает формат для вывода времени.</span><span class="sxs-lookup"><span data-stu-id="84ff3-145">Specifies the format in which to display time.</span></span> <span data-ttu-id="84ff3-146">Применяется, если <strong>форматас &quot; = &quot; General</strong>.</span><span class="sxs-lookup"><span data-stu-id="84ff3-146">Applies when <strong>formatAs=&quot;General&quot;</strong>.</span></span> <span data-ttu-id="84ff3-147">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="84ff3-147">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="84ff3-148">Значение</span><span class="sxs-lookup"><span data-stu-id="84ff3-148">Value</span></span></th>
<th><span data-ttu-id="84ff3-149">Значение</span><span class="sxs-lookup"><span data-stu-id="84ff3-149">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="84ff3-150">шорттиме</span><span class="sxs-lookup"><span data-stu-id="84ff3-150">ShortTime</span></span></td>
<td><span data-ttu-id="84ff3-151">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="84ff3-151">Default.</span></span> <span data-ttu-id="84ff3-152">Показывать время, например &quot; 7:48 PM &quot; .</span><span class="sxs-lookup"><span data-stu-id="84ff3-152">Show the time like &quot;7:48 PM&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84ff3-153">Давнего</span><span class="sxs-lookup"><span data-stu-id="84ff3-153">LongTime</span></span></td>
<td><span data-ttu-id="84ff3-154">Показывать время, например &quot; 7:48:33 PM &quot; .</span><span class="sxs-lookup"><span data-stu-id="84ff3-154">Show the time like &quot;7:48:33 PM&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84ff3-155">хидетиме</span><span class="sxs-lookup"><span data-stu-id="84ff3-155">HideTime</span></span></td>
<td><span data-ttu-id="84ff3-156">Не отображать временную часть даты.</span><span class="sxs-lookup"><span data-stu-id="84ff3-156">Do not display the time portion of the date.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84ff3-157">форматдатеас</span><span class="sxs-lookup"><span data-stu-id="84ff3-157">formatDateAs</span></span></td>
<td><span data-ttu-id="84ff3-158">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="84ff3-158">Public.</span></span> <span data-ttu-id="84ff3-159">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="84ff3-159">Optional.</span></span> <span data-ttu-id="84ff3-160">Значение по умолчанию — &quot; шортдате &quot; .</span><span class="sxs-lookup"><span data-stu-id="84ff3-160">Default is &quot;ShortDate&quot;.</span></span> <span data-ttu-id="84ff3-161">Задает формат для вывода даты.</span><span class="sxs-lookup"><span data-stu-id="84ff3-161">Specifies the format in which to display the date.</span></span> <span data-ttu-id="84ff3-162">Применяется, если <strong>форматас &quot; = &quot; General</strong>.</span><span class="sxs-lookup"><span data-stu-id="84ff3-162">Applies when <strong>formatAs=&quot;General&quot;</strong>.</span></span> <span data-ttu-id="84ff3-163">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="84ff3-163">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="84ff3-164">Значение</span><span class="sxs-lookup"><span data-stu-id="84ff3-164">Value</span></span></th>
<th><span data-ttu-id="84ff3-165">Пример</span><span class="sxs-lookup"><span data-stu-id="84ff3-165">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="84ff3-166">шортдате</span><span class="sxs-lookup"><span data-stu-id="84ff3-166">ShortDate</span></span></td>
<td><span data-ttu-id="84ff3-167">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="84ff3-167">Default.</span></span> <span data-ttu-id="84ff3-168">Отображение даты, например &quot; 5/13/59 &quot; .</span><span class="sxs-lookup"><span data-stu-id="84ff3-168">Show the date like &quot;5/13/59&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84ff3-169">лонгдате</span><span class="sxs-lookup"><span data-stu-id="84ff3-169">LongDate</span></span></td>
<td><span data-ttu-id="84ff3-170">Отображение даты, например &quot; среды, 13 мая 1959 &quot; .</span><span class="sxs-lookup"><span data-stu-id="84ff3-170">Show the date like &quot;Wednesday, May 13, 1959&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84ff3-171">хидедате</span><span class="sxs-lookup"><span data-stu-id="84ff3-171">HideDate</span></span></td>
<td><span data-ttu-id="84ff3-172">Не отображать дату.</span><span class="sxs-lookup"><span data-stu-id="84ff3-172">Do not display the date portion.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84ff3-173">релативешортдате</span><span class="sxs-lookup"><span data-stu-id="84ff3-173">RelativeShortDate</span></span></td>
<td><span data-ttu-id="84ff3-174">Показывать дату, такую как &quot; шортдате &quot; , но при возможности использовать относительные описания, например, &quot; вчера &quot; .</span><span class="sxs-lookup"><span data-stu-id="84ff3-174">Show the date like &quot;ShortDate&quot;, but use relative descriptions, such as &quot;yesterday&quot;, whenever possible.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84ff3-175">релативелонгдате</span><span class="sxs-lookup"><span data-stu-id="84ff3-175">RelativeLongDate</span></span></td>
<td><span data-ttu-id="84ff3-176">Показывать дату, такую как &quot; лонгдате &quot; , но при возможности использовать относительные описания, например, &quot; вчера &quot; .</span><span class="sxs-lookup"><span data-stu-id="84ff3-176">Show the date like &quot;LongDate&quot;, but use relative descriptions, such as &quot;yesterday&quot;, whenever possible.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
