---
title: Свойство адаптера Ивмвиртуалнетворк (Впккоминтерфацес. h)
description: Извлекает перечисляемую коллекцию сетевых адаптеров, подключенных к виртуальной сети.
ms.assetid: d5b95831-4642-441e-93e8-34e125087a43
keywords:
- Адаптера свойство Virtual PC
- Адаптера свойство Virtual PC, интерфейс Ивмвиртуалнетворк
- Ивмвиртуалнетворк интерфейс Virtual PC, свойство адаптера
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.NetworkAdapters
- IVMVirtualNetwork.get_NetworkAdapters
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ba86f649744eeb34139c65de9aa4523ddc74d1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691941"
---
# <a name="ivmvirtualnetworknetworkadapters-property"></a><span data-ttu-id="fd7f7-106">Свойство Ивмвиртуалнетворк:: адаптера</span><span class="sxs-lookup"><span data-stu-id="fd7f7-106">IVMVirtualNetwork::NetworkAdapters property</span></span>

<span data-ttu-id="fd7f7-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fd7f7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fd7f7-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fd7f7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fd7f7-109">Извлекает перечисляемую коллекцию сетевых адаптеров, подключенных к виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="fd7f7-109">Retrieves an enumerable collection of NICs attached to the virtual network.</span></span>

<span data-ttu-id="fd7f7-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="fd7f7-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd7f7-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd7f7-111">Syntax</span></span>


```C++
HRESULT get_NetworkAdapters(
  [out, retval] IVMNetworkAdapterCollection **networkInterfaceCollection
);
```



## <a name="property-value"></a><span data-ttu-id="fd7f7-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="fd7f7-112">Property value</span></span>

<span data-ttu-id="fd7f7-113">Новый [**ивмнетворкадаптерколлектион**](ivmnetworkadaptercollection.md) , содержащий виртуальные сетевые карты, подключенные к этой виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="fd7f7-113">A new [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md) which holds the virtual NICs attached to this virtual network.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fd7f7-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="fd7f7-114">Error codes</span></span>



| <span data-ttu-id="fd7f7-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="fd7f7-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="fd7f7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="fd7f7-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="fd7f7-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fd7f7-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="fd7f7-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="fd7f7-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="fd7f7-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="fd7f7-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="fd7f7-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="fd7f7-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="fd7f7-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="fd7f7-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="fd7f7-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="fd7f7-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="fd7f7-123">Требования</span><span class="sxs-lookup"><span data-stu-id="fd7f7-123">Requirements</span></span>



| <span data-ttu-id="fd7f7-124">Требование</span><span class="sxs-lookup"><span data-stu-id="fd7f7-124">Requirement</span></span> | <span data-ttu-id="fd7f7-125">Значение</span><span class="sxs-lookup"><span data-stu-id="fd7f7-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd7f7-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fd7f7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fd7f7-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="fd7f7-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fd7f7-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fd7f7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fd7f7-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="fd7f7-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fd7f7-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="fd7f7-130">End of client support</span></span><br/>    | <span data-ttu-id="fd7f7-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fd7f7-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fd7f7-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="fd7f7-132">Product</span></span><br/>                  | <span data-ttu-id="fd7f7-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fd7f7-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fd7f7-134">Header</span><span class="sxs-lookup"><span data-stu-id="fd7f7-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd7f7-135"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd7f7-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fd7f7-136">IID</span><span class="sxs-lookup"><span data-stu-id="fd7f7-136">IID</span></span><br/>                      | <span data-ttu-id="fd7f7-137">IID \_ ивмвиртуалнетворк определен как 431cb7a1-2469-4563-b94e-38b987adca63</span><span class="sxs-lookup"><span data-stu-id="fd7f7-137">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="fd7f7-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd7f7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd7f7-139">**ивмвиртуалнетворк**</span><span class="sxs-lookup"><span data-stu-id="fd7f7-139">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> </dl>

 

