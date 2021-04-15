---
title: Функция Гладдсвафинтректвин (GL. h)
description: Функция обратного вызова Гладдсвафинтректвин задает набор прямоугольников, которые должны быть скопированы с помощью Свапбуфферс.
ms.assetid: f242e755-8e8a-471a-9884-47efa22a3de6
keywords:
- Функция Гладдсвафинтректвин OpenGL
topic_type:
- apiref
api_name:
- glAddSwapHintRectWIN
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae3e10c2f51ff8d7c9763ff1dad7d09d800cd60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415708"
---
# <a name="gladdswaphintrectwin-function"></a><span data-ttu-id="91a36-104">Функция Гладдсвафинтректвин</span><span class="sxs-lookup"><span data-stu-id="91a36-104">glAddSwapHintRectWIN function</span></span>

<span data-ttu-id="91a36-105">Функция обратного вызова **гладдсвафинтректвин** задает набор прямоугольников, которые должны быть скопированы с помощью [**свапбуфферс**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span><span class="sxs-lookup"><span data-stu-id="91a36-105">The **glAddSwapHintRectWIN** callback function specifies a set of rectangles that are to be copied by [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span></span>

## <a name="syntax"></a><span data-ttu-id="91a36-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91a36-106">Syntax</span></span>


```C++
void WINAPI glAddSwapHintRectWIN(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a><span data-ttu-id="91a36-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="91a36-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91a36-108">*x*</span><span class="sxs-lookup"><span data-stu-id="91a36-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="91a36-109">Координата *x*(в координатах окна) левого нижнего угла прямоугольника области подсказки.</span><span class="sxs-lookup"><span data-stu-id="91a36-109">The *x*-coordinate (in window coordinates) of the lower-left corner of the hint region rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="91a36-110">*y*</span><span class="sxs-lookup"><span data-stu-id="91a36-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="91a36-111">Координата *y*(в координатах окна) левого нижнего угла прямоугольника области подсказки.</span><span class="sxs-lookup"><span data-stu-id="91a36-111">The *y*-coordinate (in window coordinates) of the lower-left corner of the hint region rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="91a36-112">*width*</span><span class="sxs-lookup"><span data-stu-id="91a36-112">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="91a36-113">Ширина прямоугольника области подсказки.</span><span class="sxs-lookup"><span data-stu-id="91a36-113">The width of the hint region rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="91a36-114">*height*</span><span class="sxs-lookup"><span data-stu-id="91a36-114">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="91a36-115">Высота прямоугольника области подсказки.</span><span class="sxs-lookup"><span data-stu-id="91a36-115">The height of the hint region rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91a36-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="91a36-116">Return value</span></span>

<span data-ttu-id="91a36-117">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="91a36-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="91a36-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="91a36-118">Remarks</span></span>

<span data-ttu-id="91a36-119">Функция **гладдсвафинтректвин** ускоряет анимацию, уменьшая объем перерисовки кадров.</span><span class="sxs-lookup"><span data-stu-id="91a36-119">The **glAddSwapHintRectWIN** function speeds up animation by reducing the amount of repainting between frames.</span></span> <span data-ttu-id="91a36-120">С помощью **гладдсвафинтректвин** вы указываете набор прямоугольных областей, которые необходимо скопировать при вызове [**свапбуфферс**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span><span class="sxs-lookup"><span data-stu-id="91a36-120">With **glAddSwapHintRectWIN**, you specify a set of rectangular areas that you want copied when you call [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span></span> <span data-ttu-id="91a36-121">Если не указать ни одного прямоугольника с **гладдсвафинтректвин** перед вызовом **свапбуфферс**, весь буфера кадров будет заменен.</span><span class="sxs-lookup"><span data-stu-id="91a36-121">When you do not specify any rectangles with **glAddSwapHintRectWIN** before calling **SwapBuffers**, the entire framebuffer is swapped.</span></span> <span data-ttu-id="91a36-122">Использование **гладдсвафинтректвин** для копирования только измененных частей буфера может значительно повысить производительность **свапбуфферс**, особенно при реализации **свапбуфферс** в программном обеспечении.</span><span class="sxs-lookup"><span data-stu-id="91a36-122">Using **glAddSwapHintRectWIN** to copy only changed parts of the buffer can significantly increase the performance of **SwapBuffers**, especially when **SwapBuffers** is implemented in software.</span></span>

<span data-ttu-id="91a36-123">Функция **гладдсвафинтректвин** Добавляет прямоугольник в область подсказки.</span><span class="sxs-lookup"><span data-stu-id="91a36-123">The **glAddSwapHintRectWIN** function adds a rectangle to the hint region.</span></span> <span data-ttu-id="91a36-124">Если \_ \_ ЗАДАН флаг ПФД swap Copy структуры формата пикселей [**пикселформатдескриптор**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) , **свапбуфферс** использует этот регион для обрезки копирования заднего буфера в передний буфер.</span><span class="sxs-lookup"><span data-stu-id="91a36-124">When the PFD\_SWAP\_COPY flag of the [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) pixel format structure is set, **SwapBuffers** uses this region to clip the copying of the back buffer to the front buffer.</span></span> <span data-ttu-id="91a36-125">Вы не укажете \_ копию ПФД Swap \_ ; она устанавливается с поддержкой оборудования.</span><span class="sxs-lookup"><span data-stu-id="91a36-125">You don't specify PFD\_SWAP\_COPY; it is set by capable hardware.</span></span> <span data-ttu-id="91a36-126">Область подсказки удаляется после каждого вызова **свапбуфферс**.</span><span class="sxs-lookup"><span data-stu-id="91a36-126">The hint region is cleared after each call to **SwapBuffers**.</span></span> <span data-ttu-id="91a36-127">В некоторых конфигурациях оборудования **свапбуфферс** может игнорировать область подсказки и переключить весь буфер.</span><span class="sxs-lookup"><span data-stu-id="91a36-127">With some hardware configurations, **SwapBuffers** can ignore the hint region and exchange the entire buffer.</span></span> <span data-ttu-id="91a36-128">**Свапбуфферс** реализуется системой, а не приложением.</span><span class="sxs-lookup"><span data-stu-id="91a36-128">**SwapBuffers** is implemented by the system, not by the application.</span></span>

<span data-ttu-id="91a36-129">OpenGL поддерживает отдельную область подсказки для каждого окна.</span><span class="sxs-lookup"><span data-stu-id="91a36-129">OpenGL maintains a separate hint region for each window.</span></span> <span data-ttu-id="91a36-130">При вызове **гладдсвафинтректвин** для любого контекста отрисовки, связанного с окном, прямоугольники подсказки объединяются в один регион.</span><span class="sxs-lookup"><span data-stu-id="91a36-130">When you call **glAddSwapHintRectWIN** on any rendering contexts associated with a window, the hint rectangles are combined into a single region.</span></span>

<span data-ttu-id="91a36-131">Вызовите **гладдсвафинтректвин** с ограничивающим прямоугольником для каждого объекта, рисуемого для рамки, и для каждого прямоугольника, очищенного для стирания предыдущих объектов Frame.</span><span class="sxs-lookup"><span data-stu-id="91a36-131">Call **glAddSwapHintRectWIN** with a bounding rectangle for each object drawn for a frame and for each rectangle cleared to erase previous frame objects.</span></span>

> [!Note]  
> <span data-ttu-id="91a36-132">Функция **гладдсвафинтректвин** — это функция расширения, которая не является частью стандартной библиотеки OpenGL, но является частью \_ \_ расширения подсказок для функции подкачки GL \_ .</span><span class="sxs-lookup"><span data-stu-id="91a36-132">The **glAddSwapHintRectWIN** function is an extension function that is not part of the standard OpenGL library but is part of the GL\_WIN\_swap\_hint extension.</span></span> <span data-ttu-id="91a36-133">Чтобы проверить, поддерживает ли ваша реализация OpenGL **гладдсвафинтректвин**, вызовите **глжетстринг**( \_ расширения GL).</span><span class="sxs-lookup"><span data-stu-id="91a36-133">To check whether your implementation of OpenGL supports **glAddSwapHintRectWIN**, call **glGetString**(GL\_EXTENSIONS).</span></span> <span data-ttu-id="91a36-134">Если он возвращает \_ Указание на выигрывает \_ выставляемую \_ подсказку, **гладдсвафинтректвин** поддерживается.</span><span class="sxs-lookup"><span data-stu-id="91a36-134">If it returns GL\_WIN\_swap\_hint, **glAddSwapHintRectWIN** is supported.</span></span> <span data-ttu-id="91a36-135">Чтобы получить адрес функции расширения, вызовите **вглжетпрокаддресс**.</span><span class="sxs-lookup"><span data-stu-id="91a36-135">To obtain the address of an extension function, call **wglGetProcAddress**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="91a36-136">Требования</span><span class="sxs-lookup"><span data-stu-id="91a36-136">Requirements</span></span>



| <span data-ttu-id="91a36-137">Требование</span><span class="sxs-lookup"><span data-stu-id="91a36-137">Requirement</span></span> | <span data-ttu-id="91a36-138">Значение</span><span class="sxs-lookup"><span data-stu-id="91a36-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="91a36-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="91a36-139">Minimum supported client</span></span><br/> | <span data-ttu-id="91a36-140">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="91a36-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="91a36-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="91a36-141">Minimum supported server</span></span><br/> | <span data-ttu-id="91a36-142">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="91a36-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="91a36-143">Заголовок</span><span class="sxs-lookup"><span data-stu-id="91a36-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="91a36-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="91a36-144"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91a36-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="91a36-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91a36-146">**глжетстринг**</span><span class="sxs-lookup"><span data-stu-id="91a36-146">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="91a36-147">**пикселформатдескриптор**</span><span class="sxs-lookup"><span data-stu-id="91a36-147">**PIXELFORMATDESCRIPTOR**</span></span>](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)
</dt> <dt>

[<span data-ttu-id="91a36-148">**свапбуфферс**</span><span class="sxs-lookup"><span data-stu-id="91a36-148">**SwapBuffers**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)
</dt> <dt>

[<span data-ttu-id="91a36-149">**вглжетпрокаддресс**</span><span class="sxs-lookup"><span data-stu-id="91a36-149">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





