---
description: Статический метод класса Енаблеипфилтерсек WMI используется для глобального обеспечения безопасности протокола IPsec во всех сетевых адаптерах, привязанных к IP-адресу.
ms.assetid: 565acc18-61e7-473e-b2cc-41f0e8c29193
ms.tgt_platform: multiple
title: Метод Енаблеипфилтерсек класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableIPFilterSec
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3429e2c2ba78e013da9195961b76ff84ffda9b68
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895726"
---
# <a name="enableipfiltersec-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="26451-103">Метод Енаблеипфилтерсек \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="26451-103">EnableIPFilterSec method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="26451-104">Статический метод класса **енаблеипфилтерсек** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) используется для глобального обеспечения безопасности протокола IPSec во всех сетевых адаптерах, привязанных к IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="26451-104">The **EnableIPFilterSec** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable Internet Protocol security (IPsec) globally across all IP-bound network adapters.</span></span>

<span data-ttu-id="26451-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="26451-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="26451-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="26451-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="26451-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="26451-107">Syntax</span></span>


```mof
uint32 EnableIPFilterSec(
  [in] boolean IPFilterSecurityEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="26451-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="26451-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26451-109">*Ипфилтерсекуритенаблед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="26451-109">*IPFilterSecurityEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26451-110">Если **значение — true**, протокол IPsec включен глобально для всех сетевых адаптеров, привязанных к IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="26451-110">If **true**, IPsec is enabled globally across all IP-bound network adapters.</span></span> <span data-ttu-id="26451-111">**Значение false** показывает, что весь трафик порта и протокола разрешен для нефильтрованного потока.</span><span class="sxs-lookup"><span data-stu-id="26451-111">If **false**, all port and protocol traffic is allowed to flow unfiltered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26451-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="26451-112">Return value</span></span>

<span data-ttu-id="26451-113">Возвращает значение 0 (ноль) для успешного завершения, если перезагрузка не требуется, 1 (один) для успешного завершения, когда требуется перезагрузка, и любое другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="26451-113">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="26451-114">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="26451-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="26451-115">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="26451-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="26451-116">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="26451-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="26451-117">0</span><span class="sxs-lookup"><span data-stu-id="26451-117">0</span></span>

<span data-ttu-id="26451-118">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="26451-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="26451-119">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="26451-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="26451-120">1</span><span class="sxs-lookup"><span data-stu-id="26451-120">1</span></span>

<span data-ttu-id="26451-121">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="26451-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="26451-122">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="26451-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="26451-123">64</span><span class="sxs-lookup"><span data-stu-id="26451-123">64</span></span>

<span data-ttu-id="26451-124">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="26451-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="26451-125">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="26451-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="26451-126">65</span><span class="sxs-lookup"><span data-stu-id="26451-126">65</span></span>

<span data-ttu-id="26451-127">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="26451-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="26451-128">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="26451-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="26451-129">66</span><span class="sxs-lookup"><span data-stu-id="26451-129">66</span></span>

<span data-ttu-id="26451-130">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="26451-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="26451-131">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="26451-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="26451-132">67</span><span class="sxs-lookup"><span data-stu-id="26451-132">67</span></span>

<span data-ttu-id="26451-133">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="26451-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="26451-134">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="26451-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="26451-135">68</span><span class="sxs-lookup"><span data-stu-id="26451-135">68</span></span>

<span data-ttu-id="26451-136">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="26451-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="26451-137">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="26451-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="26451-138">69</span><span class="sxs-lookup"><span data-stu-id="26451-138">69</span></span>

<span data-ttu-id="26451-139">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="26451-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="26451-140">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="26451-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="26451-141">70</span><span class="sxs-lookup"><span data-stu-id="26451-141">70</span></span>

<span data-ttu-id="26451-142">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="26451-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="26451-143">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="26451-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="26451-144">71</span><span class="sxs-lookup"><span data-stu-id="26451-144">71</span></span>

<span data-ttu-id="26451-145">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="26451-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="26451-146">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="26451-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="26451-147">72</span><span class="sxs-lookup"><span data-stu-id="26451-147">72</span></span>

<span data-ttu-id="26451-148">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="26451-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="26451-149">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="26451-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="26451-150">73</span><span class="sxs-lookup"><span data-stu-id="26451-150">73</span></span>

<span data-ttu-id="26451-151">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="26451-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="26451-152">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="26451-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="26451-153">74</span><span class="sxs-lookup"><span data-stu-id="26451-153">74</span></span>

<span data-ttu-id="26451-154">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="26451-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="26451-155">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="26451-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="26451-156">75</span><span class="sxs-lookup"><span data-stu-id="26451-156">75</span></span>

<span data-ttu-id="26451-157">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="26451-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="26451-158">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="26451-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="26451-159">76</span><span class="sxs-lookup"><span data-stu-id="26451-159">76</span></span>

<span data-ttu-id="26451-160">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="26451-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="26451-161">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="26451-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="26451-162">77</span><span class="sxs-lookup"><span data-stu-id="26451-162">77</span></span>

<span data-ttu-id="26451-163">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="26451-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="26451-164">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="26451-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="26451-165">78</span><span class="sxs-lookup"><span data-stu-id="26451-165">78</span></span>

<span data-ttu-id="26451-166">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="26451-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="26451-167">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="26451-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="26451-168">79</span><span class="sxs-lookup"><span data-stu-id="26451-168">79</span></span>

<span data-ttu-id="26451-169">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="26451-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="26451-170">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="26451-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="26451-171">80</span><span class="sxs-lookup"><span data-stu-id="26451-171">80</span></span>

<span data-ttu-id="26451-172">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="26451-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="26451-173">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="26451-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="26451-174">81</span><span class="sxs-lookup"><span data-stu-id="26451-174">81</span></span>

<span data-ttu-id="26451-175">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="26451-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="26451-176">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="26451-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="26451-177">82</span><span class="sxs-lookup"><span data-stu-id="26451-177">82</span></span>

<span data-ttu-id="26451-178">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="26451-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="26451-179">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="26451-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="26451-180">83</span><span class="sxs-lookup"><span data-stu-id="26451-180">83</span></span>

<span data-ttu-id="26451-181">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="26451-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="26451-182">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="26451-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="26451-183">84</span><span class="sxs-lookup"><span data-stu-id="26451-183">84</span></span>

<span data-ttu-id="26451-184">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="26451-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="26451-185">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="26451-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="26451-186">85</span><span class="sxs-lookup"><span data-stu-id="26451-186">85</span></span>

<span data-ttu-id="26451-187">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="26451-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="26451-188">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="26451-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="26451-189">86</span><span class="sxs-lookup"><span data-stu-id="26451-189">86</span></span>

<span data-ttu-id="26451-190">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="26451-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="26451-191">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="26451-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="26451-192">87</span><span class="sxs-lookup"><span data-stu-id="26451-192">87</span></span>

<span data-ttu-id="26451-193">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="26451-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="26451-194">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="26451-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="26451-195">88</span><span class="sxs-lookup"><span data-stu-id="26451-195">88</span></span>

<span data-ttu-id="26451-196">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="26451-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="26451-197">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="26451-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="26451-198">89</span><span class="sxs-lookup"><span data-stu-id="26451-198">89</span></span>

<span data-ttu-id="26451-199">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="26451-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="26451-200">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="26451-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="26451-201">90</span><span class="sxs-lookup"><span data-stu-id="26451-201">90</span></span>

<span data-ttu-id="26451-202">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="26451-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="26451-203">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="26451-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="26451-204">91</span><span class="sxs-lookup"><span data-stu-id="26451-204">91</span></span>

<span data-ttu-id="26451-205">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="26451-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="26451-206">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="26451-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="26451-207">92</span><span class="sxs-lookup"><span data-stu-id="26451-207">92</span></span>

<span data-ttu-id="26451-208">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="26451-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="26451-209">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="26451-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="26451-210">93</span><span class="sxs-lookup"><span data-stu-id="26451-210">93</span></span>

<span data-ttu-id="26451-211">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="26451-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="26451-212">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="26451-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="26451-213">94</span><span class="sxs-lookup"><span data-stu-id="26451-213">94</span></span>

<span data-ttu-id="26451-214">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="26451-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="26451-215">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="26451-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="26451-216">95</span><span class="sxs-lookup"><span data-stu-id="26451-216">95</span></span>

<span data-ttu-id="26451-217">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="26451-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="26451-218">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="26451-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="26451-219">96</span><span class="sxs-lookup"><span data-stu-id="26451-219">96</span></span>

<span data-ttu-id="26451-220">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="26451-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="26451-221">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="26451-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="26451-222">97</span><span class="sxs-lookup"><span data-stu-id="26451-222">97</span></span>

<span data-ttu-id="26451-223">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="26451-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="26451-224">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="26451-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="26451-225">98</span><span class="sxs-lookup"><span data-stu-id="26451-225">98</span></span>

<span data-ttu-id="26451-226">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="26451-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="26451-227">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="26451-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="26451-228">100</span><span class="sxs-lookup"><span data-stu-id="26451-228">100</span></span>

<span data-ttu-id="26451-229">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="26451-229">DHCP not enabled on the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="26451-230">**Другое**</span><span class="sxs-lookup"><span data-stu-id="26451-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="26451-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="26451-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="26451-232">Комментарии</span><span class="sxs-lookup"><span data-stu-id="26451-232">Remarks</span></span>

<span data-ttu-id="26451-233">При включенной системе безопасности характеристики операционной безопасности для любого сетевого адаптера можно контролировать с помощью метода [**енаблеипсек**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="26451-233">With security enabled, the operational security characteristics for any one network adapter can be controlled by using the network adapter-specific [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="26451-234">Примеры</span><span class="sxs-lookup"><span data-stu-id="26451-234">Examples</span></span>

<span data-ttu-id="26451-235">Следующий код, взятый из примера [включения безопасности ипфилтер для всех сетевых адаптеров](https://Gallery.TechNet.Microsoft.Com/f8e56021-5a54-4554-b7b6-d76cc40d8d1d) в коллекции TechNet, обеспечивает безопасность IP-фильтра для всех сетевых адаптеров, установленных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="26451-235">The following code, taken from the [Enable IPFilter Security on All Network Adapters](https://Gallery.TechNet.Microsoft.Com/f8e56021-5a54-4554-b7b6-d76cc40d8d1d) sample on TechNet Gallery, enables IP filter security for all the network adapters installed in a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objNetworkSettings = objWMIService.Get("Win32_NetworkAdapterConfiguration") 
objNetworkSettings.EnableIPFilterSec(True)
```



## <a name="requirements"></a><span data-ttu-id="26451-236">Требования</span><span class="sxs-lookup"><span data-stu-id="26451-236">Requirements</span></span>



| <span data-ttu-id="26451-237">Требование</span><span class="sxs-lookup"><span data-stu-id="26451-237">Requirement</span></span> | <span data-ttu-id="26451-238">Значение</span><span class="sxs-lookup"><span data-stu-id="26451-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26451-239">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="26451-239">Minimum supported client</span></span><br/> | <span data-ttu-id="26451-240">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="26451-240">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="26451-241">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="26451-241">Minimum supported server</span></span><br/> | <span data-ttu-id="26451-242">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26451-242">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="26451-243">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="26451-243">Namespace</span></span><br/>                | <span data-ttu-id="26451-244">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="26451-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="26451-245">MOF</span><span class="sxs-lookup"><span data-stu-id="26451-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26451-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="26451-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="26451-247">DLL</span><span class="sxs-lookup"><span data-stu-id="26451-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26451-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26451-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26451-249">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26451-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26451-250">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="26451-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="26451-251">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="26451-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="26451-252">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="26451-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="26451-253">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="26451-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="26451-254">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="26451-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

