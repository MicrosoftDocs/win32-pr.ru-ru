---
description: Сетднссерверсеарчордер &\# 32; Метод класса WMI использует массив строковых элементов для задания порядка поиска сервера.
ms.assetid: fce688fa-7264-4965-8e1c-138160e03a7e
ms.tgt_platform: multiple
title: Метод Сетднссерверсеарчордер класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDNSServerSearchOrder
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2bfe731ea1d89e8e0ad702bfa229a61fba30dfc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072488"
---
# <a name="setdnsserversearchorder-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="e2804-103">Метод Сетднссерверсеарчордер \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2804-103">SetDNSServerSearchOrder method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="e2804-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) сетднссерверсеарчордер использует массив строковых элементов для задания порядка поиска сервера.</span><span class="sxs-lookup"><span data-stu-id="e2804-104">The **SetDNSServerSearchOrder** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uses an array of string elements to set the server search order.</span></span>

<span data-ttu-id="e2804-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="e2804-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e2804-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e2804-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e2804-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2804-107">Syntax</span></span>


```mof
uint32 SetDNSServerSearchOrder(
  [in] string DNSServerSearchOrder[]
);
```



## <a name="parameters"></a><span data-ttu-id="e2804-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2804-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2804-109">*Днссерверсеарчордер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e2804-109">*DNSServerSearchOrder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2804-110">Список IP-адресов серверов для запроса DNS-серверов.</span><span class="sxs-lookup"><span data-stu-id="e2804-110">List of server IP addresses to query for DNS servers.</span></span>

<span data-ttu-id="e2804-111">Пример: 130.215.24.1 или 157.54.164.1</span><span class="sxs-lookup"><span data-stu-id="e2804-111">Example: 130.215.24.1 or 157.54.164.1</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2804-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e2804-112">Return value</span></span>

