---
description: Статический метод класса Сетткпмаксдатаретрансмиссионс WMI используется для задания числа раз, которое TCP повторно передает отдельный сегмент данных перед прерыванием соединения.
ms.assetid: 1b5407ee-8e2b-4aed-a17a-58d960f976f2
ms.tgt_platform: multiple
title: Метод Сетткпмаксдатаретрансмиссионс класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpMaxDataRetransmissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 59998888eb2aed170b626fb4cb61780cbe0cb6e4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142871"
---
# <a name="settcpmaxdataretransmissions-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="8f585-103">Метод Сетткпмаксдатаретрансмиссионс \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f585-103">SetTcpMaxDataRetransmissions method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="8f585-104">Статический метод класса **сетткпмаксдатаретрансмиссионс** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) используется для задания числа раз, которое TCP повторно передает отдельный сегмент данных перед прерыванием соединения.</span><span class="sxs-lookup"><span data-stu-id="8f585-104">The **SetTcpMaxDataRetransmissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the number of times TCP retransmits an individual data segment before aborting the connection.</span></span>

<span data-ttu-id="8f585-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="8f585-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8f585-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8f585-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8f585-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f585-107">Syntax</span></span>


```mof
uint32 SetTcpMaxDataRetransmissions(
  [in] uint32 TcpMaxDataRetransmissions
);
```



## <a name="parameters"></a><span data-ttu-id="8f585-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8f585-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f585-109">*TcpMaxDataRetransmissions* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8f585-109">*TcpMaxDataRetransmissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f585-110">Число раз, когда TCP пересылает отдельный сегмент данных перед прерыванием соединения.</span><span class="sxs-lookup"><span data-stu-id="8f585-110">Number of times TCP retransmits an individual data segment before aborting the connection.</span></span> <span data-ttu-id="8f585-111">Допустимый диапазон: 0 – 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="8f585-111">Valid range: 0 - 0xFFFFFFFF.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f585-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8f585-112">Return value</span></span>

<span data-ttu-id="8f585-113">Возвращает значение 0 (ноль) для успешного завершения, если не требуется перезагрузка, 1 (один) для успешного завершения, когда требуется перезагрузка, и другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="8f585-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="8f585-114">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="8f585-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="8f585-115">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="8f585-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="8f585-116">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="8f585-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-117">0</span><span class="sxs-lookup"><span data-stu-id="8f585-117">0</span></span>

<span data-ttu-id="8f585-118">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="8f585-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-119">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="8f585-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-120">1</span><span class="sxs-lookup"><span data-stu-id="8f585-120">1</span></span>

<span data-ttu-id="8f585-121">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="8f585-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-122">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="8f585-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-123">64</span><span class="sxs-lookup"><span data-stu-id="8f585-123">64</span></span>

<span data-ttu-id="8f585-124">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="8f585-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-125">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="8f585-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-126">65</span><span class="sxs-lookup"><span data-stu-id="8f585-126">65</span></span>

<span data-ttu-id="8f585-127">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="8f585-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-128">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="8f585-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-129">66</span><span class="sxs-lookup"><span data-stu-id="8f585-129">66</span></span>

<span data-ttu-id="8f585-130">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="8f585-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-131">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="8f585-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-132">67</span><span class="sxs-lookup"><span data-stu-id="8f585-132">67</span></span>

<span data-ttu-id="8f585-133">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8f585-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-134">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="8f585-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-135">68</span><span class="sxs-lookup"><span data-stu-id="8f585-135">68</span></span>

<span data-ttu-id="8f585-136">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="8f585-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-137">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="8f585-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-138">69</span><span class="sxs-lookup"><span data-stu-id="8f585-138">69</span></span>

<span data-ttu-id="8f585-139">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="8f585-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-140">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="8f585-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-141">70</span><span class="sxs-lookup"><span data-stu-id="8f585-141">70</span></span>

<span data-ttu-id="8f585-142">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="8f585-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-143">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="8f585-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-144">71</span><span class="sxs-lookup"><span data-stu-id="8f585-144">71</span></span>

