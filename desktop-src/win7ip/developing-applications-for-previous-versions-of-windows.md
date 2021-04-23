---
title: Разработка приложений для предыдущих версий Windows
description: Объясняет, что нужно сделать для разработки приложений, работающих в предыдущих версиях Windows, и воспользоваться преимуществами API, которые поддерживаются в обновлении платформы для Windows Vista и обновления платформы для Windows Server 2008.
ms.assetid: 9c46f894-e5cd-46a1-81c8-f63b09504735
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 299d4c61b0e2b931c3833934c843bf964fc3fa7c
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "104424158"
---
# <a name="developing-applications-for-previous-versions-of-windows"></a><span data-ttu-id="75da9-103">Разработка приложений для предыдущих версий Windows</span><span class="sxs-lookup"><span data-stu-id="75da9-103">Developing Applications for Previous Versions of Windows</span></span>

<span data-ttu-id="75da9-104">Объясняет, что нужно сделать для разработки приложений, работающих в предыдущих версиях Windows, и воспользоваться преимуществами API, которые поддерживаются в обновлении платформы для Windows Vista и обновления платформы для Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="75da9-104">Explains what to do to develop applications that run on previous versions of Windows and take advantage of the API that are supported with the Platform Update for Windows Vista and the Platform Update for Windows Server 2008.</span></span>

## <a name="required-downloads"></a><span data-ttu-id="75da9-105">Необходимые загрузки</span><span class="sxs-lookup"><span data-stu-id="75da9-105">Required Downloads</span></span>

<span data-ttu-id="75da9-106">Загрузка и установка пакетов, описанных в следующих разделах, необходима для разработки приложений, использующих API, которые представлены в пакете средств разработки программного обеспечения Microsoft Windows (SDK) для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="75da9-106">Download and installation of the packages described in the following sections is required if you want to develop applications that use API that are introduced with the Microsoft Windows Software Development Kit (SDK) for Windows 7.</span></span>

### <a name="microsoft-windows-sdk"></a><span data-ttu-id="75da9-107">Microsoft Windows SDK</span><span class="sxs-lookup"><span data-stu-id="75da9-107">Microsoft Windows SDK</span></span>

<span data-ttu-id="75da9-108">Windows SDK для Windows 7 требуется для создания приложений, использующих API, поддерживаемых в обновлении платформы для Windows Vista и обновления платформы для Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="75da9-108">The Windows SDK for Windows 7 is required for creating applications that use APIs supported with the Platform Update for Windows Vista and the Platform Update for Windows Server 2008.</span></span>

