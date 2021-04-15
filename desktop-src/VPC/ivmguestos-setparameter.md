---
title: Метод Ивмгуестос Сетпараметер (Впккоминтерфацес. h)
description: Задает именованный параметр в гостевой операционной системе.
ms.assetid: ed6ade61-19dc-44ac-9e86-29fffe80e874
keywords:
- Метод Сетпараметер Virtual PC
- Метод Сетпараметер Virtual PC, интерфейс Ивмгуестос
- Ивмгуестос интерфейс Virtual PC, метод Сетпараметер
topic_type:
- apiref
api_name:
- IVMGuestOS.SetParameter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80dd2290578ef55d56e4c194e27102a1075d7a10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534283"
---
# <a name="ivmguestossetparameter-method"></a><span data-ttu-id="f4fd5-106">Метод Ивмгуестос:: Сетпараметер</span><span class="sxs-lookup"><span data-stu-id="f4fd5-106">IVMGuestOS::SetParameter method</span></span>

<span data-ttu-id="f4fd5-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f4fd5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f4fd5-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f4fd5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f4fd5-109">Задает именованный параметр в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="f4fd5-109">Sets a named parameter within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4fd5-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f4fd5-110">Syntax</span></span>


```C++
HRESULT SetParameter(
  [in] BSTR inParameterName,
  [in] BSTR inParameterValue
);
```



## <a name="parameters"></a><span data-ttu-id="f4fd5-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="f4fd5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4fd5-112">*инпараметернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f4fd5-112">*inParameterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4fd5-113">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="f4fd5-113">The parameter name.</span></span> <span data-ttu-id="f4fd5-114">Длина должна составлять от 1 до 255 символов и не может содержать обратную косую черту ( \) символ).</span><span class="sxs-lookup"><span data-stu-id="f4fd5-114">It must be between 1 and 255 characters in length and cannot contain a backslash (\) character.</span></span>

</dd> <dt>

<span data-ttu-id="f4fd5-115">*инпараметервалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f4fd5-115">*inParameterValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4fd5-116">Значение параметра.</span><span class="sxs-lookup"><span data-stu-id="f4fd5-116">The parameter value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4fd5-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f4fd5-117">Return value</span></span>

<span data-ttu-id="f4fd5-118">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="f4fd5-118">This method can return one of these values.</span></span>



| <span data-ttu-id="f4fd5-119">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="f4fd5-119">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="f4fd5-120">Описание</span><span class="sxs-lookup"><span data-stu-id="f4fd5-120">Description</span></span>                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="f4fd5-121"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f4fd5-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="f4fd5-122">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="f4fd5-122">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="f4fd5-123"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="f4fd5-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="f4fd5-124">Параметр является недопустимым или не указан.</span><span class="sxs-lookup"><span data-stu-id="f4fd5-124">A parameter is not valid or not specified.</span></span><br/>           |
| <dl> <span data-ttu-id="f4fd5-125"><dt>**Виртуальная машина \_ \_Истекло время \_ ожидания**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="f4fd5-125"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="f4fd5-126">Операция не завершилась своевременно.</span><span class="sxs-lookup"><span data-stu-id="f4fd5-126">The operation did not complete in a timely manner.</span></span><br/>   |
| <dl> <span data-ttu-id="f4fd5-127"><dt>**Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="f4fd5-127"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="f4fd5-128">Виртуальная машина не запущена.</span><span class="sxs-lookup"><span data-stu-id="f4fd5-128">The virtual machine (VM) is not running.</span></span><br/>             |
| <dl> <span data-ttu-id="f4fd5-129"><dt>**Виртуальная машина \_ 0xA00400507 \_ Виртуальная машина \_ приостановлена**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f4fd5-129"><dt>**VM\_E\_VM\_PAUSED**</dt> <dt>0xA00400507</dt></span></span> </dl>                    | <span data-ttu-id="f4fd5-130">Виртуальная машина приостановлена.</span><span class="sxs-lookup"><span data-stu-id="f4fd5-130">The VM is paused.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f4fd5-131"><dt>**Виртуальная машина \_ Добавление компонента "E" \_ \_ \_ не \_**</dt> доступно <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="f4fd5-131"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="f4fd5-132">Компоненты интеграции не установлены в этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="f4fd5-132">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="f4fd5-133"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f4fd5-133"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="f4fd5-134">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="f4fd5-134">An unexpected error has occurred.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="f4fd5-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f4fd5-135">Remarks</span></span>

