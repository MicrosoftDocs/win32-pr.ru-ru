---
description: Роамаппликабилититипе описывает условия роуминга, для которых применяется перемещаемый профиль.
MS-HAID: WWAN\_profile\_v4.simpleType\_roamApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Простой тип Роамаппликабилититипе
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95d81214ab5a44dcac60bb5e1a6accc81b0d0418
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897273"
---
# <a name="span-idwwan_profile_v4simpletype_roamapplicabilitytypespanroamapplicabilitytype-simple-type"></a><span data-ttu-id="5531d-103"><span id="WWAN_profile_v4.simpleType_roamApplicabilityType"></span>Простой тип Роамаппликабилититипе</span><span class="sxs-lookup"><span data-stu-id="5531d-103"><span id="WWAN_profile_v4.simpleType_roamApplicabilityType"></span>roamApplicabilityType Simple Type</span></span>

<span data-ttu-id="5531d-104">Роамаппликабилититипе описывает условия роуминга, для которых применяется перемещаемый профиль.</span><span class="sxs-lookup"><span data-stu-id="5531d-104">The roamApplicabilityType describes the roaming conditions for which a roaming profile applies.</span></span>

<span data-ttu-id="5531d-105">Это более выразительный атрибут, чем [**роамконтролтипе**](simpletype-roamcontroltype.md), и профиль должен использовать либо **Роамконтролтипе** , либо **роамаппликабилититипе**, но не оба.</span><span class="sxs-lookup"><span data-stu-id="5531d-105">This is a more expressive attribute than [**roamControlType**](simpletype-roamcontroltype.md), and a profile should use either **roamControlType** or **roamApplicabilityType**, but not both.</span></span> <span data-ttu-id="5531d-106">(Если профиль использует оба значения, применяются оба.</span><span class="sxs-lookup"><span data-stu-id="5531d-106">(If a profile uses both, then both are applied.</span></span> <span data-ttu-id="5531d-107">Результатом является пересечение двух.)</span><span class="sxs-lookup"><span data-stu-id="5531d-107">The result is the intersection of the two.)</span></span>

<span data-ttu-id="5531d-108">Этот атрибут используется для различения нескольких профилей с несвязанными условиями роуминга для указания различных атрибутов профиля для, например домашних и перемещаемых.</span><span class="sxs-lookup"><span data-stu-id="5531d-108">Use this attribute to differentiate between multiple profiles with disjoint roaming conditions, to specify different profile attributes for, for example, home versus roaming.</span></span>

<span data-ttu-id="5531d-109">Существует три возможных состояния регистрации домашних и перемещаемых компьютеров:</span><span class="sxs-lookup"><span data-stu-id="5531d-109">There are three possible home/roam registration states:</span></span>

-   <span data-ttu-id="5531d-110">Главная: зарегистрировано в домашней сети</span><span class="sxs-lookup"><span data-stu-id="5531d-110">Home: registered on the home network</span></span>
-   <span data-ttu-id="5531d-111">Партнер: Зарегистрирован в сети, тесно связанной с домашней сетью</span><span class="sxs-lookup"><span data-stu-id="5531d-111">Partner: registered on a network closely affiliated with the home network</span></span>
-   <span data-ttu-id="5531d-112">Не партнер: Зарегистрирован в сети, которая не тесно связана с домашней сетью</span><span class="sxs-lookup"><span data-stu-id="5531d-112">Non-partner: registered on a network that is not closely affiliated with the home network</span></span>

