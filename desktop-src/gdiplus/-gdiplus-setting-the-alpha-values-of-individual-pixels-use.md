---
description: В разделе Использование матрицы цветов для установки альфа-значений в изображениях показан неразрушающий метод изменения альфа-значений изображения.
ms.assetid: 38c6254d-5191-4948-804a-1a4427aab7c6
title: Установка альфа-значений отдельных пикселов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cd45bf32284ffc9a8cef13f368cff59e1e8a74f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541455"
---
# <a name="setting-the-alpha-values-of-individual-pixels"></a>Установка альфа-значений отдельных пикселов

В разделе [Использование матрицы цветов для установки альфа-значений в изображениях](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md) показан неразрушающий метод изменения альфа-значений изображения. Пример в этом разделе отображает изображение полупрозрачным образом, но данные пикселей в точечном рисунке не изменяются. Альфа-значения изменяются только во время подготовки к просмотру.

В следующем примере показано, как изменить альфа-значения отдельных пикселов. Код в примере фактически изменяет альфа-информацию в объекте [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) . Этот подход намного медленнее, чем использование матрицы цветов и объекта [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) , но позволяет управлять отдельными пикселями в точечном рисунке.


```
INT iWidth = bitmap.GetWidth();
INT iHeight = bitmap.GetHeight();
Color color, colorTemp;
for(INT iRow = 0; iRow < iHeight; iRow++)
{
   for(INT iColumn = 0; iColumn < iWidth; iColumn++)
   {
      bitmap.GetPixel(iColumn, iRow, &color);
      colorTemp.SetValue(color.MakeARGB(
         (BYTE)(255 * iColumn / iWidth), 
         color.GetRed(),
         color.GetGreen(),
         color.GetBlue()));
      bitmap.SetPixel(iColumn, iRow, colorTemp);
   }
}
// First draw a wide black line.
Pen pen(Color(255, 0, 0, 0), 25);
graphics.DrawLine(&pen, 10, 35, 200, 35);
// Now draw the modified bitmap.
graphics.DrawImage(&bitmap, 30, 0, iWidth, iHeight);
```



На следующем рисунке показан полученный рисунок.

![Иллюстрация, показывающая, что изображение становится более непрозрачным слева направо, над черным прямоугольником](images/image3.png)

В предыдущем примере кода используются вложенные циклы для изменения альфа-значения каждого пикселя в точечном рисунке. Для каждого пикселя [**Bitmap::**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) SetPixel получает существующий цвет, [**Color:: SetValue**](/windows/desktop/api/Gdipluscolor/nf-gdipluscolor-color-setvalue) создает временный цвет, содержащий новое альфа-значение, а затем [**Bitmap::**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) /задает новый цвет. Альфа-значение задается на основе столбца точечного рисунка. В первом столбце альфа-каналу присвоено значение 0. В последнем столбце альфа-каналу присвоено значение 255. Таким образом, полученный образ поступает от полностью прозрачного (на левом краю) до полностью непрозрачного (на правом краю).

[**Bitmap::**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) [**SetPixel и Bitmap::**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) , позволяющие управлять отдельными значениями пикселей. Однако использование **Bitmap::** **SetPixel и Bitmap::** не так быстро, как использование класса [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) и структуры [**КолорМатрикс**](/windows/desktop/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) .

 

 



