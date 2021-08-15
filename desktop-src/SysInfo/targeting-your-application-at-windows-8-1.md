---
description: в Windows 8.1 и Windows 10 функции функций и GetVersionEx не рекомендуются.
ms.assetid: E7A1A16A-95B3-4B45-81AD-A19E33F15AE4
title: Настройка приложения для Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e045dff2f46501c4715e2ffebe484dfeadb3aa9f276d79c7e7c1afdbec6ba7e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763115"
---
# <a name="targeting-your-application-for-windows"></a>Настройка приложения для Windows

в Windows 8.1 и Windows 10 функции функций [**и**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion) [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) не рекомендуются. в Windows 10 функция [**верифиверсионинфо**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa) также является устаревшей. хотя вы по-прежнему можете вызывать нерекомендуемые функции, если приложение не предназначено для Windows 8.1 или Windows 10, функции возвращают Windows 8 версию (6,2).

> [!Note]  
> Функции [**верифиверсионинфо и**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion) [Version](version-helper-apis.md) поддерживаются только для настольных приложений. [](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) [](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa) универсальные Windows приложения могут использовать свойство [**аналитиксинфо. VersionInfo**](/uwp/api/windows.system.profile.analyticsinfo.versioninfo) для журналов телеметрии и диагностики.

чтобы приложение было предназначено Windows 8.1 или Windows 10, необходимо включить [манифест приложения (исполняемый файл)](/windows/compatibility/application-executable-manifest) для исполняемого файла приложения. затем в разделе " [ **&lt; совместимость &gt;**](../SbsCs/application-manifests.md#compatibility) " манифеста необходимо добавить элемент **&lt; &gt; суппортедос** для каждой версии Windows, которую нужно объявить, чтобы приложение поддерживалось.

в следующем примере показан файл манифеста приложения для приложения, поддерживающего все версии Windows из Windows Vista в Windows 10:

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

объявление поддержки для Windows 8.1 или Windows 10 в манифесте приложения не будет оказывать никакого влияния при запуске приложения в предыдущих операционных системах.

Приведенный выше манифест приложения также включает [раздел **&lt; trustInfo &gt;**](/previous-versions/bb756929(v=msdn.10)), который указывает, как система должна обрабатывать ее в отношении [контроля учетных записей (UAC)](/windows/security/identity-protection/user-account-control/how-user-account-control-works). Добавление **trustInfo** не является обязательным, но настоятельно рекомендуется даже в том случае, если приложению не требуется определенное поведение, связанное с UAC. в частности, если вы не добавили **trustInfo** вообще, то для 32-разрядных версий x86 приложения будет применяться [виртуализация файлов UAC](/windows/security/identity-protection/user-account-control/how-user-account-control-works#virtualization), которая позволяет выполнять запись в административные папки, такие как Windows системные папки, для успешности выполнения в случае сбоя, но перенаправляет их в определяемую пользователем папку "виртуалсторе".

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Получение версии системы](getting-the-system-version.md)
</dt> <dt>

[Вспомогательные функции версии](version-helper-apis.md)
</dt> <dt>

[осверсионинфо](/windows/desktop/api/winnt/ns-winnt-osversioninfoa)
</dt> <dt>

[осверсионинфоекс](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa)
</dt> </dl>
