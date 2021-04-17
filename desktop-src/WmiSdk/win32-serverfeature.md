---
description: Класс Win32 \_ ServerFeature представляет компоненты, установленные на компьютере под Windows Server.
ms.assetid: fe3bb95c-7f69-47b5-9c3d-771cdc3ed9ca
ms.tgt_platform: multiple
title: Класс Win32_ServerFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ServerFeature
- Win32_ServerFeature.ID
- Win32_ServerFeature.ParentID
- Win32_ServerFeature.Name
api_type:
- DllExport
api_location:
- ServerCompProv.dll
ms.openlocfilehash: 1be8a2ea1d646e9d882febc7c8eba08b69bb69f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703112"
---
# <a name="win32_serverfeature-class"></a><span data-ttu-id="74210-103">\_Класс Win32 ServerFeature</span><span class="sxs-lookup"><span data-stu-id="74210-103">Win32\_ServerFeature class</span></span>

<span data-ttu-id="74210-104">\[Класс **Win32 \_ ServerFeature** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="74210-104">\[The **Win32\_ServerFeature** class is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="74210-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="74210-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="74210-106">Вместо этого используйте [классы поставщика ServerManager deploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment).\]</span><span class="sxs-lookup"><span data-stu-id="74210-106">Instead, use the [ServerManager Deploymentprovider Provider Classes](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment).\]</span></span>

<span data-ttu-id="74210-107">Класс **Win32 \_ ServerFeature** представляет компоненты, установленные на компьютере под Windows Server.</span><span class="sxs-lookup"><span data-stu-id="74210-107">The **Win32\_ServerFeature** class represents the features installed on a computer running Windows Server.</span></span>

<span data-ttu-id="74210-108">Этот класс может использоваться разработчиками и администраторами, которым необходимо автоматизировать процесс определения функций, установленных на наборе серверных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="74210-108">This class can be used by developers and administrators who need to automate the process of determining the features installed on a set of server computers.</span></span> <span data-ttu-id="74210-109">Экземпляры этого класса недоступны на клиентских компьютерах.</span><span class="sxs-lookup"><span data-stu-id="74210-109">Instances of this class are not available on client computers.</span></span>

## <a name="syntax"></a><span data-ttu-id="74210-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74210-110">Syntax</span></span>

