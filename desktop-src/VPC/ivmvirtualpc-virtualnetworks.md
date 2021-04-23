---
title: Свойство VirtualNetworks Ивмвиртуалпк (Впккоминтерфацес. h)
description: Извлекает перечисляемую коллекцию виртуальных сетей.
ms.assetid: 88c68178-0399-44cd-8145-1f2e4d6ac632
keywords:
- VirtualNetworks свойство Virtual PC
- VirtualNetworks свойство Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, свойство VirtualNetworks
topic_type:
- apiref
api_name:
- IVMVirtualPC.VirtualNetworks
- IVMVirtualPC.get_VirtualNetworks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf2ea97a7d9bb65bb41842ca028ded88f9a26b63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137670"
---
# <a name="ivmvirtualpcvirtualnetworks-property"></a><span data-ttu-id="7f1b5-106">Свойство Ивмвиртуалпк:: VirtualNetworks</span><span class="sxs-lookup"><span data-stu-id="7f1b5-106">IVMVirtualPC::VirtualNetworks property</span></span>

<span data-ttu-id="7f1b5-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7f1b5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7f1b5-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7f1b5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7f1b5-109">Извлекает перечисляемую коллекцию виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="7f1b5-109">Retrieves an enumerable collection of virtual networks.</span></span>

<span data-ttu-id="7f1b5-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7f1b5-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f1b5-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f1b5-111">Syntax</span></span>


```C++
HRESULT get_VirtualNetworks(
  [out, retval] IVMVirtualNetworkCollection **virtualNetworkCollection
);
```



## <a name="property-value"></a><span data-ttu-id="7f1b5-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7f1b5-112">Property value</span></span>

<span data-ttu-id="7f1b5-113">Коллекция объектов [**ивмвиртуалнетворк**](ivmvirtualnetwork.md) .</span><span class="sxs-lookup"><span data-stu-id="7f1b5-113">A collection of [**IVMVirtualNetwork**](ivmvirtualnetwork.md) objects.</span></span> <span data-ttu-id="7f1b5-114">См. [**ивмвиртуалнетворкколлектион**](ivmvirtualnetworkcollection.md).</span><span class="sxs-lookup"><span data-stu-id="7f1b5-114">See [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="7f1b5-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="7f1b5-115">Error codes</span></span>



| <span data-ttu-id="7f1b5-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="7f1b5-116">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="7f1b5-117">Значение</span><span class="sxs-lookup"><span data-stu-id="7f1b5-117">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7f1b5-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7f1b5-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="7f1b5-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="7f1b5-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="7f1b5-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="7f1b5-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="7f1b5-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="7f1b5-121">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="7f1b5-122"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="7f1b5-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="7f1b5-123">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="7f1b5-123">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="7f1b5-124"><dt>Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="7f1b5-124"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="7f1b5-125">Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).</span><span class="sxs-lookup"><span data-stu-id="7f1b5-125">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7f1b5-126">Требования</span><span class="sxs-lookup"><span data-stu-id="7f1b5-126">Requirements</span></span>



| <span data-ttu-id="7f1b5-127">Требование</span><span class="sxs-lookup"><span data-stu-id="7f1b5-127">Requirement</span></span> | <span data-ttu-id="7f1b5-128">Значение</span><span class="sxs-lookup"><span data-stu-id="7f1b5-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f1b5-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7f1b5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7f1b5-130">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7f1b5-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7f1b5-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7f1b5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7f1b5-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7f1b5-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7f1b5-133">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="7f1b5-133">End of client support</span></span><br/>    | <span data-ttu-id="7f1b5-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7f1b5-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7f1b5-135">Продукт</span><span class="sxs-lookup"><span data-stu-id="7f1b5-135">Product</span></span><br/>                  | <span data-ttu-id="7f1b5-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7f1b5-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7f1b5-137">Header</span><span class="sxs-lookup"><span data-stu-id="7f1b5-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f1b5-138"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f1b5-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7f1b5-139">IID</span><span class="sxs-lookup"><span data-stu-id="7f1b5-139">IID</span></span><br/>                      | <span data-ttu-id="7f1b5-140">IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="7f1b5-140">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="7f1b5-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f1b5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f1b5-142">**ивмвиртуалпк**</span><span class="sxs-lookup"><span data-stu-id="7f1b5-142">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

