---
title: Изменения версии операционной системы в Windows 8.1 и Windows Server 2012 R2
description: Изменения версии операционной системы в Windows 8.1 и Windows Server 2012 R2
ms.assetid: 3040262A-85EB-4F26-BE34-D2BBD5886E9E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0078ba918c675bbc8b9b9bbaf76660388f05bda9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413581"
---
# <a name="operating-system-version-changes-in-windows-81-and-windows-server-2012-r2"></a><span data-ttu-id="76545-103">Изменения версии операционной системы в Windows 8.1 и Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="76545-103">Operating system version changes in Windows 8.1 and Windows Server 2012 R2</span></span>

## <a name="platforms"></a><span data-ttu-id="76545-104">Платформы</span><span class="sxs-lookup"><span data-stu-id="76545-104">Platforms</span></span>

<span data-ttu-id="76545-105">**Клиенты —** Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="76545-105">**Clients -** Windows 8.1</span></span>

<span data-ttu-id="76545-106">**Серверы —** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="76545-106">**Servers -** Windows Server 2012 R2</span></span>

## <a name="description"></a><span data-ttu-id="76545-107">Описание</span><span class="sxs-lookup"><span data-stu-id="76545-107">Description</span></span>

<span data-ttu-id="76545-108">Мы внесли существенные изменения в то, как работают API-интерфейсы версии (ex) в Windows 8.1 из-за нежелательных поведений клиентов, в результате которых используются API-интерфейсы в прошлом (ex).</span><span class="sxs-lookup"><span data-stu-id="76545-108">We have made some significant changes in how the GetVersion(Ex) APIs work in Windows 8.1 due to undesirable customer behaviors resulting from how the GetVersion(Ex) APIs have been used in the past.</span></span>

<span data-ttu-id="76545-109">В предыдущих версиях Windows вызов API-интерфейсов методической версии (ex) возвращал бы фактическую версию операционной системы (ОС), если только процесс не был устранен оболочкой совместимости приложения для предоставления ей другой версии.</span><span class="sxs-lookup"><span data-stu-id="76545-109">In previous versions of Windows, calling the GetVersion(Ex) APIs would return the actual version of the operating system (OS), unless the process had been mitigated by an app compat shim to give it a different version.</span></span> <span data-ttu-id="76545-110">Это было сделано на основе предварительной версии и было относительно неполным в плане количества процессов, которые корпорация Майкрософт помогла поразумно реализовать в выпуске.</span><span class="sxs-lookup"><span data-stu-id="76545-110">This was done on a provisional basis and was relatively incomplete in terms of the number of processes that Microsoft could reasonably shim in a release.</span></span> <span data-ttu-id="76545-111">Многие приложения проходят через положенное, так как они не получили оболочкой совместимости из-за плохо спроектированных проверок версии.</span><span class="sxs-lookup"><span data-stu-id="76545-111">Many applications fell through the cracks because they didn’t get shimmed due to poorly designed version checks.</span></span>

<span data-ttu-id="76545-112">Чтобы проверить версию, необходимо предупредить пользователя о том, что приложение должно выполняться в более новой версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="76545-112">The number one reason to do a version check is to warn the user that the application needs to run on a newer version of the OS.</span></span> <span data-ttu-id="76545-113">Однако из-за неудачных проверок приложения часто ошибочно предупреждают о необходимости запуска в Windows XP или более поздней версии, что, конечно же, является самой новой ОС.</span><span class="sxs-lookup"><span data-stu-id="76545-113">However due to poor checks, apps would often incorrectly warn that they needed to be run on Windows XP or later, which of course the newest OS is.</span></span> <span data-ttu-id="76545-114">Чаще всего в самой новой операционной системе приложение будет работать без каких бы то ни было проблем, если не выполнить эти проверки.</span><span class="sxs-lookup"><span data-stu-id="76545-114">More often than not, the newest OS would run the application without any issues if not for these checks.</span></span>

## <a name="manifestation"></a><span data-ttu-id="76545-115">Проявление</span><span class="sxs-lookup"><span data-stu-id="76545-115">Manifestation</span></span>

<span data-ttu-id="76545-116">В Windows 8.1 интерфейсы API-интерфейсов версии (ex) являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="76545-116">In Windows 8.1, the GetVersion(Ex) APIs have been deprecated.</span></span> <span data-ttu-id="76545-117">Это означает, что хотя вы все равно можете вызывать эти функции API, если ваше приложение не предназначено для Windows 8.1, функции будут возвращать версию Windows 8 (6,2).</span><span class="sxs-lookup"><span data-stu-id="76545-117">That means that while you can still call these API functions, if your app does not specifically target Windows 8.1, the functions will return the Windows 8 version (6.2).</span></span>

## <a name="solution"></a><span data-ttu-id="76545-118">Решение</span><span class="sxs-lookup"><span data-stu-id="76545-118">Solution</span></span>

### <a name="adding-an-app-manifest"></a><span data-ttu-id="76545-119">Добавление манифеста приложения</span><span class="sxs-lookup"><span data-stu-id="76545-119">Adding an app manifest</span></span>

