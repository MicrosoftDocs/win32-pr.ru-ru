---
description: Статический метод класса Сетигмплевел WMI используется для задания экстента, в котором система поддерживает многоадресную рассылку IP-адресов и участвует в протоколе управления группами Интернета.
ms.assetid: 38877576-aa23-4841-b3ae-1a02bfdd70d8
ms.tgt_platform: multiple
title: Метод Сетигмплевел класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIGMPLevel
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 97ead4df1d45b110c3d0a91976dc8eca6ffd72c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538993"
---
# <a name="setigmplevel-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="74399-103">Метод Сетигмплевел \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="74399-103">SetIGMPLevel method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="74399-104">Статический метод класса **сетигмплевел** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) используется для задания экстента, в котором система поддерживает многоадресную рассылку IP-адресов и участвует в протоколе управления группами Интернета.</span><span class="sxs-lookup"><span data-stu-id="74399-104">The **SetIGMPLevel** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the extent to which the system supports IP multicasting and participates in the Internet Group Management Protocol.</span></span>

<span data-ttu-id="74399-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="74399-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="74399-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="74399-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="74399-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74399-107">Syntax</span></span>


```mof
uint32 SetIGMPLevel(
  [in] uint8 IGMPLevel
);
```



## <a name="parameters"></a><span data-ttu-id="74399-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="74399-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74399-109">*Игмплевел* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="74399-109">*IGMPLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74399-110">Тип данных: **целое число**</span><span class="sxs-lookup"><span data-stu-id="74399-110">Data type: **Integer**</span></span>

<span data-ttu-id="74399-111">Задает уровень, на котором система поддерживает многоадресную рассылку IP-адресов и участвует в протоколе управления группами Интернета.</span><span class="sxs-lookup"><span data-stu-id="74399-111">Sets the level at which the system supports IP multicast and participates in the Internet Group Management Protocol.</span></span> <span data-ttu-id="74399-112">На уровне 0 система не обеспечивает поддержку многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="74399-112">At level 0, the system provides no multicast support.</span></span> <span data-ttu-id="74399-113">На уровне 1 система может только передавать пакеты IP-адресов многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="74399-113">At level 1, the system may only send IP multicast packets.</span></span> <span data-ttu-id="74399-114">На уровне 2 система может отправлять пакеты многоадресной рассылки IP-адресов и полностью участвовать в протоколе IGMP для получения пакетов многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="74399-114">At level 2, the system may send IP multicast packets and fully participate in IGMP to receive multicast packets.</span></span>

<dt>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>

<span data-ttu-id="74399-115">**Без многоадресной рассылки** (0)</span><span class="sxs-lookup"><span data-stu-id="74399-115">**No Multicast** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>

<span data-ttu-id="74399-116">**Многоадресная рассылка IP** (1)</span><span class="sxs-lookup"><span data-stu-id="74399-116">**IP Multicast** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>

<span data-ttu-id="74399-117">**IP-& многоадресная рассылка IGMP** (2)</span><span class="sxs-lookup"><span data-stu-id="74399-117">**IP & IGMP multicast** (2)</span></span>


<span data-ttu-id="74399-118"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="74399-118"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="74399-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="74399-119">Return value</span></span>

<span data-ttu-id="74399-120">Возвращает значение 0 (ноль) для успешного завершения, если не требуется перезагрузка, 1 (один) для успешного завершения, когда требуется перезагрузка, и другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="74399-120">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="74399-121">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="74399-121">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="74399-122">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="74399-122">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="74399-123">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="74399-123">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="74399-124">0</span><span class="sxs-lookup"><span data-stu-id="74399-124">0</span></span>

<span data-ttu-id="74399-125">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="74399-125">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="74399-126">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="74399-126">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="74399-127">1</span><span class="sxs-lookup"><span data-stu-id="74399-127">1</span></span>

<span data-ttu-id="74399-128">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="74399-128">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="74399-129">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="74399-129">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="74399-130">64</span><span class="sxs-lookup"><span data-stu-id="74399-130">64</span></span>

<span data-ttu-id="74399-131">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="74399-131">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="74399-132">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="74399-132">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="74399-133">65</span><span class="sxs-lookup"><span data-stu-id="74399-133">65</span></span>

<span data-ttu-id="74399-134">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="74399-134">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="74399-135">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="74399-135">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="74399-136">66</span><span class="sxs-lookup"><span data-stu-id="74399-136">66</span></span>

