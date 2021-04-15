---
description: Метод класса WMI Дисаблеипсек используется для отключения протокола IPsec на этом сетевом адаптере с поддержкой TCP/IP.
ms.assetid: 6fff2721-1ee2-42b4-bbf9-fd36b97318e3
ms.tgt_platform: multiple
title: Метод Дисаблеипсек класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.DisableIPSec
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9b2a17bbfa0f10c08edb581b4a4bf51173facfea
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655804"
---
# <a name="disableipsec-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="81de6-103">Метод Дисаблеипсек \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="81de6-103">DisableIPSec method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="81de6-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) Дисаблеипсек используется для отключения протокола IPSec на этом сетевом адаптере с поддержкой TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="81de6-104">The **DisableIPSec** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method is used to disable Internet Protocol security (IPsec) on this TCP/IP-enabled network adapter.</span></span>

<span data-ttu-id="81de6-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="81de6-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="81de6-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="81de6-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="81de6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="81de6-107">Syntax</span></span>


```mof
uint32 DisableIPSec();
```



## <a name="parameters"></a><span data-ttu-id="81de6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="81de6-108">Parameters</span></span>

<span data-ttu-id="81de6-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="81de6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="81de6-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81de6-110">Return value</span></span>

<span data-ttu-id="81de6-111">Возвращает значение 0 (ноль) для успешного завершения, если перезагрузка не требуется, 1 (один) для успешного завершения, когда требуется перезагрузка, и любое другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="81de6-111">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="81de6-112">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="81de6-112">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="81de6-113">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="81de6-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="81de6-114">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="81de6-114">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-115">0</span><span class="sxs-lookup"><span data-stu-id="81de6-115">0</span></span>

<span data-ttu-id="81de6-116">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="81de6-116">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-117">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="81de6-117">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-118">1</span><span class="sxs-lookup"><span data-stu-id="81de6-118">1</span></span>

<span data-ttu-id="81de6-119">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="81de6-119">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-120">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="81de6-120">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-121">64</span><span class="sxs-lookup"><span data-stu-id="81de6-121">64</span></span>

<span data-ttu-id="81de6-122">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="81de6-122">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-123">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="81de6-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-124">65</span><span class="sxs-lookup"><span data-stu-id="81de6-124">65</span></span>

<span data-ttu-id="81de6-125">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="81de6-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-126">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="81de6-126">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-127">66</span><span class="sxs-lookup"><span data-stu-id="81de6-127">66</span></span>

<span data-ttu-id="81de6-128">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="81de6-128">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-129">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="81de6-129">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-130">67</span><span class="sxs-lookup"><span data-stu-id="81de6-130">67</span></span>

<span data-ttu-id="81de6-131">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="81de6-131">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-132">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="81de6-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-133">68</span><span class="sxs-lookup"><span data-stu-id="81de6-133">68</span></span>

<span data-ttu-id="81de6-134">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="81de6-134">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-135">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="81de6-135">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-136">69</span><span class="sxs-lookup"><span data-stu-id="81de6-136">69</span></span>

<span data-ttu-id="81de6-137">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="81de6-137">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-138">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="81de6-138">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-139">70</span><span class="sxs-lookup"><span data-stu-id="81de6-139">70</span></span>

<span data-ttu-id="81de6-140">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="81de6-140">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-141">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="81de6-141">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-142">71</span><span class="sxs-lookup"><span data-stu-id="81de6-142">71</span></span>

<span data-ttu-id="81de6-143">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="81de6-143">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-144">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="81de6-144">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-145">72</span><span class="sxs-lookup"><span data-stu-id="81de6-145">72</span></span>

<span data-ttu-id="81de6-146">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="81de6-146">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-147">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="81de6-147">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-148">73</span><span class="sxs-lookup"><span data-stu-id="81de6-148">73</span></span>

<span data-ttu-id="81de6-149">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="81de6-149">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-150">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="81de6-150">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-151">74</span><span class="sxs-lookup"><span data-stu-id="81de6-151">74</span></span>

<span data-ttu-id="81de6-152">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="81de6-152">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-153">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="81de6-153">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-154">75</span><span class="sxs-lookup"><span data-stu-id="81de6-154">75</span></span>

<span data-ttu-id="81de6-155">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="81de6-155">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-156">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="81de6-156">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-157">76</span><span class="sxs-lookup"><span data-stu-id="81de6-157">76</span></span>

<span data-ttu-id="81de6-158">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="81de6-158">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-159">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="81de6-159">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-160">77</span><span class="sxs-lookup"><span data-stu-id="81de6-160">77</span></span>

<span data-ttu-id="81de6-161">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="81de6-161">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-162">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="81de6-162">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-163">78</span><span class="sxs-lookup"><span data-stu-id="81de6-163">78</span></span>

<span data-ttu-id="81de6-164">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="81de6-164">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-165">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="81de6-165">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-166">79</span><span class="sxs-lookup"><span data-stu-id="81de6-166">79</span></span>

<span data-ttu-id="81de6-167">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="81de6-167">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-168">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="81de6-168">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-169">80</span><span class="sxs-lookup"><span data-stu-id="81de6-169">80</span></span>

<span data-ttu-id="81de6-170">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="81de6-170">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-171">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="81de6-171">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-172">81</span><span class="sxs-lookup"><span data-stu-id="81de6-172">81</span></span>

<span data-ttu-id="81de6-173">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="81de6-173">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-174">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="81de6-174">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-175">82</span><span class="sxs-lookup"><span data-stu-id="81de6-175">82</span></span>

<span data-ttu-id="81de6-176">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="81de6-176">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-177">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="81de6-177">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-178">83</span><span class="sxs-lookup"><span data-stu-id="81de6-178">83</span></span>

