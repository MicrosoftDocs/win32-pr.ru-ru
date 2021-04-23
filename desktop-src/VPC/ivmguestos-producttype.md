---
title: Свойство Продукттипе Ивмгуестос (Впккоминтерфацес. h)
description: Возвращает тип продукта гостевой операционной системы, работающей на виртуальной машине.
ms.assetid: 426cd456-42a6-4bcd-a7a2-3aec258b02cb
keywords:
- Продукттипе свойство Virtual PC
- Продукттипе свойство Virtual PC, интерфейс Ивмгуестос
- Ивмгуестос интерфейс Virtual PC, свойство Продукттипе
topic_type:
- apiref
api_name:
- IVMGuestOS.ProductType
- IVMGuestOS.get_ProductType
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bc79ffd0717ac0949103a05d1bcdaa96da48d7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672651"
---
# <a name="ivmguestosproducttype-property"></a><span data-ttu-id="fd5fb-106">Ивмгуестос: свойство Родукттипе:P</span><span class="sxs-lookup"><span data-stu-id="fd5fb-106">IVMGuestOS::ProductType property</span></span>

<span data-ttu-id="fd5fb-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fd5fb-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fd5fb-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fd5fb-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fd5fb-109">Возвращает тип продукта гостевой операционной системы, работающей на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="fd5fb-109">Retrieves the product type of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="fd5fb-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="fd5fb-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd5fb-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd5fb-111">Syntax</span></span>


```C++
HRESULT get_ProductType(
  [out, retval] BSTR *productType
);
```



## <a name="property-value"></a><span data-ttu-id="fd5fb-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="fd5fb-112">Property value</span></span>

<span data-ttu-id="fd5fb-113">Тип продукта.</span><span class="sxs-lookup"><span data-stu-id="fd5fb-113">The product type.</span></span> <span data-ttu-id="fd5fb-114">Поддерживаются следующие строковые значения.</span><span class="sxs-lookup"><span data-stu-id="fd5fb-114">The following string values are supported.</span></span>



| <span data-ttu-id="fd5fb-115">Значение</span><span class="sxs-lookup"><span data-stu-id="fd5fb-115">Value</span></span>                                                                                  | <span data-ttu-id="fd5fb-116">Значение</span><span class="sxs-lookup"><span data-stu-id="fd5fb-116">Meaning</span></span>                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fd5fb-117"><dt>"0x0000002"</dt></span><span class="sxs-lookup"><span data-stu-id="fd5fb-117"><dt>"0x0000002"</dt></span></span> </dl> | <span data-ttu-id="fd5fb-118">Система является контроллером домена, а операционной системой является Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="fd5fb-118">The system is a domain controller and the operating system is Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003, or Windows 2000 Server.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="fd5fb-119"><dt>"0x0000003"</dt></span><span class="sxs-lookup"><span data-stu-id="fd5fb-119"><dt>"0x0000003"</dt></span></span> </dl> | <span data-ttu-id="fd5fb-120">Операционная система — Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="fd5fb-120">The operating system is Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003, or Windows 2000 Server.</span></span><br/> <span data-ttu-id="fd5fb-121">Обратите внимание, что сервер, который также является контроллером домена, сообщается как **\_ \_ \_ контроллер домена ver NT**, а не **\_ \_ сервер ver NT**.</span><span class="sxs-lookup"><span data-stu-id="fd5fb-121">Note that a server that is also a domain controller is reported as **VER\_NT\_DOMAIN\_CONTROLLER**, not **VER\_NT\_SERVER**.</span></span><br/> |
| <dl> <span data-ttu-id="fd5fb-122"><dt>"0x0000001"</dt></span><span class="sxs-lookup"><span data-stu-id="fd5fb-122"><dt>"0x0000001"</dt></span></span> </dl> | <span data-ttu-id="fd5fb-123">Операционная система — Windows 7, Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="fd5fb-123">The operating system is Windows 7, Windows Vista, Windows XP, or Windows 2000 Professional.</span></span><br/>                                                                                                                                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="fd5fb-124">Требования</span><span class="sxs-lookup"><span data-stu-id="fd5fb-124">Requirements</span></span>



| <span data-ttu-id="fd5fb-125">Требование</span><span class="sxs-lookup"><span data-stu-id="fd5fb-125">Requirement</span></span> | <span data-ttu-id="fd5fb-126">Значение</span><span class="sxs-lookup"><span data-stu-id="fd5fb-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd5fb-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fd5fb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fd5fb-128">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="fd5fb-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fd5fb-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fd5fb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fd5fb-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="fd5fb-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fd5fb-131">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="fd5fb-131">End of client support</span></span><br/>    | <span data-ttu-id="fd5fb-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fd5fb-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fd5fb-133">Продукт</span><span class="sxs-lookup"><span data-stu-id="fd5fb-133">Product</span></span><br/>                  | <span data-ttu-id="fd5fb-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fd5fb-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fd5fb-135">Header</span><span class="sxs-lookup"><span data-stu-id="fd5fb-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd5fb-136"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd5fb-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fd5fb-137">IID</span><span class="sxs-lookup"><span data-stu-id="fd5fb-137">IID</span></span><br/>                      | <span data-ttu-id="fd5fb-138">IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="fd5fb-138">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="fd5fb-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd5fb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd5fb-140">**ивмгуестос**</span><span class="sxs-lookup"><span data-stu-id="fd5fb-140">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

