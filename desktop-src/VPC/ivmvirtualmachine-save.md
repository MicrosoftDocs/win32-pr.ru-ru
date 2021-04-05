---
title: Метод Save (Впккоминтерфацес. h) Ивмвиртуалмачине
description: Сохраняет состояние виртуальной машины.
ms.assetid: e9f6e773-4e2d-4d7b-9624-e7864d5b248b
keywords:
- Сохранить метод Virtual PC
- Сохранение метода Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, метод Save
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Save
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27b4dbe18b89f107657d67fb7e7b90e024b01383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803311"
---
# <a name="ivmvirtualmachinesave-method"></a><span data-ttu-id="01b67-106">Метод Ивмвиртуалмачине:: Save</span><span class="sxs-lookup"><span data-stu-id="01b67-106">IVMVirtualMachine::Save method</span></span>

<span data-ttu-id="01b67-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="01b67-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="01b67-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="01b67-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="01b67-109">Сохраняет состояние виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="01b67-109">Saves the virtual machine (VM) state.</span></span>

## <a name="syntax"></a><span data-ttu-id="01b67-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01b67-110">Syntax</span></span>


```C++
HRESULT Save(
  [out, retval] IVMTask **saveTask
);
```



## <a name="parameters"></a><span data-ttu-id="01b67-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="01b67-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01b67-112">*саветаск* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="01b67-112">*saveTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="01b67-113">Объект [**ивмтаск**](ivmtask.md) , используемый для отслеживания хода выполнения последовательности сохранения состояния виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="01b67-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the VM's state saving sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01b67-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01b67-114">Return value</span></span>

<span data-ttu-id="01b67-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="01b67-115">This method can return one of these values.</span></span>



| <span data-ttu-id="01b67-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="01b67-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="01b67-117">Описание</span><span class="sxs-lookup"><span data-stu-id="01b67-117">Description</span></span>                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="01b67-118"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="01b67-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="01b67-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="01b67-119">The operation was successful.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="01b67-120"><dt>**Д \_ Сбой**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="01b67-120"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                                     | <span data-ttu-id="01b67-121">Не удалось сохранить виртуальную машину, так как диски отмены были помечены для удаления.</span><span class="sxs-lookup"><span data-stu-id="01b67-121">The VM could not be saved because the undo disks were marked for deletion.</span></span><br/>    |
| <dl> <span data-ttu-id="01b67-122"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="01b67-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="01b67-123">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="01b67-123">The parameter is **NULL**.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="01b67-124"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ \_ отказа в доступе)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="01b67-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="01b67-125">Вызывающий объект должен иметь разрешения на выполнение для сохранения состояния этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="01b67-125">The caller must have execute access permissions to save the state of this VM.</span></span><br/> |
| <dl> <span data-ttu-id="01b67-126"><dt>**Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="01b67-126"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="01b67-127">Виртуальная машина не запущена.</span><span class="sxs-lookup"><span data-stu-id="01b67-127">The VM is not running.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="01b67-128"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="01b67-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="01b67-129">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="01b67-129">An unexpected error has occurred.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="01b67-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01b67-130">Remarks</span></span>

<span data-ttu-id="01b67-131">Виртуальная машина будет отключена, когда задача **сохранения** достигнет завершения.</span><span class="sxs-lookup"><span data-stu-id="01b67-131">The VM is turned off when the **Save** task reaches completion.</span></span> <span data-ttu-id="01b67-132">В свойстве [**ивмвиртуалмачине:: State**](ivmvirtualmachine-state.md) будет содержаться **\_ Сохранение вмвмстате** во время сохранения, после чего **вмвмстате \_ сохраняется** после завершения сохранения и выключения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="01b67-132">The [**IVMVirtualMachine::State**](ivmvirtualmachine-state.md) property will contain **vmVMState\_Saving** while the save is in progress, followed by **vmVMState\_Saved** when the save has completed and the VM is turned off.</span></span>

## <a name="requirements"></a><span data-ttu-id="01b67-133">Требования</span><span class="sxs-lookup"><span data-stu-id="01b67-133">Requirements</span></span>



| <span data-ttu-id="01b67-134">Требование</span><span class="sxs-lookup"><span data-stu-id="01b67-134">Requirement</span></span> | <span data-ttu-id="01b67-135">Значение</span><span class="sxs-lookup"><span data-stu-id="01b67-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="01b67-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01b67-136">Minimum supported client</span></span><br/> | <span data-ttu-id="01b67-137">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="01b67-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="01b67-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01b67-138">Minimum supported server</span></span><br/> | <span data-ttu-id="01b67-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="01b67-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="01b67-140">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="01b67-140">End of client support</span></span><br/>    | <span data-ttu-id="01b67-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="01b67-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="01b67-142">Продукт</span><span class="sxs-lookup"><span data-stu-id="01b67-142">Product</span></span><br/>                  | <span data-ttu-id="01b67-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="01b67-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="01b67-144">Header</span><span class="sxs-lookup"><span data-stu-id="01b67-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="01b67-145"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="01b67-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="01b67-146">IID</span><span class="sxs-lookup"><span data-stu-id="01b67-146">IID</span></span><br/>                      | <span data-ttu-id="01b67-147">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="01b67-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="01b67-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01b67-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01b67-149">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="01b67-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

