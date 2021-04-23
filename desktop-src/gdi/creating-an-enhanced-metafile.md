---
description: Этот раздел содержит пример, демонстрирующий создание расширенного метафайла, который хранится на диске, используя имя файла, указанное пользователем.
ms.assetid: 084b2737-eb55-4587-b8e8-3eb3fa3688c4
title: Создание расширенного метафайла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4877481ed0a68d6379e7eaabb00bbe37cef74c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544538"
---
# <a name="creating-an-enhanced-metafile"></a><span data-ttu-id="392b3-103">Создание расширенного метафайла</span><span class="sxs-lookup"><span data-stu-id="392b3-103">Creating an Enhanced Metafile</span></span>

<span data-ttu-id="392b3-104">Этот раздел содержит пример, демонстрирующий создание расширенного метафайла, который хранится на диске, используя имя файла, указанное пользователем.</span><span class="sxs-lookup"><span data-stu-id="392b3-104">This section contains an example that demonstrates the creation of an enhanced metafile that is stored on a disk, using a file name specified by the user.</span></span>

<span data-ttu-id="392b3-105">В примере используется контекст устройства для окна приложения в качестве контекста устройства ссылки.</span><span class="sxs-lookup"><span data-stu-id="392b3-105">The example uses a device context for the application window as the reference device context.</span></span> <span data-ttu-id="392b3-106">(Система сохраняет данные о разрешении для этого устройства в заголовке расширенного метафайла.) Приложение получает маркер, идентифицирующий этот контекст устройства, вызывая функцию [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) .</span><span class="sxs-lookup"><span data-stu-id="392b3-106">(The system stores the resolution data for this device in the enhanced-metafile's header.) The application retrieves a handle identifying this device context by calling the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) function.</span></span>

<span data-ttu-id="392b3-107">В примере используются измерения клиентской области приложения для определения размеров рамки изображения.</span><span class="sxs-lookup"><span data-stu-id="392b3-107">The example uses the dimensions of the application's client area to define the dimensions of the picture frame.</span></span> <span data-ttu-id="392b3-108">Используя размеры прямоугольника, возвращаемые функцией [**жетклиентрект**](/windows/win32/api/winuser/nf-winuser-getclientrect) , приложение преобразует единицы устройства в единицы .01-миллиметры и передает преобразованные значения в функцию [**креатинхметафиле**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) .</span><span class="sxs-lookup"><span data-stu-id="392b3-108">Using the rectangle dimensions returned by the [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) function, the application converts the device units to .01-millimeter units and passes the converted values to the [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) function.</span></span>

<span data-ttu-id="392b3-109">В этом примере отображается диалоговое окно **Сохранить как** общее, которое позволяет пользователю указать имя файла нового расширенного метафайла.</span><span class="sxs-lookup"><span data-stu-id="392b3-109">The example displays a **Save As** common dialog box that enables the user to specify the file name of the new enhanced metafile.</span></span> <span data-ttu-id="392b3-110">Система добавляет расширение EMF из трех символов в это имя файла и передает имя в функцию [**креатинхметафиле**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) .</span><span class="sxs-lookup"><span data-stu-id="392b3-110">The system appends the three-character .emf extension to this file name and passes the name to the [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) function.</span></span>

<span data-ttu-id="392b3-111">В примере также внедряется текстовое описание изображения в заголовке расширенного метафайла.</span><span class="sxs-lookup"><span data-stu-id="392b3-111">The example also embeds a text description of the picture in the enhanced-metafile header.</span></span> <span data-ttu-id="392b3-112">Это описание указывается в виде ресурса в таблице строк файла ресурсов приложения.</span><span class="sxs-lookup"><span data-stu-id="392b3-112">This description is specified as a resource in the string table of the application's resource file.</span></span> <span data-ttu-id="392b3-113">Однако в работающем приложении эта строка будет извлекаться из пользовательского элемента управления в общем диалоговом окне или в отдельном диалоговом окне, выводимом исключительно для этой цели.</span><span class="sxs-lookup"><span data-stu-id="392b3-113">However, in a working application, this string would be retrieved from a custom control in a common dialog box or from a separate dialog box displayed solely for this purpose.</span></span>


```C++
// Obtain a handle to a reference device context.  
 
hdcRef = GetDC(hWnd); 
 
// Determine the picture frame dimensions.  
// iWidthMM is the display width in millimeters.  
// iHeightMM is the display height in millimeters.  
// iWidthPels is the display width in pixels.  
// iHeightPels is the display height in pixels  
 
iWidthMM = GetDeviceCaps(hdcRef, HORZSIZE); 
iHeightMM = GetDeviceCaps(hdcRef, VERTSIZE); 
iWidthPels = GetDeviceCaps(hdcRef, HORZRES); 
iHeightPels = GetDeviceCaps(hdcRef, VERTRES); 
 
// Retrieve the coordinates of the client  
// rectangle, in pixels.  
 
GetClientRect(hWnd, &rect); 
 
// Convert client coordinates to .01-mm units.  
// Use iWidthMM, iWidthPels, iHeightMM, and  
// iHeightPels to determine the number of  
// .01-millimeter units per pixel in the x-  
//  and y-directions.  
 
rect.left = (rect.left * iWidthMM * 100)/iWidthPels; 
rect.top = (rect.top * iHeightMM * 100)/iHeightPels; 
rect.right = (rect.right * iWidthMM * 100)/iWidthPels; 
rect.bottom = (rect.bottom * iHeightMM * 100)/iHeightPels; 
 
// Load the filename filter from the string table.  
 
LoadString(hInst, IDS_FILTERSTRING, 
     (LPSTR)szFilter, sizeof(szFilter)); 
 
// Replace the '%' separators that are embedded  
// between the strings in the string-table entry  
// with '\0'.  
 
for (i=0; szFilter[i]!='\0'; i++) 
    if (szFilter[i] == '%') 
            szFilter[i] = '\0'; 
 
// Load the dialog title string from the table.  
 
LoadString(hInst, IDS_TITLESTRING, 
     (LPSTR)szTitle, sizeof(szTitle)); 
 
// Initialize the OPENFILENAME members.  
 
szFile[0] = '\0'; 
 
Ofn.lStructSize = sizeof(OPENFILENAME); 
Ofn.hwndOwner = hWnd; 
Ofn.lpstrFilter = szFilter; 
Ofn.lpstrFile= szFile; 
Ofn.nMaxFile = sizeof(szFile)/ sizeof(*szFile); 
Ofn.lpstrFileTitle = szFileTitle; 
Ofn.nMaxFileTitle = sizeof(szFileTitle); 
Ofn.lpstrInitialDir = (LPSTR)NULL; 
Ofn.Flags = OFN_SHOWHELP | OFN_OVERWRITEPROMPT; 
Ofn.lpstrTitle = szTitle; 
 
// Display the Filename common dialog box. The  
// filename specified by the user is passed  
// to the CreateEnhMetaFile function and used to  
// store the metafile on disk.  
 
GetSaveFileName(&Ofn); 
 
// Load the description from the string table.  
 
LoadString(hInst, IDS_DESCRIPTIONSTRING, 
     (LPSTR)szDescription, sizeof(szDescription)); 
 
// Replace the '%' string separators that are  
// embedded between strings in the string-table  
// entry with '\0'.  
 
for (i=0; szDescription[i]!='\0'; i++) 
{
    if (szDescription[i] == '%') 
            szDescription[i] = '\0'; 
}
 
// Create the metafile device context.  
 
hdcMeta = CreateEnhMetaFile(hdcRef, 
          (LPTSTR) Ofn.lpstrFile, 
          &rect, (LPSTR)szDescription); 
 
if (!hdcMeta) 
    errhandler("CreateEnhMetaFile", hWnd); 
 
// Release the reference device context.  
 
ReleaseDC(hWnd, hdcRef); 
```



 

 
