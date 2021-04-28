---
description: Простой тип UInt32Type (счетчики производительности) — определяет целочисленный тип без знака.
ms.assetid: 48df484d-d663-42fa-aaec-51c463bb5350
title: Простой тип UInt32Type (счетчики производительности)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 32f8a4bbf00f569ba98dfc031f62717b1afc8734
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114582"
---
# <a name="uint32type-simple-type-performance-counters"></a><span data-ttu-id="5b656-103">Простой тип UInt32Type (счетчики производительности)</span><span class="sxs-lookup"><span data-stu-id="5b656-103">UInt32Type Simple Type (Performance Counters)</span></span>

<span data-ttu-id="5b656-104">Определяет целочисленный тип без знака.</span><span class="sxs-lookup"><span data-stu-id="5b656-104">Defines an unsigned integer type.</span></span>

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="xs:unsignedInt man:HexInt32Type"
     />
</xs:simpleType>
```

## <a name="remarks"></a><span data-ttu-id="5b656-105">Remarks</span><span class="sxs-lookup"><span data-stu-id="5b656-105">Remarks</span></span>

<span data-ttu-id="5b656-106">Значение можно указать в виде 4-байтового целого или шестнадцатеричного значения в диапазоне от 0 до 4 294 967 295.</span><span class="sxs-lookup"><span data-stu-id="5b656-106">You can specify the value as a 4-byte integer or hexadecimal value in the range from 0 through 4,294,967,295.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b656-107">Требования</span><span class="sxs-lookup"><span data-stu-id="5b656-107">Requirements</span></span>



| <span data-ttu-id="5b656-108">Требование</span><span class="sxs-lookup"><span data-stu-id="5b656-108">Requirement</span></span> | <span data-ttu-id="5b656-109">Значение</span><span class="sxs-lookup"><span data-stu-id="5b656-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5b656-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5b656-110">Minimum supported client</span></span><br/> | <span data-ttu-id="5b656-111">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5b656-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5b656-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5b656-112">Minimum supported server</span></span><br/> | <span data-ttu-id="5b656-113">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5b656-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




