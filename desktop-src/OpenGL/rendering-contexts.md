---
title: Контексты отрисовки
description: Контекст визуализации OpenGL — это порт, через который проходят все команды OpenGL. Каждый поток, выполняющий вызовы OpenGL, должен иметь текущий контекст отрисовки. Контексты отрисовки связывают OpenGL с системными окнами Windows.
ms.assetid: 9fbbb0be-2db4-4bfc-9a5c-a43d71554abc
keywords:
- OpenGL в Windows, контексты отрисовки
- Контексты отрисовки OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ac2ac6c5948da2b7372d600377666cd9e4e074
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330984"
---
# <a name="rendering-contexts"></a><span data-ttu-id="6df52-107">Контексты отрисовки</span><span class="sxs-lookup"><span data-stu-id="6df52-107">Rendering Contexts</span></span>

<span data-ttu-id="6df52-108">*Контекст визуализации* OpenGL — это порт, через который проходят все команды OpenGL.</span><span class="sxs-lookup"><span data-stu-id="6df52-108">An OpenGL *rendering context* is a port through which all OpenGL commands pass.</span></span> <span data-ttu-id="6df52-109">Каждый поток, выполняющий вызовы OpenGL, должен иметь текущий контекст отрисовки.</span><span class="sxs-lookup"><span data-stu-id="6df52-109">Every thread that makes OpenGL calls must have a current rendering context.</span></span> <span data-ttu-id="6df52-110">Контексты отрисовки связывают OpenGL с системными окнами Windows.</span><span class="sxs-lookup"><span data-stu-id="6df52-110">Rendering contexts link OpenGL to the Windows windowing systems.</span></span>

<span data-ttu-id="6df52-111">Приложение указывает контекст устройства Windows при создании контекста отрисовки.</span><span class="sxs-lookup"><span data-stu-id="6df52-111">An application specifies a Windows device context when it creates a rendering context.</span></span> <span data-ttu-id="6df52-112">Этот контекст визуализации подходит для рисования на устройстве, на которое ссылается заданный контекст устройства.</span><span class="sxs-lookup"><span data-stu-id="6df52-112">This rendering context is suitable for drawing on the device that the specified device context references.</span></span> <span data-ttu-id="6df52-113">В частности, контекст визуализации имеет тот же формат пикселей, что и контекст устройства.</span><span class="sxs-lookup"><span data-stu-id="6df52-113">In particular, the rendering context has the same pixel format as the device context.</span></span> <span data-ttu-id="6df52-114">Дополнительные сведения см. в разделе [Визуализация функций контекста](rendering-context-functions.md).</span><span class="sxs-lookup"><span data-stu-id="6df52-114">For more information, see [Rendering Context Functions](rendering-context-functions.md).</span></span>

<span data-ttu-id="6df52-115">Несмотря на эту связь, контекст визуализации не совпадает с контекстом устройства.</span><span class="sxs-lookup"><span data-stu-id="6df52-115">Despite this relationship, a rendering context is not the same as a device context.</span></span> <span data-ttu-id="6df52-116">Контекст устройства содержит сведения, относящиеся к компоненту Graphics (GDI) Windows.</span><span class="sxs-lookup"><span data-stu-id="6df52-116">A device context contains information pertinent to the graphics component (GDI) of Windows.</span></span> <span data-ttu-id="6df52-117">Контекст визуализации содержит сведения, относящиеся к OpenGL.</span><span class="sxs-lookup"><span data-stu-id="6df52-117">A rendering context contains information pertinent to OpenGL.</span></span> <span data-ttu-id="6df52-118">Контекст устройства должен быть явно указан в вызове GDI.</span><span class="sxs-lookup"><span data-stu-id="6df52-118">A device context must be explicitly specified in a GDI call.</span></span> <span data-ttu-id="6df52-119">В вызове OpenGL контекст визуализации является неявным.</span><span class="sxs-lookup"><span data-stu-id="6df52-119">A rendering context is implicit in an OpenGL call.</span></span> <span data-ttu-id="6df52-120">Перед созданием контекста отрисовки необходимо задать формат пикселей контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="6df52-120">You should set a device context's pixel format before creating a rendering context.</span></span>

<span data-ttu-id="6df52-121">Поток, выполняющий вызовы OpenGL, должен иметь текущий контекст отрисовки.</span><span class="sxs-lookup"><span data-stu-id="6df52-121">A thread that makes OpenGL calls must have a current rendering context.</span></span> <span data-ttu-id="6df52-122">Если приложение выполняет вызовы OpenGL из потока, в котором отсутствует текущий контекст отрисовки, ничего не происходит; вызов не оказывает никакого влияния.</span><span class="sxs-lookup"><span data-stu-id="6df52-122">If an application makes OpenGL calls from a thread that lacks a current rendering context, nothing happens; the call has no effect.</span></span> <span data-ttu-id="6df52-123">Приложение обычно создает контекст отрисовки, устанавливает его как текущий контекст визуализации потока, а затем вызывает функции OpenGL.</span><span class="sxs-lookup"><span data-stu-id="6df52-123">An application commonly creates a rendering context, sets it as a thread's current rendering context, and then calls OpenGL functions.</span></span> <span data-ttu-id="6df52-124">После завершения вызова функций OpenGL приложение отделяет контекст визуализации от потока, а затем удаляет контекст визуализации.</span><span class="sxs-lookup"><span data-stu-id="6df52-124">When it finishes calling OpenGL functions, the application uncouples the rendering context from the thread, and then deletes the rendering context.</span></span> <span data-ttu-id="6df52-125">Окно может одновременно рисовать несколько контекстов отрисовки, но поток может иметь только один текущий активный контекст визуализации.</span><span class="sxs-lookup"><span data-stu-id="6df52-125">A window can have multiple rendering contexts drawing to it at one time, but a thread can have only one current, active rendering context.</span></span>

<span data-ttu-id="6df52-126">Текущий контекст визуализации имеет связанный контекст устройства.</span><span class="sxs-lookup"><span data-stu-id="6df52-126">A current rendering context has an associated device context.</span></span> <span data-ttu-id="6df52-127">Этот контекст устройства не должен совпадать с контекстом устройства, который использовался при создании контекста визуализации, но должен ссылаться на то же устройство и иметь тот же формат пикселей.</span><span class="sxs-lookup"><span data-stu-id="6df52-127">That device context need not be the same device context as that used when the rendering context was created, but it must reference the same device and have the same pixel format.</span></span>

<span data-ttu-id="6df52-128">Поток может иметь только один текущий контекст отрисовки.</span><span class="sxs-lookup"><span data-stu-id="6df52-128">A thread can have only one current rendering context.</span></span> <span data-ttu-id="6df52-129">Контекст отрисовки может быть текущим только для одного потока.</span><span class="sxs-lookup"><span data-stu-id="6df52-129">A rendering context can be current to only one thread.</span></span>

 

 




