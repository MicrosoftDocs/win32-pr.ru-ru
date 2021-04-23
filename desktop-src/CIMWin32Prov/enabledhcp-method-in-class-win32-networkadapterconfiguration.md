---
description: Метод класса WMI EnableDHCP включает протокол DHCP для службы с этим сетевым адаптером. DHCP разрешает динамическое выделение IP-адресов.
ms.assetid: 8c61d731-77a3-4ef4-bad9-26edaca60892
ms.tgt_platform: multiple
title: Метод EnableDHCP класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableDHCP
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 002dedd3b0165053fea98dda035316676af638f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990501"
---
# <a name="enabledhcp-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="e0145-104">Метод EnableDHCP \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0145-104">EnableDHCP method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="e0145-105">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) EnableDHCP включает протокол DHCP для службы с этим сетевым адаптером.</span><span class="sxs-lookup"><span data-stu-id="e0145-105">The **EnableDHCP** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method enables the Dynamic Host Configuration Protocol (DHCP) for service with this network adapter.</span></span> <span data-ttu-id="e0145-106">DHCP разрешает динамическое выделение IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="e0145-106">DHCP allows IP addresses to be dynamically allocated.</span></span>

<span data-ttu-id="e0145-107">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="e0145-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e0145-108">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e0145-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e0145-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0145-109">Syntax</span></span>


```mof
uint32 EnableDHCP();
```



## <a name="parameters"></a><span data-ttu-id="e0145-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e0145-110">Parameters</span></span>

<span data-ttu-id="e0145-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="e0145-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e0145-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e0145-112">Return value</span></span>

<span data-ttu-id="e0145-113">Возвращает значение 0 (ноль) для успешного завершения, если перезагрузка не требуется, 1 (один) для успешного завершения, когда требуется перезагрузка, и любое другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="e0145-113">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="e0145-114">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="e0145-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="e0145-115">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="e0145-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="e0145-116">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="e0145-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-117">0</span><span class="sxs-lookup"><span data-stu-id="e0145-117">0</span></span>

<span data-ttu-id="e0145-118">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="e0145-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-119">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="e0145-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-120">1</span><span class="sxs-lookup"><span data-stu-id="e0145-120">1</span></span>

<span data-ttu-id="e0145-121">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="e0145-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-122">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="e0145-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-123">64</span><span class="sxs-lookup"><span data-stu-id="e0145-123">64</span></span>

<span data-ttu-id="e0145-124">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="e0145-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-125">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="e0145-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-126">65</span><span class="sxs-lookup"><span data-stu-id="e0145-126">65</span></span>

<span data-ttu-id="e0145-127">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="e0145-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-128">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="e0145-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-129">66</span><span class="sxs-lookup"><span data-stu-id="e0145-129">66</span></span>

<span data-ttu-id="e0145-130">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="e0145-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-131">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="e0145-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-132">67</span><span class="sxs-lookup"><span data-stu-id="e0145-132">67</span></span>

<span data-ttu-id="e0145-133">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e0145-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-134">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="e0145-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-135">68</span><span class="sxs-lookup"><span data-stu-id="e0145-135">68</span></span>

<span data-ttu-id="e0145-136">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="e0145-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-137">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="e0145-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-138">69</span><span class="sxs-lookup"><span data-stu-id="e0145-138">69</span></span>

<span data-ttu-id="e0145-139">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="e0145-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-140">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="e0145-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-141">70</span><span class="sxs-lookup"><span data-stu-id="e0145-141">70</span></span>

<span data-ttu-id="e0145-142">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="e0145-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-143">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="e0145-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-144">71</span><span class="sxs-lookup"><span data-stu-id="e0145-144">71</span></span>

<span data-ttu-id="e0145-145">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="e0145-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-146">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="e0145-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-147">72</span><span class="sxs-lookup"><span data-stu-id="e0145-147">72</span></span>

<span data-ttu-id="e0145-148">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="e0145-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-149">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="e0145-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-150">73</span><span class="sxs-lookup"><span data-stu-id="e0145-150">73</span></span>

<span data-ttu-id="e0145-151">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="e0145-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-152">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="e0145-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-153">74</span><span class="sxs-lookup"><span data-stu-id="e0145-153">74</span></span>

<span data-ttu-id="e0145-154">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="e0145-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-155">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="e0145-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-156">75</span><span class="sxs-lookup"><span data-stu-id="e0145-156">75</span></span>

<span data-ttu-id="e0145-157">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="e0145-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-158">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="e0145-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-159">76</span><span class="sxs-lookup"><span data-stu-id="e0145-159">76</span></span>

