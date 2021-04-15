---
description: Статический метод класса Сетдатабасепас WMI задает путь к стандартным файлам базы данных Интернета (узлы, файлы LMHOSTS, сети и ПРОТОКОЛы).
ms.assetid: 373fef0f-9cdf-4785-8d73-3f00bbd60ae2
ms.tgt_platform: multiple
title: Метод Сетдатабасепас класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDatabasePath
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b66a9979ec97d4ceda16acad6488d3b84d5d3a54
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539338"
---
# <a name="setdatabasepath-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="a3858-103">Метод Сетдатабасепас \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3858-103">SetDatabasePath method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="a3858-104">Статический метод класса **сетдатабасепас** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) задает путь к стандартным файлам базы данных Интернета (узлы, файлы LMHOSTS, сети и протоколы).</span><span class="sxs-lookup"><span data-stu-id="a3858-104">The **SetDatabasePath** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method sets the path to the standard Internet database files (HOSTS, LMHOSTS, NETWORKS, and PROTOCOLS).</span></span>

<span data-ttu-id="a3858-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="a3858-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a3858-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a3858-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a3858-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3858-107">Syntax</span></span>


```mof
uint32 SetDatabasePath(
  [in] string DatabasePath
);
```



## <a name="parameters"></a><span data-ttu-id="a3858-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3858-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3858-109">*DatabasePath* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a3858-109">*DatabasePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3858-110">Допустимый путь к файлам стандартных баз данных Интернета (узлы, файлы LMHOSTS, сети и ПРОТОКОЛы), используемые интерфейсом сокетов Windows.</span><span class="sxs-lookup"><span data-stu-id="a3858-110">Valid file path to standard Internet database files (HOSTS, LMHOSTS, NETWORKS, and PROTOCOLS) used by the Windows Sockets interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3858-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a3858-111">Return value</span></span>

<span data-ttu-id="a3858-112">Возвращает значение 0 (ноль) для успешного завершения, если не требуется перезагрузка, 1 (один) для успешного завершения, если требуется перезагрузка, другое число при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="a3858-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, a different number if there is an error.</span></span> <span data-ttu-id="a3858-113">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="a3858-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="a3858-114">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="a3858-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="a3858-115">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="a3858-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-116">0</span><span class="sxs-lookup"><span data-stu-id="a3858-116">0</span></span>

<span data-ttu-id="a3858-117">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="a3858-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-118">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="a3858-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-119">1</span><span class="sxs-lookup"><span data-stu-id="a3858-119">1</span></span>

<span data-ttu-id="a3858-120">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="a3858-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-121">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="a3858-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-122">64</span><span class="sxs-lookup"><span data-stu-id="a3858-122">64</span></span>

<span data-ttu-id="a3858-123">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="a3858-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-124">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="a3858-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-125">65</span><span class="sxs-lookup"><span data-stu-id="a3858-125">65</span></span>

<span data-ttu-id="a3858-126">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="a3858-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-127">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="a3858-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-128">66</span><span class="sxs-lookup"><span data-stu-id="a3858-128">66</span></span>

<span data-ttu-id="a3858-129">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="a3858-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-130">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="a3858-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-131">67</span><span class="sxs-lookup"><span data-stu-id="a3858-131">67</span></span>

<span data-ttu-id="a3858-132">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a3858-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-133">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="a3858-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-134">68</span><span class="sxs-lookup"><span data-stu-id="a3858-134">68</span></span>

<span data-ttu-id="a3858-135">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="a3858-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-136">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="a3858-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-137">69</span><span class="sxs-lookup"><span data-stu-id="a3858-137">69</span></span>

<span data-ttu-id="a3858-138">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="a3858-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-139">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="a3858-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-140">70</span><span class="sxs-lookup"><span data-stu-id="a3858-140">70</span></span>

<span data-ttu-id="a3858-141">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="a3858-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-142">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="a3858-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-143">71</span><span class="sxs-lookup"><span data-stu-id="a3858-143">71</span></span>

