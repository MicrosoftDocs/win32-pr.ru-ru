---
title: Свойство Девицестринг Ивмусбдевице (Впккоминтерфацес. h)
description: Возвращает имя USB-устройства.
ms.assetid: 2ae82e2a-b33a-4039-acdb-958b094b1045
keywords:
- Девицестринг свойство Virtual PC
- Девицестринг свойство Virtual PC, интерфейс Ивмусбдевице
- Ивмусбдевице интерфейс Virtual PC, свойство Девицестринг
topic_type:
- apiref
api_name:
- IVMUSBDevice.DeviceString
- IVMUSBDevice.get_DeviceString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88ed76f55f5b1218db70991f5917edf6d5b7b655
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892041"
---
# <a name="ivmusbdevicedevicestring-property"></a><span data-ttu-id="de1a6-106">Ивмусбдевице: свойство Евицестринг:D</span><span class="sxs-lookup"><span data-stu-id="de1a6-106">IVMUSBDevice::DeviceString property</span></span>

<span data-ttu-id="de1a6-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="de1a6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="de1a6-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="de1a6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="de1a6-109">Возвращает имя USB-устройства.</span><span class="sxs-lookup"><span data-stu-id="de1a6-109">Retrieves the name of the USB device.</span></span>

<span data-ttu-id="de1a6-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="de1a6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="de1a6-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de1a6-111">Syntax</span></span>


```C++
HRESULT get_DeviceString(
  [out, retval] BSTR *deviceName
);
```



## <a name="property-value"></a><span data-ttu-id="de1a6-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="de1a6-112">Property value</span></span>

<span data-ttu-id="de1a6-113">Имя USB-устройства.</span><span class="sxs-lookup"><span data-stu-id="de1a6-113">The name of the USB device.</span></span>

## <a name="error-codes"></a><span data-ttu-id="de1a6-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="de1a6-114">Error codes</span></span>



| <span data-ttu-id="de1a6-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="de1a6-115">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="de1a6-116">Значение</span><span class="sxs-lookup"><span data-stu-id="de1a6-116">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="de1a6-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="de1a6-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="de1a6-118">Метод завершился успешно.</span><span class="sxs-lookup"><span data-stu-id="de1a6-118">The method completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="de1a6-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="de1a6-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="de1a6-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="de1a6-120">The parameter is **NULL**.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="de1a6-121">Требования</span><span class="sxs-lookup"><span data-stu-id="de1a6-121">Requirements</span></span>



| <span data-ttu-id="de1a6-122">Требование</span><span class="sxs-lookup"><span data-stu-id="de1a6-122">Requirement</span></span> | <span data-ttu-id="de1a6-123">Значение</span><span class="sxs-lookup"><span data-stu-id="de1a6-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="de1a6-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="de1a6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="de1a6-125">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="de1a6-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="de1a6-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="de1a6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="de1a6-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="de1a6-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="de1a6-128">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="de1a6-128">End of client support</span></span><br/>    | <span data-ttu-id="de1a6-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="de1a6-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="de1a6-130">Продукт</span><span class="sxs-lookup"><span data-stu-id="de1a6-130">Product</span></span><br/>                  | <span data-ttu-id="de1a6-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="de1a6-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="de1a6-132">Header</span><span class="sxs-lookup"><span data-stu-id="de1a6-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="de1a6-133"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="de1a6-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="de1a6-134">IID</span><span class="sxs-lookup"><span data-stu-id="de1a6-134">IID</span></span><br/>                      | <span data-ttu-id="de1a6-135">IID \_ ивмусбдевице определяется как 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="de1a6-135">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="de1a6-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de1a6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de1a6-137">**ивмусбдевице**</span><span class="sxs-lookup"><span data-stu-id="de1a6-137">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

