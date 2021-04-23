---
title: Метод Ивмвиртуалмачине Детачусбдевице (Впккоминтерфацес. h)
description: Выпускают USB-устройство из виртуальной машины.
ms.assetid: ae2b70b1-7bf3-4a84-9f05-4e91de93fa73
keywords:
- Метод Детачусбдевице Virtual PC
- Метод Детачусбдевице Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, метод Детачусбдевице
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DetachUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92f5a858c25822e9e9ba1a11686003b326133a59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691889"
---
# <a name="ivmvirtualmachinedetachusbdevice-method"></a><span data-ttu-id="a833e-106">Ивмвиртуалмачине: метод:D Етачусбдевице</span><span class="sxs-lookup"><span data-stu-id="a833e-106">IVMVirtualMachine::DetachUSBDevice method</span></span>

<span data-ttu-id="a833e-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a833e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a833e-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a833e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a833e-109">Выпускают USB-устройство из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a833e-109">Releases a USB device from a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="a833e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a833e-110">Syntax</span></span>


```C++
HRESULT DetachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a><span data-ttu-id="a833e-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="a833e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a833e-112">*инусбдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a833e-112">*inUSBDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a833e-113">Указатель [**ивмусбдевице**](ivmusbdevice.md) , представляющий USB-устройство для отсоединения от виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a833e-113">A [**IVMUSBDevice**](ivmusbdevice.md) pointer that represents the USB device to be detached from the virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a833e-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a833e-114">Return value</span></span>

<span data-ttu-id="a833e-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="a833e-115">This method can return one of these values.</span></span>



| <span data-ttu-id="a833e-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="a833e-116">Return code/value</span></span>                                                                                                                                                          | <span data-ttu-id="a833e-117">Описание</span><span class="sxs-lookup"><span data-stu-id="a833e-117">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="a833e-118"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a833e-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                | <span data-ttu-id="a833e-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a833e-119">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="a833e-120"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="a833e-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                  | <span data-ttu-id="a833e-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="a833e-121">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="a833e-122"><dt>**Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="a833e-122"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>     | <span data-ttu-id="a833e-123">Виртуальная машина не запущена.</span><span class="sxs-lookup"><span data-stu-id="a833e-123">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="a833e-124"><dt>**Виртуальная машина \_ \_ \_ \_ Не удалось отключить USB-**</dt> подключение <dt>0xA00400927</dt></span><span class="sxs-lookup"><span data-stu-id="a833e-124"><dt>**VM\_E\_USB\_DETACH\_FAILED**</dt> <dt>0xA00400927</dt></span></span> </dl> | <span data-ttu-id="a833e-125">Сбой операции отсоединения.</span><span class="sxs-lookup"><span data-stu-id="a833e-125">The detach operation failed.</span></span><br/>        |
| <dl> <span data-ttu-id="a833e-126"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a833e-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>          | <span data-ttu-id="a833e-127">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="a833e-127">An unexpected error has occurred.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="a833e-128">Требования</span><span class="sxs-lookup"><span data-stu-id="a833e-128">Requirements</span></span>



| <span data-ttu-id="a833e-129">Требование</span><span class="sxs-lookup"><span data-stu-id="a833e-129">Requirement</span></span> | <span data-ttu-id="a833e-130">Значение</span><span class="sxs-lookup"><span data-stu-id="a833e-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a833e-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a833e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a833e-132">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a833e-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a833e-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a833e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a833e-134">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a833e-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a833e-135">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="a833e-135">End of client support</span></span><br/>    | <span data-ttu-id="a833e-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a833e-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a833e-137">Продукт</span><span class="sxs-lookup"><span data-stu-id="a833e-137">Product</span></span><br/>                  | <span data-ttu-id="a833e-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a833e-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a833e-139">Header</span><span class="sxs-lookup"><span data-stu-id="a833e-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="a833e-140"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="a833e-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a833e-141">IID</span><span class="sxs-lookup"><span data-stu-id="a833e-141">IID</span></span><br/>                      | <span data-ttu-id="a833e-142">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="a833e-142">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="a833e-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a833e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a833e-144">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="a833e-144">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

