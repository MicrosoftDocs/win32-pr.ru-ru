---
title: Метод Ивмвиртуалмачине Startup2 (Впккоминтерфацес. h)
description: Запускает виртуальную машину из неинициализированного или сохраненного состояния с дополнительными параметрами.
ms.assetid: c2679ea1-bbd5-42dc-9326-2019ad99554c
keywords:
- Метод Startup2 Virtual PC
- Метод Startup2 Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, метод Startup2
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Startup2
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b40149b0b21abc126261d8b1ddec34b9948371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415616"
---
# <a name="ivmvirtualmachinestartup2-method"></a><span data-ttu-id="067b7-106">Метод Ивмвиртуалмачине:: Startup2</span><span class="sxs-lookup"><span data-stu-id="067b7-106">IVMVirtualMachine::Startup2 method</span></span>

<span data-ttu-id="067b7-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="067b7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="067b7-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="067b7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="067b7-109">Запуск виртуальной машины из неинициализированного или сохраненного состояния с дополнительными параметрами.</span><span class="sxs-lookup"><span data-stu-id="067b7-109">Starts the virtual machine (VM) from either the uninitialized or saved state, with advanced options.</span></span>

<span data-ttu-id="067b7-110">Этот метод предоставляет механизм для запуска виртуальной машины с разностным диском, даже если изменилась метка времени родительского диска.</span><span class="sxs-lookup"><span data-stu-id="067b7-110">This method provides a mechanism to start a VM with a differencing disk even if the parent disk's timestamp has been changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="067b7-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="067b7-111">Syntax</span></span>


```C++
HRESULT Startup2(
  [in]          VMStartupOption startupOption,
  [out, retval] IVMTask         **startupTask
);
```



## <a name="parameters"></a><span data-ttu-id="067b7-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="067b7-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="067b7-113">*стартупоптион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="067b7-113">*startupOption* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="067b7-114">Дополнительный параметр запуска.</span><span class="sxs-lookup"><span data-stu-id="067b7-114">The advanced startup option.</span></span> <span data-ttu-id="067b7-115">Возможные значения — из перечисления [**вмстартупоптион**](vmstartupoption.md) .</span><span class="sxs-lookup"><span data-stu-id="067b7-115">The possible values are from the [**VMStartupOption**](vmstartupoption.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="067b7-116">*стартуптаск* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="067b7-116">*startupTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="067b7-117">Объект [**ивмтаск**](ivmtask.md) , используемый для отслеживания хода выполнения последовательности запуска.</span><span class="sxs-lookup"><span data-stu-id="067b7-117">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the start sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="067b7-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="067b7-118">Return value</span></span>

<span data-ttu-id="067b7-119">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="067b7-119">This method can return one of these values.</span></span>



| <span data-ttu-id="067b7-120">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="067b7-120">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="067b7-121">Описание</span><span class="sxs-lookup"><span data-stu-id="067b7-121">Description</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="067b7-122"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="067b7-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="067b7-123">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="067b7-123">The operation was successful.</span></span><br/>                                     |
| <dl> <span data-ttu-id="067b7-124"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="067b7-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                               | <span data-ttu-id="067b7-125">Недопустимый параметр *стартупоптион* .</span><span class="sxs-lookup"><span data-stu-id="067b7-125">The *startupOption* parameter is not valid.</span></span><br/>                       |
| <dl> <span data-ttu-id="067b7-126"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="067b7-126"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="067b7-127">Параметр *стартуптаск* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="067b7-127">The *startupTask* parameter is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="067b7-128"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ \_ отказа в доступе)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="067b7-128"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="067b7-129">Вызывающий объект должен иметь разрешения на выполнение для запуска этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="067b7-129">The caller must have execute access permissions to start this VM.</span></span><br/> |
| <dl> <span data-ttu-id="067b7-130"><dt>**Виртуальная машина \_ \_Истекло время \_ ожидания**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="067b7-130"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="067b7-131">Операция не завершилась своевременно.</span><span class="sxs-lookup"><span data-stu-id="067b7-131">The operation did not complete in a timely manner.</span></span><br/>                |
| <dl> <span data-ttu-id="067b7-132"><dt>**Виртуальная машина \_ \_Извлечь \_ из 0xA0040203 \_ ресурсов**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="067b7-132"><dt>**VM\_E\_OUT\_OF\_RESOURCE**</dt> <dt>0xA0040203</dt></span></span> </dl>                    | <span data-ttu-id="067b7-133">Недостаточно ресурсов узла.</span><span class="sxs-lookup"><span data-stu-id="067b7-133">There are not enough host resources.</span></span><br/>                              |
| <dl> <span data-ttu-id="067b7-134"><dt>**Виртуальная машина \_ \_Слишком \_ много \_ виртуальных машин**</dt> <dt>0xA0040204</dt></span><span class="sxs-lookup"><span data-stu-id="067b7-134"><dt>**VM\_E\_TOO\_MANY\_VMS**</dt> <dt>0xA0040204</dt></span></span> </dl>                       | <span data-ttu-id="067b7-135">Слишком много активных виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="067b7-135">There are too many active VMs.</span></span><br/>                                    |
| <dl> <span data-ttu-id="067b7-136"><dt>**Виртуальная машина \_ \_Виртуальная машина E \_ с**</dt> <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="067b7-136"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                          | <span data-ttu-id="067b7-137">Виртуальная машина уже запущена.</span><span class="sxs-lookup"><span data-stu-id="067b7-137">The VM is already running.</span></span><br/>                                        |
| <dl> <span data-ttu-id="067b7-138"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="067b7-138"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="067b7-139">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="067b7-139">An unexpected error has occurred.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="067b7-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="067b7-140">Remarks</span></span>

