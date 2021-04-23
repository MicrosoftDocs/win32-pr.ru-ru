---
description: Метод класса WMI Сетвинссервер задает основной и дополнительный серверы Windows Internet Служба именования (WINS) в этом сетевом адаптере, привязанном к TCP/IP. Этот метод применяется независимо от сетевого адаптера.
ms.assetid: fa8ce436-b67e-4975-a5c5-1a7d6aab4c8e
ms.tgt_platform: multiple
title: Метод Сетвинссервер класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetWINSServer
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 49bfb0103a7d9cbbd6ea3faa0e1a868bac7b0196
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650442"
---
# <a name="setwinsserver-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="cc11b-104">Метод Сетвинссервер \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="cc11b-104">SetWINSServer method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="cc11b-105">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) сетвинссервер задает основной и дополнительный серверы Windows Internet служба именования (WINS) в этом сетевом адаптере, привязанном к TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="cc11b-105">The **SetWINSServer** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method sets the primary and secondary Windows Internet Naming Service (WINS) servers on this TCP/IP-bound network adapter.</span></span> <span data-ttu-id="cc11b-106">Этот метод применяется независимо от сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="cc11b-106">This method is applied independently of the network adapter.</span></span>

<span data-ttu-id="cc11b-107">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="cc11b-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="cc11b-108">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="cc11b-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="cc11b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc11b-109">Syntax</span></span>


```mof
uint32 SetWINSServer(
  [in] string WINSPrimaryServer,
  [in] string WINSSecondaryServer
);
```



## <a name="parameters"></a><span data-ttu-id="cc11b-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc11b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc11b-111">*Винспримарисервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc11b-111">*WINSPrimaryServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-112">IP-адрес основного WINS-сервера.</span><span class="sxs-lookup"><span data-stu-id="cc11b-112">IP address of the primary WINS server.</span></span>

> [!Note]  
> <span data-ttu-id="cc11b-113">Всегда проверяйте срок действия этого IP-адреса, если он из неизвестного источника, или ненадежного источника.</span><span class="sxs-lookup"><span data-stu-id="cc11b-113">Always verify the validity of this IP address when it is from an unknown source, or a source that you do not trust.</span></span>

 

</dd> <dt>

<span data-ttu-id="cc11b-114">*Винссекондарисервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc11b-114">*WINSSecondaryServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-115">IP-адрес дополнительного WINS-сервера.</span><span class="sxs-lookup"><span data-stu-id="cc11b-115">IP address of the secondary WINS server.</span></span>

> [!Note]  
> <span data-ttu-id="cc11b-116">Всегда проверяйте срок действия этого IP-адреса, если он из неизвестного источника, или ненадежного источника.</span><span class="sxs-lookup"><span data-stu-id="cc11b-116">Always verify the validity of this IP address when it is from an unknown source, or a source that you do not trust.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc11b-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc11b-117">Return value</span></span>

<span data-ttu-id="cc11b-118">Возвращает целочисленное значение 0 (ноль) при успешном завершении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="cc11b-118">Returns an integer value of 0 (zero) on successful completion, and any other number to indicate an error.</span></span> <span data-ttu-id="cc11b-119">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="cc11b-119">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="cc11b-120">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="cc11b-120">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="cc11b-121">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="cc11b-121">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-122">0</span><span class="sxs-lookup"><span data-stu-id="cc11b-122">0</span></span>

<span data-ttu-id="cc11b-123">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="cc11b-123">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-124">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="cc11b-124">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-125">1</span><span class="sxs-lookup"><span data-stu-id="cc11b-125">1</span></span>

<span data-ttu-id="cc11b-126">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="cc11b-126">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-127">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="cc11b-127">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-128">64</span><span class="sxs-lookup"><span data-stu-id="cc11b-128">64</span></span>

<span data-ttu-id="cc11b-129">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="cc11b-129">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-130">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="cc11b-130">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-131">65</span><span class="sxs-lookup"><span data-stu-id="cc11b-131">65</span></span>

<span data-ttu-id="cc11b-132">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="cc11b-132">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-133">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="cc11b-133">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-134">66</span><span class="sxs-lookup"><span data-stu-id="cc11b-134">66</span></span>

<span data-ttu-id="cc11b-135">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="cc11b-135">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-136">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="cc11b-136">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-137">67</span><span class="sxs-lookup"><span data-stu-id="cc11b-137">67</span></span>

<span data-ttu-id="cc11b-138">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="cc11b-138">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-139">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="cc11b-139">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-140">68</span><span class="sxs-lookup"><span data-stu-id="cc11b-140">68</span></span>

<span data-ttu-id="cc11b-141">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="cc11b-141">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-142">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="cc11b-142">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-143">69</span><span class="sxs-lookup"><span data-stu-id="cc11b-143">69</span></span>

