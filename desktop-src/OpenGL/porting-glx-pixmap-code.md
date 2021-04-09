---
title: Перенос кода Пиксмап ГЛКС
description: Перенос кода Пиксмап ГЛКС
ms.assetid: 5b87d26d-b3ea-4f90-9456-d3f7da462948
keywords:
- пиксмапс
- OpenGL в Windows, пиксмапс
- перенос в OpenGL, пиксмапс
- Перенос по стандарту OpenGL, пиксмапс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed0dbd7f94736f25346a9136d60feb4fa1bb6c68
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070543"
---
# <a name="porting-glx-pixmap-code"></a><span data-ttu-id="c33f5-107">Перенос кода Пиксмап ГЛКС</span><span class="sxs-lookup"><span data-stu-id="c33f5-107">Porting GLX Pixmap Code</span></span>

<span data-ttu-id="c33f5-108">Система Window X использует *пиксмапс*, которые являются областями виртуального рисования вне экрана в форме трехмерного массива битов.</span><span class="sxs-lookup"><span data-stu-id="c33f5-108">The X Window System uses *pixmaps*, which are off-screen virtual drawing surfaces in the form of a three-dimensional array of bits.</span></span> <span data-ttu-id="c33f5-109">Пиксмап можно представить как стек растровых изображений: двумерный массив пикселей, в котором каждый пиксель имеет значение от 0 до 2N1, где N — Глубина пиксмап.</span><span class="sxs-lookup"><span data-stu-id="c33f5-109">You can think of a pixmap as a stack of bitmaps: a two-dimensional array of pixels with each pixel having a value from 0 to 2N1 where N is the depth of the pixmap.</span></span>

<span data-ttu-id="c33f5-110">Для программ OpenGL используются функции ГЛКС, **глкскреатеглкспиксмап** и **глксдестройглкспиксмап**, для создания и уничтожения глкс пиксмапс, используемых для отрисовки на экране.</span><span class="sxs-lookup"><span data-stu-id="c33f5-110">For OpenGL programs you use the GLX functions, **glXCreateGLXPixmap** and **glXDestroyGLXPixmap**, to create and destroy GLX pixmaps used for off-screen rendering.</span></span>

<span data-ttu-id="c33f5-111">Windows использует аппаратно-независимые точечные рисунки, которые выполняют ту же функцию, что и X Window System пиксмапс.</span><span class="sxs-lookup"><span data-stu-id="c33f5-111">Windows uses device-independent bitmaps that serve the same function as X Window System pixmaps.</span></span> <span data-ttu-id="c33f5-112">Используйте стандартные функции точечного рисунка Windows для создания и уничтожения точечных рисунков.</span><span class="sxs-lookup"><span data-stu-id="c33f5-112">Use the standard Windows bitmap functions to create and destroy bitmaps.</span></span>

<span data-ttu-id="c33f5-113">В следующей таблице перечислены функции ГЛКС пиксмап и их эквивалентные функции Bitmap Windows.</span><span class="sxs-lookup"><span data-stu-id="c33f5-113">The following table lists the GLX pixmap functions and their equivalent Windows bitmap functions.</span></span>



| <span data-ttu-id="c33f5-114">ГЛКС пиксмап и функция Font</span><span class="sxs-lookup"><span data-stu-id="c33f5-114">GLX pixmap and font function</span></span>                                                          | <span data-ttu-id="c33f5-115">Функция Bitmap и Font в Windows</span><span class="sxs-lookup"><span data-stu-id="c33f5-115">Windows bitmap and font function</span></span>                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c33f5-116">Глкспиксмап **глкскреатеглкспиксмап**(отображение *\* ДПИ*, ксвисуалинфо *\* обратитесь*, пиксмап *пиксмап*)</span><span class="sxs-lookup"><span data-stu-id="c33f5-116">GLXPixmap **glXCreateGLXPixmap**( Display *\*dpy*,XVisualInfo *\*vis*,Pixmap *pixmap*)</span></span> | <span data-ttu-id="c33f5-117">ХБИТМАП [креатедибитмап](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) HDC *HDC*, Лпбитмапинфохеадер *лпбмих*, DWORD *фдвинит*, const Byte *\* лпбинит*, лпбитмапинфо *лпбми*, uint \* fuUsage \***)** HBITMAP [CreateDIBSection](/windows/desktop/api/wingdi/nf-wingdi-createdibsection) HDC *HDC*, LPBITMAPINFO *lpbmi*, DWORD *fInit*, DWORD *iUsage*)</span><span class="sxs-lookup"><span data-stu-id="c33f5-117">HBITMAP [CreateDIBitmap](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) HDC *hdc*,LPBITMAPINFOHEADER *lpbmih*,DWORD *fdwInit*,CONST BYTE *\*lpbInit*,LPBITMAPINFO *lpbmi*,UINT *fuUsage\*\*\*)*\* HBITMAP [CreateDIBSection](/windows/desktop/api/wingdi/nf-wingdi-createdibsection) HDC *hdc*,LPBITMAPINFO *lpbmi*,DWORD *fInit*,DWORD *iUsage*)</span></span><br/> |
| <span data-ttu-id="c33f5-118">void **глксдестройглкспиксмап**(отображение *\* ДПИ*, глкспиксмап *PIX*)</span><span class="sxs-lookup"><span data-stu-id="c33f5-118">void **glXDestroyGLXPixmap**( Display *\*dpy*,GLXPixmap *pix*)</span></span>                        | <span data-ttu-id="c33f5-119">BOOL [DeleteObject](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)(хгдиобж *хобжект*)</span><span class="sxs-lookup"><span data-stu-id="c33f5-119">BOOL [DeleteObject](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)( HGDIOBJ *hObject*)</span></span>                                                                                                                                                                                                                                  |



 

 

