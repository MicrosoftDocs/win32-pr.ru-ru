---
description: Приложения могут управлять контекстом активации путем непосредственного вызова функций контекста активации.
ms.assetid: 606147a8-435d-43d4-8fb5-79d2d1a8d870
title: Использование API контекста активации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62b3aec5b7840e70e8fae93575e65c2f06668936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144491"
---
# <a name="using-the-activation-context-api"></a><span data-ttu-id="a12b4-103">Использование API контекста активации</span><span class="sxs-lookup"><span data-stu-id="a12b4-103">Using the Activation Context API</span></span>

<span data-ttu-id="a12b4-104">Приложения могут управлять [контекстом активации](activation-contexts.md) путем непосредственного вызова функций контекста активации.</span><span class="sxs-lookup"><span data-stu-id="a12b4-104">Applications can manage an [activation context](activation-contexts.md) by directly calling the activation context functions.</span></span> <span data-ttu-id="a12b4-105">Контексты активации — это структуры данных в памяти.</span><span class="sxs-lookup"><span data-stu-id="a12b4-105">Activation contexts are data structures in memory.</span></span> <span data-ttu-id="a12b4-106">Система может использовать сведения в контексте активации для перенаправления приложения для загрузки конкретной версии DLL, экземпляра объекта COM или пользовательской версии окна.</span><span class="sxs-lookup"><span data-stu-id="a12b4-106">The system can use the information in the activation context to redirect an application to load a particular DLL version, COM object instance, or custom window version.</span></span> <span data-ttu-id="a12b4-107">Дополнительные сведения см. в разделе [Справочник по контексту активации](activation-context-reference.md).</span><span class="sxs-lookup"><span data-stu-id="a12b4-107">For more information, see [Activation Context Reference](activation-context-reference.md).</span></span>

<span data-ttu-id="a12b4-108">Прикладной программный интерфейс (API) можно использовать для управления контекстом активации и создания объектов с именованием версий с [манифестами](manifests.md).</span><span class="sxs-lookup"><span data-stu-id="a12b4-108">The application programming interface (API) can be used to manage the activation context and create version-named objects with [manifests](manifests.md).</span></span> <span data-ttu-id="a12b4-109">В следующих двух сценариях показано, как приложение может управлять контекстом активации путем непосредственного вызова функций контекста активации.</span><span class="sxs-lookup"><span data-stu-id="a12b4-109">The following two scenarios illustrate how an application can manage an activation context by directly calling the activation context functions.</span></span> <span data-ttu-id="a12b4-110">Однако в большинстве случаев управление контекстом активации осуществляется системой.</span><span class="sxs-lookup"><span data-stu-id="a12b4-110">In most cases however, the activation context is managed by the system.</span></span> <span data-ttu-id="a12b4-111">Разработчикам приложений и поставщикам сборок обычно не требуется вызывать стек для управления контекстом активации.</span><span class="sxs-lookup"><span data-stu-id="a12b4-111">Application developers and assembly providers do not commonly need to make calls to the stack to manage the activation context.</span></span>

