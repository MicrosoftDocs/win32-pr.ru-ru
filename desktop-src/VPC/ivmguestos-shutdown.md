---
title: Метод завершения работы Ивмгуестос (Впккоминтерфацес. h)
description: Завершает работу гостевой операционной системы на виртуальной машине.
ms.assetid: a1453ad1-c4c2-47bb-a612-d203a6ee8c18
keywords:
- Метод завершения работы Virtual PC
- Метод завершения работы Virtual PC, интерфейс Ивмгуестос
- Ивмгуестос интерфейс Virtual PC, метод Shutdown
topic_type:
- apiref
api_name:
- IVMGuestOS.Shutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63025270752af044a572cf9b6299e54b31b89ffe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802698"
---
# <a name="ivmguestosshutdown-method"></a><span data-ttu-id="0002c-106">Метод Ивмгуестос:: Shutdown</span><span class="sxs-lookup"><span data-stu-id="0002c-106">IVMGuestOS::Shutdown method</span></span>

<span data-ttu-id="0002c-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0002c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0002c-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0002c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0002c-109">Завершает работу гостевой операционной системы в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="0002c-109">Shuts down the guest operating system in the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="0002c-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0002c-110">Syntax</span></span>


```C++
HRESULT Shutdown(
  [in]          VARIANT_BOOL isForced,
  [out, retval] IVMTask      **outShutdownTask
);
```



## <a name="parameters"></a><span data-ttu-id="0002c-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="0002c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0002c-112">*принудительно* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0002c-112">*isForced* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0002c-113">**Вариант \_ Значение TRUE** , если завершение работы должно быть принудительным; в противном случае — значение **\_ false** .</span><span class="sxs-lookup"><span data-stu-id="0002c-113">**VARIANT\_TRUE** if the shutdown is to be forced, **VARIANT\_FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="0002c-114">*аутшутдовнтаск* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="0002c-114">*outShutdownTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0002c-115">Объект [**ивмтаск**](ivmtask.md) , который используется для отслеживания завершения процесса завершения работы.</span><span class="sxs-lookup"><span data-stu-id="0002c-115">An [**IVMTask**](ivmtask.md) object that is used to track the completion of the shutdown process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0002c-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0002c-116">Return value</span></span>

<span data-ttu-id="0002c-117">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="0002c-117">This method can return one of these values.</span></span>



| <span data-ttu-id="0002c-118">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="0002c-118">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="0002c-119">Описание</span><span class="sxs-lookup"><span data-stu-id="0002c-119">Description</span></span>                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0002c-120"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0002c-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="0002c-121">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="0002c-121">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="0002c-122"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="0002c-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="0002c-123">Параметр *аутшутдовнтаск* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="0002c-123">The *outShutdownTask* parameter is **NULL**.</span></span><br/>                    |
| <dl> <span data-ttu-id="0002c-124"><dt>**Виртуальная машина \_ \_Истекло время \_ ожидания**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="0002c-124"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="0002c-125">Операция не завершилась своевременно.</span><span class="sxs-lookup"><span data-stu-id="0002c-125">The operation did not complete in a timely manner.</span></span><br/>              |
| <dl> <span data-ttu-id="0002c-126"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="0002c-126"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="0002c-127">Не удалось найти виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="0002c-127">The VM could not be found.</span></span><br/>                                      |
| <dl> <span data-ttu-id="0002c-128"><dt>**Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="0002c-128"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="0002c-129">Для этой операции должна быть запущена виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="0002c-129">The VM must be running for this operation.</span></span><br/>                      |
| <dl> <span data-ttu-id="0002c-130"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ \_ отказа в доступе)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="0002c-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="0002c-131">Вызывающий объект должен иметь разрешения на выполнение для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0002c-131">The caller must have execute access permissions for this VM.</span></span><br/>    |
| <dl> <span data-ttu-id="0002c-132"><dt>**Виртуальная машина \_ Добавление компонента "E" \_ \_ \_ не \_**</dt> доступно <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="0002c-132"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>       | <span data-ttu-id="0002c-133">Компонент интеграции компонентов не установлен на этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="0002c-133">The integration components feature is not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="0002c-134"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="0002c-134"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="0002c-135">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="0002c-135">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="0002c-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0002c-136">Remarks</span></span>

