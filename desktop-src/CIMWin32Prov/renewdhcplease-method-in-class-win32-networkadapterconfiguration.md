---
description: Метод класса WMI RenewDHCPLease обновляет IP-адрес на конкретных сетевых адаптерах с поддержкой DHCP.
ms.assetid: b6e5d1fb-db3f-4491-bbac-46b1f2e7206e
ms.tgt_platform: multiple
title: Метод RenewDHCPLease класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.RenewDHCPLease
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4603f013c6b4c2c80edd555608b5f59325b6a6d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072548"
---
# <a name="renewdhcplease-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="7fad1-103">Метод RenewDHCPLease \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="7fad1-103">RenewDHCPLease method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="7fad1-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) RenewDHCPLease обновляет IP-адрес на конкретных сетевых адаптерах с поддержкой DHCP.</span><span class="sxs-lookup"><span data-stu-id="7fad1-104">The **RenewDHCPLease** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renews the IP address on specific DHCP-enabled network adapters.</span></span>

<span data-ttu-id="7fad1-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="7fad1-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7fad1-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="7fad1-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7fad1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7fad1-107">Syntax</span></span>


```mof
uint32 RenewDHCPLease();
```



## <a name="parameters"></a><span data-ttu-id="7fad1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7fad1-108">Parameters</span></span>

<span data-ttu-id="7fad1-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7fad1-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7fad1-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7fad1-110">Return value</span></span>

<span data-ttu-id="7fad1-111">Возвращает значение 0 (ноль) для успешного завершения, если не требуется перезагрузка, 1 (один) для успешного завершения, когда требуется перезагрузка, и другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="7fad1-111">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="7fad1-112">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="7fad1-112">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="7fad1-113">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="7fad1-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="7fad1-114">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="7fad1-114">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-115">0</span><span class="sxs-lookup"><span data-stu-id="7fad1-115">0</span></span>

<span data-ttu-id="7fad1-116">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="7fad1-116">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-117">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="7fad1-117">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-118">1</span><span class="sxs-lookup"><span data-stu-id="7fad1-118">1</span></span>

<span data-ttu-id="7fad1-119">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="7fad1-119">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-120">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="7fad1-120">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-121">64</span><span class="sxs-lookup"><span data-stu-id="7fad1-121">64</span></span>

<span data-ttu-id="7fad1-122">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="7fad1-122">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-123">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="7fad1-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-124">65</span><span class="sxs-lookup"><span data-stu-id="7fad1-124">65</span></span>

<span data-ttu-id="7fad1-125">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="7fad1-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-126">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="7fad1-126">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-127">66</span><span class="sxs-lookup"><span data-stu-id="7fad1-127">66</span></span>

<span data-ttu-id="7fad1-128">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="7fad1-128">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-129">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="7fad1-129">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-130">67</span><span class="sxs-lookup"><span data-stu-id="7fad1-130">67</span></span>

<span data-ttu-id="7fad1-131">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7fad1-131">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-132">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="7fad1-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-133">68</span><span class="sxs-lookup"><span data-stu-id="7fad1-133">68</span></span>

<span data-ttu-id="7fad1-134">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="7fad1-134">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-135">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="7fad1-135">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-136">69</span><span class="sxs-lookup"><span data-stu-id="7fad1-136">69</span></span>

<span data-ttu-id="7fad1-137">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="7fad1-137">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-138">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="7fad1-138">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-139">70</span><span class="sxs-lookup"><span data-stu-id="7fad1-139">70</span></span>

<span data-ttu-id="7fad1-140">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="7fad1-140">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-141">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="7fad1-141">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-142">71</span><span class="sxs-lookup"><span data-stu-id="7fad1-142">71</span></span>

<span data-ttu-id="7fad1-143">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="7fad1-143">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-144">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="7fad1-144">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-145">72</span><span class="sxs-lookup"><span data-stu-id="7fad1-145">72</span></span>

<span data-ttu-id="7fad1-146">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="7fad1-146">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-147">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="7fad1-147">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-148">73</span><span class="sxs-lookup"><span data-stu-id="7fad1-148">73</span></span>

<span data-ttu-id="7fad1-149">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="7fad1-149">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-150">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="7fad1-150">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-151">74</span><span class="sxs-lookup"><span data-stu-id="7fad1-151">74</span></span>

