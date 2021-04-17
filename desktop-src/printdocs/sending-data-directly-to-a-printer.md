---
description: В примере кода ниже в этом разделе показано, как отправить данные управления принтером непосредственно на принтеры, использующие драйверы принтера на основе GDI.
ms.assetid: 321f2333-d88e-4042-b9b1-0d918b3209d4
title: Руководство. Отправка данных непосредственно на принтер GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1968b435068a62ce7a7d379a66c1500d04d8936a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719592"
---
# <a name="how-to-send-data-directly-to-a-gdi-printer"></a>Руководство. Отправка данных непосредственно на принтер GDI

В примере кода ниже в этом разделе показано, как отправить данные управления принтером непосредственно на принтеры, использующие драйверы принтера на основе GDI.

Следующие шаги описывают, как отправить данные непосредственно на принтер. Эти шаги также иллюстрируются в следующем примере кода.

1.  Вызовите [**опенпринтер**](openprinter.md) , чтобы получить маркер принтера.
2.  Инициализируйте структуру [**доЦинфо**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) с данными принтера.
3.  Вызовите [**стартдокпринтер**](startdocprinter.md) , чтобы указать, что приложение будет отправлять данные документа на принтер.
4.  Вызовите [**стартпажепринтер**](startpageprinter.md) , чтобы указать, что приложение будет отправлять на принтер новую страницу.
5.  Вызовите [**вритепринтер**](writeprinter.md) , чтобы отправить данные.
6.  Вызовите [**ендпажепринтер**](endpageprinter.md) , чтобы указать, что все данные для текущей страницы отправлены.
7.  Вызовите [**енддокпринтер**](enddocprinter.md) , чтобы указать, что все данные для этого документа отправлены.
8.  Вызовите [**клосепринтер**](closeprinter.md) , чтобы освободить ресурсы.

Отправляйте данные управления принтером непосредственно на принтеры, использующие драйверы принтеров на основе GDI.


```C++
// 
// RawDataToPrinter - sends binary data directly to a printer 
//  
// szPrinterName: NULL-terminated string specifying printer name 
// lpData:        Pointer to raw data bytes 
// dwCount        Length of lpData in bytes 
//  
// Returns: TRUE for success, FALSE for failure. 
//  
BOOL RawDataToPrinter(LPTSTR szPrinterName, LPBYTE lpData, DWORD dwCount)
{
    BOOL     bStatus = FALSE;
    HANDLE     hPrinter = NULL;
    DOC_INFO_1 DocInfo;
    DWORD      dwJob = 0L;
    DWORD      dwBytesWritten = 0L;

    // Open a handle to the printer. 
    bStatus = OpenPrinter( szPrinterName, &hPrinter, NULL );
    if (bStatus) {
        // Fill in the structure with info about this "document." 
        DocInfo.pDocName = (LPTSTR)_T("My Document");
        DocInfo.pOutputFile = NULL;
        DocInfo.pDatatype = (LPTSTR)_T("RAW");

        // Inform the spooler the document is beginning. 
        dwJob = StartDocPrinter( hPrinter, 1, (LPBYTE)&DocInfo );
        if (dwJob > 0) {
            // Start a page. 
            bStatus = StartPagePrinter( hPrinter );
            if (bStatus) {
                // Send the data to the printer. 
                bStatus = WritePrinter( hPrinter, lpData, dwCount, &dwBytesWritten);
                EndPagePrinter (hPrinter);
            }
            // Inform the spooler that the document is ending. 
            EndDocPrinter( hPrinter );
        }
        // Close the printer handle. 
        ClosePrinter( hPrinter );
    }
    // Check to see if correct number of bytes were written. 
    if (!bStatus || (dwBytesWritten != dwCount)) {
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

 

 
