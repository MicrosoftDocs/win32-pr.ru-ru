---
description: 'Одна из основных задач Ивбемлокатор:: Коннектсервер для WMI — возврат указателя на прокси-сервер IWbemServices.'
ms.assetid: bbff43b7-79f8-4c7b-a772-d3d962cf3859
ms.tgt_platform: multiple
title: Настройка проверки подлинности с помощью C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7b0ef3bcd1e9908815c94dacc3815fec77eaea33f2da48119dbe3178563eae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315621"
---
# <a name="setting-authentication-using-c"></a>Настройка проверки подлинности с помощью C++

Одна из основных задач [**ивбемлокатор:: коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) для WMI — возврат указателя на прокси-сервер [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) . С помощью прокси-сервера **IWbemServices** можно получить доступ к ВОЗМОЖНОСТЯМ инфраструктуры WMI. Однако указатель на прокси-сервер **IWbemServices** имеет идентификатор процесса клиентского приложения, а не удостоверение процесса **IWbemServices** . Поэтому при попытке доступа к **IWbemServices** с помощью указателя можно получить код, запрещенный для доступа, такой как **E \_ ACCESSDENIED**. Чтобы избежать ошибки отказа в доступе, необходимо задать удостоверение нового указателя с помощью вызова интерфейса [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .

Поставщик может установить безопасность для пространства имен таким образом, чтобы никакие данные не возвращались, если только вы не используете конфиденциальность пакетов (**пктприваци**) в подключении к этому пространству имен. Это гарантирует, что данные шифруются по мере пересечения сети. При попытке задать более низкий уровень проверки подлинности будет получено сообщение об отказе в доступе. Дополнительные сведения см. в разделе [Настройка дескрипторов безопасности намепаце](setting-namespace-security-descriptors.md).

Дополнительные сведения о настройке проверки подлинности в скриптах см. в разделе [Задание уровня безопасности процесса по умолчанию с помощью VBScript](setting-the-default-process-security-level-using-vbscript.md).

## <a name="setting-security-on-a-remote-iunknown-interface"></a>Настройка безопасности на удаленном интерфейсе IUnknown

В некоторых ситуациях требуется больший доступ к серверу, чем просто указатель на прокси-сервер. Иногда может потребоваться получить безопасное подключение к интерфейсу [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) прокси. С помощью **IUnknown** можно выполнять запросы к удаленной системе для интерфейсов и других необходимых методов.

Если прокси-сервер расположен на удаленном компьютере, сервер делегирует все вызовы интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) прокси-сервера интерфейсу **IUnknown** . Например, при вызове [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) на прокси-сервере, а запрошенный интерфейс не был частью прокси-сервера, прокси-сервер отправляет вызов удаленному серверу. Удаленный сервер, в свою очередь, проверяет наличие соответствующей поддержки интерфейса. Если сервер поддерживает интерфейс, COM маршалирует новый прокси обратно клиенту, чтобы приложение может использовать новый интерфейс.

Проблемы возникают, если клиент не имеет разрешений на доступ к удаленному серверу, но использует учетные данные пользователя, который выполняет. В этом случае любая попытка доступа к [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) на удаленном сервере завершается сбоем. В окончательном выпуске прокси-сервера также происходит сбой, так как текущий пользователь не имеет доступа к удаленному серверу. Симптомом этого является одна или две секунды, прежде чем клиентское приложение завершится сбоем окончательной версии прокси-сервера. Сбой происходит из-за того, что COM пытается получить доступ к удаленному серверу, используя параметры безопасности по умолчанию текущего пользователя, которые не включают измененные учетные данные, которым разрешен доступ к серверу в первую очередь. Дополнительные сведения см. в разделе [Настройка параметров безопасности для IWbemServices и других учетных записей-посредников](setting-the-security-on-iwbemservices-and-other-proxies.md).

Чтобы избежать сбоя соединения, используйте метод [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) , чтобы явно задать проверку подлинности в указателе, возвращенном из [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). С помощью **CoSetProxyBlanket** можно убедиться, что удаленный сервер получает правильный идентификатор проверки подлинности.

В следующем примере кода показано, как использовать [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) для доступа к удаленному интерфейсу [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .


```C++
SEC_WINNT_AUTH_IDENTITY_W* pAuthIdentity = 
   new SEC_WINNT_AUTH_IDENTITY_W;
ZeroMemory(pAuthIdentity, sizeof(SEC_WINNT_AUTH_IDENTITY_W));

pAuthIdentity->User = new WCHAR[32];
StringCbCopyW(pAuthIdentity->User,sizeof(L"MyUser"),L"MyUser");
pAuthIdentity->UserLength = wcslen(pAuthIdentity->User);

pAuthIdentity->Domain = new WCHAR[32];
StringCbCopyW(pAuthIdentity->Domain,sizeof(L"MyDomain"),L"MyDomain");
pAuthIdentity->DomainLength = wcslen(pAuthIdentity->Domain);

pAuthIdentity->Password = new WCHAR[32];
pAuthIdentity->Password[0] = NULL;
pAuthIdentity->PasswordLength = wcslen( pAuthIdentity->Password);

pAuthIdentity->Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;

IWbemServices* pWbemServices = 0;

// Set proxy security
hr = CoSetProxyBlanket(pWbemServices, 
                       RPC_C_AUTHN_DEFAULT, 
                       RPC_C_AUTHZ_NONE, 
                       COLE_DEFAULT_PRINCIPAL, 
                       RPC_C_AUTHN_LEVEL_DEFAULT, 
                       RPC_C_IMP_LEVEL_IMPERSONATE, 
                       pAuthIdentity, 
                       EOAC_NONE 
);
if (FAILED(hr))
{
   cout << "Count not set proxy blanket. Error code = 0x"
        << hex << hr << endl;
   pWbemServices->Release();
   return 1;
}

// Set IUnknown security
IUnknown*    pUnk = NULL;
pWbemServices->QueryInterface(IID_IUnknown, (void**) &pUnk);

hr = CoSetProxyBlanket(pUnk, 
                       RPC_C_AUTHN_DEFAULT, 
                       RPC_C_AUTHZ_NONE, 
                       COLE_DEFAULT_PRINCIPAL, 
                       RPC_C_AUTHN_LEVEL_DEFAULT, 
                       RPC_C_IMP_LEVEL_IMPERSONATE, 
                       pAuthIdentity, 
                       EOAC_NONE 
);
if (FAILED(hr))
{
   cout << "Count not set proxy blanket. Error code = 0x"
        << hex << hr << endl;
   pUnk->Release();
   pWbemServices->Release();
   delete [] pAuthIdentity->User;
   delete [] pAuthIdentity->Domain;
   delete [] pAuthIdentity->Password;
   delete pAuthIdentity;   
   return 1;
}

// cleanup IUnknown
pUnk->Release();

//
// Perform a bunch of operations
//

// Cleanup
pWbemServices->Release();

delete [] pAuthIdentity->User;
delete [] pAuthIdentity->Domain;
delete [] pAuthIdentity->Password;

delete pAuthIdentity;
```



> [!Note]  
> При настройке безопасности для интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) прокси-сервера COM создает копию прокси-сервера, которую невозможно освободить, пока не будет вызван метод [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Настройка проверки подлинности в WMI](setting-authentication-in-wmi.md)
</dt> </dl>

 

 
