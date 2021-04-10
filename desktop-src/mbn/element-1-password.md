---
description: Модемдмконфигпрофиле \/ ... \/ Пароль (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_Password
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Пароль
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6345870c-631e-42cc-9487-14d37215d1d2
api_name:
- Password
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7e4e2ce82f67251eb0ccff03364817a2fcd8c8b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144833"
---
# <a name="span-idwwan_profile_v4element_1_passwordspanmodemdmconfigprofilepassword-v4"></a><span data-ttu-id="068de-103"><span id="WWAN_profile_v4.element_1_Password"></span>Модемдмконфигпрофиле \/ ... \/ Пароль (v4)</span><span class="sxs-lookup"><span data-stu-id="068de-103"><span id="WWAN_profile_v4.element_1_Password"></span>ModemDMConfigProfile\/...\/Password (v4)</span></span>

<span data-ttu-id="068de-104">Указывает пароль, используемый для проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="068de-104">Specifies the password used to authenticate a user.</span></span>

<span data-ttu-id="068de-105">Дополнительные сведения см. в документации по элементу [**пароля**](./schema-password-userlogoncred-element.md) v1.</span><span class="sxs-lookup"><span data-stu-id="068de-105">For more information, see the documentation for the v1 [**Password**](./schema-password-userlogoncred-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="068de-106">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="068de-106">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<Password\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-1-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<Password\>**

## <a name="syntax"></a><span data-ttu-id="068de-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="068de-107">Syntax</span></span>

``` syntax
<Password>

  string

</Password>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="068de-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="068de-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="068de-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="068de-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="068de-110">Нет.</span><span class="sxs-lookup"><span data-stu-id="068de-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="068de-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="068de-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="068de-112">Нет.</span><span class="sxs-lookup"><span data-stu-id="068de-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="068de-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="068de-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="068de-114">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="068de-114">Parent Element</span></span></th>
<th><span data-ttu-id="068de-115">Описание</span><span class="sxs-lookup"><span data-stu-id="068de-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="068de-116"><a href="element-1-userlogoncred.md">UserLogonCred</a></span><span class="sxs-lookup"><span data-stu-id="068de-116"><a href="element-1-userlogoncred.md">UserLogonCred</a></span></span></td>
<td><p><span data-ttu-id="068de-117">Учетные данные входа для подключения.</span><span class="sxs-lookup"><span data-stu-id="068de-117">Logon credentials for a connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="068de-118">Требования</span><span class="sxs-lookup"><span data-stu-id="068de-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="068de-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="068de-119">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
