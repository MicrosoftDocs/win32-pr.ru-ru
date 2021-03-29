---
title: Метод Ивмвиртуалпк Унрегистервиртуалмачине (Впккоминтерфацес. h)
description: Отменяет регистрацию конфигурации виртуальной машины, не удаляя файл конфигурации.
ms.assetid: 82ca6ef3-e9e5-471e-b2dc-0ff689a618d9
keywords:
- Метод Унрегистервиртуалмачине Virtual PC
- Метод Унрегистервиртуалмачине Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, метод Унрегистервиртуалмачине
topic_type:
- apiref
api_name:
- IVMVirtualPC.UnregisterVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d74380a822253918791b78bc34ac1c796f595ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492885"
---
# <a name="ivmvirtualpcunregistervirtualmachine-method"></a><span data-ttu-id="c5158-106">Метод Ивмвиртуалпк:: Унрегистервиртуалмачине</span><span class="sxs-lookup"><span data-stu-id="c5158-106">IVMVirtualPC::UnregisterVirtualMachine method</span></span>

<span data-ttu-id="c5158-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c5158-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c5158-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c5158-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c5158-109">Отмена регистрации конфигурации виртуальной машины без удаления файла конфигурации.</span><span class="sxs-lookup"><span data-stu-id="c5158-109">Unregisters a virtual machine (VM) configuration without deleting the configuration file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5158-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5158-110">Syntax</span></span>


```C++
HRESULT UnregisterVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="c5158-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="c5158-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5158-112">*virtualMachine* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c5158-112">*virtualMachine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5158-113">Указатель на объект [**ивмвиртуалмачине**](ivmvirtualmachine.md) , представляющий конфигурацию виртуальной машины, для которой необходимо отменить регистрацию.</span><span class="sxs-lookup"><span data-stu-id="c5158-113">A pointer to an [**IVMVirtualMachine**](ivmvirtualmachine.md) object that represents the VM configuration to be unregistered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5158-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c5158-114">Return value</span></span>

<span data-ttu-id="c5158-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="c5158-115">This method can return one of these values.</span></span>



| <span data-ttu-id="c5158-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="c5158-116">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="c5158-117">Описание</span><span class="sxs-lookup"><span data-stu-id="c5158-117">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c5158-118"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c5158-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="c5158-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c5158-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="c5158-120"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="c5158-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="c5158-121">Параметр *virtualMachine* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c5158-121">The *virtualMachine* parameter was **NULL**.</span></span><br/>                                         |
| <dl> <span data-ttu-id="c5158-122"><dt>**Виртуальная машина \_ \_Виртуальная машина E \_ с**</dt> <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="c5158-122"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                        | <span data-ttu-id="c5158-123">Виртуальная машина запущена.</span><span class="sxs-lookup"><span data-stu-id="c5158-123">The VM is running.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="c5158-124"><dt>**Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="c5158-124"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="c5158-125">Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).</span><span class="sxs-lookup"><span data-stu-id="c5158-125">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |
| <dl> <span data-ttu-id="c5158-126"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c5158-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="c5158-127">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="c5158-127">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="c5158-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c5158-128">Remarks</span></span>

<span data-ttu-id="c5158-129">Отменить регистрацию можно только для остановленных виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="c5158-129">Only stopped VMs can be unregistered.</span></span> <span data-ttu-id="c5158-130">Существующие данные о сохраненном состоянии или дисках отмены для этой конфигурации будут сохранены при отмене регистрации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c5158-130">Existing saved state or undo drive data for this configuration will be retained when a VM is unregistered.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5158-131">Требования</span><span class="sxs-lookup"><span data-stu-id="c5158-131">Requirements</span></span>



| <span data-ttu-id="c5158-132">Требование</span><span class="sxs-lookup"><span data-stu-id="c5158-132">Requirement</span></span> | <span data-ttu-id="c5158-133">Значение</span><span class="sxs-lookup"><span data-stu-id="c5158-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5158-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c5158-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c5158-135">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c5158-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c5158-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c5158-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c5158-137">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c5158-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c5158-138">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="c5158-138">End of client support</span></span><br/>    | <span data-ttu-id="c5158-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c5158-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c5158-140">Продукт</span><span class="sxs-lookup"><span data-stu-id="c5158-140">Product</span></span><br/>                  | <span data-ttu-id="c5158-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c5158-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c5158-142">Header</span><span class="sxs-lookup"><span data-stu-id="c5158-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5158-143"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5158-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c5158-144">IID</span><span class="sxs-lookup"><span data-stu-id="c5158-144">IID</span></span><br/>                      | <span data-ttu-id="c5158-145">IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="c5158-145">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="c5158-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c5158-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5158-147">**ивмвиртуалпк**</span><span class="sxs-lookup"><span data-stu-id="c5158-147">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

