---
description: Статический метод класса Сетнумфорвардпаккетс WMI используется для задания количества заголовков IP-пакетов, выделенных для очереди пакетов маршрутизатора. Если все заголовки используются, маршрутизатор начнет отбрасывать пакеты из очереди в случайном порядке.
ms.assetid: cadc7565-4cad-4e0f-a1eb-bf99d333bb28
ms.tgt_platform: multiple
title: Метод Сетнумфорвардпаккетс класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetNumForwardPackets
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f46ecd62766b5df642dff1e52614171a513a8fca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807576"
---
# <a name="setnumforwardpackets-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="b1ec3-104">Метод Сетнумфорвардпаккетс \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1ec3-104">SetNumForwardPackets method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="b1ec3-105">Статический метод класса **сетнумфорвардпаккетс** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) используется для задания количества заголовков IP-пакетов, выделенных для очереди пакетов маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-105">The **SetNumForwardPackets** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the number of IP packet headers allocated for the router packet queue.</span></span> <span data-ttu-id="b1ec3-106">Если все заголовки используются, маршрутизатор начнет отбрасывать пакеты из очереди в случайном порядке.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-106">When all headers are in use, the router will begin to discard packets from the queue at random.</span></span>

<span data-ttu-id="b1ec3-107">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="b1ec3-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b1ec3-108">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b1ec3-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b1ec3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b1ec3-109">Syntax</span></span>


```mof
uint32 SetNumForwardPackets(
  [in] uint32 NumForwardPackets
);
```



## <a name="parameters"></a><span data-ttu-id="b1ec3-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="b1ec3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1ec3-111">*Нумфорвардпаккетс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b1ec3-111">*NumForwardPackets* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-112">Число заголовков IP-пакетов, выделенных для очереди пакетов маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-112">Number of IP packet headers allocated for the router packet queue.</span></span> <span data-ttu-id="b1ec3-113">Это значение должно быть не меньше значения свойства [**ForwardBufferMemory**](win32-networkadapterconfiguration.md) , деленного на максимальный размер данных IP-адреса сетей, подключенных к маршрутизатору.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-113">This should be at least as large as the value of the [**ForwardBufferMemory**](win32-networkadapterconfiguration.md) property divided by the maximum IP data size of the networks connected to the router.</span></span> <span data-ttu-id="b1ec3-114">Оно должно быть не больше, чем значение параметра **ForwardBufferMemory** , деленное на 256, так как для каждого пакета требуется по крайней мере 256 байт памяти прямого буфера.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-114">It should be no larger than the **ForwardBufferMemory** value divided by 256, since at least 256 bytes of forward buffer memory are required by each packet.</span></span> <span data-ttu-id="b1ec3-115">Оптимальное число пересылаемых пакетов для заданного значения **ForwardBufferMemory** зависит от типа трафика, переданного в сеть, и между этими двумя значениями.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-115">The optimal number of forward packets for a given **ForwardBufferMemory** size depends on the type of traffic carried on the network, and will be somewhere between these two values.</span></span> <span data-ttu-id="b1ec3-116">Если маршрутизатор отключен, этот параметр игнорируется и заголовки не выделяются.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-116">If the router is disabled, this parameter is ignored and no headers are allocated.</span></span> <span data-ttu-id="b1ec3-117">Допустимый диапазон: 1 — 0xFFFFFFFE.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-117">Valid range: 1 - 0xFFFFFFFE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1ec3-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b1ec3-118">Return value</span></span>

<span data-ttu-id="b1ec3-119">Возвращает значение 0 (ноль) для успешного завершения, если не требуется перезагрузка, 1 (один) для успешного завершения, когда требуется перезагрузка, и другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-119">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="b1ec3-120">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="b1ec3-120">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="b1ec3-121">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="b1ec3-121">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="b1ec3-122">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-122">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-123">0</span><span class="sxs-lookup"><span data-stu-id="b1ec3-123">0</span></span>

<span data-ttu-id="b1ec3-124">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-124">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-125">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-125">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-126">1</span><span class="sxs-lookup"><span data-stu-id="b1ec3-126">1</span></span>

<span data-ttu-id="b1ec3-127">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-127">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-128">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-128">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-129">64</span><span class="sxs-lookup"><span data-stu-id="b1ec3-129">64</span></span>

