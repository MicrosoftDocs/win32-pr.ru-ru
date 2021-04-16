---
description: Метод класса WMI ReleaseDHCPLease освобождает IP-адрес, привязанный к конкретному сетевому адаптеру с поддержкой DHCP.
ms.assetid: 0cf4b531-8626-4388-bffa-e16a4aa8c794
ms.tgt_platform: multiple
title: Метод ReleaseDHCPLease класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.ReleaseDHCPLease
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5520a6b2d0960c1d4258b19f8cd4d600c9b8fe34
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655998"
---
# <a name="releasedhcplease-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="7cf03-103">Метод ReleaseDHCPLease \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="7cf03-103">ReleaseDHCPLease method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="7cf03-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) ReleaseDHCPLease освобождает IP-адрес, привязанный к конкретному сетевому адаптеру с поддержкой DHCP.</span><span class="sxs-lookup"><span data-stu-id="7cf03-104">The **ReleaseDHCPLease** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method releases the IP address bound to a specific DHCP-enabled network adapter.</span></span>

<span data-ttu-id="7cf03-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="7cf03-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7cf03-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="7cf03-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7cf03-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7cf03-107">Syntax</span></span>


```mof
uint32 ReleaseDHCPLease();
```



## <a name="parameters"></a><span data-ttu-id="7cf03-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7cf03-108">Parameters</span></span>

<span data-ttu-id="7cf03-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7cf03-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7cf03-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7cf03-110">Return value</span></span>

<span data-ttu-id="7cf03-111">Возвращает значение 0 (ноль) для успешного завершения, если не требуется перезагрузка, 1 (один) для успешного завершения, когда требуется перезагрузка, и другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="7cf03-111">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="7cf03-112">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="7cf03-112">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="7cf03-113">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="7cf03-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="7cf03-114">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="7cf03-114">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-115">0</span><span class="sxs-lookup"><span data-stu-id="7cf03-115">0</span></span>

<span data-ttu-id="7cf03-116">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="7cf03-116">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-117">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="7cf03-117">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-118">1</span><span class="sxs-lookup"><span data-stu-id="7cf03-118">1</span></span>

<span data-ttu-id="7cf03-119">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="7cf03-119">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-120">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="7cf03-120">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-121">64</span><span class="sxs-lookup"><span data-stu-id="7cf03-121">64</span></span>

<span data-ttu-id="7cf03-122">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="7cf03-122">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-123">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="7cf03-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-124">65</span><span class="sxs-lookup"><span data-stu-id="7cf03-124">65</span></span>

<span data-ttu-id="7cf03-125">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="7cf03-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-126">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="7cf03-126">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-127">66</span><span class="sxs-lookup"><span data-stu-id="7cf03-127">66</span></span>

<span data-ttu-id="7cf03-128">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="7cf03-128">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-129">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="7cf03-129">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-130">67</span><span class="sxs-lookup"><span data-stu-id="7cf03-130">67</span></span>

<span data-ttu-id="7cf03-131">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7cf03-131">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-132">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="7cf03-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-133">68</span><span class="sxs-lookup"><span data-stu-id="7cf03-133">68</span></span>

<span data-ttu-id="7cf03-134">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="7cf03-134">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-135">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="7cf03-135">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-136">69</span><span class="sxs-lookup"><span data-stu-id="7cf03-136">69</span></span>

<span data-ttu-id="7cf03-137">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="7cf03-137">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-138">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="7cf03-138">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-139">70</span><span class="sxs-lookup"><span data-stu-id="7cf03-139">70</span></span>

<span data-ttu-id="7cf03-140">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="7cf03-140">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-141">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="7cf03-141">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-142">71</span><span class="sxs-lookup"><span data-stu-id="7cf03-142">71</span></span>

<span data-ttu-id="7cf03-143">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="7cf03-143">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-144">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="7cf03-144">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-145">72</span><span class="sxs-lookup"><span data-stu-id="7cf03-145">72</span></span>

<span data-ttu-id="7cf03-146">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="7cf03-146">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-147">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="7cf03-147">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-148">73</span><span class="sxs-lookup"><span data-stu-id="7cf03-148">73</span></span>

<span data-ttu-id="7cf03-149">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="7cf03-149">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-150">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="7cf03-150">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-151">74</span><span class="sxs-lookup"><span data-stu-id="7cf03-151">74</span></span>