``` syntax
[Deprecated("No value"), Dynamic, Provider("ServerFeatureProvider"), AMENDMENT]
class Win32_ServerFeature
{
  uint32 ID;
  uint32 ParentID;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="74210-111">Члены</span><span class="sxs-lookup"><span data-stu-id="74210-111">Members</span></span>

<span data-ttu-id="74210-112">Класс **Win32 \_ ServerFeature** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="74210-112">The **Win32\_ServerFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="74210-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="74210-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="74210-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="74210-114">Properties</span></span>

<span data-ttu-id="74210-115">Класс **Win32 \_ ServerFeature** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="74210-115">The **Win32\_ServerFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="74210-116">**Идентификатор**</span><span class="sxs-lookup"><span data-stu-id="74210-116">**ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74210-117">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74210-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74210-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="74210-118">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="74210-119">Квалификаторы: [**ключ**](key-qualifier.md), а [**не \_ null**](optional-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="74210-119">Qualifiers: [**Key**](key-qualifier.md), [**Not\_Null**](optional-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="74210-120">Идентификатор компонента сервера.</span><span class="sxs-lookup"><span data-stu-id="74210-120">Server feature ID.</span></span> <span data-ttu-id="74210-121">В следующем списке приведены возможные значения свойства ID:</span><span class="sxs-lookup"><span data-stu-id="74210-121">The following list shows the possible values of the ID property:</span></span>



<span data-ttu-id="74210-122">Значение</span><span class="sxs-lookup"><span data-stu-id="74210-122">Value</span></span>

<span data-ttu-id="74210-123">Имя</span><span class="sxs-lookup"><span data-stu-id="74210-123">Name</span></span>

<span data-ttu-id="74210-124">1</span><span class="sxs-lookup"><span data-stu-id="74210-124">1</span></span>

[<span data-ttu-id="74210-125">Сервер приложений</span><span class="sxs-lookup"><span data-stu-id="74210-125">Application Server</span></span>](/windows)

<span data-ttu-id="74210-126">2</span><span class="sxs-lookup"><span data-stu-id="74210-126">2</span></span>

<span data-ttu-id="74210-127">Веб-сервер (IIS)</span><span class="sxs-lookup"><span data-stu-id="74210-127">Web Server (IIS)</span></span>

<span data-ttu-id="74210-128">3</span><span class="sxs-lookup"><span data-stu-id="74210-128">3</span></span>

[<span data-ttu-id="74210-129">Службы потоков мультимедиа</span><span class="sxs-lookup"><span data-stu-id="74210-129">Streaming Media Services</span></span>](/windows)

<span data-ttu-id="74210-130">5</span><span class="sxs-lookup"><span data-stu-id="74210-130">5</span></span>

<span data-ttu-id="74210-131">Факс-сервер</span><span class="sxs-lookup"><span data-stu-id="74210-131">Fax Server</span></span>

<span data-ttu-id="74210-132">6</span><span class="sxs-lookup"><span data-stu-id="74210-132">6</span></span>

<span data-ttu-id="74210-133">Файловые службы и службы iSCSI</span><span class="sxs-lookup"><span data-stu-id="74210-133">File and iSCSI Services</span></span><br/> [<span data-ttu-id="74210-134">изменение имени</span><span class="sxs-lookup"><span data-stu-id="74210-134">name change</span></span>](/windows)<br/>

<span data-ttu-id="74210-135">7</span><span class="sxs-lookup"><span data-stu-id="74210-135">7</span></span>

<span data-ttu-id="74210-136">Службы печати и документов</span><span class="sxs-lookup"><span data-stu-id="74210-136">Print and Document Services</span></span><br/> [<span data-ttu-id="74210-137">изменение имени</span><span class="sxs-lookup"><span data-stu-id="74210-137">name change</span></span>](/windows)<br/>

<span data-ttu-id="74210-138">8</span><span class="sxs-lookup"><span data-stu-id="74210-138">8</span></span>

[<span data-ttu-id="74210-139">Службы федерации Active Directory (AD FS)</span><span class="sxs-lookup"><span data-stu-id="74210-139">Active Directory Federation Services</span></span>](/windows)

<span data-ttu-id="74210-140">9</span><span class="sxs-lookup"><span data-stu-id="74210-140">9</span></span>

<span data-ttu-id="74210-141">Службы Active Directory облегченного доступа к каталогам (AD LDS)</span><span class="sxs-lookup"><span data-stu-id="74210-141">Active Directory Lightweight Directory Services</span></span>

<span data-ttu-id="74210-142">10</span><span class="sxs-lookup"><span data-stu-id="74210-142">10</span></span>

<span data-ttu-id="74210-143">Доменные службы Active Directory</span><span class="sxs-lookup"><span data-stu-id="74210-143">Active Directory Domain Services</span></span>

<span data-ttu-id="74210-144">11</span><span class="sxs-lookup"><span data-stu-id="74210-144">11</span></span>

[<span data-ttu-id="74210-145">Службы UDDI</span><span class="sxs-lookup"><span data-stu-id="74210-145">UDDI Services</span></span>](/windows)<br/>

<span data-ttu-id="74210-146">12</span><span class="sxs-lookup"><span data-stu-id="74210-146">12</span></span>

[<span data-ttu-id="74210-147">DHCP-сервер</span><span class="sxs-lookup"><span data-stu-id="74210-147">DHCP Server</span></span>](/windows)

<span data-ttu-id="74210-148">13</span><span class="sxs-lookup"><span data-stu-id="74210-148">13</span></span>

[<span data-ttu-id="74210-149">DNS-сервер</span><span class="sxs-lookup"><span data-stu-id="74210-149">DNS Server</span></span>](/windows)

<span data-ttu-id="74210-150">14</span><span class="sxs-lookup"><span data-stu-id="74210-150">14</span></span>

<span data-ttu-id="74210-151">Network Policy and Access Services</span><span class="sxs-lookup"><span data-stu-id="74210-151">Network Policy and Access Services</span></span>

<span data-ttu-id="74210-152">16</span><span class="sxs-lookup"><span data-stu-id="74210-152">16</span></span>

<span data-ttu-id="74210-153">Службы сертификатов Active Directory</span><span class="sxs-lookup"><span data-stu-id="74210-153">Active Directory Certificate Services</span></span>

<span data-ttu-id="74210-154">17</span><span class="sxs-lookup"><span data-stu-id="74210-154">17</span></span>

<span data-ttu-id="74210-155">Службы управления правами Active Directory (AD RMS)</span><span class="sxs-lookup"><span data-stu-id="74210-155">Active Directory Rights Management Services</span></span>

<span data-ttu-id="74210-156">18</span><span class="sxs-lookup"><span data-stu-id="74210-156">18</span></span>

[<span data-ttu-id="74210-157">Службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="74210-157">Remote Desktop Services</span></span>](/windows)<br/> [<span data-ttu-id="74210-158">изменение имени</span><span class="sxs-lookup"><span data-stu-id="74210-158">name change</span></span>](/windows)<br/>

<span data-ttu-id="74210-159">19</span><span class="sxs-lookup"><span data-stu-id="74210-159">19</span></span>

<span data-ttu-id="74210-160">Windows Deployment Services</span><span class="sxs-lookup"><span data-stu-id="74210-160">Windows Deployment Services</span></span>

<span data-ttu-id="74210-161">20</span><span class="sxs-lookup"><span data-stu-id="74210-161">20</span></span>

<span data-ttu-id="74210-162">Hyper-V</span><span class="sxs-lookup"><span data-stu-id="74210-162">Hyper-V</span></span>

<span data-ttu-id="74210-163">21</span><span class="sxs-lookup"><span data-stu-id="74210-163">21</span></span>

[<span data-ttu-id="74210-164">Службы Windows Server Update Services</span><span class="sxs-lookup"><span data-stu-id="74210-164">Windows Server Update Services</span></span>](/windows)

<span data-ttu-id="74210-165">33</span><span class="sxs-lookup"><span data-stu-id="74210-165">33</span></span>

[<span data-ttu-id="74210-166">Отказоустойчивая кластеризация</span><span class="sxs-lookup"><span data-stu-id="74210-166">Failover Clustering</span></span>](/windows)

<span data-ttu-id="74210-167">34</span><span class="sxs-lookup"><span data-stu-id="74210-167">34</span></span>

[<span data-ttu-id="74210-168">Балансировка сетевой нагрузки</span><span class="sxs-lookup"><span data-stu-id="74210-168">Network Load Balancing</span></span>](/windows)

<span data-ttu-id="74210-169">36</span><span class="sxs-lookup"><span data-stu-id="74210-169">36</span></span>

[<span data-ttu-id="74210-170">Компоненты .NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="74210-170">.NET Framework 3.5.1 Features</span></span>](/windows)<br/> [<span data-ttu-id="74210-171">изменение имени</span><span class="sxs-lookup"><span data-stu-id="74210-171">name change</span></span>](/windows)<br/>

<span data-ttu-id="74210-172">37</span><span class="sxs-lookup"><span data-stu-id="74210-172">37</span></span>

[<span data-ttu-id="74210-173">Диспетчер системных ресурсов Windows</span><span class="sxs-lookup"><span data-stu-id="74210-173">Windows System Resource Manager</span></span>](/windows)

<span data-ttu-id="74210-174">38</span><span class="sxs-lookup"><span data-stu-id="74210-174">38</span></span>

<span data-ttu-id="74210-175">Служба беспроводной локальной сети</span><span class="sxs-lookup"><span data-stu-id="74210-175">Wireless LAN Service</span></span>

<span data-ttu-id="74210-176">39</span><span class="sxs-lookup"><span data-stu-id="74210-176">39</span></span>

[<span data-ttu-id="74210-177">cистема архивации данных Windows Server функции</span><span class="sxs-lookup"><span data-stu-id="74210-177">Windows Server Backup Features</span></span>](/windows)

<span data-ttu-id="74210-178">40</span><span class="sxs-lookup"><span data-stu-id="74210-178">40</span></span>

<span data-ttu-id="74210-179">WINS-сервер</span><span class="sxs-lookup"><span data-stu-id="74210-179">WINS Server</span></span>

<span data-ttu-id="74210-180">41</span><span class="sxs-lookup"><span data-stu-id="74210-180">41</span></span>

<span data-ttu-id="74210-181">Служба активации процессов Windows</span><span class="sxs-lookup"><span data-stu-id="74210-181">Windows Process Activation Service</span></span>

<span data-ttu-id="74210-182">42</span><span class="sxs-lookup"><span data-stu-id="74210-182">42</span></span>

[<span data-ttu-id="74210-183">Удаленный помощник</span><span class="sxs-lookup"><span data-stu-id="74210-183">Remote Assistance</span></span>](/windows)

<span data-ttu-id="74210-184">43</span><span class="sxs-lookup"><span data-stu-id="74210-184">43</span></span>

<span data-ttu-id="74210-185">простые службы TCP/IP;</span><span class="sxs-lookup"><span data-stu-id="74210-185">Simple TCP/IP Services</span></span>

<span data-ttu-id="74210-186">44</span><span class="sxs-lookup"><span data-stu-id="74210-186">44</span></span>

[<span data-ttu-id="74210-187">Клиент Telnet</span><span class="sxs-lookup"><span data-stu-id="74210-187">Telnet Client</span></span>](/windows)

<span data-ttu-id="74210-188">45</span><span class="sxs-lookup"><span data-stu-id="74210-188">45</span></span>

[<span data-ttu-id="74210-189">Сервер Telnet</span><span class="sxs-lookup"><span data-stu-id="74210-189">Telnet Server</span></span>](/windows)

<span data-ttu-id="74210-190">46</span><span class="sxs-lookup"><span data-stu-id="74210-190">46</span></span>

[<span data-ttu-id="74210-191">Подсистема для приложений на базе UNIX</span><span class="sxs-lookup"><span data-stu-id="74210-191">Subsystem For Unix-based Applications</span></span>](/windows)

<span data-ttu-id="74210-192">47</span><span class="sxs-lookup"><span data-stu-id="74210-192">47</span></span>

<span data-ttu-id="74210-193">Прокси-сервер RPC через HTTP</span><span class="sxs-lookup"><span data-stu-id="74210-193">RPC Over HTTP Proxy</span></span>

<span data-ttu-id="74210-194">48</span><span class="sxs-lookup"><span data-stu-id="74210-194">48</span></span>

<span data-ttu-id="74210-195">SMTP-сервер</span><span class="sxs-lookup"><span data-stu-id="74210-195">SMTP Server</span></span>

<span data-ttu-id="74210-196">49</span><span class="sxs-lookup"><span data-stu-id="74210-196">49</span></span>

<span data-ttu-id="74210-197">служба очередей сообщений</span><span class="sxs-lookup"><span data-stu-id="74210-197">Message Queuing</span></span>

<span data-ttu-id="74210-198">51</span><span class="sxs-lookup"><span data-stu-id="74210-198">51</span></span>

[<span data-ttu-id="74210-199">Внутренняя база данных Windows</span><span class="sxs-lookup"><span data-stu-id="74210-199">Windows Internal Database</span></span>](/windows)

<span data-ttu-id="74210-200">52</span><span class="sxs-lookup"><span data-stu-id="74210-200">52</span></span>

[<span data-ttu-id="74210-201">Диспетчер хранилища для сетей SAN</span><span class="sxs-lookup"><span data-stu-id="74210-201">Storage Manager For SANs</span></span>](/windows)

<span data-ttu-id="74210-202">53</span><span class="sxs-lookup"><span data-stu-id="74210-202">53</span></span>

<span data-ttu-id="74210-203">Монитор порта LPR</span><span class="sxs-lookup"><span data-stu-id="74210-203">LPR Port Monitor</span></span>

<span data-ttu-id="74210-204">55</span><span class="sxs-lookup"><span data-stu-id="74210-204">55</span></span>

[<span data-ttu-id="74210-205">Сервер имен интернет-хранилища</span><span class="sxs-lookup"><span data-stu-id="74210-205">Internet Storage Name Server</span></span>](/windows)

<span data-ttu-id="74210-206">57</span><span class="sxs-lookup"><span data-stu-id="74210-206">57</span></span>

[<span data-ttu-id="74210-207">Multipath I/O;</span><span class="sxs-lookup"><span data-stu-id="74210-207">Multipath I/O</span></span>](/windows)

<span data-ttu-id="74210-208">58</span><span class="sxs-lookup"><span data-stu-id="74210-208">58</span></span>

<span data-ttu-id="74210-209">TFTP-клиент</span><span class="sxs-lookup"><span data-stu-id="74210-209">TFTP Client</span></span>

<span data-ttu-id="74210-210">59</span><span class="sxs-lookup"><span data-stu-id="74210-210">59</span></span>

[<span data-ttu-id="74210-211">Службы SNMP</span><span class="sxs-lookup"><span data-stu-id="74210-211">SNMP Services</span></span>](/windows)

<span data-ttu-id="74210-212">60</span><span class="sxs-lookup"><span data-stu-id="74210-212">60</span></span>

[<span data-ttu-id="74210-213">Диспетчер съемных носителей</span><span class="sxs-lookup"><span data-stu-id="74210-213">Removable Storage Manager</span></span>](/windows)

<span data-ttu-id="74210-214">61</span><span class="sxs-lookup"><span data-stu-id="74210-214">61</span></span>

<span data-ttu-id="74210-215">Шифрование диска BitLocker</span><span class="sxs-lookup"><span data-stu-id="74210-215">BitLocker Drive Encryption</span></span>

<span data-ttu-id="74210-216">62</span><span class="sxs-lookup"><span data-stu-id="74210-216">62</span></span>

[<span data-ttu-id="74210-217">Службы для сетевой файловой системы</span><span class="sxs-lookup"><span data-stu-id="74210-217">Services For Network File System</span></span>](/windows)

<span data-ttu-id="74210-218">63</span><span class="sxs-lookup"><span data-stu-id="74210-218">63</span></span>

<span data-ttu-id="74210-219">Клиент печати через Интернет</span><span class="sxs-lookup"><span data-stu-id="74210-219">Internet Printing Client</span></span>

<span data-ttu-id="74210-220">64</span><span class="sxs-lookup"><span data-stu-id="74210-220">64</span></span>

[<span data-ttu-id="74210-221">Протокол PNRP</span><span class="sxs-lookup"><span data-stu-id="74210-221">Peer Name Resolution Protocol</span></span>](/windows)

<span data-ttu-id="74210-222">65</span><span class="sxs-lookup"><span data-stu-id="74210-222">65</span></span>

<span data-ttu-id="74210-223">Пакет администрирования диспетчера подключений</span><span class="sxs-lookup"><span data-stu-id="74210-223">Connection Manager Administration Kit</span></span>

<span data-ttu-id="74210-224">66</span><span class="sxs-lookup"><span data-stu-id="74210-224">66</span></span>

[<span data-ttu-id="74210-225">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="74210-225">Windows PowerShell</span></span>](/windows)<br/>

<span data-ttu-id="74210-226">67</span><span class="sxs-lookup"><span data-stu-id="74210-226">67</span></span>

[<span data-ttu-id="74210-227">Средства удаленного администрирования сервера</span><span class="sxs-lookup"><span data-stu-id="74210-227">Remote Server Administration Tools</span></span>](/windows)

<span data-ttu-id="74210-228">68</span><span class="sxs-lookup"><span data-stu-id="74210-228">68</span></span>

[<span data-ttu-id="74210-229">qWave;</span><span class="sxs-lookup"><span data-stu-id="74210-229">Quality Windows Audio Video Experience</span></span>](/windows)

<span data-ttu-id="74210-230">69</span><span class="sxs-lookup"><span data-stu-id="74210-230">69</span></span>

[<span data-ttu-id="74210-231">Управление групповой политикой</span><span class="sxs-lookup"><span data-stu-id="74210-231">Group Policy Management</span></span>](/windows)

<span data-ttu-id="74210-232">71</span><span class="sxs-lookup"><span data-stu-id="74210-232">71</span></span>

[<span data-ttu-id="74210-233">служба индексирования</span><span class="sxs-lookup"><span data-stu-id="74210-233">Indexing Service</span></span>](/windows)

<span data-ttu-id="74210-234">72</span><span class="sxs-lookup"><span data-stu-id="74210-234">72</span></span>

[<span data-ttu-id="74210-235">Диспетчер ресурсов файлового сервера</span><span class="sxs-lookup"><span data-stu-id="74210-235">File Server Resource Manager (FSRM)</span></span>](/windows)

<span data-ttu-id="74210-236">73</span><span class="sxs-lookup"><span data-stu-id="74210-236">73</span></span>

<span data-ttu-id="74210-237">Протокол удаленного разностного сжатия</span><span class="sxs-lookup"><span data-stu-id="74210-237">Remote Differential Compression</span></span>

<span data-ttu-id="74210-238">310</span><span class="sxs-lookup"><span data-stu-id="74210-238">310</span></span>

<span data-ttu-id="74210-239">Службы рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="74210-239">Ink and Handwriting Services</span></span><br/>

<span data-ttu-id="74210-240">320</span><span class="sxs-lookup"><span data-stu-id="74210-240">320</span></span>

[<span data-ttu-id="74210-241">Средства миграции Windows Server</span><span class="sxs-lookup"><span data-stu-id="74210-241">Windows Server Migration Tools</span></span>](/windows)<br/>

<span data-ttu-id="74210-242">321</span><span class="sxs-lookup"><span data-stu-id="74210-242">321</span></span>

[<span data-ttu-id="74210-243">Расширение IIS WinRM</span><span class="sxs-lookup"><span data-stu-id="74210-243">WinRM IIS Extension</span></span>](/windows)<br/>

<span data-ttu-id="74210-244">324</span><span class="sxs-lookup"><span data-stu-id="74210-244">324</span></span>

[<span data-ttu-id="74210-245">BranchCache,,</span><span class="sxs-lookup"><span data-stu-id="74210-245">BranchCache</span></span>](#branchcache)<br/>

<span data-ttu-id="74210-246">334</span><span class="sxs-lookup"><span data-stu-id="74210-246">334</span></span>

[<span data-ttu-id="74210-247">Консоль управления DirectAccess</span><span class="sxs-lookup"><span data-stu-id="74210-247">DirectAccess Management Console</span></span>](/windows)<br/>

<span data-ttu-id="74210-248">335</span><span class="sxs-lookup"><span data-stu-id="74210-248">335</span></span>

[<span data-ttu-id="74210-249">Фоновая интеллектуальная служба передачи (BITS)</span><span class="sxs-lookup"><span data-stu-id="74210-249">Background Intelligent Transfer Service (BITS)</span></span>](/windows)<br/>

<span data-ttu-id="74210-250">338</span><span class="sxs-lookup"><span data-stu-id="74210-250">338</span></span>

[<span data-ttu-id="74210-251">Средство просмотра XPS</span><span class="sxs-lookup"><span data-stu-id="74210-251">XPS Viewer</span></span>](/windows)<br/>

<span data-ttu-id="74210-252">339</span><span class="sxs-lookup"><span data-stu-id="74210-252">339</span></span>

[<span data-ttu-id="74210-253">Биометрическая платформа Windows</span><span class="sxs-lookup"><span data-stu-id="74210-253">Windows Biometric Framework</span></span>](/windows)<br/>

<span data-ttu-id="74210-254">340</span><span class="sxs-lookup"><span data-stu-id="74210-254">340</span></span>

<span data-ttu-id="74210-255">Поддержка WoW64</span><span class="sxs-lookup"><span data-stu-id="74210-255">WoW64 Support</span></span><br/>

<span data-ttu-id="74210-256">351</span><span class="sxs-lookup"><span data-stu-id="74210-256">351</span></span>

[<span data-ttu-id="74210-257">Интегрированная среда сценариев Windows PowerShell (ISE)</span><span class="sxs-lookup"><span data-stu-id="74210-257">Windows PowerShell Integrated Scripting Environment (ISE)</span></span>](/windows)<br/>

<span data-ttu-id="74210-258">352</span><span class="sxs-lookup"><span data-stu-id="74210-258">352</span></span>

<span data-ttu-id="74210-259">Фильтры Windows TIFF IFilter</span><span class="sxs-lookup"><span data-stu-id="74210-259">Windows TIFF IFilter</span></span><br/>

<span data-ttu-id="74210-260">404</span><span class="sxs-lookup"><span data-stu-id="74210-260">404</span></span>

[<span data-ttu-id="74210-261">Службы обновления Windows Server</span><span class="sxs-lookup"><span data-stu-id="74210-261">Window Server Update Services</span></span>](/windows)

<span data-ttu-id="74210-262">409</span><span class="sxs-lookup"><span data-stu-id="74210-262">409</span></span>

[<span data-ttu-id="74210-263">Сервер управления IP-адресами (IPAM)</span><span class="sxs-lookup"><span data-stu-id="74210-263">IP Address Management (IPAM) Server</span></span>](/windows)

<span data-ttu-id="74210-264">417</span><span class="sxs-lookup"><span data-stu-id="74210-264">417</span></span>

[<span data-ttu-id="74210-265">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="74210-265">Windows PowerShell</span></span>](/windows)

<span data-ttu-id="74210-266">418</span><span class="sxs-lookup"><span data-stu-id="74210-266">418</span></span>

[<span data-ttu-id="74210-267">.NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="74210-267">.NET Framework 4.5</span></span>](/windows)

<span data-ttu-id="74210-268">432</span><span class="sxs-lookup"><span data-stu-id="74210-268">432</span></span>

[<span data-ttu-id="74210-269">Служба Windows Search</span><span class="sxs-lookup"><span data-stu-id="74210-269">Windows Search Service</span></span>](/windows)

<span data-ttu-id="74210-270">438</span><span class="sxs-lookup"><span data-stu-id="74210-270">438</span></span>

[<span data-ttu-id="74210-271">Клиент для NFS</span><span class="sxs-lookup"><span data-stu-id="74210-271">Client for NFS</span></span>](/windows)

<span data-ttu-id="74210-272">441</span><span class="sxs-lookup"><span data-stu-id="74210-272">441</span></span>

[<span data-ttu-id="74210-273">Сетевая разблокировка BitLocker</span><span class="sxs-lookup"><span data-stu-id="74210-273">BitLocker Network Unlock</span></span>](/windows)

<span data-ttu-id="74210-274">442</span><span class="sxs-lookup"><span data-stu-id="74210-274">442</span></span>

[<span data-ttu-id="74210-275">Расширение IIS OData для управления</span><span class="sxs-lookup"><span data-stu-id="74210-275">Management OData IIS Extension</span></span>](/windows)

<span data-ttu-id="74210-276">450</span><span class="sxs-lookup"><span data-stu-id="74210-276">450</span></span>

[<span data-ttu-id="74210-277">Дополнительные службы .NET Framework 4.5 Advanced Services</span><span class="sxs-lookup"><span data-stu-id="74210-277">.NET Framework 4.5 Advanced Services</span></span>](/windows)

<span data-ttu-id="74210-278">466</span><span class="sxs-lookup"><span data-stu-id="74210-278">466</span></span>

[<span data-ttu-id="74210-279">Компоненты .NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="74210-279">.NET Framework 4.5 Features</span></span>](/windows)

<span data-ttu-id="74210-280">468</span><span class="sxs-lookup"><span data-stu-id="74210-280">468</span></span>

[<span data-ttu-id="74210-281">Удаленный доступ</span><span class="sxs-lookup"><span data-stu-id="74210-281">Remote Access</span></span>](/windows)<br/>

<span data-ttu-id="74210-282">477</span><span class="sxs-lookup"><span data-stu-id="74210-282">477</span></span>

[<span data-ttu-id="74210-283">Пользовательские интерфейсы и инфраструктура</span><span class="sxs-lookup"><span data-stu-id="74210-283">User Interfaces and Infrastructure</span></span>](/windows)

<span data-ttu-id="74210-284">478</span><span class="sxs-lookup"><span data-stu-id="74210-284">478</span></span>

[<span data-ttu-id="74210-285">графические средства управления и инфраструктура.</span><span class="sxs-lookup"><span data-stu-id="74210-285">Graphical Management Tools and Infrastructure</span></span>](/windows)

<span data-ttu-id="74210-286">481</span><span class="sxs-lookup"><span data-stu-id="74210-286">481</span></span>

[<span data-ttu-id="74210-287">Файловые службы и службы хранилища</span><span class="sxs-lookup"><span data-stu-id="74210-287">File and Storage Services</span></span>](/windows)

<span data-ttu-id="74210-288">485</span><span class="sxs-lookup"><span data-stu-id="74210-288">485</span></span>

[<span data-ttu-id="74210-289">Режим Windows Server Essentials</span><span class="sxs-lookup"><span data-stu-id="74210-289">Windows Server Essentials Experience</span></span>](/windows)

<span data-ttu-id="74210-290">488</span><span class="sxs-lookup"><span data-stu-id="74210-290">488</span></span>

[<span data-ttu-id="74210-291">Direct Play</span><span class="sxs-lookup"><span data-stu-id="74210-291">Direct Play</span></span>](/windows)

<span data-ttu-id="74210-292">Файловые службы — службы ролей (6)</span><span class="sxs-lookup"><span data-stu-id="74210-292">File Services - Role Services (6)</span></span>

<span data-ttu-id="74210-293">Значение</span><span class="sxs-lookup"><span data-stu-id="74210-293">Value</span></span>

<span data-ttu-id="74210-294">Имя</span><span class="sxs-lookup"><span data-stu-id="74210-294">Name</span></span>

<span data-ttu-id="74210-295">100</span><span class="sxs-lookup"><span data-stu-id="74210-295">100</span></span>

[<span data-ttu-id="74210-296">распределенная файловая система</span><span class="sxs-lookup"><span data-stu-id="74210-296">Distributed File System</span></span>](/windows)

<span data-ttu-id="74210-297">101</span><span class="sxs-lookup"><span data-stu-id="74210-297">101</span></span>

<span data-ttu-id="74210-298">Пространство имен DFS</span><span class="sxs-lookup"><span data-stu-id="74210-298">DFS Namespace</span></span>

<span data-ttu-id="74210-299">102</span><span class="sxs-lookup"><span data-stu-id="74210-299">102</span></span>

<span data-ttu-id="74210-300">Репликация DFS</span><span class="sxs-lookup"><span data-stu-id="74210-300">DFS Replication</span></span>

<span data-ttu-id="74210-301">103</span><span class="sxs-lookup"><span data-stu-id="74210-301">103</span></span>

[<span data-ttu-id="74210-302">Служба репликации файлов</span><span class="sxs-lookup"><span data-stu-id="74210-302">File Replication Service</span></span>](/windows)

<span data-ttu-id="74210-303">104</span><span class="sxs-lookup"><span data-stu-id="74210-303">104</span></span>

[<span data-ttu-id="74210-304">Диспетчер ресурсов файлового сервера</span><span class="sxs-lookup"><span data-stu-id="74210-304">File Server Resource Manager (FSRM)</span></span>](/windows)

<span data-ttu-id="74210-305">105</span><span class="sxs-lookup"><span data-stu-id="74210-305">105</span></span>

[<span data-ttu-id="74210-306">Службы для сетевой файловой системы</span><span class="sxs-lookup"><span data-stu-id="74210-306">Services For Network File System</span></span>](/windows)

<span data-ttu-id="74210-307">106</span><span class="sxs-lookup"><span data-stu-id="74210-307">106</span></span>

[<span data-ttu-id="74210-308">Хранилище единственных копий</span><span class="sxs-lookup"><span data-stu-id="74210-308">Single Instance Storage</span></span>](/windows)

<span data-ttu-id="74210-309">107</span><span class="sxs-lookup"><span data-stu-id="74210-309">107</span></span>

[<span data-ttu-id="74210-310">Служба Windows Search</span><span class="sxs-lookup"><span data-stu-id="74210-310">Windows Search Service</span></span>](/windows)

<span data-ttu-id="74210-311">108</span><span class="sxs-lookup"><span data-stu-id="74210-311">108</span></span>

[<span data-ttu-id="74210-312">служба индексирования</span><span class="sxs-lookup"><span data-stu-id="74210-312">Indexing Service</span></span>](/windows)

<span data-ttu-id="74210-313">255</span><span class="sxs-lookup"><span data-stu-id="74210-313">255</span></span>

<span data-ttu-id="74210-314">Файловый сервер</span><span class="sxs-lookup"><span data-stu-id="74210-314">File Server</span></span>

<span data-ttu-id="74210-315">350</span><span class="sxs-lookup"><span data-stu-id="74210-315">350</span></span>

<span data-ttu-id="74210-316">Служба BranchCache для сетевых файлов</span><span class="sxs-lookup"><span data-stu-id="74210-316">BranchCache for Network Files</span></span>

<span data-ttu-id="74210-317">431</span><span class="sxs-lookup"><span data-stu-id="74210-317">431</span></span>

[<span data-ttu-id="74210-318">Сервер для NFS</span><span class="sxs-lookup"><span data-stu-id="74210-318">Server for NFS</span></span>](/windows)<br/>

<span data-ttu-id="74210-319">434</span><span class="sxs-lookup"><span data-stu-id="74210-319">434</span></span>

[<span data-ttu-id="74210-320">Служба агента VSS файлового сервера</span><span class="sxs-lookup"><span data-stu-id="74210-320">File Server VSS Agent Service</span></span>](/windows)<br/>

<span data-ttu-id="74210-321">435</span><span class="sxs-lookup"><span data-stu-id="74210-321">435</span></span>

[<span data-ttu-id="74210-322">Целевой сервер iSCSI</span><span class="sxs-lookup"><span data-stu-id="74210-322">iSCSI Target Server</span></span>](/windows)<br/>

<span data-ttu-id="74210-323">436</span><span class="sxs-lookup"><span data-stu-id="74210-323">436</span></span>

[<span data-ttu-id="74210-324">Дедупликация данных</span><span class="sxs-lookup"><span data-stu-id="74210-324">Data Deduplication</span></span>](/windows)<br/>

<span data-ttu-id="74210-325">437</span><span class="sxs-lookup"><span data-stu-id="74210-325">437</span></span>

[<span data-ttu-id="74210-326">Поставщик хранилища цели iSCSI (поставщики оборудования VDS и VSS)</span><span class="sxs-lookup"><span data-stu-id="74210-326">iSCSI Target Storage Provider (VDS and VSS hardware providers)</span></span>](/windows)

<span data-ttu-id="74210-327">486</span><span class="sxs-lookup"><span data-stu-id="74210-327">486</span></span>

[<span data-ttu-id="74210-328">Рабочие папки</span><span class="sxs-lookup"><span data-stu-id="74210-328">Work Folders</span></span>](/windows)

<span data-ttu-id="74210-329">Службы ролей AD DS (10)</span><span class="sxs-lookup"><span data-stu-id="74210-329">AD DS - Role Services (10)</span></span>

<span data-ttu-id="74210-330">Значение</span><span class="sxs-lookup"><span data-stu-id="74210-330">Value</span></span>

<span data-ttu-id="74210-331">Имя</span><span class="sxs-lookup"><span data-stu-id="74210-331">Name</span></span>

<span data-ttu-id="74210-332">110</span><span class="sxs-lookup"><span data-stu-id="74210-332">110</span></span>

[<span data-ttu-id="74210-333">Контроллер домена Active Directory</span><span class="sxs-lookup"><span data-stu-id="74210-333">Active Directory Domain Controller</span></span>](/windows)

<span data-ttu-id="74210-334">111</span><span class="sxs-lookup"><span data-stu-id="74210-334">111</span></span>

[<span data-ttu-id="74210-335">Управление удостоверениями для UNIX</span><span class="sxs-lookup"><span data-stu-id="74210-335">Identity Management For Unix</span></span>](/windows)

<span data-ttu-id="74210-336">112</span><span class="sxs-lookup"><span data-stu-id="74210-336">112</span></span>

[<span data-ttu-id="74210-337">Сервер для служб сведений о сети</span><span class="sxs-lookup"><span data-stu-id="74210-337">Server For Network Information Services</span></span>](/windows)

<span data-ttu-id="74210-338">113</span><span class="sxs-lookup"><span data-stu-id="74210-338">113</span></span>

[<span data-ttu-id="74210-339">Синхронизация паролей</span><span class="sxs-lookup"><span data-stu-id="74210-339">Password Synchronization</span></span>](/windows)

<span data-ttu-id="74210-340">294</span><span class="sxs-lookup"><span data-stu-id="74210-340">294</span></span>

[<span data-ttu-id="74210-341">Средства удаленного администрирования сервера</span><span class="sxs-lookup"><span data-stu-id="74210-341">Remote Server Administration Tools</span></span>](/windows)

<span data-ttu-id="74210-342">Службы ролей потоковой передачи мультимедиа (3)</span><span class="sxs-lookup"><span data-stu-id="74210-342">Streaming Media - Role Services (3)</span></span>

<span data-ttu-id="74210-343">Значение</span><span class="sxs-lookup"><span data-stu-id="74210-343">Value</span></span>

<span data-ttu-id="74210-344">Имя</span><span class="sxs-lookup"><span data-stu-id="74210-344">Name</span></span>

<span data-ttu-id="74210-345">120</span><span class="sxs-lookup"><span data-stu-id="74210-345">120</span></span>

[<span data-ttu-id="74210-346">Windows Media Server</span><span class="sxs-lookup"><span data-stu-id="74210-346">Windows Media Server</span></span>](/windows)

<span data-ttu-id="74210-347">121</span><span class="sxs-lookup"><span data-stu-id="74210-347">121</span></span>

[<span data-ttu-id="74210-348">Веб-администрирование</span><span class="sxs-lookup"><span data-stu-id="74210-348">Web-based Administration</span></span>](/windows)

<span data-ttu-id="74210-349">122</span><span class="sxs-lookup"><span data-stu-id="74210-349">122</span></span>

[<span data-ttu-id="74210-350">Агент ведения журнала</span><span class="sxs-lookup"><span data-stu-id="74210-350">Logging Agent</span></span>](/windows)

<span data-ttu-id="74210-351">ADFS — службы ролей (8)</span><span class="sxs-lookup"><span data-stu-id="74210-351">ADFS - Role Services (8)</span></span>

<span data-ttu-id="74210-352">Значение</span><span class="sxs-lookup"><span data-stu-id="74210-352">Value</span></span>

<span data-ttu-id="74210-353">Имя</span><span class="sxs-lookup"><span data-stu-id="74210-353">Name</span></span>

<span data-ttu-id="74210-354">125</span><span class="sxs-lookup"><span data-stu-id="74210-354">125</span></span>

[<span data-ttu-id="74210-355">Службы федерации Active Directory (AD FS)</span><span class="sxs-lookup"><span data-stu-id="74210-355">Active Directory Federation Services</span></span>](/windows)

<span data-ttu-id="74210-356">126</span><span class="sxs-lookup"><span data-stu-id="74210-356">126</span></span>

[<span data-ttu-id="74210-357">Политика служба федерации</span><span class="sxs-lookup"><span data-stu-id="74210-357">Federation Service Policy</span></span>](/windows)

<span data-ttu-id="74210-358">127</span><span class="sxs-lookup"><span data-stu-id="74210-358">127</span></span>

[<span data-ttu-id="74210-359">Веб-агенты служб федерации Active Directory</span><span class="sxs-lookup"><span data-stu-id="74210-359">AD FS Web Agents</span></span>](/windows)

<span data-ttu-id="74210-360">128</span><span class="sxs-lookup"><span data-stu-id="74210-360">128</span></span>

[<span data-ttu-id="74210-361">Агент, поддерживающий утверждения</span><span class="sxs-lookup"><span data-stu-id="74210-361">Claims-aware Agent</span></span>](/windows)

<span data-ttu-id="74210-362">129</span><span class="sxs-lookup"><span data-stu-id="74210-362">129</span></span>

[<span data-ttu-id="74210-363">Агент, использующий токены Windows</span><span class="sxs-lookup"><span data-stu-id="74210-363">Windows Token-based Agent</span></span>](/windows)

<span data-ttu-id="74210-364">Службы ролей службы удаленных рабочих столов (18)</span><span class="sxs-lookup"><span data-stu-id="74210-364">Remote Desktop Services - Role Services (18)</span></span>

<span data-ttu-id="74210-365">Значение</span><span class="sxs-lookup"><span data-stu-id="74210-365">Value</span></span>

<span data-ttu-id="74210-366">Имя</span><span class="sxs-lookup"><span data-stu-id="74210-366">Name</span></span>

<span data-ttu-id="74210-367">130</span><span class="sxs-lookup"><span data-stu-id="74210-367">130</span></span>

<span data-ttu-id="74210-368">Узел сеансов удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="74210-368">Remote Desktop Session Host</span></span><br/> [<span data-ttu-id="74210-369">изменение имени</span><span class="sxs-lookup"><span data-stu-id="74210-369">name change</span></span>](/windows)<br/>

<span data-ttu-id="74210-370">131</span><span class="sxs-lookup"><span data-stu-id="74210-370">131</span></span>

[<span data-ttu-id="74210-371">Лицензирование удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="74210-371">Remote Desktop Licensing</span></span>](/windows)<br/> [<span data-ttu-id="74210-372">изменение имени</span><span class="sxs-lookup"><span data-stu-id="74210-372">name change</span></span>](/windows)<br/>

<span data-ttu-id="74210-373">132</span><span class="sxs-lookup"><span data-stu-id="74210-373">132</span></span>

<span data-ttu-id="74210-374">Шлюз удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="74210-374">Remote Desktop Gateway</span></span><br/> [<span data-ttu-id="74210-375">изменение имени</span><span class="sxs-lookup"><span data-stu-id="74210-375">name change</span></span>](/windows)<br/>

<span data-ttu-id="74210-376">133</span><span class="sxs-lookup"><span data-stu-id="74210-376">133</span></span>

<span data-ttu-id="74210-377">Посредник подключений к удаленному рабочему столу</span><span class="sxs-lookup"><span data-stu-id="74210-377">Remote Desktop Connection Broker</span></span><br/> [<span data-ttu-id="74210-378">изменение имени</span><span class="sxs-lookup"><span data-stu-id="74210-378">name change</span></span>](/windows)<br/>

<span data-ttu-id="74210-379">134</span><span class="sxs-lookup"><span data-stu-id="74210-379">134</span></span>

<span data-ttu-id="74210-380">Веб-доступ к удаленным рабочим столам</span><span class="sxs-lookup"><span data-stu-id="74210-380">Remote Desktop Web Access</span></span><br/> [<span data-ttu-id="74210-381">изменение имени</span><span class="sxs-lookup"><span data-stu-id="74210-381">name change</span></span>](/windows)<br/>

<span data-ttu-id="74210-382">322</span><span class="sxs-lookup"><span data-stu-id="74210-382">322</span></span>

<span data-ttu-id="74210-383">Узел виртуализации удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="74210-383">Remote Desktop Virtualization Host</span></span><br/>

<span data-ttu-id="74210-384">Службы ролей Узел виртуализации удаленных рабочих столов (322)</span><span class="sxs-lookup"><span data-stu-id="74210-384">Remote Desktop Virtualization Host - Role Services (322)</span></span>

<span data-ttu-id="74210-385">Значение</span><span class="sxs-lookup"><span data-stu-id="74210-385">Value</span></span>

<span data-ttu-id="74210-386">Имя</span><span class="sxs-lookup"><span data-stu-id="74210-386">Name</span></span>

<span data-ttu-id="74210-387">325</span><span class="sxs-lookup"><span data-stu-id="74210-387">325</span></span>

[<span data-ttu-id="74210-388">Основные службы</span><span class="sxs-lookup"><span data-stu-id="74210-388">Core Services</span></span>](/windows)<br/>

<span data-ttu-id="74210-389">327</span><span class="sxs-lookup"><span data-stu-id="74210-389">327</span></span>

[<span data-ttu-id="74210-390">удаленный рабочий стол виртуальных графических элементов</span><span class="sxs-lookup"><span data-stu-id="74210-390">Remote Desktop Virtual Graphics</span></span>](/windows)<br/>

<span data-ttu-id="74210-391">Службы ролей службы печати и документов (7)</span><span class="sxs-lookup"><span data-stu-id="74210-391">Print and Document Services - Role Services (7)</span></span>

<span data-ttu-id="74210-392">Значение</span><span class="sxs-lookup"><span data-stu-id="74210-392">Value</span></span>

<span data-ttu-id="74210-393">Имя</span><span class="sxs-lookup"><span data-stu-id="74210-393">Name</span></span>

<span data-ttu-id="74210-394">135</span><span class="sxs-lookup"><span data-stu-id="74210-394">135</span></span>

<span data-ttu-id="74210-395">Сервер печати</span><span class="sxs-lookup"><span data-stu-id="74210-395">Print Server</span></span>

<span data-ttu-id="74210-396">136</span><span class="sxs-lookup"><span data-stu-id="74210-396">136</span></span>

<span data-ttu-id="74210-397">Печать через Интернет</span><span class="sxs-lookup"><span data-stu-id="74210-397">Internet Printing</span></span>

<span data-ttu-id="74210-398">137</span><span class="sxs-lookup"><span data-stu-id="74210-398">137</span></span>

<span data-ttu-id="74210-399">Служба печати LPD</span><span class="sxs-lookup"><span data-stu-id="74210-399">LPD Print Service</span></span>

<span data-ttu-id="74210-400">328</span><span class="sxs-lookup"><span data-stu-id="74210-400">328</span></span>

[<span data-ttu-id="74210-401">Сервер распределенного сканирования</span><span class="sxs-lookup"><span data-stu-id="74210-401">Distributed Scan Server</span></span>](/windows)<br/>

<span data-ttu-id="74210-402">Веб-сервер (IIS) — службы ролей (2)</span><span class="sxs-lookup"><span data-stu-id="74210-402">Web Server (IIS) - Role Services (2)</span></span>

<span data-ttu-id="74210-403">Значение</span><span class="sxs-lookup"><span data-stu-id="74210-403">Value</span></span>

<span data-ttu-id="74210-404">Имя</span><span class="sxs-lookup"><span data-stu-id="74210-404">Name</span></span>

<span data-ttu-id="74210-405">140</span><span class="sxs-lookup"><span data-stu-id="74210-405">140</span></span>

<span data-ttu-id="74210-406">Веб-сервер</span><span class="sxs-lookup"><span data-stu-id="74210-406">Web Server</span></span>

<span data-ttu-id="74210-407">141</span><span class="sxs-lookup"><span data-stu-id="74210-407">141</span></span>

<span data-ttu-id="74210-408">Общие функции HTTP</span><span class="sxs-lookup"><span data-stu-id="74210-408">Common HTTP Features</span></span>

<span data-ttu-id="74210-409">142</span><span class="sxs-lookup"><span data-stu-id="74210-409">142</span></span>

<span data-ttu-id="74210-410">Статическое содержимое</span><span class="sxs-lookup"><span data-stu-id="74210-410">Static Content</span></span>

<span data-ttu-id="74210-411">143</span><span class="sxs-lookup"><span data-stu-id="74210-411">143</span></span>

<span data-ttu-id="74210-412">Документ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="74210-412">Default Document</span></span>

<span data-ttu-id="74210-413">144</span><span class="sxs-lookup"><span data-stu-id="74210-413">144</span></span>

<span data-ttu-id="74210-414">Обзор каталога</span><span class="sxs-lookup"><span data-stu-id="74210-414">Directory Browse</span></span>

<span data-ttu-id="74210-415">145</span><span class="sxs-lookup"><span data-stu-id="74210-415">145</span></span>

<span data-ttu-id="74210-416">Ошибки HTTP</span><span class="sxs-lookup"><span data-stu-id="74210-416">HTTP Errors</span></span>

<span data-ttu-id="74210-417">146</span><span class="sxs-lookup"><span data-stu-id="74210-417">146</span></span>

<span data-ttu-id="74210-418">Перенаправление HTTP</span><span class="sxs-lookup"><span data-stu-id="74210-418">HTTP Redirection</span></span>

<span data-ttu-id="74210-419">147</span><span class="sxs-lookup"><span data-stu-id="74210-419">147</span></span>

<span data-ttu-id="74210-420">Разработка приложений</span><span class="sxs-lookup"><span data-stu-id="74210-420">Application Development</span></span>

<span data-ttu-id="74210-421">148</span><span class="sxs-lookup"><span data-stu-id="74210-421">148</span></span>

<span data-ttu-id="74210-422">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="74210-422">ASP.NET</span></span>

<span data-ttu-id="74210-423">149</span><span class="sxs-lookup"><span data-stu-id="74210-423">149</span></span>

<span data-ttu-id="74210-424">Расширяемость платформы .NET</span><span class="sxs-lookup"><span data-stu-id="74210-424">.NET Extensibility</span></span>

<span data-ttu-id="74210-425">150</span><span class="sxs-lookup"><span data-stu-id="74210-425">150</span></span>

<span data-ttu-id="74210-426">ASP</span><span class="sxs-lookup"><span data-stu-id="74210-426">ASP</span></span>

<span data-ttu-id="74210-427">151</span><span class="sxs-lookup"><span data-stu-id="74210-427">151</span></span>

<span data-ttu-id="74210-428">CGI</span><span class="sxs-lookup"><span data-stu-id="74210-428">CGI</span></span>

<span data-ttu-id="74210-429">152</span><span class="sxs-lookup"><span data-stu-id="74210-429">152</span></span>

<span data-ttu-id="74210-430">Расширения ISAPI</span><span class="sxs-lookup"><span data-stu-id="74210-430">ISAPI Extensions</span></span>

<span data-ttu-id="74210-431">153</span><span class="sxs-lookup"><span data-stu-id="74210-431">153</span></span>

<span data-ttu-id="74210-432">Фильтры ISAPI</span><span class="sxs-lookup"><span data-stu-id="74210-432">ISAPI Filters</span></span>

<span data-ttu-id="74210-433">154</span><span class="sxs-lookup"><span data-stu-id="74210-433">154</span></span>

<span data-ttu-id="74210-434">Включения на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="74210-434">Server Side Includes</span></span>

<span data-ttu-id="74210-435">155</span><span class="sxs-lookup"><span data-stu-id="74210-435">155</span></span>

<span data-ttu-id="74210-436">Работоспособность и диагностика</span><span class="sxs-lookup"><span data-stu-id="74210-436">Health And Diagnostics</span></span>

<span data-ttu-id="74210-437">156</span><span class="sxs-lookup"><span data-stu-id="74210-437">156</span></span>

<span data-ttu-id="74210-438">Ведение журнала HTTP</span><span class="sxs-lookup"><span data-stu-id="74210-438">HTTP Logging</span></span>

<span data-ttu-id="74210-439">157</span><span class="sxs-lookup"><span data-stu-id="74210-439">157</span></span>

<span data-ttu-id="74210-440">Средства ведения журнала</span><span class="sxs-lookup"><span data-stu-id="74210-440">Logging Tools</span></span>

<span data-ttu-id="74210-441">158</span><span class="sxs-lookup"><span data-stu-id="74210-441">158</span></span>

<span data-ttu-id="74210-442">Монитор запросов</span><span class="sxs-lookup"><span data-stu-id="74210-442">Request Monitor</span></span>

<span data-ttu-id="74210-443">159</span><span class="sxs-lookup"><span data-stu-id="74210-443">159</span></span>

<span data-ttu-id="74210-444">Трассировка</span><span class="sxs-lookup"><span data-stu-id="74210-444">Tracing</span></span>

<span data-ttu-id="74210-445">160</span><span class="sxs-lookup"><span data-stu-id="74210-445">160</span></span>

<span data-ttu-id="74210-446">Настраиваемое ведение журнала</span><span class="sxs-lookup"><span data-stu-id="74210-446">Custom Logging</span></span>

<span data-ttu-id="74210-447">161</span><span class="sxs-lookup"><span data-stu-id="74210-447">161</span></span>

<span data-ttu-id="74210-448">Ведение журнала ODBC</span><span class="sxs-lookup"><span data-stu-id="74210-448">ODBC Logging</span></span>

<span data-ttu-id="74210-449">162</span><span class="sxs-lookup"><span data-stu-id="74210-449">162</span></span>

<span data-ttu-id="74210-450">Безопасность</span><span class="sxs-lookup"><span data-stu-id="74210-450">Security</span></span>

<span data-ttu-id="74210-451">163</span><span class="sxs-lookup"><span data-stu-id="74210-451">163</span></span>

<span data-ttu-id="74210-452">Обычная проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="74210-452">Basic Authentication</span></span>

<span data-ttu-id="74210-453">164</span><span class="sxs-lookup"><span data-stu-id="74210-453">164</span></span>

<span data-ttu-id="74210-454">Проверка подлинности Windows</span><span class="sxs-lookup"><span data-stu-id="74210-454">Windows Authentication</span></span>

<span data-ttu-id="74210-455">165</span><span class="sxs-lookup"><span data-stu-id="74210-455">165</span></span>

<span data-ttu-id="74210-456">Дайджест-проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="74210-456">Digest Authentication</span></span>

<span data-ttu-id="74210-457">166</span><span class="sxs-lookup"><span data-stu-id="74210-457">166</span></span>

<span data-ttu-id="74210-458">Проверка подлинности с сопоставлением сертификата клиента</span><span class="sxs-lookup"><span data-stu-id="74210-458">Client Certificate Mapping Authentication</span></span>

<span data-ttu-id="74210-459">167</span><span class="sxs-lookup"><span data-stu-id="74210-459">167</span></span>

<span data-ttu-id="74210-460">Аутентификация IIS с сопоставлением сертификата клиента</span><span class="sxs-lookup"><span data-stu-id="74210-460">IIS Client Certificate Mapping Authentication</span></span>

<span data-ttu-id="74210-461">168</span><span class="sxs-lookup"><span data-stu-id="74210-461">168</span></span>

<span data-ttu-id="74210-462">Авторизация URL-адресов</span><span class="sxs-lookup"><span data-stu-id="74210-462">URL Authorization</span></span>

<span data-ttu-id="74210-463">169</span><span class="sxs-lookup"><span data-stu-id="74210-463">169</span></span>

<span data-ttu-id="74210-464">Фильтрация запросов</span><span class="sxs-lookup"><span data-stu-id="74210-464">Request Filtering</span></span>

<span data-ttu-id="74210-465">170</span><span class="sxs-lookup"><span data-stu-id="74210-465">170</span></span>

<span data-ttu-id="74210-466">Ограничения IP-адресов и доменов</span><span class="sxs-lookup"><span data-stu-id="74210-466">IP And Domain Restrictions</span></span>

<span data-ttu-id="74210-467">171</span><span class="sxs-lookup"><span data-stu-id="74210-467">171</span></span>

<span data-ttu-id="74210-468">Производительность</span><span class="sxs-lookup"><span data-stu-id="74210-468">Performance</span></span>

<span data-ttu-id="74210-469">172</span><span class="sxs-lookup"><span data-stu-id="74210-469">172</span></span>

<span data-ttu-id="74210-470">Сжатие статического содержимого</span><span class="sxs-lookup"><span data-stu-id="74210-470">Static Content Compression</span></span>

<span data-ttu-id="74210-471">173</span><span class="sxs-lookup"><span data-stu-id="74210-471">173</span></span>

<span data-ttu-id="74210-472">Функция сжатия динамического содержимого</span><span class="sxs-lookup"><span data-stu-id="74210-472">Dynamic Content Compression</span></span>

<span data-ttu-id="74210-473">174</span><span class="sxs-lookup"><span data-stu-id="74210-473">174</span></span>

<span data-ttu-id="74210-474">Средства управления</span><span class="sxs-lookup"><span data-stu-id="74210-474">Management Tools</span></span>

<span data-ttu-id="74210-475">175</span><span class="sxs-lookup"><span data-stu-id="74210-475">175</span></span>

<span data-ttu-id="74210-476">Консоль управления (IIS)</span><span class="sxs-lookup"><span data-stu-id="74210-476">IIS Management Console</span></span>

<span data-ttu-id="74210-477">176</span><span class="sxs-lookup"><span data-stu-id="74210-477">176</span></span>

<span data-ttu-id="74210-478">Сценарии и средства управления IIS</span><span class="sxs-lookup"><span data-stu-id="74210-478">IIS Management Scripts And Tools</span></span>

<span data-ttu-id="74210-479">177</span><span class="sxs-lookup"><span data-stu-id="74210-479">177</span></span>

<span data-ttu-id="74210-480">Служба Management Service</span><span class="sxs-lookup"><span data-stu-id="74210-480">Management Service</span></span>

<span data-ttu-id="74210-481">178</span><span class="sxs-lookup"><span data-stu-id="74210-481">178</span></span>

<span data-ttu-id="74210-482">Совместимость управления IIS 6</span><span class="sxs-lookup"><span data-stu-id="74210-482">IIS 6 Management Compatibility</span></span>

<span data-ttu-id="74210-483">179</span><span class="sxs-lookup"><span data-stu-id="74210-483">179</span></span>

<span data-ttu-id="74210-484">Совместимость метабазы IIS 6</span><span class="sxs-lookup"><span data-stu-id="74210-484">IIS 6 Metabase Compatibility</span></span>

<span data-ttu-id="74210-485">180</span><span class="sxs-lookup"><span data-stu-id="74210-485">180</span></span>

<span data-ttu-id="74210-486">Совместимость с WMI IIS 6</span><span class="sxs-lookup"><span data-stu-id="74210-486">IIS 6 WMI Compatibility</span></span>

<span data-ttu-id="74210-487">181</span><span class="sxs-lookup"><span data-stu-id="74210-487">181</span></span>

<span data-ttu-id="74210-488">Инструменты для работы со сценариев IIS 6</span><span class="sxs-lookup"><span data-stu-id="74210-488">IIS 6 Scripting Tools</span></span>

<span data-ttu-id="74210-489">182</span><span class="sxs-lookup"><span data-stu-id="74210-489">182</span></span>

<span data-ttu-id="74210-490">Консоль управления IIS 6</span><span class="sxs-lookup"><span data-stu-id="74210-490">IIS 6 Management Console</span></span>

<span data-ttu-id="74210-491">183</span><span class="sxs-lookup"><span data-stu-id="74210-491">183</span></span>

<span data-ttu-id="74210-492">Служба FTP-публикаций</span><span class="sxs-lookup"><span data-stu-id="74210-492">FTP Publishing Service</span></span><br/>

<span data-ttu-id="74210-493">184</span><span class="sxs-lookup"><span data-stu-id="74210-493">184</span></span>

<span data-ttu-id="74210-494">FTP-сервер</span><span class="sxs-lookup"><span data-stu-id="74210-494">FTP Server</span></span>

<span data-ttu-id="74210-495">185</span><span class="sxs-lookup"><span data-stu-id="74210-495">185</span></span>

<span data-ttu-id="74210-496">Консоль управления FTP</span><span class="sxs-lookup"><span data-stu-id="74210-496">FTP Management Console</span></span><br/>

<span data-ttu-id="74210-497">314</span><span class="sxs-lookup"><span data-stu-id="74210-497">314</span></span>

<span data-ttu-id="74210-498">Публикация WebDAV</span><span class="sxs-lookup"><span data-stu-id="74210-498">WebDAV Publishing</span></span>

<span data-ttu-id="74210-499">316</span><span class="sxs-lookup"><span data-stu-id="74210-499">316</span></span>

<span data-ttu-id="74210-500">Служба FTP</span><span class="sxs-lookup"><span data-stu-id="74210-500">FTP Service</span></span><br/>

<span data-ttu-id="74210-501">317</span><span class="sxs-lookup"><span data-stu-id="74210-501">317</span></span>

<span data-ttu-id="74210-502">Расширяемость FTP</span><span class="sxs-lookup"><span data-stu-id="74210-502">FTP Extensibility</span></span><br/>

<span data-ttu-id="74210-503">336</span><span class="sxs-lookup"><span data-stu-id="74210-503">336</span></span>

<span data-ttu-id="74210-504">Внедряемое веб-ядро служб IIS</span><span class="sxs-lookup"><span data-stu-id="74210-504">IIS Hostable Web Core</span></span><br/>

<span data-ttu-id="74210-505">413</span><span class="sxs-lookup"><span data-stu-id="74210-505">413</span></span>

[<span data-ttu-id="74210-506">ASP.NET 4,5</span><span class="sxs-lookup"><span data-stu-id="74210-506">ASP.NET 4.5</span></span>](/windows)

<span data-ttu-id="74210-507">414</span><span class="sxs-lookup"><span data-stu-id="74210-507">414</span></span>

[<span data-ttu-id="74210-508">Расширяемость .NET 4.5</span><span class="sxs-lookup"><span data-stu-id="74210-508">.NET Extensibility 4.5</span></span>](/windows)

<span data-ttu-id="74210-509">445</span><span class="sxs-lookup"><span data-stu-id="74210-509">445</span></span>

[<span data-ttu-id="74210-510">аппиализатион</span><span class="sxs-lookup"><span data-stu-id="74210-510">appialization</span></span>](/windows)

<span data-ttu-id="74210-511">446</span><span class="sxs-lookup"><span data-stu-id="74210-511">446</span></span>

[<span data-ttu-id="74210-512">централизованная поддержка SSL-сертификатов</span><span class="sxs-lookup"><span data-stu-id="74210-512">Centralized SSL Certificate Support</span></span>](/windows)

<span data-ttu-id="74210-513">447</span><span class="sxs-lookup"><span data-stu-id="74210-513">447</span></span>

[<span data-ttu-id="74210-514">Протокол WebSocket</span><span class="sxs-lookup"><span data-stu-id="74210-514">WebSocket Protocol</span></span>](/windows)

<span data-ttu-id="74210-515">Очередь сообщений — функции (49)</span><span class="sxs-lookup"><span data-stu-id="74210-515">Message Queuing - Features (49)</span></span>

<span data-ttu-id="74210-516">Значение</span><span class="sxs-lookup"><span data-stu-id="74210-516">Value</span></span>

<span data-ttu-id="74210-517">Имя</span><span class="sxs-lookup"><span data-stu-id="74210-517">Name</span></span>

<span data-ttu-id="74210-518">190</span><span class="sxs-lookup"><span data-stu-id="74210-518">190</span></span>

<span data-ttu-id="74210-519">Службы очереди сообщений</span><span class="sxs-lookup"><span data-stu-id="74210-519">Message Queuing Services</span></span>

<span data-ttu-id="74210-520">191</span><span class="sxs-lookup"><span data-stu-id="74210-520">191</span></span>

<span data-ttu-id="74210-521">Сервер службы очередей сообщений</span><span class="sxs-lookup"><span data-stu-id="74210-521">Message Queuing Server</span></span>

<span data-ttu-id="74210-522">192</span><span class="sxs-lookup"><span data-stu-id="74210-522">192</span></span>

<span data-ttu-id="74210-523">Интеграция служб каталогов</span><span class="sxs-lookup"><span data-stu-id="74210-523">Directory Service Integration</span></span>

<span data-ttu-id="74210-524">193</span><span class="sxs-lookup"><span data-stu-id="74210-524">193</span></span>

<span data-ttu-id="74210-525">Триггеры очереди сообщений</span><span class="sxs-lookup"><span data-stu-id="74210-525">Message Queuing Triggers</span></span>

<span data-ttu-id="74210-526">194</span><span class="sxs-lookup"><span data-stu-id="74210-526">194</span></span>

<span data-ttu-id="74210-527">Поддержка HTTP</span><span class="sxs-lookup"><span data-stu-id="74210-527">HTTP Support</span></span>

<span data-ttu-id="74210-528">195</span><span class="sxs-lookup"><span data-stu-id="74210-528">195</span></span>

<span data-ttu-id="74210-529">Служба маршрутизации</span><span class="sxs-lookup"><span data-stu-id="74210-529">Routing Service</span></span>

<span data-ttu-id="74210-530">196</span><span class="sxs-lookup"><span data-stu-id="74210-530">196</span></span>

[<span data-ttu-id="74210-531">Поддержка клиентов Windows 2000</span><span class="sxs-lookup"><span data-stu-id="74210-531">Windows 2000 Client Support</span></span>](/windows)<br/>

<span data-ttu-id="74210-532">197</span><span class="sxs-lookup"><span data-stu-id="74210-532">197</span></span>

<span data-ttu-id="74210-533">DCOM-прокси очереди сообщений</span><span class="sxs-lookup"><span data-stu-id="74210-533">Message Queuing DCOM Proxy</span></span>

<span data-ttu-id="74210-534">228</span><span class="sxs-lookup"><span data-stu-id="74210-534">228</span></span>

<span data-ttu-id="74210-535">Поддержка многоадресной рассылки</span><span class="sxs-lookup"><span data-stu-id="74210-535">Multicasting Support</span></span>

<span data-ttu-id="74210-536">Службы сертификации Active Directory — службы ролей (16)</span><span class="sxs-lookup"><span data-stu-id="74210-536">Active Directory Certificate Services - Role Services (16)</span></span>

<span data-ttu-id="74210-537">Значение</span><span class="sxs-lookup"><span data-stu-id="74210-537">Value</span></span>

<span data-ttu-id="74210-538">Имя</span><span class="sxs-lookup"><span data-stu-id="74210-538">Name</span></span>

<span data-ttu-id="74210-539">200</span><span class="sxs-lookup"><span data-stu-id="74210-539">200</span></span>

<span data-ttu-id="74210-540">Центр сертификации</span><span class="sxs-lookup"><span data-stu-id="74210-540">Certification Authority</span></span>

<span data-ttu-id="74210-541">201</span><span class="sxs-lookup"><span data-stu-id="74210-541">201</span></span>

<span data-ttu-id="74210-542">Служба регистрации в центре сертификации через Интернет</span><span class="sxs-lookup"><span data-stu-id="74210-542">Certification Authority Web Enrollment</span></span>

<span data-ttu-id="74210-543">202</span><span class="sxs-lookup"><span data-stu-id="74210-543">202</span></span>

<span data-ttu-id="74210-544">Сетевой ответчик</span><span class="sxs-lookup"><span data-stu-id="74210-544">Online Responder</span></span>

<span data-ttu-id="74210-545">204</span><span class="sxs-lookup"><span data-stu-id="74210-545">204</span></span>

<span data-ttu-id="74210-546">Служба подачи заявок на сетевые устройства</span><span class="sxs-lookup"><span data-stu-id="74210-546">Network Device Enrollment Service</span></span>

<span data-ttu-id="74210-547">318</span><span class="sxs-lookup"><span data-stu-id="74210-547">318</span></span>

[<span data-ttu-id="74210-548">Веб-служба регистрации сертификатов</span><span class="sxs-lookup"><span data-stu-id="74210-548">Certificate Enrollment Web Service</span></span>](/windows)<br/>

<span data-ttu-id="74210-549">319</span><span class="sxs-lookup"><span data-stu-id="74210-549">319</span></span>

[<span data-ttu-id="74210-550">веб-служба политик регистрации сертификатов</span><span class="sxs-lookup"><span data-stu-id="74210-550">Certificate Enrollment Policy Web Service</span></span>](/windows)<br/>

<span data-ttu-id="74210-551">Службы политики сети и доступа — службы ролей (14)</span><span class="sxs-lookup"><span data-stu-id="74210-551">Network Policy and Access Services - Role Services (14)</span></span>

<span data-ttu-id="74210-552">Значение</span><span class="sxs-lookup"><span data-stu-id="74210-552">Value</span></span>

<span data-ttu-id="74210-553">Имя</span><span class="sxs-lookup"><span data-stu-id="74210-553">Name</span></span>

<span data-ttu-id="74210-554">205</span><span class="sxs-lookup"><span data-stu-id="74210-554">205</span></span>

[<span data-ttu-id="74210-555">Сервер политики сети</span><span class="sxs-lookup"><span data-stu-id="74210-555">Network Policy Server</span></span>](/windows)

<span data-ttu-id="74210-556">206</span><span class="sxs-lookup"><span data-stu-id="74210-556">206</span></span>

[<span data-ttu-id="74210-557">VPN</span><span class="sxs-lookup"><span data-stu-id="74210-557">VPN</span></span>](#vpn)

<span data-ttu-id="74210-558">207</span><span class="sxs-lookup"><span data-stu-id="74210-558">207</span></span>

[<span data-ttu-id="74210-559">Службы удаленного доступа</span><span class="sxs-lookup"><span data-stu-id="74210-559">Remote Access Services</span></span>](/windows)

<span data-ttu-id="74210-560">208</span><span class="sxs-lookup"><span data-stu-id="74210-560">208</span></span>

[<span data-ttu-id="74210-561">Маршрутизация</span><span class="sxs-lookup"><span data-stu-id="74210-561">Routing</span></span>](#routing)

<span data-ttu-id="74210-562">210</span><span class="sxs-lookup"><span data-stu-id="74210-562">210</span></span>

[<span data-ttu-id="74210-563">Центр регистрации работоспособности</span><span class="sxs-lookup"><span data-stu-id="74210-563">Health Registration Authority</span></span>](/windows)

<span data-ttu-id="74210-564">250</span><span class="sxs-lookup"><span data-stu-id="74210-564">250</span></span>

[<span data-ttu-id="74210-565">Протокол авторизации учетных данных узла</span><span class="sxs-lookup"><span data-stu-id="74210-565">Host Credential Authorization Protocol</span></span>](/windows)

<span data-ttu-id="74210-566">Службы UDDI — службы ролей (11)</span><span class="sxs-lookup"><span data-stu-id="74210-566">UDDI Services - Role Services (11)</span></span>

<span data-ttu-id="74210-567">Значение</span><span class="sxs-lookup"><span data-stu-id="74210-567">Value</span></span>

<span data-ttu-id="74210-568">Имя</span><span class="sxs-lookup"><span data-stu-id="74210-568">Name</span></span>

<span data-ttu-id="74210-569">215</span><span class="sxs-lookup"><span data-stu-id="74210-569">215</span></span>

[<span data-ttu-id="74210-570">Веб-приложение служб UDDI</span><span class="sxs-lookup"><span data-stu-id="74210-570">UDDI Services Web Application</span></span>](/windows)<br/>

<span data-ttu-id="74210-571">216</span><span class="sxs-lookup"><span data-stu-id="74210-571">216</span></span>

[<span data-ttu-id="74210-572">База данных служб UDDI</span><span class="sxs-lookup"><span data-stu-id="74210-572">UDDI Services Database</span></span>](/windows)<br/>

<span data-ttu-id="74210-573">Служба активации процессов Windows — службы ролей (41)</span><span class="sxs-lookup"><span data-stu-id="74210-573">Windows Process Activation Service - Role Services (41)</span></span>

<span data-ttu-id="74210-574">Значение</span><span class="sxs-lookup"><span data-stu-id="74210-574">Value</span></span>

<span data-ttu-id="74210-575">Имя</span><span class="sxs-lookup"><span data-stu-id="74210-575">Name</span></span>

<span data-ttu-id="74210-576">217</span><span class="sxs-lookup"><span data-stu-id="74210-576">217</span></span>

<span data-ttu-id="74210-577">API настройки</span><span class="sxs-lookup"><span data-stu-id="74210-577">Configuration API</span></span>

<span data-ttu-id="74210-578">218</span><span class="sxs-lookup"><span data-stu-id="74210-578">218</span></span>

<span data-ttu-id="74210-579">Среда .NET</span><span class="sxs-lookup"><span data-stu-id="74210-579">.NET Environment</span></span>

<span data-ttu-id="74210-580">219</span><span class="sxs-lookup"><span data-stu-id="74210-580">219</span></span>

<span data-ttu-id="74210-581">Модель процесса</span><span class="sxs-lookup"><span data-stu-id="74210-581">Process Model</span></span>

<span data-ttu-id="74210-582">Платформа .NET Framework 3.5.1 — функции (36)</span><span class="sxs-lookup"><span data-stu-id="74210-582">.NET Framework 3.5.1 - Features (36)</span></span>

<span data-ttu-id="74210-583">Значение</span><span class="sxs-lookup"><span data-stu-id="74210-583">Value</span></span>

<span data-ttu-id="74210-584">Имя</span><span class="sxs-lookup"><span data-stu-id="74210-584">Name</span></span>

<span data-ttu-id="74210-585">220</span><span class="sxs-lookup"><span data-stu-id="74210-585">220</span></span>

<span data-ttu-id="74210-586">.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="74210-586">.NET Framework 3.5.1</span></span><br/> [<span data-ttu-id="74210-587">изменение имени</span><span class="sxs-lookup"><span data-stu-id="74210-587">name change</span></span>](/windows)<br/>

<span data-ttu-id="74210-588">221</span><span class="sxs-lookup"><span data-stu-id="74210-588">221</span></span>

<span data-ttu-id="74210-589">Активация WCF</span><span class="sxs-lookup"><span data-stu-id="74210-589">WCF Activation</span></span>

<span data-ttu-id="74210-590">222</span><span class="sxs-lookup"><span data-stu-id="74210-590">222</span></span>

<span data-ttu-id="74210-591">Активация по протоколам HTTP</span><span class="sxs-lookup"><span data-stu-id="74210-591">HTTP Activation</span></span>

<span data-ttu-id="74210-592">223</span><span class="sxs-lookup"><span data-stu-id="74210-592">223</span></span>

<span data-ttu-id="74210-593">Не-HTTP активация</span><span class="sxs-lookup"><span data-stu-id="74210-593">Non-HTTP Activation</span></span>

<span data-ttu-id="74210-594">227</span><span class="sxs-lookup"><span data-stu-id="74210-594">227</span></span>

<span data-ttu-id="74210-595">Средство просмотра XPS</span><span class="sxs-lookup"><span data-stu-id="74210-595">XPS Viewer</span></span><br/>

<span data-ttu-id="74210-596">Службы SNMP — функции (59)</span><span class="sxs-lookup"><span data-stu-id="74210-596">SNMP Services - Features (59)</span></span>

<span data-ttu-id="74210-597">Значение</span><span class="sxs-lookup"><span data-stu-id="74210-597">Value</span></span>

<span data-ttu-id="74210-598">Имя</span><span class="sxs-lookup"><span data-stu-id="74210-598">Name</span></span>

<span data-ttu-id="74210-599">224</span><span class="sxs-lookup"><span data-stu-id="74210-599">224</span></span>

[<span data-ttu-id="74210-600">служба SNMP;</span><span class="sxs-lookup"><span data-stu-id="74210-600">SNMP Service</span></span>](/windows)

<span data-ttu-id="74210-601">225</span><span class="sxs-lookup"><span data-stu-id="74210-601">225</span></span>

[<span data-ttu-id="74210-602">Поставщик WMI SNMP</span><span class="sxs-lookup"><span data-stu-id="74210-602">SNMP WMI Provider</span></span>](/windows)

<span data-ttu-id="74210-603">Службы ролей Службы приложений</span><span class="sxs-lookup"><span data-stu-id="74210-603">Application Services - Role Services</span></span>

<span data-ttu-id="74210-604">Значение</span><span class="sxs-lookup"><span data-stu-id="74210-604">Value</span></span>

<span data-ttu-id="74210-605">Имя</span><span class="sxs-lookup"><span data-stu-id="74210-605">Name</span></span>

<span data-ttu-id="74210-606">230</span><span class="sxs-lookup"><span data-stu-id="74210-606">230</span></span>

[<span data-ttu-id="74210-607">.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="74210-607">.NET Framework 3.5.1</span></span>](/windows)<br/> [<span data-ttu-id="74210-608">изменение имени</span><span class="sxs-lookup"><span data-stu-id="74210-608">name change</span></span>](/windows)<br/>

<span data-ttu-id="74210-609">231</span><span class="sxs-lookup"><span data-stu-id="74210-609">231</span></span>

[<span data-ttu-id="74210-610">Поддержка веб-сервера (IIS)</span><span class="sxs-lookup"><span data-stu-id="74210-610">Web Server (IIS) Support</span></span>](/windows)

<span data-ttu-id="74210-611">232</span><span class="sxs-lookup"><span data-stu-id="74210-611">232</span></span>

[<span data-ttu-id="74210-612">Доступ к сети COM+</span><span class="sxs-lookup"><span data-stu-id="74210-612">COM+ Network Access</span></span>](/windows)

<span data-ttu-id="74210-613">233</span><span class="sxs-lookup"><span data-stu-id="74210-613">233</span></span>

[<span data-ttu-id="74210-614">Совместное использование TCP-портов</span><span class="sxs-lookup"><span data-stu-id="74210-614">TCP Port Sharing</span></span>](/windows)

<span data-ttu-id="74210-615">234</span><span class="sxs-lookup"><span data-stu-id="74210-615">234</span></span>

[<span data-ttu-id="74210-616">Поддержка службы активации процессов Windows</span><span class="sxs-lookup"><span data-stu-id="74210-616">Windows Process Activation Service Support</span></span>](/windows)

<span data-ttu-id="74210-617">235</span><span class="sxs-lookup"><span data-stu-id="74210-617">235</span></span>

[<span data-ttu-id="74210-618">Активация по HTTP</span><span class="sxs-lookup"><span data-stu-id="74210-618">HTTP Activation</span></span>](/windows)

<span data-ttu-id="74210-619">236</span><span class="sxs-lookup"><span data-stu-id="74210-619">236</span></span>

[<span data-ttu-id="74210-620">Активация службы очередей сообщений</span><span class="sxs-lookup"><span data-stu-id="74210-620">Message Queuing Activation</span></span>](/windows)

<span data-ttu-id="74210-621">237</span><span class="sxs-lookup"><span data-stu-id="74210-621">237</span></span>

[<span data-ttu-id="74210-622">Активация TCP</span><span class="sxs-lookup"><span data-stu-id="74210-622">TCP Activation</span></span>](/windows)

<span data-ttu-id="74210-623">238</span><span class="sxs-lookup"><span data-stu-id="74210-623">238</span></span>

[<span data-ttu-id="74210-624">Активация по именованным каналам</span><span class="sxs-lookup"><span data-stu-id="74210-624">Named Pipes Activation</span></span>](/windows)

<span data-ttu-id="74210-625">239</span><span class="sxs-lookup"><span data-stu-id="74210-625">239</span></span>

[<span data-ttu-id="74210-626">Распределенные транзакции</span><span class="sxs-lookup"><span data-stu-id="74210-626">Distributed Transactions</span></span>](/windows)

<span data-ttu-id="74210-627">240</span><span class="sxs-lookup"><span data-stu-id="74210-627">240</span></span>

[<span data-ttu-id="74210-628">Входящие удаленные транзакции</span><span class="sxs-lookup"><span data-stu-id="74210-628">Incoming Remote Transactions</span></span>](/windows)

<span data-ttu-id="74210-629">241</span><span class="sxs-lookup"><span data-stu-id="74210-629">241</span></span>

[<span data-ttu-id="74210-630">Исходящие удаленные транзакции</span><span class="sxs-lookup"><span data-stu-id="74210-630">Outgoing Remote Transactions</span></span>](/windows)

<span data-ttu-id="74210-631">242</span><span class="sxs-lookup"><span data-stu-id="74210-631">242</span></span>

[<span data-ttu-id="74210-632">WS-автоматические транзакции</span><span class="sxs-lookup"><span data-stu-id="74210-632">WS-Automatic Transactions</span></span>](/windows)

<span data-ttu-id="74210-633">353</span><span class="sxs-lookup"><span data-stu-id="74210-633">353</span></span>

[<span data-ttu-id="74210-634">Расширения сервера приложений для .NET 4,0</span><span class="sxs-lookup"><span data-stu-id="74210-634">Application Server Extensions for .NET 4.0</span></span>](/windows)<br/>

<span data-ttu-id="74210-635">Службы развертывания Windows — роль (19)</span><span class="sxs-lookup"><span data-stu-id="74210-635">Windows Deployment Services - Role (19)</span></span>

<span data-ttu-id="74210-636">Значение</span><span class="sxs-lookup"><span data-stu-id="74210-636">Value</span></span>

<span data-ttu-id="74210-637">Имя</span><span class="sxs-lookup"><span data-stu-id="74210-637">Name</span></span>

<span data-ttu-id="74210-638">251</span><span class="sxs-lookup"><span data-stu-id="74210-638">251</span></span>

<span data-ttu-id="74210-639">Сервер развертывания</span><span class="sxs-lookup"><span data-stu-id="74210-639">Deployment Server</span></span>

<span data-ttu-id="74210-640">252</span><span class="sxs-lookup"><span data-stu-id="74210-640">252</span></span>

<span data-ttu-id="74210-641">Транспортный сервер</span><span class="sxs-lookup"><span data-stu-id="74210-641">Transport Server</span></span>

<span data-ttu-id="74210-642">Службы ролей службы Active Directory Rights Management (17)</span><span class="sxs-lookup"><span data-stu-id="74210-642">Active Directory Rights Management Services - Role Services (17)</span></span>

<span data-ttu-id="74210-643">Значение</span><span class="sxs-lookup"><span data-stu-id="74210-643">Value</span></span>

<span data-ttu-id="74210-644">Имя</span><span class="sxs-lookup"><span data-stu-id="74210-644">Name</span></span>

<span data-ttu-id="74210-645">253</span><span class="sxs-lookup"><span data-stu-id="74210-645">253</span></span>

<span data-ttu-id="74210-646">Сервер управления правами Active Directory</span><span class="sxs-lookup"><span data-stu-id="74210-646">Active Directory Rights Management Server</span></span>

<span data-ttu-id="74210-647">254</span><span class="sxs-lookup"><span data-stu-id="74210-647">254</span></span>

<span data-ttu-id="74210-648">Поддержка федерации удостоверений</span><span class="sxs-lookup"><span data-stu-id="74210-648">Identity Federation Support</span></span>

<span data-ttu-id="74210-649">Средства удаленного администрирования сервера (67)</span><span class="sxs-lookup"><span data-stu-id="74210-649">Remote Server Administration Tools (67)</span></span>

<span data-ttu-id="74210-650">Значение</span><span class="sxs-lookup"><span data-stu-id="74210-650">Value</span></span>

<span data-ttu-id="74210-651">Имя</span><span class="sxs-lookup"><span data-stu-id="74210-651">Name</span></span>

<span data-ttu-id="74210-652">256</span><span class="sxs-lookup"><span data-stu-id="74210-652">256</span></span>

[<span data-ttu-id="74210-653">Средства администрирования ролей</span><span class="sxs-lookup"><span data-stu-id="74210-653">Role Administration Tools</span></span>](/windows)

<span data-ttu-id="74210-654">257</span><span class="sxs-lookup"><span data-stu-id="74210-654">257</span></span>

[<span data-ttu-id="74210-655">Средства AD DS</span><span class="sxs-lookup"><span data-stu-id="74210-655">AD DS Tools</span></span>](/windows)<br/> [<span data-ttu-id="74210-656">изменение имени</span><span class="sxs-lookup"><span data-stu-id="74210-656">name change</span></span>](/windows)<br/>

<span data-ttu-id="74210-657">258</span><span class="sxs-lookup"><span data-stu-id="74210-657">258</span></span>

[<span data-ttu-id="74210-658">Средства Snap-Ins и Command-Line AD LDS</span><span class="sxs-lookup"><span data-stu-id="74210-658">AD LDS Snap-Ins and Command-Line Tools</span></span>](/windows)<br/> [<span data-ttu-id="74210-659">изменение имени</span><span class="sxs-lookup"><span data-stu-id="74210-659">name change</span></span>](/windows)<br/>

<span data-ttu-id="74210-660">259</span><span class="sxs-lookup"><span data-stu-id="74210-660">259</span></span>

<span data-ttu-id="74210-661">Средства служб сертификатов Active Directory</span><span class="sxs-lookup"><span data-stu-id="74210-661">Active Directory Certificate Services Tools</span></span>

<span data-ttu-id="74210-662">260</span><span class="sxs-lookup"><span data-stu-id="74210-662">260</span></span>

[<span data-ttu-id="74210-663">Network Policy and Access Services</span><span class="sxs-lookup"><span data-stu-id="74210-663">Network Policy and Access Services</span></span>](/windows)

<span data-ttu-id="74210-664">261</span><span class="sxs-lookup"><span data-stu-id="74210-664">261</span></span>

<span data-ttu-id="74210-665">Средства службы печати и документов</span><span class="sxs-lookup"><span data-stu-id="74210-665">Print and Document Services Tools</span></span><br/> [<span data-ttu-id="74210-666">изменение имени</span><span class="sxs-lookup"><span data-stu-id="74210-666">name change</span></span>](/windows)<br/>

<span data-ttu-id="74210-667">262</span><span class="sxs-lookup"><span data-stu-id="74210-667">262</span></span>

[<span data-ttu-id="74210-668">Службы управления правами Active Directory (AD RMS)</span><span class="sxs-lookup"><span data-stu-id="74210-668">Active Directory Rights Management Services</span></span>](/windows)

<span data-ttu-id="74210-669">263</span><span class="sxs-lookup"><span data-stu-id="74210-669">263</span></span>

[<span data-ttu-id="74210-670">Средства службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="74210-670">Remote Desktop Services Tools</span></span>](/windows)<br/> [<span data-ttu-id="74210-671">изменение имени</span><span class="sxs-lookup"><span data-stu-id="74210-671">name change</span></span>](/windows)<br/>

<span data-ttu-id="74210-672">264</span><span class="sxs-lookup"><span data-stu-id="74210-672">264</span></span>

<span data-ttu-id="74210-673">Средства служб развертывания Windows</span><span class="sxs-lookup"><span data-stu-id="74210-673">Windows Deployment Services Tools</span></span>

<span data-ttu-id="74210-674">265</span><span class="sxs-lookup"><span data-stu-id="74210-674">265</span></span>

[<span data-ttu-id="74210-675">Средства администрирования компонентов</span><span class="sxs-lookup"><span data-stu-id="74210-675">Feature Administration Tools</span></span>](/windows)

<span data-ttu-id="74210-676">266</span><span class="sxs-lookup"><span data-stu-id="74210-676">266</span></span>

<span data-ttu-id="74210-677">Средства шифрования диска BitLocker</span><span class="sxs-lookup"><span data-stu-id="74210-677">BitLocker Drive Encryption Tools</span></span>

<span data-ttu-id="74210-678">267</span><span class="sxs-lookup"><span data-stu-id="74210-678">267</span></span>

<span data-ttu-id="74210-679">Средства серверных расширений BITS</span><span class="sxs-lookup"><span data-stu-id="74210-679">BITS Server Extensions Tools</span></span>

<span data-ttu-id="74210-680">268</span><span class="sxs-lookup"><span data-stu-id="74210-680">268</span></span>

[<span data-ttu-id="74210-681">Средства отказоустойчивости кластеров</span><span class="sxs-lookup"><span data-stu-id="74210-681">Failover Clustering Tools</span></span>](/windows)

<span data-ttu-id="74210-682">269</span><span class="sxs-lookup"><span data-stu-id="74210-682">269</span></span>

<span data-ttu-id="74210-683">Средства балансировки сетевой нагрузки</span><span class="sxs-lookup"><span data-stu-id="74210-683">Network Load Balancing Tools</span></span>

<span data-ttu-id="74210-684">270</span><span class="sxs-lookup"><span data-stu-id="74210-684">270</span></span>

<span data-ttu-id="74210-685">Средства SMTP-сервера</span><span class="sxs-lookup"><span data-stu-id="74210-685">SMTP Server Tools</span></span>

<span data-ttu-id="74210-686">273</span><span class="sxs-lookup"><span data-stu-id="74210-686">273</span></span>

[<span data-ttu-id="74210-687">Средства DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="74210-687">DNS Server Tools</span></span>](/windows)

<span data-ttu-id="74210-688">277</span><span class="sxs-lookup"><span data-stu-id="74210-688">277</span></span>

<span data-ttu-id="74210-689">Средства файловых служб</span><span class="sxs-lookup"><span data-stu-id="74210-689">File Services Tools</span></span>

<span data-ttu-id="74210-690">278</span><span class="sxs-lookup"><span data-stu-id="74210-690">278</span></span>

<span data-ttu-id="74210-691">Средства распределенная файловая система</span><span class="sxs-lookup"><span data-stu-id="74210-691">Distributed File System Tools</span></span>

<span data-ttu-id="74210-692">279</span><span class="sxs-lookup"><span data-stu-id="74210-692">279</span></span>

<span data-ttu-id="74210-693">Средства диспетчер ресурсов файлового сервера</span><span class="sxs-lookup"><span data-stu-id="74210-693">File Server Resource Manager Tools</span></span>

<span data-ttu-id="74210-694">280</span><span class="sxs-lookup"><span data-stu-id="74210-694">280</span></span>

[<span data-ttu-id="74210-695">Службы для средств сетевой файловой системы</span><span class="sxs-lookup"><span data-stu-id="74210-695">Services For Network File System Tools</span></span>](/windows)

<span data-ttu-id="74210-696">281</span><span class="sxs-lookup"><span data-stu-id="74210-696">281</span></span>

<span data-ttu-id="74210-697">Средства веб-сервера (IIS)</span><span class="sxs-lookup"><span data-stu-id="74210-697">Web Server (IIS) Tools</span></span>

<span data-ttu-id="74210-698">284</span><span class="sxs-lookup"><span data-stu-id="74210-698">284</span></span>

[<span data-ttu-id="74210-699">Средства хоста удаленный рабочий стол сеансов</span><span class="sxs-lookup"><span data-stu-id="74210-699">Remote Desktop Session Host Tools</span></span>](/windows)<br/> [<span data-ttu-id="74210-700">изменение имени</span><span class="sxs-lookup"><span data-stu-id="74210-700">name change</span></span>](/windows)<br/>

<span data-ttu-id="74210-701">285</span><span class="sxs-lookup"><span data-stu-id="74210-701">285</span></span>

<span data-ttu-id="74210-702">Средства шлюза удаленный рабочий стол</span><span class="sxs-lookup"><span data-stu-id="74210-702">Remote Desktop Gateway Tools</span></span><br/> [<span data-ttu-id="74210-703">изменение имени</span><span class="sxs-lookup"><span data-stu-id="74210-703">name change</span></span>](/windows)<br/>

<span data-ttu-id="74210-704">286</span><span class="sxs-lookup"><span data-stu-id="74210-704">286</span></span>

<span data-ttu-id="74210-705">Средства лицензирования удаленный рабочий стол</span><span class="sxs-lookup"><span data-stu-id="74210-705">Remote Desktop Licensing Tools</span></span><br/> [<span data-ttu-id="74210-706">изменение имени</span><span class="sxs-lookup"><span data-stu-id="74210-706">name change</span></span>](/windows)<br/>

<span data-ttu-id="74210-707">288</span><span class="sxs-lookup"><span data-stu-id="74210-707">288</span></span>

<span data-ttu-id="74210-708">Средства факсового сервера</span><span class="sxs-lookup"><span data-stu-id="74210-708">Fax Server Tools</span></span>

<span data-ttu-id="74210-709">290</span><span class="sxs-lookup"><span data-stu-id="74210-709">290</span></span>

<span data-ttu-id="74210-710">Средства WINS-сервера</span><span class="sxs-lookup"><span data-stu-id="74210-710">WINS Server Tools</span></span>

<span data-ttu-id="74210-711">291</span><span class="sxs-lookup"><span data-stu-id="74210-711">291</span></span>

[<span data-ttu-id="74210-712">Средства служб UDDI</span><span class="sxs-lookup"><span data-stu-id="74210-712">UDDI Services Tools</span></span>](/windows)<br/>

<span data-ttu-id="74210-713">292</span><span class="sxs-lookup"><span data-stu-id="74210-713">292</span></span>

<span data-ttu-id="74210-714">Средства центра сертификации</span><span class="sxs-lookup"><span data-stu-id="74210-714">Certification Authority Tools</span></span>

<span data-ttu-id="74210-715">293</span><span class="sxs-lookup"><span data-stu-id="74210-715">293</span></span>

<span data-ttu-id="74210-716">Средства сетевого ответчика</span><span class="sxs-lookup"><span data-stu-id="74210-716">Online Responder Tools</span></span>

<span data-ttu-id="74210-717">297</span><span class="sxs-lookup"><span data-stu-id="74210-717">297</span></span>

[<span data-ttu-id="74210-718">Средства сервера для NIS</span><span class="sxs-lookup"><span data-stu-id="74210-718">Server for NIS Tools</span></span>](/windows)

<span data-ttu-id="74210-719">299</span><span class="sxs-lookup"><span data-stu-id="74210-719">299</span></span>

[<span data-ttu-id="74210-720">Средства Snap-Ins и Command-Line AD DS</span><span class="sxs-lookup"><span data-stu-id="74210-720">AD DS Snap-Ins and Command-Line Tools</span></span>](/windows)<br/> [<span data-ttu-id="74210-721">изменение имени</span><span class="sxs-lookup"><span data-stu-id="74210-721">name change</span></span>](/windows)<br/>

<span data-ttu-id="74210-722">300</span><span class="sxs-lookup"><span data-stu-id="74210-722">300</span></span>

[<span data-ttu-id="74210-723">Центр администрирования Active Directory</span><span class="sxs-lookup"><span data-stu-id="74210-723">Active Directory Administrative Center</span></span>](/windows)

<span data-ttu-id="74210-724">301</span><span class="sxs-lookup"><span data-stu-id="74210-724">301</span></span>

<span data-ttu-id="74210-725">Средства Hyper-V</span><span class="sxs-lookup"><span data-stu-id="74210-725">Hyper-V Tools</span></span>

<span data-ttu-id="74210-726">323</span><span class="sxs-lookup"><span data-stu-id="74210-726">323</span></span>

[<span data-ttu-id="74210-727">Средство просмотра паролей восстановления BitLocker</span><span class="sxs-lookup"><span data-stu-id="74210-727">BitLocker Recovery Password Viewer</span></span>](/windows)<br/>

<span data-ttu-id="74210-728">326</span><span class="sxs-lookup"><span data-stu-id="74210-728">326</span></span>

[<span data-ttu-id="74210-729">Служебные программы шифрование диска BitLocker Administration</span><span class="sxs-lookup"><span data-stu-id="74210-729">BitLocker Drive Encryption Administration Utilities</span></span>](/windows)<br/>

<span data-ttu-id="74210-730">329</span><span class="sxs-lookup"><span data-stu-id="74210-730">329</span></span>

[<span data-ttu-id="74210-731">Средства AD DS и AD LDS</span><span class="sxs-lookup"><span data-stu-id="74210-731">AD DS and AD LDS Tools</span></span>](/windows)<br/>

<span data-ttu-id="74210-732">330</span><span class="sxs-lookup"><span data-stu-id="74210-732">330</span></span>

<span data-ttu-id="74210-733">Центр администрирования Active Directory</span><span class="sxs-lookup"><span data-stu-id="74210-733">Active Directory Administrative Center</span></span><br/>

<span data-ttu-id="74210-734">331</span><span class="sxs-lookup"><span data-stu-id="74210-734">331</span></span>

[<span data-ttu-id="74210-735">Модуль Active Directory для Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="74210-735">Active Directory module for Windows PowerShell</span></span>](/windows)<br/>

<span data-ttu-id="74210-736">337</span><span class="sxs-lookup"><span data-stu-id="74210-736">337</span></span>

[<span data-ttu-id="74210-737">Средства брокера подключение к удаленному рабочему столу</span><span class="sxs-lookup"><span data-stu-id="74210-737">Remote Desktop Connection Broker Tools</span></span>](/windows)<br/>

<span data-ttu-id="74210-738">410</span><span class="sxs-lookup"><span data-stu-id="74210-738">410</span></span>

[<span data-ttu-id="74210-739">Клиент управления IP-адресами (IPAM)</span><span class="sxs-lookup"><span data-stu-id="74210-739">IP Address Management (IPAM) Client</span></span>](/windows)

<span data-ttu-id="74210-740">450</span><span class="sxs-lookup"><span data-stu-id="74210-740">450</span></span>

[<span data-ttu-id="74210-741">Модуль Hyper-V для Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="74210-741">Hyper-V Module for Windows PowerShell</span></span>](/windows)

<span data-ttu-id="74210-742">462</span><span class="sxs-lookup"><span data-stu-id="74210-742">462</span></span>

[<span data-ttu-id="74210-743">Средства службы Active Directory Rights Management</span><span class="sxs-lookup"><span data-stu-id="74210-743">Active Directory Rights Management Services Tools</span></span>](/windows)

<span data-ttu-id="74210-744">465</span><span class="sxs-lookup"><span data-stu-id="74210-744">465</span></span>

[<span data-ttu-id="74210-745">Средство управления общими ресурсами и хранилищами</span><span class="sxs-lookup"><span data-stu-id="74210-745">Share and Storage Management Tool</span></span>](/windows)

<span data-ttu-id="74210-746">471</span><span class="sxs-lookup"><span data-stu-id="74210-746">471</span></span>

[<span data-ttu-id="74210-747">Средства управления удаленным доступом</span><span class="sxs-lookup"><span data-stu-id="74210-747">Remote Access Management Tools</span></span>](/windows)

<span data-ttu-id="74210-748">472</span><span class="sxs-lookup"><span data-stu-id="74210-748">472</span></span>

[<span data-ttu-id="74210-749">модуль удаленного доступа для Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="74210-749">Remote Access module for Windows PowerShell</span></span>](/windows)

<span data-ttu-id="74210-750">473</span><span class="sxs-lookup"><span data-stu-id="74210-750">473</span></span>

[<span data-ttu-id="74210-751">Графический интерфейс удаленного доступа и средства Command-Line</span><span class="sxs-lookup"><span data-stu-id="74210-751">Remote Access GUI and Command-Line Tools</span></span>](/windows)

<span data-ttu-id="74210-752">474</span><span class="sxs-lookup"><span data-stu-id="74210-752">474</span></span>

[<span data-ttu-id="74210-753">Средства Windows Server Update Services</span><span class="sxs-lookup"><span data-stu-id="74210-753">Windows Server Update Services Tools</span></span>](/windows)

<span data-ttu-id="74210-754">476</span><span class="sxs-lookup"><span data-stu-id="74210-754">476</span></span>

[<span data-ttu-id="74210-755">Средства диагностики лицензирования удаленный рабочий стол</span><span class="sxs-lookup"><span data-stu-id="74210-755">Remote Desktop Licensing Diagnoser Tools</span></span>](/windows)

<span data-ttu-id="74210-756">479</span><span class="sxs-lookup"><span data-stu-id="74210-756">479</span></span>

[<span data-ttu-id="74210-757">Средства SNMP</span><span class="sxs-lookup"><span data-stu-id="74210-757">SNMP Tools</span></span>](/windows)

<span data-ttu-id="74210-758">480</span><span class="sxs-lookup"><span data-stu-id="74210-758">480</span></span>

[<span data-ttu-id="74210-759">Средства многопользовательской активации</span><span class="sxs-lookup"><span data-stu-id="74210-759">Volume Activation Tools</span></span>](/windows)

<span data-ttu-id="74210-760">Функции cистема архивации данных Windows Server (39)</span><span class="sxs-lookup"><span data-stu-id="74210-760">Windows Server Backup - Features (39)</span></span>

<span data-ttu-id="74210-761">Значение</span><span class="sxs-lookup"><span data-stu-id="74210-761">Value</span></span>

<span data-ttu-id="74210-762">Имя</span><span class="sxs-lookup"><span data-stu-id="74210-762">Name</span></span>

<span data-ttu-id="74210-763">296</span><span class="sxs-lookup"><span data-stu-id="74210-763">296</span></span>

[<span data-ttu-id="74210-764">Система архивации данных Windows Server</span><span class="sxs-lookup"><span data-stu-id="74210-764">Windows Server Backup</span></span>](/windows)

<span data-ttu-id="74210-765">297</span><span class="sxs-lookup"><span data-stu-id="74210-765">297</span></span>

[<span data-ttu-id="74210-766">Программы командной строки</span><span class="sxs-lookup"><span data-stu-id="74210-766">Command Line Tools</span></span>](/windows)

<span data-ttu-id="74210-767">Функции службы рукописного ввода (310)</span><span class="sxs-lookup"><span data-stu-id="74210-767">Ink and Handwriting Services - Features (310)</span></span>

<span data-ttu-id="74210-768">Значение</span><span class="sxs-lookup"><span data-stu-id="74210-768">Value</span></span>

<span data-ttu-id="74210-769">Имя</span><span class="sxs-lookup"><span data-stu-id="74210-769">Name</span></span>

<span data-ttu-id="74210-770">311</span><span class="sxs-lookup"><span data-stu-id="74210-770">311</span></span>

[<span data-ttu-id="74210-771">Поддержка рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="74210-771">Ink Support</span></span>](/windows)<br/>

<span data-ttu-id="74210-772">312</span><span class="sxs-lookup"><span data-stu-id="74210-772">312</span></span>

[<span data-ttu-id="74210-773">Распознавание рукописного текста</span><span class="sxs-lookup"><span data-stu-id="74210-773">Handwriting Recognition</span></span>](/windows)<br/>

<span data-ttu-id="74210-774">Фоновая интеллектуальная служба передачи (BITS) — функции (335)</span><span class="sxs-lookup"><span data-stu-id="74210-774">Background Intelligent Transfer Service (BITS) - Features (335)</span></span>

<span data-ttu-id="74210-775">Значение</span><span class="sxs-lookup"><span data-stu-id="74210-775">Value</span></span>

<span data-ttu-id="74210-776">Имя</span><span class="sxs-lookup"><span data-stu-id="74210-776">Name</span></span>

<span data-ttu-id="74210-777">54</span><span class="sxs-lookup"><span data-stu-id="74210-777">54</span></span>

<span data-ttu-id="74210-778">Расширение сервера IIS</span><span class="sxs-lookup"><span data-stu-id="74210-778">IIS Server Extension</span></span>

<span data-ttu-id="74210-779">332</span><span class="sxs-lookup"><span data-stu-id="74210-779">332</span></span>

[<span data-ttu-id="74210-780">Облегченный сервер загрузки</span><span class="sxs-lookup"><span data-stu-id="74210-780">Compact Server</span></span>](/windows)<br/>

<span data-ttu-id="74210-781">Поддержка WOW64 — функции (340)</span><span class="sxs-lookup"><span data-stu-id="74210-781">Wow64 Support - Features (340)</span></span>

<span data-ttu-id="74210-782">Значение</span><span class="sxs-lookup"><span data-stu-id="74210-782">Value</span></span>

<span data-ttu-id="74210-783">Имя</span><span class="sxs-lookup"><span data-stu-id="74210-783">Name</span></span>

<span data-ttu-id="74210-784">341</span><span class="sxs-lookup"><span data-stu-id="74210-784">341</span></span>

[<span data-ttu-id="74210-785">WoW64</span><span class="sxs-lookup"><span data-stu-id="74210-785">WoW64</span></span>](#wow64)<br/>

<span data-ttu-id="74210-786">342</span><span class="sxs-lookup"><span data-stu-id="74210-786">342</span></span>

[<span data-ttu-id="74210-787">Подсистема WoW64 для платформа .NET Framework 2,0 и Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="74210-787">WoW64 for .NET Framework 2.0 and Windows PowerShell</span></span>](/windows)<br/>

<span data-ttu-id="74210-788">343</span><span class="sxs-lookup"><span data-stu-id="74210-788">343</span></span>

[<span data-ttu-id="74210-789">Подсистема WoW64 для платформа .NET Framework 2,0</span><span class="sxs-lookup"><span data-stu-id="74210-789">WoW64 for .NET Framework 2.0</span></span>](/windows)<br/>

<span data-ttu-id="74210-790">344</span><span class="sxs-lookup"><span data-stu-id="74210-790">344</span></span>

[<span data-ttu-id="74210-791">Подсистема WoW64 для PowerShell</span><span class="sxs-lookup"><span data-stu-id="74210-791">WoW64 for PowerShell</span></span>](/windows)<br/>

<span data-ttu-id="74210-792">345</span><span class="sxs-lookup"><span data-stu-id="74210-792">345</span></span>

[<span data-ttu-id="74210-793">Подсистема WoW64 для платформа .NET Framework 3,0 и 3,5</span><span class="sxs-lookup"><span data-stu-id="74210-793">WoW64 for .NET Framework 3.0 and 3.5</span></span>](/windows)<br/>

<span data-ttu-id="74210-794">346</span><span class="sxs-lookup"><span data-stu-id="74210-794">346</span></span>

[<span data-ttu-id="74210-795">Подсистема WoW64 для служб печати</span><span class="sxs-lookup"><span data-stu-id="74210-795">WoW64 for Print Services</span></span>](/windows)<br/>

<span data-ttu-id="74210-796">347</span><span class="sxs-lookup"><span data-stu-id="74210-796">347</span></span>

[<span data-ttu-id="74210-797">Подсистема WoW64 для отказоустойчивой кластеризации</span><span class="sxs-lookup"><span data-stu-id="74210-797">WoW64 for Failover Clustering</span></span>](/windows)<br/>

<span data-ttu-id="74210-798">348</span><span class="sxs-lookup"><span data-stu-id="74210-798">348</span></span>

[<span data-ttu-id="74210-799">Подсистема WoW64 для редактора метода ввода</span><span class="sxs-lookup"><span data-stu-id="74210-799">WoW64 for Input Method Editor</span></span>](/windows)<br/>

<span data-ttu-id="74210-800">349</span><span class="sxs-lookup"><span data-stu-id="74210-800">349</span></span>

[<span data-ttu-id="74210-801">Подсистема WoW64 для приложений на основе UNIX</span><span class="sxs-lookup"><span data-stu-id="74210-801">WoW64 for Subsystem for UNIX-based Applications</span></span>](/windows)<br/>

<span data-ttu-id="74210-802">Пользовательские интерфейсы и инфраструктура — службы ролей (447)</span><span class="sxs-lookup"><span data-stu-id="74210-802">User Interfaces and Infrastructure - Role Services (447)</span></span>

<span data-ttu-id="74210-803">Значение</span><span class="sxs-lookup"><span data-stu-id="74210-803">Value</span></span>

<span data-ttu-id="74210-804">Имя</span><span class="sxs-lookup"><span data-stu-id="74210-804">Name</span></span>

<span data-ttu-id="74210-805">35</span><span class="sxs-lookup"><span data-stu-id="74210-805">35</span></span>

[<span data-ttu-id="74210-806">Возможности рабочего стола</span><span class="sxs-lookup"><span data-stu-id="74210-806">Desktop Experience</span></span>](/windows)

<span data-ttu-id="74210-807">99</span><span class="sxs-lookup"><span data-stu-id="74210-807">99</span></span>

[<span data-ttu-id="74210-808">Графическая оболочка сервера</span><span class="sxs-lookup"><span data-stu-id="74210-808">Server Graphical Shell</span></span>](/windows)

<span data-ttu-id="74210-809">Службы Windows Server Update Services — функции (404)</span><span class="sxs-lookup"><span data-stu-id="74210-809">Window Server Update Services - Features (404)</span></span>

<span data-ttu-id="74210-810">Значение</span><span class="sxs-lookup"><span data-stu-id="74210-810">Value</span></span>

<span data-ttu-id="74210-811">Имя</span><span class="sxs-lookup"><span data-stu-id="74210-811">Name</span></span>

<span data-ttu-id="74210-812">405</span><span class="sxs-lookup"><span data-stu-id="74210-812">405</span></span>

[<span data-ttu-id="74210-813">API и командлеты PowerShell</span><span class="sxs-lookup"><span data-stu-id="74210-813">API and PowerShell cmdlets</span></span>](/windows)

<span data-ttu-id="74210-814">406</span><span class="sxs-lookup"><span data-stu-id="74210-814">406</span></span>

[<span data-ttu-id="74210-815">Подключение SQL Server</span><span class="sxs-lookup"><span data-stu-id="74210-815">SQL Server Connectivity</span></span>](/windows)

<span data-ttu-id="74210-816">407</span><span class="sxs-lookup"><span data-stu-id="74210-816">407</span></span>

[<span data-ttu-id="74210-817">Службы WSUS</span><span class="sxs-lookup"><span data-stu-id="74210-817">WSUS Services</span></span>](/windows)

<span data-ttu-id="74210-818">408</span><span class="sxs-lookup"><span data-stu-id="74210-818">408</span></span>

[<span data-ttu-id="74210-819">Консоль управления пользовательским интерфейсом</span><span class="sxs-lookup"><span data-stu-id="74210-819">User Interface Management Console</span></span>](/windows)

<span data-ttu-id="74210-820">449</span><span class="sxs-lookup"><span data-stu-id="74210-820">449</span></span>

[<span data-ttu-id="74210-821">Подключение WID</span><span class="sxs-lookup"><span data-stu-id="74210-821">WID Connectivity</span></span>](/windows)

<span data-ttu-id="74210-822">Windows PowerShell — функции (417)</span><span class="sxs-lookup"><span data-stu-id="74210-822">Windows PowerShell - Features (417)</span></span>

<span data-ttu-id="74210-823">Значение</span><span class="sxs-lookup"><span data-stu-id="74210-823">Value</span></span>

<span data-ttu-id="74210-824">Имя</span><span class="sxs-lookup"><span data-stu-id="74210-824">Name</span></span>

<span data-ttu-id="74210-825">411</span><span class="sxs-lookup"><span data-stu-id="74210-825">411</span></span>

[<span data-ttu-id="74210-826">Подсистема Windows PowerShell 2,0</span><span class="sxs-lookup"><span data-stu-id="74210-826">Windows PowerShell 2.0 Engine</span></span>](/windows)

<span data-ttu-id="74210-827">412</span><span class="sxs-lookup"><span data-stu-id="74210-827">412</span></span>

[<span data-ttu-id="74210-828">Windows PowerShell 3.0</span><span class="sxs-lookup"><span data-stu-id="74210-828">Windows PowerShell 3.0</span></span>](/windows)

<span data-ttu-id="74210-829">448</span><span class="sxs-lookup"><span data-stu-id="74210-829">448</span></span>

[<span data-ttu-id="74210-830">Windows PowerShell Web Access</span><span class="sxs-lookup"><span data-stu-id="74210-830">Windows PowerShell Web Access</span></span>](/windows)

<span data-ttu-id="74210-831">1000</span><span class="sxs-lookup"><span data-stu-id="74210-831">1000</span></span>

[<span data-ttu-id="74210-832">Служба настройки требуемого состояния Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="74210-832">Windows PowerShell Desired State Configuration Service</span></span>](/windows)

<span data-ttu-id="74210-833">Платформа .NET Framework 4,5-функции (418)</span><span class="sxs-lookup"><span data-stu-id="74210-833">.NET Framework 4.5 - Features (418)</span></span>

<span data-ttu-id="74210-834">Значение</span><span class="sxs-lookup"><span data-stu-id="74210-834">Value</span></span>

<span data-ttu-id="74210-835">Имя</span><span class="sxs-lookup"><span data-stu-id="74210-835">Name</span></span>

<span data-ttu-id="74210-836">419</span><span class="sxs-lookup"><span data-stu-id="74210-836">419</span></span>

[<span data-ttu-id="74210-837">Расширенная платформа .NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="74210-837">.NET Framework 4.5 Extended</span></span>](/windows)

<span data-ttu-id="74210-838">420</span><span class="sxs-lookup"><span data-stu-id="74210-838">420</span></span>

[<span data-ttu-id="74210-839">Службы WCF</span><span class="sxs-lookup"><span data-stu-id="74210-839">WCF Services</span></span>](/windows)

<span data-ttu-id="74210-840">421</span><span class="sxs-lookup"><span data-stu-id="74210-840">421</span></span>

[<span data-ttu-id="74210-841">Активация по HTTP</span><span class="sxs-lookup"><span data-stu-id="74210-841">HTTP Activation</span></span>](/windows)

<span data-ttu-id="74210-842">422</span><span class="sxs-lookup"><span data-stu-id="74210-842">422</span></span>

[<span data-ttu-id="74210-843">Активация очереди сообщений (MSMQ)</span><span class="sxs-lookup"><span data-stu-id="74210-843">Message Queuing (MSMQ) Activation</span></span>](/windows)

<span data-ttu-id="74210-844">423</span><span class="sxs-lookup"><span data-stu-id="74210-844">423</span></span>

[<span data-ttu-id="74210-845">Активация именованного канала</span><span class="sxs-lookup"><span data-stu-id="74210-845">Named Pipe Activation</span></span>](/windows)

<span data-ttu-id="74210-846">424</span><span class="sxs-lookup"><span data-stu-id="74210-846">424</span></span>

[<span data-ttu-id="74210-847">Активация TCP</span><span class="sxs-lookup"><span data-stu-id="74210-847">TCP Activation</span></span>](/windows)

<span data-ttu-id="74210-848">425</span><span class="sxs-lookup"><span data-stu-id="74210-848">425</span></span>

[<span data-ttu-id="74210-849">Совместное использование TCP-портов</span><span class="sxs-lookup"><span data-stu-id="74210-849">TCP Port Sharing</span></span>](/windows)

<span data-ttu-id="74210-850">429</span><span class="sxs-lookup"><span data-stu-id="74210-850">429</span></span>

[<span data-ttu-id="74210-851">ASP.NET 4,5</span><span class="sxs-lookup"><span data-stu-id="74210-851">ASP.NET 4.5</span></span>](/windows)

<span data-ttu-id="74210-852">Удаленный доступ — роль (468)</span><span class="sxs-lookup"><span data-stu-id="74210-852">Remote Access - Role (468)</span></span>

<span data-ttu-id="74210-853">Значение</span><span class="sxs-lookup"><span data-stu-id="74210-853">Value</span></span>

<span data-ttu-id="74210-854">Имя</span><span class="sxs-lookup"><span data-stu-id="74210-854">Name</span></span>

<span data-ttu-id="74210-855">469</span><span class="sxs-lookup"><span data-stu-id="74210-855">469</span></span>

[<span data-ttu-id="74210-856">DirectAccess и VPN (RAS)</span><span class="sxs-lookup"><span data-stu-id="74210-856">DirectAccess and VPN (RAS)</span></span>](/windows)

<span data-ttu-id="74210-857">470</span><span class="sxs-lookup"><span data-stu-id="74210-857">470</span></span>

[<span data-ttu-id="74210-858">Маршрутизация</span><span class="sxs-lookup"><span data-stu-id="74210-858">Routing</span></span>](#routing)

<span data-ttu-id="74210-859">Службы файлов и хранения — роль (481)</span><span class="sxs-lookup"><span data-stu-id="74210-859">File and Storage Services - Role (481)</span></span>

<span data-ttu-id="74210-860">Значение</span><span class="sxs-lookup"><span data-stu-id="74210-860">Value</span></span>

<span data-ttu-id="74210-861">Имя</span><span class="sxs-lookup"><span data-stu-id="74210-861">Name</span></span>

<span data-ttu-id="74210-862">482</span><span class="sxs-lookup"><span data-stu-id="74210-862">482</span></span>

[<span data-ttu-id="74210-863">Службы хранилища</span><span class="sxs-lookup"><span data-stu-id="74210-863">Storage Services</span></span>](/windows)

<span data-ttu-id="74210-864">484</span><span class="sxs-lookup"><span data-stu-id="74210-864">484</span></span>

[<span data-ttu-id="74210-865">Средства управления отказоустойчивыми кластерами</span><span class="sxs-lookup"><span data-stu-id="74210-865">Failover Cluster Management Tools</span></span>](/windows)



 

</dd> <dt>

<span data-ttu-id="74210-866">**Name**</span><span class="sxs-lookup"><span data-stu-id="74210-866">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74210-867">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="74210-867">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74210-868">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="74210-868">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74210-869">Отображаемое имя компонента сервера, например "файловый сервер", "сервер печати" или "возможности рабочего стола".</span><span class="sxs-lookup"><span data-stu-id="74210-869">Display name of the server feature, such as "File Server", "Print Server", or "Desktop Experience".</span></span>

</dd> <dt>

<span data-ttu-id="74210-870">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="74210-870">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74210-871">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74210-871">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74210-872">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="74210-872">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74210-873">ИДЕНТИФИКАЦИОНный номер компонента родительского сервера.</span><span class="sxs-lookup"><span data-stu-id="74210-873">ID number of the parent server feature.</span></span> <span data-ttu-id="74210-874">Это свойство равно 0, если функция, представленная текущим экземпляром класса, не имеет родительского компонента.</span><span class="sxs-lookup"><span data-stu-id="74210-874">This property is 0 if the feature represented by the current instance of the class does not have a parent feature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="74210-875">Комментарии</span><span class="sxs-lookup"><span data-stu-id="74210-875">Remarks</span></span>

<span data-ttu-id="74210-876">Ознакомьтесь с [техническим обзором Windows Server 2008 диспетчер сервера](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753319(v=ws.10)) , чтобы узнать о возможностях сервера.</span><span class="sxs-lookup"><span data-stu-id="74210-876">Read the [Windows Server 2008 Server Manager Technical Overview](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753319(v=ws.10)) to learn about server features.</span></span>

<span data-ttu-id="74210-877">Предприятия, которые не используют программное обеспечение для управления, которое сообщает о возможностях сервера, например System Center Operations Manager с установленными пакетами управления, могут получить эту информацию, запросив класс **Win32 \_ ServerFeature** .</span><span class="sxs-lookup"><span data-stu-id="74210-877">Enterprises that do not use management software that reports server features, such as System Center Operations Manager with management packs installed, can get that information by querying the **Win32\_ServerFeature** class.</span></span>

<span data-ttu-id="74210-878">Функции удаленного взаимодействия WMI или WinRM можно использовать для получения сведений о компонентах сервера с удаленных серверов.</span><span class="sxs-lookup"><span data-stu-id="74210-878">You can use the remoting features of WMI or WinRM to get server feature information from remote servers.</span></span> <span data-ttu-id="74210-879">Дополнительные сведения об удаленных DCOM-подключениях WMI см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="74210-879">For more information about remote WMI DCOM connections, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span> <span data-ttu-id="74210-880">Дополнительные сведения о WinRM см. в статье Windows Remote Management (Удаленное управление Windows).</span><span class="sxs-lookup"><span data-stu-id="74210-880">For more information about WinRM, see Windows Remote Management.</span></span>

<span data-ttu-id="74210-881">Windows Server 2012: **Win32 \_ ServerFeature** является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="74210-881">Windows Server 2012: **Win32\_ServerFeature** has been deprecated.</span></span> <span data-ttu-id="74210-882">Для программного доступа к сведениям о компонентах Windows Server можно использовать [командлеты Диспетчер сервера](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee662311(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="74210-882">To access windows server feature information programmatically, you can use the [Server Manager Cmdlets](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee662311(v=technet.10)).</span></span>

### <a name="windows-server-2012-r2"></a><span data-ttu-id="74210-883">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="74210-883">Windows Server 2012 R2</span></span>

<dl> <dt>

<span data-ttu-id="74210-884"><span id="Application_Server"></span><span id="application_server"></span><span id="APPLICATION_SERVER"></span>Сервер приложений</span><span class="sxs-lookup"><span data-stu-id="74210-884"><span id="Application_Server"></span><span id="application_server"></span><span id="APPLICATION_SERVER"></span>Application Server</span></span>
</dt> <dd>

<span data-ttu-id="74210-885">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-885">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-886"><span id="Streaming_Media_Services"></span><span id="streaming_media_services"></span><span id="STREAMING_MEDIA_SERVICES"></span>Службы потокового мультимедиа</span><span class="sxs-lookup"><span data-stu-id="74210-886"><span id="Streaming_Media_Services"></span><span id="streaming_media_services"></span><span id="STREAMING_MEDIA_SERVICES"></span>Streaming Media Services</span></span>
</dt> <dd>

<span data-ttu-id="74210-887">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-887">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-888"><span id="Active_Directory_Federation_Services"></span><span id="active_directory_federation_services"></span><span id="ACTIVE_DIRECTORY_FEDERATION_SERVICES"></span>службы федерации Active Directory (AD FS)</span><span class="sxs-lookup"><span data-stu-id="74210-888"><span id="Active_Directory_Federation_Services"></span><span id="active_directory_federation_services"></span><span id="ACTIVE_DIRECTORY_FEDERATION_SERVICES"></span>Active Directory Federation Services</span></span>
</dt> <dd>

<span data-ttu-id="74210-889">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-889">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-890"><span id="DHCP_Server"></span><span id="dhcp_server"></span><span id="DHCP_SERVER"></span>DHCP-сервер</span><span class="sxs-lookup"><span data-stu-id="74210-890"><span id="DHCP_Server"></span><span id="dhcp_server"></span><span id="DHCP_SERVER"></span>DHCP Server</span></span>
</dt> <dd>

<span data-ttu-id="74210-891">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-891">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-892"><span id="DNS_Server"></span><span id="dns_server"></span><span id="DNS_SERVER"></span>DNS-сервер</span><span class="sxs-lookup"><span data-stu-id="74210-892"><span id="DNS_Server"></span><span id="dns_server"></span><span id="DNS_SERVER"></span>DNS Server</span></span>
</dt> <dd>

<span data-ttu-id="74210-893">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-893">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-894"><span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="74210-894"><span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>Remote Desktop Services</span></span>
</dt> <dd>

<span data-ttu-id="74210-895">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-895">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-896"><span id="Windows_Server_Update_Services"></span><span id="windows_server_update_services"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES"></span>Windows Server Update Services</span><span class="sxs-lookup"><span data-stu-id="74210-896"><span id="Windows_Server_Update_Services"></span><span id="windows_server_update_services"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES"></span>Windows Server Update Services</span></span>
</dt> <dd>

<span data-ttu-id="74210-897">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-897">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-898"><span id="Failover_Clustering"></span><span id="failover_clustering"></span><span id="FAILOVER_CLUSTERING"></span>Отказоустойчивая кластеризация</span><span class="sxs-lookup"><span data-stu-id="74210-898"><span id="Failover_Clustering"></span><span id="failover_clustering"></span><span id="FAILOVER_CLUSTERING"></span>Failover Clustering</span></span>
</dt> <dd>

<span data-ttu-id="74210-899">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-899">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-900"><span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Балансировка сетевой нагрузки</span><span class="sxs-lookup"><span data-stu-id="74210-900"><span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Network Load Balancing</span></span>
</dt> <dd>

<span data-ttu-id="74210-901">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-901">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-902"><span id=".NET_Framework_3.5.1_Features"></span><span id=".net_framework_3.5.1_features"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES"></span>Функции платформа .NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="74210-902"><span id=".NET_Framework_3.5.1_Features"></span><span id=".net_framework_3.5.1_features"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES"></span>.NET Framework 3.5.1 Features</span></span>
</dt> <dd>

<span data-ttu-id="74210-903">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-903">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-904"><span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>диспетчер ресурсов системы Windows</span><span class="sxs-lookup"><span data-stu-id="74210-904"><span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Windows System Resource Manager</span></span>
</dt> <dd>

<span data-ttu-id="74210-905">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-905">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-906"><span id="Windows_Server_Backup_Features"></span><span id="windows_server_backup_features"></span><span id="WINDOWS_SERVER_BACKUP_FEATURES"></span>cистема архивации данных Windows Server функции</span><span class="sxs-lookup"><span data-stu-id="74210-906"><span id="Windows_Server_Backup_Features"></span><span id="windows_server_backup_features"></span><span id="WINDOWS_SERVER_BACKUP_FEATURES"></span>Windows Server Backup Features</span></span>
</dt> <dd>

<span data-ttu-id="74210-907">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-907">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-908"><span id="Remote_Assistance"></span><span id="remote_assistance"></span><span id="REMOTE_ASSISTANCE"></span>Удаленный помощник</span><span class="sxs-lookup"><span data-stu-id="74210-908"><span id="Remote_Assistance"></span><span id="remote_assistance"></span><span id="REMOTE_ASSISTANCE"></span>Remote Assistance</span></span>
</dt> <dd>

<span data-ttu-id="74210-909">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-909">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-910"><span id="Telnet_Client"></span><span id="telnet_client"></span><span id="TELNET_CLIENT"></span>Клиент Telnet</span><span class="sxs-lookup"><span data-stu-id="74210-910"><span id="Telnet_Client"></span><span id="telnet_client"></span><span id="TELNET_CLIENT"></span>Telnet Client</span></span>
</dt> <dd>

<span data-ttu-id="74210-911">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-911">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-912"><span id="Telnet_Server"></span><span id="telnet_server"></span><span id="TELNET_SERVER"></span>Сервер Telnet</span><span class="sxs-lookup"><span data-stu-id="74210-912"><span id="Telnet_Server"></span><span id="telnet_server"></span><span id="TELNET_SERVER"></span>Telnet Server</span></span>
</dt> <dd>

<span data-ttu-id="74210-913">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-913">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-914"><span id="Subsystem_For_Unix-based_Applications"></span><span id="subsystem_for_unix-based_applications"></span><span id="SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>Подсистема для приложений на базе UNIX</span><span class="sxs-lookup"><span data-stu-id="74210-914"><span id="Subsystem_For_Unix-based_Applications"></span><span id="subsystem_for_unix-based_applications"></span><span id="SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>Subsystem For Unix-based Applications</span></span>
</dt> <dd>

<span data-ttu-id="74210-915">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-915">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-916"><span id="Windows_Internal_Database"></span><span id="windows_internal_database"></span><span id="WINDOWS_INTERNAL_DATABASE"></span>Внутренняя база данных Windows</span><span class="sxs-lookup"><span data-stu-id="74210-916"><span id="Windows_Internal_Database"></span><span id="windows_internal_database"></span><span id="WINDOWS_INTERNAL_DATABASE"></span>Windows Internal Database</span></span>
</dt> <dd>

<span data-ttu-id="74210-917">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-917">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-918"><span id="Storage_Manager_For_SANs"></span><span id="storage_manager_for_sans"></span><span id="STORAGE_MANAGER_FOR_SANS"></span>Диспетчер хранилища для сетей SAN</span><span class="sxs-lookup"><span data-stu-id="74210-918"><span id="Storage_Manager_For_SANs"></span><span id="storage_manager_for_sans"></span><span id="STORAGE_MANAGER_FOR_SANS"></span>Storage Manager For SANs</span></span>
</dt> <dd>

<span data-ttu-id="74210-919">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-919">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-920"><span id="Internet_Storage_Name_Server"></span><span id="internet_storage_name_server"></span><span id="INTERNET_STORAGE_NAME_SERVER"></span>Сервер службы имен хранилищ Интернета</span><span class="sxs-lookup"><span data-stu-id="74210-920"><span id="Internet_Storage_Name_Server"></span><span id="internet_storage_name_server"></span><span id="INTERNET_STORAGE_NAME_SERVER"></span>Internet Storage Name Server</span></span>
</dt> <dd>

<span data-ttu-id="74210-921">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-921">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-922"><span id="Multipath_I_O"></span><span id="multipath_i_o"></span><span id="MULTIPATH_I_O"></span>Multipath I/O</span><span class="sxs-lookup"><span data-stu-id="74210-922"><span id="Multipath_I_O"></span><span id="multipath_i_o"></span><span id="MULTIPATH_I_O"></span>Multipath I/O</span></span>
</dt> <dd>

<span data-ttu-id="74210-923">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-923">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-924"><span id="SNMP_Services"></span><span id="snmp_services"></span><span id="SNMP_SERVICES"></span>Службы SNMP</span><span class="sxs-lookup"><span data-stu-id="74210-924"><span id="SNMP_Services"></span><span id="snmp_services"></span><span id="SNMP_SERVICES"></span>SNMP Services</span></span>
</dt> <dd>

<span data-ttu-id="74210-925">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-925">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-926"><span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Службы для сетевой файловой системы</span><span class="sxs-lookup"><span data-stu-id="74210-926"><span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Services For Network File System</span></span>
</dt> <dd>

<span data-ttu-id="74210-927">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-927">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-928"><span id="Peer_Name_Resolution_Protocol"></span><span id="peer_name_resolution_protocol"></span><span id="PEER_NAME_RESOLUTION_PROTOCOL"></span>Протокол разрешения имен одноранговых узлов</span><span class="sxs-lookup"><span data-stu-id="74210-928"><span id="Peer_Name_Resolution_Protocol"></span><span id="peer_name_resolution_protocol"></span><span id="PEER_NAME_RESOLUTION_PROTOCOL"></span>Peer Name Resolution Protocol</span></span>
</dt> <dd>

<span data-ttu-id="74210-929">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-929">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-930"><span id="Remote_Server_Administration_Tools"></span><span id="remote_server_administration_tools"></span><span id="REMOTE_SERVER_ADMINISTRATION_TOOLS"></span>средства удаленного администрирования сервера</span><span class="sxs-lookup"><span data-stu-id="74210-930"><span id="Remote_Server_Administration_Tools"></span><span id="remote_server_administration_tools"></span><span id="REMOTE_SERVER_ADMINISTRATION_TOOLS"></span>Remote Server Administration Tools</span></span>
</dt> <dd>

<span data-ttu-id="74210-931">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-931">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-932"><span id="Quality_Windows_Audio_Video_Experience"></span><span id="quality_windows_audio_video_experience"></span><span id="QUALITY_WINDOWS_AUDIO_VIDEO_EXPERIENCE"></span>Качество звука Windows Audio Video</span><span class="sxs-lookup"><span data-stu-id="74210-932"><span id="Quality_Windows_Audio_Video_Experience"></span><span id="quality_windows_audio_video_experience"></span><span id="QUALITY_WINDOWS_AUDIO_VIDEO_EXPERIENCE"></span>Quality Windows Audio Video Experience</span></span>
</dt> <dd>

<span data-ttu-id="74210-933">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-933">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-934"><span id="Group_Policy_Management"></span><span id="group_policy_management"></span><span id="GROUP_POLICY_MANAGEMENT"></span>Управление групповая политика</span><span class="sxs-lookup"><span data-stu-id="74210-934"><span id="Group_Policy_Management"></span><span id="group_policy_management"></span><span id="GROUP_POLICY_MANAGEMENT"></span>Group Policy Management</span></span>
</dt> <dd>

<span data-ttu-id="74210-935">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-935">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-936"><span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Служба индексирования</span><span class="sxs-lookup"><span data-stu-id="74210-936"><span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Indexing Service</span></span>
</dt> <dd>

<span data-ttu-id="74210-937">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-937">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-938"><span id="File_Server_Resource_Manager__FSRM_"></span><span id="file_server_resource_manager__fsrm_"></span><span id="FILE_SERVER_RESOURCE_MANAGER__FSRM_"></span>Диспетчер ресурсов файлового сервера (FSRM)</span><span class="sxs-lookup"><span data-stu-id="74210-938"><span id="File_Server_Resource_Manager__FSRM_"></span><span id="file_server_resource_manager__fsrm_"></span><span id="FILE_SERVER_RESOURCE_MANAGER__FSRM_"></span>File Server Resource Manager (FSRM)</span></span>
</dt> <dd>

<span data-ttu-id="74210-939">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-939">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-940"><span id="Windows_Server_Migration_Tools"></span><span id="windows_server_migration_tools"></span><span id="WINDOWS_SERVER_MIGRATION_TOOLS"></span>средства миграции Windows Server</span><span class="sxs-lookup"><span data-stu-id="74210-940"><span id="Windows_Server_Migration_Tools"></span><span id="windows_server_migration_tools"></span><span id="WINDOWS_SERVER_MIGRATION_TOOLS"></span>Windows Server Migration Tools</span></span>
</dt> <dd>

<span data-ttu-id="74210-941">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-941">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-942"><span id="BranchCache"></span><span id="branchcache"></span><span id="BRANCHCACHE"></span>BranchCache</span><span class="sxs-lookup"><span data-stu-id="74210-942"><span id="BranchCache"></span><span id="branchcache"></span><span id="BRANCHCACHE"></span>BranchCache</span></span>
</dt> <dd>

<span data-ttu-id="74210-943">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-943">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-944"><span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>Консоль управления DirectAccess</span><span class="sxs-lookup"><span data-stu-id="74210-944"><span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>DirectAccess Management Console</span></span>
</dt> <dd>

<span data-ttu-id="74210-945">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-945">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-946"><span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Фоновая интеллектуальная служба передачи (бит)</span><span class="sxs-lookup"><span data-stu-id="74210-946"><span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Background Intelligent Transfer Service (BITS)</span></span>
</dt> <dd>

<span data-ttu-id="74210-947">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-947">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-948"><span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>Поддержка WoW64</span><span class="sxs-lookup"><span data-stu-id="74210-948"><span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>WoW64 Support</span></span>
</dt> <dd>

<span data-ttu-id="74210-949">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-949">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-950"><span id="Window_Server_Update_Services"></span><span id="window_server_update_services"></span><span id="WINDOW_SERVER_UPDATE_SERVICES"></span>Службы обновления Windows Server</span><span class="sxs-lookup"><span data-stu-id="74210-950"><span id="Window_Server_Update_Services"></span><span id="window_server_update_services"></span><span id="WINDOW_SERVER_UPDATE_SERVICES"></span>Window Server Update Services</span></span>
</dt> <dd>

<span data-ttu-id="74210-951">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-951">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-952"><span id="IP_Address_Management__IPAM__Server"></span><span id="ip_address_management__ipam__server"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>Сервер управления IP-адресами (IPAM)</span><span class="sxs-lookup"><span data-stu-id="74210-952"><span id="IP_Address_Management__IPAM__Server"></span><span id="ip_address_management__ipam__server"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>IP Address Management (IPAM) Server</span></span>
</dt> <dd>

<span data-ttu-id="74210-953">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-953">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-954"><span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="74210-954"><span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="74210-955">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-955">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-956"><span id=".NET_Framework_4.5"></span><span id=".net_framework_4.5"></span><span id=".NET_FRAMEWORK_4.5"></span>Платформа .NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="74210-956"><span id=".NET_Framework_4.5"></span><span id=".net_framework_4.5"></span><span id=".NET_FRAMEWORK_4.5"></span>.NET Framework 4.5</span></span>
</dt> <dd>

<span data-ttu-id="74210-957">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-957">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-958"><span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Служба поиска Windows</span><span class="sxs-lookup"><span data-stu-id="74210-958"><span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Windows Search Service</span></span>
</dt> <dd>

<span data-ttu-id="74210-959">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-959">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-960"><span id="Client_for_NFS"></span><span id="client_for_nfs"></span><span id="CLIENT_FOR_NFS"></span>Клиент для NFS</span><span class="sxs-lookup"><span data-stu-id="74210-960"><span id="Client_for_NFS"></span><span id="client_for_nfs"></span><span id="CLIENT_FOR_NFS"></span>Client for NFS</span></span>
</dt> <dd>

<span data-ttu-id="74210-961">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-961">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-962"><span id="BitLocker_Network_Unlock"></span><span id="bitlocker_network_unlock"></span><span id="BITLOCKER_NETWORK_UNLOCK"></span>Сетевая разблокировка BitLocker</span><span class="sxs-lookup"><span data-stu-id="74210-962"><span id="BitLocker_Network_Unlock"></span><span id="bitlocker_network_unlock"></span><span id="BITLOCKER_NETWORK_UNLOCK"></span>BitLocker Network Unlock</span></span>
</dt> <dd>

<span data-ttu-id="74210-963">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-963">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-964"><span id="Management_OData_IIS_Extension"></span><span id="management_odata_iis_extension"></span><span id="MANAGEMENT_ODATA_IIS_EXTENSION"></span>Расширение IIS OData для управления</span><span class="sxs-lookup"><span data-stu-id="74210-964"><span id="Management_OData_IIS_Extension"></span><span id="management_odata_iis_extension"></span><span id="MANAGEMENT_ODATA_IIS_EXTENSION"></span>Management OData IIS Extension</span></span>
</dt> <dd>

<span data-ttu-id="74210-965">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-965">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-966"><span id=".NET_Framework_4.5_Advanced_Services"></span><span id=".net_framework_4.5_advanced_services"></span><span id=".NET_FRAMEWORK_4.5_ADVANCED_SERVICES"></span>Платформа .NET Framework 4,5 дополнительные службы</span><span class="sxs-lookup"><span data-stu-id="74210-966"><span id=".NET_Framework_4.5_Advanced_Services"></span><span id=".net_framework_4.5_advanced_services"></span><span id=".NET_FRAMEWORK_4.5_ADVANCED_SERVICES"></span>.NET Framework 4.5 Advanced Services</span></span>
</dt> <dd>

<span data-ttu-id="74210-967">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-967">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-968"><span id=".NET_Framework_4.5_Features"></span><span id=".net_framework_4.5_features"></span><span id=".NET_FRAMEWORK_4.5_FEATURES"></span>Функции платформа .NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="74210-968"><span id=".NET_Framework_4.5_Features"></span><span id=".net_framework_4.5_features"></span><span id=".NET_FRAMEWORK_4.5_FEATURES"></span>.NET Framework 4.5 Features</span></span>
</dt> <dd>

<span data-ttu-id="74210-969">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-969">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-970"><span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>Пользовательские интерфейсы и инфраструктура</span><span class="sxs-lookup"><span data-stu-id="74210-970"><span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>User Interfaces and Infrastructure</span></span>
</dt> <dd>

<span data-ttu-id="74210-971">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-971">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-972"><span id="Graphical_Management_Tools_and_Infrastructure"></span><span id="graphical_management_tools_and_infrastructure"></span><span id="GRAPHICAL_MANAGEMENT_TOOLS_AND_INFRASTRUCTURE"></span>Графические средства управления и инфраструктура</span><span class="sxs-lookup"><span data-stu-id="74210-972"><span id="Graphical_Management_Tools_and_Infrastructure"></span><span id="graphical_management_tools_and_infrastructure"></span><span id="GRAPHICAL_MANAGEMENT_TOOLS_AND_INFRASTRUCTURE"></span>Graphical Management Tools and Infrastructure</span></span>
</dt> <dd>

<span data-ttu-id="74210-973">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-973">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-974"><span id="File_and_Storage_Services"></span><span id="file_and_storage_services"></span><span id="FILE_AND_STORAGE_SERVICES"></span>Службы файлов и хранилища</span><span class="sxs-lookup"><span data-stu-id="74210-974"><span id="File_and_Storage_Services"></span><span id="file_and_storage_services"></span><span id="FILE_AND_STORAGE_SERVICES"></span>File and Storage Services</span></span>
</dt> <dd>

<span data-ttu-id="74210-975">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-975">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-976"><span id="Windows_Server_Essentials_Experience"></span><span id="windows_server_essentials_experience"></span><span id="WINDOWS_SERVER_ESSENTIALS_EXPERIENCE"></span>Опыт работы с Windows Server Essentials</span><span class="sxs-lookup"><span data-stu-id="74210-976"><span id="Windows_Server_Essentials_Experience"></span><span id="windows_server_essentials_experience"></span><span id="WINDOWS_SERVER_ESSENTIALS_EXPERIENCE"></span>Windows Server Essentials Experience</span></span>
</dt> <dd>

<span data-ttu-id="74210-977">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-977">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-978"><span id="Direct_Play"></span><span id="direct_play"></span><span id="DIRECT_PLAY"></span>Прямое воспроизведение</span><span class="sxs-lookup"><span data-stu-id="74210-978"><span id="Direct_Play"></span><span id="direct_play"></span><span id="DIRECT_PLAY"></span>Direct Play</span></span>
</dt> <dd>

<span data-ttu-id="74210-979">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-979">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-980"><span id="Distributed_File_System"></span><span id="distributed_file_system"></span><span id="DISTRIBUTED_FILE_SYSTEM"></span>распределенная файловая система</span><span class="sxs-lookup"><span data-stu-id="74210-980"><span id="Distributed_File_System"></span><span id="distributed_file_system"></span><span id="DISTRIBUTED_FILE_SYSTEM"></span>Distributed File System</span></span>
</dt> <dd>

<span data-ttu-id="74210-981">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-981">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-982"><span id="File_Server_Resource_Manager"></span><span id="file_server_resource_manager"></span><span id="FILE_SERVER_RESOURCE_MANAGER"></span>диспетчер ресурсов файлового сервера</span><span class="sxs-lookup"><span data-stu-id="74210-982"><span id="File_Server_Resource_Manager"></span><span id="file_server_resource_manager"></span><span id="FILE_SERVER_RESOURCE_MANAGER"></span>File Server Resource Manager</span></span>
</dt> <dd>

<span data-ttu-id="74210-983">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-983">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-984"><span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Службы для сетевой файловой системы</span><span class="sxs-lookup"><span data-stu-id="74210-984"><span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Services For Network File System</span></span>
</dt> <dd>

<span data-ttu-id="74210-985">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-985">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-986"><span id="Single_Instance_Storage"></span><span id="single_instance_storage"></span><span id="SINGLE_INSTANCE_STORAGE"></span>Хранилище единственных экземпляров</span><span class="sxs-lookup"><span data-stu-id="74210-986"><span id="Single_Instance_Storage"></span><span id="single_instance_storage"></span><span id="SINGLE_INSTANCE_STORAGE"></span>Single Instance Storage</span></span>
</dt> <dd>

<span data-ttu-id="74210-987">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-987">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-988"><span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Служба поиска Windows</span><span class="sxs-lookup"><span data-stu-id="74210-988"><span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Windows Search Service</span></span>
</dt> <dd>

<span data-ttu-id="74210-989">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-989">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-990"><span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Служба индексирования</span><span class="sxs-lookup"><span data-stu-id="74210-990"><span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Indexing Service</span></span>
</dt> <dd>

<span data-ttu-id="74210-991">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-991">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-992"><span id="iSCSI_Target_Storage_Provider__VDS_and_VSS_hardware_providers_"></span><span id="iscsi_target_storage_provider__vds_and_vss_hardware_providers_"></span><span id="ISCSI_TARGET_STORAGE_PROVIDER__VDS_AND_VSS_HARDWARE_PROVIDERS_"></span>Поставщик хранилища цели iSCSI (поставщики оборудования VDS и VSS)</span><span class="sxs-lookup"><span data-stu-id="74210-992"><span id="iSCSI_Target_Storage_Provider__VDS_and_VSS_hardware_providers_"></span><span id="iscsi_target_storage_provider__vds_and_vss_hardware_providers_"></span><span id="ISCSI_TARGET_STORAGE_PROVIDER__VDS_AND_VSS_HARDWARE_PROVIDERS_"></span>iSCSI Target Storage Provider (VDS and VSS hardware providers)</span></span>
</dt> <dd>

<span data-ttu-id="74210-993">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-993">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-994"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Рабочие папки</span><span class="sxs-lookup"><span data-stu-id="74210-994"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Work Folders</span></span>
</dt> <dd>

<span data-ttu-id="74210-995">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-995">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-996"><span id="Active_Directory_Domain_Controller"></span><span id="active_directory_domain_controller"></span><span id="ACTIVE_DIRECTORY_DOMAIN_CONTROLLER"></span>Контроллер домен Active Directory</span><span class="sxs-lookup"><span data-stu-id="74210-996"><span id="Active_Directory_Domain_Controller"></span><span id="active_directory_domain_controller"></span><span id="ACTIVE_DIRECTORY_DOMAIN_CONTROLLER"></span>Active Directory Domain Controller</span></span>
</dt> <dd>

<span data-ttu-id="74210-997">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-997">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-998"><span id="Identity_Management_For_Unix"></span><span id="identity_management_for_unix"></span><span id="IDENTITY_MANAGEMENT_FOR_UNIX"></span>Управление удостоверениями для UNIX</span><span class="sxs-lookup"><span data-stu-id="74210-998"><span id="Identity_Management_For_Unix"></span><span id="identity_management_for_unix"></span><span id="IDENTITY_MANAGEMENT_FOR_UNIX"></span>Identity Management For Unix</span></span>
</dt> <dd>

<span data-ttu-id="74210-999">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-999">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1000"><span id="Server_For_Network_Information_Services"></span><span id="server_for_network_information_services"></span><span id="SERVER_FOR_NETWORK_INFORMATION_SERVICES"></span>Сервер для служб сведений о сети</span><span class="sxs-lookup"><span data-stu-id="74210-1000"><span id="Server_For_Network_Information_Services"></span><span id="server_for_network_information_services"></span><span id="SERVER_FOR_NETWORK_INFORMATION_SERVICES"></span>Server For Network Information Services</span></span>
</dt> <dd>

<span data-ttu-id="74210-1001">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1001">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1002"><span id="Password_Synchronization"></span><span id="password_synchronization"></span><span id="PASSWORD_SYNCHRONIZATION"></span>Синхронизация паролей</span><span class="sxs-lookup"><span data-stu-id="74210-1002"><span id="Password_Synchronization"></span><span id="password_synchronization"></span><span id="PASSWORD_SYNCHRONIZATION"></span>Password Synchronization</span></span>
</dt> <dd>

<span data-ttu-id="74210-1003">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1003">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1004"><span id="Administration_Tools"></span><span id="administration_tools"></span><span id="ADMINISTRATION_TOOLS"></span>Средства администрирования</span><span class="sxs-lookup"><span data-stu-id="74210-1004"><span id="Administration_Tools"></span><span id="administration_tools"></span><span id="ADMINISTRATION_TOOLS"></span>Administration Tools</span></span>
</dt> <dd>

<span data-ttu-id="74210-1005">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1005">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1006"><span id="Windows_Media_Server"></span><span id="windows_media_server"></span><span id="WINDOWS_MEDIA_SERVER"></span>Windows Media Server</span><span class="sxs-lookup"><span data-stu-id="74210-1006"><span id="Windows_Media_Server"></span><span id="windows_media_server"></span><span id="WINDOWS_MEDIA_SERVER"></span>Windows Media Server</span></span>
</dt> <dd>

<span data-ttu-id="74210-1007">Больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="74210-1007">No longer supported.</span></span>

</dd> <dt>

<span data-ttu-id="74210-1008"><span id="Web-based_Administration"></span><span id="web-based_administration"></span><span id="WEB-BASED_ADMINISTRATION"></span>Веб-администрирование</span><span class="sxs-lookup"><span data-stu-id="74210-1008"><span id="Web-based_Administration"></span><span id="web-based_administration"></span><span id="WEB-BASED_ADMINISTRATION"></span>Web-based Administration</span></span>
</dt> <dd>

<span data-ttu-id="74210-1009">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1009">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1010"><span id="Logging_Agent"></span><span id="logging_agent"></span><span id="LOGGING_AGENT"></span>Агент ведения журнала</span><span class="sxs-lookup"><span data-stu-id="74210-1010"><span id="Logging_Agent"></span><span id="logging_agent"></span><span id="LOGGING_AGENT"></span>Logging Agent</span></span>
</dt> <dd>

<span data-ttu-id="74210-1011">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1011">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1012"><span id="Federation_Service"></span><span id="federation_service"></span><span id="FEDERATION_SERVICE"></span>служба федерации</span><span class="sxs-lookup"><span data-stu-id="74210-1012"><span id="Federation_Service"></span><span id="federation_service"></span><span id="FEDERATION_SERVICE"></span>Federation Service</span></span>
</dt> <dd>

<span data-ttu-id="74210-1013">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1013">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1014"><span id="Federation_Service_Policy"></span><span id="federation_service_policy"></span><span id="FEDERATION_SERVICE_POLICY"></span>Политика служба федерации</span><span class="sxs-lookup"><span data-stu-id="74210-1014"><span id="Federation_Service_Policy"></span><span id="federation_service_policy"></span><span id="FEDERATION_SERVICE_POLICY"></span>Federation Service Policy</span></span>
</dt> <dd>

<span data-ttu-id="74210-1015">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1015">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1016"><span id="AD_FS_Web_Agents"></span><span id="ad_fs_web_agents"></span><span id="AD_FS_WEB_AGENTS"></span>Веб-агенты AD FS</span><span class="sxs-lookup"><span data-stu-id="74210-1016"><span id="AD_FS_Web_Agents"></span><span id="ad_fs_web_agents"></span><span id="AD_FS_WEB_AGENTS"></span>AD FS Web Agents</span></span>
</dt> <dd>

<span data-ttu-id="74210-1017">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1017">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1018"><span id="Windows_Token-based_Agent"></span><span id="windows_token-based_agent"></span><span id="WINDOWS_TOKEN-BASED_AGENT"></span>Агент Windows на основе токенов</span><span class="sxs-lookup"><span data-stu-id="74210-1018"><span id="Windows_Token-based_Agent"></span><span id="windows_token-based_agent"></span><span id="WINDOWS_TOKEN-BASED_AGENT"></span>Windows Token-based Agent</span></span>
</dt> <dd>

<span data-ttu-id="74210-1019">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1019">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1020"><span id="Remote_Desktop_Licensing"></span><span id="remote_desktop_licensing"></span><span id="REMOTE_DESKTOP_LICENSING"></span>Лицензирование удаленный рабочий стол</span><span class="sxs-lookup"><span data-stu-id="74210-1020"><span id="Remote_Desktop_Licensing"></span><span id="remote_desktop_licensing"></span><span id="REMOTE_DESKTOP_LICENSING"></span>Remote Desktop Licensing</span></span>
</dt> <dd>

<span data-ttu-id="74210-1021">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1021">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1022"><span id="Network_Policy_Server"></span><span id="network_policy_server"></span><span id="NETWORK_POLICY_SERVER"></span>Сервер политики сети</span><span class="sxs-lookup"><span data-stu-id="74210-1022"><span id="Network_Policy_Server"></span><span id="network_policy_server"></span><span id="NETWORK_POLICY_SERVER"></span>Network Policy Server</span></span>
</dt> <dd>

<span data-ttu-id="74210-1023">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1023">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1024"><span id="VPN"></span><span id="vpn"></span>ЧЕРЕЗ</span><span class="sxs-lookup"><span data-stu-id="74210-1024"><span id="VPN"></span><span id="vpn"></span>VPN</span></span>
</dt> <dd>

<span data-ttu-id="74210-1025">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1025">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1026"><span id="Remote_Access_Services"></span><span id="remote_access_services"></span><span id="REMOTE_ACCESS_SERVICES"></span>Службы удаленного доступа</span><span class="sxs-lookup"><span data-stu-id="74210-1026"><span id="Remote_Access_Services"></span><span id="remote_access_services"></span><span id="REMOTE_ACCESS_SERVICES"></span>Remote Access Services</span></span>
</dt> <dd>

<span data-ttu-id="74210-1027">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1027">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1028"><span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Маршруты</span><span class="sxs-lookup"><span data-stu-id="74210-1028"><span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Routing</span></span>
</dt> <dd>

<span data-ttu-id="74210-1029">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1029">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1030"><span id="Health_Registration_Authority"></span><span id="health_registration_authority"></span><span id="HEALTH_REGISTRATION_AUTHORITY"></span>Центр регистрации работоспособности</span><span class="sxs-lookup"><span data-stu-id="74210-1030"><span id="Health_Registration_Authority"></span><span id="health_registration_authority"></span><span id="HEALTH_REGISTRATION_AUTHORITY"></span>Health Registration Authority</span></span>
</dt> <dd>

<span data-ttu-id="74210-1031">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1031">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1032"><span id="Host_Credential_Authorization_Protocol"></span><span id="host_credential_authorization_protocol"></span><span id="HOST_CREDENTIAL_AUTHORIZATION_PROTOCOL"></span>Протокол авторизации учетных данных узла</span><span class="sxs-lookup"><span data-stu-id="74210-1032"><span id="Host_Credential_Authorization_Protocol"></span><span id="host_credential_authorization_protocol"></span><span id="HOST_CREDENTIAL_AUTHORIZATION_PROTOCOL"></span>Host Credential Authorization Protocol</span></span>
</dt> <dd>

<span data-ttu-id="74210-1033">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1033">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1034"><span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>Платформа .NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="74210-1034"><span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1</span></span>
</dt> <dd>

<span data-ttu-id="74210-1035">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1035">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1036"><span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>Средство просмотра XPS</span><span class="sxs-lookup"><span data-stu-id="74210-1036"><span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>XPS Viewer</span></span>
</dt> <dd>

<span data-ttu-id="74210-1037">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1037">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1038"><span id="SNMP_Service"></span><span id="snmp_service"></span><span id="SNMP_SERVICE"></span>Служба SNMP</span><span class="sxs-lookup"><span data-stu-id="74210-1038"><span id="SNMP_Service"></span><span id="snmp_service"></span><span id="SNMP_SERVICE"></span>SNMP Service</span></span>
</dt> <dd>

<span data-ttu-id="74210-1039">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1039">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1040"><span id="SNMP_WMI_Provider"></span><span id="snmp_wmi_provider"></span><span id="SNMP_WMI_PROVIDER"></span>Поставщик WMI SNMP</span><span class="sxs-lookup"><span data-stu-id="74210-1040"><span id="SNMP_WMI_Provider"></span><span id="snmp_wmi_provider"></span><span id="SNMP_WMI_PROVIDER"></span>SNMP WMI Provider</span></span>
</dt> <dd>

<span data-ttu-id="74210-1041">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1041">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1042"><span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>Платформа .NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="74210-1042"><span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1</span></span>
</dt> <dd>

<span data-ttu-id="74210-1043">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1043">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1044"><span id="Web_Server__IIS__Support"></span><span id="web_server__iis__support"></span><span id="WEB_SERVER__IIS__SUPPORT"></span>Поддержка веб-сервера (IIS)</span><span class="sxs-lookup"><span data-stu-id="74210-1044"><span id="Web_Server__IIS__Support"></span><span id="web_server__iis__support"></span><span id="WEB_SERVER__IIS__SUPPORT"></span>Web Server (IIS) Support</span></span>
</dt> <dd>

<span data-ttu-id="74210-1045">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1045">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1046"><span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>Доступ к сети COM+</span><span class="sxs-lookup"><span data-stu-id="74210-1046"><span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>COM+ Network Access</span></span>
</dt> <dd>

<span data-ttu-id="74210-1047">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1047">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1048"><span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>Совместное использование TCP-портов</span><span class="sxs-lookup"><span data-stu-id="74210-1048"><span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>TCP Port Sharing</span></span>
</dt> <dd>

<span data-ttu-id="74210-1049">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1049">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1050"><span id="Windows_Process_Activation_Service_Support"></span><span id="windows_process_activation_service_support"></span><span id="WINDOWS_PROCESS_ACTIVATION_SERVICE_SUPPORT"></span>Поддержка службы активации процессов Windows</span><span class="sxs-lookup"><span data-stu-id="74210-1050"><span id="Windows_Process_Activation_Service_Support"></span><span id="windows_process_activation_service_support"></span><span id="WINDOWS_PROCESS_ACTIVATION_SERVICE_SUPPORT"></span>Windows Process Activation Service Support</span></span>
</dt> <dd>

<span data-ttu-id="74210-1051">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1051">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1052"><span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>Активация по HTTP</span><span class="sxs-lookup"><span data-stu-id="74210-1052"><span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>HTTP Activation</span></span>
</dt> <dd>

<span data-ttu-id="74210-1053">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1053">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1054"><span id="Message_Queuing_Activation"></span><span id="message_queuing_activation"></span><span id="MESSAGE_QUEUING_ACTIVATION"></span>Активация службы очередей сообщений</span><span class="sxs-lookup"><span data-stu-id="74210-1054"><span id="Message_Queuing_Activation"></span><span id="message_queuing_activation"></span><span id="MESSAGE_QUEUING_ACTIVATION"></span>Message Queuing Activation</span></span>
</dt> <dd>

<span data-ttu-id="74210-1055">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1055">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1056"><span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>Активация по TCP</span><span class="sxs-lookup"><span data-stu-id="74210-1056"><span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>TCP Activation</span></span>
</dt> <dd>

<span data-ttu-id="74210-1057">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1057">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1058"><span id="Named_Pipes_Activation"></span><span id="named_pipes_activation"></span><span id="NAMED_PIPES_ACTIVATION"></span>Активация по именованным каналам</span><span class="sxs-lookup"><span data-stu-id="74210-1058"><span id="Named_Pipes_Activation"></span><span id="named_pipes_activation"></span><span id="NAMED_PIPES_ACTIVATION"></span>Named Pipes Activation</span></span>
</dt> <dd>

<span data-ttu-id="74210-1059">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1059">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1060"><span id="Distributed_Transactions"></span><span id="distributed_transactions"></span><span id="DISTRIBUTED_TRANSACTIONS"></span>Распределенные транзакции</span><span class="sxs-lookup"><span data-stu-id="74210-1060"><span id="Distributed_Transactions"></span><span id="distributed_transactions"></span><span id="DISTRIBUTED_TRANSACTIONS"></span>Distributed Transactions</span></span>
</dt> <dd>

<span data-ttu-id="74210-1061">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1061">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1062"><span id="Incoming_Remote_Transactions"></span><span id="incoming_remote_transactions"></span><span id="INCOMING_REMOTE_TRANSACTIONS"></span>Входящие удаленные транзакции</span><span class="sxs-lookup"><span data-stu-id="74210-1062"><span id="Incoming_Remote_Transactions"></span><span id="incoming_remote_transactions"></span><span id="INCOMING_REMOTE_TRANSACTIONS"></span>Incoming Remote Transactions</span></span>
</dt> <dd>

<span data-ttu-id="74210-1063">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1063">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1064"><span id="Outgoing_Remote_Transactions"></span><span id="outgoing_remote_transactions"></span><span id="OUTGOING_REMOTE_TRANSACTIONS"></span>Исходящие удаленные транзакции</span><span class="sxs-lookup"><span data-stu-id="74210-1064"><span id="Outgoing_Remote_Transactions"></span><span id="outgoing_remote_transactions"></span><span id="OUTGOING_REMOTE_TRANSACTIONS"></span>Outgoing Remote Transactions</span></span>
</dt> <dd>

<span data-ttu-id="74210-1065">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1065">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1066"><span id="WS-Automatic_Transactions"></span><span id="ws-automatic_transactions"></span><span id="WS-AUTOMATIC_TRANSACTIONS"></span>WS-автоматические транзакции</span><span class="sxs-lookup"><span data-stu-id="74210-1066"><span id="WS-Automatic_Transactions"></span><span id="ws-automatic_transactions"></span><span id="WS-AUTOMATIC_TRANSACTIONS"></span>WS-Automatic Transactions</span></span>
</dt> <dd>

<span data-ttu-id="74210-1067">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1067">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1068"><span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Расширения сервера приложений для .NET 4,0</span><span class="sxs-lookup"><span data-stu-id="74210-1068"><span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Application Server Extensions for .NET 4.0</span></span>
</dt> <dd>

<span data-ttu-id="74210-1069">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1069">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1070"><span id="Role_Administration_Tools"></span><span id="role_administration_tools"></span><span id="ROLE_ADMINISTRATION_TOOLS"></span>Средства администрирования ролей</span><span class="sxs-lookup"><span data-stu-id="74210-1070"><span id="Role_Administration_Tools"></span><span id="role_administration_tools"></span><span id="ROLE_ADMINISTRATION_TOOLS"></span>Role Administration Tools</span></span>
</dt> <dd>

<span data-ttu-id="74210-1071">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1071">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1072"><span id="AD_DS_Tools"></span><span id="ad_ds_tools"></span><span id="AD_DS_TOOLS"></span>Средства AD DS</span><span class="sxs-lookup"><span data-stu-id="74210-1072"><span id="AD_DS_Tools"></span><span id="ad_ds_tools"></span><span id="AD_DS_TOOLS"></span>AD DS Tools</span></span>
</dt> <dd>

<span data-ttu-id="74210-1073">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1073">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1074"><span id="AD_LDS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_lds_snap-ins_and_command-line_tools"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>Средства Snap-Ins и Command-Line AD LDS</span><span class="sxs-lookup"><span data-stu-id="74210-1074"><span id="AD_LDS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_lds_snap-ins_and_command-line_tools"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>AD LDS Snap-Ins and Command-Line Tools</span></span>
</dt> <dd>

<span data-ttu-id="74210-1075">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1075">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1076"><span id="Network_Policy_and_Access_Services"></span><span id="network_policy_and_access_services"></span><span id="NETWORK_POLICY_AND_ACCESS_SERVICES"></span>Службы политики сети и доступа</span><span class="sxs-lookup"><span data-stu-id="74210-1076"><span id="Network_Policy_and_Access_Services"></span><span id="network_policy_and_access_services"></span><span id="NETWORK_POLICY_AND_ACCESS_SERVICES"></span>Network Policy and Access Services</span></span>
</dt> <dd>

<span data-ttu-id="74210-1077">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1077">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1078"><span id="Active_Directory_Rights_Management_Services"></span><span id="active_directory_rights_management_services"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES"></span>службы Active Directory Rights Management</span><span class="sxs-lookup"><span data-stu-id="74210-1078"><span id="Active_Directory_Rights_Management_Services"></span><span id="active_directory_rights_management_services"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES"></span>Active Directory Rights Management Services</span></span>
</dt> <dd>

<span data-ttu-id="74210-1079">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1079">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1080"><span id="Remote_Desktop_Services_Tools"></span><span id="remote_desktop_services_tools"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS"></span>Средства службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="74210-1080"><span id="Remote_Desktop_Services_Tools"></span><span id="remote_desktop_services_tools"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS"></span>Remote Desktop Services Tools</span></span>
</dt> <dd>

<span data-ttu-id="74210-1081">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1081">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1082"><span id="Feature_Administration_Tools"></span><span id="feature_administration_tools"></span><span id="FEATURE_ADMINISTRATION_TOOLS"></span>Средства администрирования компонентов</span><span class="sxs-lookup"><span data-stu-id="74210-1082"><span id="Feature_Administration_Tools"></span><span id="feature_administration_tools"></span><span id="FEATURE_ADMINISTRATION_TOOLS"></span>Feature Administration Tools</span></span>
</dt> <dd>

<span data-ttu-id="74210-1083">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1083">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1084"><span id="Failover_Clustering_Tools"></span><span id="failover_clustering_tools"></span><span id="FAILOVER_CLUSTERING_TOOLS"></span>Средства отказоустойчивой кластеризации</span><span class="sxs-lookup"><span data-stu-id="74210-1084"><span id="Failover_Clustering_Tools"></span><span id="failover_clustering_tools"></span><span id="FAILOVER_CLUSTERING_TOOLS"></span>Failover Clustering Tools</span></span>
</dt> <dd>

<span data-ttu-id="74210-1085">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1085">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1086"><span id="DNS_Server_Tools"></span><span id="dns_server_tools"></span><span id="DNS_SERVER_TOOLS"></span>Средства DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="74210-1086"><span id="DNS_Server_Tools"></span><span id="dns_server_tools"></span><span id="DNS_SERVER_TOOLS"></span>DNS Server Tools</span></span>
</dt> <dd>

<span data-ttu-id="74210-1087">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1087">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1088"><span id="Services_For_Network_File_System_Tools"></span><span id="services_for_network_file_system_tools"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM_TOOLS"></span>Службы для средств сетевой файловой системы</span><span class="sxs-lookup"><span data-stu-id="74210-1088"><span id="Services_For_Network_File_System_Tools"></span><span id="services_for_network_file_system_tools"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM_TOOLS"></span>Services For Network File System Tools</span></span>
</dt> <dd>

<span data-ttu-id="74210-1089">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1089">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1090"><span id="Web_Server__IIS__Tools"></span><span id="web_server__iis__tools"></span><span id="WEB_SERVER__IIS__TOOLS"></span>Средства веб-сервера (IIS)</span><span class="sxs-lookup"><span data-stu-id="74210-1090"><span id="Web_Server__IIS__Tools"></span><span id="web_server__iis__tools"></span><span id="WEB_SERVER__IIS__TOOLS"></span>Web Server (IIS) Tools</span></span>
</dt> <dd>

<span data-ttu-id="74210-1091">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1091">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1092"><span id="Server_for_NIS_Tools"></span><span id="server_for_nis_tools"></span><span id="SERVER_FOR_NIS_TOOLS"></span>Средства сервера для NIS</span><span class="sxs-lookup"><span data-stu-id="74210-1092"><span id="Server_for_NIS_Tools"></span><span id="server_for_nis_tools"></span><span id="SERVER_FOR_NIS_TOOLS"></span>Server for NIS Tools</span></span>
</dt> <dd>

<span data-ttu-id="74210-1093">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1093">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1094"><span id="AD_DS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_ds_snap-ins_and_command-line_tools"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>Средства Snap-Ins и Command-Line AD DS</span><span class="sxs-lookup"><span data-stu-id="74210-1094"><span id="AD_DS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_ds_snap-ins_and_command-line_tools"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>AD DS Snap-Ins and Command-Line Tools</span></span>
</dt> <dd>

<span data-ttu-id="74210-1095">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1095">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1096"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>Средства AD DS и AD LDS</span><span class="sxs-lookup"><span data-stu-id="74210-1096"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS and AD LDS Tools</span></span>
</dt> <dd>

<span data-ttu-id="74210-1097">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1097">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1098"><span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Средства брокера подключение к удаленному рабочему столу</span><span class="sxs-lookup"><span data-stu-id="74210-1098"><span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Remote Desktop Connection Broker Tools</span></span>
</dt> <dd>

<span data-ttu-id="74210-1099">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1099">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1100"><span id="IP_Address_Management__IPAM__Client"></span><span id="ip_address_management__ipam__client"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__CLIENT"></span>Клиент управления IP-адресами (IPAM)</span><span class="sxs-lookup"><span data-stu-id="74210-1100"><span id="IP_Address_Management__IPAM__Client"></span><span id="ip_address_management__ipam__client"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__CLIENT"></span>IP Address Management (IPAM) Client</span></span>
</dt> <dd>

<span data-ttu-id="74210-1101">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1101">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1102"><span id="Hyper-V_Module_for_Windows_PowerShell"></span><span id="hyper-v_module_for_windows_powershell"></span><span id="HYPER-V_MODULE_FOR_WINDOWS_POWERSHELL"></span>Модуль Hyper-V для Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="74210-1102"><span id="Hyper-V_Module_for_Windows_PowerShell"></span><span id="hyper-v_module_for_windows_powershell"></span><span id="HYPER-V_MODULE_FOR_WINDOWS_POWERSHELL"></span>Hyper-V Module for Windows PowerShell</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="74210-1103"><span id="Active_Directory_Rights_Management_Services_Tool"></span><span id="active_directory_rights_management_services_tool"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOL"></span>Инструмент службы Active Directory Rights Management</span><span class="sxs-lookup"><span data-stu-id="74210-1103"><span id="Active_Directory_Rights_Management_Services_Tool"></span><span id="active_directory_rights_management_services_tool"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOL"></span>Active Directory Rights Management Services Tool</span></span>
</dt> <dd>

<span data-ttu-id="74210-1104">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1104">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1105"><span id="Share_and_Storage_Management_Tool"></span><span id="share_and_storage_management_tool"></span><span id="SHARE_AND_STORAGE_MANAGEMENT_TOOL"></span>Средство управления общими ресурсами и хранилищами</span><span class="sxs-lookup"><span data-stu-id="74210-1105"><span id="Share_and_Storage_Management_Tool"></span><span id="share_and_storage_management_tool"></span><span id="SHARE_AND_STORAGE_MANAGEMENT_TOOL"></span>Share and Storage Management Tool</span></span>
</dt> <dd>

<span data-ttu-id="74210-1106">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1106">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1107"><span id="Remote_Access_Management_Tools"></span><span id="remote_access_management_tools"></span><span id="REMOTE_ACCESS_MANAGEMENT_TOOLS"></span>Средства управления удаленным доступом</span><span class="sxs-lookup"><span data-stu-id="74210-1107"><span id="Remote_Access_Management_Tools"></span><span id="remote_access_management_tools"></span><span id="REMOTE_ACCESS_MANAGEMENT_TOOLS"></span>Remote Access Management Tools</span></span>
</dt> <dd>

<span data-ttu-id="74210-1108">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1108">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1109"><span id="Remote_Access_module_for_Windows_PowerShell"></span><span id="remote_access_module_for_windows_powershell"></span><span id="REMOTE_ACCESS_MODULE_FOR_WINDOWS_POWERSHELL"></span>Модуль удаленного доступа для Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="74210-1109"><span id="Remote_Access_module_for_Windows_PowerShell"></span><span id="remote_access_module_for_windows_powershell"></span><span id="REMOTE_ACCESS_MODULE_FOR_WINDOWS_POWERSHELL"></span>Remote Access module for Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="74210-1110">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1110">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1111"><span id="Remote_Access_GUI_and_Command-Line_Tools"></span><span id="remote_access_gui_and_command-line_tools"></span><span id="REMOTE_ACCESS_GUI_AND_COMMAND-LINE_TOOLS"></span>Графический интерфейс удаленного доступа и средства Command-Line</span><span class="sxs-lookup"><span data-stu-id="74210-1111"><span id="Remote_Access_GUI_and_Command-Line_Tools"></span><span id="remote_access_gui_and_command-line_tools"></span><span id="REMOTE_ACCESS_GUI_AND_COMMAND-LINE_TOOLS"></span>Remote Access GUI and Command-Line Tools</span></span>
</dt> <dd>

<span data-ttu-id="74210-1112">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1112">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1113"><span id="Windows_Server_Update_Services_Tools"></span><span id="windows_server_update_services_tools"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES_TOOLS"></span>Средства Windows Server Update Services</span><span class="sxs-lookup"><span data-stu-id="74210-1113"><span id="Windows_Server_Update_Services_Tools"></span><span id="windows_server_update_services_tools"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES_TOOLS"></span>Windows Server Update Services Tools</span></span>
</dt> <dd>

<span data-ttu-id="74210-1114">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1114">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1115"><span id="Remote_Desktop_Licensing_Diagnoser_Tools"></span><span id="remote_desktop_licensing_diagnoser_tools"></span><span id="REMOTE_DESKTOP_LICENSING_DIAGNOSER_TOOLS"></span>Средства диагностики лицензирования удаленный рабочий стол</span><span class="sxs-lookup"><span data-stu-id="74210-1115"><span id="Remote_Desktop_Licensing_Diagnoser_Tools"></span><span id="remote_desktop_licensing_diagnoser_tools"></span><span id="REMOTE_DESKTOP_LICENSING_DIAGNOSER_TOOLS"></span>Remote Desktop Licensing Diagnoser Tools</span></span>
</dt> <dd>

<span data-ttu-id="74210-1116">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1116">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1117"><span id="SNMP_Tools"></span><span id="snmp_tools"></span><span id="SNMP_TOOLS"></span>Средства SNMP</span><span class="sxs-lookup"><span data-stu-id="74210-1117"><span id="SNMP_Tools"></span><span id="snmp_tools"></span><span id="SNMP_TOOLS"></span>SNMP Tools</span></span>
</dt> <dd>

<span data-ttu-id="74210-1118">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1118">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1119"><span id="Volume_Activation_Tools"></span><span id="volume_activation_tools"></span><span id="VOLUME_ACTIVATION_TOOLS"></span>Средства многопользовательской активации</span><span class="sxs-lookup"><span data-stu-id="74210-1119"><span id="Volume_Activation_Tools"></span><span id="volume_activation_tools"></span><span id="VOLUME_ACTIVATION_TOOLS"></span>Volume Activation Tools</span></span>
</dt> <dd>

<span data-ttu-id="74210-1120">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1120">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1121"><span id="Windows_Server_Backup"></span><span id="windows_server_backup"></span><span id="WINDOWS_SERVER_BACKUP"></span>cистема архивации данных Windows Server</span><span class="sxs-lookup"><span data-stu-id="74210-1121"><span id="Windows_Server_Backup"></span><span id="windows_server_backup"></span><span id="WINDOWS_SERVER_BACKUP"></span>Windows Server Backup</span></span>
</dt> <dd>

<span data-ttu-id="74210-1122">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1122">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1123"><span id="Command_Line_Tools"></span><span id="command_line_tools"></span><span id="COMMAND_LINE_TOOLS"></span>Программы командной строки</span><span class="sxs-lookup"><span data-stu-id="74210-1123"><span id="Command_Line_Tools"></span><span id="command_line_tools"></span><span id="COMMAND_LINE_TOOLS"></span>Command Line Tools</span></span>
</dt> <dd>

<span data-ttu-id="74210-1124">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1124">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1125"><span id="Ink_Support"></span><span id="ink_support"></span><span id="INK_SUPPORT"></span>Поддержка рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="74210-1125"><span id="Ink_Support"></span><span id="ink_support"></span><span id="INK_SUPPORT"></span>Ink Support</span></span>
</dt> <dd>

<span data-ttu-id="74210-1126">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1126">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1127"><span id="Handwriting_Recognition"></span><span id="handwriting_recognition"></span><span id="HANDWRITING_RECOGNITION"></span>Распознавание рукописного текста</span><span class="sxs-lookup"><span data-stu-id="74210-1127"><span id="Handwriting_Recognition"></span><span id="handwriting_recognition"></span><span id="HANDWRITING_RECOGNITION"></span>Handwriting Recognition</span></span>
</dt> <dd>

<span data-ttu-id="74210-1128">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1128">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1129"><span id="Compact_Server"></span><span id="compact_server"></span><span id="COMPACT_SERVER"></span>Сервер Compact</span><span class="sxs-lookup"><span data-stu-id="74210-1129"><span id="Compact_Server"></span><span id="compact_server"></span><span id="COMPACT_SERVER"></span>Compact Server</span></span>
</dt> <dd>

<span data-ttu-id="74210-1130">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1130">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1131"><span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64</span><span class="sxs-lookup"><span data-stu-id="74210-1131"><span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64</span></span>
</dt> <dd>

<span data-ttu-id="74210-1132">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1132">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1133"><span id="WoW64_for_.NET_Framework_2.0_and___________"></span><span id="wow64_for_.net_framework_2.0_and___________"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND___________"></span>Подсистема WoW64 для платформа .NET Framework 2,0 и PowerShell</span><span class="sxs-lookup"><span data-stu-id="74210-1133"><span id="WoW64_for_.NET_Framework_2.0_and___________"></span><span id="wow64_for_.net_framework_2.0_and___________"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND___________"></span>WoW64 for .NET Framework 2.0 and PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="74210-1134">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1134">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1135"><span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>Подсистема WoW64 для платформа .NET Framework 2,0</span><span class="sxs-lookup"><span data-stu-id="74210-1135"><span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 for .NET Framework 2.0</span></span>
</dt> <dd>

<span data-ttu-id="74210-1136">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1136">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1137"><span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>Подсистема WoW64 для PowerShell</span><span class="sxs-lookup"><span data-stu-id="74210-1137"><span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 for PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="74210-1138">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1138">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1139"><span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>Подсистема WoW64 для платформа .NET Framework 3,0 и 3,5</span><span class="sxs-lookup"><span data-stu-id="74210-1139"><span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 for .NET Framework 3.0 and 3.5</span></span>
</dt> <dd>

<span data-ttu-id="74210-1140">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1140">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1141"><span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>Подсистема WoW64 для служб печати</span><span class="sxs-lookup"><span data-stu-id="74210-1141"><span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 for Print Services</span></span>
</dt> <dd>

<span data-ttu-id="74210-1142">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1142">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1143"><span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>Подсистема WoW64 для отказоустойчивой кластеризации</span><span class="sxs-lookup"><span data-stu-id="74210-1143"><span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 for Failover Clustering</span></span>
</dt> <dd>

<span data-ttu-id="74210-1144">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1144">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1145"><span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>Подсистема WoW64 для редактора метода ввода</span><span class="sxs-lookup"><span data-stu-id="74210-1145"><span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 for Input Method Editor</span></span>
</dt> <dd>

<span data-ttu-id="74210-1146">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1146">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1147"><span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>Подсистема WoW64 для приложений на основе UNIX</span><span class="sxs-lookup"><span data-stu-id="74210-1147"><span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 for Subsystem for UNIX-based Applications</span></span>
</dt> <dd>

<span data-ttu-id="74210-1148">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1148">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1149"><span id="Desktop_Experience"></span><span id="desktop_experience"></span><span id="DESKTOP_EXPERIENCE"></span>Возможности рабочего стола</span><span class="sxs-lookup"><span data-stu-id="74210-1149"><span id="Desktop_Experience"></span><span id="desktop_experience"></span><span id="DESKTOP_EXPERIENCE"></span>Desktop Experience</span></span>
</dt> <dd>

<span data-ttu-id="74210-1150">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1150">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1151"><span id="Server_Graphical_Shell"></span><span id="server_graphical_shell"></span><span id="SERVER_GRAPHICAL_SHELL"></span>Графическая оболочка сервера</span><span class="sxs-lookup"><span data-stu-id="74210-1151"><span id="Server_Graphical_Shell"></span><span id="server_graphical_shell"></span><span id="SERVER_GRAPHICAL_SHELL"></span>Server Graphical Shell</span></span>
</dt> <dd>

<span data-ttu-id="74210-1152">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1152">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1153"><span id="API_and_PowerShell_cmdlets"></span><span id="api_and_powershell_cmdlets"></span><span id="API_AND_POWERSHELL_CMDLETS"></span>API и командлеты PowerShell</span><span class="sxs-lookup"><span data-stu-id="74210-1153"><span id="API_and_PowerShell_cmdlets"></span><span id="api_and_powershell_cmdlets"></span><span id="API_AND_POWERSHELL_CMDLETS"></span>API and PowerShell cmdlets</span></span>
</dt> <dd>

<span data-ttu-id="74210-1154">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1154">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1155"><span id="SQL_Server_Connectivity"></span><span id="sql_server_connectivity"></span><span id="SQL_SERVER_CONNECTIVITY"></span>Подключение SQL Server</span><span class="sxs-lookup"><span data-stu-id="74210-1155"><span id="SQL_Server_Connectivity"></span><span id="sql_server_connectivity"></span><span id="SQL_SERVER_CONNECTIVITY"></span>SQL Server Connectivity</span></span>
</dt> <dd>

<span data-ttu-id="74210-1156">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1156">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1157"><span id="WSUS_Services"></span><span id="wsus_services"></span><span id="WSUS_SERVICES"></span>Службы WSUS</span><span class="sxs-lookup"><span data-stu-id="74210-1157"><span id="WSUS_Services"></span><span id="wsus_services"></span><span id="WSUS_SERVICES"></span>WSUS Services</span></span>
</dt> <dd>

<span data-ttu-id="74210-1158">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1158">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1159"><span id="User_Interface_Management_Console"></span><span id="user_interface_management_console"></span><span id="USER_INTERFACE_MANAGEMENT_CONSOLE"></span>Консоль управления пользовательским интерфейсом</span><span class="sxs-lookup"><span data-stu-id="74210-1159"><span id="User_Interface_Management_Console"></span><span id="user_interface_management_console"></span><span id="USER_INTERFACE_MANAGEMENT_CONSOLE"></span>User Interface Management Console</span></span>
</dt> <dd>

<span data-ttu-id="74210-1160">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1160">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1161"><span id="WID_Connectivity"></span><span id="wid_connectivity"></span><span id="WID_CONNECTIVITY"></span>Подключение WID</span><span class="sxs-lookup"><span data-stu-id="74210-1161"><span id="WID_Connectivity"></span><span id="wid_connectivity"></span><span id="WID_CONNECTIVITY"></span>WID Connectivity</span></span>
</dt> <dd>

<span data-ttu-id="74210-1162">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1162">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1163"><span id="Windows_PowerShell_2.0_Engine"></span><span id="windows_powershell_2.0_engine"></span><span id="WINDOWS_POWERSHELL_2.0_ENGINE"></span>Подсистема Windows PowerShell 2,0</span><span class="sxs-lookup"><span data-stu-id="74210-1163"><span id="Windows_PowerShell_2.0_Engine"></span><span id="windows_powershell_2.0_engine"></span><span id="WINDOWS_POWERSHELL_2.0_ENGINE"></span>Windows PowerShell 2.0 Engine</span></span>
</dt> <dd>

<span data-ttu-id="74210-1164">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1164">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1165"><span id="Windows_PowerShell_3.0"></span><span id="windows_powershell_3.0"></span><span id="WINDOWS_POWERSHELL_3.0"></span>Windows PowerShell 3,0</span><span class="sxs-lookup"><span data-stu-id="74210-1165"><span id="Windows_PowerShell_3.0"></span><span id="windows_powershell_3.0"></span><span id="WINDOWS_POWERSHELL_3.0"></span>Windows PowerShell 3.0</span></span>
</dt> <dd>

<span data-ttu-id="74210-1166">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1166">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1167"><span id="Windows_PowerShell_Web_Access"></span><span id="windows_powershell_web_access"></span><span id="WINDOWS_POWERSHELL_WEB_ACCESS"></span>Веб-доступ Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="74210-1167"><span id="Windows_PowerShell_Web_Access"></span><span id="windows_powershell_web_access"></span><span id="WINDOWS_POWERSHELL_WEB_ACCESS"></span>Windows PowerShell Web Access</span></span>
</dt> <dd>

<span data-ttu-id="74210-1168">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1168">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1169"><span id="Windows_PowerShell_Desired_State_Configuration_Service"></span><span id="windows_powershell_desired_state_configuration_service"></span><span id="WINDOWS_POWERSHELL_DESIRED_STATE_CONFIGURATION_SERVICE"></span>Служба настройки требуемого состояния Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="74210-1169"><span id="Windows_PowerShell_Desired_State_Configuration_Service"></span><span id="windows_powershell_desired_state_configuration_service"></span><span id="WINDOWS_POWERSHELL_DESIRED_STATE_CONFIGURATION_SERVICE"></span>Windows PowerShell Desired State Configuration Service</span></span>
</dt> <dd>

<span data-ttu-id="74210-1170">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1170">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1171"><span id=".NET_Framework_4.5_Extended"></span><span id=".net_framework_4.5_extended"></span><span id=".NET_FRAMEWORK_4.5_EXTENDED"></span>Расширенная платформа .NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="74210-1171"><span id=".NET_Framework_4.5_Extended"></span><span id=".net_framework_4.5_extended"></span><span id=".NET_FRAMEWORK_4.5_EXTENDED"></span>.NET Framework 4.5 Extended</span></span>
</dt> <dd>

<span data-ttu-id="74210-1172">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1172">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1173"><span id="WCF_Services"></span><span id="wcf_services"></span><span id="WCF_SERVICES"></span>Службы WCF</span><span class="sxs-lookup"><span data-stu-id="74210-1173"><span id="WCF_Services"></span><span id="wcf_services"></span><span id="WCF_SERVICES"></span>WCF Services</span></span>
</dt> <dd>

<span data-ttu-id="74210-1174">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1174">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1175"><span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>Активация по HTTP</span><span class="sxs-lookup"><span data-stu-id="74210-1175"><span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>HTTP Activation</span></span>
</dt> <dd>

<span data-ttu-id="74210-1176">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1176">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1177"><span id="Message_Queuing__MSMQ__Activation"></span><span id="message_queuing__msmq__activation"></span><span id="MESSAGE_QUEUING__MSMQ__ACTIVATION"></span>Активация очереди сообщений (MSMQ)</span><span class="sxs-lookup"><span data-stu-id="74210-1177"><span id="Message_Queuing__MSMQ__Activation"></span><span id="message_queuing__msmq__activation"></span><span id="MESSAGE_QUEUING__MSMQ__ACTIVATION"></span>Message Queuing (MSMQ) Activation</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="74210-1178"><span id="Named_Pipe_Activation"></span><span id="named_pipe_activation"></span><span id="NAMED_PIPE_ACTIVATION"></span>Активация именованного канала</span><span class="sxs-lookup"><span data-stu-id="74210-1178"><span id="Named_Pipe_Activation"></span><span id="named_pipe_activation"></span><span id="NAMED_PIPE_ACTIVATION"></span>Named Pipe Activation</span></span>
</dt> <dd>

<span data-ttu-id="74210-1179">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1179">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1180"><span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>Активация по TCP</span><span class="sxs-lookup"><span data-stu-id="74210-1180"><span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>TCP Activation</span></span>
</dt> <dd>

<span data-ttu-id="74210-1181">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1181">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1182"><span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>Совместное использование TCP-портов</span><span class="sxs-lookup"><span data-stu-id="74210-1182"><span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>TCP Port Sharing</span></span>
</dt> <dd>

<span data-ttu-id="74210-1183">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1183">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1184"><span id="ASP.NET_4.5"></span><span id="asp.net_4.5"></span>ASP.NET 4,5</span><span class="sxs-lookup"><span data-stu-id="74210-1184"><span id="ASP.NET_4.5"></span><span id="asp.net_4.5"></span>ASP.NET 4.5</span></span>
</dt> <dd>

<span data-ttu-id="74210-1185">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1185">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1186"><span id=".NET_Extensibility_4.5"></span><span id=".net_extensibility_4.5"></span><span id=".NET_EXTENSIBILITY_4.5"></span>Расширяемость .NET 4,5</span><span class="sxs-lookup"><span data-stu-id="74210-1186"><span id=".NET_Extensibility_4.5"></span><span id=".net_extensibility_4.5"></span><span id=".NET_EXTENSIBILITY_4.5"></span>.NET Extensibility 4.5</span></span>
</dt> <dd>

<span data-ttu-id="74210-1187">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1187">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1188"><span id="DirectAccess_and_VPN__RAS_"></span><span id="directaccess_and_vpn__ras_"></span><span id="DIRECTACCESS_AND_VPN__RAS_"></span>DirectAccess и VPN (RAS)</span><span class="sxs-lookup"><span data-stu-id="74210-1188"><span id="DirectAccess_and_VPN__RAS_"></span><span id="directaccess_and_vpn__ras_"></span><span id="DIRECTACCESS_AND_VPN__RAS_"></span>DirectAccess and VPN (RAS)</span></span>
</dt> <dd>

<span data-ttu-id="74210-1189">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1189">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1190"><span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Маршруты</span><span class="sxs-lookup"><span data-stu-id="74210-1190"><span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Routing</span></span>
</dt> <dd>

<span data-ttu-id="74210-1191">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1191">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1192"><span id="Storage_Services"></span><span id="storage_services"></span><span id="STORAGE_SERVICES"></span>Службы хранилища</span><span class="sxs-lookup"><span data-stu-id="74210-1192"><span id="Storage_Services"></span><span id="storage_services"></span><span id="STORAGE_SERVICES"></span>Storage Services</span></span>
</dt> <dd>

<span data-ttu-id="74210-1193">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1193">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1194"><span id="Failover_Cluster_Management_Tools"></span><span id="failover_cluster_management_tools"></span><span id="FAILOVER_CLUSTER_MANAGEMENT_TOOLS"></span>Средства управления отказоустойчивыми кластерами</span><span class="sxs-lookup"><span data-stu-id="74210-1194"><span id="Failover_Cluster_Management_Tools"></span><span id="failover_cluster_management_tools"></span><span id="FAILOVER_CLUSTER_MANAGEMENT_TOOLS"></span>Failover Cluster Management Tools</span></span>
</dt> <dd>

<span data-ttu-id="74210-1195">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1195">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1196"><span id="Active_Directory_Rights_Management_Services_Tools"></span><span id="active_directory_rights_management_services_tools"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOLS"></span>Средства службы Active Directory Rights Management</span><span class="sxs-lookup"><span data-stu-id="74210-1196"><span id="Active_Directory_Rights_Management_Services_Tools"></span><span id="active_directory_rights_management_services_tools"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOLS"></span>Active Directory Rights Management Services Tools</span></span>
</dt> <dd>

<span data-ttu-id="74210-1197">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1197">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1198"><span id="Application_Initialization"></span><span id="application_initialization"></span><span id="APPLICATION_INITIALIZATION"></span>Инициализация приложения</span><span class="sxs-lookup"><span data-stu-id="74210-1198"><span id="Application_Initialization"></span><span id="application_initialization"></span><span id="APPLICATION_INITIALIZATION"></span>Application Initialization</span></span>
</dt> <dd>

<span data-ttu-id="74210-1199">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1199">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1200"><span id="Centralized_SSL_Certificate_Support"></span><span id="centralized_ssl_certificate_support"></span><span id="CENTRALIZED_SSL_CERTIFICATE_SUPPORT"></span>Централизованная поддержка SSL-сертификатов</span><span class="sxs-lookup"><span data-stu-id="74210-1200"><span id="Centralized_SSL_Certificate_Support"></span><span id="centralized_ssl_certificate_support"></span><span id="CENTRALIZED_SSL_CERTIFICATE_SUPPORT"></span>Centralized SSL Certificate Support</span></span>
</dt> <dd>

<span data-ttu-id="74210-1201">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1201">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1202"><span id="Claims-aware_Agent"></span><span id="claims-aware_agent"></span><span id="CLAIMS-AWARE_AGENT"></span>Агент, поддерживающий утверждения</span><span class="sxs-lookup"><span data-stu-id="74210-1202"><span id="Claims-aware_Agent"></span><span id="claims-aware_agent"></span><span id="CLAIMS-AWARE_AGENT"></span>Claims-aware Agent</span></span>
</dt> <dd>

<span data-ttu-id="74210-1203">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1203">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1204"><span id="Remote_Desktop_Session_Host_Tools"></span><span id="remote_desktop_session_host_tools"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS"></span>Средства хоста удаленный рабочий стол сеансов</span><span class="sxs-lookup"><span data-stu-id="74210-1204"><span id="Remote_Desktop_Session_Host_Tools"></span><span id="remote_desktop_session_host_tools"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS"></span>Remote Desktop Session Host Tools</span></span>
</dt> <dd>

<span data-ttu-id="74210-1205">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1205">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1206"><span id="WebSocket_Protocol"></span><span id="websocket_protocol"></span><span id="WEBSOCKET_PROTOCOL"></span>Протокол WebSocket</span><span class="sxs-lookup"><span data-stu-id="74210-1206"><span id="WebSocket_Protocol"></span><span id="websocket_protocol"></span><span id="WEBSOCKET_PROTOCOL"></span>WebSocket Protocol</span></span>
</dt> <dd>

<span data-ttu-id="74210-1207">больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1207">no longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1208"><span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>Доступ к сети COM+</span><span class="sxs-lookup"><span data-stu-id="74210-1208"><span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>COM+ Network Access</span></span>
</dt> <dd>

<span data-ttu-id="74210-1209">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1209">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1210"><span id="File_and_iSCSI_Services_name_change"></span><span id="file_and_iscsi_services_name_change"></span><span id="FILE_AND_ISCSI_SERVICES_NAME_CHANGE"></span>Изменение имени файла и служб iSCSI</span><span class="sxs-lookup"><span data-stu-id="74210-1210"><span id="File_and_iSCSI_Services_name_change"></span><span id="file_and_iscsi_services_name_change"></span><span id="FILE_AND_ISCSI_SERVICES_NAME_CHANGE"></span>File and iSCSI Services name change</span></span>
</dt> <dd>

<span data-ttu-id="74210-1211">Изменено на файловые службы</span><span class="sxs-lookup"><span data-stu-id="74210-1211">Changed to File Services</span></span>

</dd> </dl>

### <a name="windows-server-2012"></a><span data-ttu-id="74210-1212">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="74210-1212">Windows Server 2012</span></span>

<dl> <dt>

<span data-ttu-id="74210-1213"><span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>Пользовательские интерфейсы и инфраструктура</span><span class="sxs-lookup"><span data-stu-id="74210-1213"><span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>User Interfaces and Infrastructure</span></span>
</dt> <dd>

<span data-ttu-id="74210-1214">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1214">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1215"><span id="Server_for_NFS"></span><span id="server_for_nfs"></span><span id="SERVER_FOR_NFS"></span>Сервер для NFS</span><span class="sxs-lookup"><span data-stu-id="74210-1215"><span id="Server_for_NFS"></span><span id="server_for_nfs"></span><span id="SERVER_FOR_NFS"></span>Server for NFS</span></span>
</dt> <dd>

<span data-ttu-id="74210-1216">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1216">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1217"><span id="File_Server_VSS_Agent_Service"></span><span id="file_server_vss_agent_service"></span><span id="FILE_SERVER_VSS_AGENT_SERVICE"></span>Служба агента VSS файлового сервера</span><span class="sxs-lookup"><span data-stu-id="74210-1217"><span id="File_Server_VSS_Agent_Service"></span><span id="file_server_vss_agent_service"></span><span id="FILE_SERVER_VSS_AGENT_SERVICE"></span>File Server VSS Agent Service</span></span>
</dt> <dd>

<span data-ttu-id="74210-1218">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1218">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1219"><span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>Сервер цели iSCSI</span><span class="sxs-lookup"><span data-stu-id="74210-1219"><span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>iSCSI Target Server</span></span>
</dt> <dd>

<span data-ttu-id="74210-1220">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1220">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1221"><span id="Data_Deduplication"></span><span id="data_deduplication"></span><span id="DATA_DEDUPLICATION"></span>Дедупликация данных</span><span class="sxs-lookup"><span data-stu-id="74210-1221"><span id="Data_Deduplication"></span><span id="data_deduplication"></span><span id="DATA_DEDUPLICATION"></span>Data Deduplication</span></span>
</dt> <dd>

<span data-ttu-id="74210-1222">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1222">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1223"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Рабочие папки</span><span class="sxs-lookup"><span data-stu-id="74210-1223"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Work Folders</span></span>
</dt> <dd>

<span data-ttu-id="74210-1224">Удалено</span><span class="sxs-lookup"><span data-stu-id="74210-1224">Removed</span></span>

</dd> <dt>

<span data-ttu-id="74210-1225"><span id="Core_Services"></span><span id="core_services"></span><span id="CORE_SERVICES"></span>Основные службы</span><span class="sxs-lookup"><span data-stu-id="74210-1225"><span id="Core_Services"></span><span id="core_services"></span><span id="CORE_SERVICES"></span>Core Services</span></span>
</dt> <dd>

<span data-ttu-id="74210-1226">Добавляется только для этой версии.</span><span class="sxs-lookup"><span data-stu-id="74210-1226">Added for this version only.</span></span>

</dd> <dt>

<span data-ttu-id="74210-1227"><span id="Remote_Desktop_Virtual_Graphics"></span><span id="remote_desktop_virtual_graphics"></span><span id="REMOTE_DESKTOP_VIRTUAL_GRAPHICS"></span>удаленный рабочий стол виртуальных графических элементов</span><span class="sxs-lookup"><span data-stu-id="74210-1227"><span id="Remote_Desktop_Virtual_Graphics"></span><span id="remote_desktop_virtual_graphics"></span><span id="REMOTE_DESKTOP_VIRTUAL_GRAPHICS"></span>Remote Desktop Virtual Graphics</span></span>
</dt> <dd>

<span data-ttu-id="74210-1228">Добавлено только для этой версии</span><span class="sxs-lookup"><span data-stu-id="74210-1228">Added for this version only</span></span>

</dd> <dt>

<span data-ttu-id="74210-1229"><span id="Remote_Access"></span><span id="remote_access"></span><span id="REMOTE_ACCESS"></span>Удаленный доступ</span><span class="sxs-lookup"><span data-stu-id="74210-1229"><span id="Remote_Access"></span><span id="remote_access"></span><span id="REMOTE_ACCESS"></span>Remote Access</span></span>
</dt> <dd>

<span data-ttu-id="74210-1230">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1230">Added</span></span>

</dd> </dl>

### <a name="windows-server-2008-r2"></a><span data-ttu-id="74210-1231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="74210-1231">Windows Server 2008 R2</span></span>

<dl> <dt>

<span data-ttu-id="74210-1232"><span id="UDDI_Services"></span><span id="uddi_services"></span><span id="UDDI_SERVICES"></span>Службы UDDI</span><span class="sxs-lookup"><span data-stu-id="74210-1232"><span id="UDDI_Services"></span><span id="uddi_services"></span><span id="UDDI_SERVICES"></span>UDDI Services</span></span>
</dt> <dd>

<span data-ttu-id="74210-1233">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1233">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1234"><span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>диспетчер ресурсов системы Windows</span><span class="sxs-lookup"><span data-stu-id="74210-1234"><span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Windows System Resource Manager</span></span>
</dt> <dd>

<span data-ttu-id="74210-1235">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1235">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1236"><span id="Removable_Storage_Manager"></span><span id="removable_storage_manager"></span><span id="REMOVABLE_STORAGE_MANAGER"></span>Диспетчер съемных носителей</span><span class="sxs-lookup"><span data-stu-id="74210-1236"><span id="Removable_Storage_Manager"></span><span id="removable_storage_manager"></span><span id="REMOVABLE_STORAGE_MANAGER"></span>Removable Storage Manager</span></span>
</dt> <dd>

<span data-ttu-id="74210-1237">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1237">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1238"><span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="74210-1238"><span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="74210-1239">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1239">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1240"><span id="Ink_and_Handwriting_Services"></span><span id="ink_and_handwriting_services"></span><span id="INK_AND_HANDWRITING_SERVICES"></span>службы рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="74210-1240"><span id="Ink_and_Handwriting_Services"></span><span id="ink_and_handwriting_services"></span><span id="INK_AND_HANDWRITING_SERVICES"></span>Ink and Handwriting Services</span></span>
</dt> <dd>

<span data-ttu-id="74210-1241">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1241">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1242"><span id="WinRM_IIS_Extension"></span><span id="winrm_iis_extension"></span><span id="WINRM_IIS_EXTENSION"></span>Расширение IIS для WinRM</span><span class="sxs-lookup"><span data-stu-id="74210-1242"><span id="WinRM_IIS_Extension"></span><span id="winrm_iis_extension"></span><span id="WINRM_IIS_EXTENSION"></span>WinRM IIS Extension</span></span>
</dt> <dd>

<span data-ttu-id="74210-1243">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1243">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1244"><span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>Консоль управления DirectAccess</span><span class="sxs-lookup"><span data-stu-id="74210-1244"><span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>DirectAccess Management Console</span></span>
</dt> <dd>

<span data-ttu-id="74210-1245">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1245">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1246"><span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Фоновая интеллектуальная служба передачи (бит)</span><span class="sxs-lookup"><span data-stu-id="74210-1246"><span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Background Intelligent Transfer Service (BITS)</span></span>
</dt> <dd>

<span data-ttu-id="74210-1247">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1247">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1248"><span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>Средство просмотра XPS</span><span class="sxs-lookup"><span data-stu-id="74210-1248"><span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>XPS Viewer</span></span>
</dt> <dd>

<span data-ttu-id="74210-1249">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1249">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1250"><span id="Windows_Biometric_Framework"></span><span id="windows_biometric_framework"></span><span id="WINDOWS_BIOMETRIC_FRAMEWORK"></span>биометрическая платформа Windows</span><span class="sxs-lookup"><span data-stu-id="74210-1250"><span id="Windows_Biometric_Framework"></span><span id="windows_biometric_framework"></span><span id="WINDOWS_BIOMETRIC_FRAMEWORK"></span>Windows Biometric Framework</span></span>
</dt> <dd>

<span data-ttu-id="74210-1251">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1251">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1252"><span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>Поддержка WoW64</span><span class="sxs-lookup"><span data-stu-id="74210-1252"><span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>WoW64 Support</span></span>
</dt> <dd>

<span data-ttu-id="74210-1253">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1253">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1254"><span id="Windows_PowerShell_Integrated_Scripting_Environment__ISE_"></span><span id="windows_powershell_integrated_scripting_environment__ise_"></span><span id="WINDOWS_POWERSHELL_INTEGRATED_SCRIPTING_ENVIRONMENT__ISE_"></span>Интегрированная среда сценариев Windows PowerShell (ISE)</span><span class="sxs-lookup"><span data-stu-id="74210-1254"><span id="Windows_PowerShell_Integrated_Scripting_Environment__ISE_"></span><span id="windows_powershell_integrated_scripting_environment__ise_"></span><span id="WINDOWS_POWERSHELL_INTEGRATED_SCRIPTING_ENVIRONMENT__ISE_"></span>Windows PowerShell Integrated Scripting Environment (ISE)</span></span>
</dt> <dd>

<span data-ttu-id="74210-1255">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1255">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1256"><span id="File_Replication_Service"></span><span id="file_replication_service"></span><span id="FILE_REPLICATION_SERVICE"></span>Служба репликации файлов</span><span class="sxs-lookup"><span data-stu-id="74210-1256"><span id="File_Replication_Service"></span><span id="file_replication_service"></span><span id="FILE_REPLICATION_SERVICE"></span>File Replication Service</span></span>
</dt> <dd>

<span data-ttu-id="74210-1257">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1257">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1258"><span id="BranchCache_for_Network_Files"></span><span id="branchcache_for_network_files"></span><span id="BRANCHCACHE_FOR_NETWORK_FILES"></span>BranchCache для сетевых файлов</span><span class="sxs-lookup"><span data-stu-id="74210-1258"><span id="BranchCache_for_Network_Files"></span><span id="branchcache_for_network_files"></span><span id="BRANCHCACHE_FOR_NETWORK_FILES"></span>BranchCache for Network Files</span></span>
</dt> <dd>

<span data-ttu-id="74210-1259">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1259">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1260"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Рабочие папки</span><span class="sxs-lookup"><span data-stu-id="74210-1260"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Work Folders</span></span>
</dt> <dd>

<span data-ttu-id="74210-1261">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1261">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1262"><span id="Distributed_Scan_Server"></span><span id="distributed_scan_server"></span><span id="DISTRIBUTED_SCAN_SERVER"></span>сервер распределенного сканирования</span><span class="sxs-lookup"><span data-stu-id="74210-1262"><span id="Distributed_Scan_Server"></span><span id="distributed_scan_server"></span><span id="DISTRIBUTED_SCAN_SERVER"></span>Distributed Scan Server</span></span>
</dt> <dd>

<span data-ttu-id="74210-1263">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1263">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1264"><span id="FTP_Publishing_Service"></span><span id="ftp_publishing_service"></span><span id="FTP_PUBLISHING_SERVICE"></span>Служба FTP-публикаций</span><span class="sxs-lookup"><span data-stu-id="74210-1264"><span id="FTP_Publishing_Service"></span><span id="ftp_publishing_service"></span><span id="FTP_PUBLISHING_SERVICE"></span>FTP Publishing Service</span></span>
</dt> <dd>

<span data-ttu-id="74210-1265">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1265">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1266"><span id="FTP_Management_Console"></span><span id="ftp_management_console"></span><span id="FTP_MANAGEMENT_CONSOLE"></span>Консоль управления FTP</span><span class="sxs-lookup"><span data-stu-id="74210-1266"><span id="FTP_Management_Console"></span><span id="ftp_management_console"></span><span id="FTP_MANAGEMENT_CONSOLE"></span>FTP Management Console</span></span>
</dt> <dd>

<span data-ttu-id="74210-1267">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1267">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1268"><span id="FTP_Service"></span><span id="ftp_service"></span><span id="FTP_SERVICE"></span>Служба FTP</span><span class="sxs-lookup"><span data-stu-id="74210-1268"><span id="FTP_Service"></span><span id="ftp_service"></span><span id="FTP_SERVICE"></span>FTP Service</span></span>
</dt> <dd>

<span data-ttu-id="74210-1269">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1269">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1270"><span id="FTP_Extensibility"></span><span id="ftp_extensibility"></span><span id="FTP_EXTENSIBILITY"></span>Расширяемость FTP</span><span class="sxs-lookup"><span data-stu-id="74210-1270"><span id="FTP_Extensibility"></span><span id="ftp_extensibility"></span><span id="FTP_EXTENSIBILITY"></span>FTP Extensibility</span></span>
</dt> <dd>

<span data-ttu-id="74210-1271">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1271">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1272"><span id="IIS_Hostable_Web_Core"></span><span id="iis_hostable_web_core"></span><span id="IIS_HOSTABLE_WEB_CORE"></span>Размещаемый в IIS веб-ядро</span><span class="sxs-lookup"><span data-stu-id="74210-1272"><span id="IIS_Hostable_Web_Core"></span><span id="iis_hostable_web_core"></span><span id="IIS_HOSTABLE_WEB_CORE"></span>IIS Hostable Web Core</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="74210-1273"><span id="Windows_2000_Client_Support"></span><span id="windows_2000_client_support"></span><span id="WINDOWS_2000_CLIENT_SUPPORT"></span>Поддержка клиентов Windows 2000</span><span class="sxs-lookup"><span data-stu-id="74210-1273"><span id="Windows_2000_Client_Support"></span><span id="windows_2000_client_support"></span><span id="WINDOWS_2000_CLIENT_SUPPORT"></span>Windows 2000 Client Support</span></span>
</dt> <dd>

<span data-ttu-id="74210-1274">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1274">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1275"><span id="Certificate_Enrollment_Web_Service"></span><span id="certificate_enrollment_web_service"></span><span id="CERTIFICATE_ENROLLMENT_WEB_SERVICE"></span>веб-служба регистрации сертификатов</span><span class="sxs-lookup"><span data-stu-id="74210-1275"><span id="Certificate_Enrollment_Web_Service"></span><span id="certificate_enrollment_web_service"></span><span id="CERTIFICATE_ENROLLMENT_WEB_SERVICE"></span>Certificate Enrollment Web Service</span></span>
</dt> <dd>

<span data-ttu-id="74210-1276">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1276">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1277"><span id="Certificate_Enrollment_Policy_Web_Service"></span><span id="certificate_enrollment_policy_web_service"></span><span id="CERTIFICATE_ENROLLMENT_POLICY_WEB_SERVICE"></span>веб-служба политик регистрации сертификатов</span><span class="sxs-lookup"><span data-stu-id="74210-1277"><span id="Certificate_Enrollment_Policy_Web_Service"></span><span id="certificate_enrollment_policy_web_service"></span><span id="CERTIFICATE_ENROLLMENT_POLICY_WEB_SERVICE"></span>Certificate Enrollment Policy Web Service</span></span>
</dt> <dd>

<span data-ttu-id="74210-1278">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1278">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1279"><span id="UDDI_Services_Web_Application"></span><span id="uddi_services_web_application"></span><span id="UDDI_SERVICES_WEB_APPLICATION"></span>Веб-приложение служб UDDI</span><span class="sxs-lookup"><span data-stu-id="74210-1279"><span id="UDDI_Services_Web_Application"></span><span id="uddi_services_web_application"></span><span id="UDDI_SERVICES_WEB_APPLICATION"></span>UDDI Services Web Application</span></span>
</dt> <dd>

<span data-ttu-id="74210-1280">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1280">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1281"><span id="UDDI_Services_Database"></span><span id="uddi_services_database"></span><span id="UDDI_SERVICES_DATABASE"></span>База данных служб UDDI</span><span class="sxs-lookup"><span data-stu-id="74210-1281"><span id="UDDI_Services_Database"></span><span id="uddi_services_database"></span><span id="UDDI_SERVICES_DATABASE"></span>UDDI Services Database</span></span>
</dt> <dd>

<span data-ttu-id="74210-1282">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1282">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1283"><span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Расширения сервера приложений для .NET 4,0</span><span class="sxs-lookup"><span data-stu-id="74210-1283"><span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Application Server Extensions for .NET 4.0</span></span>
</dt> <dd>

<span data-ttu-id="74210-1284">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1284">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1285"><span id="UDDI_Services_Tools"></span><span id="uddi_services_tools"></span><span id="UDDI_SERVICES_TOOLS"></span>Средства служб UDDI</span><span class="sxs-lookup"><span data-stu-id="74210-1285"><span id="UDDI_Services_Tools"></span><span id="uddi_services_tools"></span><span id="UDDI_SERVICES_TOOLS"></span>UDDI Services Tools</span></span>
</dt> <dd>

<span data-ttu-id="74210-1286">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1286">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1287"><span id="BitLocker_Drive_Encryption_Administration_Utilities"></span><span id="bitlocker_drive_encryption_administration_utilities"></span><span id="BITLOCKER_DRIVE_ENCRYPTION_ADMINISTRATION_UTILITIES"></span>Служебные программы шифрование диска BitLocker Administration</span><span class="sxs-lookup"><span data-stu-id="74210-1287"><span id="BitLocker_Drive_Encryption_Administration_Utilities"></span><span id="bitlocker_drive_encryption_administration_utilities"></span><span id="BITLOCKER_DRIVE_ENCRYPTION_ADMINISTRATION_UTILITIES"></span>BitLocker Drive Encryption Administration Utilities</span></span>
</dt> <dd>

<span data-ttu-id="74210-1288">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1288">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1289"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>Средства AD DS и AD LDS</span><span class="sxs-lookup"><span data-stu-id="74210-1289"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS and AD LDS Tools</span></span>
</dt> <dd>

<span data-ttu-id="74210-1290">Больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1290">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="74210-1291"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>Средства AD DS и AD LDS</span><span class="sxs-lookup"><span data-stu-id="74210-1291"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS and AD LDS Tools</span></span>
</dt> <dd>

<span data-ttu-id="74210-1292">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1292">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1293"><span id="Active_Directory_Administrative_Center"></span><span id="active_directory_administrative_center"></span><span id="ACTIVE_DIRECTORY_ADMINISTRATIVE_CENTER"></span>центр администрирования Active Directory</span><span class="sxs-lookup"><span data-stu-id="74210-1293"><span id="Active_Directory_Administrative_Center"></span><span id="active_directory_administrative_center"></span><span id="ACTIVE_DIRECTORY_ADMINISTRATIVE_CENTER"></span>Active Directory Administrative Center</span></span>
</dt> <dd>

<span data-ttu-id="74210-1294">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1294">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1295"><span id="Active_Directory_module_for___________Windows_PowerShell"></span><span id="active_directory_module_for___________windows_powershell"></span><span id="ACTIVE_DIRECTORY_MODULE_FOR___________WINDOWS_POWERSHELL"></span>модуль Active Directory для Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="74210-1295"><span id="Active_Directory_module_for___________Windows_PowerShell"></span><span id="active_directory_module_for___________windows_powershell"></span><span id="ACTIVE_DIRECTORY_MODULE_FOR___________WINDOWS_POWERSHELL"></span>Active Directory module for Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="74210-1296">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1296">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1297"><span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Средства брокера подключение к удаленному рабочему столу</span><span class="sxs-lookup"><span data-stu-id="74210-1297"><span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Remote Desktop Connection Broker Tools</span></span>
</dt> <dd>

<span data-ttu-id="74210-1298">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1298">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1299"><span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64</span><span class="sxs-lookup"><span data-stu-id="74210-1299"><span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64</span></span>
</dt> <dd>

<span data-ttu-id="74210-1300">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1300">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1301"><span id="WoW64_for_.NET_Framework_2.0_and_Windows_PowerShell"></span><span id="wow64_for_.net_framework_2.0_and_windows_powershell"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND_WINDOWS_POWERSHELL"></span>Подсистема WoW64 для платформа .NET Framework 2,0 и Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="74210-1301"><span id="WoW64_for_.NET_Framework_2.0_and_Windows_PowerShell"></span><span id="wow64_for_.net_framework_2.0_and_windows_powershell"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND_WINDOWS_POWERSHELL"></span>WoW64 for .NET Framework 2.0 and Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="74210-1302">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1302">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1303"><span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>Подсистема WoW64 для платформа .NET Framework 2,0</span><span class="sxs-lookup"><span data-stu-id="74210-1303"><span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 for .NET Framework 2.0</span></span>
</dt> <dd>

<span data-ttu-id="74210-1304">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1304">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1305"><span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>Подсистема WoW64 для PowerShell</span><span class="sxs-lookup"><span data-stu-id="74210-1305"><span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 for PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="74210-1306">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1306">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1307"><span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>Подсистема WoW64 для платформа .NET Framework 3,0 и 3,5</span><span class="sxs-lookup"><span data-stu-id="74210-1307"><span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 for .NET Framework 3.0 and 3.5</span></span>
</dt> <dd>

<span data-ttu-id="74210-1308">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1308">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1309"><span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>Подсистема WoW64 для служб печати</span><span class="sxs-lookup"><span data-stu-id="74210-1309"><span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 for Print Services</span></span>
</dt> <dd>

<span data-ttu-id="74210-1310">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1310">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1311"><span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>Подсистема WoW64 для отказоустойчивой кластеризации</span><span class="sxs-lookup"><span data-stu-id="74210-1311"><span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 for Failover Clustering</span></span>
</dt> <dd>

<span data-ttu-id="74210-1312">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1312">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1313"><span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>Подсистема WoW64 для редактора метода ввода</span><span class="sxs-lookup"><span data-stu-id="74210-1313"><span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 for Input Method Editor</span></span>
</dt> <dd>

<span data-ttu-id="74210-1314">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1314">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1315"><span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>Подсистема WoW64 для приложений на основе UNIX</span><span class="sxs-lookup"><span data-stu-id="74210-1315"><span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 for Subsystem for UNIX-based Applications</span></span>
</dt> <dd>

<span data-ttu-id="74210-1316">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1316">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1317"><span id="BitLocker_Recovery_Password_Viewer"></span><span id="bitlocker_recovery_password_viewer"></span><span id="BITLOCKER_RECOVERY_PASSWORD_VIEWER"></span>Средство просмотра паролей восстановления BitLocker</span><span class="sxs-lookup"><span data-stu-id="74210-1317"><span id="BitLocker_Recovery_Password_Viewer"></span><span id="bitlocker_recovery_password_viewer"></span><span id="BITLOCKER_RECOVERY_PASSWORD_VIEWER"></span>BitLocker Recovery Password Viewer</span></span>
</dt> <dd>

<span data-ttu-id="74210-1318">Добавлено</span><span class="sxs-lookup"><span data-stu-id="74210-1318">Added</span></span>

</dd> <dt>

<span data-ttu-id="74210-1319"><span id="Print_and_Document_Services_name_change"></span><span id="print_and_document_services_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_NAME_CHANGE"></span>Изменение имени службы печати и документов</span><span class="sxs-lookup"><span data-stu-id="74210-1319"><span id="Print_and_Document_Services_name_change"></span><span id="print_and_document_services_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_NAME_CHANGE"></span>Print and Document Services name change</span></span>
</dt> <dd>

<span data-ttu-id="74210-1320">Именованные службы печати для этого выпуска</span><span class="sxs-lookup"><span data-stu-id="74210-1320">named Print Services for this release</span></span>

</dd> <dt>

<span data-ttu-id="74210-1321"><span id="Remote_Desktop_Services_name_change"></span><span id="remote_desktop_services_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_NAME_CHANGE"></span>Изменение имени службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="74210-1321"><span id="Remote_Desktop_Services_name_change"></span><span id="remote_desktop_services_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_NAME_CHANGE"></span>Remote Desktop Services name change</span></span>
</dt> <dd>

<span data-ttu-id="74210-1322">Именованные службы терминалов в этом выпуске</span><span class="sxs-lookup"><span data-stu-id="74210-1322">named Terminal Services in this release</span></span>

</dd> <dt>

<span data-ttu-id="74210-1323"><span id=".NET_Framework_3.5.1_Features_name_change"></span><span id=".net_framework_3.5.1_features_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES_NAME_CHANGE"></span>Изменение имени компонентов платформа .NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="74210-1323"><span id=".NET_Framework_3.5.1_Features_name_change"></span><span id=".net_framework_3.5.1_features_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES_NAME_CHANGE"></span>.NET Framework 3.5.1 Features name change</span></span>
</dt> <dd>

<span data-ttu-id="74210-1324">В этом выпуске есть именованные функции платформа .NET Framework 3,0</span><span class="sxs-lookup"><span data-stu-id="74210-1324">Named .NET Framework 3.0 Features in this release</span></span>

</dd> <dt>

<span data-ttu-id="74210-1325"><span id="Remote_Desktop_Session_Host_name_change"></span><span id="remote_desktop_session_host_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_NAME_CHANGE"></span>Изменение имени узла сеанса удаленный рабочий стол</span><span class="sxs-lookup"><span data-stu-id="74210-1325"><span id="Remote_Desktop_Session_Host_name_change"></span><span id="remote_desktop_session_host_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_NAME_CHANGE"></span>Remote Desktop Session Host name change</span></span>
</dt> <dd>

<span data-ttu-id="74210-1326">Именованный сервер терминалов в этом выпуске</span><span class="sxs-lookup"><span data-stu-id="74210-1326">Named Terminal Server in this release</span></span>

</dd> <dt>

<span data-ttu-id="74210-1327"><span id="Remote_Desktop_Licensing_name_change"></span><span id="remote_desktop_licensing_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_NAME_CHANGE"></span>Изменение имени лицензирования удаленный рабочий стол</span><span class="sxs-lookup"><span data-stu-id="74210-1327"><span id="Remote_Desktop_Licensing_name_change"></span><span id="remote_desktop_licensing_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_NAME_CHANGE"></span>Remote Desktop Licensing name change</span></span>
</dt> <dd>

<span data-ttu-id="74210-1328">Лицензирование служб терминалов в этом выпуске</span><span class="sxs-lookup"><span data-stu-id="74210-1328">Named TS Licensing in this release</span></span>

</dd> <dt>

<span data-ttu-id="74210-1329"><span id="Remote_Desktop_Gateway_name_change"></span><span id="remote_desktop_gateway_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_NAME_CHANGE"></span>Изменение имени шлюза удаленный рабочий стол</span><span class="sxs-lookup"><span data-stu-id="74210-1329"><span id="Remote_Desktop_Gateway_name_change"></span><span id="remote_desktop_gateway_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_NAME_CHANGE"></span>Remote Desktop Gateway name change</span></span>
</dt> <dd>

<span data-ttu-id="74210-1330">Именованный шлюз TS в этом выпуске</span><span class="sxs-lookup"><span data-stu-id="74210-1330">Named TS Gateway in this release</span></span>

</dd> <dt>

<span data-ttu-id="74210-1331"><span id="Remote_Desktop_Connection_Broker_name_change"></span><span id="remote_desktop_connection_broker_name_change"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_NAME_CHANGE"></span>Изменение имени компонента Service Broker подключение к удаленному рабочему столу</span><span class="sxs-lookup"><span data-stu-id="74210-1331"><span id="Remote_Desktop_Connection_Broker_name_change"></span><span id="remote_desktop_connection_broker_name_change"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_NAME_CHANGE"></span>Remote Desktop Connection Broker name change</span></span>
</dt> <dd>

<span data-ttu-id="74210-1332">Посредник сеансов служб терминалов в этом выпуске</span><span class="sxs-lookup"><span data-stu-id="74210-1332">Named TS Session Broker in this release</span></span>

</dd> <dt>

<span data-ttu-id="74210-1333"><span id="Remote_Desktop_Web_Access_name_change"></span><span id="remote_desktop_web_access_name_change"></span><span id="REMOTE_DESKTOP_WEB_ACCESS_NAME_CHANGE"></span>Изменение имени Веб-доступ удаленный рабочий стол</span><span class="sxs-lookup"><span data-stu-id="74210-1333"><span id="Remote_Desktop_Web_Access_name_change"></span><span id="remote_desktop_web_access_name_change"></span><span id="REMOTE_DESKTOP_WEB_ACCESS_NAME_CHANGE"></span>Remote Desktop Web Access name change</span></span>
</dt> <dd>

<span data-ttu-id="74210-1334">Именованные Веб-доступ TS в этом выпуске</span><span class="sxs-lookup"><span data-stu-id="74210-1334">Named TS Web Access in this release</span></span>

</dd> <dt>

<span data-ttu-id="74210-1335"><span id=".NET_Framework_3.5.1_name_change"></span><span id=".net_framework_3.5.1_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_NAME_CHANGE"></span>Изменение имени платформа .NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="74210-1335"><span id=".NET_Framework_3.5.1_name_change"></span><span id=".net_framework_3.5.1_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_NAME_CHANGE"></span>.NET Framework 3.5.1 name change</span></span>
</dt> <dd>

<span data-ttu-id="74210-1336">(220) в этом выпуске есть компоненты NET FX 3,0</span><span class="sxs-lookup"><span data-stu-id="74210-1336">(220) Named Net FX 3.0 Features in this release</span></span>

<span data-ttu-id="74210-1337">(230) в этом выпуске имеется имя ядра сервера приложений</span><span class="sxs-lookup"><span data-stu-id="74210-1337">(230) Named Application Server Core in this release</span></span>

</dd> <dt>

<span data-ttu-id="74210-1338"><span id="AD_DS_Tools_name_change"></span><span id="ad_ds_tools_name_change"></span><span id="AD_DS_TOOLS_NAME_CHANGE"></span>Изменение имени инструментов AD DS</span><span class="sxs-lookup"><span data-stu-id="74210-1338"><span id="AD_DS_Tools_name_change"></span><span id="ad_ds_tools_name_change"></span><span id="AD_DS_TOOLS_NAME_CHANGE"></span>AD DS Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="74210-1339">В этом выпуске имеются именованные средства домен Active Directory Services</span><span class="sxs-lookup"><span data-stu-id="74210-1339">Named Active Directory Domain Services Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="74210-1340"><span id="AD_LDS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_lds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>Изменение имени AD LDS Snap-Ins и Command-Line средств</span><span class="sxs-lookup"><span data-stu-id="74210-1340"><span id="AD_LDS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_lds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>AD LDS Snap-Ins and Command-Line Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="74210-1341">В этом выпуске службы Active Directory облегченного доступа к каталогам средства с именем.</span><span class="sxs-lookup"><span data-stu-id="74210-1341">Named Active Directory Lightweight Directory Services Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="74210-1342"><span id="Print_and_Document_Services_Tools_name_change"></span><span id="print_and_document_services_tools_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_TOOLS_NAME_CHANGE"></span>Изменение имени инструментов службы печати и документов</span><span class="sxs-lookup"><span data-stu-id="74210-1342"><span id="Print_and_Document_Services_Tools_name_change"></span><span id="print_and_document_services_tools_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_TOOLS_NAME_CHANGE"></span>Print and Document Services Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="74210-1343">Средства именованных служб печати в этом выпуске</span><span class="sxs-lookup"><span data-stu-id="74210-1343">Named Print Services Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="74210-1344"><span id="Remote_Desktop_Services_Tools_name_change"></span><span id="remote_desktop_services_tools_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS_NAME_CHANGE"></span>Изменение имени инструментов службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="74210-1344"><span id="Remote_Desktop_Services_Tools_name_change"></span><span id="remote_desktop_services_tools_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS_NAME_CHANGE"></span>Remote Desktop Services Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="74210-1345">В этом выпуске имеются именованные средства служб терминалов</span><span class="sxs-lookup"><span data-stu-id="74210-1345">Named Terminal Services Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="74210-1346"><span id="Remote_Desktop_Session_Host_Tools_name_change"></span><span id="remote_desktop_session_host_tools_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS_NAME_CHANGE"></span>Изменение имени средств узла для удаленный рабочий стол сеансов</span><span class="sxs-lookup"><span data-stu-id="74210-1346"><span id="Remote_Desktop_Session_Host_Tools_name_change"></span><span id="remote_desktop_session_host_tools_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS_NAME_CHANGE"></span>Remote Desktop Session Host Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="74210-1347">В этом выпуске есть именованные средства сервера терминалов</span><span class="sxs-lookup"><span data-stu-id="74210-1347">Named Terminal Server Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="74210-1348"><span id="Remote_Desktop_Gateway_Tools_name_change"></span><span id="remote_desktop_gateway_tools_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_TOOLS_NAME_CHANGE"></span>Изменение имени средств шлюза удаленный рабочий стол</span><span class="sxs-lookup"><span data-stu-id="74210-1348"><span id="Remote_Desktop_Gateway_Tools_name_change"></span><span id="remote_desktop_gateway_tools_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_TOOLS_NAME_CHANGE"></span>Remote Desktop Gateway Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="74210-1349">В этом выпуске есть именованные средства шлюза служб терминалов</span><span class="sxs-lookup"><span data-stu-id="74210-1349">Named TS Gateway Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="74210-1350"><span id="Remote_Desktop_Licensing_Tools_name_change"></span><span id="remote_desktop_licensing_tools_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_TOOLS_NAME_CHANGE"></span>Изменение имени средств лицензирования удаленный рабочий стол</span><span class="sxs-lookup"><span data-stu-id="74210-1350"><span id="Remote_Desktop_Licensing_Tools_name_change"></span><span id="remote_desktop_licensing_tools_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_TOOLS_NAME_CHANGE"></span>Remote Desktop Licensing Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="74210-1351">Именованные средства лицензирования служб терминалов в этом выпуске</span><span class="sxs-lookup"><span data-stu-id="74210-1351">Named TS Licensing Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="74210-1352"><span id="AD_DS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_ds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>Изменение имени AD DS Snap-Ins и Command-Line средств</span><span class="sxs-lookup"><span data-stu-id="74210-1352"><span id="AD_DS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_ds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>AD DS Snap-Ins and Command-Line Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="74210-1353">Средства контроллера домена Active Directory</span><span class="sxs-lookup"><span data-stu-id="74210-1353">Active Directory Domain Controller Tools</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="74210-1354">Примеры</span><span class="sxs-lookup"><span data-stu-id="74210-1354">Examples</span></span>

<span data-ttu-id="74210-1355">Следующий скрипт отображает имена всех компонентов сервера на компьютере с именем FABRIKAM.</span><span class="sxs-lookup"><span data-stu-id="74210-1355">The following script displays the names of all the server features on the computer named "FABRIKAM".</span></span> <span data-ttu-id="74210-1356">Обратите внимание, что целевой компьютер должен работать под управлением Windows Server 2008 или более поздней серверной операционной системы.</span><span class="sxs-lookup"><span data-stu-id="74210-1356">Note that the target computer must be running Windows Server 2008 or a later server operating system.</span></span>


```VB
strComputer = "FABRIKAM"

Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")

