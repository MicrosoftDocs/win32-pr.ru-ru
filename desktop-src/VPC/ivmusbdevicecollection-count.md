---
title: Свойство Ивмусбдевицеколлектион Count (Впккоминтерфацес. h)
description: Возвращает число USB-устройств в этой коллекции.
ms.assetid: 8d17397b-4f4a-475d-99fe-4df0d74fe5a5
keywords:
- Число свойств Virtual PC
- Число свойств Virtual PC, интерфейс Ивмусбдевицеколлектион
- Ивмусбдевицеколлектион интерфейс Virtual PC, свойство Count
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection.Count
- IVMUSBDeviceCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5a0c2146df70f0432a19d65daad44ba6f1ec372
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490941"
---
# <a name="ivmusbdevicecollectioncount-property"></a><span data-ttu-id="97fd8-106">Свойство Ивмусбдевицеколлектион:: count</span><span class="sxs-lookup"><span data-stu-id="97fd8-106">IVMUSBDeviceCollection::Count property</span></span>

<span data-ttu-id="97fd8-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="97fd8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="97fd8-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="97fd8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="97fd8-109">Возвращает число USB-устройств в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="97fd8-109">Retrieves the number of USB devices in this collection.</span></span>

<span data-ttu-id="97fd8-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="97fd8-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="97fd8-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="97fd8-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="97fd8-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="97fd8-112">Property value</span></span>

<span data-ttu-id="97fd8-113">Число USB-устройств.</span><span class="sxs-lookup"><span data-stu-id="97fd8-113">The number of USB devices.</span></span>

## <a name="error-codes"></a><span data-ttu-id="97fd8-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="97fd8-114">Error codes</span></span>



| <span data-ttu-id="97fd8-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="97fd8-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="97fd8-116">Значение</span><span class="sxs-lookup"><span data-stu-id="97fd8-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="97fd8-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="97fd8-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="97fd8-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="97fd8-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="97fd8-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="97fd8-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="97fd8-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="97fd8-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="97fd8-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="97fd8-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="97fd8-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="97fd8-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="97fd8-123">Требования</span><span class="sxs-lookup"><span data-stu-id="97fd8-123">Requirements</span></span>



| <span data-ttu-id="97fd8-124">Требование</span><span class="sxs-lookup"><span data-stu-id="97fd8-124">Requirement</span></span> | <span data-ttu-id="97fd8-125">Значение</span><span class="sxs-lookup"><span data-stu-id="97fd8-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="97fd8-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97fd8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="97fd8-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="97fd8-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="97fd8-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97fd8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="97fd8-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="97fd8-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="97fd8-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="97fd8-130">End of client support</span></span><br/>    | <span data-ttu-id="97fd8-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="97fd8-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="97fd8-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="97fd8-132">Product</span></span><br/>                  | <span data-ttu-id="97fd8-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="97fd8-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="97fd8-134">Header</span><span class="sxs-lookup"><span data-stu-id="97fd8-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="97fd8-135"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="97fd8-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="97fd8-136">IID</span><span class="sxs-lookup"><span data-stu-id="97fd8-136">IID</span></span><br/>                      | <span data-ttu-id="97fd8-137">IID \_ ивмусбдевицеколлектион определен как 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span><span class="sxs-lookup"><span data-stu-id="97fd8-137">IID\_IVMUSBDeviceCollection is defined as 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="97fd8-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97fd8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97fd8-139">**ивмусбдевицеколлектион**</span><span class="sxs-lookup"><span data-stu-id="97fd8-139">**IVMUSBDeviceCollection**</span></span>](ivmusbdevicecollection.md)
</dt> </dl>

 

