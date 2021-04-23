---
description: Метод Сетипконнектионметрик используется для задания метрики маршрутизации, связанной с данным адаптером, привязанным к IP-адресу.
ms.assetid: d7f7c0df-51e3-4dc8-8a53-977ecde075df
ms.tgt_platform: multiple
title: Метод Сетипконнектионметрик класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPConnectionMetric
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73d6dde0a8faea2aeaf0982459e3c377bb1ac51d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141875"
---
# <a name="setipconnectionmetric-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="f4705-103">Метод Сетипконнектионметрик \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4705-103">SetIPConnectionMetric method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="f4705-104">Метод **сетипконнектионметрик** используется для задания метрики маршрутизации, связанной с данным адаптером, привязанным к IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="f4705-104">The **SetIPConnectionMetric** method is used to set the routing metric associated with this IP-bound adapter.</span></span>

<span data-ttu-id="f4705-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="f4705-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f4705-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f4705-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f4705-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f4705-107">Syntax</span></span>


```mof
uint32 SetIPConnectionMetric(
  [in] uint32 IPConnectionMetric
);
```



## <a name="parameters"></a><span data-ttu-id="f4705-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f4705-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4705-109">*Ипконнектионметрик* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f4705-109">*IPConnectionMetric* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4705-110">Указывает стоимость использования настроенных маршрутов для этого IP-связанного адаптера.</span><span class="sxs-lookup"><span data-stu-id="f4705-110">Indicates the cost of using the configured routes for this IP-bound adapter.</span></span> <span data-ttu-id="f4705-111">Значение будет взвешено для этих маршрутов в таблице IP-маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="f4705-111">The value is weighted for those routes in the IP routing table.</span></span> <span data-ttu-id="f4705-112">При наличии нескольких маршрутов к назначению в таблице маршрутизации используется маршрут с наименьшей метрикой.</span><span class="sxs-lookup"><span data-stu-id="f4705-112">If there are multiple routes to a destination in the routing table, the route with the lowest metric is used.</span></span> <span data-ttu-id="f4705-113">Диапазон допустимых значений — от 1 до 9999.</span><span class="sxs-lookup"><span data-stu-id="f4705-113">The range of valid values is 1 through 9999.</span></span> <span data-ttu-id="f4705-114">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="f4705-114">The default value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4705-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f4705-115">Return value</span></span>

<span data-ttu-id="f4705-116">Возвращает значение 0 (ноль) для успешного завершения, если не требуется перезагрузка, 1 (один) для успешного завершения, когда требуется перезагрузка, и другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="f4705-116">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="f4705-117">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f4705-117">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f4705-118">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f4705-118">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f4705-119">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="f4705-119">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-120">0</span><span class="sxs-lookup"><span data-stu-id="f4705-120">0</span></span>

<span data-ttu-id="f4705-121">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="f4705-121">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-122">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="f4705-122">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-123">1</span><span class="sxs-lookup"><span data-stu-id="f4705-123">1</span></span>

<span data-ttu-id="f4705-124">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="f4705-124">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-125">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="f4705-125">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-126">64</span><span class="sxs-lookup"><span data-stu-id="f4705-126">64</span></span>

<span data-ttu-id="f4705-127">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="f4705-127">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-128">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="f4705-128">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-129">65</span><span class="sxs-lookup"><span data-stu-id="f4705-129">65</span></span>

<span data-ttu-id="f4705-130">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="f4705-130">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-131">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="f4705-131">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-132">66</span><span class="sxs-lookup"><span data-stu-id="f4705-132">66</span></span>

<span data-ttu-id="f4705-133">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="f4705-133">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-134">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="f4705-134">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-135">67</span><span class="sxs-lookup"><span data-stu-id="f4705-135">67</span></span>

<span data-ttu-id="f4705-136">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f4705-136">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-137">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="f4705-137">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-138">68</span><span class="sxs-lookup"><span data-stu-id="f4705-138">68</span></span>

<span data-ttu-id="f4705-139">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="f4705-139">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-140">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="f4705-140">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-141">69</span><span class="sxs-lookup"><span data-stu-id="f4705-141">69</span></span>

