---
title: Метод Ивмвиртуалмачине Турнофф (Впккоминтерфацес. h)
description: Отключит виртуальную машину.
ms.assetid: 4ea00314-8f1e-47d9-bbb8-b5791af1fb86
keywords:
- Метод Турнофф Virtual PC
- Метод Турнофф Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, метод Турнофф
topic_type:
- apiref
api_name:
- IVMVirtualMachine.TurnOff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27a5b14955fcc8a060c49932e3fa4f238497a567
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071882"
---
# <a name="ivmvirtualmachineturnoff-method"></a><span data-ttu-id="b7e05-106">Метод Ивмвиртуалмачине:: Турнофф</span><span class="sxs-lookup"><span data-stu-id="b7e05-106">IVMVirtualMachine::TurnOff method</span></span>

<span data-ttu-id="b7e05-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b7e05-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b7e05-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b7e05-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b7e05-109">Отключит виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="b7e05-109">Turns off the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7e05-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7e05-110">Syntax</span></span>


```C++
HRESULT TurnOff(
  [out, retval] IVMTask **turnOffTask
);
```



## <a name="parameters"></a><span data-ttu-id="b7e05-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="b7e05-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7e05-112">*турноффтаск* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="b7e05-112">*turnOffTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b7e05-113">Объект [**ивмтаск**](ivmtask.md) , используемый для отслеживания хода выполнения последовательности турнофф виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b7e05-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the virtual machine's turnoff sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7e05-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b7e05-114">Return value</span></span>

<span data-ttu-id="b7e05-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="b7e05-115">This method can return one of these values.</span></span>



| <span data-ttu-id="b7e05-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="b7e05-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="b7e05-117">Описание</span><span class="sxs-lookup"><span data-stu-id="b7e05-117">Description</span></span>                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b7e05-118"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b7e05-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="b7e05-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="b7e05-119">The operation was successful.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="b7e05-120"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="b7e05-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="b7e05-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b7e05-121">The parameter is **NULL**.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="b7e05-122"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ \_ отказа в доступе)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="b7e05-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="b7e05-123">Вызывающий объект должен иметь разрешения на выполнение для отключения этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b7e05-123">The caller must have execute access permissions to turn off this virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="b7e05-124"><dt>**Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="b7e05-124"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="b7e05-125">Виртуальная машина не запущена.</span><span class="sxs-lookup"><span data-stu-id="b7e05-125">The virtual machine is not running.</span></span><br/>                                               |
| <dl> <span data-ttu-id="b7e05-126"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b7e05-126"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="b7e05-127">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="b7e05-127">The configuration is unknown.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="b7e05-128"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b7e05-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="b7e05-129">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="b7e05-129">An unexpected error has occurred.</span></span><br/>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="b7e05-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b7e05-130">Remarks</span></span>

<span data-ttu-id="b7e05-131">Этот метод выключает виртуальную машину таким же образом, как и отключение питания на физическом компьютере.</span><span class="sxs-lookup"><span data-stu-id="b7e05-131">This method turns off the virtual machine in the same manner as turning the power off on a physical machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7e05-132">Требования</span><span class="sxs-lookup"><span data-stu-id="b7e05-132">Requirements</span></span>



| <span data-ttu-id="b7e05-133">Требование</span><span class="sxs-lookup"><span data-stu-id="b7e05-133">Requirement</span></span> | <span data-ttu-id="b7e05-134">Значение</span><span class="sxs-lookup"><span data-stu-id="b7e05-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7e05-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b7e05-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b7e05-136">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b7e05-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b7e05-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b7e05-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b7e05-138">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b7e05-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b7e05-139">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="b7e05-139">End of client support</span></span><br/>    | <span data-ttu-id="b7e05-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b7e05-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b7e05-141">Продукт</span><span class="sxs-lookup"><span data-stu-id="b7e05-141">Product</span></span><br/>                  | <span data-ttu-id="b7e05-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b7e05-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b7e05-143">Header</span><span class="sxs-lookup"><span data-stu-id="b7e05-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7e05-144"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7e05-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b7e05-145">IID</span><span class="sxs-lookup"><span data-stu-id="b7e05-145">IID</span></span><br/>                      | <span data-ttu-id="b7e05-146">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="b7e05-146">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="b7e05-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b7e05-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7e05-148">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="b7e05-148">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

