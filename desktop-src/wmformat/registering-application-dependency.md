---
title: Регистрация зависимости приложения (пакет SDK для формата Windows Media 11)
description: Узнайте, как зарегистрировать приложение с помощью компонентов среды выполнения API, предоставляемых пакетом SDK для Windows Media Format 11.
ms.assetid: 09f63519-5c65-4784-9ea4-4fbecfa6d4aa
keywords:
- Пакет SDK для Windows Media Format, регистрация зависимостей приложений
- регистрация зависимостей приложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cd546ee9b162652f00a131e87561a7e34f7e3a2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406167"
---
# <a name="registering-application-dependency-windows-media-format-11-sdk"></a><span data-ttu-id="e885d-105">Регистрация зависимости приложения (пакет SDK для формата Windows Media 11)</span><span class="sxs-lookup"><span data-stu-id="e885d-105">Registering Application Dependency (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="e885d-106">Приложения, использующие интерфейсы API, предоставляемые пакетом SDK для Windows Media Format или пакетом SDK для проигрывателя Windows Media, зависят от компонентов среды выполнения этих технологий.</span><span class="sxs-lookup"><span data-stu-id="e885d-106">Applications that use APIs provided by the Windows Media Format SDK or Windows Media Player SDK are dependent upon the run-time components of those technologies.</span></span> <span data-ttu-id="e885d-107">Приложение можно зарегистрировать как зависящее от этих компонентов в процессе настройки приложения.</span><span class="sxs-lookup"><span data-stu-id="e885d-107">You can register your application as being dependent on those components as part of your application setup.</span></span>

<span data-ttu-id="e885d-108">При регистрации приложения можно выбрать один из двух уровней зависимости: блокировка или зависимая.</span><span class="sxs-lookup"><span data-stu-id="e885d-108">When you register your application, you can choose one of two levels of dependency: blocking, or dependent.</span></span> <span data-ttu-id="e885d-109">Если одно или несколько приложений зарегистрированы с блокировкой зависимостей на одном из компонентов времени выполнения, компонент будет заблокирован от отката к предыдущей версии.</span><span class="sxs-lookup"><span data-stu-id="e885d-109">When one or more applications are registered with a blocking dependency on one of the run-time components, the component will be blocked from a rollback to a previous version.</span></span> <span data-ttu-id="e885d-110">Зависимые приложения, которые не зарегистрированы как блокирующие, не блокируют откат.</span><span class="sxs-lookup"><span data-stu-id="e885d-110">Dependent applications that are not registered as blocking, do not block rollback.</span></span> <span data-ttu-id="e885d-111">Вместо этого перед выполнением отката пользователю предлагается сообщение о том, что приложения зависят от компонента.</span><span class="sxs-lookup"><span data-stu-id="e885d-111">Instead, before the rollback is performed, the user is prompted with a message stating that applications are dependent on the component.</span></span>

<span data-ttu-id="e885d-112">Чтобы зарегистрировать приложение, необходимо задать в реестре значение, идентифицирующее приложение.</span><span class="sxs-lookup"><span data-stu-id="e885d-112">To register your application, you must set a value in the registry that identifies your application.</span></span> <span data-ttu-id="e885d-113">Устанавливаемое значение реестра зависит от компонента, от которого зависит приложение.</span><span class="sxs-lookup"><span data-stu-id="e885d-113">The registry value to set depends on the component on which your application is dependent.</span></span> <span data-ttu-id="e885d-114">Можно также задать два дополнительных значения для зависимости, чтобы предоставить дополнительные сведения о приложении.</span><span class="sxs-lookup"><span data-stu-id="e885d-114">You can also set two additional values per dependency to provide extra information about your application.</span></span>

<span data-ttu-id="e885d-115">Следующие значения реестра используются для регистрации зависимостей в среде выполнения пакета SDK Windows Media Format:</span><span class="sxs-lookup"><span data-stu-id="e885d-115">The following registry values are used to register dependence on the Windows Media Format SDK runtime:</span></span>

