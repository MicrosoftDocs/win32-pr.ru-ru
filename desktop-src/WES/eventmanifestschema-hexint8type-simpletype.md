---
title: Простой тип UInt8Type
description: Определяет тип Byte без знака.
ms.assetid: bda12d06-683f-4183-a84b-2bc3159c4eff
keywords:
- Журнал событий простого типа UInt8Type
topic_type:
- apiref
api_name:
- UInt8Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3236d7416cbb199037813a8ae870d4f87718081
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691827"
---
# <a name="uint8type-simple-type"></a><span data-ttu-id="8606c-104">Простой тип UInt8Type</span><span class="sxs-lookup"><span data-stu-id="8606c-104">UInt8Type Simple Type</span></span>

<span data-ttu-id="8606c-105">Определяет тип Byte без знака.</span><span class="sxs-lookup"><span data-stu-id="8606c-105">Defines an unsigned byte type.</span></span> <span data-ttu-id="8606c-106">Значение может быть указано в виде 1-байтового целого или шестнадцатеричного значения в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="8606c-106">The value can be specified as a 1-byte integer or hexadecimal value in the range from 0 through 255.</span></span>

``` syntax
<xs:simpleType name="UInt8Type">
    <xs:union
        memberValues="unsignedByte HexInt8Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="8606c-107">Требования</span><span class="sxs-lookup"><span data-stu-id="8606c-107">Requirements</span></span>



| <span data-ttu-id="8606c-108">Требование</span><span class="sxs-lookup"><span data-stu-id="8606c-108">Requirement</span></span> | <span data-ttu-id="8606c-109">Значение</span><span class="sxs-lookup"><span data-stu-id="8606c-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8606c-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8606c-110">Minimum supported client</span></span><br/> | <span data-ttu-id="8606c-111">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8606c-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8606c-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8606c-112">Minimum supported server</span></span><br/> | <span data-ttu-id="8606c-113">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8606c-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





