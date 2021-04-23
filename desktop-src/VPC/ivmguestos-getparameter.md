---
title: Метод Ивмгуестос-Parameter (Впккоминтерфацес. h)
description: Извлекает именованный параметр в гостевой операционной системе.
ms.assetid: d4d5acbd-fa19-4eb2-af75-2c94e5f6f7f0
keywords:
- Метод параметра Virtual PC
- Метод параметра Virtual PC, интерфейс Ивмгуестос
- Интерфейс Ивмгуестос Virtual PC, метод «, параметр»
topic_type:
- apiref
api_name:
- IVMGuestOS.GetParameter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0acbdd5a1d633a8c032651d2df16f4d0e26dec70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535183"
---
# <a name="ivmguestosgetparameter-method"></a><span data-ttu-id="aa9d2-106">Метод Ивмгуестос:: Parameter</span><span class="sxs-lookup"><span data-stu-id="aa9d2-106">IVMGuestOS::GetParameter method</span></span>

<span data-ttu-id="aa9d2-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="aa9d2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="aa9d2-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="aa9d2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="aa9d2-109">Извлекает именованный параметр в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="aa9d2-109">Retrieves a named parameter within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa9d2-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aa9d2-110">Syntax</span></span>


```C++
HRESULT GetParameter(
  [in]          BSTR inParameterName,
  [out, retval] BSTR *outParameterValue
);
```



## <a name="parameters"></a><span data-ttu-id="aa9d2-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="aa9d2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa9d2-112">*инпараметернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aa9d2-112">*inParameterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa9d2-113">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="aa9d2-113">The parameter name.</span></span> <span data-ttu-id="aa9d2-114">Длина должна составлять от 1 до 255 символов и не может содержать обратную косую черту ( \) символ).</span><span class="sxs-lookup"><span data-stu-id="aa9d2-114">It must be between 1 and 255 characters in length and cannot contain a backslash (\) character.</span></span>

</dd> <dt>

<span data-ttu-id="aa9d2-115">*аутпараметервалуе* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="aa9d2-115">*outParameterValue* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="aa9d2-116">Значение параметра.</span><span class="sxs-lookup"><span data-stu-id="aa9d2-116">The parameter value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa9d2-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aa9d2-117">Return value</span></span>

<span data-ttu-id="aa9d2-118">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="aa9d2-118">This method can return one of these values.</span></span>



| <span data-ttu-id="aa9d2-119">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="aa9d2-119">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="aa9d2-120">Описание</span><span class="sxs-lookup"><span data-stu-id="aa9d2-120">Description</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aa9d2-121"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="aa9d2-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="aa9d2-122">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="aa9d2-122">The operation was successful.</span></span><br/>                                     |
| <dl> <span data-ttu-id="aa9d2-123"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="aa9d2-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="aa9d2-124">Параметр является недопустимым или не указан.</span><span class="sxs-lookup"><span data-stu-id="aa9d2-124">A parameter is not valid or not specified.</span></span><br/>                        |
| <dl> <span data-ttu-id="aa9d2-125"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="aa9d2-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="aa9d2-126">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="aa9d2-126">The parameter is **NULL**.</span></span><br/>                                        |
| <dl> <span data-ttu-id="aa9d2-127"><dt>**Виртуальная машина \_ \_Истекло время \_ ожидания**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="aa9d2-127"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="aa9d2-128">Операция не завершилась своевременно.</span><span class="sxs-lookup"><span data-stu-id="aa9d2-128">The operation did not complete in a timely manner.</span></span><br/>                |
| <dl> <span data-ttu-id="aa9d2-129"><dt>**Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="aa9d2-129"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="aa9d2-130">Виртуальная машина не запущена.</span><span class="sxs-lookup"><span data-stu-id="aa9d2-130">The virtual machine is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="aa9d2-131"><dt>**Виртуальная машина \_ 0xA00400507 \_ Виртуальная машина \_ приостановлена**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="aa9d2-131"><dt>**VM\_E\_VM\_PAUSED**</dt> <dt>0xA00400507</dt></span></span> </dl>                    | <span data-ttu-id="aa9d2-132">Виртуальная машина приостановлена.</span><span class="sxs-lookup"><span data-stu-id="aa9d2-132">The virtual machine is paused.</span></span><br/>                                    |
| <dl> <span data-ttu-id="aa9d2-133"><dt>**Виртуальная машина \_ Добавление компонента "E" \_ \_ \_ не \_**</dt> доступно <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="aa9d2-133"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="aa9d2-134">Компоненты интеграции не установлены на этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="aa9d2-134">Integration components are not installed in this virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="aa9d2-135"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="aa9d2-135"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="aa9d2-136">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="aa9d2-136">An unexpected error has occurred.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="aa9d2-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aa9d2-137">Remarks</span></span>

