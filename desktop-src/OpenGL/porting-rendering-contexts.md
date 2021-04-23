---
title: Перенос контекстов рендеринга
description: Перенос контекстов рендеринга
ms.assetid: 8655a81b-9f13-4ee5-ba0d-9aa9da1bfd09
keywords:
- Контексты отрисовки OpenGL, перенос
- OpenGL в Windows, контексты отрисовки
- Перенос на OpenGL, контексты отрисовки
- Перенос содержимого OpenGL, контексты отрисовки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e72839d04838b3173d772fbbf29a903a295cfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411122"
---
# <a name="porting-rendering-contexts"></a><span data-ttu-id="5e476-107">Перенос контекстов рендеринга</span><span class="sxs-lookup"><span data-stu-id="5e476-107">Porting Rendering Contexts</span></span>

<span data-ttu-id="5e476-108">Система Window X и окна отображаются с помощью контекстов отрисовки.</span><span class="sxs-lookup"><span data-stu-id="5e476-108">The X Window System and Windows render through rendering contexts.</span></span> <span data-ttu-id="5e476-109">Шесть функций ГЛКС, управляющих контекстами отрисовки и пять из них, имеют эквивалентную функцию Windows.</span><span class="sxs-lookup"><span data-stu-id="5e476-109">Six GLX functions manage rendering contexts and five of them have an equivalent Windows function.</span></span>

<span data-ttu-id="5e476-110">В следующей таблице перечислены функции подготовки к просмотру ГЛКС и их эквивалентные функции Windows.</span><span class="sxs-lookup"><span data-stu-id="5e476-110">The following table lists the GLX rendering functions and their equivalent Windows functions.</span></span>



| <span data-ttu-id="5e476-111">Функция контекста отрисовки ГЛКС</span><span class="sxs-lookup"><span data-stu-id="5e476-111">GLX rendering context function</span></span>                                                                            | <span data-ttu-id="5e476-112">Функция контекста отрисовки Windows</span><span class="sxs-lookup"><span data-stu-id="5e476-112">Windows rendering context function</span></span>                                      |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="5e476-113">Глксконтекст **глкскопиконтекст**(отображение *\* ДПИ*, глксконтекст *src*, глксконтекст *DST*, глуинт *Mask*)</span><span class="sxs-lookup"><span data-stu-id="5e476-113">GLXContext **glXCopyContext**( Display *\*dpy*,GLXContext *src*,GLXContext *dst*,GLuint *mask*)</span></span>            | <span data-ttu-id="5e476-114">Не применяется</span><span class="sxs-lookup"><span data-stu-id="5e476-114">Not applicable.</span></span>                                                         |
| <span data-ttu-id="5e476-115">Глксконтекст **глкскреатеконтекст**(отображение *\* ДПИ*, ксвисуалинфо *\* обратитесь*, глксконтекст *шарелист*, bool *Direct*)</span><span class="sxs-lookup"><span data-stu-id="5e476-115">GLXContext **glXCreateContext**( Display *\*dpy*,XVisualInfo *\*vis*,GLXContext *shareList*,Bool *direct*)</span></span> | <span data-ttu-id="5e476-116">ХГЛРК [**вглкреатеконтекст**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)(HDC *HDC*)</span><span class="sxs-lookup"><span data-stu-id="5e476-116">HGLRC [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)( HDC *hdc*)</span></span>          |
| <span data-ttu-id="5e476-117">void **глксделетеконтекст**(отображение *\* ДПИ*, глксконтекст *CTX*)</span><span class="sxs-lookup"><span data-stu-id="5e476-117">void **glXDeleteContext**( Display *\*dpy*,GLXContext *ctx*)</span></span>                                              | <span data-ttu-id="5e476-118">BOOL [**вглделетеконтекст**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)(хглрк *хглрк*)</span><span class="sxs-lookup"><span data-stu-id="5e476-118">BOOL [**wglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)( HGLRC *hglrc*)</span></span>       |
| <span data-ttu-id="5e476-119">Глксконтекст **глксжеткуррентконтекст**(*void*)</span><span class="sxs-lookup"><span data-stu-id="5e476-119">GLXContext **glXGetCurrentContext**(*void*)</span></span>                                                               | <span data-ttu-id="5e476-120">ХГЛРК [**вглжеткуррентконтекст**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)(*void*)</span><span class="sxs-lookup"><span data-stu-id="5e476-120">HGLRC [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)(*VOID*)</span></span>      |
| <span data-ttu-id="5e476-121">Глксдравабле **глксжеткуррентдравабле**(*void*)</span><span class="sxs-lookup"><span data-stu-id="5e476-121">GLXDrawable **glXGetCurrentDrawable**(*void*)</span></span>                                                             | <span data-ttu-id="5e476-122">HDC [**вглжеткуррентдк**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)(*void*)</span><span class="sxs-lookup"><span data-stu-id="5e476-122">HDC [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)(*VOID*)</span></span>                  |
| <span data-ttu-id="5e476-123">Bool **глксмакекуррент**(отображение *\* ДПИ*, глксдравабле *Draw*, глксконтекст *CTX*)</span><span class="sxs-lookup"><span data-stu-id="5e476-123">Bool **glXMakeCurrent**( Display *\*dpy*,GLXDrawable *draw*,GLXContext *ctx*)</span></span>                              | <span data-ttu-id="5e476-124">BOOL [**вглмакекуррент**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)(HDC *HDC*, хглрк *хглрк*)</span><span class="sxs-lookup"><span data-stu-id="5e476-124">BOOL [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)( HDC *hdc*,HGLRC *hglrc*)</span></span> |



 

<span data-ttu-id="5e476-125">Возвращаемые типы и другие типы имеют разные имена в системе Window X, чем в Windows.</span><span class="sxs-lookup"><span data-stu-id="5e476-125">Return types and other types have different names in the X Window System than in Windows.</span></span> <span data-ttu-id="5e476-126">Можно выполнить поиск вхождений Глксконтекст, чтобы найти части кода, которые необходимо перенести.</span><span class="sxs-lookup"><span data-stu-id="5e476-126">You can search for occurrences of GLXContext to help find parts of your code that need to be ported.</span></span>

<span data-ttu-id="5e476-127">В следующих разделах сравниваются примеры кода контекста для отображения в программе X Window System и том же коде после переноса в Windows.</span><span class="sxs-lookup"><span data-stu-id="5e476-127">The following sections compare rendering context code samples in an X Window System program and the same code after it has been ported to Windows.</span></span>

<span data-ttu-id="5e476-128">Дополнительные сведения о контекстах подготовки к просмотру см. в разделе [контексты отрисовки](rendering-contexts.md).</span><span class="sxs-lookup"><span data-stu-id="5e476-128">For more information on rendering contexts, see [Rendering Contexts](rendering-contexts.md).</span></span>

 

 




