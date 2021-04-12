---
title: Свойство Кпуутилизатионхистори Ивмаккаунтант (Впккоминтерфацес. h)
description: Получает последнюю загрузку ЦП этой виртуальной машины (в виде массива процентных значений).
ms.assetid: f6b92b25-9455-4061-8db0-3e42f9f7391d
keywords:
- Кпуутилизатионхистори свойство Virtual PC
- Кпуутилизатионхистори свойство Virtual PC, интерфейс Ивмаккаунтант
- Ивмаккаунтант интерфейс Virtual PC, свойство Кпуутилизатионхистори
topic_type:
- apiref
api_name:
- IVMAccountant.CPUUtilizationHistory
- IVMAccountant.get_CPUUtilizationHistory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfa7e91a83be7ab4c09a0b779a729745e80e1e74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492912"
---
# <a name="ivmaccountantcpuutilizationhistory-property"></a><span data-ttu-id="839b6-106">Свойство Ивмаккаунтант:: Кпуутилизатионхистори</span><span class="sxs-lookup"><span data-stu-id="839b6-106">IVMAccountant::CPUUtilizationHistory property</span></span>

<span data-ttu-id="839b6-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="839b6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="839b6-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="839b6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="839b6-109">Получает последнюю загрузку ЦП этой виртуальной машины (в виде массива процентных значений).</span><span class="sxs-lookup"><span data-stu-id="839b6-109">Retrieves the recent CPU utilization of this virtual machine (as an array of percentage values).</span></span>

<span data-ttu-id="839b6-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="839b6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="839b6-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="839b6-111">Syntax</span></span>


```C++
HRESULT get_CPUUtilizationHistory(
  [out, retval] VARIANT *percentageUtilization
);
```



## <a name="property-value"></a><span data-ttu-id="839b6-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="839b6-112">Property value</span></span>

<span data-ttu-id="839b6-113">Последнее использование ЦП этой виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="839b6-113">The recent CPU use of this virtual machine.</span></span> <span data-ttu-id="839b6-114">Эти данные возвращаются в виде массива элементов 60, представляющих процент использования ЦП в секунду за последнюю минуту.</span><span class="sxs-lookup"><span data-stu-id="839b6-114">This data is returned as an array of 60 elements that represent the percentage of CPU use at each second over the past minute.</span></span> <span data-ttu-id="839b6-115">Тип Variant — это VT \_ array \| VT \_ UI1.</span><span class="sxs-lookup"><span data-stu-id="839b6-115">Variant type is VT\_ARRAY\|VT\_UI1.</span></span>

## <a name="error-codes"></a><span data-ttu-id="839b6-116">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="839b6-116">Error codes</span></span>



| <span data-ttu-id="839b6-117">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="839b6-117">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="839b6-118">Значение</span><span class="sxs-lookup"><span data-stu-id="839b6-118">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="839b6-119"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="839b6-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="839b6-120">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="839b6-120">The operation was successful.</span></span><br/>                                           |
| <dl> <span data-ttu-id="839b6-121"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="839b6-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="839b6-122">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="839b6-122">The parameter is **NULL**.</span></span><br/>                                              |
| <dl> <span data-ttu-id="839b6-123"><dt>С \_ ЛОЖЬ</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="839b6-123"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="839b6-124">Виртуальная машина не запущена.</span><span class="sxs-lookup"><span data-stu-id="839b6-124">The virtual machine is not running.</span></span> <span data-ttu-id="839b6-125">Все элементы массива 60 имеют значение 0.</span><span class="sxs-lookup"><span data-stu-id="839b6-125">All 60 array elements are set to 0.</span></span><br/> |
| <dl> <span data-ttu-id="839b6-126"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="839b6-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="839b6-127">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="839b6-127">An unexpected error has occurred.</span></span><br/>                                       |



## <a name="requirements"></a><span data-ttu-id="839b6-128">Требования</span><span class="sxs-lookup"><span data-stu-id="839b6-128">Requirements</span></span>



| <span data-ttu-id="839b6-129">Требование</span><span class="sxs-lookup"><span data-stu-id="839b6-129">Requirement</span></span> | <span data-ttu-id="839b6-130">Значение</span><span class="sxs-lookup"><span data-stu-id="839b6-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="839b6-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="839b6-131">Minimum supported client</span></span><br/> | <span data-ttu-id="839b6-132">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="839b6-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="839b6-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="839b6-133">Minimum supported server</span></span><br/> | <span data-ttu-id="839b6-134">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="839b6-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="839b6-135">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="839b6-135">End of client support</span></span><br/>    | <span data-ttu-id="839b6-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="839b6-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="839b6-137">Продукт</span><span class="sxs-lookup"><span data-stu-id="839b6-137">Product</span></span><br/>                  | <span data-ttu-id="839b6-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="839b6-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="839b6-139">Header</span><span class="sxs-lookup"><span data-stu-id="839b6-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="839b6-140"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="839b6-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="839b6-141">IID</span><span class="sxs-lookup"><span data-stu-id="839b6-141">IID</span></span><br/>                      | <span data-ttu-id="839b6-142">IID \_ ивмаккаунтант определен как 6376c067-7f57-4d63-b754-06e2e4f51d73</span><span class="sxs-lookup"><span data-stu-id="839b6-142">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="839b6-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="839b6-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="839b6-144">**ивмаккаунтант**</span><span class="sxs-lookup"><span data-stu-id="839b6-144">**IVMAccountant**</span></span>](ivmaccountant.md)
</dt> </dl>

 

