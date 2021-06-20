---
title: Регистрация зависимости приложения (пакет SDK для проигрывателя Windows Media)
description: Узнайте, как зарегистрировать приложение с помощью компонентов среды выполнения API-интерфейсов, предоставляемых пакетом SDK для проигрывателя Windows Media.
ms.assetid: 966683d6-e082-448d-8473-baae2311c082
keywords:
- Проигрыватель Windows Media, параметры реестра зависимостей приложений
- Проигрыватель Windows Media, параметры реестра зависимостей
- Проигрыватель Windows Media, реестр
- реестр, параметры зависимости приложений
- реестр, параметры зависимостей
- реестр, параметры для проигрывателя Windows Media
- параметры реестра зависимостей
- параметры реестра зависимостей приложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4b1692c6a4e1a8274472bbe9d718721c1ab4f1
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407367"
---
# <a name="registering-application-dependency-windows-media-player-sdk"></a><span data-ttu-id="d3c92-111">Регистрация зависимости приложения (пакет SDK для проигрывателя Windows Media)</span><span class="sxs-lookup"><span data-stu-id="d3c92-111">Registering Application Dependency (Windows Media Player SDK)</span></span>

<span data-ttu-id="d3c92-112">Приложения, использующие интерфейсы API, предоставляемые пакетом SDK для проигрывателя Windows Media или Windows Media Format SDK, зависят от компонентов среды выполнения этих технологий.</span><span class="sxs-lookup"><span data-stu-id="d3c92-112">Applications that use APIs provided by the Windows Media Player SDK or Windows Media Format SDK are dependent upon the runtime components of those technologies.</span></span> <span data-ttu-id="d3c92-113">Приложение можно зарегистрировать как зависящее от этих компонентов в процессе настройки приложения.</span><span class="sxs-lookup"><span data-stu-id="d3c92-113">You can register your application as being dependent on those components as part of your application setup.</span></span>

<span data-ttu-id="d3c92-114">При регистрации приложения можно выбрать один из двух уровней зависимости: блокировка или зависимость.</span><span class="sxs-lookup"><span data-stu-id="d3c92-114">When you register your application, you can choose one of two levels of dependency: blocking or dependent.</span></span> <span data-ttu-id="d3c92-115">Если одно или несколько приложений зарегистрированы в блокирующей зависимости от одного из компонентов среды выполнения, компонент будет заблокирован от отката к предыдущей версии.</span><span class="sxs-lookup"><span data-stu-id="d3c92-115">When one or more application is registered with a blocking dependency on one of the runtime components, the component will be blocked from a rollback to a previous version.</span></span> <span data-ttu-id="d3c92-116">Зависимые приложения, которые не зарегистрированы как блокирующие, не блокируют откат.</span><span class="sxs-lookup"><span data-stu-id="d3c92-116">Dependent applications that are not registered as blocking do not block rollback.</span></span> <span data-ttu-id="d3c92-117">Вместо этого при выполнении отката пользователю отображается сообщение о том, что приложения зависят от компонента.</span><span class="sxs-lookup"><span data-stu-id="d3c92-117">Instead, before the rollback is performed, the user is displayed a message stating that applications are dependent on the component.</span></span>

<span data-ttu-id="d3c92-118">Чтобы зарегистрировать приложение, необходимо задать в реестре значение, идентифицирующее приложение.</span><span class="sxs-lookup"><span data-stu-id="d3c92-118">To register your application, you must set a value in the registry that identifies your application.</span></span> <span data-ttu-id="d3c92-119">Устанавливаемое значение реестра зависит от компонента, от которого зависит приложение.</span><span class="sxs-lookup"><span data-stu-id="d3c92-119">The registry value to set depends on the component on which your application is dependent.</span></span> <span data-ttu-id="d3c92-120">Можно также задать два дополнительных значения для зависимости, чтобы предоставить дополнительные сведения о приложении.</span><span class="sxs-lookup"><span data-stu-id="d3c92-120">You can also set two additional values per dependency to provide extra information about your application.</span></span>