<span data-ttu-id="81de6-179">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="81de6-179">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-180">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="81de6-180">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-181">84</span><span class="sxs-lookup"><span data-stu-id="81de6-181">84</span></span>

<span data-ttu-id="81de6-182">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="81de6-182">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-183">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="81de6-183">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-184">85</span><span class="sxs-lookup"><span data-stu-id="81de6-184">85</span></span>

<span data-ttu-id="81de6-185">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="81de6-185">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-186">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="81de6-186">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-187">86</span><span class="sxs-lookup"><span data-stu-id="81de6-187">86</span></span>

<span data-ttu-id="81de6-188">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="81de6-188">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-189">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="81de6-189">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-190">87</span><span class="sxs-lookup"><span data-stu-id="81de6-190">87</span></span>

<span data-ttu-id="81de6-191">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="81de6-191">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-192">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="81de6-192">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-193">88</span><span class="sxs-lookup"><span data-stu-id="81de6-193">88</span></span>

<span data-ttu-id="81de6-194">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="81de6-194">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-195">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="81de6-195">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-196">89</span><span class="sxs-lookup"><span data-stu-id="81de6-196">89</span></span>

<span data-ttu-id="81de6-197">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="81de6-197">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-198">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="81de6-198">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-199">90</span><span class="sxs-lookup"><span data-stu-id="81de6-199">90</span></span>

<span data-ttu-id="81de6-200">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="81de6-200">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-201">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="81de6-201">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-202">91</span><span class="sxs-lookup"><span data-stu-id="81de6-202">91</span></span>

<span data-ttu-id="81de6-203">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="81de6-203">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-204">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="81de6-204">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-205">92</span><span class="sxs-lookup"><span data-stu-id="81de6-205">92</span></span>

<span data-ttu-id="81de6-206">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="81de6-206">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-207">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="81de6-207">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-208">93</span><span class="sxs-lookup"><span data-stu-id="81de6-208">93</span></span>

<span data-ttu-id="81de6-209">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="81de6-209">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-210">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="81de6-210">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-211">94</span><span class="sxs-lookup"><span data-stu-id="81de6-211">94</span></span>

<span data-ttu-id="81de6-212">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="81de6-212">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-213">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="81de6-213">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-214">95</span><span class="sxs-lookup"><span data-stu-id="81de6-214">95</span></span>

<span data-ttu-id="81de6-215">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="81de6-215">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-216">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="81de6-216">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-217">96</span><span class="sxs-lookup"><span data-stu-id="81de6-217">96</span></span>

<span data-ttu-id="81de6-218">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="81de6-218">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-219">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="81de6-219">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-220">97</span><span class="sxs-lookup"><span data-stu-id="81de6-220">97</span></span>

<span data-ttu-id="81de6-221">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="81de6-221">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-222">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="81de6-222">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-223">98</span><span class="sxs-lookup"><span data-stu-id="81de6-223">98</span></span>

<span data-ttu-id="81de6-224">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="81de6-224">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-225">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="81de6-225">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-226">100</span><span class="sxs-lookup"><span data-stu-id="81de6-226">100</span></span>

<span data-ttu-id="81de6-227">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="81de6-227">DHCP not enabled on the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="81de6-228">**Другое**</span><span class="sxs-lookup"><span data-stu-id="81de6-228">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="81de6-229">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="81de6-229">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="81de6-230">Примеры</span><span class="sxs-lookup"><span data-stu-id="81de6-230">Examples</span></span>

<span data-ttu-id="81de6-231">Следующий пример сценария VBScript отключает IP-безопасность на компьютере.</span><span class="sxs-lookup"><span data-stu-id="81de6-231">The following VBScript sample disables the IP Security on a computer.</span></span> <span data-ttu-id="81de6-232">Обратите внимание, что в целях безопасности фактический вызов Дисаблеипсек записывается в комментарий.</span><span class="sxs-lookup"><span data-stu-id="81de6-232">Note that the actual call to DisableIPSec is commented out, for safety purposes.</span></span>


```VB
strServer = "."

Set objWMI = GetObject("winmgmts:\\" & strServer & "\root\cimv2")

strWQL = "select * from Win32_NetworkAdapterConfiguration"
Set objInstances = objWMI.ExecQuery(strWQL,,48)

For Each objInstance in objInstances

 ' Uncomment next line to disable security
 ' intResult = objInstance.DisableIPSec

Next
```



## <a name="requirements"></a><span data-ttu-id="81de6-233">Требования</span><span class="sxs-lookup"><span data-stu-id="81de6-233">Requirements</span></span>



| <span data-ttu-id="81de6-234">Требование</span><span class="sxs-lookup"><span data-stu-id="81de6-234">Requirement</span></span> | <span data-ttu-id="81de6-235">Значение</span><span class="sxs-lookup"><span data-stu-id="81de6-235">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81de6-236">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="81de6-236">Minimum supported client</span></span><br/> | <span data-ttu-id="81de6-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81de6-237">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="81de6-238">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="81de6-238">Minimum supported server</span></span><br/> | <span data-ttu-id="81de6-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81de6-239">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="81de6-240">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="81de6-240">Namespace</span></span><br/>                | <span data-ttu-id="81de6-241">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="81de6-241">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="81de6-242">MOF</span><span class="sxs-lookup"><span data-stu-id="81de6-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81de6-243"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81de6-243"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="81de6-244">DLL</span><span class="sxs-lookup"><span data-stu-id="81de6-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81de6-245"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81de6-245"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81de6-246">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81de6-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81de6-247">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="81de6-247">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="81de6-248">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="81de6-248">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="81de6-249">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="81de6-249">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="81de6-250">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="81de6-250">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="81de6-251">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="81de6-251">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

