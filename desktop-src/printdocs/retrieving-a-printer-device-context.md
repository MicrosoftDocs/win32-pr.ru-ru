---
description: В этом разделе описывается, как получить контекст печатающего устройства.
ms.assetid: b3eb9c48-f4c4-42f1-b189-1fa42670008e
title: Как получить контекст печатающего устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f723ece0e00d58ed684029e0eb3202d637443bd7f0e9d8878024346b9d79ba9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600564"
---
# <a name="how-to-retrieve-a-printer-device-context"></a>Как получить контекст печатающего устройства

В этом разделе описывается, как получить контекст печатающего устройства. Контекст печатающего устройства можно получить, вызвав функцию [**креатедк**](/windows/desktop/api/wingdi/nf-wingdi-createdca) напрямую или выполнив общее диалоговое окно **Печать** .

При отображении общего диалогового окна « **Печать** » пользователь сможет выбрать принтер, страницы документа и число копий документов, которые нужно напечатать. Диалоговое окно « **Печать** общего» возвращает эти варианты в структуре данных.

В этом разделе описывается, как получить контекст печатающего устройства с помощью следующих методов.

-   [Вызов Креатедк](#call-createdc)
-   [Отображение общего диалогового окна «Печать»](#display-a-print-common-dialog-box)
    -   [Использование функции Принтдлжекс](#using-the-printdlgex-function)
    -   [Использование функции Принтдлг](#using-the-printdlg-function)

## <a name="call-createdc"></a>Вызов Креатедк

Если известно устройство, на которое нужно выполнить печать, можно вызвать [**креатедк**](/windows/desktop/api/wingdi/nf-wingdi-createdca) и передать эту информацию непосредственно в функцию. **Креатедк** Возвращает контекст устройства, в котором можно визуализировать содержимое для печати.

Самый простой вызов для получения контекста устройства показан в следующем примере кода. Код в этом примере извлекает контекст устройства для устройства вывода по умолчанию.


```C++
    hDC = CreateDC(TEXT("DISPLAY"),NULL,NULL,NULL);
```



Чтобы подготовиться к просмотру на определенном принтере, необходимо указать "ВИНСПУЛ" в качестве устройства и передать правильное имя принтера в [**креатедк**](/windows/desktop/api/wingdi/nf-wingdi-createdca). Можно также передать структуру [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) в вызове **креатедк** , если вы хотите предоставить данные инициализации для драйвера устройства при создании контекста устройства.

В следующем примере показан вызов [**креатедк**](/windows/desktop/api/wingdi/nf-wingdi-createdca) , в котором выбран драйвер "винспул", а имя принтера указано по имени.


```C++
    printerDC = CreateDC( L"WINSPOOL", printerName, NULL, NULL);
```



Вы можете получить точную строку имени принтера для передачи в [**креатедк**](/windows/desktop/api/wingdi/nf-wingdi-createdca) , вызвав функцию [**енумпринтерс**](enumprinters.md) . В следующем примере кода показано, как вызвать **енумпринтерс** и получить имена локальных и локально подключенных принтеров. Так как размер требуемого буфера не может быть заранее известен, **енумпринтерс** вызывается два раза. Первый вызов возвращает размер требуемого буфера. Эта информация используется для выделения буфера требуемого размера, а второй вызов **енумпринтерс** возвращает необходимые данные.


```C++
    fnReturn = EnumPrinters(
                PRINTER_ENUM_LOCAL | PRINTER_ENUM_CONNECTIONS,
                NULL,
                1L,                // printer info level
                (LPBYTE)NULL,
                0L,
                &dwNeeded,
                &dwReturned);
    
    if (dwNeeded > 0)
    {
        pInfo = (PRINTER_INFO_1 *)HeapAlloc(
                    GetProcessHeap(), 0L, dwNeeded);
    }

    if (NULL != pInfo)
    {
        dwReturned = 0;
        fnReturn = EnumPrinters(
                PRINTER_ENUM_LOCAL | PRINTER_ENUM_CONNECTIONS,
                NULL,
                1L,                // printer info level
                (LPBYTE)pInfo,
                dwNeeded,
                &dwNeeded,
                &dwReturned);
    }

    if (fnReturn)
    {
        // Review the information from all the printers
        //  returned by EnumPrinters.
        for (i=0; i < dwReturned; i++)
        {
            // pThisInfo[i]->pName contains the printer
            //  name to use in the CreateDC function call.
            //
            // When this desired printer is found in the list of
            //  returned printer, set the printerName value to 
            //  use in the call to CreateDC.

            // printerName = pThisInfo[i]->pName
        }
    }
```



## <a name="display-a-print-common-dialog-box"></a>Отображение общего диалогового окна «Печать»

Можно выбрать один из двух общих диалоговых окон **печати** для отображения пользователю. новое диалоговое окно, которое можно отобразить, вызвав функцию [**принтдлжекс**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) и диалоговое окно старого стиля, которое можно отобразить, вызвав функцию [**принтдлг**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) . В следующих разделах описывается вызов каждого диалогового окна из приложения.

### <a name="using-the-printdlgex-function"></a>Использование функции Принтдлжекс

Вызовите функцию [**принтдлжекс**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) для отображения страницы свойств **Печать** . С помощью страницы свойств пользователь может указать сведения о задании печати. Например, пользователь может выбрать диапазон страниц для печати, число копий и т. д. **Принтдлжекс** также может получить маркер для контекста устройства для выбранного принтера. Вы можете использовать этот маркер для отрисовки выходных данных на принтере.

Пример кода, иллюстрирующий использование [**принтдлжекс**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) для получения контекста печатающего устройства, см. в разделе «Использование страницы свойств печати» раздела « [использование общих диалоговых](../dlgbox/using-common-dialog-boxes.md)окон».

### <a name="using-the-printdlg-function"></a>Использование функции Принтдлг

если приложение должно выполняться в системе, которая не поддерживает функцию [**принтдлжекс**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) , например в системе, где используется версия Windows более ранней, чем Windows 2000, или не требуются дополнительные функции, предоставляемые функцией **принтдлжекс** , используйте функцию [**принтдлг**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) . В следующих шагах описывается, как отобразить диалоговое окно "Общие" для **печати** старого стиля.

1.  Инициализируйте структуру данных [**принтдлг**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .
2.  Вызовите [**принтдлг**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) , чтобы отобразить для пользователя общее диалоговое окно **печати** .
3.  Если вызов [**принтдлг**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) возвращает **значение true**, блокирует возвращенную память структуры [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) . Если вызов **принтдлг** возвращает **значение false**, пользователь нажал кнопку **Отмена** в диалоговом окне **Печать** общего, чтобы больше не обрабатываться.
4.  Выделите буфер локальной памяти, достаточно большой для хранения копии структуры [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .
5.  Скопируйте возвращенную структуру [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) в локально выделенный.
6.  Сохраните другие сведения, возвращаемые в структуре [**принтдлг**](/windows/win32/api/commdlg/ns-commdlg-printdlga) , и необходимо обработать задание печати.
7.  Освободите [**принтдлг**](/windows/win32/api/commdlg/ns-commdlg-printdlga) и буферы памяти, на которые он ссылается.

В следующем примере кода показано, как использовать функцию [**принтдлг**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) для получения контекста устройства и имени выбранного принтера.


```C++
// Display the printer dialog box so the user can select the 
//  printer and the number of copies to print.
BOOL            printDlgReturn = FALSE;
HDC                printerDC = NULL;
PRINTDLG        printDlgInfo = {0};
LPWSTR            localPrinterName = NULL;
PDEVMODE        returnedDevmode = NULL;
PDEVMODE        localDevmode = NULL;
int                localNumberOfCopies = 0;

// Initialize the print dialog box's data structure.
printDlgInfo.lStructSize = sizeof( printDlgInfo );
printDlgInfo.Flags = 
    // Return a printer device context.
    PD_RETURNDC 
    // Don't allow separate print to file.
    // Remove these flags if you want to support this feature.
    | PD_HIDEPRINTTOFILE        
    | PD_DISABLEPRINTTOFILE 
    // Don't allow selecting individual document pages to print.
    // Remove this flag if you want to support this feature.
    | PD_NOSELECTION;

// Display the printer dialog and retrieve the printer DC.
printDlgReturn = PrintDlg(&printDlgInfo);

// Check the return value.
if (TRUE == printDlgReturn)
{
    // The user clicked OK so the printer dialog box data 
    //  structure was returned with the user's selections.
    //  Copy the relevant data from the data structure and 
    //  save them to a local data structure.

    //
    // Get the HDC of the selected printer
    printerDC = printDlgInfo.hDC;
    
    // In this example, the DEVMODE structure returned by 
    //    the printer dialog box is copied to a local memory
    //    block and a pointer to the printer name that is 
    //    stored in the copied DEVMODE structure is saved.

    //
    //  Lock the handle to get a pointer to the DEVMODE structure.
    returnedDevmode = (PDEVMODE)GlobalLock(printDlgInfo.hDevMode);

    localDevmode = (LPDEVMODE)HeapAlloc(
                        GetProcessHeap(), 
                        HEAP_ZERO_MEMORY | HEAP_GENERATE_EXCEPTIONS, 
                        returnedDevmode->dmSize);

    if (NULL != localDevmode) 
    {
        memcpy(
            (LPVOID)localDevmode,
            (LPVOID)returnedDevmode, 
            returnedDevmode->dmSize);

        // Save the printer name from the DEVMODE structure.
        //  This is done here just to illustrate how to access
        //  the name field. The printer name can also be accessed
        //  by referring to the dmDeviceName in the local 
        //  copy of the DEVMODE structure.
        localPrinterName = localDevmode->dmDeviceName;

        // Save the number of copies as entered by the user
        localNumberOfCopies = printDlgInfo.nCopies;    
    }
    else
    {
        // Unable to allocate a new structure so leave
        //  the pointer as NULL to indicate that it's empty.
    }

    // Free the DEVMODE structure returned by the print 
    //  dialog box.
    if (NULL != printDlgInfo.hDevMode) 
    {
        GlobalFree(printDlgInfo.hDevMode);
    }
}
else
{
    // The user cancelled out of the print dialog box.
}
```



Дополнительные сведения о функции [**принтдлг**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) см. в разделе "Отображение диалогового окна печати" раздела [использование общих диалоговых](../dlgbox/using-common-dialog-boxes.md)окон.

 

 
