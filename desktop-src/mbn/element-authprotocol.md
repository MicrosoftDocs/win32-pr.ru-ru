---
description: Мбнпрофиликст \/ ... \/ Ауспротокол (v4)
MS-HAID: WWAN\_profile\_v4.element\_AuthProtocol
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: AuthProtocol
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8274effe-1fcc-43f8-a609-795fe19a1c4f
api_name:
- AuthProtocol
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 90b3b64c5052a16f18c0a1b9fd154e2e73acd714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692252"
---
# <a name="span-idwwan_profile_v4element_authprotocolspanmbnprofileextauthprotocol-v4"></a><span data-ttu-id="1ee0a-103"><span id="WWAN_profile_v4.element_AuthProtocol"></span>Мбнпрофиликст \/ ... \/ Ауспротокол (v4)</span><span class="sxs-lookup"><span data-stu-id="1ee0a-103"><span id="WWAN_profile_v4.element_AuthProtocol"></span>MBNProfileExt\/...\/AuthProtocol (v4)</span></span>

><span data-ttu-id="1ee0a-104">Указывает протокол проверки подлинности, используемый для активации контекста протокола данных пакетов (PDP).</span><span class="sxs-lookup"><span data-stu-id="1ee0a-104">Specifies the authentication protocol to be used for activating a Packet Data Protocol (PDP) context.</span></span>

<span data-ttu-id="1ee0a-105">Обратите внимание, что в версии v4 для этого элемента доступно новое значение перечисления.</span><span class="sxs-lookup"><span data-stu-id="1ee0a-105">Note that in v4, a new enumeration value is available for this element.</span></span> <span data-ttu-id="1ee0a-106">**Автовыбор** означает, что протокол проверки подлинности должен быть выбран более низкими слоями.</span><span class="sxs-lookup"><span data-stu-id="1ee0a-106">**AutoSelection** means that an auth protocol is to be picked by lower layer(s).</span></span>

<span data-ttu-id="1ee0a-107">Дополнительные сведения см. в документации по элементу [**ауспротокол**](./schema-authprotocol-contexttype-element.md) v1.</span><span class="sxs-lookup"><span data-stu-id="1ee0a-107">For further information, see the documentation for the v1 [**AuthProtocol**](./schema-authprotocol-contexttype-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="1ee0a-108">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="1ee0a-108">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<AuthProtocol\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<AuthProtocol\>**

## <a name="syntax"></a><span data-ttu-id="1ee0a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ee0a-109">Syntax</span></span>

``` syntax
<AuthProtocol>

  "NONE" | "PAP" | "CHAP" | "MsCHAPv2" | "AutoSelection"

</AuthProtocol>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="1ee0a-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="1ee0a-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="1ee0a-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1ee0a-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="1ee0a-112">Нет.</span><span class="sxs-lookup"><span data-stu-id="1ee0a-112">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="1ee0a-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1ee0a-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="1ee0a-114">Нет.</span><span class="sxs-lookup"><span data-stu-id="1ee0a-114">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="1ee0a-115"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="1ee0a-115"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1ee0a-116">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="1ee0a-116">Parent Element</span></span></th>
<th><span data-ttu-id="1ee0a-117">Описание</span><span class="sxs-lookup"><span data-stu-id="1ee0a-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1ee0a-118"><a href="element-context.md">Контекст</a></span><span class="sxs-lookup"><span data-stu-id="1ee0a-118"><a href="element-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="1ee0a-119">Задает параметры, необходимые для установления подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="1ee0a-119">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="1ee0a-120">Требования</span><span class="sxs-lookup"><span data-stu-id="1ee0a-120">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ee0a-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1ee0a-121">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
