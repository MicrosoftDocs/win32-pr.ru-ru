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
# <a name="handling-mci-errors"></a>Обработка ошибок MCI

Всегда следует проверять возвращаемое значение функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) . Если он указывает на ошибку, можно использовать [**мЦижетеррорстринг**](/previous-versions//dd757158(v=vs.85)) для получения текстового описания ошибки.

В следующем примере код ошибки MCI, указанный параметром *дверрор* , передается в **мЦижетеррорстринг**, а затем выводится полученное текстовое описание ошибки с помощью функции [MessageBox](/windows/win32/api/winuser/nf-winuser-messagebox) .


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
> Чтобы самостоятельно интерпретировать возвращаемое значение ошибки [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , необходимо замаскировать слово в высоком порядке (слово низкого порядка содержит код ошибки). При передаче возвращаемого значения ошибки в [**мЦижетеррорстринг**](/previous-versions//dd757158(v=vs.85))необходимо передать полное значение даублеворд.

 

 

 