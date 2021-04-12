---
description: Статический метод класса Сетткпнумконнектионс WMI используется для установки максимального числа подключений, которые TCP может открыть одновременно.
ms.assetid: 50458161-1f28-47f9-b395-09586e859d5d
ms.tgt_platform: multiple
title: Метод Сетткпнумконнектионс класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpNumConnections
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5708c7ce80930c0924b560cc7b84e5af45ad7962
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141563"
---
# <a name="settcpnumconnections-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="3dde1-103">Метод Сетткпнумконнектионс \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="3dde1-103">SetTcpNumConnections method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="3dde1-104">Статический метод класса **сетткпнумконнектионс** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) используется для установки максимального числа подключений, которые TCP может открыть одновременно.</span><span class="sxs-lookup"><span data-stu-id="3dde1-104">The **SetTcpNumConnections** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the maximum number of connections that TCP may have open simultaneously.</span></span>

<span data-ttu-id="3dde1-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="3dde1-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3dde1-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3dde1-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3dde1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3dde1-107">Syntax</span></span>


```mof
uint32 SetTcpNumConnections(
  [in] uint32 TcpNumConnections
);
```



## <a name="parameters"></a><span data-ttu-id="3dde1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3dde1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dde1-109">*Ткпнумконнектионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3dde1-109">*TcpNumConnections* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-110">Максимальное число подключений, которые TCP может открыть одновременно.</span><span class="sxs-lookup"><span data-stu-id="3dde1-110">Maximum number of connections that TCP may have open simultaneously.</span></span> <span data-ttu-id="3dde1-111">Допустимый диапазон значений — 0-0xFFFFFE.</span><span class="sxs-lookup"><span data-stu-id="3dde1-111">The valid range of values is 0 - 0xFFFFFE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dde1-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3dde1-112">Return value</span></span>

<span data-ttu-id="3dde1-113">Возвращает значение 0 (ноль) для успешного завершения, если не требуется перезагрузка, 1 (один) для успешного завершения, когда требуется перезагрузка, и другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="3dde1-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="3dde1-114">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="3dde1-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="3dde1-115">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="3dde1-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="3dde1-116">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="3dde1-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-117">0</span><span class="sxs-lookup"><span data-stu-id="3dde1-117">0</span></span>

<span data-ttu-id="3dde1-118">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="3dde1-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-119">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="3dde1-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-120">1</span><span class="sxs-lookup"><span data-stu-id="3dde1-120">1</span></span>

<span data-ttu-id="3dde1-121">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="3dde1-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-122">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="3dde1-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-123">64</span><span class="sxs-lookup"><span data-stu-id="3dde1-123">64</span></span>

<span data-ttu-id="3dde1-124">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="3dde1-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-125">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="3dde1-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-126">65</span><span class="sxs-lookup"><span data-stu-id="3dde1-126">65</span></span>

<span data-ttu-id="3dde1-127">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="3dde1-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-128">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="3dde1-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-129">66</span><span class="sxs-lookup"><span data-stu-id="3dde1-129">66</span></span>

<span data-ttu-id="3dde1-130">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="3dde1-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-131">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="3dde1-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-132">67</span><span class="sxs-lookup"><span data-stu-id="3dde1-132">67</span></span>

<span data-ttu-id="3dde1-133">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="3dde1-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-134">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="3dde1-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-135">68</span><span class="sxs-lookup"><span data-stu-id="3dde1-135">68</span></span>

<span data-ttu-id="3dde1-136">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="3dde1-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-137">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="3dde1-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-138">69</span><span class="sxs-lookup"><span data-stu-id="3dde1-138">69</span></span>

<span data-ttu-id="3dde1-139">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="3dde1-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-140">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="3dde1-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-141">70</span><span class="sxs-lookup"><span data-stu-id="3dde1-141">70</span></span>

<span data-ttu-id="3dde1-142">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="3dde1-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-143">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="3dde1-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-144">71</span><span class="sxs-lookup"><span data-stu-id="3dde1-144">71</span></span>

