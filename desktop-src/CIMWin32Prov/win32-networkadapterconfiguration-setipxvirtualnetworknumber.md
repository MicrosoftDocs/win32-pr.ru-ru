---
description: Задает номер виртуальной сети сетевого обмена пакетами (IPX) на целевом компьютере.
ms.assetid: 52064250-b94f-4dc0-bf1a-8601cd135a90
ms.tgt_platform: multiple
title: Метод Сетипксвиртуалнетворкнумбер класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPXVirtualNetworkNumber
api_type:
- COM
api_location:
- cimwin32.dll
ms.openlocfilehash: ed6e6802a17ef6ec4393d2ae0c5ec43f0e21d247
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656020"
---
# <a name="setipxvirtualnetworknumber-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="d095a-103">Метод Сетипксвиртуалнетворкнумбер \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="d095a-103">SetIPXVirtualNetworkNumber method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="d095a-104">Задает номер виртуальной сети сетевого обмена пакетами (IPX) на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="d095a-104">Sets the Internetworking Packet Exchange (IPX) virtual network number on the target computer system.</span></span> <span data-ttu-id="d095a-105">В Windows 2000 и Windows NT 3,51 или более поздней версии используется внутренний номер сети для внутренней маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="d095a-105">Windows 2000 and Windows NT 3.51 or greater uses an internal network number for internal routing.</span></span> <span data-ttu-id="d095a-106">Номер внутренней сети также известен как номер виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d095a-106">The internal network number is also known as a virtual network number.</span></span> <span data-ttu-id="d095a-107">Он однозначно определяет компьютерную систему в сети.</span><span class="sxs-lookup"><span data-stu-id="d095a-107">It uniquely identifies the computer system on the network.</span></span> <span data-ttu-id="d095a-108">Метод возвращает целочисленное значение, которое можно интерпреттед следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d095a-108">The method returns an integer value that can be interpretted as follows:</span></span>

## <a name="syntax"></a><span data-ttu-id="d095a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d095a-109">Syntax</span></span>


```mof
uint32 SetIPXVirtualNetworkNumber(
  [in] string IPXVirtualNetNumber
);
```



## <a name="parameters"></a><span data-ttu-id="d095a-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d095a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d095a-111">*Ипксвиртуалнетнумбер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d095a-111">*IPXVirtualNetNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d095a-112">Номер виртуальной сети для этой системы.</span><span class="sxs-lookup"><span data-stu-id="d095a-112">The virtual network number for this system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d095a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d095a-113">Return value</span></span>

<dl> <dt>