<span data-ttu-id="8f585-145">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="8f585-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-146">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="8f585-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-147">72</span><span class="sxs-lookup"><span data-stu-id="8f585-147">72</span></span>

<span data-ttu-id="8f585-148">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="8f585-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-149">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="8f585-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-150">73</span><span class="sxs-lookup"><span data-stu-id="8f585-150">73</span></span>

<span data-ttu-id="8f585-151">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="8f585-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-152">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="8f585-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-153">74</span><span class="sxs-lookup"><span data-stu-id="8f585-153">74</span></span>

<span data-ttu-id="8f585-154">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="8f585-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-155">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="8f585-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-156">75</span><span class="sxs-lookup"><span data-stu-id="8f585-156">75</span></span>

<span data-ttu-id="8f585-157">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="8f585-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-158">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="8f585-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-159">76</span><span class="sxs-lookup"><span data-stu-id="8f585-159">76</span></span>

<span data-ttu-id="8f585-160">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="8f585-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-161">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="8f585-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-162">77</span><span class="sxs-lookup"><span data-stu-id="8f585-162">77</span></span>

<span data-ttu-id="8f585-163">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="8f585-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-164">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="8f585-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-165">78</span><span class="sxs-lookup"><span data-stu-id="8f585-165">78</span></span>

<span data-ttu-id="8f585-166">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="8f585-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-167">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="8f585-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-168">79</span><span class="sxs-lookup"><span data-stu-id="8f585-168">79</span></span>

<span data-ttu-id="8f585-169">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="8f585-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-170">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="8f585-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-171">80</span><span class="sxs-lookup"><span data-stu-id="8f585-171">80</span></span>

<span data-ttu-id="8f585-172">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="8f585-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-173">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="8f585-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-174">81</span><span class="sxs-lookup"><span data-stu-id="8f585-174">81</span></span>

<span data-ttu-id="8f585-175">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="8f585-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-176">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="8f585-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-177">82</span><span class="sxs-lookup"><span data-stu-id="8f585-177">82</span></span>

<span data-ttu-id="8f585-178">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="8f585-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-179">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="8f585-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-180">83</span><span class="sxs-lookup"><span data-stu-id="8f585-180">83</span></span>

<span data-ttu-id="8f585-181">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="8f585-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-182">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="8f585-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-183">84</span><span class="sxs-lookup"><span data-stu-id="8f585-183">84</span></span>

<span data-ttu-id="8f585-184">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="8f585-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-185">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="8f585-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-186">85</span><span class="sxs-lookup"><span data-stu-id="8f585-186">85</span></span>

<span data-ttu-id="8f585-187">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="8f585-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-188">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="8f585-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-189">86</span><span class="sxs-lookup"><span data-stu-id="8f585-189">86</span></span>

<span data-ttu-id="8f585-190">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="8f585-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-191">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="8f585-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-192">87</span><span class="sxs-lookup"><span data-stu-id="8f585-192">87</span></span>

<span data-ttu-id="8f585-193">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="8f585-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-194">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="8f585-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-195">88</span><span class="sxs-lookup"><span data-stu-id="8f585-195">88</span></span>

<span data-ttu-id="8f585-196">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="8f585-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-197">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="8f585-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-198">89</span><span class="sxs-lookup"><span data-stu-id="8f585-198">89</span></span>

<span data-ttu-id="8f585-199">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="8f585-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-200">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="8f585-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-201">90</span><span class="sxs-lookup"><span data-stu-id="8f585-201">90</span></span>

<span data-ttu-id="8f585-202">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="8f585-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-203">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="8f585-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-204">91</span><span class="sxs-lookup"><span data-stu-id="8f585-204">91</span></span>

<span data-ttu-id="8f585-205">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="8f585-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-206">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="8f585-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-207">92</span><span class="sxs-lookup"><span data-stu-id="8f585-207">92</span></span>

<span data-ttu-id="8f585-208">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="8f585-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-209">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="8f585-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-210">93</span><span class="sxs-lookup"><span data-stu-id="8f585-210">93</span></span>

