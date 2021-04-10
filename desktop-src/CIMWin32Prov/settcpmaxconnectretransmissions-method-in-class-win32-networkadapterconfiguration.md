---
description: Статический метод класса Сетткпмаксконнектретрансмиссионс WMI используется для задания числа попыток, которые TCP будет повторно передавать запрос на подключение перед прерыванием.
ms.assetid: cb0dfba3-4ef5-4052-94f3-f688a1c55d90
ms.tgt_platform: multiple
title: Метод Сетткпмаксконнектретрансмиссионс класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpMaxConnectRetransmissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 160d84c2a466bff34070a6dec4a34804d5a3a7fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142874"
---
# <a name="settcpmaxconnectretransmissions-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="8cacc-103">Метод Сетткпмаксконнектретрансмиссионс \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="8cacc-103">SetTcpMaxConnectRetransmissions method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="8cacc-104">Статический метод класса **сетткпмаксконнектретрансмиссионс** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) используется для задания числа попыток, которые TCP будет повторно передавать запрос на подключение перед прерыванием.</span><span class="sxs-lookup"><span data-stu-id="8cacc-104">The **SetTcpMaxConnectRetransmissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the number of attempts TCP will retransmit a connect request before aborting.</span></span>

<span data-ttu-id="8cacc-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="8cacc-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8cacc-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8cacc-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8cacc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8cacc-107">Syntax</span></span>


```mof
uint32 SetTcpMaxConnectRetransmissions(
  [in] uint32 TcpMaxConnectRetransmissions
);
```



## <a name="parameters"></a><span data-ttu-id="8cacc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8cacc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cacc-109">*Ткпмаксконнектретрансмиссионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8cacc-109">*TcpMaxConnectRetransmissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-110">Число попыток, по истечении которых TCP будет повторно передавать запрос на подключение.</span><span class="sxs-lookup"><span data-stu-id="8cacc-110">Number of attempts TCP will retransmit a connect request before aborting.</span></span> <span data-ttu-id="8cacc-111">Допустимый диапазон значений — 0 – 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="8cacc-111">The valid range for values is 0 - 0xFFFFFFFF.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cacc-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8cacc-112">Return value</span></span>

<span data-ttu-id="8cacc-113">Возвращает значение 0 (ноль) для успешного завершения, если не требуется перезагрузка, 1 (один) для успешного завершения, когда требуется перезагрузка, и другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="8cacc-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="8cacc-114">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="8cacc-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="8cacc-115">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="8cacc-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="8cacc-116">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="8cacc-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-117">0</span><span class="sxs-lookup"><span data-stu-id="8cacc-117">0</span></span>

<span data-ttu-id="8cacc-118">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="8cacc-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-119">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="8cacc-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-120">1</span><span class="sxs-lookup"><span data-stu-id="8cacc-120">1</span></span>

<span data-ttu-id="8cacc-121">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="8cacc-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-122">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="8cacc-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-123">64</span><span class="sxs-lookup"><span data-stu-id="8cacc-123">64</span></span>

<span data-ttu-id="8cacc-124">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="8cacc-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-125">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="8cacc-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-126">65</span><span class="sxs-lookup"><span data-stu-id="8cacc-126">65</span></span>

<span data-ttu-id="8cacc-127">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="8cacc-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-128">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="8cacc-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-129">66</span><span class="sxs-lookup"><span data-stu-id="8cacc-129">66</span></span>

<span data-ttu-id="8cacc-130">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="8cacc-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-131">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="8cacc-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-132">67</span><span class="sxs-lookup"><span data-stu-id="8cacc-132">67</span></span>

<span data-ttu-id="8cacc-133">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8cacc-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-134">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="8cacc-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-135">68</span><span class="sxs-lookup"><span data-stu-id="8cacc-135">68</span></span>

<span data-ttu-id="8cacc-136">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="8cacc-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-137">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="8cacc-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-138">69</span><span class="sxs-lookup"><span data-stu-id="8cacc-138">69</span></span>

<span data-ttu-id="8cacc-139">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="8cacc-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-140">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="8cacc-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-141">70</span><span class="sxs-lookup"><span data-stu-id="8cacc-141">70</span></span>

