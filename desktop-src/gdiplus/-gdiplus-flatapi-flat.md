---
description: Windows GDI+ предоставляет плоский API, состоящий из примерно 600 функций. Microsoft .NET Framework предоставляет набор классов-оболочек управляемого кода для GDI+.
ms.assetid: afd8cf81-8a20-4592-bd0a-46341742cc9b
title: API плоских структур GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65f91c3c925b7de31f27e91c70cbd1bf0cbbb2a4
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394989"
---
# <a name="gdi-flat-api"></a><span data-ttu-id="2d9ab-104">API плоских структур GDI+</span><span class="sxs-lookup"><span data-stu-id="2d9ab-104">GDI+ Flat API</span></span>

<span data-ttu-id="2d9ab-105">Windows GDI+ предоставляет плоский API, состоящий из примерно 600 функций, которые реализуются в Gdiplus.dll и объявлены в Гдиплусфлат. h.</span><span class="sxs-lookup"><span data-stu-id="2d9ab-105">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="2d9ab-106">Функции в плоском API-интерфейсе GDI+ упаковываются в коллекцию из примерно 40 классов C++.</span><span class="sxs-lookup"><span data-stu-id="2d9ab-106">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="2d9ab-107">Не рекомендуется напрямую вызывать функции в плоском API.</span><span class="sxs-lookup"><span data-stu-id="2d9ab-107">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="2d9ab-108">При каждом вызове GDI+ это следует делать путем вызова методов и функций, предоставляемых оболочками C++.</span><span class="sxs-lookup"><span data-stu-id="2d9ab-108">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="2d9ab-109">Служба технической поддержки Майкрософт не предоставит поддержку для кода, который напрямую вызывает плоский API.</span><span class="sxs-lookup"><span data-stu-id="2d9ab-109">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span>

<span data-ttu-id="2d9ab-110">В качестве альтернативы оболочкам C++ Microsoft .NET Framework предоставляет набор классов-оболочек управляемого кода для GDI+.</span><span class="sxs-lookup"><span data-stu-id="2d9ab-110">As an alternative to the C++ wrappers, the Microsoft .NET Framework provides a set of managed-code wrapper classes for GDI+.</span></span> <span data-ttu-id="2d9ab-111">Оболочки управляемого кода для GDI+ относятся к следующим пространствам имен.</span><span class="sxs-lookup"><span data-stu-id="2d9ab-111">The managed-code wrappers for GDI+ belong to the following namespaces.</span></span>

