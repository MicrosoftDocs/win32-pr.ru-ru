---
title: Функция Фрирепаиринфос (Ндаттрибутилс. h)
description: Освобождает память, выделенную внутреннему массиву структур Репаиринфо.
ms.assetid: c40f9d10-8d9e-4c79-ac0b-fa88608888f1
keywords:
- Фрирепаиринфос функция NDF
topic_type:
- apiref
api_name:
- FreeRepairInfos
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63bf6ab2154376302e4c9dd076ccaf83a0c565c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135522"
---
# <a name="freerepairinfos-function"></a><span data-ttu-id="5fd8f-104">Функция Фрирепаиринфос</span><span class="sxs-lookup"><span data-stu-id="5fd8f-104">FreeRepairInfos function</span></span>

<span data-ttu-id="5fd8f-105">Функция **фрирепаиринфос** освобождает память, выделенную внутреннему массиву структур [**репаиринфо**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) .</span><span class="sxs-lookup"><span data-stu-id="5fd8f-105">The **FreeRepairInfos** function deallocates the memory allocated internally to an array of [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) structures.</span></span> <span data-ttu-id="5fd8f-106">Эта функция вызывает [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="5fd8f-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fd8f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5fd8f-107">Syntax</span></span>


```C++
VOID FreeRepairInfos(
  _In_ RepairInfo *pInfo,
       ULONG      RepairCount,
       BOOL       bFreePointer
);
```



## <a name="parameters"></a><span data-ttu-id="5fd8f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5fd8f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fd8f-109">*пинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5fd8f-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fd8f-110">Тип: \**[**репаиринфо**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="5fd8f-110">Type: \**[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)\** _</span></span>

<span data-ttu-id="5fd8f-111">Массив структур.</span><span class="sxs-lookup"><span data-stu-id="5fd8f-111">The array of structures.</span></span> <span data-ttu-id="5fd8f-112">Выделенная память, на которую указывают эти структуры, будет освобождена.</span><span class="sxs-lookup"><span data-stu-id="5fd8f-112">The allocated memory pointed to by these structures will be freed.</span></span>

</dd> <dt>

<span data-ttu-id="5fd8f-113">_RepairCount \*</span><span class="sxs-lookup"><span data-stu-id="5fd8f-113">_RepairCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="5fd8f-114">Тип: **ulong**</span><span class="sxs-lookup"><span data-stu-id="5fd8f-114">Type: **ULONG**</span></span>

<span data-ttu-id="5fd8f-115">Количество структур в массиве, на которое указывает *пинфо*.</span><span class="sxs-lookup"><span data-stu-id="5fd8f-115">The number of structures in the array pointed to by *pInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="5fd8f-116">*бфрипоинтер*</span><span class="sxs-lookup"><span data-stu-id="5fd8f-116">*bFreePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="5fd8f-117">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="5fd8f-117">Type: **BOOL**</span></span>

<span data-ttu-id="5fd8f-118">Значение true, если массив структур также должен быть удален; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="5fd8f-118">True if the array of structures should also be deleted; otherwise, false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fd8f-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5fd8f-119">Return value</span></span>

<span data-ttu-id="5fd8f-120">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5fd8f-120">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fd8f-121">Требования</span><span class="sxs-lookup"><span data-stu-id="5fd8f-121">Requirements</span></span>



| <span data-ttu-id="5fd8f-122">Требование</span><span class="sxs-lookup"><span data-stu-id="5fd8f-122">Requirement</span></span> | <span data-ttu-id="5fd8f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="5fd8f-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fd8f-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5fd8f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5fd8f-125">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5fd8f-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5fd8f-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5fd8f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5fd8f-127">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5fd8f-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5fd8f-128">Header</span><span class="sxs-lookup"><span data-stu-id="5fd8f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fd8f-129"><dt>Ндаттрибутилс. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fd8f-129"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fd8f-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5fd8f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fd8f-131">**репаиринфо**</span><span class="sxs-lookup"><span data-stu-id="5fd8f-131">**RepairInfo**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)
</dt> <dt>

[<span data-ttu-id="5fd8f-132">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="5fd8f-132">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

