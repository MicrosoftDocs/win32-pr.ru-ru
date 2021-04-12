---
title: Метод Restart Ивмгуестос (Впккоминтерфацес. h)
description: Перезапускает операционную систему на виртуальной машине.
ms.assetid: 328c7aa1-d9bd-452d-95dd-9f6a03fa8c9e
keywords:
- Метод Restart Virtual PC
- Метод Restart Virtual PC, интерфейс Ивмгуестос
- Ивмгуестос интерфейс Virtual PC, метод Restart
topic_type:
- apiref
api_name:
- IVMGuestOS.Restart
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 110718e45d04445dd895a2bdb27419fbd24731c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415628"
---
# <a name="ivmguestosrestart-method"></a><span data-ttu-id="4fcf1-106">Метод Ивмгуестос:: Restart</span><span class="sxs-lookup"><span data-stu-id="4fcf1-106">IVMGuestOS::Restart method</span></span>

<span data-ttu-id="4fcf1-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4fcf1-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4fcf1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4fcf1-109">Перезапускает операционную систему на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-109">Restarts the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fcf1-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4fcf1-110">Syntax</span></span>


```C++
HRESULT Restart(
  [in]          VARIANT_BOOL inForced,
  [out, retval] IVMTask      **outRestartTask
);
```



## <a name="parameters"></a><span data-ttu-id="4fcf1-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="4fcf1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fcf1-112">не *принудительно* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4fcf1-112">*inForced* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fcf1-113">**Вариант \_ Значение TRUE** , если требуется Принудительная перезагрузка, и значение **Variant \_ false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-113">**VARIANT\_TRUE** if a forced restart is required and **VARIANT\_FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="4fcf1-114">*аутрестарттаск* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="4fcf1-114">*outRestartTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4fcf1-115">Объект [**ивмтаск**](ivmtask.md) , используемый для отслеживания хода выполнения последовательности перезапуска.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-115">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the restart sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fcf1-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4fcf1-116">Return value</span></span>

<span data-ttu-id="4fcf1-117">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-117">This method can return one of these values.</span></span>



| <span data-ttu-id="4fcf1-118">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="4fcf1-118">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="4fcf1-119">Описание</span><span class="sxs-lookup"><span data-stu-id="4fcf1-119">Description</span></span>                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4fcf1-120"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4fcf1-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="4fcf1-121">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-121">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="4fcf1-122"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="4fcf1-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="4fcf1-123">Параметр *аутрестарттаск* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-123">The *outRestartTask* parameter is **NULL**.</span></span><br/>                     |
| <dl> <span data-ttu-id="4fcf1-124"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4fcf1-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="4fcf1-125">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-125">An unexpected error has occurred.</span></span><br/>                               |
| <dl> <span data-ttu-id="4fcf1-126"><dt>**Виртуальная машина \_ \_Истекло время \_ ожидания**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="4fcf1-126"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="4fcf1-127">Операция не завершилась своевременно.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-127">The operation did not complete in a timely manner.</span></span><br/>              |
| <dl> <span data-ttu-id="4fcf1-128"><dt>**Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="4fcf1-128"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="4fcf1-129">Для этой операции должна быть запущена виртуальная машина (ВМ).</span><span class="sxs-lookup"><span data-stu-id="4fcf1-129">The virtual machine (VM) must be running for this operation.</span></span><br/>    |
| <dl> <span data-ttu-id="4fcf1-130"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4fcf1-130"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                    | <span data-ttu-id="4fcf1-131">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-131">The configuration is unknown.</span></span><br/>                                   |
| <dl> <span data-ttu-id="4fcf1-132"><dt>**Виртуальная машина \_ Добавление компонента "E" \_ \_ \_ не \_**</dt> доступно <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="4fcf1-132"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="4fcf1-133">Компонент интеграции компонентов не установлен на этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-133">The integration components feature is not installed in this VM.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4fcf1-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4fcf1-134">Remarks</span></span>

<span data-ttu-id="4fcf1-135">Следующие значения можно возвратить с помощью свойства [**Error**](ivmtask-error.md) возвращенного объекта [**ивмтаск**](ivmtask.md) .</span><span class="sxs-lookup"><span data-stu-id="4fcf1-135">The following values can be returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object.</span></span>



| <span data-ttu-id="4fcf1-136">Код [**ошибки**](ivmtask-error.md) /значение</span><span class="sxs-lookup"><span data-stu-id="4fcf1-136">[**Error**](ivmtask-error.md) code/Value</span></span>                                                                                                                                                                                                                                                                          | <span data-ttu-id="4fcf1-137">Описание</span><span class="sxs-lookup"><span data-stu-id="4fcf1-137">Description</span></span>                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4fcf1-138"><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` 0x80070005</span><span class="sxs-lookup"><span data-stu-id="4fcf1-138"><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` (0x80070005)</span></span><br/>                             | <span data-ttu-id="4fcf1-139">Вызывающий объект должен иметь разрешения на выполнение для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-139">The caller must have execute access permissions for this VM.</span></span><br/>             |
| <span data-ttu-id="4fcf1-140"><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7)</span><span class="sxs-lookup"><span data-stu-id="4fcf1-140"><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7)</span></span><br/>                         | <span data-ttu-id="4fcf1-141">Компьютер заблокирован и не может завершить работу без параметра Force.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-141">The computer is locked and cannot be shut down without the force option.</span></span><br/> |
| <span data-ttu-id="4fcf1-142"><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)</span><span class="sxs-lookup"><span data-stu-id="4fcf1-142"><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)</span></span><br/>                                             | <span data-ttu-id="4fcf1-143">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-143">The device is not ready.</span></span><br/>                                                 |
| <span data-ttu-id="4fcf1-144"><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)</span><span class="sxs-lookup"><span data-stu-id="4fcf1-144"><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)</span></span><br/> | <span data-ttu-id="4fcf1-145">Выполняется завершение работы системы.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-145">A system shutdown is in progress.</span></span><br/>                                        |



 

## <a name="requirements"></a><span data-ttu-id="4fcf1-146">Требования</span><span class="sxs-lookup"><span data-stu-id="4fcf1-146">Requirements</span></span>



| <span data-ttu-id="4fcf1-147">Требование</span><span class="sxs-lookup"><span data-stu-id="4fcf1-147">Requirement</span></span> | <span data-ttu-id="4fcf1-148">Значение</span><span class="sxs-lookup"><span data-stu-id="4fcf1-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fcf1-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4fcf1-149">Minimum supported client</span></span><br/> | <span data-ttu-id="4fcf1-150">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4fcf1-150">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4fcf1-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4fcf1-151">Minimum supported server</span></span><br/> | <span data-ttu-id="4fcf1-152">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4fcf1-152">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4fcf1-153">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="4fcf1-153">End of client support</span></span><br/>    | <span data-ttu-id="4fcf1-154">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4fcf1-154">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4fcf1-155">Продукт</span><span class="sxs-lookup"><span data-stu-id="4fcf1-155">Product</span></span><br/>                  | <span data-ttu-id="4fcf1-156">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4fcf1-156">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4fcf1-157">Header</span><span class="sxs-lookup"><span data-stu-id="4fcf1-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fcf1-158"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fcf1-158"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4fcf1-159">IID</span><span class="sxs-lookup"><span data-stu-id="4fcf1-159">IID</span></span><br/>                      | <span data-ttu-id="4fcf1-160">IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="4fcf1-160">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="4fcf1-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4fcf1-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fcf1-162">**ивмгуестос**</span><span class="sxs-lookup"><span data-stu-id="4fcf1-162">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

