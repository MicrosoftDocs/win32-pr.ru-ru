---
description: Статический метод класса Сетарпалвайссаурцерауте WMI используется для настройки передачи запросов ARP по протоколу TCP/IP.
ms.assetid: bbff4e2e-aea6-400e-8bd8-f62aaa9fa601
ms.tgt_platform: multiple
title: Метод Сетарпалвайссаурцерауте класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetArpAlwaysSourceRoute
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7151fbbd13d3ac6fdf4ac3b129cdcb438abe73a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141175"
---
# <a name="setarpalwayssourceroute-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="661b8-103">Метод Сетарпалвайссаурцерауте \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="661b8-103">SetArpAlwaysSourceRoute method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="661b8-104">Статический метод класса **сетарпалвайссаурцерауте** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) используется для настройки передачи запросов ARP по протоколу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="661b8-104">The **SetArpAlwaysSourceRoute** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the transmission of ARP queries by TCP/IP.</span></span>

<span data-ttu-id="661b8-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="661b8-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="661b8-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="661b8-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="661b8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="661b8-107">Syntax</span></span>


```mof
uint32 SetArpAlwaysSourceRoute(
  [in] boolean ArpAlwaysSourceRoute
);
```



## <a name="parameters"></a><span data-ttu-id="661b8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="661b8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="661b8-109">*Арпалвайссаурцерауте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="661b8-109">*ArpAlwaysSourceRoute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="661b8-110">Если задано **значение true**, TCP/IP вынужден ПЕРЕДАВАТЬ запросы ARP с включенной маршрутизацией источника в сетях Token Ring.</span><span class="sxs-lookup"><span data-stu-id="661b8-110">If **true**, TCP/IP is forced to transmit ARP queries with source routing enabled on Token Ring networks.</span></span> <span data-ttu-id="661b8-111">По умолчанию стек передает запросы ARP без маршрутизации исходного кода, а затем выполняет повторную попытку с включенной маршрутизацией источника, если ответ не получен.</span><span class="sxs-lookup"><span data-stu-id="661b8-111">By default, the stack transmits ARP queries without source routing first, then retries with source routing enabled if no reply is received.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="661b8-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="661b8-112">Return value</span></span>

<span data-ttu-id="661b8-113">Возвращает значение 0 (ноль) для успешного завершения, если не требуется перезагрузка, 1 (один) для успешного завершения, когда требуется перезагрузка, и другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="661b8-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="661b8-114">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="661b8-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="661b8-115">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="661b8-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="661b8-116">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="661b8-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-117">0</span><span class="sxs-lookup"><span data-stu-id="661b8-117">0</span></span>

<span data-ttu-id="661b8-118">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="661b8-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-119">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="661b8-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-120">1</span><span class="sxs-lookup"><span data-stu-id="661b8-120">1</span></span>

<span data-ttu-id="661b8-121">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="661b8-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-122">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="661b8-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-123">64</span><span class="sxs-lookup"><span data-stu-id="661b8-123">64</span></span>

<span data-ttu-id="661b8-124">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="661b8-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-125">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="661b8-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-126">65</span><span class="sxs-lookup"><span data-stu-id="661b8-126">65</span></span>

<span data-ttu-id="661b8-127">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="661b8-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-128">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="661b8-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-129">66</span><span class="sxs-lookup"><span data-stu-id="661b8-129">66</span></span>

<span data-ttu-id="661b8-130">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="661b8-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-131">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="661b8-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-132">67</span><span class="sxs-lookup"><span data-stu-id="661b8-132">67</span></span>

<span data-ttu-id="661b8-133">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="661b8-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-134">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="661b8-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-135">68</span><span class="sxs-lookup"><span data-stu-id="661b8-135">68</span></span>

<span data-ttu-id="661b8-136">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="661b8-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-137">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="661b8-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-138">69</span><span class="sxs-lookup"><span data-stu-id="661b8-138">69</span></span>

<span data-ttu-id="661b8-139">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="661b8-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-140">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="661b8-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-141">70</span><span class="sxs-lookup"><span data-stu-id="661b8-141">70</span></span>

