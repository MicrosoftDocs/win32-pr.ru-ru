---
title: Простой тип Кнамелист
description: Определяет список полных имен.
ms.assetid: 727d87a0-82f5-44fa-a841-4c2445f78063
keywords:
- Журнал событий простого типа Кнамелист
topic_type:
- apiref
api_name:
- QNameList
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ffcb078c2fcddd9b1549ff095820ce19eb7d5a13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103800946"
---
# <a name="qnamelist-simple-type"></a><span data-ttu-id="d564d-104">Простой тип Кнамелист</span><span class="sxs-lookup"><span data-stu-id="d564d-104">QNameList Simple Type</span></span>

<span data-ttu-id="d564d-105">Определяет список полных имен.</span><span class="sxs-lookup"><span data-stu-id="d564d-105">Defines a list of qualified names.</span></span>

``` syntax
<xs:simpleType name="QNameList">
    <xs:list>
        <xs:itemType name="QName" />
    </xs:list>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="d564d-106">Требования</span><span class="sxs-lookup"><span data-stu-id="d564d-106">Requirements</span></span>



| <span data-ttu-id="d564d-107">Требование</span><span class="sxs-lookup"><span data-stu-id="d564d-107">Requirement</span></span> | <span data-ttu-id="d564d-108">Значение</span><span class="sxs-lookup"><span data-stu-id="d564d-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d564d-109">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d564d-109">Minimum supported client</span></span><br/> | <span data-ttu-id="d564d-110">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d564d-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d564d-111">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d564d-111">Minimum supported server</span></span><br/> | <span data-ttu-id="d564d-112">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d564d-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





