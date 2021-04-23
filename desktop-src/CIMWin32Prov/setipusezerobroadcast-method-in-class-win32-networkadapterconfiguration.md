---
description: Статический метод класса WMI Сетипусезероброадкаст используется для задания использования IP-датаграмм без широковещательной рассылки.
ms.assetid: d20ac6fc-a5d5-4ad9-a2a5-65142b4c7d02
ms.tgt_platform: multiple
title: Метод Сетипусезероброадкаст класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPUseZeroBroadcast
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 564f122242407f4d6f5dd28da9fd4d151ab6b47f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141872"
---
# <a name="setipusezerobroadcast-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="9e865-103">Метод Сетипусезероброадкаст \_ класса Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e865-103">SetIPUseZeroBroadcast method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="9e865-104">Статический метод [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) **сетипусезероброадкаст** используется для задания использования IP-датаграмм без широковещательной рассылки.</span><span class="sxs-lookup"><span data-stu-id="9e865-104">The **SetIPUseZeroBroadcast** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set IP zero broadcast usage.</span></span>

<span data-ttu-id="9e865-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="9e865-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9e865-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9e865-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9e865-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e865-107">Syntax</span></span>


```mof
uint32 SetIPUseZeroBroadcast(
  [in] boolean IPUseZeroBroadcast
);
```



## <a name="parameters"></a><span data-ttu-id="9e865-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e865-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e865-109">*Ипусезероброадкаст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9e865-109">*IPUseZeroBroadcast* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e865-110">Если задано **значение true**, используется широковещательная рассылка по IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="9e865-110">If **true**, IP zero broadcast is used.</span></span> <span data-ttu-id="9e865-111">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="9e865-111">The default is **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e865-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9e865-112">Return value</span></span>

<span data-ttu-id="9e865-113">Возвращает значение 0 (ноль) для успешного завершения, если не требуется перезагрузка, 1 (один) для успешного завершения, когда требуется перезагрузка, и другое число в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="9e865-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="9e865-114">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="9e865-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="9e865-115">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="9e865-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="9e865-116">**Успешное завершение, перезагрузка не требуется**</span><span class="sxs-lookup"><span data-stu-id="9e865-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-117">0</span><span class="sxs-lookup"><span data-stu-id="9e865-117">0</span></span>

<span data-ttu-id="9e865-118">Успешное завершение, перезагрузка не требуется.</span><span class="sxs-lookup"><span data-stu-id="9e865-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-119">**Успешное завершение, требуется перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="9e865-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-120">1</span><span class="sxs-lookup"><span data-stu-id="9e865-120">1</span></span>

<span data-ttu-id="9e865-121">Успешное завершение, требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="9e865-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-122">**Метод не поддерживается на этой платформе**</span><span class="sxs-lookup"><span data-stu-id="9e865-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-123">64</span><span class="sxs-lookup"><span data-stu-id="9e865-123">64</span></span>

<span data-ttu-id="9e865-124">Метод не поддерживается на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="9e865-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-125">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="9e865-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-126">65</span><span class="sxs-lookup"><span data-stu-id="9e865-126">65</span></span>

<span data-ttu-id="9e865-127">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="9e865-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-128">**Недопустимая маска подсети**</span><span class="sxs-lookup"><span data-stu-id="9e865-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-129">66</span><span class="sxs-lookup"><span data-stu-id="9e865-129">66</span></span>

<span data-ttu-id="9e865-130">Недопустимая маска подсети.</span><span class="sxs-lookup"><span data-stu-id="9e865-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-131">**Произошла ошибка при обработке возвращенного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="9e865-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-132">67</span><span class="sxs-lookup"><span data-stu-id="9e865-132">67</span></span>

<span data-ttu-id="9e865-133">Произошла ошибка при обработке возвращенного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="9e865-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-134">**Недопустимый входной параметр**</span><span class="sxs-lookup"><span data-stu-id="9e865-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-135">68</span><span class="sxs-lookup"><span data-stu-id="9e865-135">68</span></span>

<span data-ttu-id="9e865-136">Недопустимый входной параметр.</span><span class="sxs-lookup"><span data-stu-id="9e865-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-137">**Указано более 5 шлюзов**</span><span class="sxs-lookup"><span data-stu-id="9e865-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-138">69</span><span class="sxs-lookup"><span data-stu-id="9e865-138">69</span></span>

