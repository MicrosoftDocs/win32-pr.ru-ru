---
description: Можно потребовать, чтобы клиентские скрипты и приложения установили зашифрованное подключение для проверки подлинности, добавив квалификатор Рекуиресенкриптион в MOF-файл MOF-файл (MOF), который создает пространство имен.
ms.assetid: 07b225a2-3834-4879-beae-f5b9180d112f
ms.tgt_platform: multiple
title: Требуется зашифрованное соединение с пространством имен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42415c0f714f99a51d6a1a0ee1a0b22f398b1b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693638"
---
# <a name="requiring-an-encrypted-connection-to-a-namespace"></a><span data-ttu-id="c3d2a-103">Требуется зашифрованное соединение с пространством имен</span><span class="sxs-lookup"><span data-stu-id="c3d2a-103">Requiring an Encrypted Connection to a Namespace</span></span>

<span data-ttu-id="c3d2a-104">Можно потребовать, чтобы клиентские скрипты и приложения установили зашифрованное подключение для проверки подлинности, добавив квалификатор **рекуиресенкриптион** в MOF-файл MOF-файл (MOF), который создает пространство имен.</span><span class="sxs-lookup"><span data-stu-id="c3d2a-104">You can require that client scripts and applications establish an encrypted connection for authentication by adding the **RequiresEncryption** qualifier to the Managed Object Format (MOF) .mof file that creates the namespace.</span></span>


<span data-ttu-id="c3d2a-105">Зашифрованное соединение с пространством имен WMI указывает на проверку подлинности **RPC \_ C \_ AUTHN \_ Level \_ PKT \_** (или **пктприваци** в сценарии).</span><span class="sxs-lookup"><span data-stu-id="c3d2a-105">An encrypted connection to a WMI namespace specifies **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** (or **PktPrivacy** in a script) for authentication.</span></span> <span data-ttu-id="c3d2a-106">Квалификатор **рекуиресенкриптион** заставляет Инструментарий WMI отклонять любые входящие запросы к данным, если они явно не используют зашифрованную проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="c3d2a-106">The **RequiresEncryption** qualifier causes WMI to reject any incoming data requests unless they explicitly use encrypted authentication.</span></span> <span data-ttu-id="c3d2a-107">Дополнительные сведения см. [в разделе Задание уровня безопасности процесса по умолчанию с помощью VBScript](setting-the-default-process-security-level-using-vbscript.md) или [Настройка проверки подлинности с помощью C++](setting-authentication-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="c3d2a-107">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md) or [Setting Authentication Using C++](setting-authentication-using-c-.md).</span></span>

