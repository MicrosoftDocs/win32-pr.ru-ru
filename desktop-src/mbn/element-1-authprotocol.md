---
description: Модемдмконфигпрофиле \/ ... \/ Ауспротокол (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_AuthProtocol
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Ауспротокол (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5e6c5a25-fe9e-4d0a-8b5b-4ff585f562af
api_name:
- AuthProtocol
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 99a4b02ec173e070f4a6d615f3632f11f4949b64
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388858"
---
# <a name="span-idwwan_profile_v4element_1_authprotocolspanmodemdmconfigprofileauthprotocol-v4"></a><span data-ttu-id="abf23-103"><span id="WWAN_profile_v4.element_1_AuthProtocol"></span>Модемдмконфигпрофиле \/ ... \/ Ауспротокол (v4)</span><span class="sxs-lookup"><span data-stu-id="abf23-103"><span id="WWAN_profile_v4.element_1_AuthProtocol"></span>ModemDMConfigProfile\/...\/AuthProtocol (v4)</span></span>

><span data-ttu-id="abf23-104">Указывает протокол проверки подлинности, используемый для активации контекста протокола данных пакетов (PDP).</span><span class="sxs-lookup"><span data-stu-id="abf23-104">Specifies the authentication protocol to be used for activating a Packet Data Protocol (PDP) context.</span></span>

<span data-ttu-id="abf23-105">Обратите внимание, что в версии v4 для этого элемента доступно новое значение перечисления.</span><span class="sxs-lookup"><span data-stu-id="abf23-105">Note that in v4, a new enumeration value is available for this element.</span></span> <span data-ttu-id="abf23-106">**Автовыбор** означает, что протокол проверки подлинности должен быть выбран более низкими слоями.</span><span class="sxs-lookup"><span data-stu-id="abf23-106">**AutoSelection** means that an auth protocol is to be picked by lower layer(s).</span></span>

<span data-ttu-id="abf23-107">Дополнительные сведения см. в документации по элементу [**ауспротокол**](./schema-authprotocol-contexttype-element.md) v1.</span><span class="sxs-lookup"><span data-stu-id="abf23-107">For further information, see the documentation for the v1 [**AuthProtocol**](./schema-authprotocol-contexttype-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="abf23-108">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="abf23-108">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<AuthProtocol\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<AuthProtocol\>**

## <a name="syntax"></a><span data-ttu-id="abf23-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="abf23-109">Syntax</span></span>

``` syntax
<AuthProtocol>

  "NONE" | "PAP" | "CHAP" | "MsCHAPv2" | "AutoSelection"

</AuthProtocol>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="abf23-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="abf23-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="abf23-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="abf23-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="abf23-112">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="abf23-112">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="abf23-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="abf23-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="abf23-114">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="abf23-114">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="abf23-115"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="abf23-115"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="abf23-116">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="abf23-116">Parent Element</span></span></th>
<th><span data-ttu-id="abf23-117">Описание</span><span class="sxs-lookup"><span data-stu-id="abf23-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="abf23-118"><a href="element-1-context.md">Контекст</a></span><span class="sxs-lookup"><span data-stu-id="abf23-118"><a href="element-1-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="abf23-119">Задает параметры, необходимые для установления подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="abf23-119">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="abf23-120">Требования</span><span class="sxs-lookup"><span data-stu-id="abf23-120">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="abf23-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="abf23-121">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
