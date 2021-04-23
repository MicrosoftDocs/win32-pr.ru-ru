---
description: Задает пары номеров или кадров сети протокола IPX для этого сетевого адаптера.
ms.assetid: 8190564f-7d9f-4b05-9949-2e732ce36dba
ms.tgt_platform: multiple
title: Метод Сетипксфраметипенетворкпаирс класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPXFrameTypeNetworkPairs
api_type:
- COM
api_location:
- cimwin32.dll
ms.openlocfilehash: e4d53ec7b5600a767505e517a02fbf87b5a43d13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142484"
---
# <a name="setipxframetypenetworkpairs-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="e962a-103">Метод Сетипксфраметипенетворкпаирс \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="e962a-103">SetIPXFrameTypeNetworkPairs method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="e962a-104">Задает пары номеров или кадров сети протокола IPX для этого сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="e962a-104">Sets the Internetworking Packet Exchange (IPX) network number/frame pairs for this network adapter.</span></span>

<span data-ttu-id="e962a-105">В Windows 2000 и Windows NT 3,51 и более поздних версиях для маршрутизации используется номер сети IPX.</span><span class="sxs-lookup"><span data-stu-id="e962a-105">Windows 2000 and Windows NT 3.51 and higher use an IPX network number for routing purposes.</span></span> <span data-ttu-id="e962a-106">Он назначается каждому настроенному сочетанию типа кадра или сетевого адаптера в компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="e962a-106">It is assigned to each configured frame type/network adapter combination on your computer system.</span></span> <span data-ttu-id="e962a-107">Этот номер иногда называют "номером внешней сети".</span><span class="sxs-lookup"><span data-stu-id="e962a-107">This number is sometimes referred to as the "external network number."</span></span> <span data-ttu-id="e962a-108">Оно должно быть уникальным для каждого сегмента сети.</span><span class="sxs-lookup"><span data-stu-id="e962a-108">It must be unique for each network segment.</span></span> <span data-ttu-id="e962a-109">Если для типа кадра задано значение Авто, то номер сети должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="e962a-109">If the frame type is set to AUTO, the network number should to zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="e962a-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e962a-110">Syntax</span></span>


```mof
uint32 SetIPXFrameTypeNetworkPairs(
  [in] string IPXNetworkNumber[],
  [in] uint32 IPXFrameType[]
);
```



## <a name="parameters"></a><span data-ttu-id="e962a-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="e962a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e962a-112">*Ипкснетворкнумбер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e962a-112">*IPXNetworkNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e962a-113">Массив символов, которые уникально идентифицируют адаптер в компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="e962a-113">An array of characters that uniquely identify an adapter on the computer system.</span></span> <span data-ttu-id="e962a-114">Транспорт связи NetWare (NWLink), совместимый с IPX/SPX в Windows 2000 и Windows NT 3,51 или более поздней версии, использует два разных типа сетевых номеров.</span><span class="sxs-lookup"><span data-stu-id="e962a-114">The NetWare Link (NWLink) IPX/SPX-compatible transport in Windows 2000 and Windows NT 3.51 or higher, uses two different types of network numbers.</span></span> <span data-ttu-id="e962a-115">Это число иногда называют номером внешней сети.</span><span class="sxs-lookup"><span data-stu-id="e962a-115">This number is sometimes referred to as the External Network Number.</span></span> <span data-ttu-id="e962a-116">Оно должно быть уникальным для каждого сегмента сети.</span><span class="sxs-lookup"><span data-stu-id="e962a-116">It must be unique for each network segment.</span></span> <span data-ttu-id="e962a-117">Значения в этом списке строк должны иметь соответствующее значение в параметре Ипксфраметипе, определяющем тип кадра пакетов, используемый для этой сети.</span><span class="sxs-lookup"><span data-stu-id="e962a-117">The values in this string list must have a corresponding value in the IPXFrameType parameter identifying the packet frame type used for this network.</span></span>

</dd> <dt>

<span data-ttu-id="e962a-118">*Ипксфраметипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e962a-118">*IPXFrameType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e962a-119">Целочисленный массив идентификаторов типов кадров.</span><span class="sxs-lookup"><span data-stu-id="e962a-119">An integer array of frame type identifiers.</span></span> <span data-ttu-id="e962a-120">Значения в этом массиве соответствуют элементам в параметре *ипкснетворкнумбер* .</span><span class="sxs-lookup"><span data-stu-id="e962a-120">The values in this array correspond to the elements in the *IPXNetworkNumber* parameter.</span></span>

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

