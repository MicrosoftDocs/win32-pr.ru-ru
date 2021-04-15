---
description: 'Указывает, как Ипропертидескриптион:: Форматфордисплай должен форматировать значение свойства в виде строки. Это применимо только в том случае <displayInfo displayType=&\#0034;Number&\#0034;> , если.'
ms.assetid: 9e8cfe5c-e17a-40d6-958f-a1bd1130c699
title: numberFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6750a9fb4dcf6a7a56c350fccf80241644b956da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662766"
---
# <a name="numberformat"></a><span data-ttu-id="a63a4-104">numberFormat</span><span class="sxs-lookup"><span data-stu-id="a63a4-104">numberFormat</span></span>

<span data-ttu-id="a63a4-105">Указывает, как [**ипропертидескриптион:: форматфордисплай**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) должен форматировать значение свойства в виде строки.</span><span class="sxs-lookup"><span data-stu-id="a63a4-105">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="a63a4-106">Это применимо только в том случае <displayInfo displayType="Number"> , если.</span><span class="sxs-lookup"><span data-stu-id="a63a4-106">This is applicable only if <displayInfo displayType="Number">.</span></span> <span data-ttu-id="a63a4-107">Для каждого элемента [displayInfo](./propdesc-schema-displayinfo.md) должен быть только один элемент [NumberFormat]() .</span><span class="sxs-lookup"><span data-stu-id="a63a4-107">There should be only one [numberFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="a63a4-108">При наличии нескольких элементов используется последний из них.</span><span class="sxs-lookup"><span data-stu-id="a63a4-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="a63a4-109">Если элемент [NumberFormat]() не указан, к описанию свойства применяются параметры атрибута по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a63a4-109">If no [numberFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="a63a4-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a63a4-110">Syntax</span></span>


```
      <!-- numberFormat -->
      <xs:element name="numberFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="General"/>
                <xs:enumeration value="Percentage"/>
                <xs:enumeration value="ByteSize"/>
                <xs:enumeration value="KBSize"/>
                <xs:enumeration value="SampleSize"/>
                <xs:enumeration value="Bitrate"/>
                <xs:enumeration value="SampleRate"/>
                <xs:enumeration value="FrameRate"/>
                <xs:enumeration value="Pixels"/>
                <xs:enumeration value="DPI"/>
                <xs:enumeration value="Duration"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatDurationAs">
              <xs:restriction base="xs:string">
                <xs:enumeration value="hh:mm"/>
                <xs:enumeration value="hh:mm:ss"/>
                <xs:enumeration value="hh:mm:ss.fff"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
        </xs:complexType>
      </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="a63a4-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="a63a4-111">Element Information</span></span>



| <span data-ttu-id="a63a4-112">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="a63a4-112">Parent Element</span></span>                                   | <span data-ttu-id="a63a4-113">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a63a4-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="a63a4-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="a63a4-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="a63a4-115">Нет</span><span class="sxs-lookup"><span data-stu-id="a63a4-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="a63a4-116">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a63a4-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a63a4-117">Атрибут</span><span class="sxs-lookup"><span data-stu-id="a63a4-117">Attribute</span></span></th>
<th><span data-ttu-id="a63a4-118">Описание</span><span class="sxs-lookup"><span data-stu-id="a63a4-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a63a4-119">форматас</span><span class="sxs-lookup"><span data-stu-id="a63a4-119">formatAs</span></span></td>
<td><span data-ttu-id="a63a4-120">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="a63a4-120">Public.</span></span> <span data-ttu-id="a63a4-121">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="a63a4-121">Optional.</span></span> <span data-ttu-id="a63a4-122">Значение по умолчанию — &quot; General &quot; .</span><span class="sxs-lookup"><span data-stu-id="a63a4-122">Default is &quot;General&quot;.</span></span> <span data-ttu-id="a63a4-123">Задает формат вывода.</span><span class="sxs-lookup"><span data-stu-id="a63a4-123">Specifies the display format.</span></span> <span data-ttu-id="a63a4-124">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="a63a4-124">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a63a4-125">Значение</span><span class="sxs-lookup"><span data-stu-id="a63a4-125">Value</span></span></th>
<th><span data-ttu-id="a63a4-126">Значение</span><span class="sxs-lookup"><span data-stu-id="a63a4-126">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a63a4-127">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="a63a4-127">General</span></span></td>
<td><span data-ttu-id="a63a4-128">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a63a4-128">Default.</span></span> <span data-ttu-id="a63a4-129">Отображает значение в виде неформатированного числа.</span><span class="sxs-lookup"><span data-stu-id="a63a4-129">Displays the value as an unformatted number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a63a4-130">Процент</span><span class="sxs-lookup"><span data-stu-id="a63a4-130">Percentage</span></span></td>
<td><span data-ttu-id="a63a4-131">Форматирует значение в процентах.</span><span class="sxs-lookup"><span data-stu-id="a63a4-131">Formats the value as a percentage.</span></span> <span data-ttu-id="a63a4-132">Требует, чтобы свойство было UInt32.</span><span class="sxs-lookup"><span data-stu-id="a63a4-132">Requires the property to be UInt32.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a63a4-133">битесизе</span><span class="sxs-lookup"><span data-stu-id="a63a4-133">ByteSize</span></span></td>
<td><span data-ttu-id="a63a4-134">При необходимости форматирует значение как байт, &quot; КБ &quot; , &quot; МБ &quot; или &quot; ГБ &quot; .</span><span class="sxs-lookup"><span data-stu-id="a63a4-134">Formats the value as a byte, &quot;KB&quot;, &quot;MB&quot;, or &quot;GB&quot; as appropriate.</span></span> <span data-ttu-id="a63a4-135">Свойство должно иметь значение UInt64.</span><span class="sxs-lookup"><span data-stu-id="a63a4-135">Requires the property to be UInt64.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a63a4-136">кбсизе</span><span class="sxs-lookup"><span data-stu-id="a63a4-136">KBSize</span></span></td>
<td><span data-ttu-id="a63a4-137">Форматирует значение в &quot; КБ &quot; , независимо от значения.</span><span class="sxs-lookup"><span data-stu-id="a63a4-137">Formats the value as a &quot;KB&quot;, no matter what the value is.</span></span> <span data-ttu-id="a63a4-138">Свойство должно иметь значение UInt64.</span><span class="sxs-lookup"><span data-stu-id="a63a4-138">Requires the property to be UInt64.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a63a4-139">SampleSize</span><span class="sxs-lookup"><span data-stu-id="a63a4-139">SampleSize</span></span></td>
<td><span data-ttu-id="a63a4-140">Форматирует значение как число битов.</span><span class="sxs-lookup"><span data-stu-id="a63a4-140">Formats the value as a number of bits.</span></span> <span data-ttu-id="a63a4-141">Требует, чтобы свойство было UInt32.</span><span class="sxs-lookup"><span data-stu-id="a63a4-141">Requires the property to be UInt32.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a63a4-142">Скорость</span><span class="sxs-lookup"><span data-stu-id="a63a4-142">BitRate</span></span></td>
<td><span data-ttu-id="a63a4-143">Форматирует значение в &quot; кбит/с &quot; .</span><span class="sxs-lookup"><span data-stu-id="a63a4-143">Formats the value in &quot;Kbps&quot;.</span></span> <span data-ttu-id="a63a4-144">Требует, чтобы свойство было UInt32.</span><span class="sxs-lookup"><span data-stu-id="a63a4-144">Requires the property to be UInt32.</span></span> <span data-ttu-id="a63a4-145">Значение должно храниться в единицах с количеством &quot; бит в секунду &quot; .</span><span class="sxs-lookup"><span data-stu-id="a63a4-145">The value must be stored in &quot;bits-per-second&quot; units.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a63a4-146">SampleRate</span><span class="sxs-lookup"><span data-stu-id="a63a4-146">SampleRate</span></span></td>
<td><span data-ttu-id="a63a4-147">Форматирует значение в &quot; кГц &quot; .</span><span class="sxs-lookup"><span data-stu-id="a63a4-147">Formats the value in &quot;KHz&quot;.</span></span> <span data-ttu-id="a63a4-148">Требует, чтобы свойство было UInt32.</span><span class="sxs-lookup"><span data-stu-id="a63a4-148">Requires the property to be UInt32.</span></span> <span data-ttu-id="a63a4-149">Значение должно храниться в &quot; &quot; единицах Герц.</span><span class="sxs-lookup"><span data-stu-id="a63a4-149">The value must be stored in &quot;Hertz&quot; units.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a63a4-150">FrameRate</span><span class="sxs-lookup"><span data-stu-id="a63a4-150">FrameRate</span></span></td>
<td><span data-ttu-id="a63a4-151">Форматирует значение в кадрах/сек.</span><span class="sxs-lookup"><span data-stu-id="a63a4-151">Formats the value in frames/second.</span></span> <span data-ttu-id="a63a4-152">Требует, чтобы свойство было UInt32.</span><span class="sxs-lookup"><span data-stu-id="a63a4-152">Requires the property to be UInt32.</span></span> <span data-ttu-id="a63a4-153">Значение должно храниться в &quot; единицах килобайтах-Frame-to-Second &quot; .</span><span class="sxs-lookup"><span data-stu-id="a63a4-153">The value must be stored in &quot;kilo-frames-per-second&quot; units.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a63a4-154">Перекрытых</span><span class="sxs-lookup"><span data-stu-id="a63a4-154">Pixels</span></span></td>
<td><span data-ttu-id="a63a4-155">Форматирует значение в пикселных единицах.</span><span class="sxs-lookup"><span data-stu-id="a63a4-155">Formats the value in pixel units.</span></span> <span data-ttu-id="a63a4-156">Требует, чтобы свойство было UInt32.</span><span class="sxs-lookup"><span data-stu-id="a63a4-156">Requires the property to be UInt32.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a63a4-157">DPI</span><span class="sxs-lookup"><span data-stu-id="a63a4-157">DPI</span></span></td>
<td><span data-ttu-id="a63a4-158">Форматирует значение в точках на дюйм.</span><span class="sxs-lookup"><span data-stu-id="a63a4-158">Formats the value in dots-per-inch.</span></span> <span data-ttu-id="a63a4-159">Требует, чтобы свойство было UInt32.</span><span class="sxs-lookup"><span data-stu-id="a63a4-159">Requires the property to be UInt32.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a63a4-160">Duration</span><span class="sxs-lookup"><span data-stu-id="a63a4-160">Duration</span></span></td>
<td><span data-ttu-id="a63a4-161">Форматирует значение как длительность.</span><span class="sxs-lookup"><span data-stu-id="a63a4-161">Formats the value as a duration.</span></span> <span data-ttu-id="a63a4-162">Используйте <formatDurationAs> для указания формата длительности.</span><span class="sxs-lookup"><span data-stu-id="a63a4-162">Use <formatDurationAs> to specify the duration format.</span></span> <span data-ttu-id="a63a4-163">Свойство должно иметь значение UInt64.</span><span class="sxs-lookup"><span data-stu-id="a63a4-163">Requires the property to be UInt64.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a63a4-164">форматдуратионас</span><span class="sxs-lookup"><span data-stu-id="a63a4-164">formatDurationAs</span></span></td>
<td><span data-ttu-id="a63a4-165">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="a63a4-165">Public.</span></span> <span data-ttu-id="a63a4-166">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="a63a4-166">Optional.</span></span> <span data-ttu-id="a63a4-167">Значение по умолчанию — &quot; чч: мм: СС &quot; .</span><span class="sxs-lookup"><span data-stu-id="a63a4-167">Default is &quot;hh:mm:ss&quot;.</span></span> <span data-ttu-id="a63a4-168">Применяется только в том случае, если <em>форматас = &quot; Duration &quot; </em>.</span><span class="sxs-lookup"><span data-stu-id="a63a4-168">Only applies if <em>formatAs=&quot;Duration&quot;</em>.</span></span> <span data-ttu-id="a63a4-169">Свойство должно иметь значение UInt64.</span><span class="sxs-lookup"><span data-stu-id="a63a4-169">Requires the property to be UInt64.</span></span> <span data-ttu-id="a63a4-170">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="a63a4-170">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a63a4-171">Значение</span><span class="sxs-lookup"><span data-stu-id="a63a4-171">Value</span></span></th>
<th><span data-ttu-id="a63a4-172">Значение</span><span class="sxs-lookup"><span data-stu-id="a63a4-172">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a63a4-173">чч:мм</span><span class="sxs-lookup"><span data-stu-id="a63a4-173">hh:mm</span></span></td>
<td><span data-ttu-id="a63a4-174">Форматирует значение в часах и минутах.</span><span class="sxs-lookup"><span data-stu-id="a63a4-174">Formats the value in hours and minutes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a63a4-175">чч:мм:сс</span><span class="sxs-lookup"><span data-stu-id="a63a4-175">hh:mm:ss</span></span></td>
<td><span data-ttu-id="a63a4-176">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a63a4-176">Default.</span></span> <span data-ttu-id="a63a4-177">Форматирует значение в часах, минутах и секундах.</span><span class="sxs-lookup"><span data-stu-id="a63a4-177">Formats the value in hours, minutes, and seconds.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a63a4-178">чч: мм: СС. FFF</span><span class="sxs-lookup"><span data-stu-id="a63a4-178">hh:mm:ss.fff</span></span></td>
<td><span data-ttu-id="a63a4-179">Форматирует значение в часах, минутах, секундах и миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="a63a4-179">Formats the value in hours, minutes, seconds, and milliseconds.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
