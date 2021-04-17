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
# <a name="implementing-iamerrorlog"></a><span data-ttu-id="3671d-103">Реализация Иамеррорлог</span><span class="sxs-lookup"><span data-stu-id="3671d-103">Implementing IAMErrorLog</span></span>

<span data-ttu-id="3671d-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="3671d-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="3671d-105">Интерфейс [**иамеррорлог**](iamerrorlog.md) содержит один метод [**LogError**](iamerrorlog-logerror.md).</span><span class="sxs-lookup"><span data-stu-id="3671d-105">The [**IAMErrorLog**](iamerrorlog.md) interface contains a single method, [**LogError**](iamerrorlog-logerror.md).</span></span> <span data-ttu-id="3671d-106">Параметры метода содержат сведения о произошедшей ошибке.</span><span class="sxs-lookup"><span data-stu-id="3671d-106">The parameters to the method contain information about the error that occurred.</span></span>


```C++
STDMETHODIMP LogError(
    LONG Severity,          // Reserved. Do not use.
    BSTR ErrorString,       // Description.
    LONG ErrorCode,         // Error code.
    HRESULT hresult,        // HRESULT that caused the error.
    VARIANT *pExtraInfo);   // Extra information about the error.
```



<span data-ttu-id="3671d-107">Код ошибки и строка ошибки определяются службами редактирования DirectShow.</span><span class="sxs-lookup"><span data-stu-id="3671d-107">The error code and the error string are defined by DirectShow Editing Services.</span></span> <span data-ttu-id="3671d-108">Список ошибок см. в разделе [ошибки отрисовки](rendering-errors.md).</span><span class="sxs-lookup"><span data-stu-id="3671d-108">For a list of errors, see [Rendering Errors](rendering-errors.md).</span></span>

<span data-ttu-id="3671d-109">Параметр *пекстраинфо* содержит указатель на тип Variant, содержащий дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="3671d-109">The *pExtraInfo* parameter contains a pointer to a VARIANT type that holds additional information about the error.</span></span> <span data-ttu-id="3671d-110">Тип данных и содержимое варианта зависит от конкретной произошедшей ошибки.</span><span class="sxs-lookup"><span data-stu-id="3671d-110">The data type and contents of the VARIANT depend on the specific error that occurred.</span></span> <span data-ttu-id="3671d-111">Например, если ошибка вызвана неправильным именем файла, то вариант представляет собой строку с неправильным именем файла.</span><span class="sxs-lookup"><span data-stu-id="3671d-111">For example, if the error was caused by an incorrect file name, the VARIANT is a string with the bad file name.</span></span> <span data-ttu-id="3671d-112">Некоторые ошибки не имеют дополнительной информации, поэтому *пекстраинфо* может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="3671d-112">Some errors do not have extra information, so *pExtraInfo* might be **NULL**.</span></span> <span data-ttu-id="3671d-113">В следующем коде показано, как протестировать элемент **VT** объекта Variant, который указывает тип данных, и отформатировать сообщение соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="3671d-113">The following code shows how to test the **vt** member of the VARIANT, which indicates the data type, and format a message accordingly.</span></span>


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
> <span data-ttu-id="3671d-114">Не освобождайте вариант, на который указывает</span><span class="sxs-lookup"><span data-stu-id="3671d-114">Do not free the VARIANT pointed to by</span></span>
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
> <span data-ttu-id="3671d-115">.</span><span class="sxs-lookup"><span data-stu-id="3671d-115">.</span></span> <span data-ttu-id="3671d-116">Кроме того, вариант станет недопустимым после возврата метода, поэтому не сослаться на него позже.</span><span class="sxs-lookup"><span data-stu-id="3671d-116">Also, the VARIANT becomes invalid after the method returns, so do not reference it later.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3671d-117">См. также</span><span class="sxs-lookup"><span data-stu-id="3671d-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3671d-118">Регистрация ошибок</span><span class="sxs-lookup"><span data-stu-id="3671d-118">Logging Errors</span></span>](logging-errors.md)
</dt> </dl>

 

 



