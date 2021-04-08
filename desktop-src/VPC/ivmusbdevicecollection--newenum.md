---
title: Свойство _NewEnum Ивмусбдевицеколлектион (Впккоминтерфацес. h)
description: Возвращает перечислитель для коллекции. | Свойство _NewEnum Ивмусбдевицеколлектион (Впккоминтерфацес. h)
ms.assetid: f14f64a0-e65a-44d6-b053-54bbcb9ea804
keywords:
- _NewEnum свойств Virtual PC
- _NewEnum свойств Virtual PC, интерфейс Ивмусбдевицеколлектион
- Ивмусбдевицеколлектион интерфейс Virtual PC, свойство _NewEnum
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection._NewEnum
- IVMUSBDeviceCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e1e2a4d80691be26161ae4835ccb85c0e722d8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000284"
---
# <a name="ivmusbdevicecollection_newenum-property"></a><span data-ttu-id="eeda8-107">Свойство Ивмусбдевицеколлектион:: \_ NewEnum</span><span class="sxs-lookup"><span data-stu-id="eeda8-107">IVMUSBDeviceCollection::\_NewEnum property</span></span>

<span data-ttu-id="eeda8-108">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="eeda8-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="eeda8-109">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="eeda8-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="eeda8-110">Возвращает перечислитель для коллекции.</span><span class="sxs-lookup"><span data-stu-id="eeda8-110">Retrieves an enumerator for the collection.</span></span>

<span data-ttu-id="eeda8-111">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="eeda8-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeda8-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eeda8-112">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a><span data-ttu-id="eeda8-113">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="eeda8-113">Property value</span></span>

<span data-ttu-id="eeda8-114">Перечислитель [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="eeda8-114">The [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumerator.</span></span>

## <a name="error-codes"></a><span data-ttu-id="eeda8-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="eeda8-115">Error codes</span></span>



| <span data-ttu-id="eeda8-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="eeda8-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="eeda8-117">Значение</span><span class="sxs-lookup"><span data-stu-id="eeda8-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="eeda8-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="eeda8-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="eeda8-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="eeda8-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="eeda8-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="eeda8-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="eeda8-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="eeda8-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="eeda8-122"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="eeda8-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="eeda8-123">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="eeda8-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="eeda8-124">Требования</span><span class="sxs-lookup"><span data-stu-id="eeda8-124">Requirements</span></span>



| <span data-ttu-id="eeda8-125">Требование</span><span class="sxs-lookup"><span data-stu-id="eeda8-125">Requirement</span></span> | <span data-ttu-id="eeda8-126">Значение</span><span class="sxs-lookup"><span data-stu-id="eeda8-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeda8-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eeda8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="eeda8-128">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="eeda8-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eeda8-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eeda8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="eeda8-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="eeda8-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="eeda8-131">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="eeda8-131">End of client support</span></span><br/>    | <span data-ttu-id="eeda8-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="eeda8-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="eeda8-133">Продукт</span><span class="sxs-lookup"><span data-stu-id="eeda8-133">Product</span></span><br/>                  | <span data-ttu-id="eeda8-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="eeda8-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="eeda8-135">Header</span><span class="sxs-lookup"><span data-stu-id="eeda8-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="eeda8-136"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="eeda8-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="eeda8-137">IID</span><span class="sxs-lookup"><span data-stu-id="eeda8-137">IID</span></span><br/>                      | <span data-ttu-id="eeda8-138">IID \_ ивмусбдевицеколлектион определен как 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span><span class="sxs-lookup"><span data-stu-id="eeda8-138">IID\_IVMUSBDeviceCollection is defined as 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="eeda8-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eeda8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeda8-140">**ивмусбдевицеколлектион**</span><span class="sxs-lookup"><span data-stu-id="eeda8-140">**IVMUSBDeviceCollection**</span></span>](ivmusbdevicecollection.md)
</dt> </dl>

 

