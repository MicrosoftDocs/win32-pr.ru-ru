---
title: Свойство Девиценумбер Ивмдвддриве (Впккоминтерфацес. h)
description: Возвращает номер устройства, к которому подключен этот диск.
ms.assetid: 57b09400-e0c8-4ca2-bcd4-e6dd047daf95
keywords:
- Девиценумбер свойство Virtual PC
- Девиценумбер свойство Virtual PC, интерфейс Ивмдвддриве
- Ивмдвддриве интерфейс Virtual PC, свойство Девиценумбер
topic_type:
- apiref
api_name:
- IVMDVDDrive.DeviceNumber
- IVMDVDDrive.get_DeviceNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de189b162ed2c880819f4c8729e996236ace250a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071761"
---
# <a name="ivmdvddrivedevicenumber-property"></a><span data-ttu-id="16db3-106">Ивмдвддриве: свойство Евиценумбер:D</span><span class="sxs-lookup"><span data-stu-id="16db3-106">IVMDVDDrive::DeviceNumber property</span></span>

<span data-ttu-id="16db3-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="16db3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="16db3-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="16db3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="16db3-109">Возвращает номер устройства, к которому подключен этот диск.</span><span class="sxs-lookup"><span data-stu-id="16db3-109">Retrieves the device number to which this drive is attached.</span></span>

<span data-ttu-id="16db3-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="16db3-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="16db3-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16db3-111">Syntax</span></span>


```C++
HRESULT get_DeviceNumber(
  [out, retval] long *vmDeviceNumber
);
```



## <a name="property-value"></a><span data-ttu-id="16db3-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="16db3-112">Property value</span></span>

<span data-ttu-id="16db3-113">Номер устройства.</span><span class="sxs-lookup"><span data-stu-id="16db3-113">The device number.</span></span> <span data-ttu-id="16db3-114">Например, на шине IDE это значение будет представлять собой либо основное, либо дополнительное расположение.</span><span class="sxs-lookup"><span data-stu-id="16db3-114">For example, on an IDE bus, this value would represent either the primary or secondary location.</span></span>

## <a name="error-codes"></a><span data-ttu-id="16db3-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="16db3-115">Error codes</span></span>



| <span data-ttu-id="16db3-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="16db3-116">Name/value</span></span>                                                                                                                                                       | <span data-ttu-id="16db3-117">Значение</span><span class="sxs-lookup"><span data-stu-id="16db3-117">Meaning</span></span>                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="16db3-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="16db3-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="16db3-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="16db3-119">The operation was successful.</span></span><br/>                                          |
| <dl> <span data-ttu-id="16db3-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="16db3-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="16db3-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="16db3-121">The parameter is **NULL**.</span></span><br/>                                             |
| <dl> <span data-ttu-id="16db3-122"><dt>Виртуальная машина \_ \_Диск E \_ Недопустимый</dt> <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="16db3-122"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="16db3-123">Расположение шины для этого DVD-дисковода не инициализировано должным образом.</span><span class="sxs-lookup"><span data-stu-id="16db3-123">The bus location for this DVD drive has not been properly initialized.</span></span><br/> |
| <dl> <span data-ttu-id="16db3-124"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="16db3-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="16db3-125">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="16db3-125">An unexpected error has occurred.</span></span><br/>                                      |



## <a name="requirements"></a><span data-ttu-id="16db3-126">Требования</span><span class="sxs-lookup"><span data-stu-id="16db3-126">Requirements</span></span>



| <span data-ttu-id="16db3-127">Требование</span><span class="sxs-lookup"><span data-stu-id="16db3-127">Requirement</span></span> | <span data-ttu-id="16db3-128">Значение</span><span class="sxs-lookup"><span data-stu-id="16db3-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="16db3-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="16db3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="16db3-130">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="16db3-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="16db3-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="16db3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="16db3-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="16db3-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="16db3-133">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="16db3-133">End of client support</span></span><br/>    | <span data-ttu-id="16db3-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="16db3-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="16db3-135">Продукт</span><span class="sxs-lookup"><span data-stu-id="16db3-135">Product</span></span><br/>                  | <span data-ttu-id="16db3-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="16db3-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="16db3-137">Header</span><span class="sxs-lookup"><span data-stu-id="16db3-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="16db3-138"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="16db3-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="16db3-139">IID</span><span class="sxs-lookup"><span data-stu-id="16db3-139">IID</span></span><br/>                      | <span data-ttu-id="16db3-140">IID \_ ивмдвддриве определен как b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="16db3-140">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="16db3-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="16db3-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16db3-142">**ивмдвддриве**</span><span class="sxs-lookup"><span data-stu-id="16db3-142">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

