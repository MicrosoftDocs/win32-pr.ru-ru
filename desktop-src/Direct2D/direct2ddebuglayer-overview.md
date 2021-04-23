---
title: Общие сведения о слое отладки Direct2D
description: .
ms.assetid: 7c28e00b-ebb9-4b79-939c-64eade1351ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df560595ea0ae6c7a56c3fa568f2f94ae56652ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654211"
---
# <a name="direct2d-debug-layer-overview"></a><span data-ttu-id="56dc3-103">Общие сведения о слое отладки Direct2D</span><span class="sxs-lookup"><span data-stu-id="56dc3-103">Direct2D Debug Layer Overview</span></span>

<span data-ttu-id="56dc3-104">Уровень отладки Direct2D предоставляет отладочные сообщения времени разработки для снижения сбоев приложения среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="56dc3-104">The Direct2D debug layer provides design-time debug messages for you to minimize runtime application failure.</span></span> <span data-ttu-id="56dc3-105">В этом обзоре описываются основы слоя отладки Direct2D.</span><span class="sxs-lookup"><span data-stu-id="56dc3-105">This overview describes the basics of the Direct2D debug layer.</span></span> <span data-ttu-id="56dc3-106">Предполагается, что вы знакомы с созданием базовых приложений Direct2D.</span><span class="sxs-lookup"><span data-stu-id="56dc3-106">It assumes that you are familiar with creating basic Direct2D applications.</span></span>

<span data-ttu-id="56dc3-107">Этот обзор содержит следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="56dc3-107">This overview contains the following sections.</span></span>

