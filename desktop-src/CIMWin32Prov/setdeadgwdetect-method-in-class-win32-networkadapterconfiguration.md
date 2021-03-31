---
description: Статический метод класса WMI Сетдеадгвдетект используется для включения обнаружения неработающих шлюзов.
ms.assetid: c813aaef-7215-4759-b68f-7808fd203d9c
ms.tgt_platform: multiple
title: Метод Сетдеадгвдетект класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDeadGWDetect
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 83f62d84af193be99850f1a82b720a2983ca77c3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104495993"
---
# <a name="setdeadgwdetect-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="ace83-103">Метод Сетдеадгвдетект \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="ace83-103">SetDeadGWDetect method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="ace83-104">Статический метод [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) **сетдеадгвдетект** используется для включения обнаружения неработающих шлюзов.</span><span class="sxs-lookup"><span data-stu-id="ace83-104">The **SetDeadGWDetect** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable dead gateway detection.</span></span>

<span data-ttu-id="ace83-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="ace83-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ace83-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ace83-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ace83-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ace83-107">Syntax</span></span>


```mof
uint32 SetDeadGWDetect(
  [in] boolean DeadGWDetectEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="ace83-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ace83-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ace83-109">*Деадгвдетектенаблед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ace83-109">*DeadGWDetectEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace83-110">Если задано **значение true**, обнаружение недоставленных шлюзов должно быть включено.</span><span class="sxs-lookup"><span data-stu-id="ace83-110">If **true**, dead gateway detection should be enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ace83-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ace83-111">Return value</span></span>

<span data-ttu-id="ace83-112">Возвращает значение 0 (ноль) для успешного завершения, если не требуется перезагрузка, 1 (один) для успешного завершения, когда требуется перезагрузка, и другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="ace83-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="ace83-113">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="ace83-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="ace83-114">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="ace83-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="ace83-115">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="ace83-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-116">0</span><span class="sxs-lookup"><span data-stu-id="ace83-116">0</span></span>

<span data-ttu-id="ace83-117">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="ace83-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-118">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="ace83-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-119">1</span><span class="sxs-lookup"><span data-stu-id="ace83-119">1</span></span>

<span data-ttu-id="ace83-120">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="ace83-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-121">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="ace83-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-122">64</span><span class="sxs-lookup"><span data-stu-id="ace83-122">64</span></span>

<span data-ttu-id="ace83-123">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="ace83-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-124">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="ace83-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-125">65</span><span class="sxs-lookup"><span data-stu-id="ace83-125">65</span></span>

<span data-ttu-id="ace83-126">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="ace83-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-127">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="ace83-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-128">66</span><span class="sxs-lookup"><span data-stu-id="ace83-128">66</span></span>

<span data-ttu-id="ace83-129">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="ace83-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-130">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="ace83-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-131">67</span><span class="sxs-lookup"><span data-stu-id="ace83-131">67</span></span>

<span data-ttu-id="ace83-132">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ace83-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-133">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="ace83-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-134">68</span><span class="sxs-lookup"><span data-stu-id="ace83-134">68</span></span>

<span data-ttu-id="ace83-135">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="ace83-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-136">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="ace83-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-137">69</span><span class="sxs-lookup"><span data-stu-id="ace83-137">69</span></span>

<span data-ttu-id="ace83-138">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="ace83-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-139">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="ace83-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-140">70</span><span class="sxs-lookup"><span data-stu-id="ace83-140">70</span></span>

<span data-ttu-id="ace83-141">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="ace83-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-142">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="ace83-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-143">71</span><span class="sxs-lookup"><span data-stu-id="ace83-143">71</span></span>

<span data-ttu-id="ace83-144">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="ace83-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-145">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="ace83-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-146">72</span><span class="sxs-lookup"><span data-stu-id="ace83-146">72</span></span>

<span data-ttu-id="ace83-147">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="ace83-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-148">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="ace83-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-149">73</span><span class="sxs-lookup"><span data-stu-id="ace83-149">73</span></span>

<span data-ttu-id="ace83-150">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="ace83-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-151">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="ace83-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-152">74</span><span class="sxs-lookup"><span data-stu-id="ace83-152">74</span></span>

<span data-ttu-id="ace83-153">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="ace83-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-154">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="ace83-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-155">75</span><span class="sxs-lookup"><span data-stu-id="ace83-155">75</span></span>

<span data-ttu-id="ace83-156">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="ace83-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-157">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="ace83-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-158">76</span><span class="sxs-lookup"><span data-stu-id="ace83-158">76</span></span>

<span data-ttu-id="ace83-159">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="ace83-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-160">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="ace83-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-161">77</span><span class="sxs-lookup"><span data-stu-id="ace83-161">77</span></span>

<span data-ttu-id="ace83-162">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="ace83-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-163">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="ace83-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-164">78</span><span class="sxs-lookup"><span data-stu-id="ace83-164">78</span></span>

<span data-ttu-id="ace83-165">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="ace83-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-166">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="ace83-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-167">79</span><span class="sxs-lookup"><span data-stu-id="ace83-167">79</span></span>

<span data-ttu-id="ace83-168">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="ace83-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-169">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="ace83-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-170">80</span><span class="sxs-lookup"><span data-stu-id="ace83-170">80</span></span>

<span data-ttu-id="ace83-171">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="ace83-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-172">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="ace83-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-173">81</span><span class="sxs-lookup"><span data-stu-id="ace83-173">81</span></span>

<span data-ttu-id="ace83-174">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="ace83-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-175">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="ace83-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-176">82</span><span class="sxs-lookup"><span data-stu-id="ace83-176">82</span></span>

<span data-ttu-id="ace83-177">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="ace83-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-178">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="ace83-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-179">83</span><span class="sxs-lookup"><span data-stu-id="ace83-179">83</span></span>

<span data-ttu-id="ace83-180">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="ace83-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-181">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="ace83-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-182">84</span><span class="sxs-lookup"><span data-stu-id="ace83-182">84</span></span>

<span data-ttu-id="ace83-183">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="ace83-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-184">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="ace83-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-185">85</span><span class="sxs-lookup"><span data-stu-id="ace83-185">85</span></span>

<span data-ttu-id="ace83-186">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="ace83-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-187">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="ace83-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-188">86</span><span class="sxs-lookup"><span data-stu-id="ace83-188">86</span></span>

<span data-ttu-id="ace83-189">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="ace83-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-190">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="ace83-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-191">87</span><span class="sxs-lookup"><span data-stu-id="ace83-191">87</span></span>

<span data-ttu-id="ace83-192">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="ace83-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-193">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="ace83-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-194">88</span><span class="sxs-lookup"><span data-stu-id="ace83-194">88</span></span>

<span data-ttu-id="ace83-195">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="ace83-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-196">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="ace83-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-197">89</span><span class="sxs-lookup"><span data-stu-id="ace83-197">89</span></span>

<span data-ttu-id="ace83-198">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="ace83-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-199">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="ace83-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-200">90</span><span class="sxs-lookup"><span data-stu-id="ace83-200">90</span></span>

<span data-ttu-id="ace83-201">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="ace83-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-202">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="ace83-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-203">91</span><span class="sxs-lookup"><span data-stu-id="ace83-203">91</span></span>

<span data-ttu-id="ace83-204">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="ace83-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-205">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="ace83-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-206">92</span><span class="sxs-lookup"><span data-stu-id="ace83-206">92</span></span>

<span data-ttu-id="ace83-207">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="ace83-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-208">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="ace83-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-209">93</span><span class="sxs-lookup"><span data-stu-id="ace83-209">93</span></span>

<span data-ttu-id="ace83-210">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="ace83-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-211">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="ace83-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-212">94</span><span class="sxs-lookup"><span data-stu-id="ace83-212">94</span></span>

<span data-ttu-id="ace83-213">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="ace83-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-214">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="ace83-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-215">95</span><span class="sxs-lookup"><span data-stu-id="ace83-215">95</span></span>

<span data-ttu-id="ace83-216">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="ace83-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-217">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="ace83-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-218">96</span><span class="sxs-lookup"><span data-stu-id="ace83-218">96</span></span>

<span data-ttu-id="ace83-219">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="ace83-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-220">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="ace83-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-221">97</span><span class="sxs-lookup"><span data-stu-id="ace83-221">97</span></span>

<span data-ttu-id="ace83-222">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="ace83-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-223">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="ace83-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-224">98</span><span class="sxs-lookup"><span data-stu-id="ace83-224">98</span></span>

<span data-ttu-id="ace83-225">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="ace83-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-226">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="ace83-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-227">100</span><span class="sxs-lookup"><span data-stu-id="ace83-227">100</span></span>

<span data-ttu-id="ace83-228">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="ace83-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ace83-229">**Другое**</span><span class="sxs-lookup"><span data-stu-id="ace83-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="ace83-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="ace83-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ace83-231">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ace83-231">Remarks</span></span>

<span data-ttu-id="ace83-232">Если эта функция включена, TCP запрашивает IP-адрес для смены резервного шлюза, если он повторно передает сегмент несколько раз без получения ответа.</span><span class="sxs-lookup"><span data-stu-id="ace83-232">With this feature enabled, TCP asks IP to change to a backup gateway if it retransmits a segment several times without receiving a response.</span></span>

## <a name="examples"></a><span data-ttu-id="ace83-233">Примеры</span><span class="sxs-lookup"><span data-stu-id="ace83-233">Examples</span></span>

<span data-ttu-id="ace83-234">Пример [включения обнаружения недоставленных шлюзов для всех сетевых адаптеров](https://Gallery.TechNet.Microsoft.Com/4a24b080-1a8b-4085-9419-58d096ef8437) в коллекции TechNet использует **сетдеадгвдетект** для настройки всех сетевых адаптеров на компьютере для автоматического обнаружения неработающих шлюзов.</span><span class="sxs-lookup"><span data-stu-id="ace83-234">The [Enable Dead Gateway Detection for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/4a24b080-1a8b-4085-9419-58d096ef8437) VBScript sample on TechNet Gallery uses **SetDeadGWDetect** to configure all network adapters on a computer to automatically detect dead gateways.</span></span>

## <a name="requirements"></a><span data-ttu-id="ace83-235">Требования</span><span class="sxs-lookup"><span data-stu-id="ace83-235">Requirements</span></span>



| <span data-ttu-id="ace83-236">Требование</span><span class="sxs-lookup"><span data-stu-id="ace83-236">Requirement</span></span> | <span data-ttu-id="ace83-237">Значение</span><span class="sxs-lookup"><span data-stu-id="ace83-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ace83-238">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ace83-238">Minimum supported client</span></span><br/> | <span data-ttu-id="ace83-239">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ace83-239">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ace83-240">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ace83-240">Minimum supported server</span></span><br/> | <span data-ttu-id="ace83-241">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ace83-241">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ace83-242">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ace83-242">Namespace</span></span><br/>                | <span data-ttu-id="ace83-243">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ace83-243">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ace83-244">MOF</span><span class="sxs-lookup"><span data-stu-id="ace83-244">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ace83-245"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ace83-245"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ace83-246">DLL</span><span class="sxs-lookup"><span data-stu-id="ace83-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ace83-247"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ace83-247"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ace83-248">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ace83-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ace83-249">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="ace83-249">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="ace83-250">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="ace83-250">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="ace83-251">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="ace83-251">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="ace83-252">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="ace83-252">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="ace83-253">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="ace83-253">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