<span data-ttu-id="a3858-144">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="a3858-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-145">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="a3858-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-146">72</span><span class="sxs-lookup"><span data-stu-id="a3858-146">72</span></span>

<span data-ttu-id="a3858-147">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="a3858-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-148">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="a3858-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-149">73</span><span class="sxs-lookup"><span data-stu-id="a3858-149">73</span></span>

<span data-ttu-id="a3858-150">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="a3858-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-151">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="a3858-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-152">74</span><span class="sxs-lookup"><span data-stu-id="a3858-152">74</span></span>

<span data-ttu-id="a3858-153">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="a3858-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-154">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="a3858-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-155">75</span><span class="sxs-lookup"><span data-stu-id="a3858-155">75</span></span>

<span data-ttu-id="a3858-156">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="a3858-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-157">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="a3858-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-158">76</span><span class="sxs-lookup"><span data-stu-id="a3858-158">76</span></span>

<span data-ttu-id="a3858-159">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="a3858-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-160">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="a3858-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-161">77</span><span class="sxs-lookup"><span data-stu-id="a3858-161">77</span></span>

<span data-ttu-id="a3858-162">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="a3858-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-163">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="a3858-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-164">78</span><span class="sxs-lookup"><span data-stu-id="a3858-164">78</span></span>

<span data-ttu-id="a3858-165">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="a3858-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-166">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="a3858-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-167">79</span><span class="sxs-lookup"><span data-stu-id="a3858-167">79</span></span>

<span data-ttu-id="a3858-168">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="a3858-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-169">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="a3858-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-170">80</span><span class="sxs-lookup"><span data-stu-id="a3858-170">80</span></span>

<span data-ttu-id="a3858-171">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="a3858-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-172">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="a3858-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-173">81</span><span class="sxs-lookup"><span data-stu-id="a3858-173">81</span></span>

<span data-ttu-id="a3858-174">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="a3858-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-175">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="a3858-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-176">82</span><span class="sxs-lookup"><span data-stu-id="a3858-176">82</span></span>

<span data-ttu-id="a3858-177">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="a3858-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-178">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="a3858-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-179">83</span><span class="sxs-lookup"><span data-stu-id="a3858-179">83</span></span>

<span data-ttu-id="a3858-180">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="a3858-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-181">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="a3858-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-182">84</span><span class="sxs-lookup"><span data-stu-id="a3858-182">84</span></span>

<span data-ttu-id="a3858-183">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="a3858-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-184">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="a3858-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-185">85</span><span class="sxs-lookup"><span data-stu-id="a3858-185">85</span></span>

<span data-ttu-id="a3858-186">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="a3858-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-187">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="a3858-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-188">86</span><span class="sxs-lookup"><span data-stu-id="a3858-188">86</span></span>

<span data-ttu-id="a3858-189">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="a3858-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-190">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="a3858-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-191">87</span><span class="sxs-lookup"><span data-stu-id="a3858-191">87</span></span>

<span data-ttu-id="a3858-192">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="a3858-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-193">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="a3858-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-194">88</span><span class="sxs-lookup"><span data-stu-id="a3858-194">88</span></span>

<span data-ttu-id="a3858-195">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="a3858-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-196">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="a3858-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-197">89</span><span class="sxs-lookup"><span data-stu-id="a3858-197">89</span></span>

<span data-ttu-id="a3858-198">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="a3858-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-199">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="a3858-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-200">90</span><span class="sxs-lookup"><span data-stu-id="a3858-200">90</span></span>

<span data-ttu-id="a3858-201">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="a3858-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-202">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="a3858-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-203">91</span><span class="sxs-lookup"><span data-stu-id="a3858-203">91</span></span>

<span data-ttu-id="a3858-204">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="a3858-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-205">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="a3858-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-206">92</span><span class="sxs-lookup"><span data-stu-id="a3858-206">92</span></span>

<span data-ttu-id="a3858-207">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="a3858-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-208">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="a3858-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-209">93</span><span class="sxs-lookup"><span data-stu-id="a3858-209">93</span></span>

