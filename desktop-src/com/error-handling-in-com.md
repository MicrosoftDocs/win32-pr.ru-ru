---
title: Обработка ошибок в COM (COM)
description: Обработка ошибок в COM
ms.assetid: 15f3ae3e-1794-4948-a7aa-6309a703364b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19af496eabf50833c99d462ff074254bc39bb7a0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488901"
---
# <a name="error-handling-in-com-com"></a><span data-ttu-id="0c1b7-103">Обработка ошибок в COM (COM)</span><span class="sxs-lookup"><span data-stu-id="0c1b7-103">Error Handling in COM (COM)</span></span>

<span data-ttu-id="0c1b7-104">Почти все COM-функции и методы интерфейса возвращают значение типа **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0c1b7-104">Almost all COM functions and interface methods return a value of the type **HRESULT**.</span></span> <span data-ttu-id="0c1b7-105">**HRESULT** (для *результирующего маркера*) — это способ возвращения значений успеха, предупреждения и ошибки.</span><span class="sxs-lookup"><span data-stu-id="0c1b7-105">The **HRESULT** (for *result handle*) is a way of returning success, warning, and error values.</span></span> <span data-ttu-id="0c1b7-106">**Значения HRESULT** в действительности не обрабатывают ничего; они являются только значениями с несколькими полями, закодированными в значении.</span><span class="sxs-lookup"><span data-stu-id="0c1b7-106">**HRESULT** s are really not handles to anything; they are only values with several fields encoded in the value.</span></span> <span data-ttu-id="0c1b7-107">Как и в случае со спецификацией COM, результатом нулевого результата является Success и ненулевое значение указывает на сбой.</span><span class="sxs-lookup"><span data-stu-id="0c1b7-107">As per the COM specification, a result of zero indicates success and a nonzero result indicates failure.</span></span>

<span data-ttu-id="0c1b7-108">На уровне исходного кода все значения ошибок состоят из трех частей, разделенных символами подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="0c1b7-108">At the source code level, all error values consist of three parts, separated by underscores.</span></span> <span data-ttu-id="0c1b7-109">Первая часть — это префикс, определяющий средство, связанное с ошибкой, вторая часть — E для ошибки, а третья часть — строка, описывающая фактическое условие.</span><span class="sxs-lookup"><span data-stu-id="0c1b7-109">The first part is the prefix that identifies the facility associated with the error, the second part is E for error, and the third part is a string that describes the actual condition.</span></span> <span data-ttu-id="0c1b7-110">Например, **STG \_ E \_ медиумфулл** возвращается, если на жестком диске не осталось места.</span><span class="sxs-lookup"><span data-stu-id="0c1b7-110">For example, **STG\_E\_MEDIUMFULL** is returned when there is no space left on a hard disk.</span></span> <span data-ttu-id="0c1b7-111">Префикс **STG** указывает на хранилище, а значение **E** указывает на то, что код состояния представляет ошибку, а **медиумфулл** предоставляет конкретные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="0c1b7-111">The **STG** prefix indicates the storage facility, the **E** indicates that the status code represents an error, and the **MEDIUMFULL** provides specific information about the error.</span></span> <span data-ttu-id="0c1b7-112">Многие из значений, которые могут быть возвращены из метода или функции интерфейса, определены в файле Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="0c1b7-112">Many of the values that you might want to return from an interface method or function are defined in Winerror.h.</span></span>

<span data-ttu-id="0c1b7-113">Дополнительные сведения об обработке ошибок см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="0c1b7-113">For more information about error handling, see the following sections:</span></span>

-   [<span data-ttu-id="0c1b7-114">Структура кодов ошибок COM</span><span class="sxs-lookup"><span data-stu-id="0c1b7-114">Structure of COM Error Codes</span></span>](structure-of-com-error-codes.md)
-   [<span data-ttu-id="0c1b7-115">Коды в СРЕДСТВе \_ ИТФ</span><span class="sxs-lookup"><span data-stu-id="0c1b7-115">Codes in FACILITY\_ITF</span></span>](codes-in-facility-itf.md)
-   [<span data-ttu-id="0c1b7-116">Использование макросов для обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="0c1b7-116">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)
-   [<span data-ttu-id="0c1b7-117">Обработка ошибок COM в Java и Visual Basic</span><span class="sxs-lookup"><span data-stu-id="0c1b7-117">COM Error Handling in Java and Visual Basic</span></span>](com-error-handling-in-java-and-visual-basic.md)
-   [<span data-ttu-id="0c1b7-118">Стратегии обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="0c1b7-118">Error Handling Strategies</span></span>](error-handling-strategies.md)
-   [<span data-ttu-id="0c1b7-119">Обработка неизвестных ошибок</span><span class="sxs-lookup"><span data-stu-id="0c1b7-119">Handling Unknown Errors</span></span>](handling-unknown-errors.md)

## <a name="related-topics"></a><span data-ttu-id="0c1b7-120">См. также</span><span class="sxs-lookup"><span data-stu-id="0c1b7-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c1b7-121">Коды ошибок COM</span><span class="sxs-lookup"><span data-stu-id="0c1b7-121">COM Error Codes</span></span>](com-error-codes.md)
</dt> </dl>

 

 