<span data-ttu-id="c3d2a-108">Можно также изменить существующее пространство имен, добавив этот атрибут, а затем снова скомпилировать MOF-файл.</span><span class="sxs-lookup"><span data-stu-id="c3d2a-108">You can also modify an existing namespace by adding this attribute and then compile the MOF file again.</span></span> <span data-ttu-id="c3d2a-109">**Рекуиресенкриптион** используется в [*MOF*](gloss-m.md) с помощью инструкции препроцессора [директивы pragma Namespace](pragma-namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="c3d2a-109">**RequiresEncryption** is used in [*MOF*](gloss-m.md) with the [pragma namespace](pragma-namespace.md) preprocessor instruction.</span></span>

<span data-ttu-id="c3d2a-110">Следующая процедура задает для пространства имен требование зашифрованного соединения.</span><span class="sxs-lookup"><span data-stu-id="c3d2a-110">The following procedure sets the namespace to require an encrypted connection.</span></span>

<span data-ttu-id="c3d2a-111">**Настройка обязательного шифрования**</span><span class="sxs-lookup"><span data-stu-id="c3d2a-111">**To set required encryption**</span></span>

1.  <span data-ttu-id="c3d2a-112">Создайте MOF-файл (MOF-файл) или измените существующий MOF-файл, определяющий пространство имен.</span><span class="sxs-lookup"><span data-stu-id="c3d2a-112">Create a Managed Object Format (MOF) file or modify your existing MOF file that defines the namespace.</span></span>

    <span data-ttu-id="c3d2a-113">В следующем примере кода показано пространство имен, которое будет изменено, — *root \\ MyNamespace* , а файл — с именем *MyNamespace \_ Security. mof*.</span><span class="sxs-lookup"><span data-stu-id="c3d2a-113">The following code example shows the namespace that will be modified is *root\\MyNamespace* and the file is named *MyNamespace\_security.mof*.</span></span> <span data-ttu-id="c3d2a-114">**Рекуиресенкриптион** имеет логический тип данных, поэтому для него должно быть задано **значение true** или **false**.</span><span class="sxs-lookup"><span data-stu-id="c3d2a-114">**RequiresEncryption** has a Boolean datatype so it must be set to **True** or **False**.</span></span>

    ```mof
    #pragma namespace("\\\\.\\Root\\MyNamespace") 

    [RequiresEncryption(TRUE)] 
    instance of __systemSecurity { };
    ```

    

2.  <span data-ttu-id="c3d2a-115">Запустите [**mofcomp.exe**](mofcomp.md) , чтобы скомпилировать MOF-файл.</span><span class="sxs-lookup"><span data-stu-id="c3d2a-115">Run [**mofcomp.exe**](mofcomp.md) to compile the MOF file.</span></span>

    <span data-ttu-id="c3d2a-116">**c: \\ mofcomp MyNamespace \_ Security. mof**</span><span class="sxs-lookup"><span data-stu-id="c3d2a-116">**c:\\mofcomp MyNamespace\_security.mof**</span></span>

    <span data-ttu-id="c3d2a-117">В C++ используйте методы [**имофкомпилер**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="c3d2a-117">In C++, use the [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) methods.</span></span>

<span data-ttu-id="c3d2a-118">WMI отклоняет клиент, использующий уровень проверки подлинности по умолчанию, так как DCOM согласовывает безопасность с уровнем, необходимым процессу SVCHOST, в котором запущена служба WMI.</span><span class="sxs-lookup"><span data-stu-id="c3d2a-118">WMI rejects a client that uses the default authentication level because DCOM negotiates the security to the level required by the SVCHOST process in which the WMI service is running.</span></span> <span data-ttu-id="c3d2a-119">Дополнительные сведения о размещении служб см. в разделе [размещение и безопасность поставщика](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="c3d2a-119">For more information about service hosts, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span> <span data-ttu-id="c3d2a-120">Дополнительные сведения о настройке уровней проверки подлинности при подключении к пространствам имен WMI см. в статьях [Настройка уровня безопасности процесса по умолчанию с помощью c++](setting-the-default-process-security-level-using-c-.md), [Настройка проверки подлинности с помощью C++](setting-authentication-using-c-.md)или [Установка уровня безопасности процесса по умолчанию с помощью VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="c3d2a-120">For more information about setting authentication levels when connecting to WMI namespaces, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md), [Setting Authentication Using C++](setting-authentication-using-c-.md), or [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

<span data-ttu-id="c3d2a-121">При возврате данных через асинхронное соединение обратного вызова Инструментарий WMI возвращает запрашивающему компьютеру сообщение об отказе в доступе.</span><span class="sxs-lookup"><span data-stu-id="c3d2a-121">When returning data on an asynchronous callback connection, WMI returns an access denied message to the requesting computer.</span></span> <span data-ttu-id="c3d2a-122">Кроме того, Инструментарий WMI создает запись в журнале событий NT компьютера с зашифрованным пространством имен, указывая, что для клиента невозможно установить безопасное соединение.</span><span class="sxs-lookup"><span data-stu-id="c3d2a-122">WMI also makes a log entry in the NT Event Log of the computer with the encrypted namespace stating that a secure connection cannot be established to the client.</span></span>

<span data-ttu-id="c3d2a-123">Начиная с Windows Vista файл Вбемкоре. log больше не существует.</span><span class="sxs-lookup"><span data-stu-id="c3d2a-123">Starting with Windows Vista, the WbemCore.log file no longer exists.</span></span> <span data-ttu-id="c3d2a-124">Можно проверить журнал событий NT на наличие записей, указывающих на отклоненные входящие запросы к данным, для пространств имен, требующих шифрования.</span><span class="sxs-lookup"><span data-stu-id="c3d2a-124">You can check the NT Event Log for entries indicating rejected inbound data requests to namespaces that require encryption.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3d2a-125">См. также</span><span class="sxs-lookup"><span data-stu-id="c3d2a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3d2a-126">Настройка дескрипторов безопасности Намепаце</span><span class="sxs-lookup"><span data-stu-id="c3d2a-126">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="c3d2a-127">**вбемаусентикатионлевеленум**</span><span class="sxs-lookup"><span data-stu-id="c3d2a-127">**WbemAuthenticationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[<span data-ttu-id="c3d2a-128">Защита удаленного WMI-подключения</span><span class="sxs-lookup"><span data-stu-id="c3d2a-128">Securing a Remote WMI Connection</span></span>](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 



