---
title: Метод Resume Ивмвиртуалмачине (Впккоминтерфацес. h)
description: Возобновляет работу виртуальной машины.
ms.assetid: 4a2d6b64-8dcf-484e-940d-b0180aba9f01
keywords:
- Метод возобновления работы Virtual PC
- Метод возобновления работы Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, метод Resume
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Resume
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c24af1e1a00aa0fa29acc077faf48287c0307414
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892409"
---
# <a name="ivmvirtualmachineresume-method"></a><span data-ttu-id="d1b19-106">Метод Ивмвиртуалмачине:: Resume</span><span class="sxs-lookup"><span data-stu-id="d1b19-106">IVMVirtualMachine::Resume method</span></span>

<span data-ttu-id="d1b19-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d1b19-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d1b19-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d1b19-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d1b19-109">Возобновляет виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="d1b19-109">Resumes the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="d1b19-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1b19-110">Syntax</span></span>


```C++
HRESULT Resume();
```



## <a name="parameters"></a><span data-ttu-id="d1b19-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="d1b19-111">Parameters</span></span>

<span data-ttu-id="d1b19-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="d1b19-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d1b19-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d1b19-113">Return value</span></span>

<span data-ttu-id="d1b19-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="d1b19-114">This method can return one of these values.</span></span>



| <span data-ttu-id="d1b19-115">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="d1b19-115">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="d1b19-116">Описание</span><span class="sxs-lookup"><span data-stu-id="d1b19-116">Description</span></span>                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d1b19-117"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d1b19-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="d1b19-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d1b19-118">The operation was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="d1b19-119"><dt>**Д \_ Сбой**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="d1b19-119"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                                     | <span data-ttu-id="d1b19-120">Виртуальная машина не приостановлена.</span><span class="sxs-lookup"><span data-stu-id="d1b19-120">The VM is not paused.</span></span><br/>                                              |
| <dl> <span data-ttu-id="d1b19-121"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ \_ отказа в доступе)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="d1b19-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="d1b19-122">Вызывающий объект должен иметь разрешения на выполнение для возобновления работы этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d1b19-122">The caller must have execute access permissions to resume this VM.</span></span><br/> |
| <dl> <span data-ttu-id="d1b19-123"><dt>**Виртуальная машина \_ \_Истекло время \_ ожидания**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="d1b19-123"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="d1b19-124">Операция не завершилась своевременно.</span><span class="sxs-lookup"><span data-stu-id="d1b19-124">The operation did not complete in a timely manner.</span></span><br/>                 |
| <dl> <span data-ttu-id="d1b19-125"><dt>**Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="d1b19-125"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="d1b19-126">Виртуальная машина не запущена.</span><span class="sxs-lookup"><span data-stu-id="d1b19-126">The VM is not running.</span></span><br/>                                             |
| <dl> <span data-ttu-id="d1b19-127"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d1b19-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="d1b19-128">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="d1b19-128">The configuration is unknown.</span></span><br/>                                      |
| <dl> <span data-ttu-id="d1b19-129"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d1b19-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="d1b19-130">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="d1b19-130">An unexpected error has occurred.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="d1b19-131">Требования</span><span class="sxs-lookup"><span data-stu-id="d1b19-131">Requirements</span></span>



| <span data-ttu-id="d1b19-132">Требование</span><span class="sxs-lookup"><span data-stu-id="d1b19-132">Requirement</span></span> | <span data-ttu-id="d1b19-133">Значение</span><span class="sxs-lookup"><span data-stu-id="d1b19-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1b19-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1b19-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d1b19-135">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d1b19-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d1b19-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1b19-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d1b19-137">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d1b19-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d1b19-138">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d1b19-138">End of client support</span></span><br/>    | <span data-ttu-id="d1b19-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d1b19-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d1b19-140">Продукт</span><span class="sxs-lookup"><span data-stu-id="d1b19-140">Product</span></span><br/>                  | <span data-ttu-id="d1b19-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d1b19-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d1b19-142">Header</span><span class="sxs-lookup"><span data-stu-id="d1b19-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1b19-143"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1b19-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d1b19-144">IID</span><span class="sxs-lookup"><span data-stu-id="d1b19-144">IID</span></span><br/>                      | <span data-ttu-id="d1b19-145">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="d1b19-145">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="d1b19-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d1b19-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1b19-147">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="d1b19-147">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

