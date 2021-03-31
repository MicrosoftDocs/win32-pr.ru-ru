---
title: Простой тип UInt16Type
description: Определяет короткий тип без знака.
ms.assetid: 2200bb14-8f38-43fd-aed3-2a6b3ac33ed5
keywords:
- Журнал событий простого типа UInt16Type
topic_type:
- apiref
api_name:
- UInt16Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e687f42a43a12266267a0531ce078e8c6b5d1031
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803574"
---
# <a name="uint16type-simple-type"></a><span data-ttu-id="6ac2e-104">Простой тип UInt16Type</span><span class="sxs-lookup"><span data-stu-id="6ac2e-104">UInt16Type Simple Type</span></span>

<span data-ttu-id="6ac2e-105">Определяет короткий тип без знака.</span><span class="sxs-lookup"><span data-stu-id="6ac2e-105">Defines an unsigned short type.</span></span> <span data-ttu-id="6ac2e-106">Значение может быть задано в виде 2-байтового целого или шестнадцатеричного значения в диапазоне от 0 до 65 535.</span><span class="sxs-lookup"><span data-stu-id="6ac2e-106">The value can be specified as a 2-byte integer or hexadecimal value in the range from 0 through 65,535.</span></span>

``` syntax
<xs:simpleType name="UInt16Type">
    <xs:union
        memberValues="unsignedShort HexInt16Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="6ac2e-107">Требования</span><span class="sxs-lookup"><span data-stu-id="6ac2e-107">Requirements</span></span>



| <span data-ttu-id="6ac2e-108">Требование</span><span class="sxs-lookup"><span data-stu-id="6ac2e-108">Requirement</span></span> | <span data-ttu-id="6ac2e-109">Значение</span><span class="sxs-lookup"><span data-stu-id="6ac2e-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6ac2e-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6ac2e-110">Minimum supported client</span></span><br/> | <span data-ttu-id="6ac2e-111">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6ac2e-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6ac2e-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6ac2e-112">Minimum supported server</span></span><br/> | <span data-ttu-id="6ac2e-113">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6ac2e-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