<span data-ttu-id="5531d-113">Точное значение "Partner" зависит от сети, но оно представляет более близкую связь с более выгодными тарифами, чем у другого партнера.</span><span class="sxs-lookup"><span data-stu-id="5531d-113">The precise meaning of "partner" varies based upon the network, but it represents a closer relationship with more favorable rates than a non-partner.</span></span> <span data-ttu-id="5531d-114">Это может быть, если у оператора, основанного на регионе, есть бизнес-трансляция для использования радио доступа другого оператора за пределами своей домашней области.</span><span class="sxs-lookup"><span data-stu-id="5531d-114">This could be the case if a regionally-based operator has a business arrangement to use another operator’s radio access network outside of its home area.</span></span> <span data-ttu-id="5531d-115">Он также может представлять разницу между перемещением в пределах региона (например, ЕС) и за его пределами.</span><span class="sxs-lookup"><span data-stu-id="5531d-115">It could also represent the difference between roaming within a region (e.g., EU) and outside of it.</span></span>

``` syntax
<xs:simpleType name="roamApplicabilityType">
    <xs:restriction
        base="token"
    >
        <xs:enumeration
            value="NonPartnerOnly"
         />
        <xs:enumeration
            value="PartnerOnly"
         />
        <xs:enumeration
            value="HomeOnly"
         />
        <xs:enumeration
            value="HomeAndPartner"
         />
        <xs:enumeration
            value="PartnerAndNonpartner"
         />
        <xs:enumeration
            value="AllRoaming"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="5531d-116">Значения перечисления</span><span class="sxs-lookup"><span data-stu-id="5531d-116">Enumeration values</span></span>

<span data-ttu-id="5531d-117">Простой тип **роамаппликабилититипе** определяет следующие значения.</span><span class="sxs-lookup"><span data-stu-id="5531d-117">The **roamApplicabilityType** simple type defines the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5531d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="5531d-118">Value</span></span></th>
<th><span data-ttu-id="5531d-119">Описание</span><span class="sxs-lookup"><span data-stu-id="5531d-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5531d-120">нонпартнеронли</span><span class="sxs-lookup"><span data-stu-id="5531d-120">NonPartnerOnly</span></span></td>
<td><p><span data-ttu-id="5531d-121">Этот профиль используется только при роуминге в сети, отличной от партнера</span><span class="sxs-lookup"><span data-stu-id="5531d-121">This profile is used only when roaming on a non-partner network</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5531d-122">партнеронли</span><span class="sxs-lookup"><span data-stu-id="5531d-122">PartnerOnly</span></span></td>
<td><p><span data-ttu-id="5531d-123">Этот профиль используется только при роуминге в сети партнера</span><span class="sxs-lookup"><span data-stu-id="5531d-123">This profile is used only when roaming on a partner network</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5531d-124">хомеонли</span><span class="sxs-lookup"><span data-stu-id="5531d-124">HomeOnly</span></span></td>
<td><p><span data-ttu-id="5531d-125">Этот профиль используется только в домашней сети.</span><span class="sxs-lookup"><span data-stu-id="5531d-125">This profile is used only when on the home network</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5531d-126">хомеандпартнер</span><span class="sxs-lookup"><span data-stu-id="5531d-126">HomeAndPartner</span></span></td>
<td><p><span data-ttu-id="5531d-127">Этот профиль используется только дома или в партнерской сети</span><span class="sxs-lookup"><span data-stu-id="5531d-127">This profile is used only when at home or on a partner network</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5531d-128">партнеранднонпартнер</span><span class="sxs-lookup"><span data-stu-id="5531d-128">PartnerAndNonpartner</span></span></td>
<td><p><span data-ttu-id="5531d-129">Этот профиль используется, если вы не дома (роуминг в любой сети)</span><span class="sxs-lookup"><span data-stu-id="5531d-129">This profile is used when not at home (roaming on any network)</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5531d-130">аллроаминг</span><span class="sxs-lookup"><span data-stu-id="5531d-130">AllRoaming</span></span></td>
<td><p><span data-ttu-id="5531d-131">Этот профиль используется во всех сетях</span><span class="sxs-lookup"><span data-stu-id="5531d-131">This profile is used on all networks</span></span></p></td>
</tr>
</tbody>
</table>

 

 



