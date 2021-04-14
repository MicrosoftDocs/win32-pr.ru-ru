---
title: OpenGL
description: В качестве программного интерфейса для графического оборудования OpenGL преобразует многомерные объекты в буфера кадров.
ms.assetid: ddd7c8d0-f1d1-4d16-bd0c-99cee3d733c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02bec69473f937d4dfff9c496d291e8070ffadef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488185"
---
# <a name="opengl"></a><span data-ttu-id="651cd-103">OpenGL</span><span class="sxs-lookup"><span data-stu-id="651cd-103">OpenGL</span></span>

## <a name="purpose"></a><span data-ttu-id="651cd-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="651cd-104">Purpose</span></span>

<span data-ttu-id="651cd-105">В качестве программного интерфейса для графического оборудования OpenGL преобразует многомерные объекты в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="651cd-105">As a software interface for graphics hardware, OpenGL renders multidimensional objects into a framebuffer.</span></span> <span data-ttu-id="651cd-106">Реализация OpenGL в корпорации Майкрософт для операционной системы Windows — это стандартное графическое программное обеспечение, с помощью которого программисты могут создавать высококачественные и анимированные трехмерные изображения.</span><span class="sxs-lookup"><span data-stu-id="651cd-106">The Microsoft implementation of OpenGL for the Windows operating system is industry-standard graphics software with which programmers can create high-quality still and animated three-dimensional color images.</span></span> <span data-ttu-id="651cd-107">Версия OpenGL, описанная в этом разделе, — 1,1.</span><span class="sxs-lookup"><span data-stu-id="651cd-107">The version of OpenGL described in this section is 1.1.</span></span>

<span data-ttu-id="651cd-108">Сведения о стандарте OpenGL ES, работающем в Windows, см. в разделе " [угол для Магазина Windows](https://github.com/microsoft/angle/wiki)".</span><span class="sxs-lookup"><span data-stu-id="651cd-108">For information about OpenGL ES running on Windows, see [ANGLE for Windows Store](https://github.com/microsoft/angle/wiki).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="651cd-109">Где применимо</span><span class="sxs-lookup"><span data-stu-id="651cd-109">Where applicable</span></span>

<span data-ttu-id="651cd-110">OpenGL разработан для обеспечения совместимости оборудования и операционных систем.</span><span class="sxs-lookup"><span data-stu-id="651cd-110">OpenGL is built for compatibility across hardware and operating systems.</span></span> <span data-ttu-id="651cd-111">Эта архитектура упрощает перенос программ OpenGL с одной системы на другую.</span><span class="sxs-lookup"><span data-stu-id="651cd-111">This architecture makes it easy to port OpenGL programs from one system to another.</span></span> <span data-ttu-id="651cd-112">Хотя каждая операционная система имеет уникальные требования, код OpenGL во многих программах можно использовать как есть.</span><span class="sxs-lookup"><span data-stu-id="651cd-112">While each operating system has unique requirements, the OpenGL code in many programs can be used as is.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="651cd-113">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="651cd-113">Developer audience</span></span>

<span data-ttu-id="651cd-114">Стандарт OpenGL, предназначенный для программистов C/C++, требует знакомства с графическим пользовательским интерфейсом Windows, а также с архитектурой, управляемой сообщениями.</span><span class="sxs-lookup"><span data-stu-id="651cd-114">Designed for use by C/C++ programmers, OpenGL requires familiarity with the Windows graphical user interface as well as message-driven architecture.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="651cd-115">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="651cd-115">Run-time requirements</span></span>

<span data-ttu-id="651cd-116">Дополнительные сведения о том, какие операционные системы требуются для конкретной функции, см. в разделе «требования» документации по функции.</span><span class="sxs-lookup"><span data-stu-id="651cd-116">For more information on which operating systems are required for a particular function, see the Requirements section of the documentation for the function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="651cd-117">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="651cd-117">In this section</span></span>



| <span data-ttu-id="651cd-118">Раздел</span><span class="sxs-lookup"><span data-stu-id="651cd-118">Topic</span></span>                                             | <span data-ttu-id="651cd-119">Описание</span><span class="sxs-lookup"><span data-stu-id="651cd-119">Description</span></span>                                                                        |
|---------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="651cd-120">Обзор</span><span class="sxs-lookup"><span data-stu-id="651cd-120">Overview</span></span>](basic-opengl-operation.md)<br/> | <span data-ttu-id="651cd-121">Общие сведения о работе OpenGL.</span><span class="sxs-lookup"><span data-stu-id="651cd-121">General information about how OpenGL works.</span></span><br/>                             |
| [<span data-ttu-id="651cd-122">Ссылки</span><span class="sxs-lookup"><span data-stu-id="651cd-122">Reference</span></span>](opengl-reference.md)<br/>      | <span data-ttu-id="651cd-123">Документация по функциям, структурам и другим программным элементам.</span><span class="sxs-lookup"><span data-stu-id="651cd-123">Documentation of functions, structures, and other programming elements.</span></span><br/> |
| [<span data-ttu-id="651cd-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="651cd-124">Samples</span></span>](a-porting-sample.md)<br/>        | <span data-ttu-id="651cd-125">Примеры кода OpenGL.</span><span class="sxs-lookup"><span data-stu-id="651cd-125">Examples of OpenGL code.</span></span><br/>                                                |



 

## <a name="related-topics"></a><span data-ttu-id="651cd-126">См. также</span><span class="sxs-lookup"><span data-stu-id="651cd-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="651cd-127">Графика и игры DirectX</span><span class="sxs-lookup"><span data-stu-id="651cd-127">DirectX Graphics and Gaming</span></span>](/windows/desktop/directx)
</dt> <dt>

<span data-ttu-id="651cd-128">[Изображение по-прежнему](/previous-versions/windows/desktop/legacy/cc836557(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="651cd-128">[Still Image](/previous-versions/windows/desktop/legacy/cc836557(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="651cd-129">[Цветовая система Windows (WCS)](/previous-versions//dd372446(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="651cd-129">[Windows Color System (WCS)](/previous-versions//dd372446(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="651cd-130">Windows GDI</span><span class="sxs-lookup"><span data-stu-id="651cd-130">Windows GDI</span></span>](/windows/desktop/gdi/windows-gdi)
</dt> <dt>

[<span data-ttu-id="651cd-131">Получение образа Windows</span><span class="sxs-lookup"><span data-stu-id="651cd-131">Windows Image Acquisition</span></span>](../wia/-wia-startpage.md)
</dt> <dt>

[<span data-ttu-id="651cd-132">Мультимедиа Windows</span><span class="sxs-lookup"><span data-stu-id="651cd-132">Windows Multimedia</span></span>](/windows/desktop/Multimedia/windows-multimedia-start-page)
</dt> <dt>

<span data-ttu-id="651cd-133">[API Windows](/previous-versions//cc433218(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="651cd-133">[Windows API](/previous-versions//cc433218(v=vs.85))</span></span>
</dt> </dl>

 

