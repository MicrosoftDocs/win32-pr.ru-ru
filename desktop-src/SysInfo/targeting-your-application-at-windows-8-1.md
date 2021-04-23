---
description: В Windows 8.1 и Windows 10 функции функций и GetVersionEx не рекомендуются.
ms.assetid: E7A1A16A-95B3-4B45-81AD-A19E33F15AE4
title: Настройка приложения для Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0bd280451e5a1dd6a5162dd7b9ccb34495d22be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348455"
---
# <a name="targeting-your-application-for-windows"></a><span data-ttu-id="d336c-103">Настройка приложения для Windows</span><span class="sxs-lookup"><span data-stu-id="d336c-103">Targeting your application for Windows</span></span>

<span data-ttu-id="d336c-104">В Windows 8.1 и Windows 10 функции функций [**и**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion) [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) не рекомендуются.</span><span class="sxs-lookup"><span data-stu-id="d336c-104">In Windows 8.1 and Windows 10, the [**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion) and [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) functions have been deprecated.</span></span> <span data-ttu-id="d336c-105">В Windows 10 функция [**верифиверсионинфо**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa) также является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="d336c-105">In Windows 10, the [**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa) function has also been deprecated.</span></span> <span data-ttu-id="d336c-106">Хотя вы по-прежнему можете вызывать нерекомендуемые функции, если приложение не предназначено специально для Windows 8.1 или Windows 10, функции возвращают версию Windows 8 (6,2).</span><span class="sxs-lookup"><span data-stu-id="d336c-106">While you can still call the deprecated functions, if your application does not specifically target Windows 8.1 or Windows 10, the functions will return the Windows 8 version (6.2).</span></span>

> [!Note]  
> <span data-ttu-id="d336c-107">Функции [**верифиверсионинфо и**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion) [Version](version-helper-apis.md) поддерживаются только для настольных приложений. [](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) [](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)</span><span class="sxs-lookup"><span data-stu-id="d336c-107">[**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion), [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa), [**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa), and the [Version Helper functions](version-helper-apis.md) are for desktop apps only.</span></span> <span data-ttu-id="d336c-108">Универсальные приложения для Windows могут использовать свойство [**аналитиксинфо. versionInfo**](/uwp/api/windows.system.profile.analyticsinfo.versioninfo) для журналов телеметрии и диагностики.</span><span class="sxs-lookup"><span data-stu-id="d336c-108">Universal Windows apps can use the [**AnalyticsInfo.VersionInfo**](/uwp/api/windows.system.profile.analyticsinfo.versioninfo) property for telemetry and diagnostic logs.</span></span>

