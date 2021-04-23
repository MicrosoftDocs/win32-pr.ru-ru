---
description: Статический метод класса RenewDHCPLeaseAll WMI обновляет IP-адреса на всех сетевых адаптерах с поддержкой DHCP.
ms.assetid: cbe0a607-cb3b-47c4-ad3a-c4fa03fe688c
ms.tgt_platform: multiple
title: Метод RenewDHCPLeaseAll класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.RenewDHCPLeaseAll
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a3ed94b44a629f619617186415ed3822387c6967
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656071"
---
# <a name="renewdhcpleaseall-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="7e9af-103">Метод RenewDHCPLeaseAll \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e9af-103">RenewDHCPLeaseAll method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="7e9af-104">Статический метод класса **RenewDHCPLeaseAll** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) обновляет IP-адреса на всех сетевых адаптерах с поддержкой DHCP.</span><span class="sxs-lookup"><span data-stu-id="7e9af-104">The **RenewDHCPLeaseAll** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method renews the IP addresses on all DHCP-enabled network adapters.</span></span>

<span data-ttu-id="7e9af-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="7e9af-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7e9af-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="7e9af-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7e9af-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e9af-107">Syntax</span></span>


```mof
uint32 RenewDHCPLeaseAll();
```



## <a name="parameters"></a><span data-ttu-id="7e9af-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e9af-108">Parameters</span></span>

<span data-ttu-id="7e9af-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7e9af-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7e9af-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7e9af-110">Return value</span></span>

<span data-ttu-id="7e9af-111">Возвращает значение 0 (ноль) для успешного завершения, если не требуется перезагрузка, 1 (один) для успешного завершения, когда требуется перезагрузка, и другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="7e9af-111">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="7e9af-112">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="7e9af-112">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="7e9af-113">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="7e9af-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="7e9af-114">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="7e9af-114">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-115">0</span><span class="sxs-lookup"><span data-stu-id="7e9af-115">0</span></span>

<span data-ttu-id="7e9af-116">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="7e9af-116">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-117">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="7e9af-117">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-118">1</span><span class="sxs-lookup"><span data-stu-id="7e9af-118">1</span></span>

<span data-ttu-id="7e9af-119">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="7e9af-119">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-120">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="7e9af-120">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-121">64</span><span class="sxs-lookup"><span data-stu-id="7e9af-121">64</span></span>

<span data-ttu-id="7e9af-122">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="7e9af-122">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-123">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="7e9af-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-124">65</span><span class="sxs-lookup"><span data-stu-id="7e9af-124">65</span></span>

<span data-ttu-id="7e9af-125">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="7e9af-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-126">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="7e9af-126">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-127">66</span><span class="sxs-lookup"><span data-stu-id="7e9af-127">66</span></span>

<span data-ttu-id="7e9af-128">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="7e9af-128">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-129">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="7e9af-129">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-130">67</span><span class="sxs-lookup"><span data-stu-id="7e9af-130">67</span></span>

<span data-ttu-id="7e9af-131">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7e9af-131">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-132">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="7e9af-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-133">68</span><span class="sxs-lookup"><span data-stu-id="7e9af-133">68</span></span>

<span data-ttu-id="7e9af-134">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="7e9af-134">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-135">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="7e9af-135">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-136">69</span><span class="sxs-lookup"><span data-stu-id="7e9af-136">69</span></span>

<span data-ttu-id="7e9af-137">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="7e9af-137">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-138">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="7e9af-138">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-139">70</span><span class="sxs-lookup"><span data-stu-id="7e9af-139">70</span></span>

<span data-ttu-id="7e9af-140">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="7e9af-140">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-141">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="7e9af-141">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-142">71</span><span class="sxs-lookup"><span data-stu-id="7e9af-142">71</span></span>

<span data-ttu-id="7e9af-143">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="7e9af-143">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-144">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="7e9af-144">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-145">72</span><span class="sxs-lookup"><span data-stu-id="7e9af-145">72</span></span>

<span data-ttu-id="7e9af-146">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="7e9af-146">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-147">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="7e9af-147">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-148">73</span><span class="sxs-lookup"><span data-stu-id="7e9af-148">73</span></span>