<span data-ttu-id="7fad1-152">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="7fad1-152">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-153">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="7fad1-153">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-154">75</span><span class="sxs-lookup"><span data-stu-id="7fad1-154">75</span></span>

<span data-ttu-id="7fad1-155">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="7fad1-155">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-156">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="7fad1-156">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-157">76</span><span class="sxs-lookup"><span data-stu-id="7fad1-157">76</span></span>

<span data-ttu-id="7fad1-158">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="7fad1-158">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-159">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="7fad1-159">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-160">77</span><span class="sxs-lookup"><span data-stu-id="7fad1-160">77</span></span>

<span data-ttu-id="7fad1-161">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="7fad1-161">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-162">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="7fad1-162">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-163">78</span><span class="sxs-lookup"><span data-stu-id="7fad1-163">78</span></span>

<span data-ttu-id="7fad1-164">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="7fad1-164">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-165">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="7fad1-165">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-166">79</span><span class="sxs-lookup"><span data-stu-id="7fad1-166">79</span></span>

<span data-ttu-id="7fad1-167">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="7fad1-167">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-168">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="7fad1-168">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-169">80</span><span class="sxs-lookup"><span data-stu-id="7fad1-169">80</span></span>

<span data-ttu-id="7fad1-170">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="7fad1-170">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-171">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="7fad1-171">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-172">81</span><span class="sxs-lookup"><span data-stu-id="7fad1-172">81</span></span>

<span data-ttu-id="7fad1-173">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="7fad1-173">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-174">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="7fad1-174">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-175">82</span><span class="sxs-lookup"><span data-stu-id="7fad1-175">82</span></span>

<span data-ttu-id="7fad1-176">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="7fad1-176">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-177">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="7fad1-177">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-178">83</span><span class="sxs-lookup"><span data-stu-id="7fad1-178">83</span></span>

<span data-ttu-id="7fad1-179">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="7fad1-179">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-180">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="7fad1-180">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-181">84</span><span class="sxs-lookup"><span data-stu-id="7fad1-181">84</span></span>

<span data-ttu-id="7fad1-182">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="7fad1-182">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-183">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="7fad1-183">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-184">85</span><span class="sxs-lookup"><span data-stu-id="7fad1-184">85</span></span>

<span data-ttu-id="7fad1-185">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="7fad1-185">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-186">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="7fad1-186">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-187">86</span><span class="sxs-lookup"><span data-stu-id="7fad1-187">86</span></span>

<span data-ttu-id="7fad1-188">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="7fad1-188">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-189">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="7fad1-189">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-190">87</span><span class="sxs-lookup"><span data-stu-id="7fad1-190">87</span></span>

<span data-ttu-id="7fad1-191">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="7fad1-191">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-192">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="7fad1-192">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-193">88</span><span class="sxs-lookup"><span data-stu-id="7fad1-193">88</span></span>

<span data-ttu-id="7fad1-194">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="7fad1-194">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-195">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="7fad1-195">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-196">89</span><span class="sxs-lookup"><span data-stu-id="7fad1-196">89</span></span>

<span data-ttu-id="7fad1-197">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="7fad1-197">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-198">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="7fad1-198">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-199">90</span><span class="sxs-lookup"><span data-stu-id="7fad1-199">90</span></span>

<span data-ttu-id="7fad1-200">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="7fad1-200">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-201">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="7fad1-201">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-202">91</span><span class="sxs-lookup"><span data-stu-id="7fad1-202">91</span></span>

<span data-ttu-id="7fad1-203">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="7fad1-203">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-204">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="7fad1-204">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-205">92</span><span class="sxs-lookup"><span data-stu-id="7fad1-205">92</span></span>

<span data-ttu-id="7fad1-206">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="7fad1-206">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-207">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="7fad1-207">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-208">93</span><span class="sxs-lookup"><span data-stu-id="7fad1-208">93</span></span>

<span data-ttu-id="7fad1-209">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="7fad1-209">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-210">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="7fad1-210">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-211">94</span><span class="sxs-lookup"><span data-stu-id="7fad1-211">94</span></span>

<span data-ttu-id="7fad1-212">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="7fad1-212">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-213">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="7fad1-213">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-214">95</span><span class="sxs-lookup"><span data-stu-id="7fad1-214">95</span></span>