<span data-ttu-id="9e865-139">Указано более пяти шлюзов.</span><span class="sxs-lookup"><span data-stu-id="9e865-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-140">**Недопустимый IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="9e865-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-141">70</span><span class="sxs-lookup"><span data-stu-id="9e865-141">70</span></span>

<span data-ttu-id="9e865-142">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="9e865-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-143">**Недопустимый IP-адрес шлюза**</span><span class="sxs-lookup"><span data-stu-id="9e865-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-144">71</span><span class="sxs-lookup"><span data-stu-id="9e865-144">71</span></span>

<span data-ttu-id="9e865-145">Недопустимый IP-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="9e865-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-146">**Произошла ошибка при доступе к реестру для запрашиваемой информации**</span><span class="sxs-lookup"><span data-stu-id="9e865-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-147">72</span><span class="sxs-lookup"><span data-stu-id="9e865-147">72</span></span>

<span data-ttu-id="9e865-148">Произошла ошибка при доступе к реестру для запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="9e865-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-149">**Недопустимое имя домена**</span><span class="sxs-lookup"><span data-stu-id="9e865-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-150">73</span><span class="sxs-lookup"><span data-stu-id="9e865-150">73</span></span>

<span data-ttu-id="9e865-151">Недопустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="9e865-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-152">**Недопустимое имя узла**</span><span class="sxs-lookup"><span data-stu-id="9e865-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-153">74</span><span class="sxs-lookup"><span data-stu-id="9e865-153">74</span></span>

<span data-ttu-id="9e865-154">Недопустимое имя узла.</span><span class="sxs-lookup"><span data-stu-id="9e865-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-155">**Не определен основной или дополнительный WINS-сервер**</span><span class="sxs-lookup"><span data-stu-id="9e865-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-156">75</span><span class="sxs-lookup"><span data-stu-id="9e865-156">75</span></span>

<span data-ttu-id="9e865-157">Не определен основной или дополнительный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="9e865-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-158">**Недопустимый файл**</span><span class="sxs-lookup"><span data-stu-id="9e865-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-159">76</span><span class="sxs-lookup"><span data-stu-id="9e865-159">76</span></span>

<span data-ttu-id="9e865-160">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="9e865-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-161">**Недопустимый системный путь**</span><span class="sxs-lookup"><span data-stu-id="9e865-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-162">77</span><span class="sxs-lookup"><span data-stu-id="9e865-162">77</span></span>

<span data-ttu-id="9e865-163">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="9e865-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-164">**Не удалось скопировать файл**</span><span class="sxs-lookup"><span data-stu-id="9e865-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-165">78</span><span class="sxs-lookup"><span data-stu-id="9e865-165">78</span></span>

<span data-ttu-id="9e865-166">Не удалось скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="9e865-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-167">**Недопустимый параметр безопасности**</span><span class="sxs-lookup"><span data-stu-id="9e865-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-168">79</span><span class="sxs-lookup"><span data-stu-id="9e865-168">79</span></span>

<span data-ttu-id="9e865-169">Недопустимый параметр безопасности.</span><span class="sxs-lookup"><span data-stu-id="9e865-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-170">**Не удалось настроить службу TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="9e865-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-171">80</span><span class="sxs-lookup"><span data-stu-id="9e865-171">80</span></span>

<span data-ttu-id="9e865-172">Не удалось настроить службу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="9e865-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-173">**Не удалось настроить службу DHCP**</span><span class="sxs-lookup"><span data-stu-id="9e865-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-174">81</span><span class="sxs-lookup"><span data-stu-id="9e865-174">81</span></span>

<span data-ttu-id="9e865-175">Не удалось настроить службу DHCP.</span><span class="sxs-lookup"><span data-stu-id="9e865-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-176">**Не удалось продлить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="9e865-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-177">82</span><span class="sxs-lookup"><span data-stu-id="9e865-177">82</span></span>

<span data-ttu-id="9e865-178">Не удалось продлить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="9e865-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-179">**Не удалось освободить аренду DHCP**</span><span class="sxs-lookup"><span data-stu-id="9e865-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-180">83</span><span class="sxs-lookup"><span data-stu-id="9e865-180">83</span></span>

