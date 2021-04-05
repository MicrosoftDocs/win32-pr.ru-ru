---
title: Обработка неизвестных ошибок
description: Обработка неизвестных ошибок
ms.assetid: d6a4cc60-8320-4b67-9f2e-7c4bea6c37fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8c3d9e70b89a9a78be62d2940ad8a69ac34c8f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068537"
---
# <a name="handling-unknown-errors"></a><span data-ttu-id="62524-103">Обработка неизвестных ошибок</span><span class="sxs-lookup"><span data-stu-id="62524-103">Handling Unknown Errors</span></span>

<span data-ttu-id="62524-104">Допускается возврат кода состояния только из реализации метода интерфейса, санкционированный на получение законных результатов.</span><span class="sxs-lookup"><span data-stu-id="62524-104">It is legal to return a status code only from the implementation of an interface method sanctioned as legally returnable.</span></span> <span data-ttu-id="62524-105">Несоблюдение этого правила дает возможность конфликта между возвращаемыми значениями кода ошибки и теми, которые санкционированы в приложении.</span><span class="sxs-lookup"><span data-stu-id="62524-105">Failure to observe this rule invites the possibility of conflict between returned error-code values and those sanctioned by the application.</span></span> <span data-ttu-id="62524-106">Обратите особое внимание на эту потенциальную проблему при распространении кодов ошибок из функций, которые вызываются внутренним образом.</span><span class="sxs-lookup"><span data-stu-id="62524-106">Pay particular attention to this potential problem when propagating error codes from functions that are called internally.</span></span>

<span data-ttu-id="62524-107">Приложения, вызывающие интерфейсы, должны обрабатывать все неизвестные возвращенные коды ошибок (в отличие от кода успешного выполнения) как синонима с \_ непредвиденным кодом E.</span><span class="sxs-lookup"><span data-stu-id="62524-107">Applications that call interfaces should treat any unknown returned error code (as opposed to a success code) as synonymous with E\_UNEXPECTED.</span></span> <span data-ttu-id="62524-108">Эта практика обработки неизвестных кодов ошибок необходима клиентам интерфейсов и функций, определяемых моделью COM.</span><span class="sxs-lookup"><span data-stu-id="62524-108">This practice of handling unknown error codes is required by clients of the COM-defined interfaces and functions.</span></span> <span data-ttu-id="62524-109">Поскольку типичная практика программирования заключается в подробной обработке нескольких специфических кодов ошибок и универсальности, это требование к обработке непредвиденных или неизвестных кодов ошибок легко.</span><span class="sxs-lookup"><span data-stu-id="62524-109">Because typical programming practice is to handle a few specific error codes in detail and treat the rest generically, this requirement of handling unexpected or unknown error codes is easily met.</span></span>

<span data-ttu-id="62524-110">При вызове метода интерфейса важно выполнять все возможные ошибки.</span><span class="sxs-lookup"><span data-stu-id="62524-110">It is important to handle all possible errors when calling an interface method.</span></span> <span data-ttu-id="62524-111">Невыполнение этого действия может привести к сбою приложения, повреждению данных или к уязвимости в системе безопасности.</span><span class="sxs-lookup"><span data-stu-id="62524-111">Failure to do so could cause your application to crash, to corrupt data, or to become vulnerable to security exploits.</span></span> <span data-ttu-id="62524-112">В следующем примере кода показан рекомендуемый способ обработки неизвестных ошибок.</span><span class="sxs-lookup"><span data-stu-id="62524-112">The following code sample shows the recommended way of handling unknown errors:</span></span>


```C++
HRESULT hr; 
hr = xxMethod(); 
 
switch (GetScode(hr))  
{ 
    case NOERROR: 
      // Method returned success. 
      break; 
 
    case x1: 
      // Handle error x1 here.
      break; 
 
    case x2: 
      // Handle error x2 here.
      break; 
 
    case E_UNEXPECTED: 
    default: 
      // Handle unexpected errors here. 
      break; 
} 
 
```



<span data-ttu-id="62524-113">Следующая проверка ошибок часто используется с теми подзадачами, которые не возвращают никаких специальных (кроме \_ "ОК" или непредвиденной ошибки).</span><span class="sxs-lookup"><span data-stu-id="62524-113">The following error check is often used with those routines that do not return anything special (other than S\_OK or some unexpected error):</span></span>


```C++
if (xxMethod() == NOERROR) 
{
    // Handle success here.
} 
else 
{
    // Handle failure here.
} 
```



## <a name="related-topics"></a><span data-ttu-id="62524-114">См. также</span><span class="sxs-lookup"><span data-stu-id="62524-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62524-115">Обработка ошибок в COM</span><span class="sxs-lookup"><span data-stu-id="62524-115">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

 




