---
title: Цветовая система Windows
description: Схемы управления цветом реализованы в операционных системах Microsoft Windows, чтобы улучшить отрисовку цветового содержимого во всех формах цифрового взаимодействия. Схема управления цветом, которая используется начиная с Windows 2000, Windows XP и Windows Server 2003, называется управление цветом изображений (ICM) 2,0. Схема управления цветом, используемая начиная с Windows Vista, называется цветовой системой Windows (WCS) 1,0. Схема управления цветом WCS 1,0 представляет собой надмножество интерфейсов API и функций ICM 2,0.
ms.assetid: 9e8b7c38-3c4f-4537-a7e1-6ad0daa39497
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 558ccb84caa4ff10ab4c97115b9759730cd0ef26
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105720067"
---
# <a name="windows-color-system"></a><span data-ttu-id="3773b-105">Цветовая система Windows</span><span class="sxs-lookup"><span data-stu-id="3773b-105">Windows Color System</span></span>

## <a name="purpose"></a><span data-ttu-id="3773b-106">Назначение</span><span class="sxs-lookup"><span data-stu-id="3773b-106">Purpose</span></span>

<span data-ttu-id="3773b-107">Схемы управления цветом реализованы в операционных системах Microsoft Windows, чтобы улучшить отрисовку цветового содержимого во всех формах цифрового взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="3773b-107">Color management schemes are implemented in Microsoft Windows operating systems to improve the rendering of color content in all forms of digital communication.</span></span>

<span data-ttu-id="3773b-108">Схема управления цветом, которая используется начиная с Windows 2000, Windows XP и Windows Server 2003, называется управление цветом изображений (ICM) 2,0.</span><span class="sxs-lookup"><span data-stu-id="3773b-108">The color management scheme that's used starting with Windows 2000, Windows XP, and Windows Server 2003 is called Image Color Management (ICM) 2.0.</span></span> <span data-ttu-id="3773b-109">Схема управления цветом, используемая начиная с Windows Vista, называется цветовой системой Windows (WCS) 1,0.</span><span class="sxs-lookup"><span data-stu-id="3773b-109">The color management scheme that's used starting with Windows Vista is called Windows Color System (WCS) 1.0.</span></span> <span data-ttu-id="3773b-110">Схема управления цветом WCS 1,0 представляет собой надмножество интерфейсов API и функций ICM 2,0.</span><span class="sxs-lookup"><span data-stu-id="3773b-110">The WCS 1.0 color management scheme is a superset of ICM 2.0 APIs and functionality.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="3773b-111">Где применимо</span><span class="sxs-lookup"><span data-stu-id="3773b-111">Where applicable</span></span>

<span data-ttu-id="3773b-112">ICM можно использовать во всех приложениях в операционных системах Windows 2000 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="3773b-112">ICM can be used in all applications on Windows 2000 and later operating systems.</span></span> <span data-ttu-id="3773b-113">WCS можно использовать во всех приложениях Windows Vista и более поздних операционных систем.</span><span class="sxs-lookup"><span data-stu-id="3773b-113">WCS can be used in all applications on Windows Vista and later operating systems.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="3773b-114">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="3773b-114">Developer audience</span></span>

<span data-ttu-id="3773b-115">API-интерфейс WCS предназначен для использования программистами C/C++.</span><span class="sxs-lookup"><span data-stu-id="3773b-115">The WCS API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="3773b-116">Вы знакомы с графическим пользовательским интерфейсом Windows, управляемой на основе сообщений архитектурой, и вам нужны основные понятия управления цветом.</span><span class="sxs-lookup"><span data-stu-id="3773b-116">Familiarity with the Windows graphical user interface, message-driven architecture, and a working knowledge of color management concepts are required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="3773b-117">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="3773b-117">Run-time requirements</span></span>

<span data-ttu-id="3773b-118">Для приложений, использующих ICM API, требуется Windows 2000 или более поздняя версия.</span><span class="sxs-lookup"><span data-stu-id="3773b-118">Applications that use the ICM API require Windows 2000 or later.</span></span> <span data-ttu-id="3773b-119">Для приложений, использующих API-интерфейс WCS, требуется Windows Vista или более поздняя версия.</span><span class="sxs-lookup"><span data-stu-id="3773b-119">Applications that use the WCS API require Windows Vista or later.</span></span> <span data-ttu-id="3773b-120">Сведения о конкретных данных времени выполнения для функции см. в разделе "требования" на странице справки по этой функции.</span><span class="sxs-lookup"><span data-stu-id="3773b-120">For specific run-time information on a function, see the Requirements section of the reference page for that function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3773b-121">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="3773b-121">In this section</span></span>

-   [<span data-ttu-id="3773b-122">Вопросы безопасности: цветовая система Windows</span><span class="sxs-lookup"><span data-stu-id="3773b-122">Security Considerations: Windows Color System</span></span>](security-considerations--windows-color-system.md)
-   [<span data-ttu-id="3773b-123">Основные понятия управления цветом</span><span class="sxs-lookup"><span data-stu-id="3773b-123">Basic color management concepts</span></span>](basic-color-management-concepts.md)
-   [<span data-ttu-id="3773b-124">Схемы и алгоритмы цветовой системы Windows</span><span class="sxs-lookup"><span data-stu-id="3773b-124">Windows Color System Schemas and Algorithms</span></span>](windows-color-system-schemas-and-algorithms.md)
-   [<span data-ttu-id="3773b-125">Сведения о цветовой системе Windows версии 1.0</span><span class="sxs-lookup"><span data-stu-id="3773b-125">About Windows Color System Version 1.0</span></span>](about-windows-color-system-version-1-0.md)
-   [<span data-ttu-id="3773b-126">Использование WCS 1.0</span><span class="sxs-lookup"><span data-stu-id="3773b-126">Using WCS 1.0</span></span>](using-wcs-1-0.md)
-   [<span data-ttu-id="3773b-127">Ссылки</span><span class="sxs-lookup"><span data-stu-id="3773b-127">Reference</span></span>](reference.md)
-   [<span data-ttu-id="3773b-128">Глоссарий WCS 1.0</span><span class="sxs-lookup"><span data-stu-id="3773b-128">WCS 1.0 Glossary</span></span>](wcs-1-0-glossary.md)

## <a name="related-topics"></a><span data-ttu-id="3773b-129">См. также</span><span class="sxs-lookup"><span data-stu-id="3773b-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3773b-130">OpenGL</span><span class="sxs-lookup"><span data-stu-id="3773b-130">OpenGL</span></span>](../opengl/introduction-to-opengl.md)
</dt> <dt>

[<span data-ttu-id="3773b-131">Мультимедиа Windows</span><span class="sxs-lookup"><span data-stu-id="3773b-131">Windows Multimedia</span></span>](../multimedia/windows-multimedia-start-page.md)
</dt> <dt>

[<span data-ttu-id="3773b-132">Windows GDI</span><span class="sxs-lookup"><span data-stu-id="3773b-132">Windows GDI</span></span>](../gdi/windows-gdi.md)
</dt> </dl>

 

 