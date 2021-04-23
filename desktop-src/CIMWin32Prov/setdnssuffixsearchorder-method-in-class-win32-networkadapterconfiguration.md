---
description: Статический метод класса Сетднссуффикссеарчордер WMI использует массив строковых элементов для задания порядка поиска суффиксов.
ms.assetid: 1ad9fc99-8c57-43d4-92d2-b12f2c1451cb
ms.tgt_platform: multiple
title: Метод Сетднссуффикссеарчордер класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDNSSuffixSearchOrder
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 10088b1d0722f968e5d3742984baa91ec3e423aa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896150"
---
# <a name="setdnssuffixsearchorder-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="9ba08-103">Метод Сетднссуффикссеарчордер \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="9ba08-103">SetDNSSuffixSearchOrder method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="9ba08-104">Статический метод класса **сетднссуффикссеарчордер** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) использует массив строковых элементов для задания порядка поиска суффиксов.</span><span class="sxs-lookup"><span data-stu-id="9ba08-104">The **SetDNSSuffixSearchOrder** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method uses an array of string elements to set the suffix search order.</span></span>

<span data-ttu-id="9ba08-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="9ba08-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9ba08-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9ba08-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9ba08-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ba08-107">Syntax</span></span>


```mof
uint32 SetDNSSuffixSearchOrder(
  [in] string DNSDomainSuffixSearchOrder[]
);
```



## <a name="parameters"></a><span data-ttu-id="9ba08-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9ba08-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ba08-109">*Днсдомаинсуффикссеарчордер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9ba08-109">*DNSDomainSuffixSearchOrder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-110">Список суффиксов сервера для запроса DNS-серверов.</span><span class="sxs-lookup"><span data-stu-id="9ba08-110">List of server suffixes to query for DNS servers.</span></span> <span data-ttu-id="9ba08-111">В реестре DNS-суффикса находится путь к папке **hKey \_ Local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **tcpip \| nameserver** .</span><span class="sxs-lookup"><span data-stu-id="9ba08-111">The registry location of the DNS suffix is **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**Tcpip\|NameServer**</span></span>

<span data-ttu-id="9ba08-112">Пример: "suffix1.company.com", "suffix2.company.com"</span><span class="sxs-lookup"><span data-stu-id="9ba08-112">Example: "suffix1.company.com", "suffix2.company.com"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ba08-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9ba08-113">Return value</span></span>

<span data-ttu-id="9ba08-114">Возвращает значение 0 (ноль) для успешного завершения, если не требуется перезагрузка, 1 (один) для успешного завершения, когда требуется перезагрузка, и другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="9ba08-114">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="9ba08-115">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="9ba08-115">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="9ba08-116">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="9ba08-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="9ba08-117">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="9ba08-117">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-118">0</span><span class="sxs-lookup"><span data-stu-id="9ba08-118">0</span></span>

<span data-ttu-id="9ba08-119">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="9ba08-119">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-120">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="9ba08-120">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-121">1</span><span class="sxs-lookup"><span data-stu-id="9ba08-121">1</span></span>

<span data-ttu-id="9ba08-122">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="9ba08-122">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-123">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="9ba08-123">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-124">64</span><span class="sxs-lookup"><span data-stu-id="9ba08-124">64</span></span>

<span data-ttu-id="9ba08-125">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="9ba08-125">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-126">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="9ba08-126">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-127">65</span><span class="sxs-lookup"><span data-stu-id="9ba08-127">65</span></span>

<span data-ttu-id="9ba08-128">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="9ba08-128">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-129">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="9ba08-129">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-130">66</span><span class="sxs-lookup"><span data-stu-id="9ba08-130">66</span></span>

<span data-ttu-id="9ba08-131">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="9ba08-131">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-132">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="9ba08-132">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-133">67</span><span class="sxs-lookup"><span data-stu-id="9ba08-133">67</span></span>

<span data-ttu-id="9ba08-134">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="9ba08-134">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-135">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="9ba08-135">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-136">68</span><span class="sxs-lookup"><span data-stu-id="9ba08-136">68</span></span>

<span data-ttu-id="9ba08-137">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="9ba08-137">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-138">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="9ba08-138">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-139">69</span><span class="sxs-lookup"><span data-stu-id="9ba08-139">69</span></span>

<span data-ttu-id="9ba08-140">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="9ba08-140">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-141">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="9ba08-141">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-142">70</span><span class="sxs-lookup"><span data-stu-id="9ba08-142">70</span></span>

<span data-ttu-id="9ba08-143">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="9ba08-143">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-144">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="9ba08-144">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-145">71</span><span class="sxs-lookup"><span data-stu-id="9ba08-145">71</span></span>

<span data-ttu-id="9ba08-146">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="9ba08-146">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-147">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="9ba08-147">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-148">72</span><span class="sxs-lookup"><span data-stu-id="9ba08-148">72</span></span>

