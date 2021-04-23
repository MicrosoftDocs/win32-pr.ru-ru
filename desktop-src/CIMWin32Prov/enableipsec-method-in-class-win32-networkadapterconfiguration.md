---
description: Енаблеипсек&\# 8194; Метод класса WMI включает протокол IPsec на сетевом адаптере с поддержкой TCP/IP.
ms.assetid: 0a45d864-606d-4adb-9b51-62d46a0d68b1
ms.tgt_platform: multiple
title: Метод Енаблеипсек класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableIPSec
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6988d68f9939752e3c8c2c9ace063b895a2d3720
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895725"
---
# <a name="enableipsec-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="63bad-103">Метод Енаблеипсек \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="63bad-103">EnableIPSec method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="63bad-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) енаблеипсек включает протокол IPsec на сетевом адаптере с поддержкой TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="63bad-104">The **EnableIPSec** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method enables Internet Protocol security (IPsec) on a TCP/IP-enabled network adapter.</span></span>

<span data-ttu-id="63bad-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="63bad-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="63bad-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="63bad-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="63bad-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63bad-107">Syntax</span></span>


```mof
uint32 EnableIPSec(
  [in] string IPSecPermitTCPPorts[],
  [in] string IPSecPermitUDPPorts[],
  [in] string IPSecPermitIPProtocols[]
);
```



## <a name="parameters"></a><span data-ttu-id="63bad-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="63bad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63bad-109">*Ипсекпермитткппортс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63bad-109">*IPSecPermitTCPPorts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63bad-110">Список портов, которым предоставляется разрешение на доступ для TCP.</span><span class="sxs-lookup"><span data-stu-id="63bad-110">List of ports to be granted access permission for TCP.</span></span> <span data-ttu-id="63bad-111">Числовое значение 0 (ноль) означает, что разрешение на доступ предоставляется для всех портов.</span><span class="sxs-lookup"><span data-stu-id="63bad-111">A numeric value of 0 (zero) indicates access permission is granted for all ports.</span></span> <span data-ttu-id="63bad-112">Пустой массив указывает, что нет ни одного порта, которым предоставляется разрешение на доступ.</span><span class="sxs-lookup"><span data-stu-id="63bad-112">An empty array indicates that no ports are to be granted access permission.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-113">*Ипсекпермитудппортс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63bad-113">*IPSecPermitUDPPorts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63bad-114">Список портов, которым предоставляется разрешение на доступ к UDP.</span><span class="sxs-lookup"><span data-stu-id="63bad-114">List of ports to be granted access permission for UDP.</span></span> <span data-ttu-id="63bad-115">Числовое значение 0 (ноль) означает, что разрешение на доступ предоставляется для всех портов.</span><span class="sxs-lookup"><span data-stu-id="63bad-115">A numeric value of 0 (zero) indicates access permission is granted for all ports.</span></span> <span data-ttu-id="63bad-116">Пустой массив указывает, что нет ни одного порта, которым предоставляется разрешение на доступ.</span><span class="sxs-lookup"><span data-stu-id="63bad-116">An empty array indicates that no ports are to be granted access permission.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-117">*Ипсекпермитиппротоколс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63bad-117">*IPSecPermitIPProtocols* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63bad-118">Список протоколов, разрешенных для запуска по IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="63bad-118">List of protocols permitted to run over the IP.</span></span> <span data-ttu-id="63bad-119">Числовое значение 0 (ноль) означает, что разрешение на доступ предоставляется для всех протоколов.</span><span class="sxs-lookup"><span data-stu-id="63bad-119">A numeric value of 0 (zero) indicates access permission is granted for all protocols.</span></span> <span data-ttu-id="63bad-120">Пустой массив указывает, что нет протоколов, которым предоставлено разрешение на доступ.</span><span class="sxs-lookup"><span data-stu-id="63bad-120">An empty array indicates that no protocols are granted access permission.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63bad-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63bad-121">Return value</span></span>

<span data-ttu-id="63bad-122">Возвращает значение 0 (ноль) для успешного завершения, если перезагрузка не требуется, 1 (один) для успешного завершения, когда требуется перезагрузка, и любое другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="63bad-122">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="63bad-123">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="63bad-123">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="63bad-124">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="63bad-124">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="63bad-125">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="63bad-125">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-126">0</span><span class="sxs-lookup"><span data-stu-id="63bad-126">0</span></span>

<span data-ttu-id="63bad-127">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="63bad-127">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-128">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="63bad-128">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-129">1</span><span class="sxs-lookup"><span data-stu-id="63bad-129">1</span></span>

<span data-ttu-id="63bad-130">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="63bad-130">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-131">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="63bad-131">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-132">64</span><span class="sxs-lookup"><span data-stu-id="63bad-132">64</span></span>

