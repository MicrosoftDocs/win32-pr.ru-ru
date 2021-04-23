---
description: Статический метод класса Енабледнс WMI включает систему доменных имен (DNS) для службы.
ms.assetid: 083dccb1-eb38-4ae5-a252-0001759c0f50
ms.tgt_platform: multiple
title: Метод Енабледнс класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableDNS
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: fc217211455d8804de47b2b3ffc761d4328fa49a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141331"
---
# <a name="enabledns-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="1e32f-103">Метод Енабледнс \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e32f-103">EnableDNS method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="1e32f-104">Статический метод класса **енабледнс** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) включает систему доменных имен (DNS) для службы.</span><span class="sxs-lookup"><span data-stu-id="1e32f-104">The **EnableDNS** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method enables the Domain Name System (DNS) for service.</span></span>

<span data-ttu-id="1e32f-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="1e32f-105">This topic uses the Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1e32f-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1e32f-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1e32f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e32f-107">Syntax</span></span>


```mof
uint32 EnableDNS(
  [in, optional] string DNSHostName,
  [in, optional] string DNSDomain,
  [in, optional] string DNSServerSearchOrder[],
  [in, optional] string DNSDomainSuffixSearchOrder[]
);
```



## <a name="parameters"></a><span data-ttu-id="1e32f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1e32f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e32f-109">*DNSHostName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="1e32f-109">*DNSHostName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-110">Имя DNS-узла, который включает этот метод.</span><span class="sxs-lookup"><span data-stu-id="1e32f-110">Name of the DNS host that this method enables.</span></span>

<span data-ttu-id="1e32f-111">Пример: "корпднс"</span><span class="sxs-lookup"><span data-stu-id="1e32f-111">Example: "corpdns"</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-112">*Днсдомаин* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="1e32f-112">*DNSDomain* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-113">Представляет название организации, за которой следует точка и расширение, указывающее тип организации.</span><span class="sxs-lookup"><span data-stu-id="1e32f-113">Represents an organization name followed by a period and an extension that indicates the type of organization.</span></span>

<span data-ttu-id="1e32f-114">Пример: "microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="1e32f-114">Example: "microsoft.com"</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-115">*Днссерверсеарчордер* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="1e32f-115">*DNSServerSearchOrder* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-116">Список IP-адресов серверов для запроса DNS-серверов.</span><span class="sxs-lookup"><span data-stu-id="1e32f-116">List of server IP addresses to query for DNS servers.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-117">*Днсдомаинсуффикссеарчордер* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="1e32f-117">*DNSDomainSuffixSearchOrder* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-118">DNS-суффикс домена, добавляемый к имени узла во время разрешения имени.</span><span class="sxs-lookup"><span data-stu-id="1e32f-118">DNS domain suffix that is appended to a host name during name resolution.</span></span> <span data-ttu-id="1e32f-119">При разрешении полного доменного имени (FQDN) из имени только для узла система добавляет имя локального домена.</span><span class="sxs-lookup"><span data-stu-id="1e32f-119">When resolving a fully qualified domain name (FQDN) from a host-only name, the system appends the local domain name.</span></span> <span data-ttu-id="1e32f-120">Если разрешение имен не прошло успешно, система использует список суффиксов доменов для создания дополнительных полных доменных имен в указанном порядке, а затем запрашивает DNS-серверы для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="1e32f-120">If the name resolution is not successful, the system uses the domain suffix list to create additional FQDNs in the order listed, and then queries DNS servers for each one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e32f-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1e32f-121">Return value</span></span>

<span data-ttu-id="1e32f-122">Возвращает значение 0 (ноль) для успешного завершения, если перезагрузка не требуется, 1 (один) для успешного завершения, когда требуется перезагрузка, и любое другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="1e32f-122">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="1e32f-123">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="1e32f-123">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="1e32f-124">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="1e32f-124">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="1e32f-125">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="1e32f-125">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-126">0</span><span class="sxs-lookup"><span data-stu-id="1e32f-126">0</span></span>

<span data-ttu-id="1e32f-127">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="1e32f-127">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-128">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="1e32f-128">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-129">1</span><span class="sxs-lookup"><span data-stu-id="1e32f-129">1</span></span>

<span data-ttu-id="1e32f-130">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="1e32f-130">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-131">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="1e32f-131">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-132">64</span><span class="sxs-lookup"><span data-stu-id="1e32f-132">64</span></span>

<span data-ttu-id="1e32f-133">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="1e32f-133">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-134">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="1e32f-134">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-135">65</span><span class="sxs-lookup"><span data-stu-id="1e32f-135">65</span></span>

<span data-ttu-id="1e32f-136">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="1e32f-136">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-137">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="1e32f-137">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-138">66</span><span class="sxs-lookup"><span data-stu-id="1e32f-138">66</span></span>

