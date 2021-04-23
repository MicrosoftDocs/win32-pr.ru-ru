---
description: аутоконнектонинтернет
MS-HAID: WWAN\_profile\_v4.element\_AutoConnectOnInternet
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: аутоконнектонинтернет
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4e42d42285ba97e8415fdd1c8e8ddddb329338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701621"
---
# <a name="span-idwwan_profile_v4element_autoconnectoninternetspanautoconnectoninternet"></a><span data-ttu-id="cdc1f-103"><span id="WWAN_profile_v4.element_AutoConnectOnInternet"></span>аутоконнектонинтернет</span><span class="sxs-lookup"><span data-stu-id="cdc1f-103"><span id="WWAN_profile_v4.element_AutoConnectOnInternet"></span>AutoConnectOnInternet</span></span>

<span data-ttu-id="cdc1f-104">Указывает, будет ли устройство мобильной широкополосной связи автоматически подключаться к сети.</span><span class="sxs-lookup"><span data-stu-id="cdc1f-104">Specifies whether the Mobile Broadband device will automatically connect to a network.</span></span>

<span data-ttu-id="cdc1f-105">Дополнительные сведения см. в документации по элементу [**аутоконнектонинтернет**](./schema-autoconnectoninternet-mbnprofile-element.md) v1.</span><span class="sxs-lookup"><span data-stu-id="cdc1f-105">For more information, see the documentation for the v1 [**AutoConnectOnInternet**](./schema-autoconnectoninternet-mbnprofile-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="cdc1f-106">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="cdc1f-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<AutoConnectOnInternet>**

## <a name="syntax"></a><span data-ttu-id="cdc1f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cdc1f-107">Syntax</span></span>

``` syntax
<AutoConnectOnInternet>

  boolean

</AutoConnectOnInternet>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="cdc1f-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="cdc1f-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="cdc1f-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="cdc1f-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="cdc1f-110">Нет.</span><span class="sxs-lookup"><span data-stu-id="cdc1f-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="cdc1f-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="cdc1f-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="cdc1f-112">Нет.</span><span class="sxs-lookup"><span data-stu-id="cdc1f-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="cdc1f-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="cdc1f-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cdc1f-114">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="cdc1f-114">Parent Element</span></span></th>
<th><span data-ttu-id="cdc1f-115">Описание</span><span class="sxs-lookup"><span data-stu-id="cdc1f-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cdc1f-116"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="cdc1f-116"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="cdc1f-117">Элемент <strong>мбнпрофиликст</strong> является расширением более раннего элемента мбнпрофиле.</span><span class="sxs-lookup"><span data-stu-id="cdc1f-117">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="cdc1f-118">Он определяет профиль мобильного широкополосного подключения с более широким набором параметров, чем элемент Мбнпрофиле.</span><span class="sxs-lookup"><span data-stu-id="cdc1f-118">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="cdc1f-119">В профиле может быть несколько элементов Мбнпрофиликст, описывающих параметры профиля для определенного набора условий.</span><span class="sxs-lookup"><span data-stu-id="cdc1f-119">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="cdc1f-120">Используйте дочерний элемент <a href="element-profileconditionedon.md"><strong>профилекондитионедон</strong></a> из <strong>мбнпрофиликст</strong> , чтобы указать, какие операционные условия делают определенный профиль активным.</span><span class="sxs-lookup"><span data-stu-id="cdc1f-120">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="cdc1f-121">Требования</span><span class="sxs-lookup"><span data-stu-id="cdc1f-121">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdc1f-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cdc1f-122">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