<span data-ttu-id="661b8-142">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="661b8-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-143">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="661b8-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-144">71</span><span class="sxs-lookup"><span data-stu-id="661b8-144">71</span></span>

<span data-ttu-id="661b8-145">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="661b8-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-146">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="661b8-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-147">72</span><span class="sxs-lookup"><span data-stu-id="661b8-147">72</span></span>

<span data-ttu-id="661b8-148">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="661b8-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-149">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="661b8-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-150">73</span><span class="sxs-lookup"><span data-stu-id="661b8-150">73</span></span>

<span data-ttu-id="661b8-151">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="661b8-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-152">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="661b8-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-153">74</span><span class="sxs-lookup"><span data-stu-id="661b8-153">74</span></span>

<span data-ttu-id="661b8-154">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="661b8-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-155">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="661b8-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-156">75</span><span class="sxs-lookup"><span data-stu-id="661b8-156">75</span></span>

<span data-ttu-id="661b8-157">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="661b8-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-158">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="661b8-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-159">76</span><span class="sxs-lookup"><span data-stu-id="661b8-159">76</span></span>

<span data-ttu-id="661b8-160">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="661b8-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-161">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="661b8-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-162">77</span><span class="sxs-lookup"><span data-stu-id="661b8-162">77</span></span>

<span data-ttu-id="661b8-163">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="661b8-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-164">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="661b8-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-165">78</span><span class="sxs-lookup"><span data-stu-id="661b8-165">78</span></span>

<span data-ttu-id="661b8-166">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="661b8-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-167">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="661b8-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-168">79</span><span class="sxs-lookup"><span data-stu-id="661b8-168">79</span></span>

<span data-ttu-id="661b8-169">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="661b8-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-170">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="661b8-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-171">80</span><span class="sxs-lookup"><span data-stu-id="661b8-171">80</span></span>

<span data-ttu-id="661b8-172">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="661b8-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-173">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="661b8-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-174">81</span><span class="sxs-lookup"><span data-stu-id="661b8-174">81</span></span>

<span data-ttu-id="661b8-175">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="661b8-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-176">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="661b8-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-177">82</span><span class="sxs-lookup"><span data-stu-id="661b8-177">82</span></span>

<span data-ttu-id="661b8-178">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="661b8-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-179">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="661b8-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-180">83</span><span class="sxs-lookup"><span data-stu-id="661b8-180">83</span></span>

<span data-ttu-id="661b8-181">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="661b8-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-182">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="661b8-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-183">84</span><span class="sxs-lookup"><span data-stu-id="661b8-183">84</span></span>

<span data-ttu-id="661b8-184">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="661b8-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-185">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="661b8-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-186">85</span><span class="sxs-lookup"><span data-stu-id="661b8-186">85</span></span>

<span data-ttu-id="661b8-187">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="661b8-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-188">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="661b8-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-189">86</span><span class="sxs-lookup"><span data-stu-id="661b8-189">86</span></span>

<span data-ttu-id="661b8-190">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="661b8-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-191">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="661b8-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-192">87</span><span class="sxs-lookup"><span data-stu-id="661b8-192">87</span></span>

<span data-ttu-id="661b8-193">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="661b8-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-194">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="661b8-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-195">88</span><span class="sxs-lookup"><span data-stu-id="661b8-195">88</span></span>

<span data-ttu-id="661b8-196">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="661b8-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-197">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="661b8-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-198">89</span><span class="sxs-lookup"><span data-stu-id="661b8-198">89</span></span>

<span data-ttu-id="661b8-199">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="661b8-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-200">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="661b8-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-201">90</span><span class="sxs-lookup"><span data-stu-id="661b8-201">90</span></span>

<span data-ttu-id="661b8-202">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="661b8-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-203">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="661b8-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-204">91</span><span class="sxs-lookup"><span data-stu-id="661b8-204">91</span></span>

<span data-ttu-id="661b8-205">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="661b8-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-206">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="661b8-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-207">92</span><span class="sxs-lookup"><span data-stu-id="661b8-207">92</span></span>

