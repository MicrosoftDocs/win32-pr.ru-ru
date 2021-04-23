---
description: Определяет строковый тип для имени или описания профиля политики беспроводной локальной сети.
ms.assetid: a01e8789-3401-4e58-b733-2ec95fc895b6
title: Простой тип Наметипе (LAN_policy)
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
ms.openlocfilehash: 8a2c0bdf281e27ba7a85271fe7777076ada9ff2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674297"
---
# <a name="nametype-simple-type-lan_policy"></a><span data-ttu-id="9c7b0-103">Простой тип Наметипе (LAN_policy)</span><span class="sxs-lookup"><span data-stu-id="9c7b0-103">nameType Simple Type (LAN_policy)</span></span>

<span data-ttu-id="9c7b0-104">Простой тип Наметипе определяет строковый тип для имени или описания профиля политики беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="9c7b0-104">The nameType simple type defines a string type for either the name or the description of a wireless LAN policy profile.</span></span> <span data-ttu-id="9c7b0-105">Имена и описания — это строки длиной не менее одного символа и не более 255 символов.</span><span class="sxs-lookup"><span data-stu-id="9c7b0-105">Names and descriptions are strings that are at least one character long and at most 255 characters long.</span></span>

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

## <a name="requirements"></a><span data-ttu-id="9c7b0-106">Требования</span><span class="sxs-lookup"><span data-stu-id="9c7b0-106">Requirements</span></span>



| <span data-ttu-id="9c7b0-107">Требование</span><span class="sxs-lookup"><span data-stu-id="9c7b0-107">Requirement</span></span> | <span data-ttu-id="9c7b0-108">Значение</span><span class="sxs-lookup"><span data-stu-id="9c7b0-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9c7b0-109">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c7b0-109">Minimum supported client</span></span><br/> | <span data-ttu-id="9c7b0-110">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9c7b0-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9c7b0-111">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c7b0-111">Minimum supported server</span></span><br/> | <span data-ttu-id="9c7b0-112">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9c7b0-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