<span data-ttu-id="9e865-181">Не удалось освободить аренду DHCP.</span><span class="sxs-lookup"><span data-stu-id="9e865-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-182">**IP-адрес не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="9e865-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-183">84</span><span class="sxs-lookup"><span data-stu-id="9e865-183">84</span></span>

<span data-ttu-id="9e865-184">IP-адрес не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="9e865-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-185">**IPX не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="9e865-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-186">85</span><span class="sxs-lookup"><span data-stu-id="9e865-186">85</span></span>

<span data-ttu-id="9e865-187">IPX не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="9e865-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-188">**Ошибка границ кадра или сети**</span><span class="sxs-lookup"><span data-stu-id="9e865-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-189">86</span><span class="sxs-lookup"><span data-stu-id="9e865-189">86</span></span>

<span data-ttu-id="9e865-190">Ошибка границ кадра или номера сети.</span><span class="sxs-lookup"><span data-stu-id="9e865-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-191">**Недопустимый тип кадра**</span><span class="sxs-lookup"><span data-stu-id="9e865-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-192">87</span><span class="sxs-lookup"><span data-stu-id="9e865-192">87</span></span>

<span data-ttu-id="9e865-193">Недопустимый тип кадра.</span><span class="sxs-lookup"><span data-stu-id="9e865-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-194">**Недопустимый номер сети**</span><span class="sxs-lookup"><span data-stu-id="9e865-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-195">88</span><span class="sxs-lookup"><span data-stu-id="9e865-195">88</span></span>

<span data-ttu-id="9e865-196">Недопустимый номер сети.</span><span class="sxs-lookup"><span data-stu-id="9e865-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-197">**Дублирующийся номер сети**</span><span class="sxs-lookup"><span data-stu-id="9e865-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-198">89</span><span class="sxs-lookup"><span data-stu-id="9e865-198">89</span></span>

<span data-ttu-id="9e865-199">Дублирующийся номер сети.</span><span class="sxs-lookup"><span data-stu-id="9e865-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-200">**Параметр вне границ**</span><span class="sxs-lookup"><span data-stu-id="9e865-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-201">90</span><span class="sxs-lookup"><span data-stu-id="9e865-201">90</span></span>

<span data-ttu-id="9e865-202">Параметр вне допустимых границ.</span><span class="sxs-lookup"><span data-stu-id="9e865-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-203">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="9e865-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-204">91</span><span class="sxs-lookup"><span data-stu-id="9e865-204">91</span></span>

<span data-ttu-id="9e865-205">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="9e865-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-206">**Нет памяти**</span><span class="sxs-lookup"><span data-stu-id="9e865-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-207">92</span><span class="sxs-lookup"><span data-stu-id="9e865-207">92</span></span>

<span data-ttu-id="9e865-208">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="9e865-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-209">**Уже существует**</span><span class="sxs-lookup"><span data-stu-id="9e865-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-210">93</span><span class="sxs-lookup"><span data-stu-id="9e865-210">93</span></span>

<span data-ttu-id="9e865-211">Уже существует.</span><span class="sxs-lookup"><span data-stu-id="9e865-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-212">**Путь, файл или объект не найдены**</span><span class="sxs-lookup"><span data-stu-id="9e865-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-213">94</span><span class="sxs-lookup"><span data-stu-id="9e865-213">94</span></span>

<span data-ttu-id="9e865-214">Путь, файл или объект не найдены.</span><span class="sxs-lookup"><span data-stu-id="9e865-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-215">**Не удалось уведомить службу**</span><span class="sxs-lookup"><span data-stu-id="9e865-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-216">95</span><span class="sxs-lookup"><span data-stu-id="9e865-216">95</span></span>

<span data-ttu-id="9e865-217">Не удалось уведомить службу.</span><span class="sxs-lookup"><span data-stu-id="9e865-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-218">**Не удалось уведомить службу DNS**</span><span class="sxs-lookup"><span data-stu-id="9e865-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-219">96</span><span class="sxs-lookup"><span data-stu-id="9e865-219">96</span></span>

<span data-ttu-id="9e865-220">Не удалось уведомить службу DNS.</span><span class="sxs-lookup"><span data-stu-id="9e865-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-221">**Интерфейс не может быть настроен**</span><span class="sxs-lookup"><span data-stu-id="9e865-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-222">97</span><span class="sxs-lookup"><span data-stu-id="9e865-222">97</span></span>

