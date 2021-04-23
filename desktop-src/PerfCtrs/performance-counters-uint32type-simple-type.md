---
description: Определяет целочисленный тип без знака.
ms.assetid: 48df484d-d663-42fa-aaec-51c463bb5350
title: Простой тип UInt32Type (счетчики производительности)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4c32901167bcf181e5400ddb1d3b91ed7383965c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663173"
---
# <a name="uint32type-simple-type-performance-counters"></a><span data-ttu-id="52dd7-103">Простой тип UInt32Type (счетчики производительности)</span><span class="sxs-lookup"><span data-stu-id="52dd7-103">UInt32Type Simple Type (Performance Counters)</span></span>

<span data-ttu-id="52dd7-104">Определяет целочисленный тип без знака.</span><span class="sxs-lookup"><span data-stu-id="52dd7-104">Defines an unsigned integer type.</span></span>

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="xs:unsignedInt man:HexInt32Type"
     />
</xs:simpleType>
```

## <a name="remarks"></a><span data-ttu-id="52dd7-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="52dd7-105">Remarks</span></span>

<span data-ttu-id="52dd7-106">Значение можно указать в виде 4-байтового целого или шестнадцатеричного значения в диапазоне от 0 до 4 294 967 295.</span><span class="sxs-lookup"><span data-stu-id="52dd7-106">You can specify the value as a 4-byte integer or hexadecimal value in the range from 0 through 4,294,967,295.</span></span>

## <a name="requirements"></a><span data-ttu-id="52dd7-107">Требования</span><span class="sxs-lookup"><span data-stu-id="52dd7-107">Requirements</span></span>



| <span data-ttu-id="52dd7-108">Требование</span><span class="sxs-lookup"><span data-stu-id="52dd7-108">Requirement</span></span> | <span data-ttu-id="52dd7-109">Значение</span><span class="sxs-lookup"><span data-stu-id="52dd7-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="52dd7-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="52dd7-110">Minimum supported client</span></span><br/> | <span data-ttu-id="52dd7-111">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="52dd7-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="52dd7-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="52dd7-112">Minimum supported server</span></span><br/> | <span data-ttu-id="52dd7-113">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="52dd7-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




