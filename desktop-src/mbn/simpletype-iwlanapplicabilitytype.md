---
description: Перечисление, описывающее тип сетевого подключения, к которому применим профиль.
MS-HAID: WWAN\_profile\_v4.simpleType\_iwlanApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Простой тип Ивланаппликабилититипе
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80013fa21574221de24a7fc8309e4459a80ad670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542178"
---
# <a name="span-idwwan_profile_v4simpletype_iwlanapplicabilitytypespaniwlanapplicabilitytype-simple-type"></a><span data-ttu-id="0f9a6-103"><span id="WWAN_profile_v4.simpleType_iwlanApplicabilityType"></span>Простой тип Ивланаппликабилититипе</span><span class="sxs-lookup"><span data-stu-id="0f9a6-103"><span id="WWAN_profile_v4.simpleType_iwlanApplicabilityType"></span>iwlanApplicabilityType Simple Type</span></span>

<span data-ttu-id="0f9a6-104">Перечисление, описывающее тип сетевого подключения, к которому применим профиль.</span><span class="sxs-lookup"><span data-stu-id="0f9a6-104">Enumeration that describes the kind of network connection where a profile is applicable.</span></span>

``` syntax
<xs:simpleType name="iwlanApplicabilityType">
    <xs:restriction
        base="token"
    >
        <xs:enumeration
            value="CellularOnly"
         />
        <xs:enumeration
            value="CellularAndIwlan"
         />
        <xs:enumeration
            value="IwlanOnly"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="0f9a6-105">Значения перечисления</span><span class="sxs-lookup"><span data-stu-id="0f9a6-105">Enumeration values</span></span>

<span data-ttu-id="0f9a6-106">Простой тип **ивланаппликабилититипе** определяет следующие значения.</span><span class="sxs-lookup"><span data-stu-id="0f9a6-106">The **iwlanApplicabilityType** simple type defines the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0f9a6-107">Значение</span><span class="sxs-lookup"><span data-stu-id="0f9a6-107">Value</span></span></th>
<th><span data-ttu-id="0f9a6-108">Описание</span><span class="sxs-lookup"><span data-stu-id="0f9a6-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0f9a6-109">целлуларонли</span><span class="sxs-lookup"><span data-stu-id="0f9a6-109">CellularOnly</span></span></td>
<td><p><span data-ttu-id="0f9a6-110">Профиль действителен только для подключений по сотовой сети.</span><span class="sxs-lookup"><span data-stu-id="0f9a6-110">Profile is valid for cellular network connections only.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f9a6-111">целлуларандивлан</span><span class="sxs-lookup"><span data-stu-id="0f9a6-111">CellularAndIwlan</span></span></td>
<td><p><span data-ttu-id="0f9a6-112">Профиль действителен для сотовой сети или Wi-Fi разгрузки подключений.</span><span class="sxs-lookup"><span data-stu-id="0f9a6-112">Profile is valid for cellular or Wi-Fi offloaded connections.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0f9a6-113">ивланонли</span><span class="sxs-lookup"><span data-stu-id="0f9a6-113">IwlanOnly</span></span></td>
<td><p><span data-ttu-id="0f9a6-114">Профиль действителен только для Wi-Fi разгрузок подключений.</span><span class="sxs-lookup"><span data-stu-id="0f9a6-114">Profile is valid for Wi-Fi offloaded connections only.</span></span></p></td>
</tr>
</tbody>
</table>

 

 