-   <span data-ttu-id="a12b4-112">Процессы и приложения, которые реализуют слои косвенного обращения или диспетчеризации.</span><span class="sxs-lookup"><span data-stu-id="a12b4-112">Processes and applications that implement indirection or dispatch layers.</span></span>

    <span data-ttu-id="a12b4-113">Например, пользователь управляет контекстами активации в цикле событий.</span><span class="sxs-lookup"><span data-stu-id="a12b4-113">For example, a user managing activation contexts in the event loop.</span></span> <span data-ttu-id="a12b4-114">При каждом доступе к окну, например при перемещении указателя мыши на окно, вызывается [**активатеакткткс**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) , который активирует текущий контекст активации для ресурса, как показано в следующем фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="a12b4-114">Each time the window is accessed, such as by moving the mouse over the window, [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) is called, which activates the current activation context for the resource, as shown in the following code fragment.</span></span>

    <dl> <span data-ttu-id="a12b4-115">Обработайте Хакткткс;</span><span class="sxs-lookup"><span data-stu-id="a12b4-115">HANDLE hActCtx;</span></span>  
    <span data-ttu-id="a12b4-116">CreateWindow ();</span><span class="sxs-lookup"><span data-stu-id="a12b4-116">CreateWindow();</span></span>  
    <span data-ttu-id="a12b4-117">...</span><span class="sxs-lookup"><span data-stu-id="a12b4-117">...</span></span>  
    <span data-ttu-id="a12b4-118">Жеткуррентакткткс (&Акткткс);</span><span class="sxs-lookup"><span data-stu-id="a12b4-118">GetCurrentActCtx(&ActCtx);</span></span>  
    <span data-ttu-id="a12b4-119">...</span><span class="sxs-lookup"><span data-stu-id="a12b4-119">...</span></span>  
    <span data-ttu-id="a12b4-120">Релеасеакткткс (&Акткткс);</span><span class="sxs-lookup"><span data-stu-id="a12b4-120">ReleaseActCtx(&ActCtx);</span></span>  
    </dl>

    <span data-ttu-id="a12b4-121">В следующем фрагменте кода функция API активирует соответствующие контексты активации перед вызовом [**каллвиндовпрок**](/windows/win32/api/winuser/nf-winuser-callwindowproca).</span><span class="sxs-lookup"><span data-stu-id="a12b4-121">In the following code fragment, the API function activates the appropriate activation contexts before calling [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca).</span></span> <span data-ttu-id="a12b4-122">При вызове **каллвиндовпрок** он использует этот контекст для передачи сообщения в Windows.</span><span class="sxs-lookup"><span data-stu-id="a12b4-122">When **CallWindowProc** is called, it uses this context to pass a message to Windows.</span></span> <span data-ttu-id="a12b4-123">По завершении всех операций с ресурсами функция деактивирует контекст.</span><span class="sxs-lookup"><span data-stu-id="a12b4-123">When all resource operations have completed, the function will deactivate the context.</span></span>

    <dl> <span data-ttu-id="a12b4-124">ULONG \_ ptr улпкукие;</span><span class="sxs-lookup"><span data-stu-id="a12b4-124">ULONG\_PTR ulpCookie;</span></span>  
    <span data-ttu-id="a12b4-125">Обработайте Хакткткс;</span><span class="sxs-lookup"><span data-stu-id="a12b4-125">HANDLE hActCtx;</span></span>  
    <span data-ttu-id="a12b4-126">If (Активатеакткткс (Хакткткс, &Улпкукие))</span><span class="sxs-lookup"><span data-stu-id="a12b4-126">if(ActivateActCtx(hActCtx, &ulpCookie))</span></span>  
    <span data-ttu-id="a12b4-127">{</span><span class="sxs-lookup"><span data-stu-id="a12b4-127">{</span></span>  
    <span data-ttu-id="a12b4-128">...</span><span class="sxs-lookup"><span data-stu-id="a12b4-128">...</span></span>  
    <span data-ttu-id="a12b4-129">Каллвиндовпрок (...);</span><span class="sxs-lookup"><span data-stu-id="a12b4-129">CallWindowProc(...);</span></span>  
    <span data-ttu-id="a12b4-130">...</span><span class="sxs-lookup"><span data-stu-id="a12b4-130">...</span></span>  
    <span data-ttu-id="a12b4-131">Деактиватеакткткс (0, Улпкукие);</span><span class="sxs-lookup"><span data-stu-id="a12b4-131">DeactivateActCtx(0, ulpCookie);</span></span>  
    <span data-ttu-id="a12b4-132">}</span><span class="sxs-lookup"><span data-stu-id="a12b4-132">}</span></span>  
    </dl>

