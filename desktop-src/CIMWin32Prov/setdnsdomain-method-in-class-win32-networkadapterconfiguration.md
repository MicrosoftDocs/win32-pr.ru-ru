---
description: Метод класса WMI SetDNSDomain позволяет настроить домен DNS.
ms.assetid: a531133e-1b7c-4d85-979d-63bf4f7c9bed
ms.tgt_platform: multiple
title: Метод SetDNSDomain класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDNSDomain
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c440d8cb5c720bf6922707f04bc75e2383755c1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262729"
---
# <a name="setdnsdomain-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="13bed-103">Метод SetDNSDomain \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="13bed-103">SetDNSDomain method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="13bed-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) SETDNSDOMAIN позволяет настроить домен DNS.</span><span class="sxs-lookup"><span data-stu-id="13bed-104">The **SetDNSDomain** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method allows for the setting of the DNS domain.</span></span>

<span data-ttu-id="13bed-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="13bed-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="13bed-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="13bed-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="13bed-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13bed-107">Syntax</span></span>


```mof
uint32 SetDNSDomain(
  [in] string DNSDomain
);
```



## <a name="parameters"></a><span data-ttu-id="13bed-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="13bed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13bed-109">*Днсдомаин* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13bed-109">*DNSDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13bed-110">Домен, с которым связана служба DNS, представленная именем Организации, за которой следует точка и расширение, указывающее тип организации.</span><span class="sxs-lookup"><span data-stu-id="13bed-110">Domain with which the DNS is associated, represented by an organization name followed by a period and an extension that indicates the type of organization.</span></span>

<span data-ttu-id="13bed-111">Пример: "microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="13bed-111">Example: "microsoft.com"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13bed-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="13bed-112">Return value</span></span>

<span data-ttu-id="13bed-113">Возвращает значение 0 (ноль) для успешного завершения, если не требуется перезагрузка, 1 (один) для успешного завершения, если требуется перезагрузка, и другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="13bed-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required and a different number if there is an error.</span></span> <span data-ttu-id="13bed-114">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="13bed-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="13bed-115">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="13bed-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="13bed-116">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="13bed-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-117">0</span><span class="sxs-lookup"><span data-stu-id="13bed-117">0</span></span>

<span data-ttu-id="13bed-118">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="13bed-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-119">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="13bed-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-120">1</span><span class="sxs-lookup"><span data-stu-id="13bed-120">1</span></span>

<span data-ttu-id="13bed-121">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="13bed-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-122">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="13bed-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-123">64</span><span class="sxs-lookup"><span data-stu-id="13bed-123">64</span></span>

<span data-ttu-id="13bed-124">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="13bed-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-125">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="13bed-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-126">65</span><span class="sxs-lookup"><span data-stu-id="13bed-126">65</span></span>

<span data-ttu-id="13bed-127">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="13bed-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-128">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="13bed-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-129">66</span><span class="sxs-lookup"><span data-stu-id="13bed-129">66</span></span>

<span data-ttu-id="13bed-130">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="13bed-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-131">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="13bed-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-132">67</span><span class="sxs-lookup"><span data-stu-id="13bed-132">67</span></span>

<span data-ttu-id="13bed-133">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="13bed-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-134">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="13bed-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-135">68</span><span class="sxs-lookup"><span data-stu-id="13bed-135">68</span></span>

<span data-ttu-id="13bed-136">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="13bed-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-137">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="13bed-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-138">69</span><span class="sxs-lookup"><span data-stu-id="13bed-138">69</span></span>

<span data-ttu-id="13bed-139">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="13bed-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-140">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="13bed-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-141">70</span><span class="sxs-lookup"><span data-stu-id="13bed-141">70</span></span>

<span data-ttu-id="13bed-142">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="13bed-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-143">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="13bed-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-144">71</span><span class="sxs-lookup"><span data-stu-id="13bed-144">71</span></span>

<span data-ttu-id="13bed-145">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="13bed-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-146">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="13bed-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-147">72</span><span class="sxs-lookup"><span data-stu-id="13bed-147">72</span></span>

<span data-ttu-id="13bed-148">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="13bed-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-149">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="13bed-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-150">73</span><span class="sxs-lookup"><span data-stu-id="13bed-150">73</span></span>

<span data-ttu-id="13bed-151">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="13bed-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-152">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="13bed-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-153">74</span><span class="sxs-lookup"><span data-stu-id="13bed-153">74</span></span>