<span data-ttu-id="9ba08-149">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="9ba08-149">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-150">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="9ba08-150">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-151">73</span><span class="sxs-lookup"><span data-stu-id="9ba08-151">73</span></span>

<span data-ttu-id="9ba08-152">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="9ba08-152">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-153">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="9ba08-153">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-154">74</span><span class="sxs-lookup"><span data-stu-id="9ba08-154">74</span></span>

<span data-ttu-id="9ba08-155">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="9ba08-155">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-156">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="9ba08-156">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-157">75</span><span class="sxs-lookup"><span data-stu-id="9ba08-157">75</span></span>

<span data-ttu-id="9ba08-158">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="9ba08-158">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-159">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="9ba08-159">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-160">76</span><span class="sxs-lookup"><span data-stu-id="9ba08-160">76</span></span>

<span data-ttu-id="9ba08-161">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="9ba08-161">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-162">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="9ba08-162">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-163">77</span><span class="sxs-lookup"><span data-stu-id="9ba08-163">77</span></span>

<span data-ttu-id="9ba08-164">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="9ba08-164">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-165">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="9ba08-165">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-166">78</span><span class="sxs-lookup"><span data-stu-id="9ba08-166">78</span></span>

<span data-ttu-id="9ba08-167">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="9ba08-167">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-168">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="9ba08-168">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-169">79</span><span class="sxs-lookup"><span data-stu-id="9ba08-169">79</span></span>

<span data-ttu-id="9ba08-170">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="9ba08-170">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-171">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="9ba08-171">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-172">80</span><span class="sxs-lookup"><span data-stu-id="9ba08-172">80</span></span>

<span data-ttu-id="9ba08-173">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="9ba08-173">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-174">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="9ba08-174">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-175">81</span><span class="sxs-lookup"><span data-stu-id="9ba08-175">81</span></span>

<span data-ttu-id="9ba08-176">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="9ba08-176">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-177">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="9ba08-177">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-178">82</span><span class="sxs-lookup"><span data-stu-id="9ba08-178">82</span></span>

<span data-ttu-id="9ba08-179">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="9ba08-179">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-180">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="9ba08-180">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-181">83</span><span class="sxs-lookup"><span data-stu-id="9ba08-181">83</span></span>

<span data-ttu-id="9ba08-182">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="9ba08-182">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-183">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="9ba08-183">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-184">84</span><span class="sxs-lookup"><span data-stu-id="9ba08-184">84</span></span>

<span data-ttu-id="9ba08-185">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="9ba08-185">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-186">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="9ba08-186">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-187">85</span><span class="sxs-lookup"><span data-stu-id="9ba08-187">85</span></span>

<span data-ttu-id="9ba08-188">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="9ba08-188">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-189">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="9ba08-189">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-190">86</span><span class="sxs-lookup"><span data-stu-id="9ba08-190">86</span></span>

<span data-ttu-id="9ba08-191">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="9ba08-191">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-192">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="9ba08-192">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-193">87</span><span class="sxs-lookup"><span data-stu-id="9ba08-193">87</span></span>

<span data-ttu-id="9ba08-194">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="9ba08-194">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-195">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="9ba08-195">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-196">88</span><span class="sxs-lookup"><span data-stu-id="9ba08-196">88</span></span>

<span data-ttu-id="9ba08-197">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="9ba08-197">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-198">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="9ba08-198">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-199">89</span><span class="sxs-lookup"><span data-stu-id="9ba08-199">89</span></span>

<span data-ttu-id="9ba08-200">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="9ba08-200">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-201">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="9ba08-201">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-202">90</span><span class="sxs-lookup"><span data-stu-id="9ba08-202">90</span></span>

<span data-ttu-id="9ba08-203">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="9ba08-203">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-204">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="9ba08-204">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-205">91</span><span class="sxs-lookup"><span data-stu-id="9ba08-205">91</span></span>

<span data-ttu-id="9ba08-206">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="9ba08-206">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-207">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="9ba08-207">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-208">92</span><span class="sxs-lookup"><span data-stu-id="9ba08-208">92</span></span>

<span data-ttu-id="9ba08-209">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="9ba08-209">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-210">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="9ba08-210">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-211">93</span><span class="sxs-lookup"><span data-stu-id="9ba08-211">93</span></span>

<span data-ttu-id="9ba08-212">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="9ba08-212">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-213">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="9ba08-213">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-214">94</span><span class="sxs-lookup"><span data-stu-id="9ba08-214">94</span></span>

<span data-ttu-id="9ba08-215">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="9ba08-215">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-216">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="9ba08-216">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-217">95</span><span class="sxs-lookup"><span data-stu-id="9ba08-217">95</span></span>

<span data-ttu-id="9ba08-218">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="9ba08-218">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-219">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="9ba08-219">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-220">96</span><span class="sxs-lookup"><span data-stu-id="9ba08-220">96</span></span>