<span data-ttu-id="76545-120">Чтобы приложение было предназначено для Windows 8.1, необходимо включить [манифест приложения (исполняемый файл)](/windows/compatibility/application-executable-manifest) для исполняемого файла приложения.</span><span class="sxs-lookup"><span data-stu-id="76545-120">In order for your app to target Windows 8.1, you'll need to include an [app (executable) manifest](/windows/compatibility/application-executable-manifest) for the app's executable.</span></span> <span data-ttu-id="76545-121">Затем в разделе " [ **&lt; Совместимость &gt;**](../SbsCs/application-manifests.md#compatibility) " манифеста необходимо добавить элемент **&lt; &gt; суппортедос** для каждой версии Windows, которую необходимо объявить, чтобы приложение поддерживалось.</span><span class="sxs-lookup"><span data-stu-id="76545-121">Then, in the [**&lt;compatibility&gt;** section](../SbsCs/application-manifests.md#compatibility) of the manifest, you'll need to add a **&lt;supportedOS&gt;** element for each Windows version you want to declare that your app supports.</span></span>

<span data-ttu-id="76545-122">В следующем примере показан файл манифеста приложения для приложения, поддерживающего все версии Windows из Windows Vista для Windows 8.1:</span><span class="sxs-lookup"><span data-stu-id="76545-122">The following example shows an app manifest file for an app that supports all versions of Windows from Windows Vista to Windows 8.1:</span></span>

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

<span data-ttu-id="76545-123">В приведенной выше строке `* ADD THIS LINE *` показано, как точно выбрать для приложения Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="76545-123">The line above marked `* ADD THIS LINE *` shows how to accurately target your application for Windows 8.1.</span></span>

<span data-ttu-id="76545-124">Объявление поддержки для Windows 8.1 в манифесте приложения не будет оказывать никакого влияния при запуске приложения в предыдущих операционных системах.</span><span class="sxs-lookup"><span data-stu-id="76545-124">Declaring support for Windows 8.1 in your app manifest will not have any effect when running your app on previous operating systems.</span></span>

### <a name="using-versionhelpers-instead-of-getversionex"></a><span data-ttu-id="76545-125">Использование Версионхелперс вместо метода "-Version" (ex)</span><span class="sxs-lookup"><span data-stu-id="76545-125">Using VersionHelpers instead of GetVersion(Ex)</span></span>

<span data-ttu-id="76545-126">В Windows 8.1 введены новые функции API замены для функций-Версионхелперс (ex).</span><span class="sxs-lookup"><span data-stu-id="76545-126">Windows 8.1 introduces new replacement API functions for GetVersion(Ex), known as VersionHelpers.</span></span> <span data-ttu-id="76545-127">Они чрезвычайно просты в использовании. все, что нужно сделать, — это `#include <VersionHelpers.h>` .</span><span class="sxs-lookup"><span data-stu-id="76545-127">They are extremely easy to use; all you have to do is `#include <VersionHelpers.h>`.</span></span> <span data-ttu-id="76545-128">Встроенные функции, доступные в файле заголовка Версионхелперс. h, позволяют коду запрашивать, является ли операционная система данной версией Windows или более поздней.</span><span class="sxs-lookup"><span data-stu-id="76545-128">The inline functions available in the VersionHelpers.h header file allow your code to ask whether the operating system is a given version of Windows or later.</span></span>

<span data-ttu-id="76545-129">**Пример** Например, если приложению требуется Windows 8 или более поздней версии, используйте следующий тест:</span><span class="sxs-lookup"><span data-stu-id="76545-129">**Example** For example, if your application requires Windows 8 or later, use the following test:</span></span>

```cpp
#include <VersionHelpers.h>
// ...
    if (!IsWindows8OrGreater())
    {
       MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
    }
```

<span data-ttu-id="76545-130">Доступны следующие функции API Версионхелпер:</span><span class="sxs-lookup"><span data-stu-id="76545-130">The available VersionHelper API functions are:</span></span>

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

<span data-ttu-id="76545-131">Они возвращают TRUE или FALSE в зависимости от вопроса, который вы запрашиваете, и вам нужно определить только поддерживаемую операционную систему минимального уровня.</span><span class="sxs-lookup"><span data-stu-id="76545-131">They will return TRUE or FALSE depending on the question you are asking, and you only need to define the minimum level operating system that you support.</span></span>

## <a name="resources"></a><span data-ttu-id="76545-132">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="76545-132">Resources</span></span>

-   [<span data-ttu-id="76545-133">Загрузка набора средств для обеспечения совместимости приложений</span><span class="sxs-lookup"><span data-stu-id="76545-133">Application Compatibility Toolkit Download</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyId=24DA89E9-B581-47B0-B45E-492DD6DA2971)
-   <span data-ttu-id="76545-134">[Известные исправления совместимости, режимы совместимости и сообщения AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="76545-134">[Known Compatibility Fixes, Compatibility Modes, and AppHelp Messages](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span></span>
-   [<span data-ttu-id="76545-135">API-интерфейсы Версионхелперс</span><span class="sxs-lookup"><span data-stu-id="76545-135">VersionHelpers APIs</span></span>](../sysinfo/version-helper-apis.md)