<span data-ttu-id="cc11b-144">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="cc11b-144">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-145">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="cc11b-145">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-146">70</span><span class="sxs-lookup"><span data-stu-id="cc11b-146">70</span></span>

<span data-ttu-id="cc11b-147">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="cc11b-147">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-148">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="cc11b-148">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-149">71</span><span class="sxs-lookup"><span data-stu-id="cc11b-149">71</span></span>

<span data-ttu-id="cc11b-150">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="cc11b-150">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-151">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="cc11b-151">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-152">72</span><span class="sxs-lookup"><span data-stu-id="cc11b-152">72</span></span>

<span data-ttu-id="cc11b-153">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="cc11b-153">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-154">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="cc11b-154">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-155">73</span><span class="sxs-lookup"><span data-stu-id="cc11b-155">73</span></span>

<span data-ttu-id="cc11b-156">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="cc11b-156">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-157">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="cc11b-157">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-158">74</span><span class="sxs-lookup"><span data-stu-id="cc11b-158">74</span></span>

<span data-ttu-id="cc11b-159">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="cc11b-159">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-160">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="cc11b-160">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-161">75</span><span class="sxs-lookup"><span data-stu-id="cc11b-161">75</span></span>

<span data-ttu-id="cc11b-162">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="cc11b-162">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-163">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="cc11b-163">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-164">76</span><span class="sxs-lookup"><span data-stu-id="cc11b-164">76</span></span>

<span data-ttu-id="cc11b-165">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="cc11b-165">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-166">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="cc11b-166">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-167">77</span><span class="sxs-lookup"><span data-stu-id="cc11b-167">77</span></span>

<span data-ttu-id="cc11b-168">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="cc11b-168">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-169">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="cc11b-169">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-170">78</span><span class="sxs-lookup"><span data-stu-id="cc11b-170">78</span></span>

<span data-ttu-id="cc11b-171">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="cc11b-171">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-172">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="cc11b-172">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-173">79</span><span class="sxs-lookup"><span data-stu-id="cc11b-173">79</span></span>

<span data-ttu-id="cc11b-174">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="cc11b-174">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-175">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="cc11b-175">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-176">80</span><span class="sxs-lookup"><span data-stu-id="cc11b-176">80</span></span>

<span data-ttu-id="cc11b-177">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="cc11b-177">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-178">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="cc11b-178">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-179">81</span><span class="sxs-lookup"><span data-stu-id="cc11b-179">81</span></span>

<span data-ttu-id="cc11b-180">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="cc11b-180">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-181">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="cc11b-181">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-182">82</span><span class="sxs-lookup"><span data-stu-id="cc11b-182">82</span></span>

<span data-ttu-id="cc11b-183">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="cc11b-183">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-184">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="cc11b-184">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-185">83</span><span class="sxs-lookup"><span data-stu-id="cc11b-185">83</span></span>

<span data-ttu-id="cc11b-186">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="cc11b-186">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-187">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="cc11b-187">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-188">84</span><span class="sxs-lookup"><span data-stu-id="cc11b-188">84</span></span>

<span data-ttu-id="cc11b-189">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="cc11b-189">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-190">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="cc11b-190">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-191">85</span><span class="sxs-lookup"><span data-stu-id="cc11b-191">85</span></span>

<span data-ttu-id="cc11b-192">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="cc11b-192">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-193">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="cc11b-193">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-194">86</span><span class="sxs-lookup"><span data-stu-id="cc11b-194">86</span></span>

<span data-ttu-id="cc11b-195">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="cc11b-195">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-196">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="cc11b-196">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-197">87</span><span class="sxs-lookup"><span data-stu-id="cc11b-197">87</span></span>

<span data-ttu-id="cc11b-198">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="cc11b-198">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-199">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="cc11b-199">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-200">88</span><span class="sxs-lookup"><span data-stu-id="cc11b-200">88</span></span>

<span data-ttu-id="cc11b-201">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="cc11b-201">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-202">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="cc11b-202">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-203">89</span><span class="sxs-lookup"><span data-stu-id="cc11b-203">89</span></span>

<span data-ttu-id="cc11b-204">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="cc11b-204">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-205">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="cc11b-205">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-206">90</span><span class="sxs-lookup"><span data-stu-id="cc11b-206">90</span></span>

<span data-ttu-id="cc11b-207">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="cc11b-207">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-208">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="cc11b-208">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-209">91</span><span class="sxs-lookup"><span data-stu-id="cc11b-209">91</span></span>

<span data-ttu-id="cc11b-210">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="cc11b-210">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-211">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="cc11b-211">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-212">92</span><span class="sxs-lookup"><span data-stu-id="cc11b-212">92</span></span>

<span data-ttu-id="cc11b-213">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="cc11b-213">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-214">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="cc11b-214">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-215">93</span><span class="sxs-lookup"><span data-stu-id="cc11b-215">93</span></span>

