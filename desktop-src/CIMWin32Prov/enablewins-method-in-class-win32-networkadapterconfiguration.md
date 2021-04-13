---
description: Свойство enablewins &\# 32; Статический метод класса WMI включает параметры Windows Internet Служба именования (WINS), относящиеся к TCP/IP, но не зависящие от сетевого адаптера.
ms.assetid: ce0fb170-978f-4d70-bced-e530e43da719
ms.tgt_platform: multiple
title: Метод свойство enablewins класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableWINS
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 77f5ba32606ff228908e8b7a1559a73ae5139e9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538693"
---
# <a name="enablewins-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="6cf39-103">Метод свойство enablewins \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="6cf39-103">EnableWINS method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="6cf39-104">Статический метод класса **свойство enablewins** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) включает параметры Windows Internet служба именования (WINS), относящиеся к TCP/IP, но не зависящие от сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="6cf39-104">The **EnableWINS** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method enables Windows Internet Naming Service (WINS) settings specific to TCP/IP, but independent of the network adapter.</span></span>

<span data-ttu-id="6cf39-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="6cf39-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6cf39-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6cf39-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6cf39-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6cf39-107">Syntax</span></span>


```mof
uint32 EnableWINS(
  [in]           boolean DNSEnabledForWINSResolution,
  [in]           boolean WINSEnableLMHostsLookup,
  [in, optional] string  WINSHostLookupFile,
  [in, optional] string  WINSScopeID
);
```



## <a name="parameters"></a><span data-ttu-id="6cf39-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6cf39-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cf39-109">*Днсенабледфорвинсресолутион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6cf39-109">*DNSEnabledForWINSResolution* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cf39-110">Если **значение — true**, система доменных имен (DNS) включает разрешение имен через разрешение WINS.</span><span class="sxs-lookup"><span data-stu-id="6cf39-110">If **true**, the Domain Name System (DNS) is enabled for name resolution over WINS resolution.</span></span>

</dd> <dt>

<span data-ttu-id="6cf39-111">*Винсенаблелмхостслукуп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6cf39-111">*WINSEnableLMHostsLookup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cf39-112">Если **значение — true**, используются локальные файлы поиска.</span><span class="sxs-lookup"><span data-stu-id="6cf39-112">If **true**, local lookup files are used.</span></span> <span data-ttu-id="6cf39-113">Файлы подстановок будут содержать сопоставления IP-адресов с именами узлов.</span><span class="sxs-lookup"><span data-stu-id="6cf39-113">Lookup files will contain mappings of IP addresses to host names.</span></span>

</dd> <dt>

<span data-ttu-id="6cf39-114">*Виншостлукупфиле* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="6cf39-114">*WINSHostLookupFile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6cf39-115">Файлы подстановок, содержащие сопоставления IP-адресов с именами узлов.</span><span class="sxs-lookup"><span data-stu-id="6cf39-115">Lookup files that contain mappings of IP addresses to host names.</span></span> <span data-ttu-id="6cf39-116">Если он доступен, файлы будут находиться в драйверах% SystemRoot \\ % \\ system32 \\ .</span><span class="sxs-lookup"><span data-stu-id="6cf39-116">If available, the files will be found in %SystemRoot%\\system32\\drivers\\ .</span></span>

</dd> <dt>

<span data-ttu-id="6cf39-117">*Винсскопеид* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="6cf39-117">*WINSScopeID* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6cf39-118">Значение идентификатора области, которое будет добавлено к концу NetBIOS-имени компьютера.</span><span class="sxs-lookup"><span data-stu-id="6cf39-118">Scope identifier value that will be appended to the end of the computer's NetBIOS name.</span></span> <span data-ttu-id="6cf39-119">Системы, использующие один и тот же идентификатор области, могут взаимодействовать с этим компьютером.</span><span class="sxs-lookup"><span data-stu-id="6cf39-119">Systems that use the same scope identifier can communicate with this computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cf39-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6cf39-120">Return value</span></span>

