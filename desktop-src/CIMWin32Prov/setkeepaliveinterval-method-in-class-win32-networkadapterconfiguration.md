---
description: Статический метод класса Сеткипаливеинтервал WMI используется для установки интервала повторных попыток поддержания активности, пока не будет получен ответ.
ms.assetid: 83415000-124a-44a7-93cc-92ce9df143aa
ms.tgt_platform: multiple
title: Метод Сеткипаливеинтервал класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetKeepAliveInterval
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2ce6a1491fd9e414f503d0165216794c67db0e97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141866"
---
# <a name="setkeepaliveinterval-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="0fad3-103">Метод Сеткипаливеинтервал \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="0fad3-103">SetKeepAliveInterval method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="0fad3-104">Статический метод класса **сеткипаливеинтервал** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) используется для установки интервала повторных попыток поддержания активности, пока не будет получен ответ.</span><span class="sxs-lookup"><span data-stu-id="0fad3-104">The **SetKeepAliveInterval** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the interval separating Keep Alive Retransmissions until a response is received.</span></span>

<span data-ttu-id="0fad3-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="0fad3-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0fad3-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0fad3-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0fad3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0fad3-107">Syntax</span></span>


```mof
uint32 SetKeepAliveInterval(
  [in] uint32 KeepAliveInterval
);
```



## <a name="parameters"></a><span data-ttu-id="0fad3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0fad3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fad3-109">*KeepAliveInterval* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0fad3-109">*KeepAliveInterval* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-110">Значение, в миллисекундах, для интервала, в течение которого выполняется повторная передача проверки активности до получения ответа.</span><span class="sxs-lookup"><span data-stu-id="0fad3-110">Value, in milliseconds, for the interval separating Keep Alive Retransmissions until a response is received.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fad3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0fad3-111">Return value</span></span>

<span data-ttu-id="0fad3-112">Возвращает значение 0 (ноль) для успешного завершения, если не требуется перезагрузка, 1 (один) для успешного завершения, когда требуется перезагрузка, и другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="0fad3-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="0fad3-113">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="0fad3-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="0fad3-114">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="0fad3-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="0fad3-115">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="0fad3-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-116">0</span><span class="sxs-lookup"><span data-stu-id="0fad3-116">0</span></span>

<span data-ttu-id="0fad3-117">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="0fad3-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-118">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="0fad3-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-119">1</span><span class="sxs-lookup"><span data-stu-id="0fad3-119">1</span></span>

<span data-ttu-id="0fad3-120">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="0fad3-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-121">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="0fad3-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-122">64</span><span class="sxs-lookup"><span data-stu-id="0fad3-122">64</span></span>

<span data-ttu-id="0fad3-123">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="0fad3-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-124">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="0fad3-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-125">65</span><span class="sxs-lookup"><span data-stu-id="0fad3-125">65</span></span>

<span data-ttu-id="0fad3-126">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="0fad3-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-127">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="0fad3-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-128">66</span><span class="sxs-lookup"><span data-stu-id="0fad3-128">66</span></span>

<span data-ttu-id="0fad3-129">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="0fad3-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-130">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="0fad3-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-131">67</span><span class="sxs-lookup"><span data-stu-id="0fad3-131">67</span></span>

<span data-ttu-id="0fad3-132">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="0fad3-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-133">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="0fad3-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-134">68</span><span class="sxs-lookup"><span data-stu-id="0fad3-134">68</span></span>

<span data-ttu-id="0fad3-135">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="0fad3-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-136">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="0fad3-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-137">69</span><span class="sxs-lookup"><span data-stu-id="0fad3-137">69</span></span>

<span data-ttu-id="0fad3-138">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="0fad3-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-139">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="0fad3-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-140">70</span><span class="sxs-lookup"><span data-stu-id="0fad3-140">70</span></span>

<span data-ttu-id="0fad3-141">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="0fad3-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-142">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="0fad3-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-143">71</span><span class="sxs-lookup"><span data-stu-id="0fad3-143">71</span></span>

<span data-ttu-id="0fad3-144">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="0fad3-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-145">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="0fad3-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-146">72</span><span class="sxs-lookup"><span data-stu-id="0fad3-146">72</span></span>