<span data-ttu-id="8cacc-142">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="8cacc-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-143">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="8cacc-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-144">71</span><span class="sxs-lookup"><span data-stu-id="8cacc-144">71</span></span>

<span data-ttu-id="8cacc-145">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="8cacc-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-146">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="8cacc-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-147">72</span><span class="sxs-lookup"><span data-stu-id="8cacc-147">72</span></span>

<span data-ttu-id="8cacc-148">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="8cacc-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-149">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="8cacc-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-150">73</span><span class="sxs-lookup"><span data-stu-id="8cacc-150">73</span></span>

<span data-ttu-id="8cacc-151">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="8cacc-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-152">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="8cacc-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-153">74</span><span class="sxs-lookup"><span data-stu-id="8cacc-153">74</span></span>

<span data-ttu-id="8cacc-154">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="8cacc-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-155">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="8cacc-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-156">75</span><span class="sxs-lookup"><span data-stu-id="8cacc-156">75</span></span>

<span data-ttu-id="8cacc-157">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="8cacc-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-158">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="8cacc-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-159">76</span><span class="sxs-lookup"><span data-stu-id="8cacc-159">76</span></span>

<span data-ttu-id="8cacc-160">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="8cacc-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-161">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="8cacc-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-162">77</span><span class="sxs-lookup"><span data-stu-id="8cacc-162">77</span></span>

<span data-ttu-id="8cacc-163">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="8cacc-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-164">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="8cacc-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-165">78</span><span class="sxs-lookup"><span data-stu-id="8cacc-165">78</span></span>

<span data-ttu-id="8cacc-166">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="8cacc-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-167">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="8cacc-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-168">79</span><span class="sxs-lookup"><span data-stu-id="8cacc-168">79</span></span>

<span data-ttu-id="8cacc-169">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="8cacc-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-170">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="8cacc-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-171">80</span><span class="sxs-lookup"><span data-stu-id="8cacc-171">80</span></span>

<span data-ttu-id="8cacc-172">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="8cacc-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-173">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="8cacc-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-174">81</span><span class="sxs-lookup"><span data-stu-id="8cacc-174">81</span></span>

<span data-ttu-id="8cacc-175">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="8cacc-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-176">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="8cacc-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-177">82</span><span class="sxs-lookup"><span data-stu-id="8cacc-177">82</span></span>

<span data-ttu-id="8cacc-178">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="8cacc-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-179">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="8cacc-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-180">83</span><span class="sxs-lookup"><span data-stu-id="8cacc-180">83</span></span>

<span data-ttu-id="8cacc-181">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="8cacc-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-182">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="8cacc-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-183">84</span><span class="sxs-lookup"><span data-stu-id="8cacc-183">84</span></span>

<span data-ttu-id="8cacc-184">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="8cacc-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-185">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="8cacc-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-186">85</span><span class="sxs-lookup"><span data-stu-id="8cacc-186">85</span></span>

<span data-ttu-id="8cacc-187">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="8cacc-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-188">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="8cacc-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-189">86</span><span class="sxs-lookup"><span data-stu-id="8cacc-189">86</span></span>

<span data-ttu-id="8cacc-190">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="8cacc-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-191">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="8cacc-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-192">87</span><span class="sxs-lookup"><span data-stu-id="8cacc-192">87</span></span>

<span data-ttu-id="8cacc-193">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="8cacc-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-194">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="8cacc-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-195">88</span><span class="sxs-lookup"><span data-stu-id="8cacc-195">88</span></span>

<span data-ttu-id="8cacc-196">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="8cacc-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-197">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="8cacc-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-198">89</span><span class="sxs-lookup"><span data-stu-id="8cacc-198">89</span></span>

<span data-ttu-id="8cacc-199">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="8cacc-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-200">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="8cacc-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-201">90</span><span class="sxs-lookup"><span data-stu-id="8cacc-201">90</span></span>

<span data-ttu-id="8cacc-202">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="8cacc-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-203">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="8cacc-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-204">91</span><span class="sxs-lookup"><span data-stu-id="8cacc-204">91</span></span>

<span data-ttu-id="8cacc-205">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="8cacc-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-206">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="8cacc-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-207">92</span><span class="sxs-lookup"><span data-stu-id="8cacc-207">92</span></span>

