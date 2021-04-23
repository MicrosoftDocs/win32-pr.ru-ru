---
description: Мбнпрофиликст \/ ... \/ Имя пользователя (v4)
MS-HAID: WWAN\_profile\_v4.element\_UserName
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Имя пользователя
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1f06d5b0-f229-4db7-a06b-9b66a8d792c1
api_name:
- UserName
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4c901a78e37bd3a4d883e0bd1c5c2006c7e2bc81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541402"
---
# <a name="span-idwwan_profile_v4element_usernamespanmbnprofileextusername-v4"></a><span data-ttu-id="03654-103"><span id="WWAN_profile_v4.element_UserName"></span>Мбнпрофиликст \/ ... \/ Имя пользователя (v4)</span><span class="sxs-lookup"><span data-stu-id="03654-103"><span id="WWAN_profile_v4.element_UserName"></span>MBNProfileExt\/...\/UserName (v4)</span></span>

<span data-ttu-id="03654-104">Имя пользователя, используемое для входа в систему.</span><span class="sxs-lookup"><span data-stu-id="03654-104">The user name to use for logon.</span></span>

<span data-ttu-id="03654-105">Дополнительные сведения см. в документации по элементу [**имени пользователя**](./schema-username-userlogoncred-element.md) v1.</span><span class="sxs-lookup"><span data-stu-id="03654-105">For more details, see the documentation for the v1 [**UserName**](./schema-username-userlogoncred-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="03654-106">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="03654-106">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<UserName\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-1-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<UserName\>**

## <a name="syntax"></a><span data-ttu-id="03654-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03654-107">Syntax</span></span>

``` syntax
<UserName>

  nameType

</UserName>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="03654-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="03654-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="03654-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="03654-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="03654-110">Нет.</span><span class="sxs-lookup"><span data-stu-id="03654-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="03654-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="03654-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="03654-112">Нет.</span><span class="sxs-lookup"><span data-stu-id="03654-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="03654-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="03654-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="03654-114">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="03654-114">Parent Element</span></span></th>
<th><span data-ttu-id="03654-115">Описание</span><span class="sxs-lookup"><span data-stu-id="03654-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="03654-116"><a href="element-userlogoncred.md">UserLogonCred</a></span><span class="sxs-lookup"><span data-stu-id="03654-116"><a href="element-userlogoncred.md">UserLogonCred</a></span></span></td>
<td><p><span data-ttu-id="03654-117">Учетные данные входа для подключения.</span><span class="sxs-lookup"><span data-stu-id="03654-117">Logon credentials for a connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="03654-118">Требования</span><span class="sxs-lookup"><span data-stu-id="03654-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03654-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="03654-119">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
