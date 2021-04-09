---
description: Статический метод класса SetTcpUseRFC1122UrgentPointer WMI используется для указания того, использует ли TCP спецификацию RFC 1122 для срочных данных или режим, используемый в производных системах проектирования программного обеспечения (BSD).
ms.assetid: f8d07690-2723-4bc3-b15f-a24d575456a7
ms.tgt_platform: multiple
title: Метод SetTcpUseRFC1122UrgentPointer класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpUseRFC1122UrgentPointer
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 928a809211288eb7f024c735ce033b819e5d49f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141560"
---
# <a name="settcpuserfc1122urgentpointer-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="324df-103">Метод SetTcpUseRFC1122UrgentPointer \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="324df-103">SetTcpUseRFC1122UrgentPointer method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="324df-104">Статический метод класса **SetTcpUseRFC1122UrgentPointer** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) используется для указания того, использует ли TCP спецификацию RFC 1122 для срочных данных или режим, используемый в производных системах проектирования программного обеспечения (BSD).</span><span class="sxs-lookup"><span data-stu-id="324df-104">The **SetTcpUseRFC1122UrgentPointer** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to specify whether TCP uses the RFC 1122 specification for urgent data, or the mode used by Berkeley Software Design (BSD) derived systems.</span></span>

<span data-ttu-id="324df-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="324df-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="324df-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="324df-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="324df-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="324df-107">Syntax</span></span>


```mof
uint32 SetTcpUseRFC1122UrgentPointer(
  [in] boolean TcpUseRFC1122UrgentPointer
);
```



## <a name="parameters"></a><span data-ttu-id="324df-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="324df-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="324df-109">*TcpUseRFC1122UrgentPointer* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="324df-109">*TcpUseRFC1122UrgentPointer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="324df-110">Если **значение — true**, TCP использует спецификацию RFC 1122.</span><span class="sxs-lookup"><span data-stu-id="324df-110">If **true**, TCP uses the RFC 1122 specification.</span></span> <span data-ttu-id="324df-111">Если задано **значение false**, срочные данные отправляются в режиме, который используется системами, производными от BSD.</span><span class="sxs-lookup"><span data-stu-id="324df-111">If **false**, urgent data is sent in the mode used by BSD-derived systems.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="324df-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="324df-112">Return value</span></span>

<span data-ttu-id="324df-113">Возвращает значение 0 (ноль) для успешного завершения, если не требуется перезагрузка, 1 (один) для успешного завершения, когда требуется перезагрузка, и другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="324df-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="324df-114">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="324df-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="324df-115">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="324df-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="324df-116">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="324df-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="324df-117">0</span><span class="sxs-lookup"><span data-stu-id="324df-117">0</span></span>

<span data-ttu-id="324df-118">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="324df-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="324df-119">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="324df-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="324df-120">1</span><span class="sxs-lookup"><span data-stu-id="324df-120">1</span></span>

<span data-ttu-id="324df-121">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="324df-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="324df-122">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="324df-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="324df-123">64</span><span class="sxs-lookup"><span data-stu-id="324df-123">64</span></span>

<span data-ttu-id="324df-124">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="324df-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="324df-125">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="324df-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="324df-126">65</span><span class="sxs-lookup"><span data-stu-id="324df-126">65</span></span>

<span data-ttu-id="324df-127">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="324df-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="324df-128">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="324df-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="324df-129">66</span><span class="sxs-lookup"><span data-stu-id="324df-129">66</span></span>

<span data-ttu-id="324df-130">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="324df-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="324df-131">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="324df-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="324df-132">67</span><span class="sxs-lookup"><span data-stu-id="324df-132">67</span></span>

<span data-ttu-id="324df-133">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="324df-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="324df-134">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="324df-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="324df-135">68</span><span class="sxs-lookup"><span data-stu-id="324df-135">68</span></span>

<span data-ttu-id="324df-136">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="324df-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="324df-137">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="324df-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="324df-138">69</span><span class="sxs-lookup"><span data-stu-id="324df-138">69</span></span>

<span data-ttu-id="324df-139">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="324df-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="324df-140">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="324df-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="324df-141">70</span><span class="sxs-lookup"><span data-stu-id="324df-141">70</span></span>

