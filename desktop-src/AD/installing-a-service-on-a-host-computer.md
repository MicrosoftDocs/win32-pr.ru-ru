---
title: Установка службы на главном компьютере
description: В следующем примере кода показаны основные шаги установки службы с поддержкой каталогов на главном компьютере.
ms.assetid: 35a3b261-d499-4154-a022-1e33a9ef7ba8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d0d22098b0a6b823aa5b7db50c20b5a5e2c80c7e540ffdb95e4e2f73c2550fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187392"
---
# <a name="installing-a-service-on-a-host-computer"></a>Установка службы на главном компьютере

В следующем примере кода показаны основные шаги установки службы с поддержкой каталогов на главном компьютере. Она выполняет следующие операции:

1.  Вызывает функцию [**OpenSCManager**](/windows/desktop/api/winsvc/nf-winsvc-openscmanagera) для открытия на локальном компьютере маркера диспетчера управления СЛУЖБАМИ (SCM).
2.  Вызывает функцию [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) для установки службы в базе данных SCM. Этот вызов задает учетную запись входа и пароль службы, а также исполняемый файл службы и другие сведения о службе. **CreateService** завершается ошибкой, если указана недопустимая учетная запись входа. Однако **CreateService** не проверяет допустимость пароля. Он также не проверяет, имеет ли учетная запись право входа в качестве службы на локальном компьютере. Дополнительные сведения см. в разделе [предоставление входных данных в качестве службы непосредственно на главном компьютере](granting-logon-as-service-right-on-the-host-computer.md).
3.  Вызывает подпрограммы **скпкреате** службы, которая создает объект точки подключения службы (SCP) в каталоге для публикации расположения этого экземпляра службы. Дополнительные сведения см. [в статье как клиенты находят и используют точку подключения службы](how-clients-find-and-use-a-service-connection-point.md). Эта подпрограммы также хранит сведения о привязке службы в SCP, устанавливает ACE на SCP, чтобы служба могла обращаться к ней во время выполнения, кэширует различающееся имя SCP в локальном реестре и возвращает различающееся имя новой точки подключения службы.
4.  Вызывает подпрограммы **спнкомпосе** службы, которая использует строку класса службы, и различающееся имя SCP для создания имени участника-службы (SPN). Дополнительные сведения см. [в разделе Составление имен участников-служб для службы с SCP](composing-the-spns-for-a-service-with-an-scp.md). Имя субъекта-службы однозначно определяет этот экземпляр службы.
5.  Вызывает подпрограммы **спнрегистер** службы, которая регистрирует SPN в объекте учетной записи, связанном с учетной записью входа службы. Дополнительные сведения см. [в статье регистрация имен участников-служб для службы](registering-the-spns-for-a-service.md). Регистрация имени участника-службы позволяет клиентским приложениям проходить проверку подлинности службы.

Этот пример кода работает правильно независимо от того, является ли учетная запись входа локальной или учетной записью пользователя домена или учетной записью LocalSystem. Для учетной записи пользователя домена параметр *сзсервицеаккаунтсам* содержит *домен * **\\** имя _пользователя_ учетной записи, а параметр *сзсервицеаккаунтдн* содержит различающееся имя объекта учетной записи пользователя в каталоге. Для учетной записи LocalSystem *сзсервицеаккаунтсам* и *Сзпассворд* имеют **значение NULL**, а *сзсервицеаккаунтсн* — различающееся имя объекта учетной записи локального компьютера в каталоге. Если *сзсервицеаккаунтсам* указывает локальную учетную запись пользователя (формат имени — \\ ").* UserName * "), в примере кода пропускается регистрация имени участника-службы, так как взаимная проверка подлинности не поддерживается для локальных учетных записей пользователей.

Имейте в виду, что конфигурация безопасности по умолчанию позволяет только администраторам домена выполнять этот код.

Кроме того, обратите внимание, что этот пример кода, как написано, должен выполняться на компьютере, где устанавливается служба. Следовательно, обычно он находится в отдельном исполняемом файле установки из кода установки службы, если таковой имеется, который расширяет схему, расширяет пользовательский интерфейс или настраивает групповую политику. Эти операции устанавливают компоненты службы для всего леса, в то время как этот код устанавливает службу на одном компьютере.


