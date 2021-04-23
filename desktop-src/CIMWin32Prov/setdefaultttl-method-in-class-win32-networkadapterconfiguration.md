---
description: Статический метод класса Сетдефаултттл WMI используется для установки значения срока жизни (TTL) по умолчанию в заголовке исходящих пакетов IP.
ms.assetid: 74b060de-512c-407e-9f93-c3b496f8d09d
ms.tgt_platform: multiple
title: Метод Сетдефаултттл класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDefaultTTL
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 253048b44a836f92646124fb972fe32c135e3b9a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895321"
---
# <a name="setdefaultttl-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="a7ae3-103">Метод Сетдефаултттл \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7ae3-103">SetDefaultTTL method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="a7ae3-104">Статический метод класса **сетдефаултттл** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) используется для установки значения срока жизни (TTL) по умолчанию в заголовке исходящих пакетов IP.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-104">The **SetDefaultTTL** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the default Time to Live (TTL) value in the header of outgoing IP packets.</span></span>

<span data-ttu-id="a7ae3-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="a7ae3-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a7ae3-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a7ae3-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a7ae3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7ae3-107">Syntax</span></span>


```mof
uint32 SetDefaultTTL(
  [in] uint8 DefaultTTL
);
```



## <a name="parameters"></a><span data-ttu-id="a7ae3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7ae3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7ae3-109">*DefaultTTL* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a7ae3-109">*DefaultTTL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-110">Значение срока жизни, заданное в заголовке исходящих IP-пакетов.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-110">Time to Live value set in the header of outgoing IP packets.</span></span> <span data-ttu-id="a7ae3-111">Значение по умолчанию — 32; Допустимый диапазон: 1-255</span><span class="sxs-lookup"><span data-stu-id="a7ae3-111">The default value is 32; Valid range: 1 - 255</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7ae3-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a7ae3-112">Return value</span></span>

<span data-ttu-id="a7ae3-113">Возвращает значение 0 (ноль) для успешного завершения, если не требуется перезагрузка, 1 (один) для успешного завершения, когда требуется перезагрузка, и другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="a7ae3-114">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="a7ae3-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="a7ae3-115">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="a7ae3-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="a7ae3-116">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-117">0</span><span class="sxs-lookup"><span data-stu-id="a7ae3-117">0</span></span>

<span data-ttu-id="a7ae3-118">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-119">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-120">1</span><span class="sxs-lookup"><span data-stu-id="a7ae3-120">1</span></span>

<span data-ttu-id="a7ae3-121">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-122">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-123">64</span><span class="sxs-lookup"><span data-stu-id="a7ae3-123">64</span></span>

<span data-ttu-id="a7ae3-124">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-125">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-126">65</span><span class="sxs-lookup"><span data-stu-id="a7ae3-126">65</span></span>

<span data-ttu-id="a7ae3-127">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-128">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-129">66</span><span class="sxs-lookup"><span data-stu-id="a7ae3-129">66</span></span>

<span data-ttu-id="a7ae3-130">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-131">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-132">67</span><span class="sxs-lookup"><span data-stu-id="a7ae3-132">67</span></span>

<span data-ttu-id="a7ae3-133">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-134">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-135">68</span><span class="sxs-lookup"><span data-stu-id="a7ae3-135">68</span></span>

<span data-ttu-id="a7ae3-136">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-137">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-138">69</span><span class="sxs-lookup"><span data-stu-id="a7ae3-138">69</span></span>

<span data-ttu-id="a7ae3-139">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-140">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-141">70</span><span class="sxs-lookup"><span data-stu-id="a7ae3-141">70</span></span>

<span data-ttu-id="a7ae3-142">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-143">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-144">71</span><span class="sxs-lookup"><span data-stu-id="a7ae3-144">71</span></span>

<span data-ttu-id="a7ae3-145">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-146">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-147">72</span><span class="sxs-lookup"><span data-stu-id="a7ae3-147">72</span></span>

<span data-ttu-id="a7ae3-148">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-149">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-150">73</span><span class="sxs-lookup"><span data-stu-id="a7ae3-150">73</span></span>

<span data-ttu-id="a7ae3-151">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-152">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-153">74</span><span class="sxs-lookup"><span data-stu-id="a7ae3-153">74</span></span>

<span data-ttu-id="a7ae3-154">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-155">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-156">75</span><span class="sxs-lookup"><span data-stu-id="a7ae3-156">75</span></span>

<span data-ttu-id="a7ae3-157">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-158">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-159">76</span><span class="sxs-lookup"><span data-stu-id="a7ae3-159">76</span></span>

<span data-ttu-id="a7ae3-160">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-161">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-162">77</span><span class="sxs-lookup"><span data-stu-id="a7ae3-162">77</span></span>

<span data-ttu-id="a7ae3-163">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-164">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-165">78</span><span class="sxs-lookup"><span data-stu-id="a7ae3-165">78</span></span>

<span data-ttu-id="a7ae3-166">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-167">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-168">79</span><span class="sxs-lookup"><span data-stu-id="a7ae3-168">79</span></span>

<span data-ttu-id="a7ae3-169">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-170">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-171">80</span><span class="sxs-lookup"><span data-stu-id="a7ae3-171">80</span></span>

<span data-ttu-id="a7ae3-172">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-173">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-174">81</span><span class="sxs-lookup"><span data-stu-id="a7ae3-174">81</span></span>

<span data-ttu-id="a7ae3-175">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-176">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-177">82</span><span class="sxs-lookup"><span data-stu-id="a7ae3-177">82</span></span>

<span data-ttu-id="a7ae3-178">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-179">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-180">83</span><span class="sxs-lookup"><span data-stu-id="a7ae3-180">83</span></span>

