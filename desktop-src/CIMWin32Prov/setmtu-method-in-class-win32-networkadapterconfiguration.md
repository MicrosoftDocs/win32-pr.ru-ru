---
description: Статический метод класса Сетмту WMI используется для установки максимального значения MTU для сетевого интерфейса по умолчанию.
ms.assetid: 262c8bd7-1057-4204-80ab-725c60fc9c52
ms.tgt_platform: multiple
title: Метод Сетмту класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetMTU
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 466c344892f2c4bf4a1e979ac9c1f50cd709325a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807577"
---
# <a name="setmtu-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="1bd02-103">Метод Сетмту \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="1bd02-103">SetMTU method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="1bd02-104">Статический метод класса **сетмту** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) используется для установки максимального значения MTU для сетевого интерфейса по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1bd02-104">The **SetMTU** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the default Maximum Transmission Unit (MTU) for a network interface.</span></span>

<span data-ttu-id="1bd02-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="1bd02-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1bd02-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1bd02-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1bd02-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1bd02-107">Syntax</span></span>


```mof
uint32 SetMTU(
  [in] uint32 MTU
);
```



## <a name="parameters"></a><span data-ttu-id="1bd02-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1bd02-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bd02-109">*MTU* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1bd02-109">*MTU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-110">Максимальный размер блока передачи (MTU) для сетевого интерфейса по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1bd02-110">Default Maximum Transmission Unit (MTU) for a network interface.</span></span> <span data-ttu-id="1bd02-111">Диапазон этого значения охватывает минимальный размер пакета (68) до MTU, поддерживаемый базовой сетью.</span><span class="sxs-lookup"><span data-stu-id="1bd02-111">The range of this value spans the minimum packet size (68) to the MTU supported by the underlying network.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bd02-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1bd02-112">Return value</span></span>

<span data-ttu-id="1bd02-113">Возвращает значение 0 (ноль) для успешного завершения, если не требуется перезагрузка, 1 (один) для успешного завершения, когда требуется перезагрузка, и другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="1bd02-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="1bd02-114">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="1bd02-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="1bd02-115">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="1bd02-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="1bd02-116">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="1bd02-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-117">0</span><span class="sxs-lookup"><span data-stu-id="1bd02-117">0</span></span>

<span data-ttu-id="1bd02-118">Успешное завершение.</span><span class="sxs-lookup"><span data-stu-id="1bd02-118">Successful completion.</span></span> <span data-ttu-id="1bd02-119">Перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="1bd02-119">No reboot is required.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-120">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="1bd02-120">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-121">1</span><span class="sxs-lookup"><span data-stu-id="1bd02-121">1</span></span>

<span data-ttu-id="1bd02-122">Успешное завершение.</span><span class="sxs-lookup"><span data-stu-id="1bd02-122">Successful completion.</span></span> <span data-ttu-id="1bd02-123">Потребуется перезагрузка компьютера.</span><span class="sxs-lookup"><span data-stu-id="1bd02-123">Reboot is required.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-124">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="1bd02-124">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-125">64</span><span class="sxs-lookup"><span data-stu-id="1bd02-125">64</span></span>

<span data-ttu-id="1bd02-126">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="1bd02-126">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-127">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="1bd02-127">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-128">65</span><span class="sxs-lookup"><span data-stu-id="1bd02-128">65</span></span>

<span data-ttu-id="1bd02-129">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="1bd02-129">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-130">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="1bd02-130">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-131">66</span><span class="sxs-lookup"><span data-stu-id="1bd02-131">66</span></span>

<span data-ttu-id="1bd02-132">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="1bd02-132">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-133">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="1bd02-133">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-134">67</span><span class="sxs-lookup"><span data-stu-id="1bd02-134">67</span></span>

<span data-ttu-id="1bd02-135">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1bd02-135">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-136">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="1bd02-136">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-137">68</span><span class="sxs-lookup"><span data-stu-id="1bd02-137">68</span></span>

<span data-ttu-id="1bd02-138">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="1bd02-138">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-139">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="1bd02-139">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-140">69</span><span class="sxs-lookup"><span data-stu-id="1bd02-140">69</span></span>

<span data-ttu-id="1bd02-141">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="1bd02-141">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-142">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="1bd02-142">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-143">70</span><span class="sxs-lookup"><span data-stu-id="1bd02-143">70</span></span>

<span data-ttu-id="1bd02-144">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="1bd02-144">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-145">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="1bd02-145">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-146">71</span><span class="sxs-lookup"><span data-stu-id="1bd02-146">71</span></span>

<span data-ttu-id="1bd02-147">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="1bd02-147">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-148">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="1bd02-148">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-149">72</span><span class="sxs-lookup"><span data-stu-id="1bd02-149">72</span></span>

