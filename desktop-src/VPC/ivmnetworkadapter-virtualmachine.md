---
title: Свойство VirtualMachine Ивмнетворкадаптер (Впккоминтерфацес. h)
description: Извлекает виртуальную машину, связанную с этим сетевым интерфейсом.
ms.assetid: a3519041-0081-44e7-aa76-760d59ca8587
keywords:
- VirtualMachine свойство Virtual PC
- VirtualMachine свойство Virtual PC, интерфейс Ивмнетворкадаптер
- Ивмнетворкадаптер интерфейс Virtual PC, свойство VirtualMachine
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.VirtualMachine
- IVMNetworkAdapter.get_VirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea50e43bdcffcd16f668ef596a0f9db9d9bccfe2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071063"
---
# <a name="ivmnetworkadaptervirtualmachine-property"></a><span data-ttu-id="dd33c-106">Свойство Ивмнетворкадаптер:: VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="dd33c-106">IVMNetworkAdapter::VirtualMachine property</span></span>

<span data-ttu-id="dd33c-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="dd33c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="dd33c-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="dd33c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="dd33c-109">Извлекает виртуальную машину, связанную с этим сетевым интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="dd33c-109">Retrieves the virtual machine associated with this network interface.</span></span>

<span data-ttu-id="dd33c-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dd33c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd33c-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd33c-111">Syntax</span></span>


```C++
HRESULT get_VirtualMachine(
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="property-value"></a><span data-ttu-id="dd33c-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="dd33c-112">Property value</span></span>

<span data-ttu-id="dd33c-113">Интерфейс [**ивмвиртуалмачине**](ivmvirtualmachine.md) , представляющий виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="dd33c-113">An [**IVMVirtualMachine**](ivmvirtualmachine.md) interface that represents the virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="dd33c-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="dd33c-114">Error codes</span></span>



| <span data-ttu-id="dd33c-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="dd33c-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="dd33c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="dd33c-116">Meaning</span></span>                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="dd33c-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="dd33c-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="dd33c-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="dd33c-118">The operation was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="dd33c-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="dd33c-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="dd33c-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="dd33c-120">The parameter is **NULL**.</span></span><br/>           |
| <dl> <span data-ttu-id="dd33c-121"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="dd33c-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="dd33c-122">Не удается найти виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="dd33c-122">The virtual machine cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="dd33c-123"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="dd33c-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="dd33c-124">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="dd33c-124">An unexpected error has occurred.</span></span><br/>    |



## <a name="requirements"></a><span data-ttu-id="dd33c-125">Требования</span><span class="sxs-lookup"><span data-stu-id="dd33c-125">Requirements</span></span>



| <span data-ttu-id="dd33c-126">Требование</span><span class="sxs-lookup"><span data-stu-id="dd33c-126">Requirement</span></span> | <span data-ttu-id="dd33c-127">Значение</span><span class="sxs-lookup"><span data-stu-id="dd33c-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd33c-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd33c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="dd33c-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="dd33c-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dd33c-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd33c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="dd33c-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="dd33c-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="dd33c-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="dd33c-132">End of client support</span></span><br/>    | <span data-ttu-id="dd33c-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dd33c-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="dd33c-134">Продукт</span><span class="sxs-lookup"><span data-stu-id="dd33c-134">Product</span></span><br/>                  | <span data-ttu-id="dd33c-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="dd33c-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="dd33c-136">Header</span><span class="sxs-lookup"><span data-stu-id="dd33c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd33c-137"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd33c-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="dd33c-138">IID</span><span class="sxs-lookup"><span data-stu-id="dd33c-138">IID</span></span><br/>                      | <span data-ttu-id="dd33c-139">IID \_ ивмнетворкадаптер определен как e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="dd33c-139">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="dd33c-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd33c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd33c-141">**ивмнетворкадаптер**</span><span class="sxs-lookup"><span data-stu-id="dd33c-141">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