<span data-ttu-id="7e9af-149">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="7e9af-149">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-150">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="7e9af-150">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-151">74</span><span class="sxs-lookup"><span data-stu-id="7e9af-151">74</span></span>

<span data-ttu-id="7e9af-152">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="7e9af-152">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-153">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="7e9af-153">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-154">75</span><span class="sxs-lookup"><span data-stu-id="7e9af-154">75</span></span>

<span data-ttu-id="7e9af-155">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="7e9af-155">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-156">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="7e9af-156">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-157">76</span><span class="sxs-lookup"><span data-stu-id="7e9af-157">76</span></span>

<span data-ttu-id="7e9af-158">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="7e9af-158">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-159">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="7e9af-159">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-160">77</span><span class="sxs-lookup"><span data-stu-id="7e9af-160">77</span></span>

<span data-ttu-id="7e9af-161">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="7e9af-161">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-162">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="7e9af-162">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-163">78</span><span class="sxs-lookup"><span data-stu-id="7e9af-163">78</span></span>

<span data-ttu-id="7e9af-164">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="7e9af-164">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-165">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="7e9af-165">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-166">79</span><span class="sxs-lookup"><span data-stu-id="7e9af-166">79</span></span>

<span data-ttu-id="7e9af-167">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="7e9af-167">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-168">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="7e9af-168">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-169">80</span><span class="sxs-lookup"><span data-stu-id="7e9af-169">80</span></span>

<span data-ttu-id="7e9af-170">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="7e9af-170">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-171">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="7e9af-171">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-172">81</span><span class="sxs-lookup"><span data-stu-id="7e9af-172">81</span></span>

<span data-ttu-id="7e9af-173">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="7e9af-173">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-174">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="7e9af-174">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-175">82</span><span class="sxs-lookup"><span data-stu-id="7e9af-175">82</span></span>

<span data-ttu-id="7e9af-176">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="7e9af-176">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-177">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="7e9af-177">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-178">83</span><span class="sxs-lookup"><span data-stu-id="7e9af-178">83</span></span>

<span data-ttu-id="7e9af-179">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="7e9af-179">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-180">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="7e9af-180">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-181">84</span><span class="sxs-lookup"><span data-stu-id="7e9af-181">84</span></span>

<span data-ttu-id="7e9af-182">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="7e9af-182">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-183">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="7e9af-183">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-184">85</span><span class="sxs-lookup"><span data-stu-id="7e9af-184">85</span></span>

<span data-ttu-id="7e9af-185">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="7e9af-185">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-186">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="7e9af-186">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-187">86</span><span class="sxs-lookup"><span data-stu-id="7e9af-187">86</span></span>

<span data-ttu-id="7e9af-188">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="7e9af-188">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-189">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="7e9af-189">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-190">87</span><span class="sxs-lookup"><span data-stu-id="7e9af-190">87</span></span>

<span data-ttu-id="7e9af-191">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="7e9af-191">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-192">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="7e9af-192">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-193">88</span><span class="sxs-lookup"><span data-stu-id="7e9af-193">88</span></span>

<span data-ttu-id="7e9af-194">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="7e9af-194">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-195">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="7e9af-195">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-196">89</span><span class="sxs-lookup"><span data-stu-id="7e9af-196">89</span></span>

<span data-ttu-id="7e9af-197">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="7e9af-197">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-198">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="7e9af-198">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-199">90</span><span class="sxs-lookup"><span data-stu-id="7e9af-199">90</span></span>

<span data-ttu-id="7e9af-200">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="7e9af-200">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-201">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="7e9af-201">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-202">91</span><span class="sxs-lookup"><span data-stu-id="7e9af-202">91</span></span>

<span data-ttu-id="7e9af-203">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="7e9af-203">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-204">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="7e9af-204">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-205">92</span><span class="sxs-lookup"><span data-stu-id="7e9af-205">92</span></span>

<span data-ttu-id="7e9af-206">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="7e9af-206">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-207">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="7e9af-207">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-208">93</span><span class="sxs-lookup"><span data-stu-id="7e9af-208">93</span></span>

