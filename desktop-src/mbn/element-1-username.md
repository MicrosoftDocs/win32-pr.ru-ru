---
description: Модемдмконфигпрофиле \/ ... \/ Имя пользователя (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_UserName
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Имя пользователя (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1b43a275-cdbd-44e6-adc6-121aa935447e
api_name:
- UserName
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 98e5c425ee7982bdfddfeb31ec1e950a0dc27d61
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388823"
---
# <a name="span-idwwan_profile_v4element_1_usernamespanmodemdmconfigprofileusername-v4"></a><span data-ttu-id="81f90-103"><span id="WWAN_profile_v4.element_1_UserName"></span>Модемдмконфигпрофиле \/ ... \/ Имя пользователя (v4)</span><span class="sxs-lookup"><span data-stu-id="81f90-103"><span id="WWAN_profile_v4.element_1_UserName"></span>ModemDMConfigProfile\/...\/UserName (v4)</span></span>

<span data-ttu-id="81f90-104">Имя пользователя, используемое для входа в систему.</span><span class="sxs-lookup"><span data-stu-id="81f90-104">The user name to use for logon.</span></span>

<span data-ttu-id="81f90-105">Дополнительные сведения см. в документации по элементу [**имени пользователя**](./schema-username-userlogoncred-element.md) v1.</span><span class="sxs-lookup"><span data-stu-id="81f90-105">For more details, see the documentation for the v1 [**UserName**](./schema-username-userlogoncred-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="81f90-106">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="81f90-106">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<UserName\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-1-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<UserName\>**

## <a name="syntax"></a><span data-ttu-id="81f90-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="81f90-107">Syntax</span></span>

``` syntax
<UserName>

  nameType

</UserName>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="81f90-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="81f90-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="81f90-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="81f90-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="81f90-110">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="81f90-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="81f90-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="81f90-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="81f90-112">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="81f90-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="81f90-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="81f90-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="81f90-114">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="81f90-114">Parent Element</span></span></th>
<th><span data-ttu-id="81f90-115">Описание</span><span class="sxs-lookup"><span data-stu-id="81f90-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="81f90-116"><a href="element-1-userlogoncred.md">UserLogonCred</a></span><span class="sxs-lookup"><span data-stu-id="81f90-116"><a href="element-1-userlogoncred.md">UserLogonCred</a></span></span></td>
<td><p><span data-ttu-id="81f90-117">Учетные данные входа для подключения.</span><span class="sxs-lookup"><span data-stu-id="81f90-117">Logon credentials for a connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="81f90-118">Требования</span><span class="sxs-lookup"><span data-stu-id="81f90-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="81f90-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="81f90-119">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