<span data-ttu-id="74399-137">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="74399-137">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="74399-138">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="74399-138">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="74399-139">67</span><span class="sxs-lookup"><span data-stu-id="74399-139">67</span></span>

<span data-ttu-id="74399-140">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="74399-140">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="74399-141">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="74399-141">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="74399-142">68</span><span class="sxs-lookup"><span data-stu-id="74399-142">68</span></span>

<span data-ttu-id="74399-143">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="74399-143">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="74399-144">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="74399-144">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="74399-145">69</span><span class="sxs-lookup"><span data-stu-id="74399-145">69</span></span>

<span data-ttu-id="74399-146">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="74399-146">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="74399-147">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="74399-147">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="74399-148">70</span><span class="sxs-lookup"><span data-stu-id="74399-148">70</span></span>

<span data-ttu-id="74399-149">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="74399-149">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="74399-150">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="74399-150">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="74399-151">71</span><span class="sxs-lookup"><span data-stu-id="74399-151">71</span></span>

<span data-ttu-id="74399-152">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="74399-152">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="74399-153">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="74399-153">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="74399-154">72</span><span class="sxs-lookup"><span data-stu-id="74399-154">72</span></span>

<span data-ttu-id="74399-155">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="74399-155">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="74399-156">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="74399-156">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="74399-157">73</span><span class="sxs-lookup"><span data-stu-id="74399-157">73</span></span>

<span data-ttu-id="74399-158">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="74399-158">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="74399-159">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="74399-159">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="74399-160">74</span><span class="sxs-lookup"><span data-stu-id="74399-160">74</span></span>

<span data-ttu-id="74399-161">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="74399-161">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="74399-162">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="74399-162">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="74399-163">75</span><span class="sxs-lookup"><span data-stu-id="74399-163">75</span></span>

<span data-ttu-id="74399-164">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="74399-164">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="74399-165">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="74399-165">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="74399-166">76</span><span class="sxs-lookup"><span data-stu-id="74399-166">76</span></span>

<span data-ttu-id="74399-167">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="74399-167">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="74399-168">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="74399-168">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="74399-169">77</span><span class="sxs-lookup"><span data-stu-id="74399-169">77</span></span>

<span data-ttu-id="74399-170">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="74399-170">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="74399-171">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="74399-171">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="74399-172">78</span><span class="sxs-lookup"><span data-stu-id="74399-172">78</span></span>

<span data-ttu-id="74399-173">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="74399-173">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="74399-174">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="74399-174">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="74399-175">79</span><span class="sxs-lookup"><span data-stu-id="74399-175">79</span></span>

<span data-ttu-id="74399-176">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="74399-176">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="74399-177">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="74399-177">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="74399-178">80</span><span class="sxs-lookup"><span data-stu-id="74399-178">80</span></span>

<span data-ttu-id="74399-179">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="74399-179">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="74399-180">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="74399-180">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="74399-181">81</span><span class="sxs-lookup"><span data-stu-id="74399-181">81</span></span>

<span data-ttu-id="74399-182">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="74399-182">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="74399-183">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="74399-183">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="74399-184">82</span><span class="sxs-lookup"><span data-stu-id="74399-184">82</span></span>

<span data-ttu-id="74399-185">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="74399-185">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="74399-186">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="74399-186">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="74399-187">83</span><span class="sxs-lookup"><span data-stu-id="74399-187">83</span></span>

<span data-ttu-id="74399-188">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="74399-188">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="74399-189">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="74399-189">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="74399-190">84</span><span class="sxs-lookup"><span data-stu-id="74399-190">84</span></span>

<span data-ttu-id="74399-191">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="74399-191">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="74399-192">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="74399-192">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="74399-193">85</span><span class="sxs-lookup"><span data-stu-id="74399-193">85</span></span>

<span data-ttu-id="74399-194">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="74399-194">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="74399-195">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="74399-195">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="74399-196">86</span><span class="sxs-lookup"><span data-stu-id="74399-196">86</span></span>

<span data-ttu-id="74399-197">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="74399-197">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="74399-198">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="74399-198">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="74399-199">87</span><span class="sxs-lookup"><span data-stu-id="74399-199">87</span></span>

