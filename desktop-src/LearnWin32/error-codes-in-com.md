---
title: Коды ошибок в COM
description: .
ms.assetid: ed430863-f416-4611-81b4-0c31d819944a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f082afbabf367179b02c0fb3b0fc979dcda664a4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790189"
---
# <a name="error-codes-in-com"></a><span data-ttu-id="ca2d1-103">Коды ошибок в COM</span><span class="sxs-lookup"><span data-stu-id="ca2d1-103">Error Codes in COM</span></span>

<span data-ttu-id="ca2d1-104">Чтобы указать на успех или неудачу, методы и функции COM возвращают значение типа **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ca2d1-104">To indicate success or failure, COM methods and functions return a value of type **HRESULT**.</span></span> <span data-ttu-id="ca2d1-105">**HRESULT** — это 32-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="ca2d1-105">An **HRESULT** is a 32-bit integer.</span></span> <span data-ttu-id="ca2d1-106">Старший бит успешных или неудачных сигналов **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ca2d1-106">The high-order bit of the **HRESULT** signals success or failure.</span></span> <span data-ttu-id="ca2d1-107">Ноль (0) указывает на успешное выполнение, а 1 — на сбой.</span><span class="sxs-lookup"><span data-stu-id="ca2d1-107">Zero (0) indicates success and 1 indicates failure.</span></span>

<span data-ttu-id="ca2d1-108">При этом создаются следующие числовые диапазоны:</span><span class="sxs-lookup"><span data-stu-id="ca2d1-108">This produces the following numeric ranges:</span></span>

-   <span data-ttu-id="ca2d1-109">Коды успеха: 0x0 – 0x7FFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="ca2d1-109">Success codes: 0x0–0x7FFFFFFF.</span></span>
-   <span data-ttu-id="ca2d1-110">Коды ошибок: 0x80000000 – 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="ca2d1-110">Error codes: 0x80000000–0xFFFFFFFF.</span></span>

<span data-ttu-id="ca2d1-111">Небольшое количество методов COM не возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ca2d1-111">A small number of COM methods do not return an **HRESULT** value.</span></span> <span data-ttu-id="ca2d1-112">Например, методы [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) и [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) возвращают неподписанные длинные значения.</span><span class="sxs-lookup"><span data-stu-id="ca2d1-112">For example, the [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) methods return unsigned long values.</span></span> <span data-ttu-id="ca2d1-113">Но каждый COM-метод, который возвращает код ошибки, делает это, возвращая значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ca2d1-113">But every COM method that returns an error code does so by returning an **HRESULT** value.</span></span>

<span data-ttu-id="ca2d1-114">Чтобы проверить, завершился ли метод COM, проверьте старший бит возвращенного **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ca2d1-114">To check whether a COM method succeeds, examine the high-order bit of the returned **HRESULT**.</span></span> <span data-ttu-id="ca2d1-115">Заголовки Windows SDK предоставляют два макроса, которые упрощают выполнение следующих действий: макрос « [**успешно**](/windows/desktop/api/winerror/nf-winerror-succeeded) » и [**сбой**](/windows/desktop/api/winerror/nf-winerror-failed) макроса.</span><span class="sxs-lookup"><span data-stu-id="ca2d1-115">The Windows SDK headers provide two macros that make this easier: the [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) macro and the [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macro.</span></span> <span data-ttu-id="ca2d1-116">Макрос  Success возвращает **значение true** , если **HRESULT** является кодом успешного выполнения, и **false** , если это код ошибки.</span><span class="sxs-lookup"><span data-stu-id="ca2d1-116">The **SUCCEEDED** macro returns **TRUE** if an **HRESULT** is a success code and **FALSE** if it is an error code.</span></span> <span data-ttu-id="ca2d1-117">В следующем примере проверяется успешность завершения [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) .</span><span class="sxs-lookup"><span data-stu-id="ca2d1-117">The following example checks whether [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) succeeds.</span></span>


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
    COINIT_DISABLE_OLE1DDE);

if (SUCCEEDED(hr))
{
    // The function succeeded.
}
else
{
    // Handle the error.
}
```



<span data-ttu-id="ca2d1-118">Иногда удобнее протестировать обратное условие.</span><span class="sxs-lookup"><span data-stu-id="ca2d1-118">Sometimes it is more convenient to test the inverse condition.</span></span> <span data-ttu-id="ca2d1-119">[**Невыполненный**](/windows/desktop/api/winerror/nf-winerror-failed) макрос выполняет противоположный [**результат.**](/windows/desktop/api/winerror/nf-winerror-succeeded)</span><span class="sxs-lookup"><span data-stu-id="ca2d1-119">The [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macro does the opposite of [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded).</span></span> <span data-ttu-id="ca2d1-120">Он возвращает **значение true** для кода ошибки и **значение false** для кода успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="ca2d1-120">It returns **TRUE** for an error code and **FALSE** for a success code.</span></span>


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
    COINIT_DISABLE_OLE1DDE);

if (FAILED(hr))
{
    // Handle the error.
}
else
{
    // The function succeeded.
}
```



<span data-ttu-id="ca2d1-121">Далее в этом модуле мы рассмотрим некоторые практические советы по структурированию кода для устранения ошибок COM.</span><span class="sxs-lookup"><span data-stu-id="ca2d1-121">Later in this module, we will look at some practical advice for how to structure your code to handle COM errors.</span></span> <span data-ttu-id="ca2d1-122">(См. раздел [Обработка ошибок в com](error-handling-in-com.md).)</span><span class="sxs-lookup"><span data-stu-id="ca2d1-122">(See [Error Handling in COM](error-handling-in-com.md).)</span></span>

## <a name="next"></a><span data-ttu-id="ca2d1-123">Следующая</span><span class="sxs-lookup"><span data-stu-id="ca2d1-123">Next</span></span>

[<span data-ttu-id="ca2d1-124">Создание объекта в COM</span><span class="sxs-lookup"><span data-stu-id="ca2d1-124">Creating an Object in COM</span></span>](creating-an-object-in-com.md)

 

 