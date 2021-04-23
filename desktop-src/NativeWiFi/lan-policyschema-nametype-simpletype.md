---
description: Определяет строковый тип для имени или описания профиля политики проводной локальной сети.
ms.assetid: 89de1e7a-618d-4501-a134-c7a37f9c552d
title: простой тип Наметипе (LAN_policy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 702ee6340fa3d03217c884a48625d3a38be4ad9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998905"
---
# <a name="nametype-simple-type-lan_policy"></a><span data-ttu-id="77dc4-103">простой тип Наметипе (LAN_policy)</span><span class="sxs-lookup"><span data-stu-id="77dc4-103">nameType simple type (LAN_policy)</span></span>

<span data-ttu-id="77dc4-104">Простой тип Наметипе определяет строковый тип для имени или описания профиля политики проводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="77dc4-104">The nameType simple type defines a string type for either the name or the description of a wired LAN policy profile.</span></span> <span data-ttu-id="77dc4-105">Имена и описания — это строки длиной не менее одного символа и не более 255 символов.</span><span class="sxs-lookup"><span data-stu-id="77dc4-105">Names and descriptions are strings that are at least one character long and at most 255 characters long.</span></span>

``` syntax
<xs:simpleType name="nameType">
    <xs:restriction
        base="string"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="255"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="77dc4-106">Требования</span><span class="sxs-lookup"><span data-stu-id="77dc4-106">Requirements</span></span>



| <span data-ttu-id="77dc4-107">Требование</span><span class="sxs-lookup"><span data-stu-id="77dc4-107">Requirement</span></span> | <span data-ttu-id="77dc4-108">Значение</span><span class="sxs-lookup"><span data-stu-id="77dc4-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="77dc4-109">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="77dc4-109">Minimum supported client</span></span><br/> | <span data-ttu-id="77dc4-110">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="77dc4-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="77dc4-111">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="77dc4-111">Minimum supported server</span></span><br/> | <span data-ttu-id="77dc4-112">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="77dc4-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