<span data-ttu-id="63bad-133">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="63bad-133">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-134">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="63bad-134">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-135">65</span><span class="sxs-lookup"><span data-stu-id="63bad-135">65</span></span>

<span data-ttu-id="63bad-136">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="63bad-136">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-137">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="63bad-137">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-138">66</span><span class="sxs-lookup"><span data-stu-id="63bad-138">66</span></span>

<span data-ttu-id="63bad-139">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="63bad-139">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-140">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="63bad-140">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-141">67</span><span class="sxs-lookup"><span data-stu-id="63bad-141">67</span></span>

<span data-ttu-id="63bad-142">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="63bad-142">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-143">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="63bad-143">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-144">68</span><span class="sxs-lookup"><span data-stu-id="63bad-144">68</span></span>

<span data-ttu-id="63bad-145">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="63bad-145">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-146">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="63bad-146">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-147">69</span><span class="sxs-lookup"><span data-stu-id="63bad-147">69</span></span>

<span data-ttu-id="63bad-148">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="63bad-148">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-149">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="63bad-149">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-150">70</span><span class="sxs-lookup"><span data-stu-id="63bad-150">70</span></span>

<span data-ttu-id="63bad-151">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="63bad-151">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-152">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="63bad-152">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-153">71</span><span class="sxs-lookup"><span data-stu-id="63bad-153">71</span></span>

<span data-ttu-id="63bad-154">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="63bad-154">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-155">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="63bad-155">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-156">72</span><span class="sxs-lookup"><span data-stu-id="63bad-156">72</span></span>

<span data-ttu-id="63bad-157">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="63bad-157">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-158">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="63bad-158">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-159">73</span><span class="sxs-lookup"><span data-stu-id="63bad-159">73</span></span>

<span data-ttu-id="63bad-160">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="63bad-160">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-161">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="63bad-161">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-162">74</span><span class="sxs-lookup"><span data-stu-id="63bad-162">74</span></span>

<span data-ttu-id="63bad-163">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="63bad-163">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-164">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="63bad-164">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-165">75</span><span class="sxs-lookup"><span data-stu-id="63bad-165">75</span></span>

<span data-ttu-id="63bad-166">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="63bad-166">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-167">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="63bad-167">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-168">76</span><span class="sxs-lookup"><span data-stu-id="63bad-168">76</span></span>

<span data-ttu-id="63bad-169">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="63bad-169">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-170">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="63bad-170">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-171">77</span><span class="sxs-lookup"><span data-stu-id="63bad-171">77</span></span>

<span data-ttu-id="63bad-172">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="63bad-172">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-173">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="63bad-173">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-174">78</span><span class="sxs-lookup"><span data-stu-id="63bad-174">78</span></span>

<span data-ttu-id="63bad-175">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="63bad-175">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-176">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="63bad-176">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-177">79</span><span class="sxs-lookup"><span data-stu-id="63bad-177">79</span></span>

<span data-ttu-id="63bad-178">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="63bad-178">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-179">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="63bad-179">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-180">80</span><span class="sxs-lookup"><span data-stu-id="63bad-180">80</span></span>

<span data-ttu-id="63bad-181">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="63bad-181">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-182">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="63bad-182">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-183">81</span><span class="sxs-lookup"><span data-stu-id="63bad-183">81</span></span>

<span data-ttu-id="63bad-184">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="63bad-184">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-185">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="63bad-185">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-186">82</span><span class="sxs-lookup"><span data-stu-id="63bad-186">82</span></span>

<span data-ttu-id="63bad-187">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="63bad-187">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-188">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="63bad-188">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-189">83</span><span class="sxs-lookup"><span data-stu-id="63bad-189">83</span></span>

<span data-ttu-id="63bad-190">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="63bad-190">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-191">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="63bad-191">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-192">84</span><span class="sxs-lookup"><span data-stu-id="63bad-192">84</span></span>

<span data-ttu-id="63bad-193">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="63bad-193">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-194">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="63bad-194">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-195">85</span><span class="sxs-lookup"><span data-stu-id="63bad-195">85</span></span>

<span data-ttu-id="63bad-196">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="63bad-196">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-197">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="63bad-197">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-198">86</span><span class="sxs-lookup"><span data-stu-id="63bad-198">86</span></span>

<span data-ttu-id="63bad-199">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="63bad-199">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-200">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="63bad-200">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-201">87</span><span class="sxs-lookup"><span data-stu-id="63bad-201">87</span></span>

<span data-ttu-id="63bad-202">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="63bad-202">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-203">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="63bad-203">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-204">88</span><span class="sxs-lookup"><span data-stu-id="63bad-204">88</span></span>

<span data-ttu-id="63bad-205">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="63bad-205">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-206">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="63bad-206">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-207">89</span><span class="sxs-lookup"><span data-stu-id="63bad-207">89</span></span>