<span data-ttu-id="d336c-109">Чтобы приложение было предназначено Windows 8.1 или Windows 10, необходимо включить [манифест приложения (исполняемый файл)](/windows/compatibility/application-executable-manifest) для исполняемого файла приложения.</span><span class="sxs-lookup"><span data-stu-id="d336c-109">In order for your app to target Windows 8.1 or Windows 10, you'll need to include an [app (executable) manifest](/windows/compatibility/application-executable-manifest) for the app's executable.</span></span> <span data-ttu-id="d336c-110">Затем в разделе " [ **&lt; Совместимость &gt;**](../SbsCs/application-manifests.md#compatibility) " манифеста необходимо добавить элемент **&lt; &gt; суппортедос** для каждой версии Windows, которую необходимо объявить, чтобы приложение поддерживалось.</span><span class="sxs-lookup"><span data-stu-id="d336c-110">Then, in the [**&lt;compatibility&gt;** section](../SbsCs/application-manifests.md#compatibility) of the manifest, you'll need to add a **&lt;supportedOS&gt;** element for each Windows version you want to declare that your app supports.</span></span>

<span data-ttu-id="d336c-111">В следующем примере показан файл манифеста приложения для приложения, поддерживающего все версии Windows с Windows Vista до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="d336c-111">The following example shows an app manifest file for an app that supports all versions of Windows from Windows Vista to Windows 10:</span></span>

```XML
<!-- example.exe.manifest -->
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly manifestVersion="1.0" xmlns="urn:schemas-microsoft-com:asm.v1" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
    <assemblyIdentity
        type="win32"
        name="Contoso.ExampleApplication.ExampleBinary"
        version="1.2.3.4"
        processorArchitecture="x86"
    />
    <description>Contoso Example Application</description>
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1">
        <application>
            <!-- Windows 10 -->
            <supportedOS Id="{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}"/>
            <!-- Windows 8.1 -->
            <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/>
            <!-- Windows 8 -->
            <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
            <!-- Windows 7 -->
            <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
            <!-- Windows Vista -->
            <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        </application>
    </compatibility>
    <trustInfo xmlns="urn:schemas-microsoft-com:asm.v3">
        <security>
            <requestedPrivileges>
                <!--
                  UAC settings:
                  - app should run at same integrity level as calling process
                  - app does not need to manipulate windows belonging to
                    higher-integrity-level processes
                  -->
                <requestedExecutionLevel
                    level="asInvoker"
                    uiAccess="false"
                />   
            </requestedPrivileges>
        </security>
    </trustInfo>
</assembly>
```

<span data-ttu-id="d336c-112">Объявление поддержки для Windows 8.1 или Windows 10 в манифесте приложения не будет оказывать никакого влияния при запуске приложения в предыдущих операционных системах.</span><span class="sxs-lookup"><span data-stu-id="d336c-112">Declaring support for Windows 8.1 or Windows 10 in your app manifest will not have any effect when running your app on previous operating systems.</span></span>

<span data-ttu-id="d336c-113">Приведенный выше манифест приложения также включает [раздел **&lt; trustInfo &gt;**](/previous-versions/bb756929(v=msdn.10)), который указывает, как система должна обрабатывать ее в отношении [контроля учетных записей (UAC)](/windows/security/identity-protection/user-account-control/how-user-account-control-works).</span><span class="sxs-lookup"><span data-stu-id="d336c-113">The above app manifest also includes a [**&lt;trustInfo&gt;** section](/previous-versions/bb756929(v=msdn.10)), which specifies how the system should treat it with respect to [User Account Control (UAC)](/windows/security/identity-protection/user-account-control/how-user-account-control-works).</span></span> <span data-ttu-id="d336c-114">Добавление **trustInfo** не является обязательным, но настоятельно рекомендуется даже в том случае, если приложению не требуется определенное поведение, связанное с UAC.</span><span class="sxs-lookup"><span data-stu-id="d336c-114">Adding **trustInfo** isn't essential, but it is highly recommended, even when your app doesn't need any particular UAC-related behavior.</span></span> <span data-ttu-id="d336c-115">В частности, если вы не добавили **trustInfo** вообще, то для 32-разрядных версий x86 приложения будет применяться [виртуализация файлов UAC](/windows/security/identity-protection/user-account-control/how-user-account-control-works#virtualization), которая позволяет выполнять запись в административные папки, такие как системные папки Windows, в случае сбоя, если в противном случае они перенаправлены в пользовательскую папку «виртуалсторе».</span><span class="sxs-lookup"><span data-stu-id="d336c-115">In particular, if you don't add **trustInfo** at all, then 32-bit x86 versions of your app will be subject to [UAC file virtualization](/windows/security/identity-protection/user-account-control/how-user-account-control-works#virtualization), which allows writes to administrator-privileged folders like the Windows system folders to succeed when they would otherwise fail, but redirects them to a user-specific "VirtualStore" folder.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d336c-116">См. также</span><span class="sxs-lookup"><span data-stu-id="d336c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d336c-117">Получение версии системы</span><span class="sxs-lookup"><span data-stu-id="d336c-117">Getting the system version</span></span>](getting-the-system-version.md)
</dt> <dt>

[<span data-ttu-id="d336c-118">Вспомогательные функции версии</span><span class="sxs-lookup"><span data-stu-id="d336c-118">Version Helper functions</span></span>](version-helper-apis.md)
</dt> <dt>

[<span data-ttu-id="d336c-119">осверсионинфо</span><span class="sxs-lookup"><span data-stu-id="d336c-119">OSVERSIONINFO</span></span>](/windows/desktop/api/winnt/ns-winnt-osversioninfoa)
</dt> <dt>

[<span data-ttu-id="d336c-120">осверсионинфоекс</span><span class="sxs-lookup"><span data-stu-id="d336c-120">OSVERSIONINFOEX</span></span>](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa)
</dt> </dl>