<span data-ttu-id="6cf39-121">Возвращает значение 0 (ноль) для успешного завершения, если перезагрузка не требуется. 1 (один) для успешного завершения, если требуется перезагрузка; другое число при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="6cf39-121">Returns a value of 0 (zero) for a successful completion when no reboot is required; 1 (one) for a successful completion when a reboot is required; a different number if there is an error.</span></span> <span data-ttu-id="6cf39-122">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="6cf39-122">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="6cf39-123">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="6cf39-123">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="6cf39-124">**Успешное завершение, перезагрузка не требуется** (0)</span><span class="sxs-lookup"><span data-stu-id="6cf39-124">**Successful completion, no reboot required** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-125">**Успешное завершение, требуется перезагрузка** (1)</span><span class="sxs-lookup"><span data-stu-id="6cf39-125">**Successful completion, reboot required** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-126">**Метод не поддерживается на этой платформе** (64)</span><span class="sxs-lookup"><span data-stu-id="6cf39-126">**Method not supported on this platform** (64)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-127">**Неизвестный сбой** (65)</span><span class="sxs-lookup"><span data-stu-id="6cf39-127">**Unknown failure** (65)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-128">**Недопустимая маска подсети** (66)</span><span class="sxs-lookup"><span data-stu-id="6cf39-128">**Invalid subnet mask** (66)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-129">Произошла **Ошибка при обработке возвращенного экземпляра** (67)</span><span class="sxs-lookup"><span data-stu-id="6cf39-129">**An error occurred while processing an Instance that was returned** (67)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-130">**Недопустимый входной параметр** (68)</span><span class="sxs-lookup"><span data-stu-id="6cf39-130">**Invalid input parameter** (68)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-131">**Указано более 5 шлюзов** (69)</span><span class="sxs-lookup"><span data-stu-id="6cf39-131">**More than 5 gateways specified** (69)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-132">**Недопустимый IP-адрес** (70)</span><span class="sxs-lookup"><span data-stu-id="6cf39-132">**Invalid IP address** (70)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-133">**Недопустимый IP-адрес шлюза** (71)</span><span class="sxs-lookup"><span data-stu-id="6cf39-133">**Invalid gateway IP address** (71)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-134">Произошла **Ошибка при доступе к реестру для запрашиваемой информации** (72)</span><span class="sxs-lookup"><span data-stu-id="6cf39-134">**An error occurred while accessing the Registry for the requested information** (72)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-135">**Недопустимое имя домена** (73)</span><span class="sxs-lookup"><span data-stu-id="6cf39-135">**Invalid domain name** (73)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-136">**Недопустимое имя узла** (74)</span><span class="sxs-lookup"><span data-stu-id="6cf39-136">**Invalid host name** (74)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-137">**Не определен основной или дополнительный WINS-сервер** (75)</span><span class="sxs-lookup"><span data-stu-id="6cf39-137">**No primary/secondary WINS server defined** (75)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-138">**Недопустимый файл** (76)</span><span class="sxs-lookup"><span data-stu-id="6cf39-138">**Invalid file** (76)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-139">**Недопустимый системный путь** (77)</span><span class="sxs-lookup"><span data-stu-id="6cf39-139">**Invalid system path** (77)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-140">**Не удалось скопировать файл** (78)</span><span class="sxs-lookup"><span data-stu-id="6cf39-140">**File copy failed** (78)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-141">**Недопустимый параметр безопасности** (79)</span><span class="sxs-lookup"><span data-stu-id="6cf39-141">**Invalid security parameter** (79)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-142">**Не удалось настроить службу TCP/IP** (80)</span><span class="sxs-lookup"><span data-stu-id="6cf39-142">**Unable to configure TCP/IP service** (80)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-143">**Не удалось настроить службу DHCP** (81)</span><span class="sxs-lookup"><span data-stu-id="6cf39-143">**Unable to configure DHCP service** (81)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-144">**Не удалось продлить аренду DHCP** (82)</span><span class="sxs-lookup"><span data-stu-id="6cf39-144">**Unable to renew DHCP lease** (82)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-145">**Не удалось освободить аренду DHCP** (83)</span><span class="sxs-lookup"><span data-stu-id="6cf39-145">**Unable to release DHCP lease** (83)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-146">**IP-адрес не включен на адаптере** (84)</span><span class="sxs-lookup"><span data-stu-id="6cf39-146">**IP not enabled on adapter** (84)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-147">**Протокол IPX не включен на адаптере** (85)</span><span class="sxs-lookup"><span data-stu-id="6cf39-147">**IPX not enabled on adapter** (85)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-148">**Ошибка границ кадра или сети** (86)</span><span class="sxs-lookup"><span data-stu-id="6cf39-148">**Frame/network number bounds error** (86)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-149">**Недопустимый тип кадра** (87)</span><span class="sxs-lookup"><span data-stu-id="6cf39-149">**Invalid frame type** (87)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-150">**Недопустимый номер сети** (88)</span><span class="sxs-lookup"><span data-stu-id="6cf39-150">**Invalid network number** (88)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-151">**Дублирующийся номер сети** (89)</span><span class="sxs-lookup"><span data-stu-id="6cf39-151">**Duplicate network number** (89)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-152">**Параметр вне** допустимых границ (90)</span><span class="sxs-lookup"><span data-stu-id="6cf39-152">**Parameter out of bounds** (90)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-153">**Отказано в доступе** (91)</span><span class="sxs-lookup"><span data-stu-id="6cf39-153">**Access denied** (91)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-154">**Недостаточно памяти** (92)</span><span class="sxs-lookup"><span data-stu-id="6cf39-154">**Out of memory** (92)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-155">**Уже существует** (93)</span><span class="sxs-lookup"><span data-stu-id="6cf39-155">**Already exists** (93)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-156">**Путь, файл или объект не найден** (94)</span><span class="sxs-lookup"><span data-stu-id="6cf39-156">**Path, file or object not found** (94)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-157">**Не удалось уведомить службу** (95)</span><span class="sxs-lookup"><span data-stu-id="6cf39-157">**Unable to notify service** (95)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-158">**Не удалось уведомить службу DNS** (96)</span><span class="sxs-lookup"><span data-stu-id="6cf39-158">**Unable to notify DNS service** (96)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-159">**Интерфейс не настраивается** (97)</span><span class="sxs-lookup"><span data-stu-id="6cf39-159">**Interface not configurable** (97)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-160">**Не все аренды DHCP могут быть освобождены или обновлены** (98)</span><span class="sxs-lookup"><span data-stu-id="6cf39-160">**Not all DHCP leases could be released/renewed** (98)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-161">**DHCP не включен на адаптере** (100)</span><span class="sxs-lookup"><span data-stu-id="6cf39-161">**DHCP not enabled on adapter** (100)</span></span>
</dt> <dt>

