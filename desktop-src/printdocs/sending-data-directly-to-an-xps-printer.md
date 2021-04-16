---
description: В этом разделе описывается, как отправить данные управления принтером непосредственно на принтеры, использующие драйверы принтера XPSDrv.
ms.assetid: 7e98e08a-d572-451d-befb-18fc86f0e505
title: Руководство. Отправка данных непосредственно на принтер XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d78a8c36d6862860862059f9bbcc8db25e171b19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719498"
---
# <a name="how-to-send-data-directly-to-an-xps-printer"></a>Руководство. Отправка данных непосредственно на принтер XPS

В этом разделе описывается, как отправить данные управления принтером непосредственно на принтеры, использующие драйверы принтера XPSDrv.

Следующие шаги описывают, как отправить данные непосредственно на принтер. Эти шаги также иллюстрируются в следующем примере кода.

1.  Вызовите [**опенпринтер**](openprinter.md) , чтобы получить маркер принтера.
2.  Инициализируйте структуру [**доЦинфо**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) с данными принтера.
3.  Вызовите [**стартдокпринтер**](startdocprinter.md) , чтобы указать, что приложение будет отправлять данные документа на принтер.
4.  Вызовите [**вритепринтер**](writeprinter.md) , чтобы отправить данные.
5.  Вызовите [**енддокпринтер**](enddocprinter.md) , чтобы указать, что все данные для этого документа отправлены.
6.  Вызовите [**клосепринтер**](closeprinter.md) , чтобы освободить ресурсы.

Отправляйте данные управления принтером непосредственно на принтеры, использующие драйверы принтера XPSDrv.


```C++
// 
//  RawDataToXpsPrinter - sends binary data directly to a printer 
//          with an XPSDrv Printer Driver 
//  
// szPrinterName: NULL-terminated string specifying printer name 
// lpData:        Pointer to raw data bytes 
// dwCount        Length of lpData in bytes 
//  
// Returns: TRUE for success, FALSE for failure. 
//  
BOOL RawDataToXpsPrinter (LPTSTR szPrinterName, LPBYTE lpData, DWORD dwCount)
{
    BOOL     bStatus = FALSE;
    HANDLE     hPrinter = NULL;
    DOC_INFO_1       DocInfo;
    DWORD    dwPrtJob = 0L;
    DWORD    dwBytesWritten = 0L;

    // Open a handle to the printer. 
    bStatus = OpenPrinter (szPrinterName, &hPrinter, NULL);
    
    if (bStatus) {
        // Fill in the structure with info about this "document." 
        DocInfo.pDocName = (LPTSTR)_T("My Document");
        DocInfo.pOutputFile = NULL;

        // Enter the datatype of this buffer.
        //  Use "XPS_PASS" when the data buffer should bypass the 
        //    print filter pipeline of the XPSDrv printer driver. 
        //    This datatype would be used to send the buffer directly 
        //    to the printer, such as when sending print head alignment 
        //    commands. Normally, a data buffer would be sent as the
        //    "RAW" datatype.
        //
        DocInfo.pDatatype = (LPTSTR)_T("XPS_PASS");

        dwPrtJob = StartDocPrinter (
                        hPrinter,
                        1,
                        (LPBYTE)&DocInfo);

        if (dwPrtJob > 0) {
                // Send the data to the printer. 
                bStatus = WritePrinter (
                hPrinter,
                lpData,
                dwCount,
                &dwBytesWritten);
        }
        
        EndDocPrinter (hPrinter);

        // Close the printer handle. 
        bStatus = ClosePrinter(hPrinter);
    }
    
    if (!bStatus || (dwCount != dwBytesWritten)) {
        bStatus = FALSE;
    } else {
        bStatus = TRUE;
    }

    return bStatus;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**клосепринтер**](closeprinter.md)
</dt> <dt>

[**енддокпринтер**](enddocprinter.md)
</dt> <dt>

[**ендпажепринтер**](endpageprinter.md)
</dt> <dt>

[**опенпринтер**](openprinter.md)
</dt> <dt>

[**стартдокпринтер**](startdocprinter.md)
</dt> <dt>

[**стартпажепринтер**](startpageprinter.md)
</dt> <dt>

[**вритепринтер**](writeprinter.md)
</dt> </dl>

 

 
