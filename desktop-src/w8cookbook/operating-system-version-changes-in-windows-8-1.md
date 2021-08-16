---
title: изменения версии операционной системы в Windows 8.1 и Windows Server 2012 R2
description: изменения версии операционной системы в Windows 8.1 и Windows Server 2012 R2
ms.assetid: 3040262A-85EB-4F26-BE34-D2BBD5886E9E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e1fe0972a915d0f13ca3c3f8f52e5dd0559ad9c24e1afd2dd005f4a733373c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882694"
---
# <a name="operating-system-version-changes-in-windows-81-and-windows-server-2012-r2"></a>изменения версии операционной системы в Windows 8.1 и Windows Server 2012 R2

## <a name="platforms"></a>Платформы

**клиенты —** Windows 8.1

**серверы —** Windows Server 2012 R2

## <a name="description"></a>Описание

мы внесли существенные изменения в то, как работают api-интерфейсы версии (ex) в Windows 8.1 из-за нежелательных поведений клиентов, в результате которых используются api-интерфейсы в прошлом (ex).

в предыдущих версиях Windows вызов api-интерфейсов методической версии (Ex) возвращал бы фактическую версию операционной системы (ос), если только процесс не был устранен оболочкой совместимости приложения для предоставления ей другой версии. Это было сделано на основе предварительной версии и было относительно неполным в плане количества процессов, которые корпорация Майкрософт помогла поразумно реализовать в выпуске. Многие приложения проходят через положенное, так как они не получили оболочкой совместимости из-за плохо спроектированных проверок версии.

Чтобы проверить версию, необходимо предупредить пользователя о том, что приложение должно выполняться в более новой версии операционной системы. однако из-за неудачных проверок приложения часто ошибочно предупреждают о необходимости запуска в Windows XP или более поздней версии, что, конечно же, является самой новой ос. Чаще всего в самой новой операционной системе приложение будет работать без каких бы то ни было проблем, если не выполнить эти проверки.

## <a name="manifestation"></a>Проявление

в Windows 8.1 интерфейсы api-интерфейсов версии (Ex) являются устаревшими. это означает, что хотя все равно можно вызывать эти функции API, если ваше приложение не предназначено для Windows 8.1, функции возвращают Windows 8 версию (6,2).

## <a name="solution"></a>Решение

### <a name="adding-an-app-manifest"></a>Добавление манифеста приложения

чтобы приложение было предназначено для Windows 8.1, необходимо включить [манифест приложения (исполняемый файл)](/windows/compatibility/application-executable-manifest) для исполняемого файла приложения. затем в разделе " [ **&lt; совместимость &gt;**](../SbsCs/application-manifests.md#compatibility) " манифеста необходимо добавить элемент **&lt; &gt; суппортедос** для каждой версии Windows, которую нужно объявить, чтобы приложение поддерживалось.

в следующем примере показан файл манифеста приложения для приложения, поддерживающего все версии Windows из Windows Vista в Windows 8.1:

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
            <!-- Windows 8.1 -->
            <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/> <!-- * ADD THIS LINE * -->
            <!-- Windows 8 -->
            <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
            <!-- Windows 7 -->
            <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
            <!-- Windows Vista -->
            <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        </application>
    </compatibility>
</assembly>
```

В приведенной выше строке `* ADD THIS LINE *` показано, как точно выбрать для приложения Windows 8.1.

объявление поддержки для Windows 8.1 в манифесте приложения не будет оказывать никакого влияния при запуске приложения в предыдущих операционных системах.

### <a name="using-versionhelpers-instead-of-getversionex"></a>Использование Версионхелперс вместо метода "-Version" (ex)

в Windows 8.1 введены новые функции API замены для функций-версионхелперс (Ex). Они чрезвычайно просты в использовании. все, что нужно сделать, — это `#include <VersionHelpers.h>` . встроенные функции, доступные в файле заголовка версионхелперс. h, позволяют коду запрашивать, является ли операционная система определенной версией Windows или более поздней.

**Пример** например, если приложению требуется Windows 8 или более поздней версии, используйте следующий тест:

```cpp
#include <VersionHelpers.h>
// ...
    if (!IsWindows8OrGreater())
    {
       MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
    }
```

Доступны следующие функции API Версионхелпер:

```c
#define VERSIONHELPERAPI FORCEINLINE BOOL
VERSIONHELPERAPI IsWindowsXPOrGreater();
VERSIONHELPERAPI IsWindowsXPSP1OrGreater();
VERSIONHELPERAPI IsWindowsXPSP2OrGreater();
VERSIONHELPERAPI IsWindowsXPSP3OrGreater();
VERSIONHELPERAPI IsWindowsVistaOrGreater();
VERSIONHELPERAPI IsWindowsVistaSP1OrGreater();
VERSIONHELPERAPI IsWindowsVistaSP2OrGreater();
VERSIONHELPERAPI IsWindows7OrGreater();
VERSIONHELPERAPI IsWindows7SP1OrGreater();
VERSIONHELPERAPI IsWindows8OrGreater();
VERSIONHELPERAPI IsWindows8Point1OrGreater();
VERSIONHELPERAPI IsWindowsServer();
```

Они возвращают TRUE или FALSE в зависимости от вопроса, который вы запрашиваете, и вам нужно определить только поддерживаемую операционную систему минимального уровня.

## <a name="resources"></a>Ресурсы

-   [загрузка набор средств совместимости приложений](https://www.microsoft.com/downloads/details.aspx?FamilyId=24DA89E9-B581-47B0-B45E-492DD6DA2971)
-   [Известные исправления совместимости, режимы совместимости и сообщения AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))
-   [API-интерфейсы Версионхелперс](../sysinfo/version-helper-apis.md)