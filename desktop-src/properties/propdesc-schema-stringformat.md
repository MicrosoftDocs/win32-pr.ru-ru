---
description: 'Указывает, как Ипропертидескриптион:: Форматфордисплай должен форматировать значение свойства в виде строки. Это применимо только в том случае <displayInfo displayType=&\#0034;String&\#0034;> , если.'
ms.assetid: 7c38bc15-be86-4260-b2e4-13afc90de6d7
title: stringFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec05a6eedf1734c1d62c0503027810ad05916160
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662757"
---
# <a name="stringformat"></a><span data-ttu-id="245a7-104">stringFormat</span><span class="sxs-lookup"><span data-stu-id="245a7-104">stringFormat</span></span>

<span data-ttu-id="245a7-105">Указывает, как [**ипропертидескриптион:: форматфордисплай**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) должен форматировать значение свойства в виде строки.</span><span class="sxs-lookup"><span data-stu-id="245a7-105">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="245a7-106">Это применимо только в том случае <displayInfo displayType="String"> , если.</span><span class="sxs-lookup"><span data-stu-id="245a7-106">This is applicable only if <displayInfo displayType="String">.</span></span> <span data-ttu-id="245a7-107">Для каждого элемента [displayInfo](./propdesc-schema-displayinfo.md) должен быть только один элемент [StringFormat]() .</span><span class="sxs-lookup"><span data-stu-id="245a7-107">There should be only one [stringFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="245a7-108">При наличии нескольких элементов используется последний из них.</span><span class="sxs-lookup"><span data-stu-id="245a7-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="245a7-109">Если элемент [StringFormat]() не указан, к описанию свойства применяются параметры атрибута по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="245a7-109">If no [stringFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="245a7-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="245a7-110">Syntax</span></span>


```
<!-- stringFormat -->
<xs:element name="stringFormat"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="formatAs">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="FileName"/>
                    <xs:enumeration value="FilePath"/>
                    <xs:enumeration value="Hyperlink"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="245a7-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="245a7-111">Element Information</span></span>



| <span data-ttu-id="245a7-112">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="245a7-112">Parent Element</span></span>                                   | <span data-ttu-id="245a7-113">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="245a7-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="245a7-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="245a7-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="245a7-115">Нет</span><span class="sxs-lookup"><span data-stu-id="245a7-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="245a7-116">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="245a7-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="245a7-117">Атрибут</span><span class="sxs-lookup"><span data-stu-id="245a7-117">Attribute</span></span></th>
<th><span data-ttu-id="245a7-118">Описание</span><span class="sxs-lookup"><span data-stu-id="245a7-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="245a7-119">форматас</span><span class="sxs-lookup"><span data-stu-id="245a7-119">formatAs</span></span></td>
<td><span data-ttu-id="245a7-120">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="245a7-120">Public.</span></span> <span data-ttu-id="245a7-121">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="245a7-121">Optional.</span></span> <span data-ttu-id="245a7-122">Значение по умолчанию — &quot; General &quot; .</span><span class="sxs-lookup"><span data-stu-id="245a7-122">Default is &quot;General&quot;.</span></span> <span data-ttu-id="245a7-123">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="245a7-123">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="245a7-124">Значение</span><span class="sxs-lookup"><span data-stu-id="245a7-124">Value</span></span></th>
<th><span data-ttu-id="245a7-125">Значение</span><span class="sxs-lookup"><span data-stu-id="245a7-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="245a7-126">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="245a7-126">General</span></span></td>
<td><span data-ttu-id="245a7-127">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="245a7-127">Default.</span></span> <span data-ttu-id="245a7-128">Возвращает значение в виде неформатированной строки.</span><span class="sxs-lookup"><span data-stu-id="245a7-128">Returns the value as an unformatted string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="245a7-129">FileName</span><span class="sxs-lookup"><span data-stu-id="245a7-129">FileName</span></span></td>
<td><span data-ttu-id="245a7-130">Форматирует значение в виде имени файла.</span><span class="sxs-lookup"><span data-stu-id="245a7-130">Formats the value as a file name.</span></span> <span data-ttu-id="245a7-131">Скрывает расширение в соответствии с параметрами пользователя.</span><span class="sxs-lookup"><span data-stu-id="245a7-131">Hides the extension according to user settings.</span></span> <span data-ttu-id="245a7-132">Требует, чтобы тип свойства был строковым.</span><span class="sxs-lookup"><span data-stu-id="245a7-132">Requires the property type to be String.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="245a7-133">FilePath</span><span class="sxs-lookup"><span data-stu-id="245a7-133">FilePath</span></span></td>
<td><span data-ttu-id="245a7-134">Форматирует значение как путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="245a7-134">Formats the value as a file path.</span></span> <span data-ttu-id="245a7-135">Скрывает расширение в соответствии с параметрами пользователя.</span><span class="sxs-lookup"><span data-stu-id="245a7-135">Hides the extension according to user settings.</span></span> <span data-ttu-id="245a7-136">Требует, чтобы тип свойства был строковым.</span><span class="sxs-lookup"><span data-stu-id="245a7-136">Requires the property type to be String.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="245a7-137">Гиперссылка</span><span class="sxs-lookup"><span data-stu-id="245a7-137">Hyperlink</span></span></td>
<td><span data-ttu-id="245a7-138">Форматирует значение как гиперссылку.</span><span class="sxs-lookup"><span data-stu-id="245a7-138">Formats the value as a hyperlink.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
