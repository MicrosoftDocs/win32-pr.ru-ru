---
description: Этот метод устарел. Приложения должны использовать API качества обслуживания (QoS) для управления битами типа службы (TOS).
ms.assetid: 18860c13-7324-4a37-b83c-f3d15c425acb
ms.tgt_platform: multiple
title: Метод Сетдефаулттос класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDefaultTOS
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5df55ff88c87047a48a84a122c8e58c8148a7cff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656032"
---
# <a name="setdefaulttos-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="41651-104">Метод Сетдефаулттос \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="41651-104">SetDefaultTOS method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="41651-105">Этот метод устарел.</span><span class="sxs-lookup"><span data-stu-id="41651-105">This method is obsolete.</span></span> <span data-ttu-id="41651-106">Приложения должны использовать API качества обслуживания (QoS) для управления битами типа службы (TOS).</span><span class="sxs-lookup"><span data-stu-id="41651-106">Applications should use the Quality of Service (QoS) API to manipulate Type of Service (TOS) bits.</span></span> <span data-ttu-id="41651-107">Дополнительные сведения см. в разделе [качество обслуживания](/previous-versions/windows/desktop/qos/qos-start-page).</span><span class="sxs-lookup"><span data-stu-id="41651-107">For more information, see [Quality of Service](/previous-versions/windows/desktop/qos/qos-start-page).</span></span>

<span data-ttu-id="41651-108">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="41651-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="41651-109">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="41651-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="41651-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="41651-110">Syntax</span></span>


```mof
uint32 SetDefaultTOS(
  [in] uint8 DefaultTOS
);
```



## <a name="parameters"></a><span data-ttu-id="41651-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="41651-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41651-112">*Дефаулттос* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="41651-112">*DefaultTOS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41651-113">Тип значения службы (TOS), который помещается в заголовок исходящих IP-пакетов.</span><span class="sxs-lookup"><span data-stu-id="41651-113">Type of Service (TOS) value put in the header of outgoing IP packets.</span></span> <span data-ttu-id="41651-114">Определение значений см. в документе RFC 791.</span><span class="sxs-lookup"><span data-stu-id="41651-114">For a definition of the values, see RFC 791.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41651-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="41651-115">Return value</span></span>

<span data-ttu-id="41651-116">Возвращает значение 0 (ноль) для успешного завершения, если не требуется перезагрузка, 1 (один) для успешного завершения, когда требуется перезагрузка, и другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="41651-116">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="41651-117">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="41651-117">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="41651-118">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="41651-118">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="41651-119">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="41651-119">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="41651-120">0</span><span class="sxs-lookup"><span data-stu-id="41651-120">0</span></span>

<span data-ttu-id="41651-121">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="41651-121">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="41651-122">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="41651-122">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="41651-123">1</span><span class="sxs-lookup"><span data-stu-id="41651-123">1</span></span>

<span data-ttu-id="41651-124">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="41651-124">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="41651-125">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="41651-125">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="41651-126">64</span><span class="sxs-lookup"><span data-stu-id="41651-126">64</span></span>

<span data-ttu-id="41651-127">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="41651-127">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="41651-128">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="41651-128">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="41651-129">65</span><span class="sxs-lookup"><span data-stu-id="41651-129">65</span></span>

<span data-ttu-id="41651-130">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="41651-130">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="41651-131">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="41651-131">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="41651-132">66</span><span class="sxs-lookup"><span data-stu-id="41651-132">66</span></span>

<span data-ttu-id="41651-133">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="41651-133">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="41651-134">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="41651-134">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="41651-135">67</span><span class="sxs-lookup"><span data-stu-id="41651-135">67</span></span>

<span data-ttu-id="41651-136">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="41651-136">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="41651-137">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="41651-137">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="41651-138">68</span><span class="sxs-lookup"><span data-stu-id="41651-138">68</span></span>

<span data-ttu-id="41651-139">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="41651-139">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="41651-140">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="41651-140">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="41651-141">69</span><span class="sxs-lookup"><span data-stu-id="41651-141">69</span></span>

