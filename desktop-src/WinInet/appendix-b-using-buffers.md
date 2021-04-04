---
title: Использование буферов строк
description: Функции, возвращающие строки, содержат входной параметр, Лпсзбуффер и параметр size, Лпдвбуфферленгс. Хотя Лпсзбуффер может иметь значение NULL, Лпдвбуфферленгс должен быть допустимым указателем на переменную типа DWORD.
ms.assetid: ae7f84ba-15d4-483b-bdda-0042854f9e1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 309d887458521b99069b381f8bf6650ebeda488a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792721"
---
# <a name="using-string-buffers"></a><span data-ttu-id="53f3a-104">Использование буферов строк</span><span class="sxs-lookup"><span data-stu-id="53f3a-104">Using String Buffers</span></span>

<span data-ttu-id="53f3a-105">Функции, возвращающие строки, содержат входной параметр, *лпсзбуффер* и параметр size, *лпдвбуфферленгс*.</span><span class="sxs-lookup"><span data-stu-id="53f3a-105">Functions that return strings contain an input parameter, *lpszBuffer*, and a size parameter, *lpdwBufferLength*.</span></span> <span data-ttu-id="53f3a-106">Хотя *лпсзбуффер* может иметь **значение NULL**, *лпдвбуфферленгс* должен быть допустимым указателем на переменную **типа DWORD** .</span><span class="sxs-lookup"><span data-stu-id="53f3a-106">Although *lpszBuffer* can be **NULL**, *lpdwBufferLength* must be a valid pointer to a **DWORD** variable.</span></span> <span data-ttu-id="53f3a-107">Если входной буфер, на который указывает *лпсзбуффер* , имеет **значение NULL** или слишком мал для хранения выходной строки, функция завершается ошибкой, а [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает **ошибку, \_ недостаточную для \_ буфера**.</span><span class="sxs-lookup"><span data-stu-id="53f3a-107">If the input buffer pointed to by *lpszBuffer* is **NULL** or too small to hold the output string, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_INSUFFICIENT\_BUFFER**.</span></span> <span data-ttu-id="53f3a-108">Переменная, на которую указывает *лпдвбуфферленгс* , содержит число, представляющее число байтов, необходимых функции для возврата запрошенной строки, включая завершающий символ **null** .</span><span class="sxs-lookup"><span data-stu-id="53f3a-108">The variable pointed to by *lpdwBufferLength* contains a number that represents the number of bytes the function requires to return the requested string, including the **null** terminator.</span></span> <span data-ttu-id="53f3a-109">Приложение должно выделить буфер такого размера, установить переменную, на которую указывает *лпдвбуфферленгс* , в это значение и повторно отправить запрос.</span><span class="sxs-lookup"><span data-stu-id="53f3a-109">The application should allocate a buffer of this size, set the variable pointed to by *lpdwBufferLength* to this value, and resubmit the request.</span></span> <span data-ttu-id="53f3a-110">Если размер буфера достаточно для получения запрошенной строки, строка копируется в выходной буфер с **нулевым** символом конца строки, а функция возвращает признак успеха.</span><span class="sxs-lookup"><span data-stu-id="53f3a-110">If the buffer size is sufficient to receive the requested string, the string is copied to the output buffer with a **null** terminator and the function returns a success indication.</span></span> <span data-ttu-id="53f3a-111">Переменная, на которую указывает *лпдвбуфферленгс* , теперь содержит количество символов, хранящихся в буфере, за исключением терминатора **null** .</span><span class="sxs-lookup"><span data-stu-id="53f3a-111">The variable pointed to by *lpdwBufferLength* now contains the number of characters stored in the buffer, excluding the **null** terminator.</span></span>

> [!Note]  
> <span data-ttu-id="53f3a-112">WinINet не поддерживает реализации серверов.</span><span class="sxs-lookup"><span data-stu-id="53f3a-112">WinINet does not support server implementations.</span></span> <span data-ttu-id="53f3a-113">Кроме того, его не следует использовать из службы.</span><span class="sxs-lookup"><span data-stu-id="53f3a-113">In addition, it should not be used from a service.</span></span> <span data-ttu-id="53f3a-114">Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="53f3a-114">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 