```C++
void InstallServiceOnLocalComputer(
            LPTSTR szServiceAccountDN,  // Distinguished name of logon account.
            LPTSTR szServiceAccountSAM, // SAM name of logon account.
            LPTSTR szPassword)          // Password of logon account.
{
SC_HANDLE   schService = NULL;
SC_HANDLE   schSCManager = NULL;
TCHAR szPath[512];
LPTSTR lpFilePart;
TCHAR szDNofSCP[MAX_PATH];
TCHAR szServiceClass[]=TEXT("ADSockAuth");
 
DWORD dwStatus;
TCHAR **pspn=NULL;
ULONG ulSpn=1;
 
// Get the full path of the service's executable.
// The code example assumes that the executable is in the current directory.
dwStatus = GetFullPathName(TEXT("service.exe"), 512, szPath, &lpFilePart);
if (dwStatus == 0) {
    _tprintf(TEXT("Unable to install %s - %s\n"), 
            TEXT(SZSERVICEDISPLAYNAME), GetLastErrorText(szErr, 256));
    return;
}
_tprintf(TEXT("path of service.exe: %s\n"), szPath);
 
// Open the Service Control Manager on the local computer.
schSCManager = OpenSCManager(
                NULL,                   // Computer (NULL == local)
                NULL,                   // Database (NULL == default)
                SC_MANAGER_ALL_ACCESS   // Access required
                );
if (! schSCManager) {
    _tprintf(TEXT("OpenSCManager failed - %s\n"), 
                   GetLastErrorText(szErr,256));
    goto cleanup;
}
        
// Install the service in the SCM database.
schService = CreateService(
            schSCManager,               // SCManager database
            TEXT(SZSERVICENAME),        // Name of service
            TEXT(SZSERVICEDISPLAYNAME), // Name to display
            SERVICE_ALL_ACCESS,         // Desired access
            SERVICE_WIN32_OWN_PROCESS,  // Service type
            SERVICE_DEMAND_START,       // Start type
            SERVICE_ERROR_NORMAL,       // Error control type
            szPath,                     // Service binary
            NULL,                       // No load ordering group
            NULL,                       // No tag identifier
            TEXT(SZDEPENDENCIES),       // Dependencies
            szServiceAccountSAM,        // Service account
            szPassword);                // Account password
if (! schService) {
    _tprintf(TEXT("CreateService failed - %s\n"), 
                   GetLastErrorText(szErr,256));
    goto cleanup;
}
 
_tprintf(TEXT("%s installed.\n"), TEXT(SZSERVICEDISPLAYNAME) );
 
// Create the service's Service Connection Point (SCP).
dwStatus = ScpCreate(
        2000,                 // Service default port number
        szServiceClass,       // Specifies the service class string
        szServiceAccountSAM,  // SAM name of logon account for ACE
        szDNofSCP             // Buffer returns the DN of the SCP
        );
if (dwStatus != 0) {
    _tprintf(TEXT("ScpCreate failed: %d\n"), dwStatus );
    DeleteService(schService);
    goto cleanup;
}
 
// Compose and register a service principal name for this service.
// This is performed on the install path because this requires elevated
// privileges for updating the directory.
// If a local account of the format ".\user name", skip the SPN.
if ( szServiceAccountSAM[0] == '.' ) 
{
    _tprintf(TEXT("Do not register SPN for a local account.\n"));
    goto cleanup;
}
 
dwStatus = SpnCompose(
        &pspn,            // Receives pointer to the SPN array.
        &ulSpn,           // Receives number of SPNs returned.
        szDNofSCP,        // Input: DN of the SCP.
        szServiceClass);  // Input: the service's class string.
 
if (dwStatus == NO_ERROR) 
    dwStatus = SpnRegister(
        szServiceAccountDN,  // Account on which SPNs are registered.
        pspn,                // Array of SPNs to register.
        ulSpn,               // Number of SPNs in array.
        DS_SPN_ADD_SPN_OP);  // Operation code: Add SPNs.
 
if (dwStatus != NO_ERROR) 
{
    _tprintf(TEXT("Failed to compose SPN: Error was %X\n"), 
                  dwStatus);
    DeleteService(schService);
    ScpDelete(szDNofSCP, szServiceClass, szServiceAccountDN);
    goto cleanup;
}
 
cleanup:
if (schSCManager)
    CloseServiceHandle(schSCManager);
if (schService)
    CloseServiceHandle(schService);
DsFreeSpnArray(ulSpn, pspn);
return;
}
```



Дополнительные сведения о предыдущем примере кода см. в разделе [составление имен участников-служб для службы с SCP](composing-the-spns-for-a-service-with-an-scp.md) и [Регистрация имен участников-служб для службы](registering-the-spns-for-a-service.md).

 

 