<span data-ttu-id="8cacc-208">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="8cacc-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-209">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="8cacc-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-210">93</span><span class="sxs-lookup"><span data-stu-id="8cacc-210">93</span></span>

<span data-ttu-id="8cacc-211">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="8cacc-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-212">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="8cacc-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-213">94</span><span class="sxs-lookup"><span data-stu-id="8cacc-213">94</span></span>

<span data-ttu-id="8cacc-214">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="8cacc-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-215">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="8cacc-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-216">95</span><span class="sxs-lookup"><span data-stu-id="8cacc-216">95</span></span>

<span data-ttu-id="8cacc-217">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="8cacc-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-218">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="8cacc-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-219">96</span><span class="sxs-lookup"><span data-stu-id="8cacc-219">96</span></span>

<span data-ttu-id="8cacc-220">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="8cacc-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-221">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="8cacc-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-222">97</span><span class="sxs-lookup"><span data-stu-id="8cacc-222">97</span></span>

<span data-ttu-id="8cacc-223">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="8cacc-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-224">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="8cacc-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-225">98</span><span class="sxs-lookup"><span data-stu-id="8cacc-225">98</span></span>

<span data-ttu-id="8cacc-226">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="8cacc-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-227">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="8cacc-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-228">100</span><span class="sxs-lookup"><span data-stu-id="8cacc-228">100</span></span>

<span data-ttu-id="8cacc-229">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="8cacc-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8cacc-230">**Другое**</span><span class="sxs-lookup"><span data-stu-id="8cacc-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="8cacc-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="8cacc-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8cacc-232">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8cacc-232">Remarks</span></span>

<span data-ttu-id="8cacc-233">Начальное время ожидания повторной передачи составляет три секунды и удваивается для каждой последующей попытки.</span><span class="sxs-lookup"><span data-stu-id="8cacc-233">The initial retransmission timeout is three seconds, and doubles for each successive attempt.</span></span>

## <a name="examples"></a><span data-ttu-id="8cacc-234">Примеры</span><span class="sxs-lookup"><span data-stu-id="8cacc-234">Examples</span></span>

<span data-ttu-id="8cacc-235">Пример [изменения максимального разрешенного подключения TCP с повторными передачами](https://Gallery.TechNet.Microsoft.Com/e599c6bc-fa37-457d-b7e3-3c003517ed46) позволяет настроить число повторных попыток подключения TCP, прежде чем отказаться от усилий.</span><span class="sxs-lookup"><span data-stu-id="8cacc-235">The [Modify the Maximum Allowed TCP Connection Retransmissions](https://Gallery.TechNet.Microsoft.Com/e599c6bc-fa37-457d-b7e3-3c003517ed46) VBScript sample configures the number of times TCP will retransmit a connection attempt before abandoning the effort.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cacc-236">Требования</span><span class="sxs-lookup"><span data-stu-id="8cacc-236">Requirements</span></span>



| <span data-ttu-id="8cacc-237">Требование</span><span class="sxs-lookup"><span data-stu-id="8cacc-237">Requirement</span></span> | <span data-ttu-id="8cacc-238">Значение</span><span class="sxs-lookup"><span data-stu-id="8cacc-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8cacc-239">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8cacc-239">Minimum supported client</span></span><br/> | <span data-ttu-id="8cacc-240">Windows Vista, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8cacc-240">Windows Vista, Windows Vista</span></span><br/>                                                 |
| <span data-ttu-id="8cacc-241">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8cacc-241">Minimum supported server</span></span><br/> | <span data-ttu-id="8cacc-242">Windows Server 2008, Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8cacc-242">Windows Server 2008, Windows Server 2008</span></span><br/>                                     |
| <span data-ttu-id="8cacc-243">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8cacc-243">Namespace</span></span><br/>                | <span data-ttu-id="8cacc-244">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8cacc-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8cacc-245">MOF</span><span class="sxs-lookup"><span data-stu-id="8cacc-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8cacc-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8cacc-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8cacc-247">DLL</span><span class="sxs-lookup"><span data-stu-id="8cacc-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8cacc-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8cacc-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cacc-249">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8cacc-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cacc-250">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="8cacc-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="8cacc-251">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="8cacc-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="8cacc-252">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="8cacc-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="8cacc-253">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="8cacc-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="8cacc-254">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="8cacc-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

