---
title: Функция Фрихелператтрибутес (Ндаттрибутилс. h)
description: Освобождает память, выделенную внутри, в массив ВСПОМОГАТЕЛЬных \_ структур атрибутов.
ms.assetid: d973bdb9-c1d1-4cea-bcc6-98671349413f
keywords:
- Фрихелператтрибутес функция NDF
topic_type:
- apiref
api_name:
- FreeHelperAttributes
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 400addd7d32914cb4e849e4e0bfae76ccc3ddf22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489879"
---
# <a name="freehelperattributes-function"></a><span data-ttu-id="95fd9-104">Функция Фрихелператтрибутес</span><span class="sxs-lookup"><span data-stu-id="95fd9-104">FreeHelperAttributes function</span></span>

<span data-ttu-id="95fd9-105">Функция **фрихелператтрибутес** освобождает память, выделенную внутри, в массив [**вспомогательных структур \_ атрибутов**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) .</span><span class="sxs-lookup"><span data-stu-id="95fd9-105">The **FreeHelperAttributes** function deallocates the memory allocated internally to an array of [**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) structures.</span></span> <span data-ttu-id="95fd9-106">Эта функция вызывает [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="95fd9-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="95fd9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95fd9-107">Syntax</span></span>


```C++
VOID FreeHelperAttributes(
  _In_ HELPER_ATTRIBUTE *pInfo,
       ULONG            HelperAttributeCount,
       BOOL             bFreePointer
);
```



## <a name="parameters"></a><span data-ttu-id="95fd9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="95fd9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95fd9-109">*пинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="95fd9-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95fd9-110">Тип: \**[**вспомогательный \_ атрибут**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) \** _</span><span class="sxs-lookup"><span data-stu-id="95fd9-110">Type: \**[**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)\** _</span></span>

<span data-ttu-id="95fd9-111">Массив структур.</span><span class="sxs-lookup"><span data-stu-id="95fd9-111">The array of structures.</span></span> <span data-ttu-id="95fd9-112">Выделенная память, на которую указывают эти структуры, будет освобождена.</span><span class="sxs-lookup"><span data-stu-id="95fd9-112">The allocated memory pointed to by these structures will be freed.</span></span>

</dd> <dt>

<span data-ttu-id="95fd9-113">_HelperAttributeCount \*</span><span class="sxs-lookup"><span data-stu-id="95fd9-113">_HelperAttributeCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="95fd9-114">Тип: **ulong**</span><span class="sxs-lookup"><span data-stu-id="95fd9-114">Type: **ULONG**</span></span>

<span data-ttu-id="95fd9-115">Количество структур в массиве, на которое указывает *пинфо*.</span><span class="sxs-lookup"><span data-stu-id="95fd9-115">The number of structures in the array pointed to by *pInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="95fd9-116">*бфрипоинтер*</span><span class="sxs-lookup"><span data-stu-id="95fd9-116">*bFreePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="95fd9-117">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="95fd9-117">Type: **BOOL**</span></span>

<span data-ttu-id="95fd9-118">Значение true, если массив структур также должен быть удален; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="95fd9-118">True if the array of structures should also be deleted; otherwise, false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95fd9-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="95fd9-119">Return value</span></span>

<span data-ttu-id="95fd9-120">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="95fd9-120">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="95fd9-121">Требования</span><span class="sxs-lookup"><span data-stu-id="95fd9-121">Requirements</span></span>



| <span data-ttu-id="95fd9-122">Требование</span><span class="sxs-lookup"><span data-stu-id="95fd9-122">Requirement</span></span> | <span data-ttu-id="95fd9-123">Значение</span><span class="sxs-lookup"><span data-stu-id="95fd9-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="95fd9-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="95fd9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="95fd9-125">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="95fd9-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="95fd9-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="95fd9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="95fd9-127">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="95fd9-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="95fd9-128">Header</span><span class="sxs-lookup"><span data-stu-id="95fd9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="95fd9-129"><dt>Ндаттрибутилс. h</dt></span><span class="sxs-lookup"><span data-stu-id="95fd9-129"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95fd9-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95fd9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95fd9-131">**ВСПОМОГАТЕЛЬный \_ атрибут**</span><span class="sxs-lookup"><span data-stu-id="95fd9-131">**HELPER\_ATTRIBUTE**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)
</dt> <dt>

[<span data-ttu-id="95fd9-132">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="95fd9-132">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

