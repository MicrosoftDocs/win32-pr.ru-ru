---
description: Метод Сетдинамикднсрегистратион указывает на динамическую регистрацию DNS IP-адресов для этого адаптера, привязанного к IP-адресу.
ms.assetid: 8e6ca408-3283-40b8-b621-9befdc39b730
ms.tgt_platform: multiple
title: Метод Сетдинамикднсрегистратион класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDynamicDNSRegistration
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 36818205e356f873b391159293e9204a9ced44a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896149"
---
# <a name="setdynamicdnsregistration-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="cebd7-103">Метод Сетдинамикднсрегистратион \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="cebd7-103">SetDynamicDNSRegistration method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="cebd7-104">Метод **сетдинамикднсрегистратион** указывает на динамическую регистрацию DNS IP-адресов для этого адаптера, привязанного к IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="cebd7-104">The **SetDynamicDNSRegistration** method indicates the dynamic DNS registration of IP addresses for this IP-bound adapter.</span></span>

<span data-ttu-id="cebd7-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="cebd7-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="cebd7-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="cebd7-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="cebd7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cebd7-107">Syntax</span></span>


```mof
uint32 SetDynamicDNSRegistration(
  [in]           boolean FullDNSRegistrationEnabled,
  [in, optional] boolean DomainDNSRegistrationEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="cebd7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cebd7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cebd7-109">*Фуллднсрегистратионенаблед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cebd7-109">*FullDNSRegistrationEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-110">Если **значение — true**, IP-адреса для этого подключения регистрируются в DNS под полным DNS-именем компьютера.</span><span class="sxs-lookup"><span data-stu-id="cebd7-110">If **true**, the IP addresses for this connection is registered in DNS under the computer's full DNS name.</span></span> <span data-ttu-id="cebd7-111">Полное DNS-имя компьютера отображается на вкладке **Сетевая идентификация** на панели управления системой.</span><span class="sxs-lookup"><span data-stu-id="cebd7-111">The full DNS name of the computer is displayed on the **Network Identification** tab of the system Control Panel.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-112">*Домаинднсрегистратионенаблед* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="cebd7-112">*DomainDNSRegistrationEnabled* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-113">Если **значение — true**, IP-адреса для этого подключения регистрируются в доменном имени этого подключения, а не в полном DNS-имени компьютера.</span><span class="sxs-lookup"><span data-stu-id="cebd7-113">If **true**, the IP addresses for this connection are registered under the domain name of this connection, in addition to being registered under the computer's full DNS name.</span></span> <span data-ttu-id="cebd7-114">Доменное имя этого подключения задается с помощью метода [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md) или назначено DHCP.</span><span class="sxs-lookup"><span data-stu-id="cebd7-114">The domain name of this connection is either set using the method [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md) or assigned by DHCP.</span></span> <span data-ttu-id="cebd7-115">Зарегистрированное имя — это имя узла компьютера с добавленным доменным именем.</span><span class="sxs-lookup"><span data-stu-id="cebd7-115">The registered name is the host name of the computer with the domain name appended.</span></span> <span data-ttu-id="cebd7-116">Этот параметр имеет значение только в том случае, если включен *фуллднсрегистратионенаблед* .</span><span class="sxs-lookup"><span data-stu-id="cebd7-116">This parameter has meaning only when *FullDNSRegistrationEnabled* is enabled.</span></span> <span data-ttu-id="cebd7-117">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="cebd7-117">The default value is **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cebd7-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cebd7-118">Return value</span></span>

<span data-ttu-id="cebd7-119">Возвращает значение 0 (ноль) для успешного завершения, если не требуется перезагрузка, 1 (один) для успешного завершения, когда требуется перезагрузка, и другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="cebd7-119">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="cebd7-120">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="cebd7-120">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="cebd7-121">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="cebd7-121">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="cebd7-122">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="cebd7-122">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-123">0</span><span class="sxs-lookup"><span data-stu-id="cebd7-123">0</span></span>

<span data-ttu-id="cebd7-124">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="cebd7-124">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-125">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="cebd7-125">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-126">1</span><span class="sxs-lookup"><span data-stu-id="cebd7-126">1</span></span>

<span data-ttu-id="cebd7-127">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="cebd7-127">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-128">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="cebd7-128">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-129">64</span><span class="sxs-lookup"><span data-stu-id="cebd7-129">64</span></span>

<span data-ttu-id="cebd7-130">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="cebd7-130">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-131">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="cebd7-131">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-132">65</span><span class="sxs-lookup"><span data-stu-id="cebd7-132">65</span></span>

<span data-ttu-id="cebd7-133">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="cebd7-133">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-134">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="cebd7-134">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-135">66</span><span class="sxs-lookup"><span data-stu-id="cebd7-135">66</span></span>

<span data-ttu-id="cebd7-136">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="cebd7-136">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-137">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="cebd7-137">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-138">67</span><span class="sxs-lookup"><span data-stu-id="cebd7-138">67</span></span>

<span data-ttu-id="cebd7-139">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="cebd7-139">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-140">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="cebd7-140">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-141">68</span><span class="sxs-lookup"><span data-stu-id="cebd7-141">68</span></span>

<span data-ttu-id="cebd7-142">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="cebd7-142">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-143">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="cebd7-143">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-144">69</span><span class="sxs-lookup"><span data-stu-id="cebd7-144">69</span></span>

<span data-ttu-id="cebd7-145">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="cebd7-145">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-146">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="cebd7-146">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-147">70</span><span class="sxs-lookup"><span data-stu-id="cebd7-147">70</span></span>

<span data-ttu-id="cebd7-148">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="cebd7-148">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-149">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="cebd7-149">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-150">71</span><span class="sxs-lookup"><span data-stu-id="cebd7-150">71</span></span>

<span data-ttu-id="cebd7-151">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="cebd7-151">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-152">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="cebd7-152">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-153">72</span><span class="sxs-lookup"><span data-stu-id="cebd7-153">72</span></span>

<span data-ttu-id="cebd7-154">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="cebd7-154">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-155">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="cebd7-155">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-156">73</span><span class="sxs-lookup"><span data-stu-id="cebd7-156">73</span></span>

<span data-ttu-id="cebd7-157">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="cebd7-157">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-158">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="cebd7-158">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-159">74</span><span class="sxs-lookup"><span data-stu-id="cebd7-159">74</span></span>

<span data-ttu-id="cebd7-160">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="cebd7-160">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-161">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="cebd7-161">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-162">75</span><span class="sxs-lookup"><span data-stu-id="cebd7-162">75</span></span>

<span data-ttu-id="cebd7-163">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="cebd7-163">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-164">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="cebd7-164">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-165">76</span><span class="sxs-lookup"><span data-stu-id="cebd7-165">76</span></span>

<span data-ttu-id="cebd7-166">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="cebd7-166">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-167">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="cebd7-167">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-168">77</span><span class="sxs-lookup"><span data-stu-id="cebd7-168">77</span></span>

<span data-ttu-id="cebd7-169">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="cebd7-169">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-170">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="cebd7-170">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-171">78</span><span class="sxs-lookup"><span data-stu-id="cebd7-171">78</span></span>

<span data-ttu-id="cebd7-172">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="cebd7-172">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-173">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="cebd7-173">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-174">79</span><span class="sxs-lookup"><span data-stu-id="cebd7-174">79</span></span>

<span data-ttu-id="cebd7-175">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="cebd7-175">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-176">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="cebd7-176">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-177">80</span><span class="sxs-lookup"><span data-stu-id="cebd7-177">80</span></span>

<span data-ttu-id="cebd7-178">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="cebd7-178">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-179">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="cebd7-179">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-180">81</span><span class="sxs-lookup"><span data-stu-id="cebd7-180">81</span></span>

<span data-ttu-id="cebd7-181">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="cebd7-181">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-182">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="cebd7-182">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-183">82</span><span class="sxs-lookup"><span data-stu-id="cebd7-183">82</span></span>

<span data-ttu-id="cebd7-184">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="cebd7-184">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-185">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="cebd7-185">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-186">83</span><span class="sxs-lookup"><span data-stu-id="cebd7-186">83</span></span>

<span data-ttu-id="cebd7-187">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="cebd7-187">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-188">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="cebd7-188">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-189">84</span><span class="sxs-lookup"><span data-stu-id="cebd7-189">84</span></span>

<span data-ttu-id="cebd7-190">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="cebd7-190">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-191">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="cebd7-191">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-192">85</span><span class="sxs-lookup"><span data-stu-id="cebd7-192">85</span></span>

<span data-ttu-id="cebd7-193">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="cebd7-193">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-194">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="cebd7-194">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-195">86</span><span class="sxs-lookup"><span data-stu-id="cebd7-195">86</span></span>

<span data-ttu-id="cebd7-196">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="cebd7-196">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-197">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="cebd7-197">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-198">87</span><span class="sxs-lookup"><span data-stu-id="cebd7-198">87</span></span>

<span data-ttu-id="cebd7-199">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="cebd7-199">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-200">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="cebd7-200">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-201">88</span><span class="sxs-lookup"><span data-stu-id="cebd7-201">88</span></span>

<span data-ttu-id="cebd7-202">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="cebd7-202">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-203">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="cebd7-203">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-204">89</span><span class="sxs-lookup"><span data-stu-id="cebd7-204">89</span></span>

<span data-ttu-id="cebd7-205">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="cebd7-205">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-206">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="cebd7-206">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-207">90</span><span class="sxs-lookup"><span data-stu-id="cebd7-207">90</span></span>

<span data-ttu-id="cebd7-208">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="cebd7-208">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-209">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="cebd7-209">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-210">91</span><span class="sxs-lookup"><span data-stu-id="cebd7-210">91</span></span>

<span data-ttu-id="cebd7-211">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="cebd7-211">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-212">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="cebd7-212">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-213">92</span><span class="sxs-lookup"><span data-stu-id="cebd7-213">92</span></span>

<span data-ttu-id="cebd7-214">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="cebd7-214">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-215">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="cebd7-215">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-216">93</span><span class="sxs-lookup"><span data-stu-id="cebd7-216">93</span></span>

<span data-ttu-id="cebd7-217">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="cebd7-217">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-218">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="cebd7-218">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-219">94</span><span class="sxs-lookup"><span data-stu-id="cebd7-219">94</span></span>

<span data-ttu-id="cebd7-220">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="cebd7-220">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-221">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="cebd7-221">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-222">95</span><span class="sxs-lookup"><span data-stu-id="cebd7-222">95</span></span>

<span data-ttu-id="cebd7-223">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="cebd7-223">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-224">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="cebd7-224">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-225">96</span><span class="sxs-lookup"><span data-stu-id="cebd7-225">96</span></span>

<span data-ttu-id="cebd7-226">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="cebd7-226">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-227">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="cebd7-227">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-228">97</span><span class="sxs-lookup"><span data-stu-id="cebd7-228">97</span></span>

<span data-ttu-id="cebd7-229">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="cebd7-229">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-230">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="cebd7-230">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-231">98</span><span class="sxs-lookup"><span data-stu-id="cebd7-231">98</span></span>

<span data-ttu-id="cebd7-232">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="cebd7-232">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-233">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="cebd7-233">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-234">100</span><span class="sxs-lookup"><span data-stu-id="cebd7-234">100</span></span>

<span data-ttu-id="cebd7-235">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="cebd7-235">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-236">**Другое**</span><span class="sxs-lookup"><span data-stu-id="cebd7-236">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-237">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="cebd7-237">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="cebd7-238">Примеры</span><span class="sxs-lookup"><span data-stu-id="cebd7-238">Examples</span></span>

<span data-ttu-id="cebd7-239">Пример [изменения динамической регистрации DNS для сетевого адаптера](https://Gallery.TechNet.Microsoft.Com/6c72969c-16c8-4bb6-92e9-b9020001759f) на языке VBScript настраивает динамическую регистрацию DNS для сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="cebd7-239">The [Modify Dynamic DNS Registration for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/6c72969c-16c8-4bb6-92e9-b9020001759f) VBScript sample configures dynamic DNS registration for a network adapter.</span></span>

<span data-ttu-id="cebd7-240">На странице [Настройка сетевых адаптеров iSCSI согласно рекомендациям Microsoft PowerShell для каждого](https://Gallery.TechNet.Microsoft.Com/Configure-iSCSI-Network-81232a5e) из них автоматизируются параметры конфигурации для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cebd7-240">The [Configure iSCSI Network Cards as per Microsoft Best Practices PowerShell](https://Gallery.TechNet.Microsoft.Com/Configure-iSCSI-Network-81232a5e) sample automates the configuration settings for a Virtual Machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="cebd7-241">Требования</span><span class="sxs-lookup"><span data-stu-id="cebd7-241">Requirements</span></span>



| <span data-ttu-id="cebd7-242">Требование</span><span class="sxs-lookup"><span data-stu-id="cebd7-242">Requirement</span></span> | <span data-ttu-id="cebd7-243">Значение</span><span class="sxs-lookup"><span data-stu-id="cebd7-243">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cebd7-244">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cebd7-244">Minimum supported client</span></span><br/> | <span data-ttu-id="cebd7-245">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cebd7-245">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cebd7-246">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cebd7-246">Minimum supported server</span></span><br/> | <span data-ttu-id="cebd7-247">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cebd7-247">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cebd7-248">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cebd7-248">Namespace</span></span><br/>                | <span data-ttu-id="cebd7-249">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cebd7-249">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cebd7-250">MOF</span><span class="sxs-lookup"><span data-stu-id="cebd7-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cebd7-251"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cebd7-251"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cebd7-252">DLL</span><span class="sxs-lookup"><span data-stu-id="cebd7-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cebd7-253"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cebd7-253"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cebd7-254">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cebd7-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cebd7-255">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="cebd7-255">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="cebd7-256">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="cebd7-256">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="cebd7-257">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="cebd7-257">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="cebd7-258">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="cebd7-258">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="cebd7-259">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="cebd7-259">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

