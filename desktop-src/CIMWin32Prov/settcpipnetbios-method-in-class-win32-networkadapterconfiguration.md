---
description: Метод Сетткпипнетбиос используется для задания по умолчанию операции NetBIOS через TCP/IP.
ms.assetid: 2c639595-da13-400d-b4d0-432b39460554
ms.tgt_platform: multiple
title: Метод Сетткпипнетбиос класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpipNetbios
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 20ecab5918d00dc5f189464becc0252f2a8c0569
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896494"
---
# <a name="settcpipnetbios-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="40997-103">Метод Сетткпипнетбиос \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="40997-103">SetTcpipNetbios method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="40997-104">Метод **сетткпипнетбиос** используется для задания по умолчанию операции NetBIOS через TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="40997-104">The **SetTcpipNetbios** method is used to set the default operation of NetBIOS over TCP/IP.</span></span>

<span data-ttu-id="40997-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="40997-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="40997-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="40997-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="40997-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="40997-107">Syntax</span></span>


```mof
uint32 SetTcpipNetbios(
  [in] uint32 TcpipNetbiosOptions
);
```



## <a name="parameters"></a><span data-ttu-id="40997-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="40997-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40997-109">*Ткпипнетбиосоптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="40997-109">*TcpipNetbiosOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40997-110">Значение, указывающее возможные параметры, связанные с NetBIOS через TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="40997-110">Value that specifies the possible settings related to NetBIOS over TCP/IP.</span></span>

<dt>

<span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>

<span data-ttu-id="40997-111"><span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>**Енабленетбиосвиадхкп** (0)</span><span class="sxs-lookup"><span data-stu-id="40997-111"><span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>**EnableNetbiosViaDhcp** (0)</span></span>


</dt> <dd>

<span data-ttu-id="40997-112">Включение NetBIOS через DHCP</span><span class="sxs-lookup"><span data-stu-id="40997-112">Enable Netbios via DHCP</span></span>

</dd> <dt>

<span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>

<span data-ttu-id="40997-113"><span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>**EnableNetbios** (1)</span><span class="sxs-lookup"><span data-stu-id="40997-113"><span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>**EnableNetbios** (1)</span></span>


</dt> <dd>

<span data-ttu-id="40997-114">Включить NetBIOS</span><span class="sxs-lookup"><span data-stu-id="40997-114">Enable Netbios</span></span>

</dd> <dt>

<span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>

<span data-ttu-id="40997-115"><span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>**Дисабленетбиос** (2)</span><span class="sxs-lookup"><span data-stu-id="40997-115"><span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>**DisableNetbios** (2)</span></span>


</dt> <dd>

<span data-ttu-id="40997-116">Отключить NetBIOS</span><span class="sxs-lookup"><span data-stu-id="40997-116">Disable Netbios</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40997-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="40997-117">Return value</span></span>

<span data-ttu-id="40997-118">Возвращает значение 0 (ноль) для успешного завершения, если не требуется перезагрузка, 1 (один) для успешного завершения, когда требуется перезагрузка, и другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="40997-118">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="40997-119">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="40997-119">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="40997-120">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="40997-120">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="40997-121">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="40997-121">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="40997-122">0</span><span class="sxs-lookup"><span data-stu-id="40997-122">0</span></span>

<span data-ttu-id="40997-123">Успешное завершение.</span><span class="sxs-lookup"><span data-stu-id="40997-123">Successful completion.</span></span> <span data-ttu-id="40997-124">Перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="40997-124">No reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="40997-125">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="40997-125">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="40997-126">1</span><span class="sxs-lookup"><span data-stu-id="40997-126">1</span></span>

<span data-ttu-id="40997-127">Успешное завершение.</span><span class="sxs-lookup"><span data-stu-id="40997-127">Successful completion.</span></span> <span data-ttu-id="40997-128">Требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="40997-128">Reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="40997-129">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="40997-129">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="40997-130">64</span><span class="sxs-lookup"><span data-stu-id="40997-130">64</span></span>

<span data-ttu-id="40997-131">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="40997-131">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="40997-132">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="40997-132">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="40997-133">65</span><span class="sxs-lookup"><span data-stu-id="40997-133">65</span></span>

<span data-ttu-id="40997-134">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="40997-134">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="40997-135">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="40997-135">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="40997-136">66</span><span class="sxs-lookup"><span data-stu-id="40997-136">66</span></span>

<span data-ttu-id="40997-137">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="40997-137">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="40997-138">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="40997-138">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="40997-139">67</span><span class="sxs-lookup"><span data-stu-id="40997-139">67</span></span>

