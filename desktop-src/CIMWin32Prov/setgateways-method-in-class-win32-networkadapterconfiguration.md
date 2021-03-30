---
description: Сетгатевайс &\# 32; Метод класса WMI указывает список шлюзов для маршрутизации пакетов в подсеть, отличную от подсети, к которой подключен сетевой адаптер.
ms.assetid: 240f7aff-7a07-4e0d-af30-7bcabb68c736
ms.tgt_platform: multiple
title: Метод Сетгатевайс класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetGateways
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 215bfa736a0f9d67ae587ac1f0e1b4aa394b85d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896085"
---
# <a name="setgateways-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="82cd0-103">Метод Сетгатевайс \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="82cd0-103">SetGateways method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="82cd0-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) сетгатевайс указывает список шлюзов для маршрутизации пакетов в подсеть, отличную от подсети, к которой подключен сетевой адаптер.</span><span class="sxs-lookup"><span data-stu-id="82cd0-104">The **SetGateways** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method specifies a list of gateways for routing packets to a subnet that is different from the subnet that the network adapter is connected to.</span></span>

<span data-ttu-id="82cd0-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="82cd0-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="82cd0-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="82cd0-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="82cd0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82cd0-107">Syntax</span></span>


```mof
uint32 SetGateways(
  [in]           string DefaultIPGateway[],
  [in, optional] uint16 GatewayCostMetric[]
);
```



## <a name="parameters"></a><span data-ttu-id="82cd0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="82cd0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82cd0-109">*Дефаултипгатевай* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="82cd0-109">*DefaultIPGateway* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-110">Список IP-адресов шлюзов, на которые направляются сетевые пакеты.</span><span class="sxs-lookup"><span data-stu-id="82cd0-110">List of IP addresses to gateways where network packets are routed.</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-111">*Гатевайкостметрик* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="82cd0-111">*GatewayCostMetric* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-112">Присваивает значение, которое находится в диапазоне от 1 до 9999, которое используется для вычисления самого быстрого и наиболее надежного маршрута.</span><span class="sxs-lookup"><span data-stu-id="82cd0-112">Assigns a value that ranges from 1 to 9999, which is used to calculate the fastest and most reliable routes.</span></span> <span data-ttu-id="82cd0-113">Значения этого параметра соответствуют значениям в параметре *дефаултипгатевай* .</span><span class="sxs-lookup"><span data-stu-id="82cd0-113">The values of this parameter correspond with the values in the *DefaultIPGateway* parameter.</span></span> <span data-ttu-id="82cd0-114">Значение по умолчанию для шлюза — 1.</span><span class="sxs-lookup"><span data-stu-id="82cd0-114">The default value for a gateway is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82cd0-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82cd0-115">Return value</span></span>

<span data-ttu-id="82cd0-116">Возвращает значение 0 (ноль) для успешного завершения, если перезагрузка не требуется, 1 (один) для успешного завершения, когда требуется перезагрузка, и любое другое значение при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="82cd0-116">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other value if there is an error.</span></span> <span data-ttu-id="82cd0-117">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="82cd0-117">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="82cd0-118">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="82cd0-118">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="82cd0-119">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="82cd0-119">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-120">0</span><span class="sxs-lookup"><span data-stu-id="82cd0-120">0</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-121">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="82cd0-121">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-122">1</span><span class="sxs-lookup"><span data-stu-id="82cd0-122">1</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-123">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="82cd0-123">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-124">64</span><span class="sxs-lookup"><span data-stu-id="82cd0-124">64</span></span>

