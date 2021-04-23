---
title: Свойство Ивмгуестос-пульса (Впккоминтерфацес. h)
description: Определяет, имеет ли виртуальная машина пульс.
ms.assetid: b1697a7b-6119-47aa-b261-6009f5287993
keywords:
- Свойство пульса Virtual PC
- Свойство пульса Virtual PC, интерфейс Ивмгуестос
- Ивмгуестос интерфейс Virtual PC, свойство "Пульс"
topic_type:
- apiref
api_name:
- IVMGuestOS.IsHeartbeating
- IVMGuestOS.get_IsHeartbeating
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faad446749cbf3cdb75d6e8fa7469022cc004ea7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691949"
---
# <a name="ivmguestosisheartbeating-property"></a><span data-ttu-id="88256-106">Свойство Ивмгуестос::</span><span class="sxs-lookup"><span data-stu-id="88256-106">IVMGuestOS::IsHeartbeating property</span></span>

<span data-ttu-id="88256-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="88256-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="88256-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="88256-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="88256-109">Определяет, имеет ли виртуальная машина пульс.</span><span class="sxs-lookup"><span data-stu-id="88256-109">Determines whether the virtual machine has a heartbeat.</span></span>

<span data-ttu-id="88256-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="88256-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="88256-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88256-111">Syntax</span></span>


```C++
HRESULT get_IsHeartbeating(
  [out, retval] VARIANT_BOOL *heartBeating
);
```



## <a name="property-value"></a><span data-ttu-id="88256-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="88256-112">Property value</span></span>

<span data-ttu-id="88256-113">**Вариант \_ Значение TRUE** , если период пульса обнаружен; в противном случае — значение **\_ false** .</span><span class="sxs-lookup"><span data-stu-id="88256-113">**VARIANT\_TRUE** if a heartbeat is detected, **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="88256-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="88256-114">Error codes</span></span>



| <span data-ttu-id="88256-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="88256-115">Name/value</span></span>                                                                                                                                                              | <span data-ttu-id="88256-116">Значение</span><span class="sxs-lookup"><span data-stu-id="88256-116">Meaning</span></span>                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="88256-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="88256-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="88256-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="88256-118">The operation was successful.</span></span><br/>                                                                                                                         |
| <dl> <span data-ttu-id="88256-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="88256-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                   | <span data-ttu-id="88256-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="88256-120">The parameter is **NULL**.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="88256-121"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="88256-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="88256-122">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="88256-122">The configuration is unknown.</span></span><br/>                                                                                                                         |
| <dl> <span data-ttu-id="88256-123"><dt>Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="88256-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>      | <span data-ttu-id="88256-124">Для этой операции должна быть запущена виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="88256-124">The virtual machine must be running for this operation.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="88256-125"><dt>Виртуальная машина \_ \_ \_ \_ </dt> <dt>Не0xA0040504ные</dt> дополнения</span><span class="sxs-lookup"><span data-stu-id="88256-125"><dt>VM\_E\_ADDITIONS\_NOT\_AVAIL</dt> <dt>0xA0040504</dt></span></span> </dl> | <span data-ttu-id="88256-126">Виртуальная машина не полностью загружена, компонент интеграции не установлен, или установленная версия не поддерживает эту функцию.</span><span class="sxs-lookup"><span data-stu-id="88256-126">The virtual machine is not fully booted, the integration components feature is not installed, or the installed version does not support this feature.</span></span><br/> |
| <dl> <span data-ttu-id="88256-127"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="88256-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="88256-128">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="88256-128">An unexpected error has occurred.</span></span><br/>                                                                                                                     |



## <a name="remarks"></a><span data-ttu-id="88256-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="88256-129">Remarks</span></span>

<span data-ttu-id="88256-130">Когда компоненты интеграции устанавливаются в гостевой операционной системе, в сеансе виртуальной машины в Windows Virtual PC отправляется обычный такт или пульс.</span><span class="sxs-lookup"><span data-stu-id="88256-130">When integration components is installed in the guest operating system, a regular 'tick' or heartbeat is sent from the virtual machine session to Windows Virtual PC.</span></span> <span data-ttu-id="88256-131">Если операционная система на виртуальной машине сильно загружена, возможно, виртуальная машина будет принимать меньше периодических сигналов, чем ожидалось.</span><span class="sxs-lookup"><span data-stu-id="88256-131">If the guest operating system is heavily loaded, it's possible that Virtual PC will receive fewer heartbeats than expected.</span></span> <span data-ttu-id="88256-132">Если пульс не обнаружен, возможно, что гостевая операционная система не отвечает на запросы или происходит сбой.</span><span class="sxs-lookup"><span data-stu-id="88256-132">If no heartbeat is detected, it is possible that the guest operating system is not responding or is crashed.</span></span>

