---
title: Преобразование строк
description: Преобразование строк
ms.assetid: 40621c71-4264-40bc-b6c3-6b639d2f28fa
keywords:
- Функция mciSendString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4efeb5801c46d89686ed3fe9fcf25b311d57d4d553c220902907ac0e70a5b7e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144797"
---
# <a name="converting-strings"></a>Преобразование строк

При использовании функции [**mciSendString**](/previous-versions//dd757161(v=vs.85)) все значения, передаваемые с помощью команды и все возвращаемые значения, являются текстовыми строками, поэтому приложению требуются подпрограммы преобразования для преобразования переменных в строки или обратно. Следующий пример извлекает исходный прямоугольник и преобразует возвращенную строку в координаты прямоугольника.


```C++
BOOL GetSourceRect(LPTSTR lpstrAlias, LPRECT lprc) 
{ 
    TCHAR achRetBuff[128]; 
    TCHAR achCommandBuff[128]; 

    int result;
    MCIERROR err;
 
    // Build the command string. 
    result = _stprintf_s(
        achCommandBuff, 
        TEXT("where %s source"), 
        lpstrAlias); 

    if (result == -1)
    {
        return FALSE;
    }
    
    // Clear the RECT.
    SetRectEmpty(lprc);
 
    // Send the MCI command. 
    err = mciSendString(
        achCommandBuff, 
        achRetBuff, 
        sizeof(achRetBuff), 
        NULL);

    if (err != 0)
    {
        return FALSE;
    }
        
    // The rectangle is returned as "x y dx dy". 
    // Translate the string into the RECT structure. 

    // Warning: This example omits error checking
    // for the _tcstok_s and _tstoi functions.
    TCHAR *p; 
    TCHAR *context;

    // Left.
    p = _tcstok_s(achRetBuff, TEXT(" "), &context);
    lprc->left = _tstoi(p);

    // Top.
    p = _tcstok_s(NULL, TEXT(" "), &context);
    lprc->top = _tstoi(p);

    // Right.
    p = _tcstok_s(NULL, TEXT(" "), &context);
    lprc->right = _tstoi(p);
    
    // Bottom.
    p = _tcstok_s(NULL, TEXT(" "), &context);
    lprc->bottom = _tstoi(p);

    return TRUE;
}
 
```



> [!Note]  
> Структуры **Rect** в MCI обрабатываются по-разному, чем в других частях Windows; в MCI **правый** элемент содержит ширину прямоугольника, а **Нижний** элемент содержит его высоту. В интерфейсе строки прямоугольник задается как *x1*, *Y1*, *x2* и *Y2*. Координаты *x1* и *Y1* указывают левый верхний угол прямоугольника, а координаты *x2* и *Y2* задают ширину и высоту.

 

 

 