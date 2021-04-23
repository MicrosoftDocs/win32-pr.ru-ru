---
description: Статический метод класса Сетпмтудисковери WMI используется для включения максимального обнаружения единиц передачи (MTU) по пути к удаленному узлу.
ms.assetid: 43c640bb-c4e7-4b4b-9c18-6cc426229954
ms.tgt_platform: multiple
title: Метод Сетпмтудисковери класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetPMTUDiscovery
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ef3bc9ad5d6203077275f3665c4b0efc98265fbe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807571"
---
# <a name="setpmtudiscovery-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="264d5-103">Метод Сетпмтудисковери \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="264d5-103">SetPMTUDiscovery method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="264d5-104">Статический метод класса **сетпмтудисковери** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) используется для включения максимального обнаружения единиц передачи (MTU) по пути к удаленному узлу.</span><span class="sxs-lookup"><span data-stu-id="264d5-104">The **SetPMTUDiscovery** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable Maximum Transmission Unit (MTU) discovery over the path to a remote host.</span></span>

<span data-ttu-id="264d5-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="264d5-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="264d5-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="264d5-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="264d5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="264d5-107">Syntax</span></span>


```mof
uint32 SetPMTUDiscovery(
  [in] boolean PMTUDiscoveryEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="264d5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="264d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="264d5-109">*Пмтудисковеренаблед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="264d5-109">*PMTUDiscoveryEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="264d5-110">Если **значение — true**, протокол TCP должен попытаться обнаружить максимальный или наибольший размер пакета по пути к удаленному узлу.</span><span class="sxs-lookup"><span data-stu-id="264d5-110">If **true**, TCP is enabled to attempt to discover the Maximum Transmission Unit (MTU) or largest packet size over the path to a remote host.</span></span> <span data-ttu-id="264d5-111">Значение по умолчанию — **true**.</span><span class="sxs-lookup"><span data-stu-id="264d5-111">The default is **true**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="264d5-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="264d5-112">Return value</span></span>

<span data-ttu-id="264d5-113">Возвращает значение 0 (ноль) для успешного завершения, если не требуется перезагрузка, 1 (один) для успешного завершения, когда требуется перезагрузка, и другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="264d5-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="264d5-114">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="264d5-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="264d5-115">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="264d5-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="264d5-116">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="264d5-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-117">0</span><span class="sxs-lookup"><span data-stu-id="264d5-117">0</span></span>

<span data-ttu-id="264d5-118">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="264d5-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-119">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="264d5-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-120">1</span><span class="sxs-lookup"><span data-stu-id="264d5-120">1</span></span>

<span data-ttu-id="264d5-121">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="264d5-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-122">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="264d5-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-123">64</span><span class="sxs-lookup"><span data-stu-id="264d5-123">64</span></span>

<span data-ttu-id="264d5-124">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="264d5-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-125">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="264d5-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-126">65</span><span class="sxs-lookup"><span data-stu-id="264d5-126">65</span></span>

<span data-ttu-id="264d5-127">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="264d5-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-128">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="264d5-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-129">66</span><span class="sxs-lookup"><span data-stu-id="264d5-129">66</span></span>

<span data-ttu-id="264d5-130">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="264d5-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-131">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="264d5-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-132">67</span><span class="sxs-lookup"><span data-stu-id="264d5-132">67</span></span>

<span data-ttu-id="264d5-133">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="264d5-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-134">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="264d5-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-135">68</span><span class="sxs-lookup"><span data-stu-id="264d5-135">68</span></span>

<span data-ttu-id="264d5-136">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="264d5-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-137">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="264d5-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-138">69</span><span class="sxs-lookup"><span data-stu-id="264d5-138">69</span></span>

<span data-ttu-id="264d5-139">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="264d5-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-140">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="264d5-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-141">70</span><span class="sxs-lookup"><span data-stu-id="264d5-141">70</span></span>

<span data-ttu-id="264d5-142">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="264d5-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-143">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="264d5-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-144">71</span><span class="sxs-lookup"><span data-stu-id="264d5-144">71</span></span>

<span data-ttu-id="264d5-145">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="264d5-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-146">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="264d5-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-147">72</span><span class="sxs-lookup"><span data-stu-id="264d5-147">72</span></span>

<span data-ttu-id="264d5-148">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="264d5-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-149">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="264d5-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-150">73</span><span class="sxs-lookup"><span data-stu-id="264d5-150">73</span></span>

<span data-ttu-id="264d5-151">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="264d5-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-152">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="264d5-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-153">74</span><span class="sxs-lookup"><span data-stu-id="264d5-153">74</span></span>

<span data-ttu-id="264d5-154">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="264d5-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-155">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="264d5-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-156">75</span><span class="sxs-lookup"><span data-stu-id="264d5-156">75</span></span>

<span data-ttu-id="264d5-157">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="264d5-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-158">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="264d5-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-159">76</span><span class="sxs-lookup"><span data-stu-id="264d5-159">76</span></span>

<span data-ttu-id="264d5-160">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="264d5-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-161">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="264d5-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-162">77</span><span class="sxs-lookup"><span data-stu-id="264d5-162">77</span></span>

<span data-ttu-id="264d5-163">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="264d5-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-164">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="264d5-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-165">78</span><span class="sxs-lookup"><span data-stu-id="264d5-165">78</span></span>

<span data-ttu-id="264d5-166">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="264d5-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-167">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="264d5-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-168">79</span><span class="sxs-lookup"><span data-stu-id="264d5-168">79</span></span>

<span data-ttu-id="264d5-169">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="264d5-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-170">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="264d5-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-171">80</span><span class="sxs-lookup"><span data-stu-id="264d5-171">80</span></span>

<span data-ttu-id="264d5-172">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="264d5-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-173">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="264d5-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-174">81</span><span class="sxs-lookup"><span data-stu-id="264d5-174">81</span></span>

<span data-ttu-id="264d5-175">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="264d5-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-176">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="264d5-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-177">82</span><span class="sxs-lookup"><span data-stu-id="264d5-177">82</span></span>

<span data-ttu-id="264d5-178">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="264d5-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-179">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="264d5-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-180">83</span><span class="sxs-lookup"><span data-stu-id="264d5-180">83</span></span>

<span data-ttu-id="264d5-181">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="264d5-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-182">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="264d5-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-183">84</span><span class="sxs-lookup"><span data-stu-id="264d5-183">84</span></span>

<span data-ttu-id="264d5-184">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="264d5-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-185">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="264d5-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-186">85</span><span class="sxs-lookup"><span data-stu-id="264d5-186">85</span></span>

<span data-ttu-id="264d5-187">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="264d5-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-188">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="264d5-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-189">86</span><span class="sxs-lookup"><span data-stu-id="264d5-189">86</span></span>

<span data-ttu-id="264d5-190">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="264d5-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-191">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="264d5-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-192">87</span><span class="sxs-lookup"><span data-stu-id="264d5-192">87</span></span>

<span data-ttu-id="264d5-193">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="264d5-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-194">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="264d5-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-195">88</span><span class="sxs-lookup"><span data-stu-id="264d5-195">88</span></span>

<span data-ttu-id="264d5-196">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="264d5-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-197">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="264d5-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-198">89</span><span class="sxs-lookup"><span data-stu-id="264d5-198">89</span></span>

<span data-ttu-id="264d5-199">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="264d5-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-200">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="264d5-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-201">90</span><span class="sxs-lookup"><span data-stu-id="264d5-201">90</span></span>

<span data-ttu-id="264d5-202">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="264d5-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-203">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="264d5-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-204">91</span><span class="sxs-lookup"><span data-stu-id="264d5-204">91</span></span>

<span data-ttu-id="264d5-205">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="264d5-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-206">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="264d5-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-207">92</span><span class="sxs-lookup"><span data-stu-id="264d5-207">92</span></span>

<span data-ttu-id="264d5-208">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="264d5-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-209">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="264d5-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-210">93</span><span class="sxs-lookup"><span data-stu-id="264d5-210">93</span></span>

<span data-ttu-id="264d5-211">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="264d5-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-212">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="264d5-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-213">94</span><span class="sxs-lookup"><span data-stu-id="264d5-213">94</span></span>

<span data-ttu-id="264d5-214">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="264d5-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-215">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="264d5-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-216">95</span><span class="sxs-lookup"><span data-stu-id="264d5-216">95</span></span>

<span data-ttu-id="264d5-217">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="264d5-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-218">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="264d5-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-219">96</span><span class="sxs-lookup"><span data-stu-id="264d5-219">96</span></span>

<span data-ttu-id="264d5-220">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="264d5-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-221">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="264d5-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-222">97</span><span class="sxs-lookup"><span data-stu-id="264d5-222">97</span></span>

<span data-ttu-id="264d5-223">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="264d5-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-224">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="264d5-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-225">98</span><span class="sxs-lookup"><span data-stu-id="264d5-225">98</span></span>

<span data-ttu-id="264d5-226">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="264d5-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-227">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="264d5-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-228">100</span><span class="sxs-lookup"><span data-stu-id="264d5-228">100</span></span>

<span data-ttu-id="264d5-229">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="264d5-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="264d5-230">**Другое**</span><span class="sxs-lookup"><span data-stu-id="264d5-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="264d5-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="264d5-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="264d5-232">Комментарии</span><span class="sxs-lookup"><span data-stu-id="264d5-232">Remarks</span></span>

<span data-ttu-id="264d5-233">Выполняя обнаружение MTU и ограничивая размер TCP-сегментов, TCP может исключить фрагментацию маршрутизаторов по пути, соединяющего сети с разными MTU.</span><span class="sxs-lookup"><span data-stu-id="264d5-233">By discovering the Path MTU and limiting TCP segments to this size, TCP can eliminate fragmentation at routers along the path that connect networks with different MTUs.</span></span> <span data-ttu-id="264d5-234">Фрагментация негативно влияет на пропускную способность TCP и перегрузку сети.</span><span class="sxs-lookup"><span data-stu-id="264d5-234">Fragmentation adversely affects TCP throughput and network congestion.</span></span> <span data-ttu-id="264d5-235">Если задать для этого параметра **значение false** , то для всех подключений, которые не являются компьютерами в локальной подсети, будет использоваться значение MTU в 576 байт.</span><span class="sxs-lookup"><span data-stu-id="264d5-235">Setting this parameter to **FALSE** causes an MTU of 576 bytes to be used for all connections that are not to machines on the local subnet</span></span>

## <a name="examples"></a><span data-ttu-id="264d5-236">Примеры</span><span class="sxs-lookup"><span data-stu-id="264d5-236">Examples</span></span>

<span data-ttu-id="264d5-237">Пример [включения обнаружения PMTU на всех сетевых адаптерах](https://Gallery.TechNet.Microsoft.Com/dd68dc8d-d452-484c-add7-2da5c87c3568) VBScript позволяет компьютеру автоматически обнаруживать максимальный блок передачи в сети.</span><span class="sxs-lookup"><span data-stu-id="264d5-237">The [Enable PMTU Discovery on all Network Adapters](https://Gallery.TechNet.Microsoft.Com/dd68dc8d-d452-484c-add7-2da5c87c3568) VBScript sample enables a computer to automatically discover the maximum transmission unit on a network.</span></span>

## <a name="requirements"></a><span data-ttu-id="264d5-238">Требования</span><span class="sxs-lookup"><span data-stu-id="264d5-238">Requirements</span></span>



| <span data-ttu-id="264d5-239">Требование</span><span class="sxs-lookup"><span data-stu-id="264d5-239">Requirement</span></span> | <span data-ttu-id="264d5-240">Значение</span><span class="sxs-lookup"><span data-stu-id="264d5-240">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="264d5-241">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="264d5-241">Minimum supported client</span></span><br/> | <span data-ttu-id="264d5-242">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="264d5-242">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="264d5-243">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="264d5-243">Minimum supported server</span></span><br/> | <span data-ttu-id="264d5-244">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="264d5-244">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="264d5-245">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="264d5-245">Namespace</span></span><br/>                | <span data-ttu-id="264d5-246">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="264d5-246">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="264d5-247">MOF</span><span class="sxs-lookup"><span data-stu-id="264d5-247">MOF</span></span><br/>                      | <dl> <span data-ttu-id="264d5-248"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="264d5-248"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="264d5-249">DLL</span><span class="sxs-lookup"><span data-stu-id="264d5-249">DLL</span></span><br/>                      | <dl> <span data-ttu-id="264d5-250"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="264d5-250"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="264d5-251">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="264d5-251">See also</span></span>

<dl> <dt>

[<span data-ttu-id="264d5-252">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="264d5-252">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="264d5-253">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="264d5-253">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="264d5-254">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="264d5-254">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="264d5-255">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="264d5-255">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="264d5-256">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="264d5-256">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