<span data-ttu-id="b1ec3-130">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-130">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-131">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-131">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-132">65</span><span class="sxs-lookup"><span data-stu-id="b1ec3-132">65</span></span>

<span data-ttu-id="b1ec3-133">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-133">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-134">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-134">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-135">66</span><span class="sxs-lookup"><span data-stu-id="b1ec3-135">66</span></span>

<span data-ttu-id="b1ec3-136">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-136">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-137">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-137">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-138">67</span><span class="sxs-lookup"><span data-stu-id="b1ec3-138">67</span></span>

<span data-ttu-id="b1ec3-139">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-139">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-140">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-140">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-141">68</span><span class="sxs-lookup"><span data-stu-id="b1ec3-141">68</span></span>

<span data-ttu-id="b1ec3-142">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-142">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-143">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-143">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-144">69</span><span class="sxs-lookup"><span data-stu-id="b1ec3-144">69</span></span>

<span data-ttu-id="b1ec3-145">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-145">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-146">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-146">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-147">70</span><span class="sxs-lookup"><span data-stu-id="b1ec3-147">70</span></span>

<span data-ttu-id="b1ec3-148">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-148">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-149">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-149">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-150">71</span><span class="sxs-lookup"><span data-stu-id="b1ec3-150">71</span></span>

<span data-ttu-id="b1ec3-151">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-151">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-152">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-152">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-153">72</span><span class="sxs-lookup"><span data-stu-id="b1ec3-153">72</span></span>

<span data-ttu-id="b1ec3-154">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-154">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-155">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-155">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-156">73</span><span class="sxs-lookup"><span data-stu-id="b1ec3-156">73</span></span>

<span data-ttu-id="b1ec3-157">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-157">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-158">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-158">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-159">74</span><span class="sxs-lookup"><span data-stu-id="b1ec3-159">74</span></span>

<span data-ttu-id="b1ec3-160">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-160">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-161">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-161">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-162">75</span><span class="sxs-lookup"><span data-stu-id="b1ec3-162">75</span></span>

<span data-ttu-id="b1ec3-163">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-163">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-164">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-164">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-165">76</span><span class="sxs-lookup"><span data-stu-id="b1ec3-165">76</span></span>

<span data-ttu-id="b1ec3-166">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-166">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-167">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-167">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-168">77</span><span class="sxs-lookup"><span data-stu-id="b1ec3-168">77</span></span>

<span data-ttu-id="b1ec3-169">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-169">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-170">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-170">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-171">78</span><span class="sxs-lookup"><span data-stu-id="b1ec3-171">78</span></span>

<span data-ttu-id="b1ec3-172">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-172">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-173">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-173">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-174">79</span><span class="sxs-lookup"><span data-stu-id="b1ec3-174">79</span></span>

<span data-ttu-id="b1ec3-175">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-175">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-176">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-176">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-177">80</span><span class="sxs-lookup"><span data-stu-id="b1ec3-177">80</span></span>

<span data-ttu-id="b1ec3-178">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-178">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-179">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-179">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-180">81</span><span class="sxs-lookup"><span data-stu-id="b1ec3-180">81</span></span>

<span data-ttu-id="b1ec3-181">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-181">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-182">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-182">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-183">82</span><span class="sxs-lookup"><span data-stu-id="b1ec3-183">82</span></span>

<span data-ttu-id="b1ec3-184">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-184">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-185">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-185">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-186">83</span><span class="sxs-lookup"><span data-stu-id="b1ec3-186">83</span></span>

<span data-ttu-id="b1ec3-187">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-187">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-188">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-188">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-189">84</span><span class="sxs-lookup"><span data-stu-id="b1ec3-189">84</span></span>

<span data-ttu-id="b1ec3-190">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-190">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-191">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-191">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-192">85</span><span class="sxs-lookup"><span data-stu-id="b1ec3-192">85</span></span>

<span data-ttu-id="b1ec3-193">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-193">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-194">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-194">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-195">86</span><span class="sxs-lookup"><span data-stu-id="b1ec3-195">86</span></span>

<span data-ttu-id="b1ec3-196">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-196">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-197">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-197">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-198">87</span><span class="sxs-lookup"><span data-stu-id="b1ec3-198">87</span></span>

<span data-ttu-id="b1ec3-199">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-199">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-200">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-200">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-201">88</span><span class="sxs-lookup"><span data-stu-id="b1ec3-201">88</span></span>

