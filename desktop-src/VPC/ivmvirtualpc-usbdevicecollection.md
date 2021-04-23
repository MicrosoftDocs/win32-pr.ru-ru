---
title: Свойство Усбдевицеколлектион Ивмвиртуалпк (Впккоминтерфацес. h)
description: Перечисляемая коллекция всех USB-устройств, подключенных к узлу.
ms.assetid: 80844912-15b1-44d1-8d07-dca90c579927
keywords:
- Усбдевицеколлектион свойство Virtual PC
- Усбдевицеколлектион свойство Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, свойство Усбдевицеколлектион
topic_type:
- apiref
api_name:
- IVMVirtualPC.USBDeviceCollection
- IVMVirtualPC.get_USBDeviceCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0428862cdd53ef6e657624d5dbd3e15c2445042f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802680"
---
# <a name="ivmvirtualpcusbdevicecollection-property"></a><span data-ttu-id="30576-106">Свойство Ивмвиртуалпк:: Усбдевицеколлектион</span><span class="sxs-lookup"><span data-stu-id="30576-106">IVMVirtualPC::USBDeviceCollection property</span></span>

<span data-ttu-id="30576-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="30576-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="30576-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="30576-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="30576-109">Возвращает перечисляемую коллекцию всех USB-устройств, подключенных к узлу.</span><span class="sxs-lookup"><span data-stu-id="30576-109">Retrieves an enumerable collection of all USB devices connected to the host.</span></span>

<span data-ttu-id="30576-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="30576-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="30576-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30576-111">Syntax</span></span>


```C++
HRESULT get_USBDeviceCollection(
  [out, retval] IVMUSBDeviceCollection **usbDeviceCollection
);
```



## <a name="property-value"></a><span data-ttu-id="30576-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="30576-112">Property value</span></span>

<span data-ttu-id="30576-113">Ссылка на указатель [**ивмусбдевицеколлектион**](ivmusbdevicecollection.md) , представляющий коллекцию объектов [**ивмусбдевице**](ivmusbdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="30576-113">A reference to an [**IVMUSBDeviceCollection**](ivmusbdevicecollection.md) pointer that represents a collection of [**IVMUSBDevice**](ivmusbdevice.md) objects.</span></span>

## <a name="error-codes"></a><span data-ttu-id="30576-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="30576-114">Error codes</span></span>



| <span data-ttu-id="30576-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="30576-115">Name/value</span></span>                                                                                                                                                                                | <span data-ttu-id="30576-116">Значение</span><span class="sxs-lookup"><span data-stu-id="30576-116">Meaning</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="30576-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="30576-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                   | <span data-ttu-id="30576-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="30576-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="30576-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="30576-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                     | <span data-ttu-id="30576-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="30576-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="30576-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="30576-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                             | <span data-ttu-id="30576-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="30576-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="30576-123"><dt>Виртуальная машина \_ \_ \_ Не удалось перечислить устройства E USB \_ \_ больше \_ устройств</dt> <dt>0xA0040930</dt></span><span class="sxs-lookup"><span data-stu-id="30576-123"><dt>VM\_E\_USB\_ENUMERATION\_FAILED\_MORE\_DEVICES</dt> <dt>0xA0040930</dt></span></span> </dl> | <span data-ttu-id="30576-124">К узлу подключено более 16 устройств USB.</span><span class="sxs-lookup"><span data-stu-id="30576-124">More than 16 USB devices are connected to the host.</span></span><br/>                                  |
| <dl> <span data-ttu-id="30576-125"><dt>Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="30576-125"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl>      | <span data-ttu-id="30576-126">Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).</span><span class="sxs-lookup"><span data-stu-id="30576-126">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="30576-127">Требования</span><span class="sxs-lookup"><span data-stu-id="30576-127">Requirements</span></span>



| <span data-ttu-id="30576-128">Требование</span><span class="sxs-lookup"><span data-stu-id="30576-128">Requirement</span></span> | <span data-ttu-id="30576-129">Значение</span><span class="sxs-lookup"><span data-stu-id="30576-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="30576-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="30576-130">Minimum supported client</span></span><br/> | <span data-ttu-id="30576-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="30576-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="30576-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="30576-132">Minimum supported server</span></span><br/> | <span data-ttu-id="30576-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="30576-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="30576-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="30576-134">End of client support</span></span><br/>    | <span data-ttu-id="30576-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="30576-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="30576-136">Продукт</span><span class="sxs-lookup"><span data-stu-id="30576-136">Product</span></span><br/>                  | <span data-ttu-id="30576-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="30576-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="30576-138">Header</span><span class="sxs-lookup"><span data-stu-id="30576-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="30576-139"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="30576-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="30576-140">IID</span><span class="sxs-lookup"><span data-stu-id="30576-140">IID</span></span><br/>                      | <span data-ttu-id="30576-141">IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="30576-141">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="30576-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30576-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30576-143">**ивмвиртуалпк**</span><span class="sxs-lookup"><span data-stu-id="30576-143">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