<span data-ttu-id="13bed-154">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="13bed-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-155">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="13bed-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-156">75</span><span class="sxs-lookup"><span data-stu-id="13bed-156">75</span></span>

<span data-ttu-id="13bed-157">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="13bed-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-158">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="13bed-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-159">76</span><span class="sxs-lookup"><span data-stu-id="13bed-159">76</span></span>

<span data-ttu-id="13bed-160">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="13bed-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-161">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="13bed-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-162">77</span><span class="sxs-lookup"><span data-stu-id="13bed-162">77</span></span>

<span data-ttu-id="13bed-163">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="13bed-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-164">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="13bed-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-165">78</span><span class="sxs-lookup"><span data-stu-id="13bed-165">78</span></span>

<span data-ttu-id="13bed-166">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="13bed-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-167">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="13bed-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-168">79</span><span class="sxs-lookup"><span data-stu-id="13bed-168">79</span></span>

<span data-ttu-id="13bed-169">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="13bed-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-170">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="13bed-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-171">80</span><span class="sxs-lookup"><span data-stu-id="13bed-171">80</span></span>

<span data-ttu-id="13bed-172">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="13bed-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-173">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="13bed-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-174">81</span><span class="sxs-lookup"><span data-stu-id="13bed-174">81</span></span>

<span data-ttu-id="13bed-175">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="13bed-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-176">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="13bed-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-177">82</span><span class="sxs-lookup"><span data-stu-id="13bed-177">82</span></span>

<span data-ttu-id="13bed-178">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="13bed-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-179">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="13bed-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-180">83</span><span class="sxs-lookup"><span data-stu-id="13bed-180">83</span></span>

<span data-ttu-id="13bed-181">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="13bed-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-182">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="13bed-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-183">84</span><span class="sxs-lookup"><span data-stu-id="13bed-183">84</span></span>

<span data-ttu-id="13bed-184">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="13bed-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-185">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="13bed-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-186">85</span><span class="sxs-lookup"><span data-stu-id="13bed-186">85</span></span>

<span data-ttu-id="13bed-187">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="13bed-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-188">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="13bed-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-189">86</span><span class="sxs-lookup"><span data-stu-id="13bed-189">86</span></span>

<span data-ttu-id="13bed-190">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="13bed-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-191">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="13bed-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-192">87</span><span class="sxs-lookup"><span data-stu-id="13bed-192">87</span></span>

<span data-ttu-id="13bed-193">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="13bed-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-194">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="13bed-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-195">88</span><span class="sxs-lookup"><span data-stu-id="13bed-195">88</span></span>

<span data-ttu-id="13bed-196">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="13bed-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-197">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="13bed-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-198">89</span><span class="sxs-lookup"><span data-stu-id="13bed-198">89</span></span>

<span data-ttu-id="13bed-199">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="13bed-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-200">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="13bed-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-201">90</span><span class="sxs-lookup"><span data-stu-id="13bed-201">90</span></span>

<span data-ttu-id="13bed-202">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="13bed-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-203">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="13bed-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-204">91</span><span class="sxs-lookup"><span data-stu-id="13bed-204">91</span></span>

<span data-ttu-id="13bed-205">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="13bed-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-206">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="13bed-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-207">92</span><span class="sxs-lookup"><span data-stu-id="13bed-207">92</span></span>

<span data-ttu-id="13bed-208">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="13bed-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-209">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="13bed-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-210">93</span><span class="sxs-lookup"><span data-stu-id="13bed-210">93</span></span>

<span data-ttu-id="13bed-211">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="13bed-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-212">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="13bed-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-213">94</span><span class="sxs-lookup"><span data-stu-id="13bed-213">94</span></span>

<span data-ttu-id="13bed-214">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="13bed-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-215">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="13bed-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-216">95</span><span class="sxs-lookup"><span data-stu-id="13bed-216">95</span></span>

<span data-ttu-id="13bed-217">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="13bed-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-218">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="13bed-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-219">96</span><span class="sxs-lookup"><span data-stu-id="13bed-219">96</span></span>

<span data-ttu-id="13bed-220">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="13bed-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-221">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="13bed-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-222">97</span><span class="sxs-lookup"><span data-stu-id="13bed-222">97</span></span>

<span data-ttu-id="13bed-223">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="13bed-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-224">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="13bed-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-225">98</span><span class="sxs-lookup"><span data-stu-id="13bed-225">98</span></span>