<span data-ttu-id="e2804-113">Возвращает значение 0 (ноль) для успешного завершения, если не требуется перезагрузка, 1 (один) для успешного завершения, когда требуется перезагрузка, и другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="e2804-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="e2804-114">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="e2804-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="e2804-115">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="e2804-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="e2804-116">**Успешное завершение, перезагрузка не требуется** (0)</span><span class="sxs-lookup"><span data-stu-id="e2804-116">**Successful completion, no reboot required** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-117">**Успешное завершение, требуется перезагрузка** (1)</span><span class="sxs-lookup"><span data-stu-id="e2804-117">**Successful completion, reboot required** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-118">**Метод не поддерживается на этой платформе** (64)</span><span class="sxs-lookup"><span data-stu-id="e2804-118">**Method not supported on this platform** (64)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-119">**Неизвестный сбой** (65)</span><span class="sxs-lookup"><span data-stu-id="e2804-119">**Unknown failure** (65)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-120">**Недопустимая маска подсети** (66)</span><span class="sxs-lookup"><span data-stu-id="e2804-120">**Invalid subnet mask** (66)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-121">Произошла **Ошибка при обработке возвращенного экземпляра** (67)</span><span class="sxs-lookup"><span data-stu-id="e2804-121">**An error occurred while processing an Instance that was returned** (67)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-122">**Недопустимый входной параметр** (68)</span><span class="sxs-lookup"><span data-stu-id="e2804-122">**Invalid input parameter** (68)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-123">**Указано более 5 шлюзов** (69)</span><span class="sxs-lookup"><span data-stu-id="e2804-123">**More than 5 gateways specified** (69)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-124">**Недопустимый IP-адрес** (70)</span><span class="sxs-lookup"><span data-stu-id="e2804-124">**Invalid IP address** (70)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-125">**Недопустимый IP-адрес шлюза** (71)</span><span class="sxs-lookup"><span data-stu-id="e2804-125">**Invalid gateway IP address** (71)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-126">Произошла **Ошибка при доступе к реестру для запрашиваемой информации** (72)</span><span class="sxs-lookup"><span data-stu-id="e2804-126">**An error occurred while accessing the Registry for the requested information** (72)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-127">**Недопустимое имя домена** (73)</span><span class="sxs-lookup"><span data-stu-id="e2804-127">**Invalid domain name** (73)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-128">**Недопустимое имя узла** (74)</span><span class="sxs-lookup"><span data-stu-id="e2804-128">**Invalid host name** (74)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-129">**Не определен основной или дополнительный WINS-сервер** (75)</span><span class="sxs-lookup"><span data-stu-id="e2804-129">**No primary/secondary WINS server defined** (75)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-130">**Недопустимый файл** (76)</span><span class="sxs-lookup"><span data-stu-id="e2804-130">**Invalid file** (76)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-131">**Недопустимый системный путь** (77)</span><span class="sxs-lookup"><span data-stu-id="e2804-131">**Invalid system path** (77)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-132">**Не удалось скопировать файл** (78)</span><span class="sxs-lookup"><span data-stu-id="e2804-132">**File copy failed** (78)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-133">**Недопустимый параметр безопасности** (79)</span><span class="sxs-lookup"><span data-stu-id="e2804-133">**Invalid security parameter** (79)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-134">**Не удалось настроить службу TCP/IP** (80)</span><span class="sxs-lookup"><span data-stu-id="e2804-134">**Unable to configure TCP/IP service** (80)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-135">**Не удалось настроить службу DHCP** (81)</span><span class="sxs-lookup"><span data-stu-id="e2804-135">**Unable to configure DHCP service** (81)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-136">**Не удалось продлить аренду DHCP** (82)</span><span class="sxs-lookup"><span data-stu-id="e2804-136">**Unable to renew DHCP lease** (82)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-137">**Не удалось освободить аренду DHCP** (83)</span><span class="sxs-lookup"><span data-stu-id="e2804-137">**Unable to release DHCP lease** (83)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-138">**IP-адрес не включен на адаптере** (84)</span><span class="sxs-lookup"><span data-stu-id="e2804-138">**IP not enabled on adapter** (84)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-139">**Протокол IPX не включен на адаптере** (85)</span><span class="sxs-lookup"><span data-stu-id="e2804-139">**IPX not enabled on adapter** (85)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-140">**Ошибка границ кадра или сети** (86)</span><span class="sxs-lookup"><span data-stu-id="e2804-140">**Frame/network number bounds error** (86)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-141">**Недопустимый тип кадра** (87)</span><span class="sxs-lookup"><span data-stu-id="e2804-141">**Invalid frame type** (87)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-142">**Недопустимый номер сети** (88)</span><span class="sxs-lookup"><span data-stu-id="e2804-142">**Invalid network number** (88)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-143">**Дублирующийся номер сети** (89)</span><span class="sxs-lookup"><span data-stu-id="e2804-143">**Duplicate network number** (89)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-144">**Параметр вне** допустимых границ (90)</span><span class="sxs-lookup"><span data-stu-id="e2804-144">**Parameter out of bounds** (90)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-145">**Отказано в доступе** (91)</span><span class="sxs-lookup"><span data-stu-id="e2804-145">**Access denied** (91)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-146">**Недостаточно памяти** (92)</span><span class="sxs-lookup"><span data-stu-id="e2804-146">**Out of memory** (92)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-147">**Уже существует** (93)</span><span class="sxs-lookup"><span data-stu-id="e2804-147">**Already exists** (93)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-148">**Путь, файл или объект не найден** (94)</span><span class="sxs-lookup"><span data-stu-id="e2804-148">**Path, file or object not found** (94)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-149">**Не удалось уведомить службу** (95)</span><span class="sxs-lookup"><span data-stu-id="e2804-149">**Unable to notify service** (95)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-150">**Не удалось уведомить службу DNS** (96)</span><span class="sxs-lookup"><span data-stu-id="e2804-150">**Unable to notify DNS service** (96)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-151">**Интерфейс не настраивается** (97)</span><span class="sxs-lookup"><span data-stu-id="e2804-151">**Interface not configurable** (97)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-152">**Не все аренды DHCP могут быть освобождены или обновлены** (98)</span><span class="sxs-lookup"><span data-stu-id="e2804-152">**Not all DHCP leases could be released/renewed** (98)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-153">**DHCP не включен на адаптере** (100)</span><span class="sxs-lookup"><span data-stu-id="e2804-153">**DHCP not enabled on adapter** (100)</span></span>
</dt> <dt>