<span data-ttu-id="d095a-114">**Успешное завершение, перезагрузка не требуется** (0)</span><span class="sxs-lookup"><span data-stu-id="d095a-114">**Successful completion, no reboot required** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-115">**Успешное завершение, требуется перезагрузка** (1)</span><span class="sxs-lookup"><span data-stu-id="d095a-115">**Successful completion, reboot required** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-116">**Метод не поддерживается на этой платформе** (64)</span><span class="sxs-lookup"><span data-stu-id="d095a-116">**Method not supported on this platform** (64)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-117">**Неизвестный сбой** (65)</span><span class="sxs-lookup"><span data-stu-id="d095a-117">**Unknown failure** (65)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-118">**Недопустимая маска подсети** (66)</span><span class="sxs-lookup"><span data-stu-id="d095a-118">**Invalid subnet mask** (66)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-119">Произошла **Ошибка при обработке возвращенного экземпляра** (67)</span><span class="sxs-lookup"><span data-stu-id="d095a-119">**An error occurred while processing an Instance that was returned** (67)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-120">**Недопустимый входной параметр** (68)</span><span class="sxs-lookup"><span data-stu-id="d095a-120">**Invalid input parameter** (68)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-121">**Указано более 5 шлюзов** (69)</span><span class="sxs-lookup"><span data-stu-id="d095a-121">**More than 5 gateways specified** (69)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-122">**Недопустимый IP-адрес** (70)</span><span class="sxs-lookup"><span data-stu-id="d095a-122">**Invalid IP address** (70)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-123">**Недопустимый IP-адрес шлюза** (71)</span><span class="sxs-lookup"><span data-stu-id="d095a-123">**Invalid gateway IP address** (71)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-124">Произошла **Ошибка при доступе к реестру для запрашиваемой информации** (72)</span><span class="sxs-lookup"><span data-stu-id="d095a-124">**An error occurred while accessing the Registry for the requested information** (72)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-125">**Недопустимое имя домена** (73)</span><span class="sxs-lookup"><span data-stu-id="d095a-125">**Invalid domain name** (73)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-126">**Недопустимое имя узла** (74)</span><span class="sxs-lookup"><span data-stu-id="d095a-126">**Invalid host name** (74)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-127">**Не определен основной или дополнительный WINS-сервер** (75)</span><span class="sxs-lookup"><span data-stu-id="d095a-127">**No primary/secondary WINS server defined** (75)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-128">**Недопустимый файл** (76)</span><span class="sxs-lookup"><span data-stu-id="d095a-128">**Invalid file** (76)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-129">**Недопустимый системный путь** (77)</span><span class="sxs-lookup"><span data-stu-id="d095a-129">**Invalid system path** (77)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-130">**Не удалось скопировать файл** (78)</span><span class="sxs-lookup"><span data-stu-id="d095a-130">**File copy failed** (78)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-131">**Недопустимый параметр безопасности** (79)</span><span class="sxs-lookup"><span data-stu-id="d095a-131">**Invalid security parameter** (79)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-132">**Не удалось настроить службу TCP/IP** (80)</span><span class="sxs-lookup"><span data-stu-id="d095a-132">**Unable to configure TCP/IP service** (80)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-133">**Не удалось настроить службу DHCP** (81)</span><span class="sxs-lookup"><span data-stu-id="d095a-133">**Unable to configure DHCP service** (81)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-134">**Не удалось продлить аренду DHCP** (82)</span><span class="sxs-lookup"><span data-stu-id="d095a-134">**Unable to renew DHCP lease** (82)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-135">**Не удалось освободить аренду DHCP** (83)</span><span class="sxs-lookup"><span data-stu-id="d095a-135">**Unable to release DHCP lease** (83)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-136">**IP-адрес не включен на адаптере** (84)</span><span class="sxs-lookup"><span data-stu-id="d095a-136">**IP not enabled on adapter** (84)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-137">**Протокол IPX не включен на адаптере** (85)</span><span class="sxs-lookup"><span data-stu-id="d095a-137">**IPX not enabled on adapter** (85)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-138">**Ошибка границ кадра или сети** (86)</span><span class="sxs-lookup"><span data-stu-id="d095a-138">**Frame/network number bounds error** (86)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-139">**Недопустимый тип кадра** (87)</span><span class="sxs-lookup"><span data-stu-id="d095a-139">**Invalid frame type** (87)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-140">**Недопустимый номер сети** (88)</span><span class="sxs-lookup"><span data-stu-id="d095a-140">**Invalid network number** (88)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-141">**Дублирующийся номер сети** (89)</span><span class="sxs-lookup"><span data-stu-id="d095a-141">**Duplicate network number** (89)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-142">**Параметр вне** допустимых границ (90)</span><span class="sxs-lookup"><span data-stu-id="d095a-142">**Parameter out of bounds** (90)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-143">**Отказано в доступе** (91)</span><span class="sxs-lookup"><span data-stu-id="d095a-143">**Access denied** (91)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-144">**Недостаточно памяти** (92)</span><span class="sxs-lookup"><span data-stu-id="d095a-144">**Out of memory** (92)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-145">**Уже существует** (93)</span><span class="sxs-lookup"><span data-stu-id="d095a-145">**Already exists** (93)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-146">**Путь, файл или объект не найден** (94)</span><span class="sxs-lookup"><span data-stu-id="d095a-146">**Path, file or object not found** (94)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-147">**Не удалось уведомить службу** (95)</span><span class="sxs-lookup"><span data-stu-id="d095a-147">**Unable to notify service** (95)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-148">**Не удалось уведомить службу DNS** (96)</span><span class="sxs-lookup"><span data-stu-id="d095a-148">**Unable to notify DNS service** (96)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-149">**Интерфейс не настраивается** (97)</span><span class="sxs-lookup"><span data-stu-id="d095a-149">**Interface not configurable** (97)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-150">**Не все аренды DHCP могут быть освобождены или обновлены** (98)</span><span class="sxs-lookup"><span data-stu-id="d095a-150">**Not all DHCP leases could be released/renewed** (98)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-151">**DHCP не включен на адаптере** (100)</span><span class="sxs-lookup"><span data-stu-id="d095a-151">**DHCP not enabled on adapter** (100)</span></span>
</dt> <dt>

<span data-ttu-id="d095a-152">**Другое** (101 – 4294967295)</span><span class="sxs-lookup"><span data-stu-id="d095a-152">**Other** (101–4294967295)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d095a-153">Требования</span><span class="sxs-lookup"><span data-stu-id="d095a-153">Requirements</span></span>



| <span data-ttu-id="d095a-154">Требование</span><span class="sxs-lookup"><span data-stu-id="d095a-154">Requirement</span></span> | <span data-ttu-id="d095a-155">Значение</span><span class="sxs-lookup"><span data-stu-id="d095a-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d095a-156">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d095a-156">Minimum supported client</span></span><br/> | <span data-ttu-id="d095a-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d095a-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d095a-158">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d095a-158">Minimum supported server</span></span><br/> | <span data-ttu-id="d095a-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d095a-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d095a-160">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d095a-160">Namespace</span></span><br/>                | <span data-ttu-id="d095a-161">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d095a-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d095a-162">MOF</span><span class="sxs-lookup"><span data-stu-id="d095a-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d095a-163"><dt>CimWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d095a-163"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d095a-164">DLL</span><span class="sxs-lookup"><span data-stu-id="d095a-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d095a-165"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d095a-165"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d095a-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d095a-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d095a-167">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="d095a-167">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> </dl>

 

 




