---
description: Статический метод класса WMI Сетткпвиндовсизе используется для установки максимального размера окна приема TCP, предлагаемого системой.
ms.assetid: c108fd9c-6de4-4f3e-9691-b0b5c1a3dc5f
ms.tgt_platform: multiple
title: Метод Сетткпвиндовсизе класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpWindowSize
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d4a77acdc81c06d1f78da8bbc0160bd0d21bcfd8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141557"
---
# <a name="settcpwindowsize-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="2224b-103">Метод Сетткпвиндовсизе \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="2224b-103">SetTcpWindowSize method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="2224b-104">Статический метод [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) **сетткпвиндовсизе** используется для установки максимального размера окна приема TCP, предлагаемого системой.</span><span class="sxs-lookup"><span data-stu-id="2224b-104">The **SetTcpWindowSize** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the maximum TCP Receive Window size offered by the system.</span></span>

<span data-ttu-id="2224b-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="2224b-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2224b-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2224b-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2224b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2224b-107">Syntax</span></span>


```mof
uint32 SetTcpWindowSize(
  [in] uint16 TcpWindowSize
);
```



## <a name="parameters"></a><span data-ttu-id="2224b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2224b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2224b-109">*TcpWindowSize* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2224b-109">*TcpWindowSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2224b-110">Максимальный размер окна приема TCP, предлагаемый системой.</span><span class="sxs-lookup"><span data-stu-id="2224b-110">Maximum TCP receive window size offered by the system.</span></span> <span data-ttu-id="2224b-111">Допустимый диапазон значений в байтах — 0-65535.</span><span class="sxs-lookup"><span data-stu-id="2224b-111">The valid range of values in bytes is 0 - 65535.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2224b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2224b-112">Return value</span></span>

<span data-ttu-id="2224b-113">Возвращает значение 0 (ноль) для успешного завершения, если не требуется перезагрузка, 1 (один) для успешного завершения, когда требуется перезагрузка, и другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="2224b-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="2224b-114">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="2224b-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="2224b-115">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="2224b-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="2224b-116">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="2224b-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-117">0</span><span class="sxs-lookup"><span data-stu-id="2224b-117">0</span></span>

<span data-ttu-id="2224b-118">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="2224b-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-119">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="2224b-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-120">1</span><span class="sxs-lookup"><span data-stu-id="2224b-120">1</span></span>

<span data-ttu-id="2224b-121">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="2224b-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-122">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="2224b-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-123">64</span><span class="sxs-lookup"><span data-stu-id="2224b-123">64</span></span>

<span data-ttu-id="2224b-124">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="2224b-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-125">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="2224b-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-126">65</span><span class="sxs-lookup"><span data-stu-id="2224b-126">65</span></span>

<span data-ttu-id="2224b-127">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="2224b-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-128">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="2224b-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-129">66</span><span class="sxs-lookup"><span data-stu-id="2224b-129">66</span></span>

<span data-ttu-id="2224b-130">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="2224b-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-131">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="2224b-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-132">67</span><span class="sxs-lookup"><span data-stu-id="2224b-132">67</span></span>

<span data-ttu-id="2224b-133">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="2224b-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-134">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="2224b-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-135">68</span><span class="sxs-lookup"><span data-stu-id="2224b-135">68</span></span>

<span data-ttu-id="2224b-136">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="2224b-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-137">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="2224b-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-138">69</span><span class="sxs-lookup"><span data-stu-id="2224b-138">69</span></span>

<span data-ttu-id="2224b-139">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="2224b-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-140">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="2224b-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-141">70</span><span class="sxs-lookup"><span data-stu-id="2224b-141">70</span></span>

<span data-ttu-id="2224b-142">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="2224b-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-143">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="2224b-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-144">71</span><span class="sxs-lookup"><span data-stu-id="2224b-144">71</span></span>

<span data-ttu-id="2224b-145">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="2224b-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-146">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="2224b-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-147">72</span><span class="sxs-lookup"><span data-stu-id="2224b-147">72</span></span>

<span data-ttu-id="2224b-148">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="2224b-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-149">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="2224b-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-150">73</span><span class="sxs-lookup"><span data-stu-id="2224b-150">73</span></span>

