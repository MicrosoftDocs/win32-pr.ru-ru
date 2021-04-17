---
description: Представляет сведения о целевых объектах вызова для защиты потока управления (CFG).
ms.assetid: 8DEF907F-3F23-4122-95CE-F413FC7FD96B
title: Структура CFG_CALL_TARGET_INFO (Нтммапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFG_CALL_TARGET_INFO
api_type:
- HeaderDef
api_location:
- ntmmapi.h
ms.openlocfilehash: 66177f6b478264a10c1ce0e50297d943a16407c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673685"
---
# <a name="cfg_call_target_info-structure"></a><span data-ttu-id="a2c61-103">\_ \_ \_ Структура сведений о цели вызова cfg</span><span class="sxs-lookup"><span data-stu-id="a2c61-103">CFG\_CALL\_TARGET\_INFO structure</span></span>

<span data-ttu-id="a2c61-104">Представляет сведения о целевых объектах вызова для защиты потока управления (CFG).</span><span class="sxs-lookup"><span data-stu-id="a2c61-104">Represents information about call targets for Control Flow Guard (CFG).</span></span>

## <a name="syntax"></a><span data-ttu-id="a2c61-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a2c61-105">Syntax</span></span>


```C++
typedef struct _CFG_CALL_TARGET_INFO {
  ULONG_PTR Offset;
  ULONG_PTR Flags;
} CFG_CALL_TARGET_INFO, *PCFG_CALL_TARGET_INFO;
```



## <a name="members"></a><span data-ttu-id="a2c61-106">Члены</span><span class="sxs-lookup"><span data-stu-id="a2c61-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a2c61-107">**Offset**</span><span class="sxs-lookup"><span data-stu-id="a2c61-107">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="a2c61-108">Смещение относительно указанного (начального) виртуального адреса.</span><span class="sxs-lookup"><span data-stu-id="a2c61-108">Offset relative to a provided (start) virtual address.</span></span> <span data-ttu-id="a2c61-109">Это смещение должно быть равно 16 байтам.</span><span class="sxs-lookup"><span data-stu-id="a2c61-109">This offset should be 16 byte aligned.</span></span>

</dd> <dt>

<span data-ttu-id="a2c61-110">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="a2c61-110">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="a2c61-111">Флаги, описывающие операцию, которая должна быть выполнена с адресом.</span><span class="sxs-lookup"><span data-stu-id="a2c61-111">Flags describing the operation to be performed on the address.</span></span> <span data-ttu-id="a2c61-112">Если задана **\_ \_ \_ допустимая цель вызова cfg** , адрес будет ПОМЕЧЕН как допустимый для cfg.</span><span class="sxs-lookup"><span data-stu-id="a2c61-112">If **CFG\_CALL\_TARGET\_VALID** is set, then the address will be marked valid for CFG.</span></span> <span data-ttu-id="a2c61-113">В противном случае он будет помечен как недопустимый целевой объект вызова.</span><span class="sxs-lookup"><span data-stu-id="a2c61-113">Otherwise, it will be marked an invalid call target.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a2c61-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a2c61-114">Requirements</span></span>



| <span data-ttu-id="a2c61-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a2c61-115">Requirement</span></span> | <span data-ttu-id="a2c61-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a2c61-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a2c61-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a2c61-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a2c61-118">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="a2c61-118">Windows 10 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a2c61-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a2c61-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a2c61-120">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="a2c61-120">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a2c61-121">Header</span><span class="sxs-lookup"><span data-stu-id="a2c61-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2c61-122"><dt>Нтммапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2c61-122"><dt>Ntmmapi.h</dt></span></span> </dl> |



 

 




