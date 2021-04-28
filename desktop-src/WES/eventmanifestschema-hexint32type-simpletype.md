---
title: Простой тип UInt32Type (журнал событий Windows)
description: Простой тип UInt32Type (журнал событий Windows) — определяет целочисленный тип без знака.
ms.assetid: 11e99c26-3be7-4fac-b3e1-97cb0428a886
keywords:
- Журнал событий простого типа UInt32Type
topic_type:
- apiref
api_name:
- UInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 631bb3e8424db8a5d781aaa43df6096730aaa4d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090572"
---
# <a name="uint32type-simple-type-windows-event-log"></a><span data-ttu-id="05eed-104">Простой тип UInt32Type (журнал событий Windows)</span><span class="sxs-lookup"><span data-stu-id="05eed-104">UInt32Type Simple Type (Windows Event Log)</span></span>

<span data-ttu-id="05eed-105">Определяет целочисленный тип без знака.</span><span class="sxs-lookup"><span data-stu-id="05eed-105">Defines an unsigned integer type.</span></span> <span data-ttu-id="05eed-106">Значение может быть указано в виде 4-байтового целого или шестнадцатеричного значения в диапазоне от 0 до 4 294 967 295.</span><span class="sxs-lookup"><span data-stu-id="05eed-106">The value can be specified as a 4-byte integer or hexadecimal value in the range from 0 through 4,294,967,295.</span></span>

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="unsignedInt HexInt32Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="05eed-107">Требования</span><span class="sxs-lookup"><span data-stu-id="05eed-107">Requirements</span></span>



| <span data-ttu-id="05eed-108">Требование</span><span class="sxs-lookup"><span data-stu-id="05eed-108">Requirement</span></span> | <span data-ttu-id="05eed-109">Значение</span><span class="sxs-lookup"><span data-stu-id="05eed-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="05eed-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="05eed-110">Minimum supported client</span></span><br/> | <span data-ttu-id="05eed-111">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="05eed-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="05eed-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="05eed-112">Minimum supported server</span></span><br/> | <span data-ttu-id="05eed-113">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="05eed-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