<span data-ttu-id="40997-140">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="40997-140">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="40997-141">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="40997-141">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="40997-142">68</span><span class="sxs-lookup"><span data-stu-id="40997-142">68</span></span>

<span data-ttu-id="40997-143">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="40997-143">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="40997-144">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="40997-144">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="40997-145">69</span><span class="sxs-lookup"><span data-stu-id="40997-145">69</span></span>

<span data-ttu-id="40997-146">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="40997-146">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="40997-147">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="40997-147">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="40997-148">70</span><span class="sxs-lookup"><span data-stu-id="40997-148">70</span></span>

<span data-ttu-id="40997-149">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="40997-149">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="40997-150">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="40997-150">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="40997-151">71</span><span class="sxs-lookup"><span data-stu-id="40997-151">71</span></span>

<span data-ttu-id="40997-152">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="40997-152">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="40997-153">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="40997-153">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="40997-154">72</span><span class="sxs-lookup"><span data-stu-id="40997-154">72</span></span>

<span data-ttu-id="40997-155">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="40997-155">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="40997-156">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="40997-156">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="40997-157">73</span><span class="sxs-lookup"><span data-stu-id="40997-157">73</span></span>

<span data-ttu-id="40997-158">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="40997-158">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="40997-159">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="40997-159">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="40997-160">74</span><span class="sxs-lookup"><span data-stu-id="40997-160">74</span></span>

<span data-ttu-id="40997-161">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="40997-161">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="40997-162">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="40997-162">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="40997-163">75</span><span class="sxs-lookup"><span data-stu-id="40997-163">75</span></span>

<span data-ttu-id="40997-164">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="40997-164">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="40997-165">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="40997-165">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="40997-166">76</span><span class="sxs-lookup"><span data-stu-id="40997-166">76</span></span>

<span data-ttu-id="40997-167">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="40997-167">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="40997-168">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="40997-168">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="40997-169">77</span><span class="sxs-lookup"><span data-stu-id="40997-169">77</span></span>

<span data-ttu-id="40997-170">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="40997-170">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="40997-171">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="40997-171">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="40997-172">78</span><span class="sxs-lookup"><span data-stu-id="40997-172">78</span></span>

<span data-ttu-id="40997-173">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="40997-173">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="40997-174">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="40997-174">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="40997-175">79</span><span class="sxs-lookup"><span data-stu-id="40997-175">79</span></span>

<span data-ttu-id="40997-176">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="40997-176">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="40997-177">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="40997-177">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="40997-178">80</span><span class="sxs-lookup"><span data-stu-id="40997-178">80</span></span>

<span data-ttu-id="40997-179">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="40997-179">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="40997-180">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="40997-180">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="40997-181">81</span><span class="sxs-lookup"><span data-stu-id="40997-181">81</span></span>

<span data-ttu-id="40997-182">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="40997-182">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="40997-183">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="40997-183">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="40997-184">82</span><span class="sxs-lookup"><span data-stu-id="40997-184">82</span></span>

<span data-ttu-id="40997-185">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="40997-185">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="40997-186">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="40997-186">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="40997-187">83</span><span class="sxs-lookup"><span data-stu-id="40997-187">83</span></span>

<span data-ttu-id="40997-188">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="40997-188">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="40997-189">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="40997-189">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="40997-190">84</span><span class="sxs-lookup"><span data-stu-id="40997-190">84</span></span>

<span data-ttu-id="40997-191">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="40997-191">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="40997-192">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="40997-192">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="40997-193">85</span><span class="sxs-lookup"><span data-stu-id="40997-193">85</span></span>

<span data-ttu-id="40997-194">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="40997-194">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="40997-195">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="40997-195">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="40997-196">86</span><span class="sxs-lookup"><span data-stu-id="40997-196">86</span></span>

<span data-ttu-id="40997-197">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="40997-197">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="40997-198">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="40997-198">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="40997-199">87</span><span class="sxs-lookup"><span data-stu-id="40997-199">87</span></span>

<span data-ttu-id="40997-200">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="40997-200">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="40997-201">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="40997-201">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="40997-202">88</span><span class="sxs-lookup"><span data-stu-id="40997-202">88</span></span>

<span data-ttu-id="40997-203">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="40997-203">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="40997-204">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="40997-204">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="40997-205">89</span><span class="sxs-lookup"><span data-stu-id="40997-205">89</span></span>

<span data-ttu-id="40997-206">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="40997-206">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="40997-207">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="40997-207">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="40997-208">90</span><span class="sxs-lookup"><span data-stu-id="40997-208">90</span></span>

