---
title: Свойство памяти Ивмвиртуалмачине (Впккоминтерфацес. h)
description: Объем физической памяти виртуальной машины в мегабайтах.
ms.assetid: 1a1d4cc7-a537-49f0-981f-0b72eca9013e
keywords:
- Свойство памяти Virtual PC
- Свойство памяти Virtual PC, интерфейс Ивмвиртуалмачине
- Виртуальный ПК интерфейса Ивмвиртуалмачине, свойство Memory
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Memory
- IVMVirtualMachine.get_Memory
- IVMVirtualMachine.put_Memory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b73251b58639e0311e33120cd4bb0e778a017b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105650360"
---
# <a name="ivmvirtualmachinememory-property"></a><span data-ttu-id="e9dc6-106">Свойство Ивмвиртуалмачине:: Memory</span><span class="sxs-lookup"><span data-stu-id="e9dc6-106">IVMVirtualMachine::Memory property</span></span>

<span data-ttu-id="e9dc6-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e9dc6-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e9dc6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e9dc6-109">Извлекает и задает объем физической памяти виртуальной машины в мегабайтах.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-109">Retrieves and sets the amount of physical memory in the virtual machine, in megabytes.</span></span>

<span data-ttu-id="e9dc6-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9dc6-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9dc6-111">Syntax</span></span>


```C++
HRESULT put_Memory(
  [in]          long megabytesOfMemory
);

HRESULT get_Memory(
  [out, retval] long *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="e9dc6-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e9dc6-112">Property value</span></span>

<span data-ttu-id="e9dc6-113">Указывает объем физической памяти в мегабайтах.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-113">Specifies the amount of physical memory, in megabytes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e9dc6-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="e9dc6-114">Error codes</span></span>



| <span data-ttu-id="e9dc6-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="e9dc6-115">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="e9dc6-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e9dc6-116">Meaning</span></span>                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="e9dc6-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e9dc6-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="e9dc6-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-118">The operation was successful.</span></span><br/>                  |
| <dl> <span data-ttu-id="e9dc6-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="e9dc6-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="e9dc6-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-120">The parameter is **NULL**.</span></span><br/>                     |
| <dl> <span data-ttu-id="e9dc6-121"><dt>Д \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="e9dc6-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="e9dc6-122">Параметр является недопустимым или выходит за пределы допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-122">The parameter is not valid or is out of range.</span></span><br/> |
| <dl> <span data-ttu-id="e9dc6-123"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e9dc6-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="e9dc6-124">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-124">The configuration is unknown.</span></span><br/>                  |
| <dl> <span data-ttu-id="e9dc6-125"><dt>Виртуальная машина \_ E \_ преф \_ не \_ Найдено</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="e9dc6-125"><dt>VM\_E\_PREF\_NOT\_FOUND</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="e9dc6-126">Предпочтение не найдено.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-126">The preference was not found.</span></span><br/>                  |
| <dl> <span data-ttu-id="e9dc6-127"><dt>Виртуальная машина \_ \_Преф \_ Виртуальная машина E \_ Active</dt> <dt>0xA0040302</dt></span><span class="sxs-lookup"><span data-stu-id="e9dc6-127"><dt>VM\_E\_PREF\_VM\_ACTIVE</dt> <dt>0xA0040302</dt></span></span> </dl> | <span data-ttu-id="e9dc6-128">Виртуальная машина запущена или сохранена.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-128">The virtual machine is running or saved.</span></span><br/>       |
| <dl> <span data-ttu-id="e9dc6-129"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e9dc6-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="e9dc6-130">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-130">An unexpected error has occurred.</span></span><br/>              |



## <a name="remarks"></a><span data-ttu-id="e9dc6-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e9dc6-131">Remarks</span></span>

<span data-ttu-id="e9dc6-132">Объем физической памяти виртуальной машины должен составлять не менее 4 МБ.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-132">The amount of physical memory in a virtual machine must be at least 4 MB.</span></span> <span data-ttu-id="e9dc6-133">Верхний предел памяти зависит от конфигурации узла, но может быть не более 3 712 МБ.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-133">The upper limit on memory depends on the host configuration, but can be at most 3,712 MB.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9dc6-134">Требования</span><span class="sxs-lookup"><span data-stu-id="e9dc6-134">Requirements</span></span>



| <span data-ttu-id="e9dc6-135">Требование</span><span class="sxs-lookup"><span data-stu-id="e9dc6-135">Requirement</span></span> | <span data-ttu-id="e9dc6-136">Значение</span><span class="sxs-lookup"><span data-stu-id="e9dc6-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9dc6-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e9dc6-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e9dc6-138">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e9dc6-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e9dc6-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e9dc6-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e9dc6-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e9dc6-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e9dc6-141">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="e9dc6-141">End of client support</span></span><br/>    | <span data-ttu-id="e9dc6-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e9dc6-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e9dc6-143">Продукт</span><span class="sxs-lookup"><span data-stu-id="e9dc6-143">Product</span></span><br/>                  | <span data-ttu-id="e9dc6-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e9dc6-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e9dc6-145">Header</span><span class="sxs-lookup"><span data-stu-id="e9dc6-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9dc6-146"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9dc6-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e9dc6-147">IID</span><span class="sxs-lookup"><span data-stu-id="e9dc6-147">IID</span></span><br/>                      | <span data-ttu-id="e9dc6-148">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="e9dc6-148">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="e9dc6-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e9dc6-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9dc6-150">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="e9dc6-150">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

