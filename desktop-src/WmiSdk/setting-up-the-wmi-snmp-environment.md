---
description: Для взаимодействия с сетевым устройством с помощью WMI-интерфейса SNMP требуется настройка устройств, SNMP и служб WMI. Сведения в этом разделе поясняют, как настроить среду WMI SNMP.
ms.assetid: 8074175a-af66-49b2-9723-dfb38a08fb63
ms.tgt_platform: multiple
title: Настройка среды SNMP WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eeed470b1e38bf853bd6b023fa0f07b01c5df47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349225"
---
# <a name="setting-up-the-wmi-snmp-environment"></a><span data-ttu-id="a0fa8-104">Настройка среды SNMP WMI</span><span class="sxs-lookup"><span data-stu-id="a0fa8-104">Setting up the WMI SNMP Environment</span></span>

<span data-ttu-id="a0fa8-105">Для взаимодействия с сетевым устройством с помощью WMI-интерфейса SNMP требуется настройка устройств, SNMP и служб WMI.</span><span class="sxs-lookup"><span data-stu-id="a0fa8-105">Communicating with a network device using the WMI SNMP interface requires the configuration of the device, SNMP, and WMI services.</span></span> <span data-ttu-id="a0fa8-106">Сведения в этом разделе поясняют, как настроить среду WMI SNMP.</span><span class="sxs-lookup"><span data-stu-id="a0fa8-106">The information in this topic explains how to set up the WMI SNMP environment.</span></span>

<span data-ttu-id="a0fa8-107">В этом разделе обсуждаются следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="a0fa8-107">The following sections are discussed in this topic:</span></span>

## <a name="installing-the-snmp-provider"></a><span data-ttu-id="a0fa8-108">Установка поставщика SNMP</span><span class="sxs-lookup"><span data-stu-id="a0fa8-108">Installing the SNMP Provider</span></span>

<span data-ttu-id="a0fa8-109">Служба SNMP не включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a0fa8-109">The SNMP service is not enabled by default.</span></span> <span data-ttu-id="a0fa8-110">Вы можете включить службу SNMP и поставщик SNMP WMI с помощью панели управления.</span><span class="sxs-lookup"><span data-stu-id="a0fa8-110">You can enable the SNMP service and the WMI SNMP Provider through the Control Panel.</span></span> <span data-ttu-id="a0fa8-111">Имейте в виду, что служба SNMP должна быть включена и запущена для работы поставщика SNMP WMI.</span><span class="sxs-lookup"><span data-stu-id="a0fa8-111">Be aware that the SNMP service must be enabled and running for the WMI SNMP provider to work.</span></span>

<span data-ttu-id="a0fa8-112">Начиная с Windows Vista, используйте следующую процедуру для установки поставщика SNMP.</span><span class="sxs-lookup"><span data-stu-id="a0fa8-112">Starting with Windows Vista, use the following procedure to install the SNMP provider.</span></span>

<span data-ttu-id="a0fa8-113">**Установка поставщика SNMP**</span><span class="sxs-lookup"><span data-stu-id="a0fa8-113">**To install the SNMP Provider**</span></span>

