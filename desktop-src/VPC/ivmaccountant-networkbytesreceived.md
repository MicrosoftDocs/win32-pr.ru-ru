---
title: Свойство Нетворкбитесрецеивед Ивмаккаунтант (Впккоминтерфацес. h)
description: Общее число байтов, полученных всеми виртуальными сетевыми адаптерами для этой виртуальной машины.
ms.assetid: 6f6b32e6-d99b-405c-a788-ed646b3a7593
keywords:
- Нетворкбитесрецеивед свойство Virtual PC
- Нетворкбитесрецеивед свойство Virtual PC, интерфейс Ивмаккаунтант
- Ивмаккаунтант интерфейс Virtual PC, свойство Нетворкбитесрецеивед
topic_type:
- apiref
api_name:
- IVMAccountant.NetworkBytesReceived
- IVMAccountant.get_NetworkBytesReceived
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e14d7454516ff4e83771744c74f31ee594aa67f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492906"
---
# <a name="ivmaccountantnetworkbytesreceived-property"></a><span data-ttu-id="158c8-106">Свойство Ивмаккаунтант:: Нетворкбитесрецеивед</span><span class="sxs-lookup"><span data-stu-id="158c8-106">IVMAccountant::NetworkBytesReceived property</span></span>

<span data-ttu-id="158c8-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="158c8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="158c8-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="158c8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="158c8-109">Получает общее число байтов, полученных всеми виртуальными сетевыми адаптерами для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="158c8-109">Retrieves the total number of bytes received by all virtual network adapters for this virtual machine.</span></span>

<span data-ttu-id="158c8-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="158c8-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="158c8-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="158c8-111">Syntax</span></span>


```C++
HRESULT get_NetworkBytesReceived(
  [out, retval] VARIANT *bytesReceived
);
```



## <a name="property-value"></a><span data-ttu-id="158c8-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="158c8-112">Property value</span></span>

<span data-ttu-id="158c8-113">Общее число полученных байтов.</span><span class="sxs-lookup"><span data-stu-id="158c8-113">The total number of bytes received.</span></span> <span data-ttu-id="158c8-114">Эти данные возвращаются как **разновидность** типа " **VT \_ Decimal**".</span><span class="sxs-lookup"><span data-stu-id="158c8-114">This data is returned as a **VARIANT** of type **VT\_DECIMAL**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="158c8-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="158c8-115">Error codes</span></span>



| <span data-ttu-id="158c8-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="158c8-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="158c8-117">Значение</span><span class="sxs-lookup"><span data-stu-id="158c8-117">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="158c8-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="158c8-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="158c8-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="158c8-119">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="158c8-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="158c8-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="158c8-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="158c8-121">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="158c8-122"><dt>С \_ ЛОЖЬ</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="158c8-122"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="158c8-123">Виртуальная машина не запущена.</span><span class="sxs-lookup"><span data-stu-id="158c8-123">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="158c8-124"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="158c8-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="158c8-125">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="158c8-125">An unexpected error has occurred.</span></span><br/>   |



## <a name="remarks"></a><span data-ttu-id="158c8-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="158c8-126">Remarks</span></span>

<span data-ttu-id="158c8-127">Обратите внимание, что статистика сетевого ввода-вывода сбрасывается в ноль, когда виртуальная машина включается, сбрасывается или восстанавливается из сохраненного состояния.</span><span class="sxs-lookup"><span data-stu-id="158c8-127">Note that network I/O statistics are reset to zero when a virtual machine is powered up, reset, or restored from saved state.</span></span>

## <a name="requirements"></a><span data-ttu-id="158c8-128">Требования</span><span class="sxs-lookup"><span data-stu-id="158c8-128">Requirements</span></span>



| <span data-ttu-id="158c8-129">Требование</span><span class="sxs-lookup"><span data-stu-id="158c8-129">Requirement</span></span> | <span data-ttu-id="158c8-130">Значение</span><span class="sxs-lookup"><span data-stu-id="158c8-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="158c8-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="158c8-131">Minimum supported client</span></span><br/> | <span data-ttu-id="158c8-132">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="158c8-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="158c8-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="158c8-133">Minimum supported server</span></span><br/> | <span data-ttu-id="158c8-134">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="158c8-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="158c8-135">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="158c8-135">End of client support</span></span><br/>    | <span data-ttu-id="158c8-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="158c8-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="158c8-137">Продукт</span><span class="sxs-lookup"><span data-stu-id="158c8-137">Product</span></span><br/>                  | <span data-ttu-id="158c8-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="158c8-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="158c8-139">Header</span><span class="sxs-lookup"><span data-stu-id="158c8-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="158c8-140"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="158c8-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="158c8-141">IID</span><span class="sxs-lookup"><span data-stu-id="158c8-141">IID</span></span><br/>                      | <span data-ttu-id="158c8-142">IID \_ ивмаккаунтант определен как 6376c067-7f57-4d63-b754-06e2e4f51d73</span><span class="sxs-lookup"><span data-stu-id="158c8-142">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="158c8-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="158c8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="158c8-144">**ивмаккаунтант**</span><span class="sxs-lookup"><span data-stu-id="158c8-144">**IVMAccountant**</span></span>](ivmaccountant.md)
</dt> </dl>

 

