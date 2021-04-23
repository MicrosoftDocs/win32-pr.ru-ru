---
description: Метод класса WMI EnableStatic включает статическую адресацию TCP/IP для целевого сетевого адаптера. В результате DHCP для этого сетевого адаптера отключен.
ms.assetid: d0076424-58c0-4cfe-b55b-44c0f2620388
ms.tgt_platform: multiple
title: Метод EnableStatic класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableStatic
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 74a7b9ca8c8016cca5a78f2e7fe753f00398193e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807258"
---
# <a name="enablestatic-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="934cc-104">Метод EnableStatic \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="934cc-104">EnableStatic method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="934cc-105">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) EnableStatic включает статическую адресацию TCP/IP для целевого сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="934cc-105">The **EnableStatic** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method enables static TCP/IP addressing for the target network adapter.</span></span> <span data-ttu-id="934cc-106">В результате DHCP для этого сетевого адаптера отключен.</span><span class="sxs-lookup"><span data-stu-id="934cc-106">As a result, DHCP for this network adapter is disabled.</span></span>

<span data-ttu-id="934cc-107">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="934cc-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="934cc-108">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="934cc-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="934cc-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="934cc-109">Syntax</span></span>


```mof
uint32 EnableStatic(
  [in] string IPAddress[],
  [in] string SubnetMask[]
);
```



## <a name="parameters"></a><span data-ttu-id="934cc-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="934cc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="934cc-111">*IP-адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="934cc-111">*IPAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="934cc-112">Список всех статических IP-адресов для текущего сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="934cc-112">Lists all of the static IP addresses for the current network adapter.</span></span>

<span data-ttu-id="934cc-113">Пример: 155.34.22.0.</span><span class="sxs-lookup"><span data-stu-id="934cc-113">Example: 155.34.22.0.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-114">*Маска* \[ подсети окне\]</span><span class="sxs-lookup"><span data-stu-id="934cc-114">*SubnetMask* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="934cc-115">Маски подсети, дополняющие значения параметра *IPAddress* .</span><span class="sxs-lookup"><span data-stu-id="934cc-115">Subnet masks that complement the values in the *IPAddress* parameter.</span></span>

<span data-ttu-id="934cc-116">Пример: 255.255.0.0.</span><span class="sxs-lookup"><span data-stu-id="934cc-116">Example: 255.255.0.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="934cc-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="934cc-117">Return value</span></span>

<span data-ttu-id="934cc-118">Возвращает значение 0 (ноль) для успешного завершения, если перезагрузка не требуется, 1 (один) для успешного завершения, когда требуется перезагрузка, и любое другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="934cc-118">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="934cc-119">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="934cc-119">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="934cc-120">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="934cc-120">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="934cc-121">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="934cc-121">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-122">0</span><span class="sxs-lookup"><span data-stu-id="934cc-122">0</span></span>

<span data-ttu-id="934cc-123">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="934cc-123">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-124">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="934cc-124">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-125">1</span><span class="sxs-lookup"><span data-stu-id="934cc-125">1</span></span>

<span data-ttu-id="934cc-126">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="934cc-126">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-127">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="934cc-127">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-128">64</span><span class="sxs-lookup"><span data-stu-id="934cc-128">64</span></span>

<span data-ttu-id="934cc-129">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="934cc-129">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-130">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="934cc-130">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-131">65</span><span class="sxs-lookup"><span data-stu-id="934cc-131">65</span></span>

<span data-ttu-id="934cc-132">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="934cc-132">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-133">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="934cc-133">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-134">66</span><span class="sxs-lookup"><span data-stu-id="934cc-134">66</span></span>

<span data-ttu-id="934cc-135">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="934cc-135">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-136">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="934cc-136">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-137">67</span><span class="sxs-lookup"><span data-stu-id="934cc-137">67</span></span>

<span data-ttu-id="934cc-138">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="934cc-138">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-139">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="934cc-139">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-140">68</span><span class="sxs-lookup"><span data-stu-id="934cc-140">68</span></span>

<span data-ttu-id="934cc-141">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="934cc-141">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-142">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="934cc-142">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-143">69</span><span class="sxs-lookup"><span data-stu-id="934cc-143">69</span></span>

<span data-ttu-id="934cc-144">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="934cc-144">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-145">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="934cc-145">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-146">70</span><span class="sxs-lookup"><span data-stu-id="934cc-146">70</span></span>

<span data-ttu-id="934cc-147">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="934cc-147">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-148">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="934cc-148">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-149">71</span><span class="sxs-lookup"><span data-stu-id="934cc-149">71</span></span>