<span data-ttu-id="e962a-121">**Ethernet II** (0)</span><span class="sxs-lookup"><span data-stu-id="e962a-121">**Ethernet II** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

<span data-ttu-id="e962a-122">**Ethernet 802,3** (1)</span><span class="sxs-lookup"><span data-stu-id="e962a-122">**Ethernet 802.3** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

<span data-ttu-id="e962a-123">**Ethernet 802,2** (2)</span><span class="sxs-lookup"><span data-stu-id="e962a-123">**Ethernet 802.2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

<span data-ttu-id="e962a-124">**Оснастка Ethernet** (3)</span><span class="sxs-lookup"><span data-stu-id="e962a-124">**Ethernet SNAP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

<span data-ttu-id="e962a-125">**Авто** (255)</span><span class="sxs-lookup"><span data-stu-id="e962a-125">**AUTO** (255)</span></span>


<span data-ttu-id="e962a-126"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e962a-126"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="e962a-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e962a-127">Return value</span></span>

<dl> <dt>

<span data-ttu-id="e962a-128">**Успешное завершение, перезагрузка не требуется** (0)</span><span class="sxs-lookup"><span data-stu-id="e962a-128">**Successful completion, no reboot required** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-129">**Успешное завершение, требуется перезагрузка** (1)</span><span class="sxs-lookup"><span data-stu-id="e962a-129">**Successful completion, reboot required** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-130">**Метод не поддерживается на этой платформе** (64)</span><span class="sxs-lookup"><span data-stu-id="e962a-130">**Method not supported on this platform** (64)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-131">**Неизвестный сбой** (65)</span><span class="sxs-lookup"><span data-stu-id="e962a-131">**Unknown failure** (65)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-132">**Недопустимая маска подсети** (66)</span><span class="sxs-lookup"><span data-stu-id="e962a-132">**Invalid subnet mask** (66)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-133">Произошла **Ошибка при обработке возвращенного экземпляра** (67)</span><span class="sxs-lookup"><span data-stu-id="e962a-133">**An error occurred while processing an Instance that was returned** (67)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-134">**Недопустимый входной параметр** (68)</span><span class="sxs-lookup"><span data-stu-id="e962a-134">**Invalid input parameter** (68)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-135">**Указано более 5 шлюзов** (69)</span><span class="sxs-lookup"><span data-stu-id="e962a-135">**More than 5 gateways specified** (69)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-136">**Недопустимый IP-адрес** (70)</span><span class="sxs-lookup"><span data-stu-id="e962a-136">**Invalid IP address** (70)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-137">**Недопустимый IP-адрес шлюза** (71)</span><span class="sxs-lookup"><span data-stu-id="e962a-137">**Invalid gateway IP address** (71)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-138">Произошла **Ошибка при доступе к реестру для запрашиваемой информации** (72)</span><span class="sxs-lookup"><span data-stu-id="e962a-138">**An error occurred while accessing the Registry for the requested information** (72)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-139">**Недопустимое имя домена** (73)</span><span class="sxs-lookup"><span data-stu-id="e962a-139">**Invalid domain name** (73)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-140">**Недопустимое имя узла** (74)</span><span class="sxs-lookup"><span data-stu-id="e962a-140">**Invalid host name** (74)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-141">**Не определен основной или дополнительный WINS-сервер** (75)</span><span class="sxs-lookup"><span data-stu-id="e962a-141">**No primary/secondary WINS server defined** (75)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-142">**Недопустимый файл** (76)</span><span class="sxs-lookup"><span data-stu-id="e962a-142">**Invalid file** (76)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-143">**Недопустимый системный путь** (77)</span><span class="sxs-lookup"><span data-stu-id="e962a-143">**Invalid system path** (77)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-144">**Не удалось скопировать файл** (78)</span><span class="sxs-lookup"><span data-stu-id="e962a-144">**File copy failed** (78)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-145">**Недопустимый параметр безопасности** (79)</span><span class="sxs-lookup"><span data-stu-id="e962a-145">**Invalid security parameter** (79)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-146">**Не удалось настроить службу TCP/IP** (80)</span><span class="sxs-lookup"><span data-stu-id="e962a-146">**Unable to configure TCP/IP service** (80)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-147">**Не удалось настроить службу DHCP** (81)</span><span class="sxs-lookup"><span data-stu-id="e962a-147">**Unable to configure DHCP service** (81)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-148">**Не удалось продлить аренду DHCP** (82)</span><span class="sxs-lookup"><span data-stu-id="e962a-148">**Unable to renew DHCP lease** (82)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-149">**Не удалось освободить аренду DHCP** (83)</span><span class="sxs-lookup"><span data-stu-id="e962a-149">**Unable to release DHCP lease** (83)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-150">**IP-адрес не включен на адаптере** (84)</span><span class="sxs-lookup"><span data-stu-id="e962a-150">**IP not enabled on adapter** (84)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-151">**Протокол IPX не включен на адаптере** (85)</span><span class="sxs-lookup"><span data-stu-id="e962a-151">**IPX not enabled on adapter** (85)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-152">**Ошибка границ кадра или сети** (86)</span><span class="sxs-lookup"><span data-stu-id="e962a-152">**Frame/network number bounds error** (86)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-153">**Недопустимый тип кадра** (87)</span><span class="sxs-lookup"><span data-stu-id="e962a-153">**Invalid frame type** (87)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-154">**Недопустимый номер сети** (88)</span><span class="sxs-lookup"><span data-stu-id="e962a-154">**Invalid network number** (88)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-155">**Дублирующийся номер сети** (89)</span><span class="sxs-lookup"><span data-stu-id="e962a-155">**Duplicate network number** (89)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-156">**Параметр вне** допустимых границ (90)</span><span class="sxs-lookup"><span data-stu-id="e962a-156">**Parameter out of bounds** (90)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-157">**Отказано в доступе** (91)</span><span class="sxs-lookup"><span data-stu-id="e962a-157">**Access denied** (91)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-158">**Недостаточно памяти** (92)</span><span class="sxs-lookup"><span data-stu-id="e962a-158">**Out of memory** (92)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-159">**Уже существует** (93)</span><span class="sxs-lookup"><span data-stu-id="e962a-159">**Already exists** (93)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-160">**Путь, файл или объект не найден** (94)</span><span class="sxs-lookup"><span data-stu-id="e962a-160">**Path, file or object not found** (94)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-161">**Не удалось уведомить службу** (95)</span><span class="sxs-lookup"><span data-stu-id="e962a-161">**Unable to notify service** (95)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-162">**Не удалось уведомить службу DNS** (96)</span><span class="sxs-lookup"><span data-stu-id="e962a-162">**Unable to notify DNS service** (96)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-163">**Интерфейс не настраивается** (97)</span><span class="sxs-lookup"><span data-stu-id="e962a-163">**Interface not configurable** (97)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-164">**Не все аренды DHCP могут быть освобождены или обновлены** (98)</span><span class="sxs-lookup"><span data-stu-id="e962a-164">**Not all DHCP leases could be released/renewed** (98)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-165">**DHCP не включен на адаптере** (100)</span><span class="sxs-lookup"><span data-stu-id="e962a-165">**DHCP not enabled on adapter** (100)</span></span>
</dt> <dt>

