---
title: Метод запуска Ивмвиртуалмачине (Впккоминтерфацес. h)
description: Запускает виртуальную машину из неинициализированного или сохраненного состояния.
ms.assetid: 82f9b6f1-99b1-4402-93f5-b4aa3520a505
keywords:
- Метод запуска Virtual PC
- Метод запуска Virtual PC, интерфейс Ивмвиртуалмачине
- Виртуальный ПК интерфейса Ивмвиртуалмачине, метод запуска
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Startup
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a45e0952fc1a17fc6ba2ea639f2ee87f7b9ef2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989142"
---
# <a name="ivmvirtualmachinestartup-method"></a><span data-ttu-id="871e2-106">Метод Ивмвиртуалмачине:: Startup</span><span class="sxs-lookup"><span data-stu-id="871e2-106">IVMVirtualMachine::Startup method</span></span>

<span data-ttu-id="871e2-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="871e2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="871e2-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="871e2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="871e2-109">Запускает виртуальную машину из неинициализированного или сохраненного состояния.</span><span class="sxs-lookup"><span data-stu-id="871e2-109">Starts the virtual machine from either the uninitialized or saved state.</span></span>

## <a name="syntax"></a><span data-ttu-id="871e2-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="871e2-110">Syntax</span></span>


```C++
HRESULT Startup(
  [out, retval] IVMTask **startupTask
);
```



## <a name="parameters"></a><span data-ttu-id="871e2-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="871e2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="871e2-112">*стартуптаск* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="871e2-112">*startupTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="871e2-113">Объект [**ивмтаск**](ivmtask.md) , используемый для отслеживания хода выполнения последовательности запуска виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="871e2-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the virtual machine's startup sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="871e2-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="871e2-114">Return value</span></span>

<span data-ttu-id="871e2-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="871e2-115">This method can return one of these values.</span></span>



| <span data-ttu-id="871e2-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="871e2-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="871e2-117">Описание</span><span class="sxs-lookup"><span data-stu-id="871e2-117">Description</span></span>                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="871e2-118"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="871e2-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="871e2-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="871e2-119">The operation was successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="871e2-120"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="871e2-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="871e2-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="871e2-121">The parameter is **NULL**.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="871e2-122"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ \_ отказа в доступе)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="871e2-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="871e2-123">Вызывающий объект должен иметь разрешения на выполнение для запуска этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="871e2-123">The caller must have execute access permissions to start this virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="871e2-124"><dt>**Виртуальная машина \_ \_Истекло время \_ ожидания**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="871e2-124"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="871e2-125">Операция не завершилась своевременно.</span><span class="sxs-lookup"><span data-stu-id="871e2-125">The operation did not complete in a timely manner.</span></span><br/>                             |
| <dl> <span data-ttu-id="871e2-126"><dt>**Виртуальная машина \_ \_Извлечь \_ из 0xA0040203 \_ ресурсов**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="871e2-126"><dt>**VM\_E\_OUT\_OF\_RESOURCE**</dt> <dt>0xA0040203</dt></span></span> </dl>                    | <span data-ttu-id="871e2-127">Недостаточно ресурсов узла.</span><span class="sxs-lookup"><span data-stu-id="871e2-127">There are not enough host resources.</span></span><br/>                                           |
| <dl> <span data-ttu-id="871e2-128"><dt>**Виртуальная машина \_ \_Слишком \_ много \_ виртуальных машин**</dt> <dt>0xA0040204</dt></span><span class="sxs-lookup"><span data-stu-id="871e2-128"><dt>**VM\_E\_TOO\_MANY\_VMS**</dt> <dt>0xA0040204</dt></span></span> </dl>                       | <span data-ttu-id="871e2-129">Слишком много активных виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="871e2-129">There are too many active virtual machines.</span></span><br/>                                    |
| <dl> <span data-ttu-id="871e2-130"><dt>**Виртуальная машина \_ \_Виртуальная машина E \_ с**</dt> <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="871e2-130"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                          | <span data-ttu-id="871e2-131">Виртуальная машина уже запущена.</span><span class="sxs-lookup"><span data-stu-id="871e2-131">The virtual machine is already running.</span></span><br/>                                        |
| <dl> <span data-ttu-id="871e2-132"><dt>**Виртуальная машина \_ \_ \_ Измененный родительский**</dt> <dt>0xA00400687</dt></span><span class="sxs-lookup"><span data-stu-id="871e2-132"><dt>**VM\_E\_PARENT\_MODIFIED**</dt> <dt>0xA00400687</dt></span></span> </dl>                    | <span data-ttu-id="871e2-133">Не удается запустить виртуальную машину, так как родительский виртуальный жесткий диск был изменен.</span><span class="sxs-lookup"><span data-stu-id="871e2-133">The virtual machine cannot be started as the parent VHD has been modified.</span></span><br/>     |
| <dl> <span data-ttu-id="871e2-134"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="871e2-134"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="871e2-135">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="871e2-135">An unexpected error has occurred.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="871e2-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="871e2-136">Remarks</span></span>

