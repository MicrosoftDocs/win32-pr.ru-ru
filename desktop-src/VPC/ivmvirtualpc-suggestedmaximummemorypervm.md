---
title: Свойство Сугжестедмаксимуммеморипервм Ивмвиртуалпк (Впккоминтерфацес. h)
description: Извлекает рекомендуемое максимально допустимое количество физической памяти на виртуальную машину в мегабайтах, чтобы избежать нехватки памяти на узле.
ms.assetid: 533cca40-f41d-4717-87ae-d8072414a637
keywords:
- Сугжестедмаксимуммеморипервм свойство Virtual PC
- Сугжестедмаксимуммеморипервм свойство Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, свойство Сугжестедмаксимуммеморипервм
topic_type:
- apiref
api_name:
- IVMVirtualPC.SuggestedMaximumMemoryPerVM
- IVMVirtualPC.get_SuggestedMaximumMemoryPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142c4ade861116876342d598fbf10b5925fa100e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104072015"
---
# <a name="ivmvirtualpcsuggestedmaximummemorypervm-property"></a><span data-ttu-id="84cd8-106">Свойство Ивмвиртуалпк:: Сугжестедмаксимуммеморипервм</span><span class="sxs-lookup"><span data-stu-id="84cd8-106">IVMVirtualPC::SuggestedMaximumMemoryPerVM property</span></span>

<span data-ttu-id="84cd8-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="84cd8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="84cd8-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="84cd8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="84cd8-109">Извлекает рекомендуемое максимально допустимое количество физической памяти на виртуальную машину в мегабайтах, чтобы избежать нехватки памяти на узле.</span><span class="sxs-lookup"><span data-stu-id="84cd8-109">Retrieves the suggested maximum allowable quantity of physical memory per virtual machine, in megabytes, to avoid low memory conditions on the host.</span></span>

<span data-ttu-id="84cd8-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="84cd8-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="84cd8-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84cd8-111">Syntax</span></span>


```C++
HRESULT get_SuggestedMaximumMemoryPerVM(
  [out, retval] long *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="84cd8-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="84cd8-112">Property value</span></span>

<span data-ttu-id="84cd8-113">Рекомендуемое максимально допустимое количество (в мегабайтах) физической памяти на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="84cd8-113">The suggested maximum allowable quantity, in megabytes, of physical memory per virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="84cd8-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="84cd8-114">Error codes</span></span>



| <span data-ttu-id="84cd8-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="84cd8-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="84cd8-116">Значение</span><span class="sxs-lookup"><span data-stu-id="84cd8-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="84cd8-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="84cd8-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="84cd8-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="84cd8-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="84cd8-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="84cd8-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="84cd8-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="84cd8-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="84cd8-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="84cd8-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="84cd8-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="84cd8-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="84cd8-123"><dt>Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="84cd8-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="84cd8-124">Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).</span><span class="sxs-lookup"><span data-stu-id="84cd8-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="84cd8-125">Требования</span><span class="sxs-lookup"><span data-stu-id="84cd8-125">Requirements</span></span>



| <span data-ttu-id="84cd8-126">Требование</span><span class="sxs-lookup"><span data-stu-id="84cd8-126">Requirement</span></span> | <span data-ttu-id="84cd8-127">Значение</span><span class="sxs-lookup"><span data-stu-id="84cd8-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="84cd8-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84cd8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="84cd8-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="84cd8-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="84cd8-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84cd8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="84cd8-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="84cd8-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="84cd8-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="84cd8-132">End of client support</span></span><br/>    | <span data-ttu-id="84cd8-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="84cd8-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="84cd8-134">Продукт</span><span class="sxs-lookup"><span data-stu-id="84cd8-134">Product</span></span><br/>                  | <span data-ttu-id="84cd8-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="84cd8-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="84cd8-136">Header</span><span class="sxs-lookup"><span data-stu-id="84cd8-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="84cd8-137"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="84cd8-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="84cd8-138">IID</span><span class="sxs-lookup"><span data-stu-id="84cd8-138">IID</span></span><br/>                      | <span data-ttu-id="84cd8-139">IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="84cd8-139">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="84cd8-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84cd8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84cd8-141">**ивмвиртуалпк**</span><span class="sxs-lookup"><span data-stu-id="84cd8-141">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