1.  <span data-ttu-id="a0fa8-114">В **панели управления** выберите **программы**.</span><span class="sxs-lookup"><span data-stu-id="a0fa8-114">From the **Control Panel**, select **Programs**.</span></span>
2.  <span data-ttu-id="a0fa8-115">В разделе **программы и компоненты** выберите **Включение или отключение компонентов Windows**.</span><span class="sxs-lookup"><span data-stu-id="a0fa8-115">Under **Programs and Features**, select **Turn Windows features on or off**.</span></span>
3.  <span data-ttu-id="a0fa8-116">В списке компонентов Windows прокрутите вниз до **компонента SNMP** и разверните список, чтобы увидеть **поставщик WMI SNMP**.</span><span class="sxs-lookup"><span data-stu-id="a0fa8-116">In the Windows features list, scroll down to **SNMP feature** and expand the list so that you can see **WMI SNMP Provider**.</span></span>
4.  <span data-ttu-id="a0fa8-117">Установите флажок для **поставщика WMI SNMP**.</span><span class="sxs-lookup"><span data-stu-id="a0fa8-117">Select the check box for **WMI SNMP Provider**.</span></span> <span data-ttu-id="a0fa8-118">Флажок для **компонента SNMP** выбирается автоматически, так как поставщик требует протокол SNMP.</span><span class="sxs-lookup"><span data-stu-id="a0fa8-118">The check box for **SNMP feature** is selected automatically because the provider requires SNMP.</span></span>
5.  <span data-ttu-id="a0fa8-119">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a0fa8-119">Click **OK**.</span></span>
6.  <span data-ttu-id="a0fa8-120">В командной строке или в меню " **Пуск** " запустите Services. msc и убедитесь, что служба SNMP запущена.</span><span class="sxs-lookup"><span data-stu-id="a0fa8-120">From a command prompt or the **Start** menu, run Services.msc and ensure that the SNMP service is started.</span></span>

## <a name="creating-an-snmp-namespace"></a><span data-ttu-id="a0fa8-121">Создание пространства имен SNMP</span><span class="sxs-lookup"><span data-stu-id="a0fa8-121">Creating an SNMP Namespace</span></span>

<span data-ttu-id="a0fa8-122">Пространство имен SNMP определяет представление сетевого устройства.</span><span class="sxs-lookup"><span data-stu-id="a0fa8-122">An SNMP namespace defines a view of a network device.</span></span>

