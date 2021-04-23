---
description: Мбнпрофиликст \/ ... \/ Игнорепассворд (v4)
MS-HAID: WWAN\_profile\_v4.element\_IgnorePassword
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: игнорепассворд
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc73050a01f6f0f9799290ba267b8ecaaee1003a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263186"
---
# <a name="span-idwwan_profile_v4element_ignorepasswordspanmbnprofileextignorepassword-v4"></a><span data-ttu-id="cb338-103"><span id="WWAN_profile_v4.element_IgnorePassword"></span>Мбнпрофиликст \/ ... \/ Игнорепассворд (v4)</span><span class="sxs-lookup"><span data-stu-id="cb338-103"><span id="WWAN_profile_v4.element_IgnorePassword"></span>MBNProfileExt\/...\/IgnorePassword (v4)</span></span>

<span data-ttu-id="cb338-104">Указывает способ обработки паролей при обновлении профилей.</span><span class="sxs-lookup"><span data-stu-id="cb338-104">Specifies how passwords are handled when upgrading profiles.</span></span>

<span data-ttu-id="cb338-105">Если задано значение **true** и профиль с тем же именем существует во время операции обновления, то пароль из этого профиля будет создан и сохранен в новом профиле.</span><span class="sxs-lookup"><span data-stu-id="cb338-105">If set to **TRUE** and a profile with the same name exists at the time of the update operation, then the password from that profile will be taken and stored in the new profile.</span></span>

<span data-ttu-id="cb338-106">Дополнительные сведения см. в документации по элементу [**игнорепассворд**](./schema-ignorepassword-userlogoncred-element.md) v1.</span><span class="sxs-lookup"><span data-stu-id="cb338-106">For more details, see the documentation for the v1 [**IgnorePassword**](./schema-ignorepassword-userlogoncred-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="cb338-107">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="cb338-107">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<IgnorePassword\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-1-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<IgnorePassword\>**

## <a name="syntax"></a><span data-ttu-id="cb338-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb338-108">Syntax</span></span>

``` syntax
<IgnorePassword>

  boolean

</IgnorePassword>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="cb338-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="cb338-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="cb338-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="cb338-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="cb338-111">Нет.</span><span class="sxs-lookup"><span data-stu-id="cb338-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="cb338-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="cb338-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="cb338-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="cb338-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="cb338-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="cb338-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cb338-115">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="cb338-115">Parent Element</span></span></th>
<th><span data-ttu-id="cb338-116">Описание</span><span class="sxs-lookup"><span data-stu-id="cb338-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cb338-117"><a href="element-userlogoncred.md">UserLogonCred</a></span><span class="sxs-lookup"><span data-stu-id="cb338-117"><a href="element-userlogoncred.md">UserLogonCred</a></span></span></td>
<td><p><span data-ttu-id="cb338-118">Учетные данные входа для подключения.</span><span class="sxs-lookup"><span data-stu-id="cb338-118">Logon credentials for a connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="cb338-119">Требования</span><span class="sxs-lookup"><span data-stu-id="cb338-119">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb338-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cb338-120">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