<span data-ttu-id="7cf03-152">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="7cf03-152">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-153">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="7cf03-153">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-154">75</span><span class="sxs-lookup"><span data-stu-id="7cf03-154">75</span></span>

<span data-ttu-id="7cf03-155">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="7cf03-155">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-156">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="7cf03-156">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-157">76</span><span class="sxs-lookup"><span data-stu-id="7cf03-157">76</span></span>

<span data-ttu-id="7cf03-158">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="7cf03-158">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-159">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="7cf03-159">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-160">77</span><span class="sxs-lookup"><span data-stu-id="7cf03-160">77</span></span>

<span data-ttu-id="7cf03-161">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="7cf03-161">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-162">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="7cf03-162">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-163">78</span><span class="sxs-lookup"><span data-stu-id="7cf03-163">78</span></span>

<span data-ttu-id="7cf03-164">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="7cf03-164">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-165">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="7cf03-165">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-166">79</span><span class="sxs-lookup"><span data-stu-id="7cf03-166">79</span></span>

<span data-ttu-id="7cf03-167">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="7cf03-167">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-168">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="7cf03-168">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-169">80</span><span class="sxs-lookup"><span data-stu-id="7cf03-169">80</span></span>

<span data-ttu-id="7cf03-170">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="7cf03-170">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-171">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="7cf03-171">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-172">81</span><span class="sxs-lookup"><span data-stu-id="7cf03-172">81</span></span>

<span data-ttu-id="7cf03-173">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="7cf03-173">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-174">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="7cf03-174">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-175">82</span><span class="sxs-lookup"><span data-stu-id="7cf03-175">82</span></span>

<span data-ttu-id="7cf03-176">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="7cf03-176">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-177">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="7cf03-177">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-178">83</span><span class="sxs-lookup"><span data-stu-id="7cf03-178">83</span></span>

<span data-ttu-id="7cf03-179">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="7cf03-179">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-180">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="7cf03-180">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-181">84</span><span class="sxs-lookup"><span data-stu-id="7cf03-181">84</span></span>

<span data-ttu-id="7cf03-182">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="7cf03-182">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-183">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="7cf03-183">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-184">85</span><span class="sxs-lookup"><span data-stu-id="7cf03-184">85</span></span>

<span data-ttu-id="7cf03-185">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="7cf03-185">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-186">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="7cf03-186">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-187">86</span><span class="sxs-lookup"><span data-stu-id="7cf03-187">86</span></span>

<span data-ttu-id="7cf03-188">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="7cf03-188">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-189">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="7cf03-189">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-190">87</span><span class="sxs-lookup"><span data-stu-id="7cf03-190">87</span></span>

<span data-ttu-id="7cf03-191">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="7cf03-191">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-192">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="7cf03-192">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-193">88</span><span class="sxs-lookup"><span data-stu-id="7cf03-193">88</span></span>

<span data-ttu-id="7cf03-194">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="7cf03-194">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-195">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="7cf03-195">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-196">89</span><span class="sxs-lookup"><span data-stu-id="7cf03-196">89</span></span>

<span data-ttu-id="7cf03-197">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="7cf03-197">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-198">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="7cf03-198">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-199">90</span><span class="sxs-lookup"><span data-stu-id="7cf03-199">90</span></span>

<span data-ttu-id="7cf03-200">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="7cf03-200">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-201">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="7cf03-201">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-202">91</span><span class="sxs-lookup"><span data-stu-id="7cf03-202">91</span></span>

<span data-ttu-id="7cf03-203">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="7cf03-203">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-204">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="7cf03-204">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-205">92</span><span class="sxs-lookup"><span data-stu-id="7cf03-205">92</span></span>

<span data-ttu-id="7cf03-206">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="7cf03-206">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-207">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="7cf03-207">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-208">93</span><span class="sxs-lookup"><span data-stu-id="7cf03-208">93</span></span>

<span data-ttu-id="7cf03-209">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="7cf03-209">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-210">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="7cf03-210">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-211">94</span><span class="sxs-lookup"><span data-stu-id="7cf03-211">94</span></span>

<span data-ttu-id="7cf03-212">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="7cf03-212">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-213">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="7cf03-213">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-214">95</span><span class="sxs-lookup"><span data-stu-id="7cf03-214">95</span></span>

