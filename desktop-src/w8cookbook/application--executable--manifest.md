---
title: Манифест приложения (исполняемый)
description: Манифест приложения (исполняемый)
ms.assetid: F46F33A6-0B2F-4086-9C6D-4AD43C26BCD3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de6f5a1d26af4b8ac6314655013ed56275bf7d73
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "104070749"
---
# <a name="app-executable-manifest"></a><span data-ttu-id="8dc5c-103">Манифест приложения (исполняемый)</span><span class="sxs-lookup"><span data-stu-id="8dc5c-103">App (executable) manifest</span></span>

## <a name="platforms"></a><span data-ttu-id="8dc5c-104">Платформы</span><span class="sxs-lookup"><span data-stu-id="8dc5c-104">Platforms</span></span>

<span data-ttu-id="8dc5c-105">**Клиенты** — Windows 8</span><span class="sxs-lookup"><span data-stu-id="8dc5c-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="8dc5c-106">**Серверы** — Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8dc5c-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="8dc5c-107">Описание</span><span class="sxs-lookup"><span data-stu-id="8dc5c-107">Description</span></span>

<span data-ttu-id="8dc5c-108">Раздел Compatibility (совместимость) манифеста приложения, представленный в Windows, помогает операционной системе определить версии Windows, для которых предназначено приложение.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-108">The compatibility section of the app (executable) manifest introduced in Windows helps the operating system determine the versions of Windows an app was designed to target.</span></span> <span data-ttu-id="8dc5c-109">Кроме того, манифест приложения позволяет Windows предоставлять поведение, ожидаемое приложением в зависимости от версии Windows, для которой предназначено приложение.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-109">Additionally, the app manifest enables Windows to provide the behavior that the app expects based on the version of Windows that the app targeted.</span></span>

<span data-ttu-id="8dc5c-110">Раздел Compatibility (совместимость) манифеста позволяет Windows предоставлять новое поведение для вновь создаваемого программного обеспечения, сохраняя совместимость с существующим программным обеспечением.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-110">The compatibility section of the manifest allows Windows to provide new behavior to newly created software while maintaining the compatibility for existing software.</span></span> <span data-ttu-id="8dc5c-111">Этот раздел поможет Windows обеспечить более высокую совместимость в будущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-111">This section helps Windows deliver greater compatibility in future versions of Windows as well.</span></span> <span data-ttu-id="8dc5c-112">Например, приложение, объявляющая поддержку только для Windows 8 в разделе "совместимость", будет продолжать появление поведения Windows 8 в будущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-112">For example, an app declaring support for only Windows 8 in the compatibility section will continue to receive Windows 8 behavior in future versions of Windows.</span></span>

## <a name="manifestation"></a><span data-ttu-id="8dc5c-113">Проявление</span><span class="sxs-lookup"><span data-stu-id="8dc5c-113">Manifestation</span></span>

<span data-ttu-id="8dc5c-114">Приложения без раздела совместимости в манифесте будут иметь поведение Windows Vista по умолчанию в Windows 7 и Windows 8 и в будущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-114">Apps without a compatibility section in their manifest will have Windows Vista behavior by default on Windows 7 and Windows 8 and future Windows versions.</span></span> <span data-ttu-id="8dc5c-115">Имейте в виду, что в Windows XP и Windows Vista этот раздел манифеста не влияет на них.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-115">Be aware that Windows XP and Windows Vista ignore this manifest section and it has no impact on them.</span></span>

<span data-ttu-id="8dc5c-116">Эти компоненты Windows предоставляют разные режимы работы на основе раздела совместимости:</span><span class="sxs-lookup"><span data-stu-id="8dc5c-116">These Windows components provide divergent behavior based on the compatibility section:</span></span>

<span data-ttu-id="8dc5c-117">**Пул потоков по умолчанию для удаленного вызова процедур (RPC)**</span><span class="sxs-lookup"><span data-stu-id="8dc5c-117">**Remote procedure call (RPC) default thread pool**</span></span>

