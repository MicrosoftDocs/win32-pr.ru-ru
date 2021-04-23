---
title: Метод Pause Ивмвиртуалмачине (Впккоминтерфацес. h)
description: Приостанавливает работу виртуальной машины.
ms.assetid: 29ac40c4-7713-4782-8a31-42f2c32b8f7d
keywords:
- Приостановить метод Virtual PC
- Приостановить метод Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, метод Pause
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Pause
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c953da05d34c999066a6bc87cb1f51983defbd5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892297"
---
# <a name="ivmvirtualmachinepause-method"></a><span data-ttu-id="38b29-106">Ивмвиртуалмачине: метод:P Аусе</span><span class="sxs-lookup"><span data-stu-id="38b29-106">IVMVirtualMachine::Pause method</span></span>

<span data-ttu-id="38b29-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="38b29-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="38b29-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="38b29-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="38b29-109">Приостанавливает виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="38b29-109">Pauses the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="38b29-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38b29-110">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="38b29-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="38b29-111">Parameters</span></span>

<span data-ttu-id="38b29-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="38b29-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="38b29-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="38b29-113">Return value</span></span>

<span data-ttu-id="38b29-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="38b29-114">This method can return one of these values.</span></span>



| <span data-ttu-id="38b29-115">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="38b29-115">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="38b29-116">Описание</span><span class="sxs-lookup"><span data-stu-id="38b29-116">Description</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="38b29-117"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="38b29-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="38b29-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="38b29-118">The operation was successful.</span></span><br/>                                     |
| <dl> <span data-ttu-id="38b29-119"><dt>**Д \_ Сбой**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="38b29-119"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                                     | <span data-ttu-id="38b29-120">Виртуальная машина уже приостановлена.</span><span class="sxs-lookup"><span data-stu-id="38b29-120">The VM is already paused.</span></span><br/>                                         |
| <dl> <span data-ttu-id="38b29-121"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ \_ отказа в доступе)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="38b29-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="38b29-122">Чтобы приостановить эту виртуальную машину, вызывающая сторона должна иметь разрешения на выполнение.</span><span class="sxs-lookup"><span data-stu-id="38b29-122">The caller must have execute access permissions to pause this VM.</span></span><br/> |
| <dl> <span data-ttu-id="38b29-123"><dt>**Виртуальная машина \_ \_Истекло время \_ ожидания**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="38b29-123"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="38b29-124">Операция не завершилась своевременно.</span><span class="sxs-lookup"><span data-stu-id="38b29-124">The operation did not complete in a timely manner.</span></span><br/>                |
| <dl> <span data-ttu-id="38b29-125"><dt>**Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="38b29-125"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="38b29-126">Виртуальная машина не запущена.</span><span class="sxs-lookup"><span data-stu-id="38b29-126">The virtual machine is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="38b29-127"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="38b29-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="38b29-128">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="38b29-128">The configuration is unknown.</span></span><br/>                                     |
| <dl> <span data-ttu-id="38b29-129"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="38b29-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="38b29-130">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="38b29-130">An unexpected error has occurred.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="38b29-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38b29-131">Remarks</span></span>

<span data-ttu-id="38b29-132">**Приостановка** не сохраняет текущее состояние виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="38b29-132">**Pause** does not save the current state of the VM.</span></span>

## <a name="requirements"></a><span data-ttu-id="38b29-133">Требования</span><span class="sxs-lookup"><span data-stu-id="38b29-133">Requirements</span></span>



| <span data-ttu-id="38b29-134">Требование</span><span class="sxs-lookup"><span data-stu-id="38b29-134">Requirement</span></span> | <span data-ttu-id="38b29-135">Значение</span><span class="sxs-lookup"><span data-stu-id="38b29-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="38b29-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38b29-136">Minimum supported client</span></span><br/> | <span data-ttu-id="38b29-137">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="38b29-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="38b29-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38b29-138">Minimum supported server</span></span><br/> | <span data-ttu-id="38b29-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="38b29-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="38b29-140">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="38b29-140">End of client support</span></span><br/>    | <span data-ttu-id="38b29-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="38b29-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="38b29-142">Продукт</span><span class="sxs-lookup"><span data-stu-id="38b29-142">Product</span></span><br/>                  | <span data-ttu-id="38b29-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="38b29-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="38b29-144">Header</span><span class="sxs-lookup"><span data-stu-id="38b29-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="38b29-145"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="38b29-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="38b29-146">IID</span><span class="sxs-lookup"><span data-stu-id="38b29-146">IID</span></span><br/>                      | <span data-ttu-id="38b29-147">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="38b29-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="38b29-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38b29-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38b29-149">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="38b29-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

