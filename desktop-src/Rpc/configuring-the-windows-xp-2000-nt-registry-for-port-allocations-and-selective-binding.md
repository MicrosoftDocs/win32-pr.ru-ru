---
title: Настройка реестра для выделения портов и выборочной привязки
description: Начиная с Windows 2000, для установки привязок следует использовать служебную программу в пакете Windows Resource Kit с именем Rpccfg.exe. Дополнительные сведения см. в пакете Windows Resource Kit для соответствующей версии операционной системы.
ms.assetid: a33b51e7-2ded-46bd-aadb-27cbd99e1029
keywords:
- Удаленный вызов процедур RPC, задачи, Настройка реестра для выделения портов и выборочная привязка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ef1749fab1beb8e637d208a7d7af64577066fe6
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "103987961"
---
# <a name="configuring-the-registry-for-port-allocations-and-selective-binding"></a><span data-ttu-id="5a116-105">Настройка реестра для выделения портов и выборочной привязки</span><span class="sxs-lookup"><span data-stu-id="5a116-105">Configuring the Registry for Port Allocations and Selective Binding</span></span>

<span data-ttu-id="5a116-106">Начиная с Windows 2000, для установки привязок следует использовать служебную программу в пакете Windows Resource Kit с именем Rpccfg.exe.</span><span class="sxs-lookup"><span data-stu-id="5a116-106">Starting with Windows 2000, a utility in the Windows Resource Kit called Rpccfg.exe should be used to set bindings.</span></span> <span data-ttu-id="5a116-107">Дополнительные сведения см. в пакете Windows Resource Kit для соответствующей версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="5a116-107">For more information, consult the Windows Resource Kit for the appropriate operating system version.</span></span>

<span data-ttu-id="5a116-108">Для версий Windows, предшествовавших Windows 2000, в разделах реестра в следующей таблице указаны системные значения по умолчанию для динамического выделения портов и привязки к сетевым картам на многосетевых компьютерах.</span><span class="sxs-lookup"><span data-stu-id="5a116-108">For versions of windows prior to Windows 2000, the registry keys in the following table specify the system defaults for dynamic port allocation and for binding to NICs on multihomed computers.</span></span> <span data-ttu-id="5a116-109">Сначала необходимо создать эти ключи, а затем указать соответствующие параметры.</span><span class="sxs-lookup"><span data-stu-id="5a116-109">You must first create these keys and then specify the appropriate settings.</span></span>

<span data-ttu-id="5a116-110">Применение функции [**рпксерверусепротсекекс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) влияет на эти параметры.</span><span class="sxs-lookup"><span data-stu-id="5a116-110">Using the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function affects these settings.</span></span> <span data-ttu-id="5a116-111">Разработчикам следует ознакомиться с параметрами реестра, описанными в этом разделе, и функцией **рпксерверусепротсекекс** при управлении выделением портов.</span><span class="sxs-lookup"><span data-stu-id="5a116-111">Developers should be familiar with the registry settings explained in this section and the **RpcServerUseProtseqEx** function when managing port allocations.</span></span> <span data-ttu-id="5a116-112">Пример с тремя гипотетическыми приложениями следует таблицей ниже и иллюстрирует взаимодействие этих параметров и функции **рпксерверусепротсекекс** .</span><span class="sxs-lookup"><span data-stu-id="5a116-112">An example with three hypothetical applications follows the table below, and illustrates how these settings and the **RpcServerUseProtseqEx** function interoperate.</span></span>

<span data-ttu-id="5a116-113">Если ключ отсутствует или содержит недопустимое значение, вся конфигурация помечается как недопустимая, и все вызовы **рпксерверусепротсек \*** через [**нкакн \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp) или [**нкадг \_ IP \_ UDP**](/windows/desktop/Midl/ncadg-ip-udp) завершатся сбоем.</span><span class="sxs-lookup"><span data-stu-id="5a116-113">If a key is missing or if it contains an invalid value, the entire configuration is marked as invalid, and all **RpcServerUseProtseq\*** calls over [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp) or [**ncadg\_ip\_udp**](/windows/desktop/Midl/ncadg-ip-udp) will fail.</span></span>

