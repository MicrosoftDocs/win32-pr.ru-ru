---
description: Для подключения к пространству имен WMI на удаленном компьютере может потребоваться изменить параметры брандмауэра Windows, контроля учетных записей пользователей (UAC), DCOM или диспетчера объектов модель CIM (CIMOM).
ms.assetid: 028b3101-0945-4288-bf32-ef4ad12a55f9
ms.tgt_platform: multiple
title: Настройка удаленного WMI-подключения
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6ee254e12ecd806cd286d4a55746e203a3136b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544847"
---
# <a name="setting-up-a-remote-wmi-connection"></a><span data-ttu-id="97b60-103">Настройка удаленного WMI-подключения</span><span class="sxs-lookup"><span data-stu-id="97b60-103">Setting up a Remote WMI Connection</span></span>

<span data-ttu-id="97b60-104">Для подключения к пространству имен WMI на удаленном компьютере может потребоваться изменить параметры [брандмауэра Windows](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), [контроля учетных записей пользователей (UAC)](/previous-versions/aa905108(v=msdn.10)), DCOM или ДИСПЕТЧЕРА объектов модель CIM (CIMOM).</span><span class="sxs-lookup"><span data-stu-id="97b60-104">Connecting to a WMI namespace on a remote computer may require that you change the settings for [Windows Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), [User Account Control (UAC)](/previous-versions/aa905108(v=msdn.10)), DCOM, or Common Information Model Object Manager (CIMOM).</span></span>

