---
title: Свойство Ивмтаскколлектион Count (Впккоминтерфацес. h)
description: Возвращает число задач в этой коллекции.
ms.assetid: 5ff33bea-3f27-47ad-bcbc-6c40f2a8d78d
keywords:
- Число свойств Virtual PC
- Число свойств Virtual PC, интерфейс Ивмтаскколлектион
- Ивмтаскколлектион интерфейс Virtual PC, свойство Count
topic_type:
- apiref
api_name:
- IVMTaskCollection.Count
- IVMTaskCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e868296437a8939b29947e785aabaff08fdcb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892301"
---
# <a name="ivmtaskcollectioncount-property"></a><span data-ttu-id="6f99d-106">Свойство Ивмтаскколлектион:: count</span><span class="sxs-lookup"><span data-stu-id="6f99d-106">IVMTaskCollection::Count property</span></span>

<span data-ttu-id="6f99d-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6f99d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6f99d-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6f99d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6f99d-109">Возвращает число задач в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="6f99d-109">Retrieves the number of tasks in this collection.</span></span>

<span data-ttu-id="6f99d-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6f99d-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f99d-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f99d-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="6f99d-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6f99d-112">Property value</span></span>

<span data-ttu-id="6f99d-113">Число задач.</span><span class="sxs-lookup"><span data-stu-id="6f99d-113">The number of tasks.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6f99d-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="6f99d-114">Error codes</span></span>



| <span data-ttu-id="6f99d-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="6f99d-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="6f99d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="6f99d-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="6f99d-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6f99d-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="6f99d-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="6f99d-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="6f99d-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="6f99d-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="6f99d-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="6f99d-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="6f99d-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="6f99d-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="6f99d-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="6f99d-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="6f99d-123">Требования</span><span class="sxs-lookup"><span data-stu-id="6f99d-123">Requirements</span></span>



| <span data-ttu-id="6f99d-124">Требование</span><span class="sxs-lookup"><span data-stu-id="6f99d-124">Requirement</span></span> | <span data-ttu-id="6f99d-125">Значение</span><span class="sxs-lookup"><span data-stu-id="6f99d-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f99d-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6f99d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6f99d-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6f99d-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6f99d-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6f99d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6f99d-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6f99d-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6f99d-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="6f99d-130">End of client support</span></span><br/>    | <span data-ttu-id="6f99d-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6f99d-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6f99d-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="6f99d-132">Product</span></span><br/>                  | <span data-ttu-id="6f99d-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6f99d-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6f99d-134">Header</span><span class="sxs-lookup"><span data-stu-id="6f99d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f99d-135"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f99d-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6f99d-136">IID</span><span class="sxs-lookup"><span data-stu-id="6f99d-136">IID</span></span><br/>                      | <span data-ttu-id="6f99d-137">IID \_ ивмтаскколлектион определен как 5c4387c8-0e8b-4b97-8058-84679adf4c40</span><span class="sxs-lookup"><span data-stu-id="6f99d-137">IID\_IVMTaskCollection is defined as 5c4387c8-0e8b-4b97-8058-84679adf4c40</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="6f99d-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6f99d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f99d-139">**ивмтаскколлектион**</span><span class="sxs-lookup"><span data-stu-id="6f99d-139">**IVMTaskCollection**</span></span>](ivmtaskcollection.md)
</dt> </dl>

 

