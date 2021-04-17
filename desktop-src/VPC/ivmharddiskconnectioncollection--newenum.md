---
title: Свойство _NewEnum Ивмхарддискконнектионколлектион (Впккоминтерфацес. h)
description: Возвращает перечислитель для коллекции. | Свойство _NewEnum Ивмхарддискконнектионколлектион (Впккоминтерфацес. h)
ms.assetid: 9302f536-de25-4aac-88cf-9f4af6efcda7
keywords:
- _NewEnum свойств Virtual PC
- _NewEnum свойств Virtual PC, интерфейс Ивмхарддискконнектионколлектион
- Ивмхарддискконнектионколлектион интерфейс Virtual PC, свойство _NewEnum
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection._NewEnum
- IVMHardDiskConnectionCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66a6e8d5278b0aa164e2bc1ffd75b07a54300b45
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105693951"
---
# <a name="ivmharddiskconnectioncollection_newenum-property"></a><span data-ttu-id="679a8-107">Свойство Ивмхарддискконнектионколлектион:: \_ NewEnum</span><span class="sxs-lookup"><span data-stu-id="679a8-107">IVMHardDiskConnectionCollection::\_NewEnum property</span></span>

<span data-ttu-id="679a8-108">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="679a8-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="679a8-109">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="679a8-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="679a8-110">Возвращает перечислитель для коллекции.</span><span class="sxs-lookup"><span data-stu-id="679a8-110">Retrieves an enumerator for the collection.</span></span>

<span data-ttu-id="679a8-111">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="679a8-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="679a8-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="679a8-112">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a><span data-ttu-id="679a8-113">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="679a8-113">Property value</span></span>

<span data-ttu-id="679a8-114">Перечислитель [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="679a8-114">The [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumerator.</span></span>

## <a name="error-codes"></a><span data-ttu-id="679a8-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="679a8-115">Error codes</span></span>



| <span data-ttu-id="679a8-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="679a8-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="679a8-117">Значение</span><span class="sxs-lookup"><span data-stu-id="679a8-117">Meaning</span></span>                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="679a8-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="679a8-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="679a8-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="679a8-119">The operation was successful.</span></span><br/> |
| <dl> <span data-ttu-id="679a8-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="679a8-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="679a8-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="679a8-121">The parameter is **NULL**.</span></span><br/>    |
| <dl> <span data-ttu-id="679a8-122"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="679a8-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="679a8-123">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="679a8-123">An unexpected error occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="679a8-124">Требования</span><span class="sxs-lookup"><span data-stu-id="679a8-124">Requirements</span></span>



| <span data-ttu-id="679a8-125">Требование</span><span class="sxs-lookup"><span data-stu-id="679a8-125">Requirement</span></span> | <span data-ttu-id="679a8-126">Значение</span><span class="sxs-lookup"><span data-stu-id="679a8-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="679a8-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="679a8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="679a8-128">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="679a8-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="679a8-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="679a8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="679a8-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="679a8-130">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="679a8-131">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="679a8-131">End of client support</span></span><br/>    | <span data-ttu-id="679a8-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="679a8-132">Windows 7</span></span><br/>                                                                               |
| <span data-ttu-id="679a8-133">Продукт</span><span class="sxs-lookup"><span data-stu-id="679a8-133">Product</span></span><br/>                  | <span data-ttu-id="679a8-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="679a8-134">Windows Virtual PC</span></span><br/>                                                                      |
| <span data-ttu-id="679a8-135">Header</span><span class="sxs-lookup"><span data-stu-id="679a8-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="679a8-136"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="679a8-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>      |
| <span data-ttu-id="679a8-137">IID</span><span class="sxs-lookup"><span data-stu-id="679a8-137">IID</span></span><br/>                      | <span data-ttu-id="679a8-138">IID \_ ивмхарддискконнектионколлектион определен как b9f2caf4-0aeb-4085-B105-ceddb90dbf62</span><span class="sxs-lookup"><span data-stu-id="679a8-138">IID\_IVMHardDiskconnectionCollection is defined as b9f2caf4-0aeb-4085-b105-ceddb90dbf62</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="679a8-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="679a8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="679a8-140">**ивмхарддискконнектионколлектион**</span><span class="sxs-lookup"><span data-stu-id="679a8-140">**IVMHardDiskConnectionCollection**</span></span>](ivmharddiskconnectioncollection.md)
</dt> </dl>

 

