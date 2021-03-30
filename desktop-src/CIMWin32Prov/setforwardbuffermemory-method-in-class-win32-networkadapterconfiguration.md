---
description: Статический метод класса Сетфорвардбуффермемори WMI используется для указания того, какой объем памяти выделяется IP-адресом для хранения данных пакета в очереди пакетов маршрутизатора.
ms.assetid: e76452e8-2ee8-4d39-9405-33b0aeeac74d
ms.tgt_platform: multiple
title: Метод Сетфорвардбуффермемори класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetForwardBufferMemory
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 30179610e6eee121a86119fa347067b40ef04c2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896086"
---
# <a name="setforwardbuffermemory-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="2ab13-103">Метод Сетфорвардбуффермемори \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ab13-103">SetForwardBufferMemory method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="2ab13-104">Статический метод класса **сетфорвардбуффермемори** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) используется для указания того, какой объем памяти выделяется IP-адресом для хранения данных пакета в очереди пакетов маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="2ab13-104">The **SetForwardBufferMemory** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to specify how much memory IP allocates to store packet data in the router packet queue.</span></span>

<span data-ttu-id="2ab13-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="2ab13-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2ab13-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2ab13-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2ab13-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2ab13-107">Syntax</span></span>


```mof
uint32 SetForwardBufferMemory(
  [in] uint32 ForwardBufferMemory
);
```



## <a name="parameters"></a><span data-ttu-id="2ab13-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2ab13-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ab13-109">*ForwardBufferMemory* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2ab13-109">*ForwardBufferMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-110">Размер в байтах очереди пакетов маршрутизатора, используемой для хранения данных пакета.</span><span class="sxs-lookup"><span data-stu-id="2ab13-110">Size, in bytes, of the router packet queue used to store packet data.</span></span> <span data-ttu-id="2ab13-111">Значение по умолчанию — 74240 (50 1480-байтовых пакетов, округленное до кратного 256).</span><span class="sxs-lookup"><span data-stu-id="2ab13-111">The default value is 74240 (fifty 1480-byte packets, rounded to a multiple of 256).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ab13-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2ab13-112">Return value</span></span>

<span data-ttu-id="2ab13-113">Возвращает значение 0 (ноль) для успешного завершения, если не требуется перезагрузка, 1 (один) для успешного завершения, когда требуется перезагрузка, и другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="2ab13-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="2ab13-114">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="2ab13-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="2ab13-115">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="2ab13-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="2ab13-116">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="2ab13-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-117">0</span><span class="sxs-lookup"><span data-stu-id="2ab13-117">0</span></span>

<span data-ttu-id="2ab13-118">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="2ab13-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-119">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="2ab13-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-120">1</span><span class="sxs-lookup"><span data-stu-id="2ab13-120">1</span></span>

<span data-ttu-id="2ab13-121">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="2ab13-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-122">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="2ab13-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-123">64</span><span class="sxs-lookup"><span data-stu-id="2ab13-123">64</span></span>

<span data-ttu-id="2ab13-124">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="2ab13-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-125">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="2ab13-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-126">65</span><span class="sxs-lookup"><span data-stu-id="2ab13-126">65</span></span>

<span data-ttu-id="2ab13-127">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="2ab13-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-128">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="2ab13-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-129">66</span><span class="sxs-lookup"><span data-stu-id="2ab13-129">66</span></span>

<span data-ttu-id="2ab13-130">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="2ab13-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-131">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="2ab13-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-132">67</span><span class="sxs-lookup"><span data-stu-id="2ab13-132">67</span></span>

<span data-ttu-id="2ab13-133">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="2ab13-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-134">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="2ab13-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-135">68</span><span class="sxs-lookup"><span data-stu-id="2ab13-135">68</span></span>

<span data-ttu-id="2ab13-136">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="2ab13-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-137">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="2ab13-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-138">69</span><span class="sxs-lookup"><span data-stu-id="2ab13-138">69</span></span>

<span data-ttu-id="2ab13-139">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="2ab13-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-140">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="2ab13-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-141">70</span><span class="sxs-lookup"><span data-stu-id="2ab13-141">70</span></span>

<span data-ttu-id="2ab13-142">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="2ab13-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-143">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="2ab13-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-144">71</span><span class="sxs-lookup"><span data-stu-id="2ab13-144">71</span></span>

<span data-ttu-id="2ab13-145">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="2ab13-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-146">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="2ab13-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-147">72</span><span class="sxs-lookup"><span data-stu-id="2ab13-147">72</span></span>