<span data-ttu-id="97b60-105">В этом разделе обсуждаются следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="97b60-105">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="97b60-106">Параметры брандмауэра Windows</span><span class="sxs-lookup"><span data-stu-id="97b60-106">Windows Firewall Settings</span></span>](#windows-firewall-settings)
-   [<span data-ttu-id="97b60-107">Параметры контроля учетных записей</span><span class="sxs-lookup"><span data-stu-id="97b60-107">User Account Control Settings</span></span>](#user-account-control-settings)
-   [<span data-ttu-id="97b60-108">Параметры DCOM</span><span class="sxs-lookup"><span data-stu-id="97b60-108">DCOM Settings</span></span>](#dcom-settings)
-   [<span data-ttu-id="97b60-109">Параметры CIMOM</span><span class="sxs-lookup"><span data-stu-id="97b60-109">CIMOM Settings</span></span>](#cimom-settings)
-   [<span data-ttu-id="97b60-110">См. также</span><span class="sxs-lookup"><span data-stu-id="97b60-110">Related topics</span></span>](#related-topics)

## <a name="windows-firewall-settings"></a><span data-ttu-id="97b60-111">Параметры брандмауэра Windows</span><span class="sxs-lookup"><span data-stu-id="97b60-111">Windows Firewall Settings</span></span>

<span data-ttu-id="97b60-112">Параметры WMI для параметров брандмауэра Windows позволяют использовать только подключения WMI, а не другие приложения DCOM.</span><span class="sxs-lookup"><span data-stu-id="97b60-112">WMI settings for Windows Firewall settings enable only WMI connections, rather than other DCOM applications as well.</span></span>

<span data-ttu-id="97b60-113">Необходимо задать исключение в брандмауэре для инструментария WMI на удаленном целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="97b60-113">An exception must be set in the firewall for WMI on the remote target computer.</span></span> <span data-ttu-id="97b60-114">Исключение для WMI позволяет инструментарию WMI принимать удаленные подключения и асинхронные обратные вызовы для Unsecapp.exe.</span><span class="sxs-lookup"><span data-stu-id="97b60-114">The exception for WMI allows WMI to receive remote connections and asynchronous callbacks to Unsecapp.exe.</span></span> <span data-ttu-id="97b60-115">Дополнительные сведения см. [в разделе Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="97b60-115">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="97b60-116">Если клиентское приложение создает собственный приемник, этот приемник необходимо явно добавить в исключения брандмауэра, чтобы разрешить успешные обратные вызовы.</span><span class="sxs-lookup"><span data-stu-id="97b60-116">If a client application creates its own sink, that sink must be explicitly added to the firewall exceptions to allow callbacks to succeed.</span></span>

<span data-ttu-id="97b60-117">Исключение для WMI также работает, если Инструментарий WMI запущен с фиксированным портом с помощью команды **Winmgmt/стандалонехост** .</span><span class="sxs-lookup"><span data-stu-id="97b60-117">The exception for WMI also works if WMI has been started with a fixed port, using the **winmgmt /standalonehost** command.</span></span> <span data-ttu-id="97b60-118">Дополнительные сведения см. [в разделе Настройка фиксированного порта для WMI](setting-up-a-fixed-port-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="97b60-118">For more information, see [Setting Up a Fixed Port for WMI](setting-up-a-fixed-port-for-wmi.md).</span></span>

<span data-ttu-id="97b60-119">Вы можете включить или отключить трафик WMI с помощью пользовательского интерфейса брандмауэра Windows.</span><span class="sxs-lookup"><span data-stu-id="97b60-119">You can enable or disable WMI traffic through the Windows Firewall UI.</span></span>

<span data-ttu-id="97b60-120">**Включение или отключение трафика WMI с помощью пользовательского интерфейса брандмауэра**</span><span class="sxs-lookup"><span data-stu-id="97b60-120">**To enable or disable WMI traffic using firewall UI**</span></span>

1.  <span data-ttu-id="97b60-121">На **панели управления** щелкните **Безопасность** , а затем — **Брандмауэр Windows**.</span><span class="sxs-lookup"><span data-stu-id="97b60-121">In the **Control Panel**, click **Security** and then click **Windows Firewall**.</span></span>
2.  <span data-ttu-id="97b60-122">Щелкните **изменить параметры** , а затем перейдите на вкладку **исключения** .</span><span class="sxs-lookup"><span data-stu-id="97b60-122">Click **Change Settings** and then click the **Exceptions** tab.</span></span>
3.  <span data-ttu-id="97b60-123">В окне Исключения установите флажок для **инструментарий управления Windows (WMI) (WMI)** , чтобы включить трафик WMI через брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="97b60-123">In the Exceptions window, select the check box for **Windows Management Instrumentation (WMI)** to enable WMI traffic through the firewall.</span></span> <span data-ttu-id="97b60-124">Чтобы отключить трафик WMI, снимите флажок.</span><span class="sxs-lookup"><span data-stu-id="97b60-124">To disable WMI traffic, clear the check box.</span></span>

<span data-ttu-id="97b60-125">Вы можете включить или отключить трафик WMI через брандмауэр в командной строке.</span><span class="sxs-lookup"><span data-stu-id="97b60-125">You can enable or disable WMI traffic through the firewall at the command prompt.</span></span>

<span data-ttu-id="97b60-126">**Включение или отключение трафика WMI в командной строке с помощью группы правил WMI**</span><span class="sxs-lookup"><span data-stu-id="97b60-126">**To enable or disable WMI traffic at command prompt using WMI rule group**</span></span>

-   <span data-ttu-id="97b60-127">Используйте следующие команды в командной строке.</span><span class="sxs-lookup"><span data-stu-id="97b60-127">Use the following commands at a command prompt.</span></span> <span data-ttu-id="97b60-128">Введите следующую команду, чтобы включить трафик WMI через брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="97b60-128">Type the following to enable WMI traffic through the firewall.</span></span>

    <span data-ttu-id="97b60-129">**netsh advfirewall firewall set Rule Group = "Инструментарий управления Windows (WMI)" новое включение = да**</span><span class="sxs-lookup"><span data-stu-id="97b60-129">**netsh advfirewall firewall set rule group="windows management instrumentation (wmi)" new enable=yes**</span></span>

    <span data-ttu-id="97b60-130">Введите следующую команду, чтобы отключить трафик WMI через брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="97b60-130">Type the following command to disable WMI traffic through the firewall.</span></span>

    <span data-ttu-id="97b60-131">**netsh advfirewall firewall set Rule Group = "Инструментарий управления Windows (WMI)" новое включение = нет**</span><span class="sxs-lookup"><span data-stu-id="97b60-131">**netsh advfirewall firewall set rule group="windows management instrumentation (wmi)" new enable=no**</span></span>

<span data-ttu-id="97b60-132">Вместо использования одной команды группы правил WMI можно также использовать отдельные команды для каждой DCOM, службы WMI и приемника.</span><span class="sxs-lookup"><span data-stu-id="97b60-132">Rather than using the single WMI rule group command, you also can use individual commands for each of the DCOM, WMI service, and sink.</span></span>

<span data-ttu-id="97b60-133">**Включение трафика WMI с помощью отдельных правил для DCOM, WMI, приемника обратного вызова и исходящих подключений**</span><span class="sxs-lookup"><span data-stu-id="97b60-133">**To enable WMI traffic using separate rules for DCOM, WMI, callback sink and outgoing connections**</span></span>

1.  <span data-ttu-id="97b60-134">Чтобы установить исключение брандмауэра для порта DCOM 135, используйте следующую команду.</span><span class="sxs-lookup"><span data-stu-id="97b60-134">To establish a firewall exception for DCOM port 135, use the following command.</span></span>

    <span data-ttu-id="97b60-135">**netsh advfirewall Firewall добавить правило dir = in Name = "DCOM" Program =% systemroot% \\ system32 \\svchost.exe Service = RPCSS Action = Allow Protocol = TCP localPort = 135**</span><span class="sxs-lookup"><span data-stu-id="97b60-135">**netsh advfirewall firewall add rule dir=in name="DCOM" program=%systemroot%\\system32\\svchost.exe service=rpcss action=allow protocol=TCP localport=135**</span></span>

2.  <span data-ttu-id="97b60-136">Чтобы установить исключение брандмауэра для службы WMI, используйте следующую команду.</span><span class="sxs-lookup"><span data-stu-id="97b60-136">To establish a firewall exception for the WMI service, use the following command.</span></span>

    <span data-ttu-id="97b60-137">**netsh advfirewall Firewall Add правило dir = in Name = "WMI" Program =% системный_корневой_каталог% \\ system32 \\svchost.exe Service = Winmgmt Action = Allow Protocol = TCP localPort = Any**</span><span class="sxs-lookup"><span data-stu-id="97b60-137">**netsh advfirewall firewall add rule dir=in name ="WMI" program=%systemroot%\\system32\\svchost.exe service=winmgmt action = allow protocol=TCP localport=any**</span></span>

3.  <span data-ttu-id="97b60-138">Чтобы установить исключение брандмауэра для приемника, который получает обратные вызовы с удаленного компьютера, используйте следующую команду.</span><span class="sxs-lookup"><span data-stu-id="97b60-138">To establish a firewall exception for the sink that receives callbacks from a remote computer, use the following command.</span></span>

    <span data-ttu-id="97b60-139">**netsh advfirewall Firewall добавить правило dir = in имя = "Унсекапп" Program =% systemroot% \\ system32 \\ WBEM \\unsecapp.exe действие = разрешить**</span><span class="sxs-lookup"><span data-stu-id="97b60-139">**netsh advfirewall firewall add rule dir=in name ="UnsecApp" program=%systemroot%\\system32\\wbem\\unsecapp.exe action=allow**</span></span>

4.  <span data-ttu-id="97b60-140">Чтобы установить исключение брандмауэра для исходящих подключений к удаленному компьютеру, с которым локальный компьютер обменивается данными в асинхронном режиме, используйте следующую команду.</span><span class="sxs-lookup"><span data-stu-id="97b60-140">To establish a firewall exception for outgoing connections to a remote computer that the local computer is communicating with asynchronously, use the following command.</span></span>

    <span data-ttu-id="97b60-141">**netsh advfirewall Firewall добавить правило DIR = OUT имя = "WMI \_ out" программа =% SystemRoot% \\ system32 \\svchost.exe служба = Winmgmt Action = разрешить протокол = TCP localPort = Any**</span><span class="sxs-lookup"><span data-stu-id="97b60-141">**netsh advfirewall firewall add rule dir=out name ="WMI\_OUT" program=%systemroot%\\system32\\svchost.exe service=winmgmt action=allow protocol=TCP localport=any**</span></span>

<span data-ttu-id="97b60-142">Чтобы отключить исключения брандмауэра по отдельности, используйте следующие команды.</span><span class="sxs-lookup"><span data-stu-id="97b60-142">To disable the firewall exceptions separately, use the following commands.</span></span>

<span data-ttu-id="97b60-143">**Отключение трафика WMI с помощью отдельных правил для DCOM, WMI, приемника обратного вызова и исходящих подключений**</span><span class="sxs-lookup"><span data-stu-id="97b60-143">**To disable WMI traffic using separate rules for DCOM, WMI, callback sink and outgoing connections**</span></span>

1.  <span data-ttu-id="97b60-144">Для отключения исключения DCOM.</span><span class="sxs-lookup"><span data-stu-id="97b60-144">To disable the DCOM exception.</span></span>

    <span data-ttu-id="97b60-145">**netsh advfirewall Firewall Delete Rule Name = "DCOM"**</span><span class="sxs-lookup"><span data-stu-id="97b60-145">**netsh advfirewall firewall delete rule name="DCOM"**</span></span>

2.  <span data-ttu-id="97b60-146">Для отключения исключения службы WMI.</span><span class="sxs-lookup"><span data-stu-id="97b60-146">To disable the WMI service exception.</span></span>

    <span data-ttu-id="97b60-147">**netsh advfirewall Firewall Delete Rule Name = "WMI"**</span><span class="sxs-lookup"><span data-stu-id="97b60-147">**netsh advfirewall firewall delete rule name="WMI"**</span></span>

3.  <span data-ttu-id="97b60-148">Для отключения исключения приемника.</span><span class="sxs-lookup"><span data-stu-id="97b60-148">To disable the sink exception.</span></span>

    <span data-ttu-id="97b60-149">**netsh advfirewall Firewall Delete Rule Name = "Унсекапп"**</span><span class="sxs-lookup"><span data-stu-id="97b60-149">**netsh advfirewall firewall delete rule name="UnsecApp"**</span></span>

4.  <span data-ttu-id="97b60-150">, Чтобы отключить исходящее исключение.</span><span class="sxs-lookup"><span data-stu-id="97b60-150">To disable the outgoing exception.</span></span>

    <span data-ttu-id="97b60-151">**netsh advfirewall Firewall удаление правила Name = "WMI \_ out"**</span><span class="sxs-lookup"><span data-stu-id="97b60-151">**netsh advfirewall firewall delete rule name="WMI\_OUT"**</span></span>

## <a name="user-account-control-settings"></a><span data-ttu-id="97b60-152">Параметры контроля учетных записей</span><span class="sxs-lookup"><span data-stu-id="97b60-152">User Account Control Settings</span></span>

<span data-ttu-id="97b60-153">Управление учетными записями пользователей (UAC) — фильтрация маркеров может влиять на то, какие операции разрешены в пространствах имен WMI или какие данные возвращаются.</span><span class="sxs-lookup"><span data-stu-id="97b60-153">User Account Control (UAC) access-token filtering can affect which operations are allowed in WMI namespaces or what data is returned.</span></span> <span data-ttu-id="97b60-154">В разделе UAC все учетные записи в локальной группе "Администраторы" выполняются с [*маркером доступа*](/windows/desktop/SecGloss/a-gly)обычного пользователя, также известным как фильтрация маркера доступа UAC.</span><span class="sxs-lookup"><span data-stu-id="97b60-154">Under UAC, all accounts in the local Administrators group run with a standard user [*access token*](/windows/desktop/SecGloss/a-gly), also known as UAC access-token filtering.</span></span> <span data-ttu-id="97b60-155">Учетная запись администратора может выполнять скрипт с повышенными привилегиями — "Запуск от имени администратора".</span><span class="sxs-lookup"><span data-stu-id="97b60-155">An administrator account can run a script with an elevated privilege—"Run as Administrator".</span></span>

<span data-ttu-id="97b60-156">При отсутствии подключения к встроенной учетной записи администратора UAC влияет на подключения к удаленному компьютеру по-разному в зависимости от того, находятся ли два компьютера в домене или рабочей группе.</span><span class="sxs-lookup"><span data-stu-id="97b60-156">When you are not connecting to the built-in Administrator account, UAC affects connections to a remote computer differently depending on whether the two computers are in a domain or a workgroup.</span></span> <span data-ttu-id="97b60-157">Дополнительные сведения об UAC и удаленных подключениях см. в разделе [Управление учетными записями пользователей и инструментарий WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="97b60-157">For more information about UAC and remote connections, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

## <a name="dcom-settings"></a><span data-ttu-id="97b60-158">Параметры DCOM</span><span class="sxs-lookup"><span data-stu-id="97b60-158">DCOM Settings</span></span>

<span data-ttu-id="97b60-159">Дополнительные сведения о параметрах DCOM см. в разделе [Защита удаленного WMI-подключения](securing-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="97b60-159">For more information on DCOM settings, see [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md).</span></span> <span data-ttu-id="97b60-160">Однако UAC влияет на подключения для недоменных учетных записей пользователей.</span><span class="sxs-lookup"><span data-stu-id="97b60-160">However, UAC affects connections for nondomain user accounts.</span></span> <span data-ttu-id="97b60-161">При подключении к удаленному компьютеру с использованием недоменной учетной записи пользователя, входящей в локальную группу администраторов удаленного компьютера, необходимо явным образом предоставить учетной записи права удаленного доступа DCOM, активации и запуска.</span><span class="sxs-lookup"><span data-stu-id="97b60-161">If you connect to a remote computer using a nondomain user account included in the local Administrators group of the remote computer, then you must explicitly grant remote DCOM access, activation, and launch rights to the account.</span></span>

## <a name="cimom-settings"></a><span data-ttu-id="97b60-162">Параметры CIMOM</span><span class="sxs-lookup"><span data-stu-id="97b60-162">CIMOM Settings</span></span>

<span data-ttu-id="97b60-163">Необходимо обновить параметры CIMOM, если удаленное подключение установлено между компьютерами, не имеющими отношения доверия. в противном случае асинхронное соединение завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="97b60-163">The CIMOM settings need to be updated if the remote connection is between computers that do not have a trust relationship; otherwise, an asynchronous connection will fail.</span></span> <span data-ttu-id="97b60-164">Этот параметр не следует изменять для компьютеров в том же домене или в доверенных доменах.</span><span class="sxs-lookup"><span data-stu-id="97b60-164">This setting should not be modified for computers in the same domain or in trusted domains.</span></span>

<span data-ttu-id="97b60-165">Чтобы разрешить анонимный обратный вызов, необходимо изменить следующую запись реестра:</span><span class="sxs-lookup"><span data-stu-id="97b60-165">The following registry entry needs to be modified to allow anonymous callbacks:</span></span>

<span data-ttu-id="97b60-166">**HKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **аллованонимаускаллбакк**</span><span class="sxs-lookup"><span data-stu-id="97b60-166">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**AllowAnonymousCallback**</span></span><dl> <dt>

               Data type
</dt> <dd>               <span data-ttu-id="97b60-167">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="97b60-167">REG\_DWORD</span></span></dd> </dl>

<span data-ttu-id="97b60-168">Если значение **аллованонимаускаллбакк** равно 0, то служба WMI предотвращает анонимный обратный вызов клиента.</span><span class="sxs-lookup"><span data-stu-id="97b60-168">If the **AllowAnonymousCallback** value is set to 0, the WMI service prevents anonymous callbacks to the client.</span></span> <span data-ttu-id="97b60-169">Если значение равно 1, служба WMI разрешает клиенту анонимные обратные вызовы.</span><span class="sxs-lookup"><span data-stu-id="97b60-169">If the value is set to 1, the WMI service allows anonymous callbacks to the client.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97b60-170">См. также</span><span class="sxs-lookup"><span data-stu-id="97b60-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97b60-171">Подключение к инструментарию WMI на удаленном компьютере</span><span class="sxs-lookup"><span data-stu-id="97b60-171">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