<span data-ttu-id="f4705-142">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="f4705-142">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-143">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="f4705-143">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-144">70</span><span class="sxs-lookup"><span data-stu-id="f4705-144">70</span></span>

<span data-ttu-id="f4705-145">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="f4705-145">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-146">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="f4705-146">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-147">71</span><span class="sxs-lookup"><span data-stu-id="f4705-147">71</span></span>

<span data-ttu-id="f4705-148">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="f4705-148">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-149">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="f4705-149">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-150">72</span><span class="sxs-lookup"><span data-stu-id="f4705-150">72</span></span>

<span data-ttu-id="f4705-151">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="f4705-151">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-152">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="f4705-152">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-153">73</span><span class="sxs-lookup"><span data-stu-id="f4705-153">73</span></span>

<span data-ttu-id="f4705-154">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="f4705-154">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-155">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="f4705-155">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-156">74</span><span class="sxs-lookup"><span data-stu-id="f4705-156">74</span></span>

<span data-ttu-id="f4705-157">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="f4705-157">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-158">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="f4705-158">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-159">75</span><span class="sxs-lookup"><span data-stu-id="f4705-159">75</span></span>

<span data-ttu-id="f4705-160">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="f4705-160">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-161">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="f4705-161">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-162">76</span><span class="sxs-lookup"><span data-stu-id="f4705-162">76</span></span>

<span data-ttu-id="f4705-163">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="f4705-163">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-164">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="f4705-164">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-165">77</span><span class="sxs-lookup"><span data-stu-id="f4705-165">77</span></span>

<span data-ttu-id="f4705-166">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="f4705-166">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-167">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="f4705-167">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-168">78</span><span class="sxs-lookup"><span data-stu-id="f4705-168">78</span></span>

<span data-ttu-id="f4705-169">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="f4705-169">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-170">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="f4705-170">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-171">79</span><span class="sxs-lookup"><span data-stu-id="f4705-171">79</span></span>

<span data-ttu-id="f4705-172">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="f4705-172">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-173">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="f4705-173">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-174">80</span><span class="sxs-lookup"><span data-stu-id="f4705-174">80</span></span>

<span data-ttu-id="f4705-175">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="f4705-175">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-176">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="f4705-176">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-177">81</span><span class="sxs-lookup"><span data-stu-id="f4705-177">81</span></span>

<span data-ttu-id="f4705-178">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="f4705-178">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-179">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="f4705-179">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-180">82</span><span class="sxs-lookup"><span data-stu-id="f4705-180">82</span></span>

<span data-ttu-id="f4705-181">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="f4705-181">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-182">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="f4705-182">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-183">83</span><span class="sxs-lookup"><span data-stu-id="f4705-183">83</span></span>

<span data-ttu-id="f4705-184">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="f4705-184">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-185">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="f4705-185">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-186">84</span><span class="sxs-lookup"><span data-stu-id="f4705-186">84</span></span>

<span data-ttu-id="f4705-187">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="f4705-187">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-188">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="f4705-188">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-189">85</span><span class="sxs-lookup"><span data-stu-id="f4705-189">85</span></span>

<span data-ttu-id="f4705-190">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="f4705-190">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-191">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="f4705-191">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-192">86</span><span class="sxs-lookup"><span data-stu-id="f4705-192">86</span></span>

<span data-ttu-id="f4705-193">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="f4705-193">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-194">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="f4705-194">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-195">87</span><span class="sxs-lookup"><span data-stu-id="f4705-195">87</span></span>

<span data-ttu-id="f4705-196">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="f4705-196">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-197">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="f4705-197">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-198">88</span><span class="sxs-lookup"><span data-stu-id="f4705-198">88</span></span>

<span data-ttu-id="f4705-199">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="f4705-199">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-200">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="f4705-200">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-201">89</span><span class="sxs-lookup"><span data-stu-id="f4705-201">89</span></span>

<span data-ttu-id="f4705-202">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="f4705-202">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-203">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="f4705-203">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-204">90</span><span class="sxs-lookup"><span data-stu-id="f4705-204">90</span></span>