<span data-ttu-id="e0145-160">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="e0145-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-161">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="e0145-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-162">77</span><span class="sxs-lookup"><span data-stu-id="e0145-162">77</span></span>

<span data-ttu-id="e0145-163">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="e0145-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-164">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="e0145-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-165">78</span><span class="sxs-lookup"><span data-stu-id="e0145-165">78</span></span>

<span data-ttu-id="e0145-166">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="e0145-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-167">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="e0145-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-168">79</span><span class="sxs-lookup"><span data-stu-id="e0145-168">79</span></span>

<span data-ttu-id="e0145-169">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="e0145-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-170">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="e0145-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-171">80</span><span class="sxs-lookup"><span data-stu-id="e0145-171">80</span></span>

<span data-ttu-id="e0145-172">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="e0145-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-173">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="e0145-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-174">81</span><span class="sxs-lookup"><span data-stu-id="e0145-174">81</span></span>

<span data-ttu-id="e0145-175">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="e0145-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-176">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="e0145-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-177">82</span><span class="sxs-lookup"><span data-stu-id="e0145-177">82</span></span>

<span data-ttu-id="e0145-178">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="e0145-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-179">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="e0145-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-180">83</span><span class="sxs-lookup"><span data-stu-id="e0145-180">83</span></span>

<span data-ttu-id="e0145-181">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="e0145-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-182">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="e0145-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-183">84</span><span class="sxs-lookup"><span data-stu-id="e0145-183">84</span></span>

<span data-ttu-id="e0145-184">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="e0145-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-185">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="e0145-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-186">85</span><span class="sxs-lookup"><span data-stu-id="e0145-186">85</span></span>

<span data-ttu-id="e0145-187">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="e0145-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-188">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="e0145-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-189">86</span><span class="sxs-lookup"><span data-stu-id="e0145-189">86</span></span>

<span data-ttu-id="e0145-190">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="e0145-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-191">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="e0145-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-192">87</span><span class="sxs-lookup"><span data-stu-id="e0145-192">87</span></span>

<span data-ttu-id="e0145-193">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="e0145-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-194">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="e0145-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-195">88</span><span class="sxs-lookup"><span data-stu-id="e0145-195">88</span></span>

<span data-ttu-id="e0145-196">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="e0145-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-197">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="e0145-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-198">89</span><span class="sxs-lookup"><span data-stu-id="e0145-198">89</span></span>

<span data-ttu-id="e0145-199">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="e0145-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-200">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="e0145-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-201">90</span><span class="sxs-lookup"><span data-stu-id="e0145-201">90</span></span>

<span data-ttu-id="e0145-202">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="e0145-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-203">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="e0145-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-204">91</span><span class="sxs-lookup"><span data-stu-id="e0145-204">91</span></span>

<span data-ttu-id="e0145-205">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="e0145-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-206">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="e0145-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-207">92</span><span class="sxs-lookup"><span data-stu-id="e0145-207">92</span></span>

<span data-ttu-id="e0145-208">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="e0145-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-209">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="e0145-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-210">93</span><span class="sxs-lookup"><span data-stu-id="e0145-210">93</span></span>

<span data-ttu-id="e0145-211">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="e0145-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-212">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="e0145-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-213">94</span><span class="sxs-lookup"><span data-stu-id="e0145-213">94</span></span>

<span data-ttu-id="e0145-214">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="e0145-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-215">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="e0145-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-216">95</span><span class="sxs-lookup"><span data-stu-id="e0145-216">95</span></span>

<span data-ttu-id="e0145-217">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="e0145-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-218">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="e0145-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-219">96</span><span class="sxs-lookup"><span data-stu-id="e0145-219">96</span></span>

<span data-ttu-id="e0145-220">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="e0145-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-221">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="e0145-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-222">97</span><span class="sxs-lookup"><span data-stu-id="e0145-222">97</span></span>

<span data-ttu-id="e0145-223">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="e0145-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-224">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="e0145-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-225">98</span><span class="sxs-lookup"><span data-stu-id="e0145-225">98</span></span>

<span data-ttu-id="e0145-226">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="e0145-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-227">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="e0145-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-228">100</span><span class="sxs-lookup"><span data-stu-id="e0145-228">100</span></span>

<span data-ttu-id="e0145-229">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="e0145-229">DHCP not enabled on the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="e0145-230">**Другое**</span><span class="sxs-lookup"><span data-stu-id="e0145-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="e0145-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="e0145-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e0145-232">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e0145-232">Remarks</span></span>

<span data-ttu-id="e0145-233">Этот метод не очищает статические шлюзы по умолчанию, имеющиеся на компьютере.</span><span class="sxs-lookup"><span data-stu-id="e0145-233">This method does not clears any static default gateways present on the machine.</span></span>