<span data-ttu-id="7cf03-215">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="7cf03-215">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-216">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="7cf03-216">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-217">96</span><span class="sxs-lookup"><span data-stu-id="7cf03-217">96</span></span>

<span data-ttu-id="7cf03-218">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="7cf03-218">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-219">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="7cf03-219">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-220">97</span><span class="sxs-lookup"><span data-stu-id="7cf03-220">97</span></span>

<span data-ttu-id="7cf03-221">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="7cf03-221">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-222">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="7cf03-222">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-223">98</span><span class="sxs-lookup"><span data-stu-id="7cf03-223">98</span></span>

<span data-ttu-id="7cf03-224">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="7cf03-224">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-225">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="7cf03-225">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-226">100</span><span class="sxs-lookup"><span data-stu-id="7cf03-226">100</span></span>

<span data-ttu-id="7cf03-227">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="7cf03-227">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="7cf03-228">**Другое**</span><span class="sxs-lookup"><span data-stu-id="7cf03-228">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="7cf03-229">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="7cf03-229">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7cf03-230">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7cf03-230">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="7cf03-231">Если DHCP включен на локальном компьютере, параметр отключает TCP/IP для этого конкретного сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="7cf03-231">If DHCP is enabled on the local computer system, the option disables TCP/IP on this specific network adapter.</span></span> <span data-ttu-id="7cf03-232">Если нет альтернативного пути к целевой системе, то есть другим связанным с TCP/IP сетевым адаптером, все связи TCP/IP будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="7cf03-232">Unless you have an alternate path to the target system, that is, another TCP/IP bound network adapter, all TCP/IP communications will be lost.</span></span>

 

## <a name="examples"></a><span data-ttu-id="7cf03-233">Примеры</span><span class="sxs-lookup"><span data-stu-id="7cf03-233">Examples</span></span>

<span data-ttu-id="7cf03-234">В этом примере для [обновления IP-адресов с помощью PowerShell](https://Gallery.TechNet.Microsoft.Com/Renew-IP-Adresses-Using-365f6bfa) PowerShell в коллекции TechNet используется **ReleaseDHCPLease** для выпуска и продления IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="7cf03-234">The [Release Renew IP Adresses Using PowerShell](https://Gallery.TechNet.Microsoft.Com/Renew-IP-Adresses-Using-365f6bfa) PowerShell example on TechNet Gallery uses **ReleaseDHCPLease** to release and renew an IP address.</span></span>

<span data-ttu-id="7cf03-235">Следующий код VBScript освобождает аренду DHCP для всех сетевых адаптеров, привязанных к TCP/IP, на компьютере.</span><span class="sxs-lookup"><span data-stu-id="7cf03-235">The following VBScript code releases the DHCP leases for all TCP/IP-bound network adapters on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colNetCards = objWMIService.ExecQuery _ 
    ("Select * From Win32_NetworkAdapterConfiguration Where IPEnabled = True") 
 
For Each objNetCard in colNetCards 
    objNetCard.ReleaseDHCPLease() 
Next 
```



## <a name="requirements"></a><span data-ttu-id="7cf03-236">Требования</span><span class="sxs-lookup"><span data-stu-id="7cf03-236">Requirements</span></span>



| <span data-ttu-id="7cf03-237">Требование</span><span class="sxs-lookup"><span data-stu-id="7cf03-237">Requirement</span></span> | <span data-ttu-id="7cf03-238">Значение</span><span class="sxs-lookup"><span data-stu-id="7cf03-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7cf03-239">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7cf03-239">Minimum supported client</span></span><br/> | <span data-ttu-id="7cf03-240">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7cf03-240">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7cf03-241">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7cf03-241">Minimum supported server</span></span><br/> | <span data-ttu-id="7cf03-242">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7cf03-242">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7cf03-243">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7cf03-243">Namespace</span></span><br/>                | <span data-ttu-id="7cf03-244">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7cf03-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7cf03-245">MOF</span><span class="sxs-lookup"><span data-stu-id="7cf03-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7cf03-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7cf03-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7cf03-247">DLL</span><span class="sxs-lookup"><span data-stu-id="7cf03-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cf03-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cf03-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cf03-249">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7cf03-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cf03-250">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="7cf03-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="7cf03-251">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="7cf03-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="7cf03-252">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="7cf03-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="7cf03-253">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="7cf03-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="7cf03-254">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="7cf03-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

