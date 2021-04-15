---
description: Мбнпрофиликст \/ ... \/ Усерлогонкред (v4)
MS-HAID: WWAN\_profile\_v4.element\_UserLogonCred
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: UserLogonCred
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 12a65d91-1917-49d4-9b58-68c60464c857
api_name:
- UserLogonCred
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3f6999763e82051fa30af6109c3a04ae8dc65f77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682749"
---
# <a name="span-idwwan_profile_v4element_userlogoncredspanmbnprofileextuserlogoncred-v4"></a><span data-ttu-id="e100f-103"><span id="WWAN_profile_v4.element_UserLogonCred"></span>Мбнпрофиликст \/ ... \/ Усерлогонкред (v4)</span><span class="sxs-lookup"><span data-stu-id="e100f-103"><span id="WWAN_profile_v4.element_UserLogonCred"></span>MBNProfileExt\/...\/UserLogonCred (v4)</span></span>

<span data-ttu-id="e100f-104">Учетные данные входа для подключения.</span><span class="sxs-lookup"><span data-stu-id="e100f-104">Logon credentials for a connection.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="e100f-105">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="e100f-105">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<UserLogonCred\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-1-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<UserLogonCred\>**

## <a name="syntax"></a><span data-ttu-id="e100f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e100f-106">Syntax</span></span>

``` syntax
<UserLogonCred>

  <!-- Child elements -->
  UserName,
  IgnorePassword?,
  Password?

</UserLogonCred>
```

### <a name="key"></a><span data-ttu-id="e100f-107">Ключ</span><span class="sxs-lookup"><span data-stu-id="e100f-107">Key</span></span>

<span data-ttu-id="e100f-108">`?`   необязательно (ноль или один)</span><span class="sxs-lookup"><span data-stu-id="e100f-108">`?`   optional (zero or one)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="e100f-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="e100f-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="e100f-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e100f-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="e100f-111">Нет.</span><span class="sxs-lookup"><span data-stu-id="e100f-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="e100f-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e100f-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e100f-113">Дочерний элемент</span><span class="sxs-lookup"><span data-stu-id="e100f-113">Child Element</span></span></th>
<th><span data-ttu-id="e100f-114">Описание</span><span class="sxs-lookup"><span data-stu-id="e100f-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e100f-115"><a href="element-ignorepassword.md">игнорепассворд</a></span><span class="sxs-lookup"><span data-stu-id="e100f-115"><a href="element-ignorepassword.md">IgnorePassword</a></span></span></td>
<td><p><span data-ttu-id="e100f-116">Указывает способ обработки паролей при обновлении профилей.</span><span class="sxs-lookup"><span data-stu-id="e100f-116">Specifies how passwords are handled when upgrading profiles.</span></span></p>
<p><span data-ttu-id="e100f-117">Если задано значение <strong>true</strong> и профиль с тем же именем существует во время операции обновления, то пароль из этого профиля будет создан и сохранен в новом профиле.</span><span class="sxs-lookup"><span data-stu-id="e100f-117">If set to <strong>TRUE</strong> and a profile with the same name exists at the time of the update operation, then the password from that profile will be taken and stored in the new profile.</span></span></p>
<p><span data-ttu-id="e100f-118">Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-ignorepassword-userlogoncred-element.md"><strong>игнорепассворд</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="e100f-118">For more details, see the documentation for the v1 <a href="../mbn/schema-ignorepassword-userlogoncred-element.md"><strong>IgnorePassword</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e100f-119"><a href="element-password.md">Пароль</a></span><span class="sxs-lookup"><span data-stu-id="e100f-119"><a href="element-password.md">Password</a></span></span></td>
<td><p><span data-ttu-id="e100f-120">Указывает пароль, используемый для проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="e100f-120">Specifies the password used to authenticate a user.</span></span></p>
<p><span data-ttu-id="e100f-121">Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-password-userlogoncred-element.md"><strong>пароля</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="e100f-121">For more information, see the documentation for the v1 <a href="../mbn/schema-password-userlogoncred-element.md"><strong>Password</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e100f-122"><a href="element-username.md">UserName</a></span><span class="sxs-lookup"><span data-stu-id="e100f-122"><a href="element-username.md">UserName</a></span></span></td>
<td><p><span data-ttu-id="e100f-123">Имя пользователя, используемое для входа в систему.</span><span class="sxs-lookup"><span data-stu-id="e100f-123">The user name to use for logon.</span></span></p>
<p><span data-ttu-id="e100f-124">Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-username-userlogoncred-element.md"><strong>имени пользователя</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="e100f-124">For more details, see the documentation for the v1 <a href="../mbn/schema-username-userlogoncred-element.md"><strong>UserName</strong></a> element.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="e100f-125"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="e100f-125"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e100f-126">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="e100f-126">Parent Element</span></span></th>
<th><span data-ttu-id="e100f-127">Описание</span><span class="sxs-lookup"><span data-stu-id="e100f-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e100f-128"><a href="element-context.md">Контекст</a></span><span class="sxs-lookup"><span data-stu-id="e100f-128"><a href="element-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="e100f-129">Задает параметры, необходимые для установления подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="e100f-129">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="e100f-130">Требования</span><span class="sxs-lookup"><span data-stu-id="e100f-130">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e100f-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e100f-131">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