<span data-ttu-id="88256-133">По умолчанию виртуальная машина выдает десять тактов пульса в минуту.</span><span class="sxs-lookup"><span data-stu-id="88256-133">By default, a virtual machine produces ten heartbeat ticks per minute.</span></span> <span data-ttu-id="88256-134">Если тактовые импульсы не обнаруживаются в течение всей минуты, Windows Virtual PC попытается перезапустить сеанс виртуальной машины каждые десять секунд в течение двух минут.</span><span class="sxs-lookup"><span data-stu-id="88256-134">If no heartbeat ticks are detected for an entire minute, Windows Virtual PC will attempt to restart the virtual machine session once every ten seconds for up to two minutes.</span></span> <span data-ttu-id="88256-135">Это поведение управляется следующими значениями ключей в файле конфигурации сеанса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="88256-135">This behavior is controlled by the following key values in the virtual machine session's configuration file.</span></span>



| <span data-ttu-id="88256-136">Ключ конфигурации</span><span class="sxs-lookup"><span data-stu-id="88256-136">Configuration key</span></span>                                            | <span data-ttu-id="88256-137">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="88256-137">Default</span></span>       | <span data-ttu-id="88256-138">Описание</span><span class="sxs-lookup"><span data-stu-id="88256-138">Description</span></span>                                                                                                                             |
|--------------------------------------------------------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88256-139">интеграция/Microsoft/пульс/время</span><span class="sxs-lookup"><span data-stu-id="88256-139">integration/microsoft/heartbeat/time</span></span><br/>              | <span data-ttu-id="88256-140">60</span><span class="sxs-lookup"><span data-stu-id="88256-140">60</span></span><br/> | <span data-ttu-id="88256-141">Длина блока времени, используемого для создания тактов пульса в секундах.</span><span class="sxs-lookup"><span data-stu-id="88256-141">The length of the block of time used to generate heartbeat ticks, in in seconds.</span></span><br/>                                             |
| <span data-ttu-id="88256-142">интеграция/Microsoft/пульс/ставка</span><span class="sxs-lookup"><span data-stu-id="88256-142">integration/microsoft/heartbeat/rate</span></span><br/>              | <span data-ttu-id="88256-143">10</span><span class="sxs-lookup"><span data-stu-id="88256-143">10</span></span><br/> | <span data-ttu-id="88256-144">Число тактов, созданных в каждом блоке времени пульса.</span><span class="sxs-lookup"><span data-stu-id="88256-144">The number of ticks generated in each heartbeat time block.</span></span><br/>                                                                  |
| <span data-ttu-id="88256-145">интеграция/Microsoft/пульс/ \_ интервал сбоев</span><span class="sxs-lookup"><span data-stu-id="88256-145">integration/microsoft/heartbeat/failure\_interval</span></span><br/> | <span data-ttu-id="88256-146">10</span><span class="sxs-lookup"><span data-stu-id="88256-146">10</span></span><br/> | <span data-ttu-id="88256-147">Время в секундах между попытками перезапуска, по истечении которого тактовые импульсы не будут получены в течение определенного блока времени пульса.</span><span class="sxs-lookup"><span data-stu-id="88256-147">The number of seconds between restart attempts, once no heartbeat ticks are received within a specific heartbeat time block.</span></span><br/> |
| <span data-ttu-id="88256-148">интеграция/Microsoft/пульс/неудачные \_ попытки</span><span class="sxs-lookup"><span data-stu-id="88256-148">integration/microsoft/heartbeat/failure\_attempts</span></span><br/> | <span data-ttu-id="88256-149">12</span><span class="sxs-lookup"><span data-stu-id="88256-149">12</span></span><br/> | <span data-ttu-id="88256-150">Число выполненных попыток перезапуска.</span><span class="sxs-lookup"><span data-stu-id="88256-150">The number of restart attempts made.</span></span><br/>                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="88256-151">Требования</span><span class="sxs-lookup"><span data-stu-id="88256-151">Requirements</span></span>



| <span data-ttu-id="88256-152">Требование</span><span class="sxs-lookup"><span data-stu-id="88256-152">Requirement</span></span> | <span data-ttu-id="88256-153">Значение</span><span class="sxs-lookup"><span data-stu-id="88256-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="88256-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="88256-154">Minimum supported client</span></span><br/> | <span data-ttu-id="88256-155">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="88256-155">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="88256-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="88256-156">Minimum supported server</span></span><br/> | <span data-ttu-id="88256-157">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="88256-157">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="88256-158">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="88256-158">End of client support</span></span><br/>    | <span data-ttu-id="88256-159">Windows 7</span><span class="sxs-lookup"><span data-stu-id="88256-159">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="88256-160">Продукт</span><span class="sxs-lookup"><span data-stu-id="88256-160">Product</span></span><br/>                  | <span data-ttu-id="88256-161">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="88256-161">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="88256-162">Header</span><span class="sxs-lookup"><span data-stu-id="88256-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="88256-163"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="88256-163"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="88256-164">IID</span><span class="sxs-lookup"><span data-stu-id="88256-164">IID</span></span><br/>                      | <span data-ttu-id="88256-165">IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="88256-165">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="88256-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="88256-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88256-167">**ивмгуестос**</span><span class="sxs-lookup"><span data-stu-id="88256-167">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