Set colFeatureList = objWMIService.ExecQuery("SELECT Name FROM Win32_ServerFeature")

For Each objFeature In colFeatureList
   WScript.Echo objFeature.Name

Next
```



## <a name="requirements"></a><span data-ttu-id="74210-1357">Требования</span><span class="sxs-lookup"><span data-stu-id="74210-1357">Requirements</span></span>



| <span data-ttu-id="74210-1358">Требование</span><span class="sxs-lookup"><span data-stu-id="74210-1358">Requirement</span></span> | <span data-ttu-id="74210-1359">Значение</span><span class="sxs-lookup"><span data-stu-id="74210-1359">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="74210-1360">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74210-1360">Minimum supported client</span></span><br/> | <span data-ttu-id="74210-1361">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74210-1361">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="74210-1362">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="74210-1362">Minimum supported server</span></span><br/> | <span data-ttu-id="74210-1363">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="74210-1363">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="74210-1364">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="74210-1364">Namespace</span></span><br/>                | <span data-ttu-id="74210-1365">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="74210-1365">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="74210-1366">MOF</span><span class="sxs-lookup"><span data-stu-id="74210-1366">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74210-1367"><dt>Серверкомппров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="74210-1367"><dt>ServerCompProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="74210-1368">DLL</span><span class="sxs-lookup"><span data-stu-id="74210-1368">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74210-1369"><dt>ServerCompProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74210-1369"><dt>ServerCompProv.dll</dt></span></span> </dl> |



 