<span data-ttu-id="aa9d2-138">Виртуальная машина должна быть запущена, и при вызове этого метода должны быть установлены компоненты интеграции.</span><span class="sxs-lookup"><span data-stu-id="aa9d2-138">The virtual machine must be running and integration components must be installed when this method is invoked.</span></span> <span data-ttu-id="aa9d2-139">Этот метод поддерживается только для гостевых операционных систем под управлением Windows.</span><span class="sxs-lookup"><span data-stu-id="aa9d2-139">This method is only supported for Windows-based guest operating systems.</span></span>

<span data-ttu-id="aa9d2-140">После установки компонентов интеграции в реестр гостевой операционной системы автоматически добавляется следующий ключ:</span><span class="sxs-lookup"><span data-stu-id="aa9d2-140">With integration components installed, the following key is automatically added to the guest operating system's registry:</span></span>

<span data-ttu-id="aa9d2-141">**HKEY \_ локальный \_ компьютер \\ программное обеспечение \\ \\ виртуальные машины Microsoft \\ Гостевые \\ Параметры**</span><span class="sxs-lookup"><span data-stu-id="aa9d2-141">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Virtual Machine\\Guest\\Parameters**</span></span>

<span data-ttu-id="aa9d2-142">При запуске гостевой операционной системы в разделе **параметров** заполняются следующие строковые значения реестра:</span><span class="sxs-lookup"><span data-stu-id="aa9d2-142">When the guest operating system starts, the following registry string values are populated in the **Parameters** key:</span></span>

-   <span data-ttu-id="aa9d2-143">**HostName**</span><span class="sxs-lookup"><span data-stu-id="aa9d2-143">**HostName**</span></span>
-   <span data-ttu-id="aa9d2-144">**фисикалхостнаме**</span><span class="sxs-lookup"><span data-stu-id="aa9d2-144">**PhysicalHostName**</span></span>
-   <span data-ttu-id="aa9d2-145">**фисикалхостнамефулликуалифиед**</span><span class="sxs-lookup"><span data-stu-id="aa9d2-145">**PhysicalHostNameFullyQualified**</span></span>
-   <span data-ttu-id="aa9d2-146">**VirtualMachineName**</span><span class="sxs-lookup"><span data-stu-id="aa9d2-146">**VirtualMachineName**</span></span>

## <a name="requirements"></a><span data-ttu-id="aa9d2-147">Требования</span><span class="sxs-lookup"><span data-stu-id="aa9d2-147">Requirements</span></span>



| <span data-ttu-id="aa9d2-148">Требование</span><span class="sxs-lookup"><span data-stu-id="aa9d2-148">Requirement</span></span> | <span data-ttu-id="aa9d2-149">Значение</span><span class="sxs-lookup"><span data-stu-id="aa9d2-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa9d2-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aa9d2-150">Minimum supported client</span></span><br/> | <span data-ttu-id="aa9d2-151">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="aa9d2-151">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="aa9d2-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aa9d2-152">Minimum supported server</span></span><br/> | <span data-ttu-id="aa9d2-153">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="aa9d2-153">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="aa9d2-154">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="aa9d2-154">End of client support</span></span><br/>    | <span data-ttu-id="aa9d2-155">Windows 7</span><span class="sxs-lookup"><span data-stu-id="aa9d2-155">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="aa9d2-156">Продукт</span><span class="sxs-lookup"><span data-stu-id="aa9d2-156">Product</span></span><br/>                  | <span data-ttu-id="aa9d2-157">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="aa9d2-157">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="aa9d2-158">Header</span><span class="sxs-lookup"><span data-stu-id="aa9d2-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa9d2-159"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa9d2-159"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="aa9d2-160">IID</span><span class="sxs-lookup"><span data-stu-id="aa9d2-160">IID</span></span><br/>                      | <span data-ttu-id="aa9d2-161">IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="aa9d2-161">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="aa9d2-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa9d2-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa9d2-163">**ивмгуестос**</span><span class="sxs-lookup"><span data-stu-id="aa9d2-163">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

