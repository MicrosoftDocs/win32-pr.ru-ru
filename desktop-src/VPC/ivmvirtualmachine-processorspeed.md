---
title: Свойство ProcessorSpeed Ивмвиртуалмачине (Впккоминтерфацес. h)
description: Скорость процессора в мегагерцах (МГц) или ГГц.
ms.assetid: 465157a9-08ad-4636-b7c6-a188ff21e131
keywords:
- ProcessorSpeed свойство Virtual PC
- ProcessorSpeed свойство Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, свойство ProcessorSpeed
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ProcessorSpeed
- IVMVirtualMachine.get_ProcessorSpeed
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebaeb6f17e867d7618241b099b765ff450a2a4e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492567"
---
# <a name="ivmvirtualmachineprocessorspeed-property"></a><span data-ttu-id="b2aa3-106">Ивмвиртуалмачине: свойство Роцессорспид:P</span><span class="sxs-lookup"><span data-stu-id="b2aa3-106">IVMVirtualMachine::ProcessorSpeed property</span></span>

<span data-ttu-id="b2aa3-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b2aa3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b2aa3-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b2aa3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b2aa3-109">Возвращает скорость процессора в мегагерцах (МГц) или ГГц.</span><span class="sxs-lookup"><span data-stu-id="b2aa3-109">Retrieves the speed of the processor, in megahertz (MHz) or gigahertz (GHz).</span></span>

<span data-ttu-id="b2aa3-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b2aa3-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2aa3-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2aa3-111">Syntax</span></span>


```C++
HRESULT get_ProcessorSpeed(
  [out, retval] long *processorSpeed
);
```



## <a name="property-value"></a><span data-ttu-id="b2aa3-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b2aa3-112">Property value</span></span>

<span data-ttu-id="b2aa3-113">Скорость в мегагерцах или в ГГц.</span><span class="sxs-lookup"><span data-stu-id="b2aa3-113">The speed, in megahertz or gigahertz.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b2aa3-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="b2aa3-114">Error codes</span></span>



| <span data-ttu-id="b2aa3-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="b2aa3-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="b2aa3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b2aa3-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="b2aa3-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b2aa3-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="b2aa3-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="b2aa3-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="b2aa3-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="b2aa3-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="b2aa3-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b2aa3-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="b2aa3-121"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b2aa3-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="b2aa3-122">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="b2aa3-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="b2aa3-123"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b2aa3-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="b2aa3-124">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="b2aa3-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b2aa3-125">Требования</span><span class="sxs-lookup"><span data-stu-id="b2aa3-125">Requirements</span></span>



| <span data-ttu-id="b2aa3-126">Требование</span><span class="sxs-lookup"><span data-stu-id="b2aa3-126">Requirement</span></span> | <span data-ttu-id="b2aa3-127">Значение</span><span class="sxs-lookup"><span data-stu-id="b2aa3-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2aa3-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b2aa3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b2aa3-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b2aa3-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b2aa3-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b2aa3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b2aa3-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b2aa3-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b2aa3-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="b2aa3-132">End of client support</span></span><br/>    | <span data-ttu-id="b2aa3-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b2aa3-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b2aa3-134">Продукт</span><span class="sxs-lookup"><span data-stu-id="b2aa3-134">Product</span></span><br/>                  | <span data-ttu-id="b2aa3-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b2aa3-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b2aa3-136">Header</span><span class="sxs-lookup"><span data-stu-id="b2aa3-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2aa3-137"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2aa3-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b2aa3-138">IID</span><span class="sxs-lookup"><span data-stu-id="b2aa3-138">IID</span></span><br/>                      | <span data-ttu-id="b2aa3-139">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="b2aa3-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="b2aa3-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b2aa3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2aa3-141">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="b2aa3-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