<span data-ttu-id="b1ec3-202">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-202">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-203">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-203">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-204">89</span><span class="sxs-lookup"><span data-stu-id="b1ec3-204">89</span></span>

<span data-ttu-id="b1ec3-205">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-205">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-206">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-206">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-207">90</span><span class="sxs-lookup"><span data-stu-id="b1ec3-207">90</span></span>

<span data-ttu-id="b1ec3-208">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-208">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-209">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-209">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-210">91</span><span class="sxs-lookup"><span data-stu-id="b1ec3-210">91</span></span>

<span data-ttu-id="b1ec3-211">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-211">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-212">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-212">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-213">92</span><span class="sxs-lookup"><span data-stu-id="b1ec3-213">92</span></span>

<span data-ttu-id="b1ec3-214">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-214">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-215">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-215">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-216">93</span><span class="sxs-lookup"><span data-stu-id="b1ec3-216">93</span></span>

<span data-ttu-id="b1ec3-217">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-217">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-218">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-218">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-219">94</span><span class="sxs-lookup"><span data-stu-id="b1ec3-219">94</span></span>

<span data-ttu-id="b1ec3-220">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-220">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-221">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-221">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-222">95</span><span class="sxs-lookup"><span data-stu-id="b1ec3-222">95</span></span>

<span data-ttu-id="b1ec3-223">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-223">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-224">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-224">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-225">96</span><span class="sxs-lookup"><span data-stu-id="b1ec3-225">96</span></span>

<span data-ttu-id="b1ec3-226">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-226">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-227">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-227">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-228">97</span><span class="sxs-lookup"><span data-stu-id="b1ec3-228">97</span></span>

<span data-ttu-id="b1ec3-229">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-229">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-230">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-230">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-231">98</span><span class="sxs-lookup"><span data-stu-id="b1ec3-231">98</span></span>

<span data-ttu-id="b1ec3-232">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-232">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-233">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-233">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-234">100</span><span class="sxs-lookup"><span data-stu-id="b1ec3-234">100</span></span>

<span data-ttu-id="b1ec3-235">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-235">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b1ec3-236">**Другое**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-236">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="b1ec3-237">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="b1ec3-237">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="b1ec3-238">Примеры</span><span class="sxs-lookup"><span data-stu-id="b1ec3-238">Examples</span></span>

<span data-ttu-id="b1ec3-239">Пример [изменения числа разрешенных пересылаемых пакетов](https://Gallery.TechNet.Microsoft.Com/4123c28e-25c4-444e-818b-67bdbcc0cd4c) VBScript настраивает число передаваемых пакетов, выделенных очереди пакетов маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="b1ec3-239">The [Modify the Number of Allowed Forward Packets](https://Gallery.TechNet.Microsoft.Com/4123c28e-25c4-444e-818b-67bdbcc0cd4c) VBScript sample configures the number of forward packets allocated to the router packet queue.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1ec3-240">Требования</span><span class="sxs-lookup"><span data-stu-id="b1ec3-240">Requirements</span></span>



| <span data-ttu-id="b1ec3-241">Требование</span><span class="sxs-lookup"><span data-stu-id="b1ec3-241">Requirement</span></span> | <span data-ttu-id="b1ec3-242">Значение</span><span class="sxs-lookup"><span data-stu-id="b1ec3-242">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1ec3-243">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b1ec3-243">Minimum supported client</span></span><br/> | <span data-ttu-id="b1ec3-244">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b1ec3-244">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b1ec3-245">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b1ec3-245">Minimum supported server</span></span><br/> | <span data-ttu-id="b1ec3-246">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1ec3-246">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b1ec3-247">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b1ec3-247">Namespace</span></span><br/>                | <span data-ttu-id="b1ec3-248">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b1ec3-248">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b1ec3-249">MOF</span><span class="sxs-lookup"><span data-stu-id="b1ec3-249">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b1ec3-250"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b1ec3-250"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b1ec3-251">DLL</span><span class="sxs-lookup"><span data-stu-id="b1ec3-251">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1ec3-252"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1ec3-252"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1ec3-253">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b1ec3-253">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1ec3-254">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="b1ec3-254">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="b1ec3-255">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="b1ec3-255">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="b1ec3-256">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="b1ec3-256">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="b1ec3-257">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="b1ec3-257">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="b1ec3-258">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="b1ec3-258">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

