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
# <a name="targeting-your-application-for-windows"></a>Настройка приложения для Windows

В Windows 8.1 и Windows 10 функции функций [**и**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion) [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) не рекомендуются. В Windows 10 функция [**верифиверсионинфо**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa) также является устаревшей. Хотя вы по-прежнему можете вызывать нерекомендуемые функции, если приложение не предназначено специально для Windows 8.1 или Windows 10, функции возвращают версию Windows 8 (6,2).

> [!Note]  
> Функции [**верифиверсионинфо и**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion) [Version](version-helper-apis.md) поддерживаются только для настольных приложений. [](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) [](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa) Универсальные приложения для Windows могут использовать свойство [**аналитиксинфо. versionInfo**](/uwp/api/windows.system.profile.analyticsinfo.versioninfo) для журналов телеметрии и диагностики.

Чтобы приложение было предназначено Windows 8.1 или Windows 10, необходимо включить [манифест приложения (исполняемый файл)](/windows/compatibility/application-executable-manifest) для исполняемого файла приложения. Затем в разделе " [ **&lt; Совместимость &gt;**](../SbsCs/application-manifests.md#compatibility) " манифеста необходимо добавить элемент **&lt; &gt; суппортедос** для каждой версии Windows, которую необходимо объявить, чтобы приложение поддерживалось.

В следующем примере показан файл манифеста приложения для приложения, поддерживающего все версии Windows с Windows Vista до Windows 10.

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

Объявление поддержки для Windows 8.1 или Windows 10 в манифесте приложения не будет оказывать никакого влияния при запуске приложения в предыдущих операционных системах.

Приведенный выше манифест приложения также включает [раздел **&lt; trustInfo &gt;**](/previous-versions/bb756929(v=msdn.10)), который указывает, как система должна обрабатывать ее в отношении [контроля учетных записей (UAC)](/windows/security/identity-protection/user-account-control/how-user-account-control-works). Добавление **trustInfo** не является обязательным, но настоятельно рекомендуется даже в том случае, если приложению не требуется определенное поведение, связанное с UAC. В частности, если вы не добавили **trustInfo** вообще, то для 32-разрядных версий x86 приложения будет применяться [виртуализация файлов UAC](/windows/security/identity-protection/user-account-control/how-user-account-control-works#virtualization), которая позволяет выполнять запись в административные папки, такие как системные папки Windows, в случае сбоя, если в противном случае они перенаправлены в пользовательскую папку «виртуалсторе».

## <a name="related-topics"></a>См. также

<dl> <dt>

[Получение версии системы](getting-the-system-version.md)
</dt> <dt>

[Вспомогательные функции версии](version-helper-apis.md)
</dt> <dt>

[осверсионинфо](/windows/desktop/api/winnt/ns-winnt-osversioninfoa)
</dt> <dt>

[осверсионинфоекс](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa)
</dt> </dl>
