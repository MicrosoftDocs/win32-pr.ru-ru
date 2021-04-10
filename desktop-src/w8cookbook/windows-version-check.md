---
title: Проверка версии Windows
description: Версия ОС была увеличена с выпуском ОС Windows 10.
ms.assetid: 55BB7B44-1AFD-456D-9380-38B4D26E5EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ea1e65ed97859486bdd0a18fe53ee44a653faf
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "104134726"
---
# <a name="windows-version-check"></a><span data-ttu-id="1be2f-103">Проверка версии Windows</span><span class="sxs-lookup"><span data-stu-id="1be2f-103">Windows version check</span></span>

<span data-ttu-id="1be2f-104">Версия ОС была увеличена с выпуском ОС Windows 10.</span><span class="sxs-lookup"><span data-stu-id="1be2f-104">The OS version has been incremented with the Windows 10 OS release.</span></span> <span data-ttu-id="1be2f-105">Это означает, что внутренний номер версии для Windows 10 также был изменен на 10,0.</span><span class="sxs-lookup"><span data-stu-id="1be2f-105">This means that the internal version number for Windows 10 has also been changed to 10.0.</span></span> <span data-ttu-id="1be2f-106">Как и раньше, мы хотим сделать все возможное для обеспечения совместимости с приложениями и устройствами после изменения номера версии ОС.</span><span class="sxs-lookup"><span data-stu-id="1be2f-106">As in the past, we go to great lengths to maintain application and device compatibility after an OS version change.</span></span> <span data-ttu-id="1be2f-107">Для большинства категорий приложений (без зависимостей ядра) изменение не оказывает негативного воздействия на функциональность приложения, и существующие приложения будут работать нормально в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="1be2f-107">For most app categories (without any kernel dependencies) the change will not negatively impact app functionality, and existing apps will continue to work fine on Windows 10.</span></span>

## <a name="manifestations"></a><span data-ttu-id="1be2f-108">Проявлениями</span><span class="sxs-lookup"><span data-stu-id="1be2f-108">Manifestations</span></span>

<span data-ttu-id="1be2f-109">Проявление этого изменения будет зависеть от конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="1be2f-109">The manifestation of this change is app-specific.</span></span> <span data-ttu-id="1be2f-110">Это означает, что любое приложение, выполняющее непосредственную проверку версии ОС, в ответ на запрос будет получать ответ с указанием более высокого номера версии, что может привести к возникновению одной или нескольких ситуаций, описанных ниже:</span><span class="sxs-lookup"><span data-stu-id="1be2f-110">This means any app that specifically checks for the OS version will get a higher version number, which can lead to one or more of the following situations:</span></span>

-   <span data-ttu-id="1be2f-111">Установщик приложения не сможет установить приложение, и оно может не запуститься.</span><span class="sxs-lookup"><span data-stu-id="1be2f-111">App installers might not be able to install the app, and apps might not be able to start.</span></span>
-   <span data-ttu-id="1be2f-112">Приложения могут работать нестабильно или со сбоями.</span><span class="sxs-lookup"><span data-stu-id="1be2f-112">Apps might become unstable or crash.</span></span>
-   <span data-ttu-id="1be2f-113">Приложения могут создавать сообщения об ошибках, но продолжать работать в штатном режиме.</span><span class="sxs-lookup"><span data-stu-id="1be2f-113">Apps might generate error messages, but continue to function properly.</span></span>

<span data-ttu-id="1be2f-114">Некоторые приложения выполняют проверку номера версии ОС и просто передают пользователям предупреждение.</span><span class="sxs-lookup"><span data-stu-id="1be2f-114">Some apps perform a version check and simply pass a warning to users.</span></span> <span data-ttu-id="1be2f-115">Но есть приложения, работа которых очень сильно зависит от результатов проверки номера версии ОС (в драйверах или в режиме ядра для предотвращения обнаружения номера версии).</span><span class="sxs-lookup"><span data-stu-id="1be2f-115">However, there are apps that are bound very tightly to a version check (in the drivers, or in kernel mode to avoid detection).</span></span> <span data-ttu-id="1be2f-116">В этих случаях при обнаружении несовместимой версии приложение запустить не удастся.</span><span class="sxs-lookup"><span data-stu-id="1be2f-116">In these cases, the app will fail if an incorrect version is found.</span></span> <span data-ttu-id="1be2f-117">Поэтому вместо проверки версии мы рекомендуем использовать один из следующих подходов.</span><span class="sxs-lookup"><span data-stu-id="1be2f-117">Rather than a version check, we recommend one of the following approaches:</span></span>

