---
title: Свойство адаптера Ивмвиртуалмачине (Впккоминтерфацес. h)
description: Извлекает перечисляемую коллекцию сетевых адаптеров, подключенных к виртуальной машине.
ms.assetid: 3877edf7-92b8-43c9-8229-a198a07079a4
keywords:
- Адаптера свойство Virtual PC
- Адаптера свойство Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, свойство адаптера
topic_type:
- apiref
api_name:
- IVMVirtualMachine.NetworkAdapters
- IVMVirtualMachine.get_NetworkAdapters
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9ce6e1fa22eca40c037eebb48803fe182810c38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415672"
---
# <a name="ivmvirtualmachinenetworkadapters-property"></a><span data-ttu-id="6d679-106">Свойство Ивмвиртуалмачине:: адаптера</span><span class="sxs-lookup"><span data-stu-id="6d679-106">IVMVirtualMachine::NetworkAdapters property</span></span>

<span data-ttu-id="6d679-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6d679-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6d679-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6d679-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6d679-109">Извлекает перечисляемую коллекцию сетевых адаптеров, подключенных к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="6d679-109">Retrieves an enumerable collection of NICs attached to the virtual machine.</span></span>

<span data-ttu-id="6d679-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6d679-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d679-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d679-111">Syntax</span></span>


```C++
HRESULT get_NetworkAdapters(
  [out, retval] IVMNetworkAdapterCollection **networkAdapterCollection
);
```



## <a name="property-value"></a><span data-ttu-id="6d679-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6d679-112">Property value</span></span>

<span data-ttu-id="6d679-113">Объект [**ивмнетворкадаптерколлектион**](ivmnetworkadaptercollection.md) .</span><span class="sxs-lookup"><span data-stu-id="6d679-113">An [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6d679-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="6d679-114">Error codes</span></span>



| <span data-ttu-id="6d679-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="6d679-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="6d679-116">Значение</span><span class="sxs-lookup"><span data-stu-id="6d679-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="6d679-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6d679-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="6d679-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="6d679-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="6d679-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="6d679-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="6d679-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="6d679-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="6d679-121"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="6d679-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="6d679-122">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="6d679-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="6d679-123"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="6d679-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="6d679-124">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="6d679-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="6d679-125">Требования</span><span class="sxs-lookup"><span data-stu-id="6d679-125">Requirements</span></span>



| <span data-ttu-id="6d679-126">Требование</span><span class="sxs-lookup"><span data-stu-id="6d679-126">Requirement</span></span> | <span data-ttu-id="6d679-127">Значение</span><span class="sxs-lookup"><span data-stu-id="6d679-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d679-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6d679-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6d679-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6d679-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6d679-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6d679-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6d679-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6d679-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6d679-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="6d679-132">End of client support</span></span><br/>    | <span data-ttu-id="6d679-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6d679-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6d679-134">Продукт</span><span class="sxs-lookup"><span data-stu-id="6d679-134">Product</span></span><br/>                  | <span data-ttu-id="6d679-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6d679-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6d679-136">Header</span><span class="sxs-lookup"><span data-stu-id="6d679-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d679-137"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d679-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6d679-138">IID</span><span class="sxs-lookup"><span data-stu-id="6d679-138">IID</span></span><br/>                      | <span data-ttu-id="6d679-139">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="6d679-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="6d679-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d679-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d679-141">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="6d679-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

