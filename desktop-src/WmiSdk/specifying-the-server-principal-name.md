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
# <a name="specifying-the-server-principal-name"></a>Указание имени участника на сервере

Служба проверки подлинности Kerberos задает имя участника на сервере, чтобы обеспечить идентификацию компьютера, к которому он подключается. Укажите имя участника-сервера в вызове метода скрипта [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md) , указав имя удаленного компьютера. В C++ укажите имя участника на сервере в параметре *псерверпринкнаме* при вызове [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) для прокси-сервера. Дополнительные сведения см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).

Этот параметр необходим для поддержки взаимной проверки подлинности Kerberos. Однако использование имени участника сервера по умолчанию не допускает взаимной проверки подлинности. Клиенты, для которых важна взаимная проверка подлинности, должны указывать имя участника на сервере, совпадающее с удостоверением сервера, используемым службой WMI. Дополнительные сведения о настройке безопасности прокси-сервера и примеры кода на C++, показывающие, как задать имя участника на сервере, см. в разделе [Настройка параметров безопасности для IWbemServices и других прокси](setting-the-security-on-iwbemservices-and-other-proxies.md)-серверов.

Дополнительные сведения о настройке имени участника-сервера в скрипте и Visual Basic см. в разделе [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md) и [Подключение к инструментарию WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).

В отличие от большинства протоколов безопасности для инструментарий управления Windows (WMI) (WMI) и модели компонентных объектов (COM), нельзя задать сервер-участник в вызове [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). Однако можно задать сервер-участник с параметром *бстраусорити* для [**Ивбемлокатор:: коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)или параметром *псерверпринкнаме* для [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

В примере кода в этом разделе \# для правильной компиляции требуется следующая инструкция include.


```C++
#include <wbemidl.h>
```



В следующем примере кода показано, как задать имя участника на сервере с помощью [**коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Настройка службы проверки подлинности с помощью VBScript](setting-the-authentication-service-using-vbscript.md)
</dt> <dt>

[Настройка проверки подлинности с помощью C++](setting-authentication-using-c-.md)
</dt> <dt>

[Настройка безопасности для IWbemServices и других прокси-серверов](setting-the-security-on-iwbemservices-and-other-proxies.md)
</dt> </dl>

 

 
