---
title: Свойство Ивмнетворкадаптерколлектион Count (Впккоминтерфацес. h)
description: Возвращает число сетевых интерфейсов в этой коллекции.
ms.assetid: 0b6391fa-62fe-4db1-b0a2-565ab17157ab
keywords:
- Число свойств Virtual PC
- Число свойств Virtual PC, интерфейс Ивмнетворкадаптерколлектион
- Ивмнетворкадаптерколлектион интерфейс Virtual PC, свойство Count
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection.Count
- IVMNetworkAdapterCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a287122d9829cd98f355d44e6bd408f6ca0d67a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135039"
---
# <a name="ivmnetworkadaptercollectioncount-property"></a><span data-ttu-id="2fc4d-106">Свойство Ивмнетворкадаптерколлектион:: count</span><span class="sxs-lookup"><span data-stu-id="2fc4d-106">IVMNetworkAdapterCollection::Count property</span></span>

<span data-ttu-id="2fc4d-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2fc4d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2fc4d-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2fc4d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2fc4d-109">Возвращает число сетевых интерфейсов в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="2fc4d-109">Retrieves the number of network interfaces in this collection.</span></span>

<span data-ttu-id="2fc4d-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="2fc4d-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fc4d-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2fc4d-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="2fc4d-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="2fc4d-112">Property value</span></span>

<span data-ttu-id="2fc4d-113">Число сетевых интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="2fc4d-113">The number of network interfaces.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2fc4d-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="2fc4d-114">Error codes</span></span>



| <span data-ttu-id="2fc4d-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="2fc4d-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="2fc4d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="2fc4d-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="2fc4d-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2fc4d-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="2fc4d-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="2fc4d-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="2fc4d-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="2fc4d-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="2fc4d-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2fc4d-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="2fc4d-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2fc4d-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="2fc4d-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="2fc4d-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="2fc4d-123">Требования</span><span class="sxs-lookup"><span data-stu-id="2fc4d-123">Requirements</span></span>



| <span data-ttu-id="2fc4d-124">Требование</span><span class="sxs-lookup"><span data-stu-id="2fc4d-124">Requirement</span></span> | <span data-ttu-id="2fc4d-125">Значение</span><span class="sxs-lookup"><span data-stu-id="2fc4d-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fc4d-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2fc4d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2fc4d-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2fc4d-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2fc4d-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2fc4d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2fc4d-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2fc4d-129">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2fc4d-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="2fc4d-130">End of client support</span></span><br/>    | <span data-ttu-id="2fc4d-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2fc4d-131">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="2fc4d-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="2fc4d-132">Product</span></span><br/>                  | <span data-ttu-id="2fc4d-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2fc4d-133">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="2fc4d-134">Header</span><span class="sxs-lookup"><span data-stu-id="2fc4d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fc4d-135"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fc4d-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="2fc4d-136">IID</span><span class="sxs-lookup"><span data-stu-id="2fc4d-136">IID</span></span><br/>                      | <span data-ttu-id="2fc4d-137">IID \_ ивмнетворкадаптерколлектион определен как ebaeafe9-EBCD-47cf-866e-ad87d735e479</span><span class="sxs-lookup"><span data-stu-id="2fc4d-137">IID\_IVMNetworkAdapterCollection is defined as ebaeafe9-ebcd-47cf-866e-ad87d735e479</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2fc4d-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2fc4d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fc4d-139">**ивмнетворкадаптерколлектион**</span><span class="sxs-lookup"><span data-stu-id="2fc4d-139">**IVMNetworkAdapterCollection**</span></span>](ivmnetworkadaptercollection.md)
</dt> </dl>

 

