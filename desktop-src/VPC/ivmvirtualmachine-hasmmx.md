---
title: Свойство Хасммкс Ивмвиртуалмачине (Впккоминтерфацес. h)
description: Определяет, поддерживает ли процессор набор инструкций MMX. | Свойство Хасммкс Ивмвиртуалмачине (Впккоминтерфацес. h)
ms.assetid: 85350abe-ab44-42d2-9f3e-0fbdb64ff854
keywords:
- Хасммкс свойство Virtual PC
- Хасммкс свойство Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, свойство Хасммкс
topic_type:
- apiref
api_name:
- IVMVirtualMachine.HasMMX
- IVMVirtualMachine.get_HasMMX
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26e6b780d14749db193b2a7ce9a41083c6bf7031
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104081826"
---
# <a name="ivmvirtualmachinehasmmx-property"></a><span data-ttu-id="1d0f8-107">Свойство Ивмвиртуалмачине:: Хасммкс</span><span class="sxs-lookup"><span data-stu-id="1d0f8-107">IVMVirtualMachine::HasMMX property</span></span>

<span data-ttu-id="1d0f8-108">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1d0f8-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1d0f8-109">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1d0f8-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1d0f8-110">Определяет, поддерживает ли процессор набор инструкций MMX.</span><span class="sxs-lookup"><span data-stu-id="1d0f8-110">Determines whether the processor supports the MMX instruction set.</span></span>

<span data-ttu-id="1d0f8-111">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1d0f8-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d0f8-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d0f8-112">Syntax</span></span>


```C++
HRESULT get_HasMMX(
  [out, retval] VARIANT_BOOL *mmxEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="1d0f8-113">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1d0f8-113">Property value</span></span>

<span data-ttu-id="1d0f8-114">**Значение true** , если процессор поддерживал набор инструкций MMX; в противном случае — **значение false** .</span><span class="sxs-lookup"><span data-stu-id="1d0f8-114">**TRUE** if the processor supported the MMX instruction set, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1d0f8-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="1d0f8-115">Error codes</span></span>



| <span data-ttu-id="1d0f8-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="1d0f8-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="1d0f8-117">Значение</span><span class="sxs-lookup"><span data-stu-id="1d0f8-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="1d0f8-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1d0f8-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="1d0f8-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="1d0f8-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="1d0f8-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="1d0f8-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="1d0f8-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="1d0f8-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="1d0f8-122"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1d0f8-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="1d0f8-123">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="1d0f8-123">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="1d0f8-124"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="1d0f8-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="1d0f8-125">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="1d0f8-125">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="1d0f8-126">Требования</span><span class="sxs-lookup"><span data-stu-id="1d0f8-126">Requirements</span></span>



| <span data-ttu-id="1d0f8-127">Требование</span><span class="sxs-lookup"><span data-stu-id="1d0f8-127">Requirement</span></span> | <span data-ttu-id="1d0f8-128">Значение</span><span class="sxs-lookup"><span data-stu-id="1d0f8-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d0f8-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1d0f8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1d0f8-130">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1d0f8-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1d0f8-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1d0f8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1d0f8-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1d0f8-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1d0f8-133">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="1d0f8-133">End of client support</span></span><br/>    | <span data-ttu-id="1d0f8-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1d0f8-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1d0f8-135">Продукт</span><span class="sxs-lookup"><span data-stu-id="1d0f8-135">Product</span></span><br/>                  | <span data-ttu-id="1d0f8-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1d0f8-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1d0f8-137">Header</span><span class="sxs-lookup"><span data-stu-id="1d0f8-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d0f8-138"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d0f8-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1d0f8-139">IID</span><span class="sxs-lookup"><span data-stu-id="1d0f8-139">IID</span></span><br/>                      | <span data-ttu-id="1d0f8-140">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="1d0f8-140">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="1d0f8-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d0f8-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d0f8-142">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="1d0f8-142">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

