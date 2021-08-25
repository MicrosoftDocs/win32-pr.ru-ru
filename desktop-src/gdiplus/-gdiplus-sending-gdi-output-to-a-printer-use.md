---
description: использование Windows GDI+ для рисования на принтере аналогично использованию GDI+ для рисования на экране компьютера. Для рисования на принтере получите маркер контекста устройства для принтера, а затем передайте этот обработчик графическому конструктору.
ms.assetid: a76cca57-6ed8-44cd-a9f6-f2692d14b68a
title: Отправка выходных данных GDI+ на принтер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51116e27f3ef4e457d2d3cf8d39b26c1a5e2275da4b964bd4de58ec273db1e2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943784"
---
# <a name="sending-gdi-output-to-a-printer"></a>Отправка выходных данных GDI+ на принтер

использование Windows GDI+ для рисования на принтере аналогично использованию GDI+ для рисования на экране компьютера. Для рисования на принтере получите маркер контекста устройства для принтера, а затем передайте этот обработчик [**графическому**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) конструктору.

Следующее консольное приложение рисует линию, прямоугольник и эллипс на принтере с именем MyPrinter:


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   // Get a device context for the printer.
   HDC hdcPrint = CreateDC(NULL, TEXT("\\\\printserver\\print1"), NULL, NULL);

   DOCINFO docInfo;
   ZeroMemory(&docInfo, sizeof(docInfo));
   docInfo.cbSize = sizeof(docInfo);
   docInfo.lpszDocName = "GdiplusPrint";

   StartDoc(hdcPrint, &docInfo);
   StartPage(hdcPrint);
      Graphics* graphics = new Graphics(hdcPrint);
      Pen* pen = new Pen(Color(255, 0, 0, 0));
      graphics->DrawLine(pen, 50, 50, 350, 550);
      graphics->DrawRectangle(pen, 50, 50, 300, 500);
      graphics->DrawEllipse(pen, 50, 50, 300, 500);
      delete pen;
      delete graphics;
   EndPage(hdcPrint);
   EndDoc(hdcPrint);
   
   DeleteDC(hdcPrint);
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



в приведенном выше коде три команды рисования GDI+ находятся между вызовами функций [стартдок](/windows/win32/api/wingdi/nf-wingdi-startdocw) и [енддок](/windows/win32/api/wingdi/nf-wingdi-enddoc) , каждый из которых получает маркер контекста для устройства печати. Все команды графики между Стартдок и Енддок направляются во временный метафайл. После вызова Енддок драйвер принтера преобразует данные из метафайла в формат, необходимый для используемого принтера.

> [!Note]  
> Если для используемого принтера не включена буферизация, выходные данные графики не направляются в метафайл. Вместо этого отдельные графические команды обрабатываются драйвером принтера, а затем отправляются на принтер.

 

Обычно не требуется жестко кодировать имя принтера, как было сделано в предыдущем консольном приложении. Одной из альтернатив для жесткого кодирования имени является вызов [жетдефаултпринтер](../printdocs/getdefaultprinter.md) для получения имени принтера по умолчанию. Перед вызовом Жетдефаултпринтер необходимо выделить буфер, достаточно большой для хранения имени принтера. Размер требуемого буфера можно определить путем вызова Жетдефаултпринтер, передав **значение NULL** в качестве первого аргумента.

> [!Note]  
> функция [жетдефаултпринтер](../printdocs/getdefaultprinter.md) поддерживается только в Windows 2000 и более поздних версиях.

 

Следующее консольное приложение получает имя принтера по умолчанию, а затем рисует прямоугольник и эллипс на этом принтере. [**Graphics::D вызов равректангле**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) между вызовами [StartPage](/windows/win32/api/wingdi/nf-wingdi-startpage) и [EndPage](/windows/win32/api/wingdi/nf-wingdi-endpage), поэтому прямоугольник находится на отдельной странице. Аналогичным образом, эллипс находится на отдельной странице.


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   DWORD size;
   HDC hdcPrint;

   DOCINFO docInfo;
   ZeroMemory(&docInfo, sizeof(docInfo));
   docInfo.cbSize = sizeof(docInfo);
   docInfo.lpszDocName = "GdiplusPrint";

   // Get the size of the default printer name.
   GetDefaultPrinter(NULL, &size);

   // Allocate a buffer large enough to hold the printer name.
   TCHAR* buffer = new TCHAR[size];

   // Get the printer name.
   if(!GetDefaultPrinter(buffer, &size))
   {
      printf("Failure");
   }
   else
   {
      // Get a device context for the printer.
      hdcPrint = CreateDC(NULL, buffer, NULL, NULL);

      StartDoc(hdcPrint, &docInfo);
         Graphics* graphics;
         Pen* pen = new Pen(Color(255, 0, 0, 0));

         StartPage(hdcPrint);
            graphics = new Graphics(hdcPrint);
            graphics->DrawRectangle(pen, 50, 50, 200, 300);
            delete graphics;
         EndPage(hdcPrint);

         StartPage(hdcPrint);
            graphics = new Graphics(hdcPrint);
            graphics->DrawEllipse(pen, 50, 50, 200, 300);
            delete graphics;
         EndPage(hdcPrint);

         delete pen;
      EndDoc(hdcPrint);

      DeleteDC(hdcPrint);
   }

   delete buffer;

   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
