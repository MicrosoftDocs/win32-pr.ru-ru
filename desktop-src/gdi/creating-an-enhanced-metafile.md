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
# <a name="creating-an-enhanced-metafile"></a>Создание расширенного метафайла

Этот раздел содержит пример, демонстрирующий создание расширенного метафайла, который хранится на диске, используя имя файла, указанное пользователем.

В примере используется контекст устройства для окна приложения в качестве контекста устройства ссылки. (Система сохраняет данные о разрешении для этого устройства в заголовке расширенного метафайла.) Приложение получает маркер, идентифицирующий этот контекст устройства, вызывая функцию [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) .

В примере используются измерения клиентской области приложения для определения размеров рамки изображения. Используя размеры прямоугольника, возвращаемые функцией [**жетклиентрект**](/windows/win32/api/winuser/nf-winuser-getclientrect) , приложение преобразует единицы устройства в единицы .01-миллиметры и передает преобразованные значения в функцию [**креатинхметафиле**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) .

В этом примере отображается диалоговое окно **Сохранить как** общее, которое позволяет пользователю указать имя файла нового расширенного метафайла. Система добавляет расширение EMF из трех символов в это имя файла и передает имя в функцию [**креатинхметафиле**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) .

В примере также внедряется текстовое описание изображения в заголовке расширенного метафайла. Это описание указывается в виде ресурса в таблице строк файла ресурсов приложения. Однако в работающем приложении эта строка будет извлекаться из пользовательского элемента управления в общем диалоговом окне или в отдельном диалоговом окне, выводимом исключительно для этой цели.


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



 

 