<span data-ttu-id="934cc-150">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="934cc-150">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-151">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="934cc-151">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-152">72</span><span class="sxs-lookup"><span data-stu-id="934cc-152">72</span></span>

<span data-ttu-id="934cc-153">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="934cc-153">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-154">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="934cc-154">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-155">73</span><span class="sxs-lookup"><span data-stu-id="934cc-155">73</span></span>

<span data-ttu-id="934cc-156">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="934cc-156">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-157">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="934cc-157">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-158">74</span><span class="sxs-lookup"><span data-stu-id="934cc-158">74</span></span>

<span data-ttu-id="934cc-159">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="934cc-159">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-160">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="934cc-160">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-161">75</span><span class="sxs-lookup"><span data-stu-id="934cc-161">75</span></span>

<span data-ttu-id="934cc-162">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="934cc-162">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-163">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="934cc-163">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-164">76</span><span class="sxs-lookup"><span data-stu-id="934cc-164">76</span></span>

<span data-ttu-id="934cc-165">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="934cc-165">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-166">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="934cc-166">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-167">77</span><span class="sxs-lookup"><span data-stu-id="934cc-167">77</span></span>

<span data-ttu-id="934cc-168">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="934cc-168">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-169">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="934cc-169">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-170">78</span><span class="sxs-lookup"><span data-stu-id="934cc-170">78</span></span>

<span data-ttu-id="934cc-171">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="934cc-171">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-172">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="934cc-172">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-173">79</span><span class="sxs-lookup"><span data-stu-id="934cc-173">79</span></span>

<span data-ttu-id="934cc-174">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="934cc-174">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-175">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="934cc-175">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-176">80</span><span class="sxs-lookup"><span data-stu-id="934cc-176">80</span></span>

<span data-ttu-id="934cc-177">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="934cc-177">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-178">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="934cc-178">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-179">81</span><span class="sxs-lookup"><span data-stu-id="934cc-179">81</span></span>

<span data-ttu-id="934cc-180">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="934cc-180">Unable to configure DHCP service.</span></span> <span data-ttu-id="934cc-181">Дополнительные сведения см. в разделе "Замечания".</span><span class="sxs-lookup"><span data-stu-id="934cc-181">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-182">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="934cc-182">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-183">82</span><span class="sxs-lookup"><span data-stu-id="934cc-183">82</span></span>

<span data-ttu-id="934cc-184">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="934cc-184">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-185">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="934cc-185">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-186">83</span><span class="sxs-lookup"><span data-stu-id="934cc-186">83</span></span>

<span data-ttu-id="934cc-187">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="934cc-187">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-188">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="934cc-188">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-189">84</span><span class="sxs-lookup"><span data-stu-id="934cc-189">84</span></span>

<span data-ttu-id="934cc-190">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="934cc-190">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-191">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="934cc-191">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-192">85</span><span class="sxs-lookup"><span data-stu-id="934cc-192">85</span></span>

<span data-ttu-id="934cc-193">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="934cc-193">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-194">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="934cc-194">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-195">86</span><span class="sxs-lookup"><span data-stu-id="934cc-195">86</span></span>

<span data-ttu-id="934cc-196">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="934cc-196">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-197">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="934cc-197">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-198">87</span><span class="sxs-lookup"><span data-stu-id="934cc-198">87</span></span>

<span data-ttu-id="934cc-199">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="934cc-199">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-200">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="934cc-200">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-201">88</span><span class="sxs-lookup"><span data-stu-id="934cc-201">88</span></span>

<span data-ttu-id="934cc-202">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="934cc-202">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-203">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="934cc-203">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-204">89</span><span class="sxs-lookup"><span data-stu-id="934cc-204">89</span></span>

<span data-ttu-id="934cc-205">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="934cc-205">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-206">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="934cc-206">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-207">90</span><span class="sxs-lookup"><span data-stu-id="934cc-207">90</span></span>

<span data-ttu-id="934cc-208">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="934cc-208">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-209">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="934cc-209">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-210">91</span><span class="sxs-lookup"><span data-stu-id="934cc-210">91</span></span>

<span data-ttu-id="934cc-211">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="934cc-211">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-212">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="934cc-212">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-213">92</span><span class="sxs-lookup"><span data-stu-id="934cc-213">92</span></span>

<span data-ttu-id="934cc-214">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="934cc-214">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-215">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="934cc-215">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-216">93</span><span class="sxs-lookup"><span data-stu-id="934cc-216">93</span></span>

<span data-ttu-id="934cc-217">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="934cc-217">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-218">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="934cc-218">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-219">94</span><span class="sxs-lookup"><span data-stu-id="934cc-219">94</span></span>

