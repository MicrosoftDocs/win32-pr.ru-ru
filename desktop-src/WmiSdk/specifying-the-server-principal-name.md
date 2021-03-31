---
description: Служба проверки подлинности Kerberos задает имя участника на сервере, чтобы обеспечить идентификацию компьютера, к которому он подключается.
ms.assetid: 3d58db28-2e69-4e27-9f27-61529abbf750
ms.tgt_platform: multiple
title: Указание имени участника на сервере
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a2f5aa4053b5ae7452e5f5e9c0ddcac15630ae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155850"
---
# <a name="specifying-the-server-principal-name"></a><span data-ttu-id="4412c-103">Указание имени участника на сервере</span><span class="sxs-lookup"><span data-stu-id="4412c-103">Specifying the Server Principal Name</span></span>

<span data-ttu-id="4412c-104">Служба проверки подлинности Kerberos задает имя участника на сервере, чтобы обеспечить идентификацию компьютера, к которому он подключается.</span><span class="sxs-lookup"><span data-stu-id="4412c-104">The Kerberos authentication service specifies the server principal name to ensure the identity of the computer to which it is connecting.</span></span> <span data-ttu-id="4412c-105">Укажите имя участника-сервера в вызове метода скрипта [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md) , указав имя удаленного компьютера.</span><span class="sxs-lookup"><span data-stu-id="4412c-105">Specify the server principal name in the call to the scripting method [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) by giving the name of the remote computer.</span></span> <span data-ttu-id="4412c-106">В C++ укажите имя участника на сервере в параметре *псерверпринкнаме* при вызове [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) для прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="4412c-106">In C++, specify the server principal name in the *pServerPrincName* parameter when calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) for the proxy.</span></span> <span data-ttu-id="4412c-107">Дополнительные сведения см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="4412c-107">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="4412c-108">Этот параметр необходим для поддержки взаимной проверки подлинности Kerberos.</span><span class="sxs-lookup"><span data-stu-id="4412c-108">This parameter is required for Kerberos to support mutual authentication.</span></span> <span data-ttu-id="4412c-109">Однако использование имени участника сервера по умолчанию не допускает взаимной проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="4412c-109">However, using the default server principal name does not allow mutual authentication.</span></span> <span data-ttu-id="4412c-110">Клиенты, для которых важна взаимная проверка подлинности, должны указывать имя участника на сервере, совпадающее с удостоверением сервера, используемым службой WMI.</span><span class="sxs-lookup"><span data-stu-id="4412c-110">Clients for which mutual authentication is critical, must specify a server principal name that matches the server identity that the WMI service is using.</span></span> <span data-ttu-id="4412c-111">Дополнительные сведения о настройке безопасности прокси-сервера и примеры кода на C++, показывающие, как задать имя участника на сервере, см. в разделе [Настройка параметров безопасности для IWbemServices и других прокси](setting-the-security-on-iwbemservices-and-other-proxies.md)-серверов.</span><span class="sxs-lookup"><span data-stu-id="4412c-111">For more information about setting proxy security and a C++ example showing how to set the server principal name, see [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

<span data-ttu-id="4412c-112">Дополнительные сведения о настройке имени участника-сервера в скрипте и Visual Basic см. в разделе [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md) и [Подключение к инструментарию WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="4412c-112">For more information about setting the server principal name in script and Visual Basic, see [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) and [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="4412c-113">В отличие от большинства протоколов безопасности для инструментарий управления Windows (WMI) (WMI) и модели компонентных объектов (COM), нельзя задать сервер-участник в вызове [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="4412c-113">Unlike most security protocols for Windows Management Instrumentation (WMI) and Component Object Model (COM), you cannot set the server principal in a call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="4412c-114">Однако можно задать сервер-участник с параметром *бстраусорити* для [**Ивбемлокатор:: коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)или параметром *псерверпринкнаме* для [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="4412c-114">However, you can set the server principal with the *bstrAuthority* parameter for [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), or the *pServerPrincName* parameter for [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

<span data-ttu-id="4412c-115">В примере кода в этом разделе \# для правильной компиляции требуется следующая инструкция include.</span><span class="sxs-lookup"><span data-stu-id="4412c-115">The code example in this topic requires the following \#include statement to correctly compile.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="4412c-116">В следующем примере кода показано, как задать имя участника на сервере с помощью [**коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="4412c-116">The following code example shows how to set the server principal name with [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span>


```C++
IWbemServices* g_pNameSpace = NULL;

// Namespace to which to connect
BSTR  bstrNameSpace = 
SysAllocString( L"\\\\MyMachine\\root\default" );

// The bstrAuthority string contains the server
// principal name MyDomain\\MyMachine
// and the authentication service, which is Kerberos.
BSTR  bstrAuthority = 
SysAllocString( L"kerberos:MyDomain\\MyMachine"  );

HRESULT hr = NULL;
IWbemLocator* pWbemLocator = 0;

  hr = pWbemLocator->ConnectServer(
          bstrNameSpace,  // NameSpace name
          NULL,           // User name
          NULL,           // Password
          NULL,           // Locale
          0L,             // Security flags
          bstrAuthority,  // Authority, server principal name
          NULL,           // WBEM context
          &g_pNameSpace   // Namespace
          );

  // Free memory resources.
  g_pNameSpace->Release();
  SysFreeString(bstrNameSpace);
  SysFreeString(bstrAuthority);
```



## <a name="related-topics"></a><span data-ttu-id="4412c-117">См. также</span><span class="sxs-lookup"><span data-stu-id="4412c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4412c-118">Настройка службы проверки подлинности с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="4412c-118">Setting the Authentication Service Using VBScript</span></span>](setting-the-authentication-service-using-vbscript.md)
</dt> <dt>

[<span data-ttu-id="4412c-119">Настройка проверки подлинности с помощью C++</span><span class="sxs-lookup"><span data-stu-id="4412c-119">Setting Authentication Using C++</span></span>](setting-authentication-using-c-.md)
</dt> <dt>

[<span data-ttu-id="4412c-120">Настройка безопасности для IWbemServices и других прокси-серверов</span><span class="sxs-lookup"><span data-stu-id="4412c-120">Setting the Security on IWbemServices and Other Proxies</span></span>](setting-the-security-on-iwbemservices-and-other-proxies.md)
</dt> </dl>

 

 
