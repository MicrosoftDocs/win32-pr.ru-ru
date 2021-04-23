---
title: Простой тип UInt64Type (схема Евентманифест)
description: Определяет тип long без знака.
ms.assetid: 6f69dbde-8292-4f8e-bf49-3ef41ea7315e
keywords:
- Журнал событий простого типа UInt64Type
topic_type:
- apiref
api_name:
- UInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b375a8e452760f9e59bae9cae8449889483d9b4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071578"
---
# <a name="uint64type-simple-type"></a><span data-ttu-id="f30ef-104">Простой тип UInt64Type</span><span class="sxs-lookup"><span data-stu-id="f30ef-104">UInt64Type Simple Type</span></span>

<span data-ttu-id="f30ef-105">Определяет тип long без знака.</span><span class="sxs-lookup"><span data-stu-id="f30ef-105">Defines an unsigned long type.</span></span> <span data-ttu-id="f30ef-106">Значение может быть задано как 8-байтовое целое или шестнадцатеричное значение в диапазоне от 0 до 18446744073709551615.</span><span class="sxs-lookup"><span data-stu-id="f30ef-106">The value can be specified as an 8-byte integer or hexadecimal value in the range from 0 through 18,446,744,073,709,551,615.</span></span>

``` syntax
<xs:simpleType name="UInt64Type">
    <xs:union
        memberValues="unsignedLong HexInt64Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="f30ef-107">Требования</span><span class="sxs-lookup"><span data-stu-id="f30ef-107">Requirements</span></span>



| <span data-ttu-id="f30ef-108">Требование</span><span class="sxs-lookup"><span data-stu-id="f30ef-108">Requirement</span></span> | <span data-ttu-id="f30ef-109">Значение</span><span class="sxs-lookup"><span data-stu-id="f30ef-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f30ef-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f30ef-110">Minimum supported client</span></span><br/> | <span data-ttu-id="f30ef-111">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f30ef-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f30ef-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f30ef-112">Minimum supported server</span></span><br/> | <span data-ttu-id="f30ef-113">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f30ef-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