-   <span data-ttu-id="e885d-116">Классы HKEY — \_ \_ корневое \\ программное обеспечение \\ Microsoft \\ виндовсмедиа \\ программа установки \\ *ссылочный \_ тип* \\ приложение, "*app*", "*\_ строка приложения*"</span><span class="sxs-lookup"><span data-stu-id="e885d-116">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="e885d-117">\_Классы hKey \_ корневое \\ программное обеспечение \\ Microsoft \\ виндовсмедиа \\ Setup \\ дескриптор *\_ типа ref* \\ , "*app*", "*ref \_ дескриптор*"</span><span class="sxs-lookup"><span data-stu-id="e885d-117">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="e885d-118">HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ виндовсмедиа \\ программа установки \\ *\_ тип ссылки* \\ версия, "*приложение*", "*\_ версия WMF*"</span><span class="sxs-lookup"><span data-stu-id="e885d-118">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\Version, "*APP*", "*WMF\_VERSION*"</span></span>

<span data-ttu-id="e885d-119">Для регистрации зависимостей в среде выполнения пакета SDK проигрывателя Windows Media используется следующее значение реестра:</span><span class="sxs-lookup"><span data-stu-id="e885d-119">The following registry value are used to register dependence on Windows Media Player SDK runtime:</span></span>

-   <span data-ttu-id="e885d-120">\_Классы hKey \_ — корневое \\ программное обеспечение \\ Microsoft \\ MediaPlayer \\ Настройка \\ *ссылочного \_ типа* \\ приложение, "*приложение*", "*\_ строка приложения*"</span><span class="sxs-lookup"><span data-stu-id="e885d-120">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="e885d-121">\_Классы hKey \_ корневое \\ программное обеспечение \\ Microsoft \\ MediaPlayer \\ Setup \\ дескриптор *\_ типа ref* \\ , "*app*", "*ref \_ дескриптор*"</span><span class="sxs-lookup"><span data-stu-id="e885d-121">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="e885d-122">Классы HKEY: \_ \_ корневое \\ программное обеспечение \\ Microsoft \\ MediaPlayer \\ программа установки \\ *\_ тип ссылки* \\ версия, "*приложение*", "*\_ версия WMP*"</span><span class="sxs-lookup"><span data-stu-id="e885d-122">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\Version, "*APP*", "*WMP\_VERSION*"</span></span>

<span data-ttu-id="e885d-123">В приведенных выше значениях реестра используются следующие переменные:</span><span class="sxs-lookup"><span data-stu-id="e885d-123">The following variables are used in the registry values listed above:</span></span>

<span data-ttu-id="e885d-124">*ССЫЛОЧный \_ тип*</span><span class="sxs-lookup"><span data-stu-id="e885d-124">*REF\_TYPE*</span></span>

<span data-ttu-id="e885d-125">Замените на Блоккингрефкаунтс для блокирующей зависимости или на Депендентрефкаунтс для неблокирующей зависимости.</span><span class="sxs-lookup"><span data-stu-id="e885d-125">Replace with BlockingRefCounts for blocking dependency, or with DependentRefCounts for non-blocking dependency.</span></span>

<span data-ttu-id="e885d-126">*APP*</span><span class="sxs-lookup"><span data-stu-id="e885d-126">*APP*</span></span>

<span data-ttu-id="e885d-127">Имя или короткий дескриптор приложения.</span><span class="sxs-lookup"><span data-stu-id="e885d-127">Name or short descriptor of your application.</span></span> <span data-ttu-id="e885d-128">Эта строка не будет использоваться в сообщениях, отображаемых для пользователя.</span><span class="sxs-lookup"><span data-stu-id="e885d-128">This string will not be used in messages displayed for the user.</span></span> <span data-ttu-id="e885d-129">Это значение является идентификатором, используемым во всех трех значениях реестра, связанных с каждым из компонентов времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="e885d-129">This value is the identifier used in all three registry values associated with each of the run-time components.</span></span>

