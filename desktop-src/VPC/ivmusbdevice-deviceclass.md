---
title: Свойство Девицекласс Ивмусбдевице (Впккоминтерфацес. h)
description: Возвращает класс устройства USB-устройства.
ms.assetid: 46c258b9-6064-4e8c-aa5d-71b26c07351c
keywords:
- Девицекласс свойство Virtual PC
- Девицекласс свойство Virtual PC, интерфейс Ивмусбдевице
- Ивмусбдевице интерфейс Virtual PC, свойство Девицекласс
topic_type:
- apiref
api_name:
- IVMUSBDevice.DeviceClass
- IVMUSBDevice.get_DeviceClass
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b758092763c95c4443caeaca3f50be08e31c112c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415916"
---
# <a name="ivmusbdevicedeviceclass-property"></a><span data-ttu-id="50832-106">Ивмусбдевице: свойство Евицекласс:D</span><span class="sxs-lookup"><span data-stu-id="50832-106">IVMUSBDevice::DeviceClass property</span></span>

<span data-ttu-id="50832-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="50832-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="50832-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="50832-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="50832-109">Возвращает класс устройства USB-устройства.</span><span class="sxs-lookup"><span data-stu-id="50832-109">Retrieves the device class of the USB device.</span></span>

<span data-ttu-id="50832-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="50832-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="50832-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50832-111">Syntax</span></span>


```C++
HRESULT get_DeviceClass(
  [out, retval] VMUSBDeviceClassEnum *deviceClass
);
```



## <a name="property-value"></a><span data-ttu-id="50832-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="50832-112">Property value</span></span>

<span data-ttu-id="50832-113">Класс устройства.</span><span class="sxs-lookup"><span data-stu-id="50832-113">The device class.</span></span> <span data-ttu-id="50832-114">Список значений см. в разделе [**вмусбдевицеклассенум**](vmusbdeviceclassenum.md).</span><span class="sxs-lookup"><span data-stu-id="50832-114">For a list of values, see [**VMUSBDeviceClassEnum**](vmusbdeviceclassenum.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="50832-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="50832-115">Error codes</span></span>



| <span data-ttu-id="50832-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="50832-116">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="50832-117">Значение</span><span class="sxs-lookup"><span data-stu-id="50832-117">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="50832-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="50832-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="50832-119">Метод завершился успешно.</span><span class="sxs-lookup"><span data-stu-id="50832-119">The method completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="50832-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="50832-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="50832-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="50832-121">The parameter is **NULL**.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="50832-122">Требования</span><span class="sxs-lookup"><span data-stu-id="50832-122">Requirements</span></span>



| <span data-ttu-id="50832-123">Требование</span><span class="sxs-lookup"><span data-stu-id="50832-123">Requirement</span></span> | <span data-ttu-id="50832-124">Значение</span><span class="sxs-lookup"><span data-stu-id="50832-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="50832-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="50832-125">Minimum supported client</span></span><br/> | <span data-ttu-id="50832-126">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="50832-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="50832-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="50832-127">Minimum supported server</span></span><br/> | <span data-ttu-id="50832-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="50832-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="50832-129">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="50832-129">End of client support</span></span><br/>    | <span data-ttu-id="50832-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="50832-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="50832-131">Продукт</span><span class="sxs-lookup"><span data-stu-id="50832-131">Product</span></span><br/>                  | <span data-ttu-id="50832-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="50832-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="50832-133">Header</span><span class="sxs-lookup"><span data-stu-id="50832-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="50832-134"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="50832-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="50832-135">IID</span><span class="sxs-lookup"><span data-stu-id="50832-135">IID</span></span><br/>                      | <span data-ttu-id="50832-136">IID \_ ивмусбдевице определяется как 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="50832-136">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="50832-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50832-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50832-138">**ивмусбдевице**</span><span class="sxs-lookup"><span data-stu-id="50832-138">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

