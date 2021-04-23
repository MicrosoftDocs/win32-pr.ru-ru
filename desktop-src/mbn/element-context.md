---
description: '\/Контекст мбнпрофиликст (v4)'
MS-HAID: WWAN\_profile\_v4.element\_Context
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Контекст
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: eff61884-1d37-4e1a-85f0-2fadf14227ac
api_name:
- Context
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8ec231b5d7e2769d86262864e0b9a53621c36a99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719335"
---
# <a name="span-idwwan_profile_v4element_contextspanmbnprofileextcontext-v4"></a><span data-ttu-id="bb101-103"><span id="WWAN_profile_v4.element_Context"></span>\/Контекст мбнпрофиликст (v4)</span><span class="sxs-lookup"><span data-stu-id="bb101-103"><span id="WWAN_profile_v4.element_Context"></span>MBNProfileExt\/Context (v4)</span></span>

<span data-ttu-id="bb101-104">Задает параметры, необходимые для установления подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="bb101-104">Specifies the parameters required to establish a data connection.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="bb101-105">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="bb101-105">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<Context\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<Context\>**

## <a name="syntax"></a><span data-ttu-id="bb101-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb101-106">Syntax</span></span>

``` syntax
<Context>

  <!-- Child elements -->
  AccessString?,
  UserLogonCred?,
  Compression?,
  AuthProtocol?,
  IPType?

</Context>
```

### <a name="key"></a><span data-ttu-id="bb101-107">Ключ</span><span class="sxs-lookup"><span data-stu-id="bb101-107">Key</span></span>