<span data-ttu-id="e962a-166">**Другое** (101 – 4294967295)</span><span class="sxs-lookup"><span data-stu-id="e962a-166">**Other** (101–4294967295)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e962a-167">Требования</span><span class="sxs-lookup"><span data-stu-id="e962a-167">Requirements</span></span>



| <span data-ttu-id="e962a-168">Требование</span><span class="sxs-lookup"><span data-stu-id="e962a-168">Requirement</span></span> | <span data-ttu-id="e962a-169">Значение</span><span class="sxs-lookup"><span data-stu-id="e962a-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e962a-170">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e962a-170">Minimum supported client</span></span><br/> | <span data-ttu-id="e962a-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e962a-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e962a-172">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e962a-172">Minimum supported server</span></span><br/> | <span data-ttu-id="e962a-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e962a-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e962a-174">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e962a-174">Namespace</span></span><br/>                | <span data-ttu-id="e962a-175">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e962a-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e962a-176">MOF</span><span class="sxs-lookup"><span data-stu-id="e962a-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e962a-177"><dt>CimWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e962a-177"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e962a-178">DLL</span><span class="sxs-lookup"><span data-stu-id="e962a-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e962a-179"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e962a-179"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e962a-180">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e962a-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e962a-181">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="e962a-181">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> </dl>

 

 