<span data-ttu-id="871e2-137">Если виртуальная машина сохранена, она будет восстановлена из сохраненного состояния.</span><span class="sxs-lookup"><span data-stu-id="871e2-137">If the virtual machine is saved, it will be restored from the saved state.</span></span>

<span data-ttu-id="871e2-138">Следующие значения можно возвратить с помощью свойства [**Error**](ivmtask-error.md) возвращенного объекта [**ивмтаск**](ivmtask.md) .</span><span class="sxs-lookup"><span data-stu-id="871e2-138">The following values can be returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object.</span></span>



| <span data-ttu-id="871e2-139">Код [**ошибки**](ivmtask-error.md) /значение</span><span class="sxs-lookup"><span data-stu-id="871e2-139">[**Error**](ivmtask-error.md) code/Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="871e2-140">Описание</span><span class="sxs-lookup"><span data-stu-id="871e2-140">Description</span></span>                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="871e2-141"><span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xA0040950)</span><span class="sxs-lookup"><span data-stu-id="871e2-141"><span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xA0040950)</span></span><br/>                                                 | <span data-ttu-id="871e2-142">Оборудование не поддерживает виртуализацию.</span><span class="sxs-lookup"><span data-stu-id="871e2-142">The hardware does not support virtualization.</span></span><br/>              |
| <span data-ttu-id="871e2-143"><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xA0040951)</span><span class="sxs-lookup"><span data-stu-id="871e2-143"><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xA0040951)</span></span><br/> | <span data-ttu-id="871e2-144">Виртуализация оборудования отключена.</span><span class="sxs-lookup"><span data-stu-id="871e2-144">Hardware virtualization is disabled.</span></span><br/>                       |
| <span data-ttu-id="871e2-145"><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xA0040952)</span><span class="sxs-lookup"><span data-stu-id="871e2-145"><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xA0040952)</span></span><br/>                             | <span data-ttu-id="871e2-146">Установлены виртуальные компьютеры 2007 и Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="871e2-146">Both Virtual PC 2007 and Windows Virtual PC are installed.</span></span><br/> |
| <span data-ttu-id="871e2-147"><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xA0040953)</span><span class="sxs-lookup"><span data-stu-id="871e2-147"><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xA0040953)</span></span><br/>             | <span data-ttu-id="871e2-148">Установлено другое программное обеспечение виртуализации.</span><span class="sxs-lookup"><span data-stu-id="871e2-148">Other virtualization software is installed.</span></span><br/>                |
| <span data-ttu-id="871e2-149"><span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203)</span><span class="sxs-lookup"><span data-stu-id="871e2-149"><span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203)</span></span><br/>                                                                 | <span data-ttu-id="871e2-150">Недостаточно ресурсов узла.</span><span class="sxs-lookup"><span data-stu-id="871e2-150">There are not enough host resources.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="871e2-151">Требования</span><span class="sxs-lookup"><span data-stu-id="871e2-151">Requirements</span></span>



| <span data-ttu-id="871e2-152">Требование</span><span class="sxs-lookup"><span data-stu-id="871e2-152">Requirement</span></span> | <span data-ttu-id="871e2-153">Значение</span><span class="sxs-lookup"><span data-stu-id="871e2-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="871e2-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="871e2-154">Minimum supported client</span></span><br/> | <span data-ttu-id="871e2-155">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="871e2-155">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="871e2-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="871e2-156">Minimum supported server</span></span><br/> | <span data-ttu-id="871e2-157">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="871e2-157">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="871e2-158">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="871e2-158">End of client support</span></span><br/>    | <span data-ttu-id="871e2-159">Windows 7</span><span class="sxs-lookup"><span data-stu-id="871e2-159">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="871e2-160">Продукт</span><span class="sxs-lookup"><span data-stu-id="871e2-160">Product</span></span><br/>                  | <span data-ttu-id="871e2-161">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="871e2-161">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="871e2-162">Header</span><span class="sxs-lookup"><span data-stu-id="871e2-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="871e2-163"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="871e2-163"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="871e2-164">IID</span><span class="sxs-lookup"><span data-stu-id="871e2-164">IID</span></span><br/>                      | <span data-ttu-id="871e2-165">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="871e2-165">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="871e2-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="871e2-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="871e2-167">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="871e2-167">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

