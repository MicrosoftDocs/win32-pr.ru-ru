---
title: Свойство Минимуммеморипервм Ивмвиртуалпк (Впккоминтерфацес. h)
description: Возвращает минимально допустимое количество физической памяти на одну виртуальную машину в мегабайтах.
ms.assetid: 3e7757cd-df45-4b30-9a38-6cfca0ee631a
keywords:
- Минимуммеморипервм свойство Virtual PC
- Минимуммеморипервм свойство Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, свойство Минимуммеморипервм
topic_type:
- apiref
api_name:
- IVMVirtualPC.MinimumMemoryPerVM
- IVMVirtualPC.get_MinimumMemoryPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 068e083bd788c7bc51a45b7dd556107da13196ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135022"
---
# <a name="ivmvirtualpcminimummemorypervm-property"></a><span data-ttu-id="881b6-106">Свойство Ивмвиртуалпк:: Минимуммеморипервм</span><span class="sxs-lookup"><span data-stu-id="881b6-106">IVMVirtualPC::MinimumMemoryPerVM property</span></span>

<span data-ttu-id="881b6-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="881b6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="881b6-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="881b6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="881b6-109">Возвращает минимально допустимое количество физической памяти на одну виртуальную машину в мегабайтах.</span><span class="sxs-lookup"><span data-stu-id="881b6-109">Retrieves the minimum allowable quantity of physical memory per virtual machine, in megabytes.</span></span>

<span data-ttu-id="881b6-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="881b6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="881b6-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="881b6-111">Syntax</span></span>


```C++
HRESULT get_MinimumMemoryPerVM(
  [out, retval] long *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="881b6-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="881b6-112">Property value</span></span>

<span data-ttu-id="881b6-113">Минимальное допустимое количество (в мегабайтах) физической памяти на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="881b6-113">The minimum allowable quantity, in megabytes, of physical memory per virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="881b6-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="881b6-114">Error codes</span></span>



| <span data-ttu-id="881b6-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="881b6-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="881b6-116">Значение</span><span class="sxs-lookup"><span data-stu-id="881b6-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="881b6-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="881b6-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="881b6-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="881b6-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="881b6-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="881b6-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="881b6-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="881b6-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="881b6-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="881b6-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="881b6-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="881b6-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="881b6-123"><dt>Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="881b6-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="881b6-124">Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).</span><span class="sxs-lookup"><span data-stu-id="881b6-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="881b6-125">Требования</span><span class="sxs-lookup"><span data-stu-id="881b6-125">Requirements</span></span>



| <span data-ttu-id="881b6-126">Требование</span><span class="sxs-lookup"><span data-stu-id="881b6-126">Requirement</span></span> | <span data-ttu-id="881b6-127">Значение</span><span class="sxs-lookup"><span data-stu-id="881b6-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="881b6-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="881b6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="881b6-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="881b6-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="881b6-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="881b6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="881b6-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="881b6-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="881b6-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="881b6-132">End of client support</span></span><br/>    | <span data-ttu-id="881b6-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="881b6-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="881b6-134">Продукт</span><span class="sxs-lookup"><span data-stu-id="881b6-134">Product</span></span><br/>                  | <span data-ttu-id="881b6-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="881b6-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="881b6-136">Header</span><span class="sxs-lookup"><span data-stu-id="881b6-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="881b6-137"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="881b6-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="881b6-138">IID</span><span class="sxs-lookup"><span data-stu-id="881b6-138">IID</span></span><br/>                      | <span data-ttu-id="881b6-139">IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="881b6-139">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="881b6-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="881b6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="881b6-141">**ивмвиртуалпк**</span><span class="sxs-lookup"><span data-stu-id="881b6-141">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

