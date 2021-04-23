---
description: При доступе к серверу инструментарий управления Windows (WMI) (WMI) с помощью скрипта можно выбрать между протоколами проверки подлинности NT LAN Manager (NTLM) или Kerberos.
ms.assetid: db2dc750-bfdd-4f6c-859b-e104814f0800
ms.tgt_platform: multiple
title: Настройка службы проверки подлинности с помощью VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bd2cf444560aac7ebce96b52d9abaa528bdcaa76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712946"
---
# <a name="setting-the-authentication-service-using-vbscript"></a><span data-ttu-id="74c27-103">Настройка службы проверки подлинности с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="74c27-103">Setting the Authentication Service Using VBScript</span></span>

<span data-ttu-id="74c27-104">При доступе к серверу инструментарий управления Windows (WMI) (WMI) с помощью скрипта можно выбрать между протоколами проверки подлинности NT LAN Manager (NTLM) или Kerberos.</span><span class="sxs-lookup"><span data-stu-id="74c27-104">When accessing a Windows Management Instrumentation (WMI) server with a script, you can choose between NT LAN Manager (NTLM) or Kerberos authentication protocols.</span></span> <span data-ttu-id="74c27-105">Указание Kerberos не требуется, кроме случаев использования делегирования.</span><span class="sxs-lookup"><span data-stu-id="74c27-105">Specifying Kerberos is not required except when using delegation.</span></span> <span data-ttu-id="74c27-106">Дополнительные сведения см. в разделе [Подключение к третьим компьютерам-делегирование](connecting-to-a-3rd-computer-delegation.md).</span><span class="sxs-lookup"><span data-stu-id="74c27-106">For more information, see [Connecting to a 3rd Computer-Delegation](connecting-to-a-3rd-computer-delegation.md).</span></span>

<span data-ttu-id="74c27-107">Поскольку версии операционной системы отличаются от используемых ими служб проверки подлинности, рекомендуется не указывать значение для поля Authority при подключении к удаленной системе.</span><span class="sxs-lookup"><span data-stu-id="74c27-107">Because operating system versions differ in which authentication service they use, it is recommended that you do not specify a value for the authority field when connecting to a remote system.</span></span> <span data-ttu-id="74c27-108">Вместо этого разрешите операционной системе и распределенной версии модели объектов (DCOM) выбрать NTLM или Kerberos.</span><span class="sxs-lookup"><span data-stu-id="74c27-108">Instead, allow the operating system and distributed version of Component Object Model (DCOM) to select NTLM or Kerberos.</span></span> <span data-ttu-id="74c27-109">Если указана служба проверки подлинности, для синтаксиса требуется имя участника на сервере, то есть имя целевого компьютера, а не контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="74c27-109">If an authentication service is specified, the syntax requires the server principal name, which is the name of the target computer rather than the domain controller.</span></span>

<span data-ttu-id="74c27-110">Параметр Authority можно использовать только с подключениями к удаленным серверам WMI.</span><span class="sxs-lookup"><span data-stu-id="74c27-110">You can use the authority parameter only with connections to remote WMI servers.</span></span> <span data-ttu-id="74c27-111">Попытка соединения завершится неудачей, если вы попытаетесь установить уровни авторизации как часть моникера или с помощью вызова [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md) для локального соединения.</span><span class="sxs-lookup"><span data-stu-id="74c27-111">The connection attempt fails if you attempt to set authorization levels as part of a moniker or with a call to [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) for a local connection.</span></span>

<span data-ttu-id="74c27-112">Выполните следующую процедуру, чтобы указать службу проверки подлинности, которую необходимо использовать в параметре *страусорити* метода [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md) или в соединении строки [моникера](constructing-a-moniker-string.md) .</span><span class="sxs-lookup"><span data-stu-id="74c27-112">Perform the following procedure to specify the authentication service that you want to use in the *strAuthority* parameter of the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method or the [moniker](constructing-a-moniker-string.md) string connection.</span></span>

<span data-ttu-id="74c27-113">**Указание проверки подлинности NTLM или Kerberos с помощью API скриптов для WMI**</span><span class="sxs-lookup"><span data-stu-id="74c27-113">**To specify NTLM or Kerberos authentication with the Scripting API for WMI**</span></span>

1.  <span data-ttu-id="74c27-114">Если параметр *страусорити* начинается со строки "Kerberos:", WMI предполагает, что строка ссылается на имя участника Kerberos и используется проверка подлинности Kerberos.</span><span class="sxs-lookup"><span data-stu-id="74c27-114">If the *strAuthority* parameter begins with the string "kerberos:", WMI assumes the string refers to a Kerberos principal name and Kerberos authentication is used.</span></span> <span data-ttu-id="74c27-115">Если параметр *страусорити* начинается со строки "нтлмдомаин:", WMI использует проверку подлинности NTLM.</span><span class="sxs-lookup"><span data-stu-id="74c27-115">If the *strAuthority* parameter begins with the string "ntlmdomain:", WMI uses NTLM authentication instead.</span></span>
2.  <span data-ttu-id="74c27-116">Кроме того, можно использовать часть полномочия моникера для указания типа проверки подлинности, используемой для подключения к WMI.</span><span class="sxs-lookup"><span data-stu-id="74c27-116">Alternately, You can use the authority part of a moniker to specify the type of authentication used to connect to WMI.</span></span> <span data-ttu-id="74c27-117">Чтобы использовать проверку подлинности Kerberos при использовании моникера, укажите строку "Authority = Kerberos:", за которой следует имя участника.</span><span class="sxs-lookup"><span data-stu-id="74c27-117">To use Kerberos authentication when using a moniker include the string, "authority=kerberos:" followed by the principal name.</span></span> <span data-ttu-id="74c27-118">Чтобы использовать проверку подлинности NTLM, включите строку "Authority = нтлмдомаин:", за которой следует имя домена NTLM.</span><span class="sxs-lookup"><span data-stu-id="74c27-118">To use NTLM authentication, include the string, "authority=ntlmdomain:" followed by the NTLM domain name.</span></span>

    <span data-ttu-id="74c27-119">В следующем примере показан моникер, запрашивающий проверку подлинности Kerberos с помощью основного \\ сервера "MyDomain".</span><span class="sxs-lookup"><span data-stu-id="74c27-119">The following example shows you a moniker that requests Kerberos authentication using the principal "mydomain\\server".</span></span>

    ```VB
    winmgmts:{impersonationLevel=delegate, _
            authority=kerberos:mydomain\server} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

    <span data-ttu-id="74c27-120">В следующем примере показан моникер, который запрашивает проверку подлинности NTLM с использованием домена mydomain.</span><span class="sxs-lookup"><span data-stu-id="74c27-120">In contrast, the following example shows you a moniker that requests NTLM authentication using the domain "mydomain".</span></span>

    ```VB
    winmgmts:{impersonationLevel=impersonate, _
            authority=ntlmdomain:mydomain} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

 

 