<span data-ttu-id="41651-142">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="41651-142">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="41651-143">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="41651-143">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="41651-144">70</span><span class="sxs-lookup"><span data-stu-id="41651-144">70</span></span>

<span data-ttu-id="41651-145">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="41651-145">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="41651-146">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="41651-146">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="41651-147">71</span><span class="sxs-lookup"><span data-stu-id="41651-147">71</span></span>

<span data-ttu-id="41651-148">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="41651-148">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="41651-149">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="41651-149">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="41651-150">72</span><span class="sxs-lookup"><span data-stu-id="41651-150">72</span></span>

<span data-ttu-id="41651-151">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="41651-151">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="41651-152">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="41651-152">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="41651-153">73</span><span class="sxs-lookup"><span data-stu-id="41651-153">73</span></span>

<span data-ttu-id="41651-154">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="41651-154">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="41651-155">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="41651-155">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="41651-156">74</span><span class="sxs-lookup"><span data-stu-id="41651-156">74</span></span>

<span data-ttu-id="41651-157">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="41651-157">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="41651-158">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="41651-158">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="41651-159">75</span><span class="sxs-lookup"><span data-stu-id="41651-159">75</span></span>

<span data-ttu-id="41651-160">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="41651-160">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="41651-161">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="41651-161">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="41651-162">76</span><span class="sxs-lookup"><span data-stu-id="41651-162">76</span></span>

<span data-ttu-id="41651-163">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="41651-163">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="41651-164">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="41651-164">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="41651-165">77</span><span class="sxs-lookup"><span data-stu-id="41651-165">77</span></span>

<span data-ttu-id="41651-166">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="41651-166">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="41651-167">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="41651-167">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="41651-168">78</span><span class="sxs-lookup"><span data-stu-id="41651-168">78</span></span>

<span data-ttu-id="41651-169">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="41651-169">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="41651-170">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="41651-170">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="41651-171">79</span><span class="sxs-lookup"><span data-stu-id="41651-171">79</span></span>

<span data-ttu-id="41651-172">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="41651-172">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="41651-173">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="41651-173">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="41651-174">80</span><span class="sxs-lookup"><span data-stu-id="41651-174">80</span></span>

<span data-ttu-id="41651-175">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="41651-175">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="41651-176">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="41651-176">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="41651-177">81</span><span class="sxs-lookup"><span data-stu-id="41651-177">81</span></span>

<span data-ttu-id="41651-178">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="41651-178">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="41651-179">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="41651-179">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="41651-180">82</span><span class="sxs-lookup"><span data-stu-id="41651-180">82</span></span>

<span data-ttu-id="41651-181">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="41651-181">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="41651-182">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="41651-182">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="41651-183">83</span><span class="sxs-lookup"><span data-stu-id="41651-183">83</span></span>

<span data-ttu-id="41651-184">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="41651-184">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="41651-185">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="41651-185">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="41651-186">84</span><span class="sxs-lookup"><span data-stu-id="41651-186">84</span></span>

<span data-ttu-id="41651-187">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="41651-187">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="41651-188">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="41651-188">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="41651-189">85</span><span class="sxs-lookup"><span data-stu-id="41651-189">85</span></span>

<span data-ttu-id="41651-190">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="41651-190">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="41651-191">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="41651-191">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="41651-192">86</span><span class="sxs-lookup"><span data-stu-id="41651-192">86</span></span>

<span data-ttu-id="41651-193">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="41651-193">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="41651-194">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="41651-194">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="41651-195">87</span><span class="sxs-lookup"><span data-stu-id="41651-195">87</span></span>

<span data-ttu-id="41651-196">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="41651-196">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="41651-197">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="41651-197">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="41651-198">88</span><span class="sxs-lookup"><span data-stu-id="41651-198">88</span></span>

