---
title: Свойство Максимумнумберофидебусес Ивмвиртуалпк (Впккоминтерфацес. h)
description: Возвращает максимальное число шин, разрешенное для интегрированной среды разработки.
ms.assetid: 7b88eda4-0f66-4e26-96cb-1e9ebef9d0b8
keywords:
- Максимумнумберофидебусес свойство Virtual PC
- Максимумнумберофидебусес свойство Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, свойство Максимумнумберофидебусес
topic_type:
- apiref
api_name:
- IVMVirtualPC.MaximumNumberOfIDEBuses
- IVMVirtualPC.get_MaximumNumberOfIDEBuses
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceabc071c0bf294eed3423d36c2c019586754101
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071056"
---
# <a name="ivmvirtualpcmaximumnumberofidebuses-property"></a><span data-ttu-id="2e97f-106">Свойство Ивмвиртуалпк:: Максимумнумберофидебусес</span><span class="sxs-lookup"><span data-stu-id="2e97f-106">IVMVirtualPC::MaximumNumberOfIDEBuses property</span></span>

<span data-ttu-id="2e97f-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2e97f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2e97f-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2e97f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2e97f-109">Возвращает максимальное число шин, разрешенное для интегрированной среды разработки.</span><span class="sxs-lookup"><span data-stu-id="2e97f-109">Retrieves the maximum number of buses allowed for IDE.</span></span>

<span data-ttu-id="2e97f-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="2e97f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e97f-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e97f-111">Syntax</span></span>


```C++
HRESULT get_MaximumNumberOfIDEBuses(
  [out, retval] long *maxNumBuses
);
```



## <a name="property-value"></a><span data-ttu-id="2e97f-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="2e97f-112">Property value</span></span>

<span data-ttu-id="2e97f-113">Максимальное число шин, разрешенное для интегрированной среды разработки.</span><span class="sxs-lookup"><span data-stu-id="2e97f-113">The maximum number of buses allowed for IDE.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2e97f-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="2e97f-114">Error codes</span></span>



| <span data-ttu-id="2e97f-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="2e97f-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="2e97f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="2e97f-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2e97f-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2e97f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="2e97f-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="2e97f-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="2e97f-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="2e97f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="2e97f-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2e97f-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="2e97f-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2e97f-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="2e97f-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="2e97f-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="2e97f-123"><dt>Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="2e97f-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="2e97f-124">Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).</span><span class="sxs-lookup"><span data-stu-id="2e97f-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="2e97f-125">Требования</span><span class="sxs-lookup"><span data-stu-id="2e97f-125">Requirements</span></span>



| <span data-ttu-id="2e97f-126">Требование</span><span class="sxs-lookup"><span data-stu-id="2e97f-126">Requirement</span></span> | <span data-ttu-id="2e97f-127">Значение</span><span class="sxs-lookup"><span data-stu-id="2e97f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e97f-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2e97f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2e97f-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2e97f-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2e97f-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2e97f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2e97f-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2e97f-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2e97f-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="2e97f-132">End of client support</span></span><br/>    | <span data-ttu-id="2e97f-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2e97f-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2e97f-134">Продукт</span><span class="sxs-lookup"><span data-stu-id="2e97f-134">Product</span></span><br/>                  | <span data-ttu-id="2e97f-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2e97f-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2e97f-136">Header</span><span class="sxs-lookup"><span data-stu-id="2e97f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e97f-137"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e97f-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2e97f-138">IID</span><span class="sxs-lookup"><span data-stu-id="2e97f-138">IID</span></span><br/>                      | <span data-ttu-id="2e97f-139">IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="2e97f-139">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="2e97f-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e97f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e97f-141">**ивмвиртуалпк**</span><span class="sxs-lookup"><span data-stu-id="2e97f-141">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

