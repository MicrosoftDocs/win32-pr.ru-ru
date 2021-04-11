---
title: Доступ к удаленным компьютерам
description: Для доступа к данным на локальном или удаленном компьютере можно использовать API журнала событий Windows.
ms.assetid: df789981-0e1c-4d68-9bd5-5d054f1724d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e0063238560ddd7f1613e94b83ecc7f27900bb3
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2020
ms.locfileid: "104133599"
---
# <a name="accessing-remote-computers"></a>Доступ к удаленным компьютерам

Для доступа к данным на локальном или удаленном компьютере можно использовать API журнала событий Windows. Чтобы получить доступ к данным на удаленном компьютере, необходимо вызвать функцию [**евтопенсессион**](/windows/desktop/api/WinEvt/nf-winevt-evtopensession) , чтобы создать контекст удаленного сеанса. При вызове этой функции указывается имя удаленного компьютера, к которому необходимо подключиться, учетные данные пользователя, используемые для подключения, и тип проверки подлинности, используемый для проверки подлинности пользователя. Чтобы указать текущего пользователя, задайте для членов домена, пользователя и пароля **значение NULL**.

При вызове API журнала событий Windows этот обработчик передается в контекст удаленного сеанса, возвращаемый функцией [**евтопенсессион**](/windows/desktop/api/WinEvt/nf-winevt-evtopensession) . (Чтобы получить доступ к данным на локальном компьютере, передайте **значение NULL** , чтобы указать сеанс по умолчанию.) Для доступа к данным на удаленном компьютере удаленный компьютер должен включить удаленное управление журналом событий, исключение брандмауэра Windows. в противном случае при попытке использовать обработчик сеанса произойдет ошибка, так как сервер RPC \_ S \_ \_ недоступен. Компьютер, к которому выполняется подключение, должен работать под управлением Windows Vista или более поздней версии.

В следующем примере показано, как подключиться к удаленному компьютеру.


```C++
#include <windows.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

EVT_HANDLE ConnectToRemote(LPWSTR lpwszRemote);
void EnumProviders(EVT_HANDLE hRemote);

void main(void)
{
    EVT_HANDLE hRemote = NULL;
    LPWSTR pwsComputerName = L"<name of the remote computer goes here>";
    

    // Enumerate the registered providers on the local computer.
    wprintf(L"Registered providers on the local computer\n\n");
    EnumProviders(hRemote);

    hRemote = ConnectToRemote(pwsComputerName);
    if (NULL == hRemote)
    {
        wprintf(L"Failed to connect to remote computer. Error code is %d.\n", GetLastError());
        goto cleanup;
    }

    // Enumerate the registered providers on the remote computer.
    // To access a remote computer, the remote computer must enable 
    // Remote Event Log Management as an exception in the firewall;
    // otherwise, the remote call fails with RPC_S_SERVER_UNAVAILABLE.
    wprintf(L"\n\nRegistered providers on the remote computer\n\n");
    EnumProviders(hRemote);

cleanup:

    if (hRemote)
        EvtClose(hRemote);
}

// Create a session conext for the remote computer. Set the 
// Domain, User, and Password member to NULL to specify
// the current user.
EVT_HANDLE ConnectToRemote(LPWSTR lpwszRemote)
{
    EVT_HANDLE hRemote = NULL;
    EVT_RPC_LOGIN Credentials;

    RtlZeroMemory(&Credentials, sizeof(EVT_RPC_LOGIN));
    Credentials.Server = lpwszRemote;
    Credentials.Domain = NULL; 
    Credentials.User = NULL; 
    Credentials.Password = NULL; 
    Credentials.Flags = EvtRpcLoginAuthNegotiate; 

    // This call creates a remote session context; it does not actually
    // create a connection to the remote computer. The connection to
    // the remote computer happens when you use the context.
    hRemote = EvtOpenSession(EvtRpcLogin, &Credentials, 0, 0);

    SecureZeroMemory(&Credentials, sizeof(EVT_RPC_LOGIN));

    return hRemote;
}

// Enumerate the registered providers on the computer.
void EnumProviders(EVT_HANDLE hRemote)
{
    EVT_HANDLE hPublishers = NULL;
    WCHAR wszPublisherName[255 + 1];
    DWORD dwBufferUsed = 0;
    DWORD status = ERROR_SUCCESS;

    hPublishers = EvtOpenPublisherEnum(hRemote, 0);
    if (NULL == hPublishers)
    {
        wprintf(L"EvtOpenPublisherEnum failed with %d\n", GetLastError());
        goto cleanup;
    }

    while (true)
    {
        if (EvtNextPublisherId(hPublishers, sizeof(wszPublisherName)/sizeof(WCHAR), wszPublisherName, &dwBufferUsed))
        {
            wprintf(L"%s\n", wszPublisherName);
        }
        else
        {
            status = GetLastError();
            if (ERROR_NO_MORE_ITEMS == status)
            {
                break;
            }
            else
            {
                wprintf(L"EvtNextPublisherId failed with 0x%ud\n", GetLastError());
            }
        }
    }

cleanup:

    if (hPublishers)
        EvtClose(hPublishers);
}
```