<span data-ttu-id="41651-199">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="41651-199">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="41651-200">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="41651-200">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="41651-201">89</span><span class="sxs-lookup"><span data-stu-id="41651-201">89</span></span>

<span data-ttu-id="41651-202">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="41651-202">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="41651-203">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="41651-203">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="41651-204">90</span><span class="sxs-lookup"><span data-stu-id="41651-204">90</span></span>

<span data-ttu-id="41651-205">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="41651-205">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="41651-206">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="41651-206">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="41651-207">91</span><span class="sxs-lookup"><span data-stu-id="41651-207">91</span></span>

<span data-ttu-id="41651-208">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="41651-208">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="41651-209">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="41651-209">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="41651-210">92</span><span class="sxs-lookup"><span data-stu-id="41651-210">92</span></span>

<span data-ttu-id="41651-211">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="41651-211">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="41651-212">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="41651-212">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="41651-213">93</span><span class="sxs-lookup"><span data-stu-id="41651-213">93</span></span>

<span data-ttu-id="41651-214">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="41651-214">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="41651-215">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="41651-215">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="41651-216">94</span><span class="sxs-lookup"><span data-stu-id="41651-216">94</span></span>

<span data-ttu-id="41651-217">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="41651-217">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="41651-218">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="41651-218">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="41651-219">95</span><span class="sxs-lookup"><span data-stu-id="41651-219">95</span></span>

<span data-ttu-id="41651-220">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="41651-220">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="41651-221">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="41651-221">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="41651-222">96</span><span class="sxs-lookup"><span data-stu-id="41651-222">96</span></span>

<span data-ttu-id="41651-223">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="41651-223">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="41651-224">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="41651-224">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="41651-225">97</span><span class="sxs-lookup"><span data-stu-id="41651-225">97</span></span>

<span data-ttu-id="41651-226">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="41651-226">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="41651-227">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="41651-227">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="41651-228">98</span><span class="sxs-lookup"><span data-stu-id="41651-228">98</span></span>

<span data-ttu-id="41651-229">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="41651-229">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="41651-230">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="41651-230">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="41651-231">100</span><span class="sxs-lookup"><span data-stu-id="41651-231">100</span></span>

<span data-ttu-id="41651-232">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="41651-232">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="41651-233">**Другое**</span><span class="sxs-lookup"><span data-stu-id="41651-233">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="41651-234">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="41651-234">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41651-235">Комментарии</span><span class="sxs-lookup"><span data-stu-id="41651-235">Remarks</span></span>

<span data-ttu-id="41651-236">Статический метод класса **сетдефаулттос** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) используется для задания значения TOS по умолчанию в заголовке исходящих пакетов IP.</span><span class="sxs-lookup"><span data-stu-id="41651-236">The **SetDefaultTOS** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the default TOS value in the header of outgoing IP packets.</span></span>

## <a name="requirements"></a><span data-ttu-id="41651-237">Требования</span><span class="sxs-lookup"><span data-stu-id="41651-237">Requirements</span></span>



| <span data-ttu-id="41651-238">Требование</span><span class="sxs-lookup"><span data-stu-id="41651-238">Requirement</span></span> | <span data-ttu-id="41651-239">Значение</span><span class="sxs-lookup"><span data-stu-id="41651-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41651-240">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="41651-240">Minimum supported client</span></span><br/> | <span data-ttu-id="41651-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41651-241">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="41651-242">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="41651-242">Minimum supported server</span></span><br/> | <span data-ttu-id="41651-243">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41651-243">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="41651-244">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="41651-244">Namespace</span></span><br/>                | <span data-ttu-id="41651-245">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="41651-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="41651-246">MOF</span><span class="sxs-lookup"><span data-stu-id="41651-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41651-247"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="41651-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="41651-248">DLL</span><span class="sxs-lookup"><span data-stu-id="41651-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41651-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41651-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41651-250">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41651-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41651-251">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="41651-251">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="41651-252">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="41651-252">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="41651-253">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="41651-253">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="41651-254">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="41651-254">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="41651-255">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="41651-255">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