## <a name="examples"></a><span data-ttu-id="e0145-234">Примеры</span><span class="sxs-lookup"><span data-stu-id="e0145-234">Examples</span></span>

<span data-ttu-id="e0145-235">Пример кода VBScript для [включения DHCP и назначения DNS-серверов](https://Gallery.TechNet.Microsoft.Com/7b1cec46-bdb8-4afc-b240-9789eefce6de) в коллекции TechNet использует EnableDHCP для включения DHCP и назначения DNS-серверов компьютеру.</span><span class="sxs-lookup"><span data-stu-id="e0145-235">The [Enable DHCP and Assign DNS Servers](https://Gallery.TechNet.Microsoft.Com/7b1cec46-bdb8-4afc-b240-9789eefce6de) VBScript code sample on TechNet Gallery uses EnableDHCP to enable DHCP and assign DNS servers to a computer.</span></span>

<span data-ttu-id="e0145-236">В следующем примере кода VBScript показано, как включить использование DHCP в экземпляре [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="e0145-236">The following VBScript code sample demonstrates how to enable DHCP use on an instance of [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) .</span></span> <span data-ttu-id="e0145-237">В этом случае мы указываем адаптер с индексом 0.</span><span class="sxs-lookup"><span data-stu-id="e0145-237">In this case we specify the adapter with an Index of 0.</span></span> <span data-ttu-id="e0145-238">Правильный индекс должен быть выбран из экземпляров Win32 \_ сетевого адаптера для других интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="e0145-238">The correct index should be selected from Win32\_NetworkAdapter instances for other interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="e0145-239">Поддерживается только на платформах NT.</span><span class="sxs-lookup"><span data-stu-id="e0145-239">Supported on NT platforms only.</span></span>

 


```VB
Set Adapter = GetObject("winmgmts:Win32_NetworkAdapterConfiguration=0")

RetVal = Adapter.EnableDHCP()

if RetVal = 0 then 
 WScript.Echo "DHCP Enabled"
else 
 WScript.Echo "DHCP enable failed"
end if
```



<span data-ttu-id="e0145-240">В следующем образце кода Perl показано, как включить использование DHCP в экземпляре [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="e0145-240">The following Perl code sample demonstrates how to enable DHCP use on an instance of [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) .</span></span> <span data-ttu-id="e0145-241">В этом случае мы указываем адаптер с индексом 0.</span><span class="sxs-lookup"><span data-stu-id="e0145-241">In this case we specify the adapter with an Index of 0.</span></span> <span data-ttu-id="e0145-242">Правильный индекс должен быть выбран из экземпляров Win32 \_ сетевого адаптера для других интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="e0145-242">The correct index should be selected from Win32\_NetworkAdapter instances for other interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="e0145-243">Поддерживается только на платформах NT.</span><span class="sxs-lookup"><span data-stu-id="e0145-243">Supported on NT platforms only.</span></span>

 


```
use strict;
use Win32::OLE;

my ( $Adapter, $RetVal );

eval { $Adapter = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
       Get("Win32_NetworkAdapterConfiguration=0"); };
unless ($@)
{
 print "\n";
 $RetVal = $Adapter->EnableDHCP();
 if ( $RetVal == 0)
 {
  print "DHCP Enabled\n";
 }
 else
 {
  print "DHCP enable failed\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="e0145-244">Требования</span><span class="sxs-lookup"><span data-stu-id="e0145-244">Requirements</span></span>



| <span data-ttu-id="e0145-245">Требование</span><span class="sxs-lookup"><span data-stu-id="e0145-245">Requirement</span></span> | <span data-ttu-id="e0145-246">Значение</span><span class="sxs-lookup"><span data-stu-id="e0145-246">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0145-247">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e0145-247">Minimum supported client</span></span><br/> | <span data-ttu-id="e0145-248">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e0145-248">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e0145-249">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e0145-249">Minimum supported server</span></span><br/> | <span data-ttu-id="e0145-250">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0145-250">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e0145-251">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e0145-251">Namespace</span></span><br/>                | <span data-ttu-id="e0145-252">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e0145-252">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e0145-253">MOF</span><span class="sxs-lookup"><span data-stu-id="e0145-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0145-254"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0145-254"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e0145-255">DLL</span><span class="sxs-lookup"><span data-stu-id="e0145-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0145-256"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0145-256"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0145-257">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0145-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0145-258">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="e0145-258">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="e0145-259">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="e0145-259">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="e0145-260">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="e0145-260">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="e0145-261">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="e0145-261">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="e0145-262">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="e0145-262">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

