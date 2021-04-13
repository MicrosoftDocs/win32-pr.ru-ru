---
title: Метод Ивмвиртуалмачине Мержеундодискс (Впккоминтерфацес. h)
description: Слияние виртуальных дисков отмены.
ms.assetid: 6445b097-220e-48c4-9a7b-1139ca7b3338
keywords:
- Метод Мержеундодискс Virtual PC
- Метод Мержеундодискс Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, метод Мержеундодискс
topic_type:
- apiref
api_name:
- IVMVirtualMachine.MergeUndoDisks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48863bf998ebc02bac93aa9e74d8cdbe07265477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341065"
---
# <a name="ivmvirtualmachinemergeundodisks-method"></a><span data-ttu-id="2f48d-106">Метод Ивмвиртуалмачине:: Мержеундодискс</span><span class="sxs-lookup"><span data-stu-id="2f48d-106">IVMVirtualMachine::MergeUndoDisks method</span></span>

<span data-ttu-id="2f48d-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2f48d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2f48d-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2f48d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2f48d-109">Слияние виртуальных дисков отмены.</span><span class="sxs-lookup"><span data-stu-id="2f48d-109">Merges the virtual undo disks.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f48d-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f48d-110">Syntax</span></span>


```C++
HRESULT MergeUndoDisks(
  [out, retval] IVMTask **undoMergeTask
);
```



## <a name="parameters"></a><span data-ttu-id="2f48d-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f48d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f48d-112">*ундомержетаск* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="2f48d-112">*undoMergeTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2f48d-113">Объект [**ивмтаск**](ivmtask.md) , используемый для отслеживания создания образа.</span><span class="sxs-lookup"><span data-stu-id="2f48d-113">An [**IVMTask**](ivmtask.md) object that is used to track the creation of the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f48d-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2f48d-114">Return value</span></span>

<span data-ttu-id="2f48d-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="2f48d-115">This method can return one of these values.</span></span>



| <span data-ttu-id="2f48d-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="2f48d-116">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="2f48d-117">Описание</span><span class="sxs-lookup"><span data-stu-id="2f48d-117">Description</span></span>                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2f48d-118"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2f48d-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="2f48d-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="2f48d-119">The operation was successful.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="2f48d-120"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2f48d-120"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="2f48d-121">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="2f48d-121">An unexpected error has occurred.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="2f48d-122"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="2f48d-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="2f48d-123">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2f48d-123">The parameter is **NULL**.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="2f48d-124"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ путь ошибки \_ не \_ найден)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="2f48d-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="2f48d-125">Системе не удается найти путь, указанный параметром *конвертеддискимажепас* , или один из родительских дисков является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="2f48d-125">The system cannot find the path specified by the *convertedDiskImagePath* parameter or one of the parent disks is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="2f48d-126"><dt>**Д \_ ACCESSDENIED**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="2f48d-126"><dt>**E\_ACCESSDENIED**</dt> <dt>0x80070005</dt></span></span> </dl>                               | <span data-ttu-id="2f48d-127">У текущего пользователя недостаточно прав доступа к родительскому файлу.</span><span class="sxs-lookup"><span data-stu-id="2f48d-127">The current user has insufficient access to the parent file.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="2f48d-128"><dt>**Д \_ Обработайте**</dt> <dt>0x80070006</dt></span><span class="sxs-lookup"><span data-stu-id="2f48d-128"><dt>**E\_HANDLE**</dt> <dt>0x80070006</dt></span></span> </dl>                                     | <span data-ttu-id="2f48d-129">Один из родительских дисков используется.</span><span class="sxs-lookup"><span data-stu-id="2f48d-129">One of the parent disks is in use.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="2f48d-130"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="2f48d-130"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="2f48d-131">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="2f48d-131">The configuration is unknown.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="2f48d-132"><dt>**Виртуальная машина \_ \_Виртуальная машина E \_ с**</dt> <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="2f48d-132"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                            | <span data-ttu-id="2f48d-133">Виртуальная машина запущена.</span><span class="sxs-lookup"><span data-stu-id="2f48d-133">The virtual machine is running.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="2f48d-134"><dt>**Виртуальная машина \_ E \_ файл \_ доступен \_ только для чтения**</dt> <dt>0xA004067A</dt></span><span class="sxs-lookup"><span data-stu-id="2f48d-134"><dt>**VM\_E\_FILE\_READ\_ONLY**</dt> <dt>0xA004067A</dt></span></span> </dl>                       | <span data-ttu-id="2f48d-135">Родительский диск для виртуальных дисков отмены помечается как "только для чтения".</span><span class="sxs-lookup"><span data-stu-id="2f48d-135">The parent of virtual undo disks is marked as read only.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="2f48d-136"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2f48d-136"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="2f48d-137">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="2f48d-137">An unexpected error has occurred.</span></span><br/>                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="2f48d-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2f48d-138">Remarks</span></span>

<span data-ttu-id="2f48d-139">**Мержеундодискс** нельзя вызвать, пока выполняется виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="2f48d-139">**MergeUndoDisks** cannot be called while the virtual machine is still running.</span></span> <span data-ttu-id="2f48d-140">Используйте [**ивмвиртуалмачине:: Save**](ivmvirtualmachine-save.md) , чтобы сохранить состояние виртуальной машины перед вызовом **мержеундодискс** или [**ивмвиртуалмачине:: турнофф**](ivmvirtualmachine-turnoff.md) , чтобы отключить виртуальную машину, не сохраняя ее текущее состояние заранее.</span><span class="sxs-lookup"><span data-stu-id="2f48d-140">Use [**IVMVirtualMachine::Save**](ivmvirtualmachine-save.md) to save the state of the virtual machine before calling **MergeUndoDisks**, or [**IVMVirtualMachine::TurnOff**](ivmvirtualmachine-turnoff.md) to turn off the virtual machine without saving its current state beforehand.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f48d-141">Требования</span><span class="sxs-lookup"><span data-stu-id="2f48d-141">Requirements</span></span>



| <span data-ttu-id="2f48d-142">Требование</span><span class="sxs-lookup"><span data-stu-id="2f48d-142">Requirement</span></span> | <span data-ttu-id="2f48d-143">Значение</span><span class="sxs-lookup"><span data-stu-id="2f48d-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f48d-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2f48d-144">Minimum supported client</span></span><br/> | <span data-ttu-id="2f48d-145">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2f48d-145">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2f48d-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2f48d-146">Minimum supported server</span></span><br/> | <span data-ttu-id="2f48d-147">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2f48d-147">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2f48d-148">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="2f48d-148">End of client support</span></span><br/>    | <span data-ttu-id="2f48d-149">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2f48d-149">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2f48d-150">Продукт</span><span class="sxs-lookup"><span data-stu-id="2f48d-150">Product</span></span><br/>                  | <span data-ttu-id="2f48d-151">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2f48d-151">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2f48d-152">Header</span><span class="sxs-lookup"><span data-stu-id="2f48d-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f48d-153"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f48d-153"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2f48d-154">IID</span><span class="sxs-lookup"><span data-stu-id="2f48d-154">IID</span></span><br/>                      | <span data-ttu-id="2f48d-155">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="2f48d-155">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="2f48d-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f48d-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f48d-157">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="2f48d-157">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