<span data-ttu-id="0fad3-147">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="0fad3-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-148">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="0fad3-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-149">73</span><span class="sxs-lookup"><span data-stu-id="0fad3-149">73</span></span>

<span data-ttu-id="0fad3-150">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="0fad3-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-151">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="0fad3-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-152">74</span><span class="sxs-lookup"><span data-stu-id="0fad3-152">74</span></span>

<span data-ttu-id="0fad3-153">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="0fad3-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-154">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="0fad3-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-155">75</span><span class="sxs-lookup"><span data-stu-id="0fad3-155">75</span></span>

<span data-ttu-id="0fad3-156">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="0fad3-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-157">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="0fad3-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-158">76</span><span class="sxs-lookup"><span data-stu-id="0fad3-158">76</span></span>

<span data-ttu-id="0fad3-159">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="0fad3-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-160">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="0fad3-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-161">77</span><span class="sxs-lookup"><span data-stu-id="0fad3-161">77</span></span>

<span data-ttu-id="0fad3-162">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="0fad3-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-163">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="0fad3-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-164">78</span><span class="sxs-lookup"><span data-stu-id="0fad3-164">78</span></span>

<span data-ttu-id="0fad3-165">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="0fad3-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-166">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="0fad3-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-167">79</span><span class="sxs-lookup"><span data-stu-id="0fad3-167">79</span></span>

<span data-ttu-id="0fad3-168">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="0fad3-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-169">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="0fad3-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-170">80</span><span class="sxs-lookup"><span data-stu-id="0fad3-170">80</span></span>

<span data-ttu-id="0fad3-171">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="0fad3-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-172">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="0fad3-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-173">81</span><span class="sxs-lookup"><span data-stu-id="0fad3-173">81</span></span>

<span data-ttu-id="0fad3-174">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="0fad3-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-175">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="0fad3-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-176">82</span><span class="sxs-lookup"><span data-stu-id="0fad3-176">82</span></span>

<span data-ttu-id="0fad3-177">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="0fad3-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-178">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="0fad3-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-179">83</span><span class="sxs-lookup"><span data-stu-id="0fad3-179">83</span></span>

<span data-ttu-id="0fad3-180">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="0fad3-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-181">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="0fad3-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-182">84</span><span class="sxs-lookup"><span data-stu-id="0fad3-182">84</span></span>

<span data-ttu-id="0fad3-183">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="0fad3-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-184">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="0fad3-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-185">85</span><span class="sxs-lookup"><span data-stu-id="0fad3-185">85</span></span>

<span data-ttu-id="0fad3-186">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="0fad3-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-187">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="0fad3-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-188">86</span><span class="sxs-lookup"><span data-stu-id="0fad3-188">86</span></span>

<span data-ttu-id="0fad3-189">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="0fad3-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-190">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="0fad3-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-191">87</span><span class="sxs-lookup"><span data-stu-id="0fad3-191">87</span></span>

<span data-ttu-id="0fad3-192">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="0fad3-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-193">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="0fad3-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-194">88</span><span class="sxs-lookup"><span data-stu-id="0fad3-194">88</span></span>

<span data-ttu-id="0fad3-195">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="0fad3-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-196">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="0fad3-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-197">89</span><span class="sxs-lookup"><span data-stu-id="0fad3-197">89</span></span>

<span data-ttu-id="0fad3-198">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="0fad3-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-199">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="0fad3-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-200">90</span><span class="sxs-lookup"><span data-stu-id="0fad3-200">90</span></span>

<span data-ttu-id="0fad3-201">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="0fad3-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-202">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="0fad3-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-203">91</span><span class="sxs-lookup"><span data-stu-id="0fad3-203">91</span></span>

<span data-ttu-id="0fad3-204">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="0fad3-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-205">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="0fad3-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-206">92</span><span class="sxs-lookup"><span data-stu-id="0fad3-206">92</span></span>

<span data-ttu-id="0fad3-207">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="0fad3-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-208">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="0fad3-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-209">93</span><span class="sxs-lookup"><span data-stu-id="0fad3-209">93</span></span>

<span data-ttu-id="0fad3-210">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="0fad3-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-211">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="0fad3-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-212">94</span><span class="sxs-lookup"><span data-stu-id="0fad3-212">94</span></span>

