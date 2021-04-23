---
description: В следующих разделах описываются распространенные проблемы, с которыми могут столкнуться разработчики при создании удаленного WMI-подключения.
ms.assetid: 328e420b-a859-4ce9-8a31-67150eb0a78f
ms.tgt_platform: multiple
title: Устранение неполадок удаленного WMI-подключения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae475f91836b9e99b1c7faaf149c452e00a66722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692691"
---
# <a name="troubleshooting-a-remote-wmi-connection"></a><span data-ttu-id="75d8c-103">Устранение неполадок удаленного WMI-подключения</span><span class="sxs-lookup"><span data-stu-id="75d8c-103">Troubleshooting a Remote WMI Connection</span></span>

<span data-ttu-id="75d8c-104">В следующих разделах описываются распространенные проблемы, с которыми могут столкнуться разработчики при создании удаленного WMI-подключения.</span><span class="sxs-lookup"><span data-stu-id="75d8c-104">The following sections describe common issues developers may have with creating a remote WMI connection.</span></span>

<span data-ttu-id="75d8c-105">В этом разделе обсуждаются следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="75d8c-105">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="75d8c-106">Отказано в доступе DCOM</span><span class="sxs-lookup"><span data-stu-id="75d8c-106">DCOM Access Denied</span></span>](#dcom-access-denied)
-   [<span data-ttu-id="75d8c-107">Не удалось подключиться</span><span class="sxs-lookup"><span data-stu-id="75d8c-107">Failure to Connect</span></span>](#failure-to-connect)
-   [<span data-ttu-id="75d8c-108">Истекло время ожидания подключения WMI</span><span class="sxs-lookup"><span data-stu-id="75d8c-108">WMI Connection Timed Out</span></span>](#wmi-connection-timed-out)
-   [<span data-ttu-id="75d8c-109">См. также</span><span class="sxs-lookup"><span data-stu-id="75d8c-109">Related topics</span></span>](#related-topics)

## <a name="dcom-access-denied"></a><span data-ttu-id="75d8c-110">Отказано в доступе DCOM</span><span class="sxs-lookup"><span data-stu-id="75d8c-110">DCOM Access Denied</span></span>

<dl> <dt>

<span data-ttu-id="75d8c-111"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Случай</span><span class="sxs-lookup"><span data-stu-id="75d8c-111"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Symptom</span></span>
</dt> <dd>

<span data-ttu-id="75d8c-112">произошел сбой подключения с ошибкой "DCOM-доступ запрещен", а также десятичное значение-2147024891 или шестнадцатеричный value0x80070005.</span><span class="sxs-lookup"><span data-stu-id="75d8c-112">your connection failed with the error "DCOM Access Denied", along with the decimal value -2147024891 or hex value0x80070005.</span></span>

</dd> <dt>

<span data-ttu-id="75d8c-113"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Issue</span><span class="sxs-lookup"><span data-stu-id="75d8c-113"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Issue</span></span>
</dt> <dd>

<span data-ttu-id="75d8c-114">Невозможно настроить DCOM для разрешения WMI-подключения.</span><span class="sxs-lookup"><span data-stu-id="75d8c-114">DCOM may not be configured to allow a WMI connection.</span></span>

</dd> <dt>

<span data-ttu-id="75d8c-115"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Разрешением</span><span class="sxs-lookup"><span data-stu-id="75d8c-115"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Resolution</span></span>
</dt> <dd>

<span data-ttu-id="75d8c-116">Параметры DCOM для WMI можно настроить с помощью служебной программы настройки DCOM (**DCOMCnfg.exe**), которая находится в **меню "Администрирование** " на **панели управления**.</span><span class="sxs-lookup"><span data-stu-id="75d8c-116">You can configure DCOM settings for WMI using the DCOM Config utility (**DCOMCnfg.exe**) found in **Administrative Tools** in **Control Panel**.</span></span> <span data-ttu-id="75d8c-117">Эта программа предоставляет параметры, позволяющие определенным пользователям подключаться к компьютеру удаленно через DCOM.</span><span class="sxs-lookup"><span data-stu-id="75d8c-117">This utility exposes the settings that enable certain users to connect to the computer remotely through DCOM.</span></span> <span data-ttu-id="75d8c-118">Члены группы "Администраторы" могут удаленно подключаться к компьютеру по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="75d8c-118">Members of the Administrators group are allowed to remotely connect to the computer by default.</span></span> <span data-ttu-id="75d8c-119">С помощью этой служебной программы можно настроить безопасность для запуска, доступа и настройки службы WMI.</span><span class="sxs-lookup"><span data-stu-id="75d8c-119">With this utility you can set the security to start, access, and configure the WMI service.</span></span>

<span data-ttu-id="75d8c-120">Дополнительные сведения см. [в разделе Защита удаленного WMI-подключения](securing-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="75d8c-120">For more information, see [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md).</span></span>

</dd> </dl>

## <a name="failure-to-connect"></a><span data-ttu-id="75d8c-121">Не удалось подключиться</span><span class="sxs-lookup"><span data-stu-id="75d8c-121">Failure to Connect</span></span>

<dl> <dt>

<span data-ttu-id="75d8c-122"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Случай</span><span class="sxs-lookup"><span data-stu-id="75d8c-122"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Symptom</span></span>
</dt> <dd>

<span data-ttu-id="75d8c-123">Невозможно подключиться к инструментарию WMI в удаленной системе.</span><span class="sxs-lookup"><span data-stu-id="75d8c-123">You cannot connect to WMI on a remote system.</span></span>

</dd> <dt>

<span data-ttu-id="75d8c-124"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Issue</span><span class="sxs-lookup"><span data-stu-id="75d8c-124"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Issue</span></span>
</dt> <dd>

<span data-ttu-id="75d8c-125">Возможно, вы пытаетесь подключиться к системе, которая не поддерживает Инструментарий WMI.</span><span class="sxs-lookup"><span data-stu-id="75d8c-125">You may be trying to connect to a system that does not support WMI.</span></span> <span data-ttu-id="75d8c-126">Следующие подключения между версиями операционной системы не поддерживаются:</span><span class="sxs-lookup"><span data-stu-id="75d8c-126">The following connections between operating system versions are not supported:</span></span>

-   <span data-ttu-id="75d8c-127">Невозможно подключиться к компьютеру, на котором выполняется начальное, базовое или Домашняя версии.</span><span class="sxs-lookup"><span data-stu-id="75d8c-127">You cannot connect to a computer that is running a Starter, Basic, or Home edition.</span></span>

<span data-ttu-id="75d8c-128">Кроме того, возможно, вы пытаетесь подключиться к пространству имен, для которого требуется зашифрованное соединение, которое требует уровня проверки подлинности `pktPrivacy` , **Вбемаусентикатионлевелпктприваци** или **RPC \_ C \_ AUTHN на \_ уровне \_ \_ безопасности PKT**.</span><span class="sxs-lookup"><span data-stu-id="75d8c-128">Alternately, you may be trying to connect to a namespace which requires an encrypted connection, one that requires an authentication level of `pktPrivacy`, **WbemAuthenticationLevelPktPrivacy**, or **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span>

</dd> <dt>

<span data-ttu-id="75d8c-129"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Разрешением</span><span class="sxs-lookup"><span data-stu-id="75d8c-129"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Resolution</span></span>
</dt> <dd>

<span data-ttu-id="75d8c-130">Дополнительные сведения см. в статьях [Защита пространств имен WMI](securing-wmi-namespaces.md), [Защита клиентов и поставщиков C++](securing-c---clients-and-providers.md)или [Установка уровня безопасности процесса по умолчанию с помощью VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="75d8c-130">For more information, see [Securing WMI Namespaces](securing-wmi-namespaces.md), [Securing C++ Clients and Providers](securing-c---clients-and-providers.md), or [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

</dd> </dl>

## <a name="wmi-connection-timed-out"></a><span data-ttu-id="75d8c-131">Истекло время ожидания подключения WMI</span><span class="sxs-lookup"><span data-stu-id="75d8c-131">WMI Connection Timed Out</span></span>

<dl> <dt>

<span data-ttu-id="75d8c-132"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Случай</span><span class="sxs-lookup"><span data-stu-id="75d8c-132"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Symptom</span></span>
</dt> <dd>

<span data-ttu-id="75d8c-133">Истекло время ожидания подключения WMI.</span><span class="sxs-lookup"><span data-stu-id="75d8c-133">Your WMI connection times out.</span></span>

</dd> <dt>

<span data-ttu-id="75d8c-134"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Issue</span><span class="sxs-lookup"><span data-stu-id="75d8c-134"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Issue</span></span>
</dt> <dd>

<span data-ttu-id="75d8c-135">Из-за проблем с задержкой сети компьютер просто не может ответить вовремя.</span><span class="sxs-lookup"><span data-stu-id="75d8c-135">Due to network lag issues, the computer is simply not able to respond in time.</span></span>

</dd> <dt>

<span data-ttu-id="75d8c-136"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Разрешением</span><span class="sxs-lookup"><span data-stu-id="75d8c-136"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Resolution</span></span>
</dt> <dd>

<span data-ttu-id="75d8c-137">При подключении к инструментарию WMI с помощью вызова [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md) или [**Ивбемлокатор:: коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)можно задать флаг **вбемконнектфлагусемаксваит** (скрипт) или установить **\_ флаг WBEM \_ Connect \_ использовать максимальное время \_ \_ ожидания** в C++ значение 128 (0x80), чтобы наложить в вызове два (2) минуты.</span><span class="sxs-lookup"><span data-stu-id="75d8c-137">When connecting to WMI through a call to [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) or [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), you can set the **wbemConnectFlagUseMaxWait** flag (scripting) or the **WBEM\_FLAG\_CONNECT\_USE\_MAX\_WAIT** in C++ value to 128 (0x80) to impose a two (2) minute time-out on the call.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="75d8c-138">См. также</span><span class="sxs-lookup"><span data-stu-id="75d8c-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75d8c-139">Подключение к инструментарию WMI на удаленном компьютере</span><span class="sxs-lookup"><span data-stu-id="75d8c-139">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 



