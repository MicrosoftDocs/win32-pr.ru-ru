---
title: Свойство Ивмаккаунтант "время работы" (Впккоминтерфацес. h)
description: Возвращает количество секунд, в течение которых виртуальная машина была запущена.
ms.assetid: 0c62d51b-fdf1-43f6-81d8-a5f0538c510f
keywords:
- Свойство "время работоспособности" Virtual PC
- Свойство "время работы" Virtual PC, интерфейс Ивмаккаунтант
- Виртуальный ПК интерфейса Ивмаккаунтант, свойство времени работы
topic_type:
- apiref
api_name:
- IVMAccountant.UpTime
- IVMAccountant.get_UpTime
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c496aa9c32d402dcc8e84bad5410ec7774d2a80a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136098"
---
# <a name="ivmaccountantuptime-property"></a><span data-ttu-id="89fff-106">Свойство Ивмаккаунтант:: время работы</span><span class="sxs-lookup"><span data-stu-id="89fff-106">IVMAccountant::UpTime property</span></span>

<span data-ttu-id="89fff-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="89fff-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="89fff-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="89fff-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="89fff-109">Возвращает количество секунд, в течение которых виртуальная машина была запущена.</span><span class="sxs-lookup"><span data-stu-id="89fff-109">Retrieves the number of seconds that the virtual machine has been running.</span></span>

<span data-ttu-id="89fff-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="89fff-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="89fff-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89fff-111">Syntax</span></span>


```C++
HRESULT get_UpTime(
  [out, retval] long *secondsAlive
);
```



## <a name="property-value"></a><span data-ttu-id="89fff-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="89fff-112">Property value</span></span>

<span data-ttu-id="89fff-113">количество секунд.</span><span class="sxs-lookup"><span data-stu-id="89fff-113">The number of seconds.</span></span>

## <a name="error-codes"></a><span data-ttu-id="89fff-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="89fff-114">Error codes</span></span>



| <span data-ttu-id="89fff-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="89fff-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="89fff-116">Значение</span><span class="sxs-lookup"><span data-stu-id="89fff-116">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="89fff-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="89fff-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="89fff-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="89fff-118">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="89fff-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="89fff-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="89fff-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="89fff-120">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="89fff-121"><dt>С \_ ЛОЖЬ</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="89fff-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="89fff-122">Виртуальная машина не запущена.</span><span class="sxs-lookup"><span data-stu-id="89fff-122">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="89fff-123"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="89fff-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="89fff-124">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="89fff-124">An unexpected error has occurred.</span></span><br/>   |



## <a name="requirements"></a><span data-ttu-id="89fff-125">Требования</span><span class="sxs-lookup"><span data-stu-id="89fff-125">Requirements</span></span>



| <span data-ttu-id="89fff-126">Требование</span><span class="sxs-lookup"><span data-stu-id="89fff-126">Requirement</span></span> | <span data-ttu-id="89fff-127">Значение</span><span class="sxs-lookup"><span data-stu-id="89fff-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="89fff-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="89fff-128">Minimum supported client</span></span><br/> | <span data-ttu-id="89fff-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="89fff-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="89fff-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="89fff-130">Minimum supported server</span></span><br/> | <span data-ttu-id="89fff-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="89fff-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="89fff-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="89fff-132">End of client support</span></span><br/>    | <span data-ttu-id="89fff-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="89fff-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="89fff-134">Продукт</span><span class="sxs-lookup"><span data-stu-id="89fff-134">Product</span></span><br/>                  | <span data-ttu-id="89fff-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="89fff-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="89fff-136">Header</span><span class="sxs-lookup"><span data-stu-id="89fff-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="89fff-137"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="89fff-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="89fff-138">IID</span><span class="sxs-lookup"><span data-stu-id="89fff-138">IID</span></span><br/>                      | <span data-ttu-id="89fff-139">IID \_ ивмаккаунтант определен как 6376c067-7f57-4d63-b754-06e2e4f51d73</span><span class="sxs-lookup"><span data-stu-id="89fff-139">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="89fff-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89fff-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89fff-141">**ивмаккаунтант**</span><span class="sxs-lookup"><span data-stu-id="89fff-141">**IVMAccountant**</span></span>](ivmaccountant.md)
</dt> </dl>

 