<span data-ttu-id="a3858-210">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="a3858-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-211">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="a3858-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-212">94</span><span class="sxs-lookup"><span data-stu-id="a3858-212">94</span></span>

<span data-ttu-id="a3858-213">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="a3858-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-214">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="a3858-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-215">95</span><span class="sxs-lookup"><span data-stu-id="a3858-215">95</span></span>

<span data-ttu-id="a3858-216">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="a3858-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-217">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="a3858-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-218">96</span><span class="sxs-lookup"><span data-stu-id="a3858-218">96</span></span>

<span data-ttu-id="a3858-219">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="a3858-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-220">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="a3858-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-221">97</span><span class="sxs-lookup"><span data-stu-id="a3858-221">97</span></span>

<span data-ttu-id="a3858-222">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="a3858-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-223">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="a3858-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-224">98</span><span class="sxs-lookup"><span data-stu-id="a3858-224">98</span></span>

<span data-ttu-id="a3858-225">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="a3858-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-226">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="a3858-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-227">100</span><span class="sxs-lookup"><span data-stu-id="a3858-227">100</span></span>

<span data-ttu-id="a3858-228">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="a3858-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="a3858-229">**Другое**</span><span class="sxs-lookup"><span data-stu-id="a3858-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="a3858-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="a3858-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a3858-231">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a3858-231">Remarks</span></span>

<span data-ttu-id="a3858-232">Этот метод используется интерфейсом сокетов Windows.</span><span class="sxs-lookup"><span data-stu-id="a3858-232">This method is used by the Windows Sockets interface.</span></span> <span data-ttu-id="a3858-233">По умолчанию используется путь% SystemRoot \\ % \\ system32 \\ .</span><span class="sxs-lookup"><span data-stu-id="a3858-233">The default path is %SystemRoot%\\system32\\drivers\\ .</span></span>

## <a name="examples"></a><span data-ttu-id="a3858-234">Примеры</span><span class="sxs-lookup"><span data-stu-id="a3858-234">Examples</span></span>

<span data-ttu-id="a3858-235">Пример " [изменение пути к базе данных для всех сетевых адаптеров"](https://Gallery.TechNet.Microsoft.Com/94bfa42f-f6a3-482f-8d5a-5445a2475bee) в коллекции TechNet использует **сетдатабасепас** , чтобы задать путь к стандартным файлам базы данных Интернета (УЗЛАМИ, LMHOSTS, сетям, протоколам), используемым интерфейсом сокетов Windows.</span><span class="sxs-lookup"><span data-stu-id="a3858-235">The [Modify the Database Path for all Network Adapters](https://Gallery.TechNet.Microsoft.Com/94bfa42f-f6a3-482f-8d5a-5445a2475bee) VBScript sample on TechNet Gallery uses **SetDatabasePath** to set the path to the standard Internet database files (HOSTS, LMHOSTS, NETWORKS, PROTOCOLS) used by the Windows Sockets interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3858-236">Требования</span><span class="sxs-lookup"><span data-stu-id="a3858-236">Requirements</span></span>



| <span data-ttu-id="a3858-237">Требование</span><span class="sxs-lookup"><span data-stu-id="a3858-237">Requirement</span></span> | <span data-ttu-id="a3858-238">Значение</span><span class="sxs-lookup"><span data-stu-id="a3858-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3858-239">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a3858-239">Minimum supported client</span></span><br/> | <span data-ttu-id="a3858-240">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3858-240">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a3858-241">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a3858-241">Minimum supported server</span></span><br/> | <span data-ttu-id="a3858-242">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3858-242">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a3858-243">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a3858-243">Namespace</span></span><br/>                | <span data-ttu-id="a3858-244">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a3858-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a3858-245">MOF</span><span class="sxs-lookup"><span data-stu-id="a3858-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a3858-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a3858-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a3858-247">DLL</span><span class="sxs-lookup"><span data-stu-id="a3858-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3858-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3858-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3858-249">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3858-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3858-250">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="a3858-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="a3858-251">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="a3858-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="a3858-252">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="a3858-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="a3858-253">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="a3858-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="a3858-254">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="a3858-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

