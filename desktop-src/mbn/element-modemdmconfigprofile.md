---
description: ModemDMConfigProfile
MS-HAID: WWAN\_profile\_v4.element\_ModemDMConfigProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ModemDMConfigProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43f4593d1b55b4c95a2ec185fe5545ad7eb04141
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647161"
---
# <a name="span-idwwan_profile_v4element_modemdmconfigprofilespanmodemdmconfigprofile"></a><span data-ttu-id="18ede-103"><span id="WWAN_profile_v4.element_ModemDMConfigProfile"></span>модемдмконфигпрофиле</span><span class="sxs-lookup"><span data-stu-id="18ede-103"><span id="WWAN_profile_v4.element_ModemDMConfigProfile"></span>ModemDMConfigProfile</span></span>

<span data-ttu-id="18ede-104">Профиль конфигурации DM для модема.</span><span class="sxs-lookup"><span data-stu-id="18ede-104">Modem DM configuration profile.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="18ede-105">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="18ede-105">Element hierarchy</span></span>

**<ModemDMConfigProfile>**

## <a name="syntax"></a><span data-ttu-id="18ede-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18ede-106">Syntax</span></span>

``` syntax
<ModemDMConfigProfile>

  <!-- Child elements -->
  Name,
  SimIccID,
  ApnID,
  OemConnectionId,
  RoamApplicability?,
  Context,
  AdminEnable,
  AdminRoamControl,
  ProfileCreationType?,
  any element in a non-schema namespace*

</ModemDMConfigProfile>
```

### <a name="key"></a><span data-ttu-id="18ede-107">Ключ</span><span class="sxs-lookup"><span data-stu-id="18ede-107">Key</span></span>

<span data-ttu-id="18ede-108">`?`   необязательно (ноль или один)</span><span class="sxs-lookup"><span data-stu-id="18ede-108">`?`   optional (zero or one)</span></span>

