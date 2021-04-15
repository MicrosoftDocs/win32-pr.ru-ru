---
description: Статический метод класса ReleaseDHCPLeaseAll WMI освобождает IP-адреса, привязанные ко всем сетевым адаптерам с поддержкой DHCP.
ms.assetid: d9f83953-f3da-419d-8c84-649c39b4945e
ms.tgt_platform: multiple
title: Метод ReleaseDHCPLeaseAll класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.ReleaseDHCPLeaseAll
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3e7b1f7cf2f09fa20f7bf19b15e82f536ca0aa50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655997"
---
# <a name="releasedhcpleaseall-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="d1440-103">Метод ReleaseDHCPLeaseAll \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1440-103">ReleaseDHCPLeaseAll method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="d1440-104">Статический метод класса **ReleaseDHCPLeaseAll** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) освобождает IP-адреса, привязанные ко всем сетевым адаптерам с поддержкой DHCP.</span><span class="sxs-lookup"><span data-stu-id="d1440-104">The **ReleaseDHCPLeaseAll** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method releases the IP addresses bound to all DHCP-enabled network adapters.</span></span>

> [!Note]  
> <span data-ttu-id="d1440-105">Предупреждение. Если на локальном компьютере включен DHCP, параметр приведет к прерыванию всех TCP/IP-подключений.</span><span class="sxs-lookup"><span data-stu-id="d1440-105">Warning If DHCP is enabled on the local computer system, the option will terminate all DHCP TCP/IP connections.</span></span>

 

<span data-ttu-id="d1440-106">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="d1440-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d1440-107">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d1440-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d1440-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1440-108">Syntax</span></span>


```mof
uint32 ReleaseDHCPLeaseAll();
```



## <a name="parameters"></a><span data-ttu-id="d1440-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d1440-109">Parameters</span></span>

<span data-ttu-id="d1440-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="d1440-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d1440-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d1440-111">Return value</span></span>

<span data-ttu-id="d1440-112">Возвращает значение 0 (ноль) для успешного завершения, если не требуется перезагрузка, 1 (один) для успешного завершения, когда требуется перезагрузка, и другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="d1440-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="d1440-113">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="d1440-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="d1440-114">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="d1440-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="d1440-115">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="d1440-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-116">0</span><span class="sxs-lookup"><span data-stu-id="d1440-116">0</span></span>

<span data-ttu-id="d1440-117">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="d1440-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-118">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="d1440-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-119">1</span><span class="sxs-lookup"><span data-stu-id="d1440-119">1</span></span>

<span data-ttu-id="d1440-120">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="d1440-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-121">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="d1440-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-122">64</span><span class="sxs-lookup"><span data-stu-id="d1440-122">64</span></span>

<span data-ttu-id="d1440-123">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="d1440-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-124">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="d1440-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-125">65</span><span class="sxs-lookup"><span data-stu-id="d1440-125">65</span></span>

<span data-ttu-id="d1440-126">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="d1440-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-127">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="d1440-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-128">66</span><span class="sxs-lookup"><span data-stu-id="d1440-128">66</span></span>

<span data-ttu-id="d1440-129">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="d1440-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-130">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="d1440-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-131">67</span><span class="sxs-lookup"><span data-stu-id="d1440-131">67</span></span>

<span data-ttu-id="d1440-132">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d1440-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-133">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="d1440-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-134">68</span><span class="sxs-lookup"><span data-stu-id="d1440-134">68</span></span>

<span data-ttu-id="d1440-135">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="d1440-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-136">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="d1440-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-137">69</span><span class="sxs-lookup"><span data-stu-id="d1440-137">69</span></span>

<span data-ttu-id="d1440-138">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="d1440-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-139">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="d1440-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-140">70</span><span class="sxs-lookup"><span data-stu-id="d1440-140">70</span></span>

<span data-ttu-id="d1440-141">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="d1440-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-142">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="d1440-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-143">71</span><span class="sxs-lookup"><span data-stu-id="d1440-143">71</span></span>

<span data-ttu-id="d1440-144">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="d1440-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-145">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="d1440-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-146">72</span><span class="sxs-lookup"><span data-stu-id="d1440-146">72</span></span>

<span data-ttu-id="d1440-147">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="d1440-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-148">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="d1440-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-149">73</span><span class="sxs-lookup"><span data-stu-id="d1440-149">73</span></span>

<span data-ttu-id="d1440-150">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="d1440-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-151">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="d1440-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-152">74</span><span class="sxs-lookup"><span data-stu-id="d1440-152">74</span></span>

<span data-ttu-id="d1440-153">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="d1440-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-154">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="d1440-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-155">75</span><span class="sxs-lookup"><span data-stu-id="d1440-155">75</span></span>

<span data-ttu-id="d1440-156">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="d1440-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-157">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="d1440-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-158">76</span><span class="sxs-lookup"><span data-stu-id="d1440-158">76</span></span>

<span data-ttu-id="d1440-159">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="d1440-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-160">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="d1440-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-161">77</span><span class="sxs-lookup"><span data-stu-id="d1440-161">77</span></span>

<span data-ttu-id="d1440-162">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="d1440-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-163">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="d1440-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-164">78</span><span class="sxs-lookup"><span data-stu-id="d1440-164">78</span></span>

<span data-ttu-id="d1440-165">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="d1440-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-166">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="d1440-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-167">79</span><span class="sxs-lookup"><span data-stu-id="d1440-167">79</span></span>

<span data-ttu-id="d1440-168">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="d1440-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-169">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="d1440-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-170">80</span><span class="sxs-lookup"><span data-stu-id="d1440-170">80</span></span>