<span data-ttu-id="d3c92-121">Для регистрации зависимостей в среде выполнения пакета SDK проигрывателя Windows Media используются следующие значения реестра:</span><span class="sxs-lookup"><span data-stu-id="d3c92-121">The following registry values are used to register dependence on Windows Media Player SDK runtime:</span></span>

-   <span data-ttu-id="d3c92-122">\_Классы hKey \_ — корневое \\ программное обеспечение \\ Microsoft \\ MediaPlayer \\ Настройка \\ *ссылочного \_ типа* \\ приложение, "*приложение*", "*\_ строка приложения*"</span><span class="sxs-lookup"><span data-stu-id="d3c92-122">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="d3c92-123">\_Классы hKey \_ корневое \\ программное обеспечение \\ Microsoft \\ MediaPlayer \\ Setup \\ дескриптор *\_ типа ref* \\ , "*app*", "*ref \_ дескриптор*"</span><span class="sxs-lookup"><span data-stu-id="d3c92-123">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="d3c92-124">Классы HKEY: \_ \_ корневое \\ программное обеспечение \\ Microsoft \\ MediaPlayer \\ программа установки \\ *\_ тип ссылки* \\ версия, "*приложение*", "*\_ версия WMP*"</span><span class="sxs-lookup"><span data-stu-id="d3c92-124">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\Version, "*APP*", "*WMP\_VERSION*"</span></span>

<span data-ttu-id="d3c92-125">Следующие значения реестра используются для регистрации зависимостей в среде выполнения пакета SDK Windows Media Format:</span><span class="sxs-lookup"><span data-stu-id="d3c92-125">The following registry values are used to register dependence on the Windows Media Format SDK runtime:</span></span>

-   <span data-ttu-id="d3c92-126">Классы HKEY — \_ \_ корневое \\ программное обеспечение \\ Microsoft \\ виндовсмедиа \\ программа установки \\ *ссылочный \_ тип* \\ приложение, "*app*", "*\_ строка приложения*"</span><span class="sxs-lookup"><span data-stu-id="d3c92-126">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="d3c92-127">\_Классы hKey \_ корневое \\ программное обеспечение \\ Microsoft \\ виндовсмедиа \\ Setup \\ дескриптор *\_ типа ref* \\ , "*app*", "*ref \_ дескриптор*"</span><span class="sxs-lookup"><span data-stu-id="d3c92-127">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="d3c92-128">HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ виндовсмедиа \\ программа установки \\ *\_ тип ссылки* \\ версия, "*приложение*", "*\_ версия WMF*"</span><span class="sxs-lookup"><span data-stu-id="d3c92-128">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\Version, "*APP*", "*WMF\_VERSION*"</span></span>

<span data-ttu-id="d3c92-129">В приведенных выше значениях реестра используются следующие переменные:</span><span class="sxs-lookup"><span data-stu-id="d3c92-129">The following variables are used in the registry values listed above:</span></span>

<span data-ttu-id="d3c92-130">*ССЫЛОЧный \_ тип*</span><span class="sxs-lookup"><span data-stu-id="d3c92-130">*REF\_TYPE*</span></span>

<span data-ttu-id="d3c92-131">Замените на Блоккингрефкаунтс для блокирующей зависимости или на Депендентрефкаунтс для неблокирующей зависимости.</span><span class="sxs-lookup"><span data-stu-id="d3c92-131">Replace with BlockingRefCounts for blocking dependency, or with DependentRefCounts for non-blocking dependency.</span></span>

<span data-ttu-id="d3c92-132">*APP*</span><span class="sxs-lookup"><span data-stu-id="d3c92-132">*APP*</span></span>

<span data-ttu-id="d3c92-133">Имя или короткий дескриптор приложения.</span><span class="sxs-lookup"><span data-stu-id="d3c92-133">Name or short descriptor of your application.</span></span> <span data-ttu-id="d3c92-134">Эта строка не будет использоваться в сообщениях, отображаемых для пользователя.</span><span class="sxs-lookup"><span data-stu-id="d3c92-134">This string will not be used in messages displayed for the user.</span></span> <span data-ttu-id="d3c92-135">Это значение является идентификатором, используемым во всех трех значениях реестра, связанных с каждым из компонентов среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="d3c92-135">This value is the identifier used in all three registry values associated with each of the runtime components.</span></span>