<span data-ttu-id="1e32f-139">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="1e32f-139">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-140">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="1e32f-140">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-141">67</span><span class="sxs-lookup"><span data-stu-id="1e32f-141">67</span></span>

<span data-ttu-id="1e32f-142">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1e32f-142">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-143">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="1e32f-143">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-144">68</span><span class="sxs-lookup"><span data-stu-id="1e32f-144">68</span></span>

<span data-ttu-id="1e32f-145">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="1e32f-145">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-146">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="1e32f-146">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-147">69</span><span class="sxs-lookup"><span data-stu-id="1e32f-147">69</span></span>

<span data-ttu-id="1e32f-148">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="1e32f-148">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-149">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="1e32f-149">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-150">70</span><span class="sxs-lookup"><span data-stu-id="1e32f-150">70</span></span>

<span data-ttu-id="1e32f-151">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="1e32f-151">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-152">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="1e32f-152">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-153">71</span><span class="sxs-lookup"><span data-stu-id="1e32f-153">71</span></span>

<span data-ttu-id="1e32f-154">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="1e32f-154">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-155">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="1e32f-155">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-156">72</span><span class="sxs-lookup"><span data-stu-id="1e32f-156">72</span></span>

<span data-ttu-id="1e32f-157">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="1e32f-157">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-158">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="1e32f-158">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-159">73</span><span class="sxs-lookup"><span data-stu-id="1e32f-159">73</span></span>

<span data-ttu-id="1e32f-160">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="1e32f-160">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-161">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="1e32f-161">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-162">74</span><span class="sxs-lookup"><span data-stu-id="1e32f-162">74</span></span>

<span data-ttu-id="1e32f-163">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="1e32f-163">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-164">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="1e32f-164">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-165">75</span><span class="sxs-lookup"><span data-stu-id="1e32f-165">75</span></span>

<span data-ttu-id="1e32f-166">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="1e32f-166">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-167">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="1e32f-167">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-168">76</span><span class="sxs-lookup"><span data-stu-id="1e32f-168">76</span></span>

<span data-ttu-id="1e32f-169">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="1e32f-169">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-170">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="1e32f-170">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-171">77</span><span class="sxs-lookup"><span data-stu-id="1e32f-171">77</span></span>

<span data-ttu-id="1e32f-172">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="1e32f-172">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-173">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="1e32f-173">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-174">78</span><span class="sxs-lookup"><span data-stu-id="1e32f-174">78</span></span>

<span data-ttu-id="1e32f-175">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="1e32f-175">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-176">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="1e32f-176">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-177">79</span><span class="sxs-lookup"><span data-stu-id="1e32f-177">79</span></span>

<span data-ttu-id="1e32f-178">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="1e32f-178">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-179">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="1e32f-179">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-180">80</span><span class="sxs-lookup"><span data-stu-id="1e32f-180">80</span></span>

<span data-ttu-id="1e32f-181">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="1e32f-181">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-182">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="1e32f-182">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-183">81</span><span class="sxs-lookup"><span data-stu-id="1e32f-183">81</span></span>

<span data-ttu-id="1e32f-184">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="1e32f-184">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-185">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="1e32f-185">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-186">82</span><span class="sxs-lookup"><span data-stu-id="1e32f-186">82</span></span>

<span data-ttu-id="1e32f-187">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="1e32f-187">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-188">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="1e32f-188">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-189">83</span><span class="sxs-lookup"><span data-stu-id="1e32f-189">83</span></span>

<span data-ttu-id="1e32f-190">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="1e32f-190">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-191">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="1e32f-191">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-192">84</span><span class="sxs-lookup"><span data-stu-id="1e32f-192">84</span></span>

<span data-ttu-id="1e32f-193">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="1e32f-193">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-194">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="1e32f-194">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-195">85</span><span class="sxs-lookup"><span data-stu-id="1e32f-195">85</span></span>

<span data-ttu-id="1e32f-196">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="1e32f-196">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-197">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="1e32f-197">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-198">86</span><span class="sxs-lookup"><span data-stu-id="1e32f-198">86</span></span>

<span data-ttu-id="1e32f-199">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="1e32f-199">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-200">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="1e32f-200">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-201">87</span><span class="sxs-lookup"><span data-stu-id="1e32f-201">87</span></span>

<span data-ttu-id="1e32f-202">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="1e32f-202">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-203">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="1e32f-203">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-204">88</span><span class="sxs-lookup"><span data-stu-id="1e32f-204">88</span></span>

<span data-ttu-id="1e32f-205">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="1e32f-205">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-206">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="1e32f-206">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-207">89</span><span class="sxs-lookup"><span data-stu-id="1e32f-207">89</span></span>

