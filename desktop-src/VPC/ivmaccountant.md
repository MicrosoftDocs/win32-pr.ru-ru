---
title: Интерфейс Ивмаккаунтант (Впккоминтерфацес. h)
description: Предоставляет доступ к сведениям, связанным с учетом, для виртуальной машины.
ms.assetid: 047fa4c9-cb2e-4830-bab8-0513247eff9b
keywords:
- Виртуальный ПК с интерфейсом Ивмаккаунтант
- Ивмаккаунтант интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMAccountant
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d207833b92794510789e66e31b10e94d70b319fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803755"
---
# <a name="ivmaccountant-interface"></a><span data-ttu-id="520ea-105">Интерфейс Ивмаккаунтант</span><span class="sxs-lookup"><span data-stu-id="520ea-105">IVMAccountant interface</span></span>

<span data-ttu-id="520ea-106">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="520ea-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="520ea-107">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="520ea-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="520ea-108">Предоставляет доступ к сведениям, связанным с учетом, для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="520ea-108">Provides access to accounting-related information for a virtual machine.</span></span> <span data-ttu-id="520ea-109">Чтобы получить **ивмаккаунтант** для виртуальной машины, используйте свойство [**Ивмвиртуалмачине:: бухгалтер**](ivmvirtualmachine-accountant.md) .</span><span class="sxs-lookup"><span data-stu-id="520ea-109">To retrieve the **IVMAccountant** for a virtual machine, use the [**IVMVirtualMachine::Accountant**](ivmvirtualmachine-accountant.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="520ea-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="520ea-110">Members</span></span>

<span data-ttu-id="520ea-111">Интерфейс **ивмаккаунтант** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="520ea-111">The **IVMAccountant** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="520ea-112">**Ивмаккаунтант** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="520ea-112">**IVMAccountant** also has these types of members:</span></span>

-   [<span data-ttu-id="520ea-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="520ea-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="520ea-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="520ea-114">Properties</span></span>

<span data-ttu-id="520ea-115">Интерфейс **ивмаккаунтант** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="520ea-115">The **IVMAccountant** interface has these properties.</span></span>



| <span data-ttu-id="520ea-116">Свойство</span><span class="sxs-lookup"><span data-stu-id="520ea-116">Property</span></span>                                                                        | <span data-ttu-id="520ea-117">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="520ea-117">Access type</span></span>          | <span data-ttu-id="520ea-118">Описание</span><span class="sxs-lookup"><span data-stu-id="520ea-118">Description</span></span>                                                                                             |
|:--------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="520ea-119">**График**</span><span class="sxs-lookup"><span data-stu-id="520ea-119">**CPUUtilization**</span></span>](ivmaccountant-cpuutilization.md)<br/>               | <span data-ttu-id="520ea-120">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="520ea-120">Read-only</span></span><br/> | <span data-ttu-id="520ea-121">Процент текущей загрузки ЦП для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="520ea-121">The percentage of current CPU utilization for this virtual machine.</span></span><br/>                          |
| [<span data-ttu-id="520ea-122">**кпуутилизатионхистори**</span><span class="sxs-lookup"><span data-stu-id="520ea-122">**CPUUtilizationHistory**</span></span>](ivmaccountant-cpuutilizationhistory.md)<br/> | <span data-ttu-id="520ea-123">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="520ea-123">Read-only</span></span><br/> | <span data-ttu-id="520ea-124">Последняя загрузка ЦП этой виртуальной машины (в виде массива процентных значений).</span><span class="sxs-lookup"><span data-stu-id="520ea-124">The recent CPU utilization of this virtual machine (as an array of percentage values).</span></span><br/>       |
| [<span data-ttu-id="520ea-125">**дискбитесреад**</span><span class="sxs-lookup"><span data-stu-id="520ea-125">**DiskBytesRead**</span></span>](ivmaccountant-diskbytesread.md)<br/>                 | <span data-ttu-id="520ea-126">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="520ea-126">Read-only</span></span><br/> | <span data-ttu-id="520ea-127">Общее число байтов, считанных всеми контроллерами хранилища для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="520ea-127">The total number of bytes read by all storage controllers for this virtual machine.</span></span><br/>          |
| [<span data-ttu-id="520ea-128">**дискбитесвриттен**</span><span class="sxs-lookup"><span data-stu-id="520ea-128">**DiskBytesWritten**</span></span>](ivmaccountant-diskbyteswritten.md)<br/>           | <span data-ttu-id="520ea-129">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="520ea-129">Read-only</span></span><br/> | <span data-ttu-id="520ea-130">Общее число байтов, записанных всеми контроллерами хранилища для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="520ea-130">The total number of bytes written by all storage controllers for this virtual machine.</span></span><br/>       |
| [<span data-ttu-id="520ea-131">**нетворкбитесрецеивед**</span><span class="sxs-lookup"><span data-stu-id="520ea-131">**NetworkBytesReceived**</span></span>](ivmaccountant-networkbytesreceived.md)<br/>   | <span data-ttu-id="520ea-132">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="520ea-132">Read-only</span></span><br/> | <span data-ttu-id="520ea-133">Общее число байтов, полученных всеми виртуальными сетевыми адаптерами для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="520ea-133">The total number of bytes received by all virtual network adapters for this virtual machine.</span></span><br/> |
| [<span data-ttu-id="520ea-134">**нетворкбитессент**</span><span class="sxs-lookup"><span data-stu-id="520ea-134">**NetworkBytesSent**</span></span>](ivmaccountant-networkbytessent.md)<br/>           | <span data-ttu-id="520ea-135">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="520ea-135">Read-only</span></span><br/> | <span data-ttu-id="520ea-136">Общее число байтов, отправленных всеми виртуальными сетевыми адаптерами для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="520ea-136">The total number of bytes sent by all virtual network adapters for this virtual machine.</span></span><br/>     |
| [<span data-ttu-id="520ea-137">**Просто**</span><span class="sxs-lookup"><span data-stu-id="520ea-137">**UpTime**</span></span>](ivmaccountant-uptime.md)<br/>                               | <span data-ttu-id="520ea-138">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="520ea-138">Read-only</span></span><br/> | <span data-ttu-id="520ea-139">Количество секунд, в течение которых виртуальная машина была запущена.</span><span class="sxs-lookup"><span data-stu-id="520ea-139">The number of seconds that the virtual machine has been running.</span></span><br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="520ea-140">Требования</span><span class="sxs-lookup"><span data-stu-id="520ea-140">Requirements</span></span>



| <span data-ttu-id="520ea-141">Требование</span><span class="sxs-lookup"><span data-stu-id="520ea-141">Requirement</span></span> | <span data-ttu-id="520ea-142">Значение</span><span class="sxs-lookup"><span data-stu-id="520ea-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="520ea-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="520ea-143">Minimum supported client</span></span><br/> | <span data-ttu-id="520ea-144">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="520ea-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="520ea-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="520ea-145">Minimum supported server</span></span><br/> | <span data-ttu-id="520ea-146">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="520ea-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="520ea-147">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="520ea-147">End of client support</span></span><br/>    | <span data-ttu-id="520ea-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="520ea-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="520ea-149">Продукт</span><span class="sxs-lookup"><span data-stu-id="520ea-149">Product</span></span><br/>                  | <span data-ttu-id="520ea-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="520ea-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="520ea-151">Header</span><span class="sxs-lookup"><span data-stu-id="520ea-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="520ea-152"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="520ea-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="520ea-153">IID</span><span class="sxs-lookup"><span data-stu-id="520ea-153">IID</span></span><br/>                      | <span data-ttu-id="520ea-154">IID \_ ивмаккаунтант определен как 6376c067-7f57-4d63-b754-06e2e4f51d73</span><span class="sxs-lookup"><span data-stu-id="520ea-154">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



 