<span data-ttu-id="7fad1-215">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="7fad1-215">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-216">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="7fad1-216">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-217">96</span><span class="sxs-lookup"><span data-stu-id="7fad1-217">96</span></span>

<span data-ttu-id="7fad1-218">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="7fad1-218">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-219">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="7fad1-219">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-220">97</span><span class="sxs-lookup"><span data-stu-id="7fad1-220">97</span></span>

<span data-ttu-id="7fad1-221">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="7fad1-221">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-222">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="7fad1-222">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-223">98</span><span class="sxs-lookup"><span data-stu-id="7fad1-223">98</span></span>

<span data-ttu-id="7fad1-224">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="7fad1-224">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-225">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="7fad1-225">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-226">100</span><span class="sxs-lookup"><span data-stu-id="7fad1-226">100</span></span>

<span data-ttu-id="7fad1-227">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="7fad1-227">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="7fad1-228">**Другое**</span><span class="sxs-lookup"><span data-stu-id="7fad1-228">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="7fad1-229">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="7fad1-229">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7fad1-230">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7fad1-230">Remarks</span></span>

<span data-ttu-id="7fad1-231">Аренда IP-адреса, назначенного DHCP-сервером, имеет дату окончания срока действия, которую клиент должен продлить, если планируется продолжать использовать назначенный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="7fad1-231">The lease for the IP address assigned by a DHCP server has an expiration date that the client must renew if it intends to continue use of the assigned IP address.</span></span>

## <a name="examples"></a><span data-ttu-id="7fad1-232">Примеры</span><span class="sxs-lookup"><span data-stu-id="7fad1-232">Examples</span></span>

<span data-ttu-id="7fad1-233">В этом примере для [обновления IP-адресов с помощью PowerShell](https://Gallery.TechNet.Microsoft.Com/Renew-IP-Adresses-Using-365f6bfa) PowerShell в коллекции TechNet используется **RenewDHCPLease** для выпуска и продления IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="7fad1-233">The [Release Renew IP Adresses Using PowerShell](https://Gallery.TechNet.Microsoft.Com/Renew-IP-Adresses-Using-365f6bfa) PowerShell example on TechNet Gallery uses **RenewDHCPLease** to release and renew an IP address.</span></span>

<span data-ttu-id="7fad1-234">Пример [обновления аренды DHCP для сетевого адаптера](https://Gallery.TechNet.Microsoft.Com/39443fd7-0152-4c0a-89e9-e2753049b203) на языке VBScript в коллекции TechNet использует **RenewDHCPLease** для продления аренды DHCP для каждого сетевого адаптера, связанного с TCP/IP, на компьютере.</span><span class="sxs-lookup"><span data-stu-id="7fad1-234">The [Renew the DHCP Lease for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/39443fd7-0152-4c0a-89e9-e2753049b203) VBScript sample on TechNet Gallery uses **RenewDHCPLease** to renew the DHCP lease for each TCP/IP-bound network adapter in a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fad1-235">Требования</span><span class="sxs-lookup"><span data-stu-id="7fad1-235">Requirements</span></span>



| <span data-ttu-id="7fad1-236">Требование</span><span class="sxs-lookup"><span data-stu-id="7fad1-236">Requirement</span></span> | <span data-ttu-id="7fad1-237">Значение</span><span class="sxs-lookup"><span data-stu-id="7fad1-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fad1-238">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7fad1-238">Minimum supported client</span></span><br/> | <span data-ttu-id="7fad1-239">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7fad1-239">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7fad1-240">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7fad1-240">Minimum supported server</span></span><br/> | <span data-ttu-id="7fad1-241">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7fad1-241">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7fad1-242">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7fad1-242">Namespace</span></span><br/>                | <span data-ttu-id="7fad1-243">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7fad1-243">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7fad1-244">MOF</span><span class="sxs-lookup"><span data-stu-id="7fad1-244">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7fad1-245"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7fad1-245"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7fad1-246">DLL</span><span class="sxs-lookup"><span data-stu-id="7fad1-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fad1-247"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fad1-247"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fad1-248">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7fad1-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fad1-249">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="7fad1-249">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="7fad1-250">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="7fad1-250">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="7fad1-251">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="7fad1-251">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="7fad1-252">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="7fad1-252">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="7fad1-253">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="7fad1-253">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

