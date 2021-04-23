---
description: .
ms.assetid: f022374d-ea3f-477f-9b59-3188b775ed64
title: Манифест приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf4fd1ae8a9f66dafbe65a3db09dd014dbef31e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713037"
---
# <a name="application-manifest"></a><span data-ttu-id="dd632-103">Манифест приложения</span><span class="sxs-lookup"><span data-stu-id="dd632-103">Application Manifest</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="dd632-104">Затронутые платформы</span><span class="sxs-lookup"><span data-stu-id="dd632-104">Affected Platforms</span></span>

<span data-ttu-id="dd632-105">**Клиенты** — Windows 7</span><span class="sxs-lookup"><span data-stu-id="dd632-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="dd632-106">**Серверы** — Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dd632-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="dd632-107">Воздействие на функции</span><span class="sxs-lookup"><span data-stu-id="dd632-107">Feature Impact</span></span>

 <span data-ttu-id="dd632-108">**Серьезность** — низкая</span><span class="sxs-lookup"><span data-stu-id="dd632-108">**Severity** - Low</span></span>  
<span data-ttu-id="dd632-109">**Частота** -низкая</span><span class="sxs-lookup"><span data-stu-id="dd632-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="dd632-110">Описание</span><span class="sxs-lookup"><span data-stu-id="dd632-110">Description</span></span>

<span data-ttu-id="dd632-111">В Windows 7 появился новый раздел манифеста приложения под названием «совместимость».</span><span class="sxs-lookup"><span data-stu-id="dd632-111">Windows 7 introduces a new section in the application manifest called "Compatibility."</span></span> <span data-ttu-id="dd632-112">В этом разделе описывается, как Windows определяет версии Windows, предназначенные для приложения, и позволяет Windows предоставлять поведение, ожидаемое приложением в зависимости от версии Windows, для которой предназначено приложение.</span><span class="sxs-lookup"><span data-stu-id="dd632-112">This section helps Windows determine the versions of Windows that an application was designed to target, and enables Windows to provide the behavior that the application expects based on the version of Windows that the application targeted.</span></span>

<span data-ttu-id="dd632-113">Раздел совместимости позволяет Windows предоставлять новое поведение для нового программного обеспечения, созданного разработчиком, сохраняя совместимость с существующим программным обеспечением.</span><span class="sxs-lookup"><span data-stu-id="dd632-113">The Compatibility section allows Windows to provide new behavior to new developer-created software while maintaining the compatibility for existing software.</span></span> <span data-ttu-id="dd632-114">Этот раздел также помогает Windows обеспечить более высокую совместимость в будущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="dd632-114">This section also helps Windows deliver greater compatibility in future versions of Windows as well.</span></span> <span data-ttu-id="dd632-115">Например, приложение, объявляющая поддержку только для Windows 7 в разделе "совместимость", будет продолжать появление поведения Windows 7 в будущей версии Windows.</span><span class="sxs-lookup"><span data-stu-id="dd632-115">For example, an application declaring support only for Windows 7 in the Compatibility section will continue to receive Windows 7 behavior in future version of Windows.</span></span>

## <a name="manifestation-of-change"></a><span data-ttu-id="dd632-116">Изменение манифеста</span><span class="sxs-lookup"><span data-stu-id="dd632-116">Manifestation of Change</span></span>

<span data-ttu-id="dd632-117">Приложения без раздела совместимости в манифесте по умолчанию получат поведение Windows Vista в Windows 7 и будущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="dd632-117">Applications without a Compatibility section in their manifest will receive Windows Vista behavior by default on Windows 7 and future Windows versions.</span></span> <span data-ttu-id="dd632-118">Обратите внимание, что Windows XP и Windows Vista не пропускают этот раздел манифеста и не влияют на них.</span><span class="sxs-lookup"><span data-stu-id="dd632-118">Note that Windows XP and Windows Vista ignore this manifest section and it has no impact on them.</span></span>

<span data-ttu-id="dd632-119">Следующие компоненты Windows предоставляют разные режимы работы на основе раздела Compatibility в Windows 7:</span><span class="sxs-lookup"><span data-stu-id="dd632-119">The following Windows components provide divergent behavior based on the Compatibility section in Windows 7:</span></span>

<span data-ttu-id="dd632-120">**Пул потоков RPC по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="dd632-120">**RPC Default Thread Pool**</span></span>

