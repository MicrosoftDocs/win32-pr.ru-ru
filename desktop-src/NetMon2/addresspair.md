---
description: Структура АДДРЕССПАИР конструирует фильтр записи.
ms.assetid: 0dd2bcaa-5e0f-448f-969e-14b923a01a2f
title: Структура АДДРЕССПАИР (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESSPAIR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7960a8bb1c3ed1b2fc86c93f371b2f05d299b97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663650"
---
# <a name="addresspair-structure"></a><span data-ttu-id="d3e08-103">Структура АДДРЕССПАИР</span><span class="sxs-lookup"><span data-stu-id="d3e08-103">ADDRESSPAIR structure</span></span>

<span data-ttu-id="d3e08-104">Структура **аддресспаир** конструирует фильтр записи.</span><span class="sxs-lookup"><span data-stu-id="d3e08-104">The **ADDRESSPAIR** structure constructs a capture filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3e08-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d3e08-105">Syntax</span></span>


```C++
typedef struct _ADDRESSPAIR {
  WORD    AddressFlags;
  WORD    NalReserved;
  ADDRESS DstAddress;
  ADDRESS SrcAddress;
} ADDRESSPAIR, *LPADDRESSPAIR;
```



## <a name="members"></a><span data-ttu-id="d3e08-106">Члены</span><span class="sxs-lookup"><span data-stu-id="d3e08-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d3e08-107">**аддрессфлагс**</span><span class="sxs-lookup"><span data-stu-id="d3e08-107">**AddressFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d3e08-108">Флаги, описывающие адреса, используемые фильтром записи.</span><span class="sxs-lookup"><span data-stu-id="d3e08-108">Flags that describe the addresses used by a capture filter.</span></span> <span data-ttu-id="d3e08-109">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="d3e08-109">See Remarks for more information.</span></span>



| <span data-ttu-id="d3e08-110">Значение</span><span class="sxs-lookup"><span data-stu-id="d3e08-110">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="d3e08-111">Значение</span><span class="sxs-lookup"><span data-stu-id="d3e08-111">Meaning</span></span>                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="ADDRESS_FLAGS_MATCH_DST"></span><span id="address_flags_match_dst"></span><dl> <span data-ttu-id="d3e08-112"><dt>**\_Флаги адреса \_ соответствуют \_ летнему времени**</dt></span><span class="sxs-lookup"><span data-stu-id="d3e08-112"><dt>**ADDRESS\_FLAGS\_MATCH\_DST**</dt></span></span> </dl>                 | <span data-ttu-id="d3e08-113">Соответствует адресу назначения.</span><span class="sxs-lookup"><span data-stu-id="d3e08-113">Matches the destination address.</span></span><br/>                              |
| <span id="ADDRESS_FLAGS_MATCH_SRC"></span><span id="address_flags_match_src"></span><dl> <span data-ttu-id="d3e08-114"><dt>**\_Флаги адреса \_ совпадают с \_ src**</dt></span><span class="sxs-lookup"><span data-stu-id="d3e08-114"><dt>**ADDRESS\_FLAGS\_MATCH\_SRC**</dt></span></span> </dl>                 | <span data-ttu-id="d3e08-115">Соответствует исходному адресу.</span><span class="sxs-lookup"><span data-stu-id="d3e08-115">Matches the source address.</span></span><br/>                                   |
| <span id="ADDRESS_FLAGS_EXCLUDED"></span><span id="address_flags_excluded"></span><dl> <span data-ttu-id="d3e08-116"><dt>**\_исключаемые флаги адреса \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d3e08-116"><dt>**ADDRESS\_FLAGS\_EXCLUDED**</dt></span></span> </dl>                     | <span data-ttu-id="d3e08-117">Исключает рамку, если этот адрес найден.</span><span class="sxs-lookup"><span data-stu-id="d3e08-117">Excludes the frame if this address is found.</span></span><br/>                  |
| <span id="ADDRESS_FLAGS_DST_GROUP_ADDR"></span><span id="address_flags_dst_group_addr"></span><dl> <span data-ttu-id="d3e08-118"><dt>**\_флаг адреса \_ адрес \_ группы \_ DST**</dt></span><span class="sxs-lookup"><span data-stu-id="d3e08-118"><dt>**ADDRESS\_FLAGS\_DST\_GROUP\_ADDR**</dt></span></span> </dl> | <span data-ttu-id="d3e08-119">Соответствует только биту группы.</span><span class="sxs-lookup"><span data-stu-id="d3e08-119">Matches group bit only.</span></span> <span data-ttu-id="d3e08-120">Используйте этот параметр для сообщений типа Broadcast.</span><span class="sxs-lookup"><span data-stu-id="d3e08-120">Use this for broadcast-type messages.</span></span><br/> |
| <span id="ADDRESS_FLAGS_MATCH_BOTH"></span><span id="address_flags_match_both"></span><dl> <span data-ttu-id="d3e08-121"><dt>**\_Флаги адреса \_ совпадают \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d3e08-121"><dt>**ADDRESS\_FLAGS\_MATCH\_BOTH**</dt></span></span> </dl>              | <span data-ttu-id="d3e08-122">Совпадает с адресами назначения и источника.</span><span class="sxs-lookup"><span data-stu-id="d3e08-122">Matches destination and source addresses.</span></span><br/>                     |



 

</dd> <dt>

<span data-ttu-id="d3e08-123">**налресервед**</span><span class="sxs-lookup"><span data-stu-id="d3e08-123">**NalReserved**</span></span>
</dt> <dd>

<span data-ttu-id="d3e08-124">Это зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="d3e08-124">This is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="d3e08-125">**дстаддресс**</span><span class="sxs-lookup"><span data-stu-id="d3e08-125">**DstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="d3e08-126">Адрес назначения элемента пары адресов.</span><span class="sxs-lookup"><span data-stu-id="d3e08-126">Destination address of the address pair element.</span></span>

</dd> <dt>

<span data-ttu-id="d3e08-127">**сркаддресс**</span><span class="sxs-lookup"><span data-stu-id="d3e08-127">**SrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="d3e08-128">Исходный адрес элемента пары адресов.</span><span class="sxs-lookup"><span data-stu-id="d3e08-128">Source address of the address pair element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d3e08-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d3e08-129">Remarks</span></span>

<span data-ttu-id="d3e08-130">Флаги элемента **аддрессфлагс** можно объединить.</span><span class="sxs-lookup"><span data-stu-id="d3e08-130">The flags of the **AddressFlags** member can be combined.</span></span> <span data-ttu-id="d3e08-131">Например, следующий параметр исключает кадр при обнаружении указанного исходного адреса.</span><span class="sxs-lookup"><span data-stu-id="d3e08-131">For example the following setting excludes the frame if the specified source address is detected.</span></span>

``` syntax
ADDRESS_FLAGS_MATCH_SOURCE|ADDRESS_FLAGS_EXCLUDED
```

<span data-ttu-id="d3e08-132">Дополнительные сведения о реализации этой структуры см. в разделе [фильтры записи](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="d3e08-132">For more information about implementing this structure, see [Capture Filters](capture-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3e08-133">Требования</span><span class="sxs-lookup"><span data-stu-id="d3e08-133">Requirements</span></span>



| <span data-ttu-id="d3e08-134">Требование</span><span class="sxs-lookup"><span data-stu-id="d3e08-134">Requirement</span></span> | <span data-ttu-id="d3e08-135">Значение</span><span class="sxs-lookup"><span data-stu-id="d3e08-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d3e08-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d3e08-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d3e08-137">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d3e08-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d3e08-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d3e08-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d3e08-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d3e08-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d3e08-140">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d3e08-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3e08-141"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3e08-141"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3e08-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d3e08-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3e08-143">каптурефилтер</span><span class="sxs-lookup"><span data-stu-id="d3e08-143">CAPTUREFILTER</span></span>](capturefilter.md)
</dt> </dl>

 

 