<span data-ttu-id="40997-209">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="40997-209">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="40997-210">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="40997-210">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="40997-211">91</span><span class="sxs-lookup"><span data-stu-id="40997-211">91</span></span>

<span data-ttu-id="40997-212">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="40997-212">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="40997-213">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="40997-213">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="40997-214">92</span><span class="sxs-lookup"><span data-stu-id="40997-214">92</span></span>

<span data-ttu-id="40997-215">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="40997-215">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="40997-216">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="40997-216">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="40997-217">93</span><span class="sxs-lookup"><span data-stu-id="40997-217">93</span></span>

<span data-ttu-id="40997-218">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="40997-218">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="40997-219">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="40997-219">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="40997-220">94</span><span class="sxs-lookup"><span data-stu-id="40997-220">94</span></span>

<span data-ttu-id="40997-221">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="40997-221">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="40997-222">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="40997-222">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="40997-223">95</span><span class="sxs-lookup"><span data-stu-id="40997-223">95</span></span>

<span data-ttu-id="40997-224">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="40997-224">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="40997-225">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="40997-225">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="40997-226">96</span><span class="sxs-lookup"><span data-stu-id="40997-226">96</span></span>

<span data-ttu-id="40997-227">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="40997-227">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="40997-228">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="40997-228">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="40997-229">97</span><span class="sxs-lookup"><span data-stu-id="40997-229">97</span></span>

<span data-ttu-id="40997-230">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="40997-230">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="40997-231">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="40997-231">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="40997-232">98</span><span class="sxs-lookup"><span data-stu-id="40997-232">98</span></span>

<span data-ttu-id="40997-233">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="40997-233">Not all DHCP leases can be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="40997-234">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="40997-234">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="40997-235">100</span><span class="sxs-lookup"><span data-stu-id="40997-235">100</span></span>

<span data-ttu-id="40997-236">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="40997-236">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="40997-237">**Другое**</span><span class="sxs-lookup"><span data-stu-id="40997-237">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="40997-238">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="40997-238">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="40997-239">Примеры</span><span class="sxs-lookup"><span data-stu-id="40997-239">Examples</span></span>

<span data-ttu-id="40997-240">Пример [изменения протокола NetBIOS USE в сетевом адаптере](https://Gallery.TechNet.Microsoft.Com/01d541f7-5c0d-46d3-8619-28aaab154dc0) на языке VBScript включает протокол NetBIOS для сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="40997-240">The [Modify NetBIOS Use on a Network Adapter](https://Gallery.TechNet.Microsoft.Com/01d541f7-5c0d-46d3-8619-28aaab154dc0) VBScript sample enables NetBIOS for a network adapter.</span></span>

<span data-ttu-id="40997-241">На странице [Настройка сетевых адаптеров iSCSI согласно рекомендациям Microsoft PowerShell для каждого](https://Gallery.TechNet.Microsoft.Com/Configure-iSCSI-Network-81232a5e) из них автоматизируются параметры конфигурации для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="40997-241">The [Configure iSCSI Network Cards as per Microsoft Best Practices PowerShell](https://Gallery.TechNet.Microsoft.Com/Configure-iSCSI-Network-81232a5e) sample automates the configuration settings for a Virtual Machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="40997-242">Требования</span><span class="sxs-lookup"><span data-stu-id="40997-242">Requirements</span></span>



| <span data-ttu-id="40997-243">Требование</span><span class="sxs-lookup"><span data-stu-id="40997-243">Requirement</span></span> | <span data-ttu-id="40997-244">Значение</span><span class="sxs-lookup"><span data-stu-id="40997-244">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40997-245">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="40997-245">Minimum supported client</span></span><br/> | <span data-ttu-id="40997-246">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40997-246">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="40997-247">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="40997-247">Minimum supported server</span></span><br/> | <span data-ttu-id="40997-248">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40997-248">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="40997-249">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="40997-249">Namespace</span></span><br/>                | <span data-ttu-id="40997-250">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="40997-250">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="40997-251">MOF</span><span class="sxs-lookup"><span data-stu-id="40997-251">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40997-252"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="40997-252"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="40997-253">DLL</span><span class="sxs-lookup"><span data-stu-id="40997-253">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40997-254"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40997-254"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40997-255">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="40997-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40997-256">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="40997-256">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="40997-257">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="40997-257">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="40997-258">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="40997-258">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="40997-259">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="40997-259">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="40997-260">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="40997-260">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