<span data-ttu-id="3dde1-145">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="3dde1-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-146">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="3dde1-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-147">72</span><span class="sxs-lookup"><span data-stu-id="3dde1-147">72</span></span>

<span data-ttu-id="3dde1-148">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="3dde1-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-149">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="3dde1-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-150">73</span><span class="sxs-lookup"><span data-stu-id="3dde1-150">73</span></span>

<span data-ttu-id="3dde1-151">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="3dde1-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-152">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="3dde1-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-153">74</span><span class="sxs-lookup"><span data-stu-id="3dde1-153">74</span></span>

<span data-ttu-id="3dde1-154">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="3dde1-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-155">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="3dde1-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-156">75</span><span class="sxs-lookup"><span data-stu-id="3dde1-156">75</span></span>

<span data-ttu-id="3dde1-157">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="3dde1-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-158">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="3dde1-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-159">76</span><span class="sxs-lookup"><span data-stu-id="3dde1-159">76</span></span>

<span data-ttu-id="3dde1-160">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="3dde1-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-161">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="3dde1-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-162">77</span><span class="sxs-lookup"><span data-stu-id="3dde1-162">77</span></span>

<span data-ttu-id="3dde1-163">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="3dde1-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-164">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="3dde1-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-165">78</span><span class="sxs-lookup"><span data-stu-id="3dde1-165">78</span></span>

<span data-ttu-id="3dde1-166">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="3dde1-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-167">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="3dde1-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-168">79</span><span class="sxs-lookup"><span data-stu-id="3dde1-168">79</span></span>

<span data-ttu-id="3dde1-169">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="3dde1-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-170">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="3dde1-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-171">80</span><span class="sxs-lookup"><span data-stu-id="3dde1-171">80</span></span>

<span data-ttu-id="3dde1-172">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="3dde1-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-173">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="3dde1-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-174">81</span><span class="sxs-lookup"><span data-stu-id="3dde1-174">81</span></span>

<span data-ttu-id="3dde1-175">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="3dde1-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-176">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="3dde1-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-177">82</span><span class="sxs-lookup"><span data-stu-id="3dde1-177">82</span></span>

<span data-ttu-id="3dde1-178">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="3dde1-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-179">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="3dde1-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-180">83</span><span class="sxs-lookup"><span data-stu-id="3dde1-180">83</span></span>

<span data-ttu-id="3dde1-181">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="3dde1-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-182">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="3dde1-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-183">84</span><span class="sxs-lookup"><span data-stu-id="3dde1-183">84</span></span>

<span data-ttu-id="3dde1-184">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="3dde1-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-185">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="3dde1-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-186">85</span><span class="sxs-lookup"><span data-stu-id="3dde1-186">85</span></span>

<span data-ttu-id="3dde1-187">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="3dde1-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-188">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="3dde1-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-189">86</span><span class="sxs-lookup"><span data-stu-id="3dde1-189">86</span></span>

<span data-ttu-id="3dde1-190">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="3dde1-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-191">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="3dde1-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-192">87</span><span class="sxs-lookup"><span data-stu-id="3dde1-192">87</span></span>

<span data-ttu-id="3dde1-193">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="3dde1-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-194">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="3dde1-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-195">88</span><span class="sxs-lookup"><span data-stu-id="3dde1-195">88</span></span>

<span data-ttu-id="3dde1-196">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="3dde1-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-197">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="3dde1-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-198">89</span><span class="sxs-lookup"><span data-stu-id="3dde1-198">89</span></span>

<span data-ttu-id="3dde1-199">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="3dde1-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-200">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="3dde1-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-201">90</span><span class="sxs-lookup"><span data-stu-id="3dde1-201">90</span></span>

<span data-ttu-id="3dde1-202">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="3dde1-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-203">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="3dde1-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-204">91</span><span class="sxs-lookup"><span data-stu-id="3dde1-204">91</span></span>

