---
title: Свойство Item Ивмусбдевицеколлектион (Впккоминтерфацес. h)
description: Извлекает объект USB-устройства, соответствующий указанному индексу.
ms.assetid: 664a038e-7c86-43a9-a376-c913d431dc93
keywords:
- Свойство элемента Virtual PC
- Свойство элемента Virtual PC, интерфейс Ивмусбдевицеколлектион
- Интерфейс Ивмусбдевицеколлектион Virtual PC, свойство Item
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection.Item
- IVMUSBDeviceCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b50b96de6b19dab15852f58d78480b46da1e9ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490938"
---
# <a name="ivmusbdevicecollectionitem-property"></a><span data-ttu-id="abe3a-106">Свойство Ивмусбдевицеколлектион:: Item</span><span class="sxs-lookup"><span data-stu-id="abe3a-106">IVMUSBDeviceCollection::Item property</span></span>

<span data-ttu-id="abe3a-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="abe3a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="abe3a-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="abe3a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="abe3a-109">Извлекает объект USB-устройства, соответствующий указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="abe3a-109">Retrieves the USB device object that corresponds to the specified index.</span></span>

<span data-ttu-id="abe3a-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="abe3a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="abe3a-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="abe3a-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long         index,
  [out, retval] IVMUSBDevice **usbDevice
);
```



## <a name="property-value"></a><span data-ttu-id="abe3a-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="abe3a-112">Property value</span></span>

<span data-ttu-id="abe3a-113">Объект [**ивмусбдевице**](ivmusbdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="abe3a-113">The [**IVMUSBDevice**](ivmusbdevice.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="abe3a-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="abe3a-114">Error codes</span></span>



| <span data-ttu-id="abe3a-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="abe3a-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="abe3a-116">Значение</span><span class="sxs-lookup"><span data-stu-id="abe3a-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="abe3a-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="abe3a-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="abe3a-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="abe3a-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="abe3a-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="abe3a-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="abe3a-120">Параметр *усбдевице* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="abe3a-120">The *usbDevice* parameter is **NULL**.</span></span> <br/>                                             |
| <dl> <span data-ttu-id="abe3a-121"><dt> \_ E \_ бадиндекс</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="abe3a-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="abe3a-122">Индекс запрошенного элемента не соответствует элементу в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="abe3a-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="abe3a-123"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="abe3a-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="abe3a-124">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="abe3a-124">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="abe3a-125">Требования</span><span class="sxs-lookup"><span data-stu-id="abe3a-125">Requirements</span></span>



| <span data-ttu-id="abe3a-126">Требование</span><span class="sxs-lookup"><span data-stu-id="abe3a-126">Requirement</span></span> | <span data-ttu-id="abe3a-127">Значение</span><span class="sxs-lookup"><span data-stu-id="abe3a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="abe3a-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="abe3a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="abe3a-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="abe3a-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="abe3a-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="abe3a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="abe3a-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="abe3a-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="abe3a-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="abe3a-132">End of client support</span></span><br/>    | <span data-ttu-id="abe3a-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="abe3a-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="abe3a-134">Продукт</span><span class="sxs-lookup"><span data-stu-id="abe3a-134">Product</span></span><br/>                  | <span data-ttu-id="abe3a-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="abe3a-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="abe3a-136">Header</span><span class="sxs-lookup"><span data-stu-id="abe3a-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="abe3a-137"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="abe3a-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="abe3a-138">IID</span><span class="sxs-lookup"><span data-stu-id="abe3a-138">IID</span></span><br/>                      | <span data-ttu-id="abe3a-139">IID \_ ивмусбдевицеколлектион определен как 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span><span class="sxs-lookup"><span data-stu-id="abe3a-139">IID\_IVMUSBDeviceCollection is defined as 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="abe3a-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="abe3a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abe3a-141">**ивмусбдевице**</span><span class="sxs-lookup"><span data-stu-id="abe3a-141">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> <dt>

[<span data-ttu-id="abe3a-142">**ивмусбдевицеколлектион**</span><span class="sxs-lookup"><span data-stu-id="abe3a-142">**IVMUSBDeviceCollection**</span></span>](ivmusbdevicecollection.md)
</dt> </dl>

 