<span data-ttu-id="2224b-151">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="2224b-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-152">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="2224b-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-153">74</span><span class="sxs-lookup"><span data-stu-id="2224b-153">74</span></span>

<span data-ttu-id="2224b-154">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="2224b-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-155">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="2224b-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-156">75</span><span class="sxs-lookup"><span data-stu-id="2224b-156">75</span></span>

<span data-ttu-id="2224b-157">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="2224b-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-158">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="2224b-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-159">76</span><span class="sxs-lookup"><span data-stu-id="2224b-159">76</span></span>

<span data-ttu-id="2224b-160">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="2224b-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-161">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="2224b-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-162">77</span><span class="sxs-lookup"><span data-stu-id="2224b-162">77</span></span>

<span data-ttu-id="2224b-163">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="2224b-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-164">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="2224b-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-165">78</span><span class="sxs-lookup"><span data-stu-id="2224b-165">78</span></span>

<span data-ttu-id="2224b-166">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="2224b-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-167">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="2224b-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-168">79</span><span class="sxs-lookup"><span data-stu-id="2224b-168">79</span></span>

<span data-ttu-id="2224b-169">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="2224b-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-170">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="2224b-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-171">80</span><span class="sxs-lookup"><span data-stu-id="2224b-171">80</span></span>

<span data-ttu-id="2224b-172">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="2224b-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-173">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="2224b-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-174">81</span><span class="sxs-lookup"><span data-stu-id="2224b-174">81</span></span>

<span data-ttu-id="2224b-175">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="2224b-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-176">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="2224b-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-177">82</span><span class="sxs-lookup"><span data-stu-id="2224b-177">82</span></span>

<span data-ttu-id="2224b-178">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="2224b-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-179">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="2224b-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-180">83</span><span class="sxs-lookup"><span data-stu-id="2224b-180">83</span></span>

<span data-ttu-id="2224b-181">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="2224b-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-182">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="2224b-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-183">84</span><span class="sxs-lookup"><span data-stu-id="2224b-183">84</span></span>

<span data-ttu-id="2224b-184">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="2224b-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-185">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="2224b-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-186">85</span><span class="sxs-lookup"><span data-stu-id="2224b-186">85</span></span>

<span data-ttu-id="2224b-187">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="2224b-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-188">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="2224b-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-189">86</span><span class="sxs-lookup"><span data-stu-id="2224b-189">86</span></span>

<span data-ttu-id="2224b-190">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="2224b-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-191">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="2224b-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-192">87</span><span class="sxs-lookup"><span data-stu-id="2224b-192">87</span></span>

<span data-ttu-id="2224b-193">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="2224b-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-194">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="2224b-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-195">88</span><span class="sxs-lookup"><span data-stu-id="2224b-195">88</span></span>

<span data-ttu-id="2224b-196">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="2224b-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-197">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="2224b-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-198">89</span><span class="sxs-lookup"><span data-stu-id="2224b-198">89</span></span>

<span data-ttu-id="2224b-199">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="2224b-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-200">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="2224b-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-201">90</span><span class="sxs-lookup"><span data-stu-id="2224b-201">90</span></span>

<span data-ttu-id="2224b-202">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="2224b-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-203">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="2224b-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-204">91</span><span class="sxs-lookup"><span data-stu-id="2224b-204">91</span></span>

<span data-ttu-id="2224b-205">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="2224b-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-206">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="2224b-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-207">92</span><span class="sxs-lookup"><span data-stu-id="2224b-207">92</span></span>

<span data-ttu-id="2224b-208">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="2224b-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-209">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="2224b-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-210">93</span><span class="sxs-lookup"><span data-stu-id="2224b-210">93</span></span>

<span data-ttu-id="2224b-211">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="2224b-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-212">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="2224b-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-213">94</span><span class="sxs-lookup"><span data-stu-id="2224b-213">94</span></span>

<span data-ttu-id="2224b-214">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="2224b-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-215">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="2224b-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-216">95</span><span class="sxs-lookup"><span data-stu-id="2224b-216">95</span></span>

<span data-ttu-id="2224b-217">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="2224b-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-218">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="2224b-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-219">96</span><span class="sxs-lookup"><span data-stu-id="2224b-219">96</span></span>