<span data-ttu-id="13bed-226">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="13bed-226">Not all DHCP leases can be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-227">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="13bed-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-228">100</span><span class="sxs-lookup"><span data-stu-id="13bed-228">100</span></span>

<span data-ttu-id="13bed-229">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="13bed-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="13bed-230">**Другое**</span><span class="sxs-lookup"><span data-stu-id="13bed-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="13bed-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="13bed-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="13bed-232">Комментарии</span><span class="sxs-lookup"><span data-stu-id="13bed-232">Remarks</span></span>

<span data-ttu-id="13bed-233">Это зависящий от экземпляра вызов метода, который применяется для каждого адаптера.</span><span class="sxs-lookup"><span data-stu-id="13bed-233">This is an instance-dependent method call that applies on a per-adapter basis.</span></span> <span data-ttu-id="13bed-234">Параметр применяется к целевому адаптеру.</span><span class="sxs-lookup"><span data-stu-id="13bed-234">The setting applies to the targeted adapter.</span></span>

## <a name="examples"></a><span data-ttu-id="13bed-235">Примеры</span><span class="sxs-lookup"><span data-stu-id="13bed-235">Examples</span></span>

<span data-ttu-id="13bed-236">Пример кода сценария " [Назначение домена DNS для сетевого адаптера](https://Gallery.TechNet.Microsoft.Com/6044a0a4-d320-4c18-a94b-c125796d219b) " в коллекции TechNet использует **SetDNSDomain** , чтобы задать домен DNS для сетевого адаптера, связанного с TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="13bed-236">The [Assign the DNS Domain for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/6044a0a4-d320-4c18-a94b-c125796d219b) VBScript code sample on TechNet gallery uses **SetDNSDomain** to set the DNS domain for a TCP/IP-bound network adapter.</span></span>

<span data-ttu-id="13bed-237">Пример [изменения конфигурации TCP/IP для компьютера](https://Gallery.TechNet.Microsoft.Com/3d5ae334-1d75-4cea-8079-78c6bd836faf) в коллекции TechNet использует **SetDNSDomain** для изменения параметров TCP/IP сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="13bed-237">The [Modify the TCP/IP Configuration for a Computer](https://Gallery.TechNet.Microsoft.Com/3d5ae334-1d75-4cea-8079-78c6bd836faf) VBScript code sample on TechNet Gallery uses **SetDNSDomain** to modify TCP/IP settings for a network adapter.</span></span>

<span data-ttu-id="13bed-238">Пример [включения параметров DHCP на компьютере](https://Gallery.TechNet.Microsoft.Com/41e6ab51-78c0-4413-b086-03fde33ea125) в коллекции TechNet использует **SetDNSDomain** для настройки всех параметров, которые обычно необходимы для включения DHCP на компьютере.</span><span class="sxs-lookup"><span data-stu-id="13bed-238">The [Enable DHCP Settings on a Computer](https://Gallery.TechNet.Microsoft.Com/41e6ab51-78c0-4413-b086-03fde33ea125) VBScript sample on TechNet Gallery uses **SetDNSDomain** to configure all the settings typically required to enable DHCP on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="13bed-239">Требования</span><span class="sxs-lookup"><span data-stu-id="13bed-239">Requirements</span></span>



| <span data-ttu-id="13bed-240">Требование</span><span class="sxs-lookup"><span data-stu-id="13bed-240">Requirement</span></span> | <span data-ttu-id="13bed-241">Значение</span><span class="sxs-lookup"><span data-stu-id="13bed-241">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13bed-242">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13bed-242">Minimum supported client</span></span><br/> | <span data-ttu-id="13bed-243">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13bed-243">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="13bed-244">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13bed-244">Minimum supported server</span></span><br/> | <span data-ttu-id="13bed-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13bed-245">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="13bed-246">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="13bed-246">Namespace</span></span><br/>                | <span data-ttu-id="13bed-247">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="13bed-247">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="13bed-248">MOF</span><span class="sxs-lookup"><span data-stu-id="13bed-248">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13bed-249"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13bed-249"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="13bed-250">DLL</span><span class="sxs-lookup"><span data-stu-id="13bed-250">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13bed-251"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13bed-251"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13bed-252">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13bed-252">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13bed-253">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="13bed-253">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="13bed-254">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="13bed-254">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="13bed-255">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="13bed-255">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="13bed-256">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="13bed-256">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="13bed-257">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="13bed-257">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