<span data-ttu-id="6cf39-162">**Другие** (101 4294967295)</span><span class="sxs-lookup"><span data-stu-id="6cf39-162">**Other** (101 4294967295)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="6cf39-163">Примеры</span><span class="sxs-lookup"><span data-stu-id="6cf39-163">Examples</span></span>

<span data-ttu-id="6cf39-164">Пример кода " [включить WINS для всех сетевых адаптеров](https://Gallery.TechNet.Microsoft.Com/64cae6dd-4155-4825-ab25-5727503edf5a) " в коллекции TechNet использует **свойство ENABLEWINS** для включения WINS на всех сетевых адаптерах, установленных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="6cf39-164">The [Enable WINS for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/64cae6dd-4155-4825-ab25-5727503edf5a) VBScript code sample, on TechNet Gallery, uses **EnableWINS** to Enables WINS on all the network adapters installed in a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cf39-165">Требования</span><span class="sxs-lookup"><span data-stu-id="6cf39-165">Requirements</span></span>



| <span data-ttu-id="6cf39-166">Требование</span><span class="sxs-lookup"><span data-stu-id="6cf39-166">Requirement</span></span> | <span data-ttu-id="6cf39-167">Значение</span><span class="sxs-lookup"><span data-stu-id="6cf39-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6cf39-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6cf39-168">Minimum supported client</span></span><br/> | <span data-ttu-id="6cf39-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6cf39-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6cf39-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6cf39-170">Minimum supported server</span></span><br/> | <span data-ttu-id="6cf39-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6cf39-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6cf39-172">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6cf39-172">Namespace</span></span><br/>                | <span data-ttu-id="6cf39-173">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6cf39-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6cf39-174">MOF</span><span class="sxs-lookup"><span data-stu-id="6cf39-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6cf39-175"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6cf39-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6cf39-176">DLL</span><span class="sxs-lookup"><span data-stu-id="6cf39-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cf39-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6cf39-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cf39-178">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6cf39-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cf39-179">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="6cf39-179">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="6cf39-180">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="6cf39-180">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="6cf39-181">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="6cf39-181">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="6cf39-182">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="6cf39-182">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="6cf39-183">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="6cf39-183">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