-   [<span data-ttu-id="56dc3-108">Что такое уровень отладки Direct2D</span><span class="sxs-lookup"><span data-stu-id="56dc3-108">What Is the Direct2D Debug Layer</span></span>](#what-is-the-direct2d-debug-layer)
-   [<span data-ttu-id="56dc3-109">Установка слоя отладки Direct2D</span><span class="sxs-lookup"><span data-stu-id="56dc3-109">Installing the Direct2D Debug Layer</span></span>](#installing-the-direct2d-debug-layer)
-   [<span data-ttu-id="56dc3-110">Включение слоя отладки</span><span class="sxs-lookup"><span data-stu-id="56dc3-110">Enabling the Debug Layer</span></span>](#enabling-the-debug-layer)
-   [<span data-ttu-id="56dc3-111">Уровни отладки</span><span class="sxs-lookup"><span data-stu-id="56dc3-111">Debug Levels</span></span>](#debug-levels)
-   [<span data-ttu-id="56dc3-112">См. также</span><span class="sxs-lookup"><span data-stu-id="56dc3-112">Related topics</span></span>](#related-topics)

## <a name="what-is-the-direct2d-debug-layer"></a><span data-ttu-id="56dc3-113">Что такое уровень отладки Direct2D</span><span class="sxs-lookup"><span data-stu-id="56dc3-113">What Is the Direct2D Debug Layer</span></span>

<span data-ttu-id="56dc3-114">Слой отладки Direct2D, реализованный отдельно от Direct2D в собственной библиотеке DLL с именем d2d1debug.dll, предоставляет отладочные сообщения, позволяющие точно использовать функции Direct2D.</span><span class="sxs-lookup"><span data-stu-id="56dc3-114">The Direct2D debug layer, implemented separately from Direct2D in its own DLL named d2d1debug.dll, provides debug messages to enable you to accurately use Direct2D functions.</span></span> <span data-ttu-id="56dc3-115">Сообщения об отладке часто возникают из-за нарушений контракта API, например недопустимых параметров (может быть связано с Direct3D), недопустимых ресурсов, нарушений потоков и проблем с производительностью, таких как использование слоя при достаточном фрагменте.</span><span class="sxs-lookup"><span data-stu-id="56dc3-115">The debug messages often result from API contract violations such as invalid parameters (could be Direct3D-related), invalid resources, threading violations, and performance issues such as using a layer when a clip would suffice.</span></span> <span data-ttu-id="56dc3-116">Чтобы указать объем данных, отслеживаемый слоем отладки, можно указать один из трех уровней отладки: сведения, предупреждение и ошибка. и сообщение об ошибке уровня активирует точку останова, которая поможет вам выполнить отладку.</span><span class="sxs-lookup"><span data-stu-id="56dc3-116">To specify how much information is traced by the debug layer, you can specify one of the three debug levels: information, warning, and error; and a message of level error triggers the breakpoint to help you debug.</span></span>

## <a name="installing-the-direct2d-debug-layer"></a><span data-ttu-id="56dc3-117">Установка слоя отладки Direct2D</span><span class="sxs-lookup"><span data-stu-id="56dc3-117">Installing the Direct2D Debug Layer</span></span>

<span data-ttu-id="56dc3-118">Инструкции по установке отладочного слоя см. в разделе [Установка отладочного слоя Direct2D](installing-the-direct2d-debug-layer.md).</span><span class="sxs-lookup"><span data-stu-id="56dc3-118">For instructions on installing the debug layer, see [Installing the Direct2D Debug Layer](installing-the-direct2d-debug-layer.md).</span></span>

## <a name="enabling-the-debug-layer"></a><span data-ttu-id="56dc3-119">Включение слоя отладки</span><span class="sxs-lookup"><span data-stu-id="56dc3-119">Enabling the Debug Layer</span></span>

<span data-ttu-id="56dc3-120">Чтобы включить слой отладки в приложении, укажите значение [**\_ \_ уровня отладки D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) , отличное от **D2D1 \_ \_ уровень отладки \_ None** , при создании фабрики с помощью функции [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) .</span><span class="sxs-lookup"><span data-stu-id="56dc3-120">To enable the debug layer in your application, specify a [**D2D1\_DEBUG\_LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) value other than **D2D1\_DEBUG\_LEVEL\_NONE** when you create a factory with the [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) function.</span></span>

> [!Note]  
> <span data-ttu-id="56dc3-121">Если включен слой отладки Direct2D, то \_ при задании контекста цвета может возникнуть нарушение прав доступа для управления цветом Direct2D (CLSID D2D1ColorManagement).</span><span class="sxs-lookup"><span data-stu-id="56dc3-121">If the Direct2D debug layer is enabled, the Direct2D color management effect (CLSID\_D2D1ColorManagement) may cause an access violation when setting a color context.</span></span> <span data-ttu-id="56dc3-122">Обходной путь заключается в отключении отладочного слоя при использовании эффекта управления цветом.</span><span class="sxs-lookup"><span data-stu-id="56dc3-122">The workaround is to disable the debug layer when using the color management effect</span></span>

 

<span data-ttu-id="56dc3-123">Включение слоя отладки для фабрики также включает отладочную информацию для любого объекта, созданного этой фабрикой.</span><span class="sxs-lookup"><span data-stu-id="56dc3-123">Enabling the debug layer for a factory also enables debugging information for any object created by that factory.</span></span>

<span data-ttu-id="56dc3-124">В следующем примере включается уровень отладки для фабрики при компиляции приложения для конфигурации ОТЛАДОЧной сборки.</span><span class="sxs-lookup"><span data-stu-id="56dc3-124">The following example enables the debug layer for a factory when the application is compiled for the DEBUG build configuration.</span></span>


```C++
        // If you set the options.debugLevel to D2D1_DEBUG_LEVEL_NONE,
        // the debug layer is not enabled.
#if defined(DEBUG) || defined(_DEBUG)
        D2D1_FACTORY_OPTIONS options;
        options.debugLevel = D2D1_DEBUG_LEVEL_INFORMATION;

        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            options,
            &m_pD2DFactory
            );
#else
        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            &m_pD2DFactory
            );
#endif
```



> [!Note]  
> <span data-ttu-id="56dc3-125">Если параметры фабрики не заданы или указан уровень отладки "нет", отладочный слой не вызывается.</span><span class="sxs-lookup"><span data-stu-id="56dc3-125">If no factory options are specified or a debug level of "none" is specified, the debug layer is not invoked.</span></span> <span data-ttu-id="56dc3-126">Отладочный слой никогда не должен быть активным в окончательной версии приложения.</span><span class="sxs-lookup"><span data-stu-id="56dc3-126">The debug layer should never be active in the release version of an application.</span></span>

 

<span data-ttu-id="56dc3-127">В следующем разделе описаны различные уровни отладки, определяемые перечислением [**\_ \_ уровня отладки D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) .</span><span class="sxs-lookup"><span data-stu-id="56dc3-127">The next section describes the different debug levels defined by the [**D2D1\_DEBUG\_LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) enumeration.</span></span>

## <a name="debug-levels"></a><span data-ttu-id="56dc3-128">Уровни отладки</span><span class="sxs-lookup"><span data-stu-id="56dc3-128">Debug Levels</span></span>

<span data-ttu-id="56dc3-129">В перечислении [**\_ \_ уровня отладки D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) заданы три уровня отладки: \_ Ошибка на \_ уровне отладки \_ (ошибка), D2D1 \_ \_ \_ warning (предупреждение) и D2D1 \_ \_ \_ (сведения) на уровне отладки.</span><span class="sxs-lookup"><span data-stu-id="56dc3-129">The [**D2D1\_DEBUG\_LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) enumeration specifies three debug levels: D2D1\_DEBUG\_LEVEL\_ERROR (error), D2D1\_DEBUG\_LEVEL\_WARNING (warning), and D2D1\_DEBUG\_LEVEL\_INFORMATION (information).</span></span> <span data-ttu-id="56dc3-130">Эти уровни интерпретируется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="56dc3-130">These levels are interpreted as follows:</span></span>

-   <span data-ttu-id="56dc3-131">**Ошибка:** Direct2D отправляет серьезные сообщения об ошибках на слой отладки.</span><span class="sxs-lookup"><span data-stu-id="56dc3-131">**Error:** Direct2D sends severe error messages to the debug layer.</span></span> <span data-ttu-id="56dc3-132">Например, при критическом ограничении потоков будет создаваться серьезная ошибка.</span><span class="sxs-lookup"><span data-stu-id="56dc3-132">For example, breaking a threading constraint will generate a severe error.</span></span>

-   <span data-ttu-id="56dc3-133">**Предупреждение:** Direct2D отправляет сообщения об ошибках и предупреждения на слой отладки, чтобы можно было обращаться к любому из этих сообщений.</span><span class="sxs-lookup"><span data-stu-id="56dc3-133">**Warning:** Direct2D sends error messages and warnings to the debug layer so that you can address any of these messages.</span></span>

-   <span data-ttu-id="56dc3-134">**Сведения:** Direct2D отправляет сообщения об ошибках, предупреждения и дополнительные диагностические сведения на слой отладки.</span><span class="sxs-lookup"><span data-stu-id="56dc3-134">**Information:** Direct2D sends error messages, warnings, and additional diagnostic information to the debug layer.</span></span> <span data-ttu-id="56dc3-135">Например, сообщения улучшения производительности будут отправляться на этом уровне отладки.</span><span class="sxs-lookup"><span data-stu-id="56dc3-135">For example, performance improvement messages will be sent at this debug level.</span></span>

<span data-ttu-id="56dc3-136">Значение D2D1 \_ уровень отладки \_ \_ None (нет) указывает, что Direct2D не предоставляет никаких выходных данных отладки.</span><span class="sxs-lookup"><span data-stu-id="56dc3-136">The value D2D1\_DEBUG\_LEVEL\_NONE (none) indicates that Direct2D does not provide any debugging output.</span></span>

## <a name="related-topics"></a><span data-ttu-id="56dc3-137">См. также</span><span class="sxs-lookup"><span data-stu-id="56dc3-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56dc3-138">Сообщения отладки</span><span class="sxs-lookup"><span data-stu-id="56dc3-138">Debug Messages</span></span>](direct2ddebuglayer-debugmessages.md)
</dt> </dl>

 

 