<span data-ttu-id="9e865-223">Интерфейс недоступен для настройки.</span><span class="sxs-lookup"><span data-stu-id="9e865-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-224">**Не все аренды DHCP могут быть освобождены или обновлены**</span><span class="sxs-lookup"><span data-stu-id="9e865-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-225">98</span><span class="sxs-lookup"><span data-stu-id="9e865-225">98</span></span>

<span data-ttu-id="9e865-226">Не все аренды DHCP могут быть освобождены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="9e865-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-227">**DHCP не включен на адаптере**</span><span class="sxs-lookup"><span data-stu-id="9e865-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-228">100</span><span class="sxs-lookup"><span data-stu-id="9e865-228">100</span></span>

<span data-ttu-id="9e865-229">DHCP не включен на адаптере.</span><span class="sxs-lookup"><span data-stu-id="9e865-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9e865-230">**Другое**</span><span class="sxs-lookup"><span data-stu-id="9e865-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="9e865-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="9e865-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e865-232">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9e865-232">Remarks</span></span>

<span data-ttu-id="9e865-233">Если параметр *ипусезероброадкаст* имеет значение **true**, IP-адрес будет использовать нулевые широковещательные рассылки (0.0.0.0) вместо широковещательных (255.255.255.255).</span><span class="sxs-lookup"><span data-stu-id="9e865-233">If the *IPUseZeroBroadcast* parameter is set to **TRUE**, then IP will use zero-broadcasts (0.0.0.0) instead of one-broadcasts (255.255.255.255).</span></span> <span data-ttu-id="9e865-234">Большинство систем используют один широковещательный, но системы, производные от реализаций BSD, используют нулевые широковещательные рассылки.</span><span class="sxs-lookup"><span data-stu-id="9e865-234">Most systems use one-broadcasts, but systems derived from BSD implementations use zero-broadcasts.</span></span> <span data-ttu-id="9e865-235">Системы, использующие разные широковещательные рассылки, не будут взаимодействовать в одной сети.</span><span class="sxs-lookup"><span data-stu-id="9e865-235">Systems that use different broadcasts will not interoperate on the same network.</span></span>

## <a name="examples"></a><span data-ttu-id="9e865-236">Примеры</span><span class="sxs-lookup"><span data-stu-id="9e865-236">Examples</span></span>

<span data-ttu-id="9e865-237">Пример [изменения Zero-Broadcast использования для всех сетевых адаптеров](https://Gallery.TechNet.Microsoft.Com/3d1ec74a-bf96-41cf-bb90-f98cd6494fb3) VBScript настраивает компьютер для использования нулевых широковещательных рассылок (0.0.0.0), а не широковещательных (255.255.255.255).</span><span class="sxs-lookup"><span data-stu-id="9e865-237">The [Modify Zero-Broadcast Use for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/3d1ec74a-bf96-41cf-bb90-f98cd6494fb3) VBScript sample configures a computer to use zero-broadcasts (0.0.0.0) rather than one-broadcasts (255.255.255.255).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e865-238">Требования</span><span class="sxs-lookup"><span data-stu-id="9e865-238">Requirements</span></span>



| <span data-ttu-id="9e865-239">Требование</span><span class="sxs-lookup"><span data-stu-id="9e865-239">Requirement</span></span> | <span data-ttu-id="9e865-240">Значение</span><span class="sxs-lookup"><span data-stu-id="9e865-240">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e865-241">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9e865-241">Minimum supported client</span></span><br/> | <span data-ttu-id="9e865-242">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9e865-242">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9e865-243">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9e865-243">Minimum supported server</span></span><br/> | <span data-ttu-id="9e865-244">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e865-244">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9e865-245">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9e865-245">Namespace</span></span><br/>                | <span data-ttu-id="9e865-246">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9e865-246">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9e865-247">MOF</span><span class="sxs-lookup"><span data-stu-id="9e865-247">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e865-248"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9e865-248"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e865-249">DLL</span><span class="sxs-lookup"><span data-stu-id="9e865-249">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e865-250"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e865-250"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e865-251">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9e865-251">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e865-252">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="9e865-252">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="9e865-253">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="9e865-253">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="9e865-254">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="9e865-254">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="9e865-255">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="9e865-255">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="9e865-256">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="9e865-256">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