<span data-ttu-id="d1440-171">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="d1440-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-172">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="d1440-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-173">81</span><span class="sxs-lookup"><span data-stu-id="d1440-173">81</span></span>

<span data-ttu-id="d1440-174">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="d1440-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-175">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="d1440-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-176">82</span><span class="sxs-lookup"><span data-stu-id="d1440-176">82</span></span>

<span data-ttu-id="d1440-177">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="d1440-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-178">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="d1440-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-179">83</span><span class="sxs-lookup"><span data-stu-id="d1440-179">83</span></span>

<span data-ttu-id="d1440-180">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="d1440-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-181">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="d1440-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-182">84</span><span class="sxs-lookup"><span data-stu-id="d1440-182">84</span></span>

<span data-ttu-id="d1440-183">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="d1440-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-184">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="d1440-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-185">85</span><span class="sxs-lookup"><span data-stu-id="d1440-185">85</span></span>

<span data-ttu-id="d1440-186">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="d1440-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-187">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="d1440-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-188">86</span><span class="sxs-lookup"><span data-stu-id="d1440-188">86</span></span>

<span data-ttu-id="d1440-189">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="d1440-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-190">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="d1440-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-191">87</span><span class="sxs-lookup"><span data-stu-id="d1440-191">87</span></span>

<span data-ttu-id="d1440-192">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="d1440-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-193">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="d1440-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-194">88</span><span class="sxs-lookup"><span data-stu-id="d1440-194">88</span></span>

<span data-ttu-id="d1440-195">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="d1440-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-196">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="d1440-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-197">89</span><span class="sxs-lookup"><span data-stu-id="d1440-197">89</span></span>

<span data-ttu-id="d1440-198">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="d1440-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-199">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="d1440-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-200">90</span><span class="sxs-lookup"><span data-stu-id="d1440-200">90</span></span>

<span data-ttu-id="d1440-201">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="d1440-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-202">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="d1440-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-203">91</span><span class="sxs-lookup"><span data-stu-id="d1440-203">91</span></span>

<span data-ttu-id="d1440-204">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="d1440-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-205">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="d1440-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-206">92</span><span class="sxs-lookup"><span data-stu-id="d1440-206">92</span></span>

<span data-ttu-id="d1440-207">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="d1440-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-208">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="d1440-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-209">93</span><span class="sxs-lookup"><span data-stu-id="d1440-209">93</span></span>

<span data-ttu-id="d1440-210">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="d1440-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-211">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="d1440-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-212">94</span><span class="sxs-lookup"><span data-stu-id="d1440-212">94</span></span>

<span data-ttu-id="d1440-213">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="d1440-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-214">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="d1440-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-215">95</span><span class="sxs-lookup"><span data-stu-id="d1440-215">95</span></span>

<span data-ttu-id="d1440-216">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="d1440-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-217">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="d1440-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-218">96</span><span class="sxs-lookup"><span data-stu-id="d1440-218">96</span></span>

<span data-ttu-id="d1440-219">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="d1440-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-220">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="d1440-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-221">97</span><span class="sxs-lookup"><span data-stu-id="d1440-221">97</span></span>

<span data-ttu-id="d1440-222">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="d1440-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-223">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="d1440-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-224">98</span><span class="sxs-lookup"><span data-stu-id="d1440-224">98</span></span>

<span data-ttu-id="d1440-225">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="d1440-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-226">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="d1440-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-227">100</span><span class="sxs-lookup"><span data-stu-id="d1440-227">100</span></span>

<span data-ttu-id="d1440-228">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="d1440-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d1440-229">**Другое**</span><span class="sxs-lookup"><span data-stu-id="d1440-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="d1440-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="d1440-230">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="d1440-231">Примеры</span><span class="sxs-lookup"><span data-stu-id="d1440-231">Examples</span></span>

<span data-ttu-id="d1440-232">Следующий пример кода VBScript освобождает все аренды DHCP, используемые в настоящее время на компьютере.</span><span class="sxs-lookup"><span data-stu-id="d1440-232">The following VBScript code sample releases all the DHCP leases currently in use on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objNetworkSettings = objWMIService.Get("Win32_NetworkAdapterConfiguration") 
objNetworkSettings.ReleaseDHCPLeaseAll() 
```



## <a name="requirements"></a><span data-ttu-id="d1440-233">Требования</span><span class="sxs-lookup"><span data-stu-id="d1440-233">Requirements</span></span>



| <span data-ttu-id="d1440-234">Требование</span><span class="sxs-lookup"><span data-stu-id="d1440-234">Requirement</span></span> | <span data-ttu-id="d1440-235">Значение</span><span class="sxs-lookup"><span data-stu-id="d1440-235">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1440-236">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1440-236">Minimum supported client</span></span><br/> | <span data-ttu-id="d1440-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1440-237">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d1440-238">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1440-238">Minimum supported server</span></span><br/> | <span data-ttu-id="d1440-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1440-239">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d1440-240">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d1440-240">Namespace</span></span><br/>                | <span data-ttu-id="d1440-241">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d1440-241">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d1440-242">MOF</span><span class="sxs-lookup"><span data-stu-id="d1440-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1440-243"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1440-243"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1440-244">DLL</span><span class="sxs-lookup"><span data-stu-id="d1440-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1440-245"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1440-245"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1440-246">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d1440-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1440-247">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="d1440-247">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="d1440-248">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="d1440-248">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="d1440-249">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="d1440-249">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="d1440-250">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="d1440-250">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="d1440-251">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="d1440-251">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