<span data-ttu-id="2ab13-148">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="2ab13-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-149">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="2ab13-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-150">73</span><span class="sxs-lookup"><span data-stu-id="2ab13-150">73</span></span>

<span data-ttu-id="2ab13-151">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="2ab13-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-152">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="2ab13-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-153">74</span><span class="sxs-lookup"><span data-stu-id="2ab13-153">74</span></span>

<span data-ttu-id="2ab13-154">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="2ab13-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-155">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="2ab13-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-156">75</span><span class="sxs-lookup"><span data-stu-id="2ab13-156">75</span></span>

<span data-ttu-id="2ab13-157">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="2ab13-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-158">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="2ab13-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-159">76</span><span class="sxs-lookup"><span data-stu-id="2ab13-159">76</span></span>

<span data-ttu-id="2ab13-160">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="2ab13-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-161">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="2ab13-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-162">77</span><span class="sxs-lookup"><span data-stu-id="2ab13-162">77</span></span>

<span data-ttu-id="2ab13-163">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="2ab13-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-164">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="2ab13-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-165">78</span><span class="sxs-lookup"><span data-stu-id="2ab13-165">78</span></span>

<span data-ttu-id="2ab13-166">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="2ab13-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-167">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="2ab13-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-168">79</span><span class="sxs-lookup"><span data-stu-id="2ab13-168">79</span></span>

<span data-ttu-id="2ab13-169">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="2ab13-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-170">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="2ab13-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-171">80</span><span class="sxs-lookup"><span data-stu-id="2ab13-171">80</span></span>

<span data-ttu-id="2ab13-172">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="2ab13-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-173">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="2ab13-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-174">81</span><span class="sxs-lookup"><span data-stu-id="2ab13-174">81</span></span>

<span data-ttu-id="2ab13-175">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="2ab13-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-176">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="2ab13-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-177">82</span><span class="sxs-lookup"><span data-stu-id="2ab13-177">82</span></span>

<span data-ttu-id="2ab13-178">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="2ab13-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-179">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="2ab13-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-180">83</span><span class="sxs-lookup"><span data-stu-id="2ab13-180">83</span></span>

<span data-ttu-id="2ab13-181">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="2ab13-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-182">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="2ab13-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-183">84</span><span class="sxs-lookup"><span data-stu-id="2ab13-183">84</span></span>

<span data-ttu-id="2ab13-184">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="2ab13-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-185">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="2ab13-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-186">85</span><span class="sxs-lookup"><span data-stu-id="2ab13-186">85</span></span>

<span data-ttu-id="2ab13-187">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="2ab13-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-188">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="2ab13-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-189">86</span><span class="sxs-lookup"><span data-stu-id="2ab13-189">86</span></span>

<span data-ttu-id="2ab13-190">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="2ab13-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-191">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="2ab13-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-192">87</span><span class="sxs-lookup"><span data-stu-id="2ab13-192">87</span></span>

<span data-ttu-id="2ab13-193">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="2ab13-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-194">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="2ab13-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-195">88</span><span class="sxs-lookup"><span data-stu-id="2ab13-195">88</span></span>

<span data-ttu-id="2ab13-196">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="2ab13-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-197">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="2ab13-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-198">89</span><span class="sxs-lookup"><span data-stu-id="2ab13-198">89</span></span>

<span data-ttu-id="2ab13-199">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="2ab13-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-200">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="2ab13-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-201">90</span><span class="sxs-lookup"><span data-stu-id="2ab13-201">90</span></span>

<span data-ttu-id="2ab13-202">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="2ab13-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-203">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="2ab13-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-204">91</span><span class="sxs-lookup"><span data-stu-id="2ab13-204">91</span></span>

<span data-ttu-id="2ab13-205">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="2ab13-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-206">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="2ab13-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-207">92</span><span class="sxs-lookup"><span data-stu-id="2ab13-207">92</span></span>

<span data-ttu-id="2ab13-208">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="2ab13-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-209">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="2ab13-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-210">93</span><span class="sxs-lookup"><span data-stu-id="2ab13-210">93</span></span>

<span data-ttu-id="2ab13-211">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="2ab13-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-212">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="2ab13-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-213">94</span><span class="sxs-lookup"><span data-stu-id="2ab13-213">94</span></span>

<span data-ttu-id="2ab13-214">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="2ab13-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-215">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="2ab13-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-216">95</span><span class="sxs-lookup"><span data-stu-id="2ab13-216">95</span></span>

<span data-ttu-id="2ab13-217">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="2ab13-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-218">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="2ab13-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-219">96</span><span class="sxs-lookup"><span data-stu-id="2ab13-219">96</span></span>

