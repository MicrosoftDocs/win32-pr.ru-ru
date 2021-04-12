---
description: Макросы Assert и точка останова
ms.assetid: c34db182-1f65-4a2f-9534-268638c2502d
title: Макросы Assert и точка останова
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4771fb7e302ec9e1093fca82d7842212e0b68e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140551"
---
# <a name="assert-and-breakpoint-macros"></a><span data-ttu-id="983c6-103">Макросы Assert и точка останова</span><span class="sxs-lookup"><span data-stu-id="983c6-103">Assert and Breakpoint Macros</span></span>

<span data-ttu-id="983c6-104">[Базовые классы DirectShow](directshow-base-classes.md) предоставляют несколько макросов, выполняющих утверждения или вызывающие точки останова.</span><span class="sxs-lookup"><span data-stu-id="983c6-104">The [DirectShow Base Classes](directshow-base-classes.md) provide several macros that perform asserts or cause breakpoints.</span></span>



| <span data-ttu-id="983c6-105">Макрос</span><span class="sxs-lookup"><span data-stu-id="983c6-105">Macro</span></span>                                        | <span data-ttu-id="983c6-106">Описание</span><span class="sxs-lookup"><span data-stu-id="983c6-106">Description</span></span>                                                                                                                        |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="983c6-107">**УТВЕРЖДАЮЩЕ**</span><span class="sxs-lookup"><span data-stu-id="983c6-107">**ASSERT**</span></span>](assert.md)                     | <span data-ttu-id="983c6-108">Вычисляет выражение и отображает диагностическое сообщение, если выражение имеет **значение false**.</span><span class="sxs-lookup"><span data-stu-id="983c6-108">Evaluates an expression, and displays a diagnostic message if the expression is **FALSE**.</span></span>                                         |
| [<span data-ttu-id="983c6-109">**дбгассерталигнед**</span><span class="sxs-lookup"><span data-stu-id="983c6-109">**DbgAssertAligned**</span></span>](dbgassertaligned.md) | <span data-ttu-id="983c6-110">Проверяет, соответствует ли указатель заданной границе.</span><span class="sxs-lookup"><span data-stu-id="983c6-110">Tests whether a pointer is aligned to a specified boundary.</span></span>                                                                        |
| [<span data-ttu-id="983c6-111">**дбгбреак**</span><span class="sxs-lookup"><span data-stu-id="983c6-111">**DbgBreak**</span></span>](dbgbreak.md)                 | <span data-ttu-id="983c6-112">Отображает окно сообщения с указанной строкой, именем исходного файла и номером строки.</span><span class="sxs-lookup"><span data-stu-id="983c6-112">Displays a message box with the specified string, the name of the source file, and the line number.</span></span>                                |
| [<span data-ttu-id="983c6-113">**ВЫПОЛНИТЬ \_ Assert**</span><span class="sxs-lookup"><span data-stu-id="983c6-113">**EXECUTE\_ASSERT**</span></span>](execute-assert.md)    | <span data-ttu-id="983c6-114">Вычисляет выражение в сборках Debug и Retail.</span><span class="sxs-lookup"><span data-stu-id="983c6-114">Evaluates an expression in debug and retail builds.</span></span> <span data-ttu-id="983c6-115">В отладочных сборках отображает диагностическое сообщение, если выражение имеет **значение false**.</span><span class="sxs-lookup"><span data-stu-id="983c6-115">In debug builds, displays a diagnostic message if the expression is **FALSE**.</span></span> |
| [<span data-ttu-id="983c6-116">**кассерт**</span><span class="sxs-lookup"><span data-stu-id="983c6-116">**KASSERT**</span></span>](kassert.md)                   | <span data-ttu-id="983c6-117">Вычисляет выражение и вызывает исключение точки останова, если выражение имеет **значение false**.</span><span class="sxs-lookup"><span data-stu-id="983c6-117">Evaluates an expression, and causes a breakpoint exception if the expression is **FALSE**.</span></span>                                         |
| [<span data-ttu-id="983c6-118">**кдбгбреак**</span><span class="sxs-lookup"><span data-stu-id="983c6-118">**KDbgBreak**</span></span>](kdbgbreak.md)               | <span data-ttu-id="983c6-119">Вызывает исключение точки останова и записывает в журнал указанную строку.</span><span class="sxs-lookup"><span data-stu-id="983c6-119">Causes a breakpoint exception, and logs the specified string.</span></span>                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="983c6-120">См. также</span><span class="sxs-lookup"><span data-stu-id="983c6-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="983c6-121">Отладка служебных программ</span><span class="sxs-lookup"><span data-stu-id="983c6-121">Debugging Utilities</span></span>](debugging-utilities.md)
</dt> </dl>

 

 