<span data-ttu-id="1e32f-208">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="1e32f-208">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-209">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="1e32f-209">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-210">90</span><span class="sxs-lookup"><span data-stu-id="1e32f-210">90</span></span>

<span data-ttu-id="1e32f-211">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="1e32f-211">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-212">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="1e32f-212">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-213">91</span><span class="sxs-lookup"><span data-stu-id="1e32f-213">91</span></span>

<span data-ttu-id="1e32f-214">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="1e32f-214">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-215">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="1e32f-215">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-216">92</span><span class="sxs-lookup"><span data-stu-id="1e32f-216">92</span></span>

<span data-ttu-id="1e32f-217">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="1e32f-217">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-218">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="1e32f-218">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-219">93</span><span class="sxs-lookup"><span data-stu-id="1e32f-219">93</span></span>

<span data-ttu-id="1e32f-220">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="1e32f-220">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-221">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="1e32f-221">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-222">94</span><span class="sxs-lookup"><span data-stu-id="1e32f-222">94</span></span>

<span data-ttu-id="1e32f-223">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="1e32f-223">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-224">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="1e32f-224">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-225">95</span><span class="sxs-lookup"><span data-stu-id="1e32f-225">95</span></span>

<span data-ttu-id="1e32f-226">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="1e32f-226">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-227">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="1e32f-227">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-228">96</span><span class="sxs-lookup"><span data-stu-id="1e32f-228">96</span></span>

<span data-ttu-id="1e32f-229">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="1e32f-229">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-230">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="1e32f-230">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-231">97</span><span class="sxs-lookup"><span data-stu-id="1e32f-231">97</span></span>

<span data-ttu-id="1e32f-232">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="1e32f-232">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-233">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="1e32f-233">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-234">98</span><span class="sxs-lookup"><span data-stu-id="1e32f-234">98</span></span>

<span data-ttu-id="1e32f-235">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="1e32f-235">Not all DHCP leases can be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-236">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="1e32f-236">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-237">100</span><span class="sxs-lookup"><span data-stu-id="1e32f-237">100</span></span>

<span data-ttu-id="1e32f-238">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="1e32f-238">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="1e32f-239">**Другое**</span><span class="sxs-lookup"><span data-stu-id="1e32f-239">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="1e32f-240">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="1e32f-240">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="1e32f-241">Примеры</span><span class="sxs-lookup"><span data-stu-id="1e32f-241">Examples</span></span>

<span data-ttu-id="1e32f-242">Следующий пример кода, взятый из примера включения кода VBScript для [всех сетевых адаптеров](https://Gallery.TechNet.Microsoft.Com/c5736a48-71cc-4483-9605-d71d222740ac) в коллекции TechNet, включает DNS для всех сетевых адаптеров на компьютере.</span><span class="sxs-lookup"><span data-stu-id="1e32f-242">The following code sample, taken from the [Enable DNS on All Network Adapters](https://Gallery.TechNet.Microsoft.Com/c5736a48-71cc-4483-9605-d71d222740ac) VBScript code sample on TechNet Gallery, enables DNS for all network adapters on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objNetworkSettings = objWMIService.Get("Win32_NetworkAdapterConfiguration") 
strHostName = "fabrikam1" 
arrDNSSuffixes = Array("hr.fabrikam.com", "research.fabrikam.com") 
objNetworkSettings.EnableDNS strHostName, , , arrDNSSuffixes 
```



## <a name="requirements"></a><span data-ttu-id="1e32f-243">Требования</span><span class="sxs-lookup"><span data-stu-id="1e32f-243">Requirements</span></span>



| <span data-ttu-id="1e32f-244">Требование</span><span class="sxs-lookup"><span data-stu-id="1e32f-244">Requirement</span></span> | <span data-ttu-id="1e32f-245">Значение</span><span class="sxs-lookup"><span data-stu-id="1e32f-245">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e32f-246">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1e32f-246">Minimum supported client</span></span><br/> | <span data-ttu-id="1e32f-247">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e32f-247">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1e32f-248">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1e32f-248">Minimum supported server</span></span><br/> | <span data-ttu-id="1e32f-249">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e32f-249">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1e32f-250">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1e32f-250">Namespace</span></span><br/>                | <span data-ttu-id="1e32f-251">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1e32f-251">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1e32f-252">MOF</span><span class="sxs-lookup"><span data-stu-id="1e32f-252">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e32f-253"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e32f-253"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e32f-254">DLL</span><span class="sxs-lookup"><span data-stu-id="1e32f-254">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e32f-255"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e32f-255"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e32f-256">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e32f-256">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e32f-257">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="1e32f-257">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="1e32f-258">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="1e32f-258">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="1e32f-259">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="1e32f-259">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="1e32f-260">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="1e32f-260">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="1e32f-261">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="1e32f-261">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

