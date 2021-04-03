---
title: Свойство Хасссе Ивмвиртуалмачине (Впккоминтерфацес. h)
description: Определяет, поддерживает ли процессор набор инструкций SSE. | Свойство Хасссе Ивмвиртуалмачине (Впккоминтерфацес. h)
ms.assetid: 949dd93b-aa4e-4506-91ed-ed625a535d5f
keywords:
- Хасссе свойство Virtual PC
- Хасссе свойство Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, свойство Хасссе
topic_type:
- apiref
api_name:
- IVMVirtualMachine.HasSSE
- IVMVirtualMachine.get_HasSSE
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a367ddc7b32ff4627976d2c5b63ec3565dbace53
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914640"
---
# <a name="ivmvirtualmachinehassse-property"></a><span data-ttu-id="b9280-107">Свойство Ивмвиртуалмачине:: Хасссе</span><span class="sxs-lookup"><span data-stu-id="b9280-107">IVMVirtualMachine::HasSSE property</span></span>

<span data-ttu-id="b9280-108">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b9280-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b9280-109">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b9280-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b9280-110">Определяет, поддерживает ли процессор набор инструкций SSE.</span><span class="sxs-lookup"><span data-stu-id="b9280-110">Determines whether the processor supports the SSE instruction set.</span></span>

<span data-ttu-id="b9280-111">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b9280-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9280-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b9280-112">Syntax</span></span>


```C++
HRESULT get_HasSSE(
  [out, retval] VARIANT_BOOL *sseEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="b9280-113">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b9280-113">Property value</span></span>

<span data-ttu-id="b9280-114">**Значение true** , если процессор поддерживал набор инструкций SSE; в противном случае — **значение false** .</span><span class="sxs-lookup"><span data-stu-id="b9280-114">**TRUE** if the processor supported the SSE instruction set, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b9280-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="b9280-115">Error codes</span></span>



| <span data-ttu-id="b9280-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="b9280-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="b9280-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b9280-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="b9280-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b9280-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="b9280-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="b9280-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="b9280-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="b9280-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="b9280-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b9280-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="b9280-122"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b9280-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="b9280-123">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="b9280-123">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="b9280-124"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b9280-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="b9280-125">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="b9280-125">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b9280-126">Требования</span><span class="sxs-lookup"><span data-stu-id="b9280-126">Requirements</span></span>



| <span data-ttu-id="b9280-127">Требование</span><span class="sxs-lookup"><span data-stu-id="b9280-127">Requirement</span></span> | <span data-ttu-id="b9280-128">Значение</span><span class="sxs-lookup"><span data-stu-id="b9280-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9280-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b9280-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b9280-130">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b9280-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b9280-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b9280-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b9280-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b9280-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b9280-133">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="b9280-133">End of client support</span></span><br/>    | <span data-ttu-id="b9280-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b9280-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b9280-135">Продукт</span><span class="sxs-lookup"><span data-stu-id="b9280-135">Product</span></span><br/>                  | <span data-ttu-id="b9280-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b9280-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b9280-137">Header</span><span class="sxs-lookup"><span data-stu-id="b9280-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9280-138"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9280-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b9280-139">IID</span><span class="sxs-lookup"><span data-stu-id="b9280-139">IID</span></span><br/>                      | <span data-ttu-id="b9280-140">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="b9280-140">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="b9280-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b9280-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9280-142">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="b9280-142">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

