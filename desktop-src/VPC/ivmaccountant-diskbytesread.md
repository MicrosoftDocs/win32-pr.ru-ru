---
title: Свойство Дискбитесреад Ивмаккаунтант (Впккоминтерфацес. h)
description: Общее число байтов, считанных всеми контроллерами хранилища для этой виртуальной машины.
ms.assetid: cf2c1a58-2261-496d-b8e2-a0d5285c16ab
keywords:
- Дискбитесреад свойство Virtual PC
- Дискбитесреад свойство Virtual PC, интерфейс Ивмаккаунтант
- Ивмаккаунтант интерфейс Virtual PC, свойство Дискбитесреад
topic_type:
- apiref
api_name:
- IVMAccountant.DiskBytesRead
- IVMAccountant.get_DiskBytesRead
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2dec370a9669ee5f43ae67f8d47c153c342a53d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988750"
---
# <a name="ivmaccountantdiskbytesread-property"></a><span data-ttu-id="4e6f4-106">Ивмаккаунтант: свойство Искбитесреад:D</span><span class="sxs-lookup"><span data-stu-id="4e6f4-106">IVMAccountant::DiskBytesRead property</span></span>

<span data-ttu-id="4e6f4-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4e6f4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4e6f4-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4e6f4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4e6f4-109">Получает общее число байтов, считанных всеми контроллерами хранилища для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4e6f4-109">Retrieves the total number of bytes read by all storage controllers for this virtual machine.</span></span>

<span data-ttu-id="4e6f4-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4e6f4-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e6f4-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e6f4-111">Syntax</span></span>


```C++
HRESULT get_DiskBytesRead(
  [out, retval] VARIANT *bytesRead
);
```



## <a name="property-value"></a><span data-ttu-id="4e6f4-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4e6f4-112">Property value</span></span>

<span data-ttu-id="4e6f4-113">Общее количество байтов.</span><span class="sxs-lookup"><span data-stu-id="4e6f4-113">The total number of bytes.</span></span> <span data-ttu-id="4e6f4-114">Эти данные возвращаются как **разновидность** типа " **VT \_ Decimal**".</span><span class="sxs-lookup"><span data-stu-id="4e6f4-114">This data is returned as a **VARIANT** of type **VT\_DECIMAL**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4e6f4-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="4e6f4-115">Error codes</span></span>



| <span data-ttu-id="4e6f4-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="4e6f4-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="4e6f4-117">Значение</span><span class="sxs-lookup"><span data-stu-id="4e6f4-117">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="4e6f4-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4e6f4-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="4e6f4-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="4e6f4-119">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="4e6f4-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="4e6f4-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="4e6f4-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="4e6f4-121">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="4e6f4-122"><dt>С \_ ЛОЖЬ</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4e6f4-122"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="4e6f4-123">Виртуальная машина не запущена.</span><span class="sxs-lookup"><span data-stu-id="4e6f4-123">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="4e6f4-124"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4e6f4-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="4e6f4-125">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="4e6f4-125">An unexpected error has occurred.</span></span><br/>   |



## <a name="remarks"></a><span data-ttu-id="4e6f4-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4e6f4-126">Remarks</span></span>

<span data-ttu-id="4e6f4-127">Обратите внимание, что статистика дискового ввода-вывода сбрасывается в ноль, когда виртуальная машина включается, сбрасывается или восстанавливается из сохраненного состояния.</span><span class="sxs-lookup"><span data-stu-id="4e6f4-127">Note that disk I/O statistics are reset to zero when a virtual machine is powered up, reset, or restored from saved state.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e6f4-128">Требования</span><span class="sxs-lookup"><span data-stu-id="4e6f4-128">Requirements</span></span>



| <span data-ttu-id="4e6f4-129">Требование</span><span class="sxs-lookup"><span data-stu-id="4e6f4-129">Requirement</span></span> | <span data-ttu-id="4e6f4-130">Значение</span><span class="sxs-lookup"><span data-stu-id="4e6f4-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e6f4-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4e6f4-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4e6f4-132">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4e6f4-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4e6f4-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4e6f4-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4e6f4-134">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4e6f4-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4e6f4-135">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="4e6f4-135">End of client support</span></span><br/>    | <span data-ttu-id="4e6f4-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4e6f4-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4e6f4-137">Продукт</span><span class="sxs-lookup"><span data-stu-id="4e6f4-137">Product</span></span><br/>                  | <span data-ttu-id="4e6f4-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4e6f4-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4e6f4-139">Header</span><span class="sxs-lookup"><span data-stu-id="4e6f4-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e6f4-140"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e6f4-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4e6f4-141">IID</span><span class="sxs-lookup"><span data-stu-id="4e6f4-141">IID</span></span><br/>                      | <span data-ttu-id="4e6f4-142">IID \_ ивмаккаунтант определен как 6376c067-7f57-4d63-b754-06e2e4f51d73</span><span class="sxs-lookup"><span data-stu-id="4e6f4-142">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="4e6f4-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e6f4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e6f4-144">**ивмаккаунтант**</span><span class="sxs-lookup"><span data-stu-id="4e6f4-144">**IVMAccountant**</span></span>](ivmaccountant.md)
</dt> </dl>

 

