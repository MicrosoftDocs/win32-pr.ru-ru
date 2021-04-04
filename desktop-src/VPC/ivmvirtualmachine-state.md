---
title: Свойство State Ивмвиртуалмачине (Впккоминтерфацес. h)
description: Извлекает текущее состояние виртуальной машины.
ms.assetid: a4214dfc-09d2-4d6b-a053-e75e99063411
keywords:
- Virtual PC свойства State
- Свойство состояния Virtual PC, интерфейс Ивмвиртуалмачине
- Интерфейс Ивмвиртуалмачине Virtual PC, свойство State
topic_type:
- apiref
api_name:
- IVMVirtualMachine.State
- IVMVirtualMachine.get_State
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11616f2a88b9238da11a4edec00c048e69885a07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989141"
---
# <a name="ivmvirtualmachinestate-property"></a><span data-ttu-id="56625-106">Свойство Ивмвиртуалмачине:: State</span><span class="sxs-lookup"><span data-stu-id="56625-106">IVMVirtualMachine::State property</span></span>

<span data-ttu-id="56625-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="56625-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="56625-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="56625-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="56625-109">Извлекает текущее состояние виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="56625-109">Retrieves the current state of the virtual machine.</span></span>

<span data-ttu-id="56625-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="56625-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="56625-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56625-111">Syntax</span></span>


```C++
HRESULT get_State(
  [out, retval] VMVMState *virtualMachineState
);
```



## <a name="property-value"></a><span data-ttu-id="56625-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="56625-112">Property value</span></span>

<span data-ttu-id="56625-113">Текущее состояние виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="56625-113">The current state of the virtual machine.</span></span> <span data-ttu-id="56625-114">Список значений см. в разделе [**вмвмстате**](vmvmstate.md).</span><span class="sxs-lookup"><span data-stu-id="56625-114">For a list of values, see [**VMVMState**](vmvmstate.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="56625-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="56625-115">Error codes</span></span>



| <span data-ttu-id="56625-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="56625-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="56625-117">Значение</span><span class="sxs-lookup"><span data-stu-id="56625-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="56625-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="56625-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="56625-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="56625-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="56625-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="56625-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="56625-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="56625-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="56625-122"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="56625-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="56625-123">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="56625-123">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="56625-124"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="56625-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="56625-125">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="56625-125">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="56625-126">Требования</span><span class="sxs-lookup"><span data-stu-id="56625-126">Requirements</span></span>



| <span data-ttu-id="56625-127">Требование</span><span class="sxs-lookup"><span data-stu-id="56625-127">Requirement</span></span> | <span data-ttu-id="56625-128">Значение</span><span class="sxs-lookup"><span data-stu-id="56625-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="56625-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="56625-129">Minimum supported client</span></span><br/> | <span data-ttu-id="56625-130">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="56625-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="56625-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="56625-131">Minimum supported server</span></span><br/> | <span data-ttu-id="56625-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="56625-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="56625-133">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="56625-133">End of client support</span></span><br/>    | <span data-ttu-id="56625-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="56625-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="56625-135">Продукт</span><span class="sxs-lookup"><span data-stu-id="56625-135">Product</span></span><br/>                  | <span data-ttu-id="56625-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="56625-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="56625-137">Header</span><span class="sxs-lookup"><span data-stu-id="56625-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="56625-138"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="56625-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="56625-139">IID</span><span class="sxs-lookup"><span data-stu-id="56625-139">IID</span></span><br/>                      | <span data-ttu-id="56625-140">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="56625-140">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="56625-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56625-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56625-142">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="56625-142">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

