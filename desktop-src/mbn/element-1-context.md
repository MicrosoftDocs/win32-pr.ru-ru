---
description: '\/Контекст модемдмконфигпрофиле (v4)'
MS-HAID: WWAN\_profile\_v4.element\_1\_Context
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Контекст (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8f463f14-95b3-4364-b1b1-549a32291959
api_name:
- Context
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 133f48d9c9a1c9dd9f0e04f59d5e35478caa9227
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388851"
---
# <a name="span-idwwan_profile_v4element_1_contextspanmodemdmconfigprofilecontext-v4"></a><span data-ttu-id="2bdc8-103"><span id="WWAN_profile_v4.element_1_Context"></span>\/Контекст модемдмконфигпрофиле (v4)</span><span class="sxs-lookup"><span data-stu-id="2bdc8-103"><span id="WWAN_profile_v4.element_1_Context"></span>ModemDMConfigProfile\/Context (v4)</span></span>

<span data-ttu-id="2bdc8-104">Задает параметры, необходимые для установления подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="2bdc8-104">Specifies the parameters required to establish a data connection.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="2bdc8-105">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="2bdc8-105">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<Context\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<Context\>**

## <a name="syntax"></a><span data-ttu-id="2bdc8-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2bdc8-106">Syntax</span></span>

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

### <a name="key"></a><span data-ttu-id="2bdc8-107">Ключ</span><span class="sxs-lookup"><span data-stu-id="2bdc8-107">Key</span></span>

<span data-ttu-id="2bdc8-108">`?`   необязательно (ноль или один)</span><span class="sxs-lookup"><span data-stu-id="2bdc8-108">`?`   optional (zero or one)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="2bdc8-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="2bdc8-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="2bdc8-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="2bdc8-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="2bdc8-111">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="2bdc8-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="2bdc8-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="2bdc8-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bdc8-113">Дочерний элемент</span><span class="sxs-lookup"><span data-stu-id="2bdc8-113">Child Element</span></span></th>
<th><span data-ttu-id="2bdc8-114">Описание</span><span class="sxs-lookup"><span data-stu-id="2bdc8-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2bdc8-115"><a href="element-1-accessstring.md">AccessString</a></span><span class="sxs-lookup"><span data-stu-id="2bdc8-115"><a href="element-1-accessstring.md">AccessString</a></span></span></td>
<td><p><span data-ttu-id="2bdc8-116">Определяет имя APN или строку вызова, используемые для установки подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="2bdc8-116">Identifies the APN or dial string to be used to establish a data connection.</span></span></p>
<p><span data-ttu-id="2bdc8-117">Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-accessstring-contexttype-element.md"><strong>акцессстринг</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="2bdc8-117">For more information, see the documentation for the v1 <a href="../mbn/schema-accessstring-contexttype-element.md"><strong>AccessString</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bdc8-118"><a href="element-1-authprotocol.md">AuthProtocol</a></span><span class="sxs-lookup"><span data-stu-id="2bdc8-118"><a href="element-1-authprotocol.md">AuthProtocol</a></span></span></td>
<td><p><span data-ttu-id="2bdc8-119">>Указывает протокол проверки подлинности, используемый для активации контекста протокола данных пакетов (PDP).</span><span class="sxs-lookup"><span data-stu-id="2bdc8-119">>Specifies the authentication protocol to be used for activating a Packet Data Protocol (PDP) context.</span></span></p>
<p><span data-ttu-id="2bdc8-120">Обратите внимание, что в версии v4 для этого элемента доступно новое значение перечисления.</span><span class="sxs-lookup"><span data-stu-id="2bdc8-120">Note that in v4, a new enumeration value is available for this element.</span></span> <span data-ttu-id="2bdc8-121"><strong>Автовыбор</strong> означает, что протокол проверки подлинности должен быть выбран более низкими слоями.</span><span class="sxs-lookup"><span data-stu-id="2bdc8-121"><strong>AutoSelection</strong> means that an auth protocol is to be picked by lower layer(s).</span></span></p>
<p><span data-ttu-id="2bdc8-122">Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-authprotocol-contexttype-element.md"><strong>ауспротокол</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="2bdc8-122">For further information, see the documentation for the v1 <a href="../mbn/schema-authprotocol-contexttype-element.md"><strong>AuthProtocol</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2bdc8-123"><a href="element-1-compression.md">Сжатие</a></span><span class="sxs-lookup"><span data-stu-id="2bdc8-123"><a href="element-1-compression.md">Compression</a></span></span></td>
<td><p><span data-ttu-id="2bdc8-124">Указывает, будет ли использоваться сжатие по каналу данных для заголовка и передачи данных.</span><span class="sxs-lookup"><span data-stu-id="2bdc8-124">Specifies whether compression will be used at the data link for header and data transfer.</span></span></p>
<p><span data-ttu-id="2bdc8-125">Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-compression-contexttype-element.md"><strong>сжатия</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="2bdc8-125">For more information, see the documentation for the v1 <a href="../mbn/schema-compression-contexttype-element.md"><strong>Compression</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bdc8-126"><a href="element-1-iptype.md">IPType</a></span><span class="sxs-lookup"><span data-stu-id="2bdc8-126"><a href="element-1-iptype.md">IPType</a></span></span></td>
<td><p><span data-ttu-id="2bdc8-127">Указывает тип IP-адреса, используемый для этого подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="2bdc8-127">Specifies the IP type to be used on this data connection.</span></span></p>
<p><span data-ttu-id="2bdc8-128">Этот элемент впервые находится в версии v4 схемы.</span><span class="sxs-lookup"><span data-stu-id="2bdc8-128">This element is new in v4 of the schema.</span></span> <span data-ttu-id="2bdc8-129">Элемент может иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="2bdc8-129">The element can have one of the following values.</span></span></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2bdc8-130">Значение</span><span class="sxs-lookup"><span data-stu-id="2bdc8-130">Value</span></span></th>
<th><span data-ttu-id="2bdc8-131">Значение</span><span class="sxs-lookup"><span data-stu-id="2bdc8-131">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2bdc8-132">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2bdc8-132">Default</span></span></td>
<td><span data-ttu-id="2bdc8-133">Тип IP-адреса должен быть выбран более низкими слоями</span><span class="sxs-lookup"><span data-stu-id="2bdc8-133">IP type is to be picked by lower layer(s)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bdc8-134">IPv4</span><span class="sxs-lookup"><span data-stu-id="2bdc8-134">IPv4</span></span></td>
<td><span data-ttu-id="2bdc8-135">Использовать IPv4</span><span class="sxs-lookup"><span data-stu-id="2bdc8-135">Use IPv4</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2bdc8-136">IPv6</span><span class="sxs-lookup"><span data-stu-id="2bdc8-136">IPv6</span></span></td>
<td><span data-ttu-id="2bdc8-137">использовать IPv6</span><span class="sxs-lookup"><span data-stu-id="2bdc8-137">Use IPv6</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bdc8-138">IPv4v6</span><span class="sxs-lookup"><span data-stu-id="2bdc8-138">IPv4v6</span></span></td>
<td><span data-ttu-id="2bdc8-139">Используйте IPv4 и (или) IPv6, как доступно.</span><span class="sxs-lookup"><span data-stu-id="2bdc8-139">Use IPv4 and/or IPv6, as available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2bdc8-140">кслат</span><span class="sxs-lookup"><span data-stu-id="2bdc8-140">XLAT</span></span></td>
<td><span data-ttu-id="2bdc8-141">Использование 464XLAT для туннелирования IPv4 через IPv6-сети</span><span class="sxs-lookup"><span data-stu-id="2bdc8-141">Use 464XLAT to tunnel IPv4 over IPv6 networks</span></span></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2bdc8-142"><a href="element-1-userlogoncred.md">UserLogonCred</a></span><span class="sxs-lookup"><span data-stu-id="2bdc8-142"><a href="element-1-userlogoncred.md">UserLogonCred</a></span></span></td>
<td><p><span data-ttu-id="2bdc8-143">Учетные данные входа для подключения.</span><span class="sxs-lookup"><span data-stu-id="2bdc8-143">Logon credentials for a connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="2bdc8-144"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="2bdc8-144"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bdc8-145">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="2bdc8-145">Parent Element</span></span></th>
<th><span data-ttu-id="2bdc8-146">Описание</span><span class="sxs-lookup"><span data-stu-id="2bdc8-146">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2bdc8-147"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="2bdc8-147"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="2bdc8-148">Элемент <strong>мбнпрофиликст</strong> является расширением более раннего элемента мбнпрофиле.</span><span class="sxs-lookup"><span data-stu-id="2bdc8-148">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="2bdc8-149">Он определяет профиль мобильного широкополосного подключения с более широким набором параметров, чем элемент Мбнпрофиле.</span><span class="sxs-lookup"><span data-stu-id="2bdc8-149">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="2bdc8-150">В профиле может быть несколько элементов Мбнпрофиликст, описывающих параметры профиля для определенного набора условий.</span><span class="sxs-lookup"><span data-stu-id="2bdc8-150">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="2bdc8-151">Используйте дочерний элемент <a href="element-profileconditionedon.md"><strong>профилекондитионедон</strong></a> из <strong>мбнпрофиликст</strong> , чтобы указать, какие операционные условия делают определенный профиль активным.</span><span class="sxs-lookup"><span data-stu-id="2bdc8-151">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bdc8-152"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="2bdc8-152"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="2bdc8-153">Профиль конфигурации DM для модема.</span><span class="sxs-lookup"><span data-stu-id="2bdc8-153">Modem DM configuration profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="2bdc8-154">Требования</span><span class="sxs-lookup"><span data-stu-id="2bdc8-154">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2bdc8-155">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2bdc8-155">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