-   <span data-ttu-id="1be2f-118">Если приложение зависит от конкретной функции API, убедитесь, что вы используете правильную версию API.</span><span class="sxs-lookup"><span data-stu-id="1be2f-118">If the app is dependent on specific API functionality, ensure you target the correct API version.</span></span>
-   <span data-ttu-id="1be2f-119">Номер версии НТДДИ (интерфейс драйвера устройства NT) увеличится только при изменении целевой функциональности в API.</span><span class="sxs-lookup"><span data-stu-id="1be2f-119">NTDDI (NT device driver interface) version number will increment only if target functionality in the API changes.</span></span> <span data-ttu-id="1be2f-120">Убедитесь, что вы обнаружите изменение с помощью Аписет или другого доступного API, созданного специализированной группой, и не используйте версию в качестве прокси-сервера для некоторой функции или исправления.</span><span class="sxs-lookup"><span data-stu-id="1be2f-120">Ensure you detect the change via APISet or other exposed API as created by the feature team, and do not use the version as a proxy for some feature or fix.</span></span> <span data-ttu-id="1be2f-121">Если есть критические изменения и правильная проверка невозможна, можно достоверно утверждать об обнаружении ошибки.</span><span class="sxs-lookup"><span data-stu-id="1be2f-121">If there are breaking changes and a proper check is not exposed, then that is a bug.</span></span>
-   <span data-ttu-id="1be2f-122">Убедитесь, что приложение не выполняет проверку версии нечетными способами, например с помощью реестра, версий файлов, смещений, режима ядра, драйверов или других средств.</span><span class="sxs-lookup"><span data-stu-id="1be2f-122">Ensure the app does NOT check for version in odd ways, such as via the registry, file versions, offsets, kernel mode, drivers or other means.</span></span> <span data-ttu-id="1be2f-123">Если приложению абсолютно нужно проверить версию, используйте API-интерфейсы для функций, которые должны возвращать основной, дополнительный номера и номер сборки.</span><span class="sxs-lookup"><span data-stu-id="1be2f-123">If the app absolutely needs to check the version, use the GetVersion APIs, which should return the major, minor and build number.</span></span>
-   <span data-ttu-id="1be2f-124">Если вы используете API-интерфейс или другие вспомогательные функции версии, например [верифиверсионинфо](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa), помните, что поведение этого API изменилось, начиная с Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="1be2f-124">If you are using the GetVersion API or other Version Helper functions such as [VerifyVersionInfo](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa), remember that the behavior of this API has changed starting with Windows 8.1.</span></span> <span data-ttu-id="1be2f-125">Дополнительные сведения см. в [документации по API](../SysInfo/version-helper-apis.md) .</span><span class="sxs-lookup"><span data-stu-id="1be2f-125">Please refer to [the API documentation](../SysInfo/version-helper-apis.md) for more details.</span></span>
-   <span data-ttu-id="1be2f-126">Если вы владеете такими приложениями, как защита от вредоносных программ или брандмауэр, вы должны работать с обычными каналами обратной связи и с помощью программы предварительной оценки Windows.</span><span class="sxs-lookup"><span data-stu-id="1be2f-126">If you own apps such as antimalware or firewall, you should work through your usual feedback channels and via the Windows Insider program.</span></span>

## <a name="declaring-windows-10-compatibility-with-an-app-manifest"></a><span data-ttu-id="1be2f-127">Объявление совместимости Windows 10 с манифестом приложения</span><span class="sxs-lookup"><span data-stu-id="1be2f-127">Declaring Windows 10 Compatibility With An App Manifest</span></span>

