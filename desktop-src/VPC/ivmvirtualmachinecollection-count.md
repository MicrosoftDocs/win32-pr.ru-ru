---
title: Свойство Ивмвиртуалмачинеколлектион Count (Впккоминтерфацес. h)
description: Извлекает число виртуальных машин в этой коллекции.
ms.assetid: c1f38528-fd9b-4b86-aac6-de944379b92e
keywords:
- Число свойств Virtual PC
- Число свойств Virtual PC, интерфейс Ивмвиртуалмачинеколлектион
- Ивмвиртуалмачинеколлектион интерфейс Virtual PC, свойство Count
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection.Count
- IVMVirtualMachineCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f641fad504c6dd593737cf35014813f49609a4aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137211"
---
# <a name="ivmvirtualmachinecollectioncount-property"></a><span data-ttu-id="59a31-106">Свойство Ивмвиртуалмачинеколлектион:: count</span><span class="sxs-lookup"><span data-stu-id="59a31-106">IVMVirtualMachineCollection::Count property</span></span>

<span data-ttu-id="59a31-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="59a31-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="59a31-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="59a31-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="59a31-109">Извлекает число виртуальных машин в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="59a31-109">Retrieves the number of virtual machines in this collection.</span></span>

<span data-ttu-id="59a31-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="59a31-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="59a31-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59a31-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="59a31-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="59a31-112">Property value</span></span>

<span data-ttu-id="59a31-113">Число виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="59a31-113">The number of virtual machines.</span></span>

## <a name="error-codes"></a><span data-ttu-id="59a31-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="59a31-114">Error codes</span></span>



| <span data-ttu-id="59a31-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="59a31-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="59a31-116">Значение</span><span class="sxs-lookup"><span data-stu-id="59a31-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="59a31-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="59a31-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="59a31-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="59a31-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="59a31-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="59a31-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="59a31-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="59a31-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="59a31-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="59a31-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="59a31-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="59a31-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="59a31-123">Требования</span><span class="sxs-lookup"><span data-stu-id="59a31-123">Requirements</span></span>



| <span data-ttu-id="59a31-124">Требование</span><span class="sxs-lookup"><span data-stu-id="59a31-124">Requirement</span></span> | <span data-ttu-id="59a31-125">Значение</span><span class="sxs-lookup"><span data-stu-id="59a31-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59a31-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="59a31-126">Minimum supported client</span></span><br/> | <span data-ttu-id="59a31-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="59a31-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="59a31-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="59a31-128">Minimum supported server</span></span><br/> | <span data-ttu-id="59a31-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="59a31-129">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="59a31-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="59a31-130">End of client support</span></span><br/>    | <span data-ttu-id="59a31-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="59a31-131">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="59a31-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="59a31-132">Product</span></span><br/>                  | <span data-ttu-id="59a31-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="59a31-133">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="59a31-134">Header</span><span class="sxs-lookup"><span data-stu-id="59a31-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="59a31-135"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="59a31-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="59a31-136">IID</span><span class="sxs-lookup"><span data-stu-id="59a31-136">IID</span></span><br/>                      | <span data-ttu-id="59a31-137">IID \_ ивмвиртуалмачинеколлектион определен как 59f31786-2a3d-4fbf-9896-d85338ca0da1</span><span class="sxs-lookup"><span data-stu-id="59a31-137">IID\_IVMVirtualMachineCollection is defined as 59f31786-2a3d-4fbf-9896-d85338ca0da1</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="59a31-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59a31-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59a31-139">**ивмвиртуалмачинеколлектион**</span><span class="sxs-lookup"><span data-stu-id="59a31-139">**IVMVirtualMachineCollection**</span></span>](ivmvirtualmachinecollection.md)
</dt> </dl>

 