> [!Note]  
> <span data-ttu-id="a0fa8-123">Дополнительные сведения о поддержке и установке этого компонента в определенной операционной системе см. в статье [доступность компонентов WMI в операционной системе](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="a0fa8-123">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

<span data-ttu-id="a0fa8-124">В следующей процедуре описывается создание [*пространства имен*](gloss-n.md)SNMP WMI.</span><span class="sxs-lookup"><span data-stu-id="a0fa8-124">The following procedure describes how to create an SNMP WMI [*namespace*](gloss-n.md).</span></span>

<span data-ttu-id="a0fa8-125">**Создание пространства имен SNMP**</span><span class="sxs-lookup"><span data-stu-id="a0fa8-125">**To create an SNMP namespace**</span></span>

1.  <span data-ttu-id="a0fa8-126">Создайте экземпляр класса системы [**\_ \_ пространства имен**](--namespace.md) , выполнив компиляцию файла [*MOF-файл*](gloss-m.md) . mof или с помощью [API COM для WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="a0fa8-126">Create an instance of the [**\_\_Namespace**](--namespace.md) system class either by compiling a [*Managed Object Format*](gloss-m.md) .mof file or by using the [COM API for WMI](com-api-for-wmi.md).</span></span>

    <span data-ttu-id="a0fa8-127">Дополнительные сведения см. [в разделе Создание иерархий в WMI](creating-hierarchies-within-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="a0fa8-127">For more information, see [Creating Hierarchies Within WMI](creating-hierarchies-within-wmi.md).</span></span>

2.  <span data-ttu-id="a0fa8-128">Свяжите [*Квалификаторы*](gloss-q.md) поставщика SNMP с определением пространства имен.</span><span class="sxs-lookup"><span data-stu-id="a0fa8-128">Associate SNMP provider [*qualifiers*](gloss-q.md) with the namespace definition.</span></span>

    <span data-ttu-id="a0fa8-129">Квалификаторы поставщика SNMP содержат зависящую от реализации контекстную информацию и свойства транспорта, определяющие, как поставщик SNMP получает доступ к SNMP-устройству.</span><span class="sxs-lookup"><span data-stu-id="a0fa8-129">The SNMP provider qualifiers contain implementation-specific context information and transport properties that define how the SNMP provider accesses an SNMP device.</span></span> <span data-ttu-id="a0fa8-130">Дополнительные сведения см. в разделе [**квалификаторы, относящиеся к поставщику SNMP**](qualifiers-specific-to-the-snmp-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a0fa8-130">For more information, see [**Qualifiers Specific to the SNMP Provider**](qualifiers-specific-to-the-snmp-provider.md).</span></span>

3.  <span data-ttu-id="a0fa8-131">Используйте программу командной строки [mofcomp](mofcomp.md) для загрузки MOF-кода в репозиторий WMI.</span><span class="sxs-lookup"><span data-stu-id="a0fa8-131">Use the [mofcomp](mofcomp.md) command line tool to load the MOF code into the WMI repository.</span></span>

    <span data-ttu-id="a0fa8-132">Дополнительные сведения см. в разделе [Компиляция MOF-файлов](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="a0fa8-132">For more information, see [Compiling MOF files](compiling-mof-files.md).</span></span>

<span data-ttu-id="a0fa8-133">В следующем примере кода MOF определяется \\ пространство имен SNMP с подмножеством квалификаторов, которые могут быть связаны с пространством имен SNMP.</span><span class="sxs-lookup"><span data-stu-id="a0fa8-133">The following MOF code example defines the \\snmp namespace with a subset of the qualifiers that can be associated with an SNMP namespace.</span></span>

``` syntax
// Load classes and instances into <\\.\root> namespace

#pragma namespace("\\\\.\\root")               

[ 
  AgentAddress( "localhost" ), 
  AgentReadCommunityName( "public"), 
  AgentWriteCommunityName( "private"), 
  AgentRetryCount( 1 ), 
  AgentRetryTimeout( 500 ), 
  AgentVarBindsPerPdu( 10 ),
  AgentFlowControlWindowSize ( 3 ) 
]

  instance of __Namespace
  {
      Name = "snmp" ;
  };
```

## <a name="inserting-snmp-mib-data-into-wmi"></a><span data-ttu-id="a0fa8-134">Вставка данных SNMP MIB в WMI</span><span class="sxs-lookup"><span data-stu-id="a0fa8-134">Inserting SNMP MIB Data into WMI</span></span>

<span data-ttu-id="a0fa8-135">Поставщик SNMP выступает в качестве моста между данными SNMP и классами WMI.</span><span class="sxs-lookup"><span data-stu-id="a0fa8-135">As a provider, the SNMP provider acts as a bridge between SNMP data and WMI classes.</span></span> <span data-ttu-id="a0fa8-136">Поэтому в инструментарии WMI должны быть классы, которые представляют различные аспекты устройства с поддержкой SNMP.</span><span class="sxs-lookup"><span data-stu-id="a0fa8-136">Therefore, you must have classes in WMI that represent different aspects of an SNMP-enabled device.</span></span> <span data-ttu-id="a0fa8-137">Для этого необходимо использовать компилятор модуля SNMP Information ([smi2smir](smi2smir.md)) для компиляции данных SNMP-управления из формата SNMP в эквивалентные определения схемы CIM.</span><span class="sxs-lookup"><span data-stu-id="a0fa8-137">To do so, you must use the SNMP information module compiler ([smi2smir](smi2smir.md)) to compile SNMP management information from the SNMP format into the equivalent CIM schema definitions.</span></span> <span data-ttu-id="a0fa8-138">После этого выходные данные компилятора сведений можно направить в базу данных схемы SNMP, которая называется "хранилище данных модуля SNMP (Смир)", или с помощью нескольких различных типов MOF-файлов.</span><span class="sxs-lookup"><span data-stu-id="a0fa8-138">You can then direct the output of the information compiler into an SNMP schema database called the "SNMP Module Information Repository (SMIR)" or to several different kinds of MOF files.</span></span>

<span data-ttu-id="a0fa8-139">Компилятор работает в режиме командной строки, используя в качестве входных данных один файл MIB.</span><span class="sxs-lookup"><span data-stu-id="a0fa8-139">The compiler runs in the command-line mode, using one MIB file as input.</span></span> <span data-ttu-id="a0fa8-140">Следующая команда загружает указанный файл MIB в Смир.</span><span class="sxs-lookup"><span data-stu-id="a0fa8-140">The following command loads the specified MIB file into the SMIR.</span></span>

<span data-ttu-id="a0fa8-141">\**smi2smir/a\*\*\*<MIB file>*</span><span class="sxs-lookup"><span data-stu-id="a0fa8-141">**smi2smir /a** *<MIB file>*</span></span>

## <a name="setting-up-snmp-communities"></a><span data-ttu-id="a0fa8-142">Настройка SNMP-сообществ</span><span class="sxs-lookup"><span data-stu-id="a0fa8-142">Setting Up SNMP Communities</span></span>

<span data-ttu-id="a0fa8-143">Как мера безопасности, сообщество SNMP "Public" по умолчанию не создается.</span><span class="sxs-lookup"><span data-stu-id="a0fa8-143">As a security measure, the SNMP "public" community is not created by default.</span></span> <span data-ttu-id="a0fa8-144">Вы можете создать сообщество, как описано в [разделе Параметры реестра сообщества](/previous-versions/windows/embedded/ms907028(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="a0fa8-144">You can create the community as described in [Communities Registry Settings](/previous-versions/windows/embedded/ms907028(v=msdn.10)).</span></span> <span data-ttu-id="a0fa8-145">Если у вас нет сообщества, Создайте общедоступное сообщество для доступа к поставщику SNMP.</span><span class="sxs-lookup"><span data-stu-id="a0fa8-145">If you do not have any community, then create the "public" community to access the SNMP provider.</span></span>

## <a name="generating-mof-files-from-mib-files"></a><span data-ttu-id="a0fa8-146">Создание MOF-файлов из файлов MIB</span><span class="sxs-lookup"><span data-stu-id="a0fa8-146">Generating MOF Files from MIB Files</span></span>

<span data-ttu-id="a0fa8-147">Следующие команды являются примером создания MOF-файлов из файлов MIB, которые устанавливаются при установке поставщика SNMP.</span><span class="sxs-lookup"><span data-stu-id="a0fa8-147">The following commands are an example of how to generate MOF files from the MIB files that are installed when the SNMP provider is installed.</span></span>

<span data-ttu-id="a0fa8-148">**CD** *% WINDIR% \\ system32 \\ , \\ SNMP*</span><span class="sxs-lookup"><span data-stu-id="a0fa8-148">**cd** *%windir%\\system32\\wbem\\SNMP*</span></span>

<span data-ttu-id="a0fa8-149">**Smi2smir/g** *.. \\ . \\ хостмиб. MIB* **>** *хостмиб. mof*</span><span class="sxs-lookup"><span data-stu-id="a0fa8-149">**Smi2smir /g** *..\\..\\hostmib.mib* **>** *hostmib.mof*</span></span>

<span data-ttu-id="a0fa8-150">**Smi2smir/g** *.. \\ . \\ ипфорвд. MIB* **>** *ипфорвд. mof*</span><span class="sxs-lookup"><span data-stu-id="a0fa8-150">**Smi2smir /g** *..\\..\\ipforwd.mib* **>** *ipforwd.mof*</span></span>

<span data-ttu-id="a0fa8-151">**Smi2smir/g** *.. \\ . \\ нипкс. MIB* **>** *нипкс. mof*</span><span class="sxs-lookup"><span data-stu-id="a0fa8-151">**Smi2smir /g** *..\\..\\nipx.mib* **>** *nipx.mof*</span></span>

<span data-ttu-id="a0fa8-152">**Smi2smir/g** *.. \\ . \\ MIB \_ II. MIB* **>** *MIB \_ II. mof*</span><span class="sxs-lookup"><span data-stu-id="a0fa8-152">**Smi2smir /g** *..\\..\\mib\_ii.mib* **>** *mib\_ii.mof*</span></span>

<span data-ttu-id="a0fa8-153">**Smi2smir/g** *.. \\ . \\ lmmib2. MIB* **>** *lmmib2. mof*</span><span class="sxs-lookup"><span data-stu-id="a0fa8-153">**Smi2smir /g** *..\\..\\lmmib2.mib* **>** *lmmib2.mof*</span></span>

<span data-ttu-id="a0fa8-154">**Smi2smir/g** *.. \\ . \\ мкастмиб. MIB* **>** *мкастмиб. mof*</span><span class="sxs-lookup"><span data-stu-id="a0fa8-154">**Smi2smir /g** *..\\..\\mcastmib.mib* **>** *mcastmib.mof*</span></span>

<span data-ttu-id="a0fa8-155">**Smi2smir/g** *.. \\ . \\ rfc2571. MIB* **>** *rfc2571. mof*</span><span class="sxs-lookup"><span data-stu-id="a0fa8-155">**Smi2smir /g** *..\\..\\rfc2571.mib* **>** *rfc2571.mof*</span></span>

<span data-ttu-id="a0fa8-156">**Smi2smir/g** *.. \\ . \\ вфоспф. MIB* **>** *вфоспф. mof*</span><span class="sxs-lookup"><span data-stu-id="a0fa8-156">**Smi2smir /g** *..\\..\\wfospf.mib* **>** *wfospf.mof*</span></span>

<span data-ttu-id="a0fa8-157">**Smi2smir/g** *.. \\ . \\ DHCP. MIB \\ . \\ .. MSFT. MIB* **>** *DHCP. mof*</span><span class="sxs-lookup"><span data-stu-id="a0fa8-157">**Smi2smir /g** *..\\..\\dhcp.mib..\\..\\msft.mib* **>** *dhcp.mof*</span></span>

<span data-ttu-id="a0fa8-158">**Smi2smir/g** *.. \\ . \\ WINS. MIB \\ . \\ .. MSFT. MIB* **>** *WINS. mof*</span><span class="sxs-lookup"><span data-stu-id="a0fa8-158">**Smi2smir /g** *..\\..\\wins.mib..\\..\\msft.mib* **>** *wins.mof*</span></span>

<span data-ttu-id="a0fa8-159">**Smi2smir/g** *.. \\ . \\ мипкс. MIB \\ . \\ .. MSFT. MIB* **>** *мипкс. mof*</span><span class="sxs-lookup"><span data-stu-id="a0fa8-159">**Smi2smir /g** *..\\..\\mipx.mib..\\..\\msft.mib* **>** *mipx.mof*</span></span>

<span data-ttu-id="a0fa8-160">**Smi2smir/g** *.. \\ . \\ мрипсап. MIB \\ . \\ .. MSFT. MIB* **>** *мрипсап. mof*</span><span class="sxs-lookup"><span data-stu-id="a0fa8-160">**Smi2smir /g** *..\\..\\mripsap.mib..\\..\\msft.mib* **>** *mripsap.mof*</span></span>

<span data-ttu-id="a0fa8-161">**Smi2smir/g** *.. \\ . \\ мсипбтп. MIB \\ . \\ .. MSFT. MIB* **>** *мсипбтп. mof*</span><span class="sxs-lookup"><span data-stu-id="a0fa8-161">**Smi2smir /g** *..\\..\\msipbtp.mib..\\..\\msft.mib* **>** *msipbtp.mof*</span></span>

<span data-ttu-id="a0fa8-162">**Smi2smir/g** *.. \\ . \\ msiprip2. MIB \\ . \\ .. MSFT. MIB* **>** *msiprip2. mof*</span><span class="sxs-lookup"><span data-stu-id="a0fa8-162">**Smi2smir /g** *..\\..\\msiprip2.mib..\\..\\msft.mib* **>** *msiprip2.mof*</span></span>

## <a name="adding-snmp-mof-files-to-the-wmi-repository"></a><span data-ttu-id="a0fa8-163">Добавление MOF-файлов SNMP в репозиторий WMI</span><span class="sxs-lookup"><span data-stu-id="a0fa8-163">Adding SNMP MOF Files to the WMI Repository</span></span>

<span data-ttu-id="a0fa8-164">Следующие команды являются примером добавления MOF-файлов, созданных из файлов MIB, в репозиторий WMI.</span><span class="sxs-lookup"><span data-stu-id="a0fa8-164">The following commands are an example of how to add the MOF files that are generated from the MIB files to the WMI repository.</span></span> <span data-ttu-id="a0fa8-165">Если вы хотите добавить MOF-файлы в список файлов, которые будут автоматически восстановлены в процессе восстановления в [*репозитории WMI*](gloss-w.md) , добавьте флаг **— Автовосстановление** в конец каждой команды.</span><span class="sxs-lookup"><span data-stu-id="a0fa8-165">If you want to add the MOF files to the list of files to be automatically restored in a [*WMI repository*](gloss-w.md) recovery, add the **-AUTORECOVER** flag to the end of each command.</span></span> <span data-ttu-id="a0fa8-166">Дополнительные сведения о средстве командной строки WMI Mofcomp.exe см. в разделе [**mofcomp**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="a0fa8-166">For more information about the WMI Mofcomp.exe command-line tool, see [**mofcomp**](mofcomp.md).</span></span>

<span data-ttu-id="a0fa8-167">**mofcomp** *хостмиб. mof*</span><span class="sxs-lookup"><span data-stu-id="a0fa8-167">**mofcomp** *hostmib.mof*</span></span>

<span data-ttu-id="a0fa8-168">**mofcomp** *ипфорвд. mof*</span><span class="sxs-lookup"><span data-stu-id="a0fa8-168">**mofcomp** *ipforwd.mof*</span></span>

<span data-ttu-id="a0fa8-169">**mofcomp** *нипкс. mof*</span><span class="sxs-lookup"><span data-stu-id="a0fa8-169">**mofcomp** *nipx.mof*</span></span>

<span data-ttu-id="a0fa8-170">**mofcomp** *MIB \_ II. mof*</span><span class="sxs-lookup"><span data-stu-id="a0fa8-170">**mofcomp** *mib\_ii.mof*</span></span>

<span data-ttu-id="a0fa8-171">**mofcomp** *lmmib2. mof*</span><span class="sxs-lookup"><span data-stu-id="a0fa8-171">**mofcomp** *lmmib2.mof*</span></span>

<span data-ttu-id="a0fa8-172">**mofcomp** *мкастмиб. mof*</span><span class="sxs-lookup"><span data-stu-id="a0fa8-172">**mofcomp** *mcastmib.mof*</span></span>

<span data-ttu-id="a0fa8-173">**mofcomp** *rfc2571. mof*</span><span class="sxs-lookup"><span data-stu-id="a0fa8-173">**mofcomp** *rfc2571.mof*</span></span>

<span data-ttu-id="a0fa8-174">**mofcomp** *вфоспф. mof*</span><span class="sxs-lookup"><span data-stu-id="a0fa8-174">**mofcomp** *wfospf.mof*</span></span>

<span data-ttu-id="a0fa8-175">**mofcomp** *DHCP. mof*</span><span class="sxs-lookup"><span data-stu-id="a0fa8-175">**mofcomp** *dhcp.mof*</span></span>

<span data-ttu-id="a0fa8-176">**mofcomp** *мипкс. mof*</span><span class="sxs-lookup"><span data-stu-id="a0fa8-176">**mofcomp** *mipx.mof*</span></span>

<span data-ttu-id="a0fa8-177">**mofcomp** *мрипсап. mof*</span><span class="sxs-lookup"><span data-stu-id="a0fa8-177">**mofcomp** *mripsap.mof*</span></span>

<span data-ttu-id="a0fa8-178">**mofcomp** *мсипбтп. mof*</span><span class="sxs-lookup"><span data-stu-id="a0fa8-178">**mofcomp** *msipbtp.mof*</span></span>

<span data-ttu-id="a0fa8-179">**mofcomp** *msiprip2. mof*</span><span class="sxs-lookup"><span data-stu-id="a0fa8-179">**mofcomp** *msiprip2.mof*</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0fa8-180">См. также</span><span class="sxs-lookup"><span data-stu-id="a0fa8-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0fa8-181">Доступ к SNMP-устройствам</span><span class="sxs-lookup"><span data-stu-id="a0fa8-181">Accessing SNMP Devices</span></span>](accessing-snmp-devices.md)
</dt> </dl>

 

 