-   <span data-ttu-id="dd632-121">**Windows 7:** Чтобы повысить масштабируемость и сократить число потоков, RPC переключится в пул потоков NT (пул по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="dd632-121">**Windows 7:** To improve scalability and reduce thread counts, RPC switched to the NT thread pool (default pool).</span></span> <span data-ttu-id="dd632-122">В Windows Vista RPC использовал частный пул потоков.</span><span class="sxs-lookup"><span data-stu-id="dd632-122">For Windows Vista, RPC used a private thread pool.</span></span>
    -   <span data-ttu-id="dd632-123">Для двоичных файлов, скомпилированных для Win7, используется пул по умолчанию</span><span class="sxs-lookup"><span data-stu-id="dd632-123">For binaries compiled for Win7 the default pool is used</span></span>
    -   <span data-ttu-id="dd632-124">Если я \_ рпкмгмтенабледедикатедсреадпул вызов до вызова API RPC, используется пул частных потоков (поведение Vista).</span><span class="sxs-lookup"><span data-stu-id="dd632-124">If I\_RpcMgmtEnableDedicatedThreadPool is called before any RPC API is called, the private thread pool is used (Vista behavior)</span></span>
    -   <span data-ttu-id="dd632-125">Если \_ рпкмгмтенабледедикатедсреадпул вызывается после вызова RPC, используется пул по умолчанию, I \_ рпкмгмтенабледедикатедсреадпул возвращает ошибку 1764, а запрошенная операция не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dd632-125">If I\_RpcMgmtEnableDedicatedThreadPool is called after an RPC call, the default pool is used, I\_RpcMgmtEnableDedicatedThreadPool returns the error 1764, and the requested operation is not supported</span></span>
-   <span data-ttu-id="dd632-126">**Windows Vista (по умолчанию):** Для двоичных файлов, скомпилированных для Windows Vista и ниже, используется частный пул.</span><span class="sxs-lookup"><span data-stu-id="dd632-126">**Windows Vista (default):** For binaries compiled for Windows Vista and below, the private pool is used.</span></span>

<span data-ttu-id="dd632-127">**Блокировка DirectDraw**</span><span class="sxs-lookup"><span data-stu-id="dd632-127">**DirectDraw Lock**</span></span>

-   <span data-ttu-id="dd632-128">**Windows 7:** Приложения, которые были манифесты для Windows 7, не могут вызвать API блокировки в ДДРАВ для блокировки видеобуфера основного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="dd632-128">**Windows 7:** Applications manifested for Windows 7 cannot call Lock API in DDRAW to lock the primary Desktop video buffer.</span></span> <span data-ttu-id="dd632-129">Это приведет к ошибке, и будет возвращен **пустой** указатель для первичной реплики.</span><span class="sxs-lookup"><span data-stu-id="dd632-129">Doing so will result in error, and **NULL** pointer for the primary will be returned.</span></span> <span data-ttu-id="dd632-130">Это поведение применяется, даже если диспетчер окон рабочего стола композиция не включена.</span><span class="sxs-lookup"><span data-stu-id="dd632-130">This behavior is enforced even if Desktop Window Manager Composition is not turned on.</span></span> <span data-ttu-id="dd632-131">Приложения, совместимые с Windows 7, не должны блокировать основной буфер видео для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="dd632-131">Windows 7 compatible applications must not lock the primary video buffer to render.</span></span>
-   <span data-ttu-id="dd632-132">**Windows Vista (по умолчанию):** Приложения смогут получить блокировку основного видеобуфера, так как устаревшие приложения зависят от этого поведения.</span><span class="sxs-lookup"><span data-stu-id="dd632-132">**Windows Vista (default):** Applications will be able to acquire a lock on the primary video buffer as legacy applications depend on this behavior.</span></span> <span data-ttu-id="dd632-133">Запуск приложения выключает диспетчер окон рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="dd632-133">Running the application turns off Desktop Window Manager.</span></span>

<span data-ttu-id="dd632-134">**Блочный блок DirectDraw (БЛТ) до первичного без усечения окна**</span><span class="sxs-lookup"><span data-stu-id="dd632-134">**DirectDraw Bit Block Transfer (Blt) to Primary without Clipping Window**</span></span>

-   <span data-ttu-id="dd632-135">**Windows 7:** Приложения, манифестные для Windows 7, не могут выполнять БЛТ в видеобуфер основного рабочего стола без окна обрезки.</span><span class="sxs-lookup"><span data-stu-id="dd632-135">**Windows 7:** Applications manifested for Windows 7 are prevented from performing Blt's to the primary Desktop video buffer without a clipping window.</span></span> <span data-ttu-id="dd632-136">Это приведет к ошибке, и область БЛТ не будет подготовлена к просмотру.</span><span class="sxs-lookup"><span data-stu-id="dd632-136">Doing so will result in error and the Blt area will not be rendered.</span></span> <span data-ttu-id="dd632-137">Windows обеспечивает это поведение, даже если вы не включаете диспетчер окон рабочего столаную композицию.</span><span class="sxs-lookup"><span data-stu-id="dd632-137">Windows enforces this behavior even if you do not turn on Desktop Window Manager Composition.</span></span> <span data-ttu-id="dd632-138">Приложения, совместимые с Windows 7, должны БЛТ в окно обрезки.</span><span class="sxs-lookup"><span data-stu-id="dd632-138">Windows 7 compatible applications must Blt to a clipping window.</span></span>
-   <span data-ttu-id="dd632-139">**Windows Vista (по умолчанию):** Приложения должны иметь возможность БЛТ к основному приложению без окна обрезки, так как устаревшие приложения зависят от этого поведения.</span><span class="sxs-lookup"><span data-stu-id="dd632-139">**Windows Vista (default):** Applications must be able to Blt to the primary without a clipping window as legacy applications depend on this behavior.</span></span> <span data-ttu-id="dd632-140">Запуск этого приложения выключает диспетчер окон рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="dd632-140">Running this application turns off the Desktop Window Manager.</span></span>

<span data-ttu-id="dd632-141">**API GetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="dd632-141">**GetOverlappedResult API**</span></span>

-   <span data-ttu-id="dd632-142">**Windows 7:** Разрешает состояние гонки, когда многопоточное приложение, использующее GetOverlappedResult, может возвращаться без сброса события в структуре OVERLAPPED, что приводит к преждевременному возвращению следующего вызова этой функции.</span><span class="sxs-lookup"><span data-stu-id="dd632-142">**Windows 7:** Resolves a race condition where a multithreaded app using GetOverlappedResult can return without resetting the event in the overlapped structure, causing the next call to this function to return prematurely.</span></span>
-   <span data-ttu-id="dd632-143">**Windows Vista (по умолчанию):** Обеспечивает поведение с условием гонки о том, что приложения могут иметь зависимость от.</span><span class="sxs-lookup"><span data-stu-id="dd632-143">**Windows Vista (default):** Provides the behavior with the race condition that applications may have a dependency on.</span></span> <span data-ttu-id="dd632-144">Приложения, желающие избежать этого состязания перед поведением Windows 7, должны ждать перекрытое событие и при получении сигнала вызвать GetOverlappedResult с Бваит = = **false**.</span><span class="sxs-lookup"><span data-stu-id="dd632-144">Applications wishing to avoid this race prior to the Windows 7 behavior should wait on the overlapped event and when signaled, call GetOverlappedResult with bWait == **FALSE**.</span></span>

<span data-ttu-id="dd632-145">**Помощник по совместимости программ (PCA)**</span><span class="sxs-lookup"><span data-stu-id="dd632-145">**Program Compatibility Assistant (PCA)**</span></span>

-   <span data-ttu-id="dd632-146">**Windows 7:** Приложения с разделом совместимости не будут получать исправление PCA.</span><span class="sxs-lookup"><span data-stu-id="dd632-146">**Windows 7:** Applications with Compatibility section will not get the PCA mitigation.</span></span>
-   <span data-ttu-id="dd632-147">**Windows Vista (по умолчанию):** Приложения, которые не удается правильно установить или завершить работу во время выполнения при определенных обстоятельствах, приведут к устранению уязвимости PCA.</span><span class="sxs-lookup"><span data-stu-id="dd632-147">**Windows Vista (default):** Applications that fail to install properly or crash during runtime under some specific circumstances will get the PCA mitigation.</span></span> <span data-ttu-id="dd632-148">Дополнительные сведения см. в разделе справки.</span><span class="sxs-lookup"><span data-stu-id="dd632-148">For more details, see the reference section.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="dd632-149">Использование возможностей функций</span><span class="sxs-lookup"><span data-stu-id="dd632-149">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="dd632-150">Обновите манифест приложения, используя последние сведения о совместимости для поддержки операционной системы.</span><span class="sxs-lookup"><span data-stu-id="dd632-150">Update the application manifest with the latest Compatibility information for operating system support.</span></span> <span data-ttu-id="dd632-151">В разделе описаны дополнения к манифесту:</span><span class="sxs-lookup"><span data-stu-id="dd632-151">The section describes the additions to the manifest:</span></span>

-   <span data-ttu-id="dd632-152">**Пространство имен:** Compatibility. v1 (xmlns = "urn: схемы-Microsoft-COM: Compatibility. v1" >)</span><span class="sxs-lookup"><span data-stu-id="dd632-152">**Namespace:** Compatibility.v1 (xmlns="urn:schemas-microsoft-com:compatibility.v1">)</span></span>

-   <span data-ttu-id="dd632-153">**Имя раздела:** Совместимость (новый раздел)</span><span class="sxs-lookup"><span data-stu-id="dd632-153">**Section Name:** Compatibility (new section)</span></span>

-   <span data-ttu-id="dd632-154">**Суппортедос:** GUID поддерживаемой операционной системы — идентификаторы GUID, которые сопоставляются с поддерживаемыми операционными системами:</span><span class="sxs-lookup"><span data-stu-id="dd632-154">**SupportedOS:** GUID of supported operating system - The GUIDs that map to the supported operating systems are:</span></span>

    -   <span data-ttu-id="dd632-155">{e2011457-1546-43c5-a5fe-008deee3d3f0} для Windows Vista: это значение по умолчанию для контекста свитчбакк.</span><span class="sxs-lookup"><span data-stu-id="dd632-155">{e2011457-1546-43c5-a5fe-008deee3d3f0} for Windows Vista: This is the default value for the switchback context.</span></span>
    -   <span data-ttu-id="dd632-156">{35138b9a-5d96-4fbd-8e2d-a2440225f93a} для Windows 7: приложения, которые задают это значение в манифесте приложения, получают поведение Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dd632-156">{35138b9a-5d96-4fbd-8e2d-a2440225f93a} for Windows 7: Applications that set this value in the application manifest get the Windows 7 behavior.</span></span>

    > [!Note]  
    > <span data-ttu-id="dd632-157">Корпорация Майкрософт будет создавать и публиковать идентификаторы GUID для будущих версий Windows по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="dd632-157">Microsoft will generate and post GUIDs for future Windows versions as needed.</span></span>

     

<span data-ttu-id="dd632-158">Ниже приведен пример обновленного манифеста.</span><span class="sxs-lookup"><span data-stu-id="dd632-158">The following is an example of an updated manifest.</span></span>

> [!Note]  
> <span data-ttu-id="dd632-159">Имена атрибутов и тегов в манифесте приложения чувствительны к регистру.</span><span class="sxs-lookup"><span data-stu-id="dd632-159">The attribute and tag names in the application manifest are case sensitive.</span></span>

 


```XML
<?xml version="1.0" encoding="UTF-8" standalone="yes"?> 
  <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
      <application> 
        <!--The ID below indicates application support for Windows Vista --> 
          <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--The ID below indicates application support for Windows 7 --> 
          <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/> 
      </application> 
    </compatibility>
  </assembly>
```



<span data-ttu-id="dd632-160">Значение добавления идентификаторов GUID для обеих операционных систем в приведенном выше примере — предоставление поддержки нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="dd632-160">The value of adding GUIDs for both operating systems in the above example is to provide down-level support.</span></span> <span data-ttu-id="dd632-161">Для приложений, поддерживающих обе платформы, отдельные манифесты для каждой платформы не требуются.</span><span class="sxs-lookup"><span data-stu-id="dd632-161">Applications that support both platforms would not need separate manifests for each platform.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="dd632-162">Совместимость, производительность, надежность и тестирование на удобство использования</span><span class="sxs-lookup"><span data-stu-id="dd632-162">Compatibility, Performance, Reliability, and Usability Testing</span></span>

1.  <span data-ttu-id="dd632-163">Протестируйте приложение с помощью нового раздела "совместимость" и `SupportedOS ID ={35138b9a-5d96-4fbd-8e2d-a2440225f93a}` Убедитесь, что приложение работает правильно, используя Последнее поведение Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dd632-163">Test the application with the new compatibility section and `SupportedOS ID ={35138b9a-5d96-4fbd-8e2d-a2440225f93a}` to ensure that the application works properly using the latest Windows 7 behavior</span></span>
2.  <span data-ttu-id="dd632-164">Протестируйте приложение с новым разделом совместимости и `SupportedOS ID ={e2011457-1546-43c5-a5fe-008deee3d3f0}` (или без него целиком), чтобы убедиться, что приложение работает правильно с использованием поведения Windows Vista в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dd632-164">Test the application with the new compatibility section and `SupportedOS ID ={e2011457-1546-43c5-a5fe-008deee3d3f0}` (or without this section entirely) to ensure that the application works properly using the Windows Vista behaviors on Windows 7</span></span>

## <a name="known-issues"></a><span data-ttu-id="dd632-165">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="dd632-165">Known Issues</span></span>

<span data-ttu-id="dd632-166">**Несоответствие контекста** Приложение выполняется в контексте Windows Vista, а не в контексте Windows 7 на компьютере с 64-разрядной операционной системой Windows 7 или Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="dd632-166">**Context Mismatch** An application runs in a Windows Vista context instead of in a Windows 7 context on a computer that is running an x64 edition of either Windows 7 or Windows Server 2008 R2.</span></span>

<span data-ttu-id="dd632-167">**Решение** Доступны обновления для всех поддерживаемых 64-разрядных версий Windows 7 и Windows Server 2008 R2, а также для всех поддерживаемых версий Windows Server 2008 R2 на основе Itanium.</span><span class="sxs-lookup"><span data-stu-id="dd632-167">**Solution** Updates are available to correct this for all supported x64-based versions of Windows 7 and Windows Server 2008 R2, as well as for all supported Itanium-based versions of Windows Server 2008 R2.</span></span> <span data-ttu-id="dd632-168">Перейдите на страницу служба поддержки Майкрософт [KB 978637: приложение выполняется в контексте Windows Vista, а не в контексте Windows 7 на компьютере с 64-разрядной версией Windows 7 или Windows Server 2008 R2](https://support.microsoft.com/kb/978637) для получения дополнительных сведений и загрузки правильной версии для системы.</span><span class="sxs-lookup"><span data-stu-id="dd632-168">Go to the Microsoft Support page for [KB 978637: An application runs in a Windows Vista context instead of in a Windows 7 context on a computer that is running an x64 edition of Windows 7 or of Windows Server 2008 R2](https://support.microsoft.com/kb/978637) for additional details and to download the correct version for your system.</span></span>

<span data-ttu-id="dd632-169">**Диагностика аварийного дампа заблокирована**</span><span class="sxs-lookup"><span data-stu-id="dd632-169">**Crash dump diagnosis blocked**</span></span>

<span data-ttu-id="dd632-170">**Решение** Перейдите на страницу служба поддержки Майкрософт [KB 976038. исключения, возникающие в приложении, которое выполняется в 64-разрядной версии Windows, пропускаются](https://support.microsoft.com/kb/976038) для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="dd632-170">**Solution** Go to the Microsoft Support page for [KB 976038: Exceptions that are thrown from an application that runs in a 64-bit version of Windows are ignored](https://support.microsoft.com/kb/976038) for additional details.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="dd632-171">Ссылки на другие ресурсы</span><span class="sxs-lookup"><span data-stu-id="dd632-171">Links to Other Resources</span></span>

-   [<span data-ttu-id="dd632-172">**Функция Куеряктктксв**</span><span class="sxs-lookup"><span data-stu-id="dd632-172">**QueryActCtxW Function**</span></span>](/windows/win32/api/winbase/nf-winbase-queryactctxw)
-   <span data-ttu-id="dd632-173">[Манифест UAC](/previous-versions/bb756929(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="dd632-173">[UAC manifest](/previous-versions/bb756929(v=msdn.10))</span></span>
-   [<span data-ttu-id="dd632-174">Манифесты приложений для приложений Windows</span><span class="sxs-lookup"><span data-stu-id="dd632-174">Application manifests for Windows applications</span></span>](../sbscs/application-manifests.md)
-   [<span data-ttu-id="dd632-175">Диспетчер окон рабочего стола (DWM)</span><span class="sxs-lookup"><span data-stu-id="dd632-175">Desktop Window Manager (DWM)</span></span>](../dwm/dwm-overview.md)
-   [<span data-ttu-id="dd632-176">Обновление несовпадения контекста</span><span class="sxs-lookup"><span data-stu-id="dd632-176">Context Mismatch Update</span></span>](https://support.microsoft.com/kb/978637)

 

 