<span data-ttu-id="e2804-154">**Другие** (101 4294967295)</span><span class="sxs-lookup"><span data-stu-id="e2804-154">**Other** (101 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="e2804-155">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e2804-155">Remarks</span></span>

<span data-ttu-id="e2804-156">Это зависящий от экземпляра вызов метода, который применяется для каждого адаптера.</span><span class="sxs-lookup"><span data-stu-id="e2804-156">This is an instance-dependent method call that applies on a per-adapter basis.</span></span> <span data-ttu-id="e2804-157">После указания статических DNS-серверов для запуска с использованием протокола DHCP вместо статических DNS-серверов можно вызвать метод без указания параметров In.</span><span class="sxs-lookup"><span data-stu-id="e2804-157">After static DNS servers are specified to start using Dynamic Host Configuration Protocol (DHCP) instead of static DNS servers, you can call the method without supplying "in" parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="e2804-158">Примеры</span><span class="sxs-lookup"><span data-stu-id="e2804-158">Examples</span></span>

<span data-ttu-id="e2804-159">В примере " [Настройка порядка поиска DNS-серверов для нескольких компьютеров в](https://Gallery.TechNet.Microsoft.Com/Set-DNS-Server-Search-6a3e3ede) коллекции TechNet" в галерее можно получить или задать порядок поиска на DNS-сервере для нескольких компьютеров, принадлежащих одному подразделению.</span><span class="sxs-lookup"><span data-stu-id="e2804-159">The [Set DNS Server Search Order for Multiple Computers in an Organizational Unit](https://Gallery.TechNet.Microsoft.Com/Set-DNS-Server-Search-6a3e3ede) VBScript sample on TechNet Gallery retrieves or sets DNS Server search order for multiple computers that belongs to one organizational unit.</span></span>

<span data-ttu-id="e2804-160">Пример [изменения порядка поиска DNS-серверов для сетевого адаптера](https://Gallery.TechNet.Microsoft.Com/7824348c-5a92-42cb-b4e9-ef2187702e02) VBScript настраивает сетевой адаптер, привязанный к TCP/IP, для использования двух DNS-серверов.</span><span class="sxs-lookup"><span data-stu-id="e2804-160">The [Modify the DNS Server Search Order for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/7824348c-5a92-42cb-b4e9-ef2187702e02) VBScript sample configures a TCP/IP-bound network adapter to use two DNS servers.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2804-161">Требования</span><span class="sxs-lookup"><span data-stu-id="e2804-161">Requirements</span></span>



| <span data-ttu-id="e2804-162">Требование</span><span class="sxs-lookup"><span data-stu-id="e2804-162">Requirement</span></span> | <span data-ttu-id="e2804-163">Значение</span><span class="sxs-lookup"><span data-stu-id="e2804-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2804-164">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2804-164">Minimum supported client</span></span><br/> | <span data-ttu-id="e2804-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e2804-165">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e2804-166">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2804-166">Minimum supported server</span></span><br/> | <span data-ttu-id="e2804-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2804-167">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e2804-168">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e2804-168">Namespace</span></span><br/>                | <span data-ttu-id="e2804-169">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e2804-169">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e2804-170">MOF</span><span class="sxs-lookup"><span data-stu-id="e2804-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2804-171"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2804-171"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2804-172">DLL</span><span class="sxs-lookup"><span data-stu-id="e2804-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2804-173"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2804-173"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2804-174">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2804-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2804-175">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="e2804-175">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="e2804-176">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="e2804-176">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="e2804-177">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="e2804-177">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="e2804-178">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="e2804-178">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="e2804-179">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="e2804-179">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

