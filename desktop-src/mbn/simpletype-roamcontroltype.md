---
description: Описывает, как профиль управляет перемещением.
MS-HAID: WWAN\_profile\_v4.simpleType\_roamControlType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Простой тип Роамконтролтипе
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911e379773e7d8eabfb7a1524b1a21ba16718a53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701619"
---
# <a name="span-idwwan_profile_v4simpletype_roamcontroltypespanroamcontroltype-simple-type"></a><span data-ttu-id="1e84e-103"><span id="WWAN_profile_v4.simpleType_roamControlType"></span>Простой тип Роамконтролтипе</span><span class="sxs-lookup"><span data-stu-id="1e84e-103"><span id="WWAN_profile_v4.simpleType_roamControlType"></span>roamControlType Simple Type</span></span>

<span data-ttu-id="1e84e-104">Описывает, как профиль управляет перемещением.</span><span class="sxs-lookup"><span data-stu-id="1e84e-104">Describes how the profile controls roaming.</span></span>

<span data-ttu-id="1e84e-105">Существует два возможных состояния регистрации роуминга:</span><span class="sxs-lookup"><span data-stu-id="1e84e-105">There are two possible roam registration states:</span></span>

-   <span data-ttu-id="1e84e-106">Партнер: Зарегистрирован в сети, тесно связанной с домашней сетью</span><span class="sxs-lookup"><span data-stu-id="1e84e-106">Partner: registered on a network closely affiliated with the home network</span></span>
-   <span data-ttu-id="1e84e-107">Не партнер: Зарегистрирован в сети, которая не тесно связана с домашней сетью</span><span class="sxs-lookup"><span data-stu-id="1e84e-107">Non-partner: registered on a network that is not closely affiliated with the home network</span></span>

<span data-ttu-id="1e84e-108">Точное значение "Partner" зависит от сети, но оно представляет более близкую связь с более выгодными тарифами, чем у другого партнера.</span><span class="sxs-lookup"><span data-stu-id="1e84e-108">The precise meaning of "partner" varies based upon the network, but it represents a closer relationship with more favorable rates than a non-partner.</span></span> <span data-ttu-id="1e84e-109">Это может быть, если у оператора, основанного на регионе, есть бизнес-трансляция для использования радио доступа другого оператора за пределами своей домашней области.</span><span class="sxs-lookup"><span data-stu-id="1e84e-109">This could be the case if a regionally-based operator has a business arrangement to use another operator’s radio access network outside of its home area.</span></span> <span data-ttu-id="1e84e-110">Он также может представлять разницу между перемещением в пределах региона (например, ЕС) и за его пределами.</span><span class="sxs-lookup"><span data-stu-id="1e84e-110">It could also represent the difference between roaming within a region (e.g., EU) and outside of it.</span></span>

<span data-ttu-id="1e84e-111">Обратите внимание, что [**роамаппликабилититипе**](simpletype-roamapplicabilitytype.md) является более выразительным атрибутом, чем **роамконтролтипе**, и профиль должен использовать либо **роамконтролтипе** , либо **роамаппликабилититипе**, но не оба.</span><span class="sxs-lookup"><span data-stu-id="1e84e-111">Note that [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) is a more expressive attribute than **roamControlType**, and a profile should use either **roamControlType** or **roamApplicabilityType**, but not both.</span></span> <span data-ttu-id="1e84e-112">(Если профиль использует оба значения, применяются оба.</span><span class="sxs-lookup"><span data-stu-id="1e84e-112">(If a profile uses both, then both are applied.</span></span> <span data-ttu-id="1e84e-113">Результатом является пересечение двух.)</span><span class="sxs-lookup"><span data-stu-id="1e84e-113">The result is the intersection of the two.)</span></span>

``` syntax
<xs:simpleType name="roamControlType">
    <xs:restriction>
        <xs:enumeration
            value="AllRoamAllowed"
         />
        <xs:enumeration
            value="PartnerRoamAllowed"
         />
        <xs:enumeration
            value="NoRoamAllowed"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="1e84e-114">Значения перечисления</span><span class="sxs-lookup"><span data-stu-id="1e84e-114">Enumeration values</span></span>

<span data-ttu-id="1e84e-115">Простой тип **роамконтролтипе** определяет следующие значения.</span><span class="sxs-lookup"><span data-stu-id="1e84e-115">The **roamControlType** simple type defines the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1e84e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="1e84e-116">Value</span></span></th>
<th><span data-ttu-id="1e84e-117">Описание</span><span class="sxs-lookup"><span data-stu-id="1e84e-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e84e-118">аллроамалловед</span><span class="sxs-lookup"><span data-stu-id="1e84e-118">AllRoamAllowed</span></span></td>
<td><p><span data-ttu-id="1e84e-119">Роуминг разрешен в сетях партнера и других партнеров.</span><span class="sxs-lookup"><span data-stu-id="1e84e-119">Roaming is allowed on Partner and Non-Partner networks.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e84e-120">партнерроамалловед</span><span class="sxs-lookup"><span data-stu-id="1e84e-120">PartnerRoamAllowed</span></span></td>
<td><p><span data-ttu-id="1e84e-121">Роуминг разрешен только в партнерских сетях.</span><span class="sxs-lookup"><span data-stu-id="1e84e-121">Roaming is allowed only on Partner networks.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e84e-122">нороамалловед</span><span class="sxs-lookup"><span data-stu-id="1e84e-122">NoRoamAllowed</span></span></td>
<td><p><span data-ttu-id="1e84e-123">Роуминг не разрешен.</span><span class="sxs-lookup"><span data-stu-id="1e84e-123">No roaming is allowed.</span></span></p></td>
</tr>
</tbody>
</table>

 

 