<span data-ttu-id="75da9-109">Дополнительные ресурсы и сведения, такие как файлы для загрузки, сообщения на форуме и блог группы Windows SDK, см. в [центре разработчиков Windows SDK](https://msdn.microsoft.com/bb980924.aspx) ( https://msdn.microsoft.com/bb980924.aspx) .</span><span class="sxs-lookup"><span data-stu-id="75da9-109">For access to additional resources and information, such as downloads, forum posts, and the Windows SDK team blog, see the [Windows SDK Developer Center](https://msdn.microsoft.com/bb980924.aspx) (https://msdn.microsoft.com/bb980924.aspx).</span></span>

### <a name="net-framework"></a><span data-ttu-id="75da9-110">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="75da9-110">.NET Framework</span></span>

<span data-ttu-id="75da9-111">Пакет обновления 1 (SP1) для платформа .NET Framework 3,5 необходим для создания приложений, использующих API-интерфейсы, поддерживаемые обновлением платформы для Windows Vista и обновления платформы для Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="75da9-111">The .NET Framework 3.5 Service Pack 1 is required for creating applications that use APIs supported by the Platform Update for Windows Vista and the Platform Update for Windows Server 2008.</span></span>

<span data-ttu-id="75da9-112">Дополнительные ресурсы и сведения см. в [центре платформа .NET Framework Developer Center](https://msdn.microsoft.com/netframework/default.aspx) ( https://msdn.microsoft.com/netframework/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="75da9-112">For additional resources and information, see the [.NET Framework Developer Center](https://msdn.microsoft.com/netframework/default.aspx) (https://msdn.microsoft.com/netframework/default.aspx).</span></span>

### <a name="directx-sdk-required-when-using-direct3d"></a><span data-ttu-id="75da9-113">При использовании Direct3D требуется пакет SDK для DirectX</span><span class="sxs-lookup"><span data-stu-id="75da9-113">DirectX SDK Required When Using Direct3D</span></span>

<span data-ttu-id="75da9-114">При создании приложений, использующих Direct3D, [пакет SDK для DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) необходим для создания приложений, использующих API, которые поддерживаются обновлением платформы для Windows Vista и обновлением платформы для Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="75da9-114">If you create applications that use Direct3D, the [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/aa937788.aspx) is required for creating applications that use APIs supported by the Platform Update for Windows Vista and the Platform Update for Windows Server 2008.</span></span>

### <a name="update-your-development-computer"></a><span data-ttu-id="75da9-115">Обновление компьютера разработчика</span><span class="sxs-lookup"><span data-stu-id="75da9-115">Update Your Development Computer</span></span>

<span data-ttu-id="75da9-116">Убедитесь, что на компьютере разработчика установлены все последние обновления от Центр обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="75da9-116">Ensure that your development computer has all of the latest updates from Windows Update.</span></span>

<span data-ttu-id="75da9-117">При разработке приложений в предыдущей версии Windows необходимо получить обновление платформы для Windows Vista или обновление платформы для Windows Server 2008 с Центр обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="75da9-117">If you are developing applications on a previous version of Windows, you must obtain the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 update from Windows Update.</span></span> <span data-ttu-id="75da9-118">Установка любого из этих обновлений позволит вам воспользоваться преимуществами нового API, предоставляемого Windows SDK для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="75da9-118">Installing either of these updates will enable you to take advantage of the new API provided by the Windows SDK for Windows 7.</span></span>

<span data-ttu-id="75da9-119">Дополнительные сведения о получении обновлений из Центр обновления Windows см. в статье базы [знаний об обновлении платформы для Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644) ( https://support.microsoft.com/kb/971644) .</span><span class="sxs-lookup"><span data-stu-id="75da9-119">For more information about how to obtain updates from Windows Update see the [Knowledge Base article about the Platform Update for Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644) (https://support.microsoft.com/kb/971644).</span></span>

## <a name="development-environment"></a><span data-ttu-id="75da9-120">Среда разработки</span><span class="sxs-lookup"><span data-stu-id="75da9-120">Development Environment</span></span>

### <a name="set-the-build-target-to-windows-7"></a><span data-ttu-id="75da9-121">Установка целевого объекта сборки в Windows 7</span><span class="sxs-lookup"><span data-stu-id="75da9-121">Set the Build Target to Windows 7</span></span>

<span data-ttu-id="75da9-122">Все приложения, использующие библиотеки в обновлении платформы для Windows Vista, должны быть основаны на целевой платформе Windows 7.</span><span class="sxs-lookup"><span data-stu-id="75da9-122">All applications that use libraries in the Platform Update for Windows Vista must be built against the Windows 7 target platform.</span></span>

<span data-ttu-id="75da9-123">Установка параметра WINVER в значение целевой платформы Windows 7 позволяет разрабатывать приложения, использующие API, поддерживаемые с обновлением платформы для Windows Vista или обновлением платформы для Windows Server 2008 на компьютере разработки под управлением Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="75da9-123">Setting WINVER to the Windows 7 target platform value enables you to develop applications that use APIs supported with the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 on a development machine running Windows Vista.</span></span>

<span data-ttu-id="75da9-124">Целевую платформу можно задать для Windows 7 либо в исходном коде, либо с помощью параметра/D в компиляторе Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="75da9-124">You can set the target platform to Windows 7 either in your source code or by using the /D option with the Visual Studio compiler.</span></span>

<span data-ttu-id="75da9-125">В следующем примере показано, как задать WINVER в исходном коде.</span><span class="sxs-lookup"><span data-stu-id="75da9-125">The following example shows how to set WINVER in your source code.</span></span>


```C++
#define WINVER 0x0601
```



<span data-ttu-id="75da9-126">В следующем примере показано, как задать WINVER с помощью параметра компилятора/D.</span><span class="sxs-lookup"><span data-stu-id="75da9-126">The following example shows how to set WINVER using the /D compiler option.</span></span>

``` syntax
/DWINVER=0x0601
```

## <a name="application-deployment"></a><span data-ttu-id="75da9-127">Развертывание приложения</span><span class="sxs-lookup"><span data-stu-id="75da9-127">Application Deployment</span></span>

<span data-ttu-id="75da9-128">Если вы создаете приложение с помощью заголовков и библиотек, предоставляемых Windows SDK для Windows 7, поддерживаемые API-интерфейсы будут выполняться в любой версии Windows с обновлением платформы для Windows Vista или на установленном обновлении платформы для Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="75da9-128">If you build your application using the headers and libraries provided by the Windows SDK for Windows 7, supported APIs will run on any Windows version that has the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 installed.</span></span>

> [!Note]  
> <span data-ttu-id="75da9-129">Поведение, производительность или требования для некоторых интерфейсов API, которые поддерживаются при обновлении платформы для Windows Vista или обновления платформы для Windows Server 2008, могут различаться в разных версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="75da9-129">The behavior, performance, or requirements for some APIs that are supported with the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 may vary across different versions of Windows.</span></span> <span data-ttu-id="75da9-130">Дополнительные сведения о конкретном API, поддерживаемом обновлениями, см. в разделе [об обновлении платформы для Windows Vista](platform-update-for-windows-vista-overview.md).</span><span class="sxs-lookup"><span data-stu-id="75da9-130">For details about a specific API that is supported by the updates, see [About Platform Update for Windows Vista](platform-update-for-windows-vista-overview.md).</span></span>

 

### <a name="no-redistributable-components"></a><span data-ttu-id="75da9-131">Нет распространяемых компонентов</span><span class="sxs-lookup"><span data-stu-id="75da9-131">No Redistributable Components</span></span>

<span data-ttu-id="75da9-132">Приложению не требуется устанавливать распространяемые компоненты, такие как библиотеки DLL или другие файлы времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="75da9-132">Your application does not need to install redistributable components, such as DLLs or other run-time files.</span></span>

### <a name="requires-updated-end-user-computer"></a><span data-ttu-id="75da9-133">Требуется обновленный End-User компьютер</span><span class="sxs-lookup"><span data-stu-id="75da9-133">Requires Updated End-User Computer</span></span>

<span data-ttu-id="75da9-134">Поскольку обновление платформы для Windows Vista и обновление платформы для Windows Server 2008 размещаются на Центр обновления Windows, конечные пользователи с включенным автоматическим обновлением, скорее всего, уже имеют эти обновления, а также необходимые пакеты обновления.</span><span class="sxs-lookup"><span data-stu-id="75da9-134">Because Platform Update for Windows Vista and Platform Update for Windows Server 2008 are hosted by Windows Update, end-users with automatic updates enabled are highly likely to already have these updates as well as the required service packs.</span></span>

<span data-ttu-id="75da9-135">Если на компьютере конечного пользователя отсутствует обновление платформы для Windows Vista или обновление платформы для Windows Server 2008 и для приложения требуются API-интерфейсы, поддерживаемые с этими обновлениями, приложение может не быть запущено на компьютере конечного пользователя или во время выполнения могут возникать ошибки.</span><span class="sxs-lookup"><span data-stu-id="75da9-135">If the end-user's computer does not have Platform Update for Windows Vista or Platform Update for Windows Server 2008 installed and your application requires APIs that are supported with these updates, your application may not be able to run on the end-user's computer or may encounter errors during execution.</span></span>

<span data-ttu-id="75da9-136">Во избежание проблем, которые могут быть вызваны неактуальностью компьютера пользователя, необходимо убедиться, что на компьютере пользователя имеется обновление платформы для Windows Vista или обновление платформы для Windows Server 2008 во время установки приложения.</span><span class="sxs-lookup"><span data-stu-id="75da9-136">To avoid the problems that could be caused by your user's computer being out-of-date, you want to verify that your user's computer has the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 update during the installation of your application.</span></span> <span data-ttu-id="75da9-137">Вы можете использовать [API центр обновления Windows агента](/windows/desktop/Wua_Sdk/portal-client) , чтобы проверить компьютер конечного пользователя на наличие установленных обновлений.</span><span class="sxs-lookup"><span data-stu-id="75da9-137">You can use the [Windows Update Agent API](/windows/desktop/Wua_Sdk/portal-client) to check your end-user's computer for installed updates.</span></span> <span data-ttu-id="75da9-138">Вы также можете использовать API агента Центр обновления Windows, чтобы скачать и установить необходимые обновления во время установки приложения, если пользователь еще не установил обновления.</span><span class="sxs-lookup"><span data-stu-id="75da9-138">You can also use the Windows Update Agent API to download and install required updates during application installation if the end-user has not already installed the updates.</span></span>

<span data-ttu-id="75da9-139">Пример установщика, демонстрирующий использование [API агента Центр обновления Windows](/windows/desktop/Wua_Sdk/portal-client), см. в разделе [развертывание Direct3D 11 для разработчиков игр](../direct3darticles/direct3d11-deployment.md) в [пакете SDK DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) .</span><span class="sxs-lookup"><span data-stu-id="75da9-139">For an example of an installer that demonstrates how to use the [Windows Update Agent API](/windows/desktop/Wua_Sdk/portal-client), see [Direct3D 11 Deployment for Game Developers](../direct3darticles/direct3d11-deployment.md) in the [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/aa937788.aspx).</span></span>

<span data-ttu-id="75da9-140">Несмотря на то, что пример установщика D3D11InstallHelper, обсуждаемый в [развертывании Direct3D 11 для разработчиков игр](../direct3darticles/direct3d11-deployment.md), был написан для приложений, использующих Direct3D 11, он предоставляет хороший пример взаимодействия с [API агента Центр обновления Windows](/windows/desktop/Wua_Sdk/portal-client) для инициирования и контроля загрузки и установки обновлений, размещенных в центр обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="75da9-140">Although the D3D11InstallHelper installer sample that is discussed in [Direct3D 11 Deployment for Game Developers](../direct3darticles/direct3d11-deployment.md), was written for applications that use Direct3D 11, it provides a good example of how to interact with the [Windows Update Agent API](/windows/desktop/Wua_Sdk/portal-client) to initiate and track the download and installation of updates that are hosted by Windows Update.</span></span> <span data-ttu-id="75da9-141">Для компиляции этого примера может потребоваться Windows SDK для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="75da9-141">Compiling this sample may require the Windows SDK for Windows 7.</span></span> <span data-ttu-id="75da9-142">Дополнительные сведения о примере D3D11InstallHelper, включая известные проблемы, см. в [пакете SDK DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) заметки о выпуске для августа 2009 г.). обновление платформы для Windows Vista</span><span class="sxs-lookup"><span data-stu-id="75da9-142">For additional information about the D3D11InstallHelper sample, including known issues, see the [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/aa937788.aspx) Release Notes for August 2009.Platform Update for Windows Vista</span></span>

## <a name="related-topics"></a><span data-ttu-id="75da9-143">См. также</span><span class="sxs-lookup"><span data-stu-id="75da9-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75da9-144">Обновление платформы для Windows Vista</span><span class="sxs-lookup"><span data-stu-id="75da9-144">Platform Update for Windows Vista</span></span>](platform-update-for-windows-vista-portal.md)
</dt> <dt>

<span data-ttu-id="75da9-145">**Разделы общих сведений**</span><span class="sxs-lookup"><span data-stu-id="75da9-145">**Overviews**</span></span>
</dt> <dt>

[<span data-ttu-id="75da9-146">Сведения об обновлении платформы для Windows Vista</span><span class="sxs-lookup"><span data-stu-id="75da9-146">About Platform Update for Windows Vista</span></span>](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[<span data-ttu-id="75da9-147">Статья базы знаний об обновлении платформы для Windows Vista (KB 971644)</span><span class="sxs-lookup"><span data-stu-id="75da9-147">Knowledge Base article about the Platform Update for Windows Vista (KB 971644)</span></span>](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 