<span data-ttu-id="f4705-205">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="f4705-205">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-206">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="f4705-206">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-207">91</span><span class="sxs-lookup"><span data-stu-id="f4705-207">91</span></span>

<span data-ttu-id="f4705-208">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="f4705-208">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-209">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="f4705-209">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-210">92</span><span class="sxs-lookup"><span data-stu-id="f4705-210">92</span></span>

<span data-ttu-id="f4705-211">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="f4705-211">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-212">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="f4705-212">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-213">93</span><span class="sxs-lookup"><span data-stu-id="f4705-213">93</span></span>

<span data-ttu-id="f4705-214">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="f4705-214">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-215">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="f4705-215">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-216">94</span><span class="sxs-lookup"><span data-stu-id="f4705-216">94</span></span>

<span data-ttu-id="f4705-217">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="f4705-217">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-218">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="f4705-218">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-219">95</span><span class="sxs-lookup"><span data-stu-id="f4705-219">95</span></span>

<span data-ttu-id="f4705-220">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="f4705-220">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-221">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="f4705-221">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-222">96</span><span class="sxs-lookup"><span data-stu-id="f4705-222">96</span></span>

<span data-ttu-id="f4705-223">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="f4705-223">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-224">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="f4705-224">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-225">97</span><span class="sxs-lookup"><span data-stu-id="f4705-225">97</span></span>

<span data-ttu-id="f4705-226">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="f4705-226">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-227">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="f4705-227">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-228">98</span><span class="sxs-lookup"><span data-stu-id="f4705-228">98</span></span>

<span data-ttu-id="f4705-229">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="f4705-229">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-230">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="f4705-230">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-231">100</span><span class="sxs-lookup"><span data-stu-id="f4705-231">100</span></span>

<span data-ttu-id="f4705-232">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="f4705-232">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f4705-233">**Другое**</span><span class="sxs-lookup"><span data-stu-id="f4705-233">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="f4705-234">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="f4705-234">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="f4705-235">Примеры</span><span class="sxs-lookup"><span data-stu-id="f4705-235">Examples</span></span>

<span data-ttu-id="f4705-236">Пример [изменения метрики IP-подключения для сетевого адаптера](https://Gallery.TechNet.Microsoft.Com/73367c75-7a39-44dc-a8d7-eb2359030969) VBScript устанавливает МЕТРИКУ IP-подключения для сетевого адаптера равным 100.</span><span class="sxs-lookup"><span data-stu-id="f4705-236">The [Modify the IP Connection Metric for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/73367c75-7a39-44dc-a8d7-eb2359030969) VBScript sample sets the IP connection metric for a network adapter to 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4705-237">Требования</span><span class="sxs-lookup"><span data-stu-id="f4705-237">Requirements</span></span>



| <span data-ttu-id="f4705-238">Требование</span><span class="sxs-lookup"><span data-stu-id="f4705-238">Requirement</span></span> | <span data-ttu-id="f4705-239">Значение</span><span class="sxs-lookup"><span data-stu-id="f4705-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4705-240">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f4705-240">Minimum supported client</span></span><br/> | <span data-ttu-id="f4705-241">Windows Vista, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f4705-241">Windows Vista, Windows Vista</span></span><br/>                                                 |
| <span data-ttu-id="f4705-242">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f4705-242">Minimum supported server</span></span><br/> | <span data-ttu-id="f4705-243">Windows Server 2008, Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f4705-243">Windows Server 2008, Windows Server 2008</span></span><br/>                                     |
| <span data-ttu-id="f4705-244">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f4705-244">Namespace</span></span><br/>                | <span data-ttu-id="f4705-245">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f4705-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f4705-246">MOF</span><span class="sxs-lookup"><span data-stu-id="f4705-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f4705-247"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f4705-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f4705-248">DLL</span><span class="sxs-lookup"><span data-stu-id="f4705-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4705-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4705-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4705-250">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f4705-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4705-251">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="f4705-251">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="f4705-252">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="f4705-252">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="f4705-253">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="f4705-253">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="f4705-254">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="f4705-254">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="f4705-255">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="f4705-255">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