<span data-ttu-id="0002c-137">При вызове этого метода виртуальная машина должна быть запущена, а компонент интеграции должен быть установлен.</span><span class="sxs-lookup"><span data-stu-id="0002c-137">The VM must be running and integration components feature must be installed when this method is invoked.</span></span> <span data-ttu-id="0002c-138">Этот метод поддерживается только для гостевых операционных систем под управлением Windows.</span><span class="sxs-lookup"><span data-stu-id="0002c-138">This method is only supported for Windows-based guest operating systems.</span></span>

<span data-ttu-id="0002c-139">Следующие значения можно возвратить с помощью свойства [**Error**](ivmtask-error.md) возвращенного объекта [**ивмтаск**](ivmtask.md) .</span><span class="sxs-lookup"><span data-stu-id="0002c-139">The following values can be returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object.</span></span>



| <span data-ttu-id="0002c-140">Код [**ошибки**](ivmtask-error.md) /значение</span><span class="sxs-lookup"><span data-stu-id="0002c-140">[**Error**](ivmtask-error.md) code/Value</span></span>                                                                                                                                                                                                                                                                          | <span data-ttu-id="0002c-141">Описание</span><span class="sxs-lookup"><span data-stu-id="0002c-141">Description</span></span>                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0002c-142"><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` 0x80070005</span><span class="sxs-lookup"><span data-stu-id="0002c-142"><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` (0x80070005)</span></span><br/>                             | <span data-ttu-id="0002c-143">Вызывающий объект должен иметь разрешения на выполнение для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0002c-143">The caller must have execute access permissions for this VM.</span></span><br/>             |
| <span data-ttu-id="0002c-144"><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7)</span><span class="sxs-lookup"><span data-stu-id="0002c-144"><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7)</span></span><br/>                         | <span data-ttu-id="0002c-145">Компьютер заблокирован и не может завершить работу без параметра Force.</span><span class="sxs-lookup"><span data-stu-id="0002c-145">The computer is locked and cannot be shut down without the force option.</span></span><br/> |
| <span data-ttu-id="0002c-146"><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)</span><span class="sxs-lookup"><span data-stu-id="0002c-146"><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)</span></span><br/>                                             | <span data-ttu-id="0002c-147">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="0002c-147">The device is not ready.</span></span><br/>                                                 |
| <span data-ttu-id="0002c-148"><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)</span><span class="sxs-lookup"><span data-stu-id="0002c-148"><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)</span></span><br/> | <span data-ttu-id="0002c-149">Выполняется завершение работы системы.</span><span class="sxs-lookup"><span data-stu-id="0002c-149">A system shutdown is in progress.</span></span><br/>                                        |



 

## <a name="requirements"></a><span data-ttu-id="0002c-150">Требования</span><span class="sxs-lookup"><span data-stu-id="0002c-150">Requirements</span></span>



| <span data-ttu-id="0002c-151">Требование</span><span class="sxs-lookup"><span data-stu-id="0002c-151">Requirement</span></span> | <span data-ttu-id="0002c-152">Значение</span><span class="sxs-lookup"><span data-stu-id="0002c-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0002c-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0002c-153">Minimum supported client</span></span><br/> | <span data-ttu-id="0002c-154">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0002c-154">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0002c-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0002c-155">Minimum supported server</span></span><br/> | <span data-ttu-id="0002c-156">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0002c-156">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0002c-157">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="0002c-157">End of client support</span></span><br/>    | <span data-ttu-id="0002c-158">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0002c-158">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0002c-159">Продукт</span><span class="sxs-lookup"><span data-stu-id="0002c-159">Product</span></span><br/>                  | <span data-ttu-id="0002c-160">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0002c-160">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0002c-161">Header</span><span class="sxs-lookup"><span data-stu-id="0002c-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="0002c-162"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="0002c-162"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0002c-163">IID</span><span class="sxs-lookup"><span data-stu-id="0002c-163">IID</span></span><br/>                      | <span data-ttu-id="0002c-164">IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="0002c-164">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="0002c-165">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0002c-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0002c-166">**ивмгуестос**</span><span class="sxs-lookup"><span data-stu-id="0002c-166">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

