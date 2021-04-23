---
description: Статический метод класса Сетпмтубхдетект WMI позволяет обнаруживать маршрутизаторы с черными отверстиями при обнаружении MTU пути.
ms.assetid: a1e45ed9-85a9-4fdd-890a-d578c3f94b72
ms.tgt_platform: multiple
title: Метод Сетпмтубхдетект класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetPMTUBHDetect
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 098652c6ea0a53f9d3b1f616def3dd8b5e7228af
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141863"
---
# <a name="setpmtubhdetect-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="d55e9-103">Метод Сетпмтубхдетект \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="d55e9-103">SetPMTUBHDetect method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="d55e9-104">Статический метод класса **сетпмтубхдетект** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) позволяет обнаруживать маршрутизаторы с черными отверстиями при обнаружении MTU пути.</span><span class="sxs-lookup"><span data-stu-id="d55e9-104">The **SetPMTUBHDetect** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable the detection of Black Hole routers while doing Path MTU Discovery.</span></span>

<span data-ttu-id="d55e9-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="d55e9-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d55e9-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d55e9-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d55e9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d55e9-107">Syntax</span></span>


```mof
uint32 SetPMTUBHDetect(
  [in] boolean PMTUBHDetectEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="d55e9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d55e9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d55e9-109">*Пмтубхдетектенаблед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d55e9-109">*PMTUBHDetectEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-110">Если **значение — true**, TCP пытается обнаружить черные отверстия и маршрутизировать пакеты по различным сетевым путям.</span><span class="sxs-lookup"><span data-stu-id="d55e9-110">If **true**, TCP attempts to discover Black Hole and route packets in different network paths.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d55e9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d55e9-111">Return value</span></span>

<span data-ttu-id="d55e9-112">Возвращает значение 0 (ноль) для успешного завершения, если не требуется перезагрузка, 1 (один) для успешного завершения, когда требуется перезагрузка, и другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="d55e9-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="d55e9-113">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="d55e9-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="d55e9-114">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="d55e9-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="d55e9-115">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="d55e9-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-116">0</span><span class="sxs-lookup"><span data-stu-id="d55e9-116">0</span></span>

<span data-ttu-id="d55e9-117">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="d55e9-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-118">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="d55e9-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-119">1</span><span class="sxs-lookup"><span data-stu-id="d55e9-119">1</span></span>

<span data-ttu-id="d55e9-120">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="d55e9-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-121">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="d55e9-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-122">64</span><span class="sxs-lookup"><span data-stu-id="d55e9-122">64</span></span>

<span data-ttu-id="d55e9-123">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="d55e9-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-124">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="d55e9-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-125">65</span><span class="sxs-lookup"><span data-stu-id="d55e9-125">65</span></span>

<span data-ttu-id="d55e9-126">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="d55e9-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-127">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="d55e9-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-128">66</span><span class="sxs-lookup"><span data-stu-id="d55e9-128">66</span></span>

<span data-ttu-id="d55e9-129">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="d55e9-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-130">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="d55e9-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-131">67</span><span class="sxs-lookup"><span data-stu-id="d55e9-131">67</span></span>

<span data-ttu-id="d55e9-132">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d55e9-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-133">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="d55e9-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-134">68</span><span class="sxs-lookup"><span data-stu-id="d55e9-134">68</span></span>

<span data-ttu-id="d55e9-135">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="d55e9-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-136">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="d55e9-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-137">69</span><span class="sxs-lookup"><span data-stu-id="d55e9-137">69</span></span>

<span data-ttu-id="d55e9-138">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="d55e9-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-139">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="d55e9-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-140">70</span><span class="sxs-lookup"><span data-stu-id="d55e9-140">70</span></span>

<span data-ttu-id="d55e9-141">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="d55e9-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-142">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="d55e9-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-143">71</span><span class="sxs-lookup"><span data-stu-id="d55e9-143">71</span></span>

<span data-ttu-id="d55e9-144">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="d55e9-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-145">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="d55e9-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-146">72</span><span class="sxs-lookup"><span data-stu-id="d55e9-146">72</span></span>

<span data-ttu-id="d55e9-147">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="d55e9-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-148">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="d55e9-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-149">73</span><span class="sxs-lookup"><span data-stu-id="d55e9-149">73</span></span>

<span data-ttu-id="d55e9-150">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="d55e9-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-151">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="d55e9-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-152">74</span><span class="sxs-lookup"><span data-stu-id="d55e9-152">74</span></span>

<span data-ttu-id="d55e9-153">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="d55e9-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-154">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="d55e9-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-155">75</span><span class="sxs-lookup"><span data-stu-id="d55e9-155">75</span></span>

<span data-ttu-id="d55e9-156">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="d55e9-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-157">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="d55e9-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-158">76</span><span class="sxs-lookup"><span data-stu-id="d55e9-158">76</span></span>

<span data-ttu-id="d55e9-159">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="d55e9-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-160">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="d55e9-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-161">77</span><span class="sxs-lookup"><span data-stu-id="d55e9-161">77</span></span>

<span data-ttu-id="d55e9-162">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="d55e9-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-163">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="d55e9-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-164">78</span><span class="sxs-lookup"><span data-stu-id="d55e9-164">78</span></span>

<span data-ttu-id="d55e9-165">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="d55e9-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-166">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="d55e9-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-167">79</span><span class="sxs-lookup"><span data-stu-id="d55e9-167">79</span></span>

<span data-ttu-id="d55e9-168">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="d55e9-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-169">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="d55e9-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-170">80</span><span class="sxs-lookup"><span data-stu-id="d55e9-170">80</span></span>

<span data-ttu-id="d55e9-171">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="d55e9-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-172">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="d55e9-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-173">81</span><span class="sxs-lookup"><span data-stu-id="d55e9-173">81</span></span>

<span data-ttu-id="d55e9-174">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="d55e9-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-175">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="d55e9-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-176">82</span><span class="sxs-lookup"><span data-stu-id="d55e9-176">82</span></span>

<span data-ttu-id="d55e9-177">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="d55e9-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-178">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="d55e9-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-179">83</span><span class="sxs-lookup"><span data-stu-id="d55e9-179">83</span></span>

<span data-ttu-id="d55e9-180">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="d55e9-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-181">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="d55e9-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-182">84</span><span class="sxs-lookup"><span data-stu-id="d55e9-182">84</span></span>

<span data-ttu-id="d55e9-183">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="d55e9-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-184">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="d55e9-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-185">85</span><span class="sxs-lookup"><span data-stu-id="d55e9-185">85</span></span>

<span data-ttu-id="d55e9-186">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="d55e9-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-187">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="d55e9-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-188">86</span><span class="sxs-lookup"><span data-stu-id="d55e9-188">86</span></span>

<span data-ttu-id="d55e9-189">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="d55e9-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-190">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="d55e9-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-191">87</span><span class="sxs-lookup"><span data-stu-id="d55e9-191">87</span></span>

<span data-ttu-id="d55e9-192">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="d55e9-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-193">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="d55e9-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-194">88</span><span class="sxs-lookup"><span data-stu-id="d55e9-194">88</span></span>

<span data-ttu-id="d55e9-195">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="d55e9-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-196">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="d55e9-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-197">89</span><span class="sxs-lookup"><span data-stu-id="d55e9-197">89</span></span>

<span data-ttu-id="d55e9-198">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="d55e9-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-199">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="d55e9-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-200">90</span><span class="sxs-lookup"><span data-stu-id="d55e9-200">90</span></span>

<span data-ttu-id="d55e9-201">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="d55e9-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-202">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="d55e9-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-203">91</span><span class="sxs-lookup"><span data-stu-id="d55e9-203">91</span></span>

<span data-ttu-id="d55e9-204">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="d55e9-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-205">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="d55e9-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-206">92</span><span class="sxs-lookup"><span data-stu-id="d55e9-206">92</span></span>

<span data-ttu-id="d55e9-207">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="d55e9-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-208">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="d55e9-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-209">93</span><span class="sxs-lookup"><span data-stu-id="d55e9-209">93</span></span>

<span data-ttu-id="d55e9-210">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="d55e9-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-211">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="d55e9-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-212">94</span><span class="sxs-lookup"><span data-stu-id="d55e9-212">94</span></span>

<span data-ttu-id="d55e9-213">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="d55e9-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-214">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="d55e9-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-215">95</span><span class="sxs-lookup"><span data-stu-id="d55e9-215">95</span></span>

<span data-ttu-id="d55e9-216">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="d55e9-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-217">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="d55e9-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-218">96</span><span class="sxs-lookup"><span data-stu-id="d55e9-218">96</span></span>

<span data-ttu-id="d55e9-219">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="d55e9-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-220">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="d55e9-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-221">97</span><span class="sxs-lookup"><span data-stu-id="d55e9-221">97</span></span>

<span data-ttu-id="d55e9-222">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="d55e9-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-223">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="d55e9-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-224">98</span><span class="sxs-lookup"><span data-stu-id="d55e9-224">98</span></span>

<span data-ttu-id="d55e9-225">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="d55e9-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-226">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="d55e9-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-227">100</span><span class="sxs-lookup"><span data-stu-id="d55e9-227">100</span></span>

<span data-ttu-id="d55e9-228">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="d55e9-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d55e9-229">**Другое**</span><span class="sxs-lookup"><span data-stu-id="d55e9-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="d55e9-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="d55e9-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d55e9-231">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d55e9-231">Remarks</span></span>

<span data-ttu-id="d55e9-232">Маршрутизатор с черными отверстиями не возвращает сообщения о назначении протокола ICMP, когда требуется фрагментировать IP-датаграмму с установленным битом «не фрагментировать».</span><span class="sxs-lookup"><span data-stu-id="d55e9-232">A Black Hole router does not return the Internet Control Message Protocol (ICMP) Destination Unreachable messages when it needs to fragment an IP datagram with the Don't Fragment bit set.</span></span> <span data-ttu-id="d55e9-233">Протокол TCP зависит от получения этих сообщений для выполнения обнаружения MTU пути.</span><span class="sxs-lookup"><span data-stu-id="d55e9-233">TCP depends on receiving these messages to perform Path MTU Discovery.</span></span>

<span data-ttu-id="d55e9-234">Если эта функция включена, протокол TCP попытается отправить сегменты без установленного бита дефрагментации, если несколько повторных передач сегмента попадают в неподтвержденные.</span><span class="sxs-lookup"><span data-stu-id="d55e9-234">With this feature enabled, TCP will try to send segments without the Don't Fragment bit set if several retransmissions of a segment go unacknowledged.</span></span> <span data-ttu-id="d55e9-235">Если сегмент подтвержден как результат, максимальный размер сегмента (MSS) будет уменьшен, а в будущих пакетах соединения будет установлен бит не фрагмента.</span><span class="sxs-lookup"><span data-stu-id="d55e9-235">If the segment is acknowledged as a result, the maximum segment size (MSS) will be decreased and the Don't Fragment bit will be set in future packets on the connection.</span></span> <span data-ttu-id="d55e9-236">Включение обнаружения "Черная дыра" увеличивает максимальное число повторных передач, выполненных для данного сегмента.</span><span class="sxs-lookup"><span data-stu-id="d55e9-236">Enabling black hole detection increases the maximum number of retransmissions performed for a given segment.</span></span>

## <a name="examples"></a><span data-ttu-id="d55e9-237">Примеры</span><span class="sxs-lookup"><span data-stu-id="d55e9-237">Examples</span></span>

<span data-ttu-id="d55e9-238">[Обнаружение Пмтубх изменения на всех сетевых адаптерах](https://Gallery.TechNet.Microsoft.Com/a576d97b-38fe-437e-a632-d2f7e122301c) позволяет выполнять автоматическое обнаружение маршрутизаторов с черными отверстиями при определении максимального блока передачи в сети.</span><span class="sxs-lookup"><span data-stu-id="d55e9-238">The [Modify PMTUBH Detection on All Network Adapters](https://Gallery.TechNet.Microsoft.Com/a576d97b-38fe-437e-a632-d2f7e122301c) enables the auto-discovery of black hole routers when determining the maximum transmission unit on a network.</span></span>

## <a name="requirements"></a><span data-ttu-id="d55e9-239">Требования</span><span class="sxs-lookup"><span data-stu-id="d55e9-239">Requirements</span></span>



| <span data-ttu-id="d55e9-240">Требование</span><span class="sxs-lookup"><span data-stu-id="d55e9-240">Requirement</span></span> | <span data-ttu-id="d55e9-241">Значение</span><span class="sxs-lookup"><span data-stu-id="d55e9-241">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d55e9-242">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d55e9-242">Minimum supported client</span></span><br/> | <span data-ttu-id="d55e9-243">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d55e9-243">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d55e9-244">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d55e9-244">Minimum supported server</span></span><br/> | <span data-ttu-id="d55e9-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d55e9-245">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d55e9-246">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d55e9-246">Namespace</span></span><br/>                | <span data-ttu-id="d55e9-247">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d55e9-247">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d55e9-248">MOF</span><span class="sxs-lookup"><span data-stu-id="d55e9-248">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d55e9-249"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d55e9-249"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d55e9-250">DLL</span><span class="sxs-lookup"><span data-stu-id="d55e9-250">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d55e9-251"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d55e9-251"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d55e9-252">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d55e9-252">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d55e9-253">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="d55e9-253">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="d55e9-254">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="d55e9-254">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="d55e9-255">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="d55e9-255">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="d55e9-256">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="d55e9-256">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="d55e9-257">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="d55e9-257">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