<span data-ttu-id="934cc-220">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="934cc-220">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-221">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="934cc-221">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-222">95</span><span class="sxs-lookup"><span data-stu-id="934cc-222">95</span></span>

<span data-ttu-id="934cc-223">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="934cc-223">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-224">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="934cc-224">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-225">96</span><span class="sxs-lookup"><span data-stu-id="934cc-225">96</span></span>

<span data-ttu-id="934cc-226">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="934cc-226">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-227">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="934cc-227">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-228">97</span><span class="sxs-lookup"><span data-stu-id="934cc-228">97</span></span>

<span data-ttu-id="934cc-229">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="934cc-229">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-230">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="934cc-230">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-231">98</span><span class="sxs-lookup"><span data-stu-id="934cc-231">98</span></span>

<span data-ttu-id="934cc-232">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="934cc-232">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-233">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="934cc-233">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-234">100</span><span class="sxs-lookup"><span data-stu-id="934cc-234">100</span></span>

<span data-ttu-id="934cc-235">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="934cc-235">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="934cc-236">**2147786788**</span><span class="sxs-lookup"><span data-stu-id="934cc-236">**2147786788**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-237">Блокировка записи не включена.</span><span class="sxs-lookup"><span data-stu-id="934cc-237">Write lock not enabled.</span></span> <span data-ttu-id="934cc-238">Дополнительные сведения см. в разделе [**инеткфглокк:: аккуиреврителокк**](/previous-versions/windows/hardware/network/ff547914(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="934cc-238">For more information, see [**INetCfgLock::AcquireWriteLock**](/previous-versions/windows/hardware/network/ff547914(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="934cc-239">**Другое**</span><span class="sxs-lookup"><span data-stu-id="934cc-239">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="934cc-240">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="934cc-240">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="934cc-241">Комментарии</span><span class="sxs-lookup"><span data-stu-id="934cc-241">Remarks</span></span>

<span data-ttu-id="934cc-242">При использовании **EnableStatic** для изменения IP-адреса удаленного компьютера при подключении через этот адаптер, скорее всего, будет недоступно подключение к удаленному компьютеру и получено сообщение об ОШИБКе RPC No Available.</span><span class="sxs-lookup"><span data-stu-id="934cc-242">When using **EnableStatic** to change the IP address of the remote computer, while being connected through that adapter, you will likely loose connection to the remote computer, and receive an RPC not available error-message.</span></span> <span data-ttu-id="934cc-243">(Однако параметры изменены).</span><span class="sxs-lookup"><span data-stu-id="934cc-243">(the settings are changed however).</span></span> <span data-ttu-id="934cc-244">Чтобы избежать такой ситуации, рассмотрите возможность изменения шлюза и/или параметров DNS перед установкой IP-адреса адаптера.</span><span class="sxs-lookup"><span data-stu-id="934cc-244">To avoid this scenario, consider changing the Gateway and/or DNS-settings prior to setting the adapter's IP-address.</span></span>

<span data-ttu-id="934cc-245">При использовании **EnableStatic** для предоставления адаптеру СТАТИЧЕСКОЙ IP-конфигурации функция возвращает значение "81-не удается настроить службу DHCP", если адаптер уже настроен со статическим адресом.</span><span class="sxs-lookup"><span data-stu-id="934cc-245">When using **EnableStatic** to give an adapter a static IP configuration, the function returns an "81 - Unable to configure DHCP service" if the adapter is already configured with a static address.</span></span> <span data-ttu-id="934cc-246">Однако функция по-прежнему будет выполнена в параметре с новой операцией.</span><span class="sxs-lookup"><span data-stu-id="934cc-246">However, the function still succeeds in setting with the new operation.</span></span>

## <a name="examples"></a><span data-ttu-id="934cc-247">Примеры</span><span class="sxs-lookup"><span data-stu-id="934cc-247">Examples</span></span>

<span data-ttu-id="934cc-248">[Статический IP-адрес, а затем присоединение к](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) образцу кода PowerShell для домена в коллекции TechNet использует **EnableStatic** для добавления статического IP-адреса на локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="934cc-248">The [Static IP and then join to a domain](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) PowerShell code sample, on TechNet Gallery, uses **EnableStatic** to add a static IP to a local machine.</span></span>

<span data-ttu-id="934cc-249">Пример кода VBScript " [Назначение статического IP-адреса](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) " в коллекции TechNet использует **EnableStatic** для установки IP-адреса компьютера.</span><span class="sxs-lookup"><span data-stu-id="934cc-249">The [Assign a Static IP Address](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) VBScript code example, on TechNet Gallery, uses **EnableStatic** to set the IP address of a computer.</span></span>