<span data-ttu-id="d3c92-136">*\_строка приложения*</span><span class="sxs-lookup"><span data-stu-id="d3c92-136">*APP\_STRING*</span></span>

<span data-ttu-id="d3c92-137">Дескриптор приложения.</span><span class="sxs-lookup"><span data-stu-id="d3c92-137">Descriptor of your application.</span></span> <span data-ttu-id="d3c92-138">Эта строка может использоваться в сообщениях, отображаемых для пользователя.</span><span class="sxs-lookup"><span data-stu-id="d3c92-138">This string may be used in messages displayed for the user.</span></span>

<span data-ttu-id="d3c92-139">*\_дескриптор ссылки*</span><span class="sxs-lookup"><span data-stu-id="d3c92-139">*REF\_DESCRIPTOR*</span></span>

<span data-ttu-id="d3c92-140">Описание того, как приложение использует компонент.</span><span class="sxs-lookup"><span data-stu-id="d3c92-140">Description of how your application uses the component.</span></span> <span data-ttu-id="d3c92-141">Это значение может включать не более 256 символов.</span><span class="sxs-lookup"><span data-stu-id="d3c92-141">This value can include a maximum of 256 characters.</span></span>

<span data-ttu-id="d3c92-142">*\_версия WMP*</span><span class="sxs-lookup"><span data-stu-id="d3c92-142">*WMP\_VERSION*</span></span>

<span data-ttu-id="d3c92-143">Версия проигрывателя Windows Media, необходимая для приложения.</span><span class="sxs-lookup"><span data-stu-id="d3c92-143">Version of Windows Media Player required by your application.</span></span> <span data-ttu-id="d3c92-144">Если версия не указана, предполагается, что используется значение по умолчанию 9.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="d3c92-144">If no version is specified, the default value is assumed to be 9.0.0.0.</span></span>

<span data-ttu-id="d3c92-145">*\_версия WMF*</span><span class="sxs-lookup"><span data-stu-id="d3c92-145">*WMF\_VERSION*</span></span>

<span data-ttu-id="d3c92-146">Версия пакета SDK Windows Media Format, требуемая для приложения.</span><span class="sxs-lookup"><span data-stu-id="d3c92-146">Version of the Windows Media Format SDK required by your application.</span></span>

<span data-ttu-id="d3c92-147">В следующих трех примерах значений реестра показано, как настроить значения для приложения.</span><span class="sxs-lookup"><span data-stu-id="d3c92-147">The following three example registry values demonstrate how to configure the values for your application:</span></span>

-   <span data-ttu-id="d3c92-148">\_Классы hKey \_ — корневое \\ программное обеспечение \\ Microsoft \\ MediaPlayer \\ Setup \\ депендентрефкаунтс \\ приложение, "саусриджевидео", "саусридже Video Player"</span><span class="sxs-lookup"><span data-stu-id="d3c92-148">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\App, "SouthridgeVideo", "Southridge Video Player"</span></span>
-   <span data-ttu-id="d3c92-149">\_В классах hKey \_ корневое \\ программное обеспечение \\ Microsoft \\ MediaPlayer \\ Setup \\ Депендентрефкаунтс \\ дескриптор "саусриджевидео", "Саусридже Video Player использует пакет SDK Windows Media Format для воспроизведения видеофайлов".</span><span class="sxs-lookup"><span data-stu-id="d3c92-149">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\Descriptor, "SouthridgeVideo", "Southridge Video Player uses the Windows Media Format SDK to play video files."</span></span>
-   <span data-ttu-id="d3c92-150">\_Классы hKey \_ root \\ Software \\ \\ программа установки Microsoft MediaPlayer \\ \\ депендентрефкаунтс \\ версия, "саусриджевидео", "9.0.0.2600"</span><span class="sxs-lookup"><span data-stu-id="d3c92-150">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\Version, "SouthridgeVideo", "9.0.0.2600"</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3c92-151">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="d3c92-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3c92-152">**Параметры реестра**</span><span class="sxs-lookup"><span data-stu-id="d3c92-152">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