<span data-ttu-id="f4fd5-136">При вызове этого метода виртуальная машина должна быть запущена, а компоненты интеграции должны быть установлены.</span><span class="sxs-lookup"><span data-stu-id="f4fd5-136">The VM must be running and integration components must be installed when this method is invoked.</span></span> <span data-ttu-id="f4fd5-137">Этот метод поддерживается только для гостевых операционных систем под управлением Windows.</span><span class="sxs-lookup"><span data-stu-id="f4fd5-137">This method is only supported for Windows-based guest operating systems.</span></span>

<span data-ttu-id="f4fd5-138">После установки компонентов интеграции в реестр гостевой операционной системы автоматически добавляется следующий ключ:</span><span class="sxs-lookup"><span data-stu-id="f4fd5-138">With integration components installed, the following key is automatically added to the guest operating system's registry:</span></span>

<span data-ttu-id="f4fd5-139">**HKEY \_ локальный \_ компьютер \\ программное обеспечение \\ \\ виртуальные машины Microsoft \\ Гостевые \\ Параметры**</span><span class="sxs-lookup"><span data-stu-id="f4fd5-139">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Virtual Machine\\Guest\\Parameters**</span></span>

<span data-ttu-id="f4fd5-140">При запуске гостевой операционной системы в разделе **параметров** заполняются следующие строковые значения реестра:</span><span class="sxs-lookup"><span data-stu-id="f4fd5-140">When the guest operating system starts, the following registry string values are populated in the **Parameters** key:</span></span>

-   <span data-ttu-id="f4fd5-141">**HostName**</span><span class="sxs-lookup"><span data-stu-id="f4fd5-141">**HostName**</span></span>
-   <span data-ttu-id="f4fd5-142">**фисикалхостнаме**</span><span class="sxs-lookup"><span data-stu-id="f4fd5-142">**PhysicalHostName**</span></span>
-   <span data-ttu-id="f4fd5-143">**фисикалхостнамефулликуалифиед**</span><span class="sxs-lookup"><span data-stu-id="f4fd5-143">**PhysicalHostNameFullyQualified**</span></span>
-   <span data-ttu-id="f4fd5-144">**VirtualMachineName**</span><span class="sxs-lookup"><span data-stu-id="f4fd5-144">**VirtualMachineName**</span></span>

## <a name="requirements"></a><span data-ttu-id="f4fd5-145">Требования</span><span class="sxs-lookup"><span data-stu-id="f4fd5-145">Requirements</span></span>



| <span data-ttu-id="f4fd5-146">Требование</span><span class="sxs-lookup"><span data-stu-id="f4fd5-146">Requirement</span></span> | <span data-ttu-id="f4fd5-147">Значение</span><span class="sxs-lookup"><span data-stu-id="f4fd5-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4fd5-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f4fd5-148">Minimum supported client</span></span><br/> | <span data-ttu-id="f4fd5-149">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f4fd5-149">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f4fd5-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f4fd5-150">Minimum supported server</span></span><br/> | <span data-ttu-id="f4fd5-151">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f4fd5-151">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f4fd5-152">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="f4fd5-152">End of client support</span></span><br/>    | <span data-ttu-id="f4fd5-153">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f4fd5-153">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f4fd5-154">Продукт</span><span class="sxs-lookup"><span data-stu-id="f4fd5-154">Product</span></span><br/>                  | <span data-ttu-id="f4fd5-155">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f4fd5-155">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f4fd5-156">Header</span><span class="sxs-lookup"><span data-stu-id="f4fd5-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4fd5-157"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4fd5-157"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f4fd5-158">IID</span><span class="sxs-lookup"><span data-stu-id="f4fd5-158">IID</span></span><br/>                      | <span data-ttu-id="f4fd5-159">IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="f4fd5-159">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="f4fd5-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f4fd5-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4fd5-161">**ивмгуестос**</span><span class="sxs-lookup"><span data-stu-id="f4fd5-161">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

