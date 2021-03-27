---
description: Windows GDI+ — это API на основе классов для программистов C/C++.
ms.assetid: ed1396b2-2fc5-4a77-bea2-7bcc971214ae
title: GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac0dac72d27ba52071797b51573141506d5b0ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144878"
---
# <a name="gdi"></a><span data-ttu-id="878c4-103">GDI+</span><span class="sxs-lookup"><span data-stu-id="878c4-103">GDI+</span></span>

## <a name="purpose"></a><span data-ttu-id="878c4-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="878c4-104">Purpose</span></span>

<span data-ttu-id="878c4-105">Windows GDI+ — это API на основе классов для программистов C/C++.</span><span class="sxs-lookup"><span data-stu-id="878c4-105">Windows GDI+ is a class-based API for C/C++ programmers.</span></span> <span data-ttu-id="878c4-106">Она позволяет приложениям использовать графику и форматированный текст как на дисплее, так и на принтере.</span><span class="sxs-lookup"><span data-stu-id="878c4-106">It enables applications to use graphics and formatted text on both the video display and the printer.</span></span> <span data-ttu-id="878c4-107">Приложения на основе API-интерфейса Microsoft Win32 не обращаются к графическому оборудованию напрямую.</span><span class="sxs-lookup"><span data-stu-id="878c4-107">Applications based on the Microsoft Win32 API do not access graphics hardware directly.</span></span> <span data-ttu-id="878c4-108">Вместо этого GDI+ взаимодействует с драйверами устройств от имени приложений.</span><span class="sxs-lookup"><span data-stu-id="878c4-108">Instead, GDI+ interacts with device drivers on behalf of applications.</span></span> <span data-ttu-id="878c4-109">GDI+ также поддерживается Microsoft Win64.</span><span class="sxs-lookup"><span data-stu-id="878c4-109">GDI+ is also supported by Microsoft Win64.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="878c4-110">Где применимо</span><span class="sxs-lookup"><span data-stu-id="878c4-110">Where applicable</span></span>

<span data-ttu-id="878c4-111">Функции и классы GDI+ не поддерживаются для использования в службе Windows.</span><span class="sxs-lookup"><span data-stu-id="878c4-111">GDI+ functions and classes are not supported for use within a Windows service.</span></span> <span data-ttu-id="878c4-112">Попытка использовать эти функции и классы из службы Windows может привести к непредвиденным проблемам, например к снижению производительности службы и исключениям или ошибкам времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="878c4-112">Attempting to use these functions and classes from a Windows service may produce unexpected problems, such as diminished service performance and run-time exceptions or errors.</span></span>

> [!Note]  
> <span data-ttu-id="878c4-113">При использовании интерфейса GDI+ API не следует разрешать приложению скачивать произвольные шрифты из ненадежных источников.</span><span class="sxs-lookup"><span data-stu-id="878c4-113">When you use the GDI+ API, you must never allow your application to download arbitrary fonts from untrusted sources.</span></span> <span data-ttu-id="878c4-114">Операционная система требует повышенных привилегий, чтобы гарантировать, что все установленные шрифты являются доверенными.</span><span class="sxs-lookup"><span data-stu-id="878c4-114">The operating system requires elevated privileges to assure that all installed fonts are trusted.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="878c4-115">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="878c4-115">Developer audience</span></span>

<span data-ttu-id="878c4-116">Интерфейс на основе классов GDI+ C++ предназначен для использования программистами C/C++.</span><span class="sxs-lookup"><span data-stu-id="878c4-116">The GDI+ C++ class-based interface is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="878c4-117">Знание графического пользовательского интерфейса Windows и архитектуры, управляемой сообщениями, является обязательным.</span><span class="sxs-lookup"><span data-stu-id="878c4-117">Familiarity with the Windows graphical user interface and message-driven architecture is required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="878c4-118">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="878c4-118">Run-time requirements</span></span>

<span data-ttu-id="878c4-119">GDI+ можно использовать во всех приложениях на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="878c4-119">GDI+ can be used in all Windows-based applications.</span></span> <span data-ttu-id="878c4-120">Интерфейс GDI+ появился в Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="878c4-120">GDI+ was introduced in Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="878c4-121">Сведения о том, какие операционные системы требуются для использования определенного класса или метода, см. в разделе "Дополнительные сведения" документации по классу или методу.</span><span class="sxs-lookup"><span data-stu-id="878c4-121">For information about which operating systems are required to use a particular class or method, see the More Information section of the documentation for the class or method.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="878c4-122">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="878c4-122">In this section</span></span>

| <span data-ttu-id="878c4-123">Раздел</span><span class="sxs-lookup"><span data-stu-id="878c4-123">Topic</span></span>                                                    | <span data-ttu-id="878c4-124">Описание</span><span class="sxs-lookup"><span data-stu-id="878c4-124">Description</span></span>                                           |
|----------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="878c4-125">Обзор</span><span class="sxs-lookup"><span data-stu-id="878c4-125">Overview</span></span>](-gdiplus-about-gdi--about.md)<br/>     | <span data-ttu-id="878c4-126">Общие сведения о GDI+.</span><span class="sxs-lookup"><span data-stu-id="878c4-126">General information about GDI+.</span></span><br/>            |
| [<span data-ttu-id="878c4-127">Использующ</span><span class="sxs-lookup"><span data-stu-id="878c4-127">Using</span></span>](-gdiplus-using-gdi--use.md)<br/>          | <span data-ttu-id="878c4-128">Задачи и примеры с использованием GDI+.</span><span class="sxs-lookup"><span data-stu-id="878c4-128">Tasks and examples using GDI+.</span></span><br/>             |
| [<span data-ttu-id="878c4-129">Ссылки</span><span class="sxs-lookup"><span data-stu-id="878c4-129">Reference</span></span>](-gdiplus-class-gdi-reference.md)<br/> | <span data-ttu-id="878c4-130">Документация по API-интерфейсу на основе классов GDI+ C++.</span><span class="sxs-lookup"><span data-stu-id="878c4-130">Documentation of GDI+ C++ class-based API.</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="878c4-131">См. также</span><span class="sxs-lookup"><span data-stu-id="878c4-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="878c4-132">Windows GDI</span><span class="sxs-lookup"><span data-stu-id="878c4-132">Windows GDI</span></span>](../gdi/windows-gdi.md)
</dt> <dt>

<span data-ttu-id="878c4-133">[DirectX](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="878c4-133">[DirectX](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="878c4-134">Получение образа Windows</span><span class="sxs-lookup"><span data-stu-id="878c4-134">Windows Image Acquisition</span></span>](../wia/-wia-startpage.md)
</dt> <dt>

[<span data-ttu-id="878c4-135">OpenGL</span><span class="sxs-lookup"><span data-stu-id="878c4-135">OpenGL</span></span>](../opengl/opengl.md)
</dt> <dt>

[<span data-ttu-id="878c4-136">Мультимедиа Windows</span><span class="sxs-lookup"><span data-stu-id="878c4-136">Windows Multimedia</span></span>](../multimedia/windows-multimedia-start-page.md)
</dt> </dl>
