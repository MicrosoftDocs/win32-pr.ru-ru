---
title: Свойство Has3DNow Ивмвиртуалмачине (Впккоминтерфацес. h)
description: Определяет, поддерживает ли процессор набор инструкций 3DNow. | Свойство Has3DNow Ивмвиртуалмачине (Впккоминтерфацес. h)
ms.assetid: 525ee7f0-081c-4f87-b2b7-ffec09f632c4
keywords:
- Has3DNow свойство Virtual PC
- Has3DNow свойство Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, свойство Has3DNow
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Has3DNow
- IVMVirtualMachine.get_Has3DNow
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b347fa802b999707e43019e9b7808c844c0288f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820836"
---
# <a name="ivmvirtualmachinehas3dnow-property"></a><span data-ttu-id="4a55d-107">Свойство Ивмвиртуалмачине:: Has3DNow</span><span class="sxs-lookup"><span data-stu-id="4a55d-107">IVMVirtualMachine::Has3DNow property</span></span>

<span data-ttu-id="4a55d-108">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4a55d-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4a55d-109">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4a55d-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4a55d-110">Определяет, поддерживает ли процессор набор инструкций 3DNow.</span><span class="sxs-lookup"><span data-stu-id="4a55d-110">Determines whether the processor supports the 3DNow instruction set.</span></span>

<span data-ttu-id="4a55d-111">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4a55d-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a55d-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a55d-112">Syntax</span></span>


```C++
HRESULT get_Has3DNow(
  [out, retval] VARIANT_BOOL *threeDNowEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="4a55d-113">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4a55d-113">Property value</span></span>

<span data-ttu-id="4a55d-114">**Значение true** , если процессор поддерживал набор инструкций 3DNow; в противном случае — **значение false** .</span><span class="sxs-lookup"><span data-stu-id="4a55d-114">**TRUE** if the processor supported the 3DNow instruction set, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4a55d-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="4a55d-115">Error codes</span></span>



| <span data-ttu-id="4a55d-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="4a55d-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="4a55d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="4a55d-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="4a55d-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4a55d-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="4a55d-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="4a55d-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="4a55d-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="4a55d-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="4a55d-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="4a55d-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="4a55d-122"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4a55d-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="4a55d-123">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="4a55d-123">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="4a55d-124"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4a55d-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="4a55d-125">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="4a55d-125">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4a55d-126">Требования</span><span class="sxs-lookup"><span data-stu-id="4a55d-126">Requirements</span></span>



| <span data-ttu-id="4a55d-127">Требование</span><span class="sxs-lookup"><span data-stu-id="4a55d-127">Requirement</span></span> | <span data-ttu-id="4a55d-128">Значение</span><span class="sxs-lookup"><span data-stu-id="4a55d-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a55d-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4a55d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4a55d-130">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4a55d-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4a55d-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4a55d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4a55d-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4a55d-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4a55d-133">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="4a55d-133">End of client support</span></span><br/>    | <span data-ttu-id="4a55d-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4a55d-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4a55d-135">Продукт</span><span class="sxs-lookup"><span data-stu-id="4a55d-135">Product</span></span><br/>                  | <span data-ttu-id="4a55d-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4a55d-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4a55d-137">Header</span><span class="sxs-lookup"><span data-stu-id="4a55d-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a55d-138"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a55d-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4a55d-139">IID</span><span class="sxs-lookup"><span data-stu-id="4a55d-139">IID</span></span><br/>                      | <span data-ttu-id="4a55d-140">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="4a55d-140">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="4a55d-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a55d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a55d-142">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="4a55d-142">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