<span data-ttu-id="e885d-130">*\_строка приложения*</span><span class="sxs-lookup"><span data-stu-id="e885d-130">*APP\_STRING*</span></span>

<span data-ttu-id="e885d-131">Дескриптор приложения.</span><span class="sxs-lookup"><span data-stu-id="e885d-131">Descriptor of your application.</span></span> <span data-ttu-id="e885d-132">Эта строка может использоваться в сообщениях, отображаемых для пользователя.</span><span class="sxs-lookup"><span data-stu-id="e885d-132">This string may be used in messages displayed for the user.</span></span>

<span data-ttu-id="e885d-133">*\_дескриптор ссылки*</span><span class="sxs-lookup"><span data-stu-id="e885d-133">*REF\_DESCRIPTOR*</span></span>

<span data-ttu-id="e885d-134">Описание того, как приложение использует компонент.</span><span class="sxs-lookup"><span data-stu-id="e885d-134">Description of how your application uses the component.</span></span> <span data-ttu-id="e885d-135">Это значение может включать не более 256 символов.</span><span class="sxs-lookup"><span data-stu-id="e885d-135">This value can include a maximum of 256 characters.</span></span>

<span data-ttu-id="e885d-136">*\_версия WMP*</span><span class="sxs-lookup"><span data-stu-id="e885d-136">*WMP\_VERSION*</span></span>

<span data-ttu-id="e885d-137">Версия проигрывателя Windows Media, необходимая для приложения.</span><span class="sxs-lookup"><span data-stu-id="e885d-137">Version of Windows Media Player required by your application.</span></span>

<span data-ttu-id="e885d-138">*\_версия WMF*</span><span class="sxs-lookup"><span data-stu-id="e885d-138">*WMF\_VERSION*</span></span>

<span data-ttu-id="e885d-139">Версия пакета SDK Windows Media Format, требуемая для приложения.</span><span class="sxs-lookup"><span data-stu-id="e885d-139">Version of the Windows Media Format SDK required by your application.</span></span>

<span data-ttu-id="e885d-140">В следующих трех примерах значений реестра показано, как настроить значения для приложения.</span><span class="sxs-lookup"><span data-stu-id="e885d-140">The following three example registry values demonstrate how to configure the values for your application:</span></span>

-   <span data-ttu-id="e885d-141">\_Классы hKey \_ — корневое \\ программное обеспечение \\ Microsoft \\ виндовсмедиа \\ Setup \\ депендентрефкаунтс \\ приложение, "саусриджевидео", "саусридже Video Player"</span><span class="sxs-lookup"><span data-stu-id="e885d-141">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\App, "SouthridgeVideo", "Southridge Video Player"</span></span>
-   <span data-ttu-id="e885d-142">\_В классах hKey \_ корневое \\ программное обеспечение \\ Microsoft \\ виндовсмедиа \\ Setup \\ депендентрефкаунтс \\ дескриптор, "саусриджевидео", "Саусридже Video Player использует пакет SDK Windows Media Format для воспроизведения видеофайлов".</span><span class="sxs-lookup"><span data-stu-id="e885d-142">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\Descriptor, "SouthridgeVideo", "Southridge Video Player uses the Windows Media Format SDK to play video files."</span></span>
-   <span data-ttu-id="e885d-143">HKEY \_ Classes \_ root \\ Software программа \\ Microsoft \\ виндовсмедиа \\ Setup \\ депендентрефкаунтс \\ версия, "саусриджевидео", "9.0.0.2600"</span><span class="sxs-lookup"><span data-stu-id="e885d-143">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\Version, "SouthridgeVideo", "9.0.0.2600"</span></span>

## <a name="related-topics"></a><span data-ttu-id="e885d-144">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="e885d-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e885d-145">**Рекомендации по проекту**</span><span class="sxs-lookup"><span data-stu-id="e885d-145">**Project Considerations**</span></span>](project-considerations.md)
</dt> </dl>

 

 




