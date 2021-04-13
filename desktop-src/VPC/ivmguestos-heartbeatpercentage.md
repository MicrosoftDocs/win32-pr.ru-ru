---
title: Свойство Хеартбеатперцентаже Ивмгуестос (Впккоминтерфацес. h)
description: Процент ожидаемых тактов, полученных за последнюю минуту.
ms.assetid: 456dd8ae-e946-429d-98aa-5773362fdd4e
keywords:
- Хеартбеатперцентаже свойство Virtual PC
- Хеартбеатперцентаже свойство Virtual PC, интерфейс Ивмгуестос
- Ивмгуестос интерфейс Virtual PC, свойство Хеартбеатперцентаже
topic_type:
- apiref
api_name:
- IVMGuestOS.HeartbeatPercentage
- IVMGuestOS.get_HeartbeatPercentage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22d568ed85281e8940b69afd1c72e76e2f208a5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535186"
---
# <a name="ivmguestosheartbeatpercentage-property"></a><span data-ttu-id="9402c-106">Свойство Ивмгуестос:: Хеартбеатперцентаже</span><span class="sxs-lookup"><span data-stu-id="9402c-106">IVMGuestOS::HeartbeatPercentage property</span></span>

<span data-ttu-id="9402c-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9402c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9402c-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9402c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9402c-109">Возвращает процент ожидаемых периодических сигналов, полученных за последнюю минуту.</span><span class="sxs-lookup"><span data-stu-id="9402c-109">Retrieves the percentage of expected heartbeats received over the past minute.</span></span>

<span data-ttu-id="9402c-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9402c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9402c-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9402c-111">Syntax</span></span>


```C++
HRESULT get_HeartbeatPercentage(
  [out, retval] long *heartbeatPercentage
);
```



## <a name="property-value"></a><span data-ttu-id="9402c-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9402c-112">Property value</span></span>

<span data-ttu-id="9402c-113">Процент ожидаемых периодических сигналов, полученных за последнюю минуту.</span><span class="sxs-lookup"><span data-stu-id="9402c-113">The percentage of expected heartbeats received over the past minute.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9402c-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="9402c-114">Error codes</span></span>



| <span data-ttu-id="9402c-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="9402c-115">Name/value</span></span>                                                                                                                                                              | <span data-ttu-id="9402c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="9402c-116">Meaning</span></span>                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9402c-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9402c-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="9402c-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="9402c-118">The operation was successful.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="9402c-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="9402c-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                   | <span data-ttu-id="9402c-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="9402c-120">The parameter is **NULL**.</span></span><br/>                                                                                                               |
| <dl> <span data-ttu-id="9402c-121"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="9402c-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="9402c-122">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="9402c-122">The configuration is unknown.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="9402c-123"><dt>Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="9402c-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>      | <span data-ttu-id="9402c-124">Для этой операции должна быть запущена виртуальная машина (ВМ).</span><span class="sxs-lookup"><span data-stu-id="9402c-124">The virtual machine (VM) must be running for this operation.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="9402c-125"><dt>Виртуальная машина \_ \_ \_ \_ </dt> <dt>Не0xA0040504ные</dt> дополнения</span><span class="sxs-lookup"><span data-stu-id="9402c-125"><dt>VM\_E\_ADDITIONS\_NOT\_AVAIL</dt> <dt>0xA0040504</dt></span></span> </dl> | <span data-ttu-id="9402c-126">Виртуальная машина не полностью загружена, компонент интеграции не установлен, или установленная версия не поддерживает эту функцию.</span><span class="sxs-lookup"><span data-stu-id="9402c-126">The VM is not fully booted, the integration components feature is not installed, or the installed version does not support this feature.</span></span><br/> |
| <dl> <span data-ttu-id="9402c-127"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="9402c-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="9402c-128">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="9402c-128">An unexpected error has occurred.</span></span><br/>                                                                                                        |



## <a name="remarks"></a><span data-ttu-id="9402c-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9402c-129">Remarks</span></span>

<span data-ttu-id="9402c-130">Компоненты интеграции будут отсылать периодический пульс на виртуальный ПК Windows, пока выполняется гостевая операционная система.</span><span class="sxs-lookup"><span data-stu-id="9402c-130">Integration components will send a periodic heartbeat to Windows Virtual PC while the guest operating system is running.</span></span> <span data-ttu-id="9402c-131">Если операционная система на виртуальной машине сильно загружена, возможно, Windows Virtual PC будет принимать меньше периодических сигналов, чем ожидалось.</span><span class="sxs-lookup"><span data-stu-id="9402c-131">If the guest operating system is heavily loaded, it's possible that Windows Virtual PC will receive fewer heartbeats than expected.</span></span> <span data-ttu-id="9402c-132">Если процент пульса падает до нуля, возможно, что гостевая операционная система не отвечает на запросы или происходит сбой.</span><span class="sxs-lookup"><span data-stu-id="9402c-132">If the heartbeat percentage drops to zero, it is possible that the guest operating system is not responding or is crashed.</span></span> <span data-ttu-id="9402c-133">Виртуальная машина должна быть запущена (то есть полностью загружена и не завершается), а компоненты интеграции должны быть установлены при вызове этого свойства.</span><span class="sxs-lookup"><span data-stu-id="9402c-133">The virtual machine must be running (that is, fully booted and not shutting down) and integration components must be installed when this property is invoked.</span></span>

## <a name="requirements"></a><span data-ttu-id="9402c-134">Требования</span><span class="sxs-lookup"><span data-stu-id="9402c-134">Requirements</span></span>



| <span data-ttu-id="9402c-135">Требование</span><span class="sxs-lookup"><span data-stu-id="9402c-135">Requirement</span></span> | <span data-ttu-id="9402c-136">Значение</span><span class="sxs-lookup"><span data-stu-id="9402c-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9402c-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9402c-137">Minimum supported client</span></span><br/> | <span data-ttu-id="9402c-138">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9402c-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9402c-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9402c-139">Minimum supported server</span></span><br/> | <span data-ttu-id="9402c-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9402c-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9402c-141">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="9402c-141">End of client support</span></span><br/>    | <span data-ttu-id="9402c-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9402c-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9402c-143">Продукт</span><span class="sxs-lookup"><span data-stu-id="9402c-143">Product</span></span><br/>                  | <span data-ttu-id="9402c-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9402c-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9402c-145">Header</span><span class="sxs-lookup"><span data-stu-id="9402c-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="9402c-146"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="9402c-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9402c-147">IID</span><span class="sxs-lookup"><span data-stu-id="9402c-147">IID</span></span><br/>                      | <span data-ttu-id="9402c-148">IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="9402c-148">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="9402c-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9402c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9402c-150">**ивмгуестос**</span><span class="sxs-lookup"><span data-stu-id="9402c-150">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