<span data-ttu-id="1bd02-150">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="1bd02-150">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-151">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="1bd02-151">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-152">73</span><span class="sxs-lookup"><span data-stu-id="1bd02-152">73</span></span>

<span data-ttu-id="1bd02-153">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="1bd02-153">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-154">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="1bd02-154">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-155">74</span><span class="sxs-lookup"><span data-stu-id="1bd02-155">74</span></span>

<span data-ttu-id="1bd02-156">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="1bd02-156">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-157">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="1bd02-157">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-158">75</span><span class="sxs-lookup"><span data-stu-id="1bd02-158">75</span></span>

<span data-ttu-id="1bd02-159">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="1bd02-159">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-160">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="1bd02-160">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-161">76</span><span class="sxs-lookup"><span data-stu-id="1bd02-161">76</span></span>

<span data-ttu-id="1bd02-162">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="1bd02-162">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-163">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="1bd02-163">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-164">77</span><span class="sxs-lookup"><span data-stu-id="1bd02-164">77</span></span>

<span data-ttu-id="1bd02-165">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="1bd02-165">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-166">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="1bd02-166">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-167">78</span><span class="sxs-lookup"><span data-stu-id="1bd02-167">78</span></span>

<span data-ttu-id="1bd02-168">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="1bd02-168">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-169">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="1bd02-169">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-170">79</span><span class="sxs-lookup"><span data-stu-id="1bd02-170">79</span></span>

<span data-ttu-id="1bd02-171">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="1bd02-171">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-172">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="1bd02-172">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-173">80</span><span class="sxs-lookup"><span data-stu-id="1bd02-173">80</span></span>

<span data-ttu-id="1bd02-174">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="1bd02-174">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-175">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="1bd02-175">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-176">81</span><span class="sxs-lookup"><span data-stu-id="1bd02-176">81</span></span>

<span data-ttu-id="1bd02-177">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="1bd02-177">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-178">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="1bd02-178">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-179">82</span><span class="sxs-lookup"><span data-stu-id="1bd02-179">82</span></span>

<span data-ttu-id="1bd02-180">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="1bd02-180">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-181">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="1bd02-181">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-182">83</span><span class="sxs-lookup"><span data-stu-id="1bd02-182">83</span></span>

<span data-ttu-id="1bd02-183">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="1bd02-183">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-184">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="1bd02-184">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-185">84</span><span class="sxs-lookup"><span data-stu-id="1bd02-185">84</span></span>

<span data-ttu-id="1bd02-186">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="1bd02-186">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-187">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="1bd02-187">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-188">85</span><span class="sxs-lookup"><span data-stu-id="1bd02-188">85</span></span>

<span data-ttu-id="1bd02-189">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="1bd02-189">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-190">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="1bd02-190">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-191">86</span><span class="sxs-lookup"><span data-stu-id="1bd02-191">86</span></span>

<span data-ttu-id="1bd02-192">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="1bd02-192">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-193">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="1bd02-193">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-194">87</span><span class="sxs-lookup"><span data-stu-id="1bd02-194">87</span></span>

<span data-ttu-id="1bd02-195">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="1bd02-195">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-196">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="1bd02-196">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-197">88</span><span class="sxs-lookup"><span data-stu-id="1bd02-197">88</span></span>

<span data-ttu-id="1bd02-198">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="1bd02-198">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-199">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="1bd02-199">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-200">89</span><span class="sxs-lookup"><span data-stu-id="1bd02-200">89</span></span>

<span data-ttu-id="1bd02-201">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="1bd02-201">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-202">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="1bd02-202">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-203">90</span><span class="sxs-lookup"><span data-stu-id="1bd02-203">90</span></span>

<span data-ttu-id="1bd02-204">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="1bd02-204">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-205">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="1bd02-205">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-206">91</span><span class="sxs-lookup"><span data-stu-id="1bd02-206">91</span></span>

<span data-ttu-id="1bd02-207">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="1bd02-207">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-208">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="1bd02-208">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-209">92</span><span class="sxs-lookup"><span data-stu-id="1bd02-209">92</span></span>

<span data-ttu-id="1bd02-210">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="1bd02-210">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-211">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="1bd02-211">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-212">93</span><span class="sxs-lookup"><span data-stu-id="1bd02-212">93</span></span>

<span data-ttu-id="1bd02-213">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="1bd02-213">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-214">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="1bd02-214">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-215">94</span><span class="sxs-lookup"><span data-stu-id="1bd02-215">94</span></span>

<span data-ttu-id="1bd02-216">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="1bd02-216">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-217">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="1bd02-217">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-218">95</span><span class="sxs-lookup"><span data-stu-id="1bd02-218">95</span></span>

