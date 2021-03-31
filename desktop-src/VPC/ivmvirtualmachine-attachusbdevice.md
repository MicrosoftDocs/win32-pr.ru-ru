---
title: Метод Ивмвиртуалмачине Аттачусбдевице (Впккоминтерфацес. h)
description: Подключает USB-устройство к виртуальной машине.
ms.assetid: 505078ee-9159-407d-ab8c-a9aba86dec48
keywords:
- Метод Аттачусбдевице Virtual PC
- Метод Аттачусбдевице Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, метод Аттачусбдевице
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AttachUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3c36224823e4bd74b6a1c757816d55608e6d95a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071754"
---
# <a name="ivmvirtualmachineattachusbdevice-method"></a><span data-ttu-id="d77a2-106">Метод Ивмвиртуалмачине:: Аттачусбдевице</span><span class="sxs-lookup"><span data-stu-id="d77a2-106">IVMVirtualMachine::AttachUSBDevice method</span></span>

<span data-ttu-id="d77a2-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d77a2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d77a2-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d77a2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d77a2-109">Подключает USB-устройство к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="d77a2-109">Attaches a USB device to a virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="d77a2-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d77a2-110">Syntax</span></span>


```C++
HRESULT AttachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a><span data-ttu-id="d77a2-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="d77a2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d77a2-112">*инусбдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d77a2-112">*inUSBDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d77a2-113">Указатель [**ивмусбдевице**](ivmusbdevice.md) , представляющий USB-устройство, подключенное к узлу.</span><span class="sxs-lookup"><span data-stu-id="d77a2-113">A [**IVMUSBDevice**](ivmusbdevice.md) pointer that represents the USB device connected to the host.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d77a2-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d77a2-114">Return value</span></span>

<span data-ttu-id="d77a2-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="d77a2-115">This method can return one of these values.</span></span>



| <span data-ttu-id="d77a2-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="d77a2-116">Return code/value</span></span>                                                                                                                                                                             | <span data-ttu-id="d77a2-117">Описание</span><span class="sxs-lookup"><span data-stu-id="d77a2-117">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d77a2-118"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d77a2-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                   | <span data-ttu-id="d77a2-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d77a2-119">The operation was successful.</span></span><br/>                                           |
| <dl> <span data-ttu-id="d77a2-120"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="d77a2-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                     | <span data-ttu-id="d77a2-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="d77a2-121">The parameter is **NULL**.</span></span><br/>                                              |
| <dl> <span data-ttu-id="d77a2-122"><dt>**Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="d77a2-122"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                        | <span data-ttu-id="d77a2-123">Виртуальная машина не запущена.</span><span class="sxs-lookup"><span data-stu-id="d77a2-123">The VM is not running.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="d77a2-124"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d77a2-124"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                             | <span data-ttu-id="d77a2-125">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="d77a2-125">The configuration is unknown.</span></span><br/>                                           |
| <dl> <span data-ttu-id="d77a2-126"><dt>**Виртуальная машина \_ \_ \_ \_**</dt> <dt>Не0xA0040504ные</dt> дополнения</span><span class="sxs-lookup"><span data-stu-id="d77a2-126"><dt>**VM\_E\_ADDITIONS\_NOT\_AVAIL**</dt> <dt>0xA0040504</dt></span></span> </dl>                   | <span data-ttu-id="d77a2-127">Компоненты интеграции недоступны в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="d77a2-127">Integration Components are not available in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="d77a2-128"><dt>**Виртуальная машина \_ Добавление компонента "E" \_ \_ \_ не \_**</dt> доступно <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="d77a2-128"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>          | <span data-ttu-id="d77a2-129">Функция USB недоступна.</span><span class="sxs-lookup"><span data-stu-id="d77a2-129">The USB feature is not available.</span></span><br/>                                       |
| <dl> <span data-ttu-id="d77a2-130"><dt>**Виртуальная машина \_ \_ \_ \_ \_ Ошибка драйвера USB-соединителя E**</dt> <dt>0xA00400925</dt></span><span class="sxs-lookup"><span data-stu-id="d77a2-130"><dt>**VM\_E\_USB\_CONNECTOR\_DRIVER\_ERROR**</dt> <dt>0xA00400925</dt></span></span> </dl>          | <span data-ttu-id="d77a2-131">Произошла ошибка драйвера соединителя USB.</span><span class="sxs-lookup"><span data-stu-id="d77a2-131">There was a USB Connector driver error.</span></span><br/>                                 |
| <dl> <span data-ttu-id="d77a2-132"><dt>**Виртуальная машина \_ \_ \_ Не удалось подключить USB-подключение \_ \_ больше \_ устройств**</dt> <dt>0xA00400931</dt></span><span class="sxs-lookup"><span data-stu-id="d77a2-132"><dt>**VM\_E\_USB\_ATTACH\_FAILED\_MORE\_DEVICES**</dt> <dt>0xA00400931</dt></span></span> </dl>     | <span data-ttu-id="d77a2-133">Не удается подключить к виртуальной машине больше устройств.</span><span class="sxs-lookup"><span data-stu-id="d77a2-133">Cannot attach more devices to the VM.</span></span><br/>                                   |
| <dl> <span data-ttu-id="d77a2-134"><dt>**Виртуальная машина \_ E \_ USB \_ attach \_ Failed, \_ \_ Ошибка GP**</dt> <dt>0xA00400932</dt></span><span class="sxs-lookup"><span data-stu-id="d77a2-134"><dt>**VM\_E\_USB\_ATTACH\_FAILED\_GP\_ERROR**</dt> <dt>0xA00400932</dt></span></span> </dl>         | <span data-ttu-id="d77a2-135">Параметр групповой политики препятствует перенаправлению USB.</span><span class="sxs-lookup"><span data-stu-id="d77a2-135">A group policy setting is preventing the USB redirection.</span></span><br/>               |
| <dl> <span data-ttu-id="d77a2-136"><dt>**Виртуальная машина \_ \_ \_ Не удалось подключить USB-подключение \_ \_ уже \_ назначено**</dt> <dt>0xA00400933</dt></span><span class="sxs-lookup"><span data-stu-id="d77a2-136"><dt>**VM\_E\_USB\_ATTACH\_FAILED\_ALREADY\_ASSIGNED**</dt> <dt>0xA00400933</dt></span></span> </dl> | <span data-ttu-id="d77a2-137">USB-устройство уже подключено другим клиентом.</span><span class="sxs-lookup"><span data-stu-id="d77a2-137">A USB device has already been attached by some other client.</span></span><br/>            |
| <dl> <span data-ttu-id="d77a2-138"><dt>**Виртуальная машина \_ \_ \_ \_ Ошибка при подключении USB-подключения к порту E**</dt> <dt>0xA00400926</dt></span><span class="sxs-lookup"><span data-stu-id="d77a2-138"><dt>**VM\_E\_USB\_ATTACH\_FAILED**</dt> <dt>0xA00400926</dt></span></span> </dl>                    | <span data-ttu-id="d77a2-139">Не удалось выполнить операцию присоединения.</span><span class="sxs-lookup"><span data-stu-id="d77a2-139">The attach operation failed.</span></span><br/>                                            |
| <dl> <span data-ttu-id="d77a2-140"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d77a2-140"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                             | <span data-ttu-id="d77a2-141">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="d77a2-141">An unexpected error has occurred.</span></span><br/>                                       |



 

## <a name="requirements"></a><span data-ttu-id="d77a2-142">Требования</span><span class="sxs-lookup"><span data-stu-id="d77a2-142">Requirements</span></span>



| <span data-ttu-id="d77a2-143">Требование</span><span class="sxs-lookup"><span data-stu-id="d77a2-143">Requirement</span></span> | <span data-ttu-id="d77a2-144">Значение</span><span class="sxs-lookup"><span data-stu-id="d77a2-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d77a2-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d77a2-145">Minimum supported client</span></span><br/> | <span data-ttu-id="d77a2-146">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d77a2-146">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d77a2-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d77a2-147">Minimum supported server</span></span><br/> | <span data-ttu-id="d77a2-148">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d77a2-148">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d77a2-149">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d77a2-149">End of client support</span></span><br/>    | <span data-ttu-id="d77a2-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d77a2-150">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d77a2-151">Продукт</span><span class="sxs-lookup"><span data-stu-id="d77a2-151">Product</span></span><br/>                  | <span data-ttu-id="d77a2-152">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d77a2-152">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d77a2-153">Header</span><span class="sxs-lookup"><span data-stu-id="d77a2-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="d77a2-154"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="d77a2-154"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d77a2-155">IID</span><span class="sxs-lookup"><span data-stu-id="d77a2-155">IID</span></span><br/>                      | <span data-ttu-id="d77a2-156">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="d77a2-156">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="d77a2-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d77a2-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d77a2-158">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="d77a2-158">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

