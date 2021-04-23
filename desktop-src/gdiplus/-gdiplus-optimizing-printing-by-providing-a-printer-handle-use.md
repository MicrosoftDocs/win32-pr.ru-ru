---
description: Один из конструкторов для класса Graphics получает маркер контекста устройства и маркер принтера.
ms.assetid: 9be67cb2-4bf9-4758-af03-7d92dd04feaf
title: Оптимизация печати через дескриптор принтера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a247af3de037e220432c424c408b4055690ff861
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984445"
---
# <a name="optimizing-printing-by-providing-a-printer-handle"></a><span data-ttu-id="4d412-103">Оптимизация печати через дескриптор принтера</span><span class="sxs-lookup"><span data-stu-id="4d412-103">Optimizing Printing by Providing a Printer Handle</span></span>

<span data-ttu-id="4d412-104">Один из конструкторов для класса [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) получает маркер контекста устройства и маркер принтера.</span><span class="sxs-lookup"><span data-stu-id="4d412-104">One of the constructors for the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class receives a device context handle and a printer handle.</span></span> <span data-ttu-id="4d412-105">При отправке команд Windows GDI+ на определенные принтеры PostScript производительность будет выше, если вы создадите **графический** объект с этим конкретным конструктором.</span><span class="sxs-lookup"><span data-stu-id="4d412-105">When you send Windows GDI+ commands to certain PostScript printers, the performance will be better if you create your **Graphics** object with that particular constructor.</span></span>

<span data-ttu-id="4d412-106">Следующее консольное приложение вызывает [жетдефаултпринтер](../printdocs/getdefaultprinter.md) , чтобы получить имя принтера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4d412-106">The following console application calls [GetDefaultPrinter](../printdocs/getdefaultprinter.md) to get the name of the default printer.</span></span> <span data-ttu-id="4d412-107">Код передает имя принтера в [креатедк](/windows/win32/api/wingdi/nf-wingdi-createdcw) , чтобы получить маркер контекста устройства для принтера.</span><span class="sxs-lookup"><span data-stu-id="4d412-107">The code passes the printer name to [CreateDC](/windows/win32/api/wingdi/nf-wingdi-createdcw) to obtain a device context handle for the printer.</span></span> <span data-ttu-id="4d412-108">Код также передает имя принтера в [опенпринтер](../printdocs/openprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="4d412-108">The code also passes the printer name to [OpenPrinter](../printdocs/openprinter.md) to obtain a printer handle.</span></span> <span data-ttu-id="4d412-109">Маркер контекста устройства и маркер принтера передаются в конструктор [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="4d412-109">Both the device context handle and the printer handle are passed to the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor.</span></span> <span data-ttu-id="4d412-110">Затем на принтере рисуются две фигуры.</span><span class="sxs-lookup"><span data-stu-id="4d412-110">Then two figures are drawn on the printer.</span></span>

> [!Note]  
> <span data-ttu-id="4d412-111">Функция [жетдефаултпринтер](../printdocs/getdefaultprinter.md) поддерживается только в Windows 2000 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="4d412-111">The [GetDefaultPrinter](../printdocs/getdefaultprinter.md) function is supported only on Windows 2000 and later.</span></span>

 


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

   DWORD   size;
   HDC     hdcPrint;
   HANDLE  printerHandle;

   DOCINFO docInfo;
   ZeroMemory(&docInfo, sizeof(docInfo));
   docInfo.cbSize = sizeof(docInfo);
   docInfo.lpszDocName = "GdiplusPrint";

   // Get the length of the printer name.
   GetDefaultPrinter(NULL, &size);
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

      // Get a printer handle.
      OpenPrinter(buffer, &printerHandle, NULL);

      StartDoc(hdcPrint, &docInfo);
      StartPage(hdcPrint);
         Graphics* graphics = new Graphics(hdcPrint, printerHandle);
         Pen* pen = new Pen(Color(255, 0, 0, 0));
         graphics->DrawRectangle(pen, 200, 500, 200, 150);
         graphics->DrawEllipse(pen, 200, 500, 200, 150);
         delete(pen);
         delete(graphics);
      EndPage(hdcPrint);
      EndDoc(hdcPrint);

      ClosePrinter(printerHandle);
      DeleteDC(hdcPrint);
   }

   delete buffer;
   
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
