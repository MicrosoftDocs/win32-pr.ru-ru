---
description: '\_Перечисление типа кэйсвк определяет, применяется ли ключ к компьютеру или службе.'
ms.assetid: 573a412a-1e9d-47ac-bd09-2319d4b9712b
title: Перечисление KEYSVC_TYPE (Ркэйсвкк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_TYPE
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 71d6724f7bae78a3c1ac4da83289c151b7ec1a73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999664"
---
# <a name="keysvc_type-enumeration"></a><span data-ttu-id="2d3da-103">\_Перечисление типов кэйсвк</span><span class="sxs-lookup"><span data-stu-id="2d3da-103">KEYSVC\_TYPE enumeration</span></span>

<span data-ttu-id="2d3da-104">Перечисление **\_ типа кэйсвк** определяет, применяется ли ключ к компьютеру или службе.</span><span class="sxs-lookup"><span data-stu-id="2d3da-104">The **KEYSVC\_TYPE** enumeration defines whether a key applies to a computer or a service.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d3da-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d3da-105">Syntax</span></span>


```C++
typedef enum _KEYSVC_TYPE { 
  KeySvcMachine,
  KeySvcService
} KEYSVC_TYPE;
```



## <a name="constants"></a><span data-ttu-id="2d3da-106">Константы</span><span class="sxs-lookup"><span data-stu-id="2d3da-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2d3da-107"><span id="KeySvcMachine"></span><span id="keysvcmachine"></span><span id="KEYSVCMACHINE"></span>**кэйсвкмачине**</span><span class="sxs-lookup"><span data-stu-id="2d3da-107"><span id="KeySvcMachine"></span><span id="keysvcmachine"></span><span id="KEYSVCMACHINE"></span>**KeySvcMachine**</span></span>
</dt> <dd>

<span data-ttu-id="2d3da-108">Ключ для компьютера.</span><span class="sxs-lookup"><span data-stu-id="2d3da-108">The key is for a computer.</span></span>

</dd> <dt>

<span data-ttu-id="2d3da-109"><span id="KeySvcService"></span><span id="keysvcservice"></span><span id="KEYSVCSERVICE"></span>**кэйсвксервице**</span><span class="sxs-lookup"><span data-stu-id="2d3da-109"><span id="KeySvcService"></span><span id="keysvcservice"></span><span id="KEYSVCSERVICE"></span>**KeySvcService**</span></span>
</dt> <dd>

<span data-ttu-id="2d3da-110">Ключ для службы.</span><span class="sxs-lookup"><span data-stu-id="2d3da-110">The key is for a service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2d3da-111">Требования</span><span class="sxs-lookup"><span data-stu-id="2d3da-111">Requirements</span></span>



| <span data-ttu-id="2d3da-112">Требование</span><span class="sxs-lookup"><span data-stu-id="2d3da-112">Requirement</span></span> | <span data-ttu-id="2d3da-113">Значение</span><span class="sxs-lookup"><span data-stu-id="2d3da-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2d3da-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2d3da-114">Minimum supported client</span></span><br/> | <span data-ttu-id="2d3da-115">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2d3da-115">None supported</span></span><br/>                                                             |
| <span data-ttu-id="2d3da-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2d3da-116">Minimum supported server</span></span><br/> | <span data-ttu-id="2d3da-117">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2d3da-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2d3da-118">Header</span><span class="sxs-lookup"><span data-stu-id="2d3da-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d3da-119"><dt>Ркэйсвкк. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d3da-119"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d3da-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d3da-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d3da-121">**ркэйопенкэйсервице**</span><span class="sxs-lookup"><span data-stu-id="2d3da-121">**RKeyOpenKeyService**</span></span>](rkeyopenkeyservice.md)
</dt> </dl>

 

 