<span data-ttu-id="1bd02-219">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="1bd02-219">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-220">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="1bd02-220">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-221">96</span><span class="sxs-lookup"><span data-stu-id="1bd02-221">96</span></span>

<span data-ttu-id="1bd02-222">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="1bd02-222">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-223">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="1bd02-223">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-224">97</span><span class="sxs-lookup"><span data-stu-id="1bd02-224">97</span></span>

<span data-ttu-id="1bd02-225">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="1bd02-225">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-226">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="1bd02-226">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-227">98</span><span class="sxs-lookup"><span data-stu-id="1bd02-227">98</span></span>

<span data-ttu-id="1bd02-228">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="1bd02-228">Not all DHCP leases can be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-229">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="1bd02-229">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-230">100</span><span class="sxs-lookup"><span data-stu-id="1bd02-230">100</span></span>

<span data-ttu-id="1bd02-231">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="1bd02-231">DHCP is not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="1bd02-232">**Другое**</span><span class="sxs-lookup"><span data-stu-id="1bd02-232">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="1bd02-233">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="1bd02-233">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1bd02-234">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1bd02-234">Remarks</span></span>

<span data-ttu-id="1bd02-235">MTU — это максимальный размер пакета (в байтах), передаваемого транспортом в базовой сети.</span><span class="sxs-lookup"><span data-stu-id="1bd02-235">The MTU is the maximum packet size (in bytes) that a transport will transmit over the underlying network.</span></span> <span data-ttu-id="1bd02-236">Размер включает заголовок транспорта.</span><span class="sxs-lookup"><span data-stu-id="1bd02-236">The size includes the transport header.</span></span>

<span data-ttu-id="1bd02-237">Обратите внимание, что IP-датаграмма может охватывать несколько пакетов.</span><span class="sxs-lookup"><span data-stu-id="1bd02-237">Note that an IP datagram can span multiple packets.</span></span> <span data-ttu-id="1bd02-238">Значения, превышающие значение по умолчанию для базового результата сети в транспортном потоке, с использованием MTU по умолчанию сети.</span><span class="sxs-lookup"><span data-stu-id="1bd02-238">Values larger than the default for the underlying network result in the transport using the network default MTU.</span></span> <span data-ttu-id="1bd02-239">Значения меньше 68 приводят к транспортировке с использованием MTU 68.</span><span class="sxs-lookup"><span data-stu-id="1bd02-239">Values smaller than 68 result in the transport using an MTU of 68.</span></span>

## <a name="examples"></a><span data-ttu-id="1bd02-240">Примеры</span><span class="sxs-lookup"><span data-stu-id="1bd02-240">Examples</span></span>

<span data-ttu-id="1bd02-241">В примере [изменения MTU для всех сетевых адаптеров](https://Gallery.TechNet.Microsoft.Com/49c26363-d46c-4288-9c8d-feb0a1982998) на языке VBScript настраивается максимальная единица передачи для всех сетевых адаптеров, установленных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="1bd02-241">The [Modify the MTU for all Network Adapters](https://Gallery.TechNet.Microsoft.Com/49c26363-d46c-4288-9c8d-feb0a1982998) VBScript sample configures the maximum transmission unit for all network adapters installed in a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bd02-242">Требования</span><span class="sxs-lookup"><span data-stu-id="1bd02-242">Requirements</span></span>



| <span data-ttu-id="1bd02-243">Требование</span><span class="sxs-lookup"><span data-stu-id="1bd02-243">Requirement</span></span> | <span data-ttu-id="1bd02-244">Значение</span><span class="sxs-lookup"><span data-stu-id="1bd02-244">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1bd02-245">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1bd02-245">Minimum supported client</span></span><br/> | <span data-ttu-id="1bd02-246">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1bd02-246">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1bd02-247">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1bd02-247">Minimum supported server</span></span><br/> | <span data-ttu-id="1bd02-248">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1bd02-248">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1bd02-249">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1bd02-249">Namespace</span></span><br/>                | <span data-ttu-id="1bd02-250">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1bd02-250">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1bd02-251">MOF</span><span class="sxs-lookup"><span data-stu-id="1bd02-251">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1bd02-252"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1bd02-252"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1bd02-253">DLL</span><span class="sxs-lookup"><span data-stu-id="1bd02-253">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1bd02-254"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1bd02-254"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bd02-255">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1bd02-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bd02-256">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="1bd02-256">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="1bd02-257">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="1bd02-257">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="1bd02-258">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="1bd02-258">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="1bd02-259">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="1bd02-259">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="1bd02-260">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="1bd02-260">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

