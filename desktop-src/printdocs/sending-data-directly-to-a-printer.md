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
# <a name="how-to-send-data-directly-to-a-gdi-printer"></a><span data-ttu-id="350c6-103">Руководство. Отправка данных непосредственно на принтер GDI</span><span class="sxs-lookup"><span data-stu-id="350c6-103">How To: Send Data Directly to a GDI Printer</span></span>

<span data-ttu-id="350c6-104">В примере кода ниже в этом разделе показано, как отправить данные управления принтером непосредственно на принтеры, использующие драйверы принтера на основе GDI.</span><span class="sxs-lookup"><span data-stu-id="350c6-104">The code sample later in this topic shows how to send printer control data directly to printers that use GDI-based printer drivers.</span></span>

<span data-ttu-id="350c6-105">Следующие шаги описывают, как отправить данные непосредственно на принтер.</span><span class="sxs-lookup"><span data-stu-id="350c6-105">The following steps describe how to send data directly to a printer.</span></span> <span data-ttu-id="350c6-106">Эти шаги также иллюстрируются в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="350c6-106">These steps are also illustrated in the code example that follows.</span></span>

1.  <span data-ttu-id="350c6-107">Вызовите [**опенпринтер**](openprinter.md) , чтобы получить маркер принтера.</span><span class="sxs-lookup"><span data-stu-id="350c6-107">Call [**OpenPrinter**](openprinter.md) to get a handle to the printer.</span></span>
2.  <span data-ttu-id="350c6-108">Инициализируйте структуру [**доЦинфо**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) с данными принтера.</span><span class="sxs-lookup"><span data-stu-id="350c6-108">Initialize a [**DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) structure with the printer data.</span></span>
3.  <span data-ttu-id="350c6-109">Вызовите [**стартдокпринтер**](startdocprinter.md) , чтобы указать, что приложение будет отправлять данные документа на принтер.</span><span class="sxs-lookup"><span data-stu-id="350c6-109">Call [**StartDocPrinter**](startdocprinter.md) to indicate that the application will be sending document data to the printer.</span></span>
4.  <span data-ttu-id="350c6-110">Вызовите [**стартпажепринтер**](startpageprinter.md) , чтобы указать, что приложение будет отправлять на принтер новую страницу.</span><span class="sxs-lookup"><span data-stu-id="350c6-110">Call [**StartPagePrinter**](startpageprinter.md) to indicate that the application will be sending a new page to the printer.</span></span>
5.  <span data-ttu-id="350c6-111">Вызовите [**вритепринтер**](writeprinter.md) , чтобы отправить данные.</span><span class="sxs-lookup"><span data-stu-id="350c6-111">Call [**WritePrinter**](writeprinter.md) to send the data.</span></span>
6.  <span data-ttu-id="350c6-112">Вызовите [**ендпажепринтер**](endpageprinter.md) , чтобы указать, что все данные для текущей страницы отправлены.</span><span class="sxs-lookup"><span data-stu-id="350c6-112">Call [**EndPagePrinter**](endpageprinter.md) to indicate that all data for the current page has been sent.</span></span>
7.  <span data-ttu-id="350c6-113">Вызовите [**енддокпринтер**](enddocprinter.md) , чтобы указать, что все данные для этого документа отправлены.</span><span class="sxs-lookup"><span data-stu-id="350c6-113">Call [**EndDocPrinter**](enddocprinter.md) to indicate that all data for this document has been sent.</span></span>
8.  <span data-ttu-id="350c6-114">Вызовите [**клосепринтер**](closeprinter.md) , чтобы освободить ресурсы.</span><span class="sxs-lookup"><span data-stu-id="350c6-114">Call [**ClosePrinter**](closeprinter.md) to release the resources.</span></span>

<span data-ttu-id="350c6-115">Отправляйте данные управления принтером непосредственно на принтеры, использующие драйверы принтеров на основе GDI.</span><span class="sxs-lookup"><span data-stu-id="350c6-115">Send printer control data directly to printers that use GDI-based printer drivers.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="350c6-116">См. также</span><span class="sxs-lookup"><span data-stu-id="350c6-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="350c6-117">**клосепринтер**</span><span class="sxs-lookup"><span data-stu-id="350c6-117">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="350c6-118">**енддокпринтер**</span><span class="sxs-lookup"><span data-stu-id="350c6-118">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="350c6-119">**ендпажепринтер**</span><span class="sxs-lookup"><span data-stu-id="350c6-119">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="350c6-120">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="350c6-120">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="350c6-121">**стартдокпринтер**</span><span class="sxs-lookup"><span data-stu-id="350c6-121">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="350c6-122">**стартпажепринтер**</span><span class="sxs-lookup"><span data-stu-id="350c6-122">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="350c6-123">**вритепринтер**</span><span class="sxs-lookup"><span data-stu-id="350c6-123">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 