<span data-ttu-id="2224b-220">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="2224b-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-221">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="2224b-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-222">97</span><span class="sxs-lookup"><span data-stu-id="2224b-222">97</span></span>

<span data-ttu-id="2224b-223">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="2224b-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-224">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="2224b-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-225">98</span><span class="sxs-lookup"><span data-stu-id="2224b-225">98</span></span>

<span data-ttu-id="2224b-226">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="2224b-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-227">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="2224b-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-228">100</span><span class="sxs-lookup"><span data-stu-id="2224b-228">100</span></span>

<span data-ttu-id="2224b-229">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="2224b-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2224b-230">**Другое**</span><span class="sxs-lookup"><span data-stu-id="2224b-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="2224b-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="2224b-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2224b-232">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2224b-232">Remarks</span></span>

<span data-ttu-id="2224b-233">В окне приема указывается число байтов, которое отправитель может передать без получения подтверждения.</span><span class="sxs-lookup"><span data-stu-id="2224b-233">The receive window specifies the number of bytes a sender can transmit without receiving an acknowledgment.</span></span> <span data-ttu-id="2224b-234">Как правило, увеличение скорости получения Windows повышает производительность сетей с высокой задержкой и высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="2224b-234">In general, larger receive windows improve performance over high-delay and high-bandwidth networks.</span></span> <span data-ttu-id="2224b-235">Для повышения эффективности окно приема должно быть четным, кратным максимальному размеру сегмента (MSS) TCP.</span><span class="sxs-lookup"><span data-stu-id="2224b-235">For efficiency, the receive window should be an even multiple of the TCP Maximum Segment Size (MSS).</span></span>

> [!Note]  
> <span data-ttu-id="2224b-236">Windows Vista. Этот метод обращается к `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` записи реестра, которая не используется в текущей реализации операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2224b-236">Windows Vista: This method accesses the `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` registry entry, which is not used in the current implementation of the operating system.</span></span>

 

## <a name="examples"></a><span data-ttu-id="2224b-237">Примеры</span><span class="sxs-lookup"><span data-stu-id="2224b-237">Examples</span></span>

<span data-ttu-id="2224b-238">В примере [изменения размера окна TCP для всех сетевых адаптеров](https://Gallery.TechNet.Microsoft.Com/74cf7be0-0044-4a88-85a3-9bc98490897b) VBScript задается размер окна TCP для всех сетевых адаптеров компьютера.</span><span class="sxs-lookup"><span data-stu-id="2224b-238">The [Modify the TCP Window Size for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/74cf7be0-0044-4a88-85a3-9bc98490897b) VBScript sample sets the TCP window size for all network adapters on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="2224b-239">Требования</span><span class="sxs-lookup"><span data-stu-id="2224b-239">Requirements</span></span>



| <span data-ttu-id="2224b-240">Требование</span><span class="sxs-lookup"><span data-stu-id="2224b-240">Requirement</span></span> | <span data-ttu-id="2224b-241">Значение</span><span class="sxs-lookup"><span data-stu-id="2224b-241">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2224b-242">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2224b-242">Minimum supported client</span></span><br/> | <span data-ttu-id="2224b-243">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2224b-243">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2224b-244">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2224b-244">Minimum supported server</span></span><br/> | <span data-ttu-id="2224b-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2224b-245">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2224b-246">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="2224b-246">End of client support</span></span><br/>    | <span data-ttu-id="2224b-247">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2224b-247">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="2224b-248">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="2224b-248">End of server support</span></span><br/>    | <span data-ttu-id="2224b-249">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2224b-249">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2224b-250">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2224b-250">Namespace</span></span><br/>                | <span data-ttu-id="2224b-251">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2224b-251">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2224b-252">MOF</span><span class="sxs-lookup"><span data-stu-id="2224b-252">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2224b-253"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2224b-253"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2224b-254">DLL</span><span class="sxs-lookup"><span data-stu-id="2224b-254">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2224b-255"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2224b-255"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2224b-256">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2224b-256">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2224b-257">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="2224b-257">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="2224b-258">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="2224b-258">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="2224b-259">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="2224b-259">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="2224b-260">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="2224b-260">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="2224b-261">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="2224b-261">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