<span data-ttu-id="63bad-208">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="63bad-208">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-209">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="63bad-209">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-210">90</span><span class="sxs-lookup"><span data-stu-id="63bad-210">90</span></span>

<span data-ttu-id="63bad-211">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="63bad-211">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-212">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="63bad-212">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-213">91</span><span class="sxs-lookup"><span data-stu-id="63bad-213">91</span></span>

<span data-ttu-id="63bad-214">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="63bad-214">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-215">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="63bad-215">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-216">92</span><span class="sxs-lookup"><span data-stu-id="63bad-216">92</span></span>

<span data-ttu-id="63bad-217">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="63bad-217">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-218">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="63bad-218">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-219">93</span><span class="sxs-lookup"><span data-stu-id="63bad-219">93</span></span>

<span data-ttu-id="63bad-220">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="63bad-220">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-221">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="63bad-221">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-222">94</span><span class="sxs-lookup"><span data-stu-id="63bad-222">94</span></span>

<span data-ttu-id="63bad-223">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="63bad-223">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-224">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="63bad-224">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-225">95</span><span class="sxs-lookup"><span data-stu-id="63bad-225">95</span></span>

<span data-ttu-id="63bad-226">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="63bad-226">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-227">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="63bad-227">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-228">96</span><span class="sxs-lookup"><span data-stu-id="63bad-228">96</span></span>

<span data-ttu-id="63bad-229">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="63bad-229">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-230">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="63bad-230">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-231">97</span><span class="sxs-lookup"><span data-stu-id="63bad-231">97</span></span>

<span data-ttu-id="63bad-232">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="63bad-232">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-233">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="63bad-233">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-234">98</span><span class="sxs-lookup"><span data-stu-id="63bad-234">98</span></span>

<span data-ttu-id="63bad-235">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="63bad-235">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-236">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="63bad-236">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-237">100</span><span class="sxs-lookup"><span data-stu-id="63bad-237">100</span></span>

<span data-ttu-id="63bad-238">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="63bad-238">DHCP not enabled on the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="63bad-239">**Другое**</span><span class="sxs-lookup"><span data-stu-id="63bad-239">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="63bad-240">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="63bad-240">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="63bad-241">Комментарии</span><span class="sxs-lookup"><span data-stu-id="63bad-241">Remarks</span></span>

<span data-ttu-id="63bad-242">Порты защищаются только в том случае, если свойство **ипфилтерсекуритенаблед** в [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="63bad-242">Ports are secured only when the **IPFilterSecurityEnabled** property in [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) is **true**.</span></span>

## <a name="examples"></a><span data-ttu-id="63bad-243">Примеры</span><span class="sxs-lookup"><span data-stu-id="63bad-243">Examples</span></span>

<span data-ttu-id="63bad-244">Пример [включения IPsec на сетевом адаптере](https://Gallery.TechNet.Microsoft.Com/ff821218-c392-42fb-a77c-c3eab899587c) VBScript в коллекции TechNet использует **енаблеипсек** для включения IP-безопасности для сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="63bad-244">The [Enable IPSec on a Network Adapter](https://Gallery.TechNet.Microsoft.Com/ff821218-c392-42fb-a77c-c3eab899587c) VBScript sample, on TechNet Gallery, uses **EnableIPSec** to enable IP security for a network adapter.</span></span>

## <a name="requirements"></a><span data-ttu-id="63bad-245">Требования</span><span class="sxs-lookup"><span data-stu-id="63bad-245">Requirements</span></span>



| <span data-ttu-id="63bad-246">Требование</span><span class="sxs-lookup"><span data-stu-id="63bad-246">Requirement</span></span> | <span data-ttu-id="63bad-247">Значение</span><span class="sxs-lookup"><span data-stu-id="63bad-247">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63bad-248">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63bad-248">Minimum supported client</span></span><br/> | <span data-ttu-id="63bad-249">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="63bad-249">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="63bad-250">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63bad-250">Minimum supported server</span></span><br/> | <span data-ttu-id="63bad-251">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63bad-251">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="63bad-252">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="63bad-252">Namespace</span></span><br/>                | <span data-ttu-id="63bad-253">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="63bad-253">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="63bad-254">MOF</span><span class="sxs-lookup"><span data-stu-id="63bad-254">MOF</span></span><br/>                      | <dl> <span data-ttu-id="63bad-255"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="63bad-255"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="63bad-256">DLL</span><span class="sxs-lookup"><span data-stu-id="63bad-256">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63bad-257"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63bad-257"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63bad-258">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63bad-258">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63bad-259">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="63bad-259">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="63bad-260">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="63bad-260">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="63bad-261">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="63bad-261">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="63bad-262">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="63bad-262">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="63bad-263">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="63bad-263">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

