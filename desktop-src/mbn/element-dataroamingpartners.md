---
description: DataRoamingPartners
MS-HAID: WWAN\_profile\_v4.element\_DataRoamingPartners
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: DataRoamingPartners
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c29edf9c-4e70-4b8f-8c71-0ec8a9fad60d
api_name:
- DataRoamingPartners
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f6df58bc0765b5254645c45270f8145f5d10d422
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710997"
---
# <a name="span-idwwan_profile_v4element_dataroamingpartnersspandataroamingpartners"></a><span data-ttu-id="df6eb-103"><span id="WWAN_profile_v4.element_DataRoamingPartners"></span>DataRoamingPartners</span><span class="sxs-lookup"><span data-stu-id="df6eb-103"><span id="WWAN_profile_v4.element_DataRoamingPartners"></span>DataRoamingPartners</span></span>

<span data-ttu-id="df6eb-104">Указывает список предпочтительных поставщиков сети при роуминге.</span><span class="sxs-lookup"><span data-stu-id="df6eb-104">Specifies a list of preferred network providers when roaming.</span></span>

<span data-ttu-id="df6eb-105">Дополнительные сведения см. в документации по элементу [**датароамингпартнерс**](./schema-dataroamingpartners-mbnprofile-element.md) v1.</span><span class="sxs-lookup"><span data-stu-id="df6eb-105">For details, see the documentation for the v1 [**DataRoamingPartners**](./schema-dataroamingpartners-mbnprofile-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="df6eb-106">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="df6eb-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<DataRoamingPartners>**

## <a name="syntax"></a><span data-ttu-id="df6eb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df6eb-107">Syntax</span></span>

``` syntax
<DataRoamingPartners>

  <!-- Child elements -->
  Provider+

</DataRoamingPartners>
```

### <a name="key"></a><span data-ttu-id="df6eb-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="df6eb-108">Key</span></span>

<span data-ttu-id="df6eb-109">`+`   обязательный (один или несколько)</span><span class="sxs-lookup"><span data-stu-id="df6eb-109">`+`   required (one or more)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="df6eb-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="df6eb-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="df6eb-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="df6eb-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="df6eb-112">Нет.</span><span class="sxs-lookup"><span data-stu-id="df6eb-112">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="df6eb-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="df6eb-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="df6eb-114">Дочерний элемент</span><span class="sxs-lookup"><span data-stu-id="df6eb-114">Child Element</span></span></th>
<th><span data-ttu-id="df6eb-115">Описание</span><span class="sxs-lookup"><span data-stu-id="df6eb-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="df6eb-116"><a href="element-provider.md">Поставщик</a></span><span class="sxs-lookup"><span data-stu-id="df6eb-116"><a href="element-provider.md">Provider</a></span></span></td>
<td><p><span data-ttu-id="df6eb-117">Указывает одного предпочитаемого поставщика сети в списке поставщиков, которые будут использоваться при роуминге.</span><span class="sxs-lookup"><span data-stu-id="df6eb-117">Specifies one preferred network provider in a list of providers to be used when roaming.</span></span></p>
<p><span data-ttu-id="df6eb-118">Значение этого элемента является экземпляром сложного типа <a href="../mbn/schema-providertype-complextype.md"><strong>ProviderType</strong></a> на v1.</span><span class="sxs-lookup"><span data-stu-id="df6eb-118">The value of this element is an instance of the v1 <a href="../mbn/schema-providertype-complextype.md"><strong>providerType</strong></a> complex type.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="df6eb-119"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="df6eb-119"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="df6eb-120">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="df6eb-120">Parent Element</span></span></th>
<th><span data-ttu-id="df6eb-121">Описание</span><span class="sxs-lookup"><span data-stu-id="df6eb-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="df6eb-122"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="df6eb-122"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="df6eb-123">Элемент <strong>мбнпрофиликст</strong> является расширением более раннего элемента мбнпрофиле.</span><span class="sxs-lookup"><span data-stu-id="df6eb-123">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="df6eb-124">Он определяет профиль мобильного широкополосного подключения с более широким набором параметров, чем элемент Мбнпрофиле.</span><span class="sxs-lookup"><span data-stu-id="df6eb-124">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="df6eb-125">В профиле может быть несколько элементов Мбнпрофиликст, описывающих параметры профиля для определенного набора условий.</span><span class="sxs-lookup"><span data-stu-id="df6eb-125">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="df6eb-126">Используйте дочерний элемент <a href="element-profileconditionedon.md"><strong>профилекондитионедон</strong></a> из <strong>мбнпрофиликст</strong> , чтобы указать, какие операционные условия делают определенный профиль активным.</span><span class="sxs-lookup"><span data-stu-id="df6eb-126">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="df6eb-127">Требования</span><span class="sxs-lookup"><span data-stu-id="df6eb-127">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="df6eb-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="df6eb-128">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
