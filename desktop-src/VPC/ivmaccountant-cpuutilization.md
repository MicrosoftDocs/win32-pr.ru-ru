---
title: Свойство график Ивмаккаунтант (Впккоминтерфацес. h)
description: Получение процента текущей загрузки ЦП для этой виртуальной машины.
ms.assetid: 69bb61ec-af41-4bd0-95bd-4698a1d33098
keywords:
- График свойство Virtual PC
- График свойство Virtual PC, интерфейс Ивмаккаунтант
- Ивмаккаунтант интерфейс Virtual PC, свойство график
topic_type:
- apiref
api_name:
- IVMAccountant.CPUUtilization
- IVMAccountant.get_CPUUtilization
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e38c223f47678cdb9c2d49e06452d014083c94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989314"
---
# <a name="ivmaccountantcpuutilization-property"></a><span data-ttu-id="04c67-106">Свойство Ивмаккаунтант:: график</span><span class="sxs-lookup"><span data-stu-id="04c67-106">IVMAccountant::CPUUtilization property</span></span>

<span data-ttu-id="04c67-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="04c67-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="04c67-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="04c67-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="04c67-109">Получение процента текущей загрузки ЦП для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="04c67-109">Retrieves the percentage of current CPU utilization for this virtual machine.</span></span>

<span data-ttu-id="04c67-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="04c67-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="04c67-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04c67-111">Syntax</span></span>


```C++
HRESULT get_CPUUtilization(
  [out, retval] long *percentageUtilization
);
```



## <a name="property-value"></a><span data-ttu-id="04c67-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="04c67-112">Property value</span></span>

<span data-ttu-id="04c67-113">Процент текущей загрузки ЦП.</span><span class="sxs-lookup"><span data-stu-id="04c67-113">The percentage of current CPU utilization.</span></span>

## <a name="error-codes"></a><span data-ttu-id="04c67-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="04c67-114">Error codes</span></span>



| <span data-ttu-id="04c67-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="04c67-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="04c67-116">Значение</span><span class="sxs-lookup"><span data-stu-id="04c67-116">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="04c67-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="04c67-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="04c67-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="04c67-118">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="04c67-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="04c67-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="04c67-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="04c67-120">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="04c67-121"><dt>С \_ ЛОЖЬ</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="04c67-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="04c67-122">Виртуальная машина не запущена.</span><span class="sxs-lookup"><span data-stu-id="04c67-122">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="04c67-123"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="04c67-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="04c67-124">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="04c67-124">An unexpected error has occurred.</span></span><br/>   |



## <a name="requirements"></a><span data-ttu-id="04c67-125">Требования</span><span class="sxs-lookup"><span data-stu-id="04c67-125">Requirements</span></span>



| <span data-ttu-id="04c67-126">Требование</span><span class="sxs-lookup"><span data-stu-id="04c67-126">Requirement</span></span> | <span data-ttu-id="04c67-127">Значение</span><span class="sxs-lookup"><span data-stu-id="04c67-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="04c67-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="04c67-128">Minimum supported client</span></span><br/> | <span data-ttu-id="04c67-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="04c67-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="04c67-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="04c67-130">Minimum supported server</span></span><br/> | <span data-ttu-id="04c67-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="04c67-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="04c67-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="04c67-132">End of client support</span></span><br/>    | <span data-ttu-id="04c67-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="04c67-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="04c67-134">Продукт</span><span class="sxs-lookup"><span data-stu-id="04c67-134">Product</span></span><br/>                  | <span data-ttu-id="04c67-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="04c67-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="04c67-136">Header</span><span class="sxs-lookup"><span data-stu-id="04c67-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="04c67-137"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="04c67-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="04c67-138">IID</span><span class="sxs-lookup"><span data-stu-id="04c67-138">IID</span></span><br/>                      | <span data-ttu-id="04c67-139">IID \_ ивмаккаунтант определен как 6376c067-7f57-4d63-b754-06e2e4f51d73</span><span class="sxs-lookup"><span data-stu-id="04c67-139">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="04c67-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="04c67-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04c67-141">**ивмаккаунтант**</span><span class="sxs-lookup"><span data-stu-id="04c67-141">**IVMAccountant**</span></span>](ivmaccountant.md)
</dt> </dl>

 