-   <span data-ttu-id="8dc5c-118">Windows 8 и Windows 7. чтобы повысить масштабируемость и сократить число потоков, RPC переключится в пул потоков NT (пул по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="8dc5c-118">Windows 8 and Windows 7: To improve scalability and reduce thread counts, RPC switched to the NT thread pool (default pool).</span></span> <span data-ttu-id="8dc5c-119">Для Windows Vista RPC использовал частный пул потоков:</span><span class="sxs-lookup"><span data-stu-id="8dc5c-119">For Windows Vista, RPC used a private thread pool:</span></span>

    -   <span data-ttu-id="8dc5c-120">Для двоичных файлов, скомпилированных для Windows 7 и более поздних версий Windows, используется пул по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-120">For binaries compiled for Windows 7 and later versions of Windows, the default pool is used.</span></span>
    -   <span data-ttu-id="8dc5c-121">Если я \_ рпкмгмтенабледедикатедсреадпул вызов до вызова API RPC, используется пул частных потоков (поведение Vista).</span><span class="sxs-lookup"><span data-stu-id="8dc5c-121">If I\_RpcMgmtEnableDedicatedThreadPool is called before any RPC API is called, the private thread pool is used (Vista behavior).</span></span>
    -   <span data-ttu-id="8dc5c-122">Если \_ рпкмгмтенабледедикатедсреадпул вызывается после вызова RPC, используется пул по умолчанию, I \_ рпкмгмтенабледедикатедсреадпул возвращает ошибку 1764, а запрошенная операция не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-122">If I\_RpcMgmtEnableDedicatedThreadPool is called after an RPC call, the default pool is used, I\_RpcMgmtEnableDedicatedThreadPool returns the error 1764, and the requested operation is not supported.</span></span>

-   <span data-ttu-id="8dc5c-123">Windows Vista (по умолчанию). для двоичных файлов, скомпилированных для Windows Vista и более ранних версий Windows, используется частный пул.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-123">Windows Vista (default): For binaries compiled for Windows Vista and earlier versions of Windows, the private pool is used.</span></span>

<span data-ttu-id="8dc5c-124">**Блокировка DirectDraw**</span><span class="sxs-lookup"><span data-stu-id="8dc5c-124">**DirectDraw lock**</span></span>

-   <span data-ttu-id="8dc5c-125">Windows 8 и Windows 7: приложения, манифесты для Windows 7 и более поздних версий операционной системы, не могут вызывать API блокировки в ДДРАВ для блокировки видеобуфера основного рабочего стола; Это приведет к ошибке, и возвращается пустой указатель для первичной реплики.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-125">Windows 8 and Windows 7: Apps manifested for Windows 7 and later versions of the operating system cannot call Lock API in DDRAW to lock the primary desktop video buffer; doing so will result in an error, and a NULL pointer for the primary is returned.</span></span> <span data-ttu-id="8dc5c-126">Это поведение применяется, даже если диспетчер окон рабочего стола композиция не включена.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-126">This behavior is enforced even if Desktop Window Manager Composition is not turned on.</span></span> <span data-ttu-id="8dc5c-127">Приложения с совместимостью, объявленная для Windows 7 и более поздних версий, не должны блокировать основной видеобуфер для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-127">Apps with compatibility declared for Windows 7 and later must not lock the primary video buffer to render.</span></span>
-   <span data-ttu-id="8dc5c-128">Windows Vista (по умолчанию): приложения могут получить блокировку основного видеобуфера, так как устаревшие приложения зависят от этого поведения; Запуск приложения выключает диспетчер окон рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-128">Windows Vista (default): Apps can acquire a lock on the primary video buffer, as legacy apps depend on this behavior; running the app turns off Desktop Window Manager.</span></span>

<span data-ttu-id="8dc5c-129">**Бит DirectDraw — блочное перемещение (BitBlt) в основной без усечения окна**</span><span class="sxs-lookup"><span data-stu-id="8dc5c-129">**DirectDraw bit-block transfer (bitblt) to primary without clipping window**</span></span>

-   <span data-ttu-id="8dc5c-130">Windows 8 и Windows 7: приложения, манифесты для Windows 7 и более поздних версий Windows, не могут выполнять BitBlt в видеобуфер основного рабочего стола без окна обрезки. Это приведет к ошибке, а область BitBlt не будет подготовлена к просмотру.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-130">Windows 8 and Windows 7: Apps manifested for Windows 7 and later versions of Windows are prevented from performing a bitblt to the primary Desktop video buffer without a clipping window; doing so results in an error and the bitblt area will not be rendered.</span></span> <span data-ttu-id="8dc5c-131">Windows обеспечивает это поведение, даже если вы не включаете диспетчер окон рабочего столаную композицию.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-131">Windows enforces this behavior even if you do not turn on Desktop Window Manager Composition.</span></span> <span data-ttu-id="8dc5c-132">Приложения с совместимостью, объявленная для Windows 7 и более поздних версий, должны выполнять BitBlt в окне обрезки.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-132">Apps with compatibility declared for Windows 7 and later must perform a bitblt to a clipping window.</span></span>
-   <span data-ttu-id="8dc5c-133">Windows Vista (по умолчанию): приложения должны иметь возможность выполнять BitBlt к основному окну без обрезки, поскольку устаревшие приложения зависят от этого поведения; Запуск этого приложения выключает диспетчер окон рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-133">Windows Vista (default): Apps must be able to perform a bitblt to the primary without a clipping window, as legacy apps depend on this behavior; running this app turns off the Desktop Window Manager.</span></span>

<span data-ttu-id="8dc5c-134">**API GetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="8dc5c-134">**GetOverlappedResult API**</span></span>

-   <span data-ttu-id="8dc5c-135">Windows 8 и Windows 7: разрешает состояние гонки, когда многопоточное приложение, использующее **GetOverlappedResult** , может возвращаться без сброса события в структуре OVERLAPPED, что приводит к преждевременному возвращению следующего вызова этой функции.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-135">Windows 8 and Windows 7: Resolves a race condition where a multithreaded app using **GetOverlappedResult** can return without resetting the event in the overlapped structure, causing the next call to this function to return prematurely.</span></span>
-   <span data-ttu-id="8dc5c-136">Windows Vista (по умолчанию): обеспечивает поведение с условием гонки о том, что приложения могут иметь зависимость от.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-136">Windows Vista (default): Provides the behavior with the race condition that apps might have a dependency on.</span></span> <span data-ttu-id="8dc5c-137">Приложения, которые должны избежать этого состязания перед поведением Windows 7, должны ожидать перекрытое событие и при получении сигнала вызвать GetOverlappedResult с Бваит = = FALSE.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-137">Apps that must avoid this race prior to the Windows 7 behavior should wait on the overlapped event and, when signaled, call GetOverlappedResult with bWait == FALSE.</span></span>

<span data-ttu-id="8dc5c-138">**Состояние тем оболочки в режиме высокой контрастности**</span><span class="sxs-lookup"><span data-stu-id="8dc5c-138">**Shell themes status in high contrast mode**</span></span>

-   <span data-ttu-id="8dc5c-139">Windows 8: возвращает реальные сведения о состоянии в режиме высокой контрастности.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-139">Windows 8: Returns the real theming status for when in high contrast mode.</span></span>
-   <span data-ttu-id="8dc5c-140">Windows 7: возвращает их как недоступные в режиме высокой контрастности, так как DWM все еще включен.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-140">Windows 7: Returns theming as unavailable when in high contrast mode because DWM is still on.</span></span>
-   <span data-ttu-id="8dc5c-141">Windows Vista (по умолчанию): возвращает их как недоступные в режиме высокой контрастности, так как DWM все еще включен.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-141">Windows Vista (default): Returns theming as unavailable when in high contrast mode because DWM is still on.</span></span>

<span data-ttu-id="8dc5c-142">**Shell iPersistFile:: Save, метод**</span><span class="sxs-lookup"><span data-stu-id="8dc5c-142">**Shell iPersistFile::Save method**</span></span>

-   <span data-ttu-id="8dc5c-143">Windows 8: Кшелллинк:: Save теперь определяет, вызывается ли обработчик IPersistFile с аргументом относительного пути и завершается с ошибкой, если это так.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-143">Windows 8: CShellLink::Save now determines if the IPersistFile handler is called with a relative path argument and fails the call if it is.</span></span>

    <span data-ttu-id="8dc5c-144">[Общедоступная документация](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) , описывающая это поведение, указывает, что аргумент path должен быть абсолютным путем:</span><span class="sxs-lookup"><span data-stu-id="8dc5c-144">The [public documentation](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) describing this behavior indicates that path argument has to be an absolute path:</span></span>

-   <span data-ttu-id="8dc5c-145">Windows 7 и более ранние версии (по умолчанию): Кшелллинк:: Save не определяет, отправляет ли обработчик iPersistFile проверку относительного пути, и позволяет приложениям продолжать работать с абсолютными или относительными путями.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-145">Windows 7 and earlier (default): CShellLink::Save does not determine if the iPersistFile handler sends a relative path check and allows apps to continue working with absolute or relative paths.</span></span>

<span data-ttu-id="8dc5c-146">**Помощник по совместимости программ (PCA)**</span><span class="sxs-lookup"><span data-stu-id="8dc5c-146">**Program Compatibility Assistant (PCA)**</span></span>

-   <span data-ttu-id="8dc5c-147">Windows 8: приложения с разделом совместимости не получают устранения уязвимости PCA.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-147">Windows 8: Apps with the compatibility section do not get the PCA mitigation.</span></span>
-   <span data-ttu-id="8dc5c-148">Windows 7: приложения с разделом совместимости отправляются на потенциальные проблемы совместимости для изменений в Windows 8 (описанные в этом документе).</span><span class="sxs-lookup"><span data-stu-id="8dc5c-148">Windows 7: Apps with the compatibility section are tracked for potential compatibility issues for Windows 8 changes (described in this document).</span></span>
-   <span data-ttu-id="8dc5c-149">Windows Vista (по умолчанию): приложения, которые не удается правильно установить или завершить работу во время выполнения при определенных обстоятельствах, получают возможность устранения уязвимости PCA.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-149">Windows Vista (default): Apps that fail to install properly or crash during runtime under some specific circumstances get the PCA mitigation.</span></span> <span data-ttu-id="8dc5c-150">Дополнительные сведения см. в разделе Resources.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-150">For more info, see the Resources section.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="8dc5c-151">Использование возможностей функций</span><span class="sxs-lookup"><span data-stu-id="8dc5c-151">Leveraging feature capabilities</span></span>

<span data-ttu-id="8dc5c-152">Обновите манифест приложения, используя последние сведения о совместимости для поддержки операционной системы.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-152">Update the app manifest with the latest compatibility info for operating system support.</span></span> <span data-ttu-id="8dc5c-153">В этом разделе описаны дополнения к манифесту.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-153">This section describes the additions to the manifest:</span></span>

<span data-ttu-id="8dc5c-154">**Пространство имен:** Compatibility. v1 (xmlns = "urn: схемы-Microsoft-COM: Compatibility. v1" >)</span><span class="sxs-lookup"><span data-stu-id="8dc5c-154">**Namespace:** Compatibility.v1 (xmlns="urn:schemas-microsoft-com:compatibility.v1">)</span></span>

<span data-ttu-id="8dc5c-155">**Имя раздела:** Совместимость (новый раздел)</span><span class="sxs-lookup"><span data-stu-id="8dc5c-155">**Section name:** Compatibility (new section)</span></span>

<span data-ttu-id="8dc5c-156">**Суппортедос:** GUID поддерживаемой операционной системы — идентификаторы GUID, которые сопоставляются с поддерживаемыми операционными системами:</span><span class="sxs-lookup"><span data-stu-id="8dc5c-156">**SupportedOS:** GUID of supported operating system - The GUIDs that map to the supported operating systems are:</span></span>

-   <span data-ttu-id="8dc5c-157">{e2011457-1546-43c5-a5fe-008deee3d3f0}</span><span class="sxs-lookup"><span data-stu-id="8dc5c-157">{e2011457-1546-43c5-a5fe-008deee3d3f0}</span></span>

    <span data-ttu-id="8dc5c-158">для **Windows Vista**: это значение по умолчанию для контекста свитчбакк.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-158">for **Windows Vista**: This is the default value for the switchback context</span></span>

-   <span data-ttu-id="8dc5c-159">{35138b9a-5d96-4fbd-8e2d-a2440225f93a}</span><span class="sxs-lookup"><span data-stu-id="8dc5c-159">{35138b9a-5d96-4fbd-8e2d-a2440225f93a}</span></span>

    <span data-ttu-id="8dc5c-160">для **Windows 7**: приложения, которые задают это значение в манифесте приложения, получают поведение Windows 7</span><span class="sxs-lookup"><span data-stu-id="8dc5c-160">for **Windows 7**: Apps that set this value in the app manifest get the Windows 7 behavior</span></span>

-   <span data-ttu-id="8dc5c-161">{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}</span><span class="sxs-lookup"><span data-stu-id="8dc5c-161">{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}</span></span>

    <span data-ttu-id="8dc5c-162">для **Windows 8**: приложения, которые задают это значение в манифесте приложения, получают поведение Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-162">for **Windows 8**: Apps that set this value in the application manifest get the Windows 8 behavior</span></span>

<span data-ttu-id="8dc5c-163">Корпорация Майкрософт будет создавать и публиковать идентификаторы GUID для будущих версий Windows по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-163">Microsoft will generate and post GUIDs for future Windows versions as needed.</span></span>

<span data-ttu-id="8dc5c-164">XML-пример обновленного манифеста:</span><span class="sxs-lookup"><span data-stu-id="8dc5c-164">An XML example of an updated manifest:</span></span>

> [!Note]  
> <span data-ttu-id="8dc5c-165">Имена атрибутов и тегов в манифесте приложения чувствительны к регистру.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-165">The attribute and tag names in the app manifest are case sensitive.</span></span>

 


```XML
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
<compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
    <application> 
        <!--The ID below indicates app support for Windows Vista -->
        <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--The ID below indicates app support for Windows 7 -->
        <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        <!--The ID below indicates app support for Windows 8 -->
        <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
    </application> 
</compatibility>
</assembly>
```



<span data-ttu-id="8dc5c-166">Идентификаторы GUID для всех операционных систем в предыдущем примере обеспечивают поддержку нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-166">The GUIDs for all the operating systems in the previous example provide down-level support.</span></span> <span data-ttu-id="8dc5c-167">Для приложений, поддерживающих несколько платформ, отдельные манифесты для каждой платформы не требуются.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-167">Apps that support multiple platforms do not need separate manifests for each platform.</span></span>

## <a name="tests"></a><span data-ttu-id="8dc5c-168">Тесты</span><span class="sxs-lookup"><span data-stu-id="8dc5c-168">Tests</span></span>

<span data-ttu-id="8dc5c-169">В приложении можно указать несколько поддерживаемых идентификаторов операционной системы.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-169">An app can specify multiple supported operating system IDs.</span></span> <span data-ttu-id="8dc5c-170">Необходимо добавить поддерживаемый идентификатор операционной системы, если вы тестировали или намерены в процессе тестирования приложения в этой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-170">You should add a supported operating system ID if you have tested, or are in the process of testing, the app on that operating system.</span></span> <span data-ttu-id="8dc5c-171">Windows Vista и предыдущие версии операционной системы не обращают внимания на эти записи.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-171">Windows Vista and prior operating system versions do not pay attention to these entries.</span></span> <span data-ttu-id="8dc5c-172">Начиная с Windows 7, Windows выберет наивысший идентификатор GUID в манифесте вплоть до работающей версии Windows и предоставит поддержку приложений на этом уровне.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-172">Starting with Windows 7, Windows will choose the highest version GUID in the manifest up to the running Windows version, and give the app support at that level.</span></span> <span data-ttu-id="8dc5c-173">Чтобы убедиться, что приложение работает с новым разделом совместимости манифеста приложения, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-173">To verify that the app works with the new app manifest compatibility section:</span></span>

1.  <span data-ttu-id="8dc5c-174">Протестируйте приложение с новым разделом совместимости и Суппортедос ID = {4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}, чтобы убедиться, что приложение работает правильно, используя Последнее поведение Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-174">Test the app with the new compatibility section and SupportedOS ID = { 4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38} to ensure that the app works properly using the latest Windows 8 behavior.</span></span>
2.  <span data-ttu-id="8dc5c-175">Протестируйте приложение с новым разделом совместимости и Суппортедос ID = {35138b9a-5d96-4fbd-8e2d-a2440225f93a}, чтобы обеспечить правильную работу приложения с поведением Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-175">Test the app with the new compatibility section and SupportedOS ID = {35138b9a-5d96-4fbd-8e2d-a2440225f93a} to ensure that the app works properly using the Windows 7 behavior.</span></span>
3.  <span data-ttu-id="8dc5c-176">Протестируйте приложение с новым разделом совместимости и Суппортедос ID = {e2011457-1546-43c5-a5fe-008deee3d3f0}, чтобы обеспечить правильную работу приложения с поведением Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-176">Test the app with the new compatibility section and SupportedOS ID = {e2011457-1546-43c5-a5fe-008deee3d3f0} to ensure that the app works properly using the Windows Vista behavior.</span></span>

## <a name="resources"></a><span data-ttu-id="8dc5c-177">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="8dc5c-177">Resources</span></span>

-   [<span data-ttu-id="8dc5c-178">Функция Куеряктктксв</span><span class="sxs-lookup"><span data-stu-id="8dc5c-178">QueryActCtxW Function</span></span>](../sbscs/application-manifests.md)
-   <span data-ttu-id="8dc5c-179">[Манифест UAC](/previous-versions/bb756929(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="8dc5c-179">[UAC manifest](/previous-versions/bb756929(v=msdn.10))</span></span>
-   [<span data-ttu-id="8dc5c-180">Манифесты приложений для приложений Windows</span><span class="sxs-lookup"><span data-stu-id="8dc5c-180">Application Manifests for Windows Applications</span></span>](../sbscs/application-manifests.md)
-   [<span data-ttu-id="8dc5c-181">Диспетчер окон рабочего стола (DWM)</span><span class="sxs-lookup"><span data-stu-id="8dc5c-181">Desktop Window Manager (DWM)</span></span>](../dwm/dwm-overview.md)
-   [<span data-ttu-id="8dc5c-182">Обновление несовпадения контекста</span><span class="sxs-lookup"><span data-stu-id="8dc5c-182">Context Mismatch Update</span></span>](https://support.microsoft.com/kb/978637)
-   <span data-ttu-id="8dc5c-183">[Помощник по совместимости программ](/previous-versions/bb756937(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="8dc5c-183">[Program Compatibility Assistant](/previous-versions/bb756937(v=msdn.10))</span></span>

 

 