<span data-ttu-id="a7ae3-181">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-182">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-183">84</span><span class="sxs-lookup"><span data-stu-id="a7ae3-183">84</span></span>

<span data-ttu-id="a7ae3-184">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-185">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-186">85</span><span class="sxs-lookup"><span data-stu-id="a7ae3-186">85</span></span>

<span data-ttu-id="a7ae3-187">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-188">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-189">86</span><span class="sxs-lookup"><span data-stu-id="a7ae3-189">86</span></span>

<span data-ttu-id="a7ae3-190">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-191">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-192">87</span><span class="sxs-lookup"><span data-stu-id="a7ae3-192">87</span></span>

<span data-ttu-id="a7ae3-193">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-194">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-195">88</span><span class="sxs-lookup"><span data-stu-id="a7ae3-195">88</span></span>

<span data-ttu-id="a7ae3-196">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-197">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-198">89</span><span class="sxs-lookup"><span data-stu-id="a7ae3-198">89</span></span>

<span data-ttu-id="a7ae3-199">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-200">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-201">90</span><span class="sxs-lookup"><span data-stu-id="a7ae3-201">90</span></span>

<span data-ttu-id="a7ae3-202">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-203">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-204">91</span><span class="sxs-lookup"><span data-stu-id="a7ae3-204">91</span></span>

<span data-ttu-id="a7ae3-205">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-206">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-207">92</span><span class="sxs-lookup"><span data-stu-id="a7ae3-207">92</span></span>

<span data-ttu-id="a7ae3-208">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-209">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-210">93</span><span class="sxs-lookup"><span data-stu-id="a7ae3-210">93</span></span>

<span data-ttu-id="a7ae3-211">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-212">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-213">94</span><span class="sxs-lookup"><span data-stu-id="a7ae3-213">94</span></span>

<span data-ttu-id="a7ae3-214">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-215">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-216">95</span><span class="sxs-lookup"><span data-stu-id="a7ae3-216">95</span></span>

<span data-ttu-id="a7ae3-217">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-218">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-219">96</span><span class="sxs-lookup"><span data-stu-id="a7ae3-219">96</span></span>

<span data-ttu-id="a7ae3-220">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-221">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-222">97</span><span class="sxs-lookup"><span data-stu-id="a7ae3-222">97</span></span>

<span data-ttu-id="a7ae3-223">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-224">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-225">98</span><span class="sxs-lookup"><span data-stu-id="a7ae3-225">98</span></span>

<span data-ttu-id="a7ae3-226">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-227">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-228">100</span><span class="sxs-lookup"><span data-stu-id="a7ae3-228">100</span></span>

<span data-ttu-id="a7ae3-229">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="a7ae3-230">**Другое**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="a7ae3-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="a7ae3-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7ae3-232">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a7ae3-232">Remarks</span></span>

<span data-ttu-id="a7ae3-233">TTL указывает число маршрутизаторов, через которые может пройти IP-пакет, чтобы достичь его назначения, прежде чем будет удалено.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-233">The TTL specifies the number of routers an IP packet may pass through to reach its destination before being discarded.</span></span> <span data-ttu-id="a7ae3-234">Каждый маршрутизатор уменьшает число TTL пакета на единицу и отбрасывает пакеты с TTL 0 (нулем).</span><span class="sxs-lookup"><span data-stu-id="a7ae3-234">Each router decrements the TTL count of a packet by one and discards the packets with a TTL of 0 (zero).</span></span>

## <a name="examples"></a><span data-ttu-id="a7ae3-235">Примеры</span><span class="sxs-lookup"><span data-stu-id="a7ae3-235">Examples</span></span>

<span data-ttu-id="a7ae3-236">В примере [изменения срока жизни по умолчанию для всех сетевых адаптеров](https://Gallery.TechNet.Microsoft.Com/scriptcenter/3a228fb8-5517-4e23-800e-2a15f427d05d) VBScript используется **сетдефаултттл** , чтобы установить значение срока жизни по умолчанию в заголовке исходящих пакетов IP равным 64.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-236">The [Modify the Default Time-to-Live for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/scriptcenter/3a228fb8-5517-4e23-800e-2a15f427d05d) VBScript sample uses **SetDefaultTTL** to set the default time-to-live value in the header of outgoing IP packets to 64</span></span>

## <a name="requirements"></a><span data-ttu-id="a7ae3-237">Требования</span><span class="sxs-lookup"><span data-stu-id="a7ae3-237">Requirements</span></span>



| <span data-ttu-id="a7ae3-238">Требование</span><span class="sxs-lookup"><span data-stu-id="a7ae3-238">Requirement</span></span> | <span data-ttu-id="a7ae3-239">Значение</span><span class="sxs-lookup"><span data-stu-id="a7ae3-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7ae3-240">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a7ae3-240">Minimum supported client</span></span><br/> | <span data-ttu-id="a7ae3-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a7ae3-241">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a7ae3-242">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a7ae3-242">Minimum supported server</span></span><br/> | <span data-ttu-id="a7ae3-243">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7ae3-243">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a7ae3-244">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a7ae3-244">Namespace</span></span><br/>                | <span data-ttu-id="a7ae3-245">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a7ae3-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a7ae3-246">MOF</span><span class="sxs-lookup"><span data-stu-id="a7ae3-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a7ae3-247"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a7ae3-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a7ae3-248">DLL</span><span class="sxs-lookup"><span data-stu-id="a7ae3-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7ae3-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7ae3-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7ae3-250">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7ae3-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7ae3-251">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="a7ae3-251">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="a7ae3-252">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="a7ae3-252">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="a7ae3-253">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="a7ae3-253">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="a7ae3-254">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="a7ae3-254">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="a7ae3-255">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="a7ae3-255">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