<span data-ttu-id="9ba08-221">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="9ba08-221">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-222">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="9ba08-222">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-223">97</span><span class="sxs-lookup"><span data-stu-id="9ba08-223">97</span></span>

<span data-ttu-id="9ba08-224">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="9ba08-224">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-225">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="9ba08-225">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-226">98</span><span class="sxs-lookup"><span data-stu-id="9ba08-226">98</span></span>

<span data-ttu-id="9ba08-227">Не все аренды DHCP освобождаются или возобновляются.</span><span class="sxs-lookup"><span data-stu-id="9ba08-227">Not all DHCP leases are released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-228">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="9ba08-228">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-229">100</span><span class="sxs-lookup"><span data-stu-id="9ba08-229">100</span></span>

<span data-ttu-id="9ba08-230">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="9ba08-230">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9ba08-231">**Другое**</span><span class="sxs-lookup"><span data-stu-id="9ba08-231">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="9ba08-232">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="9ba08-232">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ba08-233">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ba08-233">Remarks</span></span>

<span data-ttu-id="9ba08-234">Это независимый от экземпляра вызов, который применяется ко всем адаптерам, но только для Windows.</span><span class="sxs-lookup"><span data-stu-id="9ba08-234">This is an instance-independent call that applies to all adapters but only for Windows.</span></span>

## <a name="examples"></a><span data-ttu-id="9ba08-235">Примеры</span><span class="sxs-lookup"><span data-stu-id="9ba08-235">Examples</span></span>

<span data-ttu-id="9ba08-236">Пример [изменения порядка поиска DNS-суффиксов для всех сетевых адаптеров](https://Gallery.TechNet.Microsoft.Com/2857b7b0-1327-4ce2-9f2b-b662cce387c6) VBScript настраивает компьютер для использования двух DNS-суффиксов при выполнении поиска DNS.</span><span class="sxs-lookup"><span data-stu-id="9ba08-236">The [Modify the DNS Suffix Search Order for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/2857b7b0-1327-4ce2-9f2b-b662cce387c6) VBScript code sample configures a computer to use two DNS suffixes when performing DNS searches.</span></span>

<span data-ttu-id="9ba08-237">Пример [включения параметров DHCP на компьютере](https://Gallery.TechNet.Microsoft.Com/41e6ab51-78c0-4413-b086-03fde33ea125) в сценарии VBScript настраивает все параметры, которые обычно необходимы для включения DHCP на компьютере.</span><span class="sxs-lookup"><span data-stu-id="9ba08-237">The [Enable DHCP Settings on a Computer](https://Gallery.TechNet.Microsoft.Com/41e6ab51-78c0-4413-b086-03fde33ea125) VBScript sample configures all the settings typically required to enable DHCP on a computer.</span></span>

<span data-ttu-id="9ba08-238">Следующий код PowerShell задает порядок поиска DNS-суффикса.</span><span class="sxs-lookup"><span data-stu-id="9ba08-238">The following PowerShell code sets the DNS suffix search order.</span></span>


```PowerShell
#First store the suffixes to set in a variable
$suffixes = 'microsoft.com', 'google.com', 'yahoo.com'

#Since this is a static method, get a class object and then call the method. 
$class = [wmiclass]'Win32_NetworkAdapterConfiguration'
$class.SetDNSSuffixSearchOrder($suffixes)
```



## <a name="requirements"></a><span data-ttu-id="9ba08-239">Требования</span><span class="sxs-lookup"><span data-stu-id="9ba08-239">Requirements</span></span>



| <span data-ttu-id="9ba08-240">Требование</span><span class="sxs-lookup"><span data-stu-id="9ba08-240">Requirement</span></span> | <span data-ttu-id="9ba08-241">Значение</span><span class="sxs-lookup"><span data-stu-id="9ba08-241">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ba08-242">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9ba08-242">Minimum supported client</span></span><br/> | <span data-ttu-id="9ba08-243">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9ba08-243">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9ba08-244">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9ba08-244">Minimum supported server</span></span><br/> | <span data-ttu-id="9ba08-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ba08-245">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9ba08-246">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9ba08-246">Namespace</span></span><br/>                | <span data-ttu-id="9ba08-247">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9ba08-247">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9ba08-248">MOF</span><span class="sxs-lookup"><span data-stu-id="9ba08-248">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ba08-249"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ba08-249"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ba08-250">DLL</span><span class="sxs-lookup"><span data-stu-id="9ba08-250">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ba08-251"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ba08-251"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ba08-252">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ba08-252">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ba08-253">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="9ba08-253">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="9ba08-254">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="9ba08-254">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="9ba08-255">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="9ba08-255">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="9ba08-256">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="9ba08-256">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="9ba08-257">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="9ba08-257">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

