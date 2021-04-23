---
title: Свойство Ундоактион Ивмвиртуалмачине (Впккоминтерфацес. h)
description: Действие по умолчанию, выполняемое на всех дисках отмены после завершения работы виртуальной машины.
ms.assetid: fcdd5217-4909-435a-b11d-63578ab46e37
keywords:
- Ундоактион свойство Virtual PC
- Ундоактион свойство Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, свойство Ундоактион
topic_type:
- apiref
api_name:
- IVMVirtualMachine.UndoAction
- IVMVirtualMachine.get_UndoAction
- IVMVirtualMachine.put_UndoAction
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 039a9e65863e41ba2c7edc1befd2598aa16bb362
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492213"
---
# <a name="ivmvirtualmachineundoaction-property"></a><span data-ttu-id="70e0e-106">Свойство Ивмвиртуалмачине:: Ундоактион</span><span class="sxs-lookup"><span data-stu-id="70e0e-106">IVMVirtualMachine::UndoAction property</span></span>

<span data-ttu-id="70e0e-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="70e0e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="70e0e-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="70e0e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="70e0e-109">Извлекает и задает действие по умолчанию, выполняемое на всех дисках отмены, если виртуальная машина отключена с помощью метода [**турнофф**](ivmvirtualmachine-turnoff.md) или выключена с помощью метода [**Shutdown**](ivmguestos-shutdown.md) или отключена в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="70e0e-109">Retrieves and sets the default action to be performed on all undo drives when the virtual machine (VM) is turned off using the [**TurnOff**](ivmvirtualmachine-turnoff.md) method or shut down using the [**Shutdown**](ivmguestos-shutdown.md) method or turned off from within the guest operating system.</span></span>

<span data-ttu-id="70e0e-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="70e0e-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="70e0e-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="70e0e-111">Syntax</span></span>


```C++
HRESULT put_UndoAction(
  [in]          VMUndoAction undoAction
);

HRESULT get_UndoAction(
  [out, retval] VMUndoAction *undoAction
);
```



## <a name="property-value"></a><span data-ttu-id="70e0e-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="70e0e-112">Property value</span></span>

<span data-ttu-id="70e0e-113">Указывает действие по умолчанию, выполняемое на всех дисках отмены при завершении работы виртуальной машины в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="70e0e-113">Specifies the default action to be performed on all undo drives when the VM is shut down from within the guest operating system.</span></span> <span data-ttu-id="70e0e-114">Список значений см. в разделе [**вмундоактион**](vmundoaction.md).</span><span class="sxs-lookup"><span data-stu-id="70e0e-114">For a list of values, see [**VMUndoAction**](vmundoaction.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="70e0e-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="70e0e-115">Error codes</span></span>



| <span data-ttu-id="70e0e-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="70e0e-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="70e0e-117">Значение</span><span class="sxs-lookup"><span data-stu-id="70e0e-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="70e0e-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="70e0e-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="70e0e-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="70e0e-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="70e0e-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="70e0e-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="70e0e-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="70e0e-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="70e0e-122"><dt>Д \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="70e0e-122"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="70e0e-123">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="70e0e-123">The parameter is not valid.</span></span><br/>       |
| <dl> <span data-ttu-id="70e0e-124"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="70e0e-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="70e0e-125">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="70e0e-125">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="70e0e-126"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="70e0e-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="70e0e-127">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="70e0e-127">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="70e0e-128">Требования</span><span class="sxs-lookup"><span data-stu-id="70e0e-128">Requirements</span></span>



| <span data-ttu-id="70e0e-129">Требование</span><span class="sxs-lookup"><span data-stu-id="70e0e-129">Requirement</span></span> | <span data-ttu-id="70e0e-130">Значение</span><span class="sxs-lookup"><span data-stu-id="70e0e-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="70e0e-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="70e0e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="70e0e-132">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="70e0e-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="70e0e-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="70e0e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="70e0e-134">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="70e0e-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="70e0e-135">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="70e0e-135">End of client support</span></span><br/>    | <span data-ttu-id="70e0e-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="70e0e-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="70e0e-137">Продукт</span><span class="sxs-lookup"><span data-stu-id="70e0e-137">Product</span></span><br/>                  | <span data-ttu-id="70e0e-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="70e0e-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="70e0e-139">Header</span><span class="sxs-lookup"><span data-stu-id="70e0e-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="70e0e-140"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="70e0e-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="70e0e-141">IID</span><span class="sxs-lookup"><span data-stu-id="70e0e-141">IID</span></span><br/>                      | <span data-ttu-id="70e0e-142">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="70e0e-142">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="70e0e-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="70e0e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70e0e-144">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="70e0e-144">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

