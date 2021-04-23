---
description: Структура АДДРЕССТАБЛЕ содержит таблицу пар адресов.
ms.assetid: 84577b6c-9d43-4e53-9f8d-33685329b11d
title: Структура АДДРЕССТАБЛЕ (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESSTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 41acab19f83fdcc88a384c0407b666a7f641a598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497805"
---
# <a name="addresstable-structure"></a><span data-ttu-id="0d28a-103">Структура АДДРЕССТАБЛЕ</span><span class="sxs-lookup"><span data-stu-id="0d28a-103">ADDRESSTABLE structure</span></span>

<span data-ttu-id="0d28a-104">Структура **аддресстабле** содержит таблицу пар адресов.</span><span class="sxs-lookup"><span data-stu-id="0d28a-104">The **ADDRESSTABLE** structure contains a table of address pairs.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d28a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d28a-105">Syntax</span></span>


```C++
typedef struct _ADDRESSTABLE {
  DWORD       nAddressPairs;
  DWORD       nNonMacAddressPairs;
  ADDRESSPAIR AddressPair[MAX_ADDRESS_PAIRS];
} ADDRESSTABLE, *LPADDRESSTABLE;
```



## <a name="members"></a><span data-ttu-id="0d28a-106">Члены</span><span class="sxs-lookup"><span data-stu-id="0d28a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0d28a-107">**наддресспаирс**</span><span class="sxs-lookup"><span data-stu-id="0d28a-107">**nAddressPairs**</span></span>
</dt> <dd>

<span data-ttu-id="0d28a-108">Число пар адресов в массиве **аддресспаир** .</span><span class="sxs-lookup"><span data-stu-id="0d28a-108">Number of address pairs in the **AddressPair** array.</span></span>

</dd> <dt>

<span data-ttu-id="0d28a-109">**ннонмакаддресспаирс**</span><span class="sxs-lookup"><span data-stu-id="0d28a-109">**nNonMacAddressPairs**</span></span>
</dt> <dd>

<span data-ttu-id="0d28a-110">Число пар адресов, отличных от MAC.</span><span class="sxs-lookup"><span data-stu-id="0d28a-110">Number of non-MAC address pairs.</span></span>

</dd> <dt>

<span data-ttu-id="0d28a-111">**аддресспаир**</span><span class="sxs-lookup"><span data-stu-id="0d28a-111">**AddressPair**</span></span>
</dt> <dd>

<span data-ttu-id="0d28a-112">Массив пар адресов.</span><span class="sxs-lookup"><span data-stu-id="0d28a-112">Array of address pairs.</span></span> <span data-ttu-id="0d28a-113">Обратите внимание, что можно хранить не более восьми пар адресов на структуру АДДРЕССТАБЛЕ.</span><span class="sxs-lookup"><span data-stu-id="0d28a-113">Note that you may only store up to eight address pairs per ADDRESSTABLE structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d28a-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d28a-114">Remarks</span></span>

<span data-ttu-id="0d28a-115">Используйте эту структуру как часть процесса создания фильтра записи.</span><span class="sxs-lookup"><span data-stu-id="0d28a-115">Use this structure as part of the capture filter construction process.</span></span> <span data-ttu-id="0d28a-116">Дополнительные сведения о реализации этой структуры см. в разделе [фильтры записи](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="0d28a-116">For more information about implementing this structure, see [Capture Filters](capture-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d28a-117">Требования</span><span class="sxs-lookup"><span data-stu-id="0d28a-117">Requirements</span></span>



| <span data-ttu-id="0d28a-118">Требование</span><span class="sxs-lookup"><span data-stu-id="0d28a-118">Requirement</span></span> | <span data-ttu-id="0d28a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="0d28a-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0d28a-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0d28a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0d28a-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0d28a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0d28a-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0d28a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0d28a-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0d28a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0d28a-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0d28a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d28a-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d28a-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d28a-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d28a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d28a-127">аддресспаир</span><span class="sxs-lookup"><span data-stu-id="0d28a-127">ADDRESSPAIR</span></span>](addresspair.md)
</dt> <dt>

[<span data-ttu-id="0d28a-128">каптурефилтер</span><span class="sxs-lookup"><span data-stu-id="0d28a-128">CAPTUREFILTER</span></span>](capturefilter.md)
</dt> </dl>

 

 