<span data-ttu-id="82cd0-125">Метод не поддерживается, если сетевой адаптер находится в режиме DHCP.</span><span class="sxs-lookup"><span data-stu-id="82cd0-125">Method not supported when the NIC is in DHCP mode.</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-126">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="82cd0-126">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-127">65</span><span class="sxs-lookup"><span data-stu-id="82cd0-127">65</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-128">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="82cd0-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-129">66</span><span class="sxs-lookup"><span data-stu-id="82cd0-129">66</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-130">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="82cd0-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-131">67</span><span class="sxs-lookup"><span data-stu-id="82cd0-131">67</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-132">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="82cd0-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-133">68</span><span class="sxs-lookup"><span data-stu-id="82cd0-133">68</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-134">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="82cd0-134">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-135">69</span><span class="sxs-lookup"><span data-stu-id="82cd0-135">69</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-136">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="82cd0-136">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-137">70</span><span class="sxs-lookup"><span data-stu-id="82cd0-137">70</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-138">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="82cd0-138">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-139">71</span><span class="sxs-lookup"><span data-stu-id="82cd0-139">71</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-140">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="82cd0-140">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-141">72</span><span class="sxs-lookup"><span data-stu-id="82cd0-141">72</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-142">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="82cd0-142">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-143">73</span><span class="sxs-lookup"><span data-stu-id="82cd0-143">73</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-144">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="82cd0-144">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-145">74</span><span class="sxs-lookup"><span data-stu-id="82cd0-145">74</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-146">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="82cd0-146">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-147">75</span><span class="sxs-lookup"><span data-stu-id="82cd0-147">75</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-148">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="82cd0-148">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-149">76</span><span class="sxs-lookup"><span data-stu-id="82cd0-149">76</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-150">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="82cd0-150">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-151">77</span><span class="sxs-lookup"><span data-stu-id="82cd0-151">77</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-152">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="82cd0-152">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-153">78</span><span class="sxs-lookup"><span data-stu-id="82cd0-153">78</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-154">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="82cd0-154">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-155">79</span><span class="sxs-lookup"><span data-stu-id="82cd0-155">79</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-156">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="82cd0-156">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-157">80</span><span class="sxs-lookup"><span data-stu-id="82cd0-157">80</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-158">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="82cd0-158">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-159">81</span><span class="sxs-lookup"><span data-stu-id="82cd0-159">81</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-160">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="82cd0-160">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-161">82</span><span class="sxs-lookup"><span data-stu-id="82cd0-161">82</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-162">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="82cd0-162">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-163">83</span><span class="sxs-lookup"><span data-stu-id="82cd0-163">83</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-164">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="82cd0-164">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-165">84</span><span class="sxs-lookup"><span data-stu-id="82cd0-165">84</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-166">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="82cd0-166">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-167">85</span><span class="sxs-lookup"><span data-stu-id="82cd0-167">85</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-168">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="82cd0-168">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-169">86</span><span class="sxs-lookup"><span data-stu-id="82cd0-169">86</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-170">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="82cd0-170">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-171">87</span><span class="sxs-lookup"><span data-stu-id="82cd0-171">87</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-172">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="82cd0-172">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-173">88</span><span class="sxs-lookup"><span data-stu-id="82cd0-173">88</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-174">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="82cd0-174">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-175">89</span><span class="sxs-lookup"><span data-stu-id="82cd0-175">89</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-176">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="82cd0-176">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-177">90</span><span class="sxs-lookup"><span data-stu-id="82cd0-177">90</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-178">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="82cd0-178">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-179">91</span><span class="sxs-lookup"><span data-stu-id="82cd0-179">91</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-180">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="82cd0-180">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-181">92</span><span class="sxs-lookup"><span data-stu-id="82cd0-181">92</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-182">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="82cd0-182">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-183">93</span><span class="sxs-lookup"><span data-stu-id="82cd0-183">93</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-184">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="82cd0-184">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-185">94</span><span class="sxs-lookup"><span data-stu-id="82cd0-185">94</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-186">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="82cd0-186">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-187">95</span><span class="sxs-lookup"><span data-stu-id="82cd0-187">95</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-188">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="82cd0-188">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-189">96</span><span class="sxs-lookup"><span data-stu-id="82cd0-189">96</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-190">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="82cd0-190">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-191">97</span><span class="sxs-lookup"><span data-stu-id="82cd0-191">97</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-192">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="82cd0-192">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-193">98</span><span class="sxs-lookup"><span data-stu-id="82cd0-193">98</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-194">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="82cd0-194">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-195">100</span><span class="sxs-lookup"><span data-stu-id="82cd0-195">100</span></span>

