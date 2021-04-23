---
description: Мбнпрофиликст \/ ... \/ Сжатие (v4)
MS-HAID: WWAN\_profile\_v4.element\_Compression
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Сжатие
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4b2ad853-ecb3-46ef-8ce2-aa001bb070e6
api_name:
- Compression
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 64a5387aafdce7042c46f48fcda18454a3d99f3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343365"
---
# <a name="span-idwwan_profile_v4element_compressionspanmbnprofileextcompression-v4"></a><span data-ttu-id="bb90d-103"><span id="WWAN_profile_v4.element_Compression"></span>Мбнпрофиликст \/ ... \/ Сжатие (v4)</span><span class="sxs-lookup"><span data-stu-id="bb90d-103"><span id="WWAN_profile_v4.element_Compression"></span>MBNProfileExt\/...\/Compression (v4)</span></span>

<span data-ttu-id="bb90d-104">Указывает, будет ли использоваться сжатие по каналу данных для заголовка и передачи данных.</span><span class="sxs-lookup"><span data-stu-id="bb90d-104">Specifies whether compression will be used at the data link for header and data transfer.</span></span>

<span data-ttu-id="bb90d-105">Дополнительные сведения см. в документации по элементу [**сжатия**](./schema-compression-contexttype-element.md) v1.</span><span class="sxs-lookup"><span data-stu-id="bb90d-105">For more information, see the documentation for the v1 [**Compression**](./schema-compression-contexttype-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="bb90d-106">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="bb90d-106">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<Compression\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<Compression\>**

## <a name="syntax"></a><span data-ttu-id="bb90d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb90d-107">Syntax</span></span>

``` syntax
<Compression>

  "DISABLE" | "ENABLE"

</Compression>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="bb90d-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="bb90d-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="bb90d-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="bb90d-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="bb90d-110">Нет.</span><span class="sxs-lookup"><span data-stu-id="bb90d-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="bb90d-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="bb90d-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="bb90d-112">Нет.</span><span class="sxs-lookup"><span data-stu-id="bb90d-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="bb90d-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="bb90d-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bb90d-114">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="bb90d-114">Parent Element</span></span></th>
<th><span data-ttu-id="bb90d-115">Описание</span><span class="sxs-lookup"><span data-stu-id="bb90d-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bb90d-116"><a href="element-context.md">Контекст</a></span><span class="sxs-lookup"><span data-stu-id="bb90d-116"><a href="element-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="bb90d-117">Задает параметры, необходимые для установления подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="bb90d-117">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="bb90d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="bb90d-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb90d-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bb90d-119">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
