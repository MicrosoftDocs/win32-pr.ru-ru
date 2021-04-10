---
title: Метод выхода из Ивмгуестос (Впккоминтерфацес. h)
description: Выполнит выход всех пользователей из операционной системы на виртуальной машине.
ms.assetid: 224aa7cb-0892-4e8a-84bd-78dd5cb724df
keywords:
- Метод выхода из Virtual PC
- Метод выхода из системы Virtual PC, интерфейс Ивмгуестос
- Ивмгуестос интерфейс Virtual PC, метод logoff
topic_type:
- apiref
api_name:
- IVMGuestOS.Logoff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20c67e917cc9ff93d162bc340185f426fe9eee3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071983"
---
# <a name="ivmguestoslogoff-method"></a><span data-ttu-id="df49c-106">Метод Ивмгуестос:: logoff</span><span class="sxs-lookup"><span data-stu-id="df49c-106">IVMGuestOS::Logoff method</span></span>

<span data-ttu-id="df49c-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="df49c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="df49c-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="df49c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="df49c-109">Выполнит выход всех пользователей из операционной системы на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="df49c-109">Logs off all users from the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="df49c-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df49c-110">Syntax</span></span>


```C++
HRESULT Logoff(
  [out, retval] IVMTask **outLogoffTask
);
```



## <a name="parameters"></a><span data-ttu-id="df49c-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="df49c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df49c-112">*аутлогоффтаск* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="df49c-112">*outLogoffTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="df49c-113">Объект [**ивмтаск**](ivmtask.md) , используемый для отслеживания хода выполнения последовательности выхода.</span><span class="sxs-lookup"><span data-stu-id="df49c-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the logoff sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df49c-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="df49c-114">Return value</span></span>

<span data-ttu-id="df49c-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="df49c-115">This method can return one of these values.</span></span>



| <span data-ttu-id="df49c-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="df49c-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="df49c-117">Описание</span><span class="sxs-lookup"><span data-stu-id="df49c-117">Description</span></span>                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="df49c-118"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="df49c-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="df49c-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="df49c-119">The operation was successful.</span></span><br/>                                                |
| <dl> <span data-ttu-id="df49c-120"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="df49c-120"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="df49c-121">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="df49c-121">An unexpected error has occurred.</span></span><br/>                                            |
| <dl> <span data-ttu-id="df49c-122"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="df49c-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="df49c-123">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="df49c-123">The parameter is **NULL**.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="df49c-124"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ \_ отказа в доступе)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="df49c-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="df49c-125">Вызывающий объект должен иметь разрешения на выполнение для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="df49c-125">The caller must have execute access permissions for this VM.</span></span><br/>                 |
| <dl> <span data-ttu-id="df49c-126"><dt>**Виртуальная машина \_ \_Истекло время \_ ожидания**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="df49c-126"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="df49c-127">Операция не завершилась своевременно.</span><span class="sxs-lookup"><span data-stu-id="df49c-127">The operation did not complete in a timely manner.</span></span><br/>                           |
| <dl> <span data-ttu-id="df49c-128"><dt>**Виртуальная машина \_ Добавление компонента "E" \_ \_ \_ не \_**</dt> доступно <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="df49c-128"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>       | <span data-ttu-id="df49c-129">Компонент интеграции компонентов не установлен на этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="df49c-129">The integration components feature is not installed in this virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="df49c-130"><dt>**Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="df49c-130"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="df49c-131">Для этой операции должна быть запущена виртуальная машина (ВМ).</span><span class="sxs-lookup"><span data-stu-id="df49c-131">The virtual machine (VM) must be running for this operation.</span></span><br/>                 |
| <dl> <span data-ttu-id="df49c-132"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="df49c-132"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="df49c-133">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="df49c-133">The configuration is unknown.</span></span><br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="df49c-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="df49c-134">Remarks</span></span>

<span data-ttu-id="df49c-135">`HRESULT_FROM_WIN32(ERROR_NO_SUCH_LOGON_SESSION)` (0x80070520) возвращается с помощью свойства [**Error**](ivmtask-error.md) возвращенного объекта [**ивмтаск**](ivmtask.md) в гостевой операционной системе нет сеансов входа в систему.</span><span class="sxs-lookup"><span data-stu-id="df49c-135">`HRESULT_FROM_WIN32(ERROR_NO_SUCH_LOGON_SESSION)` (0x80070520) is returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object there are no logon sessions in the guest operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="df49c-136">Требования</span><span class="sxs-lookup"><span data-stu-id="df49c-136">Requirements</span></span>



| <span data-ttu-id="df49c-137">Требование</span><span class="sxs-lookup"><span data-stu-id="df49c-137">Requirement</span></span> | <span data-ttu-id="df49c-138">Значение</span><span class="sxs-lookup"><span data-stu-id="df49c-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="df49c-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="df49c-139">Minimum supported client</span></span><br/> | <span data-ttu-id="df49c-140">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="df49c-140">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="df49c-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="df49c-141">Minimum supported server</span></span><br/> | <span data-ttu-id="df49c-142">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="df49c-142">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="df49c-143">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="df49c-143">End of client support</span></span><br/>    | <span data-ttu-id="df49c-144">Windows 7</span><span class="sxs-lookup"><span data-stu-id="df49c-144">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="df49c-145">Продукт</span><span class="sxs-lookup"><span data-stu-id="df49c-145">Product</span></span><br/>                  | <span data-ttu-id="df49c-146">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="df49c-146">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="df49c-147">Header</span><span class="sxs-lookup"><span data-stu-id="df49c-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="df49c-148"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="df49c-148"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="df49c-149">IID</span><span class="sxs-lookup"><span data-stu-id="df49c-149">IID</span></span><br/>                      | <span data-ttu-id="df49c-150">IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="df49c-150">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="df49c-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df49c-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df49c-152">**ивмгуестос**</span><span class="sxs-lookup"><span data-stu-id="df49c-152">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