<span data-ttu-id="8f585-211">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="8f585-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-212">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="8f585-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-213">94</span><span class="sxs-lookup"><span data-stu-id="8f585-213">94</span></span>

<span data-ttu-id="8f585-214">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="8f585-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-215">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="8f585-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-216">95</span><span class="sxs-lookup"><span data-stu-id="8f585-216">95</span></span>

<span data-ttu-id="8f585-217">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="8f585-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-218">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="8f585-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-219">96</span><span class="sxs-lookup"><span data-stu-id="8f585-219">96</span></span>

<span data-ttu-id="8f585-220">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="8f585-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-221">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="8f585-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-222">97</span><span class="sxs-lookup"><span data-stu-id="8f585-222">97</span></span>

<span data-ttu-id="8f585-223">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="8f585-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-224">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="8f585-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-225">98</span><span class="sxs-lookup"><span data-stu-id="8f585-225">98</span></span>

<span data-ttu-id="8f585-226">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="8f585-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-227">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="8f585-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-228">100</span><span class="sxs-lookup"><span data-stu-id="8f585-228">100</span></span>

<span data-ttu-id="8f585-229">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="8f585-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8f585-230">**Другое**</span><span class="sxs-lookup"><span data-stu-id="8f585-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="8f585-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="8f585-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f585-232">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8f585-232">Remarks</span></span>

<span data-ttu-id="8f585-233">Время ожидания повторной передачи удваивается при каждой последующей повторной передаче соединения.</span><span class="sxs-lookup"><span data-stu-id="8f585-233">The retransmission timeout doubles with each successive retransmission on a connection.</span></span>

## <a name="examples"></a><span data-ttu-id="8f585-234">Примеры</span><span class="sxs-lookup"><span data-stu-id="8f585-234">Examples</span></span>

<span data-ttu-id="8f585-235">Пример [изменения максимального допустимого числа передаваемых данных TCP](https://Gallery.TechNet.Microsoft.Com/8a581692-7950-412e-bd28-74f223b27827) в сценарии VBScript настраивает число попыток, которые TCP будет пытаться повторно передать отдельному сегменту данных, прежде чем отказаться от усилий.</span><span class="sxs-lookup"><span data-stu-id="8f585-235">The [Modify the Maximum Allowed TCP Data Retransmissions](https://Gallery.TechNet.Microsoft.Com/8a581692-7950-412e-bd28-74f223b27827) VBScript sample configures the number of times TCP will attempt to retransmit an individual data segment before abandoning the effort.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f585-236">Требования</span><span class="sxs-lookup"><span data-stu-id="8f585-236">Requirements</span></span>



| <span data-ttu-id="8f585-237">Требование</span><span class="sxs-lookup"><span data-stu-id="8f585-237">Requirement</span></span> | <span data-ttu-id="8f585-238">Значение</span><span class="sxs-lookup"><span data-stu-id="8f585-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f585-239">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8f585-239">Minimum supported client</span></span><br/> | <span data-ttu-id="8f585-240">Windows Vista, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f585-240">Windows Vista, Windows Vista</span></span><br/>                                                 |
| <span data-ttu-id="8f585-241">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8f585-241">Minimum supported server</span></span><br/> | <span data-ttu-id="8f585-242">Windows Server 2008, Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f585-242">Windows Server 2008, Windows Server 2008</span></span><br/>                                     |
| <span data-ttu-id="8f585-243">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8f585-243">Namespace</span></span><br/>                | <span data-ttu-id="8f585-244">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8f585-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8f585-245">MOF</span><span class="sxs-lookup"><span data-stu-id="8f585-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f585-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f585-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f585-247">DLL</span><span class="sxs-lookup"><span data-stu-id="8f585-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f585-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f585-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f585-249">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8f585-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f585-250">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="8f585-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="8f585-251">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="8f585-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="8f585-252">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="8f585-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="8f585-253">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="8f585-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="8f585-254">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="8f585-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

