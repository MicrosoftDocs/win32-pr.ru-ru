---
title: Простой тип Каунттипе
description: Определяет тип счетчика, который используется для указания количества элементов в массиве.
ms.assetid: 84f819d7-5c42-475b-9144-aaa5e2d215c8
keywords:
- Журнал событий простого типа Каунттипе
topic_type:
- apiref
api_name:
- CountType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f91b19df4182f5cff305de0429a308d0c5db234
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804030"
---
# <a name="counttype-simple-type"></a><span data-ttu-id="1ee40-104">Простой тип Каунттипе</span><span class="sxs-lookup"><span data-stu-id="1ee40-104">CountType Simple Type</span></span>

<span data-ttu-id="1ee40-105">Определяет тип счетчика, который используется для указания количества элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="1ee40-105">Defines a count type that is used to specify the number of elements in an array.</span></span> <span data-ttu-id="1ee40-106">Значение может быть указано в виде значения xs: Унсигнедшорт или в виде строки, которая ссылается на имя узла элемента данных, содержащего короткое значение унсижед.</span><span class="sxs-lookup"><span data-stu-id="1ee40-106">The value can be specified as an xs:unsignedShort value or as a string that references the name of data item node that contains the unsiged short value.</span></span>

``` syntax
<xs:simpleType name="CountType">
    <xs:union
        memberValues="unsignedShort string"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="1ee40-107">Требования</span><span class="sxs-lookup"><span data-stu-id="1ee40-107">Requirements</span></span>



| <span data-ttu-id="1ee40-108">Требование</span><span class="sxs-lookup"><span data-stu-id="1ee40-108">Requirement</span></span> | <span data-ttu-id="1ee40-109">Значение</span><span class="sxs-lookup"><span data-stu-id="1ee40-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1ee40-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1ee40-110">Minimum supported client</span></span><br/> | <span data-ttu-id="1ee40-111">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1ee40-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1ee40-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1ee40-112">Minimum supported server</span></span><br/> | <span data-ttu-id="1ee40-113">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1ee40-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