<span data-ttu-id="067b7-141">Следующие значения можно возвратить с помощью свойства [**Error**](ivmtask-error.md) возвращенного объекта [**ивмтаск**](ivmtask.md) .</span><span class="sxs-lookup"><span data-stu-id="067b7-141">The following values can be returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object.</span></span>



| <span data-ttu-id="067b7-142">Код [**ошибки**](ivmtask-error.md) /значение</span><span class="sxs-lookup"><span data-stu-id="067b7-142">[**Error**](ivmtask-error.md) code/Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="067b7-143">Описание</span><span class="sxs-lookup"><span data-stu-id="067b7-143">Description</span></span>                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="067b7-144"><span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xA0040950)</span><span class="sxs-lookup"><span data-stu-id="067b7-144"><span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xA0040950)</span></span><br/>                                                 | <span data-ttu-id="067b7-145">Оборудование не поддерживает виртуализацию.</span><span class="sxs-lookup"><span data-stu-id="067b7-145">The hardware does not support virtualization.</span></span><br/>              |
| <span data-ttu-id="067b7-146"><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xA0040951)</span><span class="sxs-lookup"><span data-stu-id="067b7-146"><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xA0040951)</span></span><br/> | <span data-ttu-id="067b7-147">Виртуализация оборудования отключена.</span><span class="sxs-lookup"><span data-stu-id="067b7-147">Hardware virtualization is disabled.</span></span><br/>                       |
| <span data-ttu-id="067b7-148"><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xA0040952)</span><span class="sxs-lookup"><span data-stu-id="067b7-148"><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xA0040952)</span></span><br/>                             | <span data-ttu-id="067b7-149">Установлены виртуальные компьютеры 2007 и Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="067b7-149">Both Virtual PC 2007 and Windows Virtual PC are installed.</span></span><br/> |
| <span data-ttu-id="067b7-150"><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xA0040953)</span><span class="sxs-lookup"><span data-stu-id="067b7-150"><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xA0040953)</span></span><br/>             | <span data-ttu-id="067b7-151">Установлено другое программное обеспечение виртуализации.</span><span class="sxs-lookup"><span data-stu-id="067b7-151">Other virtualization software is installed.</span></span><br/>                |
| <span data-ttu-id="067b7-152"><span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203)</span><span class="sxs-lookup"><span data-stu-id="067b7-152"><span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203)</span></span><br/>                                                                 | <span data-ttu-id="067b7-153">Недостаточно ресурсов узла.</span><span class="sxs-lookup"><span data-stu-id="067b7-153">There are not enough host resources.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="067b7-154">Требования</span><span class="sxs-lookup"><span data-stu-id="067b7-154">Requirements</span></span>



| <span data-ttu-id="067b7-155">Требование</span><span class="sxs-lookup"><span data-stu-id="067b7-155">Requirement</span></span> | <span data-ttu-id="067b7-156">Значение</span><span class="sxs-lookup"><span data-stu-id="067b7-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="067b7-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="067b7-157">Minimum supported client</span></span><br/> | <span data-ttu-id="067b7-158">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="067b7-158">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="067b7-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="067b7-159">Minimum supported server</span></span><br/> | <span data-ttu-id="067b7-160">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="067b7-160">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="067b7-161">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="067b7-161">End of client support</span></span><br/>    | <span data-ttu-id="067b7-162">Windows 7</span><span class="sxs-lookup"><span data-stu-id="067b7-162">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="067b7-163">Продукт</span><span class="sxs-lookup"><span data-stu-id="067b7-163">Product</span></span><br/>                  | <span data-ttu-id="067b7-164">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="067b7-164">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="067b7-165">Header</span><span class="sxs-lookup"><span data-stu-id="067b7-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="067b7-166"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="067b7-166"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="067b7-167">IID</span><span class="sxs-lookup"><span data-stu-id="067b7-167">IID</span></span><br/>                      | <span data-ttu-id="067b7-168">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="067b7-168">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="067b7-169">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="067b7-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="067b7-170">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="067b7-170">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

