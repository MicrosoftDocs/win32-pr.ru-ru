---
title: Функция Фрируткаусеинфос (Ндаттрибутилс. h)
description: Освобождает память, выделенную внутреннему массиву структур Руткаусеинфо.
ms.assetid: b45fa432-0db4-470b-80ce-ae25c33f88d6
keywords:
- Фрируткаусеинфос функция NDF
topic_type:
- apiref
api_name:
- FreeRootCauseInfos
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97d302a1c58f1a77aafa7611f437f3d445f29f9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801822"
---
# <a name="freerootcauseinfos-function"></a><span data-ttu-id="39afb-104">Функция Фрируткаусеинфос</span><span class="sxs-lookup"><span data-stu-id="39afb-104">FreeRootCauseInfos function</span></span>

<span data-ttu-id="39afb-105">Функция **фрируткаусеинфос** освобождает память, выделенную внутреннему массиву структур [**руткаусеинфо**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) .</span><span class="sxs-lookup"><span data-stu-id="39afb-105">The **FreeRootCauseInfos** function deallocates the memory allocated internally to an array of [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) structures.</span></span> <span data-ttu-id="39afb-106">Эта функция вызывает [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="39afb-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="39afb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39afb-107">Syntax</span></span>


```C++
VOID FreeRootCauseInfos(
  _In_ RootCauseInfo *pInfo,
       ULONG         RootCauseCount,
       BOOL          bFreePointer
);
```



## <a name="parameters"></a><span data-ttu-id="39afb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="39afb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39afb-109">*пинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39afb-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39afb-110">Тип: \**[**руткаусеинфо**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="39afb-110">Type: \**[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)\** _</span></span>

<span data-ttu-id="39afb-111">Массив структур.</span><span class="sxs-lookup"><span data-stu-id="39afb-111">The array of structures.</span></span> <span data-ttu-id="39afb-112">Выделенная память, на которую указывают эти структуры, будет освобождена.</span><span class="sxs-lookup"><span data-stu-id="39afb-112">The allocated memory pointed to by these structures will be freed.</span></span>

</dd> <dt>

<span data-ttu-id="39afb-113">_RootCauseCount \*</span><span class="sxs-lookup"><span data-stu-id="39afb-113">_RootCauseCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="39afb-114">Тип: **ulong**</span><span class="sxs-lookup"><span data-stu-id="39afb-114">Type: **ULONG**</span></span>

<span data-ttu-id="39afb-115">Количество структур в массиве, на которое указывает *пинфо*.</span><span class="sxs-lookup"><span data-stu-id="39afb-115">The number of structures in the array pointed to by *pInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="39afb-116">*бфрипоинтер*</span><span class="sxs-lookup"><span data-stu-id="39afb-116">*bFreePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="39afb-117">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="39afb-117">Type: **BOOL**</span></span>

<span data-ttu-id="39afb-118">Значение true, если массив структур также должен быть удален; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="39afb-118">True if the array of structures should also be deleted; otherwise, false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39afb-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="39afb-119">Return value</span></span>

<span data-ttu-id="39afb-120">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="39afb-120">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="39afb-121">Требования</span><span class="sxs-lookup"><span data-stu-id="39afb-121">Requirements</span></span>



| <span data-ttu-id="39afb-122">Требование</span><span class="sxs-lookup"><span data-stu-id="39afb-122">Requirement</span></span> | <span data-ttu-id="39afb-123">Значение</span><span class="sxs-lookup"><span data-stu-id="39afb-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="39afb-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39afb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="39afb-125">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="39afb-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="39afb-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39afb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="39afb-127">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="39afb-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="39afb-128">Header</span><span class="sxs-lookup"><span data-stu-id="39afb-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="39afb-129"><dt>Ндаттрибутилс. h</dt></span><span class="sxs-lookup"><span data-stu-id="39afb-129"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39afb-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39afb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39afb-131">**руткаусеинфо**</span><span class="sxs-lookup"><span data-stu-id="39afb-131">**RootCauseInfo**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)
</dt> <dt>

[<span data-ttu-id="39afb-132">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="39afb-132">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

