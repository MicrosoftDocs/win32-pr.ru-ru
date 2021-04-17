---
description: Вычисляет выражение и отображает диагностическое сообщение, если выражение имеет значение FALSE. Игнорируется в розничных сборках.
ms.assetid: 8c3815bb-3164-4066-a947-974e791af5cd
title: Макрос ASSERT (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 8617d1c86f655cc9b44ea6619931f73888ae2a67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675539"
---
# <a name="assert-macro"></a><span data-ttu-id="670af-104">ASSERT - макрос</span><span class="sxs-lookup"><span data-stu-id="670af-104">ASSERT macro</span></span>

<span data-ttu-id="670af-105">Вычисляет выражение и отображает диагностическое сообщение, если выражение имеет **значение false**.</span><span class="sxs-lookup"><span data-stu-id="670af-105">Evaluates an expression, and displays a diagnostic message if the expression is **FALSE**.</span></span> <span data-ttu-id="670af-106">Игнорируется в розничных сборках.</span><span class="sxs-lookup"><span data-stu-id="670af-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="670af-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="670af-107">Syntax</span></span>


```C++
void ASSERT(
   BOOL cond
);
```



## <a name="parameters"></a><span data-ttu-id="670af-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="670af-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="670af-109">*cond*</span><span class="sxs-lookup"><span data-stu-id="670af-109">*cond*</span></span> 
</dt> <dd>

<span data-ttu-id="670af-110">Вычисляемое выражение.</span><span class="sxs-lookup"><span data-stu-id="670af-110">Expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="670af-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="670af-111">Return value</span></span>

<span data-ttu-id="670af-112">Этот макрос не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="670af-112">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="670af-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="670af-113">Remarks</span></span>

<span data-ttu-id="670af-114">Если в отладочных сборках выражение имеет **значение false**, этот макрос отображает окно сообщения с текстом выражения, именем исходного файла и номером строки.</span><span class="sxs-lookup"><span data-stu-id="670af-114">In debug builds, if the expression is **FALSE**, this macro displays a message box with the text of the expression, the name of the source file, and the line number.</span></span> <span data-ttu-id="670af-115">Пользователь может игнорировать утверждение, ввести отладчик или выйти из приложения.</span><span class="sxs-lookup"><span data-stu-id="670af-115">The user can ignore the assertion, enter the debugger, or quit the application.</span></span>

## <a name="examples"></a><span data-ttu-id="670af-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="670af-116">Examples</span></span>


```
ASSERT(rtStartTime <= rtEndTime);
```



## <a name="requirements"></a><span data-ttu-id="670af-117">Требования</span><span class="sxs-lookup"><span data-stu-id="670af-117">Requirements</span></span>



| <span data-ttu-id="670af-118">Требование</span><span class="sxs-lookup"><span data-stu-id="670af-118">Requirement</span></span> | <span data-ttu-id="670af-119">Значение</span><span class="sxs-lookup"><span data-stu-id="670af-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="670af-120">Header</span><span class="sxs-lookup"><span data-stu-id="670af-120">Header</span></span><br/> | <dl> <span data-ttu-id="670af-121"><dt>Вксдебуг. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="670af-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="670af-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="670af-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="670af-123">Макросы Assert и точка останова</span><span class="sxs-lookup"><span data-stu-id="670af-123">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




