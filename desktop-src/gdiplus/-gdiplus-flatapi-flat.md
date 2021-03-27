---
description: Windows GDI+ предоставляет плоский API, состоящий из примерно 600 функций, которые реализуются в Gdiplus.dll и объявлены в Гдиплусфлат. h.
ms.assetid: afd8cf81-8a20-4592-bd0a-46341742cc9b
title: API плоских структур GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 450f89439b6ead3b8cd9a49f52a6620571f6db54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997491"
---
# <a name="gdi-flat-api"></a>API плоских структур GDI+

Windows GDI+ предоставляет плоский API, состоящий из примерно 600 функций, которые реализуются в Gdiplus.dll и объявлены в Гдиплусфлат. h. Функции в плоском API-интерфейсе GDI+ упаковываются в коллекцию из примерно 40 классов C++. Не рекомендуется напрямую вызывать функции в плоском API. При каждом вызове GDI+ это следует делать путем вызова методов и функций, предоставляемых оболочками C++. Служба технической поддержки Майкрософт не предоставит поддержку для кода, который напрямую вызывает плоский API.

В качестве альтернативы оболочкам C++ Microsoft .NET Framework предоставляет набор классов-оболочек управляемого кода для GDI+. Оболочки управляемого кода для GDI+ относятся к следующим пространствам имен.

-   [System.Drawing;](/dotnet/api/system.drawing?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [System. Drawing. Drawing2D](/dotnet/api/system.drawing.drawing2d?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [System. Drawing. Imaging](/dotnet/api/system.drawing.imaging?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [System. Drawing. Text](/dotnet/api/system.drawing.text?view=dotnet-plat-ext-3.1&preserve-view=true)

Оба набора оболочек (C++ и управляемого кода) используют объектно-ориентированный подход, поэтому существуют некоторые различия между тем, как параметры передаются в методы-оболочки, и способ передачи параметров в функции плоского API. Например, одна из оболочек C++ является классом [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) . Каждый объект **Matrix** имеет поле **нативематрикс**, которое указывает на внутреннюю переменную типа **гпматрикс**. При передаче параметров в метод объекта **Matrix** этот метод передает эти параметры (или набор связанных параметров) в одну из функций в плоском API-интерфейсе GDI+. Но этот метод также передает поле **нативематрикс** (в качестве входного параметра) в функцию плоского API. В следующем коде показано, как метод [**Matrix:: сдвига**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear) вызывает функцию **гдипшеарматрикс ( \* МАТРИЦа Гпматрикс, вещественная шеаркс, реальная наклонная, гпматриксордер Order)** .


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



Конструкторы [**матрицы**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) передают адрес переменной указателя **гпматрикс** (в качестве выходного параметра) в функцию **гдипкреатематрикс (гпматрикс \* \* Matrix)** . **Гдипкреатематрикс** создает и инициализирует внутреннюю переменную **гпматрикс** , а затем присваивает адрес **гпматрикс** переменной указателя. Затем конструктор копирует значение указателя в поле **нативематрикс** .


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



Методы клонирования в классах-оболочках не получают параметров, но часто передают два параметра в базовую функцию в плоском API GDI+. Например, метод [**Matrix:: Clone**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-clone) передает **нативематрикс** (в качестве входного параметра) и адрес переменной указателя **гпматрикс** (в качестве выходного параметра) в функцию **гдипклонематрикс** . В следующем коде показано, как метод **Matrix:: Clone** вызывает функцию **гдипклонематрикс (Гпматрикс \* Matrix, гпматрикс \* \* клонематрикс)** .


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



Функции в плоском API возвращают значение типа Гпстатус. Перечисление Гпстатус идентично перечислению [**состояния**](/windows/win32/api/Gdiplustypes/ne-gdiplustypes-status) , используемому методами-оболочками. В Гдиплусгпстубс. h Гпстатус определяется следующим образом:

`typedef Status GpStatus;`

Большинство методов в классах-оболочках возвращают значение состояния, указывающее, был ли метод обработан удачно. Однако некоторые из методов-оболочек возвращают значения состояния. При вызове метода-оболочки, возвращающего значение состояния, метод-оболочка передает соответствующие параметры в базовую функцию в плоском API GDI+. Например, класс [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) имеет метод [**Matrix:: исинвертибле**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-isinvertible) , который передает поле **нативематрикс** и адрес переменной **bool** (в качестве выходного параметра) в функцию **гдиписматриксинвертибле** . В следующем коде показано, как метод **Matrix:: исинвертибле** вызывает функцию **Гдиписматриксинвертибле (гдипконст ГПМАТРИКС \* Matrix, bool \* result)** .


```
BOOL IsInvertible() const
{
   BOOL result = FALSE;
   ...
   GdipIsMatrixInvertible(nativeMatrix, &result);
   return result;
}
```



Еще одна из оболочек является классом [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) . Объект **Color** имеет одно поле типа **ARGB**, которое определено как **DWORD**. При передаче объекта **Color** в один из методов-оболочек этот метод передает поле **ARGB** вместе с базовой функцией в плоском API GDI+. В следующем коде показано, как метод [**Pen:: сетколор**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setcolor) вызывает функцию **гдипсетпенколор (ГППЕН \* Pen, ARGB ARGB)** . Метод [**Color:: GetValue**](/windows/win32/api/Gdipluscolor/nf-gdipluscolor-color-getvalue) возвращает значение поля **ARGB** .


```
Status SetColor(IN const Color& color)
{
   ...
   GdipSetPenColor(nativePen, color.GetValue());
}
```



В следующих разделах показано отношение между плоским API GDI+ и методами-оболочками C++.

-   [Функции Аджустаблеарровкап](-gdiplus-adjustablearrowcap-flat.md)
-   [Функции точечного рисунка](-gdiplus-bitmap-flat.md)
-   [Функции кисти](-gdiplus-brush-flat.md)
-   [Функции Качедбитмап](-gdiplus-cachedbitmap-flat.md)
-   [Функции Кустомлинекап](-gdiplus-customlinecap-flat.md)
-   [Функции шрифтов](-gdiplus-font-flat.md)
-   [фонтфамилифунктионс](-gdiplus-fontfamily-flat.md)
-   [Графические функции](-gdiplus-graphics-flat.md)
-   [Функции GraphicsPath](-gdiplus-graphicspath-flat.md)
-   [Функции Хатчбруш](-gdiplus-hatchbrush-flat.md)
-   [Функции изображений](-gdiplus-image-flat.md)
-   [Функции ImageAttributes](-gdiplus-imageattributes-flat.md)
-   [Функции LinearGradientBrush](-gdiplus-lineargradientbrush-flat.md)
-   [Функции матрицы](-gdiplus-matrix-flat.md)
-   [Функции памяти](-gdiplus-memory-flat.md)
-   [Функции уведомлений](-gdiplus-notification-flat.md)
-   [Функции Пасградиентбруш](-gdiplus-pathgradientbrush-flat.md)
-   [Функции Паситератор](-gdiplus-pathiterator-flat.md)
-   [Функции пера](-gdiplus-pen-flat.md)
-   [Функции Region](-gdiplus-region-flat.md)
-   [Функции SolidBrush](-gdiplus-solidbrush-flat.md)
-   [Функции формата строки](-gdiplus-stringformat-flat.md)
-   [Текстовые функции](-gdiplus-text-flat.md)
-   [Функции текстурной кисти](-gdiplus-texturebrush-flat.md)

 

 
