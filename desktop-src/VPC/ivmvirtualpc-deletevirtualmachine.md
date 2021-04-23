---
title: Метод Ивмвиртуалпк Делетевиртуалмачине (Впккоминтерфацес. h)
description: Удаляет конфигурацию виртуальной машины.
ms.assetid: fc2562f3-6a83-4a40-b800-0bc2692beae8
keywords:
- Метод Делетевиртуалмачине Virtual PC
- Метод Делетевиртуалмачине Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, метод Делетевиртуалмачине
topic_type:
- apiref
api_name:
- IVMVirtualPC.DeleteVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee9c1591ccd736099fab04cce31c8a8b77b5fb06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691904"
---
# <a name="ivmvirtualpcdeletevirtualmachine-method"></a><span data-ttu-id="8e74c-106">Ивмвиртуалпк: метод:D Елетевиртуалмачине</span><span class="sxs-lookup"><span data-stu-id="8e74c-106">IVMVirtualPC::DeleteVirtualMachine method</span></span>

<span data-ttu-id="8e74c-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8e74c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8e74c-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8e74c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8e74c-109">Удаляет конфигурацию виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8e74c-109">Deletes a virtual machine configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e74c-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e74c-110">Syntax</span></span>


```C++
HRESULT DeleteVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="8e74c-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e74c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e74c-112">*virtualMachine* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8e74c-112">*virtualMachine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e74c-113">Указатель на объект [**ивмвиртуалмачине**](ivmvirtualmachine.md) , представляющий конфигурацию виртуальной машины, которую необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="8e74c-113">A pointer to an [**IVMVirtualMachine**](ivmvirtualmachine.md) object representing the virtual machine configuration to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e74c-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e74c-114">Return value</span></span>

<span data-ttu-id="8e74c-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="8e74c-115">This method can return one of these values.</span></span>



| <span data-ttu-id="8e74c-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="8e74c-116">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="8e74c-117">Описание</span><span class="sxs-lookup"><span data-stu-id="8e74c-117">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8e74c-118"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8e74c-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="8e74c-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="8e74c-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="8e74c-120"><dt>**С \_ ЛОЖЬ**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8e74c-120"><dt>**S\_FALSE**</dt> <dt>1</dt></span></span> </dl>                                           | <span data-ttu-id="8e74c-121">Не удалось найти указанную конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="8e74c-121">The specified configuration could not be found.</span></span><br/>                                      |
| <dl> <span data-ttu-id="8e74c-122"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="8e74c-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="8e74c-123">Параметр *virtualMachine* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="8e74c-123">The *virtualMachine* parameter was **NULL**.</span></span><br/>                                         |
| <dl> <span data-ttu-id="8e74c-124"><dt>**Виртуальная машина \_ \_Виртуальная машина E \_ с**</dt> <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="8e74c-124"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                        | <span data-ttu-id="8e74c-125">Виртуальная машина запущена.</span><span class="sxs-lookup"><span data-stu-id="8e74c-125">The virtual machine is running.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="8e74c-126"><dt>**Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="8e74c-126"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="8e74c-127">Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).</span><span class="sxs-lookup"><span data-stu-id="8e74c-127">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |
| <dl> <span data-ttu-id="8e74c-128"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="8e74c-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="8e74c-129">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="8e74c-129">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="8e74c-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8e74c-130">Remarks</span></span>

<span data-ttu-id="8e74c-131">Можно удалить только остановленные виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="8e74c-131">Only stopped virtual machines can be deleted.</span></span> <span data-ttu-id="8e74c-132">Обратите внимание, что все существующие данные о сохраненном состоянии или дисках отмены для этой конфигурации будут удалены в дополнение к файлу конфигурации.</span><span class="sxs-lookup"><span data-stu-id="8e74c-132">Note that any existing saved state or undo drive data for this configuration will be deleted in addition to the configuration file.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e74c-133">Требования</span><span class="sxs-lookup"><span data-stu-id="8e74c-133">Requirements</span></span>



| <span data-ttu-id="8e74c-134">Требование</span><span class="sxs-lookup"><span data-stu-id="8e74c-134">Requirement</span></span> | <span data-ttu-id="8e74c-135">Значение</span><span class="sxs-lookup"><span data-stu-id="8e74c-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e74c-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8e74c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8e74c-137">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8e74c-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8e74c-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8e74c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8e74c-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8e74c-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8e74c-140">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="8e74c-140">End of client support</span></span><br/>    | <span data-ttu-id="8e74c-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8e74c-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8e74c-142">Продукт</span><span class="sxs-lookup"><span data-stu-id="8e74c-142">Product</span></span><br/>                  | <span data-ttu-id="8e74c-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8e74c-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8e74c-144">Header</span><span class="sxs-lookup"><span data-stu-id="8e74c-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e74c-145"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e74c-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8e74c-146">IID</span><span class="sxs-lookup"><span data-stu-id="8e74c-146">IID</span></span><br/>                      | <span data-ttu-id="8e74c-147">IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="8e74c-147">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="8e74c-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e74c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e74c-149">**ивмвиртуалпк**</span><span class="sxs-lookup"><span data-stu-id="8e74c-149">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