<span data-ttu-id="74399-200">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="74399-200">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="74399-201">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="74399-201">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="74399-202">88</span><span class="sxs-lookup"><span data-stu-id="74399-202">88</span></span>

<span data-ttu-id="74399-203">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="74399-203">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="74399-204">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="74399-204">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="74399-205">89</span><span class="sxs-lookup"><span data-stu-id="74399-205">89</span></span>

<span data-ttu-id="74399-206">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="74399-206">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="74399-207">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="74399-207">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="74399-208">90</span><span class="sxs-lookup"><span data-stu-id="74399-208">90</span></span>

<span data-ttu-id="74399-209">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="74399-209">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="74399-210">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="74399-210">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="74399-211">91</span><span class="sxs-lookup"><span data-stu-id="74399-211">91</span></span>

<span data-ttu-id="74399-212">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="74399-212">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="74399-213">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="74399-213">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="74399-214">92</span><span class="sxs-lookup"><span data-stu-id="74399-214">92</span></span>

<span data-ttu-id="74399-215">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="74399-215">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="74399-216">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="74399-216">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="74399-217">93</span><span class="sxs-lookup"><span data-stu-id="74399-217">93</span></span>

<span data-ttu-id="74399-218">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="74399-218">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="74399-219">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="74399-219">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="74399-220">94</span><span class="sxs-lookup"><span data-stu-id="74399-220">94</span></span>

<span data-ttu-id="74399-221">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="74399-221">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="74399-222">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="74399-222">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="74399-223">95</span><span class="sxs-lookup"><span data-stu-id="74399-223">95</span></span>

<span data-ttu-id="74399-224">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="74399-224">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="74399-225">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="74399-225">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="74399-226">96</span><span class="sxs-lookup"><span data-stu-id="74399-226">96</span></span>

<span data-ttu-id="74399-227">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="74399-227">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="74399-228">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="74399-228">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="74399-229">97</span><span class="sxs-lookup"><span data-stu-id="74399-229">97</span></span>

<span data-ttu-id="74399-230">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="74399-230">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="74399-231">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="74399-231">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="74399-232">98</span><span class="sxs-lookup"><span data-stu-id="74399-232">98</span></span>

<span data-ttu-id="74399-233">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="74399-233">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="74399-234">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="74399-234">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="74399-235">100</span><span class="sxs-lookup"><span data-stu-id="74399-235">100</span></span>

<span data-ttu-id="74399-236">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="74399-236">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="74399-237">**Другое**</span><span class="sxs-lookup"><span data-stu-id="74399-237">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="74399-238">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="74399-238">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="74399-239">Примеры</span><span class="sxs-lookup"><span data-stu-id="74399-239">Examples</span></span>

<span data-ttu-id="74399-240">Пример [изменения уровня IGMP для всех сетевых адаптеров](https://Gallery.TechNet.Microsoft.Com/b92f894c-5cf8-4484-b5f0-d54761bacd5c) на языке VBScript отключает многоадресную рассылку IGMP на компьютере.</span><span class="sxs-lookup"><span data-stu-id="74399-240">The [Modify the IGMP Level for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/b92f894c-5cf8-4484-b5f0-d54761bacd5c) VBScript sample disables IGMP multicasting on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="74399-241">Требования</span><span class="sxs-lookup"><span data-stu-id="74399-241">Requirements</span></span>



| <span data-ttu-id="74399-242">Требование</span><span class="sxs-lookup"><span data-stu-id="74399-242">Requirement</span></span> | <span data-ttu-id="74399-243">Значение</span><span class="sxs-lookup"><span data-stu-id="74399-243">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74399-244">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74399-244">Minimum supported client</span></span><br/> | <span data-ttu-id="74399-245">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="74399-245">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="74399-246">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="74399-246">Minimum supported server</span></span><br/> | <span data-ttu-id="74399-247">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="74399-247">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="74399-248">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="74399-248">Namespace</span></span><br/>                | <span data-ttu-id="74399-249">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="74399-249">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="74399-250">MOF</span><span class="sxs-lookup"><span data-stu-id="74399-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74399-251"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="74399-251"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="74399-252">DLL</span><span class="sxs-lookup"><span data-stu-id="74399-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74399-253"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74399-253"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74399-254">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74399-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74399-255">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="74399-255">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="74399-256">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="74399-256">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="74399-257">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="74399-257">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="74399-258">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="74399-258">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="74399-259">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="74399-259">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

