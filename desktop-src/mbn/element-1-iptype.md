---
description: Модемдмконфигпрофиле \/ ... \/ Иптипе (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_IPType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ced0048e4793a1b26f2beac1e4c08ab92cbcc1b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647163"
---
# <a name="span-idwwan_profile_v4element_1_iptypespanmodemdmconfigprofileiptype-v4"></a><span data-ttu-id="dbfa8-103"><span id="WWAN_profile_v4.element_1_IPType"></span>Модемдмконфигпрофиле \/ ... \/ Иптипе (v4)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-103"><span id="WWAN_profile_v4.element_1_IPType"></span>ModemDMConfigProfile\/...\/IPType (v4)</span></span>

<span data-ttu-id="dbfa8-104">Указывает тип IP-адреса, используемый для этого подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-104">Specifies the IP type to be used on this data connection.</span></span>

<span data-ttu-id="dbfa8-105">Этот элемент впервые находится в версии v4 схемы.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-105">This element is new in v4 of the schema.</span></span> <span data-ttu-id="dbfa8-106">Элемент может иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-106">The element can have one of the following values.</span></span>

| <span data-ttu-id="dbfa8-107">Значение</span><span class="sxs-lookup"><span data-stu-id="dbfa8-107">Value</span></span>   | <span data-ttu-id="dbfa8-108">Значение</span><span class="sxs-lookup"><span data-stu-id="dbfa8-108">Meaning</span></span>                                       |
|---------|-----------------------------------------------|
| <span data-ttu-id="dbfa8-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="dbfa8-109">Default</span></span> | <span data-ttu-id="dbfa8-110">Тип IP-адреса должен быть выбран более низкими слоями</span><span class="sxs-lookup"><span data-stu-id="dbfa8-110">IP type is to be picked by lower layer(s)</span></span>     |
| <span data-ttu-id="dbfa8-111">IPv4</span><span class="sxs-lookup"><span data-stu-id="dbfa8-111">IPv4</span></span>    | <span data-ttu-id="dbfa8-112">Использовать IPv4</span><span class="sxs-lookup"><span data-stu-id="dbfa8-112">Use IPv4</span></span>                                      |
| <span data-ttu-id="dbfa8-113">IPv6;</span><span class="sxs-lookup"><span data-stu-id="dbfa8-113">IPv6</span></span>    | <span data-ttu-id="dbfa8-114">использовать IPv6</span><span class="sxs-lookup"><span data-stu-id="dbfa8-114">Use IPv6</span></span>                                      |
| <span data-ttu-id="dbfa8-115">IPv4v6</span><span class="sxs-lookup"><span data-stu-id="dbfa8-115">IPv4v6</span></span>  | <span data-ttu-id="dbfa8-116">Используйте IPv4 и (или) IPv6, как доступно.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-116">Use IPv4 and/or IPv6, as available.</span></span>           |
| <span data-ttu-id="dbfa8-117">кслат</span><span class="sxs-lookup"><span data-stu-id="dbfa8-117">XLAT</span></span>    | <span data-ttu-id="dbfa8-118">Использование 464XLAT для туннелирования IPv4 через IPv6-сети</span><span class="sxs-lookup"><span data-stu-id="dbfa8-118">Use 464XLAT to tunnel IPv4 over IPv6 networks</span></span> |

 

## <a name="element-hierarchy"></a><span data-ttu-id="dbfa8-119">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="dbfa8-119">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<IPType\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<IPType\>**

## <a name="syntax"></a><span data-ttu-id="dbfa8-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dbfa8-120">Syntax</span></span>

``` syntax
<IPType>

  "Default" | "IPv4" | "IPv6" | "IPv4v6" | "XLAT"

</IPType>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="dbfa8-121"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="dbfa8-121"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="dbfa8-122"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="dbfa8-122"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="dbfa8-123">Нет.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-123">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="dbfa8-124"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="dbfa8-124"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="dbfa8-125">Нет.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-125">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="dbfa8-126"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="dbfa8-126"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dbfa8-127">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="dbfa8-127">Parent Element</span></span></th>
<th><span data-ttu-id="dbfa8-128">Описание</span><span class="sxs-lookup"><span data-stu-id="dbfa8-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dbfa8-129"><a href="element-1-context.md">Контекст</a></span><span class="sxs-lookup"><span data-stu-id="dbfa8-129"><a href="element-1-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="dbfa8-130">Задает параметры, необходимые для установления подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-130">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="dbfa8-131">Требования</span><span class="sxs-lookup"><span data-stu-id="dbfa8-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dbfa8-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dbfa8-132">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