<span data-ttu-id="0fad3-213">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="0fad3-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-214">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="0fad3-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-215">95</span><span class="sxs-lookup"><span data-stu-id="0fad3-215">95</span></span>

<span data-ttu-id="0fad3-216">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="0fad3-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-217">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="0fad3-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-218">96</span><span class="sxs-lookup"><span data-stu-id="0fad3-218">96</span></span>

<span data-ttu-id="0fad3-219">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="0fad3-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-220">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="0fad3-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-221">97</span><span class="sxs-lookup"><span data-stu-id="0fad3-221">97</span></span>

<span data-ttu-id="0fad3-222">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="0fad3-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-223">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="0fad3-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-224">98</span><span class="sxs-lookup"><span data-stu-id="0fad3-224">98</span></span>

<span data-ttu-id="0fad3-225">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="0fad3-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-226">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="0fad3-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-227">100</span><span class="sxs-lookup"><span data-stu-id="0fad3-227">100</span></span>

<span data-ttu-id="0fad3-228">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="0fad3-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="0fad3-229">**Другое**</span><span class="sxs-lookup"><span data-stu-id="0fad3-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="0fad3-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="0fad3-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0fad3-231">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0fad3-231">Remarks</span></span>

<span data-ttu-id="0fad3-232">После получения ответа задержка до следующей передачи активности продолжает управляться значением свойства [**KeepAliveTime**](win32-networkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="0fad3-232">After a response is received, the delay until the next Keep Alive Transmission is again controlled by the value of the [**KeepAliveTime**](win32-networkadapterconfiguration.md) property.</span></span> <span data-ttu-id="0fad3-233">Соединение прерывается после того, как число повторных передач, указанных свойством **TcpMaxDataRetransmissions** , не было получено.</span><span class="sxs-lookup"><span data-stu-id="0fad3-233">The connection is terminated after the number of retransmissions specified by the **TcpMaxDataRetransmissions** property have gone unanswered</span></span>

## <a name="examples"></a><span data-ttu-id="0fad3-234">Примеры</span><span class="sxs-lookup"><span data-stu-id="0fad3-234">Examples</span></span>

<span data-ttu-id="0fad3-235">Пример [изменения интервала проверки активности для всех сетевых адаптеров](https://Gallery.TechNet.Microsoft.Com/f6d4a0e7-5b59-42e3-888d-82a028e2bf35) VBScript настраивает интервал проверки активности для всех сетевых адаптеров на компьютере равным 300, 00 миллисекундам (5 минутам).</span><span class="sxs-lookup"><span data-stu-id="0fad3-235">The [Modify the Keep Alive Interval for all Network Adapters](https://Gallery.TechNet.Microsoft.Com/f6d4a0e7-5b59-42e3-888d-82a028e2bf35) VBScript sample configures the keep alive interval for all network adapters on a computer to 300,00 milliseconds (5 minutes).</span></span>

## <a name="requirements"></a><span data-ttu-id="0fad3-236">Требования</span><span class="sxs-lookup"><span data-stu-id="0fad3-236">Requirements</span></span>



| <span data-ttu-id="0fad3-237">Требование</span><span class="sxs-lookup"><span data-stu-id="0fad3-237">Requirement</span></span> | <span data-ttu-id="0fad3-238">Значение</span><span class="sxs-lookup"><span data-stu-id="0fad3-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fad3-239">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0fad3-239">Minimum supported client</span></span><br/> | <span data-ttu-id="0fad3-240">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0fad3-240">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0fad3-241">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0fad3-241">Minimum supported server</span></span><br/> | <span data-ttu-id="0fad3-242">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0fad3-242">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0fad3-243">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0fad3-243">Namespace</span></span><br/>                | <span data-ttu-id="0fad3-244">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0fad3-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0fad3-245">MOF</span><span class="sxs-lookup"><span data-stu-id="0fad3-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0fad3-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0fad3-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0fad3-247">DLL</span><span class="sxs-lookup"><span data-stu-id="0fad3-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fad3-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fad3-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fad3-249">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0fad3-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fad3-250">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="0fad3-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="0fad3-251">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="0fad3-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="0fad3-252">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="0fad3-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="0fad3-253">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="0fad3-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="0fad3-254">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="0fad3-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