<span data-ttu-id="661b8-208">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="661b8-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-209">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="661b8-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-210">93</span><span class="sxs-lookup"><span data-stu-id="661b8-210">93</span></span>

<span data-ttu-id="661b8-211">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="661b8-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-212">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="661b8-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-213">94</span><span class="sxs-lookup"><span data-stu-id="661b8-213">94</span></span>

<span data-ttu-id="661b8-214">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="661b8-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-215">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="661b8-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-216">95</span><span class="sxs-lookup"><span data-stu-id="661b8-216">95</span></span>

<span data-ttu-id="661b8-217">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="661b8-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-218">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="661b8-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-219">96</span><span class="sxs-lookup"><span data-stu-id="661b8-219">96</span></span>

<span data-ttu-id="661b8-220">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="661b8-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-221">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="661b8-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-222">97</span><span class="sxs-lookup"><span data-stu-id="661b8-222">97</span></span>

<span data-ttu-id="661b8-223">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="661b8-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-224">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="661b8-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-225">98</span><span class="sxs-lookup"><span data-stu-id="661b8-225">98</span></span>

<span data-ttu-id="661b8-226">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="661b8-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-227">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="661b8-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-228">100</span><span class="sxs-lookup"><span data-stu-id="661b8-228">100</span></span>

<span data-ttu-id="661b8-229">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="661b8-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="661b8-230">**Другое**</span><span class="sxs-lookup"><span data-stu-id="661b8-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="661b8-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="661b8-231">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="661b8-232">Примеры</span><span class="sxs-lookup"><span data-stu-id="661b8-232">Examples</span></span>

<span data-ttu-id="661b8-233">Пример " [изменение запросов ARP для использования исходной маршрутизации](https://Gallery.TechNet.Microsoft.Com/e0298c96-acc2-4809-9365-fce3000db00e) " в коллекции TechNet использует **СЕТАРПАЛВАЙССАУРЦЕРАУТЕ** для настройки TCP/IP, чтобы всегда использовать исходную маршрутизацию во всех сетях Token Ring.</span><span class="sxs-lookup"><span data-stu-id="661b8-233">The [Modify ARP Queries to Use Source Routing](https://Gallery.TechNet.Microsoft.Com/e0298c96-acc2-4809-9365-fce3000db00e) VBScript sample on TechNet Gallery uses **SetArpAlwaysSourceRoute** to configure TCP/IP to always use source routing on all Token Ring networks.</span></span>

## <a name="requirements"></a><span data-ttu-id="661b8-234">Требования</span><span class="sxs-lookup"><span data-stu-id="661b8-234">Requirements</span></span>



| <span data-ttu-id="661b8-235">Требование</span><span class="sxs-lookup"><span data-stu-id="661b8-235">Requirement</span></span> | <span data-ttu-id="661b8-236">Значение</span><span class="sxs-lookup"><span data-stu-id="661b8-236">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="661b8-237">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="661b8-237">Minimum supported client</span></span><br/> | <span data-ttu-id="661b8-238">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="661b8-238">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="661b8-239">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="661b8-239">Minimum supported server</span></span><br/> | <span data-ttu-id="661b8-240">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="661b8-240">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="661b8-241">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="661b8-241">Namespace</span></span><br/>                | <span data-ttu-id="661b8-242">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="661b8-242">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="661b8-243">MOF</span><span class="sxs-lookup"><span data-stu-id="661b8-243">MOF</span></span><br/>                      | <dl> <span data-ttu-id="661b8-244"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="661b8-244"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="661b8-245">DLL</span><span class="sxs-lookup"><span data-stu-id="661b8-245">DLL</span></span><br/>                      | <dl> <span data-ttu-id="661b8-246"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="661b8-246"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="661b8-247">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="661b8-247">See also</span></span>

<dl> <dt>

[<span data-ttu-id="661b8-248">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="661b8-248">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="661b8-249">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="661b8-249">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="661b8-250">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="661b8-250">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="661b8-251">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="661b8-251">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="661b8-252">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="661b8-252">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

