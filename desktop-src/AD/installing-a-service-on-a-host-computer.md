---
title: Установка службы на главном компьютере
description: В следующем примере кода показаны основные шаги установки службы с поддержкой каталогов на главном компьютере.
ms.assetid: 35a3b261-d499-4154-a022-1e33a9ef7ba8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d687bbbfadb4d1ccb789e9d5f1051ebfbb4484d7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487425"
---
# <a name="installing-a-service-on-a-host-computer"></a><span data-ttu-id="5d07f-103">Установка службы на главном компьютере</span><span class="sxs-lookup"><span data-stu-id="5d07f-103">Installing a Service on a Host Computer</span></span>

<span data-ttu-id="5d07f-104">В следующем примере кода показаны основные шаги установки службы с поддержкой каталогов на главном компьютере.</span><span class="sxs-lookup"><span data-stu-id="5d07f-104">The following code example shows the basic steps of installing a directory-enabled service on a host computer.</span></span> <span data-ttu-id="5d07f-105">Она выполняет следующие операции:</span><span class="sxs-lookup"><span data-stu-id="5d07f-105">It performs the following operations:</span></span>

1.  <span data-ttu-id="5d07f-106">Вызывает функцию [**OpenSCManager**](/windows/desktop/api/winsvc/nf-winsvc-openscmanagera) для открытия на локальном компьютере маркера диспетчера управления СЛУЖБАМИ (SCM).</span><span class="sxs-lookup"><span data-stu-id="5d07f-106">Calls the [**OpenSCManager**](/windows/desktop/api/winsvc/nf-winsvc-openscmanagera) function to open a handle to the service control manager (SCM) on the local computer.</span></span>
2.  <span data-ttu-id="5d07f-107">Вызывает функцию [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) для установки службы в базе данных SCM.</span><span class="sxs-lookup"><span data-stu-id="5d07f-107">Calls the [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) function to install the service in the SCM database.</span></span> <span data-ttu-id="5d07f-108">Этот вызов задает учетную запись входа и пароль службы, а также исполняемый файл службы и другие сведения о службе.</span><span class="sxs-lookup"><span data-stu-id="5d07f-108">This call specifies the service's logon account and password, as well as the service's executable and other information about the service.</span></span> <span data-ttu-id="5d07f-109">**CreateService** завершается ошибкой, если указана недопустимая учетная запись входа.</span><span class="sxs-lookup"><span data-stu-id="5d07f-109">**CreateService** fails if the specified logon account is invalid.</span></span> <span data-ttu-id="5d07f-110">Однако **CreateService** не проверяет допустимость пароля.</span><span class="sxs-lookup"><span data-stu-id="5d07f-110">However, **CreateService** does not check the validity of the password.</span></span> <span data-ttu-id="5d07f-111">Он также не проверяет, имеет ли учетная запись право входа в качестве службы на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="5d07f-111">It also does not verify that the account has the logon as a service right on the local computer.</span></span> <span data-ttu-id="5d07f-112">Дополнительные сведения см. в разделе [предоставление входных данных в качестве службы непосредственно на главном компьютере](granting-logon-as-service-right-on-the-host-computer.md).</span><span class="sxs-lookup"><span data-stu-id="5d07f-112">For more information, see [Granting Logon as Service Right on the Host Computer](granting-logon-as-service-right-on-the-host-computer.md).</span></span>
3.  <span data-ttu-id="5d07f-113">Вызывает подпрограммы **скпкреате** службы, которая создает объект точки подключения службы (SCP) в каталоге для публикации расположения этого экземпляра службы.</span><span class="sxs-lookup"><span data-stu-id="5d07f-113">Calls the service's **ScpCreate** subroutine that creates a service connection point object (SCP) in the directory to publish the location of this instance of the service.</span></span> <span data-ttu-id="5d07f-114">Дополнительные сведения см. [в статье как клиенты находят и используют точку подключения службы](how-clients-find-and-use-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="5d07f-114">For more information, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).</span></span> <span data-ttu-id="5d07f-115">Эта подпрограммы также хранит сведения о привязке службы в SCP, устанавливает ACE на SCP, чтобы служба могла обращаться к ней во время выполнения, кэширует различающееся имя SCP в локальном реестре и возвращает различающееся имя новой точки подключения службы.</span><span class="sxs-lookup"><span data-stu-id="5d07f-115">This routine also stores the service's binding information in the SCP, sets an ACE on the SCP so the service can access it at run time, caches the distinguished name of the SCP in the local registry, and returns the distinguished name of the new SCP.</span></span>
4.  <span data-ttu-id="5d07f-116">Вызывает подпрограммы **спнкомпосе** службы, которая использует строку класса службы, и различающееся имя SCP для создания имени участника-службы (SPN).</span><span class="sxs-lookup"><span data-stu-id="5d07f-116">Calls the service's **SpnCompose** subroutine that uses the service's class string and the distinguished name of the SCP to compose a service principal name (SPN).</span></span> <span data-ttu-id="5d07f-117">Дополнительные сведения см. [в разделе Составление имен участников-служб для службы с SCP](composing-the-spns-for-a-service-with-an-scp.md).</span><span class="sxs-lookup"><span data-stu-id="5d07f-117">For more information, see [Composing the SPNs for a Service with an SCP](composing-the-spns-for-a-service-with-an-scp.md).</span></span> <span data-ttu-id="5d07f-118">Имя субъекта-службы однозначно определяет этот экземпляр службы.</span><span class="sxs-lookup"><span data-stu-id="5d07f-118">The SPN uniquely identifies this instance of the service.</span></span>
5.  <span data-ttu-id="5d07f-119">Вызывает подпрограммы **спнрегистер** службы, которая регистрирует SPN в объекте учетной записи, связанном с учетной записью входа службы.</span><span class="sxs-lookup"><span data-stu-id="5d07f-119">Calls the service's **SpnRegister** subroutine that registers the SPN on the account object associated with service's logon account.</span></span> <span data-ttu-id="5d07f-120">Дополнительные сведения см. [в статье регистрация имен участников-служб для службы](registering-the-spns-for-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="5d07f-120">For more information, see [Registering the SPNs for a Service](registering-the-spns-for-a-service.md).</span></span> <span data-ttu-id="5d07f-121">Регистрация имени участника-службы позволяет клиентским приложениям проходить проверку подлинности службы.</span><span class="sxs-lookup"><span data-stu-id="5d07f-121">Registration of the SPN enables client applications to authenticate the service.</span></span>

<span data-ttu-id="5d07f-122">Этот пример кода работает правильно независимо от того, является ли учетная запись входа локальной или учетной записью пользователя домена или учетной записью LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="5d07f-122">This code example works correctly regardless of whether the logon account is a local or domain user account or the LocalSystem account.</span></span> <span data-ttu-id="5d07f-123">Для учетной записи пользователя домена параметр *сзсервицеаккаунтсам* содержит имя \*\*\*\*\\*\*\* пользователя домена\* учетной записи, а параметр *сзсервицеаккаунтдн* содержит различающееся имя объекта учетной записи пользователя в каталоге.</span><span class="sxs-lookup"><span data-stu-id="5d07f-123">For a domain user account, the *szServiceAccountSAM* parameter contains the *Domain ***\\*** UserName* name of the account, and the *szServiceAccountDN* parameter contains the distinguished name of the user account object in the directory.</span></span> <span data-ttu-id="5d07f-124">Для учетной записи LocalSystem *сзсервицеаккаунтсам* и *Сзпассворд* имеют **значение NULL**, а *сзсервицеаккаунтсн* — различающееся имя объекта учетной записи локального компьютера в каталоге.</span><span class="sxs-lookup"><span data-stu-id="5d07f-124">For the LocalSystem account, *szServiceAccountSAM* and *szPassword* are **NULL**, and *szServiceAccountSN* is the distinguished name of the local computer's account object in the directory.</span></span> <span data-ttu-id="5d07f-125">Если *сзсервицеаккаунтсам* указывает локальную учетную запись пользователя (формат имени — "). \\ *Username*"), в примере кода пропускается регистрация имени участника-службы, так как взаимная проверка подлинности не поддерживается для локальных учетных записей пользователей.</span><span class="sxs-lookup"><span data-stu-id="5d07f-125">If *szServiceAccountSAM* specifies a local user account (name format is ".\\*UserName*"), the code example skips the SPN registration because mutual authentication is not supported for local user accounts.</span></span>

<span data-ttu-id="5d07f-126">Имейте в виду, что конфигурация безопасности по умолчанию позволяет только администраторам домена выполнять этот код.</span><span class="sxs-lookup"><span data-stu-id="5d07f-126">Be aware that the default security configuration allows only domain administrators to execute this code.</span></span>

<span data-ttu-id="5d07f-127">Кроме того, обратите внимание, что этот пример кода, как написано, должен выполняться на компьютере, где устанавливается служба.</span><span class="sxs-lookup"><span data-stu-id="5d07f-127">Also, be aware that this code example, as written, must be executed on the computer where the service is being installed.</span></span> <span data-ttu-id="5d07f-128">Следовательно, обычно он находится в отдельном исполняемом файле установки из кода установки службы, если таковой имеется, который расширяет схему, расширяет пользовательский интерфейс или настраивает групповую политику.</span><span class="sxs-lookup"><span data-stu-id="5d07f-128">Consequently, it is typically in a separate installation executable from your service installation code, if any, that extends the schema, extends the UI, or sets up group policy.</span></span> <span data-ttu-id="5d07f-129">Эти операции устанавливают компоненты службы для всего леса, в то время как этот код устанавливает службу на одном компьютере.</span><span class="sxs-lookup"><span data-stu-id="5d07f-129">Those operations install service components for an entire a forest, whereas this code installs the service on a single computer.</span></span>


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



<span data-ttu-id="5d07f-130">Дополнительные сведения о предыдущем примере кода см. в разделе [составление имен участников-служб для службы с SCP](composing-the-spns-for-a-service-with-an-scp.md) и [Регистрация имен участников-служб для службы](registering-the-spns-for-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="5d07f-130">For more information about the previous code example, see [Composing the SPNs for a Service with an SCP](composing-the-spns-for-a-service-with-an-scp.md) and [Registering the SPNs for a Service](registering-the-spns-for-a-service.md).</span></span>

 

 