> [!Note]  
> <span data-ttu-id="5a116-114">Порты, выделенные для процесса, остаются выделенными до тех пор, пока процесс не завершится.</span><span class="sxs-lookup"><span data-stu-id="5a116-114">Ports allocated to a process remain allocated until that process dies.</span></span> <span data-ttu-id="5a116-115">Если все доступные порты используются, функция возвращает RPC \_ S \_ \_ из \_ ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5a116-115">If all available ports are in use, the function returns RPC\_S\_OUT\_OF\_RESOURCES.</span></span>

 



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5a116-116">Ключ порта</span><span class="sxs-lookup"><span data-stu-id="5a116-116">Port key</span></span></th>
<th><span data-ttu-id="5a116-117">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5a116-117">Data type</span></span></th>
<th><span data-ttu-id="5a116-118">Описание</span><span class="sxs-lookup"><span data-stu-id="5a116-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               Ports</code></pre></td>
<td><span data-ttu-id="5a116-119"><strong>REG_MULTI_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="5a116-119"><strong>REG_MULTI_SZ</strong></span></span></td>
<td><span data-ttu-id="5a116-120">Указывает набор диапазонов IP-портов, состоящий из всех портов, доступных из Интернета, или всех портов, недоступных через Интернет.</span><span class="sxs-lookup"><span data-stu-id="5a116-120">Specifies a set of IP port ranges consisting of either all the ports available from the Internet or all the ports not available from the Internet.</span></span> <span data-ttu-id="5a116-121">Каждая строка представляет один порт или включающий набор портов (например, 1000-1050, 1984).</span><span class="sxs-lookup"><span data-stu-id="5a116-121">Each string represents a single port or an inclusive set of ports (for example,1000-1050, 1984).</span></span> <span data-ttu-id="5a116-122">Если какие бы то ни было записи находятся вне диапазона от 0 до 65535 или если любая строка не может быть интерпретирована, то во время выполнения RPC вся конфигурация будет считаться недопустимой.</span><span class="sxs-lookup"><span data-stu-id="5a116-122">If any entries are outside the range 0 to 65535, or if any string cannot be interpreted, the RPC run time will treat the entire configuration as invalid.</span></span></td>
</tr>
<tr class="even">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               PortsInternetAvailable</code></pre></td>
<td><span data-ttu-id="5a116-123"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="5a116-123"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="5a116-124">Y или N (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="5a116-124">Y or N (not case-sensitive).</span></span> <span data-ttu-id="5a116-125">Если да, порты, перечисленные в разделе Ports, являются портами, доступными через Интернет на этом компьютере.</span><span class="sxs-lookup"><span data-stu-id="5a116-125">If Y, the ports listed in the Ports key are all the Internet-available ports on that computer.</span></span> <span data-ttu-id="5a116-126">Если N, порты, перечисленные в разделе Ports, являются портами, которые не являются доступными в Интернете.</span><span class="sxs-lookup"><span data-stu-id="5a116-126">If N, the ports listed in the Ports key are all those ports that are not Internet-available.</span></span></td>
</tr>
<tr class="odd">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               UseInternetPorts</code></pre></td>
<td><span data-ttu-id="5a116-127"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="5a116-127"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="5a116-128">Y или N (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="5a116-128">Y or N (not case-sensitive).</span></span> <span data-ttu-id="5a116-129">Задает системную политику по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5a116-129">Specifies the system default policy.</span></span> <span data-ttu-id="5a116-130">Если да, то процессам, использующим значение по умолчанию, назначаются порты из набора портов, доступных в Интернете, как определено выше.</span><span class="sxs-lookup"><span data-stu-id="5a116-130">If Y, the processes using the default will be assigned ports from the set of Internet-available ports, as defined above.</span></span> <span data-ttu-id="5a116-131">Если N, то для процессов, использующих значение по умолчанию, будут назначены порты из набора портов только для интрасети.</span><span class="sxs-lookup"><span data-stu-id="5a116-131">If N, processes using the default will be assigned ports from the set of intranet-only ports.</span></span></td>
</tr>
<tr class="even">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rpc
               Linkage
                  Bind</code></pre></td>
<td><span data-ttu-id="5a116-132"><strong>REG_MULTI_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="5a116-132"><strong>REG_MULTI_SZ</strong></span></span></td>
<td><span data-ttu-id="5a116-133">Список имен устройств всех сетевых адаптеров, по умолчанию которые привязаны (например, \Device\AMDPCN1).</span><span class="sxs-lookup"><span data-stu-id="5a116-133">Lists the device names of all the NICs on which to bind by default (for example, \Device\AMDPCN1).</span></span> <span data-ttu-id="5a116-134">Если ключ не существует, сервер будет привязан ко всем сетевым картам.</span><span class="sxs-lookup"><span data-stu-id="5a116-134">If the key does not exist, the server will bind to all NICs.</span></span> <span data-ttu-id="5a116-135">Если ключ существует, сервер будет привязан к сетевым адаптерам, указанным в ключе, если для поля Никфлагс не задано значение RPC_C_BIND_TO_ALL_NICS.</span><span class="sxs-lookup"><span data-stu-id="5a116-135">If the key does exist, the server will bind to the NICs specified in the key, unless the NICFlags field is set to RPC_C_BIND_TO_ALL_NICS.</span></span> <span data-ttu-id="5a116-136">Если ключ имеет значение null ( &quot; &quot; ), то конфигурация будет помечена как недопустимая и все вызовы <strong>рпксерверусепротсек \*</strong> через <a href="/windows/desktop/Midl/ncacn-ip-tcp"><strong>ncacn_ip_tcp</strong></a> или <a href="/windows/desktop/Midl/ncadg-ip-udp"><strong>ncadg_ip_udp</strong></a> завершатся ошибкой.</span><span class="sxs-lookup"><span data-stu-id="5a116-136">If the key has a null (&quot;&quot;) value, the configuration will be marked as invalid and all calls to <strong>RpcServerUseProtseq\*</strong> over <a href="/windows/desktop/Midl/ncacn-ip-tcp"><strong>ncacn_ip_tcp</strong></a> or <a href="/windows/desktop/Midl/ncadg-ip-udp"><strong>ncadg_ip_udp</strong></a> will fail.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5a116-137">В следующей таблице показано, как на три примера приложений влияют параметры, определенные в предыдущей таблице, а также влияние на параметры, применяемые с помощью функции [**рпксерверусепротсекекс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) .</span><span class="sxs-lookup"><span data-stu-id="5a116-137">The following table illustrates how three sample applications are affected by the settings defined in the previous table, and how settings applied using the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function are also affected.</span></span>

<span data-ttu-id="5a116-138">В этом примере рассматриваются три гипотетических приложения:</span><span class="sxs-lookup"><span data-stu-id="5a116-138">In this example, three hypothetical applications are considered:</span></span>

-   <span data-ttu-id="5a116-139">Интернетапп: это приложение предназначено для работы в Интернете, и \_ \_ \_ \_ в элементе **ендпоинтфлагс** структуры [**\_ политики RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) , переданном в функцию [**рпксерверусепротсекекс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) , указан порт Интернета, используемый RPC C.</span><span class="sxs-lookup"><span data-stu-id="5a116-139">InternetApp: This application is intended for exposure to the Internet, and has specified RPC\_C\_USE\_INTERNET\_PORT in the **EndpointFlags** member of the [**RPC\_POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) structure passed to the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function.</span></span>
-   <span data-ttu-id="5a116-140">Локалапп: это приложение не предназначено для доступа к Интернету и указало \_ \_ \_ порт интрасети RPC C \_ в члене **ендпоинтфлагс** структуры [**\_ политики RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) , передаваемой функции [**рпксерверусепротсекекс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) .</span><span class="sxs-lookup"><span data-stu-id="5a116-140">LocalApp: This application is not intended for exposure to the Internet, and has specified RPC\_C\_USE\_INTRANET\_PORT in the **EndpointFlags** member of the [**RPC\_POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) structure passed to the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function.</span></span>
-   <span data-ttu-id="5a116-141">DefaultApp: это приложение задает ноль в члене **ендпоинтфлагс** структуры [**\_ политики RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) , передаваемой функции [**рпксерверусепротсекекс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) .</span><span class="sxs-lookup"><span data-stu-id="5a116-141">DefaultApp: This application specifies zero in the **EndpointFlags** member of the [**RPC\_POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) structure passed to the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function.</span></span>

<span data-ttu-id="5a116-142">В следующей таблице объясняется влияние этих параметров на значения, указанные в записях реестра, описанных в предыдущей таблице.</span><span class="sxs-lookup"><span data-stu-id="5a116-142">The following table explains the impact these settings have based on values specified in the registry entries explained in the previous table.</span></span> <span data-ttu-id="5a116-143">При форматировании необходимо назначить следующие коды:</span><span class="sxs-lookup"><span data-stu-id="5a116-143">For formatting considerations, the following codes are assigned:</span></span>

<span data-ttu-id="5a116-144">PIA = Портсинтернетаваилабле значение ключа</span><span class="sxs-lookup"><span data-stu-id="5a116-144">PIA = PortsInternetAvailable Key value</span></span>

<span data-ttu-id="5a116-145">УиП = значение ключа Усеинтернетпортс</span><span class="sxs-lookup"><span data-stu-id="5a116-145">UIP = UseInternetPorts Key value</span></span>

<span data-ttu-id="5a116-146">Значение ключа ports для этого примера — 5000-5100 для каждой записи.</span><span class="sxs-lookup"><span data-stu-id="5a116-146">The value of the Ports key, for sake of this example, is 5000-5100 for each entry.</span></span>



| <span data-ttu-id="5a116-147">Приложение</span><span class="sxs-lookup"><span data-stu-id="5a116-147">Application</span></span> | <span data-ttu-id="5a116-148">основная сборка взаимодействия</span><span class="sxs-lookup"><span data-stu-id="5a116-148">PIA</span></span> | <span data-ttu-id="5a116-149">уип</span><span class="sxs-lookup"><span data-stu-id="5a116-149">UIP</span></span> | <span data-ttu-id="5a116-150">Результат</span><span class="sxs-lookup"><span data-stu-id="5a116-150">Result</span></span>                                  |
|-------------|-----|-----|-----------------------------------------|
| <span data-ttu-id="5a116-151">интернетапп</span><span class="sxs-lookup"><span data-stu-id="5a116-151">InternetApp</span></span> | <span data-ttu-id="5a116-152">Да</span><span class="sxs-lookup"><span data-stu-id="5a116-152">Y</span></span>   | <span data-ttu-id="5a116-153">Да</span><span class="sxs-lookup"><span data-stu-id="5a116-153">Y</span></span>   | <span data-ttu-id="5a116-154">Использует порты от 5000 до 5100</span><span class="sxs-lookup"><span data-stu-id="5a116-154">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="5a116-155">локалапп</span><span class="sxs-lookup"><span data-stu-id="5a116-155">LocalApp</span></span>    | <span data-ttu-id="5a116-156">Да</span><span class="sxs-lookup"><span data-stu-id="5a116-156">Y</span></span>   | <span data-ttu-id="5a116-157">Да</span><span class="sxs-lookup"><span data-stu-id="5a116-157">Y</span></span>   | <span data-ttu-id="5a116-158">Использует порт за пределами диапазона 5000-5100</span><span class="sxs-lookup"><span data-stu-id="5a116-158">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="5a116-159">DefaultApp</span><span class="sxs-lookup"><span data-stu-id="5a116-159">DefaultApp</span></span>  | <span data-ttu-id="5a116-160">Да</span><span class="sxs-lookup"><span data-stu-id="5a116-160">Y</span></span>   | <span data-ttu-id="5a116-161">Да</span><span class="sxs-lookup"><span data-stu-id="5a116-161">Y</span></span>   | <span data-ttu-id="5a116-162">Использует порты от 5000 до 5100</span><span class="sxs-lookup"><span data-stu-id="5a116-162">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="5a116-163">интернетапп</span><span class="sxs-lookup"><span data-stu-id="5a116-163">InternetApp</span></span> | <span data-ttu-id="5a116-164">Да</span><span class="sxs-lookup"><span data-stu-id="5a116-164">Y</span></span>   | <span data-ttu-id="5a116-165">Нет</span><span class="sxs-lookup"><span data-stu-id="5a116-165">N</span></span>   | <span data-ttu-id="5a116-166">Использует порты от 5000 до 5100</span><span class="sxs-lookup"><span data-stu-id="5a116-166">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="5a116-167">локалапп</span><span class="sxs-lookup"><span data-stu-id="5a116-167">LocalApp</span></span>    | <span data-ttu-id="5a116-168">Да</span><span class="sxs-lookup"><span data-stu-id="5a116-168">Y</span></span>   | <span data-ttu-id="5a116-169">Нет</span><span class="sxs-lookup"><span data-stu-id="5a116-169">N</span></span>   | <span data-ttu-id="5a116-170">Использует порт за пределами диапазона 5000-5100</span><span class="sxs-lookup"><span data-stu-id="5a116-170">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="5a116-171">DefaultApp</span><span class="sxs-lookup"><span data-stu-id="5a116-171">DefaultApp</span></span>  | <span data-ttu-id="5a116-172">Да</span><span class="sxs-lookup"><span data-stu-id="5a116-172">Y</span></span>   | <span data-ttu-id="5a116-173">Нет</span><span class="sxs-lookup"><span data-stu-id="5a116-173">N</span></span>   | <span data-ttu-id="5a116-174">Использует порт за пределами диапазона 5000-5100</span><span class="sxs-lookup"><span data-stu-id="5a116-174">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="5a116-175">интернетапп</span><span class="sxs-lookup"><span data-stu-id="5a116-175">InternetApp</span></span> | <span data-ttu-id="5a116-176">Нет</span><span class="sxs-lookup"><span data-stu-id="5a116-176">N</span></span>   | <span data-ttu-id="5a116-177">Да</span><span class="sxs-lookup"><span data-stu-id="5a116-177">Y</span></span>   | <span data-ttu-id="5a116-178">Использует порт за пределами диапазона 5000-5100</span><span class="sxs-lookup"><span data-stu-id="5a116-178">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="5a116-179">локалапп</span><span class="sxs-lookup"><span data-stu-id="5a116-179">LocalApp</span></span>    | <span data-ttu-id="5a116-180">Нет</span><span class="sxs-lookup"><span data-stu-id="5a116-180">N</span></span>   | <span data-ttu-id="5a116-181">Да</span><span class="sxs-lookup"><span data-stu-id="5a116-181">Y</span></span>   | <span data-ttu-id="5a116-182">Использует порты от 5000 до 5100</span><span class="sxs-lookup"><span data-stu-id="5a116-182">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="5a116-183">DefaultApp</span><span class="sxs-lookup"><span data-stu-id="5a116-183">DefaultApp</span></span>  | <span data-ttu-id="5a116-184">Нет</span><span class="sxs-lookup"><span data-stu-id="5a116-184">N</span></span>   | <span data-ttu-id="5a116-185">Да</span><span class="sxs-lookup"><span data-stu-id="5a116-185">Y</span></span>   | <span data-ttu-id="5a116-186">Использует порт за пределами диапазона 5000-5100</span><span class="sxs-lookup"><span data-stu-id="5a116-186">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="5a116-187">интернетапп</span><span class="sxs-lookup"><span data-stu-id="5a116-187">InternetApp</span></span> | <span data-ttu-id="5a116-188">Нет</span><span class="sxs-lookup"><span data-stu-id="5a116-188">N</span></span>   | <span data-ttu-id="5a116-189">Нет</span><span class="sxs-lookup"><span data-stu-id="5a116-189">N</span></span>   | <span data-ttu-id="5a116-190">Использует порт за пределами диапазона 5000-5100</span><span class="sxs-lookup"><span data-stu-id="5a116-190">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="5a116-191">локалапп</span><span class="sxs-lookup"><span data-stu-id="5a116-191">LocalApp</span></span>    | <span data-ttu-id="5a116-192">Нет</span><span class="sxs-lookup"><span data-stu-id="5a116-192">N</span></span>   | <span data-ttu-id="5a116-193">Нет</span><span class="sxs-lookup"><span data-stu-id="5a116-193">N</span></span>   | <span data-ttu-id="5a116-194">Использует порты от 5000 до 5100</span><span class="sxs-lookup"><span data-stu-id="5a116-194">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="5a116-195">DefaultApp</span><span class="sxs-lookup"><span data-stu-id="5a116-195">DefaultApp</span></span>  | <span data-ttu-id="5a116-196">Нет</span><span class="sxs-lookup"><span data-stu-id="5a116-196">N</span></span>   | <span data-ttu-id="5a116-197">Нет</span><span class="sxs-lookup"><span data-stu-id="5a116-197">N</span></span>   | <span data-ttu-id="5a116-198">Использует порты от 5000 до 5100</span><span class="sxs-lookup"><span data-stu-id="5a116-198">Uses ports between 5000 and 5100</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5a116-199">См. также</span><span class="sxs-lookup"><span data-stu-id="5a116-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a116-200">**\_Политика RPC**</span><span class="sxs-lookup"><span data-stu-id="5a116-200">**RPC\_POLICY**</span></span>](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy)
</dt> <dt>

[<span data-ttu-id="5a116-201">**рпксерверусеаллпротсексекс**</span><span class="sxs-lookup"><span data-stu-id="5a116-201">**RpcServerUseAllProtseqsEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsex)
</dt> <dt>

[<span data-ttu-id="5a116-202">**рпксерверусеаллпротсексифекс**</span><span class="sxs-lookup"><span data-stu-id="5a116-202">**RpcServerUseAllProtseqsIfEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex)
</dt> <dt>

[<span data-ttu-id="5a116-203">**рпксерверусепротсекекс**</span><span class="sxs-lookup"><span data-stu-id="5a116-203">**RpcServerUseProtseqEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex)
</dt> <dt>

[<span data-ttu-id="5a116-204">**рпксерверусепротсекепекс**</span><span class="sxs-lookup"><span data-stu-id="5a116-204">**RpcServerUseProtseqEpEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex)
</dt> <dt>

[<span data-ttu-id="5a116-205">**рпксерверусепротсекифекс**</span><span class="sxs-lookup"><span data-stu-id="5a116-205">**RpcServerUseProtseqIfEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqifex)
</dt> <dt>

[<span data-ttu-id="5a116-206">**нкакн \_ IP \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="5a116-206">**ncacn\_ip\_tcp**</span></span>](/windows/desktop/Midl/ncacn-ip-tcp)
</dt> <dt>

[<span data-ttu-id="5a116-207">**нкадг \_ IP \_ UDP**</span><span class="sxs-lookup"><span data-stu-id="5a116-207">**ncadg\_ip\_udp**</span></span>](/windows/desktop/Midl/ncadg-ip-udp)
</dt> </dl>

 

 