<span data-ttu-id="324df-142">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="324df-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="324df-143">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="324df-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="324df-144">71</span><span class="sxs-lookup"><span data-stu-id="324df-144">71</span></span>

<span data-ttu-id="324df-145">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="324df-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="324df-146">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="324df-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="324df-147">72</span><span class="sxs-lookup"><span data-stu-id="324df-147">72</span></span>

<span data-ttu-id="324df-148">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="324df-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="324df-149">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="324df-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="324df-150">73</span><span class="sxs-lookup"><span data-stu-id="324df-150">73</span></span>

<span data-ttu-id="324df-151">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="324df-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="324df-152">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="324df-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="324df-153">74</span><span class="sxs-lookup"><span data-stu-id="324df-153">74</span></span>

<span data-ttu-id="324df-154">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="324df-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="324df-155">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="324df-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="324df-156">75</span><span class="sxs-lookup"><span data-stu-id="324df-156">75</span></span>

<span data-ttu-id="324df-157">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="324df-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="324df-158">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="324df-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="324df-159">76</span><span class="sxs-lookup"><span data-stu-id="324df-159">76</span></span>

<span data-ttu-id="324df-160">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="324df-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="324df-161">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="324df-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="324df-162">77</span><span class="sxs-lookup"><span data-stu-id="324df-162">77</span></span>

<span data-ttu-id="324df-163">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="324df-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="324df-164">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="324df-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="324df-165">78</span><span class="sxs-lookup"><span data-stu-id="324df-165">78</span></span>

<span data-ttu-id="324df-166">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="324df-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="324df-167">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="324df-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="324df-168">79</span><span class="sxs-lookup"><span data-stu-id="324df-168">79</span></span>

<span data-ttu-id="324df-169">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="324df-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="324df-170">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="324df-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="324df-171">80</span><span class="sxs-lookup"><span data-stu-id="324df-171">80</span></span>

<span data-ttu-id="324df-172">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="324df-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="324df-173">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="324df-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="324df-174">81</span><span class="sxs-lookup"><span data-stu-id="324df-174">81</span></span>

<span data-ttu-id="324df-175">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="324df-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="324df-176">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="324df-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="324df-177">82</span><span class="sxs-lookup"><span data-stu-id="324df-177">82</span></span>

<span data-ttu-id="324df-178">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="324df-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="324df-179">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="324df-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="324df-180">83</span><span class="sxs-lookup"><span data-stu-id="324df-180">83</span></span>

<span data-ttu-id="324df-181">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="324df-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="324df-182">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="324df-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="324df-183">84</span><span class="sxs-lookup"><span data-stu-id="324df-183">84</span></span>

<span data-ttu-id="324df-184">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="324df-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="324df-185">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="324df-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="324df-186">85</span><span class="sxs-lookup"><span data-stu-id="324df-186">85</span></span>

<span data-ttu-id="324df-187">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="324df-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="324df-188">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="324df-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="324df-189">86</span><span class="sxs-lookup"><span data-stu-id="324df-189">86</span></span>

<span data-ttu-id="324df-190">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="324df-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="324df-191">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="324df-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="324df-192">87</span><span class="sxs-lookup"><span data-stu-id="324df-192">87</span></span>

<span data-ttu-id="324df-193">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="324df-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="324df-194">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="324df-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="324df-195">88</span><span class="sxs-lookup"><span data-stu-id="324df-195">88</span></span>

<span data-ttu-id="324df-196">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="324df-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="324df-197">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="324df-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="324df-198">89</span><span class="sxs-lookup"><span data-stu-id="324df-198">89</span></span>

<span data-ttu-id="324df-199">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="324df-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="324df-200">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="324df-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="324df-201">90</span><span class="sxs-lookup"><span data-stu-id="324df-201">90</span></span>

<span data-ttu-id="324df-202">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="324df-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="324df-203">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="324df-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="324df-204">91</span><span class="sxs-lookup"><span data-stu-id="324df-204">91</span></span>

<span data-ttu-id="324df-205">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="324df-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="324df-206">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="324df-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="324df-207">92</span><span class="sxs-lookup"><span data-stu-id="324df-207">92</span></span>

<span data-ttu-id="324df-208">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="324df-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="324df-209">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="324df-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="324df-210">93</span><span class="sxs-lookup"><span data-stu-id="324df-210">93</span></span>

