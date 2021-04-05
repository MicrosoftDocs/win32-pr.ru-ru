---
title: Свойство Ивмвиртуалнетворкколлектион Count (Впккоминтерфацес. h)
description: Извлекает число виртуальных сетей в этой коллекции.
ms.assetid: a9a3ab48-74a0-498e-936e-a99c7b027a85
keywords:
- Число свойств Virtual PC
- Число свойств Virtual PC, интерфейс Ивмвиртуалнетворкколлектион
- Ивмвиртуалнетворкколлектион интерфейс Virtual PC, свойство Count
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection.Count
- IVMVirtualNetworkCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82e3244327d5840c8f7cce8ed498f90cd406d573
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803202"
---
# <a name="ivmvirtualnetworkcollectioncount-property"></a><span data-ttu-id="52ae1-106">Свойство Ивмвиртуалнетворкколлектион:: count</span><span class="sxs-lookup"><span data-stu-id="52ae1-106">IVMVirtualNetworkCollection::Count property</span></span>

<span data-ttu-id="52ae1-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="52ae1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="52ae1-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="52ae1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="52ae1-109">Извлекает число виртуальных сетей в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="52ae1-109">Retrieves the number of virtual networks in this collection.</span></span>

<span data-ttu-id="52ae1-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="52ae1-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="52ae1-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="52ae1-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="52ae1-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="52ae1-112">Property value</span></span>

<span data-ttu-id="52ae1-113">Число виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="52ae1-113">The number of virtual networks.</span></span>

## <a name="error-codes"></a><span data-ttu-id="52ae1-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="52ae1-114">Error codes</span></span>



| <span data-ttu-id="52ae1-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="52ae1-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="52ae1-116">Значение</span><span class="sxs-lookup"><span data-stu-id="52ae1-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="52ae1-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="52ae1-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="52ae1-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="52ae1-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="52ae1-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="52ae1-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="52ae1-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="52ae1-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="52ae1-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="52ae1-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="52ae1-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="52ae1-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="52ae1-123">Требования</span><span class="sxs-lookup"><span data-stu-id="52ae1-123">Requirements</span></span>



| <span data-ttu-id="52ae1-124">Требование</span><span class="sxs-lookup"><span data-stu-id="52ae1-124">Requirement</span></span> | <span data-ttu-id="52ae1-125">Значение</span><span class="sxs-lookup"><span data-stu-id="52ae1-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52ae1-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="52ae1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="52ae1-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="52ae1-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="52ae1-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="52ae1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="52ae1-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="52ae1-129">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="52ae1-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="52ae1-130">End of client support</span></span><br/>    | <span data-ttu-id="52ae1-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="52ae1-131">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="52ae1-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="52ae1-132">Product</span></span><br/>                  | <span data-ttu-id="52ae1-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="52ae1-133">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="52ae1-134">Header</span><span class="sxs-lookup"><span data-stu-id="52ae1-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="52ae1-135"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="52ae1-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="52ae1-136">IID</span><span class="sxs-lookup"><span data-stu-id="52ae1-136">IID</span></span><br/>                      | <span data-ttu-id="52ae1-137">IID \_ ивмвиртуалнетворкколлектион определен как 8ed680be-4242-4b2a-a21c-1982d8b0f675</span><span class="sxs-lookup"><span data-stu-id="52ae1-137">IID\_IVMVirtualNetworkCollection is defined as 8ed680be-4242-4b2a-a21c-1982d8b0f675</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="52ae1-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52ae1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52ae1-139">**ивмвиртуалнетворкколлектион**</span><span class="sxs-lookup"><span data-stu-id="52ae1-139">**IVMVirtualNetworkCollection**</span></span>](ivmvirtualnetworkcollection.md)
</dt> </dl>

 

