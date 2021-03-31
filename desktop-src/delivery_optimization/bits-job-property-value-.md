---
title: Структура BITS_JOB_PROPERTY_VALUE (Deliveryoptimization. h)
description: BITS_JOB_PROPERTY_VALUE Union предоставляет значение свойства задания DO на основе значения перечисления BITS_JOB_PROPERTY_ID.
ms.assetid: C24D9EA1-2E72-4403-939A-7B01D7133FE7
keywords:
- Структура BITS_JOB_PROPERTY_VALUE
- Структура BITS_JOB_PROPERTY_VALUE
topic_type:
- apiref
api_name:
- BITS_JOB_PROPERTY_VALUE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c48c1fe550db51b6b838379d44df21c95fa95e41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135887"
---
# <a name="bits_job_property_value-structure"></a><span data-ttu-id="7c9aa-105">Структура BITS_JOB_PROPERTY_VALUE</span><span class="sxs-lookup"><span data-stu-id="7c9aa-105">BITS_JOB_PROPERTY_VALUE structure</span></span>

<span data-ttu-id="7c9aa-106">**BITS_JOB_PROPERTY_VALUE** Union предоставляет значение свойства задания Do на основе значения перечисления [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) .</span><span class="sxs-lookup"><span data-stu-id="7c9aa-106">The **BITS_JOB_PROPERTY_VALUE** union provides the property value of the DO job based on the value of the [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c9aa-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c9aa-107">Syntax</span></span>


```C++
typedef struct {
  DWORD          Dword;
  GUID           ClsID;
  BOOL           Enable;
  UINT64         Uint64;
  BG_AUTH_TARGET Target;
} BITS_JOB_PROPERTY_VALUE;
```



## <a name="members"></a><span data-ttu-id="7c9aa-108">Члены</span><span class="sxs-lookup"><span data-stu-id="7c9aa-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7c9aa-109">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="7c9aa-109">**Dword**</span></span>
</dt> <dd>

<span data-ttu-id="7c9aa-110">Это значение возвращается при использовании идентификатора свойства Enum **BITS_JOB_PROPERTY_ID_COST_FLAGS** и применяется в качестве [политики перемещения](https://www.bing.com/search?q=transfer+policy) в задании Do.</span><span class="sxs-lookup"><span data-stu-id="7c9aa-110">This value is returned when using the enum property ID **BITS_JOB_PROPERTY_ID_COST_FLAGS** and is applied as the [transfer policy](https://www.bing.com/search?q=transfer+policy) on the DO job.</span></span>

</dd> <dt>

<span data-ttu-id="7c9aa-111">**Этому**</span><span class="sxs-lookup"><span data-stu-id="7c9aa-111">**ClsID**</span></span>
</dt> <dd>

<span data-ttu-id="7c9aa-112">Это значение возвращается при использовании идентификатора свойства перечисления **BITS_JOB_PROPERTY_NOTIFICATION_CLSID** и представляет идентификатор CLSID объекта обратного вызова, регистрируемого в задании Do.</span><span class="sxs-lookup"><span data-stu-id="7c9aa-112">This value is returned when using the enum property ID **BITS_JOB_PROPERTY_NOTIFICATION_CLSID** and represents the CLSID of the callback object to register with the DO job.</span></span>

</dd> <dt>

<span data-ttu-id="7c9aa-113">**Разрешить**</span><span class="sxs-lookup"><span data-stu-id="7c9aa-113">**Enable**</span></span>
</dt> <dd>

<span data-ttu-id="7c9aa-114">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7c9aa-114">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="7c9aa-115">**UInt64**</span><span class="sxs-lookup"><span data-stu-id="7c9aa-115">**Uint64**</span></span>
</dt> <dd>

<span data-ttu-id="7c9aa-116">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7c9aa-116">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="7c9aa-117">**Целевой объект**</span><span class="sxs-lookup"><span data-stu-id="7c9aa-117">**Target**</span></span>
</dt> <dd>

<span data-ttu-id="7c9aa-118">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7c9aa-118">Not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7c9aa-119">Требования</span><span class="sxs-lookup"><span data-stu-id="7c9aa-119">Requirements</span></span>



| <span data-ttu-id="7c9aa-120">Требование</span><span class="sxs-lookup"><span data-stu-id="7c9aa-120">Requirement</span></span> | <span data-ttu-id="7c9aa-121">Значение</span><span class="sxs-lookup"><span data-stu-id="7c9aa-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c9aa-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7c9aa-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7c9aa-123">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="7c9aa-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7c9aa-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7c9aa-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7c9aa-125">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="7c9aa-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7c9aa-126">Header</span><span class="sxs-lookup"><span data-stu-id="7c9aa-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c9aa-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c9aa-127"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c9aa-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c9aa-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c9aa-129">**BITS_JOB_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="7c9aa-129">**BITS_JOB_PROPERTY_ID**</span></span>](bits-job-property-id.md)
</dt> <dt>

[<span data-ttu-id="7c9aa-130">**BITS_JOB_TRANSFER_POLICY**</span><span class="sxs-lookup"><span data-stu-id="7c9aa-130">**BITS_JOB_TRANSFER_POLICY**</span></span>](bits-job-transfer-policy-.md)
</dt> </dl>

 

 





