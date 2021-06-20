---
description: 'Указывает, как Ипропертидескриптион:: Форматфордисплай должен форматировать значение свойства stringFormat в виде строки.'
ms.assetid: 7c38bc15-be86-4260-b2e4-13afc90de6d7
title: stringFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 730355507b78d99eba02e82666427dd29425c942
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408357"
---
# <a name="stringformat"></a><span data-ttu-id="92c87-103">stringFormat</span><span class="sxs-lookup"><span data-stu-id="92c87-103">stringFormat</span></span>

<span data-ttu-id="92c87-104">Указывает, как [**ипропертидескриптион:: форматфордисплай**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) должен форматировать значение свойства в виде строки.</span><span class="sxs-lookup"><span data-stu-id="92c87-104">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="92c87-105">Это применимо только в том случае <displayInfo displayType="String"> , если.</span><span class="sxs-lookup"><span data-stu-id="92c87-105">This is applicable only if <displayInfo displayType="String">.</span></span> <span data-ttu-id="92c87-106">Для каждого элемента [displayInfo](./propdesc-schema-displayinfo.md) должен быть только один элемент [StringFormat]() .</span><span class="sxs-lookup"><span data-stu-id="92c87-106">There should be only one [stringFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="92c87-107">При наличии нескольких элементов используется последний из них.</span><span class="sxs-lookup"><span data-stu-id="92c87-107">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="92c87-108">Если элемент [StringFormat]() не указан, к описанию свойства применяются параметры атрибута по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="92c87-108">If no [stringFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="92c87-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92c87-109">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="92c87-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="92c87-110">Element Information</span></span>



| <span data-ttu-id="92c87-111">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="92c87-111">Parent Element</span></span>                                   | <span data-ttu-id="92c87-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="92c87-112">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="92c87-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="92c87-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="92c87-114">Нет</span><span class="sxs-lookup"><span data-stu-id="92c87-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="92c87-115">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="92c87-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="92c87-116">Атрибут</span><span class="sxs-lookup"><span data-stu-id="92c87-116">Attribute</span></span></th>
<th><span data-ttu-id="92c87-117">Описание</span><span class="sxs-lookup"><span data-stu-id="92c87-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="92c87-118">форматас</span><span class="sxs-lookup"><span data-stu-id="92c87-118">formatAs</span></span></td>
<td><span data-ttu-id="92c87-119">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="92c87-119">Public.</span></span> <span data-ttu-id="92c87-120">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="92c87-120">Optional.</span></span> <span data-ttu-id="92c87-121">Значение по умолчанию — &quot; General &quot; .</span><span class="sxs-lookup"><span data-stu-id="92c87-121">Default is &quot;General&quot;.</span></span> <span data-ttu-id="92c87-122">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="92c87-122">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="92c87-123">Значение</span><span class="sxs-lookup"><span data-stu-id="92c87-123">Value</span></span></th>
<th><span data-ttu-id="92c87-124">Значение</span><span class="sxs-lookup"><span data-stu-id="92c87-124">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="92c87-125">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="92c87-125">General</span></span></td>
<td><span data-ttu-id="92c87-126">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="92c87-126">Default.</span></span> <span data-ttu-id="92c87-127">Возвращает значение в виде неформатированной строки.</span><span class="sxs-lookup"><span data-stu-id="92c87-127">Returns the value as an unformatted string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92c87-128">FileName</span><span class="sxs-lookup"><span data-stu-id="92c87-128">FileName</span></span></td>
<td><span data-ttu-id="92c87-129">Форматирует значение в виде имени файла.</span><span class="sxs-lookup"><span data-stu-id="92c87-129">Formats the value as a file name.</span></span> <span data-ttu-id="92c87-130">Скрывает расширение в соответствии с параметрами пользователя.</span><span class="sxs-lookup"><span data-stu-id="92c87-130">Hides the extension according to user settings.</span></span> <span data-ttu-id="92c87-131">Требует, чтобы тип свойства был строковым.</span><span class="sxs-lookup"><span data-stu-id="92c87-131">Requires the property type to be String.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="92c87-132">FilePath</span><span class="sxs-lookup"><span data-stu-id="92c87-132">FilePath</span></span></td>
<td><span data-ttu-id="92c87-133">Форматирует значение как путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="92c87-133">Formats the value as a file path.</span></span> <span data-ttu-id="92c87-134">Скрывает расширение в соответствии с параметрами пользователя.</span><span class="sxs-lookup"><span data-stu-id="92c87-134">Hides the extension according to user settings.</span></span> <span data-ttu-id="92c87-135">Требует, чтобы тип свойства был строковым.</span><span class="sxs-lookup"><span data-stu-id="92c87-135">Requires the property type to be String.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92c87-136">Гиперссылка</span><span class="sxs-lookup"><span data-stu-id="92c87-136">Hyperlink</span></span></td>
<td><span data-ttu-id="92c87-137">Форматирует значение как гиперссылку.</span><span class="sxs-lookup"><span data-stu-id="92c87-137">Formats the value as a hyperlink.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