<span data-ttu-id="7e9af-209">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="7e9af-209">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-210">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="7e9af-210">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-211">94</span><span class="sxs-lookup"><span data-stu-id="7e9af-211">94</span></span>

<span data-ttu-id="7e9af-212">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="7e9af-212">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-213">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="7e9af-213">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-214">95</span><span class="sxs-lookup"><span data-stu-id="7e9af-214">95</span></span>

<span data-ttu-id="7e9af-215">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="7e9af-215">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-216">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="7e9af-216">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-217">96</span><span class="sxs-lookup"><span data-stu-id="7e9af-217">96</span></span>

<span data-ttu-id="7e9af-218">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="7e9af-218">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-219">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="7e9af-219">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-220">97</span><span class="sxs-lookup"><span data-stu-id="7e9af-220">97</span></span>

<span data-ttu-id="7e9af-221">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="7e9af-221">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-222">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="7e9af-222">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-223">98</span><span class="sxs-lookup"><span data-stu-id="7e9af-223">98</span></span>

<span data-ttu-id="7e9af-224">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="7e9af-224">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-225">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="7e9af-225">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-226">100</span><span class="sxs-lookup"><span data-stu-id="7e9af-226">100</span></span>

<span data-ttu-id="7e9af-227">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="7e9af-227">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="7e9af-228">**Другое**</span><span class="sxs-lookup"><span data-stu-id="7e9af-228">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="7e9af-229">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="7e9af-229">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7e9af-230">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7e9af-230">Remarks</span></span>

<span data-ttu-id="7e9af-231">Аренда IP-адреса, назначенного DHCP-сервером, имеет дату окончания срока действия, которую клиент должен продлить, если планируется продолжать использовать назначенный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="7e9af-231">The lease for the IP address assigned by a DHCP server has an expiration date that the client must renew if it intends to continue use of the assigned IP address.</span></span>

## <a name="examples"></a><span data-ttu-id="7e9af-232">Примеры</span><span class="sxs-lookup"><span data-stu-id="7e9af-232">Examples</span></span>

<span data-ttu-id="7e9af-233">В статье [обновление всех аренд по протоколу DHCP](https://Gallery.TechNet.Microsoft.Com/b29171b8-21b0-492a-b0fe-67e650adca99) на языке VBScript в коллекции TechNet включены все аренды DHCP, используемые на компьютере.</span><span class="sxs-lookup"><span data-stu-id="7e9af-233">The [Renew All DHCP Leases](https://Gallery.TechNet.Microsoft.Com/b29171b8-21b0-492a-b0fe-67e650adca99) VBScript example on TechNet Gallery renews all the DHCP leases currently in use on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e9af-234">Требования</span><span class="sxs-lookup"><span data-stu-id="7e9af-234">Requirements</span></span>



| <span data-ttu-id="7e9af-235">Требование</span><span class="sxs-lookup"><span data-stu-id="7e9af-235">Requirement</span></span> | <span data-ttu-id="7e9af-236">Значение</span><span class="sxs-lookup"><span data-stu-id="7e9af-236">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e9af-237">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7e9af-237">Minimum supported client</span></span><br/> | <span data-ttu-id="7e9af-238">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7e9af-238">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7e9af-239">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7e9af-239">Minimum supported server</span></span><br/> | <span data-ttu-id="7e9af-240">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e9af-240">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7e9af-241">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7e9af-241">Namespace</span></span><br/>                | <span data-ttu-id="7e9af-242">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7e9af-242">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7e9af-243">MOF</span><span class="sxs-lookup"><span data-stu-id="7e9af-243">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e9af-244"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7e9af-244"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e9af-245">DLL</span><span class="sxs-lookup"><span data-stu-id="7e9af-245">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e9af-246"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e9af-246"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e9af-247">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e9af-247">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e9af-248">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="7e9af-248">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="7e9af-249">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="7e9af-249">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="7e9af-250">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="7e9af-250">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="7e9af-251">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="7e9af-251">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="7e9af-252">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="7e9af-252">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