<span data-ttu-id="324df-211">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="324df-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="324df-212">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="324df-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="324df-213">94</span><span class="sxs-lookup"><span data-stu-id="324df-213">94</span></span>

<span data-ttu-id="324df-214">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="324df-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="324df-215">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="324df-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="324df-216">95</span><span class="sxs-lookup"><span data-stu-id="324df-216">95</span></span>

<span data-ttu-id="324df-217">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="324df-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="324df-218">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="324df-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="324df-219">96</span><span class="sxs-lookup"><span data-stu-id="324df-219">96</span></span>

<span data-ttu-id="324df-220">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="324df-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="324df-221">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="324df-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="324df-222">97</span><span class="sxs-lookup"><span data-stu-id="324df-222">97</span></span>

<span data-ttu-id="324df-223">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="324df-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="324df-224">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="324df-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="324df-225">98</span><span class="sxs-lookup"><span data-stu-id="324df-225">98</span></span>

<span data-ttu-id="324df-226">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="324df-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="324df-227">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="324df-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="324df-228">100</span><span class="sxs-lookup"><span data-stu-id="324df-228">100</span></span>

<span data-ttu-id="324df-229">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="324df-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="324df-230">**Другое**</span><span class="sxs-lookup"><span data-stu-id="324df-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="324df-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="324df-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="324df-232">Комментарии</span><span class="sxs-lookup"><span data-stu-id="324df-232">Remarks</span></span>

<span data-ttu-id="324df-233">RFC 1122 и BSD рассматривает срочный указатель в заголовке TCP и длину срочных данных по-разному.</span><span class="sxs-lookup"><span data-stu-id="324df-233">RFC 1122 and BSD interpret the urgent pointer in the TCP header and the length of the urgent data differently.</span></span> <span data-ttu-id="324df-234">Они не совместимы.</span><span class="sxs-lookup"><span data-stu-id="324df-234">They are not interoperable.</span></span> <span data-ttu-id="324df-235">По умолчанию используется режим BSD.</span><span class="sxs-lookup"><span data-stu-id="324df-235">The default is BSD mode.</span></span>

## <a name="examples"></a><span data-ttu-id="324df-236">Примеры</span><span class="sxs-lookup"><span data-stu-id="324df-236">Examples</span></span>

<span data-ttu-id="324df-237">Пример " [изменение несрочного указателя" для всех сетевых адаптеров](https://Gallery.TechNet.Microsoft.Com/0ff22a90-0be6-4914-8db7-aaf72cbea9cb) на языке VBScript настраивает компьютер для использования спецификации RFC 1122 для срочных данных.</span><span class="sxs-lookup"><span data-stu-id="324df-237">The [Modify Urgent Pointer Use for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/0ff22a90-0be6-4914-8db7-aaf72cbea9cb) VBScript sample configures a computer to use the RFC 1122 specification for urgent data.</span></span>

## <a name="requirements"></a><span data-ttu-id="324df-238">Требования</span><span class="sxs-lookup"><span data-stu-id="324df-238">Requirements</span></span>



| <span data-ttu-id="324df-239">Требование</span><span class="sxs-lookup"><span data-stu-id="324df-239">Requirement</span></span> | <span data-ttu-id="324df-240">Значение</span><span class="sxs-lookup"><span data-stu-id="324df-240">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="324df-241">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="324df-241">Minimum supported client</span></span><br/> | <span data-ttu-id="324df-242">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="324df-242">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="324df-243">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="324df-243">Minimum supported server</span></span><br/> | <span data-ttu-id="324df-244">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="324df-244">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="324df-245">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="324df-245">Namespace</span></span><br/>                | <span data-ttu-id="324df-246">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="324df-246">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="324df-247">MOF</span><span class="sxs-lookup"><span data-stu-id="324df-247">MOF</span></span><br/>                      | <dl> <span data-ttu-id="324df-248"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="324df-248"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="324df-249">DLL</span><span class="sxs-lookup"><span data-stu-id="324df-249">DLL</span></span><br/>                      | <dl> <span data-ttu-id="324df-250"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="324df-250"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="324df-251">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="324df-251">See also</span></span>

<dl> <dt>

[<span data-ttu-id="324df-252">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="324df-252">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="324df-253">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="324df-253">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="324df-254">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="324df-254">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="324df-255">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="324df-255">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="324df-256">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="324df-256">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