-   [<span data-ttu-id="2d9ab-112">System.Drawing;</span><span class="sxs-lookup"><span data-stu-id="2d9ab-112">System.Drawing</span></span>](/dotnet/api/system.drawing?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [<span data-ttu-id="2d9ab-113">System. Drawing. Drawing2D</span><span class="sxs-lookup"><span data-stu-id="2d9ab-113">System.Drawing.Drawing2D</span></span>](/dotnet/api/system.drawing.drawing2d?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [<span data-ttu-id="2d9ab-114">System. Drawing. Imaging</span><span class="sxs-lookup"><span data-stu-id="2d9ab-114">System.Drawing.Imaging</span></span>](/dotnet/api/system.drawing.imaging?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [<span data-ttu-id="2d9ab-115">System. Drawing. Text</span><span class="sxs-lookup"><span data-stu-id="2d9ab-115">System.Drawing.Text</span></span>](/dotnet/api/system.drawing.text?view=dotnet-plat-ext-3.1&preserve-view=true)

<span data-ttu-id="2d9ab-116">Оба набора оболочек (C++ и управляемого кода) используют объектно-ориентированный подход, поэтому существуют некоторые различия между тем, как параметры передаются в методы-оболочки, и способ передачи параметров в функции плоского API.</span><span class="sxs-lookup"><span data-stu-id="2d9ab-116">Both sets of wrappers (C++ and managed code) use an object-oriented approach, so there are some differences between the way parameters are passed to the wrapper methods and the way parameters are passed to functions in the flat API.</span></span> <span data-ttu-id="2d9ab-117">Например, одна из оболочек C++ является классом [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) .</span><span class="sxs-lookup"><span data-stu-id="2d9ab-117">For example, one of the C++ wrappers is the [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) class.</span></span> <span data-ttu-id="2d9ab-118">Каждый объект **Matrix** имеет поле **нативематрикс**, которое указывает на внутреннюю переменную типа **гпматрикс**.</span><span class="sxs-lookup"><span data-stu-id="2d9ab-118">Each **Matrix** object has a field, **nativeMatrix**, that points to an internal variable of type **GpMatrix**.</span></span> <span data-ttu-id="2d9ab-119">При передаче параметров в метод объекта **Matrix** этот метод передает эти параметры (или набор связанных параметров) в одну из функций в плоском API-интерфейсе GDI+.</span><span class="sxs-lookup"><span data-stu-id="2d9ab-119">When you pass parameters to a method of a **Matrix** object, that method passes those parameters (or a set of related parameters) along to one of the functions in the GDI+ flat API.</span></span> <span data-ttu-id="2d9ab-120">Но этот метод также передает поле **нативематрикс** (в качестве входного параметра) в функцию плоского API.</span><span class="sxs-lookup"><span data-stu-id="2d9ab-120">But that method also passes the **nativeMatrix** field (as an input parameter) to the flat API function.</span></span> <span data-ttu-id="2d9ab-121">В следующем коде показано, как метод [**Matrix:: сдвига**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear) вызывает функцию **гдипшеарматрикс ( \* МАТРИЦа Гпматрикс, вещественная шеаркс, реальная наклонная, гпматриксордер Order)** .</span><span class="sxs-lookup"><span data-stu-id="2d9ab-121">The following code shows how the [**Matrix::Shear**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear) method calls the **GdipShearMatrix(GpMatrix \*matrix, REAL shearX, REAL shearY, GpMatrixOrder order)** function.</span></span>


```
Status Shear(
      IN REAL shearX, 
      IN REAL shearY,
      IN MatrixOrder order = MatrixOrderPrepend)
{
   ...
   GdipShearMatrix(nativeMatrix, shearX, shearY, order);
   ...
}
```



<span data-ttu-id="2d9ab-122">Конструкторы [**матрицы**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) передают адрес переменной указателя **гпматрикс** (в качестве выходного параметра) в функцию **гдипкреатематрикс (гпматрикс \* \* Matrix)** .</span><span class="sxs-lookup"><span data-stu-id="2d9ab-122">The [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) constructors pass the address of a **GpMatrix** pointer variable (as an output parameter) to the **GdipCreateMatrix(GpMatrix \*\*matrix)** function.</span></span> <span data-ttu-id="2d9ab-123">**Гдипкреатематрикс** создает и инициализирует внутреннюю переменную **гпматрикс** , а затем присваивает адрес **гпматрикс** переменной указателя.</span><span class="sxs-lookup"><span data-stu-id="2d9ab-123">**GdipCreateMatrix** creates and initializes an internal **GpMatrix** variable and then assigns the address of the **GpMatrix** to the pointer variable.</span></span> <span data-ttu-id="2d9ab-124">Затем конструктор копирует значение указателя в поле **нативематрикс** .</span><span class="sxs-lookup"><span data-stu-id="2d9ab-124">Then the constructor copies the value of the pointer to the **nativeMatrix** field.</span></span>


```
Matrix()
{
   GpMatrix *matrix = NULL;
   lastResult = DllExports::GdipCreateMatrix(&matrix);
   SetNativeMatrix(matrix);
}

VOID SetNativeMatrix(GpMatrix *nativeMatrix)
{
   this->nativeMatrix = nativeMatrix;
}
```



<span data-ttu-id="2d9ab-125">Методы клонирования в классах-оболочках не получают параметров, но часто передают два параметра в базовую функцию в плоском API GDI+.</span><span class="sxs-lookup"><span data-stu-id="2d9ab-125">Clone methods in the wrapper classes receive no parameters but often pass two parameters to the underlying function in the GDI+ flat API.</span></span> <span data-ttu-id="2d9ab-126">Например, метод [**Matrix:: Clone**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-clone) передает **нативематрикс** (в качестве входного параметра) и адрес переменной указателя **гпматрикс** (в качестве выходного параметра) в функцию **гдипклонематрикс** .</span><span class="sxs-lookup"><span data-stu-id="2d9ab-126">For example, the [**Matrix::Clone**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-clone) method passes **nativeMatrix** (as an input parameter) and the address of a **GpMatrix** pointer variable (as an output parameter) to the **GdipCloneMatrix** function.</span></span> <span data-ttu-id="2d9ab-127">В следующем коде показано, как метод **Matrix:: Clone** вызывает функцию **гдипклонематрикс (Гпматрикс \* Matrix, гпматрикс \* \* клонематрикс)** .</span><span class="sxs-lookup"><span data-stu-id="2d9ab-127">The following code shows how the **Matrix::Clone** method calls the **GdipCloneMatrix(GpMatrix \*matrix, GpMatrix \*\*cloneMatrix)** function.</span></span>


```
Matrix *Clone() const
{
   GpMatrix *cloneMatrix = NULL;
   ...
   GdipCloneMatrix(nativeMatrix, &cloneMatrix));
   ...
   return new Matrix(cloneMatrix);
 }
```



<span data-ttu-id="2d9ab-128">Функции в плоском API возвращают значение типа Гпстатус.</span><span class="sxs-lookup"><span data-stu-id="2d9ab-128">The functions in the flat API return a value of type GpStatus.</span></span> <span data-ttu-id="2d9ab-129">Перечисление Гпстатус идентично перечислению [**состояния**](/windows/win32/api/Gdiplustypes/ne-gdiplustypes-status) , используемому методами-оболочками.</span><span class="sxs-lookup"><span data-stu-id="2d9ab-129">The GpStatus enumeration is identical to the [**Status**](/windows/win32/api/Gdiplustypes/ne-gdiplustypes-status) enumeration used by the wrapper methods.</span></span> <span data-ttu-id="2d9ab-130">В Гдиплусгпстубс. h Гпстатус определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2d9ab-130">In GdiplusGpStubs.h, GpStatus is defined as follows:</span></span>

`typedef Status GpStatus;`

<span data-ttu-id="2d9ab-131">Большинство методов в классах-оболочках возвращают значение состояния, указывающее, был ли метод обработан удачно.</span><span class="sxs-lookup"><span data-stu-id="2d9ab-131">Most of the methods in the wrapper classes return a status value that indicates whether the method succeeded.</span></span> <span data-ttu-id="2d9ab-132">Однако некоторые из методов-оболочек возвращают значения состояния.</span><span class="sxs-lookup"><span data-stu-id="2d9ab-132">However, some of the wrapper methods return state values.</span></span> <span data-ttu-id="2d9ab-133">При вызове метода-оболочки, возвращающего значение состояния, метод-оболочка передает соответствующие параметры в базовую функцию в плоском API GDI+.</span><span class="sxs-lookup"><span data-stu-id="2d9ab-133">When you call a wrapper method that returns a state value, the wrapper method passes the appropriate parameters to the underlying function in the GDI+ flat API.</span></span> <span data-ttu-id="2d9ab-134">Например, класс [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) имеет метод [**Matrix:: исинвертибле**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-isinvertible) , который передает поле **нативематрикс** и адрес переменной **bool** (в качестве выходного параметра) в функцию **гдиписматриксинвертибле** .</span><span class="sxs-lookup"><span data-stu-id="2d9ab-134">For example, the [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) class has an [**Matrix::IsInvertible**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-isinvertible) method that passes the **nativeMatrix** field and and the address of a **BOOL** variable (as an output parameter) to the **GdipIsMatrixInvertible** function.</span></span> <span data-ttu-id="2d9ab-135">В следующем коде показано, как метод **Matrix:: исинвертибле** вызывает функцию **Гдиписматриксинвертибле (гдипконст ГПМАТРИКС \* Matrix, bool \* result)** .</span><span class="sxs-lookup"><span data-stu-id="2d9ab-135">The following code shows how the **Matrix::IsInvertible** method calls the **GdipIsMatrixInvertible(GDIPCONST GpMatrix \*matrix, BOOL \*result)** function.</span></span>


```
BOOL IsInvertible() const
{
   BOOL result = FALSE;
   ...
   GdipIsMatrixInvertible(nativeMatrix, &result);
   return result;
}
```



<span data-ttu-id="2d9ab-136">Еще одна из оболочек является классом [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) .</span><span class="sxs-lookup"><span data-stu-id="2d9ab-136">Another one of the wrappers is the [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) class.</span></span> <span data-ttu-id="2d9ab-137">Объект **Color** имеет одно поле типа **ARGB**, которое определено как **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="2d9ab-137">A **Color** object has a single field of type **ARGB**, which is defined as a **DWORD**.</span></span> <span data-ttu-id="2d9ab-138">При передаче объекта **Color** в один из методов-оболочек этот метод передает поле **ARGB** вместе с базовой функцией в плоском API GDI+.</span><span class="sxs-lookup"><span data-stu-id="2d9ab-138">When you pass a **Color** object to one of the wrapper methods, that method passes the **ARGB** field along to the underlying function in the GDI+ flat API.</span></span> <span data-ttu-id="2d9ab-139">В следующем коде показано, как метод [**Pen:: сетколор**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setcolor) вызывает функцию **гдипсетпенколор (ГППЕН \* Pen, ARGB ARGB)** .</span><span class="sxs-lookup"><span data-stu-id="2d9ab-139">The following code shows how the [**Pen::SetColor**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setcolor) method calls the **GdipSetPenColor(GpPen \*pen, ARGB argb)** function.</span></span> <span data-ttu-id="2d9ab-140">Метод [**Color:: GetValue**](/windows/win32/api/Gdipluscolor/nf-gdipluscolor-color-getvalue) возвращает значение поля **ARGB** .</span><span class="sxs-lookup"><span data-stu-id="2d9ab-140">The [**Color::GetValue**](/windows/win32/api/Gdipluscolor/nf-gdipluscolor-color-getvalue) method returns the value of the **ARGB** field.</span></span>


```
Status SetColor(IN const Color& color)
{
   ...
   GdipSetPenColor(nativePen, color.GetValue());
}
```



<span data-ttu-id="2d9ab-141">В следующих разделах показано отношение между плоским API GDI+ и методами-оболочками C++.</span><span class="sxs-lookup"><span data-stu-id="2d9ab-141">The following topics show the relationship between the GDI+ flat API and the C++ wrapper methods.</span></span>

-   [<span data-ttu-id="2d9ab-142">Функции Аджустаблеарровкап</span><span class="sxs-lookup"><span data-stu-id="2d9ab-142">AdjustableArrowCap Functions</span></span>](-gdiplus-adjustablearrowcap-flat.md)
-   [<span data-ttu-id="2d9ab-143">Функции точечного рисунка</span><span class="sxs-lookup"><span data-stu-id="2d9ab-143">Bitmap Functions</span></span>](-gdiplus-bitmap-flat.md)
-   [<span data-ttu-id="2d9ab-144">Функции кисти</span><span class="sxs-lookup"><span data-stu-id="2d9ab-144">Brush Functions</span></span>](-gdiplus-brush-flat.md)
-   [<span data-ttu-id="2d9ab-145">Функции Качедбитмап</span><span class="sxs-lookup"><span data-stu-id="2d9ab-145">CachedBitmap Functions</span></span>](-gdiplus-cachedbitmap-flat.md)
-   [<span data-ttu-id="2d9ab-146">Функции Кустомлинекап</span><span class="sxs-lookup"><span data-stu-id="2d9ab-146">CustomLineCap Functions</span></span>](-gdiplus-customlinecap-flat.md)
-   [<span data-ttu-id="2d9ab-147">Функции шрифтов</span><span class="sxs-lookup"><span data-stu-id="2d9ab-147">Font Functions</span></span>](-gdiplus-font-flat.md)
-   [<span data-ttu-id="2d9ab-148">фонтфамилифунктионс</span><span class="sxs-lookup"><span data-stu-id="2d9ab-148">FontFamilyFunctions</span></span>](-gdiplus-fontfamily-flat.md)
-   [<span data-ttu-id="2d9ab-149">Графические функции</span><span class="sxs-lookup"><span data-stu-id="2d9ab-149">Graphics Functions</span></span>](-gdiplus-graphics-flat.md)
-   [<span data-ttu-id="2d9ab-150">Функции GraphicsPath</span><span class="sxs-lookup"><span data-stu-id="2d9ab-150">GraphicsPath Functions</span></span>](-gdiplus-graphicspath-flat.md)
-   [<span data-ttu-id="2d9ab-151">Функции Хатчбруш</span><span class="sxs-lookup"><span data-stu-id="2d9ab-151">HatchBrush Functions</span></span>](-gdiplus-hatchbrush-flat.md)
-   [<span data-ttu-id="2d9ab-152">Функции изображений</span><span class="sxs-lookup"><span data-stu-id="2d9ab-152">Image Functions</span></span>](-gdiplus-image-flat.md)
-   [<span data-ttu-id="2d9ab-153">Функции ImageAttributes</span><span class="sxs-lookup"><span data-stu-id="2d9ab-153">ImageAttributes Functions</span></span>](-gdiplus-imageattributes-flat.md)
-   [<span data-ttu-id="2d9ab-154">Функции LinearGradientBrush</span><span class="sxs-lookup"><span data-stu-id="2d9ab-154">LinearGradientBrush Functions</span></span>](-gdiplus-lineargradientbrush-flat.md)
-   [<span data-ttu-id="2d9ab-155">Функции матрицы</span><span class="sxs-lookup"><span data-stu-id="2d9ab-155">Matrix Functions</span></span>](-gdiplus-matrix-flat.md)
-   [<span data-ttu-id="2d9ab-156">Функции памяти</span><span class="sxs-lookup"><span data-stu-id="2d9ab-156">Memory Functions</span></span>](-gdiplus-memory-flat.md)
-   [<span data-ttu-id="2d9ab-157">Функции уведомлений</span><span class="sxs-lookup"><span data-stu-id="2d9ab-157">Notification Functions</span></span>](-gdiplus-notification-flat.md)
-   [<span data-ttu-id="2d9ab-158">Функции Пасградиентбруш</span><span class="sxs-lookup"><span data-stu-id="2d9ab-158">PathGradientBrush Functions</span></span>](-gdiplus-pathgradientbrush-flat.md)
-   [<span data-ttu-id="2d9ab-159">Функции Паситератор</span><span class="sxs-lookup"><span data-stu-id="2d9ab-159">PathIterator Functions</span></span>](-gdiplus-pathiterator-flat.md)
-   [<span data-ttu-id="2d9ab-160">Функции пера</span><span class="sxs-lookup"><span data-stu-id="2d9ab-160">Pen Functions</span></span>](-gdiplus-pen-flat.md)
-   [<span data-ttu-id="2d9ab-161">Функции Region</span><span class="sxs-lookup"><span data-stu-id="2d9ab-161">Region Functions</span></span>](-gdiplus-region-flat.md)
-   [<span data-ttu-id="2d9ab-162">Функции SolidBrush</span><span class="sxs-lookup"><span data-stu-id="2d9ab-162">SolidBrush Functions</span></span>](-gdiplus-solidbrush-flat.md)
-   [<span data-ttu-id="2d9ab-163">Функции формата строки</span><span class="sxs-lookup"><span data-stu-id="2d9ab-163">String Format Functions</span></span>](-gdiplus-stringformat-flat.md)
-   [<span data-ttu-id="2d9ab-164">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="2d9ab-164">Text Functions</span></span>](-gdiplus-text-flat.md)
-   [<span data-ttu-id="2d9ab-165">Функции текстурной кисти</span><span class="sxs-lookup"><span data-stu-id="2d9ab-165">Texture Brush Functions</span></span>](-gdiplus-texturebrush-flat.md)

 

 