<span data-ttu-id="18ede-109">`*`   необязательно (ноль или более)</span><span class="sxs-lookup"><span data-stu-id="18ede-109">`*`   optional (zero or more)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="18ede-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="18ede-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="18ede-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="18ede-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="18ede-112">Нет.</span><span class="sxs-lookup"><span data-stu-id="18ede-112">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="18ede-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="18ede-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="18ede-114">Дочерний элемент</span><span class="sxs-lookup"><span data-stu-id="18ede-114">Child Element</span></span></th>
<th><span data-ttu-id="18ede-115">Описание</span><span class="sxs-lookup"><span data-stu-id="18ede-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="18ede-116"><a href="element-1-adminenable.md">админенабле</a></span><span class="sxs-lookup"><span data-stu-id="18ede-116"><a href="element-1-adminenable.md">AdminEnable</a></span></span></td>
<td><p><span data-ttu-id="18ede-117">Указывает, включен ли профиль в административном состоянии. Это новый элемент для v4.</span><span class="sxs-lookup"><span data-stu-id="18ede-117">Specifies whether the profile is enabled administratively.This is a new element for v4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18ede-118"><a href="element-1-adminroamcontrol.md">админроамконтрол</a></span><span class="sxs-lookup"><span data-stu-id="18ede-118"><a href="element-1-adminroamcontrol.md">AdminRoamControl</a></span></span></td>
<td><p><span data-ttu-id="18ede-119">Указывает, управляется ли профиль административным роумингом.</span><span class="sxs-lookup"><span data-stu-id="18ede-119">Specifies whether the profile is administratively roam controlled.</span></span> <span data-ttu-id="18ede-120">Этот элемент является новым для v4.</span><span class="sxs-lookup"><span data-stu-id="18ede-120">This element is new for v4.</span></span> <span data-ttu-id="18ede-121">Значением этого элемента является значение <a href="simpletype-roamcontroltype.md"><strong>роамконтролтипе</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="18ede-121">The value of this element is a <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> value.</span></span> <span data-ttu-id="18ede-122">Это необязательный элемент. Если значение не указано, по умолчанию используется <strong>аллроамалловед</strong> .</span><span class="sxs-lookup"><span data-stu-id="18ede-122">This is an optional element; if no value is specified, then <strong>AllRoamAllowed</strong> is the default.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="18ede-123"><a href="element-1-apnid.md">апнид</a></span><span class="sxs-lookup"><span data-stu-id="18ede-123"><a href="element-1-apnid.md">ApnID</a></span></span></td>
<td><p><span data-ttu-id="18ede-124">Идентификатор APN, связанный с этим профилем. Этот элемент является новым в v4 и является необязательным.</span><span class="sxs-lookup"><span data-stu-id="18ede-124">An APN ID associated with this profile.This element is new in v4, and it is optional.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18ede-125"><a href="element-1-context.md">Контекст</a></span><span class="sxs-lookup"><span data-stu-id="18ede-125"><a href="element-1-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="18ede-126">Задает параметры, необходимые для установления подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="18ede-126">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="18ede-127"><a href="element-1-name.md">имя</a>;</span><span class="sxs-lookup"><span data-stu-id="18ede-127"><a href="element-1-name.md">Name</a></span></span></td>
<td><p><span data-ttu-id="18ede-128">Имя профиля.</span><span class="sxs-lookup"><span data-stu-id="18ede-128">The name of the profile.</span></span> <span data-ttu-id="18ede-129">Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-name-mbnprofile-element.md"><strong>имени</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="18ede-129">For more information, see the documentation for the v1 <a href="../mbn/schema-name-mbnprofile-element.md"><strong>Name</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18ede-130"><a href="element-oemconnectionid.md">оемконнектионид</a></span><span class="sxs-lookup"><span data-stu-id="18ede-130"><a href="element-oemconnectionid.md">OemConnectionId</a></span></span></td>
<td><p><span data-ttu-id="18ede-131">Идентификатор OEM-подключения для конфигурации DM модема.</span><span class="sxs-lookup"><span data-stu-id="18ede-131">The OEM connection ID for the modem DM configuration.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="18ede-132"><a href="element-1-profilecreationtype.md">Профилекреатионтипе (в Модемдмконфигпрофиле)</a></span><span class="sxs-lookup"><span data-stu-id="18ede-132"><a href="element-1-profilecreationtype.md">ProfileCreationType (in ModemDMConfigProfile)</a></span></span></td>
<td><p><span data-ttu-id="18ede-133">Указывает, каким способом был создан профиль DM для модема.</span><span class="sxs-lookup"><span data-stu-id="18ede-133">Specifies how this modem DM profile was created.</span></span></p>
<p><span data-ttu-id="18ede-134">Это значение используется для принятия решения о том, может ли пользователь удалить профиль.</span><span class="sxs-lookup"><span data-stu-id="18ede-134">This value is used to decide whether a user can delete the profile.</span></span> <span data-ttu-id="18ede-135">Пользователи могут удалять только профили <strong>усерпровисионед</strong> .</span><span class="sxs-lookup"><span data-stu-id="18ede-135">Users can only delete <strong>UserProvisioned</strong> profiles.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18ede-136"><a href="element-1-roamapplicability.md">роамаппликабилити</a></span><span class="sxs-lookup"><span data-stu-id="18ede-136"><a href="element-1-roamapplicability.md">RoamApplicability</a></span></span></td>
<td><p><span data-ttu-id="18ede-137">Указывает, что этот профиль активен, только если указано текущее перемещаемое условие.</span><span class="sxs-lookup"><span data-stu-id="18ede-137">Specifies that this profile is active only when the current roaming condition is the one specified.</span></span> <span data-ttu-id="18ede-138">В противном случае профиль неприменим и не может использоваться для активации контекста протокола данных пакетов (PDP).</span><span class="sxs-lookup"><span data-stu-id="18ede-138">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="18ede-139">Значение этого элемента должно быть допустимым значением <a href="simpletype-roamapplicabilitytype.md"><strong>роамаппликабилититипе</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="18ede-139">The value of this element must be a valid <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> value.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="18ede-140"><a href="element-1-simiccid.md">симикЦид</a></span><span class="sxs-lookup"><span data-stu-id="18ede-140"><a href="element-1-simiccid.md">SimIccID</a></span></span></td>
<td><p><span data-ttu-id="18ede-141">Номер Идентифкатион SIM для устройств GSM.</span><span class="sxs-lookup"><span data-stu-id="18ede-141">The SIM Identifcation number for GSM devices.</span></span> <span data-ttu-id="18ede-142">Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-simiccid-mbnprofile-element.md"><strong>симикЦид</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="18ede-142">For more details , see the documentation for the v1 <a href="../mbn/schema-simiccid-mbnprofile-element.md"><strong>SimIccID</strong></a> element.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="18ede-143"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="18ede-143"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<span data-ttu-id="18ede-144">Этот внешний элемент (Document) не может содержаться в каких-либо других элементах.</span><span class="sxs-lookup"><span data-stu-id="18ede-144">This outermost (document) element may not be contained by any other elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="18ede-145">Требования</span><span class="sxs-lookup"><span data-stu-id="18ede-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18ede-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="18ede-146">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



