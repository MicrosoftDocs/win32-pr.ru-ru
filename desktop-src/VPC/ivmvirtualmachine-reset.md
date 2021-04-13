---
title: Метод Reset Ивмвиртуалмачине (Впккоминтерфацес. h)
description: Выполняет сброс виртуальной машины.
ms.assetid: 44daf6be-66ce-4291-a535-c30369eed60f
keywords:
- Сброс метода Virtual PC
- Сброс метода Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, метод Reset
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Reset
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45314eef6d837ac00647d477f3652b63221d977c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492237"
---
# <a name="ivmvirtualmachinereset-method"></a><span data-ttu-id="5acd2-106">Метод Ивмвиртуалмачине:: Reset</span><span class="sxs-lookup"><span data-stu-id="5acd2-106">IVMVirtualMachine::Reset method</span></span>

<span data-ttu-id="5acd2-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5acd2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5acd2-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5acd2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5acd2-109">Сброс виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5acd2-109">Resets the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="5acd2-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5acd2-110">Syntax</span></span>


```C++
HRESULT Reset(
  [out, retval] IVMTask **resetTask
);
```



## <a name="parameters"></a><span data-ttu-id="5acd2-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="5acd2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5acd2-112">*ресеттаск* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="5acd2-112">*resetTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5acd2-113">Объект [**ивмтаск**](ivmtask.md) , используемый для отслеживания хода выполнения последовательности сброса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5acd2-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the VM's reset sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5acd2-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5acd2-114">Return value</span></span>

<span data-ttu-id="5acd2-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="5acd2-115">This method can return one of these values.</span></span>



| <span data-ttu-id="5acd2-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="5acd2-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="5acd2-117">Описание</span><span class="sxs-lookup"><span data-stu-id="5acd2-117">Description</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5acd2-118"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5acd2-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="5acd2-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="5acd2-119">The operation was successful.</span></span><br/>                                     |
| <dl> <span data-ttu-id="5acd2-120"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="5acd2-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="5acd2-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="5acd2-121">The parameter is **NULL**.</span></span><br/>                                        |
| <dl> <span data-ttu-id="5acd2-122"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ \_ отказа в доступе)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="5acd2-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="5acd2-123">Вызывающий объект должен иметь разрешения на выполнение для сброса этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5acd2-123">The caller must have execute access permissions to reset this VM.</span></span><br/> |
| <dl> <span data-ttu-id="5acd2-124"><dt>**Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="5acd2-124"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="5acd2-125">Виртуальная машина не запущена.</span><span class="sxs-lookup"><span data-stu-id="5acd2-125">The VM is not running.</span></span><br/>                                            |
| <dl> <span data-ttu-id="5acd2-126"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="5acd2-126"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="5acd2-127">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="5acd2-127">The configuration is unknown.</span></span><br/>                                     |
| <dl> <span data-ttu-id="5acd2-128"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="5acd2-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="5acd2-129">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="5acd2-129">An unexpected error has occurred.</span></span><br/>                                 |



 

## <a name="requirements"></a><span data-ttu-id="5acd2-130">Требования</span><span class="sxs-lookup"><span data-stu-id="5acd2-130">Requirements</span></span>



| <span data-ttu-id="5acd2-131">Требование</span><span class="sxs-lookup"><span data-stu-id="5acd2-131">Requirement</span></span> | <span data-ttu-id="5acd2-132">Значение</span><span class="sxs-lookup"><span data-stu-id="5acd2-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5acd2-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5acd2-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5acd2-134">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5acd2-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5acd2-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5acd2-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5acd2-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5acd2-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5acd2-137">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="5acd2-137">End of client support</span></span><br/>    | <span data-ttu-id="5acd2-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5acd2-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5acd2-139">Продукт</span><span class="sxs-lookup"><span data-stu-id="5acd2-139">Product</span></span><br/>                  | <span data-ttu-id="5acd2-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5acd2-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5acd2-141">Header</span><span class="sxs-lookup"><span data-stu-id="5acd2-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="5acd2-142"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="5acd2-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5acd2-143">IID</span><span class="sxs-lookup"><span data-stu-id="5acd2-143">IID</span></span><br/>                      | <span data-ttu-id="5acd2-144">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="5acd2-144">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="5acd2-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5acd2-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5acd2-146">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="5acd2-146">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