<span data-ttu-id="2ab13-220">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="2ab13-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-221">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="2ab13-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-222">97</span><span class="sxs-lookup"><span data-stu-id="2ab13-222">97</span></span>

<span data-ttu-id="2ab13-223">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="2ab13-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-224">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="2ab13-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-225">98</span><span class="sxs-lookup"><span data-stu-id="2ab13-225">98</span></span>

<span data-ttu-id="2ab13-226">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="2ab13-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-227">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="2ab13-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-228">100</span><span class="sxs-lookup"><span data-stu-id="2ab13-228">100</span></span>

<span data-ttu-id="2ab13-229">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="2ab13-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2ab13-230">**Другое**</span><span class="sxs-lookup"><span data-stu-id="2ab13-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="2ab13-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="2ab13-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2ab13-232">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2ab13-232">Remarks</span></span>

<span data-ttu-id="2ab13-233">Когда это пространство буфера заполнено, маршрутизатор начинает удалять пакеты в случайном порядке из очереди.</span><span class="sxs-lookup"><span data-stu-id="2ab13-233">When this buffer space is filled, the router begins discarding packets at random from its queue.</span></span>

<span data-ttu-id="2ab13-234">Буферы данных очереди пакетов имеют длину 256 байт, поэтому значение параметра *ForwardBufferMemory* должно быть кратно 256.</span><span class="sxs-lookup"><span data-stu-id="2ab13-234">Packet queue data buffers are 256 bytes in length, so the value of the *ForwardBufferMemory* parameter should be a multiple of 256.</span></span> <span data-ttu-id="2ab13-235">Несколько буферов объединяются в цепочку для больших пакетов.</span><span class="sxs-lookup"><span data-stu-id="2ab13-235">Multiple buffers are chained together for larger packets.</span></span> <span data-ttu-id="2ab13-236">Заголовок IP-адреса для пакета хранится отдельно.</span><span class="sxs-lookup"><span data-stu-id="2ab13-236">The IP header for a packet is stored separately.</span></span> <span data-ttu-id="2ab13-237">Этот параметр игнорируется, и никакие буферы не выделяются, если IP-маршрутизатор не включен.</span><span class="sxs-lookup"><span data-stu-id="2ab13-237">This parameter is ignored and no buffers are allocated if the IP router is not enabled.</span></span> <span data-ttu-id="2ab13-238">Размер буфера может варьироваться от максимального значения (MTU) сети, которое меньше 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="2ab13-238">The buffer size can range from the network Maximum Transmission Unit (MTU) to a value smaller than 0xFFFFFFFF.</span></span>

## <a name="examples"></a><span data-ttu-id="2ab13-239">Примеры</span><span class="sxs-lookup"><span data-stu-id="2ab13-239">Examples</span></span>

<span data-ttu-id="2ab13-240">Пример [изменения памяти буфера обмена для всех сетевых адаптеров](https://Gallery.TechNet.Microsoft.Com/da5712dc-f854-4099-98a9-59c0ff20a524) на языке VBScript настраивает память прямого буфера для всех сетевых адаптеров компьютера.</span><span class="sxs-lookup"><span data-stu-id="2ab13-240">The [Modify the Forward Buffer Memory for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/da5712dc-f854-4099-98a9-59c0ff20a524) VBScript sample configures the forward buffer memory for all network adapters on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ab13-241">Требования</span><span class="sxs-lookup"><span data-stu-id="2ab13-241">Requirements</span></span>



| <span data-ttu-id="2ab13-242">Требование</span><span class="sxs-lookup"><span data-stu-id="2ab13-242">Requirement</span></span> | <span data-ttu-id="2ab13-243">Значение</span><span class="sxs-lookup"><span data-stu-id="2ab13-243">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ab13-244">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2ab13-244">Minimum supported client</span></span><br/> | <span data-ttu-id="2ab13-245">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2ab13-245">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2ab13-246">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2ab13-246">Minimum supported server</span></span><br/> | <span data-ttu-id="2ab13-247">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ab13-247">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2ab13-248">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2ab13-248">Namespace</span></span><br/>                | <span data-ttu-id="2ab13-249">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2ab13-249">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2ab13-250">MOF</span><span class="sxs-lookup"><span data-stu-id="2ab13-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2ab13-251"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2ab13-251"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2ab13-252">DLL</span><span class="sxs-lookup"><span data-stu-id="2ab13-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ab13-253"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ab13-253"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ab13-254">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2ab13-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ab13-255">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="2ab13-255">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="2ab13-256">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="2ab13-256">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="2ab13-257">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="2ab13-257">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="2ab13-258">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="2ab13-258">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="2ab13-259">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="2ab13-259">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