</dd> <dt>

<span data-ttu-id="82cd0-196">**Другое**</span><span class="sxs-lookup"><span data-stu-id="82cd0-196">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="82cd0-197">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="82cd0-197">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82cd0-198">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82cd0-198">Remarks</span></span>

<span data-ttu-id="82cd0-199">Этот метод работает, только если сетевой адаптер (NIC) находится в режиме статического IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="82cd0-199">This method only works when the Network Interface Card (NIC) is in the static IP mode.</span></span>

<span data-ttu-id="82cd0-200">Чтобы очистить шлюз, задайте для шлюза тот же IP-адрес, который используется в [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="82cd0-200">To clear the gateway, set your gateway to the same IP you use on [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md).</span></span>

## <a name="examples"></a><span data-ttu-id="82cd0-201">Примеры</span><span class="sxs-lookup"><span data-stu-id="82cd0-201">Examples</span></span>

<span data-ttu-id="82cd0-202">В примере [изменения шлюзов для сетевого адаптера](https://Gallery.TechNet.Microsoft.Com/9ea7670b-f68f-4efb-9cd2-7c299a8f657f) VBScript настраиваются два шлюза для сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="82cd0-202">The [Modify the Gateways for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/9ea7670b-f68f-4efb-9cd2-7c299a8f657f) VBScript sample configures two gateways for a network adapter.</span></span>

<span data-ttu-id="82cd0-203">В примере « [Назначение статического IP-адреса](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) на языке VBScript» задается IP-адрес и шлюз компьютера.</span><span class="sxs-lookup"><span data-stu-id="82cd0-203">The [Assign a Static IP Address](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) VBScript sample sets the IP address and gateway of a computer.</span></span>

<span data-ttu-id="82cd0-204">[Статический IP-адрес, а затем присоединение к](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) образцу PowerShell для домена помогает в перестроении компьютеров.</span><span class="sxs-lookup"><span data-stu-id="82cd0-204">The [Static IP and then join to a domain](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) PowerShell sample assists in rebuilding machines.</span></span>

## <a name="requirements"></a><span data-ttu-id="82cd0-205">Требования</span><span class="sxs-lookup"><span data-stu-id="82cd0-205">Requirements</span></span>



| <span data-ttu-id="82cd0-206">Требование</span><span class="sxs-lookup"><span data-stu-id="82cd0-206">Requirement</span></span> | <span data-ttu-id="82cd0-207">Значение</span><span class="sxs-lookup"><span data-stu-id="82cd0-207">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82cd0-208">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="82cd0-208">Minimum supported client</span></span><br/> | <span data-ttu-id="82cd0-209">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="82cd0-209">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="82cd0-210">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="82cd0-210">Minimum supported server</span></span><br/> | <span data-ttu-id="82cd0-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="82cd0-211">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="82cd0-212">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="82cd0-212">Namespace</span></span><br/>                | <span data-ttu-id="82cd0-213">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="82cd0-213">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="82cd0-214">MOF</span><span class="sxs-lookup"><span data-stu-id="82cd0-214">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82cd0-215"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="82cd0-215"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="82cd0-216">DLL</span><span class="sxs-lookup"><span data-stu-id="82cd0-216">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82cd0-217"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82cd0-217"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82cd0-218">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82cd0-218">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82cd0-219">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="82cd0-219">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="82cd0-220">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="82cd0-220">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="82cd0-221">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="82cd0-221">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="82cd0-222">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="82cd0-222">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="82cd0-223">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="82cd0-223">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

