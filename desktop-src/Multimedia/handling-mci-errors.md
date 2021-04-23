---
title: Обработка ошибок MCI
description: Обработка ошибок MCI
ms.assetid: 01a2ff95-34a2-434f-9c7e-d0cdac826c02
keywords:
- Функция МЦисендкомманд
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab8412c74153d5ddfb03a3aff895f9f2e0e73798
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105672259"
---
# <a name="handling-mci-errors"></a><span data-ttu-id="f835e-104">Обработка ошибок MCI</span><span class="sxs-lookup"><span data-stu-id="f835e-104">Handling MCI Errors</span></span>

<span data-ttu-id="f835e-105">Всегда следует проверять возвращаемое значение функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f835e-105">You should always check the return value of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span> <span data-ttu-id="f835e-106">Если он указывает на ошибку, можно использовать [**мЦижетеррорстринг**](/previous-versions//dd757158(v=vs.85)) для получения текстового описания ошибки.</span><span class="sxs-lookup"><span data-stu-id="f835e-106">If it indicates an error, you can use [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) to get a textual description of the error.</span></span>

<span data-ttu-id="f835e-107">В следующем примере код ошибки MCI, указанный параметром *дверрор* , передается в **мЦижетеррорстринг**, а затем выводится полученное текстовое описание ошибки с помощью функции [MessageBox](/windows/win32/api/winuser/nf-winuser-messagebox) .</span><span class="sxs-lookup"><span data-stu-id="f835e-107">The following example passes the MCI error code specified by *dwError* to **mciGetErrorString**, and then displays the resulting textual error description using the [MessageBox](/windows/win32/api/winuser/nf-winuser-messagebox) function.</span></span>


```C++
// Use mciGetErrorString to get a textual description of an MCI error.
// Display the error description using MessageBox.

void showError(DWORD dwError)
{
    char szErrorBuf[MAXERRORLENGTH];
    MessageBeep(MB_ICONEXCLAMATION);
    if(mciGetErrorString(dwError, (LPSTR) szErrorBuf, MAXERRORLENGTH))
    {
        MessageBox(hMainWnd, szErrorBuf, "MCI Error",
        MB_ICONEXCLAMATION);
    }
    else
    {
        MessageBox(hMainWnd, "Unknown Error", "MCI Error",
            MB_ICONEXCLAMATION);
    }
}
 
```



> [!Note]  
> <span data-ttu-id="f835e-108">Чтобы самостоятельно интерпретировать возвращаемое значение ошибки [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , необходимо замаскировать слово в высоком порядке (слово низкого порядка содержит код ошибки).</span><span class="sxs-lookup"><span data-stu-id="f835e-108">To interpret an [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) error return value yourself, mask the high-order word (the low-order word contains the error code).</span></span> <span data-ttu-id="f835e-109">При передаче возвращаемого значения ошибки в [**мЦижетеррорстринг**](/previous-versions//dd757158(v=vs.85))необходимо передать полное значение даублеворд.</span><span class="sxs-lookup"><span data-stu-id="f835e-109">If you pass the error return value to [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)), however, you must pass the entire doubleword value.</span></span>

 

 

 