<span data-ttu-id="3dde1-205">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="3dde1-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-206">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="3dde1-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-207">92</span><span class="sxs-lookup"><span data-stu-id="3dde1-207">92</span></span>

<span data-ttu-id="3dde1-208">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="3dde1-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-209">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="3dde1-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-210">93</span><span class="sxs-lookup"><span data-stu-id="3dde1-210">93</span></span>

<span data-ttu-id="3dde1-211">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="3dde1-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-212">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="3dde1-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-213">94</span><span class="sxs-lookup"><span data-stu-id="3dde1-213">94</span></span>

<span data-ttu-id="3dde1-214">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="3dde1-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-215">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="3dde1-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-216">95</span><span class="sxs-lookup"><span data-stu-id="3dde1-216">95</span></span>

<span data-ttu-id="3dde1-217">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="3dde1-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-218">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="3dde1-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-219">96</span><span class="sxs-lookup"><span data-stu-id="3dde1-219">96</span></span>

<span data-ttu-id="3dde1-220">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="3dde1-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-221">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="3dde1-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-222">97</span><span class="sxs-lookup"><span data-stu-id="3dde1-222">97</span></span>

<span data-ttu-id="3dde1-223">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="3dde1-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-224">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="3dde1-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-225">98</span><span class="sxs-lookup"><span data-stu-id="3dde1-225">98</span></span>

<span data-ttu-id="3dde1-226">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="3dde1-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-227">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="3dde1-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-228">100</span><span class="sxs-lookup"><span data-stu-id="3dde1-228">100</span></span>

<span data-ttu-id="3dde1-229">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="3dde1-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="3dde1-230">**Другое**</span><span class="sxs-lookup"><span data-stu-id="3dde1-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="3dde1-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="3dde1-231">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="3dde1-232">Примеры</span><span class="sxs-lookup"><span data-stu-id="3dde1-232">Examples</span></span>

<span data-ttu-id="3dde1-233">Пример [изменения разрешенного числа TCP-подключений](https://Gallery.TechNet.Microsoft.Com/016d09f3-28aa-47eb-b439-100b89999bab) на языке VBScript задает максимально допустимое количество одновременно открытых TCP-подключений на компьютере до 10.</span><span class="sxs-lookup"><span data-stu-id="3dde1-233">The [Modify the Allowed Number of TCP Connections](https://Gallery.TechNet.Microsoft.Com/016d09f3-28aa-47eb-b439-100b89999bab) VBScript sample sets the maximum allowed number of simultaneously-opened TCP connections on a computer to 10.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dde1-234">Требования</span><span class="sxs-lookup"><span data-stu-id="3dde1-234">Requirements</span></span>



| <span data-ttu-id="3dde1-235">Требование</span><span class="sxs-lookup"><span data-stu-id="3dde1-235">Requirement</span></span> | <span data-ttu-id="3dde1-236">Значение</span><span class="sxs-lookup"><span data-stu-id="3dde1-236">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3dde1-237">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3dde1-237">Minimum supported client</span></span><br/> | <span data-ttu-id="3dde1-238">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3dde1-238">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3dde1-239">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3dde1-239">Minimum supported server</span></span><br/> | <span data-ttu-id="3dde1-240">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3dde1-240">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3dde1-241">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3dde1-241">Namespace</span></span><br/>                | <span data-ttu-id="3dde1-242">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3dde1-242">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3dde1-243">MOF</span><span class="sxs-lookup"><span data-stu-id="3dde1-243">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3dde1-244"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3dde1-244"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3dde1-245">DLL</span><span class="sxs-lookup"><span data-stu-id="3dde1-245">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3dde1-246"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3dde1-246"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dde1-247">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3dde1-247">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dde1-248">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="3dde1-248">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="3dde1-249">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="3dde1-249">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="3dde1-250">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="3dde1-250">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="3dde1-251">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="3dde1-251">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="3dde1-252">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="3dde1-252">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

