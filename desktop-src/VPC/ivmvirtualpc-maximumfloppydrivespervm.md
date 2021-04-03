---
title: Свойство Максимумфлоппидривеспервм Ивмвиртуалпк (Впккоминтерфацес. h)
description: Возвращает максимальное число дисководов гибких дисков на виртуальную машину.
ms.assetid: f0dc351b-73de-4b6b-a953-5d5b683c4e31
keywords:
- Максимумфлоппидривеспервм свойство Virtual PC
- Максимумфлоппидривеспервм свойство Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, свойство Максимумфлоппидривеспервм
topic_type:
- apiref
api_name:
- IVMVirtualPC.MaximumFloppyDrivesPerVM
- IVMVirtualPC.get_MaximumFloppyDrivesPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecc0d672affce5364e1658d5198681268109a1b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137206"
---
# <a name="ivmvirtualpcmaximumfloppydrivespervm-property"></a><span data-ttu-id="fd372-106">Свойство Ивмвиртуалпк:: Максимумфлоппидривеспервм</span><span class="sxs-lookup"><span data-stu-id="fd372-106">IVMVirtualPC::MaximumFloppyDrivesPerVM property</span></span>

<span data-ttu-id="fd372-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fd372-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fd372-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fd372-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fd372-109">Возвращает максимальное число дисководов гибких дисков на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="fd372-109">Retrieves the maximum number of floppy drives per virtual machine.</span></span>

<span data-ttu-id="fd372-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="fd372-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd372-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd372-111">Syntax</span></span>


```C++
HRESULT get_MaximumFloppyDrivesPerVM(
  [out, retval] long *maxDrives
);
```



## <a name="property-value"></a><span data-ttu-id="fd372-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="fd372-112">Property value</span></span>

<span data-ttu-id="fd372-113">Максимальное число дисководов гибких дисков на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="fd372-113">The maximum number of floppy drives per virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fd372-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="fd372-114">Error codes</span></span>



| <span data-ttu-id="fd372-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="fd372-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="fd372-116">Значение</span><span class="sxs-lookup"><span data-stu-id="fd372-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fd372-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fd372-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="fd372-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="fd372-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="fd372-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="fd372-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="fd372-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="fd372-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="fd372-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="fd372-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="fd372-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="fd372-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="fd372-123"><dt>Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="fd372-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="fd372-124">Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).</span><span class="sxs-lookup"><span data-stu-id="fd372-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="fd372-125">Требования</span><span class="sxs-lookup"><span data-stu-id="fd372-125">Requirements</span></span>



| <span data-ttu-id="fd372-126">Требование</span><span class="sxs-lookup"><span data-stu-id="fd372-126">Requirement</span></span> | <span data-ttu-id="fd372-127">Значение</span><span class="sxs-lookup"><span data-stu-id="fd372-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd372-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fd372-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fd372-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="fd372-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fd372-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fd372-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fd372-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="fd372-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fd372-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="fd372-132">End of client support</span></span><br/>    | <span data-ttu-id="fd372-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fd372-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fd372-134">Продукт</span><span class="sxs-lookup"><span data-stu-id="fd372-134">Product</span></span><br/>                  | <span data-ttu-id="fd372-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fd372-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fd372-136">Header</span><span class="sxs-lookup"><span data-stu-id="fd372-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd372-137"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd372-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fd372-138">IID</span><span class="sxs-lookup"><span data-stu-id="fd372-138">IID</span></span><br/>                      | <span data-ttu-id="fd372-139">IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="fd372-139">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="fd372-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd372-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd372-141">**ивмвиртуалпк**</span><span class="sxs-lookup"><span data-stu-id="fd372-141">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

