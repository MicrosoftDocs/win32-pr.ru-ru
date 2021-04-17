---
title: Свойство Меморяваил Ивмхостинфо (Впккоминтерфацес. h)
description: Извлекает объем доступной физической памяти на размещающем компьютере в мегабайтах.
ms.assetid: cb593d02-cdb9-40f6-b57f-72fc3278f1bb
keywords:
- Меморяваил свойство Virtual PC
- Меморяваил свойство Virtual PC, интерфейс Ивмхостинфо
- Ивмхостинфо интерфейс Virtual PC, свойство Меморяваил
topic_type:
- apiref
api_name:
- IVMHostInfo.MemoryAvail
- IVMHostInfo.get_MemoryAvail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1df6be8bf62595720d01372ee891184952a0dd5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672811"
---
# <a name="ivmhostinfomemoryavail-property"></a><span data-ttu-id="76d9c-106">Свойство Ивмхостинфо:: Меморяваил</span><span class="sxs-lookup"><span data-stu-id="76d9c-106">IVMHostInfo::MemoryAvail property</span></span>

<span data-ttu-id="76d9c-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="76d9c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="76d9c-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="76d9c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="76d9c-109">Извлекает объем доступной физической памяти на размещающем компьютере в мегабайтах.</span><span class="sxs-lookup"><span data-stu-id="76d9c-109">Retrieves the amount of available physical memory in the host machine, in megabytes.</span></span>

<span data-ttu-id="76d9c-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="76d9c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="76d9c-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="76d9c-111">Syntax</span></span>


```C++
HRESULT get_MemoryAvail(
  [out, retval] VARIANT *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="76d9c-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="76d9c-112">Property value</span></span>

<span data-ttu-id="76d9c-113">Доступный объем физической памяти в мегабайтах.</span><span class="sxs-lookup"><span data-stu-id="76d9c-113">The available physical memory, in megabytes.</span></span> <span data-ttu-id="76d9c-114">Это значение является **разновидностью** типа \_ Decimal.</span><span class="sxs-lookup"><span data-stu-id="76d9c-114">This value is a **VARIANT** of type VT\_DECIMAL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="76d9c-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="76d9c-115">Error codes</span></span>



| <span data-ttu-id="76d9c-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="76d9c-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="76d9c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="76d9c-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="76d9c-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="76d9c-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="76d9c-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="76d9c-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="76d9c-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="76d9c-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="76d9c-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="76d9c-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="76d9c-122"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="76d9c-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="76d9c-123">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="76d9c-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="76d9c-124">Требования</span><span class="sxs-lookup"><span data-stu-id="76d9c-124">Requirements</span></span>



| <span data-ttu-id="76d9c-125">Требование</span><span class="sxs-lookup"><span data-stu-id="76d9c-125">Requirement</span></span> | <span data-ttu-id="76d9c-126">Значение</span><span class="sxs-lookup"><span data-stu-id="76d9c-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="76d9c-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="76d9c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="76d9c-128">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="76d9c-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="76d9c-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="76d9c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="76d9c-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="76d9c-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="76d9c-131">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="76d9c-131">End of client support</span></span><br/>    | <span data-ttu-id="76d9c-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="76d9c-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="76d9c-133">Продукт</span><span class="sxs-lookup"><span data-stu-id="76d9c-133">Product</span></span><br/>                  | <span data-ttu-id="76d9c-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="76d9c-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="76d9c-135">Header</span><span class="sxs-lookup"><span data-stu-id="76d9c-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="76d9c-136"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="76d9c-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="76d9c-137">IID</span><span class="sxs-lookup"><span data-stu-id="76d9c-137">IID</span></span><br/>                      | <span data-ttu-id="76d9c-138">IID \_ ивмхостинфо определен как 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="76d9c-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="76d9c-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="76d9c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76d9c-140">**ивмхостинфо**</span><span class="sxs-lookup"><span data-stu-id="76d9c-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

