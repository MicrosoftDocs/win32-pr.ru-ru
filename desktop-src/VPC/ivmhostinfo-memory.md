---
title: Свойство памяти Ивмхостинфо (Впккоминтерфацес. h)
description: Получает общий объем физической памяти на размещающем компьютере в мегабайтах.
ms.assetid: 178013c0-cf29-4f1e-9a9d-d6a5dbd4fe2d
keywords:
- Свойство памяти Virtual PC
- Свойство памяти Virtual PC, интерфейс Ивмхостинфо
- Виртуальный ПК интерфейса Ивмхостинфо, свойство Memory
topic_type:
- apiref
api_name:
- IVMHostInfo.Memory
- IVMHostInfo.get_Memory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39f634bfe3bf81dcb13c9f09d8f19a5a82aa6902
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691924"
---
# <a name="ivmhostinfomemory-property"></a><span data-ttu-id="24ffe-106">Свойство Ивмхостинфо:: Memory</span><span class="sxs-lookup"><span data-stu-id="24ffe-106">IVMHostInfo::Memory property</span></span>

<span data-ttu-id="24ffe-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="24ffe-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="24ffe-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="24ffe-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="24ffe-109">Получает общий объем физической памяти на размещающем компьютере в мегабайтах.</span><span class="sxs-lookup"><span data-stu-id="24ffe-109">Retrieves the total amount of physical memory in the host machine, in megabytes.</span></span>

<span data-ttu-id="24ffe-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="24ffe-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="24ffe-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24ffe-111">Syntax</span></span>


```C++
HRESULT get_Memory(
  [out, retval] VARIANT *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="24ffe-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="24ffe-112">Property value</span></span>

<span data-ttu-id="24ffe-113">Общий объем физической памяти в мегабайтах.</span><span class="sxs-lookup"><span data-stu-id="24ffe-113">The total amount of physical memory, in megabytes.</span></span> <span data-ttu-id="24ffe-114">Это значение является **разновидностью** типа \_ Decimal.</span><span class="sxs-lookup"><span data-stu-id="24ffe-114">This value is a **VARIANT** of type VT\_DECIMAL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="24ffe-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="24ffe-115">Error codes</span></span>



| <span data-ttu-id="24ffe-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="24ffe-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="24ffe-117">Значение</span><span class="sxs-lookup"><span data-stu-id="24ffe-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="24ffe-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="24ffe-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="24ffe-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="24ffe-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="24ffe-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="24ffe-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="24ffe-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="24ffe-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="24ffe-122"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="24ffe-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="24ffe-123">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="24ffe-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="24ffe-124">Требования</span><span class="sxs-lookup"><span data-stu-id="24ffe-124">Requirements</span></span>



| <span data-ttu-id="24ffe-125">Требование</span><span class="sxs-lookup"><span data-stu-id="24ffe-125">Requirement</span></span> | <span data-ttu-id="24ffe-126">Значение</span><span class="sxs-lookup"><span data-stu-id="24ffe-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="24ffe-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="24ffe-127">Minimum supported client</span></span><br/> | <span data-ttu-id="24ffe-128">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="24ffe-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="24ffe-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="24ffe-129">Minimum supported server</span></span><br/> | <span data-ttu-id="24ffe-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="24ffe-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="24ffe-131">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="24ffe-131">End of client support</span></span><br/>    | <span data-ttu-id="24ffe-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="24ffe-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="24ffe-133">Продукт</span><span class="sxs-lookup"><span data-stu-id="24ffe-133">Product</span></span><br/>                  | <span data-ttu-id="24ffe-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="24ffe-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="24ffe-135">Header</span><span class="sxs-lookup"><span data-stu-id="24ffe-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="24ffe-136"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="24ffe-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="24ffe-137">IID</span><span class="sxs-lookup"><span data-stu-id="24ffe-137">IID</span></span><br/>                      | <span data-ttu-id="24ffe-138">IID \_ ивмхостинфо определен как 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="24ffe-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="24ffe-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24ffe-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24ffe-140">**ивмхостинфо**</span><span class="sxs-lookup"><span data-stu-id="24ffe-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

