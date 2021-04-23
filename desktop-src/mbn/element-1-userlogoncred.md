---
description: Модемдмконфигпрофиле \/ ... \/ Усерлогонкред (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_UserLogonCred
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Усерлогонкред (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6d563cf8-ea40-46b3-a74e-ec7640ca9824
api_name:
- UserLogonCred
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: aea2cdfda61e557ff790b59e7af2a05d914d3403
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388774"
---
# <a name="span-idwwan_profile_v4element_1_userlogoncredspanmodemdmconfigprofileuserlogoncred-v4"></a><span data-ttu-id="09483-103"><span id="WWAN_profile_v4.element_1_UserLogonCred"></span>Модемдмконфигпрофиле \/ ... \/ Усерлогонкред (v4)</span><span class="sxs-lookup"><span data-stu-id="09483-103"><span id="WWAN_profile_v4.element_1_UserLogonCred"></span>ModemDMConfigProfile\/...\/UserLogonCred (v4)</span></span>

<span data-ttu-id="09483-104">Учетные данные входа для подключения.</span><span class="sxs-lookup"><span data-stu-id="09483-104">Logon credentials for a connection.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="09483-105">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="09483-105">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<UserLogonCred\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-1-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<UserLogonCred\>**

## <a name="syntax"></a><span data-ttu-id="09483-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09483-106">Syntax</span></span>

``` syntax
<UserLogonCred>

  <!-- Child elements -->
  UserName,
  IgnorePassword?,
  Password?

</UserLogonCred>
```

### <a name="key"></a><span data-ttu-id="09483-107">Ключ</span><span class="sxs-lookup"><span data-stu-id="09483-107">Key</span></span>

<span data-ttu-id="09483-108">`?`   необязательно (ноль или один)</span><span class="sxs-lookup"><span data-stu-id="09483-108">`?`   optional (zero or one)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="09483-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="09483-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="09483-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="09483-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="09483-111">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="09483-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="09483-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="09483-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="09483-113">Дочерний элемент</span><span class="sxs-lookup"><span data-stu-id="09483-113">Child Element</span></span></th>
<th><span data-ttu-id="09483-114">Описание</span><span class="sxs-lookup"><span data-stu-id="09483-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="09483-115"><a href="element-1-ignorepassword.md">игнорепассворд</a></span><span class="sxs-lookup"><span data-stu-id="09483-115"><a href="element-1-ignorepassword.md">IgnorePassword</a></span></span></td>
<td><p><span data-ttu-id="09483-116">Указывает способ обработки паролей при обновлении профилей.</span><span class="sxs-lookup"><span data-stu-id="09483-116">Specifies how passwords are handled when upgrading profiles.</span></span></p>
<p><span data-ttu-id="09483-117">Если задано значение <strong>true</strong> и профиль с тем же именем существует во время операции обновления, то пароль из этого профиля будет создан и сохранен в новом профиле.</span><span class="sxs-lookup"><span data-stu-id="09483-117">If set to <strong>TRUE</strong> and a profile with the same name exists at the time of the update operation, then the password from that profile will be taken and stored in the new profile.</span></span></p>
<p><span data-ttu-id="09483-118">Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-ignorepassword-userlogoncred-element.md"><strong>игнорепассворд</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="09483-118">For more details, see the documentation for the v1 <a href="../mbn/schema-ignorepassword-userlogoncred-element.md"><strong>IgnorePassword</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09483-119"><a href="element-1-password.md">Пароль</a></span><span class="sxs-lookup"><span data-stu-id="09483-119"><a href="element-1-password.md">Password</a></span></span></td>
<td><p><span data-ttu-id="09483-120">Указывает пароль, используемый для проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="09483-120">Specifies the password used to authenticate a user.</span></span></p>
<p><span data-ttu-id="09483-121">Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-password-userlogoncred-element.md"><strong>пароля</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="09483-121">For more information, see the documentation for the v1 <a href="../mbn/schema-password-userlogoncred-element.md"><strong>Password</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09483-122"><a href="element-1-username.md">UserName</a></span><span class="sxs-lookup"><span data-stu-id="09483-122"><a href="element-1-username.md">UserName</a></span></span></td>
<td><p><span data-ttu-id="09483-123">Имя пользователя, используемое для входа в систему.</span><span class="sxs-lookup"><span data-stu-id="09483-123">The user name to use for logon.</span></span></p>
<p><span data-ttu-id="09483-124">Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-username-userlogoncred-element.md"><strong>имени пользователя</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="09483-124">For more details, see the documentation for the v1 <a href="../mbn/schema-username-userlogoncred-element.md"><strong>UserName</strong></a> element.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="09483-125"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="09483-125"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="09483-126">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="09483-126">Parent Element</span></span></th>
<th><span data-ttu-id="09483-127">Описание</span><span class="sxs-lookup"><span data-stu-id="09483-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="09483-128"><a href="element-1-context.md">Контекст</a></span><span class="sxs-lookup"><span data-stu-id="09483-128"><a href="element-1-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="09483-129">Задает параметры, необходимые для установления подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="09483-129">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="09483-130">Требования</span><span class="sxs-lookup"><span data-stu-id="09483-130">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09483-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="09483-131">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



