---
title: Функция Фрирепаиринфоексс (Ндаттрибутилс. h)
description: Освобождает память, выделенную внутреннему массиву структур Репаиринфоекс.
ms.assetid: b4e3e758-88cd-4ce2-b1a4-5b47889aae9b
keywords:
- Фрирепаиринфоексс функция NDF
topic_type:
- apiref
api_name:
- FreeRepairInfoExs
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 094c745486526caa870a500019de3aa819b6fe5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534313"
---
# <a name="freerepairinfoexs-function"></a><span data-ttu-id="502cc-104">Функция Фрирепаиринфоексс</span><span class="sxs-lookup"><span data-stu-id="502cc-104">FreeRepairInfoExs function</span></span>

<span data-ttu-id="502cc-105">Функция **фрирепаиринфоексс** освобождает память, выделенную внутреннему массиву структур [**репаиринфоекс**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex) .</span><span class="sxs-lookup"><span data-stu-id="502cc-105">The **FreeRepairInfoExs** function deallocates the memory allocated internally to an array of [**RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex) structures.</span></span> <span data-ttu-id="502cc-106">Эта функция вызывает [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="502cc-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="502cc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="502cc-107">Syntax</span></span>


```C++
VOID FreeRepairInfoExs(
  _In_ RepairInfoEx *pInfo,
       ULONG        RepairCount,
       BOOL         bFreePointer
);
```



## <a name="parameters"></a><span data-ttu-id="502cc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="502cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="502cc-109">*пинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="502cc-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="502cc-110">Тип: \**[**репаиринфоекс**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex) \** _</span><span class="sxs-lookup"><span data-stu-id="502cc-110">Type: \**[**RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex)\** _</span></span>

<span data-ttu-id="502cc-111">Массив структур.</span><span class="sxs-lookup"><span data-stu-id="502cc-111">The array of structures.</span></span> <span data-ttu-id="502cc-112">Выделенная память, на которую указывают эти структуры, будет освобождена.</span><span class="sxs-lookup"><span data-stu-id="502cc-112">The allocated memory pointed to by these structures will be freed.</span></span>

</dd> <dt>

<span data-ttu-id="502cc-113">_RepairCount \*</span><span class="sxs-lookup"><span data-stu-id="502cc-113">_RepairCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="502cc-114">Тип: **ulong**</span><span class="sxs-lookup"><span data-stu-id="502cc-114">Type: **ULONG**</span></span>

<span data-ttu-id="502cc-115">Количество структур в массиве, на которое указывает *пинфо*.</span><span class="sxs-lookup"><span data-stu-id="502cc-115">The number of structures in the array pointed to by *pInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="502cc-116">*бфрипоинтер*</span><span class="sxs-lookup"><span data-stu-id="502cc-116">*bFreePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="502cc-117">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="502cc-117">Type: **BOOL**</span></span>

<span data-ttu-id="502cc-118">Значение true, если массив структур также должен быть удален; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="502cc-118">True if the array of structures should also be deleted; otherwise, false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="502cc-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="502cc-119">Return value</span></span>

<span data-ttu-id="502cc-120">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="502cc-120">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="502cc-121">Требования</span><span class="sxs-lookup"><span data-stu-id="502cc-121">Requirements</span></span>



| <span data-ttu-id="502cc-122">Требование</span><span class="sxs-lookup"><span data-stu-id="502cc-122">Requirement</span></span> | <span data-ttu-id="502cc-123">Значение</span><span class="sxs-lookup"><span data-stu-id="502cc-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="502cc-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="502cc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="502cc-125">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="502cc-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="502cc-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="502cc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="502cc-127">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="502cc-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="502cc-128">Header</span><span class="sxs-lookup"><span data-stu-id="502cc-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="502cc-129"><dt>Ндаттрибутилс. h</dt></span><span class="sxs-lookup"><span data-stu-id="502cc-129"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="502cc-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="502cc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="502cc-131">**репаиринфоекс**</span><span class="sxs-lookup"><span data-stu-id="502cc-131">**RepairInfoEx**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex)
</dt> <dt>

[<span data-ttu-id="502cc-132">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="502cc-132">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

