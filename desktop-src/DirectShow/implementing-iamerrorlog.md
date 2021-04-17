---
description: Реализация Иамеррорлог
ms.assetid: 0a380854-f3a9-4077-a481-dda67737d4c8
title: Реализация Иамеррорлог
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65eb968eb370d06fab6aca13af3215bb3b650257
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673070"
---
# <a name="implementing-iamerrorlog"></a>Реализация Иамеррорлог

\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]

Интерфейс [**иамеррорлог**](iamerrorlog.md) содержит один метод [**LogError**](iamerrorlog-logerror.md). Параметры метода содержат сведения о произошедшей ошибке.


```C++
STDMETHODIMP LogError(
    LONG Severity,          // Reserved. Do not use.
    BSTR ErrorString,       // Description.
    LONG ErrorCode,         // Error code.
    HRESULT hresult,        // HRESULT that caused the error.
    VARIANT *pExtraInfo);   // Extra information about the error.
```



Код ошибки и строка ошибки определяются службами редактирования DirectShow. Список ошибок см. в разделе [ошибки отрисовки](rendering-errors.md).

Параметр *пекстраинфо* содержит указатель на тип Variant, содержащий дополнительные сведения об ошибке. Тип данных и содержимое варианта зависит от конкретной произошедшей ошибки. Например, если ошибка вызвана неправильным именем файла, то вариант представляет собой строку с неправильным именем файла. Некоторые ошибки не имеют дополнительной информации, поэтому *пекстраинфо* может иметь **значение NULL**. В следующем коде показано, как протестировать элемент **VT** объекта Variant, который указывает тип данных, и отформатировать сообщение соответствующим образом.


```C++
if( pExtraInfo )    // Report extra information, if any. 
{                           
    printf("\tExtra info: ");
    if( pExtraInfo->vt == VT_BSTR )      // Extra info is a BSTR.
    {
        UINT len = SysStringLen(pExtraInfo->bstrVal);
        char *szExtra = new char[len];
        if (szExtra != NULL)
        {
            // Note - If the BSTR contains embedded NULL characters, this
            // will only pick up the first sub-string.
            WideCharToMultiByte(CP_ACP, 0, pExtraInfo->bstrVal, -1, 
                szExtra, len, 0, 0);
            printf("%s\n", szExtra);
            delete [] szExtra;
        }
    } 
    else if( pExtraInfo->vt == VT_I4 )   // Extra info is an integer.
        printf("%d\n", pExtraInfo->lVal);

    else if( pExtraInfo->vt == VT_R8 )   // Extra info is floating-point.
        printf("%f\n", pExtraInfo->dblVal);
}
```



> [!Note]  
> Не освобождайте вариант, на который указывает
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>pExtraInfo</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> . Кроме того, вариант станет недопустимым после возврата метода, поэтому не сослаться на него позже.

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Регистрация ошибок](logging-errors.md)
</dt> </dl>

 

 