<span data-ttu-id="1be2f-128">Если приложение совместимо с Windows 10, оно может объявить этот факт в [манифесте приложения (исполняемом файле)](/windows/compatibility/application-executable-manifest) для исполняемого файла приложения.</span><span class="sxs-lookup"><span data-stu-id="1be2f-128">If your app is compatible with Windows 10, it can declare this fact in the [app (executable) manifest](/windows/compatibility/application-executable-manifest) for the app's executable.</span></span> <span data-ttu-id="1be2f-129">Это говорит системе, что ваше приложение понимает номер версии 10,0 в системе Windows 10 (так что API-интерфейс версии не возвращает более раннюю версию), а также позволяет системе отключать другие поведения совместимости, применяемые к приложениям, которые не объявляют совместимость с Windows 10.</span><span class="sxs-lookup"><span data-stu-id="1be2f-129">This tells the system that your app understands Windows 10's system version number of 10.0 (so the GetVersion API does not return an earlier version), and also lets the system turn off other compatibility behaviors applied to apps that don't declare Windows 10 compatibility.</span></span>

<span data-ttu-id="1be2f-130">Чтобы объявить совместимость с Windows 10 в манифесте приложения, необходимо добавить [раздел **&lt; совместимости &gt;**](../SbsCs/application-manifests.md#compatibility) манифеста, если он еще не существует, а затем добавить элементы **&lt; суппортедос &gt;** для Windows 10 и всех остальных версий Windows, которые вы хотите объявить в приложении.</span><span class="sxs-lookup"><span data-stu-id="1be2f-130">To declare Windows 10 compatibility in an app manifest, you'll need to add a [**&lt;compatibility&gt;** section](../SbsCs/application-manifests.md#compatibility) of the manifest if one does not already exist, and then add **&lt;supportedOS&gt;** elements for Windows 10 and every other Windows version you want to declare that your app supports.</span></span>

<span data-ttu-id="1be2f-131">В следующем примере показан файл манифеста приложения для приложения, поддерживающего все версии Windows с Windows Vista до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="1be2f-131">The following example shows an app manifest file for an app that supports all versions of Windows from Windows Vista to Windows 10:</span></span>

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
            <supportedOS Id="{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}"/> <!-- * ADD THIS LINE * -->
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
</assembly>
```

<span data-ttu-id="1be2f-132">В приведенной выше строке `* ADD THIS LINE *` показано, как точно выбрать приложение для Windows 10.</span><span class="sxs-lookup"><span data-stu-id="1be2f-132">The line above marked `* ADD THIS LINE *` shows how to accurately target your application for Windows 10.</span></span>

<span data-ttu-id="1be2f-133">Объявление поддержки для Windows 10 в манифесте приложения не будет оказывать никакого влияния при запуске приложения в предыдущих операционных системах.</span><span class="sxs-lookup"><span data-stu-id="1be2f-133">Declaring support for Windows 10 in your app manifest will not have any effect when running your app on previous operating systems.</span></span>

## <a name="resources"></a><span data-ttu-id="1be2f-134">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="1be2f-134">Resources</span></span>

-   [<span data-ttu-id="1be2f-135">Загрузка набора средств для обеспечения совместимости приложений: Загрузка Windows ADK для Windows 10</span><span class="sxs-lookup"><span data-stu-id="1be2f-135">Application Compatibility Toolkit Download: Download the Windows ADK for Windows 10</span></span>](https://download.microsoft.com/download/9/A/E/9AE69DD5-BA93-44E0-864E-180F5E700AB4/adk/adksetup.exe)
-   <span data-ttu-id="1be2f-136">[Известные исправления совместимости, режимы совместимости и сообщения AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="1be2f-136">[Known Compatibility Fixes, Compatibility Modes, and AppHelp Messages](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span></span>
-   [<span data-ttu-id="1be2f-137">API вспомогательных функций версий</span><span class="sxs-lookup"><span data-stu-id="1be2f-137">Version Helpers API</span></span>](../sysinfo/version-helper-apis.md)