<span data-ttu-id="bb101-108">`?`   необязательно (ноль или один)</span><span class="sxs-lookup"><span data-stu-id="bb101-108">`?`   optional (zero or one)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="bb101-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="bb101-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="bb101-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="bb101-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="bb101-111">Нет.</span><span class="sxs-lookup"><span data-stu-id="bb101-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="bb101-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="bb101-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bb101-113">Дочерний элемент</span><span class="sxs-lookup"><span data-stu-id="bb101-113">Child Element</span></span></th>
<th><span data-ttu-id="bb101-114">Описание</span><span class="sxs-lookup"><span data-stu-id="bb101-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bb101-115"><a href="element-accessstring.md">AccessString</a></span><span class="sxs-lookup"><span data-stu-id="bb101-115"><a href="element-accessstring.md">AccessString</a></span></span></td>
<td><p><span data-ttu-id="bb101-116">Определяет имя APN или строку вызова, используемые для установки подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="bb101-116">Identifies the APN or dial string to be used to establish a data connection.</span></span></p>
<p><span data-ttu-id="bb101-117">Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-accessstring-contexttype-element.md"><strong>акцессстринг</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="bb101-117">For more information, see the documentation for the v1 <a href="../mbn/schema-accessstring-contexttype-element.md"><strong>AccessString</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb101-118"><a href="element-authprotocol.md">AuthProtocol</a></span><span class="sxs-lookup"><span data-stu-id="bb101-118"><a href="element-authprotocol.md">AuthProtocol</a></span></span></td>
<td><p><span data-ttu-id="bb101-119">>Указывает протокол проверки подлинности, используемый для активации контекста протокола данных пакетов (PDP).</span><span class="sxs-lookup"><span data-stu-id="bb101-119">>Specifies the authentication protocol to be used for activating a Packet Data Protocol (PDP) context.</span></span></p>
<p><span data-ttu-id="bb101-120">Обратите внимание, что в версии v4 для этого элемента доступно новое значение перечисления.</span><span class="sxs-lookup"><span data-stu-id="bb101-120">Note that in v4, a new enumeration value is available for this element.</span></span> <span data-ttu-id="bb101-121"><strong>Автовыбор</strong> означает, что протокол проверки подлинности должен быть выбран более низкими слоями.</span><span class="sxs-lookup"><span data-stu-id="bb101-121"><strong>AutoSelection</strong> means that an auth protocol is to be picked by lower layer(s).</span></span></p>
<p><span data-ttu-id="bb101-122">Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-authprotocol-contexttype-element.md"><strong>ауспротокол</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="bb101-122">For further information, see the documentation for the v1 <a href="../mbn/schema-authprotocol-contexttype-element.md"><strong>AuthProtocol</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bb101-123"><a href="element-compression.md">Сжатие</a></span><span class="sxs-lookup"><span data-stu-id="bb101-123"><a href="element-compression.md">Compression</a></span></span></td>
<td><p><span data-ttu-id="bb101-124">Указывает, будет ли использоваться сжатие по каналу данных для заголовка и передачи данных.</span><span class="sxs-lookup"><span data-stu-id="bb101-124">Specifies whether compression will be used at the data link for header and data transfer.</span></span></p>
<p><span data-ttu-id="bb101-125">Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-compression-contexttype-element.md"><strong>сжатия</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="bb101-125">For more information, see the documentation for the v1 <a href="../mbn/schema-compression-contexttype-element.md"><strong>Compression</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb101-126"><a href="element-iptype.md">IPType</a></span><span class="sxs-lookup"><span data-stu-id="bb101-126"><a href="element-iptype.md">IPType</a></span></span></td>
<td><p><span data-ttu-id="bb101-127">Указывает тип IP-адреса, используемый для этого подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="bb101-127">Specifies the IP type to be used on this data connection.</span></span></p>
<p><span data-ttu-id="bb101-128">Этот элемент впервые находится в версии v4 схемы.</span><span class="sxs-lookup"><span data-stu-id="bb101-128">This element is new in v4 of the schema.</span></span> <span data-ttu-id="bb101-129">Элемент может иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="bb101-129">The element can have one of the following values.</span></span></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="bb101-130">Значение</span><span class="sxs-lookup"><span data-stu-id="bb101-130">Value</span></span></th>
<th><span data-ttu-id="bb101-131">Значение</span><span class="sxs-lookup"><span data-stu-id="bb101-131">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bb101-132">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="bb101-132">Default</span></span></td>
<td><span data-ttu-id="bb101-133">Тип IP-адреса должен быть выбран более низкими слоями</span><span class="sxs-lookup"><span data-stu-id="bb101-133">IP type is to be picked by lower layer(s)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb101-134">IPv4</span><span class="sxs-lookup"><span data-stu-id="bb101-134">IPv4</span></span></td>
<td><span data-ttu-id="bb101-135">Использовать IPv4</span><span class="sxs-lookup"><span data-stu-id="bb101-135">Use IPv4</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bb101-136">IPv6;</span><span class="sxs-lookup"><span data-stu-id="bb101-136">IPv6</span></span></td>
<td><span data-ttu-id="bb101-137">использовать IPv6</span><span class="sxs-lookup"><span data-stu-id="bb101-137">Use IPv6</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb101-138">IPv4v6</span><span class="sxs-lookup"><span data-stu-id="bb101-138">IPv4v6</span></span></td>
<td><span data-ttu-id="bb101-139">Используйте IPv4 и (или) IPv6, как доступно.</span><span class="sxs-lookup"><span data-stu-id="bb101-139">Use IPv4 and/or IPv6, as available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bb101-140">кслат</span><span class="sxs-lookup"><span data-stu-id="bb101-140">XLAT</span></span></td>
<td><span data-ttu-id="bb101-141">Использование 464XLAT для туннелирования IPv4 через IPv6-сети</span><span class="sxs-lookup"><span data-stu-id="bb101-141">Use 464XLAT to tunnel IPv4 over IPv6 networks</span></span></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bb101-142"><a href="element-userlogoncred.md">UserLogonCred</a></span><span class="sxs-lookup"><span data-stu-id="bb101-142"><a href="element-userlogoncred.md">UserLogonCred</a></span></span></td>
<td><p><span data-ttu-id="bb101-143">Учетные данные входа для подключения.</span><span class="sxs-lookup"><span data-stu-id="bb101-143">Logon credentials for a connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="bb101-144"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="bb101-144"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bb101-145">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="bb101-145">Parent Element</span></span></th>
<th><span data-ttu-id="bb101-146">Описание</span><span class="sxs-lookup"><span data-stu-id="bb101-146">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bb101-147"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="bb101-147"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="bb101-148">Элемент <strong>мбнпрофиликст</strong> является расширением более раннего элемента мбнпрофиле.</span><span class="sxs-lookup"><span data-stu-id="bb101-148">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="bb101-149">Он определяет профиль мобильного широкополосного подключения с более широким набором параметров, чем элемент Мбнпрофиле.</span><span class="sxs-lookup"><span data-stu-id="bb101-149">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="bb101-150">В профиле может быть несколько элементов Мбнпрофиликст, описывающих параметры профиля для определенного набора условий.</span><span class="sxs-lookup"><span data-stu-id="bb101-150">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="bb101-151">Используйте дочерний элемент <a href="element-profileconditionedon.md"><strong>профилекондитионедон</strong></a> из <strong>мбнпрофиликст</strong> , чтобы указать, какие операционные условия делают определенный профиль активным.</span><span class="sxs-lookup"><span data-stu-id="bb101-151">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb101-152"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="bb101-152"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="bb101-153">Профиль конфигурации DM для модема.</span><span class="sxs-lookup"><span data-stu-id="bb101-153">Modem DM configuration profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="bb101-154">Требования</span><span class="sxs-lookup"><span data-stu-id="bb101-154">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb101-155">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bb101-155">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



