---
description: Использование Windows GDI+ для рисования на принтере аналогично использованию GDI+ для рисования на экране компьютера. Для рисования на принтере получите маркер контекста устройства для принтера, а затем передайте этот обработчик графическому конструктору.
ms.assetid: a76cca57-6ed8-44cd-a9f6-f2692d14b68a
title: Отправка выходных данных GDI+ на принтер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c1c4f6c05e4918663284e6d7747952040dcddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080631"
---
# <a name="sending-gdi-output-to-a-printer"></a><span data-ttu-id="bcf65-104">Отправка выходных данных GDI+ на принтер</span><span class="sxs-lookup"><span data-stu-id="bcf65-104">Sending GDI+ Output to a Printer</span></span>

<span data-ttu-id="bcf65-105">Использование Windows GDI+ для рисования на принтере аналогично использованию GDI+ для рисования на экране компьютера.</span><span class="sxs-lookup"><span data-stu-id="bcf65-105">Using Windows GDI+ to draw on a printer is similar to using GDI+ to draw on a computer screen.</span></span> <span data-ttu-id="bcf65-106">Для рисования на принтере получите маркер контекста устройства для принтера, а затем передайте этот обработчик [**графическому**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) конструктору.</span><span class="sxs-lookup"><span data-stu-id="bcf65-106">To draw on a printer, obtain a device context handle for the printer and then pass that handle to a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor.</span></span>

<span data-ttu-id="bcf65-107">Следующее консольное приложение рисует линию, прямоугольник и эллипс на принтере с именем MyPrinter:</span><span class="sxs-lookup"><span data-stu-id="bcf65-107">The following console application draws a line, a rectangle, and an ellipse on a printer named MyPrinter:</span></span>


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



<span data-ttu-id="bcf65-108">В приведенном выше коде три команды рисования GDI+ находятся между вызовами функций [стартдок](/windows/win32/api/wingdi/nf-wingdi-startdocw) и [енддок](/windows/win32/api/wingdi/nf-wingdi-enddoc) , каждый из которых получает маркер контекста для устройства печати.</span><span class="sxs-lookup"><span data-stu-id="bcf65-108">In the preceding code, the three GDI+ drawing commands are in between calls to the [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) and [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc) functions, each of which receives the printer device context handle.</span></span> <span data-ttu-id="bcf65-109">Все команды графики между Стартдок и Енддок направляются во временный метафайл.</span><span class="sxs-lookup"><span data-stu-id="bcf65-109">All graphics commands between StartDoc and EndDoc are routed to a temporary metafile.</span></span> <span data-ttu-id="bcf65-110">После вызова Енддок драйвер принтера преобразует данные из метафайла в формат, необходимый для используемого принтера.</span><span class="sxs-lookup"><span data-stu-id="bcf65-110">After the call to EndDoc, the printer driver converts the data in the metafile into the format required by the specific printer being used.</span></span>

> [!Note]  
> <span data-ttu-id="bcf65-111">Если для используемого принтера не включена буферизация, выходные данные графики не направляются в метафайл.</span><span class="sxs-lookup"><span data-stu-id="bcf65-111">If spooling is not enabled for the printer being used, the graphics output is not routed to a metafile.</span></span> <span data-ttu-id="bcf65-112">Вместо этого отдельные графические команды обрабатываются драйвером принтера, а затем отправляются на принтер.</span><span class="sxs-lookup"><span data-stu-id="bcf65-112">Instead, individual graphics commands are processed by the printer driver and then sent to the printer.</span></span>

 

<span data-ttu-id="bcf65-113">Обычно не требуется жестко кодировать имя принтера, как было сделано в предыдущем консольном приложении.</span><span class="sxs-lookup"><span data-stu-id="bcf65-113">Generally you won't want to hard-code the name of a printer as was done in the preceding console application.</span></span> <span data-ttu-id="bcf65-114">Одной из альтернатив для жесткого кодирования имени является вызов [жетдефаултпринтер](../printdocs/getdefaultprinter.md) для получения имени принтера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bcf65-114">One alternative to hard-coding the name is to call [GetDefaultPrinter](../printdocs/getdefaultprinter.md) to obtain the name of the default printer.</span></span> <span data-ttu-id="bcf65-115">Перед вызовом Жетдефаултпринтер необходимо выделить буфер, достаточно большой для хранения имени принтера.</span><span class="sxs-lookup"><span data-stu-id="bcf65-115">Before you call GetDefaultPrinter, you must allocate a buffer large enough to hold the printer name.</span></span> <span data-ttu-id="bcf65-116">Размер требуемого буфера можно определить путем вызова Жетдефаултпринтер, передав **значение NULL** в качестве первого аргумента.</span><span class="sxs-lookup"><span data-stu-id="bcf65-116">You can determine the size of the required buffer by calling GetDefaultPrinter, passing **NULL** as the first argument.</span></span>

> [!Note]  
> <span data-ttu-id="bcf65-117">Функция [жетдефаултпринтер](../printdocs/getdefaultprinter.md) поддерживается только в Windows 2000 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="bcf65-117">The [GetDefaultPrinter](../printdocs/getdefaultprinter.md) function is supported only on Windows 2000 and later.</span></span>

 

<span data-ttu-id="bcf65-118">Следующее консольное приложение получает имя принтера по умолчанию, а затем рисует прямоугольник и эллипс на этом принтере.</span><span class="sxs-lookup"><span data-stu-id="bcf65-118">The following console application gets the name of the default printer and then draws a rectangle and an ellipse on that printer.</span></span> <span data-ttu-id="bcf65-119">[**Graphics::D вызов равректангле**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) между вызовами [StartPage](/windows/win32/api/wingdi/nf-wingdi-startpage) и [EndPage](/windows/win32/api/wingdi/nf-wingdi-endpage), поэтому прямоугольник находится на отдельной странице.</span><span class="sxs-lookup"><span data-stu-id="bcf65-119">The [**Graphics::DrawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) call is in between calls to [StartPage](/windows/win32/api/wingdi/nf-wingdi-startpage) and [EndPage](/windows/win32/api/wingdi/nf-wingdi-endpage), so the rectangle is on a page by itself.</span></span> <span data-ttu-id="bcf65-120">Аналогичным образом, эллипс находится на отдельной странице.</span><span class="sxs-lookup"><span data-stu-id="bcf65-120">Similarly, the ellipse is on a page by itself.</span></span>


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



 

 