<span data-ttu-id="934cc-250">В следующем примере VBScript показано, как отключить использование DHCP на экземпляре [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="934cc-250">The following VBScript sample demonstrates how to disable DHCP use on an instance of [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md).</span></span> <span data-ttu-id="934cc-251">В этом случае мы указываем адаптер с индексом 0.</span><span class="sxs-lookup"><span data-stu-id="934cc-251">In this case we specify the adapter with an Index of 0.</span></span> <span data-ttu-id="934cc-252">Правильный индекс должен быть выбран из экземпляров Win32 \_ сетевого адаптера для других интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="934cc-252">The correct index should be selected from Win32\_NetworkAdapter instances for other interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="934cc-253">Этот сценарий применяется только к системам на основе NT. Измените переменные reduce и Subnet ниже на значения, которые вы хотите применить к адаптеру.</span><span class="sxs-lookup"><span data-stu-id="934cc-253">This script only applies to NT-based systems Change the ipaddr and subnet variables below to the values you wish to apply to the adapter.</span></span>

 


```VB
Set Adapter = GetObject("winmgmts:Win32_NetworkAdapterConfiguration=1")

ipaddr = Array("1.1.1.1")
subnet = Array("255.255.255.0")


RetVal = Adapter.EnableStatic(ipaddr,subnet)

if RetVal = 0 then 
 WScript.Echo "DHCP disabled, using static IP address"
else 
 WScript.Echo "DHCP disable failed"
end if
```



<span data-ttu-id="934cc-254">В следующем образце Perl показано, как отключить использование DHCP на экземпляре [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="934cc-254">The following Perl sample demonstrates how to disable DHCP use on an instance of [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md).</span></span> <span data-ttu-id="934cc-255">В этом случае мы указываем адаптер с индексом 0.</span><span class="sxs-lookup"><span data-stu-id="934cc-255">In this case we specify the adapter with an Index of 0.</span></span> <span data-ttu-id="934cc-256">Правильный индекс должен быть выбран из экземпляров Win32 \_ сетевого адаптера для других интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="934cc-256">The correct index should be selected from Win32\_NetworkAdapter instances for other interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="934cc-257">Этот сценарий применяется только к системам на основе NT. Измените переменные reduce и Subnet ниже на значения, которые вы хотите применить к адаптеру.</span><span class="sxs-lookup"><span data-stu-id="934cc-257">This script only applies to NT-based systems Change the ipaddr and subnet variables below to the values you wish to apply to the adapter.</span></span>

 


```
use strict;
use Win32::OLE;

my ($Adapter, @ipaddr, @subnet, $RetVal);  
eval { $Adapter = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2:Win32_NetworkAdapterConfiguration.Index=\"0\""); };

unless ($@) 
{
 push @ipaddr, "192.168.144.107";
 push @subnet, "255.255.255.0";

 $RetVal = $Adapter->EnableStatic(\@ipaddr, \@subnet);

 if ($RetVal == 0) 
 {
  print "\nDHCP disabled, using static IP address\n";
 }
 else 
 {
  print "\nDHCP disable failed\n";
 }
}
else
{
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="934cc-258">Требования</span><span class="sxs-lookup"><span data-stu-id="934cc-258">Requirements</span></span>



| <span data-ttu-id="934cc-259">Требование</span><span class="sxs-lookup"><span data-stu-id="934cc-259">Requirement</span></span> | <span data-ttu-id="934cc-260">Значение</span><span class="sxs-lookup"><span data-stu-id="934cc-260">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="934cc-261">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="934cc-261">Minimum supported client</span></span><br/> | <span data-ttu-id="934cc-262">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="934cc-262">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="934cc-263">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="934cc-263">Minimum supported server</span></span><br/> | <span data-ttu-id="934cc-264">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="934cc-264">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="934cc-265">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="934cc-265">Namespace</span></span><br/>                | <span data-ttu-id="934cc-266">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="934cc-266">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="934cc-267">MOF</span><span class="sxs-lookup"><span data-stu-id="934cc-267">MOF</span></span><br/>                      | <dl> <span data-ttu-id="934cc-268"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="934cc-268"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="934cc-269">DLL</span><span class="sxs-lookup"><span data-stu-id="934cc-269">DLL</span></span><br/>                      | <dl> <span data-ttu-id="934cc-270"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="934cc-270"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="934cc-271">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="934cc-271">See also</span></span>

<dl> <dt>

[<span data-ttu-id="934cc-272">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="934cc-272">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="934cc-273">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="934cc-273">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="934cc-274">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="934cc-274">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="934cc-275">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="934cc-275">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="934cc-276">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="934cc-276">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