-   <span data-ttu-id="a12b4-133">Уровень диспетчеризации делегирования.</span><span class="sxs-lookup"><span data-stu-id="a12b4-133">Delegator dispatch layer.</span></span>

    <span data-ttu-id="a12b4-134">Этот сценарий применяется к руководителям, управляющим несколькими сущностями с общим уровнем API, например диспетчером драйверов.</span><span class="sxs-lookup"><span data-stu-id="a12b4-134">This scenario applies to managers that manage multiple entities with a common API layer, such as a driver manager.</span></span> <span data-ttu-id="a12b4-135">Хотя это и еще не реализовано, в качестве примера можно привести драйвер ODBC.</span><span class="sxs-lookup"><span data-stu-id="a12b4-135">Although it has not yet been implemented, an example of this would be the ODBC driver.</span></span>

    <span data-ttu-id="a12b4-136">В этом сценарии средний уровень может обрабатывать привязки сборок.</span><span class="sxs-lookup"><span data-stu-id="a12b4-136">In this scenario, the middle layer becomes capable of processing assembly bindings.</span></span> <span data-ttu-id="a12b4-137">Чтобы получить драйвер привязки для конкретной версии, издатели должны предоставить манифест и указать зависимости от конкретных компонентов в этом манифесте.</span><span class="sxs-lookup"><span data-stu-id="a12b4-137">To get the version-specific binding driver, publishers must provide a manifest and specify dependencies on specific components in that manifest.</span></span> <span data-ttu-id="a12b4-138">Базовое приложение не выполняет динамическую привязку к компонентам; во время выполнения диспетчер драйверов управляет вызовами.</span><span class="sxs-lookup"><span data-stu-id="a12b4-138">The base application does not dynamically bind to the components; at run time, the driver manager manages the calls.</span></span> <span data-ttu-id="a12b4-139">При вызове драйвера ODBC на основе строки подключения он загружает соответствующий драйвер.</span><span class="sxs-lookup"><span data-stu-id="a12b4-139">When the ODBC driver is called based on the connect string it loads the appropriate driver.</span></span> <span data-ttu-id="a12b4-140">Затем он создает контекст активации, используя сведения в файле манифеста сборки.</span><span class="sxs-lookup"><span data-stu-id="a12b4-140">It then creates the activation context using the information in the assembly manifest file.</span></span>

    <span data-ttu-id="a12b4-141">Без манифеста действием по умолчанию для драйвера является использование того же контекста, который указан в приложении — в данном примере это версия 2 библиотеки MSVCRT.</span><span class="sxs-lookup"><span data-stu-id="a12b4-141">Without the manifest, the default action for the driver is to use the same context as that specified by the application—in this example, version 2 of MSVCRT.</span></span> <span data-ttu-id="a12b4-142">Поскольку манифест существует, устанавливается отдельный контекст активации.</span><span class="sxs-lookup"><span data-stu-id="a12b4-142">Since a manifest does exist, a separate activation context is established.</span></span> <span data-ttu-id="a12b4-143">При запуске драйвера ODBC он привязывается к версии 1 сборки MSVCRT.</span><span class="sxs-lookup"><span data-stu-id="a12b4-143">When the ODBC driver runs, it binds to version 1 of the MSVCRT assembly.</span></span>

    <span data-ttu-id="a12b4-144">Каждый раз, когда диспетчер драйверов вызывает слой диспетчеризации, например для получения следующего набора данных, он использует соответствующие сборки на основе контекста активации.</span><span class="sxs-lookup"><span data-stu-id="a12b4-144">Each time the driver manager calls the dispatch layer—for example, to get the next set of data—it uses the appropriate assemblies based on the activation context.</span></span> <span data-ttu-id="a12b4-145">Это показано в следующем фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="a12b4-145">The following code fragment illustrates this.</span></span>

    <dl> <span data-ttu-id="a12b4-146">Обработайте Хакткткс;</span><span class="sxs-lookup"><span data-stu-id="a12b4-146">HANDLE hActCtx;</span></span>  
    <span data-ttu-id="a12b4-147">ULONG \_ ptr улпкукие;</span><span class="sxs-lookup"><span data-stu-id="a12b4-147">ULONG\_PTR ulpCookie;</span></span>  
    <span data-ttu-id="a12b4-148">АКТКТКС Акткткстокреате = {...};</span><span class="sxs-lookup"><span data-stu-id="a12b4-148">ACTCTX ActCtxToCreate = {...};</span></span>  
    <span data-ttu-id="a12b4-149">Хакткткс = Креатеакткткс (&Акткткстокреате);</span><span class="sxs-lookup"><span data-stu-id="a12b4-149">hActCtx = CreateActCtx(&ActCtxToCreate);</span></span>  
    <span data-ttu-id="a12b4-150">...;</span><span class="sxs-lookup"><span data-stu-id="a12b4-150">...;</span></span>  
    <span data-ttu-id="a12b4-151">If (Активатеакткткс (Хакткткс, &Улпкукие))</span><span class="sxs-lookup"><span data-stu-id="a12b4-151">if (ActivateActCtx(hActCtx, &ulpCookie))</span></span>  
    <span data-ttu-id="a12b4-152">{</span><span class="sxs-lookup"><span data-stu-id="a12b4-152">{</span></span>  
    <span data-ttu-id="a12b4-153">...</span><span class="sxs-lookup"><span data-stu-id="a12b4-153">...</span></span>  
    <span data-ttu-id="a12b4-154">Коннектдб (...);</span><span class="sxs-lookup"><span data-stu-id="a12b4-154">ConnectDb(...);</span></span>  
    <span data-ttu-id="a12b4-155">Деактиватеакткткс (0, Улпкукие);</span><span class="sxs-lookup"><span data-stu-id="a12b4-155">DeactivateActCtx(0, ulpCookie);</span></span>  
    <span data-ttu-id="a12b4-156">}</span><span class="sxs-lookup"><span data-stu-id="a12b4-156">}</span></span>  
    <span data-ttu-id="a12b4-157">...</span><span class="sxs-lookup"><span data-stu-id="a12b4-157">...</span></span>  
    <span data-ttu-id="a12b4-158">Релеасеакткткс (Хакткткс);</span><span class="sxs-lookup"><span data-stu-id="a12b4-158">ReleaseActCtx(hActCtx);</span></span>  
    </dl>

 

 