<span data-ttu-id="cc11b-216">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="cc11b-216">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-217">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="cc11b-217">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-218">94</span><span class="sxs-lookup"><span data-stu-id="cc11b-218">94</span></span>

<span data-ttu-id="cc11b-219">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="cc11b-219">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-220">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="cc11b-220">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-221">95</span><span class="sxs-lookup"><span data-stu-id="cc11b-221">95</span></span>

<span data-ttu-id="cc11b-222">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="cc11b-222">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-223">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="cc11b-223">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-224">96</span><span class="sxs-lookup"><span data-stu-id="cc11b-224">96</span></span>

<span data-ttu-id="cc11b-225">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="cc11b-225">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-226">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="cc11b-226">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-227">97</span><span class="sxs-lookup"><span data-stu-id="cc11b-227">97</span></span>

<span data-ttu-id="cc11b-228">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="cc11b-228">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-229">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="cc11b-229">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-230">98</span><span class="sxs-lookup"><span data-stu-id="cc11b-230">98</span></span>

<span data-ttu-id="cc11b-231">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="cc11b-231">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-232">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="cc11b-232">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-233">100</span><span class="sxs-lookup"><span data-stu-id="cc11b-233">100</span></span>

<span data-ttu-id="cc11b-234">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="cc11b-234">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="cc11b-235">**Другое**</span><span class="sxs-lookup"><span data-stu-id="cc11b-235">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="cc11b-236">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="cc11b-236">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cc11b-237">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc11b-237">Remarks</span></span>

<span data-ttu-id="cc11b-238">Если для обоих *винспримарисервер* и *винссекондарисервер* задано значение "" (пустая строка), то явные WINS-серверы возвращаются обратно в службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="cc11b-238">If both *WINSPrimaryServer* and *WINSSecondaryServer* are set to "" (an empty string), then explicit WINS servers revert back to DHCP.</span></span>

## <a name="examples"></a><span data-ttu-id="cc11b-239">Примеры</span><span class="sxs-lookup"><span data-stu-id="cc11b-239">Examples</span></span>

<span data-ttu-id="cc11b-240">[Назначение IP-адреса, полученного из базы данных](https://Gallery.TechNet.Microsoft.Com/d4526355-e682-4116-a79a-8bba569b084d) Пример кода VBScript находит компьютер в базе данных и назначает этому компьютеру указанный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="cc11b-240">[The Assign an IP Address Retrieved from a Database](https://Gallery.TechNet.Microsoft.Com/d4526355-e682-4116-a79a-8bba569b084d) VBScript code sample looks up a computer in a database and assigns that computer the specified IP address.</span></span>

<span data-ttu-id="cc11b-241">Следующий пример кода VBScript задает основной и дополнительный WINS-серверы для сетевого адаптера, связанного с TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="cc11b-241">The following VBScript code sample sets the primary and secondary WINS server for a TCP/IP-bound network adapter.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colNetCards = objWMIService.ExecQuery _ 
    ("Select * From Win32_NetworkAdapterConfiguration Where IPEnabled = True") 
 
For Each objNetCard in colNetCards 
    strPrimaryServer = "192.168.1.100" 
    strSecondaryServer = "192.168.1.200" 
    objNetCard.SetWINSServer strPrimaryServer, strSecondaryServer 
Next 
```



## <a name="requirements"></a><span data-ttu-id="cc11b-242">Требования</span><span class="sxs-lookup"><span data-stu-id="cc11b-242">Requirements</span></span>



| <span data-ttu-id="cc11b-243">Требование</span><span class="sxs-lookup"><span data-stu-id="cc11b-243">Requirement</span></span> | <span data-ttu-id="cc11b-244">Значение</span><span class="sxs-lookup"><span data-stu-id="cc11b-244">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc11b-245">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cc11b-245">Minimum supported client</span></span><br/> | <span data-ttu-id="cc11b-246">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cc11b-246">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cc11b-247">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cc11b-247">Minimum supported server</span></span><br/> | <span data-ttu-id="cc11b-248">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cc11b-248">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cc11b-249">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cc11b-249">Namespace</span></span><br/>                | <span data-ttu-id="cc11b-250">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cc11b-250">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cc11b-251">MOF</span><span class="sxs-lookup"><span data-stu-id="cc11b-251">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cc11b-252"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cc11b-252"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cc11b-253">DLL</span><span class="sxs-lookup"><span data-stu-id="cc11b-253">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc11b-254"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc11b-254"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc11b-255">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc11b-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc11b-256">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="cc11b-256">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="cc11b-257">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="cc11b-257">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="cc11b-258">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="cc11b-258">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="cc11b-259">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="cc11b-259">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="cc11b-260">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="cc11b-260">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

