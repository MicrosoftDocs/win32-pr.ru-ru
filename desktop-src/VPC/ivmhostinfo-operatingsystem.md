---
title: Свойство операционной системы Ивмхостинфо (Впккоминтерфацес. h)
description: Возвращает операционную систему, работающую на компьютере.
ms.assetid: 1164bb7d-cdce-4649-86d6-22e3ea7bad98
keywords:
- Виртуальное ПК со свойством операционной системы
- Virtual PC, свойство операционной системы, интерфейс Ивмхостинфо
- Интерфейс Ивмхостинфо Virtual PC, свойство операционной системы
topic_type:
- apiref
api_name:
- IVMHostInfo.OperatingSystem
- IVMHostInfo.get_OperatingSystem
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55af1d0cfdc2abaa01fe78c08509c2448b4d8cc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691766"
---
# <a name="ivmhostinfooperatingsystem-property"></a><span data-ttu-id="d7f73-106">Свойство Ивмхостинфо:: операционной системы</span><span class="sxs-lookup"><span data-stu-id="d7f73-106">IVMHostInfo::OperatingSystem property</span></span>

<span data-ttu-id="d7f73-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d7f73-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d7f73-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d7f73-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d7f73-109">Возвращает операционную систему, работающую на компьютере.</span><span class="sxs-lookup"><span data-stu-id="d7f73-109">Retrieves the operating system running on the machine.</span></span>

<span data-ttu-id="d7f73-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d7f73-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7f73-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d7f73-111">Syntax</span></span>


```C++
HRESULT get_OperatingSystem(
  [out, retval] BSTR *operatingSystem
);
```



## <a name="property-value"></a><span data-ttu-id="d7f73-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d7f73-112">Property value</span></span>

<span data-ttu-id="d7f73-113">Имя операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d7f73-113">The name of the operating system.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d7f73-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="d7f73-114">Error codes</span></span>



| <span data-ttu-id="d7f73-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="d7f73-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="d7f73-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d7f73-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="d7f73-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d7f73-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="d7f73-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d7f73-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="d7f73-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="d7f73-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="d7f73-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="d7f73-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="d7f73-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d7f73-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="d7f73-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="d7f73-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d7f73-123">Требования</span><span class="sxs-lookup"><span data-stu-id="d7f73-123">Requirements</span></span>



| <span data-ttu-id="d7f73-124">Требование</span><span class="sxs-lookup"><span data-stu-id="d7f73-124">Requirement</span></span> | <span data-ttu-id="d7f73-125">Значение</span><span class="sxs-lookup"><span data-stu-id="d7f73-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f73-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d7f73-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d7f73-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d7f73-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d7f73-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d7f73-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d7f73-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d7f73-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d7f73-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d7f73-130">End of client support</span></span><br/>    | <span data-ttu-id="d7f73-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d7f73-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d7f73-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="d7f73-132">Product</span></span><br/>                  | <span data-ttu-id="d7f73-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d7f73-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d7f73-134">Header</span><span class="sxs-lookup"><span data-stu-id="d7f73-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7f73-135"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7f73-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d7f73-136">IID</span><span class="sxs-lookup"><span data-stu-id="d7f73-136">IID</span></span><br/>                      | <span data-ttu-id="d7f73-137">IID \_ ивмхостинфо определен как 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="d7f73-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="d7f73-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7f73-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7f73-139">**ивмхостинфо**</span><span class="sxs-lookup"><span data-stu-id="d7f73-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

