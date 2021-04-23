---
description: Модемдмконфигпрофиле \/ ... \/ Игнорепассворд (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_IgnorePassword
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Игнорепассворд (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0286fcc7a025bc565916e68b817c6a79f378f26d
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388795"
---
# <a name="span-idwwan_profile_v4element_1_ignorepasswordspanmodemdmconfigprofileignorepassword-v4"></a><span data-ttu-id="c9bfc-103"><span id="WWAN_profile_v4.element_1_IgnorePassword"></span>Модемдмконфигпрофиле \/ ... \/ Игнорепассворд (v4)</span><span class="sxs-lookup"><span data-stu-id="c9bfc-103"><span id="WWAN_profile_v4.element_1_IgnorePassword"></span>ModemDMConfigProfile\/...\/IgnorePassword (v4)</span></span>

<span data-ttu-id="c9bfc-104">Указывает способ обработки паролей при обновлении профилей.</span><span class="sxs-lookup"><span data-stu-id="c9bfc-104">Specifies how passwords are handled when upgrading profiles.</span></span>

<span data-ttu-id="c9bfc-105">Если задано значение **true** и профиль с тем же именем существует во время операции обновления, то пароль из этого профиля будет создан и сохранен в новом профиле.</span><span class="sxs-lookup"><span data-stu-id="c9bfc-105">If set to **TRUE** and a profile with the same name exists at the time of the update operation, then the password from that profile will be taken and stored in the new profile.</span></span>

<span data-ttu-id="c9bfc-106">Дополнительные сведения см. в документации по элементу [**игнорепассворд**](./schema-ignorepassword-userlogoncred-element.md) v1.</span><span class="sxs-lookup"><span data-stu-id="c9bfc-106">For more details, see the documentation for the v1 [**IgnorePassword**](./schema-ignorepassword-userlogoncred-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="c9bfc-107">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="c9bfc-107">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<IgnorePassword\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-1-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<IgnorePassword\>**

## <a name="syntax"></a><span data-ttu-id="c9bfc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9bfc-108">Syntax</span></span>

``` syntax
<IgnorePassword>

  boolean

</IgnorePassword>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="c9bfc-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="c9bfc-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="c9bfc-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c9bfc-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="c9bfc-111">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="c9bfc-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="c9bfc-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c9bfc-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="c9bfc-113">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="c9bfc-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="c9bfc-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="c9bfc-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c9bfc-115">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="c9bfc-115">Parent Element</span></span></th>
<th><span data-ttu-id="c9bfc-116">Описание</span><span class="sxs-lookup"><span data-stu-id="c9bfc-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c9bfc-117"><a href="element-1-userlogoncred.md">UserLogonCred</a></span><span class="sxs-lookup"><span data-stu-id="c9bfc-117"><a href="element-1-userlogoncred.md">UserLogonCred</a></span></span></td>
<td><p><span data-ttu-id="c9bfc-118">Учетные данные входа для подключения.</span><span class="sxs-lookup"><span data-stu-id="c9bfc-118">Logon credentials for a connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="c9bfc-119">Требования</span><span class="sxs-lookup"><span data-stu-id="c9bfc-119">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c9bfc-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c9bfc-120">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
