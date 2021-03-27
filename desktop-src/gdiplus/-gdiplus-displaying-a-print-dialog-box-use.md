---
description: Одним из способов получения маркера контекста устройства для принтера является отображение диалогового окна Печать и предоставление пользователю возможности выбора принтера.
ms.assetid: 73a74186-c916-4ad9-b768-6bc887fd5231
title: Отображение диалогового окна «Печать»
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b0d40365c36e3e554812ff137475ab7c6405e91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997506"
---
# <a name="displaying-a-print-dialog-box"></a><span data-ttu-id="30a7e-103">Отображение диалогового окна «Печать»</span><span class="sxs-lookup"><span data-stu-id="30a7e-103">Displaying a Print Dialog Box</span></span>

<span data-ttu-id="30a7e-104">Одним из способов получения маркера контекста устройства для принтера является отображение диалогового окна Печать и предоставление пользователю возможности выбора принтера.</span><span class="sxs-lookup"><span data-stu-id="30a7e-104">One way to get a device context handle for a printer is to display a print dialog box and allow the user to choose a printer.</span></span> <span data-ttu-id="30a7e-105">Функция [принтдлг](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) (которая отображает диалоговое окно) имеет один параметр, который является адресом структуры [принтдлг](/windows/win32/api/commdlg/ns-commdlg-printdlga?redirectedfrom=MSDN) .</span><span class="sxs-lookup"><span data-stu-id="30a7e-105">The [PrintDlg](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function (which displays the dialog box) has one parameter that is the address of a [PRINTDLG](/windows/win32/api/commdlg/ns-commdlg-printdlga?redirectedfrom=MSDN) structure.</span></span> <span data-ttu-id="30a7e-106">Структура ПРИНТДЛГ имеет несколько членов, но большинство из них можно оставить в качестве значений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="30a7e-106">The PRINTDLG structure has several members, but you can leave most of them set to their default values.</span></span> <span data-ttu-id="30a7e-107">Необходимо задать два члена — **лструктсизе** и **flags**.</span><span class="sxs-lookup"><span data-stu-id="30a7e-107">The two members you need to set are **lStructSize** and **Flags**.</span></span> <span data-ttu-id="30a7e-108">Задайте для **лструктсизе** размер переменной принтдлг и установите **Флаги** PD \_ ретурндк.</span><span class="sxs-lookup"><span data-stu-id="30a7e-108">Set **lStructSize** to the size of a PRINTDLG variable, and set **Flags** to PD\_RETURNDC.</span></span> <span data-ttu-id="30a7e-109">Установка **флагов** для PC \_ ретурндк указывает, что необходимо, чтобы функция принтдлг заполнила поле **HDC** с помощью маркера контекста устройства для принтера, выбранного пользователем.</span><span class="sxs-lookup"><span data-stu-id="30a7e-109">Setting **Flags** to PC\_RETURNDC specifies that you want the PrintDlg function to fill the **hDC** field with a device context handle for the printer chosen by the user.</span></span>


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
   
   DOCINFO docInfo;
   ZeroMemory(&docInfo, sizeof(docInfo));
   docInfo.cbSize = sizeof(docInfo);
   docInfo.lpszDocName = "GdiplusPrint";
   
   // Create a PRINTDLG structure, and initialize the appropriate fields.
   PRINTDLG printDlg;
   ZeroMemory(&printDlg, sizeof(printDlg));
   printDlg.lStructSize = sizeof(printDlg);
   printDlg.Flags = PD_RETURNDC;
   
   // Display a print dialog box.
   if(!PrintDlg(&printDlg))
   {
      printf("Failure\n");
   }
   else
   {
      // Now that PrintDlg has returned, a device context handle
      // for the chosen printer is in printDlg->hDC.
      
      StartDoc(printDlg.hDC, &docInfo);
      StartPage(printDlg.hDC);
         Graphics* graphics = new Graphics(printDlg.hDC);
         Pen* pen = new Pen(Color(255, 0, 0, 0));
         graphics->DrawRectangle(pen, 200, 500, 200, 150);
         graphics->DrawEllipse(pen, 200, 500, 200, 150);
         graphics->DrawLine(pen, 200, 500, 400, 650);
         delete pen;
         delete graphics;
      EndPage(printDlg.hDC);
      EndDoc(printDlg.hDC); 
   }
   if(printDlg.hDevMode) 
      GlobalFree(printDlg.hDevMode);
   if(printDlg.hDevNames) 
      GlobalFree(printDlg.hDevNames);
   if(printDlg.hDC)
      DeleteDC(printDlg.hDC);
   
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
